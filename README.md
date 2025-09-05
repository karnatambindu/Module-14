# Exp.No:36 APPLICATIONS OF QUEUE

# AIM
To write a Python program to implement CPU Process Scheduling using a queue.

# ALGORITHM
Start the program.
Define the function CalculateWaitingTime(at, bt, N).

Initialize a list wt of size N with all values set to 0.

Set wt[0] = 0 for the first process.

Print the table header: "P.No.", "Arrival Time", "Burst Time", "Waiting Time".

Print the values for the first process.

For each process from index 1 to N-1:

Calculate wt[i] = (at[i - 1] + bt[i - 1] + wt[i - 1]) - at[i].

Print the process number, arrival time, burst time, and waiting time.

Initialize total_waiting_time = 0.

Add up all waiting times.

Calculate average waiting time as average = total_waiting_time / N.
Print the average waiting time.

Get burst times as input from the user for 5 processes.
Call CalculateWaitingTime() with at, bt, and N.

End the program.
# PROGRAM
```
	# first process is 0
	wt[0] = 0

	# calculating waiting time
	for i in range(1, n ):
		wt[i] = bt[i - 1] + wt[i - 1]

# Function to calculate turn
# around time
def findTurnAroundTime(processes, n,
					bt, wt, tat):

	# calculating turnaround
	# time by adding bt[i] + wt[i]
	for i in range(n):
		tat[i] = bt[i] + wt[i]

# Function to calculate
# average time
def findavgTime( processes, n, bt):

	wt = [0] * n
	tat = [0] * n
	total_wt = 0
	total_tat = 0

	# Function to find waiting
	# time of all processes
	findWaitingTime(processes, n, bt, wt)

	# Function to find turn around
	# time for all processes
	findTurnAroundTime(processes, n,
					bt, wt, tat)

	# Display processes along
	# with all details
	print( "Processes Burst time " +
				" Waiting time " +
				" Turn around time")

	# Calculate total waiting time
	# and total turn around time
	for i in range(n):
	    total_wt=total_wt+wt[i]
	    total_tat=total_tat+tat[i]
	for i in range(n):
	    print(" "+ str(i+1)  +"   "+str(bt[i])+"  "+str(wt[i])+"    "+str(tat[i]))
	
	print( "Average waiting time = "+
				str(total_wt / n))
	print("Average turn around time = "+
					str(total_tat / n))

# Driver code
if __name__ =="__main__":
	
	# process id's
	processes = [ 1, 2, 3]
	n = len(processes)

	# Burst time of all processes
	t0=int(input())
	t1=int(input())
	t2=int(input())
	burst_time = [t0,t1,t2]

	findavgTime(processes, n, burst_time)
```
# OUTPUT 
<img width="1189" height="489" alt="Screenshot 2025-09-05 230815" src="https://github.com/user-attachments/assets/a9898935-9c0c-417f-9ca7-7dc44ae39585" />

# RESULT
Thus the Python program to implement CPU Process Scheduling using a queue has been implemented and executed successfully.

# Exp No: 37 Circular Queue

# AIM
To write a Python program with a function to insert float values into a Circular Queue.

# ALGORITHM
Start
1. Check if the Circular Queue is full

2 If size == max_size, print "Queue is full" and exit the function

3 If the queue is not full:

4 Read the element to be inserted

5 Convert it to float

6 Insert the element at the tail position

7 Update tail using: tail = (tail + 1) % max_size (circular increment)
8 Increment size by 1

End
# PROGRAM
```
class Queue: def init(self, size): self.items = [0] * size self.max_size = size self.head, self.tail, self.size = 0, 0, 0

def enqueue(self, item):
    if self.is_list_full():
        self.size==0
        print("Queue is full")
        return
    self.items[self.tail]=item
    self.tail=(self.tail+1)%self.max_size
    self.size+=1
        
def dequeue(self):
    item=self.items[self.head]
    self.head=(self.head+1)%self.max_size
    self.size-=1
    return item
def is_list_full(self):
    if self.size==self.max_size:
        return True
    return False
    

def is_empty(self):
    if self.size==0:
        return True
    return False
size=int(input()) a=Queue(size) str=float(input()) str1=float(input()) str2=float(input()) a.enqueue(str) a.enqueue(str1) a.enqueue(str2) print(a.items)
```
# OUTPUT
<img width="645" height="384" alt="Screenshot 2025-09-05 231142" src="https://github.com/user-attachments/assets/f1418f99-b255-4d4b-be02-d36e07ae1545" />

