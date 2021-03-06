New, updated, and deprecated options in Mitaka for OpenStack Networking
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

..
  Warning: Do not edit this file. It is automatically generated and your
  changes will be overwritten. The tool to do so lives in the
  openstack-doc-tools repository.

.. list-table:: New options
   :header-rows: 1
   :class: config-ref-table

   * - Option = default value
     - (Type) Help string
   * - ``[DEFAULT] default_availability_zones =``
     - ``(ListOpt) Default value of availability zone hints. The availability zone aware schedulers use this when the resources availability_zone_hints is empty. Multiple availability zones can be specified by a comma separated string. This value can be empty. In this case, even if availability_zone_hints for a resource is empty, availability zone is considered for high availability while scheduling the resource.``
   * - ``[DEFAULT] ipv6_pd_enabled = False``
     - ``(BoolOpt) Enables IPv6 Prefix Delegation for automatic subnet CIDR allocation. Set to True to enable IPv6 Prefix Delegation for subnet allocation in a PD-capable environment. Users making subnet creation requests for IPv6 subnets without providing a CIDR or subnetpool ID will be given a CIDR via the Prefix Delegation mechanism. Note that enabling PD will override the behavior of the default IPv6 subnetpool.``
   * - ``[DEFAULT] notification_driver = []``
     - ``(MultiStrOpt) The Drivers(s) to handle sending notifications. Possible values are messaging, messagingv2, routing, log, test, noop``
   * - ``[DEFAULT] notification_topics = notifications``
     - ``(ListOpt) AMQP topic used for OpenStack notifications.``
   * - ``[DEFAULT] notification_transport_url = None``
     - ``(StrOpt) A URL representing the messaging driver to use for notifications. If not set, we fall back to the same configuration used for RPC.``
   * - ``[DEFAULT] rpc_state_report_workers = 1``
     - ``(IntOpt) Number of RPC worker processes dedicated to state reports queue``
   * - ``[DEFAULT] wsgi_default_pool_size = 1000``
     - ``(IntOpt) Size of the pool of greenthreads used by wsgi``
   * - ``[DEFAULT] wsgi_log_format = %(client_ip)s "%(request_line)s" status: %(status_code)s  len: %(body_length)s time: %(wall_seconds).7f``
     - ``(StrOpt) A python format string that is used as the template to generate log lines. The following values can beformatted into it: client_ip, date_time, request_line, status_code, body_length, wall_seconds.``
   * - ``[AGENT] availability_zone = nova``
     - ``(StrOpt) Availability zone of this node``
   * - ``[OVS] ovsdb_connection = tcp:127.0.0.1:6640``
     - ``(StrOpt) The connection string for the native OVSDB backend. Requires the native ovsdb_interface to be enabled.``
   * - ``[OVS] vhostuser_socket_dir = /var/run/openvswitch``
     - ``(StrOpt) OVS vhost-user socket directory.``
   * - ``[nova] auth_type = None``
     - ``(Opt) Authentication type to load``
   * - ``[oslo_messaging_qpid] amqp_auto_delete = False``
     - ``(BoolOpt) Auto-delete queues in AMQP.``
   * - ``[oslo_messaging_qpid] amqp_durable_queues = False``
     - ``(BoolOpt) Use durable queues in AMQP.``
   * - ``[oslo_messaging_qpid] qpid_heartbeat = 60``
     - ``(IntOpt) Seconds between connection keepalive heartbeats.``
   * - ``[oslo_messaging_qpid] qpid_hostname = localhost``
     - ``(StrOpt) Qpid broker hostname.``
   * - ``[oslo_messaging_qpid] qpid_hosts = $qpid_hostname:$qpid_port``
     - ``(ListOpt) Qpid HA cluster host:port pairs.``
   * - ``[oslo_messaging_qpid] qpid_password =``
     - ``(StrOpt) Password for Qpid connection.``
   * - ``[oslo_messaging_qpid] qpid_port = 5672``
     - ``(IntOpt) Qpid broker port.``
   * - ``[oslo_messaging_qpid] qpid_protocol = tcp``
     - ``(StrOpt) Transport to use, either 'tcp' or 'ssl'.``
   * - ``[oslo_messaging_qpid] qpid_receiver_capacity = 1``
     - ``(IntOpt) The number of prefetched messages held by receiver.``
   * - ``[oslo_messaging_qpid] qpid_sasl_mechanisms =``
     - ``(StrOpt) Space separated list of SASL mechanisms to use for auth.``
   * - ``[oslo_messaging_qpid] qpid_tcp_nodelay = True``
     - ``(BoolOpt) Whether to disable the Nagle algorithm.``
   * - ``[oslo_messaging_qpid] qpid_topology_version = 1``
     - ``(IntOpt) The qpid topology version to use. Version 1 is what was originally used by impl_qpid. Version 2 includes some backwards-incompatible changes that allow broker federation to work. Users should update to version 2 when they are able to take everything down, as it requires a clean break.``
   * - ``[oslo_messaging_qpid] qpid_username =``
     - ``(StrOpt) Username for Qpid connection.``
   * - ``[oslo_messaging_qpid] send_single_reply = False``
     - ``(BoolOpt) Send a single AMQP reply to call message. The current behaviour since oslo-incubator is to send two AMQP replies - first one with the payload, a second one to ensure the other have finish to send the payload. We are going to remove it in the N release, but we must keep backward compatible at the same time. This option provides such compatibility - it defaults to False in Liberty and can be turned on for early adopters with a new installations or for testing. Please note, that this option will be removed in the Mitaka release.``
   * - ``[oslo_messaging_rabbit] kombu_reconnect_timeout = 60``
     - ``(IntOpt) How long to wait before considering a reconnect attempt to have failed. This value should not be longer than rpc_response_timeout.``

.. list-table:: New default values
   :header-rows: 1
   :class: config-ref-table

   * - Option
     - Previous default value
     - New default value
   * - ``[DEFAULT] host``
     - ``localhost``
     - ``example.domain``
   * - ``[DEFAULT] zmq_use_broker``
     - ``False``
     - ``True``
   * - ``[ml2_type_flat] flat_networks``
     -
     - ``*``

.. list-table:: Deprecated options
   :header-rows: 1
   :class: config-ref-table

   * - Deprecated option
     - New Option
   * - ``[DEFAULT] use_syslog``
     - ``None``

