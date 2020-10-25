# Nordic52840LowPower
Experiment on how to implement low power mode on Noridc52840

### Behaviour Description
主要实现Nordic Sleep mode，并且让外界中断可以唤醒Nordic的休眠模式


### Requirement：To have Nordic firmware 
1. be able enter low power / sleep mode
2. to be able to demonstrate it enters low power mode
3. to be able to be waken up by external interrupt

***Question to think during implementation:***

- How can you prove that Nordic enters sleep mode successfully?
- How to put Nordic into low power mode that can be woken up by the external interrupt?
- How to electrically connect External interrupt source to Nordic to do this waking up?
- will you set up some sort of push button simulated pin raise/lower to test wake up feature?
- will you set up some sort of power metering to detect power usage?




### Firmware Configuration management:

* this code is built and tested on segger embedded studio 4.50
* this code is built and tested with Nordic's nRF5_SDK_15.2.0
* this code is built and tested with either Nordic52840 or NINAB301 DK
* if any experience/knowldege is learnt while developing this task, this notice will be updated. 

### Getting started - to record any useful knowldege about Nordic low power implementation
[S] this is a reference Nordic project for a starting point for low power implmentation nRF5_SDK_15.2.0\examples\peripheral\pwr_mgmt

[S] To try to use these functions to achieve low power: they are being used by previous Boost Design projects (fw_smartaed_button) on low power mode:
power_management_init();
idle_state_handle(); 
nrf_pwr_mgmt_run(); 
sleep_mode_enter();
