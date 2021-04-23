---
description: Удаляет указанные штрихи из Иинканализер.
ms.assetid: ea7c8a9f-a427-4781-b5ba-97ffd983dbe5
title: 'Метод Иинканализер:: Ремовестрокес (Иаком. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.RemoveStrokes
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 00f065e01f9a4ff1459988d76fc9393ba24aa894
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104145451"
---
# <a name="iinkanalyzerremovestrokes-method"></a><span data-ttu-id="e4b28-103">Метод Иинканализер:: Ремовестрокес</span><span class="sxs-lookup"><span data-stu-id="e4b28-103">IInkAnalyzer::RemoveStrokes method</span></span>

<span data-ttu-id="e4b28-104">Удаляет указанные штрихи из [**иинканализер**](iinkanalyzer.md).</span><span class="sxs-lookup"><span data-stu-id="e4b28-104">Removes the specified strokes from the [**IInkAnalyzer**](iinkanalyzer.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="e4b28-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e4b28-105">Syntax</span></span>


```C++
HRESULT RemoveStrokes(
  [in] ULONG ulStrokeIdCount,
  [in] LONG  *plStrokes
);
```



## <a name="parameters"></a><span data-ttu-id="e4b28-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="e4b28-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e4b28-107">*улстрокеидкаунт* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="e4b28-107">*ulStrokeIdCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e4b28-108">Число идентификаторов Stroke в *плстрокес*.</span><span class="sxs-lookup"><span data-stu-id="e4b28-108">The number of stroke identifiers in *plStrokes*.</span></span>

</dd> <dt>

<span data-ttu-id="e4b28-109">*плстрокес* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="e4b28-109">*plStrokes* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e4b28-110">Идентификаторы для удаляемых штрихов.</span><span class="sxs-lookup"><span data-stu-id="e4b28-110">The identifiers for the strokes to remove.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e4b28-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="e4b28-111">Return value</span></span>

<span data-ttu-id="e4b28-112">Описание возвращаемых значений см. в разделе [классы и интерфейсы — анализ рукописного ввода](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="e4b28-112">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="e4b28-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="e4b28-113">Remarks</span></span>

<span data-ttu-id="e4b28-114">Этот метод удаляет данные пакета для и ссылается на указанные штрихи из [**иинканализер**](iinkanalyzer.md).</span><span class="sxs-lookup"><span data-stu-id="e4b28-114">This method removes the packet data for and references to the specified strokes from the [**IInkAnalyzer**](iinkanalyzer.md).</span></span>

<span data-ttu-id="e4b28-115">Этот метод удаляет штрихи из конечного узла контекста, который ссылается на штрихи.</span><span class="sxs-lookup"><span data-stu-id="e4b28-115">This method removes the strokes from the leaf context node that references the strokes.</span></span> <span data-ttu-id="e4b28-116">Если любые [**иконтекстноде**](icontextnode.md) больше не ссылаются на штрихи, этот метод удаляет **иконтекстноде** и все объекты предка **иконтекстноде** , которые больше не имеют дочерних узлов.</span><span class="sxs-lookup"><span data-stu-id="e4b28-116">If any [**IContextNode**](icontextnode.md) no longer references any strokes, this method deletes the **IContextNode** and any ancestor **IContextNode** objects that no longer have any child nodes.</span></span>

<span data-ttu-id="e4b28-117">После того как этот метод удаляет штрихи из [**иконтекстноде**](icontextnode.md), он обновляет "грязную" область объекта [**иинканализер**](iinkanalyzer.md) (см. [**метод иинканализер:: жетдиртирегион**](iinkanalyzer-getdirtyregion.md)) для включения ограничивающего прямоугольника удаленных штрихов.</span><span class="sxs-lookup"><span data-stu-id="e4b28-117">After this method removes the strokes from the [**IContextNode**](icontextnode.md), it updates the [**IInkAnalyzer**](iinkanalyzer.md) object's dirty region (see [**IInkAnalyzer::GetDirtyRegion Method**](iinkanalyzer-getdirtyregion.md)) to include the bounding box of the removed strokes.</span></span>

<span data-ttu-id="e4b28-118">Если штрих, определенный в *плстрокес* , не связан с [**иинканализер**](iinkanalyzer.md), этот метод игнорирует идентификатор.</span><span class="sxs-lookup"><span data-stu-id="e4b28-118">If a stroke identified in *plStrokes* is not associated with the [**IInkAnalyzer**](iinkanalyzer.md), this method ignores the identifier.</span></span>

<span data-ttu-id="e4b28-119">Если ни один из штрихов, указанных в *плстрокес* , не связан с анализатором рукописного ввода, этот метод возвращает значение без обновления [**иинканализер**](iinkanalyzer.md).</span><span class="sxs-lookup"><span data-stu-id="e4b28-119">If none of the strokes identified in *plStrokes* are associated with the ink analyzer, this method returns without updating the [**IInkAnalyzer**](iinkanalyzer.md).</span></span>

<span data-ttu-id="e4b28-120">Этот метод возвращает код ошибки, если *плстрокес* имеет значение null.</span><span class="sxs-lookup"><span data-stu-id="e4b28-120">This method returns and error code when *plStrokes* is null.</span></span>

## <a name="requirements"></a><span data-ttu-id="e4b28-121">Требования</span><span class="sxs-lookup"><span data-stu-id="e4b28-121">Requirements</span></span>



| <span data-ttu-id="e4b28-122">Требование</span><span class="sxs-lookup"><span data-stu-id="e4b28-122">Requirement</span></span> | <span data-ttu-id="e4b28-123">Значение</span><span class="sxs-lookup"><span data-stu-id="e4b28-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e4b28-124">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="e4b28-124">Minimum supported client</span></span><br/> | <span data-ttu-id="e4b28-125">Только классические приложения Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="e4b28-125">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="e4b28-126">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="e4b28-126">Minimum supported server</span></span><br/> | <span data-ttu-id="e4b28-127">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="e4b28-127">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="e4b28-128">Header</span><span class="sxs-lookup"><span data-stu-id="e4b28-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="e4b28-129"><dt>Иаком. h (также требуется Иаком \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="e4b28-129"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="e4b28-130">DLL</span><span class="sxs-lookup"><span data-stu-id="e4b28-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e4b28-131"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e4b28-131"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="e4b28-132">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e4b28-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e4b28-133">**иинканализер**</span><span class="sxs-lookup"><span data-stu-id="e4b28-133">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="e4b28-134">**Метод Иинканализер:: Аддстроке**</span><span class="sxs-lookup"><span data-stu-id="e4b28-134">**IInkAnalyzer::AddStroke Method**</span></span>](iinkanalyzer-addstroke.md)
</dt> <dt>

[<span data-ttu-id="e4b28-135">**Метод Иинканализер:: Аддстрокефорлангуаже**</span><span class="sxs-lookup"><span data-stu-id="e4b28-135">**IInkAnalyzer::AddStrokeForLanguage Method**</span></span>](iinkanalyzer-addstrokeforlanguage.md)
</dt> <dt>

[<span data-ttu-id="e4b28-136">**Метод Иинканализер:: Аддстрокес**</span><span class="sxs-lookup"><span data-stu-id="e4b28-136">**IInkAnalyzer::AddStrokes Method**</span></span>](iinkanalyzer-addstrokes.md)
</dt> <dt>

[<span data-ttu-id="e4b28-137">**Метод Иинканализер:: Аддстрокесфорлангуаже**</span><span class="sxs-lookup"><span data-stu-id="e4b28-137">**IInkAnalyzer::AddStrokesForLanguage Method**</span></span>](iinkanalyzer-addstrokesforlanguage.md)
</dt> <dt>

[<span data-ttu-id="e4b28-138">**Метод Иинканализер:: Ремовестроке**</span><span class="sxs-lookup"><span data-stu-id="e4b28-138">**IInkAnalyzer::RemoveStroke Method**</span></span>](iinkanalyzer-removestroke.md)
</dt> <dt>

[<span data-ttu-id="e4b28-139">**Метод Иинканализер:: Жетдиртирегион**</span><span class="sxs-lookup"><span data-stu-id="e4b28-139">**IInkAnalyzer::GetDirtyRegion Method**</span></span>](iinkanalyzer-getdirtyregion.md)
</dt> <dt>

[<span data-ttu-id="e4b28-140">Справочник по анализу рукописного ввода</span><span class="sxs-lookup"><span data-stu-id="e4b28-140">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




