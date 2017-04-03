.. Read the Docs Template documentation master file, created by
   sphinx-quickstart on Tue Aug 26 14:19:49 2014.
   You can adapt this file completely to your liking, but it should at least
   contain the root `toctree` directive.

Welcome to Read the Docs Template's documentation!
==================================================

Contents:

.. toctree::
   :maxdepth: 2
   :glob:

   *



Indices and tables
==================

* :ref:`genindex`
* :ref:`modindex`
* :ref:`search`

::

   public void ConfigureServices(IServiceCollection services)
   {
            //Verilen path’e loglama yapar.
            services.AddHubble(new HubbleConfiguration()
            {
                LogsFolder = "log",
                EnableSystemLogs = false,
                EnableNavigatingLog = true
            });

            //OPTIONAL
            services.AddHubble(new HubbleConfiguration 
            { 
            EnableNavigatingLog = true 
            });

            services.AddHubbleMonitoring(new HubbleMonitoringConfiguration
            {
                Key = "KEY",
                Secret = "SECRET",
                MonitoringUrl = "url"
            }); 


   }
