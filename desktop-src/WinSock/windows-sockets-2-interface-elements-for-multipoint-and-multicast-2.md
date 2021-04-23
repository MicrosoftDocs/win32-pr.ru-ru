---
description: Элементы интерфейса Windows Sockets 2 (Winsock) для MultiPoint и многоадресной рассылки.
ms.assetid: c6f704cf-031b-4714-9f07-2d7715a157a0
title: Элементы интерфейса сокетов Windows 2 для MultiPoint и многоадресной рассылки
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ad86905fe19c5c4c603db488874039b7cc8a0b2f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105711379"
---
# <a name="windows-sockets-2-interface-elements-for-multipoint-and-multicast"></a><span data-ttu-id="8ea91-103">Элементы интерфейса сокетов Windows 2 для MultiPoint и многоадресной рассылки</span><span class="sxs-lookup"><span data-stu-id="8ea91-103">Windows Sockets 2 Interface Elements for Multipoint and Multicast</span></span>

<span data-ttu-id="8ea91-104">Механизмы, включенные в сокеты Windows 2 для использования возможностей MultiPoint, можно суммировать следующим образом.</span><span class="sxs-lookup"><span data-stu-id="8ea91-104">The mechanisms that have been incorporated into Windows Sockets 2 for utilizing multipoint capabilities can be summarized as follows:</span></span>

-   <span data-ttu-id="8ea91-105">Три бита атрибутов в структуре [**\_ сведений всапротокол**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) .</span><span class="sxs-lookup"><span data-stu-id="8ea91-105">Three attribute bits in the [**WSAPROTOCOL\_INFO**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) structure.</span></span>
-   <span data-ttu-id="8ea91-106">Четыре флага, определенные  для параметра dwFlags [**всасоккет**](/windows/desktop/api/Winsock2/nf-winsock2-wsasocketa).</span><span class="sxs-lookup"><span data-stu-id="8ea91-106">Four flags defined for the *dwFlags* parameter of [**WSASocket**](/windows/desktop/api/Winsock2/nf-winsock2-wsasocketa).</span></span>
-   <span data-ttu-id="8ea91-107">Одна функция [**всажоинлеаф**](/windows/desktop/api/Winsock2/nf-winsock2-wsajoinleaf)для добавления конечных узлов в сеанс MultiPoint.</span><span class="sxs-lookup"><span data-stu-id="8ea91-107">One function, [**WSAJoinLeaf**](/windows/desktop/api/Winsock2/nf-winsock2-wsajoinleaf), for adding leaf nodes into a multipoint session.</span></span>
-   <span data-ttu-id="8ea91-108">Два кода команд [**всаиоктл**](/windows/desktop/api/Winsock2/nf-winsock2-wsaioctl) для управления замыканием на себя MultiPoint и областью многоадресных передач.</span><span class="sxs-lookup"><span data-stu-id="8ea91-108">Two [**WSAIoctl**](/windows/desktop/api/Winsock2/nf-winsock2-wsaioctl) command codes for controlling multipoint loopback and the scope of multicast transmissions.</span></span>

<span data-ttu-id="8ea91-109">В следующих разделах эти элементы интерфейса описаны более подробно:</span><span class="sxs-lookup"><span data-stu-id="8ea91-109">The following sections describe these interface elements in more detail:</span></span>

-   [<span data-ttu-id="8ea91-110">Семантика присоединения к листьям MultiPoint</span><span class="sxs-lookup"><span data-stu-id="8ea91-110">Semantics for Joining Multipoint Leaves</span></span>](semantics-for-joining-multipoint-leaves-2.md)
-   [<span data-ttu-id="8ea91-111">Как существующие протоколы MultiPoint поддерживают эти расширения</span><span class="sxs-lookup"><span data-stu-id="8ea91-111">How Existing Multipoint Protocols Support These Extensions</span></span>](how-existing-multipoint-protocols-support-these-extensions-2.md)

 

 
