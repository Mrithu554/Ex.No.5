# EXPERIMENT NO. 5 – PROMPT CHAINING

## Aim

To solve an engineering problem using **multiple connected prompts** and understand how Prompt Chaining can be used for problem analysis, system design, algorithm development, coding, testing, and documentation.

## Objective

To design an **AI-Based Smart Traffic Management System** by dividing the engineering problem into a sequence of smaller tasks and using the output of one prompt as the input for the next prompt.

---

# Engineering Problem

### AI-Based Smart Traffic Management System

Traffic congestion is a major problem in cities. Traditional traffic signals use fixed timings and cannot automatically respond to changing traffic conditions.

An **AI-Based Smart Traffic Management System** can monitor traffic density and dynamically change traffic signal timings to reduce waiting time and congestion.

---

# Prompt Chain

```text
Problem Identification
        ↓
Requirement Analysis
        ↓
System Architecture
        ↓
Algorithm Design
        ↓
Flowchart
        ↓
Python Code
        ↓
Testing
        ↓
Documentation
```

---

# 1. Problem Identification

### Prompt

> Identify a major problem in urban traffic management and propose an AI-based solution. Explain the problem, proposed solution, inputs, outputs, and expected benefits.

### Output

**Problem:**
Urban roads experience heavy traffic congestion, especially during peak hours. Fixed-time traffic signals may give unnecessary green time to roads with fewer vehicles while congested roads have to wait.

**Proposed Solution:**
An AI-Based Smart Traffic Management System is proposed to monitor vehicle density and automatically adjust traffic signal timings.

**Inputs:**

* Number of vehicles
* Traffic density
* Waiting time
* Traffic flow

**Processing:**

* Analyze traffic data
* Calculate traffic density
* Predict congestion
* Optimize signal timing

**Outputs:**

* Optimized green-light duration
* Reduced waiting time
* Better traffic flow

**Benefits:**

* Reduces traffic congestion
* Saves fuel
* Reduces waiting time
* Improves road utilization
* Provides intelligent traffic control

---

# 2. Requirement Analysis

### Prompt

> Based on the proposed AI-Based Smart Traffic Management System, identify the functional and non-functional requirements, hardware, software, inputs, outputs, and system constraints.

### Output

### Functional Requirements

1. Collect traffic information.
2. Count vehicles on each road.
3. Calculate traffic density.
4. Identify highly congested roads.
5. Dynamically change signal timing.
6. Continuously monitor traffic.

### Non-Functional Requirements

* Fast response
* High reliability
* Real-time operation
* Easy maintenance
* Scalability
* Accuracy

### Hardware Requirements

* Traffic cameras/sensors
* Microcontroller
* Traffic signal LEDs
* Computer/server
* Communication module

### Software Requirements

* Python
* OpenCV
* Machine Learning libraries
* Database
* Operating system

### Inputs and Outputs

| Input           | Output                  |
| --------------- | ----------------------- |
| Vehicle count   | Green-light duration    |
| Traffic density | Signal priority         |
| Waiting time    | Optimized signal timing |
| Traffic flow    | Congestion status       |

---

# 3. System Architecture

### Prompt

> Design a simple system architecture for an AI-Based Smart Traffic Management System. Show the flow from traffic data collection to AI processing and traffic signal control.

### Output

```text
        TRAFFIC CAMERA / SENSOR
                 ↓
          DATA COLLECTION
                 ↓
        TRAFFIC DATA PROCESSING
                 ↓
        VEHICLE COUNTING
                 ↓
        AI TRAFFIC ANALYSIS
                 ↓
       DENSITY CALCULATION
                 ↓
       SIGNAL OPTIMIZATION
                 ↓
        TRAFFIC SIGNALS
                 ↓
       CONTINUOUS MONITORING
                 ↺
```

### Explanation

Traffic sensors or cameras collect information about vehicles. The collected data is processed and given to the AI system. The AI calculates traffic density and decides how much green time should be given to each road. The traffic signals are then automatically updated.

---

# 4. Algorithm Design

### Prompt

> Develop a simple step-by-step algorithm for dynamically controlling traffic signals based on vehicle density.

### Output

### Algorithm

1. Start the system.
2. Collect vehicle data from all roads.
3. Count the number of vehicles.
4. Calculate traffic density.
5. Compare the density of all roads.
6. Identify the road with the highest traffic.
7. Give longer green time to the highly congested road.
8. Give normal or shorter green time to roads with less traffic.
9. Update the traffic signals.
10. Continue monitoring the traffic.
11. Repeat the process.

