from building import *

cwd     = GetCurrentDir()
CPPPATH = [cwd + '/inc', cwd + '/inc/qrcode', cwd + '/inc/decoder']

src     = []
LIBPATH = ['']
LIBS    = [''] 
if GetDepend(['BSP_USING_SRC_INSTEAD_LIB']):
    src     = Glob('src/*.c')
    src     += Glob('src/decoder/*.c')
    src     += Glob('src/qrcode/*.c')
else:
    LIBPATH = [cwd + '/lib']
    LIBS    = ['zbar'] 
    
group = DefineGroup('zbar', src, depend = ['PKG_USING_ZBAR'], CPPPATH = CPPPATH, LIBS = LIBS, LIBPATH=LIBPATH)

Return('group')

