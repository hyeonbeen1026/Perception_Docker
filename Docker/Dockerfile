# 1. Base Image
FROM osrf/ros:humble-desktop

# 2. Environment Variables
ENV DEBIAN_FRONTEND=noninteractive

# 3. System Packages
RUN apt-get update && apt-get install -y \
    git \
    wget \
    curl \
    nano \
    python3-pip \
    python3-opencv \
    ros-humble-cv-bridge \
    ros-humble-sensor-msgs \
    && rm -rf /var/lib/apt/lists/*

# 4. Python Libraries (requirements.txt 활용)
RUN pip3 install --upgrade pip
COPY requirements.txt /tmp/requirements.txt
RUN pip3 install --ignore-installed -r /tmp/requirements.txt

# 5. ROS2 Setup
RUN echo "source /opt/ros/humble/setup.bash" >> ~/.bashrc

# 6. Workspace Setup
WORKDIR /root/workspace

# 7. Default Command
CMD ["/bin/bash"]
