---
title: Константы последовательности протоколов
description: Microsoft RPC поддерживает следующие последовательности протоколов.
ms.assetid: 51284532-b0ac-4bf2-b322-91393b2b9dc6
topic_type:
- apiref
api_name:
- ncacn_nb_tcp
- ncacn_nb_ipx
- ncacn_nb_nb
- ncacn_ip_tcp
- ncacn_np
- ncacn_spx
- ncacn_dnet_nsp
- ncacn_at_dsp
- ncacn_vns_spp
- ncadg_ip_udp
- ncadg_ipx
- ncadg_mq
- ncacn_http
- ncalrpc
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 7e2dd716cdd969040f5315ef05200912acc54878
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104070450"
---
# <a name="protocol-sequence-constants"></a>Константы последовательности протоколов

Microsoft RPC поддерживает следующие последовательности протоколов.



| Константа/значение                                                                                                                                                                                                                                                                                 | Описание                                                                                                                                                                         |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="ncacn_nb_tcp"></span><span id="NCACN_NB_TCP"></span><dl> Протокол TCP, <dt>ориентированный на подключение (</dt> <dt>**нкакн \_ \_**</dt> ) </dl>          | Только клиент: MS-DOS, Windows 3. *x* клиент и сервер: windows Server 2003, Windows XP, Windows 2000, Windows NT<br/>                                                          |
| <span id="ncacn_nb_ipx"></span><span id="NCACN_NB_IPX"></span><dl> <dt>**нкакн \_ с \_ IPX**</dt> <dt>-ориентированным подключением NetBIOS через Internet Packet Exchange (IPX)</dt> </dl>               | Только клиент: MS-DOS, Windows 3. *x* клиент и сервер: windows Server 2003, Windows XP, Windows 2000, Windows NT<br/>                                                          |
| <span id="ncacn_nb_nb"></span><span id="NCACN_NB_NB"></span><dl> <dt>Расширенный пользовательский интерфейс NetBIOS (NetBEUI) нкакн NetBIOS, ориентированный на подключение</dt> <dt>**\_ \_**</dt> </dl>                    | Только клиент: MS-DOS, Windows 3. *x* Client and Server: windows Server 2003, Windows XP, Windows 2000, Windows NT, Windows Me, Windows 98, Windows 95<br/>                      |
| <span id="ncacn_ip_tcp"></span><span id="NCACN_IP_TCP"></span><dl> <dt>**протокол \_ \_ TCP**</dt> /IP, <dt>ориентированный на подключение через</dt> IP нкакн </dl>  | Только клиент: MS-DOS, Windows 3. *x*, клиент и сервер Apple Macintosh: windows Server 2003, Windows XP, Windows 2000, Windows NT, Windows Me, Windows 98, Windows 95<br/> |
| <span id="ncacn_np"></span><span id="NCACN_NP"></span><dl> <dt>именованные каналы</dt> <dt>**нкакн \_ NP**</dt> с ориентацией на подключения </dl>                                                            | Только клиент: MS-DOS, Windows 3. *x*, клиент и сервер Windows 95: windows Server 2003, Windows XP, Windows 2000, Windows NT<br/>                                              |
| <span id="ncacn_spx"></span><span id="NCACN_SPX"></span><dl> <dt>**нкакн \_ SPX**</dt> <dt>— ориентированный на подключение протокол обмена пакетами (SPX)</dt> </dl>                                     | Только клиент: MS-DOS, Windows 3. *x* Client and Server: windows Server 2003, Windows XP, Windows 2000, Windows NT, Windows Me, Windows 98, Windows 95<br/>                      |
| <span id="ncacn_dnet_nsp"></span><span id="NCACN_DNET_NSP"></span><dl> <dt>**нкакн \_ днет \_ NSP**</dt> , <dt>ориентированный на подключение, транспорт DECnet</dt> </dl>                                    | Только клиент: MS-DOS, Windows 3. *x*<br/>                                                                                                                                       |
| <span id="ncacn_at_dsp"></span><span id="NCACN_AT_DSP"></span><dl> <dt>**нкакн \_ в \_ DSP**</dt> с <dt>ориентацией на соединения (AppleTalk), ориентированный на соединение</dt> </dl>                                             | Клиент: сервер Apple Macintosh: Windows Server 2003, Windows XP, Windows 2000, Windows NT<br/>                                                                                |
| <span id="ncacn_vns_spp"></span><span id="NCACN_VNS_SPP"></span><dl> Транспорт <dt>**нкакн \_ ВНС \_ SPP**</dt> , <dt>ориентированный на подключение, масштабируемый параллельной обработки (SPP)</dt> </dl>     | Только клиент: MS-DOS, Windows 3. *x* клиент и сервер: windows Server 2003, Windows XP, Windows 2000, Windows NT<br/>                                                          |
| <span id="ncadg_ip_udp"></span><span id="NCADG_IP_UDP"></span><dl> <dt>**нкадг \_ IP \_ UDP**</dt> <dt>Datagram (без подключения) протокол датаграммы пользователя (UDP/IP)</dt> </dl>   | Только клиент: MS-DOS, Windows 3. *x* клиент и сервер: windows Server 2003, Windows XP, Windows 2000, Windows NT<br/>                                                          |
| <span id="ncadg_ipx"></span><span id="NCADG_IPX"></span><dl> <dt>**\_**</dt> <dt>IPX-датаграмма нкадг (без подключения)</dt> </dl>                                                           | Только клиент: MS-DOS, Windows 3. *x* клиент и сервер: windows Server 2003, Windows XP, Windows 2000, Windows NT<br/>                                                          |
| <span id="ncadg_mq"></span><span id="NCADG_MQ"></span><dl> <dt>**нкадг \_ MQ**</dt> <dt>Datagram (без подключения) на сервере очереди сообщений Майкрософт (MSMQ)</dt> </dl>                   | Только клиент: Windows Me/98/95 клиент и сервер: Windows Server 2003, Windows XP, Windows 2000, Windows NT Server 4,0 с пакетом обновления 3 (SP3) и более поздние версии<br/>                                 |
| <span id="ncacn_http"></span><span id="NCACN_HTTP"></span><dl> <dt>**НКАКН \_**</dt> <dt>TCP/IP, ориентированный на HTTP-подключение, с помощью сервера Microsoft Internet Information Server в качестве прокси-сервера HTTP</dt> </dl> | Только клиент: Windows Me/98/95 клиент и сервер: Windows Server 2003, Windows XP, Windows 2000<br/>                                                                           |
| <span id="ncalrpc"></span><span id="NCALRPC"></span><dl> <dt>**нкалрпк**</dt> <dt>вызов локальной процедуры</dt> </dl>                                                                           | Клиент и сервер: Windows Server 2003, Windows XP, Windows 2000, Windows NT, Windows Me, Windows 98, Windows 95<br/>                                                         |



## <a name="remarks"></a>Комментарии

Транспорт [**нкалрпк**](/windows/desktop/Midl/ncalrpc) поддерживает \_ \_ \_ только проверку подлинности RPC C AUTHN Winnt. Дополнительные сведения см. в разделе [Безопасность](security.md) и [константы службы проверки подлинности](authentication-service-constants.md).

Microsoft RPC поддерживает [**рпкбиндингкопи**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingcopy) только в клиентских приложениях, а не в серверных приложениях.

 

