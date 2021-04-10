---
description: Извлекает варианты анализа для штрихов с указанными идентификаторами Stroke.
ms.assetid: e8bc198e-de0b-49b7-9120-4298985dfe64
title: 'Метод Иинканализер:: Жеталтернатесфорстрокес (Иаком. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.GetAlternatesForStrokes
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 115b2cc1be4ba35614ada6fddd9c9fbcdfa76357
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104145463"
---
# <a name="iinkanalyzergetalternatesforstrokes-method"></a><span data-ttu-id="b3b74-103">Метод Иинканализер:: Жеталтернатесфорстрокес</span><span class="sxs-lookup"><span data-stu-id="b3b74-103">IInkAnalyzer::GetAlternatesForStrokes method</span></span>

<span data-ttu-id="b3b74-104">Извлекает варианты анализа для штрихов с указанными идентификаторами Stroke.</span><span class="sxs-lookup"><span data-stu-id="b3b74-104">Retrieves analysis alternates for the strokes with the specified stroke identifiers.</span></span>

## <a name="syntax"></a><span data-ttu-id="b3b74-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b3b74-105">Syntax</span></span>


```C++
HRESULT GetAlternatesForStrokes(
  [in]  ULONG              ulStrokeIdsCount,
  [in]  LONG               *plStrokes,
  [in]  ULONG              ulMaximumAlternates,
  [out] AnalysisAlternates **ppAlternates
);
```



## <a name="parameters"></a><span data-ttu-id="b3b74-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="b3b74-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b3b74-107">*улстрокеидскаунт* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="b3b74-107">*ulStrokeIdsCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b3b74-108">Число идентификаторов Stroke в *плстрокес*.</span><span class="sxs-lookup"><span data-stu-id="b3b74-108">The number of stroke identifiers in *plStrokes*.</span></span>

</dd> <dt>

<span data-ttu-id="b3b74-109">*плстрокес* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="b3b74-109">*plStrokes* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b3b74-110">Массив идентификаторов Stroke.</span><span class="sxs-lookup"><span data-stu-id="b3b74-110">The array of stroke identifiers.</span></span>

</dd> <dt>

<span data-ttu-id="b3b74-111">*улмаксимумалтернатес* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="b3b74-111">*ulMaximumAlternates* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b3b74-112">Максимальное число возвращаемых вариантов анализа.</span><span class="sxs-lookup"><span data-stu-id="b3b74-112">The maximum number of analysis alternatives returned.</span></span>

</dd> <dt>

<span data-ttu-id="b3b74-113">*ппалтернатес* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="b3b74-113">*ppAlternates* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b3b74-114">Объект [**ианалисисалтернатес**](ianalysisalternates.md) , содержащий альтернативные варианты анализа.</span><span class="sxs-lookup"><span data-stu-id="b3b74-114">The [**IAnalysisAlternates**](ianalysisalternates.md) object containing the analysis alternatives.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b3b74-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="b3b74-115">Return value</span></span>

<span data-ttu-id="b3b74-116">Описание возвращаемых значений см. в разделе [классы и интерфейсы — анализ рукописного ввода](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="b3b74-116">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="b3b74-117">Комментарии</span><span class="sxs-lookup"><span data-stu-id="b3b74-117">Remarks</span></span>

> [!Caution]  
> <span data-ttu-id="b3b74-118">Чтобы избежать утечки памяти, вызовите метод [**IUnknown:: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) в \* *ппалтернатес* , когда больше не нужно использовать объект.</span><span class="sxs-lookup"><span data-stu-id="b3b74-118">To avoid a memory leak, call [**IUnknown::Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) on \**ppAlternates* when you no longer need to use the object.</span></span>

 

<span data-ttu-id="b3b74-119">Top [**ианалисисалтернате**](ianalysisalternate.md) возвращается в качестве первой альтернативы коллекции.</span><span class="sxs-lookup"><span data-stu-id="b3b74-119">The top [**IAnalysisAlternate**](ianalysisalternate.md) is returned as the first alternate of the collection.</span></span>

<span data-ttu-id="b3b74-120">Указанные штрихи не должны представлять смежные области документа.</span><span class="sxs-lookup"><span data-stu-id="b3b74-120">The specified strokes do not have to represent adjacent areas of the document.</span></span>

## <a name="requirements"></a><span data-ttu-id="b3b74-121">Требования</span><span class="sxs-lookup"><span data-stu-id="b3b74-121">Requirements</span></span>



| <span data-ttu-id="b3b74-122">Требование</span><span class="sxs-lookup"><span data-stu-id="b3b74-122">Requirement</span></span> | <span data-ttu-id="b3b74-123">Значение</span><span class="sxs-lookup"><span data-stu-id="b3b74-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b3b74-124">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="b3b74-124">Minimum supported client</span></span><br/> | <span data-ttu-id="b3b74-125">Только классические приложения Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="b3b74-125">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="b3b74-126">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="b3b74-126">Minimum supported server</span></span><br/> | <span data-ttu-id="b3b74-127">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="b3b74-127">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="b3b74-128">Header</span><span class="sxs-lookup"><span data-stu-id="b3b74-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="b3b74-129"><dt>Иаком. h (также требуется Иаком \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="b3b74-129"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="b3b74-130">DLL</span><span class="sxs-lookup"><span data-stu-id="b3b74-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b3b74-131"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b3b74-131"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="b3b74-132">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b3b74-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b3b74-133">**иинканализер**</span><span class="sxs-lookup"><span data-stu-id="b3b74-133">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="b3b74-134">**ианалисисалтернате**</span><span class="sxs-lookup"><span data-stu-id="b3b74-134">**IAnalysisAlternate**</span></span>](ianalysisalternate.md)
</dt> <dt>

[<span data-ttu-id="b3b74-135">**ианалисисалтернатес**</span><span class="sxs-lookup"><span data-stu-id="b3b74-135">**IAnalysisAlternates**</span></span>](ianalysisalternates.md)
</dt> <dt>

[<span data-ttu-id="b3b74-136">**Метод Иинканализер:: Alternate**</span><span class="sxs-lookup"><span data-stu-id="b3b74-136">**IInkAnalyzer::GetAlternates Method**</span></span>](iinkanalyzer-getalternates.md)
</dt> <dt>

[<span data-ttu-id="b3b74-137">**Метод Иинканализер:: Жеталтернатесфорконтекстнодес**</span><span class="sxs-lookup"><span data-stu-id="b3b74-137">**IInkAnalyzer::GetAlternatesForContextNodes Method**</span></span>](iinkanalyzer-getalternatesforcontextnodes.md)
</dt> <dt>

[<span data-ttu-id="b3b74-138">**Метод Иинканализер:: Модифитопалтернате**</span><span class="sxs-lookup"><span data-stu-id="b3b74-138">**IInkAnalyzer::ModifyTopAlternate Method**</span></span>](iinkanalyzer-modifytopalternate.md)
</dt> <dt>

[<span data-ttu-id="b3b74-139">**Метод Иинканализер:: Модифитопалтернатевисконфирматион**</span><span class="sxs-lookup"><span data-stu-id="b3b74-139">**IInkAnalyzer::ModifyTopAlternateWithConfirmation Method**</span></span>](iinkanalyzer-modifytopalternatewithconfirmation.md)
</dt> <dt>

[<span data-ttu-id="b3b74-140">Справочник по анализу рукописного ввода</span><span class="sxs-lookup"><span data-stu-id="b3b74-140">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

