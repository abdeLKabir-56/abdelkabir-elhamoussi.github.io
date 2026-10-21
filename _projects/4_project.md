---
layout: page
title: IoT Access Control System
description: RFID-based door access control system with real-time events
img:
importance: 4
category: work
---

## IoT Access Control System

This project was developed during my internship at **Broadseg**.

The goal was to build an access control system using **RFID** to manage
door access and process events in real time.

### Technologies

- NestJS
- Node.js
- Kafka
- Server-Sent Events (SSE)
- RFID
- Docker

### How it works

The system receives access events from RFID devices and processes them
through the backend.

**Kafka** was used to handle the events between the different parts of
the system, while **Server-Sent Events (SSE)** were used to send
real-time updates to the application.

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid
        loading="eager"
        title="IoT access control system"
        class="img-fluid rounded z-depth-1"
        %}
    </div>

    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid
        loading="eager"
        title="Access control interface"
        class="img-fluid rounded z-depth-1"
        %}
    </div>
</div>

<div class="caption">
    Access control system and real-time event monitoring.
</div>

### Event processing

One of the main parts I worked on was the backend event processing.

When an RFID access event is received, it can be processed through the
Kafka pipeline and used to update the system in real time.

<div class="row justify-content-sm-center">
    <div class="col-sm-8 mt-3 mt-md-0">
        {% include figure.liquid
        title="Kafka event processing"
        class="img-fluid rounded z-depth-1"
        %}
    </div>
</div>

<div class="caption">
    Event processing with Kafka.
</div>

### Real-time notifications

I also worked with **Server-Sent Events (SSE)** to provide real-time
notifications to the application.

This allowed access events to be displayed without constantly refreshing
the page.

### Docker

The different components of the application were **containerized with
Docker**, which made the development and deployment environment easier
to manage.

### What I learned

This project helped me get more comfortable with **backend development,
event-driven systems and real-time communication**.

It was also my first experience working with **Kafka** and SSE in a
real project.