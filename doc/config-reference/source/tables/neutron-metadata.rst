..
    Warning: Do not edit this file. It is automatically generated from the
    software project's code and your changes will be overwritten.

    The tool to generate this file lives in openstack-doc-tools repository.

    Please make any changes needed in the code, then run the
    autogenerate-config-doc tool from the openstack-doc-tools repository, or
    ask for help on the documentation mailing list, IRC channel or meeting.

.. _neutron-metadata:

.. list-table:: Description of metadata configuration options
   :header-rows: 1
   :class: config-ref-table

   * - Configuration option = Default value
     - Description
   * - **[DEFAULT]**
     -
   * - ``metadata_access_mark`` = ``0x1``
     - (StrOpt) Iptables mangle mark used to mark metadata valid requests. This mark will be masked with 0xffff so that only the lower 16 bits will be used.
   * - ``metadata_backlog`` = ``4096``
     - (IntOpt) Number of backlog requests to configure the metadata server socket with
   * - ``metadata_port`` = ``9697``
     - (PortOpt) TCP Port used by Neutron metadata namespace proxy.
   * - ``metadata_proxy_group`` =
     - (StrOpt) Group (gid or name) running metadata proxy after its initialization (if empty: agent effective group).
   * - ``metadata_proxy_shared_secret`` =
     - (StrOpt) When proxying metadata requests, Neutron signs the Instance-ID header with a shared secret to prevent spoofing. You may select any string for a secret, but it must match here and in the configuration used by the Nova Metadata Server. NOTE: Nova uses the same config key, but in [neutron] section.
   * - ``metadata_proxy_socket`` = ``$state_path/metadata_proxy``
     - (StrOpt) Location for Metadata Proxy UNIX domain socket.
   * - ``metadata_proxy_socket_mode`` = ``deduce``
     - (StrOpt) Metadata Proxy UNIX domain socket mode, 4 values allowed: 'deduce': deduce mode from metadata_proxy_user/group values, 'user': set metadata proxy socket mode to 0o644, to use when metadata_proxy_user is agent effective user or root, 'group': set metadata proxy socket mode to 0o664, to use when metadata_proxy_group is agent effective group or root, 'all': set metadata proxy socket mode to 0o666, to use otherwise.
   * - ``metadata_proxy_user`` =
     - (StrOpt) User (uid or name) running metadata proxy after its initialization (if empty: agent effective user).
   * - ``metadata_proxy_watch_log`` = ``None``
     - (BoolOpt) Enable/Disable log watch by metadata proxy. It should be disabled when metadata_proxy_user/group is not allowed to read/write its log file and copytruncate logrotate option must be used if logrotate is enabled on metadata proxy log files. Option default value is deduced from metadata_proxy_user: watch log is enabled if metadata_proxy_user is agent effective user id/name.
   * - ``metadata_workers`` = ``1``
     - (IntOpt) Number of separate worker processes for metadata server (defaults to half of the number of CPUs)
   * - ``nova_metadata_insecure`` = ``False``
     - (BoolOpt) Allow to perform insecure SSL (https) requests to nova metadata
   * - ``nova_metadata_ip`` = ``127.0.0.1``
     - (StrOpt) IP address used by Nova metadata server.
   * - ``nova_metadata_port`` = ``8775``
     - (PortOpt) TCP Port used by Nova metadata server.
   * - ``nova_metadata_protocol`` = ``http``
     - (StrOpt) Protocol to access nova metadata, http or https
