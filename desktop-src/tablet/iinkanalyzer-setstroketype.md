---
description: Изменяет тип указанного штриха.
ms.assetid: 1608fed1-cd6c-46c3-a35f-3d262279ec2e
title: 'Метод Иинканализер:: Сетстрокетипе (Иаком. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.SetStrokeType
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 8a5f77cbefb200bad973c0f2cf28fea5d3efe1da
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104145430"
---
# <a name="iinkanalyzersetstroketype-method"></a><span data-ttu-id="9f395-103">Метод Иинканализер:: Сетстрокетипе</span><span class="sxs-lookup"><span data-stu-id="9f395-103">IInkAnalyzer::SetStrokeType method</span></span>

<span data-ttu-id="9f395-104">Изменяет тип указанного штриха.</span><span class="sxs-lookup"><span data-stu-id="9f395-104">Changes the type of the specified stroke.</span></span>

## <a name="syntax"></a><span data-ttu-id="9f395-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="9f395-105">Syntax</span></span>


```C++
HRESULT SetStrokeType(
  [in] LONG       lStrokeId,
  [in] StrokeType StrokeType
);
```



## <a name="parameters"></a><span data-ttu-id="9f395-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="9f395-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9f395-107">*лстрокеид* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="9f395-107">*lStrokeId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9f395-108">Идентификатор штриха, которому присваивается *строкетипе*.</span><span class="sxs-lookup"><span data-stu-id="9f395-108">The stroke identifier of the stroke to which to assign *StrokeType*.</span></span>

</dd> <dt>

<span data-ttu-id="9f395-109">*Строкетипе* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="9f395-109">*StrokeType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9f395-110">Значение [**строкетипе**](stroketype.md) , присваиваемое обводке.</span><span class="sxs-lookup"><span data-stu-id="9f395-110">The [**StrokeType**](stroketype.md) value to assign to the stroke.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9f395-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="9f395-111">Return value</span></span>

