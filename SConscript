from building import *

cwd     = GetCurrentDir()
CPPPATH = [cwd, cwd + '/inc', cwd + '/inc/zbar', str(Dir('#'))]

src     = Glob('src/*.c')
src     = Glob('src/decoder/*.c')
src     = Glob('src/qrcode/*.c')

group = DefineGroup('zbar', src, depend = ['PKG_USING_ZBAR'], CPPPATH = CPPPATH)

Return('group')

