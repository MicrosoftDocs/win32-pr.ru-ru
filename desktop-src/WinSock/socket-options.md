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
# <a name="socket-options"></a><span data-ttu-id="056a6-103">Параметры сокета</span><span class="sxs-lookup"><span data-stu-id="056a6-103">Socket Options</span></span>

<span data-ttu-id="056a6-104">В этом разделе описываются параметры сокетов Winsock для различных выпусков операционных систем Windows.</span><span class="sxs-lookup"><span data-stu-id="056a6-104">This section describes Winsock Socket Options for various editions of Windows operating systems.</span></span> <span data-ttu-id="056a6-105">Используйте функции [**жетсоккопт**](/windows/desktop/api/winsock/nf-winsock-getsockopt) и [**сетсоккопт**](/windows/desktop/api/winsock/nf-winsock-setsockopt) для получения дополнительных сведений о параметрах сокета.</span><span class="sxs-lookup"><span data-stu-id="056a6-105">Use the [**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt) and [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) functions for more getting and setting socket options.</span></span> <span data-ttu-id="056a6-106">Чтобы перечислить протоколы и обнаружить Поддерживаемые свойства для каждого установленного протокола, используйте функцию [**всаенумпротоколс**](/windows/desktop/api/Winsock2/nf-winsock2-wsaenumprotocolsa) .</span><span class="sxs-lookup"><span data-stu-id="056a6-106">To enumerate protocols and discover supported properties for each installed protocol, use the [**WSAEnumProtocols**](/windows/desktop/api/Winsock2/nf-winsock2-wsaenumprotocolsa) function.</span></span>

<span data-ttu-id="056a6-107">Для некоторых параметров сокета требуется больше объяснений, чем может передать таблица. такие параметры содержат ссылки на дополнительные страницы.</span><span class="sxs-lookup"><span data-stu-id="056a6-107">Some socket options require more explanation than these tables can convey; such options contain links to additional pages.</span></span>

<dl> <dt>

