---
title: Bluetooth и привязка
description: Bluetooth использует функцию bind для привязки к сокету.
ms.assetid: 308d2680-de51-49e6-a0da-7aba494d9572
keywords:
- bind
- Bluetooth
- Bluetooth
- Bluetooth и привязка
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 12ccbd088ab61edcfa3dfc511ea591593d0cf781
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "103891032"
---
# <a name="bluetooth-and-bind"></a><span data-ttu-id="9ecf5-107">Bluetooth и привязка</span><span class="sxs-lookup"><span data-stu-id="9ecf5-107">Bluetooth and bind</span></span>

<span data-ttu-id="9ecf5-108">Bluetooth использует функцию [**BIND**](/windows/desktop/api/winsock/nf-winsock-bind) для привязки к сокету.</span><span class="sxs-lookup"><span data-stu-id="9ecf5-108">Bluetooth uses the [**bind**](/windows/desktop/api/winsock/nf-winsock-bind) function to bind to a socket.</span></span> <span data-ttu-id="9ecf5-109">Чтобы привязать сокет Bluetooth, вызовите функцию **BIND** с помощью структуры [**SOCKADDR \_ БС**](/windows/desktop/api/Ws2bth/ns-ws2bth-sockaddr_bth) .</span><span class="sxs-lookup"><span data-stu-id="9ecf5-109">To bind a Bluetooth socket, call the **bind** function using the [**SOCKADDR\_BTH**](/windows/desktop/api/Ws2bth/ns-ws2bth-sockaddr_bth) structure.</span></span> <span data-ttu-id="9ecf5-110">Используйте структуру **SOCKADDR \_ БС** со следующими параметрами:</span><span class="sxs-lookup"><span data-stu-id="9ecf5-110">Use the **SOCKADDR\_BTH** structure with the following settings:</span></span>

``` syntax
name.addressFamily = AF_BTH;
name.btAddr = 0;
name.serviceClassId = GUID_NULL;
name.port = number of service channel, 0 or BT_PORT_ANY;
```

<span data-ttu-id="9ecf5-111">Для клиентских приложений элемент порта должен быть равен нулю, чтобы обеспечить назначение соответствующей локальной конечной точки.</span><span class="sxs-lookup"><span data-stu-id="9ecf5-111">On client applications, the port member must be zero to enable an appropriate local endpoint to be assigned.</span></span> <span data-ttu-id="9ecf5-112">В серверных приложениях элемент порта должен быть допустимым номером порта или BT- \_ портом \_ ANY; порты, автоматически назначенные с помощью BT- \_ порта, \_ могут быть запрошены в дальнейшем при вызове функции [**жетсоккнаме**](bluetooth-and-getsockname.md) .</span><span class="sxs-lookup"><span data-stu-id="9ecf5-112">On server applications, the port member must be a valid port number or BT\_PORT\_ANY; ports automatically assigned using BT\_PORT\_ANY may be queried subsequently with a call to the [**getsockname**](bluetooth-and-getsockname.md) function.</span></span> <span data-ttu-id="9ecf5-113">Допустимый диапазон для запроса определенного порта RFCOMM — от 1 до 30.</span><span class="sxs-lookup"><span data-stu-id="9ecf5-113">The valid range for requesting a specific RFCOMM port is 1 through 30.</span></span> <span data-ttu-id="9ecf5-114">Каналы сервера являются глобальными ресурсами, и для RFCOMM на любом устройстве Bluetooth доступно только 30 каналов сервера, которые должны быть общими для всех сокетов Windows, принадлежащих семейству адресов Bluetooth.</span><span class="sxs-lookup"><span data-stu-id="9ecf5-114">Server channels are global resource, and only 30 server channels are available for RFCOMM on any Bluetooth device, which must be shared by all Windows Sockets that belong to the Bluetooth address family.</span></span> <span data-ttu-id="9ecf5-115">Если канал сервера недоступен или указанный канал сервера уже зарезервирован, вызов [**привязки**](/windows/desktop/api/winsock/nf-winsock-bind) завершается ошибкой.</span><span class="sxs-lookup"><span data-stu-id="9ecf5-115">If no server channel is available, or if the specified server channel is already reserved, the [**bind**](/windows/desktop/api/winsock/nf-winsock-bind) call fails.</span></span>

<span data-ttu-id="9ecf5-116">После успешного возврата из BIND канал сервера резервируется до закрытия сокета.</span><span class="sxs-lookup"><span data-stu-id="9ecf5-116">Upon successful return from bind, the server channel is reserved until the socket is closed.</span></span> <span data-ttu-id="9ecf5-117">Используйте функцию [**жетсоккнаме**](bluetooth-and-getsockname.md) , чтобы получить номер канала для регистрации SDP.</span><span class="sxs-lookup"><span data-stu-id="9ecf5-117">Use the [**getsockname**](bluetooth-and-getsockname.md) function to retrieve the channel number for SDP registration.</span></span>

<span data-ttu-id="9ecf5-118">Приложения должны использовать автоматическое выделение для канала сервера.</span><span class="sxs-lookup"><span data-stu-id="9ecf5-118">Applications should use auto-allocation for the server channel.</span></span>

<span data-ttu-id="9ecf5-119">Функция [**BIND**](/windows/desktop/api/winsock/nf-winsock-bind) не объявляет серверное приложение автоматически с помощью средства распространения Bluetooth. приложения должны вызывать функцию [**всасетсервице**](/windows/desktop/api/winsock2/nf-winsock2-wsasetservicea) для обнаружения удаленными приложениями Bluetooth.</span><span class="sxs-lookup"><span data-stu-id="9ecf5-119">The [**bind**](/windows/desktop/api/winsock/nf-winsock-bind) function does not automatically advertise the server application using the Bluetooth SDP; applications must call the [**WSASetService**](/windows/desktop/api/winsock2/nf-winsock2-wsasetservicea) function to be found by remote Bluetooth applications.</span></span>

## <a name="related-topics"></a><span data-ttu-id="9ecf5-120">См. также</span><span class="sxs-lookup"><span data-stu-id="9ecf5-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9ecf5-121">Сокеты Windows</span><span class="sxs-lookup"><span data-stu-id="9ecf5-121">Windows Sockets</span></span>](/windows/desktop/WinSock/windows-sockets-start-page-2)
</dt> <dt>

[<span data-ttu-id="9ecf5-122">**выполняется**</span><span class="sxs-lookup"><span data-stu-id="9ecf5-122">**bind**</span></span>](/windows/desktop/api/winsock/nf-winsock-bind)
</dt> </dl>

 

 