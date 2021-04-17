---
description: PNRP использует структуру ВСАКУЕРИСЕТ в сочетании с различными функциями для упрощения разрешения имен и перечисления имен и облаков.
ms.assetid: 0ccf20c1-4c95-4caf-a8f3-82a9e0a9907b
title: PNRP и ВСАКУЕРИСЕТ (P2P. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7d09d135d57af0922feb5a143c41696d85dac083
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105663834"
---
# <a name="pnrp-and-wsaqueryset"></a><span data-ttu-id="7d213-103">PNRP и ВСАКУЕРИСЕТ</span><span class="sxs-lookup"><span data-stu-id="7d213-103">PNRP and WSAQUERYSET</span></span>

<span data-ttu-id="7d213-104">PNRP использует структуру [**всакуерисет**](winsock-nsp-reference-links.md) в сочетании с различными функциями для упрощения разрешения имен и перечисления имен и облаков.</span><span class="sxs-lookup"><span data-stu-id="7d213-104">PNRP uses the [**WSAQUERYSET**](winsock-nsp-reference-links.md) structure in conjunction with various functions to facilitate resolving names and enumerating names and clouds.</span></span>

<span data-ttu-id="7d213-105">Полные определения функций [**всакуерисет**](winsock-nsp-reference-links.md) или сокетов Windows см. в соответствующих определениях в документации по API Windows Sockets 2 в пакете Platform SDK.</span><span class="sxs-lookup"><span data-stu-id="7d213-105">For complete definitions of [**WSAQUERYSET**](winsock-nsp-reference-links.md) or Windows Sockets functions, see their respective definitions in the Windows Sockets 2 API documentation in the Platform SDK.</span></span>

## <a name="wsaqueryset-and-wsasetservice"></a><span data-ttu-id="7d213-106">ВСАКУЕРИСЕТ и Всасетсервице</span><span class="sxs-lookup"><span data-stu-id="7d213-106">WSAQUERYSET and WSASetService</span></span>

<span data-ttu-id="7d213-107">Функция [**всасетсервице**](winsock-nsp-reference-links.md) использует структуру **всакуерисет** для регистрации или удаления одноранговых имен.</span><span class="sxs-lookup"><span data-stu-id="7d213-107">The [**WSASetService**](winsock-nsp-reference-links.md) function uses the **WSAQUERYSET** structure to register or remove peer names.</span></span> <span data-ttu-id="7d213-108">На странице [PNRP и всасетсервице](pnrp-and-wsasetservice.md) показано, как использовать структуру **всакуерисет** с этой функцией.</span><span class="sxs-lookup"><span data-stu-id="7d213-108">The [PNRP and WSASetService](pnrp-and-wsasetservice.md) page outlines how to use the **WSAQUERYSET** structure with this function.</span></span>

## <a name="wsaqueryset-and-wsalookupservicebegin"></a><span data-ttu-id="7d213-109">ВСАКУЕРИСЕТ и Всалукупсервицебегин</span><span class="sxs-lookup"><span data-stu-id="7d213-109">WSAQUERYSET and WSALookupServiceBegin</span></span>

<span data-ttu-id="7d213-110">Структура [**всакуерисет**](winsock-nsp-reference-links.md) широко используется с функциями **всалукупсервицебегин**, **всалукупсервиценекст** и **всалукупсервицеенд** .</span><span class="sxs-lookup"><span data-stu-id="7d213-110">The [**WSAQUERYSET**](winsock-nsp-reference-links.md) structure is used extensively with the **WSALookupServiceBegin**, **WSALookupServiceNext**, and **WSALookupServiceEnd** functions.</span></span> <span data-ttu-id="7d213-111">Сведения о том, как эти функции используют структуру **всакуерисет** , подробно описаны на следующих справочных страницах:</span><span class="sxs-lookup"><span data-stu-id="7d213-111">Details about how these functions use the **WSAQUERYSET** structure are detailed in the following reference pages:</span></span>

-   [<span data-ttu-id="7d213-112">PNRP и Всалукупсервицебегин</span><span class="sxs-lookup"><span data-stu-id="7d213-112">PNRP and WSALookupServiceBegin</span></span>](pnrp-and-wsalookupservicebegin.md)
-   [<span data-ttu-id="7d213-113">PNRP и Всалукупсервиценекст</span><span class="sxs-lookup"><span data-stu-id="7d213-113">PNRP and WSALookupServiceNext</span></span>](pnrp-and-wsalookupservicenext.md)
-   [<span data-ttu-id="7d213-114">PNRP и Всалукупсервицеенд</span><span class="sxs-lookup"><span data-stu-id="7d213-114">PNRP and WSALookupServiceEnd</span></span>](pnrp-and-wsalookupserviceend.md)

## <a name="requirements"></a><span data-ttu-id="7d213-115">Требования</span><span class="sxs-lookup"><span data-stu-id="7d213-115">Requirements</span></span>



| <span data-ttu-id="7d213-116">Требование</span><span class="sxs-lookup"><span data-stu-id="7d213-116">Requirement</span></span> | <span data-ttu-id="7d213-117">Значение</span><span class="sxs-lookup"><span data-stu-id="7d213-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="7d213-118">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="7d213-118">Minimum supported client</span></span><br/> | <span data-ttu-id="7d213-119">Только для настольных приложений Windows XP с пакетом обновления 2 \[\]</span><span class="sxs-lookup"><span data-stu-id="7d213-119">Windows XP with SP2 \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="7d213-120">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="7d213-120">Minimum supported server</span></span><br/> | <span data-ttu-id="7d213-121">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="7d213-121">Windows Server 2008 \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="7d213-122">Версия</span><span class="sxs-lookup"><span data-stu-id="7d213-122">Version</span></span><br/>                  | <span data-ttu-id="7d213-123">Windows XP с пакетом обновления 1 (SP1) и расширенный сетевой пакет для Windows XP</span><span class="sxs-lookup"><span data-stu-id="7d213-123">Windows XP with SP1 with the Advanced Networking Pack for Windows XP</span></span><br/>  |
| <span data-ttu-id="7d213-124">Header</span><span class="sxs-lookup"><span data-stu-id="7d213-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="7d213-125"><dt>P2P. h</dt></span><span class="sxs-lookup"><span data-stu-id="7d213-125"><dt>P2P.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7d213-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="7d213-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7d213-127">PNRP и BLOB-объект</span><span class="sxs-lookup"><span data-stu-id="7d213-127">PNRP and BLOB</span></span>](pnrp-and-blob.md)
</dt> <dt>

[<span data-ttu-id="7d213-128">PNRP и Всасетсервице</span><span class="sxs-lookup"><span data-stu-id="7d213-128">PNRP and WSASetService</span></span>](pnrp-and-wsasetservice.md)
</dt> </dl>

 

 




