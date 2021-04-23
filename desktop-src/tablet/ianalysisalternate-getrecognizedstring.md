---
description: Возвращает распознанное строковое значение объекта Ианалисисалтернате.
ms.assetid: cdf41824-77a4-4c71-8712-f380a6cbf4c5
title: 'Метод Ианалисисалтернате:: Жетрекогнизедстринг (Иаком. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAnalysisAlternate.GetRecognizedString
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 5489773b29ade35d4b7297065c1104bfecefa117
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104542119"
---
# <a name="ianalysisalternategetrecognizedstring-method"></a><span data-ttu-id="ae5d9-103">Метод Ианалисисалтернате:: Жетрекогнизедстринг</span><span class="sxs-lookup"><span data-stu-id="ae5d9-103">IAnalysisAlternate::GetRecognizedString method</span></span>

<span data-ttu-id="ae5d9-104">Возвращает распознанное строковое значение объекта [**ианалисисалтернате**](ianalysisalternate.md) .</span><span class="sxs-lookup"><span data-stu-id="ae5d9-104">Gets the recognized string value of the [**IAnalysisAlternate**](ianalysisalternate.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="ae5d9-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ae5d9-105">Syntax</span></span>


```C++
HRESULT GetRecognizedString(
  [out] BSTR *pbstrRecognizedString
);
```



## <a name="parameters"></a><span data-ttu-id="ae5d9-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="ae5d9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ae5d9-107">*пбстррекогнизедстринг* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="ae5d9-107">*pbstrRecognizedString* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ae5d9-108">Указатель на строку **BSTR** , для которой задано распознанное строковое значение.</span><span class="sxs-lookup"><span data-stu-id="ae5d9-108">A pointer to the **BSTR** that is set to the recognized string value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ae5d9-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="ae5d9-109">Return value</span></span>

<span data-ttu-id="ae5d9-110">Описание возвращаемых значений см. в разделе [классы и интерфейсы — анализ рукописного ввода](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="ae5d9-110">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="ae5d9-111">Требования</span><span class="sxs-lookup"><span data-stu-id="ae5d9-111">Requirements</span></span>



| <span data-ttu-id="ae5d9-112">Требование</span><span class="sxs-lookup"><span data-stu-id="ae5d9-112">Requirement</span></span> | <span data-ttu-id="ae5d9-113">Значение</span><span class="sxs-lookup"><span data-stu-id="ae5d9-113">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ae5d9-114">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="ae5d9-114">Minimum supported client</span></span><br/> | <span data-ttu-id="ae5d9-115">Только классические приложения Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="ae5d9-115">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="ae5d9-116">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="ae5d9-116">Minimum supported server</span></span><br/> | <span data-ttu-id="ae5d9-117">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="ae5d9-117">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="ae5d9-118">Header</span><span class="sxs-lookup"><span data-stu-id="ae5d9-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="ae5d9-119"><dt>Иаком. h (также требуется Иаком \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="ae5d9-119"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="ae5d9-120">DLL</span><span class="sxs-lookup"><span data-stu-id="ae5d9-120">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ae5d9-121"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ae5d9-121"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="ae5d9-122">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ae5d9-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ae5d9-123">**ианалисисалтернате**</span><span class="sxs-lookup"><span data-stu-id="ae5d9-123">**IAnalysisAlternate**</span></span>](ianalysisalternate.md)
</dt> <dt>

[<span data-ttu-id="ae5d9-124">**Метод Иинканализер:: Жетрекогнизедстринг**</span><span class="sxs-lookup"><span data-stu-id="ae5d9-124">**IInkAnalyzer::GetRecognizedString Method**</span></span>](iinkanalyzer-getrecognizedstring.md)
</dt> </dl>

 

 




