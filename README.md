# Distributed System

# Main focus when designing 

1. **Fault Tolerance**
    - *Availibility:*  Can be achieved using replication
    - *Recoverability*: Can be achieved using logging/transaction, durable storage etc.

2. **Consistency**
    > Does get() returns latest put()?
    - *Strong consistency*
    - *Weak consistency*
    - *Eventual Consistency*

3. **Performance**
    - *Scalable throughput*
    - *Lower latency*

# Problems

### Map Reduce
 > https://pdos.csail.mit.edu/6.824/papers/mapreduce.pdf

**Fault Tolernace aspects**
- Co-ordinator re-runs map/redue function if worker node fails
- Map/Reduce functions are functional/determenistic and can be run more than once
- Other fail points
    - Can co-ordinator fails? NO
    - Slow workers(Stagglers)? Co-ordinator can run backup tasks and assigned to other worker node  