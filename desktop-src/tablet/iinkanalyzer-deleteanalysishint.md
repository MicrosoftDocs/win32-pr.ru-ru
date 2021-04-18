---
description: Удаляет указание анализа из Иинканализер.
ms.assetid: ba5498d4-d31c-4b3f-9004-0448e18d4835
title: 'Иинканализер: метод:D Елетеаналисишинт (Иаком. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.DeleteAnalysisHint
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: f84f718701abd5bc76b55427aab9df072f758c3a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104145478"
---
# <a name="iinkanalyzerdeleteanalysishint-method"></a><span data-ttu-id="9c125-103">Иинканализер: метод:D Елетеаналисишинт</span><span class="sxs-lookup"><span data-stu-id="9c125-103">IInkAnalyzer::DeleteAnalysisHint method</span></span>

<span data-ttu-id="9c125-104">Удаляет указание анализа из [**иинканализер**](iinkanalyzer.md).</span><span class="sxs-lookup"><span data-stu-id="9c125-104">Removes an analysis hint from the [**IInkAnalyzer**](iinkanalyzer.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="9c125-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="9c125-105">Syntax</span></span>


```C++
HRESULT DeleteAnalysisHint(
  [in] IContextNode *pHintToDelete
);
```



## <a name="parameters"></a><span data-ttu-id="9c125-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="9c125-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9c125-107">*финттоделете* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="9c125-107">*pHintToDelete* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9c125-108">Указание по анализу из [**иинканализер**](iinkanalyzer.md).</span><span class="sxs-lookup"><span data-stu-id="9c125-108">The analysis hint from the [**IInkAnalyzer**](iinkanalyzer.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9c125-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="9c125-109">Return value</span></span>

<span data-ttu-id="9c125-110">Описание возвращаемых значений см. в разделе [классы и интерфейсы — анализ рукописного ввода](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="9c125-110">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="9c125-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="9c125-111">Remarks</span></span>

<span data-ttu-id="9c125-112">Удаление подсказки анализа не помечает область подсказки для переанализа.</span><span class="sxs-lookup"><span data-stu-id="9c125-112">Removing an analysis hint does not mark the hint's area for reanalysis.</span></span> <span data-ttu-id="9c125-113">Чтобы пометить область в подсказке для переанализа, используйте [**метод иинканализер:: сетдиртирегион**](iinkanalyzer-setdirtyregion.md) , чтобы задать для "грязной" области объединение текущей "грязной" области и области указания по анализу.</span><span class="sxs-lookup"><span data-stu-id="9c125-113">To mark the area within the hint for reanalysis, use [**IInkAnalyzer::SetDirtyRegion Method**](iinkanalyzer-setdirtyregion.md) to set the dirty region to the union of the current dirty region and area of the analysis hint.</span></span>

<span data-ttu-id="9c125-114">Указание удаляется из анализатора; Однако сам [**иконтекстноде**](icontextnode.md) не удаляется.</span><span class="sxs-lookup"><span data-stu-id="9c125-114">The hint is removed from the analyzer; however, the [**IContextNode**](icontextnode.md) itself is not deleted.</span></span>

<span data-ttu-id="9c125-115">Этот метод возвращает код ошибки, если *финттоделете* является [**иконтекстноде**](icontextnode.md) , который не относится к типу Аналисишинт (см. [**иконтекстноде:: GetType**](icontextnode-gettype.md)).</span><span class="sxs-lookup"><span data-stu-id="9c125-115">This method returns an error code when *pHintToDelete* is a [**IContextNode**](icontextnode.md) that is not of type AnalysisHint (see [**IContextNode::GetType**](icontextnode-gettype.md)).</span></span>

## <a name="requirements"></a><span data-ttu-id="9c125-116">Требования</span><span class="sxs-lookup"><span data-stu-id="9c125-116">Requirements</span></span>



| <span data-ttu-id="9c125-117">Требование</span><span class="sxs-lookup"><span data-stu-id="9c125-117">Requirement</span></span> | <span data-ttu-id="9c125-118">Значение</span><span class="sxs-lookup"><span data-stu-id="9c125-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9c125-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="9c125-119">Minimum supported client</span></span><br/> | <span data-ttu-id="9c125-120">Только классические приложения Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="9c125-120">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="9c125-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="9c125-121">Minimum supported server</span></span><br/> | <span data-ttu-id="9c125-122">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="9c125-122">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="9c125-123">Header</span><span class="sxs-lookup"><span data-stu-id="9c125-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="9c125-124"><dt>Иаком. h (также требуется Иаком \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="9c125-124"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="9c125-125">DLL</span><span class="sxs-lookup"><span data-stu-id="9c125-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9c125-126"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9c125-126"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="9c125-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="9c125-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9c125-128">**иинканализер**</span><span class="sxs-lookup"><span data-stu-id="9c125-128">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="9c125-129">**Метод Иинканализер:: Креатеаналисишинт**</span><span class="sxs-lookup"><span data-stu-id="9c125-129">**IInkAnalyzer::CreateAnalysisHint Method**</span></span>](iinkanalyzer-createanalysishint.md)
</dt> <dt>

[<span data-ttu-id="9c125-130">**Метод Иинканализер:: Жетаналисишинтс**</span><span class="sxs-lookup"><span data-stu-id="9c125-130">**IInkAnalyzer::GetAnalysisHints Method**</span></span>](iinkanalyzer-getanalysishints.md)
</dt> <dt>

[<span data-ttu-id="9c125-131">**Метод Иинканализер:: Жетаналисишинтсбинаме**</span><span class="sxs-lookup"><span data-stu-id="9c125-131">**IInkAnalyzer::GetAnalysisHintsByName Method**</span></span>](iinkanalyzer-getanalysishintsbyname.md)
</dt> <dt>

[<span data-ttu-id="9c125-132">Справочник по анализу рукописного ввода</span><span class="sxs-lookup"><span data-stu-id="9c125-132">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




