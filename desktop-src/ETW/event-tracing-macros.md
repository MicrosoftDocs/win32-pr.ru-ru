---
description: ETW определяет следующие удобные макросы, которые можно использовать для доступа к членам \_ структуры дескрипторов событий.
ms.assetid: ce5439cb-8bb7-4d71-8908-d4ccf6086811
title: Макросы трассировки событий
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2a5017973627fc18b153b3b9eaed52dcb4b71c18
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104540354"
---
# <a name="event-tracing-macros"></a><span data-ttu-id="81368-103">Макросы трассировки событий</span><span class="sxs-lookup"><span data-stu-id="81368-103">Event Tracing Macros</span></span>

<span data-ttu-id="81368-104">ETW определяет следующие удобные макросы, которые можно использовать для доступа к членам \_ структуры дескрипторов событий.</span><span class="sxs-lookup"><span data-stu-id="81368-104">ETW defines the following convenience macros that you can use to access members of the EVENT\_DESCRIPTOR structure.</span></span>

<dl>

[<span data-ttu-id="81368-105">**EventDataDescCreate**</span><span class="sxs-lookup"><span data-stu-id="81368-105">**EventDataDescCreate**</span></span>](/windows/desktop/api/Evntprov/nf-evntprov-eventdatadesccreate)  
[<span data-ttu-id="81368-106">**евентдесккреате**</span><span class="sxs-lookup"><span data-stu-id="81368-106">**EventDescCreate**</span></span>](/windows/desktop/api/Evntprov/nf-evntprov-eventdesccreate)  
[<span data-ttu-id="81368-107">**евентдескжетчаннел**</span><span class="sxs-lookup"><span data-stu-id="81368-107">**EventDescGetChannel**</span></span>](/windows/desktop/api/Evntprov/nf-evntprov-eventdescgetchannel)  
[<span data-ttu-id="81368-108">**евентдескжетид**</span><span class="sxs-lookup"><span data-stu-id="81368-108">**EventDescGetId**</span></span>](/windows/desktop/api/Evntprov/nf-evntprov-eventdescgetid)  
[<span data-ttu-id="81368-109">**евентдескжеткэйворд**</span><span class="sxs-lookup"><span data-stu-id="81368-109">**EventDescGetKeyword**</span></span>](/windows/desktop/api/Evntprov/nf-evntprov-eventdescgetkeyword)  
[<span data-ttu-id="81368-110">**евентдескжетлевел**</span><span class="sxs-lookup"><span data-stu-id="81368-110">**EventDescGetLevel**</span></span>](/windows/desktop/api/Evntprov/nf-evntprov-eventdescgetlevel)  
[<span data-ttu-id="81368-111">**евентдескжетопкоде**</span><span class="sxs-lookup"><span data-stu-id="81368-111">**EventDescGetOpcode**</span></span>](/windows/desktop/api/Evntprov/nf-evntprov-eventdescgetopcode)  
[<span data-ttu-id="81368-112">**евентдескжеттаск**</span><span class="sxs-lookup"><span data-stu-id="81368-112">**EventDescGetTask**</span></span>](/windows/desktop/api/Evntprov/nf-evntprov-eventdescgettask)  
[<span data-ttu-id="81368-113">**евентдескжетверсион**</span><span class="sxs-lookup"><span data-stu-id="81368-113">**EventDescGetVersion**</span></span>](/windows/desktop/api/Evntprov/nf-evntprov-eventdescgetversion)  
[<span data-ttu-id="81368-114">**евентдескоркэйворд**</span><span class="sxs-lookup"><span data-stu-id="81368-114">**EventDescOrKeyword**</span></span>](/windows/desktop/api/Evntprov/nf-evntprov-eventdescorkeyword)  
[<span data-ttu-id="81368-115">**евентдесксетчаннел**</span><span class="sxs-lookup"><span data-stu-id="81368-115">**EventDescSetChannel**</span></span>](/windows/desktop/api/Evntprov/nf-evntprov-eventdescsetchannel)  
[<span data-ttu-id="81368-116">**евентдесксетид**</span><span class="sxs-lookup"><span data-stu-id="81368-116">**EventDescSetId**</span></span>](/windows/desktop/api/Evntprov/nf-evntprov-eventdescsetid)  
[<span data-ttu-id="81368-117">**евентдесксеткэйворд**</span><span class="sxs-lookup"><span data-stu-id="81368-117">**EventDescSetKeyword**</span></span>](/windows/desktop/api/Evntprov/nf-evntprov-eventdescsetkeyword)  
[<span data-ttu-id="81368-118">**евентдесксетлевел**</span><span class="sxs-lookup"><span data-stu-id="81368-118">**EventDescSetLevel**</span></span>](/windows/desktop/api/Evntprov/nf-evntprov-eventdescsetlevel)  
[<span data-ttu-id="81368-119">**евентдесксетопкоде**</span><span class="sxs-lookup"><span data-stu-id="81368-119">**EventDescSetOpcode**</span></span>](/windows/desktop/api/Evntprov/nf-evntprov-eventdescsetopcode)  
[<span data-ttu-id="81368-120">**евентдесксеттаск**</span><span class="sxs-lookup"><span data-stu-id="81368-120">**EventDescSetTask**</span></span>](/windows/desktop/api/Evntprov/nf-evntprov-eventdescsettask)  
[<span data-ttu-id="81368-121">**евентдесксетверсион**</span><span class="sxs-lookup"><span data-stu-id="81368-121">**EventDescSetVersion**</span></span>](/windows/desktop/api/Evntprov/nf-evntprov-eventdescsetversion)  
[<span data-ttu-id="81368-122">**евентдескзеро**</span><span class="sxs-lookup"><span data-stu-id="81368-122">**EventDescZero**</span></span>](/windows/desktop/api/Evntprov/nf-evntprov-eventdesczero)  
</dl>

 

 



