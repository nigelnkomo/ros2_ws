# A Simple Client and Service in Python

## Table of Contents 📑

- [Background](#background) 🖼️
  - [What is it? What does it do?](#what) 🤔
  - [Why is it? Why should it exist? What problems does it solve?](#why) 🤔
- [Code 🖥️](#code)
  - [Project Structure](#structure) 🌳

<!-- TODO
  - [Explanation](#explanation) 🖊️
- [How to run](#howTo) ⌨
- [Questions / Gaps / Problems / Challenges](#questions) 🙋🧐
- [Solutions to some or all the questions / How were the challenges overcome? / Thought process / Similarity or differences to other problems / Proofs](#solutions) 💡✅🎯
-->
 <h2 id="background">Background</h2>
    <h3 id="what">What is it? What does it do? 🤔</h3>
        <p>The project demonstrates how nodes in the ROS graph can communicate using services.</p>
        <p>There is a separation of concerns or reponsibilities here. What are the concerns? In order to answer this question, one needs to understand what model of communication is used.</p>
        <p>Services utilise the <strong>call-and-response model</strong>.</p>
        <img src="./img/call-and-response.jpg" alt="call and response" height="400px"/>
        <p>Think of how musicians sing a line (the call) and point the mic at the croud to sing the next line (the response).</p>
        <p>Similarly, the node that sends a request (or a call) for information is called the service client, and the node that receives the call or request and thus sends a response is called a service server.</p>
        <p>Therefore, the call concern or responsibility is handled by the service client and the response concern or responsibility is handled by the service server.<p>
    <h3 id="why">Why is it? Why should it exist? What problems does it solve? 🤔</h3>
        <p>The request-response model, utilised by services, is an indespensible tool where precision and coordination are required.</p>
        <img src="./img/car-manufacturing.jpg" alt="car manufacturing" width="400px"/>
        <p>As an example, in car manufacturing, a robotic arm trying to install a car door to the frame needs to ensure that the car door is aligned with the frame's hinges. This is a precision task. A service call or request could be sent to the service server that whose separated concern would be to check this alignment using sensor data. Once, confirmed, would respond to the service call, giving the green light for the arm to proceed with installing the car door. Were the arm to proceed without a response, this would lead to improper fitting or damage to both the door and the frame.</p>
 <h2 id="code">Code</h2>
    <h3 id="structure">Project Structure 🌳</h3>
      
    ros2_ws
    ├── img
    │   ├── call-and-response.jpg
    │   └── car-manufacturing.jpg
    ├── README.md
    └── src
        └── py_srvcli
            ├── LICENSE
            ├── package.xml
            ├── py_srvcli
            │   ├── client_member_function.py
            │   ├── __init__.py
            │   └── service_member_function.py
            ├── resource
            │   └── py_srvcli
            ├── setup.cfg
            ├── setup.py
            └── test
                ├── test_copyright.py
                ├── test_flake8.py
                └── test_pep257.py
<!--TODO
 <h3 id="explanation">Explanation 🖊️</h3>
 <h2 id="howTo">How to Run ⌨</h2>
 <h2 id="questions">Questions / Gaps / Problems / Challenges 🙋🧐</h2>
 <h2 id="solutions">Solutions to some or all the questions / How were the challenges overcome? / Thought process / Similarity or differences to other problems / Proofs 💡✅🎯</h2>
 -->
