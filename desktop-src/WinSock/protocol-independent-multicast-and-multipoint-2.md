---
description: Сокеты Windows 2 предоставляют универсальный метод для использования возможностей передачи и многоадресной рассылки для транспортов.
ms.assetid: 75cd8f21-a391-4626-b909-0760d12db995
title: Protocol-Independent многоадресной рассылки и MultiPoint
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e409c18752b32af7cf65b4a55862ec75cec7a3e7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105692717"
---
# <a name="protocol-independent-multicast-and-multipoint"></a><span data-ttu-id="9eede-103">Protocol-Independent многоадресной рассылки и MultiPoint</span><span class="sxs-lookup"><span data-stu-id="9eede-103">Protocol-Independent Multicast and Multipoint</span></span>

<span data-ttu-id="9eede-104">Сокеты Windows 2 предоставляют универсальный метод для использования возможностей передачи и многоадресной рассылки для транспортов.</span><span class="sxs-lookup"><span data-stu-id="9eede-104">Windows Sockets 2 provides a generic method for utilizing the multipoint and multicast capabilities of transports.</span></span> <span data-ttu-id="9eede-105">Этот универсальный метод реализует эти функции точно так же, как позволяет получить доступ к базовым возможностям транспорта данных многочисленных транспортных протоколов.</span><span class="sxs-lookup"><span data-stu-id="9eede-105">This generic method implements these features just as it allows the basic data transport capabilities of numerous transport protocols to be accessed.</span></span> <span data-ttu-id="9eede-106">Термин MultiPoint используется в дальнейшем для ссылки на многоадресную и MultiPoint связь.</span><span class="sxs-lookup"><span data-stu-id="9eede-106">The term, multipoint, is used hereafter to refer to both multicast and multipoint communications.</span></span>

<span data-ttu-id="9eede-107">Текущие реализации MultiPoint (например, многоадресная рассылка IP-адресов, ST-II, T. 120 и ATM UNI) могут сильно различаться.</span><span class="sxs-lookup"><span data-stu-id="9eede-107">Current multipoint implementations (for example, IP multicast, ST-II, T.120, and ATM UNI) vary widely.</span></span> <span data-ttu-id="9eede-108">Как узлы присоединяются к сеансу MultiPoint, определяется ли конкретный узел как Центральный или корневой узел, а также происходит ли обмен данными между всеми узлами или только между корневым узлом и различными конечными узлами в разных реализациях.</span><span class="sxs-lookup"><span data-stu-id="9eede-108">How nodes join a multipoint session, whether a particular node is designated as a central or root node, and whether data is exchanged between all nodes or only between a root node and the various leaf nodes differ among implementations.</span></span> <span data-ttu-id="9eede-109">Структура [**\_ сведений о Всапротокол**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) для сокетов Windows 2 используется для объявления различных атрибутов MultiPoint протокола.</span><span class="sxs-lookup"><span data-stu-id="9eede-109">The [**WSAPROTOCOL\_INFO**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) structure for Windows Sockets 2 is used to declare the various multipoint attributes of a protocol.</span></span> <span data-ttu-id="9eede-110">Изучив эти атрибуты, программист знает, какие соглашения следует соблюдать с помощью соответствующих функций Windows Sockets 2 для настройки, использования и уничтожения сеансов MultiPoint.</span><span class="sxs-lookup"><span data-stu-id="9eede-110">By examining these attributes, the programmer knows what conventions to follow with the applicable Windows Sockets 2 functions to set up, utilize, and tear down multipoint sessions.</span></span>

<span data-ttu-id="9eede-111">Ниже приведены сводные сведения о функциях Winsock, поддерживающих MultiPoint.</span><span class="sxs-lookup"><span data-stu-id="9eede-111">The following summarizes Winsock features that support multipoint:</span></span>

-   <span data-ttu-id="9eede-112">Биты с двумя атрибутами в [**структуре \_ сведений всапротокол**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) .</span><span class="sxs-lookup"><span data-stu-id="9eede-112">Two-attribute bits in the [**WSAPROTOCOL\_INFO**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) structure.</span></span>
-   <span data-ttu-id="9eede-113">Четыре флага, определенные для параметра *dwFlags* функции [**всасоккет**](/windows/desktop/api/Winsock2/nf-winsock2-wsasocketa) .</span><span class="sxs-lookup"><span data-stu-id="9eede-113">Four flags defined for the *dwFlags* parameter of the [**WSASocket**](/windows/desktop/api/Winsock2/nf-winsock2-wsasocketa) function.</span></span>
-   <span data-ttu-id="9eede-114">Одна функция [**всажоинлеаф**](/windows/desktop/api/Winsock2/nf-winsock2-wsajoinleaf)для добавления конечных узлов в сеанс MultiPoint</span><span class="sxs-lookup"><span data-stu-id="9eede-114">One function, [**WSAJoinLeaf**](/windows/desktop/api/Winsock2/nf-winsock2-wsajoinleaf), for adding leaf nodes into a multipoint session</span></span>
-   <span data-ttu-id="9eede-115">Два кода команд [**всаиоктл**](/windows/desktop/api/Winsock2/nf-winsock2-wsaioctl) для управления замыканием на себя MultiPoint и создание области для многоадресных передач.</span><span class="sxs-lookup"><span data-stu-id="9eede-115">Two [**WSAIoctl**](/windows/desktop/api/Winsock2/nf-winsock2-wsaioctl) command codes for controlling multipoint loopback and establishing the scope for multicast transmissions.</span></span> <span data-ttu-id="9eede-116">(Последнее относится к параметрам срока жизни или TTL многоадресной рассылки.)</span><span class="sxs-lookup"><span data-stu-id="9eede-116">(The latter corresponds to the IP multicast time-to-live or TTL parameter.)</span></span>

> [!Note]  
> <span data-ttu-id="9eede-117">Включение этих функций MultiPoint в сокеты Windows 2 не исключает использования существующего интерфейса, зависящего от протокола, такого как параметры сокета Диринг для многоадресной IP-рассылки.</span><span class="sxs-lookup"><span data-stu-id="9eede-117">The inclusion of these multipoint features in Windows Sockets 2 does not preclude an application from using an existing protocol-dependent interface, such as the Deering socket options for IP multicast.</span></span>

 

<span data-ttu-id="9eede-118">Подробные сведения о том, как характеризуются различные схемы MultiPoint и как используются функции сокетов Windows 2, см. в статье [семантика многоадресной рассылки и MultiPoint](multipoint-and-multicast-semantics-2.md) .</span><span class="sxs-lookup"><span data-stu-id="9eede-118">See [Multipoint and Multicast Semantics](multipoint-and-multicast-semantics-2.md) for detailed information on how the various multipoint schemes are characterized and how the applicable features of Windows Sockets 2 are utilized.</span></span>

 

 
