---
description: Реализует интерфейс Иинканализер.
ms.assetid: f17de375-a0fe-4024-bf2a-60f8de8b0345
title: Класс InkAnalyzer (Иаком. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- InkAnalyzer
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 49eeb04b1568bbef785f7d750315e0ea39491d92
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105692154"
---
# <a name="inkanalyzer-class"></a><span data-ttu-id="3abc1-103">Класс InkAnalyzer</span><span class="sxs-lookup"><span data-stu-id="3abc1-103">InkAnalyzer class</span></span>

<span data-ttu-id="3abc1-104">Реализует интерфейс [**иинканализер**](iinkanalyzer.md) .</span><span class="sxs-lookup"><span data-stu-id="3abc1-104">Implements the [**IInkAnalyzer**](iinkanalyzer.md) interface.</span></span>

## <a name="remarks"></a><span data-ttu-id="3abc1-105">Комментарии</span><span class="sxs-lookup"><span data-stu-id="3abc1-105">Remarks</span></span>

<span data-ttu-id="3abc1-106">Этот класс реализует COM-интерфейс [**иинканализер**](iinkanalyzer.md) .</span><span class="sxs-lookup"><span data-stu-id="3abc1-106">This class implements the [**IInkAnalyzer**](iinkanalyzer.md) COM interface.</span></span>

<span data-ttu-id="3abc1-107">[ \_ Ианалисисевентс](-ianalysisevents.md) является источником событий по умолчанию и предоставляет стандартные события для [**иинканализер**](iinkanalyzer.md).</span><span class="sxs-lookup"><span data-stu-id="3abc1-107">[\_IAnalysisEvents](-ianalysisevents.md) is the default source of events and provides standard events for the [**IInkAnalyzer**](iinkanalyzer.md).</span></span>

<span data-ttu-id="3abc1-108">[**\_ Ианалисиспроксевентс**](-ianalysisproxyevents.md) предоставляет события прокси-сервера данных для [**иинканализер**](iinkanalyzer.md).</span><span class="sxs-lookup"><span data-stu-id="3abc1-108">[**\_IAnalysisProxyEvents**](-ianalysisproxyevents.md) provides the data proxy events for the [**IInkAnalyzer**](iinkanalyzer.md).</span></span> <span data-ttu-id="3abc1-109">Дополнительные сведения см. [в разделе Учетная запись-посредник данных с помощью анализа рукописного ввода](data-proxy-with-ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="3abc1-109">For more information, see [Data Proxy with Ink Analysis](data-proxy-with-ink-analysis.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="3abc1-110">Требования</span><span class="sxs-lookup"><span data-stu-id="3abc1-110">Requirements</span></span>



| <span data-ttu-id="3abc1-111">Требование</span><span class="sxs-lookup"><span data-stu-id="3abc1-111">Requirement</span></span> | <span data-ttu-id="3abc1-112">Значение</span><span class="sxs-lookup"><span data-stu-id="3abc1-112">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3abc1-113">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="3abc1-113">Minimum supported client</span></span><br/> | <span data-ttu-id="3abc1-114">Только классические приложения Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="3abc1-114">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="3abc1-115">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="3abc1-115">Minimum supported server</span></span><br/> | <span data-ttu-id="3abc1-116">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="3abc1-116">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="3abc1-117">Header</span><span class="sxs-lookup"><span data-stu-id="3abc1-117">Header</span></span><br/>                   | <dl> <span data-ttu-id="3abc1-118"><dt>Иаком. h (также требуется Иаком \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="3abc1-118"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="3abc1-119">DLL</span><span class="sxs-lookup"><span data-stu-id="3abc1-119">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3abc1-120"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3abc1-120"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="3abc1-121">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="3abc1-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3abc1-122">**аналисисмодес**</span><span class="sxs-lookup"><span data-stu-id="3abc1-122">**AnalysisModes**</span></span>](analysismodes.md)
</dt> <dt>

[<span data-ttu-id="3abc1-123">**ианалисисалтернате**</span><span class="sxs-lookup"><span data-stu-id="3abc1-123">**IAnalysisAlternate**</span></span>](ianalysisalternate.md)
</dt> <dt>

[<span data-ttu-id="3abc1-124">**ианалисисстатус**</span><span class="sxs-lookup"><span data-stu-id="3abc1-124">**IAnalysisStatus**</span></span>](ianalysisstatus.md)
</dt> <dt>

[<span data-ttu-id="3abc1-125">**иконтекстлинк**</span><span class="sxs-lookup"><span data-stu-id="3abc1-125">**IContextLink**</span></span>](icontextlink.md)
</dt> <dt>

[<span data-ttu-id="3abc1-126">**иконтекстноде**</span><span class="sxs-lookup"><span data-stu-id="3abc1-126">**IContextNode**</span></span>](icontextnode.md)
</dt> <dt>

[<span data-ttu-id="3abc1-127">Справочник по анализу рукописного ввода</span><span class="sxs-lookup"><span data-stu-id="3abc1-127">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




