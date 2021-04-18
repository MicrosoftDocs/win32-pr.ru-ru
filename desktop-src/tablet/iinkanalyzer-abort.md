---
description: Отменяет текущую операцию анализа.
ms.assetid: 909bfa66-b6df-4730-95b7-809fc2170e85
title: 'Метод Иинканализер:: Abort (Иаком. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.Abort
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: eac96809bfbe41e7d6a070782da3ffd0f6407c60
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105711125"
---
# <a name="iinkanalyzerabort-method"></a><span data-ttu-id="0ee49-103">Метод Иинканализер:: Abort</span><span class="sxs-lookup"><span data-stu-id="0ee49-103">IInkAnalyzer::Abort method</span></span>

<span data-ttu-id="0ee49-104">Отменяет текущую операцию анализа.</span><span class="sxs-lookup"><span data-stu-id="0ee49-104">Cancels the current analysis operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="0ee49-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="0ee49-105">Syntax</span></span>


```C++
HRESULT Abort(
  [out] IAnalysisRegion **ppAbortedRegion
);
```



## <a name="parameters"></a><span data-ttu-id="0ee49-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="0ee49-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0ee49-107">*ппабортедрегион* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="0ee49-107">*ppAbortedRegion* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0ee49-108">Указатель на объект [**ианалисисрегион**](ianalysisregion.md) , представляющий "грязную" область (см. [**метод Иинканализер:: жетдиртирегион**](iinkanalyzer-getdirtyregion.md)) текущей операции анализа.</span><span class="sxs-lookup"><span data-stu-id="0ee49-108">A pointer to an [**IAnalysisRegion**](ianalysisregion.md) that represents the dirty region (see [**IInkAnalyzer::GetDirtyRegion Method**](iinkanalyzer-getdirtyregion.md)) of the current analysis operation.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0ee49-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="0ee49-109">Return value</span></span>

