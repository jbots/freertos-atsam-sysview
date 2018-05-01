freertos_srcs = files([
  'FreeRTOSV10.0.0/Source/list.c',
  'FreeRTOSV10.0.0/Source/event_groups.c',
  'FreeRTOSV10.0.0/Source/croutine.c',
  'FreeRTOSV10.0.0/Source/stream_buffer.c',
  'FreeRTOSV10.0.0/Source/queue.c',
  'FreeRTOSV10.0.0/Source/timers.c',
  'FreeRTOSV10.0.0/rtos_port.c',
  'FreeRTOSV10.0.0/Source/portable/GCC/ARM_CM0/port.c',
  'FreeRTOSV10.0.0/Source/tasks.c',
])

freertos_memmang_dir = 'FreeRTOSV10.0.0/Source/portable/MemMang'

freertos_src_heap_1 = files(join_paths(freertos_memmang_dir,'heap_1.c'))
freertos_src_heap_2 = files(join_paths(freertos_memmang_dir,'heap_2.c'))
freertos_src_heap_3 = files(join_paths(freertos_memmang_dir,'heap_3.c'))
freertos_src_heap_4 = files(join_paths(freertos_memmang_dir,'heap_4.c'))
freertos_src_heap_5 = files(join_paths(freertos_memmang_dir,'heap_5.c'))

freertos_incdirs = include_directories([
  '.',
  'FreeRTOSV10.0.0',
  'FreeRTOSV10.0.0/Source/include',
  'FreeRTOSV10.0.0/Source/portable/GCC/ARM_CM0',
#  'FreeRTOSV10.0.0/module_config',
])

freertos_sysview_srcs = files([
  'SEGGER_SystemView/SEGGER_SYSVIEW_FreeRTOS.c',
  'SEGGER_SystemView/Config/SEGGER_SYSVIEW_Config_FreeRTOS.c',
])

freertos_sysview_incdirs = include_directories([
  'SEGGER_SystemView',
])

