---
description: Указывает, как Иинканализер выполняет анализ рукописного ввода.
ms.assetid: bc526445-0c9c-4c53-8b02-32cf758266e6
title: Перечисление Аналисисмодес (Иаком. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AnalysisModes
api_type:
- HeaderDef
api_location:
- IACom.h
ms.openlocfilehash: b9fdebd3ef3cd505b49ff6c82f7609bc339af0a4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104423506"
---
# <a name="analysismodes-enumeration"></a><span data-ttu-id="0e410-103">Перечисление Аналисисмодес</span><span class="sxs-lookup"><span data-stu-id="0e410-103">AnalysisModes enumeration</span></span>

<span data-ttu-id="0e410-104">Указывает, как [**иинканализер**](iinkanalyzer.md) выполняет анализ рукописного ввода.</span><span class="sxs-lookup"><span data-stu-id="0e410-104">Specifies how the [**IInkAnalyzer**](iinkanalyzer.md) performs ink analysis.</span></span>

## <a name="syntax"></a><span data-ttu-id="0e410-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="0e410-105">Syntax</span></span>


```C++
typedef enum AnalysisModes { 
  AnalysisModes_None                     = 0x0000,
  AnalysisModes_AutomaticReconciliation  = 0x0002,
  AnalysisModes_StrokeCacheAutoCleanup   = 0x0004,
  AnalysisModes_PersonalizationEnabled   = 0x0008,
  AnalysisModes_Default                  = 0x000d
} AnalysisModes;
```



## <a name="constants"></a><span data-ttu-id="0e410-106">Константы</span><span class="sxs-lookup"><span data-stu-id="0e410-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="0e410-107"><span id="AnalysisModes_None"></span><span id="analysismodes_none"></span><span id="ANALYSISMODES_NONE"></span>**Аналисисмодес \_ None**</span><span class="sxs-lookup"><span data-stu-id="0e410-107"><span id="AnalysisModes_None"></span><span id="analysismodes_none"></span><span id="ANALYSISMODES_NONE"></span>**AnalysisModes\_None**</span></span>
</dt> <dd>

<span data-ttu-id="0e410-108">Не указаны режимы.</span><span class="sxs-lookup"><span data-stu-id="0e410-108">No modes are specified.</span></span>

</dd> <dt>

<span data-ttu-id="0e410-109"><span id="AnalysisModes_AutomaticReconciliation"></span><span id="analysismodes_automaticreconciliation"></span><span id="ANALYSISMODES_AUTOMATICRECONCILIATION"></span>**Аналисисмодес \_ аутоматикреконЦилиатион**</span><span class="sxs-lookup"><span data-stu-id="0e410-109"><span id="AnalysisModes_AutomaticReconciliation"></span><span id="analysismodes_automaticreconciliation"></span><span id="ANALYSISMODES_AUTOMATICRECONCILIATION"></span>**AnalysisModes\_AutomaticReconciliation**</span></span>
</dt> <dd>

<span data-ttu-id="0e410-110">Будет ли [**иинканализер**](iinkanalyzer.md) автоматически запускать операцию сверки, как только промежуточные или окончательные результаты будут готовы.</span><span class="sxs-lookup"><span data-stu-id="0e410-110">Whether the [**IInkAnalyzer**](iinkanalyzer.md) automatically starts the reconciliation operation as soon as the intermediate or final results are ready.</span></span>

<span data-ttu-id="0e410-111">Если этот режим включен, событие [**\_ ианалисисевентс:: реадитореконЦиле**](-ianalysisevents-readytoreconcile.md) не возникает.</span><span class="sxs-lookup"><span data-stu-id="0e410-111">If this mode is enabled, the [**\_IAnalysisEvents::ReadyToReconcile**](-ianalysisevents-readytoreconcile.md) event is not raised.</span></span> <span data-ttu-id="0e410-112">Если этот режим отключен, возникает событие **\_ ианалисисевентс:: реадитореконЦиле** .</span><span class="sxs-lookup"><span data-stu-id="0e410-112">If this mode is disabled, the **\_IAnalysisEvents::ReadyToReconcile** event is raised.</span></span>

</dd> <dt>

<span data-ttu-id="0e410-113"><span id="AnalysisModes_StrokeCacheAutoCleanup"></span><span id="analysismodes_strokecacheautocleanup"></span><span id="ANALYSISMODES_STROKECACHEAUTOCLEANUP"></span>**Аналисисмодес \_ строкекачеаутоклеануп**</span><span class="sxs-lookup"><span data-stu-id="0e410-113"><span id="AnalysisModes_StrokeCacheAutoCleanup"></span><span id="analysismodes_strokecacheautocleanup"></span><span id="ANALYSISMODES_STROKECACHEAUTOCLEANUP"></span>**AnalysisModes\_StrokeCacheAutoCleanup**</span></span>
</dt> <dd>

<span data-ttu-id="0e410-114">Будет ли [**иинканализер**](iinkanalyzer.md) автоматически очищать ненужные росчерки из кэша штрихов перед выполнением анализа.</span><span class="sxs-lookup"><span data-stu-id="0e410-114">Whether the [**IInkAnalyzer**](iinkanalyzer.md) automatically clears unneeded strokes from the stroke cache before performing analysis.</span></span>

<span data-ttu-id="0e410-115">Если этот режим включен, [**иинканализер**](iinkanalyzer.md) очищает данные о штрихах перед выполнением анализа.</span><span class="sxs-lookup"><span data-stu-id="0e410-115">If this mode is enabled, the [**IInkAnalyzer**](iinkanalyzer.md) clears the stroke data before performing analysis.</span></span> <span data-ttu-id="0e410-116">Код также должен обработано событие [**\_ ианалисисевентс:: упдатестрокескаче**](-ianalysisevents-updatestrokescache.md) .</span><span class="sxs-lookup"><span data-stu-id="0e410-116">Your code must also then handle the [**\_IAnalysisEvents::UpdateStrokesCache**](-ianalysisevents-updatestrokescache.md) event.</span></span> <span data-ttu-id="0e410-117">Если событие **\_ ианалисисевентс:: упдатестрокескаче** не обрабатывается, возникает исключение.</span><span class="sxs-lookup"><span data-stu-id="0e410-117">If the **\_IAnalysisEvents::UpdateStrokesCache** event is not handled, an exception is raised.</span></span> <span data-ttu-id="0e410-118">Эта проверка выполняется на стадиях анализа (или Баккграунданализе) и выверки.</span><span class="sxs-lookup"><span data-stu-id="0e410-118">This check is done both at the Analyze (or BackgroundAnalyze) and Reconciliation phases.</span></span>

<span data-ttu-id="0e410-119">Если этот режим отключен, [**иинканализер**](iinkanalyzer.md) не очищает данные росчерка.</span><span class="sxs-lookup"><span data-stu-id="0e410-119">If this mode is disabled, the [**IInkAnalyzer**](iinkanalyzer.md) does not clear the stroke data.</span></span> <span data-ttu-id="0e410-120">Чтобы очистить данные штриха, вызовите [**метод иинканализер:: клеарстрокедата**](iinkanalyzer-clearstrokedata.md).</span><span class="sxs-lookup"><span data-stu-id="0e410-120">To clear the stroke data, call [**IInkAnalyzer::ClearStrokeData Method**](iinkanalyzer-clearstrokedata.md).</span></span> <span data-ttu-id="0e410-121">Если этот режим отключен, вызывается событие [**\_ ианалисисевентс:: упдатестрокескаче**](-ianalysisevents-updatestrokescache.md) , поэтому **иинканализер** может получить последние данные о штрихах для всех штрихов, для которых был снят свой кэш.</span><span class="sxs-lookup"><span data-stu-id="0e410-121">If this mode is disabled, the [**\_IAnalysisEvents::UpdateStrokesCache**](-ianalysisevents-updatestrokescache.md) event is raised so the **IInkAnalyzer** can retrieve the latest stroke data for any strokes that have had their cache cleared.</span></span> <span data-ttu-id="0e410-122">Если кэш штрихов сброшен, но событие **\_ ианалисисевентс:: упдатестрокескаче** не обрабатывается, возникает исключение.</span><span class="sxs-lookup"><span data-stu-id="0e410-122">If the stroke cache is cleared, but the **\_IAnalysisEvents::UpdateStrokesCache** event is not handled, an exception is raised.</span></span>

</dd> <dt>

<span data-ttu-id="0e410-123"><span id="AnalysisModes_PersonalizationEnabled"></span><span id="analysismodes_personalizationenabled"></span><span id="ANALYSISMODES_PERSONALIZATIONENABLED"></span>**Аналисисмодес \_ персонализатионенаблед**</span><span class="sxs-lookup"><span data-stu-id="0e410-123"><span id="AnalysisModes_PersonalizationEnabled"></span><span id="analysismodes_personalizationenabled"></span><span id="ANALYSISMODES_PERSONALIZATIONENABLED"></span>**AnalysisModes\_PersonalizationEnabled**</span></span>
</dt> <dd>

<span data-ttu-id="0e410-124">Персонализация распознавания рукописного текста включена.</span><span class="sxs-lookup"><span data-stu-id="0e410-124">Personalization of handwriting recognition is enabled.</span></span>

</dd> <dt>

<span data-ttu-id="0e410-125"><span id="AnalysisModes_Default"></span><span id="analysismodes_default"></span><span id="ANALYSISMODES_DEFAULT"></span>**Аналисисмодес \_ по умолчанию**</span><span class="sxs-lookup"><span data-stu-id="0e410-125"><span id="AnalysisModes_Default"></span><span id="analysismodes_default"></span><span id="ANALYSISMODES_DEFAULT"></span>**AnalysisModes\_Default**</span></span>
</dt> <dd>

<span data-ttu-id="0e410-126">Все режимы включены.</span><span class="sxs-lookup"><span data-stu-id="0e410-126">All modes are enabled.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="0e410-127">Комментарии</span><span class="sxs-lookup"><span data-stu-id="0e410-127">Remarks</span></span>

<span data-ttu-id="0e410-128">Это перечисление позволяет побитовое сочетание значений его членов.</span><span class="sxs-lookup"><span data-stu-id="0e410-128">This enumeration allows a bitwise combination of its member values.</span></span>

## <a name="requirements"></a><span data-ttu-id="0e410-129">Требования</span><span class="sxs-lookup"><span data-stu-id="0e410-129">Requirements</span></span>



| <span data-ttu-id="0e410-130">Требование</span><span class="sxs-lookup"><span data-stu-id="0e410-130">Requirement</span></span> | <span data-ttu-id="0e410-131">Значение</span><span class="sxs-lookup"><span data-stu-id="0e410-131">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0e410-132">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="0e410-132">Minimum supported client</span></span><br/> | <span data-ttu-id="0e410-133">Только классические приложения Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="0e410-133">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="0e410-134">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="0e410-134">Minimum supported server</span></span><br/> | <span data-ttu-id="0e410-135">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="0e410-135">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="0e410-136">Header</span><span class="sxs-lookup"><span data-stu-id="0e410-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="0e410-137"><dt>Иаком. h (также требуется Иаком \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="0e410-137"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0e410-138">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="0e410-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0e410-139">**Метод Иинканализер:: Жетаналисисмодес**</span><span class="sxs-lookup"><span data-stu-id="0e410-139">**IInkAnalyzer::GetAnalysisModes Method**</span></span>](iinkanalyzer-getanalysismodes.md)
</dt> <dt>

[<span data-ttu-id="0e410-140">**Метод Иинканализер:: Сетаналисисмодес**</span><span class="sxs-lookup"><span data-stu-id="0e410-140">**IInkAnalyzer::SetAnalysisModes Method**</span></span>](iinkanalyzer-setanalysismodes.md)
</dt> <dt>

[<span data-ttu-id="0e410-141">**\_Ианалисисевентс:: Интермедиатересултс**</span><span class="sxs-lookup"><span data-stu-id="0e410-141">**\_IAnalysisEvents::IntermediateResults**</span></span>](-ianalysisevents-intermediateresults.md)
</dt> <dt>

[<span data-ttu-id="0e410-142">**\_Ианалисисевентс:: РеадитореконЦиле**</span><span class="sxs-lookup"><span data-stu-id="0e410-142">**\_IAnalysisEvents::ReadyToReconcile**</span></span>](-ianalysisevents-readytoreconcile.md)
</dt> <dt>

[<span data-ttu-id="0e410-143">**\_Ианалисисевентс:: Упдатестрокескаче**</span><span class="sxs-lookup"><span data-stu-id="0e410-143">**\_IAnalysisEvents::UpdateStrokesCache**</span></span>](-ianalysisevents-updatestrokescache.md)
</dt> <dt>

[<span data-ttu-id="0e410-144">Справочник по анализу рукописного ввода</span><span class="sxs-lookup"><span data-stu-id="0e410-144">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




