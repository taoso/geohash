# GeoHash

Simple php geohash class like python-geohash.


## Getting Started

### Install
You may install GeoHash with Composer (recommended) or manually.

Just add 'geo/geohash' to your composer.json and run `composer install`.

### System Requirements
You need **PHP >= 5.3.0**.

### Usage
Encode a coordinate:

    use Geo\GeoHash;
    echo GeoHash::encode(117.031689,36.65396);

The result is wwe0x0euu12.

The default precision is 0.00001 which can be changed by the third parameter
of encode method.

Find the neighbors for a given geohash:

    use Geo\GeoHash;
    var_dump(GeoHash::expand('wwe0x0'));

and the result is `array("wwe0wc","wwe0x1","wwe0x3","wwe0wb","wwe0x2","wwe0qz","wwe0rp","wwe0rr")`.
