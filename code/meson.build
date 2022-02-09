mps_core_srcs = [ 'mpsi.c', 'mpm.c', 'arenavm.c', 'arenacl.c', 'arena.c',
    'global.c', 'locus.c', 'tract.c', 'walk.c', 'protocol.c', 'pool.c',
    'poolabs.c', 'trace.c', 'traceanc.c', 'scan.c', 'root.c', 'seg.c',
    'format.c', 'buffer.c', 'ref.c', 'bt.c', 'ring.c', 'shield.c', 'ld.c',
    'event.c', 'sac.c', 'message.c', 'poolmrg.c', 'poolmfs.c', 'dbgpool.c',
    'dbgpooli.c', 'boot.c', 'meter.c', 'tree.c', 'rangetree.c', 'splay.c',
    'cbs.c', 'ss.c', 'version.c', 'table.c', 'arg.c', 'abq.c', 'range.c',
    'freelist.c', 'sa.c', 'nailboard.c', 'land.c', 'failover.c', 'vm.c',
    'policy.c', ]

mps_pool_srcs = [ 'poolamc.c', 'poolams.c', 'poolawl.c', 'poollo.c',
    'poolsnc.c', 'poolmv2.c', 'poolmvff.c', ]

mps_plat_srcs = ['lockix.c',     # Posix locks
	'thix.c',       # Posix threading
	'pthrdext.c',   # Posix thread extensions
	'vmix.c',       # Posix virtual memory
	'protix.c',     # Posix protection
	'protsgix.c',   # Posix signal handling
	'prmci6.c',     # x86-64 mutator context
	'prmcix.c',     # Posix mutator context
	'prmclii6.c',   # x86-64 for Linux mutator context
	'span.c'       # generic stack probe
]

mps_plinth_srcs = [ 'mpsliban.c', 'mpsioan.c' ]

mps = static_library('mps', mps_core_srcs, mps_pool_srcs, mps_plat_srcs,
    mps_plinth_srcs,
    include_directories: '.',
    dependencies: [ dependency('threads')])

mps_dep = declare_dependency(link_with: mps, include_directories: '.')