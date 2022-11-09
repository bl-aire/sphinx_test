List of Prometheus Metrics
============================
.. table::

    ===========  ===========================================  ==============================================
       Type                         Name                                       Description                  
    ===========  ===========================================  ==============================================
     histogram    jupyterhub_check_routes_duration_seconds      Time taken to validate all routes in proxy  
     histogram     jupyterhub_hub_startup_duration_seconds             Time taken for Hub to start          
     histogram    jupyterhub_init_spawners_duration_seconds       Time taken for spawners to initialize     
     histogram      jupyterhub_proxy_add_duration_seconds        duration for adding user routes to proxy   
     histogram    jupyterhub_proxy_delete_duration_seconds     duration for deleting user routes from proxy 
     histogram     jupyterhub_proxy_poll_duration_seconds       duration for polling all routes from proxy  
     histogram       jupyterhub_request_duration_seconds          request duration for all HTTP requests    
       gauge             jupyterhub_running_servers            the number of user servers currently running 
     histogram     jupyterhub_server_poll_duration_seconds       time taken to poll if server is running    
     histogram    jupyterhub_server_spawn_duration_seconds       time taken for server spawning operation   
     histogram         jupyterhub_server_stop_seconds            time taken for server stopping operation   
       gauge               jupyterhub_total_users                         total number of users             
    ===========  ===========================================  ==============================================