---

# 5. Flowchart

### Prompt

> Create a simple flowchart for an AI-Based Smart Traffic Management System showing traffic data collection, density calculation, decision-making, signal timing adjustment, and continuous monitoring.

### Output

```text
             START
               ↓
       Collect Traffic Data
               ↓
      Count Number of Vehicles
               ↓
       Calculate Traffic Density
               ↓
       Is Traffic Density High?
           ↙           ↘
         YES            NO
          ↓              ↓
   Increase Green     Normal Green
       Time              Time
          ↘              ↙
           Update Signal
                ↓
        Monitor Traffic
                ↓
             Repeat
```

---

# 6. Python Implementation

### Prompt

> Write a simple Python program to simulate an AI-based traffic signal controller. Take vehicle counts for four roads as input and assign green-light duration based on traffic density.

### Output

```python
roads = ["Road A", "Road B", "Road C", "Road D"]

vehicle_count = []

for road in roads:
    count = int(input("Enter vehicles on " + road + ": "))
    vehicle_count.append(count)

maximum = max(vehicle_count)

print("\nTraffic Signal Timing:")

for i in range(len(roads)):

    if vehicle_count[i] == maximum:
        green_time = 60
    elif vehicle_count[i] > 30:
        green_time = 45
    else:
        green_time = 30

    print(roads[i], "->", green_time, "seconds")
```

### Sample Input

```text
Enter vehicles on Road A: 25
Enter vehicles on Road B: 70
Enter vehicles on Road C: 35
Enter vehicles on Road D: 20
```

### Sample Output

```text
Traffic Signal Timing:

Road A -> 30 seconds
Road B -> 60 seconds
Road C -> 45 seconds
Road D -> 30 seconds
```

### Output Explanation

Road B has the highest number of vehicles. Therefore, it receives the maximum green-light duration of **60 seconds**.

Road C has medium traffic and receives **45 seconds**.

Road A and Road D have lower traffic and receive **30 seconds**.

---

# 7. Testing

### Prompt

> Test the Smart Traffic Management System using different vehicle-density conditions. Create test cases with input, expected output, and actual output.

### Output

| Test Case | Road Vehicle Count | Expected Result         | Actual Result   | Status |
| --------- | ------------------ | ----------------------- | --------------- | ------ |
| TC01      | 10, 20, 15, 12     | Maximum time for Road B | Road B – 60 sec | PASS   |
| TC02      | 25, 70, 35, 20     | Maximum time for Road B | Road B – 60 sec | PASS   |
| TC03      | 50, 40, 30, 20     | Maximum time for Road A | Road A – 60 sec | PASS   |
| TC04      | 15, 20, 25, 18     | Maximum time for Road C | Road C – 60 sec | PASS   |

### Testing Result

The system correctly identifies the road with the highest traffic density and assigns it a longer green-light duration.

---

# 8. Documentation

### Prompt

> Prepare a concise engineering documentation for the AI-Based Smart Traffic Management System including introduction, problem statement, requirements, architecture, algorithm, implementation, testing, advantages, limitations, and conclusion.

### Output
<img width="1360" height="716" alt="Screenshot 2026-08-08 083939" src="https://github.com/user-attachments/assets/d5f3fa4f-9c19-471b-89ce-e165e75fd88f" />

<img width="1361" height="678" alt="Screenshot 2026-08-08 083951" src="https://github.com/user-attachments/assets/f9b55905-b17e-4918-9e07-34890865c9a6" />

## Conclusion

The AI-Based Smart Traffic Management System demonstrates how Prompt Chaining can be used to solve an engineering problem systematically. The problem was divided into multiple stages such as requirement analysis, architecture design, algorithm development, flowchart creation, Python implementation, testing, and documentation. Each stage used the output from the previous stage, demonstrating the effective use of **Prompt Chaining**.

---

# Final Result

The **AI-Based Smart Traffic Management System** was successfully designed using a sequence of connected AI prompts. Prompt Chaining helped transform a complex engineering problem into smaller and manageable stages, from **problem identification to final documentation**.

### Learning Outcome

After completing this experiment, students can:

1. Understand the concept of Prompt Chaining.
2. Divide complex problems into smaller tasks.
3. Design connected prompts for engineering applications.
4. Use AI for system design and programming.
5. Test and document an engineering solution systematically.
