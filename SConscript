from building import *

cwd     = GetCurrentDir()
CPPPATH = [cwd + '/inc', cwd + '/inc/zbar', cwd + '/inc/qrcode', cwd + '/inc/decoder']

if GetDepend(['BSP_USING_SRC_INSTEAD_LIB']):
    src     = Glob('src/*.c')
    src     += Glob('src/decoder/*.c')
    src     += Glob('src/qrcode/*.c')
else:
    src     = ['lib/zbar.lib']

group = DefineGroup('zbar', src, depend = ['PKG_USING_ZBAR'], CPPPATH = CPPPATH)

Return('group')

