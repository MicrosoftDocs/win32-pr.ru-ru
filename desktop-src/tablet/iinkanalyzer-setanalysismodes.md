---
description: Изменяет флаги, определяющие, как Иинканализер выполняет анализ рукописного ввода.
ms.assetid: cb82edd0-1f15-4313-a286-1fcd715ac6df
title: 'Метод Иинканализер:: Сетаналисисмодес (Иаком. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.SetAnalysisModes
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 826d31fd5b61db2332ef953d55b2cf6c6331995b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104541994"
---
# <a name="iinkanalyzersetanalysismodes-method"></a><span data-ttu-id="7f660-103">Метод Иинканализер:: Сетаналисисмодес</span><span class="sxs-lookup"><span data-stu-id="7f660-103">IInkAnalyzer::SetAnalysisModes method</span></span>

<span data-ttu-id="7f660-104">Изменяет флаги, определяющие, как [**иинканализер**](iinkanalyzer.md) выполняет анализ рукописного ввода.</span><span class="sxs-lookup"><span data-stu-id="7f660-104">Modifies flags that control how the [**IInkAnalyzer**](iinkanalyzer.md) performs ink analysis.</span></span>

## <a name="syntax"></a><span data-ttu-id="7f660-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="7f660-105">Syntax</span></span>


```C++
HRESULT SetAnalysisModes(
  [in] AnalysisModes analysisMode
);
```



## <a name="parameters"></a><span data-ttu-id="7f660-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="7f660-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7f660-107">*аналисисмоде* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="7f660-107">*analysisMode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7f660-108">Побитовое сочетание значений перечисления [**аналисисмодес**](analysismodes.md) .</span><span class="sxs-lookup"><span data-stu-id="7f660-108">A bitwise combination of the [**AnalysisModes**](analysismodes.md) enumeration values.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7f660-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="7f660-109">Return value</span></span>

<span data-ttu-id="7f660-110">Описание возвращаемых значений см. в разделе [классы и интерфейсы — анализ рукописного ввода](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="7f660-110">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="7f660-111">Требования</span><span class="sxs-lookup"><span data-stu-id="7f660-111">Requirements</span></span>



| <span data-ttu-id="7f660-112">Требование</span><span class="sxs-lookup"><span data-stu-id="7f660-112">Requirement</span></span> | <span data-ttu-id="7f660-113">Значение</span><span class="sxs-lookup"><span data-stu-id="7f660-113">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7f660-114">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="7f660-114">Minimum supported client</span></span><br/> | <span data-ttu-id="7f660-115">Только классические приложения Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="7f660-115">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="7f660-116">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="7f660-116">Minimum supported server</span></span><br/> | <span data-ttu-id="7f660-117">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="7f660-117">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="7f660-118">Header</span><span class="sxs-lookup"><span data-stu-id="7f660-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="7f660-119"><dt>Иаком. h (также требуется Иаком \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="7f660-119"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="7f660-120">DLL</span><span class="sxs-lookup"><span data-stu-id="7f660-120">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7f660-121"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7f660-121"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="7f660-122">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="7f660-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7f660-123">**иинканализер**</span><span class="sxs-lookup"><span data-stu-id="7f660-123">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="7f660-124">**аналисисмодес**</span><span class="sxs-lookup"><span data-stu-id="7f660-124">**AnalysisModes**</span></span>](analysismodes.md)
</dt> <dt>

[<span data-ttu-id="7f660-125">**Метод Иинканализер:: Analyze**</span><span class="sxs-lookup"><span data-stu-id="7f660-125">**IInkAnalyzer::Analyze Method**</span></span>](iinkanalyzer-analyze.md)
</dt> <dt>

[<span data-ttu-id="7f660-126">**Метод Иинканализер:: Баккграунданализе**</span><span class="sxs-lookup"><span data-stu-id="7f660-126">**IInkAnalyzer::BackgroundAnalyze Method**</span></span>](iinkanalyzer-backgroundanalyze.md)
</dt> <dt>

[<span data-ttu-id="7f660-127">**Метод Иинканализер:: Жетаналисисмодес**</span><span class="sxs-lookup"><span data-stu-id="7f660-127">**IInkAnalyzer::GetAnalysisModes Method**</span></span>](iinkanalyzer-getanalysismodes.md)
</dt> <dt>

[<span data-ttu-id="7f660-128">Справочник по анализу рукописного ввода</span><span class="sxs-lookup"><span data-stu-id="7f660-128">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




