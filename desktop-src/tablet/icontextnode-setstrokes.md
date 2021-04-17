---
description: Связывает указанные штрихи с этим Иконтекстноде.
ms.assetid: 5ce8893a-da59-4cec-a349-d5ffc4f43905
title: 'Метод Иконтекстноде:: Сетстрокес (Иаком. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNode.SetStrokes
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: be7fd1645af70e34c747894bc8ab4317b08e2d70
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105711133"
---
# <a name="icontextnodesetstrokes-method"></a><span data-ttu-id="68d2c-103">Метод Иконтекстноде:: Сетстрокес</span><span class="sxs-lookup"><span data-stu-id="68d2c-103">IContextNode::SetStrokes method</span></span>

<span data-ttu-id="68d2c-104">Связывает указанные штрихи с этим [**иконтекстноде**](icontextnode.md).</span><span class="sxs-lookup"><span data-stu-id="68d2c-104">Associates the specified strokes with this [**IContextNode**](icontextnode.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="68d2c-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="68d2c-105">Syntax</span></span>


```C++
HRESULT SetStrokes(
  [in] ULONG ulStrokeIdsCount,
  [in] LONG  *plStrokeIds
);
```



## <a name="parameters"></a><span data-ttu-id="68d2c-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="68d2c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="68d2c-107">*улстрокеидскаунт* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="68d2c-107">*ulStrokeIdsCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="68d2c-108">Число идентификаторов Stroke в *плстрокеидс*.</span><span class="sxs-lookup"><span data-stu-id="68d2c-108">The number of stroke identifiers in *plStrokeIds*.</span></span>

</dd> <dt>

<span data-ttu-id="68d2c-109">*плстрокеидс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="68d2c-109">*plStrokeIds* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="68d2c-110">Идентификаторы штрихов, связываемых с этим [**иконтекстноде**](icontextnode.md).</span><span class="sxs-lookup"><span data-stu-id="68d2c-110">The identifiers of the strokes to associate with this [**IContextNode**](icontextnode.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="68d2c-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="68d2c-111">Return value</span></span>

<span data-ttu-id="68d2c-112">Описание возвращаемых значений см. в разделе [классы и интерфейсы — анализ рукописного ввода](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="68d2c-112">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="68d2c-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="68d2c-113">Remarks</span></span>

<span data-ttu-id="68d2c-114">Этот метод не обновляет «грязную» область анализатора рукописного ввода (см. раздел [**метод иинканализер:: жетдиртирегион**](iinkanalyzer-getdirtyregion.md)).</span><span class="sxs-lookup"><span data-stu-id="68d2c-114">This method does not update the ink analyzer's dirty region (see [**IInkAnalyzer::GetDirtyRegion Method**](iinkanalyzer-getdirtyregion.md)).</span></span>

<span data-ttu-id="68d2c-115">Используйте этот метод, если приложение поддерживает собственную структуру данных, которая синхронизируется с [**иинканализер**](iinkanalyzer.md).</span><span class="sxs-lookup"><span data-stu-id="68d2c-115">Use this method when your application maintains its own data structure, which is synchronized with that of the [**IInkAnalyzer**](iinkanalyzer.md).</span></span> <span data-ttu-id="68d2c-116">Используйте этот метод для назначения данных Stroke определенному контекстному узлу.</span><span class="sxs-lookup"><span data-stu-id="68d2c-116">Use this method to assign stroke data to a specific context node.</span></span> <span data-ttu-id="68d2c-117">Дополнительные сведения о синхронизации данных приложения с помощью **иинканализер** см. в разделе [учетная запись-посредник данных с помощью анализа рукописного ввода](data-proxy-with-ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="68d2c-117">For more information about synchronizing your application data with the **IInkAnalyzer**, see [Data Proxy with Ink Analysis](data-proxy-with-ink-analysis.md).</span></span>

<span data-ttu-id="68d2c-118">Если любой из указанных штрихов уже связан с [**иинканализер**](iinkanalyzer.md), этот метод возвращает **E \_ INVALIDARG**.</span><span class="sxs-lookup"><span data-stu-id="68d2c-118">If any of the specified strokes are already associated with the [**IInkAnalyzer**](iinkanalyzer.md), this method returns **E\_INVALIDARG**.</span></span>

## <a name="requirements"></a><span data-ttu-id="68d2c-119">Требования</span><span class="sxs-lookup"><span data-stu-id="68d2c-119">Requirements</span></span>



| <span data-ttu-id="68d2c-120">Требование</span><span class="sxs-lookup"><span data-stu-id="68d2c-120">Requirement</span></span> | <span data-ttu-id="68d2c-121">Значение</span><span class="sxs-lookup"><span data-stu-id="68d2c-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="68d2c-122">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="68d2c-122">Minimum supported client</span></span><br/> | <span data-ttu-id="68d2c-123">Только классические приложения Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="68d2c-123">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="68d2c-124">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="68d2c-124">Minimum supported server</span></span><br/> | <span data-ttu-id="68d2c-125">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="68d2c-125">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="68d2c-126">Header</span><span class="sxs-lookup"><span data-stu-id="68d2c-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="68d2c-127"><dt>Иаком. h (также требуется Иаком \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="68d2c-127"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="68d2c-128">DLL</span><span class="sxs-lookup"><span data-stu-id="68d2c-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="68d2c-129"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="68d2c-129"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="68d2c-130">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="68d2c-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="68d2c-131">**иконтекстноде**</span><span class="sxs-lookup"><span data-stu-id="68d2c-131">**IContextNode**</span></span>](icontextnode.md)
</dt> <dt>

[<span data-ttu-id="68d2c-132">**Метод Иинканализер:: Аддстроке**</span><span class="sxs-lookup"><span data-stu-id="68d2c-132">**IInkAnalyzer::AddStroke Method**</span></span>](iinkanalyzer-addstroke.md)
</dt> <dt>

[<span data-ttu-id="68d2c-133">**Метод Иинканализер:: Аддстрокефорлангуаже**</span><span class="sxs-lookup"><span data-stu-id="68d2c-133">**IInkAnalyzer::AddStrokeForLanguage Method**</span></span>](iinkanalyzer-addstrokeforlanguage.md)
</dt> <dt>

[<span data-ttu-id="68d2c-134">**Метод Иинканализер:: Аддстрокес**</span><span class="sxs-lookup"><span data-stu-id="68d2c-134">**IInkAnalyzer::AddStrokes Method**</span></span>](iinkanalyzer-addstrokes.md)
</dt> <dt>

[<span data-ttu-id="68d2c-135">**Метод Иинканализер:: Аддстрокесфорлангуаже**</span><span class="sxs-lookup"><span data-stu-id="68d2c-135">**IInkAnalyzer::AddStrokesForLanguage Method**</span></span>](iinkanalyzer-addstrokesforlanguage.md)
</dt> <dt>

[<span data-ttu-id="68d2c-136">**Метод Иинканализер:: Аддстрокестокустомрекогнизер**</span><span class="sxs-lookup"><span data-stu-id="68d2c-136">**IInkAnalyzer::AddStrokesToCustomRecognizer Method**</span></span>](iinkanalyzer-addstrokestocustomrecognizer.md)
</dt> <dt>

[<span data-ttu-id="68d2c-137">**Метод Иинканализер:: Аддстрокетокустомрекогнизер**</span><span class="sxs-lookup"><span data-stu-id="68d2c-137">**IInkAnalyzer::AddStrokeToCustomRecognizer Method**</span></span>](iinkanalyzer-addstroketocustomrecognizer.md)
</dt> <dt>

[<span data-ttu-id="68d2c-138">**Метод Иинканализер:: Ремовестроке**</span><span class="sxs-lookup"><span data-stu-id="68d2c-138">**IInkAnalyzer::RemoveStroke Method**</span></span>](iinkanalyzer-removestroke.md)
</dt> <dt>

[<span data-ttu-id="68d2c-139">**Метод Иинканализер:: Ремовестрокес**</span><span class="sxs-lookup"><span data-stu-id="68d2c-139">**IInkAnalyzer::RemoveStrokes Method**</span></span>](iinkanalyzer-removestrokes.md)
</dt> <dt>

[<span data-ttu-id="68d2c-140">**Иконтекстноде:: Жетстрокеид**</span><span class="sxs-lookup"><span data-stu-id="68d2c-140">**IContextNode::GetStrokeId**</span></span>](icontextnode-getstrokeid.md)
</dt> <dt>

[<span data-ttu-id="68d2c-141">**Иконтекстноде:: Жетстрокеидс**</span><span class="sxs-lookup"><span data-stu-id="68d2c-141">**IContextNode::GetStrokeIds**</span></span>](icontextnode-getstrokeids.md)
</dt> <dt>

[<span data-ttu-id="68d2c-142">Справочник по анализу рукописного ввода</span><span class="sxs-lookup"><span data-stu-id="68d2c-142">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




