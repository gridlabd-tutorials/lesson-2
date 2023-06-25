[![Simulation](../../actions/workflows/main.yml/badge.svg)](../../actions/workflows/main.yml)

# Lesson 2 - Static Loads

The goal of this lesson is to familiarize you with the various ways of modeling loads in GridLAB-D. The specific learning objectives are the following

1. How to modify an existing static load.
2. How to add static loads of different types.
3. How to remove a static load.
4. How to create new load objects.

## Static Load Models

Loads can be either static (i.e., constant power, current, and/or impedance).  The load composition can be specified in a variety of way including (1) the real and reactive parts, (2) the magnitudes and angles by phase, and (3) the total load and fractions by phase with the power factors. In addition, loads can be specified as 3-phase in delta or wye configuration, or as triplex loads on a split phase.

## Tasks

The following tasks are illustrated in [`main.glm`](main.glm):

1. Modify existing static loads
    1. Change constant power load on phase A of `load_1` to 48 kW real power and 24 VAr reactive power (See [`main.glm@6`](main.glm#L6-L7)).
    2. Add constant impedance load to phase B of `load_2` at 100 Ohm resistance and 10 Ohm reactance (See [`main.glm@9`](main.glm#L9-L10)).
    3. Remove constant power load on phase C of `load_4` by setting it to 0+0j complex power (See [`main.glm@12`](main.glm#L12-L13)).
2. Create new static loads
     1. Add `load_115` to `load_114` through `line_114to115` (See [`main.glm@15`](main.glm#L15-L32)). Copy the load from `load_114`.
     2. Connect `load_116` directly to `load_115` (See [`main.glm@34`](main.glm#L34-L43)). Double the load from `load_114`.

# Exercises

1. Change the constant power load on `load_116` to an equivalent constant current load. (Hint: the `constant_current = constant_power / nominal_voltage`.)

# More Information

* [Static (ZIP) Models](https://docs.gridlabd.us/index.html?owner=arras-energy&project=gridlabd&branch=master&folder=/Module/Powerflow&doc=/Module/Powerflow/Load.md)
* [PQ Models](https://docs.gridlabd.us/index.html?owner=arras-energy&project=gridlabd&branch=master&folder=/Module/Powerflow&doc=/Module/Powerflow/Pqload.md)
* [Triplex Models](https://docs.gridlabd.us/index.html?owner=arras-energy&project=gridlabd&branch=master&folder=/Module/Powerflow&doc=/Module/Powerflow/Triplex_load.md)
* [Motor Models](https://docs.gridlabd.us/index.html?owner=arras-energy&project=gridlabd&branch=master&folder=/Module/Powerflow&doc=/Module/Powerflow/Motor.md)
* [Variable Frequency Drive Models](https://docs.gridlabd.us/index.html?owner=arras-energy&project=gridlabd&branch=master&folder=/Module/Powerflow&doc=/Module/Powerflow/Vfd.md)
* [Advanced Loads](https://docs.gridlabd.us/index.html?owner=arras-energy&project=gridlabd&branch=master&folder=/Module/Powerflow&doc=/Module/Powerflow/Advanced_loads.md)
    * [Building Models](https://docs.gridlabd.us/index.html?owner=arras-energy&project=gridlabd&branch=master&folder=/Module/Powerflow&doc=/Module/Powerflow/Building.md)
    * [Agricultural Models](https://docs.gridlabd.us/index.html?owner=arras-energy&project=gridlabd&branch=master&folder=/Module/Powerflow&doc=/Module/Powerflow/Agricultural.md)
    * [Industrial Models](https://docs.gridlabd.us/index.html?owner=arras-energy&project=gridlabd&branch=master&folder=/Module/Powerflow&doc=/Module/Powerflow/Industrial.md)
    * [Public Service Models](https://docs.gridlabd.us/index.html?owner=arras-energy&project=gridlabd&branch=master&folder=/Module/Powerflow&doc=/Module/Powerflow/Public_service.md)

# Next Lesson

* [Lesson 3 - Generators](../../../lesson-3)