<span data-ttu-id="0ee49-110">Описание возвращаемых значений см. в разделе [классы и интерфейсы — анализ рукописного ввода](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="0ee49-110">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="0ee49-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="0ee49-111">Remarks</span></span>

<span data-ttu-id="0ee49-112">Вызовите [**IUnknown:: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) в *ппабортедрегион* , когда больше не нужно использовать объект.</span><span class="sxs-lookup"><span data-stu-id="0ee49-112">Call [**IUnknown::Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) on *ppAbortedRegion* when you no longer need to use the object.</span></span>

<span data-ttu-id="0ee49-113">Этот метод отменяет текущую операцию анализа.</span><span class="sxs-lookup"><span data-stu-id="0ee49-113">This method cancels the current analysis operation.</span></span>

<span data-ttu-id="0ee49-114">Если *ппабортедрегион* имеет **значение NULL**, метод Abort выполняется как обычная, так как это указывает на то, что вызывающий объект не имеет интереса в возвращаемом значении.</span><span class="sxs-lookup"><span data-stu-id="0ee49-114">When *ppAbortedRegion* is **NULL**, this method performs the abort as normal, because this indicates that the caller has no interest in the return value.</span></span>

<span data-ttu-id="0ee49-115">**Метод иинканализер:: Abort** останавливает события [**\_ ианалисисевентс:: Results**](-ianalysisevents-results.md) и [**\_ ианалисисевентс:: Activity**](-ianalysisevents-activity.md) для текущей операции анализа.</span><span class="sxs-lookup"><span data-stu-id="0ee49-115">**IInkAnalyzer::Abort Method** silences the [**\_IAnalysisEvents::Results**](-ianalysisevents-results.md) and [**\_IAnalysisEvents::Activity**](-ianalysisevents-activity.md) events for the current analysis operation.</span></span>

<span data-ttu-id="0ee49-116">**Метод иинканализер:: Abort** выполняется асинхронно до отмены текущей фоновой операции анализа.</span><span class="sxs-lookup"><span data-stu-id="0ee49-116">**IInkAnalyzer::Abort Method** runs asynchronously until the current background analysis operation is canceled.</span></span> <span data-ttu-id="0ee49-117">Поскольку процесс отмены является асинхронным, приложение может выполнять другие задачи во время отмены текущего анализа опертионс.</span><span class="sxs-lookup"><span data-stu-id="0ee49-117">Because the cancellation process is asynchronous, the application can perform other tasks while the current analysis opertions is canceled.</span></span>

<span data-ttu-id="0ee49-118">Если операций анализа не выполняется, этот метод возвращает пустой регион анализа.</span><span class="sxs-lookup"><span data-stu-id="0ee49-118">If no analysis operations are in progress, this method returns an empty analysis region.</span></span>

<span data-ttu-id="0ee49-119">Если выполняется одна операция анализа, этот метод отменяет операцию.</span><span class="sxs-lookup"><span data-stu-id="0ee49-119">If one analysis operation is in progress, this method cancels the operation.</span></span>

<span data-ttu-id="0ee49-120">Если выполняется как синхронные, так и асинхронные операции анализа, этот метод отменяет синхронную операцию.</span><span class="sxs-lookup"><span data-stu-id="0ee49-120">If both synchronous and asynchronous analysis operations are in progress, this method cancels the synchronous operation.</span></span>

<span data-ttu-id="0ee49-121">Если этот метод вызывается более одного раза для одной и той же операции анализа, первый вызов возвращает "грязную" область для операции, а последующие вызовы возвращают пустой регион.</span><span class="sxs-lookup"><span data-stu-id="0ee49-121">If this method is called more than once for the same analysis operation, the first call returns the dirty region for the operation, and the subsequent calls return an empty region.</span></span>

<span data-ttu-id="0ee49-122">Если приложение поддерживает собственную структуру данных, которая синхронизирована с [**иинканализер**](iinkanalyzer.md), вызов **метода Иинканализер:: Abort** может привести к невозможности выполнения документа с частичными результатами.</span><span class="sxs-lookup"><span data-stu-id="0ee49-122">If your application maintains its own data structure that is synchronized with that of the [**IInkAnalyzer**](iinkanalyzer.md), calling **IInkAnalyzer::Abort Method** can leave your document with partial results.</span></span> <span data-ttu-id="0ee49-123">Чтобы избежать этого, не вызывайте **метод иинканализер:: Abort** между моментом, когда **иинканализер** получает событие [**\_ ианалисиспроксевентс:: Инканализерстатечангинг**](-ianalysisproxyevents-inkanalyzerstatechanging.md) , и время, которое **иинканализер** получает событие [**\_ IAnalysisEvents:: IntermediateResults**](-ianalysisevents-intermediateresults.md) или [**\_ IAnalysisEvents:: Results**](-ianalysisevents-results.md) .</span><span class="sxs-lookup"><span data-stu-id="0ee49-123">To avoid this, do not call **IInkAnalyzer::Abort Method** between the time the **IInkAnalyzer** receives the [**\_IAnalysisProxyEvents::InkAnalyzerStateChanging**](-ianalysisproxyevents-inkanalyzerstatechanging.md) event and the time the **IInkAnalyzer** receives the [**\_IAnalysisEvents::IntermediateResults**](-ianalysisevents-intermediateresults.md) or [**\_IAnalysisEvents::Results**](-ianalysisevents-results.md) event.</span></span>

<span data-ttu-id="0ee49-124">Дополнительные сведения о синхронизации данных приложения с помощью анализатора рукописного ввода см. в разделе [учетная запись-посредник данных с анализом рукописного ввода](data-proxy-with-ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="0ee49-124">For more information about synchronizing your application data with the ink analyzer, see [Data Proxy with Ink Analysis](data-proxy-with-ink-analysis.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="0ee49-125">Требования</span><span class="sxs-lookup"><span data-stu-id="0ee49-125">Requirements</span></span>



| <span data-ttu-id="0ee49-126">Требование</span><span class="sxs-lookup"><span data-stu-id="0ee49-126">Requirement</span></span> | <span data-ttu-id="0ee49-127">Значение</span><span class="sxs-lookup"><span data-stu-id="0ee49-127">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0ee49-128">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="0ee49-128">Minimum supported client</span></span><br/> | <span data-ttu-id="0ee49-129">Только классические приложения Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="0ee49-129">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="0ee49-130">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="0ee49-130">Minimum supported server</span></span><br/> | <span data-ttu-id="0ee49-131">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="0ee49-131">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="0ee49-132">Header</span><span class="sxs-lookup"><span data-stu-id="0ee49-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="0ee49-133"><dt>Иаком. h (также требуется Иаком \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="0ee49-133"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="0ee49-134">DLL</span><span class="sxs-lookup"><span data-stu-id="0ee49-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0ee49-135"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0ee49-135"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="0ee49-136">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="0ee49-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0ee49-137">**иинканализер**</span><span class="sxs-lookup"><span data-stu-id="0ee49-137">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="0ee49-138">**Метод Иинканализер:: Analyze**</span><span class="sxs-lookup"><span data-stu-id="0ee49-138">**IInkAnalyzer::Analyze Method**</span></span>](iinkanalyzer-analyze.md)
</dt> <dt>

[<span data-ttu-id="0ee49-139">**Метод Иинканализер:: Баккграунданализе**</span><span class="sxs-lookup"><span data-stu-id="0ee49-139">**IInkAnalyzer::BackgroundAnalyze Method**</span></span>](iinkanalyzer-backgroundanalyze.md)
</dt> <dt>

[<span data-ttu-id="0ee49-140">**Метод Иинканализер:: Жетдиртирегион**</span><span class="sxs-lookup"><span data-stu-id="0ee49-140">**IInkAnalyzer::GetDirtyRegion Method**</span></span>](iinkanalyzer-getdirtyregion.md)
</dt> <dt>

[<span data-ttu-id="0ee49-141">**Метод Иинканализер:: Сетдиртирегион**</span><span class="sxs-lookup"><span data-stu-id="0ee49-141">**IInkAnalyzer::SetDirtyRegion Method**</span></span>](iinkanalyzer-setdirtyregion.md)
</dt> <dt>

[<span data-ttu-id="0ee49-142">Справочник по анализу рукописного ввода</span><span class="sxs-lookup"><span data-stu-id="0ee49-142">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

