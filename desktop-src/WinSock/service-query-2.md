---
description: Запрос имени службы в сокетах Windows (Winsock).
ms.assetid: 94d77f7b-824a-4686-b270-9c662976bbc0
title: Запрос на обслуживание
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 951ad1950c0f1d97ab0ca6d06f79ed6ff0180d96
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104080590"
---
# <a name="service-query"></a><span data-ttu-id="dc271-103">Запрос на обслуживание</span><span class="sxs-lookup"><span data-stu-id="dc271-103">Service Query</span></span>

-   [<span data-ttu-id="dc271-104">**нсплукупсервицебегин**</span><span class="sxs-lookup"><span data-stu-id="dc271-104">**NSPLookupServiceBegin**</span></span>](/windows/desktop/api/Ws2spi/nc-ws2spi-lpnsplookupservicebegin)
-   [<span data-ttu-id="dc271-105">**нсплукупсервиценекст**</span><span class="sxs-lookup"><span data-stu-id="dc271-105">**NSPLookupServiceNext**</span></span>](/windows/desktop/api/Ws2spi/nc-ws2spi-lpnsplookupservicenext)
-   [<span data-ttu-id="dc271-106">**нсплукупсервицеенд**</span><span class="sxs-lookup"><span data-stu-id="dc271-106">**NSPLookupServiceEnd**</span></span>](/windows/desktop/api/Ws2spi/nc-ws2spi-lpnsplookupserviceend)

<span data-ttu-id="dc271-107">Запрос службы имен включает ряд вызовов: [**нсплукупсервицебегин**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpnsplookupservicebegin), за которыми следует один или несколько вызовов [**нсплукупсервиценекст**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpnsplookupservicenext) и заканчивая вызовом [**нсплукупсервицеенд**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpnsplookupserviceend).</span><span class="sxs-lookup"><span data-stu-id="dc271-107">A name service query involves a series of calls: [**NSPLookupServiceBegin**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpnsplookupservicebegin), followed by one or more calls to [**NSPLookupServiceNext**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpnsplookupservicenext) and ending with a call to [**NSPLookupServiceEnd**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpnsplookupserviceend).</span></span> <span data-ttu-id="dc271-108">[**Нсплукупсервицебегин**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpnsplookupservicebegin) принимает структуру [**всакуерисет**](/windows/desktop/api/Winsock2/ns-winsock2-wsaquerysetw) в качестве входных данных, чтобы определить параметры запроса вместе с набором флагов, чтобы обеспечить дополнительный контроль над операцией поиска.</span><span class="sxs-lookup"><span data-stu-id="dc271-108">[**NSPLookupServiceBegin**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpnsplookupservicebegin) takes a [**WSAQUERYSET**](/windows/desktop/api/Winsock2/ns-winsock2-wsaquerysetw) structure as input in order to define the query parameters along with a set of flags to provide additional control over the search operation.</span></span> <span data-ttu-id="dc271-109">Он возвращает маркер запроса, который используется в последующих вызовах **нсплукупсервиценекст** и **нсплукупсервицеенд**.</span><span class="sxs-lookup"><span data-stu-id="dc271-109">It returns a query handle which is used in the subsequent calls to **NSPLookupServiceNext** and **NSPLookupServiceEnd**.</span></span>

<span data-ttu-id="dc271-110">Клиент SPI пространства имен вызывает [**нсплукупсервиценекст**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpnsplookupservicenext) для получения результатов запроса с результатами, предоставленными в буфере [**всакуерисет**](/windows/desktop/api/Winsock2/ns-winsock2-wsaquerysetw) , предоставленном клиентом.</span><span class="sxs-lookup"><span data-stu-id="dc271-110">The namespace SPI client invokes [**NSPLookupServiceNext**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpnsplookupservicenext) to obtain query results, with results supplied in an client-supplied [**WSAQUERYSET**](/windows/desktop/api/Winsock2/ns-winsock2-wsaquerysetw) buffer.</span></span> <span data-ttu-id="dc271-111">Клиент продолжит вызывать **нсплукупсервиценекст** до тех пор, пока не будет возвращен код ошибки WSA \_ E, \_ \_ указывающий, что все результаты получены.</span><span class="sxs-lookup"><span data-stu-id="dc271-111">The client continues to call **NSPLookupServiceNext** until the error code WSA\_E\_NO\_MORE is returned indicating that all results have been retrieved.</span></span> <span data-ttu-id="dc271-112">После этого поиск завершается вызовом [**нсплукупсервицеенд**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpnsplookupserviceend).</span><span class="sxs-lookup"><span data-stu-id="dc271-112">The search is then terminated by a call to [**NSPLookupServiceEnd**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpnsplookupserviceend).</span></span> <span data-ttu-id="dc271-113">Функция **нсплукупсервицеенд** может также использоваться для отмены ожидающего в данный момент **нсплукупсервиценекст** при вызове из другого потока.</span><span class="sxs-lookup"><span data-stu-id="dc271-113">The **NSPLookupServiceEnd** function can also be used to cancel a currently pending **NSPLookupServiceNext** when called from another thread.</span></span>

<span data-ttu-id="dc271-114">В Windows Sockets 2 для ВСАЕНОМОРЕ (10102) и WSA \_ E ( \_ 10110) определены конфликтующие коды ошибок \_ .</span><span class="sxs-lookup"><span data-stu-id="dc271-114">In Windows Sockets 2, conflicting error codes are defined for WSAENOMORE (10102) and WSA\_E\_NO\_MORE (10110).</span></span> <span data-ttu-id="dc271-115">Код ошибки ВСАЕНОМОРЕ будет удален в следующей версии, и только WSA E больше \_ \_ не \_ останется.</span><span class="sxs-lookup"><span data-stu-id="dc271-115">The error code WSAENOMORE will be removed in a future version and only WSA\_E\_NO\_MORE will remain.</span></span> <span data-ttu-id="dc271-116">Поставщики пространства имен должны переключиться на использование WSA \_ E \_ без \_ кода ошибки как можно скорее, чтобы обеспечить совместимость с самым широким возможным диапазоном приложений.</span><span class="sxs-lookup"><span data-stu-id="dc271-116">Namespace providers should switch to using the WSA\_E\_NO\_MORE error code as soon as possible to maintain compatibility with the widest possible range of applications.</span></span>

 

 



