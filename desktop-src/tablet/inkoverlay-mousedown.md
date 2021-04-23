---
description: Происходит при нажатии кнопки мыши, когда указатель мыши находится над объектом InkCollector или InkOverlay.
ms.assetid: 95c3b1ae-0e77-4ca2-ab73-a0e97ab115b5
title: Событие InkOverlay. MouseDown (Мсинкаут. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c011de55543bee08aeda1a8a986b597523ad805d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105702864"
---
# <a name="inkoverlaymousedown-event"></a><span data-ttu-id="b7170-103">Событие InkOverlay. MouseDown</span><span class="sxs-lookup"><span data-stu-id="b7170-103">InkOverlay.MouseDown event</span></span>

<span data-ttu-id="b7170-104">Происходит при нажатии кнопки мыши, когда указатель мыши находится над объектом [**InkCollector**](inkcollector-class.md) или [**InkOverlay**](inkoverlay-class.md) .</span><span class="sxs-lookup"><span data-stu-id="b7170-104">Occurs when the mouse pointer is over the [**InkCollector**](inkcollector-class.md) or [**InkOverlay**](inkoverlay-class.md) object and a mouse button is pressed.</span></span>

## <a name="syntax"></a><span data-ttu-id="b7170-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b7170-105">Syntax</span></span>


```C++
void MouseDown(
  [in]      InkMouseButton           Button,
  [in]      InkShiftKeyModifierFlags Shift,
  [in]      long                     pX,
  [in]      long                     pY,
  [in, out] VARIANT_BOOL             *Cancel
);
```



## <a name="parameters"></a><span data-ttu-id="b7170-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="b7170-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b7170-107">*Кнопка "* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="b7170-107">*Button* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b7170-108">Нажатая кнопка мыши.</span><span class="sxs-lookup"><span data-stu-id="b7170-108">The mouse button that was pressed.</span></span>

</dd> <dt>

<span data-ttu-id="b7170-109">*SHIFT* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="b7170-109">*Shift* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b7170-110">Состояние клавиши SHIFT.</span><span class="sxs-lookup"><span data-stu-id="b7170-110">The state of the SHIFT key.</span></span>

</dd> <dt>

<span data-ttu-id="b7170-111">*ПКС* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="b7170-111">*pX* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b7170-112">Координата по оси X (в пикселях) щелчка мыши.</span><span class="sxs-lookup"><span data-stu-id="b7170-112">The X-coordinate, in pixels, of a mouse click.</span></span>

</dd> <dt>

<span data-ttu-id="b7170-113">*Копировать* \[ в окне\]</span><span class="sxs-lookup"><span data-stu-id="b7170-113">*pY* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b7170-114">Координата по оси Y (в пикселях) щелчка мыши.</span><span class="sxs-lookup"><span data-stu-id="b7170-114">The Y-coordinate, in pixels, of a mouse click.</span></span>

</dd> <dt>

<span data-ttu-id="b7170-115">*Отмена* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="b7170-115">*Cancel* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="b7170-116">**Вариант \_ Значение TRUE** , чтобы отменить событие для родительского элемента управления; в противном случае — **\_ значение false**.</span><span class="sxs-lookup"><span data-stu-id="b7170-116">**VARIANT\_TRUE** to cancelt he event forthe parent control; otherwise, **VARIANT\_FALSE**.</span></span> <span data-ttu-id="b7170-117">Значение по умолчанию — **Variant \_ false** .</span><span class="sxs-lookup"><span data-stu-id="b7170-117">The default value is **VARIANT\_FALSE**</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b7170-118">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="b7170-118">Return value</span></span>

<span data-ttu-id="b7170-119">Это событие не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="b7170-119">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="b7170-120">Комментарии</span><span class="sxs-lookup"><span data-stu-id="b7170-120">Remarks</span></span>

<span data-ttu-id="b7170-121">Чтобы улучшить производительность рукописного ввода в режиме реального времени, скройте или покажите курсор мыши в обработчиках событий [**MouseDown**](inkcollector-mousedown.md) и [**MouseUp**](inkcollector-mouseup.md) .</span><span class="sxs-lookup"><span data-stu-id="b7170-121">To improve real-time ink performance, hide or show the mouse cursor in the [**MouseDown**](inkcollector-mousedown.md) and [**MouseUp**](inkcollector-mouseup.md) event handlers.</span></span>

> [!Note]  
> <span data-ttu-id="b7170-122">Свойства pX и корректировки находятся в пикселях, а не в HIMETRIC единицах, связанных с пространством рукописного ввода.</span><span class="sxs-lookup"><span data-stu-id="b7170-122">The properties pX and pY are in pixels, and not the HIMETRIC units that are associated with the ink space.</span></span> <span data-ttu-id="b7170-123">Это связано с тем, что это событие заменяет связанное событие мыши приложения, не поддерживающего перо, и такого типа приложения распознает только пикселы.</span><span class="sxs-lookup"><span data-stu-id="b7170-123">This is because this event replaces the related mouse event of a pen-unaware application and this type of application understands only pixels.</span></span>

 

> [!Note]  
> <span data-ttu-id="b7170-124">Некоторые элементы управления используют определенную связь между событиями [**MouseDown**](inkcollector-mousedown.md), [**MouseMove**](inkcollector-mousemove.md)и [**MouseUp**](inkcollector-mouseup.md) .</span><span class="sxs-lookup"><span data-stu-id="b7170-124">Some controls rely on a specific relationship between [**MouseDown**](inkcollector-mousedown.md), [**MouseMove**](inkcollector-mousemove.md), and [**MouseUp**](inkcollector-mouseup.md) events.</span></span> <span data-ttu-id="b7170-125">Отмена некоторых из этих событий может привести к непредвиденным результатам.</span><span class="sxs-lookup"><span data-stu-id="b7170-125">Canceling some of these events may have unanticipated results.</span></span>

 

<span data-ttu-id="b7170-126">Этот метод события определен в \_ \_ \_ интерфейсах диспетчеризации (DISP) иинкколлекторевентс, иинковерлайевентс и иинкпиктуривентс с идентификатором DISPID \_ ипемауседовн.</span><span class="sxs-lookup"><span data-stu-id="b7170-126">This event method is defined in the \_IInkCollectorEvents, \_IInkOverlayEvents, and \_IInkPictureEvents dispatch-only interfaces (dispinterfaces) with an ID of DISPID\_IPEMouseDown.</span></span>

## <a name="requirements"></a><span data-ttu-id="b7170-127">Требования</span><span class="sxs-lookup"><span data-stu-id="b7170-127">Requirements</span></span>



| <span data-ttu-id="b7170-128">Требование</span><span class="sxs-lookup"><span data-stu-id="b7170-128">Requirement</span></span> | <span data-ttu-id="b7170-129">Значение</span><span class="sxs-lookup"><span data-stu-id="b7170-129">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b7170-130">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="b7170-130">Minimum supported client</span></span><br/> | <span data-ttu-id="b7170-131">Только классические приложения Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="b7170-131">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="b7170-132">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="b7170-132">Minimum supported server</span></span><br/> | <span data-ttu-id="b7170-133">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="b7170-133">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="b7170-134">Header</span><span class="sxs-lookup"><span data-stu-id="b7170-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="b7170-135"><dt>Мсинкаут. h (также требуется Мсинкаут \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="b7170-135"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="b7170-136">Библиотека</span><span class="sxs-lookup"><span data-stu-id="b7170-136">Library</span></span><br/>                  | <dl> <span data-ttu-id="b7170-137"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b7170-137"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="b7170-138">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b7170-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b7170-139">**Класс InkOverlay**</span><span class="sxs-lookup"><span data-stu-id="b7170-139">**InkOverlay Class**</span></span>](inkoverlay-class.md)
</dt> <dt>

[<span data-ttu-id="b7170-140">**Перечисление Инкмаусебуттон**</span><span class="sxs-lookup"><span data-stu-id="b7170-140">**InkMouseButton Enumeration**</span></span>](/windows/desktop/api/msinkaut/ne-msinkaut-inkmousebutton)
</dt> <dt>

[<span data-ttu-id="b7170-141">**Перечисление Инкшифткэймодифиерфлагс**</span><span class="sxs-lookup"><span data-stu-id="b7170-141">**InkShiftKeyModifierFlags Enumeration**</span></span>](/windows/desktop/api/msinkaut/ne-msinkaut-inkshiftkeymodifierflags)
</dt> <dt>

[<span data-ttu-id="b7170-142">**MouseUp, событие**</span><span class="sxs-lookup"><span data-stu-id="b7170-142">**MouseUp Event**</span></span>](inkcollector-mouseup.md)
</dt> </dl>

 

 




