---
title: Bluetooth и функцию getaddrinfo
description: Функция функцию getaddrinfo предоставляет преобразование из имени узла в адрес для транспортов на основе IP-адресов. Поскольку функция функцию getaddrinfo относится только к транспортам на основе IP-адресов, она завершается сбоем на сокетах Bluetooth.
ms.assetid: e17d8542-d4bc-499c-bae4-1f41bff493c3
keywords:
- Bluetooth и функцию getaddrinfo Bluetooth
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 96c2e62b83ac947b74479ff435b93914661aa8da
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "103793537"
---
# <a name="bluetooth-and-getaddrinfo"></a><span data-ttu-id="d52bf-105">Bluetooth и функцию getaddrinfo</span><span class="sxs-lookup"><span data-stu-id="d52bf-105">Bluetooth and getaddrinfo</span></span>

<span data-ttu-id="d52bf-106">Функция [**функцию getaddrinfo**](/windows/desktop/api/ws2tcpip/nf-ws2tcpip-getaddrinfo) предоставляет преобразование из имени узла в адрес для транспортов на основе IP-адресов.</span><span class="sxs-lookup"><span data-stu-id="d52bf-106">The [**getaddrinfo**](/windows/desktop/api/ws2tcpip/nf-ws2tcpip-getaddrinfo) function provides translation from host name to address for IP-based transports.</span></span> <span data-ttu-id="d52bf-107">Поскольку функция **функцию getaddrinfo** относится только к транспортам на основе IP-адресов, она завершается сбоем на сокетах Bluetooth.</span><span class="sxs-lookup"><span data-stu-id="d52bf-107">Because the **getaddrinfo** function is specific to IP-based transports, it fails on Bluetooth sockets.</span></span>

<span data-ttu-id="d52bf-108">Чтобы выполнить преобразование из имени узла в адрес для сокетов Bluetooth, используйте функцию [**всалукупсервицебегин**](bluetooth-and-wsalookupservicebegin-for-device-inquiry.md) с **\_ контейнерами Луп** для запроса удаленных устройств, а затем найдите конкретное соответствующее удаленное имя и соответствующий адрес.</span><span class="sxs-lookup"><span data-stu-id="d52bf-108">To perform translation from host name to address for Bluetooth sockets, use the [**WSALookupServiceBegin**](bluetooth-and-wsalookupservicebegin-for-device-inquiry.md) function with **LUP\_CONTAINERS** to query remote devices, then search for a specific matching Remote Name and corresponding address.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d52bf-109">См. также</span><span class="sxs-lookup"><span data-stu-id="d52bf-109">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d52bf-110">Сокеты Windows</span><span class="sxs-lookup"><span data-stu-id="d52bf-110">Windows Sockets</span></span>](/windows/desktop/WinSock/windows-sockets-start-page-2)
</dt> <dt>

[<span data-ttu-id="d52bf-111">**функцию getaddrinfo**</span><span class="sxs-lookup"><span data-stu-id="d52bf-111">**getaddrinfo**</span></span>](/windows/desktop/api/ws2tcpip/nf-ws2tcpip-getaddrinfo)
</dt> <dt>

[<span data-ttu-id="d52bf-112">**всалукупсервицебегин**</span><span class="sxs-lookup"><span data-stu-id="d52bf-112">**WSALookupServiceBegin**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicebegina)
</dt> </dl>

 

 