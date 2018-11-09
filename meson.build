# Variable freertos_port must be set as a string, eg 'ARM_CM0'
if not is_variable('freertos_port')
  error('freertos_port must be set with string indicating FreeRTOS port')
endif

# Variable freertos_heap_type must be set as a string, eg 'heap_1'
if not is_variable('freertos_heap_type')
  error('freertos_heap_type must be set with string indicating heap type')
endif

# Port source
_freertos_port_src = 'FreeRTOSV10.0.0/Source/portable/GCC/@0@/port.c'.format(
  freertos_port)

# Heap source path
_freertos_heap_src = 'FreeRTOSV10.0.0/Source/portable/MemMang/@0@.c'.format(
  freertos_heap_type)

# Common source paths
freertos_srcs = files([
  'FreeRTOSV10.0.0/Source/list.c',
  'FreeRTOSV10.0.0/Source/event_groups.c',
  'FreeRTOSV10.0.0/Source/croutine.c',
  'FreeRTOSV10.0.0/Source/stream_buffer.c',
  'FreeRTOSV10.0.0/Source/queue.c',
  'FreeRTOSV10.0.0/Source/timers.c',
  'FreeRTOSV10.0.0/rtos_port.c',
  'FreeRTOSV10.0.0/Source/tasks.c',
  _freertos_port_src,
  _freertos_heap_src,
])

_freertos_port_incdir = 'FreeRTOSV10.0.0/Source/portable/GCC/@0@'.format(
  freertos_port)

freertos_incdirs = include_directories([
  '.',
  'FreeRTOSV10.0.0',
  'FreeRTOSV10.0.0/Source/include',
  _freertos_port_incdir,
#  'FreeRTOSV10.0.0/module_config',
])

freertos_sysview_srcs = files([
  'SEGGER_SystemView/SEGGER_SYSVIEW_FreeRTOS.c',
  'SEGGER_SystemView/Config/SEGGER_SYSVIEW_Config_FreeRTOS.c',
])

freertos_sysview_incdirs = include_directories([
  'SEGGER_SystemView',
])

freertos_lib = static_library(
  'freertos',
  [freertos_srcs, freertos_sysview_srcs],
  c_args              : [c_args],
  include_directories : [config_incdirs, atstart_incdirs, device_incdirs, cmsis_incdirs,
    segger_sysview_incdirs, freertos_sysview_incdirs, freertos_incdirs]
)
