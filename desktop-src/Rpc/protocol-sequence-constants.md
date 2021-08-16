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
ms.openlocfilehash: 72c28486bfa3981870ac331ae83f0cbb532bba4d27c44062ce902823e4e3c259
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118927141"
---
# <a name="protocol-sequence-constants"></a>Константы последовательности протоколов

Microsoft RPC поддерживает следующие последовательности протоколов.



| Константа/значение                                                                                                                                                                                                                                                                                 | Описание                                                                                                                                                                         |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="ncacn_nb_tcp"></span><span id="NCACN_NB_TCP"></span><dl> Протокол TCP, <dt>ориентированный на подключение (</dt> <dt>**нкакн \_ \_**</dt> ) </dl>          | только клиент: MS-DOS, Windows 3. *x* клиент и сервер: Windows Server 2003, Windows XP, Windows 2000, Windows NT<br/>                                                          |
| <span id="ncacn_nb_ipx"></span><span id="NCACN_NB_IPX"></span><dl> нкакн <dt>netbios, ориентированный на подключение ipx через Internet Packet Exchange (ipx)</dt> <dt>**\_ \_**</dt> </dl>               | только клиент: MS-DOS, Windows 3. *x* клиент и сервер: Windows Server 2003, Windows XP, Windows 2000, Windows NT<br/>                                                          |
| <span id="ncacn_nb_nb"></span><span id="NCACN_NB_NB"></span><dl> <dt>Расширенный пользовательский интерфейс NetBIOS (NetBEUI) нкакн NetBIOS, ориентированный на подключение</dt> <dt>**\_ \_**</dt> </dl>                    | только клиент: MS-DOS, Windows 3. *x* Client and Server: Windows Server 2003, Windows XP, Windows 2000, Windows NT, Windows Me, Windows 98, Windows 95<br/>                      |
| <span id="ncacn_ip_tcp"></span><span id="NCACN_IP_TCP"></span><dl> <dt>**протокол \_ \_ TCP**</dt> /IP, <dt>ориентированный на подключение через</dt> IP нкакн </dl>  | только клиент: MS-DOS, Windows 3. *x* и клиент Apple Macintosh и сервер: Windows Server 2003, Windows XP, Windows 2000, Windows NT, Windows Me, Windows 98, Windows 95<br/> |
| <span id="ncacn_np"></span><span id="NCACN_NP"></span><dl> <dt>именованные каналы</dt> <dt>**нкакн \_ NP**</dt> с ориентацией на подключения </dl>                                                            | только клиент: MS-DOS, Windows 3. *x*, Windows 95 клиент и сервер: Windows Server 2003, Windows XP, Windows 2000, Windows NT<br/>                                              |
| <span id="ncacn_spx"></span><span id="NCACN_SPX"></span><dl> <dt>**нкакн \_ spx**</dt> <dt>-ориентированный пакетный Exchange (spx)</dt> </dl>                                     | только клиент: MS-DOS, Windows 3. *x* Client and Server: Windows Server 2003, Windows XP, Windows 2000, Windows NT, Windows Me, Windows 98, Windows 95<br/>                      |
| <span id="ncacn_dnet_nsp"></span><span id="NCACN_DNET_NSP"></span><dl> <dt>**нкакн \_ днет \_ NSP**</dt> , <dt>ориентированный на подключение, транспорт DECnet</dt> </dl>                                    | только клиент: MS-DOS, Windows 3. *x*<br/>                                                                                                                                       |
| <span id="ncacn_at_dsp"></span><span id="NCACN_AT_DSP"></span><dl> <dt>**нкакн \_ в \_ DSP**</dt> с <dt>ориентацией на соединения (AppleTalk), ориентированный на соединение</dt> </dl>                                             | клиент: сервер Apple Macintosh: Windows server 2003, Windows XP, Windows 2000, Windows NT<br/>                                                                                |
| <span id="ncacn_vns_spp"></span><span id="NCACN_VNS_SPP"></span><dl> Транспорт <dt>**нкакн \_ ВНС \_ SPP**</dt> , <dt>ориентированный на подключение, масштабируемый параллельной обработки (SPP)</dt> </dl>     | только клиент: MS-DOS, Windows 3. *x* клиент и сервер: Windows Server 2003, Windows XP, Windows 2000, Windows NT<br/>                                                          |
| <span id="ncadg_ip_udp"></span><span id="NCADG_IP_UDP"></span><dl> <dt>**нкадг \_ IP \_ UDP**</dt> <dt>Datagram (без подключения) протокол датаграммы пользователя (UDP/IP)</dt> </dl>   | только клиент: MS-DOS, Windows 3. *x* клиент и сервер: Windows Server 2003, Windows XP, Windows 2000, Windows NT<br/>                                                          |
| <span id="ncadg_ipx"></span><span id="NCADG_IPX"></span><dl> <dt>**\_**</dt> <dt>IPX-датаграмма нкадг (без подключения)</dt> </dl>                                                           | только клиент: MS-DOS, Windows 3. *x* клиент и сервер: Windows Server 2003, Windows XP, Windows 2000, Windows NT<br/>                                                          |
| <span id="ncadg_mq"></span><span id="NCADG_MQ"></span><dl> <dt>**нкадг \_ MQ**</dt> <dt>Datagram (без подключения) на сервере очереди сообщений Майкрософт (MSMQ)</dt> </dl>                   | только клиент: Windows Me/98/95 client and Server: Windows Server 2003, Windows XP, Windows 2000, Windows NT server 4,0 с пакетом обновления 3 (SP3) и более поздних версий<br/>                                 |
| <span id="ncacn_http"></span><span id="NCACN_HTTP"></span><dl> <dt>**НКАКН \_**</dt> <dt>TCP/IP, ориентированный на HTTP-подключение, с помощью сервера Microsoft Internet Information Server в качестве прокси-сервера HTTP</dt> </dl> | только клиент: Windows Me/98/95 client and server: Windows Server 2003, Windows XP, Windows 2000<br/>                                                                           |
| <span id="ncalrpc"></span><span id="NCALRPC"></span><dl> <dt>**нкалрпк**</dt> <dt>вызов локальной процедуры</dt> </dl>                                                                           | клиент и сервер: Windows Server 2003, Windows XP, Windows 2000, Windows NT, Windows Me, Windows 98, Windows 95<br/>                                                         |



## <a name="remarks"></a>Remarks

Транспорт [**нкалрпк**](/windows/desktop/Midl/ncalrpc) поддерживает \_ \_ \_ только проверку подлинности RPC C AUTHN Winnt. Дополнительные сведения см. в разделе [Безопасность](security.md) и [константы службы проверки подлинности](authentication-service-constants.md).

Microsoft RPC поддерживает [**рпкбиндингкопи**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingcopy) только в клиентских приложениях, а не в серверных приложениях.

 

