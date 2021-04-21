Cosmos DB API for MongoDB Driver for tpcc
=========================================

This driver adds some opinionated pieces to how the configuration applied to the database is done.

Arguments
---------

.. code-block:: text

    ❯ python pytpcc/tpcc.py --help
    usage: tpcc.py [-h] [--config CONFIG] [--reset] [--scalefactor SF]
                [--warehouses W] [--duration D] [--ddl DDL] [--clients N]
                [--stop-on-error] [--no-load] [--no-execute] [--print-config]
                [--debug]
                {}

    Python implementation of the TPC-C Benchmark

    positional arguments:
    {}                Target system driver

    optional arguments:
    -h, --help        show this help message and exit
    --config CONFIG   Path to driver configuration file
    --reset           Instruct the driver to reset the contents of the database
    --scalefactor SF  Benchmark scale factor
    --warehouses W    Number of Warehouses
    --duration D      How long to run the benchmark in seconds
    --ddl DDL         Path to the TPC-C DDL SQL file
    --clients N       The number of blocking clients to fork
    --stop-on-error   Stop the transaction execution when the driver throws an
                        exception.
    --no-load         Disable loading the data
    --no-execute      Disable executing the workload
    --print-config    Print out the default configuration file for the system
                        and exit
    --debug           Enable debug log messages


Configuration
-------------

- ``RESET=[True|False]`` - Default: True - this will remove all the collections that are currently in the database (but keep the database)


TBD
---

- Adding Az Login for connection string management won't work with PyPy without rebuilding or switching to PyPy 3.7.2+


