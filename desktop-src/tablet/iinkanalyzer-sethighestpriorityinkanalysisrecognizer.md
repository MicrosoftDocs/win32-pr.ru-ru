---
description: Перемещает указанный Иинканалисисрекогнизер в первую точку в списке распознавателей рукописного ввода в объекте Иинканализер.
ms.assetid: 9126187f-02dd-4988-91b8-c4f3d3b6f773
title: 'Метод Иинканализер:: Сесигхестприоритинканалисисрекогнизер (Иаком. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.SetHighestPriorityInkAnalysisRecognizer
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 534b94e4f2964aa81f04e0adac6f45f346c530c4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103897450"
---
# <a name="iinkanalyzersethighestpriorityinkanalysisrecognizer-method"></a><span data-ttu-id="98d7f-103">Метод Иинканализер:: Сесигхестприоритинканалисисрекогнизер</span><span class="sxs-lookup"><span data-stu-id="98d7f-103">IInkAnalyzer::SetHighestPriorityInkAnalysisRecognizer method</span></span>

<span data-ttu-id="98d7f-104">Перемещает указанный [**иинканалисисрекогнизер**](iinkanalysisrecognizer.md) в первую точку в списке распознавателей рукописного ввода в объекте [**иинканализер**](iinkanalyzer.md) .</span><span class="sxs-lookup"><span data-stu-id="98d7f-104">Moves the specified [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) to the first position in the [**IInkAnalyzer**](iinkanalyzer.md) object's list of ink recognizers.</span></span>

## <a name="syntax"></a><span data-ttu-id="98d7f-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="98d7f-105">Syntax</span></span>


```C++
HRESULT SetHighestPriorityInkAnalysisRecognizer(
  [in] IInkAnalysisRecognizer *pInkAnalysisRecognizer
);
```



## <a name="parameters"></a><span data-ttu-id="98d7f-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="98d7f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="98d7f-107">*пинканалисисрекогнизер* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="98d7f-107">*pInkAnalysisRecognizer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="98d7f-108">[**Иинканалисисрекогнизер**](iinkanalysisrecognizer.md) , помещаемый в первую позицию.</span><span class="sxs-lookup"><span data-stu-id="98d7f-108">The [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) to place in the first position.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="98d7f-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="98d7f-109">Return value</span></span>

