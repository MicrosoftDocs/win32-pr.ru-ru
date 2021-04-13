---
description: Изменяет текущий верхний альтернативный вариант на указанный Ианалисисалтернате.
ms.assetid: 0867a662-d172-4ca2-a41f-49c0ea454768
title: 'Метод Иинканализер:: Модифитопалтернатевисконфирматион (Иаком. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.ModifyTopAlternateWithConfirmation
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 60b0221e7d27cfd5d601dcf77e80a297045d39a7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104343692"
---
# <a name="iinkanalyzermodifytopalternatewithconfirmation-method"></a><span data-ttu-id="60f15-103">Метод Иинканализер:: Модифитопалтернатевисконфирматион</span><span class="sxs-lookup"><span data-stu-id="60f15-103">IInkAnalyzer::ModifyTopAlternateWithConfirmation method</span></span>

<span data-ttu-id="60f15-104">Изменяет текущий верхний альтернативный вариант на указанный [**ианалисисалтернате**](ianalysisalternate.md).</span><span class="sxs-lookup"><span data-stu-id="60f15-104">Changes the current top alternate to the specified [**IAnalysisAlternate**](ianalysisalternate.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="60f15-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="60f15-105">Syntax</span></span>


```C++
HRESULT ModifyTopAlternateWithConfirmation(
  [in] IAnalysisAlternate *alternate,
  [in] VARIANT_BOOL       fconfirmAutomatically
);
```



## <a name="parameters"></a><span data-ttu-id="60f15-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="60f15-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="60f15-107">*альтернативный вариант* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="60f15-107">*alternate* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="60f15-108">Альтернативный анализ, который можно задать в качестве нового верхнего альтернативного.</span><span class="sxs-lookup"><span data-stu-id="60f15-108">The analysis alternate to set as the new top alternate.</span></span>

</dd> <dt>

<span data-ttu-id="60f15-109">*фконфирмаутоматикалли* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="60f15-109">*fconfirmAutomatically* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="60f15-110">**Вариант \_ Значение TRUE** , чтобы задать все узлы конечного контекста, которые соответствуют анализу, альтернативному типу подтверждения **конфирматионтипе \_ нодетипеандпропертиес** (см [**. Иконтекстноде:: Confirm**](icontextnode-isconfirmed.md) и [**конфирматионтипе**](confirmationtype.md)); **Вариант \_ Значение FALSE** , чтобы задать все узлы конечного контекста, которые соответствуют анализу, альтернативному типу подтверждения **конфирматионтипе \_ None**.</span><span class="sxs-lookup"><span data-stu-id="60f15-110">**VARIANT\_TRUE** to set all of the ink leaf context nodes that correspond to the analysis alternate to a confirmation type of **ConfirmationType\_NodeTypeAndProperties** (see [**IContextNode::IsConfirmed**](icontextnode-isconfirmed.md) and [**ConfirmationType**](confirmationtype.md)); **VARIANT\_FALSE** to set all of the ink leaf context nodes that correspond to the analysis alternate to a confirmation type of **ConfirmationType\_None**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="60f15-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="60f15-111">Return value</span></span>

<span data-ttu-id="60f15-112">Описание возвращаемых значений см. в разделе [классы и интерфейсы — анализ рукописного ввода](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="60f15-112">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="60f15-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="60f15-113">Remarks</span></span>

<span data-ttu-id="60f15-114">Для получения вариантов анализа используйте метод [**иинканализер:: alternate**](iinkanalyzer-getalternates.md), [**Иинканализер:: Жеталтернатесфорконтекстнодес**](iinkanalyzer-getalternatesforcontextnodes.md)или [**метод иинканализер:: жеталтернатесфорстрокес**](iinkanalyzer-getalternatesforstrokes.md).</span><span class="sxs-lookup"><span data-stu-id="60f15-114">To get analysis alternates, use [**IInkAnalyzer::GetAlternates Method**](iinkanalyzer-getalternates.md), [**IInkAnalyzer::GetAlternatesForContextNodes Method**](iinkanalyzer-getalternatesforcontextnodes.md), or [**IInkAnalyzer::GetAlternatesForStrokes Method**](iinkanalyzer-getalternatesforstrokes.md).</span></span> <span data-ttu-id="60f15-115">Чтобы получить объекты узла контекста, связанные с альтернативным анализом, используйте [**метод ианалисисалтернате:: жеталтернатенодес**](ianalysisalternate-getalternatenodes.md).</span><span class="sxs-lookup"><span data-stu-id="60f15-115">To get the context node objects associated with an analysis alternate, use [**IAnalysisAlternate::GetAlternateNodes Method**](ianalysisalternate-getalternatenodes.md).</span></span>

<span data-ttu-id="60f15-116">Чтобы изменить тип подтверждения для контекстного узла, используйте [**иконтекстноде:: Confirm**](icontextnode-confirm.md).</span><span class="sxs-lookup"><span data-stu-id="60f15-116">To change the confirmation type for a context node, use [**IContextNode::Confirm**](icontextnode-confirm.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="60f15-117">Требования</span><span class="sxs-lookup"><span data-stu-id="60f15-117">Requirements</span></span>



| <span data-ttu-id="60f15-118">Требование</span><span class="sxs-lookup"><span data-stu-id="60f15-118">Requirement</span></span> | <span data-ttu-id="60f15-119">Значение</span><span class="sxs-lookup"><span data-stu-id="60f15-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="60f15-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="60f15-120">Minimum supported client</span></span><br/> | <span data-ttu-id="60f15-121">Только классические приложения Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="60f15-121">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="60f15-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="60f15-122">Minimum supported server</span></span><br/> | <span data-ttu-id="60f15-123">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="60f15-123">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="60f15-124">Header</span><span class="sxs-lookup"><span data-stu-id="60f15-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="60f15-125"><dt>Иаком. h (также требуется Иаком \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="60f15-125"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="60f15-126">DLL</span><span class="sxs-lookup"><span data-stu-id="60f15-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="60f15-127"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="60f15-127"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="60f15-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="60f15-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="60f15-129">**иинканализер**</span><span class="sxs-lookup"><span data-stu-id="60f15-129">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="60f15-130">**ианалисисалтернате**</span><span class="sxs-lookup"><span data-stu-id="60f15-130">**IAnalysisAlternate**</span></span>](ianalysisalternate.md)
</dt> <dt>

[<span data-ttu-id="60f15-131">**иконтекстноде**</span><span class="sxs-lookup"><span data-stu-id="60f15-131">**IContextNode**</span></span>](icontextnode.md)
</dt> <dt>

[<span data-ttu-id="60f15-132">**Анализ рукописного ввода Конфирматионтипе**</span><span class="sxs-lookup"><span data-stu-id="60f15-132">**Ink Analysis ConfirmationType**</span></span>](confirmationtype.md)
</dt> <dt>

[<span data-ttu-id="60f15-133">Ссылки</span><span class="sxs-lookup"><span data-stu-id="60f15-133">Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




