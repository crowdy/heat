..
    Warning: Do not edit this file. It is automatically generated from the
    software project's code and your changes will be overwritten.

    The tool to generate this file lives in openstack-doc-tools repository.

    Please make any changes needed in the code, then run the
    autogenerate-config-doc tool from the openstack-doc-tools repository, or
    ask for help on the documentation mailing list, IRC channel or meeting.

.. _heat-api:

.. list-table:: Description of API configuration options
   :header-rows: 1
   :class: config-ref-table

   * - Configuration option = Default value
     - Description
   * - **[DEFAULT]**
     -
   * - ``action_retry_limit`` = ``5``
     - (Integer) Number of times to retry to bring a resource to a non-error state. Set to 0 to disable retries.
   * - ``enable_stack_abandon`` = ``False``
     - (Boolean) Enable the preview Stack Abandon feature.
   * - ``enable_stack_adopt`` = ``False``
     - (Boolean) Enable the preview Stack Adopt feature.
   * - ``encrypt_parameters_and_properties`` = ``False``
     - (Boolean) Encrypt template parameters that were marked as hidden and also all the resource properties before storing them in database.
   * - ``heat_metadata_server_url`` = ``None``
     - (String) URL of the Heat metadata server. NOTE: Setting this is only needed if you require instances to use a different endpoint than in the keystone catalog
   * - ``heat_stack_user_role`` = ``heat_stack_user``
     - (String) Keystone role for heat template-defined users.
   * - ``heat_waitcondition_server_url`` = ``None``
     - (String) URL of the Heat waitcondition server.
   * - ``heat_watch_server_url`` =
     - (String) URL of the Heat CloudWatch server.
   * - ``hidden_stack_tags`` = ``data-processing-cluster``
     - (List) Stacks containing these tag names will be hidden. Multiple tags should be given in a comma-delimited list (eg. hidden_stack_tags=hide_me,me_too).
   * - ``max_json_body_size`` = ``1048576``
     - (Integer) Maximum raw byte size of JSON request body. Should be larger than max_template_size.
   * - ``num_engine_workers`` = ``None``
     - (Integer) Number of heat-engine processes to fork and run. Will default to either to 4 or number of CPUs on the host, whichever is greater.
   * - ``observe_on_update`` = ``False``
     - (Boolean) On update, enables heat to collect existing resource properties from reality and converge to updated template.
   * - ``stack_action_timeout`` = ``3600``
     - (Integer) Timeout in seconds for stack action (ie. create or update).
   * - ``stack_domain_admin`` = ``None``
     - (String) Keystone username, a user with roles sufficient to manage users and projects in the stack_user_domain.
   * - ``stack_domain_admin_password`` = ``None``
     - (String) Keystone password for stack_domain_admin user.
   * - ``stack_scheduler_hints`` = ``False``
     - (Boolean) When this feature is enabled, scheduler hints identifying the heat stack context of a server or volume resource are passed to the configured schedulers in nova and cinder, for creates done using heat resource types OS::Cinder::Volume, OS::Nova::Server, and AWS::EC2::Instance. heat_root_stack_id will be set to the id of the root stack of the resource, heat_stack_id will be set to the id of the resource's parent stack, heat_stack_name will be set to the name of the resource's parent stack, heat_path_in_stack will be set to a list of comma delimited strings of stackresourcename and stackname with list[0] being 'rootstackname', heat_resource_name will be set to the resource's name, and heat_resource_uuid will be set to the resource's orchestration id.
   * - ``stack_user_domain_id`` = ``None``
     - (String) Keystone domain ID which contains heat template-defined users. If this option is set, stack_user_domain_name option will be ignored.
   * - ``stack_user_domain_name`` = ``None``
     - (String) Keystone domain name which contains heat template-defined users. If `stack_user_domain_id` option is set, this option is ignored.
   * - ``stale_token_duration`` = ``30``
     - (Integer) Gap, in seconds, to determine whether the given token is about to expire.
   * - ``trusts_delegated_roles`` =
     - (List) Subset of trustor roles to be delegated to heat. If left unset, all roles of a user will be delegated to heat when creating a stack.
   * - **[auth_password]**
     -
   * - ``allowed_auth_uris`` =
     - (List) Allowed keystone endpoints for auth_uri when multi_cloud is enabled. At least one endpoint needs to be specified.
   * - ``multi_cloud`` = ``False``
     - (Boolean) Allow orchestration of multiple clouds.
   * - **[ec2authtoken]**
     -
   * - ``allowed_auth_uris`` =
     - (List) Allowed keystone endpoints for auth_uri when multi_cloud is enabled. At least one endpoint needs to be specified.
   * - ``auth_uri`` = ``None``
     - (String) Authentication Endpoint URI.
   * - ``ca_file`` = ``None``
     - (String) Optional CA cert file to use in SSL connections.
   * - ``cert_file`` = ``None``
     - (String) Optional PEM-formatted certificate chain file.
   * - ``insecure`` = ``False``
     - (Boolean) If set, then the server's certificate will not be verified.
   * - ``key_file`` = ``None``
     - (String) Optional PEM-formatted file that contains the private key.
   * - ``multi_cloud`` = ``False``
     - (Boolean) Allow orchestration of multiple clouds.
   * - **[eventlet_opts]**
     -
   * - ``client_socket_timeout`` = ``900``
     - (Integer) Timeout for client connections' socket operations. If an incoming connection is idle for this number of seconds it will be closed. A value of '0' means wait forever.
   * - ``wsgi_keep_alive`` = ``True``
     - (Boolean) If False, closes the client socket connection explicitly.
   * - **[heat_api]**
     -
   * - ``backlog`` = ``4096``
     - (Integer) Number of backlog requests to configure the socket with.
   * - ``bind_host`` = ``0.0.0.0``
     - (IP) Address to bind the server. Useful when selecting a particular network interface.
   * - ``bind_port`` = ``8004``
     - (Port number) The port on which the server will listen.
   * - ``cert_file`` = ``None``
     - (String) Location of the SSL certificate file to use for SSL mode.
   * - ``key_file`` = ``None``
     - (String) Location of the SSL key file to use for enabling SSL mode.
   * - ``max_header_line`` = ``16384``
     - (Integer) Maximum line size of message headers to be accepted. max_header_line may need to be increased when using large tokens (typically those generated by the Keystone v3 API with big service catalogs).
   * - ``tcp_keepidle`` = ``600``
     - (Integer) The value for the socket option TCP_KEEPIDLE. This is the time in seconds that the connection must be idle before TCP starts sending keepalive probes.
   * - ``workers`` = ``0``
     - (Integer) Number of workers for Heat service. Default value 0 means, that service will start number of workers equal number of cores on server.
   * - **[oslo_middleware]**
     -
   * - ``enable_proxy_headers_parsing`` = ``False``
     - (Boolean) Whether the application is behind a proxy or not. This determines if the middleware should parse the headers or not.
   * - ``max_request_body_size`` = ``114688``
     - (Integer) The maximum body size for each request, in bytes.
   * - **[oslo_versionedobjects]**
     -
   * - ``fatal_exception_format_errors`` = ``False``
     - (Boolean) Make exception message format errors fatal
   * - **[paste_deploy]**
     -
   * - ``api_paste_config`` = ``api-paste.ini``
     - (String) The API paste config file to use.
   * - ``flavor`` = ``None``
     - (String) The flavor to use.
