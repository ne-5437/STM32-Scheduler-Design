# STM32 Scheduler Design 

## Project Overview:
This project focuses on designing a preemptive task scheduler for the STM32 microcontroller, leveraging semaphores, interrupts, and time quantas to manage task execution efficiently. The scheduler aims to optimize multitasking in real-time systems while ensuring smooth task transitions and minimal latency.

## Features:
- **Preemptive Scheduling:** Allows tasks to be interrupted and switched based on priority.
- **Semaphore Management:** Used to handle resource sharing between tasks.
- **Interrupt Handling:** Tasks are triggered based on interrupt events to minimize response time.
- **Time Quantum:** A time-slicing mechanism to allocate CPU time to tasks fairly.
  
## Key Components:
1. **Scheduler:** A core component that manages task queuing and context switching.
2. **Tasks:** Multiple tasks with different priorities, managed by the scheduler.
3. **Interrupts:** Hardware and software interrupts to trigger task execution.
4. **Semaphores:** Used for synchronization and resource management between tasks.

## Hardware:
- **STM32 Microcontroller:** The project is based on an STM32 microcontroller (Nucleo 64-bit STM32F411RE), utilizing its interrupt handling and peripheral capabilities.
  
## How it Works:
1. **Initialization:** The microcontroller is initialized, and the timer is set up to handle time slices.
2. **Task Creation:** Multiple tasks with different priorities are created, each associated with a specific function.
3. **Scheduling:** The scheduler decides which task to execute based on priority and availability of resources, ensuring fair CPU time distribution.
4. **Interrupts:** External or internal interrupts trigger task execution based on predefined conditions.
5. **Semaphore Management:** Tasks wait for semaphores when accessing shared resources, ensuring no data conflicts.
6. **Time Quantum:** Each task is given a predefined time quantum before switching to the next task.

## Achievements:
- Efficient handling of multiple tasks with minimal latency.
- Optimized CPU usage through preemptive scheduling and time slicing.
- Reliable resource synchronization using semaphores.

