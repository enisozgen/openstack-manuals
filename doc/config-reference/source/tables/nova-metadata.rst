..
    Warning: Do not edit this file. It is automatically generated from the
    software project's code and your changes will be overwritten.

    The tool to generate this file lives in openstack-doc-tools repository.

    Please make any changes needed in the code, then run the
    autogenerate-config-doc tool from the openstack-doc-tools repository, or
    ask for help on the documentation mailing list, IRC channel or meeting.

.. _nova-metadata:

.. list-table:: Description of metadata configuration options
   :header-rows: 1
   :class: config-ref-table

   * - Configuration option = Default value
     - Description
   * - **[DEFAULT]**
     -
   * - ``metadata_cache_expiration`` = ``15``
     - (IntOpt) Time in seconds to cache metadata; 0 to disable metadata caching entirely (not recommended). Increasingthis should improve response times of the metadata API when under heavy load. Higher values may increase memoryusage and result in longer times for host metadata changes to take effect.
   * - ``metadata_host`` = ``$my_ip``
     - (StrOpt) The IP address for the metadata API server
   * - ``metadata_listen`` = ``0.0.0.0``
     - (StrOpt) The IP address on which the metadata API will listen.
   * - ``metadata_listen_port`` = ``8775``
     - (IntOpt) The port on which the metadata API will listen.
   * - ``metadata_manager`` = ``nova.api.manager.MetadataManager``
     - (StrOpt) OpenStack metadata service manager
   * - ``metadata_port`` = ``8775``
     - (IntOpt) The port for the metadata API port
   * - ``metadata_workers`` = ``None``
     - (IntOpt) Number of workers for metadata service. The default will be the number of CPUs available.
   * - ``vendordata_driver`` = ``nova.api.metadata.vendordata_json.JsonFileVendorData``
     - (StrOpt) Driver to use for vendor data
   * - ``vendordata_jsonfile_path`` = ``None``
     - (StrOpt) File to load JSON formatted vendor data from
