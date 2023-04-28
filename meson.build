project('bx', 'cpp')

if get_option('debug')
	bx_config_debug = 1
else
	bx_config_debug = 0
endif

bx = static_library(
	'bx',
	['src/amalgamated.cpp'],
	include_directories: include_directories(['include', '3rdparty']),
	cpp_args: ['-DBX_CONFIG_DEBUG=@0@'.format(bx_config_debug)]
)

bx_deps = []
if host_machine.system() == 'darwin'
	bx_deps += [dependency('foundation')]
endif

bx_dep = declare_dependency(
	include_directories: include_directories('include'),
	link_with: bx,
	dependencies: bx_deps
)
