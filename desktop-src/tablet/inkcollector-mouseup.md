---
description: Происходит при отпускании кнопки мыши, когда указатель мыши находится над объектом InkCollector или InkOverlay.
ms.assetid: 6dcc6c68-89f7-4020-b378-56df9d46974b
title: Событие InkCollector. MouseUp (Мсинкаут. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e5f217cf6f5eeff930c1746d1a5ceac180686942
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104497031"
---
# <a name="inkcollectormouseup-event"></a><span data-ttu-id="55295-103">Событие InkCollector. MouseUp</span><span class="sxs-lookup"><span data-stu-id="55295-103">InkCollector.MouseUp event</span></span>

<span data-ttu-id="55295-104">Происходит при отпускании кнопки мыши, когда указатель мыши находится над объектом [**InkCollector**](inkcollector-class.md) или [**InkOverlay**](inkoverlay-class.md) .</span><span class="sxs-lookup"><span data-stu-id="55295-104">Occurs when the mouse pointer is over the [**InkCollector**](inkcollector-class.md) or [**InkOverlay**](inkoverlay-class.md) object and a mouse button is released.</span></span>

## <a name="syntax"></a><span data-ttu-id="55295-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="55295-105">Syntax</span></span>


```C++
void MouseUp(
  [in]      InkMouseButton           Button,
  [in]      InkShiftKeyModifierFlags Shift,
  [in]      long                     pX,
  [in]      long                     pY,
  [in, out] VARIANT_BOOL             *Cancel
);
```



## <a name="parameters"></a><span data-ttu-id="55295-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="55295-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="55295-107">*Кнопка "* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="55295-107">*Button* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="55295-108">Отжатая кнопка мыши.</span><span class="sxs-lookup"><span data-stu-id="55295-108">The mouse button that was released.</span></span>

</dd> <dt>

<span data-ttu-id="55295-109">*SHIFT* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="55295-109">*Shift* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="55295-110">Состояние клавиши SHIFT.</span><span class="sxs-lookup"><span data-stu-id="55295-110">The state of the SHIFT key.</span></span>

</dd> <dt>

<span data-ttu-id="55295-111">*ПКС* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="55295-111">*pX* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="55295-112">Координата по оси x (в пикселях) щелчка мыши.</span><span class="sxs-lookup"><span data-stu-id="55295-112">The x-coordinate, in pixels, of a mouse click.</span></span>

</dd> <dt>

<span data-ttu-id="55295-113">*Копировать* \[ в окне\]</span><span class="sxs-lookup"><span data-stu-id="55295-113">*pY* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="55295-114">Координата по оси y (в пикселях) щелчка мыши.</span><span class="sxs-lookup"><span data-stu-id="55295-114">The y-coordinate, in pixels, of a mouse click.</span></span>

</dd> <dt>

<span data-ttu-id="55295-115">*Отмена* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="55295-115">*Cancel* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="55295-116">**Вариант \_ Значение TRUE** , чтобы отменить событие для родительского элемента управления; в противном случае — **\_ значение false**.</span><span class="sxs-lookup"><span data-stu-id="55295-116">**VARIANT\_TRUE** to cancel the event for the parent control; otherwise, **VARIANT\_FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="55295-117">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="55295-117">Return value</span></span>

<span data-ttu-id="55295-118">Это событие не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="55295-118">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="55295-119">Комментарии</span><span class="sxs-lookup"><span data-stu-id="55295-119">Remarks</span></span>

<span data-ttu-id="55295-120">Чтобы улучшить производительность рукописного ввода в режиме реального времени, скройте или покажите курсор мыши в обработчиках событий [**MouseDown**](inkcollector-mousedown.md) и **MouseUp** .</span><span class="sxs-lookup"><span data-stu-id="55295-120">To improve real-time ink performance, hide or show the mouse cursor in the [**MouseDown**](inkcollector-mousedown.md) and **MouseUp** event handlers.</span></span>

> [!Note]  
> <span data-ttu-id="55295-121">Свойства *px* и *корректировки* находятся в пикселях, а не в HIMETRIC единицах, связанных с пространством рукописного ввода.</span><span class="sxs-lookup"><span data-stu-id="55295-121">The properties *pX* and *pY* are in pixels, and not the HIMETRIC units that are associated with the ink space.</span></span> <span data-ttu-id="55295-122">Это связано с тем, что это событие заменяет связанное событие мыши приложения, не поддерживающего перо, и такого типа приложения распознает только пикселы.</span><span class="sxs-lookup"><span data-stu-id="55295-122">This is because this event replaces the related mouse event of a pen-unaware application and this type of application understands only pixels.</span></span>

 

> [!Note]  
> <span data-ttu-id="55295-123">Некоторые элементы управления используют определенную связь между событиями [**MouseDown**](inkcollector-mousedown.md), [**MouseMove**](inkcollector-mousemove.md)и **MouseUp** .</span><span class="sxs-lookup"><span data-stu-id="55295-123">Some controls rely on a specific relationship between [**MouseDown**](inkcollector-mousedown.md), [**MouseMove**](inkcollector-mousemove.md), and **MouseUp** events.</span></span> <span data-ttu-id="55295-124">Отмена некоторых из этих событий может привести к непредвиденным результатам.</span><span class="sxs-lookup"><span data-stu-id="55295-124">Canceling some of these events may have unanticipated results.</span></span>

 

<span data-ttu-id="55295-125">Этот метод события определен в \_ \_ \_ интерфейсах диспетчеризации (DISP) иинкколлекторевентс, иинковерлайевентс и иинкпиктуривентс с идентификатором DISPID \_ ипемаусеуп.</span><span class="sxs-lookup"><span data-stu-id="55295-125">This event method is defined in the \_IInkCollectorEvents, \_IInkOverlayEvents, and \_IInkPictureEvents dispatch-only interfaces (dispinterfaces) with an ID of DISPID\_IPEMouseUp.</span></span>

## <a name="requirements"></a><span data-ttu-id="55295-126">Требования</span><span class="sxs-lookup"><span data-stu-id="55295-126">Requirements</span></span>



| <span data-ttu-id="55295-127">Требование</span><span class="sxs-lookup"><span data-stu-id="55295-127">Requirement</span></span> | <span data-ttu-id="55295-128">Значение</span><span class="sxs-lookup"><span data-stu-id="55295-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="55295-129">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="55295-129">Minimum supported client</span></span><br/> | <span data-ttu-id="55295-130">Только классические приложения Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="55295-130">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="55295-131">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="55295-131">Minimum supported server</span></span><br/> | <span data-ttu-id="55295-132">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="55295-132">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="55295-133">Header</span><span class="sxs-lookup"><span data-stu-id="55295-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="55295-134"><dt>Мсинкаут. h (также требуется Мсинкаут \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="55295-134"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="55295-135">Библиотека</span><span class="sxs-lookup"><span data-stu-id="55295-135">Library</span></span><br/>                  | <dl> <span data-ttu-id="55295-136"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="55295-136"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="55295-137">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="55295-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="55295-138">**Класс InkCollector**</span><span class="sxs-lookup"><span data-stu-id="55295-138">**InkCollector Class**</span></span>](inkcollector-class.md)
</dt> <dt>

[<span data-ttu-id="55295-139">**Перечисление Инкмаусебуттон**</span><span class="sxs-lookup"><span data-stu-id="55295-139">**InkMouseButton Enumeration**</span></span>](/windows/desktop/api/msinkaut/ne-msinkaut-inkmousebutton)
</dt> <dt>

[<span data-ttu-id="55295-140">**Перечисление Инкшифткэймодифиерфлагс**</span><span class="sxs-lookup"><span data-stu-id="55295-140">**InkShiftKeyModifierFlags Enumeration**</span></span>](/windows/desktop/api/msinkaut/ne-msinkaut-inkshiftkeymodifierflags)
</dt> </dl>

 

 




