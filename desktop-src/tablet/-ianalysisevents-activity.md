---
description: 'Происходит при вызове метода Иинканализер:: Analyze или Иинканализер:: Баккграунданализе.'
ms.assetid: 339b41c6-f388-4b81-b2bc-3705b39d9cc9
title: 'Событие _IAnalysisEvents:: Activity (Иаком. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- _IAnalysisEvents.Activity
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: f235d3414b0d514f32b4ebd197c04a8721968a2a
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/05/2021
ms.locfileid: "104351815"
---
# <a name="_ianalysiseventsactivity-event"></a><span data-ttu-id="79c96-103">\_Событие Ианалисисевентс:: Activity</span><span class="sxs-lookup"><span data-stu-id="79c96-103">\_IAnalysisEvents::Activity event</span></span>

<span data-ttu-id="79c96-104">Происходит при вызове метода [**иинканализер:: Analyze**](iinkanalyzer-analyze.md) или [**Иинканализер:: баккграунданализе**](iinkanalyzer-backgroundanalyze.md) .</span><span class="sxs-lookup"><span data-stu-id="79c96-104">Occurs when the [**IInkAnalyzer::Analyze**](iinkanalyzer-analyze.md) method or [**IInkAnalyzer::BackgroundAnalyze**](iinkanalyzer-backgroundanalyze.md) method is called.</span></span>

## <a name="syntax"></a><span data-ttu-id="79c96-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="79c96-105">Syntax</span></span>


```C++
HRESULT Activity();
```



## <a name="parameters"></a><span data-ttu-id="79c96-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="79c96-106">Parameters</span></span>

<span data-ttu-id="79c96-107">У этого события нет параметров.</span><span class="sxs-lookup"><span data-stu-id="79c96-107">This event has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="79c96-108">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="79c96-108">Return value</span></span>

