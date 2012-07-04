### LinkLayerAddressConfiguration

This is a Python wrapper around the ifconfig tool that can be used to set the Link Layer Addresses (also known as MAC addresses) of network interfaces by reading from a configuration file. It is meant to be used on OS X, where there is a lack of any system tools that can automatically set the MAC addresses of network interfaces based on a configuration file, particularly at startup time. On Linux this functionality is provided by ifupdown which can set MAC addresses specified in /etc/network/interfaces.

The script comes with a simple configuration file that specifies the interfaces and their desired MAC addresses, the format of which can be easily discerned by reading that file. By default this file is designed to be placed in /Library/Preferences/SystemConfiguration/ to mirror the configuration files of other OS X configuration bundles. It also comes with a startup script which can be placed in /Library/LaunchDaemons/ in order to launch the script during system startup. By default the startup script expects the actual script to be located at /Library/SystemConfiguration, which mirrors the location of other OS X configuration bundles at /System/Library/SystemConfiguration/.

The goal is to transform the script into an actual OS X configuration bundle at some point in the future, so that the script can be launched by the configd utility.
