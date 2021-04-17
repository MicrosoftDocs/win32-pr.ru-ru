---
description: Страница навигации для параметров сокета Windows Sockets (Winsock).
ms.assetid: e2831f76-4499-45b6-bc60-2908ec3a246c
title: Параметры сокета
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPPROTO_IP
- IPPROTO_IPV6
- IPPROTO_RM
- IPPROTO_TCP
- IPPROTO_UDP
- NSPROTO_IPX
- SOL_APPLETALK
- SOL_IRLMP
- SOL_SOCKET
api_type:
- NA
api_location: ''
ms.openlocfilehash: 805f779965afc808e32952b58815c7b6bc528fbc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105711017"
---
# <a name="socket-options"></a>Параметры сокета

В этом разделе описываются параметры сокетов Winsock для различных выпусков операционных систем Windows. Используйте функции [**жетсоккопт**](/windows/desktop/api/winsock/nf-winsock-getsockopt) и [**сетсоккопт**](/windows/desktop/api/winsock/nf-winsock-setsockopt) для получения дополнительных сведений о параметрах сокета. Чтобы перечислить протоколы и обнаружить Поддерживаемые свойства для каждого установленного протокола, используйте функцию [**всаенумпротоколс**](/windows/desktop/api/Winsock2/nf-winsock2-wsaenumprotocolsa) .

Для некоторых параметров сокета требуется больше объяснений, чем может передать таблица. такие параметры содержат ссылки на дополнительные страницы.

<dl> <dt>

<span id="IPPROTO_IP"></span><span id="ipproto_ip"></span>**ИППРОТО \_ IP-адрес**
</dt> <dd> <dl> <dt>



Параметры сокета, применимые на уровне IPv4. Дополнительные сведения см. в разделе [**\_ Параметры IP-сокета иппрото**](ipproto-ip-socket-options.md).


</dt> </dl> </dd> <dt>

<span id="IPPROTO_IPV6"></span><span id="ipproto_ipv6"></span>**ИППРОТО \_ IPv6**
</dt> <dd> <dl> <dt>



Параметры сокета, применимые на уровне IPv6. Дополнительные сведения см. в разделе [**\_ параметры сокета иппрото IPv6**](ipproto-ipv6-socket-options.md).


</dt> </dl> </dd> <dt>

<span id="IPPROTO_RM"></span><span id="ipproto_rm"></span>**ИППРОТО \_ RM**
</dt> <dd> <dl> <dt>



Параметры сокета, применимые на надежном уровне многоадресной рассылки. Дополнительные сведения см. в разделе [**\_ параметры сокета иппрото RM**](ipproto-rm-socket-options.md).


</dt> </dl> </dd> <dt>

<span id="IPPROTO_TCP"></span><span id="ipproto_tcp"></span>**ИППРОТО \_ TCP**
</dt> <dd> <dl> <dt>



Параметры сокета, применимые на уровне TCP. Дополнительные сведения см. в разделе [**\_ параметры TCP-сокета иппрото**](ipproto-tcp-socket-options.md).


</dt> </dl> </dd> <dt>

<span id="IPPROTO_UDP"></span><span id="ipproto_udp"></span>**ИППРОТО \_ UDP**
</dt> <dd> <dl> <dt>



Параметры сокета, применимые на уровне UDP. Дополнительные сведения см. в разделе [**\_ параметры сокета иппрото UDP**](ipproto-udp-socket-options.md).


</dt> </dl> </dd> <dt>

<span id="NSPROTO_IPX"></span><span id="nsproto_ipx"></span>**НСПРОТО \_ IPX**
</dt> <dd> <dl> <dt>



Параметры сокета, применимые на уровне IPX. Дополнительные сведения см. в разделе [**\_ параметры сокета нспрото IPX**](nsproto-ipx-socket-options.md).


</dt> </dl> </dd> <dt>

<span id="SOL_APPLETALK"></span><span id="sol_appletalk"></span>**SOL \_ APPLETALK**
</dt> <dd> <dl> <dt>



Параметры сокета, применимые на уровне AppleTalk. Дополнительные сведения см. в разделе [**\_ параметры сокета Sol APPLETALK**](sol-appletalk-socket-options.md).


</dt> </dl> </dd> <dt>

<span id="SOL_IRLMP"></span><span id="sol_irlmp"></span>**\_ИРЛМП Sol**
</dt> <dd> <dl> <dt>



Параметры сокета, применимые на уровне протокола управления инфракрасными каналами. Дополнительные сведения см. в разделе [**\_ параметры соединителя Sol ирлмп**](sol-irlmp-socket-options.md).


</dt> </dl> </dd> <dt>

<span id="SOL_SOCKET"></span><span id="sol_socket"></span>**\_сокет Sol**
</dt> <dd> <dl> <dt>



Параметры сокета, применимые на уровне сокета. Дополнительные сведения см. в разделе [**\_ параметры сокета сокета Sol**](sol-socket-socket-options.md).


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Комментарии

Все эти \_ \* параметры сокета применяются одинаково к IPv4 и IPv6 (за исключением \_ вещания, так как вещание не реализовано в IPv6).

 

 



