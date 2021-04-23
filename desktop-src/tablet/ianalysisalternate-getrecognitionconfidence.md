---
description: Возвращает значение, указывающее уровень достоверности, который Иинканализер имеет точность Ианалисисалтернате.
ms.assetid: ac1c68df-2e0c-4633-b7ee-519482a4d67a
title: 'Метод Ианалисисалтернате:: Жетрекогнитионконфиденце (Иаком. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAnalysisAlternate.GetRecognitionConfidence
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: eacaf7e5a8feaddcd437e68cf7acfa4fc5a7fc80
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103810061"
---
# <a name="ianalysisalternategetrecognitionconfidence-method"></a><span data-ttu-id="ff35a-103">Метод Ианалисисалтернате:: Жетрекогнитионконфиденце</span><span class="sxs-lookup"><span data-stu-id="ff35a-103">IAnalysisAlternate::GetRecognitionConfidence method</span></span>

<span data-ttu-id="ff35a-104">Возвращает значение, указывающее уровень достоверности, который [**иинканализер**](iinkanalyzer.md) имеет точность [**ианалисисалтернате**](ianalysisalternate.md).</span><span class="sxs-lookup"><span data-stu-id="ff35a-104">Gets a value that indicates the level of confidence that the [**IInkAnalyzer**](iinkanalyzer.md) has in the accuracy of the [**IAnalysisAlternate**](ianalysisalternate.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="ff35a-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ff35a-105">Syntax</span></span>


```C++
HRESULT GetRecognitionConfidence(
  [out] RecognitionConfidence *pConfidence
);
```



## <a name="parameters"></a><span data-ttu-id="ff35a-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="ff35a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ff35a-107">*пконфиденце* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="ff35a-107">*pConfidence* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ff35a-108">Указатель на [**перечисление инкрекогнитионконфиденце**](/windows/desktop/api/msinkaut/ne-msinkaut-inkrecognitionconfidence) , которое указывает уровень достоверности, который [**иинканалисисрекогнизер**](iinkanalysisrecognizer.md) имеет точность альтернативного распознавания.</span><span class="sxs-lookup"><span data-stu-id="ff35a-108">A pointer to an [**InkRecognitionConfidence Enumeration**](/windows/desktop/api/msinkaut/ne-msinkaut-inkrecognitionconfidence) that indicates the level of confidence that the [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) has in the accuracy of the recognition alternate.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ff35a-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="ff35a-109">Return value</span></span>

<span data-ttu-id="ff35a-110">Описание возвращаемых значений см. в разделе [классы и интерфейсы — анализ рукописного ввода](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="ff35a-110">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="ff35a-111">Требования</span><span class="sxs-lookup"><span data-stu-id="ff35a-111">Requirements</span></span>



| <span data-ttu-id="ff35a-112">Требование</span><span class="sxs-lookup"><span data-stu-id="ff35a-112">Requirement</span></span> | <span data-ttu-id="ff35a-113">Значение</span><span class="sxs-lookup"><span data-stu-id="ff35a-113">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ff35a-114">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="ff35a-114">Minimum supported client</span></span><br/> | <span data-ttu-id="ff35a-115">Только классические приложения Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="ff35a-115">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="ff35a-116">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="ff35a-116">Minimum supported server</span></span><br/> | <span data-ttu-id="ff35a-117">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="ff35a-117">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="ff35a-118">Header</span><span class="sxs-lookup"><span data-stu-id="ff35a-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="ff35a-119"><dt>Иаком. h (также требуется Иаком \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="ff35a-119"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="ff35a-120">DLL</span><span class="sxs-lookup"><span data-stu-id="ff35a-120">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ff35a-121"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ff35a-121"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="ff35a-122">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ff35a-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ff35a-123">**ианалисисалтернате**</span><span class="sxs-lookup"><span data-stu-id="ff35a-123">**IAnalysisAlternate**</span></span>](ianalysisalternate.md)
</dt> <dt>

[<span data-ttu-id="ff35a-124">**иинканализер**</span><span class="sxs-lookup"><span data-stu-id="ff35a-124">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="ff35a-125">**иинканалисисрекогнизер**</span><span class="sxs-lookup"><span data-stu-id="ff35a-125">**IInkAnalysisRecognizer**</span></span>](iinkanalysisrecognizer.md)
</dt> <dt>

[<span data-ttu-id="ff35a-126">**рекогнитионконфиденце**</span><span class="sxs-lookup"><span data-stu-id="ff35a-126">**RecognitionConfidence**</span></span>](recognitionconfidence.md)
</dt> <dt>

[<span data-ttu-id="ff35a-127">Справочник по анализу рукописного ввода</span><span class="sxs-lookup"><span data-stu-id="ff35a-127">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




