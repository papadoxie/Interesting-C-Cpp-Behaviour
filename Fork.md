# Fork

## Forking After Making Threads
Parent thread information is inherited by the child but the threads do not work
Information modified by the threads remains
No cleanup

### Mitigation
	pthread_at_fork()