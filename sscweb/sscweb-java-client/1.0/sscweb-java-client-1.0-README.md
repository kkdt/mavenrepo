# Satellite Situation Center 2.0 Web Services
Gradle project that pulls the WSDL from the [Satellite Situation Center](https://sscweb.gsfc.nasa.gov/WebServices/) interface and builds the necessary client stubs to access the web service. The built artifact is a Jar file containing all the generated JAX-WS artifacts.

WSDL: `https://sscweb.gsfc.nasa.gov/WS/ssc/2/SatelliteSituationCenterService?wsdl`.

## Quick Start

`./gradlew cleanAll` Clean all generated artifacts

`./gradlew cleanAll build publishToMavenLocal` Install to local Maven repository
