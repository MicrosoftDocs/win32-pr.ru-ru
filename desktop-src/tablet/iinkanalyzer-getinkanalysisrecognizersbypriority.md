---
description: Извлекает упорядоченную коллекцию объектов Иинканалисисрекогнизер.
ms.assetid: 67399237-38e2-4905-a97c-10ca72c7799b
title: 'Метод Иинканализер:: Жетинканалисисрекогнизерсбиприорити (Иаком. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.GetInkAnalysisRecognizersByPriority
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: d596a8138f8ab16852ce99116eef66372ff2b074
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103897454"
---
# <a name="iinkanalyzergetinkanalysisrecognizersbypriority-method"></a><span data-ttu-id="2e359-103">Метод Иинканализер:: Жетинканалисисрекогнизерсбиприорити</span><span class="sxs-lookup"><span data-stu-id="2e359-103">IInkAnalyzer::GetInkAnalysisRecognizersByPriority method</span></span>

<span data-ttu-id="2e359-104">Извлекает упорядоченную коллекцию объектов [**иинканалисисрекогнизер**](iinkanalysisrecognizer.md) .</span><span class="sxs-lookup"><span data-stu-id="2e359-104">Retrieves an ordered collection of [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) objects.</span></span>

## <a name="syntax"></a><span data-ttu-id="2e359-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="2e359-105">Syntax</span></span>


```C++
HRESULT GetInkAnalysisRecognizersByPriority(
  [out] IInkAnalysisRecognizers **ppInkAnalysisRecognizers
);
```



## <a name="parameters"></a><span data-ttu-id="2e359-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="2e359-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2e359-107">*ппинканалисисрекогнизерс* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="2e359-107">*ppInkAnalysisRecognizers* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2e359-108">Упорядоченная коллекция объектов [**иинканалисисрекогнизер**](iinkanalysisrecognizer.md) .</span><span class="sxs-lookup"><span data-stu-id="2e359-108">An ordered collection of [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) objects.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2e359-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="2e359-109">Return value</span></span>

<span data-ttu-id="2e359-110">Описание возвращаемых значений см. в разделе [классы и интерфейсы — анализ рукописного ввода](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="2e359-110">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="2e359-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="2e359-111">Remarks</span></span>

> [!Caution]  
> <span data-ttu-id="2e359-112">Чтобы избежать утечки памяти, вызовите метод [**IUnknown:: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) в *ппинканалисисрекогнизерс* , когда больше не нужно использовать объект.</span><span class="sxs-lookup"><span data-stu-id="2e359-112">To avoid a memory leak, call [**IUnknown::Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) on *ppInkAnalysisRecognizers* when you no longer need to use the object.</span></span>

 

<span data-ttu-id="2e359-113">Порядок распознавателей в этой коллекции указывает порядок, в котором [**иинканализер**](iinkanalyzer.md) оценивает доступные Распознаватели.</span><span class="sxs-lookup"><span data-stu-id="2e359-113">The order of the recognizers in this collection indicates the order in which the [**IInkAnalyzer**](iinkanalyzer.md) evaluates the available recognizers.</span></span> <span data-ttu-id="2e359-114">**Иинканализер** использует язык обводки в качестве основного критерия для применения [**иинканалисисрекогнизер**](iinkanalysisrecognizer.md).</span><span class="sxs-lookup"><span data-stu-id="2e359-114">The **IInkAnalyzer** uses the language of the strokes as its primary criterion for applying an [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md).</span></span> <span data-ttu-id="2e359-115">В качестве вторичного критерия **иинканализер** сравнивает сведения о подсказках анализа с поддерживаемыми возможностями объекта **иинканалисисрекогнизер** (см. [**иинканалисисрекогнизер::**](iinkanalysisrecognizer-getcapabilities.md)GetObject).</span><span class="sxs-lookup"><span data-stu-id="2e359-115">As a secondary criterion, the **IInkAnalyzer** compares analysis hint information against an **IInkAnalysisRecognizer** object's supported capabilities (see [**IInkAnalysisRecognizer::GetCapabilities**](iinkanalysisrecognizer-getcapabilities.md)).</span></span> <span data-ttu-id="2e359-116">Дополнительные сведения о указаниях по анализу см. в разделе [**метод иинканализер:: креатеаналисишинт**](iinkanalyzer-createanalysishint.md).</span><span class="sxs-lookup"><span data-stu-id="2e359-116">For more information about analysis hints, see [**IInkAnalyzer::CreateAnalysisHint Method**](iinkanalyzer-createanalysishint.md).</span></span>

<span data-ttu-id="2e359-117">Если в нескольких [**иинканалисисрекогнизер**](iinkanalysisrecognizer.md) поддерживается идентификатор языка, [**иинканализер**](iinkanalyzer.md) использует алгоритм "First-Fit" для выбора первого **иинканалисисрекогнизер** для анализа штрихов этого языка.</span><span class="sxs-lookup"><span data-stu-id="2e359-117">If more than one [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) supports a language identifier, the [**IInkAnalyzer**](iinkanalyzer.md) uses a "first-fit" algorithm to select the first **IInkAnalysisRecognizer** to analyze strokes of that language.</span></span>

## <a name="requirements"></a><span data-ttu-id="2e359-118">Требования</span><span class="sxs-lookup"><span data-stu-id="2e359-118">Requirements</span></span>



| <span data-ttu-id="2e359-119">Требование</span><span class="sxs-lookup"><span data-stu-id="2e359-119">Requirement</span></span> | <span data-ttu-id="2e359-120">Значение</span><span class="sxs-lookup"><span data-stu-id="2e359-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2e359-121">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="2e359-121">Minimum supported client</span></span><br/> | <span data-ttu-id="2e359-122">Только классические приложения Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="2e359-122">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="2e359-123">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="2e359-123">Minimum supported server</span></span><br/> | <span data-ttu-id="2e359-124">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="2e359-124">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="2e359-125">Header</span><span class="sxs-lookup"><span data-stu-id="2e359-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="2e359-126"><dt>Иаком. h (также требуется Иаком \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="2e359-126"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="2e359-127">DLL</span><span class="sxs-lookup"><span data-stu-id="2e359-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2e359-128"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2e359-128"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="2e359-129">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="2e359-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2e359-130">**иинканализер**</span><span class="sxs-lookup"><span data-stu-id="2e359-130">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="2e359-131">**иинканалисисрекогнизерс**</span><span class="sxs-lookup"><span data-stu-id="2e359-131">**IInkAnalysisRecognizers**</span></span>](iinkanalysisrecognizers.md)
</dt> <dt>

[<span data-ttu-id="2e359-132">**Метод Иинканализер:: Сесигхестприоритинканалисисрекогнизер**</span><span class="sxs-lookup"><span data-stu-id="2e359-132">**IInkAnalyzer::SetHighestPriorityInkAnalysisRecognizer Method**</span></span>](iinkanalyzer-sethighestpriorityinkanalysisrecognizer.md)
</dt> <dt>

[<span data-ttu-id="2e359-133">Справочник по анализу рукописного ввода</span><span class="sxs-lookup"><span data-stu-id="2e359-133">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

