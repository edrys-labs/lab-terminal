# Edrys: Terminal Laboratory

To make use of this laboratory configuration, simply import one of the following configurations with the full URL into [edrys-Lite](https://edrys-labs.github.io):

[`https://raw.githubusercontent.com/edrys-labs/lab-terminal/main/laboratory/terminal.yaml`](https://raw.githubusercontent.com/edrys-labs/lab-terminal/main/laboratory/terminal.yaml)

[`https://raw.githubusercontent.com/edrys-labs/lab-terminal/main/laboratory/terminal.json`](https://raw.githubusercontent.com/edrys-labs/lab-terminal/main/laboratory/terminal.json)

... or download them to your local machine and import them from there.

## Steps

1. Visit [edrys-Lite](https://edrys-labs.github.io) and create a new classroom.
2. Open the settings of the classroom and go to "sharing" and load one of the lab-configurations.
3. Save the settings or modify them to your needs and save them later.
4. In order to secure the classroom configuration go back to the index and click on `write protection` for the current course. This will prevent students from changing the configuration.
5. Share your classroom URL-with students.
6. Go to the station settings and open a new station.
7. In order to share a terminal with the students, you need to run a local terminal server from:

   https://github.com/edrys-labs/module-pyxtermjs

   This can be either done via docker or python.

   1. __Using Docker__

      If you haven't done it so far, install
      [docker](https://docs.docker.com/engine/install/) for your system.

      Then the only thing that is required is to run the following command:

      ```bash
      docker run -it -p 5000:5000 crosslab/edrys_pyxtermjs:latest
      ```

      This will download the pyxtermjs terminal-server from docker-hub and run it in a secure environment.

   2. __Using Python__

      You can also share your terminal directly via Python, visit the following project

      https://github.com/edrys-labs/module-pyxtermjs

      ... the easiest way is to perform the following steps:

       ``` bash
       # 1. clone the repository or download the folder manually
       git clone https://github.com/edrys-labs/module-pyxtermjs

       # 2. install all required sources
       pip3 install -r requirements.txt

       # 3. run the terminal-server
       python3 -m pyxtermjs --cors True --command bash --port 5000
       ```
