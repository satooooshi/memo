- arguments (pointer & reference)
```
yfs_client::write(inum ino, size_t size, off_t off, const char *data,
        size_t &bytes_written)

```

*dataはupper関数から受け取りたいとき
&bytes_writtenはupper関数に渡したいとき


- pthread mutex lock

```
pthread_mutex_t count_lock; //二つの異なるスレッドが同時に一つの mutex を保有することはない
pthread_cond_t count_nonzero;   //cv が指す条件変数で呼び出しスレッドをブロック
unsigned count;
decrement_count()
{
    pthread_mutex_lock(&count_lock);
    while (count == 0)  //condition条件
        pthread_cond_wait(&count_nonzero, &count_lock);
    count = count - 1;
    pthread_mutex_unlock(&count_lock);
}
increment_count()
{
    pthread_mutex_lock(&count_lock);
    if (count == 0)
        pthread_cond_signal(&count_nonzero);
    count = count + 1;
    pthread_mutex_unlock(&count_lock);
}

```