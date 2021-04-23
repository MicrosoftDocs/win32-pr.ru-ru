---
description: Сокеты Windows (Winsock) и возможности многоадресной рассылки с использованием независимых от протокола MultiPoint.
ms.assetid: 861f457c-fe7e-4128-a3f3-786424a96ea5
title: Protocol-Independent многоадресной рассылки и MultiPoint в SPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bda9e5cab1b790a1e2d2c64c4451063a94dd8bc9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104156022"
---
# <a name="protocol-independent-multicast-and-multipoint-in-the-spi"></a><span data-ttu-id="9ed70-103">Protocol-Independent многоадресной рассылки и MultiPoint в SPI</span><span class="sxs-lookup"><span data-stu-id="9ed70-103">Protocol-Independent Multicast and Multipoint in the SPI</span></span>

<span data-ttu-id="9ed70-104">Так же, как сокеты Windows 2 позволяют доступ к базовым возможностям транспорта данных многих транспортных протоколов в общем виде, он также предоставляет универсальный способ использования возможностей MultiPoint и многоадресной рассылки для транспортов, реализующих эти функции.</span><span class="sxs-lookup"><span data-stu-id="9ed70-104">Just as Windows Sockets 2 allows the basic data transport capabilities of numerous transport protocols to be accessed in a generic manner, it also provides a generic way to use multipoint and multicast capabilities of transports that implement these features.</span></span> <span data-ttu-id="9ed70-105">Для упрощения термина *MultiPoint* используется в дальнейшем для ссылки на многоадресную и MultiPoint связь.</span><span class="sxs-lookup"><span data-stu-id="9ed70-105">To simplify, the term *multipoint* is used hereafter to refer to both multicast and multipoint communications.</span></span>

<span data-ttu-id="9ed70-106">Текущие реализации MultiPoint (например, многоадресная рассылка IP-адресов, ST-II, T. 120, ATM UNI) могут сильно различаться в отношении того, как узлы присоединяются к сеансу MultiPoint, определен ли конкретный узел как Центральный или корневой узел, а также осуществляется ли обмен данными между всеми узлами или только между корневым узлом и различными конечными узлами.</span><span class="sxs-lookup"><span data-stu-id="9ed70-106">Current multipoint implementations (for example, IP multicast, ST-II, T.120, ATM UNI) vary widely with respect to how nodes join a multipoint session, whether a particular node is designated as a central or root node, and whether data is exchanged between all nodes or only between a root node and various leaf nodes.</span></span> <span data-ttu-id="9ed70-107">Для объявления атрибутов MultiPoint протокола используется структура [**\_ сведений о Всапротокол**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) Windows Sockets 2.</span><span class="sxs-lookup"><span data-stu-id="9ed70-107">The Windows Sockets 2 [**WSAPROTOCOL\_INFO**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) structure is used to declare the multipoint attributes of a protocol.</span></span> <span data-ttu-id="9ed70-108">Изучив эти атрибуты, программист узнает, какие соглашения следует соблюдать, используя применимые функции Winsock для настройки, использования и уничтожения сеансов MultiPoint.</span><span class="sxs-lookup"><span data-stu-id="9ed70-108">By examining these attributes the programmer will know what conventions to follow in using the applicable Winsock functions to set up, use, and tear down multipoint sessions.</span></span>

<span data-ttu-id="9ed70-109">Функции сокетов Windows Sockets 2, поддерживающие многоадресную рассылку, можно суммировать следующим образом.</span><span class="sxs-lookup"><span data-stu-id="9ed70-109">The features of Windows Sockets 2 that support multicast can be summarized as follows:</span></span>

-   <span data-ttu-id="9ed70-110">Три бита атрибутов в структуре [**\_ сведений всапротокол**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) .</span><span class="sxs-lookup"><span data-stu-id="9ed70-110">Three attribute bits in the [**WSAPROTOCOL\_INFO**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) structure.</span></span>
-   <span data-ttu-id="9ed70-111">Четыре флага, определенные для параметра *dwFlags* в [**вспсоккет**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpwspsocket)</span><span class="sxs-lookup"><span data-stu-id="9ed70-111">Four flags defined for the *dwFlags* parameter of [**WSPSocket**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpwspsocket)</span></span>
-   <span data-ttu-id="9ed70-112">Одна функция [**вспжоинлеаф**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpwspjoinleaf)для добавления конечных узлов в сеанс MultiPoint.</span><span class="sxs-lookup"><span data-stu-id="9ed70-112">One function, [**WSPJoinLeaf**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpwspjoinleaf), for adding leaf nodes into a multipoint session.</span></span>
-   <span data-ttu-id="9ed70-113">Два кода команд [**вспиоктл**](/previous-versions/windows/hardware/network/ff566296(v=vs.85)) для управления замыканием на себя MultiPoint и создание области для многоадресных передач.</span><span class="sxs-lookup"><span data-stu-id="9ed70-113">Two [**WSPIoctl**](/previous-versions/windows/hardware/network/ff566296(v=vs.85)) command codes for controlling multipoint loopback and establishing the scope for multicast transmissions.</span></span> <span data-ttu-id="9ed70-114">(Последнее относится к параметрам срока жизни или TTL многоадресной рассылки.)</span><span class="sxs-lookup"><span data-stu-id="9ed70-114">(The latter corresponds to the IP multicast time-to-live or TTL parameter.)</span></span>

> [!Note]  
> <span data-ttu-id="9ed70-115">Включение этих функций MultiPoint в сокеты Windows 2 не исключает поставщика услуг из-за поддержки существующего интерфейса, зависящего от протокола, такого как параметры сокета Диринг для многоадресной IP-рассылки.</span><span class="sxs-lookup"><span data-stu-id="9ed70-115">The inclusion of these multipoint features in Windows Sockets 2 does not preclude a service provider from also supporting an existing protocol-dependent interface, such as the Deering socket options for IP multicast.</span></span>

 

 

 