<span data-ttu-id="79c96-109">Описание возвращаемых значений см. в разделе [классы и интерфейсы — анализ рукописного ввода](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="79c96-109">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="79c96-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="79c96-110">Remarks</span></span>

<span data-ttu-id="79c96-111">Это событие указывает, что [**иинканализер**](iinkanalyzer.md) выполняет анализ рукописного ввода.</span><span class="sxs-lookup"><span data-stu-id="79c96-111">This event indicates that the [**IInkAnalyzer**](iinkanalyzer.md) is performing ink analysis.</span></span> <span data-ttu-id="79c96-112">Это событие не указывает на ход выполнения операции анализа рукописного ввода.</span><span class="sxs-lookup"><span data-stu-id="79c96-112">This event does not indicate the progress of the ink analysis operation.</span></span>

<span data-ttu-id="79c96-113">Чтобы выполнить любое из следующих действий, реализуйте обработчик событий **\_ ианалисисевентс:: Activity** :</span><span class="sxs-lookup"><span data-stu-id="79c96-113">To do any of the following, implement an **\_IAnalysisEvents::Activity** event handler:</span></span>

-   <span data-ttu-id="79c96-114">Указывает пользователю, что анализатор рукописного ввода выполняет анализ рукописного ввода.</span><span class="sxs-lookup"><span data-stu-id="79c96-114">Indicate to the user that the ink analyzer is performing ink analysis.</span></span>
-   <span data-ttu-id="79c96-115">Обработка входных данных пользователя во время синхронного анализа.</span><span class="sxs-lookup"><span data-stu-id="79c96-115">Process user input during synchronous analysis.</span></span>
-   <span data-ttu-id="79c96-116">Получение уведомлений о системных запросах, таких как перерисовка окна приложения, во время анализа рукописного ввода.</span><span class="sxs-lookup"><span data-stu-id="79c96-116">Receive notification of system requests, such as repainting of the application's window, during ink analysis.</span></span>

<span data-ttu-id="79c96-117">[**Иинканализер**](iinkanalyzer.md) часто вызывает это событие на этапе анализа макета и на этапе классификации рукописного ввода и отрисовки.</span><span class="sxs-lookup"><span data-stu-id="79c96-117">The [**IInkAnalyzer**](iinkanalyzer.md) raises this event frequently during the layout analysis phase and the writing and drawing classification phase of ink analysis.</span></span> <span data-ttu-id="79c96-118">**Иинканализер** создает это событие на этапе распознавания рукописного ввода до и после доступа к распознавателю рукописного ввода.</span><span class="sxs-lookup"><span data-stu-id="79c96-118">The **IInkAnalyzer** raises this event during the handwriting recognition phase before and after accessing an ink recognizer.</span></span>

<span data-ttu-id="79c96-119">Количество событий действий, создаваемых [**иинканализер**](iinkanalyzer.md) , зависит от:</span><span class="sxs-lookup"><span data-stu-id="79c96-119">The number of activity events an [**IInkAnalyzer**](iinkanalyzer.md) generates is affected by:</span></span>

-   <span data-ttu-id="79c96-120">Распознаватель рукописного ввода, применяемый [**иинканализер**](iinkanalyzer.md) к распознаванию рукописного ввода.</span><span class="sxs-lookup"><span data-stu-id="79c96-120">The ink recognizer that the [**IInkAnalyzer**](iinkanalyzer.md) applies to ink recognition.</span></span>
-   <span data-ttu-id="79c96-121">Число и длина штрихов, которые анализирует [**иинканализер**](iinkanalyzer.md) .</span><span class="sxs-lookup"><span data-stu-id="79c96-121">The number and length of strokes that the [**IInkAnalyzer**](iinkanalyzer.md) is analyzing.</span></span>
-   <span data-ttu-id="79c96-122">Число штрихов, классифицированных как запись.</span><span class="sxs-lookup"><span data-stu-id="79c96-122">The number of strokes that are classified as writing.</span></span>

<span data-ttu-id="79c96-123">Дополнительные сведения о синхронизации данных приложения с помощью [**иинканализер**](iinkanalyzer.md)см. в разделе [учетная запись-посредник данных с помощью анализа рукописного ввода](data-proxy-with-ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="79c96-123">For more information about synchronizing your application data with the [**IInkAnalyzer**](iinkanalyzer.md), see [Data Proxy with Ink Analysis](data-proxy-with-ink-analysis.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="79c96-124">Требования</span><span class="sxs-lookup"><span data-stu-id="79c96-124">Requirements</span></span>



| <span data-ttu-id="79c96-125">Требование</span><span class="sxs-lookup"><span data-stu-id="79c96-125">Requirement</span></span> | <span data-ttu-id="79c96-126">Значение</span><span class="sxs-lookup"><span data-stu-id="79c96-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="79c96-127">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="79c96-127">Minimum supported client</span></span><br/> | <span data-ttu-id="79c96-128">Только классические приложения Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="79c96-128">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="79c96-129">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="79c96-129">Minimum supported server</span></span><br/> | <span data-ttu-id="79c96-130">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="79c96-130">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="79c96-131">Header</span><span class="sxs-lookup"><span data-stu-id="79c96-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="79c96-132"><dt>Иаком. h (также требуется Иаком \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="79c96-132"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="79c96-133">DLL</span><span class="sxs-lookup"><span data-stu-id="79c96-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="79c96-134"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="79c96-134"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="79c96-135">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="79c96-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="79c96-136">**\_ианалисисевентс**</span><span class="sxs-lookup"><span data-stu-id="79c96-136">**\_IAnalysisEvents**</span></span>](-ianalysisevents.md)
</dt> <dt>

[<span data-ttu-id="79c96-137">**\_ианалисиспроксевентс**</span><span class="sxs-lookup"><span data-stu-id="79c96-137">**\_IAnalysisProxyEvents**</span></span>](-ianalysisproxyevents.md)
</dt> <dt>

[<span data-ttu-id="79c96-138">**иинканализер**</span><span class="sxs-lookup"><span data-stu-id="79c96-138">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="79c96-139">**иинканалисисрекогнизер**</span><span class="sxs-lookup"><span data-stu-id="79c96-139">**IInkAnalysisRecognizer**</span></span>](iinkanalysisrecognizer.md)
</dt> <dt>

[<span data-ttu-id="79c96-140">**Метод Иинканализер:: Analyze**</span><span class="sxs-lookup"><span data-stu-id="79c96-140">**IInkAnalyzer::Analyze Method**</span></span>](iinkanalyzer-analyze.md)
</dt> <dt>

[<span data-ttu-id="79c96-141">**Метод Иинканализер:: Баккграунданализе**</span><span class="sxs-lookup"><span data-stu-id="79c96-141">**IInkAnalyzer::BackgroundAnalyze Method**</span></span>](iinkanalyzer-backgroundanalyze.md)
</dt> <dt>

[<span data-ttu-id="79c96-142">Справочник по анализу рукописного ввода</span><span class="sxs-lookup"><span data-stu-id="79c96-142">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




