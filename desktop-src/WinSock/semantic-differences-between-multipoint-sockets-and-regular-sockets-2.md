---
title: Семантические различия между сокетами MultiPoint и стандартными сокетами
description: Различия между двумя \_ корневыми сокетами MultiPoint и стандартными сокетами "точка — точка".
ms.assetid: fbadfde8-44dc-41ac-bd93-1a22c76ca321
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 04d95b2637a4f805cea5ee6f138cc6992080a238
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105702090"
---
# <a name="semantic-differences-between-multipoint-sockets-and-regular-sockets"></a><span data-ttu-id="d76ec-103">Семантические различия между сокетами MultiPoint и стандартными сокетами</span><span class="sxs-lookup"><span data-stu-id="d76ec-103">Semantic differences between multipoint sockets and regular sockets</span></span>

<span data-ttu-id="d76ec-104">В плоскости управления существуют значительные семантические различия между \_ корневым сокетом c и обычным сокетом типа "точка — точка":</span><span class="sxs-lookup"><span data-stu-id="d76ec-104">In the control plane, there are some significant semantic differences between a c\_root socket and a regular point-to-point socket:</span></span>

-   <span data-ttu-id="d76ec-105">В \_ [**всажоинлеаф**](/windows/desktop/api/Winsock2/nf-winsock2-wsajoinleaf) можно использовать корневой сокет c для присоединения нового листа.</span><span class="sxs-lookup"><span data-stu-id="d76ec-105">The c\_root socket can be used in [**WSAJoinLeaf**](/windows/desktop/api/Winsock2/nf-winsock2-wsajoinleaf) to join a new a leaf.</span></span>
-   <span data-ttu-id="d76ec-106">Помещение \_ корневого сокета c в режим прослушивания (путем вызова [**Listen**](/windows/desktop/api/Winsock2/nf-winsock2-listen)) не исключает \_ использования корневого сокета c в вызове [**всажоинлеаф**](/windows/desktop/api/Winsock2/nf-winsock2-wsajoinleaf) для добавления нового листа или для отправки и получения данных MultiPoint.</span><span class="sxs-lookup"><span data-stu-id="d76ec-106">Placing a c\_root socket into listening mode (by calling [**listen**](/windows/desktop/api/Winsock2/nf-winsock2-listen)) does not preclude the c\_root socket from being used in a call to [**WSAJoinLeaf**](/windows/desktop/api/Winsock2/nf-winsock2-wsajoinleaf) to add a new leaf, or for sending and receiving multipoint data.</span></span>
-   <span data-ttu-id="d76ec-107">Закрытие \_ корневого сокета c приводит к тому, что все связанные \_ конечные сокеты c получат \_ уведомление о закрытии демона.</span><span class="sxs-lookup"><span data-stu-id="d76ec-107">The closing of a c\_root socket causes all of the associated c\_leaf sockets to get FD\_CLOSE notification.</span></span>

<span data-ttu-id="d76ec-108">Нет семантических различий между \_ конечным сокетом c и обычным сокетом в плоскости управления, за исключением того, что \_ конечный сокет c можно использовать в [**всажоинлеаф**](/windows/desktop/api/Winsock2/nf-winsock2-wsajoinleaf), а использование \_ конечного сокета c в [**Listen**](/windows/desktop/api/Winsock2/nf-winsock2-listen) означает, что должны приниматься только запросы на подключение к MultiPoint.</span><span class="sxs-lookup"><span data-stu-id="d76ec-108">There are no semantic differences between a c\_leaf socket and a regular socket in the control plane, except that the c\_leaf socket can be used in [**WSAJoinLeaf**](/windows/desktop/api/Winsock2/nf-winsock2-wsajoinleaf), and the use of c\_leaf socket in [**listen**](/windows/desktop/api/Winsock2/nf-winsock2-listen) indicates that only multipoint connection requests should be accepted.</span></span>

<span data-ttu-id="d76ec-109">В плоскости данных семантические различия между \_ корневым сокетом d и стандартным сокетом типа "точка — точка":</span><span class="sxs-lookup"><span data-stu-id="d76ec-109">In the data plane, the semantic differences between the d\_root socket and a regular point-to-point socket are:</span></span>

-   <span data-ttu-id="d76ec-110">Данные, отправленные на \_ корневом сокете d, доставляются во все листья в одном сеансе MultiPoint.</span><span class="sxs-lookup"><span data-stu-id="d76ec-110">The data sent on the d\_root socket is delivered to all the leaves in the same multipoint session.</span></span>
-   <span data-ttu-id="d76ec-111">Данные, полученные на \_ корневом сокете d, могут быть из любого из конечных элементов.</span><span class="sxs-lookup"><span data-stu-id="d76ec-111">The data received on the d\_root socket may be from any of the leaves.</span></span>

<span data-ttu-id="d76ec-112">\_Конечный сокет d в корневой плоскости данных не имеет семантического отличия от обычного сокета, но в некорневой плоскости данных данные, отправленные на конечный сокет d, переходят на \_ все остальные конечные узлы, и полученные данные могут быть из любых других конечных узлов.</span><span class="sxs-lookup"><span data-stu-id="d76ec-112">The d\_leaf socket in the rooted data plane has no semantic difference from the regular socket, however, in the nonrooted data plane, the data sent on the d\_leaf socket goes to all the other leaf nodes, and the data received could be from any other leaf nodes.</span></span> <span data-ttu-id="d76ec-113">Как упоминалось ранее, сведения о том, \_ находится ли конечный сокет d в корневой или некорневой плоскости данных, содержится в соответствующей структуре [**всапротокол \_ info**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) для сокета.</span><span class="sxs-lookup"><span data-stu-id="d76ec-113">As mentioned earlier, the information about whether the d\_leaf socket is in a rooted or nonrooted data plane is contained in the corresponding [**WSAPROTOCOL\_INFO**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) structure for the socket.</span></span>

 

 
