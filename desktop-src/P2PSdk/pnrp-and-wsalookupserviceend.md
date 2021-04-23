---
description: Протокол PNRP использует функцию Всалукупсервицеенд для следующих действий.
ms.assetid: 0732929e-ca03-438f-80d9-48a3da0095f7
title: PNRP и Всалукупсервицеенд
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1db499c9a736e26d630b623a29baa4c18dcfceeb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105663835"
---
# <a name="pnrp-and-wsalookupserviceend"></a><span data-ttu-id="323f0-103">PNRP и Всалукупсервицеенд</span><span class="sxs-lookup"><span data-stu-id="323f0-103">PNRP and WSALookupServiceEnd</span></span>

<span data-ttu-id="323f0-104">Протокол PNRP использует функцию [**всалукупсервицеенд**](winsock-nsp-reference-links.md) для следующих действий:</span><span class="sxs-lookup"><span data-stu-id="323f0-104">PNRP uses the [**WSALookupServiceEnd**](winsock-nsp-reference-links.md) function to do the following:</span></span>

-   <span data-ttu-id="323f0-105">Завершение запроса, инициированного в предыдущем вызове [ **всалукупсервицебегин**](winsock-nsp-reference-links.md)</span><span class="sxs-lookup"><span data-stu-id="323f0-105">Terminate a query initiated in a previous call to [**WSALookupServiceBegin**](winsock-nsp-reference-links.md)</span></span>
-   <span data-ttu-id="323f0-106">Разблокирование вызова [**всалукупсервиценекст**](winsock-nsp-reference-links.md) для отмены поиска</span><span class="sxs-lookup"><span data-stu-id="323f0-106">Unblock a call to [**WSALookupServiceNext**](winsock-nsp-reference-links.md) to stop the search</span></span>

<span data-ttu-id="323f0-107">Вызов [**всалукупсервицеенд**](winsock-nsp-reference-links.md) завершает запрос и очищает контекст.</span><span class="sxs-lookup"><span data-stu-id="323f0-107">A call to [**WSALookupServiceEnd**](winsock-nsp-reference-links.md) terminates a query and cleans up the context.</span></span> <span data-ttu-id="323f0-108">Маркер, полученный из вызова **всалукупсервицебегин** , должен быть передан в качестве параметра **всалукупсервицеенд**.</span><span class="sxs-lookup"><span data-stu-id="323f0-108">The handle obtained from a call to **WSALookupServiceBegin** must be passed as a parameter to **WSALookupServiceEnd**.</span></span>

<span data-ttu-id="323f0-109">Дополнительные сведения о протоколе PNRP и функции [**всалукупсервицебегин**](winsock-nsp-reference-links.md) см. в разделе [PNRP и всалукупсервицебегин](pnrp-and-wsalookupservicebegin.md).</span><span class="sxs-lookup"><span data-stu-id="323f0-109">For more information about PNRP and the [**WSALookupServiceBegin**](winsock-nsp-reference-links.md) function, see [PNRP and WSALookupServiceBegin](pnrp-and-wsalookupservicebegin.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="323f0-110">См. также</span><span class="sxs-lookup"><span data-stu-id="323f0-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="323f0-111">PNRP и Всалукупсервицебегин</span><span class="sxs-lookup"><span data-stu-id="323f0-111">PNRP and WSALookupServiceBegin</span></span>](pnrp-and-wsalookupservicebegin.md)
</dt> <dt>

[<span data-ttu-id="323f0-112">Коды ошибок PNRP NSP</span><span class="sxs-lookup"><span data-stu-id="323f0-112">PNRP NSP Error Codes</span></span>](pnrp-nsp-error-codes.md)
</dt> <dt>

[<span data-ttu-id="323f0-113">**всалукупсервиценекст**</span><span class="sxs-lookup"><span data-stu-id="323f0-113">**WSALookupServiceNext**</span></span>](winsock-nsp-reference-links.md)
</dt> </dl>

 

 



