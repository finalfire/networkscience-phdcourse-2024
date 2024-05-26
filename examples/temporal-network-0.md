### Temporal Network

Consider a temporal network with three nodes: \( A \), \( B \), and \( C \). The network evolves over time, and we have the following information exchange times:

- **Node \( B \) sends information to node \( A \) at times: \( t = 2 \), \( t = 5 \), and \( t = 7 \)**.
- **Node \( C \) sends information to node \( A \) at times: \( t = 4 \) and \( t = 8 \)**.

### Example

Let's look at node \( A \) at time \( t = 10 \):

1. **Node \( A \) at time \( t = 10 \)**:
    - We need to determine \( \phi_{A,10}(B) \) and \( \phi_{A,10}(C) \).

2. **Latest Information Times**:
    - The latest time before \( t = 10 \) that node \( B \)'s information could have reached \( A \) is \( t = 7 \). Hence, \( \phi_{A,10}(B) = 7 \).
    - Similarly, the latest time before \( t = 10 \) that node \( C \)'s information could have reached \( A \) is \( t = 8 \). Hence, \( \phi_{A,10}(C) = 8 \).

3. **Latencies**:
    - The latency of \( B \) with respect to \( A \) at time \( t = 10 \) is \( \lambda_{A,10}(B) = 10 - 7 = 3 \).
    - The latency of \( C \) with respect to \( A \) at time \( t = 10 \) is \( \lambda_{A,10}(C) = 10 - 8 = 2 \).

4. **Vector Clock**:
    - Node \( A \)'s vector clock at time \( t = 10 \) is \( [\phi_{A,10}(A), \phi_{A,10}(B), \phi_{A,10}(C)] \).
    - Assuming node \( A \)'s own latest information is available up to time \( t = 10 \), we have \( \phi_{A,10}(A) = 10 \).
    - Therefore, the vector clock for node \( A \) is \( [10, 7, 8] \).

In this example, the vector clock \( [10, 7, 8] \) for node \( A \) at time \( t = 10 \) captures the partial ordering of events and the latest times information from nodes \( A \), \( B \), and \( C \) has reached node \( A \). The latencies \( \lambda_{A,10}(B) = 3 \) and \( \lambda_{A,10}(C) = 2 \) represent how old the information from nodes \( B \) and \( C \) is, respectively, for node \( A \) at time \( t = 10 \).