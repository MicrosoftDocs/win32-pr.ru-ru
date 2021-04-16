---
description: Происходит, когда пользователь рисует новый штрих на любом планшете.
ms.assetid: 2829b65a-6120-402e-91e3-5587d1f456f9
title: Событие InkPicture. Stroke (Мсинкаут. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9b85d2410141c2d6d5f7ae92408b7d6da49a447f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105712818"
---
# <a name="inkpicturestroke-event"></a><span data-ttu-id="5ca93-103">Событие InkPicture. Stroke</span><span class="sxs-lookup"><span data-stu-id="5ca93-103">InkPicture.Stroke event</span></span>

<span data-ttu-id="5ca93-104">Происходит, когда пользователь рисует новый штрих на любом планшете.</span><span class="sxs-lookup"><span data-stu-id="5ca93-104">Occurs when the user draws a new stroke on any tablet.</span></span>

## <a name="syntax"></a><span data-ttu-id="5ca93-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="5ca93-105">Syntax</span></span>


```C++
void Stroke(
  [in]      IInkCursor     *Cursor,
  [in]      IInkStrokeDisp *Stroke,
  [in, out] VARIANT_BOOL   *Cancel
);
```



## <a name="parameters"></a><span data-ttu-id="5ca93-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="5ca93-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5ca93-107">*Курсор* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="5ca93-107">*Cursor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5ca93-108">Объект [**иинккурсор**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) , создавший событие **Stroke** .</span><span class="sxs-lookup"><span data-stu-id="5ca93-108">The [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) object that generated the **Stroke** event.</span></span>

</dd> <dt>

<span data-ttu-id="5ca93-109">*Штриховая линия* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="5ca93-109">*Stroke* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5ca93-110">Собранный объект [**иинкстрокедисп**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) .</span><span class="sxs-lookup"><span data-stu-id="5ca93-110">The collected [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) object.</span></span>

</dd> <dt>

<span data-ttu-id="5ca93-111">*Отмена* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="5ca93-111">*Cancel* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="5ca93-112">**Вариант \_ Значение TRUE** , чтобы отменить коллекцию штрихов; в противном случае — **\_ значение false**.</span><span class="sxs-lookup"><span data-stu-id="5ca93-112">**VARIANT\_TRUE** to cancel the collection of the stroke; otherwise, **VARIANT\_FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5ca93-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="5ca93-113">Return value</span></span>

<span data-ttu-id="5ca93-114">Это событие не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="5ca93-114">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="5ca93-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="5ca93-115">Remarks</span></span>

<span data-ttu-id="5ca93-116">Этот метод события определен в интерфейсах диспетчеризации (DISP) **\_ иинкколлекторевентс**, **\_ иинковерлайевентс** и **\_ иинкпиктуривентс** с идентификатором DISPID \_ ицестроке.</span><span class="sxs-lookup"><span data-stu-id="5ca93-116">This event method is defined in the **\_IInkCollectorEvents**, **\_IInkOverlayEvents**, and **\_IInkPictureEvents** dispatch-only interfaces (dispinterfaces) with an ID of DISPID\_ICEStroke.</span></span>

<span data-ttu-id="5ca93-117">Событие **Stroke** возникает в режиме выбора или стирания, а не только при вставке рукописного ввода.</span><span class="sxs-lookup"><span data-stu-id="5ca93-117">The **Stroke** event occurs when in select or erase mode, not just when inserting ink.</span></span> <span data-ttu-id="5ca93-118">Для этого необходимо наблюдать за режимом редактирования (который вы несете за параметром) и знать о режиме, прежде чем интерпретировать событие.</span><span class="sxs-lookup"><span data-stu-id="5ca93-118">This requires that you monitor the editing mode (which you are responsible for setting) and are aware of the mode before interpreting the event.</span></span> <span data-ttu-id="5ca93-119">Преимуществом этого требования является большая свобода для внедрения инноваций на платформе за счет большей осведомленности о событиях платформы.</span><span class="sxs-lookup"><span data-stu-id="5ca93-119">The advantage of this requirement is greater freedom to innovate on the platform through greater awareness of platform events.</span></span>

> [!Note]  
> <span data-ttu-id="5ca93-120">Событие **Stroke** возникает, когда пользователь завершает рисование штриха, а не при добавлении штриха в коллекцию [инкстрокес](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="5ca93-120">The **Stroke** event occurs when the user finishes drawing a stroke, not when a stroke is added to the [InkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) collection.</span></span> <span data-ttu-id="5ca93-121">Когда пользователь впервые начинает рисовать штрих, он сразу же добавляется в коллекцию Инкстрокес; Однако событие **Stroke** не происходит до завершения штриха.</span><span class="sxs-lookup"><span data-stu-id="5ca93-121">When the user first starts to draw a stroke, it is added immediately to the InkStrokes collection; however, the **Stroke** event does not occur until the stroke is complete.</span></span> <span data-ttu-id="5ca93-122">Таким образом, штрихи могут существовать в коллекции Инкстрокес, которая не видна обработчику событий **Stroke** .</span><span class="sxs-lookup"><span data-stu-id="5ca93-122">Therefore, strokes can exist in the InkStrokes collection that the **Stroke** event handler has not seen.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="5ca93-123">Требования</span><span class="sxs-lookup"><span data-stu-id="5ca93-123">Requirements</span></span>



| <span data-ttu-id="5ca93-124">Требование</span><span class="sxs-lookup"><span data-stu-id="5ca93-124">Requirement</span></span> | <span data-ttu-id="5ca93-125">Значение</span><span class="sxs-lookup"><span data-stu-id="5ca93-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5ca93-126">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="5ca93-126">Minimum supported client</span></span><br/> | <span data-ttu-id="5ca93-127">Только классические приложения Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="5ca93-127">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="5ca93-128">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="5ca93-128">Minimum supported server</span></span><br/> | <span data-ttu-id="5ca93-129">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="5ca93-129">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="5ca93-130">Header</span><span class="sxs-lookup"><span data-stu-id="5ca93-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="5ca93-131"><dt>Мсинкаут. h (также требуется Мсинкаут \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="5ca93-131"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="5ca93-132">Библиотека</span><span class="sxs-lookup"><span data-stu-id="5ca93-132">Library</span></span><br/>                  | <dl> <span data-ttu-id="5ca93-133"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5ca93-133"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="5ca93-134">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="5ca93-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5ca93-135">InkPicture</span><span class="sxs-lookup"><span data-stu-id="5ca93-135">InkPicture</span></span>](inkpicture-control-reference.md)
</dt> <dt>

<span data-ttu-id="5ca93-136">[**\[Элемент управления InkPicture события строкесаддед\]**](inkpicture-strokesadded.md)</span><span class="sxs-lookup"><span data-stu-id="5ca93-136">[**StrokesAdded Event \[InkPicture Control\]**](inkpicture-strokesadded.md)</span></span>
</dt> <dt>

<span data-ttu-id="5ca93-137">[**\[Элемент управления InkPicture события строкесделетед\]**](inkpicture-strokesdeleted.md)</span><span class="sxs-lookup"><span data-stu-id="5ca93-137">[**StrokesDeleted Event \[InkPicture Control\]**](inkpicture-strokesdeleted.md)</span></span>
</dt> <dt>

[<span data-ttu-id="5ca93-138">**Интерфейс Иинккурсор**</span><span class="sxs-lookup"><span data-stu-id="5ca93-138">**IInkCursor Interface**</span></span>](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor)
</dt> <dt>

[<span data-ttu-id="5ca93-139">**Интерфейс Иинкстрокедисп**</span><span class="sxs-lookup"><span data-stu-id="5ca93-139">**IInkStrokeDisp Interface**</span></span>](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp)
</dt> </dl>

 

