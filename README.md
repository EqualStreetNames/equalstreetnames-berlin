# equalstreetnames-berlin

This repository keeps the configuration to build your own equalstreetnames-berlin, which is based on [equalstreetnames](https://github.com/openknowledgebe/equalstreetnames).

Since it takes some time to process all the data I had to alter the following settings to prevent timeouts.

In composer.json I added

    ...
    "config": {
        "process-timeout": 600
    }
    ...

and in scripts/overpass-way.php I added also a timeout parameter


    $response = $client->request(
        'GET',
        sprintf('https://overpass-api.de/api/interpreter?data=%s', urlencode($query)),
        ['timeout' => 400]
    );



