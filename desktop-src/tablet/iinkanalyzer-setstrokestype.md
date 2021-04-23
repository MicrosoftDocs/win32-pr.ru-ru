---
description: Изменяет тип указанных штрихов.
ms.assetid: 8d954a7d-c987-41cf-9933-b2e6bacc9489
title: 'Метод Иинканализер:: Сетстрокестипе (Иаком. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.SetStrokesType
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: de3f4e56b24226c2f74c6572561082c1d00afc8a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105711107"
---
# <a name="iinkanalyzersetstrokestype-method"></a><span data-ttu-id="8afc7-103">Метод Иинканализер:: Сетстрокестипе</span><span class="sxs-lookup"><span data-stu-id="8afc7-103">IInkAnalyzer::SetStrokesType method</span></span>

<span data-ttu-id="8afc7-104">Изменяет тип указанных штрихов.</span><span class="sxs-lookup"><span data-stu-id="8afc7-104">Changes the type of the specified strokes.</span></span>

## <a name="syntax"></a><span data-ttu-id="8afc7-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="8afc7-105">Syntax</span></span>


```C++
HRESULT SetStrokesType(
  [in] ULONG      strokeIdCount,
  [in] LONG       *plStrokes,
  [in] StrokeType StrokeType
);
```



## <a name="parameters"></a><span data-ttu-id="8afc7-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="8afc7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8afc7-107">*строкеидкаунт* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="8afc7-107">*strokeIdCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8afc7-108">Число идентификаторов Stroke в *плстрокес*.</span><span class="sxs-lookup"><span data-stu-id="8afc7-108">The number of stroke identifiers in *plStrokes*.</span></span>

</dd> <dt>

<span data-ttu-id="8afc7-109">*плстрокес* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="8afc7-109">*plStrokes* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8afc7-110">Массив, содержащий идентификаторы штрихов штрихов, которым назначается *строкетипе*.</span><span class="sxs-lookup"><span data-stu-id="8afc7-110">An array containing the stroke identifiers of the strokes to which to assign *StrokeType*.</span></span>

</dd> <dt>

<span data-ttu-id="8afc7-111">*Строкетипе* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="8afc7-111">*StrokeType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8afc7-112">Значение [**строкетипе**](stroketype.md) , присваиваемое штрихам.</span><span class="sxs-lookup"><span data-stu-id="8afc7-112">The [**StrokeType**](stroketype.md) value to assign to the strokes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8afc7-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="8afc7-113">Return value</span></span>

