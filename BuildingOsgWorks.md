

# Dependencies #

osgWorks depends on OpenSceneGraph. See the CompatibilityMatrix.

The osgWorks build system requires [CMake](http://www.cmake.org/) v2.6.4 or later (current trunk requires v2.8.8 or later).

# Building #

Like OpenSceneGraph, osgWorks uses [CMake](http://www.cmake.org/).

The osgWorks CMake system should find the OSG dependency automatically if it's installed on your system in a standard/typical location. You might need to set a special variable required by the CMake module that finds OSG (such as the OSG\_DIR environment variable).

If the CMake system fails to find OSG, it's usually because OSG is installed in a non-typical location, or you're using OSG from a source tree. osgWorks' CMake system uses a CMake helper script to assist in finding OSG. This script is designed to work with the cmake-gui executable (but can also be used with the command line version of cmake).

To use the GUI, issue the `cmake-gui` command. After the first `Configure`, the GUI should display the OSGInstallType pulldown menu. Open it and select Default Installation, Alternate Installation, or Source And Build Tree. Then select `Configure` again. The CMake GUI will prompt you for additional directory information based on your pulldown menu selection. Supply the requested directory information and select `Configure` again.

After clicking `Generate`, use your project files / makefiles to build osgWorks.

# Installing osgWorks #

Once you have built osgWorks it is possible to install osgWorks into a directory that will contain a bin, lib, and include directory. Use 'make install' with GNUMake, or build the INSTALL target in Visual Studio. The location of this directory can be set via the CMake variable CMAKE\_INSTALL\_PREFIX. After you have installed osgWorks, be sure to point your (DY)LD\_LIBRARY\_PATH at the lib directory and your PATH at the bin directory (on Windows, add both directories to PATH). This will enable your applications to run osgWorks apps and load osgWorks libraries and plugins.