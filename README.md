# arma-3-life-trading
This is a trading script for ArmA 3 RPG Life.

## Installation

A working installation of ArmA Life RPG Framework is required for a successful installation. Modifying the ArmA Life RPG Framework could cause errors – feel free to connect to our discord if you have a problem.

### Step 1

Download the newest release and extract the archive. Copy the folder "trade" in your “cation” folder that can be found in the  root folder (subsequently called \<mission\>) of your mission.

### Step 2

Open \<mission\>/cation/cation_functions.cpp and insert

`#include "trade\functions.cpp"`

and save the file.

### Step 3

Open \<mission\>/cation/cation_master.cpp and insert

`#include "trade\config.cpp"`

and save the file.

### Step 4

Open \<mission\>/cation/cation_remoteExec.cpp and insert

`#include "trade\remoteExec.cpp"`

and save the file.

### Step 5

Open <mission/core/functions/fn_handleItem.sqf and replace 3x

`clearWeaponCargo`

with

`clearWeaponCargoGlobal`

and save the file.

### Step 6 (only 3.1.4.8 – 4.4)

Open life_server/Functions/Systems/fn_spawnVehicle.sqf and replace

`_vehicle setVariable["dbInfo",[(_vInfo select 4),_vInfo select 7]];`

with

`_vehicle setVariable["dbInfo",[(_vInfo select 4),_vInfo select 7],true];`

and save the file.

### Step 7 (only 3.1.4.8 – 4.4)

Open life_server/Functions/Systems/fn_vehicleCreate.sqf and replace

`_vehicle setVariable["dbInfo",[_uid,_plate]];`

with

`_vehicle setVariable["dbInfo",[_uid,_plate],true];`

and save the file.

**That’s it!**

You have installed the cationstudio trade system successfully!

## Configuration:

You can adjust settings in \<mission\>/cation/trade/config.cpp.

In the settings it is important to set ArmA Life version to your used version.

Texts and translations can be edited in \<mission\>/cation/trade/language.cpp.

To start trading press the key combination “SHIFT + J” and look at the same moment at the person you want to trade with. This key combination can be edited in \<mission\>/cation/trade/config.cpp.

The logo can be changed by replacing \<mission\>/cation/trade/logo.paa with another picture.