<span data-ttu-id="8afc7-114">Описание возвращаемых значений см. в разделе [классы и интерфейсы — анализ рукописного ввода](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="8afc7-114">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="8afc7-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="8afc7-115">Remarks</span></span>

<span data-ttu-id="8afc7-116">Если тип штриха — [**строкетипе**](stroketype.md) значение **строкетипе \_ неклассифицировано**, [**иинканализер**](iinkanalyzer.md) классифицирует штрих во время анализа рукописного ввода.</span><span class="sxs-lookup"><span data-stu-id="8afc7-116">If the stroke's type is the [**StrokeType**](stroketype.md) value **StrokeType\_Unclassified**, the [**IInkAnalyzer**](iinkanalyzer.md) classifies the stroke during ink analysis.</span></span> <span data-ttu-id="8afc7-117">В противном случае **иинканализер** использует тип, заданный для штриха.</span><span class="sxs-lookup"><span data-stu-id="8afc7-117">Otherwise, the **IInkAnalyzer** uses the type set on the stroke.</span></span>

<span data-ttu-id="8afc7-118">[**Иинканализер**](iinkanalyzer.md) не задает значение типа Stroke как часть анализа рукописного ввода.</span><span class="sxs-lookup"><span data-stu-id="8afc7-118">The [**IInkAnalyzer**](iinkanalyzer.md) does not set the stroke type value as part of ink analysis.</span></span> <span data-ttu-id="8afc7-119">Чтобы указать или изменить тип обводки, используйте метод [**иинканализер:: сетстрокетипе**](iinkanalyzer-setstroketype.md) или **метод Иинканализер:: сетстрокестипе**.</span><span class="sxs-lookup"><span data-stu-id="8afc7-119">To specify or change the stroke type, use [**IInkAnalyzer::SetStrokeType Method**](iinkanalyzer-setstroketype.md) or **IInkAnalyzer::SetStrokesType Method**.</span></span>

<span data-ttu-id="8afc7-120">Если штрих связан с [**иконтекстноде**](icontextnode.md) , который не является неклассифицированным узлом рукописного ввода (см. [**Иконтекстноде:: GetType**](icontextnode-gettype.md)), этот метод перемещает штрих в неклассифицированный узел рукописного ввода, который содержит штрихи того же языка.</span><span class="sxs-lookup"><span data-stu-id="8afc7-120">If a stroke is associated with an [**IContextNode**](icontextnode.md) that is not an unclassified ink node (see [**IContextNode::GetType**](icontextnode-gettype.md)), this method moves the stroke to an unclassified ink node that contains strokes of the same language.</span></span> <span data-ttu-id="8afc7-121">Если такого узла контекста не существует, этот метод создает новый неклассифицированный узел рукописного ввода и добавляет в него штрих.</span><span class="sxs-lookup"><span data-stu-id="8afc7-121">If no such context node exists, this method creates a new unclassified ink node and adds the stroke to it.</span></span> <span data-ttu-id="8afc7-122">Неклассифицированный узел рукописного ввода — это **иконтекстноде** типа унклассифиединк.</span><span class="sxs-lookup"><span data-stu-id="8afc7-122">An unclassified ink node is an **IContextNode** that is of type UnclassifiedInk.</span></span>

<span data-ttu-id="8afc7-123">Если этот метод перемещает росчерк из [**иконтекстноде**](icontextnode.md) , который не является неклассифицированным узлом рукописного ввода, этот метод также добавляет ограничивающий прямоугольник обводки в «грязную» область анализатора рукописного ввода (см. [**метод Иинканализер:: жетдиртирегион**](iinkanalyzer-getdirtyregion.md)).</span><span class="sxs-lookup"><span data-stu-id="8afc7-123">If this method moves a stroke from an [**IContextNode**](icontextnode.md) that is not an unclassified ink node, this method also adds the stroke's bounding box to the ink analyzer's dirty region (see [**IInkAnalyzer::GetDirtyRegion Method**](iinkanalyzer-getdirtyregion.md)).</span></span>

<span data-ttu-id="8afc7-124">Этот метод не перемещает штрих, если параметр *строкетипе* соответствует текущему типу Stroke.</span><span class="sxs-lookup"><span data-stu-id="8afc7-124">This method does not move a stroke if the *StrokeType* parameter matches the stroke's current type.</span></span>

<span data-ttu-id="8afc7-125">Если штрих, определенный в *строкеидс* , не связан с [**иинканализер**](iinkanalyzer.md), этот метод игнорирует идентификатор.</span><span class="sxs-lookup"><span data-stu-id="8afc7-125">If a stroke identified in *strokeIds* is not associated with the [**IInkAnalyzer**](iinkanalyzer.md), this method ignores the identifier.</span></span>

<span data-ttu-id="8afc7-126">Если ни один из указанных штрихов не определяет штрих, связанный с [**иинканализер**](iinkanalyzer.md), этот метод возвращает значение без обновления **иинканализер**.</span><span class="sxs-lookup"><span data-stu-id="8afc7-126">If none of the specified strokes identify a stroke associated with the [**IInkAnalyzer**](iinkanalyzer.md), this method returns without updating the **IInkAnalyzer**.</span></span>

<span data-ttu-id="8afc7-127">Установка типа Stroke для штрихов, связанных с Контекстноде, имеющим Нодетипеандпропертиес, приведет к вызову InvalidOperationException.</span><span class="sxs-lookup"><span data-stu-id="8afc7-127">Setting the stroke type on strokes that are associated with a ContextNode that has NodeTypeAndProperties confirmed will raise an InvalidOperationException.</span></span>

<span data-ttu-id="8afc7-128">Этот метод возвращает код ошибки, если *плстрокес* имеет **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="8afc7-128">This method returns an error code when *plStrokes* is **NULL**.</span></span>

## <a name="requirements"></a><span data-ttu-id="8afc7-129">Требования</span><span class="sxs-lookup"><span data-stu-id="8afc7-129">Requirements</span></span>



| <span data-ttu-id="8afc7-130">Требование</span><span class="sxs-lookup"><span data-stu-id="8afc7-130">Requirement</span></span> | <span data-ttu-id="8afc7-131">Значение</span><span class="sxs-lookup"><span data-stu-id="8afc7-131">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8afc7-132">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="8afc7-132">Minimum supported client</span></span><br/> | <span data-ttu-id="8afc7-133">Только классические приложения Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="8afc7-133">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="8afc7-134">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="8afc7-134">Minimum supported server</span></span><br/> | <span data-ttu-id="8afc7-135">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="8afc7-135">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="8afc7-136">Header</span><span class="sxs-lookup"><span data-stu-id="8afc7-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="8afc7-137"><dt>Иаком. h (также требуется Иаком \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="8afc7-137"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="8afc7-138">DLL</span><span class="sxs-lookup"><span data-stu-id="8afc7-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8afc7-139"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8afc7-139"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="8afc7-140">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="8afc7-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8afc7-141">**иинканализер**</span><span class="sxs-lookup"><span data-stu-id="8afc7-141">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="8afc7-142">**Метод Иинканализер:: Жетстрокетипе**</span><span class="sxs-lookup"><span data-stu-id="8afc7-142">**IInkAnalyzer::GetStrokeType Method**</span></span>](iinkanalyzer-getstroketype.md)
</dt> <dt>

[<span data-ttu-id="8afc7-143">**Метод Иинканализер:: Сетстрокетипе**</span><span class="sxs-lookup"><span data-stu-id="8afc7-143">**IInkAnalyzer::SetStrokeType Method**</span></span>](iinkanalyzer-setstroketype.md)
</dt> <dt>

[<span data-ttu-id="8afc7-144">Справочник по анализу рукописного ввода</span><span class="sxs-lookup"><span data-stu-id="8afc7-144">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




