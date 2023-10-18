# BufferDesc

Helper struct for [BufferPool](../Memory/BufferPool.md). 

## **Fields**:
### **buffer**
: The actual reference to the stored byte array. 
### **released**
: When the buffer is put back to the pool. Based on this value the pool will calculate the age of the buffer. 