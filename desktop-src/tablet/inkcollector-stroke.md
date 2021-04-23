---
description: Происходит, когда пользователь рисует новый штрих на любом планшете.
ms.assetid: eaa89dfe-6141-4205-845b-634321130e26
title: Событие InkCollector. Stroke (Мсинкаут. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e75ee7f3e8129fdab52e62178fe4b8a322807fc5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105692152"
---
# <a name="inkcollectorstroke-event"></a><span data-ttu-id="ae2ac-103">Событие InkCollector. Stroke</span><span class="sxs-lookup"><span data-stu-id="ae2ac-103">InkCollector.Stroke event</span></span>

<span data-ttu-id="ae2ac-104">Происходит, когда пользователь рисует новый штрих на любом планшете.</span><span class="sxs-lookup"><span data-stu-id="ae2ac-104">Occurs when the user draws a new stroke on any tablet.</span></span>

## <a name="syntax"></a><span data-ttu-id="ae2ac-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ae2ac-105">Syntax</span></span>


```C++
void Stroke(
  [in]      IInkCursor     *Cursor,
  [in]      IInkStrokeDisp *Stroke,
  [in, out] VARIANT_BOOL   *Cancel
);
```



## <a name="parameters"></a><span data-ttu-id="ae2ac-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="ae2ac-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ae2ac-107">*Курсор* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="ae2ac-107">*Cursor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ae2ac-108">Объект [**иинккурсор**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) , создавший событие **Stroke** .</span><span class="sxs-lookup"><span data-stu-id="ae2ac-108">The [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) object that generated the **Stroke** event.</span></span>

</dd> <dt>

<span data-ttu-id="ae2ac-109">*Штриховая линия* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="ae2ac-109">*Stroke* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ae2ac-110">Собранный объект [**иинкстрокедисп**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) .</span><span class="sxs-lookup"><span data-stu-id="ae2ac-110">The collected [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) object.</span></span>

</dd> <dt>

<span data-ttu-id="ae2ac-111">*Отмена* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="ae2ac-111">*Cancel* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="ae2ac-112">**Вариант \_ Значение TRUE** , чтобы отменить событие; в противном случае — **\_ значение false**.</span><span class="sxs-lookup"><span data-stu-id="ae2ac-112">**VARIANT\_TRUE** to cancel the event; otherwise, **VARIANT\_FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ae2ac-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="ae2ac-113">Return value</span></span>

<span data-ttu-id="ae2ac-114">Это событие не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="ae2ac-114">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="ae2ac-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="ae2ac-115">Remarks</span></span>

<span data-ttu-id="ae2ac-116">Этот метод события определен в \_ \_ \_ интерфейсах диспетчеризации (DISP) иинкколлекторевентс, иинковерлайевентс и иинкпиктуривентс с идентификатором DISPID \_ ицестроке.</span><span class="sxs-lookup"><span data-stu-id="ae2ac-116">This event method is defined in the \_IInkCollectorEvents, \_IInkOverlayEvents, and \_IInkPictureEvents dispatch-only interfaces (dispinterfaces) with an ID of DISPID\_ICEStroke.</span></span>

<span data-ttu-id="ae2ac-117">Событие **Stroke** срабатывает в режиме выборки или стирания, а не только при вставке рукописного ввода.</span><span class="sxs-lookup"><span data-stu-id="ae2ac-117">The **Stroke** event is fired when in select or erase mode, not just when inserting ink.</span></span> <span data-ttu-id="ae2ac-118">Для этого необходимо наблюдать за режимом редактирования (который вы несете за параметром) и знать о режиме, прежде чем интерпретировать событие.</span><span class="sxs-lookup"><span data-stu-id="ae2ac-118">This requires that you monitor the editing mode (which you are responsible for setting) and are aware of the mode before interpreting the event.</span></span> <span data-ttu-id="ae2ac-119">Преимуществом этого требования является большая свобода для внедрения инноваций на платформе за счет большей осведомленности о событиях платформы.</span><span class="sxs-lookup"><span data-stu-id="ae2ac-119">The advantage of this requirement is greater freedom to innovate on the platform through greater awareness of platform events.</span></span>

> [!Note]  
> <span data-ttu-id="ae2ac-120">Событие **Stroke** срабатывает, когда пользователь завершает рисование штриха, а не при добавлении штриха в коллекцию [инкстрокес](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="ae2ac-120">The **Stroke** event fires when the user finishes drawing a stroke, not when a stroke is added to the [InkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) collection.</span></span> <span data-ttu-id="ae2ac-121">Когда пользователь впервые начинает рисовать штрих, он сразу же добавляется в коллекцию Инкстрокес; Однако событие **Stroke** не срабатывает до завершения штриха.</span><span class="sxs-lookup"><span data-stu-id="ae2ac-121">When the user first starts to draw a stroke, it is added immediately to the InkStrokes collection; however, the **Stroke** event does not fire until the stroke is complete.</span></span> <span data-ttu-id="ae2ac-122">Таким образом, штрихи могут существовать в коллекции Инкстрокес, которая не видна обработчику событий **Stroke** .</span><span class="sxs-lookup"><span data-stu-id="ae2ac-122">Therefore, strokes can exist in the InkStrokes collection that the **Stroke** event handler has not seen.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="ae2ac-123">Требования</span><span class="sxs-lookup"><span data-stu-id="ae2ac-123">Requirements</span></span>



| <span data-ttu-id="ae2ac-124">Требование</span><span class="sxs-lookup"><span data-stu-id="ae2ac-124">Requirement</span></span> | <span data-ttu-id="ae2ac-125">Значение</span><span class="sxs-lookup"><span data-stu-id="ae2ac-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ae2ac-126">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="ae2ac-126">Minimum supported client</span></span><br/> | <span data-ttu-id="ae2ac-127">Только классические приложения Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="ae2ac-127">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="ae2ac-128">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="ae2ac-128">Minimum supported server</span></span><br/> | <span data-ttu-id="ae2ac-129">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="ae2ac-129">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="ae2ac-130">Header</span><span class="sxs-lookup"><span data-stu-id="ae2ac-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="ae2ac-131"><dt>Мсинкаут. h (также требуется Мсинкаут \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="ae2ac-131"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="ae2ac-132">Библиотека</span><span class="sxs-lookup"><span data-stu-id="ae2ac-132">Library</span></span><br/>                  | <dl> <span data-ttu-id="ae2ac-133"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ae2ac-133"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="ae2ac-134">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ae2ac-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ae2ac-135">**Класс InkCollector**</span><span class="sxs-lookup"><span data-stu-id="ae2ac-135">**InkCollector Class**</span></span>](inkcollector-class.md)
</dt> <dt>

<span data-ttu-id="ae2ac-136">[**\[Коллекция Инкстрокес событий строкесаддед\]**](inkstrokes-strokesadded.md)</span><span class="sxs-lookup"><span data-stu-id="ae2ac-136">[**StrokesAdded Event \[InkStrokes Collection\]**](inkstrokes-strokesadded.md)</span></span>
</dt> <dt>

<span data-ttu-id="ae2ac-137">[**\[Класс InkOverlay события строкесделетед\]**](inkoverlay-strokesdeleted.md)</span><span class="sxs-lookup"><span data-stu-id="ae2ac-137">[**StrokesDeleted Event \[InkOverlay Class\]**](inkoverlay-strokesdeleted.md)</span></span>
</dt> <dt>

[<span data-ttu-id="ae2ac-138">**Интерфейс Иинккурсор**</span><span class="sxs-lookup"><span data-stu-id="ae2ac-138">**IInkCursor Interface**</span></span>](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor)
</dt> <dt>

[<span data-ttu-id="ae2ac-139">**Интерфейс Иинкстрокедисп**</span><span class="sxs-lookup"><span data-stu-id="ae2ac-139">**IInkStrokeDisp Interface**</span></span>](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp)
</dt> </dl>

 