# RESULT
Thus the Python program with a function to insert float values into a Circular Queue has been implemented and executed successfully

# Exp.No:38 DEQUE - INSERTION
# AIM
To write a Python program to insert elements at REAR END of deque using a collection built-in function.

# ALGORITHM

Import the deque class from the collections module.
Initialize an empty deque.

Start an infinite loop using while True.
In each iteration, take input from the user.

If the input is an empty string, break the loop.
If the input is not empty, convert it to an integer and append it to the deque.

After the loop ends, append the values 14 and 15 to the deque.
Print the message "The deque after appending at right is :".

Print the contents of the deque.
# PROGRAM
```
import collections
n1=int(input())
n2=int(input())
n3=int(input())
de=collections.deque([n1,n2,n3])
de.append(14)
de.append(15)
print("The deque after appending at right is :")
print(de)
```
# OUTPUT
<img width="1207" height="336" alt="Screenshot 2025-09-05 231635" src="https://github.com/user-attachments/assets/38784b73-2c29-46b3-b447-43d2e3c0a2d3" />

# RESULT
Thus the Python program to insert elements at REAR END of deque using a collection built-in function has been implemented and executed successfully.

# Exp.No:39 Deque - DELETION
# AIM
To write a Python program to delete elements at FRONT END of deque using a collection built-in function.

# ALGORITHM

Import the deque class from the collections module.
Create an empty deque.

Define how many elements to input (e.g., 3 inputs as in the example).
Loop through the range of input size:

Read an integer from the user.
Append the integer to the deque.

Remove the front element of the deque using popleft().
Print the final deque after deletion.
# PROGRAM
```
import collections
  
n1=int(input())
n2=int(input())
n3=int(input())
# initializing deque
de = collections.deque([n1,n2,n3])
de.popleft()
# printing modified deque
print ("The deque after deleting is : ")
print (de)
```
# OUTPUT
<img width="1182" height="338" alt="Screenshot 2025-09-05 231932" src="https://github.com/user-attachments/assets/2de3222a-9769-43f1-92cc-fd369a60f2b7" />

# RESULT
Thus the Python program to delete elements at FRONT END of deque using a collection built-in function has been implemented and executed successfully.

# Exp.No:40 PRIORITY QUEUE
# AIM
To write a Python program for simple implementation of Priority Queue using Queue.

# ALGORITHM
Start the program.
Define a class PriorityQueue with an initializer to create an empty list queue.

Define the __str__ method to return queue elements as a string separated by spaces.

Define the isEmpty() method to check if the queue is empty.
Define the insert(data) method to append the given data to the queue.

Define the delete() method to:
Initialize max_val as 0.

Loop through the queue and find the index of the maximum value.
Delete and return the element at that index.

In the main code, take integer input n for number of elements.
Loop n times to take input values and insert them into the priority queue.
Print the contents of the queue.

While the queue is not empty, call delete() and print each returned element.
End the program.

# PROGRAM
```
# A simple implementation of Priority Queue
# using Queue.
class PriorityQueue(object):
	def __init__(self):
		self.queue = []

	def __str__(self):
		return ' '.join([str(i) for i in self.queue])

	# for checking if the queue is empty
	def isEmpty(self):
		return len(self.queue) == 0

	# for inserting an element in the queue
	def insert(self, data):
		self.queue.append(data)

	# for popping an element based on Priority
	def delete(self):
	    try:
	        max_val=0
	        for i in range(len(self.queue)):
	            if self.queue[i]>self.queue[max_val]:
	                max_val = i
	        item = self.queue[max_val]
	        del self.queue[max_val]
	        return item
	    except IndexError:
	        print()
	        exit()
	   

myQueue = PriorityQueue()
n=int(input())	
for i in range(0, n):
    ele = int(input())
    myQueue.insert(ele)
	
print(myQueue)		
while not myQueue.isEmpty():
	print(myQueue.delete())
```

# OUTPUT
<img width="1195" height="452" alt="Screenshot 2025-09-05 232301" src="https://github.com/user-attachments/assets/49ae142f-55ee-475f-ab0c-1d935c10b8d2" />

# RESULT
Thus the Python program for simple implementation of Priority Queue using Queue has been implemented and executed successfully.

