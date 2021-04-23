---
description: Извлекает подсказку анализа, вызвавшую это предупреждение.
ms.assetid: 715aa4b2-6c45-414b-96f2-44c73a073213
title: 'Метод Ианалисисварнинг:: optimize (Иаком. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAnalysisWarning.GetHint
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 2c38a22b799eb6836a85a42748f60207ee7e997e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105711142"
---
# <a name="ianalysiswarninggethint-method"></a><span data-ttu-id="dd00d-103">Метод Ианалисисварнинг:: NOEXPAND</span><span class="sxs-lookup"><span data-stu-id="dd00d-103">IAnalysisWarning::GetHint method</span></span>

<span data-ttu-id="dd00d-104">Извлекает подсказку анализа, вызвавшую это предупреждение.</span><span class="sxs-lookup"><span data-stu-id="dd00d-104">Retrieves the analysis hint that caused this warning.</span></span>

## <a name="syntax"></a><span data-ttu-id="dd00d-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="dd00d-105">Syntax</span></span>


```C++
HRESULT GetHint(
  [out] IContextNode **pAnalysisHint
);
```



## <a name="parameters"></a><span data-ttu-id="dd00d-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="dd00d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dd00d-107">*паналисишинт* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="dd00d-107">*pAnalysisHint* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="dd00d-108">Узел контекста указания анализа, вызвавший это предупреждение, или **значение NULL** , если указание анализа не вызвало это предупреждение.</span><span class="sxs-lookup"><span data-stu-id="dd00d-108">The analysis hint context node that caused this warning, or **NULL** if an analysis hint did not cause this warning.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dd00d-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="dd00d-109">Return value</span></span>

<span data-ttu-id="dd00d-110">Описание возвращаемых значений см. в разделе [классы и интерфейсы — анализ рукописного ввода](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="dd00d-110">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="dd00d-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="dd00d-111">Remarks</span></span>

> [!Caution]  
> <span data-ttu-id="dd00d-112">Чтобы избежать утечки памяти, вызовите метод [**IUnknown:: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) в \* *паналисишинт* , когда больше не нужно использовать узел контекста указания по анализу.</span><span class="sxs-lookup"><span data-stu-id="dd00d-112">To avoid a memory leak, call [**IUnknown::Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) on \**pAnalysisHint* when you no longer need to use the analysis hint context node.</span></span>

 

<span data-ttu-id="dd00d-113">Примером указания по анализу, создающему [**ианалисисварнинг**](ianalysiswarning.md) , является указание анализа, которое содержит неверно написанный фактоид.</span><span class="sxs-lookup"><span data-stu-id="dd00d-113">An example of an analysis hint that generates an [**IAnalysisWarning**](ianalysiswarning.md) is an analysis hint that contains an incorrectly spelled factoid.</span></span> <span data-ttu-id="dd00d-114">В этом случае анализ рукописного ввода возвращает [**ианалисисстатус**](ianalysisstatus.md) , содержащий **ианалисисварнинг** , который ссылается на узел контекста указания по анализу с ошибкой фактоид.</span><span class="sxs-lookup"><span data-stu-id="dd00d-114">In this case, ink analysis returns an [**IAnalysisStatus**](ianalysisstatus.md) that contains an **IAnalysisWarning** that references the analysis hint context node with the misspelled factoid.</span></span> <span data-ttu-id="dd00d-115">Кроме того, в этом случае метод [**ианалисисварнинг:: жетварнингкоде**](ianalysiswarning-getwarningcode.md) с предупреждением анализа возвращает значение [**аналисисварнингкоде**](/windows/desktop/tablet/analysiswarningcode) **аналисисварнингкоде \_ фактоиднотсуппортед**.</span><span class="sxs-lookup"><span data-stu-id="dd00d-115">Also, in this case, the analysis warning's [**IAnalysisWarning::GetWarningCode**](ianalysiswarning-getwarningcode.md) method returns an [**AnalysisWarningCode**](/windows/desktop/tablet/analysiswarningcode) value of **AnalysisWarningCode\_FactoidNotSupported**.</span></span>

## <a name="requirements"></a><span data-ttu-id="dd00d-116">Требования</span><span class="sxs-lookup"><span data-stu-id="dd00d-116">Requirements</span></span>



| <span data-ttu-id="dd00d-117">Требование</span><span class="sxs-lookup"><span data-stu-id="dd00d-117">Requirement</span></span> | <span data-ttu-id="dd00d-118">Значение</span><span class="sxs-lookup"><span data-stu-id="dd00d-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dd00d-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="dd00d-119">Minimum supported client</span></span><br/> | <span data-ttu-id="dd00d-120">Только классические приложения Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="dd00d-120">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="dd00d-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="dd00d-121">Minimum supported server</span></span><br/> | <span data-ttu-id="dd00d-122">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="dd00d-122">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="dd00d-123">Header</span><span class="sxs-lookup"><span data-stu-id="dd00d-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="dd00d-124"><dt>Иаком. h (также требуется Иаком \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="dd00d-124"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="dd00d-125">DLL</span><span class="sxs-lookup"><span data-stu-id="dd00d-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="dd00d-126"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="dd00d-126"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="dd00d-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="dd00d-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dd00d-128">**ианалисисварнинг**</span><span class="sxs-lookup"><span data-stu-id="dd00d-128">**IAnalysisWarning**</span></span>](ianalysiswarning.md)
</dt> <dt>

[<span data-ttu-id="dd00d-129">**ианалисисстатус**</span><span class="sxs-lookup"><span data-stu-id="dd00d-129">**IAnalysisStatus**</span></span>](ianalysisstatus.md)
</dt> <dt>

[<span data-ttu-id="dd00d-130">**Метод Иинканализер:: Analyze**</span><span class="sxs-lookup"><span data-stu-id="dd00d-130">**IInkAnalyzer::Analyze Method**</span></span>](iinkanalyzer-analyze.md)
</dt> <dt>

[<span data-ttu-id="dd00d-131">**Метод Иинканализер:: Баккграунданализе**</span><span class="sxs-lookup"><span data-stu-id="dd00d-131">**IInkAnalyzer::BackgroundAnalyze Method**</span></span>](iinkanalyzer-backgroundanalyze.md)
</dt> <dt>

[<span data-ttu-id="dd00d-132">**аналисисварнингкоде**</span><span class="sxs-lookup"><span data-stu-id="dd00d-132">**AnalysisWarningCode**</span></span>](/windows/desktop/tablet/analysiswarningcode)
</dt> <dt>

[<span data-ttu-id="dd00d-133">Справочник по анализу рукописного ввода</span><span class="sxs-lookup"><span data-stu-id="dd00d-133">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

