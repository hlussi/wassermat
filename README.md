# Resources
https://medium.com/google-cloud/build-a-weather-station-using-google-cloud-iot-core-and-mongooseos-7a78b69822c5


## Firebase installation & configuration

- project=wassermat

- npm install -g firebase-tools
- firebase login
- firebase init
- firebase functions:config:set bigquery.datasetname="wassermat_iot" bigquery.tablename="raw_data"
- firebase deploy --only functions
- firebase functions:config:get

## Big Query configuration



Google Cloud IoT Core Python Samples
===============================================================================

.. image:: https://gstatic.com/cloudssh/images/open-btn.png
   :target: https://console.cloud.google.com/cloudshell/open?git_repo=https://github.com/GoogleCloudPlatform/python-docs-samples&page=editor&open_in_editor=iot/api-client/http_example/README.rst


This directory contains samples for Google Cloud IoT Core. `Google Cloud IoT Core`_ allows developers to easily integrate Publish and Subscribe functionality with devices and programmatically manage device authorization.
The following example runs the sample using the project ID ``blue-jet-123`` and the device name ``my-python-device``::

    python cloudiot_http_example.py \
        --registry_id=my-registry \
        --cloud_region=us-central1 \
        --project_id=blue-jet-123 \
        --device_id=my-python-device \
        --message_type=event \
        --algorithm=RS256 \
        --private_key_file=../rsa_private.pem




.. _Google Cloud IoT Core: https://cloud.google.com/iot/docs

Setup
-------------------------------------------------------------------------------


Install Dependencies
++++++++++++++++++++

#. Clone python-docs-samples and change directory to the sample directory you want to use.

    .. code-block:: bash

        $ git clone https://github.com/GoogleCloudPlatform/python-docs-samples.git

#. Install `pip`_ and `virtualenv`_ if you do not already have them. You may want to refer to the `Python Development Environment Setup Guide`_ for Google Cloud Platform for instructions.

   .. _Python Development Environment Setup Guide:
       https://cloud.google.com/python/setup

#. Create a virtualenv. Samples are compatible with Python 2.7 and 3.4+.

    .. code-block:: bash

        $ virtualenv env
        $ source env/bin/activate

#. Install the dependencies needed to run the samples.

    .. code-block:: bash

        $ pip install -r requirements.txt

.. _pip: https://pip.pypa.io/
.. _virtualenv: https://virtualenv.pypa.io/

Samples
-------------------------------------------------------------------------------

HTTP Device Client Example
+++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++

.. image:: https://gstatic.com/cloudssh/images/open-btn.png
   :target: https://console.cloud.google.com/cloudshell/open?git_repo=https://github.com/GoogleCloudPlatform/python-docs-samples&page=editor&open_in_editor=iot/api-client/http_example/cloudiot_http_example.py,iot/api-client/http_example/README.rst




To run this sample:

.. code-block:: bash

    $ python cloudiot_http_example.py

    usage: cloudiot_http_example.py [-h] --project_id PROJECT_ID --registry_id
                                    REGISTRY_ID --device_id DEVICE_ID
                                    --private_key_file PRIVATE_KEY_FILE
                                    --algorithm {RS256,ES256}
                                    [--cloud_region CLOUD_REGION]
                                    [--ca_certs CA_CERTS]
                                    [--num_messages NUM_MESSAGES] --message_type
                                    {event,state} [--base_url BASE_URL]
                                    [--jwt_expires_minutes JWT_EXPIRES_MINUTES]

    Example Google Cloud IoT Core HTTP device connection code.

    optional arguments:
      -h, --help            show this help message and exit
      --project_id PROJECT_ID
                            GCP cloud project name
      --registry_id REGISTRY_ID
                            Cloud IoT Core registry id
      --device_id DEVICE_ID
                            Cloud IoT Core device id
      --private_key_file PRIVATE_KEY_FILE
                            Path to private key file.
      --algorithm {RS256,ES256}
                            The encryption algorithm to use to generate the JWT.
      --cloud_region CLOUD_REGION
                            GCP cloud region
      --ca_certs CA_CERTS   CA root from https://pki.google.com/roots.pem
      --num_messages NUM_MESSAGES
                            Number of messages to publish.
      --message_type {event,state}
                            Indicates whether the message to be published is a
                            telemetry event or a device state message.
      --base_url BASE_URL   Base URL for the Cloud IoT Core Device Service API
      --jwt_expires_minutes JWT_EXPIRES_MINUTES
                            Expiration time, in minutes, for JWT tokens.





.. _Google Cloud SDK: https://cloud.google.com/sdk/