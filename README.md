# ![LOGO](logo.png) EU BON UTIS **flow**ground Connector

## Description

A generated **flow**ground connector for the EU BON UTIS API (version 1.0).

Generated from: https://api.apis.guru/v2/specs/cybertaxonomy.eu/1.0/swagger.json<br/>
Generated at: 2019-05-07T17:40:09+03:00

## API Description

The Unified Taxonomic Information Service (UTIS) is the taxonomic backbone for the EU-BON project

## Authorization

This API does not require authorization.

## Actions

### capabilities

*Tags:* `utis-controller`

### search

*Tags:* `utis-controller`

#### Input Parameters
* `query` - _required_ - The scientific name to search for. For example: "Bellis perennis", "Prionus" or "Bolinus brandaris". This is an exact search so wildcard characters are not supported.
* `providers` - _optional_ - A list of provider id strings concatenated by comma characters. The default : "pesi,bgbm-cdm-server[col]" will be used if this parameter is not set. A list of all available provider ids can be obtained from the '/capabilities' service end point. Providers can be nested, that is a parent provider can have sub providers. If the id of the parent provider is supplied all subproviders will be queried. The query can also be restriced to one or more subproviders by using the following syntax: parent-id[sub-id-1,sub-id2,...]
* `searchMode` - _optional_ - Specifies the searchMode. Possible search modes are: scientificNameExact, scientificNameLike (begins with), vernacularNameExact, vernacularNameLike (contains), findByIdentifier. If the a provider does not support the chosen searchMode it will be skipped and the status message in the tnrClientStatus will be set to 'unsupported search mode' in this case.
    Possible values: scientificNameExact, scientificNameLike, vernacularNameExact, vernacularNameLike, findByIdentifier.
* `addSynonymy` - _optional_ - Indicates whether the synonymy of the accepted taxon should be included into the response. Turning this option on may cause an increased response time.
* `timeout` - _optional_ - The maximum of milliseconds to wait for responses from any of the providers. If the timeout is exceeded the service will jut return the resonses that have been received so far. The default timeout is 0 ms (wait for ever)

## License

**flow**ground :- Telekom iPaaS / cybertaxonomy-eu-connector<br/>
Copyright © 2019, [Deutsche Telekom AG](https://www.telekom.de)<br/>
contact: flowground@telekom.de

All files of this connector are licensed under the Apache 2.0 License. For details
see the file LICENSE on the toplevel directory.
