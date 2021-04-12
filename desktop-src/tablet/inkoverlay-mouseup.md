---
description: Происходит при отпускании кнопки мыши, когда указатель мыши находится над объектом InkCollector или InkOverlay.
ms.assetid: 049e1560-d4b2-4d34-9d54-2b45217001b2
title: Событие InkOverlay. MouseUp (Мсинкаут. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1f16fd3dc5006f43e09e093cb2c474a8578f56c6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104266158"
---
# <a name="inkoverlaymouseup-event"></a><span data-ttu-id="ad9cc-103">Событие InkOverlay. MouseUp</span><span class="sxs-lookup"><span data-stu-id="ad9cc-103">InkOverlay.MouseUp event</span></span>

<span data-ttu-id="ad9cc-104">Происходит при отпускании кнопки мыши, когда указатель мыши находится над объектом [**InkCollector**](inkcollector-class.md) или [**InkOverlay**](inkoverlay-class.md) .</span><span class="sxs-lookup"><span data-stu-id="ad9cc-104">Occurs when the mouse pointer is over the [**InkCollector**](inkcollector-class.md) or [**InkOverlay**](inkoverlay-class.md) object and a mouse button is released.</span></span>

## <a name="syntax"></a><span data-ttu-id="ad9cc-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ad9cc-105">Syntax</span></span>


```C++
void MouseUp(
  [in]      InkMouseButton           Button,
  [in]      InkShiftKeyModifierFlags Shift,
  [in]      long                     pX,
  [in]      long                     pY,
  [in, out] VARIANT_BOOL             *Cancel
);
```



## <a name="parameters"></a><span data-ttu-id="ad9cc-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="ad9cc-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ad9cc-107">*Кнопка "* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="ad9cc-107">*Button* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ad9cc-108">Отжатая кнопка мыши.</span><span class="sxs-lookup"><span data-stu-id="ad9cc-108">The mouse button that was released.</span></span>

</dd> <dt>

<span data-ttu-id="ad9cc-109">*SHIFT* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="ad9cc-109">*Shift* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ad9cc-110">Состояние клавиши SHIFT.</span><span class="sxs-lookup"><span data-stu-id="ad9cc-110">The state of the SHIFT key.</span></span>

</dd> <dt>

<span data-ttu-id="ad9cc-111">*ПКС* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="ad9cc-111">*pX* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ad9cc-112">Координата по оси x (в пикселях) щелчка мыши.</span><span class="sxs-lookup"><span data-stu-id="ad9cc-112">The x-coordinate, in pixels, of a mouse click.</span></span>

</dd> <dt>

<span data-ttu-id="ad9cc-113">*Копировать* \[ в окне\]</span><span class="sxs-lookup"><span data-stu-id="ad9cc-113">*pY* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ad9cc-114">Координата по оси y (в пикселях) щелчка мыши.</span><span class="sxs-lookup"><span data-stu-id="ad9cc-114">The y-coordinate, in pixels, of a mouse click.</span></span>

</dd> <dt>

<span data-ttu-id="ad9cc-115">*Отмена* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="ad9cc-115">*Cancel* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="ad9cc-116">Следует ли отменять событие для родительского элемента управления.</span><span class="sxs-lookup"><span data-stu-id="ad9cc-116">Whether the event should be canceled for the parent control.</span></span> <span data-ttu-id="ad9cc-117">Значение по умолчанию — **false**, которое указывает, что событие не должно быть отменено.</span><span class="sxs-lookup"><span data-stu-id="ad9cc-117">The default value is **FALSE**, which specifies that the event should not be canceled.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ad9cc-118">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="ad9cc-118">Return value</span></span>

<span data-ttu-id="ad9cc-119">Это событие не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="ad9cc-119">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="ad9cc-120">Комментарии</span><span class="sxs-lookup"><span data-stu-id="ad9cc-120">Remarks</span></span>

<span data-ttu-id="ad9cc-121">Чтобы улучшить производительность рукописного ввода в режиме реального времени, скройте или покажите курсор мыши в обработчиках событий [**MouseDown**](inkcollector-mousedown.md) и [**MouseUp**](inkcollector-mouseup.md) .</span><span class="sxs-lookup"><span data-stu-id="ad9cc-121">To improve real-time ink performance, hide or show the mouse cursor in the [**MouseDown**](inkcollector-mousedown.md) and [**MouseUp**](inkcollector-mouseup.md) event handlers.</span></span>

> [!Note]  
> <span data-ttu-id="ad9cc-122">Свойства *px* и *корректировки* находятся в пикселях, а не в HIMETRIC единицах, связанных с пространством рукописного ввода.</span><span class="sxs-lookup"><span data-stu-id="ad9cc-122">The properties *pX* and *pY* are in pixels, and not the HIMETRIC units that are associated with the ink space.</span></span> <span data-ttu-id="ad9cc-123">Это связано с тем, что это событие заменяет связанное событие мыши приложения, не поддерживающего перо, и такого типа приложения распознает только пикселы.</span><span class="sxs-lookup"><span data-stu-id="ad9cc-123">This is because this event replaces the related mouse event of a pen-unaware application and this type of application understands only pixels.</span></span>

 

> [!Note]  
> <span data-ttu-id="ad9cc-124">Некоторые элементы управления используют определенную связь между событиями [**MouseDown**](inkcollector-mousedown.md), [**MouseMove**](inkcollector-mousemove.md)и [**MouseUp**](inkcollector-mouseup.md) .</span><span class="sxs-lookup"><span data-stu-id="ad9cc-124">Some controls rely on a specific relationship between [**MouseDown**](inkcollector-mousedown.md), [**MouseMove**](inkcollector-mousemove.md), and [**MouseUp**](inkcollector-mouseup.md) events.</span></span> <span data-ttu-id="ad9cc-125">Отмена некоторых из этих событий может привести к непредвиденным результатам.</span><span class="sxs-lookup"><span data-stu-id="ad9cc-125">Canceling some of these events may have unanticipated results.</span></span>

 

<span data-ttu-id="ad9cc-126">Этот метод события определен в \_ \_ \_ интерфейсах диспетчеризации (DISP) иинкколлекторевентс, иинковерлайевентс и иинкпиктуривентс с идентификатором DISPID \_ ипемаусеуп.</span><span class="sxs-lookup"><span data-stu-id="ad9cc-126">This event method is defined in the \_IInkCollectorEvents, \_IInkOverlayEvents, and \_IInkPictureEvents dispatch-only interfaces (dispinterfaces) with an ID of DISPID\_IPEMouseUp.</span></span>

## <a name="requirements"></a><span data-ttu-id="ad9cc-127">Требования</span><span class="sxs-lookup"><span data-stu-id="ad9cc-127">Requirements</span></span>



| <span data-ttu-id="ad9cc-128">Требование</span><span class="sxs-lookup"><span data-stu-id="ad9cc-128">Requirement</span></span> | <span data-ttu-id="ad9cc-129">Значение</span><span class="sxs-lookup"><span data-stu-id="ad9cc-129">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ad9cc-130">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="ad9cc-130">Minimum supported client</span></span><br/> | <span data-ttu-id="ad9cc-131">Только классические приложения Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="ad9cc-131">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="ad9cc-132">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="ad9cc-132">Minimum supported server</span></span><br/> | <span data-ttu-id="ad9cc-133">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="ad9cc-133">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="ad9cc-134">Header</span><span class="sxs-lookup"><span data-stu-id="ad9cc-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="ad9cc-135"><dt>Мсинкаут. h (также требуется Мсинкаут \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="ad9cc-135"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="ad9cc-136">Библиотека</span><span class="sxs-lookup"><span data-stu-id="ad9cc-136">Library</span></span><br/>                  | <dl> <span data-ttu-id="ad9cc-137"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ad9cc-137"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="ad9cc-138">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ad9cc-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ad9cc-139">**Класс InkOverlay**</span><span class="sxs-lookup"><span data-stu-id="ad9cc-139">**InkOverlay Class**</span></span>](inkoverlay-class.md)
</dt> <dt>

[<span data-ttu-id="ad9cc-140">**Перечисление Инкмаусебуттон**</span><span class="sxs-lookup"><span data-stu-id="ad9cc-140">**InkMouseButton Enumeration**</span></span>](/windows/desktop/api/msinkaut/ne-msinkaut-inkmousebutton)
</dt> <dt>

[<span data-ttu-id="ad9cc-141">**Перечисление Инкшифткэймодифиерфлагс**</span><span class="sxs-lookup"><span data-stu-id="ad9cc-141">**InkShiftKeyModifierFlags Enumeration**</span></span>](/windows/desktop/api/msinkaut/ne-msinkaut-inkshiftkeymodifierflags)
</dt> </dl>

 

 




