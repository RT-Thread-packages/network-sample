from building import *
Import('rtconfig')

src   = []
cwd   = GetCurrentDir()
group = []
CPPPATH = []

# add network samples.
if GetDepend('NETWORK_SAMPLES_USING_TCP_CLIENT'):
    src += Glob('tcpclient/*.c')
    CPPPATH += [cwd + '/tcpclient']

if GetDepend('NETWORK_SAMPLES_USING_TCP_SERVER'):
    src += Glob('tcpserver/*.c')
    CPPPATH += [cwd + '/tcpserver']

if GetDepend('NETWORK_SAMPLES_USING_UDP_CLIENT'):
    src += Glob('udpclient/*.c')
    CPPPATH += [cwd + '/udpclient']

if GetDepend('NETWORK_SAMPLES_USING_UDP_SERVER'):
    src += Glob('udpserver/*.c')
    CPPPATH += [cwd + '/udpserver']

if GetDepend('NETWORK_SAMPLES_USING_TCP_CLIENT_SELECT'):
    src += Glob('tcpclient_select/*.c')
    CPPPATH += [cwd + '/tcpclient_select']

if GetDepend('NETWORK_SAMPLES_USING_HTTP_CLIENT'):
    src += Glob('httpclient/*.c')
    CPPPATH += [cwd + '/httpclient']

group = DefineGroup('network-samples', src, depend = ['PKG_USING_NETWORK_SAMPLES'], CPPPATH = CPPPATH)

Return('group')
