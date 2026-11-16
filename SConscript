from building import *
import os

cwd = GetCurrentDir()

path = [cwd]
src = ['system_at32f423.c']

if rtconfig.PLATFORM in ['gcc', 'llvm-arm']:
    src += [os.path.join('startup', 'gcc', 'startup_at32f423.s')]
elif rtconfig.PLATFORM in ['armcc', 'armclang']:
    src += [os.path.join('startup', 'mdk', 'startup_at32f423.s')]
elif rtconfig.PLATFORM in ['iccarm']:
    src += [os.path.join('startup', 'iar', 'startup_at32f423.s')]

group = DefineGroup('cmsis', src, depend = ['PKG_USING_AT32F423_CMSIS_DRIVER'], CPPPATH = path)

Return('group')
