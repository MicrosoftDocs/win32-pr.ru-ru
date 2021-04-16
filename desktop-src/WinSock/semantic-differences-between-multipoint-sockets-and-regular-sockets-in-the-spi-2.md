---
description: Различия между обычными сокетами "точка — точка" и \_ "корневыми сокетами MultiPoint" в подсистемах Windows Sockets (Winsock) SPI.
ms.assetid: 5476933b-70f2-4dcf-a6e9-f9f4a537c29f
title: Семантические различия между сокетами MultiPoint и обычными сокетами в SPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dd9e4e94583ee653a8ec0bf19c743dddd3e16253
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105702010"
---
# <a name="semantic-differences-between-multipoint-sockets-and-regular-sockets-in-the-spi"></a><span data-ttu-id="98d9c-103">Семантические различия между сокетами MultiPoint и обычными сокетами в SPI</span><span class="sxs-lookup"><span data-stu-id="98d9c-103">Semantic Differences Between Multipoint Sockets and Regular Sockets in the SPI</span></span>

<span data-ttu-id="98d9c-104">В плоскости управления существуют значительные семантические различия между \_ корневым сокетом c и обычным сокетом типа "точка — точка":</span><span class="sxs-lookup"><span data-stu-id="98d9c-104">In the control plane, there are some significant semantic differences between a c\_root socket and a regular point-to-point socket:</span></span>

-   <span data-ttu-id="98d9c-105">\_Для присоединения нового листа в [**вспжоинлеаф**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpwspjoinleaf) можно использовать корневой сокет c.</span><span class="sxs-lookup"><span data-stu-id="98d9c-105">The c\_root socket can be used in [**WSPJoinLeaf**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpwspjoinleaf) to join a new leaf.</span></span>
-   <span data-ttu-id="98d9c-106">Размещение \_ корневого сокета c в режиме прослушивания (путем вызова [**всплистен**](/previous-versions/windows/hardware/network/ff566297(v=vs.85))) не исключает \_ Использование корневого сокета c при вызове [**вспжоинлеаф**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpwspjoinleaf) для добавления нового листа или для отправки и получения данных MultiPoint.</span><span class="sxs-lookup"><span data-stu-id="98d9c-106">Placing a c\_root socket into the listening mode (by calling [**WSPListen**](/previous-versions/windows/hardware/network/ff566297(v=vs.85))) does not preclude the c\_root socket from being used in a call to [**WSPJoinLeaf**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpwspjoinleaf) to add a new leaf, or for sending and receiving multipoint data.</span></span>
-   <span data-ttu-id="98d9c-107">Закрытие \_ корневого сокета c приведет к тому, что все связанные \_ конечные сокеты c будут получать \_ уведомление о закрытии демона.</span><span class="sxs-lookup"><span data-stu-id="98d9c-107">The closing of a c\_root socket will cause all the associated c\_leaf sockets to get FD\_CLOSE notification.</span></span>

<span data-ttu-id="98d9c-108">Нет семантических различий между \_ конечным сокетом c и обычным сокетом в плоскости управления, за исключением того, что \_ конечный сокет c можно использовать в [**вспжоинлеаф**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpwspjoinleaf), а использование \_ конечного сокета c в [**всплистен**](/previous-versions/windows/hardware/network/ff566297(v=vs.85)) указывает, что должны приниматься только запросы на подключение к MultiPoint.</span><span class="sxs-lookup"><span data-stu-id="98d9c-108">There are no semantic differences between a c\_leaf socket and a regular socket in the control plane, except that the c\_leaf socket can be used in [**WSPJoinLeaf**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpwspjoinleaf), and the use of c\_leaf socket in [**WSPListen**](/previous-versions/windows/hardware/network/ff566297(v=vs.85)) indicates that only multipoint connection requests should be accepted.</span></span>

<span data-ttu-id="98d9c-109">В плоскости данных семантические различия между \_ корневым сокетом d и стандартным сокетом типа "точка — точка"</span><span class="sxs-lookup"><span data-stu-id="98d9c-109">In the data plane, the semantic differences between the d\_root socket and a regular point-to-point socket are</span></span>

-   <span data-ttu-id="98d9c-110">Данные, отправленные на \_ корневом сокете d, будут доставляться во все листья в одном сеансе MultiPoint.</span><span class="sxs-lookup"><span data-stu-id="98d9c-110">The data sent on the d\_root socket will be delivered to all the leaves in the same multipoint session.</span></span>
-   <span data-ttu-id="98d9c-111">Данные, полученные на \_ корневом сокете d, могут быть из любого из конечных элементов.</span><span class="sxs-lookup"><span data-stu-id="98d9c-111">The data received on the d\_root socket may be from any of the leaves.</span></span>

<span data-ttu-id="98d9c-112">\_Конечный сокет d в корневой плоскости данных не имеет семантического отличия от обычного сокета, но в некорневой плоскости данных данные, отправленные на конечный сокет d, будут передаваться \_ на все остальные конечные узлы, а полученные данные могут быть из любого другого конечного узла.</span><span class="sxs-lookup"><span data-stu-id="98d9c-112">The d\_leaf socket in the rooted data plane has no semantic difference from the regular socket, however, in the nonrooted data plane, the data sent on the d\_leaf socket will go to all of the other leaf nodes, and the data received could be from any of the other leaf nodes.</span></span> <span data-ttu-id="98d9c-113">Как упоминалось ранее, сведения о том, \_ находится ли конечный сокет d в корневой или некорневой плоскости данных, содержится в соответствующей структуре [**всапротокол \_ info**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) для сокета.</span><span class="sxs-lookup"><span data-stu-id="98d9c-113">As mentioned earlier, the information about whether the d\_leaf socket is in a rooted or nonrooted data plane is contained in the corresponding [**WSAPROTOCOL\_INFO**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) structure for the socket.</span></span>

 

 
