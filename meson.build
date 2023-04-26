project('bx', 'cpp')

bx = library(
	'bx',
	[
		'src/amalgamated.cpp'
	],
	include_directories: include_directories('include')
)

bx_dep = declare_dependency(
	include_directories: include_directories('include'),
	link_with: bx
)