<span data-ttu-id="98d7f-110">Описание возвращаемых значений см. в разделе [классы и интерфейсы — анализ рукописного ввода](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="98d7f-110">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="98d7f-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="98d7f-111">Remarks</span></span>

<span data-ttu-id="98d7f-112">Чтобы получить список распознавателей рукописного ввода в порядке приоритета, вызовите [**метод иинканализер:: жетинканалисисрекогнизерсбиприорити**](iinkanalyzer-getinkanalysisrecognizersbypriority.md).</span><span class="sxs-lookup"><span data-stu-id="98d7f-112">To get the list of ink recognizers in priority order, call [**IInkAnalyzer::GetInkAnalysisRecognizersByPriority Method**](iinkanalyzer-getinkanalysisrecognizersbypriority.md).</span></span>

<span data-ttu-id="98d7f-113">Этот метод не влияет на порядок остальных объектов [**иинканалисисрекогнизер**](iinkanalysisrecognizer.md) в списке распознавателей рукописного ввода в объекте [**иинканализер**](iinkanalyzer.md) .</span><span class="sxs-lookup"><span data-stu-id="98d7f-113">This method does not affect the order of the rest of the [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) objects in the [**IInkAnalyzer**](iinkanalyzer.md) object's list of ink recognizers.</span></span>

<span data-ttu-id="98d7f-114">Порядок распознавателей рукописного ввода, возвращаемых [**методом иинканализер:: жетинканалисисрекогнизерсбиприорити**](iinkanalyzer-getinkanalysisrecognizersbypriority.md) , указывает порядок, в котором [**иинканализер**](iinkanalyzer.md) оценивает доступные объекты [**иинканалисисрекогнизер**](iinkanalysisrecognizer.md) .</span><span class="sxs-lookup"><span data-stu-id="98d7f-114">The order of the ink recognizers returned by [**IInkAnalyzer::GetInkAnalysisRecognizersByPriority Method**](iinkanalyzer-getinkanalysisrecognizersbypriority.md) indicates the order in which the [**IInkAnalyzer**](iinkanalyzer.md) evaluates the available [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) objects.</span></span>

<span data-ttu-id="98d7f-115">Использование распознавателей рукописного ввода оценивается в соответствии с их порядком в списке.</span><span class="sxs-lookup"><span data-stu-id="98d7f-115">Use of the ink recognizers is evaluated based on their order in the list.</span></span>

<span data-ttu-id="98d7f-116">Во время анализа рукописного ввода [**иинканализер**](iinkanalyzer.md) перебирает Распознаватели рукописного ввода в своем списке до тех пор, пока не обнаружит распознаватель, поддерживающий язык и другие свойства штрихов.</span><span class="sxs-lookup"><span data-stu-id="98d7f-116">During ink analysis, the [**IInkAnalyzer**](iinkanalyzer.md) iterates through the ink recognizers in its list until it finds a recognizer that supports the language and other properties of the strokes.</span></span> <span data-ttu-id="98d7f-117">Этот распознаватель используется для распознавания рукописного ввода для этих штрихов.</span><span class="sxs-lookup"><span data-stu-id="98d7f-117">This recognizer is used for ink recognition for those strokes.</span></span>

<span data-ttu-id="98d7f-118">Если [**иинканализер**](iinkanalyzer.md) не находит [**иинканалисисрекогнизер**](iinkanalysisrecognizer.md) , который поддерживает набор штрихов во время анализа, **иинканализер** создает [**ианалисисварнинг**](ianalysiswarning.md) с кодом предупреждения **аналисисварнингкоде \_ InkAnalysisRecognizerNotInstalled** (см. [**IAnalysisWarning:: GetWarningCode**](ianalysiswarning-getwarningcode.md)).</span><span class="sxs-lookup"><span data-stu-id="98d7f-118">If the [**IInkAnalyzer**](iinkanalyzer.md) does not find an [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) that supports a set of strokes during analysis, the **IInkAnalyzer** generates an [**IAnalysisWarning**](ianalysiswarning.md) with a warning code of **AnalysisWarningCode\_InkAnalysisRecognizerNotInstalled** (see [**IAnalysisWarning::GetWarningCode**](ianalysiswarning-getwarningcode.md)).</span></span>

## <a name="requirements"></a><span data-ttu-id="98d7f-119">Требования</span><span class="sxs-lookup"><span data-stu-id="98d7f-119">Requirements</span></span>



| <span data-ttu-id="98d7f-120">Требование</span><span class="sxs-lookup"><span data-stu-id="98d7f-120">Requirement</span></span> | <span data-ttu-id="98d7f-121">Значение</span><span class="sxs-lookup"><span data-stu-id="98d7f-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="98d7f-122">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="98d7f-122">Minimum supported client</span></span><br/> | <span data-ttu-id="98d7f-123">Только классические приложения Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="98d7f-123">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="98d7f-124">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="98d7f-124">Minimum supported server</span></span><br/> | <span data-ttu-id="98d7f-125">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="98d7f-125">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="98d7f-126">Header</span><span class="sxs-lookup"><span data-stu-id="98d7f-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="98d7f-127"><dt>Иаком. h (также требуется Иаком \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="98d7f-127"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="98d7f-128">DLL</span><span class="sxs-lookup"><span data-stu-id="98d7f-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="98d7f-129"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="98d7f-129"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="98d7f-130">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="98d7f-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="98d7f-131">**иинканализер**</span><span class="sxs-lookup"><span data-stu-id="98d7f-131">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="98d7f-132">**Метод Иинканализер:: Жетинканалисисрекогнизерсбиприорити**</span><span class="sxs-lookup"><span data-stu-id="98d7f-132">**IInkAnalyzer::GetInkAnalysisRecognizersByPriority Method**</span></span>](iinkanalyzer-getinkanalysisrecognizersbypriority.md)
</dt> <dt>

[<span data-ttu-id="98d7f-133">**иинканалисисрекогнизерс**</span><span class="sxs-lookup"><span data-stu-id="98d7f-133">**IInkAnalysisRecognizers**</span></span>](iinkanalysisrecognizers.md)
</dt> <dt>

[<span data-ttu-id="98d7f-134">**ианалисисварнинг**</span><span class="sxs-lookup"><span data-stu-id="98d7f-134">**IAnalysisWarning**</span></span>](ianalysiswarning.md)
</dt> <dt>

[<span data-ttu-id="98d7f-135">Справочник по анализу рукописного ввода</span><span class="sxs-lookup"><span data-stu-id="98d7f-135">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