<span data-ttu-id="9f395-112">Описание возвращаемых значений см. в разделе [классы и интерфейсы — анализ рукописного ввода](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="9f395-112">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="9f395-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="9f395-113">Remarks</span></span>

<span data-ttu-id="9f395-114">Если тип штриха — [**строкетипе**](stroketype.md) значение **строкетипе \_ неклассифицировано**, [**иинканализер**](iinkanalyzer.md) классифицирует штрих во время анализа рукописного ввода.</span><span class="sxs-lookup"><span data-stu-id="9f395-114">If the stroke's type is the [**StrokeType**](stroketype.md) value **StrokeType\_Unclassified**, the [**IInkAnalyzer**](iinkanalyzer.md) classifies the stroke during ink analysis.</span></span> <span data-ttu-id="9f395-115">В противном случае **иинканализер** использует тип, заданный для штриха.</span><span class="sxs-lookup"><span data-stu-id="9f395-115">Otherwise, the **IInkAnalyzer** uses the type set on the stroke.</span></span>

<span data-ttu-id="9f395-116">[**Иинканализер**](iinkanalyzer.md) не задает значение типа Stroke как часть анализа рукописного ввода.</span><span class="sxs-lookup"><span data-stu-id="9f395-116">The [**IInkAnalyzer**](iinkanalyzer.md) does not set the stroke type value as part of ink analysis.</span></span> <span data-ttu-id="9f395-117">Чтобы указать или изменить тип обводки, используйте метод **иинканализер:: сетстрокетипе** или [**метод Иинканализер:: сетстрокестипе**](iinkanalyzer-setstrokestype.md).</span><span class="sxs-lookup"><span data-stu-id="9f395-117">To specify or change the stroke type, use **IInkAnalyzer::SetStrokeType Method** or [**IInkAnalyzer::SetStrokesType Method**](iinkanalyzer-setstrokestype.md).</span></span>

<span data-ttu-id="9f395-118">Если штрих связан с [**иконтекстноде**](icontextnode.md) , который не является неклассифицированным узлом рукописного ввода (см. [**Иконтекстноде:: GetType**](icontextnode-gettype.md)), этот метод перемещает штрих в неклассифицированный узел рукописного ввода, который содержит штрихи того же языка.</span><span class="sxs-lookup"><span data-stu-id="9f395-118">If a stroke is associated with an [**IContextNode**](icontextnode.md) that is not an unclassified ink node (see [**IContextNode::GetType**](icontextnode-gettype.md)), this method moves the stroke to an unclassified ink node that contains strokes of the same language.</span></span> <span data-ttu-id="9f395-119">Если такого узла контекста не существует, этот метод создает новый неклассифицированный узел рукописного ввода и добавляет в него штрих.</span><span class="sxs-lookup"><span data-stu-id="9f395-119">If no such context node exists, this method creates a new unclassified ink node and adds the stroke to it.</span></span> <span data-ttu-id="9f395-120">Неклассифицированный узел рукописного ввода — это **иконтекстноде** типа унклассифиединк.</span><span class="sxs-lookup"><span data-stu-id="9f395-120">An unclassified ink node is an **IContextNode** that is of type UnclassifiedInk.</span></span>

<span data-ttu-id="9f395-121">Если этот метод перемещает росчерк из [**иконтекстноде**](icontextnode.md) , который не является неклассифицированным узлом рукописного ввода, этот метод также добавляет ограничивающий прямоугольник обводки в «грязную» область анализатора рукописного ввода (см. [**метод Иинканализер:: жетдиртирегион**](iinkanalyzer-getdirtyregion.md)).</span><span class="sxs-lookup"><span data-stu-id="9f395-121">If this method moves a stroke from an [**IContextNode**](icontextnode.md) that is not an unclassified ink node, this method also adds the stroke's bounding box to the ink analyzer's dirty region (see [**IInkAnalyzer::GetDirtyRegion Method**](iinkanalyzer-getdirtyregion.md)).</span></span>

<span data-ttu-id="9f395-122">Этот метод не перемещает штрих, если параметр *строкетипе* соответствует текущему типу Stroke.</span><span class="sxs-lookup"><span data-stu-id="9f395-122">This method does not move a stroke if the *StrokeType* parameter matches the stroke's current type.</span></span>

<span data-ttu-id="9f395-123">Установка типа Stroke для штрихов, связанных с Контекстноде, имеющим Нодетипеандпропертиес, приведет к вызову InvalidOperationException.</span><span class="sxs-lookup"><span data-stu-id="9f395-123">Setting the stroke type on strokes that are associated with a ContextNode that has NodeTypeAndProperties confirmed will raise an InvalidOperationException.</span></span>

<span data-ttu-id="9f395-124">Если указанный росчерк не связан с [**иинканализер**](iinkanalyzer.md), этот метод возвращает значение без обновления **иинканализер**.</span><span class="sxs-lookup"><span data-stu-id="9f395-124">If the specified stroke is not associated with the [**IInkAnalyzer**](iinkanalyzer.md), this method returns without updating the **IInkAnalyzer**.</span></span>

## <a name="requirements"></a><span data-ttu-id="9f395-125">Требования</span><span class="sxs-lookup"><span data-stu-id="9f395-125">Requirements</span></span>



| <span data-ttu-id="9f395-126">Требование</span><span class="sxs-lookup"><span data-stu-id="9f395-126">Requirement</span></span> | <span data-ttu-id="9f395-127">Значение</span><span class="sxs-lookup"><span data-stu-id="9f395-127">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9f395-128">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="9f395-128">Minimum supported client</span></span><br/> | <span data-ttu-id="9f395-129">Только классические приложения Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="9f395-129">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="9f395-130">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="9f395-130">Minimum supported server</span></span><br/> | <span data-ttu-id="9f395-131">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="9f395-131">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="9f395-132">Header</span><span class="sxs-lookup"><span data-stu-id="9f395-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="9f395-133"><dt>Иаком. h (также требуется Иаком \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="9f395-133"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="9f395-134">DLL</span><span class="sxs-lookup"><span data-stu-id="9f395-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9f395-135"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9f395-135"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="9f395-136">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="9f395-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9f395-137">**иинканализер**</span><span class="sxs-lookup"><span data-stu-id="9f395-137">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="9f395-138">**Метод Иинканализер:: Жетстрокетипе**</span><span class="sxs-lookup"><span data-stu-id="9f395-138">**IInkAnalyzer::GetStrokeType Method**</span></span>](iinkanalyzer-getstroketype.md)
</dt> <dt>

[<span data-ttu-id="9f395-139">**Метод Иинканализер:: Сетстрокестипе**</span><span class="sxs-lookup"><span data-stu-id="9f395-139">**IInkAnalyzer::SetStrokesType Method**</span></span>](iinkanalyzer-setstrokestype.md)
</dt> <dt>

[<span data-ttu-id="9f395-140">Справочник по анализу рукописного ввода</span><span class="sxs-lookup"><span data-stu-id="9f395-140">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