<span data-ttu-id="056a6-108"><span id="IPPROTO_IP"></span><span id="ipproto_ip"></span>**ИППРОТО \_ IP-адрес**</span><span class="sxs-lookup"><span data-stu-id="056a6-108"><span id="IPPROTO_IP"></span><span id="ipproto_ip"></span>**IPPROTO\_IP**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="056a6-109">Параметры сокета, применимые на уровне IPv4.</span><span class="sxs-lookup"><span data-stu-id="056a6-109">Socket options applicable at the IPv4 level.</span></span> <span data-ttu-id="056a6-110">Дополнительные сведения см. в разделе [**\_ Параметры IP-сокета иппрото**](ipproto-ip-socket-options.md).</span><span class="sxs-lookup"><span data-stu-id="056a6-110">For more information, see the [**IPPROTO\_IP Socket Options**](ipproto-ip-socket-options.md).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="056a6-111"><span id="IPPROTO_IPV6"></span><span id="ipproto_ipv6"></span>**ИППРОТО \_ IPv6**</span><span class="sxs-lookup"><span data-stu-id="056a6-111"><span id="IPPROTO_IPV6"></span><span id="ipproto_ipv6"></span>**IPPROTO\_IPV6**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="056a6-112">Параметры сокета, применимые на уровне IPv6.</span><span class="sxs-lookup"><span data-stu-id="056a6-112">Socket options applicable at the IPv6 level.</span></span> <span data-ttu-id="056a6-113">Дополнительные сведения см. в разделе [**\_ параметры сокета иппрото IPv6**](ipproto-ipv6-socket-options.md).</span><span class="sxs-lookup"><span data-stu-id="056a6-113">For more information, see the [**IPPROTO\_IPV6 Socket Options**](ipproto-ipv6-socket-options.md).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="056a6-114"><span id="IPPROTO_RM"></span><span id="ipproto_rm"></span>**ИППРОТО \_ RM**</span><span class="sxs-lookup"><span data-stu-id="056a6-114"><span id="IPPROTO_RM"></span><span id="ipproto_rm"></span>**IPPROTO\_RM**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="056a6-115">Параметры сокета, применимые на надежном уровне многоадресной рассылки.</span><span class="sxs-lookup"><span data-stu-id="056a6-115">Socket options applicable at the reliable multicast level.</span></span> <span data-ttu-id="056a6-116">Дополнительные сведения см. в разделе [**\_ параметры сокета иппрото RM**](ipproto-rm-socket-options.md).</span><span class="sxs-lookup"><span data-stu-id="056a6-116">For more information, see the [**IPPROTO\_RM Socket Options**](ipproto-rm-socket-options.md).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="056a6-117"><span id="IPPROTO_TCP"></span><span id="ipproto_tcp"></span>**ИППРОТО \_ TCP**</span><span class="sxs-lookup"><span data-stu-id="056a6-117"><span id="IPPROTO_TCP"></span><span id="ipproto_tcp"></span>**IPPROTO\_TCP**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="056a6-118">Параметры сокета, применимые на уровне TCP.</span><span class="sxs-lookup"><span data-stu-id="056a6-118">Socket options applicable at the TCP level.</span></span> <span data-ttu-id="056a6-119">Дополнительные сведения см. в разделе [**\_ параметры TCP-сокета иппрото**](ipproto-tcp-socket-options.md).</span><span class="sxs-lookup"><span data-stu-id="056a6-119">For more information, see the [**IPPROTO\_TCP Socket Options**](ipproto-tcp-socket-options.md).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="056a6-120"><span id="IPPROTO_UDP"></span><span id="ipproto_udp"></span>**ИППРОТО \_ UDP**</span><span class="sxs-lookup"><span data-stu-id="056a6-120"><span id="IPPROTO_UDP"></span><span id="ipproto_udp"></span>**IPPROTO\_UDP**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="056a6-121">Параметры сокета, применимые на уровне UDP.</span><span class="sxs-lookup"><span data-stu-id="056a6-121">Socket options applicable at the UDP level.</span></span> <span data-ttu-id="056a6-122">Дополнительные сведения см. в разделе [**\_ параметры сокета иппрото UDP**](ipproto-udp-socket-options.md).</span><span class="sxs-lookup"><span data-stu-id="056a6-122">For more information, see the [**IPPROTO\_UDP Socket Options**](ipproto-udp-socket-options.md).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="056a6-123"><span id="NSPROTO_IPX"></span><span id="nsproto_ipx"></span>**НСПРОТО \_ IPX**</span><span class="sxs-lookup"><span data-stu-id="056a6-123"><span id="NSPROTO_IPX"></span><span id="nsproto_ipx"></span>**NSPROTO\_IPX**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="056a6-124">Параметры сокета, применимые на уровне IPX.</span><span class="sxs-lookup"><span data-stu-id="056a6-124">Socket options applicable at the IPX level.</span></span> <span data-ttu-id="056a6-125">Дополнительные сведения см. в разделе [**\_ параметры сокета нспрото IPX**](nsproto-ipx-socket-options.md).</span><span class="sxs-lookup"><span data-stu-id="056a6-125">For more information, see the [**NSPROTO\_IPX Socket Options**](nsproto-ipx-socket-options.md).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="056a6-126"><span id="SOL_APPLETALK"></span><span id="sol_appletalk"></span>**SOL \_ APPLETALK**</span><span class="sxs-lookup"><span data-stu-id="056a6-126"><span id="SOL_APPLETALK"></span><span id="sol_appletalk"></span>**SOL\_APPLETALK**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="056a6-127">Параметры сокета, применимые на уровне AppleTalk.</span><span class="sxs-lookup"><span data-stu-id="056a6-127">Socket options applicable at the AppleTalk level.</span></span> <span data-ttu-id="056a6-128">Дополнительные сведения см. в разделе [**\_ параметры сокета Sol APPLETALK**](sol-appletalk-socket-options.md).</span><span class="sxs-lookup"><span data-stu-id="056a6-128">For more information, see the [**SOL\_APPLETALK Socket Options**](sol-appletalk-socket-options.md).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="056a6-129"><span id="SOL_IRLMP"></span><span id="sol_irlmp"></span>**\_ИРЛМП Sol**</span><span class="sxs-lookup"><span data-stu-id="056a6-129"><span id="SOL_IRLMP"></span><span id="sol_irlmp"></span>**SOL\_IRLMP**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="056a6-130">Параметры сокета, применимые на уровне протокола управления инфракрасными каналами.</span><span class="sxs-lookup"><span data-stu-id="056a6-130">Socket options applicable at the InfraRed Link Management Protocol level.</span></span> <span data-ttu-id="056a6-131">Дополнительные сведения см. в разделе [**\_ параметры соединителя Sol ирлмп**](sol-irlmp-socket-options.md).</span><span class="sxs-lookup"><span data-stu-id="056a6-131">For more information, see the [**SOL\_IRLMP Socket Options**](sol-irlmp-socket-options.md).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="056a6-132"><span id="SOL_SOCKET"></span><span id="sol_socket"></span>**\_сокет Sol**</span><span class="sxs-lookup"><span data-stu-id="056a6-132"><span id="SOL_SOCKET"></span><span id="sol_socket"></span>**SOL\_SOCKET**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="056a6-133">Параметры сокета, применимые на уровне сокета.</span><span class="sxs-lookup"><span data-stu-id="056a6-133">Socket options applicable at the socket level.</span></span> <span data-ttu-id="056a6-134">Дополнительные сведения см. в разделе [**\_ параметры сокета сокета Sol**](sol-socket-socket-options.md).</span><span class="sxs-lookup"><span data-stu-id="056a6-134">For more information, see the [**SOL\_SOCKET Socket Options**](sol-socket-socket-options.md).</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="056a6-135">Комментарии</span><span class="sxs-lookup"><span data-stu-id="056a6-135">Remarks</span></span>

<span data-ttu-id="056a6-136">Все эти \_ \* параметры сокета применяются одинаково к IPv4 и IPv6 (за исключением \_ вещания, так как вещание не реализовано в IPv6).</span><span class="sxs-lookup"><span data-stu-id="056a6-136">All SO\_\* socket options apply equally to IPv4 and IPv6 (except SO\_BROADCAST, since broadcast is not implemented in IPv6).</span></span>

 

 



