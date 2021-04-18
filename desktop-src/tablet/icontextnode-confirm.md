---
description: Изменяет тип подтверждения, который управляет тем, что объект Иинканализер может измениться о Иконтекстноде.
ms.assetid: a506f27e-3909-453e-a2f3-10d4c04d78a4
title: 'Метод Иконтекстноде:: Confirm (Иаком. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNode.Confirm
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 3703bb735c0707c412b7c1e41c43819904d83ce8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105650549"
---
# <a name="icontextnodeconfirm-method"></a><span data-ttu-id="823bf-103">Метод Иконтекстноде:: Confirm</span><span class="sxs-lookup"><span data-stu-id="823bf-103">IContextNode::Confirm method</span></span>

<span data-ttu-id="823bf-104">Изменяет тип подтверждения, который управляет тем, что объект [**иинканализер**](iinkanalyzer.md) может измениться о [**иконтекстноде**](icontextnode.md).</span><span class="sxs-lookup"><span data-stu-id="823bf-104">Modifies the confirmation type, which controls what the [**IInkAnalyzer**](iinkanalyzer.md) object can change about the [**IContextNode**](icontextnode.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="823bf-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="823bf-105">Syntax</span></span>


```C++
HRESULT Confirm(
  [in] ConfirmationType confirmedType
);
```



## <a name="parameters"></a><span data-ttu-id="823bf-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="823bf-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="823bf-107">*конфирмедтипе* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="823bf-107">*confirmedType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="823bf-108">[**Конфирматионтипе**](confirmationtype.md) , применяемый к узлу.</span><span class="sxs-lookup"><span data-stu-id="823bf-108">The [**ConfirmationType**](confirmationtype.md) that is applied to the node.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="823bf-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="823bf-109">Return value</span></span>

<span data-ttu-id="823bf-110">Описание возвращаемых значений см. в разделе [классы и интерфейсы — анализ рукописного ввода](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="823bf-110">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="823bf-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="823bf-111">Remarks</span></span>

<span data-ttu-id="823bf-112">Используйте этот метод, чтобы разрешить конечному пользователю убедиться, что [**иинканализер**](iinkanalyzer.md) правильно анализировал штрихи.</span><span class="sxs-lookup"><span data-stu-id="823bf-112">Use this method to enable the end user to confirm that the [**IInkAnalyzer**](iinkanalyzer.md) has correctly analyzed the strokes.</span></span> <span data-ttu-id="823bf-113">После вызова **иконтекстноде:: Confirm** **иинканализер** не изменит объекты [**иконтекстноде**](icontextnode.md) для этих штрихов во время последующего анализа.</span><span class="sxs-lookup"><span data-stu-id="823bf-113">After **IContextNode::Confirm** is called, the **IInkAnalyzer** will not change the [**IContextNode**](icontextnode.md) objects for those strokes during later analysis.</span></span>

<span data-ttu-id="823bf-114">Используйте **иконтекстноде:: Confirm** , когда пользователь подтвердил результаты анализа и не хочет, чтобы [**иинканализер**](iinkanalyzer.md) изменил [**иконтекстноде**](icontextnode.md) во время последующего анализа.</span><span class="sxs-lookup"><span data-stu-id="823bf-114">Use **IContextNode::Confirm** when the user has confirmed analysis results and does not want the [**IInkAnalyzer**](iinkanalyzer.md) to change an [**IContextNode**](icontextnode.md) during later analysis.</span></span> <span data-ttu-id="823bf-115">Например, если пользователь записывает слово в, а затем приложение вызывает [**метод иинканализер:: Analyze**](iinkanalyzer-analyze.md), анализатор рукописного ввода создает узел инкворд со значением "to".</span><span class="sxs-lookup"><span data-stu-id="823bf-115">For example, if the user writes the word "to" and then the application calls [**IInkAnalyzer::Analyze Method**](iinkanalyzer-analyze.md), the ink analyzer generates an InkWord node with the value of "to".</span></span> <span data-ttu-id="823bf-116">Если пользователь добавляет "Me" после "to" как одно слово, и приложение вызывает **метод иинканализер:: Analyze** еще раз, анализатор рукописного ввода может удалить предыдущий узел инкворд и создать новый узел инкворд со значением "-томе".</span><span class="sxs-lookup"><span data-stu-id="823bf-116">If the user then adds "me" after "to" as one word and the application calls **IInkAnalyzer::Analyze Method** again, the ink analyzer may remove the previous InkWord node and create a new InkWord node with the value "tome".</span></span> <span data-ttu-id="823bf-117">Однако если после первого вызова **метода иинканализер:: Analyze** приложение вызывает **Иконтекстноде:: Confirm** на узле инкворд для "to" с [**конфирматионтипе**](confirmationtype.md) значением **нодетипеандпропертиес**, прежде чем пользователь добавит "Me", то при вызове приложением **метода иинканализер:: Analyze** анализатор рукописного ввода не удаляет и не изменяет узел "to".</span><span class="sxs-lookup"><span data-stu-id="823bf-117">However, if after the first call to **IInkAnalyzer::Analyze Method**, the application calls **IContextNode::Confirm** on the InkWord node for "to" with the [**ConfirmationType**](confirmationtype.md) value **NodeTypeAndProperties**, before the user adds the "me", then when the application calls **IInkAnalyzer::Analyze Method**, the ink analyzer does not remove or change the "to" node.</span></span> <span data-ttu-id="823bf-118">Вместо этого анализатор рукописного ввода может распознать два узла Инкворд для "to" и "Me".</span><span class="sxs-lookup"><span data-stu-id="823bf-118">Instead, the ink analyzer may recognize two InkWord nodes for "to" and "me".</span></span>

<span data-ttu-id="823bf-119">[**Иконтекстноде**](icontextnode.md) может только подтверждать объекты типа Инкворд и инкдравинг (см. раздел [типы узлов контекста](context-node-types.md)).</span><span class="sxs-lookup"><span data-stu-id="823bf-119">[**IContextNode**](icontextnode.md) can only confirm objects of type InkWord and InkDrawing (see [Context Node Types](context-node-types.md)).</span></span> <span data-ttu-id="823bf-120">**Иконтекстноде:: Confirm** возвращает значение **E \_ INVALIDARG** , если узел не является конечным узлом.</span><span class="sxs-lookup"><span data-stu-id="823bf-120">**IContextNode::Confirm** returns **E\_INVALIDARG** when the node is not a leaf node.</span></span>

<span data-ttu-id="823bf-121">Метод [**иинканализер:: ремовестроке**](iinkanalyzer-removestroke.md) и [**метод Иинканализер:: ремовестрокес**](iinkanalyzer-removestrokes.md) отменяют подтверждение любого узла, с которого они удаляют данные Stroke.</span><span class="sxs-lookup"><span data-stu-id="823bf-121">[**IInkAnalyzer::RemoveStroke Method**](iinkanalyzer-removestroke.md) and [**IInkAnalyzer::RemoveStrokes Method**](iinkanalyzer-removestrokes.md) unconfirm any node from which they remove stroke data.</span></span>

<span data-ttu-id="823bf-122">[**Иконтекстноде:: сетстрокес**](icontextnode-setstrokes.md), [**Иинканализер:: сетстрокестипе**](iinkanalyzer-setstrokestype.md)и [**иинканализер:: сетстрокетипе**](iinkanalyzer-setstroketype.md) возвращают **Core \_ E \_ INVALIDOPERATION** , если объект [**иконтекстноде**](icontextnode.md) уже подтвержден.</span><span class="sxs-lookup"><span data-stu-id="823bf-122">[**IContextNode::SetStrokes**](icontextnode-setstrokes.md), [**IInkAnalyzer::SetStrokesType**](iinkanalyzer-setstrokestype.md), and [**IInkAnalyzer::SetStrokeType**](iinkanalyzer-setstroketype.md) return **CORE\_E\_INVALIDOPERATION** if the [**IContextNode**](icontextnode.md) object is already confirmed.</span></span>

<span data-ttu-id="823bf-123">[**Иконтекстноде:: репарентстрокебидтоноде**](icontextnode-reparentstrokebyidtonode.md) возвращает ошибку, если подтвержден узел источника или назначения.</span><span class="sxs-lookup"><span data-stu-id="823bf-123">[**IContextNode::ReparentStrokeByIdToNode**](icontextnode-reparentstrokebyidtonode.md) returns an error if either the source or destination node is confirmed.</span></span>

## <a name="requirements"></a><span data-ttu-id="823bf-124">Требования</span><span class="sxs-lookup"><span data-stu-id="823bf-124">Requirements</span></span>



| <span data-ttu-id="823bf-125">Требование</span><span class="sxs-lookup"><span data-stu-id="823bf-125">Requirement</span></span> | <span data-ttu-id="823bf-126">Значение</span><span class="sxs-lookup"><span data-stu-id="823bf-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="823bf-127">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="823bf-127">Minimum supported client</span></span><br/> | <span data-ttu-id="823bf-128">Только классические приложения Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="823bf-128">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="823bf-129">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="823bf-129">Minimum supported server</span></span><br/> | <span data-ttu-id="823bf-130">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="823bf-130">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="823bf-131">Header</span><span class="sxs-lookup"><span data-stu-id="823bf-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="823bf-132"><dt>Иаком. h (также требуется Иаком \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="823bf-132"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="823bf-133">DLL</span><span class="sxs-lookup"><span data-stu-id="823bf-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="823bf-134"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="823bf-134"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="823bf-135">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="823bf-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="823bf-136">**иконтекстноде**</span><span class="sxs-lookup"><span data-stu-id="823bf-136">**IContextNode**</span></span>](icontextnode.md)
</dt> <dt>

[<span data-ttu-id="823bf-137">**Иконтекстноде:: Confirm**</span><span class="sxs-lookup"><span data-stu-id="823bf-137">**IContextNode::IsConfirmed**</span></span>](icontextnode-isconfirmed.md)
</dt> <dt>

[<span data-ttu-id="823bf-138">Справочник по анализу рукописного ввода</span><span class="sxs-lookup"><span data-stu-id="823bf-138">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




