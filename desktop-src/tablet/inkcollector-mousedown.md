---
description: Происходит при нажатии кнопки мыши, когда указатель мыши находится над объектом InkCollector или InkOverlay.
ms.assetid: db9ec396-b2a7-4f4f-99f2-95aad46eea28
title: Событие InkCollector. MouseDown (Мсинкаут. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 760801fb5c578ddbdd67b15a4201c21c4981b097
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104540386"
---
# <a name="inkcollectormousedown-event"></a><span data-ttu-id="51e8c-103">Событие InkCollector. MouseDown</span><span class="sxs-lookup"><span data-stu-id="51e8c-103">InkCollector.MouseDown event</span></span>

<span data-ttu-id="51e8c-104">Происходит при нажатии кнопки мыши, когда указатель мыши находится над объектом [**InkCollector**](inkcollector-class.md) или [**InkOverlay**](inkoverlay-class.md) .</span><span class="sxs-lookup"><span data-stu-id="51e8c-104">Occurs when the mouse pointer is over the [**InkCollector**](inkcollector-class.md) or [**InkOverlay**](inkoverlay-class.md) object and a mouse button is pressed.</span></span>

## <a name="syntax"></a><span data-ttu-id="51e8c-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="51e8c-105">Syntax</span></span>


```C++
void MouseDown(
  [in]      InkMouseButton           Button,
  [in]      InkShiftKeyModifierFlags Shift,
  [in]      long                     pX,
  [in]      long                     pY,
  [in, out] VARIANT_BOOL             *Cancel
);
```



## <a name="parameters"></a><span data-ttu-id="51e8c-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="51e8c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="51e8c-107">*Кнопка "* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="51e8c-107">*Button* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="51e8c-108">Нажатая кнопка мыши.</span><span class="sxs-lookup"><span data-stu-id="51e8c-108">The mouse button that was pressed.</span></span>

</dd> <dt>

<span data-ttu-id="51e8c-109">*SHIFT* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="51e8c-109">*Shift* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="51e8c-110">Состояние клавиши SHIFT.</span><span class="sxs-lookup"><span data-stu-id="51e8c-110">The state of the SHIFT key.</span></span>

</dd> <dt>

<span data-ttu-id="51e8c-111">*ПКС* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="51e8c-111">*pX* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="51e8c-112">Координата по оси X (в пикселях) щелчка мыши.</span><span class="sxs-lookup"><span data-stu-id="51e8c-112">The X-coordinate, in pixels, of a mouse click.</span></span>

</dd> <dt>

<span data-ttu-id="51e8c-113">*Копировать* \[ в окне\]</span><span class="sxs-lookup"><span data-stu-id="51e8c-113">*pY* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="51e8c-114">Координата по оси Y (в пикселях) щелчка мыши.</span><span class="sxs-lookup"><span data-stu-id="51e8c-114">The Y-coordinate, in pixels, of a mouse click.</span></span>

</dd> <dt>

<span data-ttu-id="51e8c-115">*Отмена* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="51e8c-115">*Cancel* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="51e8c-116">**Вариант \_ Значение TRUE** , чтобы отменить событие для родительского элемента управления; в противном случае — **\_ значение false**.</span><span class="sxs-lookup"><span data-stu-id="51e8c-116">**VARIANT\_TRUE** to cancel the event for the parent control; otherwise, **VARIANT\_FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="51e8c-117">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="51e8c-117">Return value</span></span>

<span data-ttu-id="51e8c-118">Это событие не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="51e8c-118">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="51e8c-119">Комментарии</span><span class="sxs-lookup"><span data-stu-id="51e8c-119">Remarks</span></span>

<span data-ttu-id="51e8c-120">Чтобы улучшить производительность рукописного ввода в режиме реального времени, скройте или покажите курсор мыши в обработчиках событий **MouseDown** и [**MouseUp**](inkcollector-mouseup.md) .</span><span class="sxs-lookup"><span data-stu-id="51e8c-120">To improve real-time ink performance, hide or show the mouse cursor in the **MouseDown** and [**MouseUp**](inkcollector-mouseup.md) event handlers.</span></span>

> [!Note]  
> <span data-ttu-id="51e8c-121">Свойства *px* и *корректировки* находятся в пикселях, а не в HIMETRIC единицах, связанных с пространством рукописного ввода.</span><span class="sxs-lookup"><span data-stu-id="51e8c-121">The properties *pX* and *pY* are in pixels, and not the HIMETRIC units that are associated with the ink space.</span></span> <span data-ttu-id="51e8c-122">Это связано с тем, что это событие заменяет связанное событие мыши приложения, не поддерживающего перо, и такого типа приложения распознает только пикселы.</span><span class="sxs-lookup"><span data-stu-id="51e8c-122">This is because this event replaces the related mouse event of a pen-unaware application and this type of application understands only pixels.</span></span>

 

> [!Note]  
> <span data-ttu-id="51e8c-123">Некоторые элементы управления используют определенную связь между событиями **MouseDown**, [**MouseMove**](inkcollector-mousemove.md)и [**MouseUp**](inkcollector-mouseup.md) .</span><span class="sxs-lookup"><span data-stu-id="51e8c-123">Some controls rely on a specific relationship between **MouseDown**, [**MouseMove**](inkcollector-mousemove.md), and [**MouseUp**](inkcollector-mouseup.md) events.</span></span> <span data-ttu-id="51e8c-124">Отмена некоторых из этих событий может привести к непредвиденным результатам.</span><span class="sxs-lookup"><span data-stu-id="51e8c-124">Canceling some of these events may have unanticipated results.</span></span>

 

<span data-ttu-id="51e8c-125">Этот метод события определен в \_ \_ \_ интерфейсах диспетчеризации (DISP) иинкколлекторевентс, иинковерлайевентс и иинкпиктуривентс с идентификатором DISPID \_ ипемауседовн.</span><span class="sxs-lookup"><span data-stu-id="51e8c-125">This event method is defined in the \_IInkCollectorEvents, \_IInkOverlayEvents, and \_IInkPictureEvents dispatch-only interfaces (dispinterfaces) with an ID of DISPID\_IPEMouseDown.</span></span>

## <a name="requirements"></a><span data-ttu-id="51e8c-126">Требования</span><span class="sxs-lookup"><span data-stu-id="51e8c-126">Requirements</span></span>



| <span data-ttu-id="51e8c-127">Требование</span><span class="sxs-lookup"><span data-stu-id="51e8c-127">Requirement</span></span> | <span data-ttu-id="51e8c-128">Значение</span><span class="sxs-lookup"><span data-stu-id="51e8c-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="51e8c-129">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="51e8c-129">Minimum supported client</span></span><br/> | <span data-ttu-id="51e8c-130">Только классические приложения Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="51e8c-130">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="51e8c-131">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="51e8c-131">Minimum supported server</span></span><br/> | <span data-ttu-id="51e8c-132">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="51e8c-132">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="51e8c-133">Header</span><span class="sxs-lookup"><span data-stu-id="51e8c-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="51e8c-134"><dt>Мсинкаут. h (также требуется Мсинкаут \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="51e8c-134"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="51e8c-135">Библиотека</span><span class="sxs-lookup"><span data-stu-id="51e8c-135">Library</span></span><br/>                  | <dl> <span data-ttu-id="51e8c-136"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="51e8c-136"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="51e8c-137">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="51e8c-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="51e8c-138">**Класс InkCollector**</span><span class="sxs-lookup"><span data-stu-id="51e8c-138">**InkCollector Class**</span></span>](inkcollector-class.md)
</dt> <dt>

[<span data-ttu-id="51e8c-139">**Перечисление Инкмаусебуттон**</span><span class="sxs-lookup"><span data-stu-id="51e8c-139">**InkMouseButton Enumeration**</span></span>](/windows/desktop/api/msinkaut/ne-msinkaut-inkmousebutton)
</dt> <dt>

[<span data-ttu-id="51e8c-140">**Перечисление Инкшифткэймодифиерфлагс**</span><span class="sxs-lookup"><span data-stu-id="51e8c-140">**InkShiftKeyModifierFlags Enumeration**</span></span>](/windows/desktop/api/msinkaut/ne-msinkaut-inkshiftkeymodifierflags)
</dt> <dt>

[<span data-ttu-id="51e8c-141">**MouseUp, событие**</span><span class="sxs-lookup"><span data-stu-id="51e8c-141">**MouseUp Event**</span></span>](inkcollector-mouseup.md)
</dt> </dl>

 

 




