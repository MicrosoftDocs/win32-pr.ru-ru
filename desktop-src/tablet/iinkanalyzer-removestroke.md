---
description: Удаляет указанный росчерк из Иинканализер.
ms.assetid: e182ae35-854e-401d-8e26-aee645c05430
title: 'Метод Иинканализер:: Ремовестроке (Иаком. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.RemoveStroke
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 03952e6e14679c53f7b65f21463fc0457f302b8e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104542007"
---
# <a name="iinkanalyzerremovestroke-method"></a><span data-ttu-id="c042d-103">Метод Иинканализер:: Ремовестроке</span><span class="sxs-lookup"><span data-stu-id="c042d-103">IInkAnalyzer::RemoveStroke method</span></span>

<span data-ttu-id="c042d-104">Удаляет указанный росчерк из [**иинканализер**](iinkanalyzer.md).</span><span class="sxs-lookup"><span data-stu-id="c042d-104">Removes the specified stroke from the [**IInkAnalyzer**](iinkanalyzer.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="c042d-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c042d-105">Syntax</span></span>


```C++
HRESULT RemoveStroke(
  [in] LONG *plStrokeId
);
```



## <a name="parameters"></a><span data-ttu-id="c042d-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="c042d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c042d-107">*плстрокеид* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="c042d-107">*plStrokeId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c042d-108">Идентификатор штриха.</span><span class="sxs-lookup"><span data-stu-id="c042d-108">The stroke identifier.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c042d-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="c042d-109">Return value</span></span>

<span data-ttu-id="c042d-110">Описание возвращаемых значений см. в разделе [классы и интерфейсы — анализ рукописного ввода](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="c042d-110">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="c042d-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="c042d-111">Remarks</span></span>

<span data-ttu-id="c042d-112">Этот метод удаляет данные пакета для и ссылается на указанный росчерк из [**иинканализер**](iinkanalyzer.md).</span><span class="sxs-lookup"><span data-stu-id="c042d-112">This method removes the packet data for, and references to, the specified stroke from the [**IInkAnalyzer**](iinkanalyzer.md).</span></span>

<span data-ttu-id="c042d-113">Этот метод удаляет штрих из узла конечного контекста, который ссылается на штрих.</span><span class="sxs-lookup"><span data-stu-id="c042d-113">This method removes the stroke from the leaf context node that references the stroke.</span></span> <span data-ttu-id="c042d-114">Если [**иконтекстноде**](icontextnode.md) больше не ссылается на штрихи, этот метод удаляет **иконтекстноде** и все объекты предка **иконтекстноде** , которые больше не имеют дочерних узлов.</span><span class="sxs-lookup"><span data-stu-id="c042d-114">If the [**IContextNode**](icontextnode.md) no longer references any strokes, this method deletes the **IContextNode** and any ancestor **IContextNode** objects that no longer have any child nodes.</span></span>

<span data-ttu-id="c042d-115">После того как этот метод удаляет штрих из [**иконтекстноде**](icontextnode.md), он обновляет "грязную" область объекта [**иинканализер**](iinkanalyzer.md) (см. [**метод иинканализер:: жетдиртирегион**](iinkanalyzer-getdirtyregion.md)) для включения ограничивающего прямоугольника удаленного росчерка.</span><span class="sxs-lookup"><span data-stu-id="c042d-115">After this method removes the stroke from the [**IContextNode**](icontextnode.md), it updates the [**IInkAnalyzer**](iinkanalyzer.md) object's dirty region (see [**IInkAnalyzer::GetDirtyRegion Method**](iinkanalyzer-getdirtyregion.md)) to include the bounding box of the removed stroke.</span></span>

<span data-ttu-id="c042d-116">Если *плстрокеид* не определяет штрих, связанный с [**иинканализер**](iinkanalyzer.md), этот метод возвращает данные без обновления анализатора рукописного ввода.</span><span class="sxs-lookup"><span data-stu-id="c042d-116">If *plStrokeId* does not identify a stroke associated with the [**IInkAnalyzer**](iinkanalyzer.md), this method returns without updating the ink analyzer.</span></span>

## <a name="requirements"></a><span data-ttu-id="c042d-117">Требования</span><span class="sxs-lookup"><span data-stu-id="c042d-117">Requirements</span></span>



| <span data-ttu-id="c042d-118">Требование</span><span class="sxs-lookup"><span data-stu-id="c042d-118">Requirement</span></span> | <span data-ttu-id="c042d-119">Значение</span><span class="sxs-lookup"><span data-stu-id="c042d-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c042d-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="c042d-120">Minimum supported client</span></span><br/> | <span data-ttu-id="c042d-121">Только классические приложения Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="c042d-121">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="c042d-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="c042d-122">Minimum supported server</span></span><br/> | <span data-ttu-id="c042d-123">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="c042d-123">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="c042d-124">Header</span><span class="sxs-lookup"><span data-stu-id="c042d-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="c042d-125"><dt>Иаком. h (также требуется Иаком \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="c042d-125"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="c042d-126">DLL</span><span class="sxs-lookup"><span data-stu-id="c042d-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c042d-127"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c042d-127"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="c042d-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c042d-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c042d-129">**иинканализер**</span><span class="sxs-lookup"><span data-stu-id="c042d-129">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="c042d-130">**Метод Иинканализер:: Аддстроке**</span><span class="sxs-lookup"><span data-stu-id="c042d-130">**IInkAnalyzer::AddStroke Method**</span></span>](iinkanalyzer-addstroke.md)
</dt> <dt>

[<span data-ttu-id="c042d-131">**Метод Иинканализер:: Аддстрокефорлангуаже**</span><span class="sxs-lookup"><span data-stu-id="c042d-131">**IInkAnalyzer::AddStrokeForLanguage Method**</span></span>](iinkanalyzer-addstrokeforlanguage.md)
</dt> <dt>

[<span data-ttu-id="c042d-132">**Метод Иинканализер:: Аддстрокес**</span><span class="sxs-lookup"><span data-stu-id="c042d-132">**IInkAnalyzer::AddStrokes Method**</span></span>](iinkanalyzer-addstrokes.md)
</dt> <dt>

[<span data-ttu-id="c042d-133">**Метод Иинканализер:: Аддстрокесфорлангуаже**</span><span class="sxs-lookup"><span data-stu-id="c042d-133">**IInkAnalyzer::AddStrokesForLanguage Method**</span></span>](iinkanalyzer-addstrokesforlanguage.md)
</dt> <dt>

[<span data-ttu-id="c042d-134">**Метод Иинканализер:: Ремовестрокес**</span><span class="sxs-lookup"><span data-stu-id="c042d-134">**IInkAnalyzer::RemoveStrokes Method**</span></span>](iinkanalyzer-removestrokes.md)
</dt> <dt>

[<span data-ttu-id="c042d-135">**Метод Иинканализер:: Жетдиртирегион**</span><span class="sxs-lookup"><span data-stu-id="c042d-135">**IInkAnalyzer::GetDirtyRegion Method**</span></span>](iinkanalyzer-getdirtyregion.md)
</dt> <dt>

[<span data-ttu-id="c042d-136">Справочник по анализу рукописного ввода</span><span class="sxs-lookup"><span data-stu-id="c042d-136">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




