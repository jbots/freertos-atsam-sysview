Commits c231921 and 866d39c, which are patches for ARM_CM0/port.c, together provide SEGGER_SYSVIEW_X_GetTimestamp which is needed for the Cortex M0 port to work with Segger SystemView.

c231921: add SEGGER_SYSVIEW_TickCnt with tick count, to be used by SEGGER_SYSVIEW_X_GetTimestamp

866d39c: implement SEGGER_SYSVIEW_X_GetTimestamp
