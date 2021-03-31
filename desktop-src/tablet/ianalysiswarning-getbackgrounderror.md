---
description: Возвращает код ошибки для фоновой операции анализа рукописного ввода, если произошла ошибка.
ms.assetid: 0255751e-9b2a-46f1-aa45-6509f9d1c658
title: 'Метод Ианалисисварнинг:: Жетбаккграундеррор (Иаком. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAnalysisWarning.GetBackgroundError
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 4367b1d52ee5d2a3bb65af0e4edd4922b8ae9a92
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104263156"
---
# <a name="ianalysiswarninggetbackgrounderror-method"></a><span data-ttu-id="ff1b1-103">Метод Ианалисисварнинг:: Жетбаккграундеррор</span><span class="sxs-lookup"><span data-stu-id="ff1b1-103">IAnalysisWarning::GetBackgroundError method</span></span>

<span data-ttu-id="ff1b1-104">Возвращает код ошибки для фоновой операции анализа рукописного ввода, если произошла ошибка.</span><span class="sxs-lookup"><span data-stu-id="ff1b1-104">Retrieves the error code for the background ink analysis operation if an error occurred.</span></span>

## <a name="syntax"></a><span data-ttu-id="ff1b1-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ff1b1-105">Syntax</span></span>


```C++
HRESULT GetBackgroundError();
```



## <a name="parameters"></a><span data-ttu-id="ff1b1-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="ff1b1-106">Parameters</span></span>

<span data-ttu-id="ff1b1-107">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="ff1b1-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="ff1b1-108">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="ff1b1-108">Return value</span></span>

<span data-ttu-id="ff1b1-109">Описание возвращаемых значений см. в разделе [классы и интерфейсы — анализ рукописного ввода](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="ff1b1-109">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="ff1b1-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="ff1b1-110">Remarks</span></span>

<span data-ttu-id="ff1b1-111">Если ошибка возникает в фоновой операции анализа, [**иинканализер**](iinkanalyzer.md) не может вернуть код ошибки, так как он происходит в другом потоке.</span><span class="sxs-lookup"><span data-stu-id="ff1b1-111">If an error occurs within a background analysis operation, the [**IInkAnalyzer**](iinkanalyzer.md) cannot return the error code because it is occurring in a different thread.</span></span> <span data-ttu-id="ff1b1-112">Вместо этого обработчик событий [**\_ ианалисисевентс:: Results**](-ianalysisevents-results.md) получает [**ианалисисстатус**](ianalysisstatus.md) , содержащий [**ианалисисварнинг**](ianalysiswarning.md) с [**аналисисварнингкоде**](/windows/desktop/tablet/analysiswarningcode) **аналисисварнингкоде \_** BackgroundException.</span><span class="sxs-lookup"><span data-stu-id="ff1b1-112">Instead, the [**\_IAnalysisEvents::Results**](-ianalysisevents-results.md) event handler receives an [**IAnalysisStatus**](ianalysisstatus.md) that contains an [**IAnalysisWarning**](ianalysiswarning.md) with an [**AnalysisWarningCode**](/windows/desktop/tablet/analysiswarningcode) of **AnalysisWarningCode\_BackgroundException**.</span></span> <span data-ttu-id="ff1b1-113">Этот **ианалисисварнинг** содержит код ошибки для фоновой операции анализа.</span><span class="sxs-lookup"><span data-stu-id="ff1b1-113">This **IAnalysisWarning** contains the error code for the background analysis operation.</span></span> <span data-ttu-id="ff1b1-114">В общем случае обработчик событий **\_ ианалисисевентс:: Results** вернет этот код ошибки, чтобы его можно было обработать в любом расположении приложения.</span><span class="sxs-lookup"><span data-stu-id="ff1b1-114">In general, your **\_IAnalysisEvents::Results** event handler will return this error code so that it can be handled elsewhere in your application.</span></span>

## <a name="requirements"></a><span data-ttu-id="ff1b1-115">Требования</span><span class="sxs-lookup"><span data-stu-id="ff1b1-115">Requirements</span></span>



| <span data-ttu-id="ff1b1-116">Требование</span><span class="sxs-lookup"><span data-stu-id="ff1b1-116">Requirement</span></span> | <span data-ttu-id="ff1b1-117">Значение</span><span class="sxs-lookup"><span data-stu-id="ff1b1-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ff1b1-118">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="ff1b1-118">Minimum supported client</span></span><br/> | <span data-ttu-id="ff1b1-119">Только классические приложения Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="ff1b1-119">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="ff1b1-120">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="ff1b1-120">Minimum supported server</span></span><br/> | <span data-ttu-id="ff1b1-121">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="ff1b1-121">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="ff1b1-122">Header</span><span class="sxs-lookup"><span data-stu-id="ff1b1-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="ff1b1-123"><dt>Иаком. h (также требуется Иаком \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="ff1b1-123"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="ff1b1-124">DLL</span><span class="sxs-lookup"><span data-stu-id="ff1b1-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ff1b1-125"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ff1b1-125"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="ff1b1-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ff1b1-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ff1b1-127">**ианалисисварнинг**</span><span class="sxs-lookup"><span data-stu-id="ff1b1-127">**IAnalysisWarning**</span></span>](ianalysiswarning.md)
</dt> <dt>

[<span data-ttu-id="ff1b1-128">**ианалисисстатус**</span><span class="sxs-lookup"><span data-stu-id="ff1b1-128">**IAnalysisStatus**</span></span>](ianalysisstatus.md)
</dt> <dt>

[<span data-ttu-id="ff1b1-129">**Метод Иинканализер:: Баккграунданализе**</span><span class="sxs-lookup"><span data-stu-id="ff1b1-129">**IInkAnalyzer::BackgroundAnalyze Method**</span></span>](iinkanalyzer-backgroundanalyze.md)
</dt> <dt>

[<span data-ttu-id="ff1b1-130">**\_Ианалисисевентс:: Results**</span><span class="sxs-lookup"><span data-stu-id="ff1b1-130">**\_IAnalysisEvents::Results**</span></span>](-ianalysisevents-results.md)
</dt> <dt>

[<span data-ttu-id="ff1b1-131">**аналисисварнингкоде**</span><span class="sxs-lookup"><span data-stu-id="ff1b1-131">**AnalysisWarningCode**</span></span>](/windows/desktop/tablet/analysiswarningcode)
</dt> <dt>

[<span data-ttu-id="ff1b1-132">Справочник по анализу рукописного ввода</span><span class="sxs-lookup"><span data-stu-id="ff1b1-132">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

