---
description: Происходит, когда пользователь рисует новый штрих на любом планшете.
ms.assetid: 315155ec-0de1-4052-ae7c-51bc3127fbbf
title: Событие InkOverlay. Stroke (Мсинкаут. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b6db3bdbe996830596a8e25cebf6f05b94638894
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103817729"
---
# <a name="inkoverlaystroke-event"></a><span data-ttu-id="76fa0-103">Событие InkOverlay. Stroke</span><span class="sxs-lookup"><span data-stu-id="76fa0-103">InkOverlay.Stroke event</span></span>

<span data-ttu-id="76fa0-104">Происходит, когда пользователь рисует новый штрих на любом планшете.</span><span class="sxs-lookup"><span data-stu-id="76fa0-104">Occurs when the user draws a new stroke on any tablet.</span></span>

## <a name="syntax"></a><span data-ttu-id="76fa0-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="76fa0-105">Syntax</span></span>


```C++
void Stroke(
  [in]      IInkCursor     *Cursor,
  [in]      IInkStrokeDisp *Stroke,
  [in, out] VARIANT_BOOL   *Cancel
);
```



## <a name="parameters"></a><span data-ttu-id="76fa0-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="76fa0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="76fa0-107">*Курсор* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="76fa0-107">*Cursor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="76fa0-108">Объект [**иинккурсор**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) , создавший событие [**Stroke**](inkcollector-stroke.md) .</span><span class="sxs-lookup"><span data-stu-id="76fa0-108">The [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) object that generated the [**Stroke**](inkcollector-stroke.md) event.</span></span>

</dd> <dt>

<span data-ttu-id="76fa0-109">*Штриховая линия* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="76fa0-109">*Stroke* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="76fa0-110">Собранный объект [**иинкстрокедисп**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) .</span><span class="sxs-lookup"><span data-stu-id="76fa0-110">The collected [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) object.</span></span>

</dd> <dt>

<span data-ttu-id="76fa0-111">*Отмена* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="76fa0-111">*Cancel* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="76fa0-112">Указывает, следует ли отменять событие.</span><span class="sxs-lookup"><span data-stu-id="76fa0-112">Specifies whether the event should be canceled.</span></span> <span data-ttu-id="76fa0-113">Если **значение — true**, коллекция штрихов отменяется.</span><span class="sxs-lookup"><span data-stu-id="76fa0-113">If **TRUE**, the collection of the stroke is canceled.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="76fa0-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="76fa0-114">Return value</span></span>

<span data-ttu-id="76fa0-115">Это событие не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="76fa0-115">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="76fa0-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="76fa0-116">Remarks</span></span>

<span data-ttu-id="76fa0-117">Этот метод события определен в \_ \_ \_ интерфейсах диспетчеризации (DISP) иинкколлекторевентс, иинковерлайевентс и иинкпиктуривентс с идентификатором DISPID \_ ицестроке.</span><span class="sxs-lookup"><span data-stu-id="76fa0-117">This event method is defined in the \_IInkCollectorEvents, \_IInkOverlayEvents, and \_IInkPictureEvents dispatch-only interfaces (dispinterfaces) with an ID of DISPID\_ICEStroke.</span></span>

<span data-ttu-id="76fa0-118">Событие [**Stroke**](inkcollector-stroke.md) срабатывает в режиме выборки или стирания, а не только при вставке рукописного ввода.</span><span class="sxs-lookup"><span data-stu-id="76fa0-118">The [**Stroke**](inkcollector-stroke.md) event is fired when in select or erase mode, not just when inserting ink.</span></span> <span data-ttu-id="76fa0-119">Для этого необходимо наблюдать за режимом редактирования (который вы несете за параметром) и знать о режиме, прежде чем интерпретировать событие.</span><span class="sxs-lookup"><span data-stu-id="76fa0-119">This requires that you monitor the editing mode (which you are responsible for setting) and are aware of the mode before interpreting the event.</span></span> <span data-ttu-id="76fa0-120">Преимуществом этого требования является большая свобода для внедрения инноваций на платформе за счет большей осведомленности о событиях платформы.</span><span class="sxs-lookup"><span data-stu-id="76fa0-120">The advantage of this requirement is greater freedom to innovate on the platform through greater awareness of platform events.</span></span>

> [!Note]  
> <span data-ttu-id="76fa0-121">Событие [**Stroke**](inkcollector-stroke.md) срабатывает, когда пользователь завершает рисование штриха, а не при добавлении штриха в коллекцию [инкстрокес](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="76fa0-121">The [**Stroke**](inkcollector-stroke.md) event fires when the user finishes drawing a stroke, not when a stroke is added to the [InkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) collection.</span></span> <span data-ttu-id="76fa0-122">Когда пользователь впервые начинает рисовать штрих, он сразу же добавляется в коллекцию Инкстрокес; Однако событие **Stroke** не срабатывает до завершения штриха.</span><span class="sxs-lookup"><span data-stu-id="76fa0-122">When the user first starts to draw a stroke, it is added immediately to the InkStrokes collection; however, the **Stroke** event does not fire until the stroke is complete.</span></span> <span data-ttu-id="76fa0-123">Таким образом, штрихи могут существовать в коллекции Инкстрокес, которая не видна обработчику событий **Stroke** .</span><span class="sxs-lookup"><span data-stu-id="76fa0-123">Therefore, strokes can exist in the InkStrokes collection that the **Stroke** event handler has not seen.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="76fa0-124">Требования</span><span class="sxs-lookup"><span data-stu-id="76fa0-124">Requirements</span></span>



| <span data-ttu-id="76fa0-125">Требование</span><span class="sxs-lookup"><span data-stu-id="76fa0-125">Requirement</span></span> | <span data-ttu-id="76fa0-126">Значение</span><span class="sxs-lookup"><span data-stu-id="76fa0-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="76fa0-127">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="76fa0-127">Minimum supported client</span></span><br/> | <span data-ttu-id="76fa0-128">Только классические приложения Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="76fa0-128">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="76fa0-129">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="76fa0-129">Minimum supported server</span></span><br/> | <span data-ttu-id="76fa0-130">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="76fa0-130">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="76fa0-131">Header</span><span class="sxs-lookup"><span data-stu-id="76fa0-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="76fa0-132"><dt>Мсинкаут. h (также требуется Мсинкаут \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="76fa0-132"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="76fa0-133">Библиотека</span><span class="sxs-lookup"><span data-stu-id="76fa0-133">Library</span></span><br/>                  | <dl> <span data-ttu-id="76fa0-134"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="76fa0-134"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="76fa0-135">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="76fa0-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="76fa0-136">**Класс InkOverlay**</span><span class="sxs-lookup"><span data-stu-id="76fa0-136">**InkOverlay Class**</span></span>](inkoverlay-class.md)
</dt> <dt>

<span data-ttu-id="76fa0-137">[**\[Коллекция Инкстрокес событий строкесаддед\]**](inkstrokes-strokesadded.md)</span><span class="sxs-lookup"><span data-stu-id="76fa0-137">[**StrokesAdded Event \[InkStrokes Collection\]**](inkstrokes-strokesadded.md)</span></span>
</dt> <dt>

<span data-ttu-id="76fa0-138">[**\[Класс InkOverlay события строкесделетед\]**](inkoverlay-strokesdeleted.md)</span><span class="sxs-lookup"><span data-stu-id="76fa0-138">[**StrokesDeleted Event \[InkOverlay Class\]**](inkoverlay-strokesdeleted.md)</span></span>
</dt> <dt>

[<span data-ttu-id="76fa0-139">**Интерфейс Иинккурсор**</span><span class="sxs-lookup"><span data-stu-id="76fa0-139">**IInkCursor Interface**</span></span>](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor)
</dt> <dt>

[<span data-ttu-id="76fa0-140">**Интерфейс Иинкстрокедисп**</span><span class="sxs-lookup"><span data-stu-id="76fa0-140">**IInkStrokeDisp Interface**</span></span>](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp)
</dt> </dl>

 

