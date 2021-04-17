---
description: Изменяет текущий верхний альтернативный вариант на указанный альтернативный вариант и очищает тип подтверждения для всех объектов Иконтекстноде, связанных с альтернативой.
ms.assetid: a4ff7e82-623f-4501-9641-5235c3083757
title: 'Метод Иинканализер:: Модифитопалтернате (Иаком. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.ModifyTopAlternate
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: da2fcde7015e993e13e47673b271c560b6c3d72a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105711109"
---
# <a name="iinkanalyzermodifytopalternate-method"></a><span data-ttu-id="1c9e2-103">Метод Иинканализер:: Модифитопалтернате</span><span class="sxs-lookup"><span data-stu-id="1c9e2-103">IInkAnalyzer::ModifyTopAlternate method</span></span>

<span data-ttu-id="1c9e2-104">Изменяет текущий верхний альтернативный вариант на указанный альтернативный вариант и очищает тип подтверждения для всех объектов [**иконтекстноде**](icontextnode.md) , связанных с альтернативой.</span><span class="sxs-lookup"><span data-stu-id="1c9e2-104">Changes the current top alternate to the specified alternate and clears the confirmation type for all [**IContextNode**](icontextnode.md) objects associated with the alternate.</span></span>

## <a name="syntax"></a><span data-ttu-id="1c9e2-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="1c9e2-105">Syntax</span></span>


```C++
HRESULT ModifyTopAlternate(
  [in] IAnalysisAlternate *pAlternate
);
```



## <a name="parameters"></a><span data-ttu-id="1c9e2-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="1c9e2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1c9e2-107">*палтернате* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="1c9e2-107">*pAlternate* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1c9e2-108">Объект [**ианалисисалтернате**](ianalysisalternate.md) , содержащий новый верхний альтернативный вариант.</span><span class="sxs-lookup"><span data-stu-id="1c9e2-108">The [**IAnalysisAlternate**](ianalysisalternate.md) object containing the new top alternate.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1c9e2-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="1c9e2-109">Return value</span></span>

<span data-ttu-id="1c9e2-110">Описание возвращаемых значений см. в разделе [классы и интерфейсы — анализ рукописного ввода](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="1c9e2-110">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="1c9e2-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="1c9e2-111">Remarks</span></span>

<span data-ttu-id="1c9e2-112">Для получения вариантов анализа используйте метод [**иинканализер:: alternate**](iinkanalyzer-getalternates.md), [**Иинканализер:: Жеталтернатесфорконтекстнодес**](iinkanalyzer-getalternatesforcontextnodes.md)или [**метод иинканализер:: жеталтернатесфорстрокес**](iinkanalyzer-getalternatesforstrokes.md).</span><span class="sxs-lookup"><span data-stu-id="1c9e2-112">To get analysis alternates, use [**IInkAnalyzer::GetAlternates Method**](iinkanalyzer-getalternates.md), [**IInkAnalyzer::GetAlternatesForContextNodes Method**](iinkanalyzer-getalternatesforcontextnodes.md), or [**IInkAnalyzer::GetAlternatesForStrokes Method**](iinkanalyzer-getalternatesforstrokes.md).</span></span> <span data-ttu-id="1c9e2-113">Чтобы получить объекты [**иконтекстноде**](icontextnode.md) , связанные с альтернативным анализом, используйте [**метод Ианалисисалтернате:: жеталтернатенодес**](ianalysisalternate-getalternatenodes.md).</span><span class="sxs-lookup"><span data-stu-id="1c9e2-113">To get the [**IContextNode**](icontextnode.md) objects associated with an analysis alternate, use [**IAnalysisAlternate::GetAlternateNodes Method**](ianalysisalternate-getalternatenodes.md).</span></span>

<span data-ttu-id="1c9e2-114">Чтобы изменить тип подтверждения для контекстного узла, используйте [**иконтекстноде:: Confirm**](icontextnode-confirm.md).</span><span class="sxs-lookup"><span data-stu-id="1c9e2-114">To change the confirmation type for a context node, use [**IContextNode::Confirm**](icontextnode-confirm.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="1c9e2-115">Требования</span><span class="sxs-lookup"><span data-stu-id="1c9e2-115">Requirements</span></span>



| <span data-ttu-id="1c9e2-116">Требование</span><span class="sxs-lookup"><span data-stu-id="1c9e2-116">Requirement</span></span> | <span data-ttu-id="1c9e2-117">Значение</span><span class="sxs-lookup"><span data-stu-id="1c9e2-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1c9e2-118">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="1c9e2-118">Minimum supported client</span></span><br/> | <span data-ttu-id="1c9e2-119">Только классические приложения Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="1c9e2-119">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="1c9e2-120">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="1c9e2-120">Minimum supported server</span></span><br/> | <span data-ttu-id="1c9e2-121">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="1c9e2-121">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="1c9e2-122">Header</span><span class="sxs-lookup"><span data-stu-id="1c9e2-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="1c9e2-123"><dt>Иаком. h (также требуется Иаком \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="1c9e2-123"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="1c9e2-124">DLL</span><span class="sxs-lookup"><span data-stu-id="1c9e2-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1c9e2-125"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1c9e2-125"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="1c9e2-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="1c9e2-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1c9e2-127">**иинканализер**</span><span class="sxs-lookup"><span data-stu-id="1c9e2-127">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="1c9e2-128">**ианалисисалтернате**</span><span class="sxs-lookup"><span data-stu-id="1c9e2-128">**IAnalysisAlternate**</span></span>](ianalysisalternate.md)
</dt> <dt>

[<span data-ttu-id="1c9e2-129">**иконтекстноде**</span><span class="sxs-lookup"><span data-stu-id="1c9e2-129">**IContextNode**</span></span>](icontextnode.md)
</dt> <dt>

[<span data-ttu-id="1c9e2-130">**конфирматионтипе**</span><span class="sxs-lookup"><span data-stu-id="1c9e2-130">**ConfirmationType**</span></span>](confirmationtype.md)
</dt> <dt>

[<span data-ttu-id="1c9e2-131">Справочник по анализу рукописного ввода</span><span class="sxs-lookup"><span data-stu-id="1c9e2-131">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




