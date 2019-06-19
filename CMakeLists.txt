##---------------------------------------------------------------------------
## Author:      Steven Adler (based on standard OpenCPN Plug-In CMAKE commands)
## Copyright:   2018
## License:     GPL v3+
##---------------------------------------------------------------------------

# define minimum cmake version
CMAKE_MINIMUM_REQUIRED(VERSION 2.8)

PROJECT(TwoCanPlugIn)

# The TwoCan plugin
ADD_SUBDIRECTORY(Plugin)

# The TwoCan plugin Windows drivers
IF(WIN32)
    ADD_SUBDIRECTORY(Common)
    ADD_SUBDIRECTORY(Axiomtek)
    ADD_SUBDIRECTORY(Cantact)
    ADD_SUBDIRECTORY(TwocanLog)
    ADD_SUBDIRECTORY(Kvaser)
    ADD_SUBDIRECTORY(CandumpLog)
    ADD_SUBDIRECTORY(KeesLog)
    ADD_SUBDIRECTORY(YachtDevicesLog)
ENDIF(WIN32)