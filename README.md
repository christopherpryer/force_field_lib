# force_field_lib
Earth's geostationary orbit simulator.

## About
```force_field_lib``` is a c++ simulation library for measurement and prediction of potential collisions during orbital travel with python bindings.

The library will be open sourced for modular interfacing. ```force_field_ui``` is an additional c++ and python packaged application for interfacing with the ```force_field_lib``` library. Abstracting the project this way allows for a more flexible development process.

## Why?
Two-fold. One, I have been interested in designing astrophysics simulation software since I was a child. My first love was space. So this project is dedicated to a large component of what has made me the curious adult I am today. 

The second reason for wanting to build something like this is more professional. I've been working as an engineer on a supply chain solutions team. I'm often tasked with completing analyses of varying levels of complexity, and I'm often required to model entire supply chains. Being able to build a simulation with performance-optimized code, in a nicely packaged and concise way, will help enable me to do more in the future within the engineering space (pun intended).

## More

### [Orbital debris](https://www.nasa.gov/centers/hq/library/find/bibliographies/space_debris)

Low earth orbit (LEO) is an orbital space littered with space debris. There's estimated to be millions of pieces of debris orbiting the earth, with this number expected to climb at different rates in the future.

The danger that this space debris poses to launches and returns through earth's orbital space makes this an interesting problem to solve. In the future this issue will hold more relevance as the commercialization of the industry grows.

To solve this problem we can employ an ecosystem of technologies to measure and predict the potential for an orbital collision.

### Other orbital regions
In addition to LEO there are medium and high earth orbital regions as well. ```force_field_lib``` can provide the contextual data of each of these regions of space and educate users on traffic located here as well.

### Other near earth objects (NEO)
Nasa and other entities collect data about NEO and [share it with the public](https://cneos.jpl.nasa.gov/ca/). ```force_field_lib``` can tie this data into its interface for additional preventative measures.

### Making this program extensible
```force_field_lib``` is intended to become a contextual tool for initial and final space travel in the future through the use of modular extensions such as (but not limited to):

- [Nasa's Lunch Sites](https://www.nasa.gov/centers/kennedy/launchingrockets/sites.html)
- [OpenSky Flight Data](https://examples.pyviz.org/opensky/opensky.html)
- [OpenWeather Data](https://openweathermap.org/api)

## Development

- Sprint 1: Build python-extendable c++ source to handle 3-dimensional data representing points on a sphere. Build tests for interfacing and running the c++ from both python and c++.

- Sprint 2: Build optimization layer for gap-space ranking & tests.

- Sprint 3: GUI?

# Build Instructions (cygwin)

- ```mkdir build```
- ```cmake -DBOOST_ROOT=to/boost/root ../src/```
- ```cmake --build .```