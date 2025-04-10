# ❇️ USAGE STATS PLUGIN FOR OJS 3.4+

```
=============================================================
=== Usage Statistics Plugin update for ojs 3.4+
=== Version: 1.0
=============================================================
```

## About

This plugin implements usage statistics logging and processing, and also 
default reports to retrieve statistics related to the journal i.e. press, 
articles i.e. monographs and article i.e. monograph files.

Usually an usage statistic event is a page view (journal i.e. press catalog index page,
abstract article i.e. monograph page, etc) or a file download (article i.e. monograph file downloads).

This plugin can also log statistics aggregated by the geo location of the
user. To activate this option, take a look at the INSTALLATION section of
this document.

## License

This plugin is licensed under the GNU General Public License v2. See the file
LICENSE for the complete terms of this license.

## System Requirements

The default usage of this plugin is automatic and doesn't require any other
extra requirement other than OJS i.e. OMP already does.

If you want to learn on how to process external log files, like apache access
files, please refer to https://pkp.sfu.ca/wiki/index.php?title=PKP_Statistics_Framework#External_access_log_files_alternative


## Installation

The plugin is integrated as a submodule in the OJS i.e. OMP.
 
To enable the plugin go as admin user either to  
- `Administration` > `Site Settings` > `Plugins` > `Generic Plugins`
  or to 
- `Settings` > `Website` > `Plugins` > `Generic Plugins`
...and select the Enable checkbox beside `Usage Statistics Plugin`

The only needed additional step depends on whether you want to have geo 
location data in your statistics or not. If that's the case, follow these
steps:

### Linux:
* 1 - open a shell prompt
* 2 - go into OJS i.e. OMP installation’s base directory
* 3 - `wget http://geolite.maxmind.com/download/geoip/database/GeoLiteCity.dat.gz`
* 4 - `gunzip GeoLiteCity.dat.gz`
* 5 - `mv GeoLiteCity.dat plugins/generic/usageStats`

### Windows
* 1 - download the file http://geolite.maxmind.com/download/geoip/database/GeoLiteCity.dat.gz
* 2 - decompress it using any decompression tool into `plugins/generic/usageStats` directory

In both cases the complete path to the installed database file should be
`plugins/generic/usageStats/GeoLiteCity.dat`

Note, that a separate license agreement is required for this use of this database. 
For details, see:
	https://dev.maxmind.com/geoip/legacy/geolite/


## Management



## Contact/Support

Documentation, bug listings, and updates can be found on this plugin's homepage
at <http://github.com/pkp/usageStats>.
