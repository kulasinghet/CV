FROM ubuntu:18.04

# RUN apt-get update
# RUN apt-get install -y texlive-xetex

# Install Roboto font
# RUN apt-get install -y fonts-roboto


# copy the current directory contents into the container at /app
COPY . /app

# Set the working directory to /app
WORKDIR /app

# Install any needed packages specified in requirements.txt
RUN apt-get update && apt-get install texlive-full -y

# XELATEX build command
RUN xelatex -interaction=nonstopmode -halt-on-error -output-directory=examples ./examples/resume.tex

# copy the build pdf to the host
CMD ["cp", "./../examples/resume.pdf", "./Thevindu Kulasinghe - Resume.pdf"]

# export the pdf to the host
