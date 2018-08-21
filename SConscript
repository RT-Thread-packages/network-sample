from building import *
Import('rtconfig')

src   = []
cwd   = GetCurrentDir()
group = []
CPPPATH = []

# add network samples.
if GetDepend('NETWORK_SAMPLES_USING_TCP_CLIENT'):
    src += ['tcpclient/tcpclient.c']
    CPPPATH += [cwd + '/tcpclient']

if GetDepend('NETWORK_SAMPLES_USING_TCP_SERVER'):
    src += ['tcpserver/tcpserver.c']
    CPPPATH += [cwd + '/tcpserver']

if GetDepend('NETWORK_SAMPLES_USING_UDP_CLIENT'):
    src += ['udpclient/udpclient.c']
    CPPPATH += [cwd + '/udpclient']

if GetDepend('NETWORK_SAMPLES_USING_UDP_SERVER'):
    src += ['udpserver/udpserver.c']
    CPPPATH += [cwd + '/udpserver']

if GetDepend('NETWORK_SAMPLES_USING_TCP_CLIENT_SELECT'):
    src += ['tcpclient_select/tcpclient_select.c']
    CPPPATH += [cwd + '/tcpclient_select']

if GetDepend('NETWORK_SAMPLES_USING_HTTP_CLIENT'):
    src += ['httpclient/httpclient.c']
    CPPPATH += [cwd + '/httpclient']

group = DefineGroup('network-samples', src, depend = ['PKG_USING_NETWORK_SAMPLES'], CPPPATH = CPPPATH)

Return('group')
