---
description: Получает флаги, определяющие, как Иинканализер выполняет анализ рукописного ввода.
ms.assetid: 982cb9cd-2d73-4064-9a6e-fe123adf0fb6
title: 'Метод Иинканализер:: Жетаналисисмодес (Иаком. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.GetAnalysisModes
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: d03ec255b10dd607889768795b00f5b2aff4dc11
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105701603"
---
# <a name="iinkanalyzergetanalysismodes-method"></a><span data-ttu-id="ebbe8-103">Метод Иинканализер:: Жетаналисисмодес</span><span class="sxs-lookup"><span data-stu-id="ebbe8-103">IInkAnalyzer::GetAnalysisModes method</span></span>

<span data-ttu-id="ebbe8-104">Получает флаги, определяющие, как [**иинканализер**](iinkanalyzer.md) выполняет анализ рукописного ввода.</span><span class="sxs-lookup"><span data-stu-id="ebbe8-104">Retrieves flags that control how the [**IInkAnalyzer**](iinkanalyzer.md) performs ink analysis.</span></span>

## <a name="syntax"></a><span data-ttu-id="ebbe8-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ebbe8-105">Syntax</span></span>


```C++
HRESULT GetAnalysisModes(
  [out] AnalysisModes *pAnalysisMode
);
```



## <a name="parameters"></a><span data-ttu-id="ebbe8-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="ebbe8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ebbe8-107">*паналисисмоде* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="ebbe8-107">*pAnalysisMode* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ebbe8-108">Побитовое сочетание значений перечисления [**аналисисмодес**](analysismodes.md) .</span><span class="sxs-lookup"><span data-stu-id="ebbe8-108">A bitwise combination of the [**AnalysisModes**](analysismodes.md) enumeration values.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ebbe8-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="ebbe8-109">Return value</span></span>

<span data-ttu-id="ebbe8-110">Описание возвращаемых значений см. в разделе [классы и интерфейсы — анализ рукописного ввода](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="ebbe8-110">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="ebbe8-111">Требования</span><span class="sxs-lookup"><span data-stu-id="ebbe8-111">Requirements</span></span>



| <span data-ttu-id="ebbe8-112">Требование</span><span class="sxs-lookup"><span data-stu-id="ebbe8-112">Requirement</span></span> | <span data-ttu-id="ebbe8-113">Значение</span><span class="sxs-lookup"><span data-stu-id="ebbe8-113">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ebbe8-114">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="ebbe8-114">Minimum supported client</span></span><br/> | <span data-ttu-id="ebbe8-115">Только классические приложения Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="ebbe8-115">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="ebbe8-116">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="ebbe8-116">Minimum supported server</span></span><br/> | <span data-ttu-id="ebbe8-117">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="ebbe8-117">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="ebbe8-118">Header</span><span class="sxs-lookup"><span data-stu-id="ebbe8-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="ebbe8-119"><dt>Иаком. h (также требуется Иаком \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="ebbe8-119"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="ebbe8-120">DLL</span><span class="sxs-lookup"><span data-stu-id="ebbe8-120">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ebbe8-121"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ebbe8-121"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="ebbe8-122">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ebbe8-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ebbe8-123">**иинканализер**</span><span class="sxs-lookup"><span data-stu-id="ebbe8-123">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="ebbe8-124">**аналисисмодес**</span><span class="sxs-lookup"><span data-stu-id="ebbe8-124">**AnalysisModes**</span></span>](analysismodes.md)
</dt> <dt>

[<span data-ttu-id="ebbe8-125">**Метод Иинканализер:: Analyze**</span><span class="sxs-lookup"><span data-stu-id="ebbe8-125">**IInkAnalyzer::Analyze Method**</span></span>](iinkanalyzer-analyze.md)
</dt> <dt>

[<span data-ttu-id="ebbe8-126">**Метод Иинканализер:: Баккграунданализе**</span><span class="sxs-lookup"><span data-stu-id="ebbe8-126">**IInkAnalyzer::BackgroundAnalyze Method**</span></span>](iinkanalyzer-backgroundanalyze.md)
</dt> <dt>

[<span data-ttu-id="ebbe8-127">**Метод Иинканализер:: Сетаналисисмодес**</span><span class="sxs-lookup"><span data-stu-id="ebbe8-127">**IInkAnalyzer::SetAnalysisModes Method**</span></span>](iinkanalyzer-setanalysismodes.md)
</dt> <dt>

[<span data-ttu-id="ebbe8-128">Справочник по анализу рукописного ввода</span><span class="sxs-lookup"><span data-stu-id="ebbe8-128">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




