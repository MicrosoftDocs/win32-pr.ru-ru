---
description: Событие InkOverlay. MouseMove — происходит при перемещении указателя мыши по объекту InkCollector или InkOverlay.
ms.assetid: b25aeead-9fb1-4221-82fa-ce2d81f5fed8
title: Событие InkOverlay. MouseMove (Мсинкаут. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5f8290a11b00dcf97b3f3d8568ebe9890f715454
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108116912"
---
# <a name="inkoverlaymousemove-event"></a><span data-ttu-id="c6f26-103">Событие InkOverlay. MouseMove</span><span class="sxs-lookup"><span data-stu-id="c6f26-103">InkOverlay.MouseMove event</span></span>

<span data-ttu-id="c6f26-104">Происходит при перемещении указателя мыши над объектом [**InkCollector**](inkcollector-class.md) или [**InkOverlay**](inkoverlay-class.md) .</span><span class="sxs-lookup"><span data-stu-id="c6f26-104">Occurs when the mouse pointer is moved over the [**InkCollector**](inkcollector-class.md) or [**InkOverlay**](inkoverlay-class.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="c6f26-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c6f26-105">Syntax</span></span>


```C++
void MouseMove(
  [in]      InkMouseButton           Button,
  [in]      InkShiftKeyModifierFlags Shift,
  [in]      long                     pX,
  [in]      long                     pY,
  [in, out] VARIANT_BOOL             *Cancel
);
```



## <a name="parameters"></a><span data-ttu-id="c6f26-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="c6f26-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c6f26-107">*Кнопка "* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="c6f26-107">*Button* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c6f26-108">Нажатая кнопка мыши.</span><span class="sxs-lookup"><span data-stu-id="c6f26-108">The mouse button that was pressed.</span></span>

</dd> <dt>

<span data-ttu-id="c6f26-109">*SHIFT* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="c6f26-109">*Shift* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c6f26-110">Состояние клавиши SHIFT.</span><span class="sxs-lookup"><span data-stu-id="c6f26-110">The state of the SHIFT key.</span></span>

</dd> <dt>

<span data-ttu-id="c6f26-111">*ПКС* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="c6f26-111">*pX* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c6f26-112">Координата по оси x (в пикселях) щелчка мыши.</span><span class="sxs-lookup"><span data-stu-id="c6f26-112">The x-coordinate, in pixels, of a mouse click.</span></span>

</dd> <dt>

<span data-ttu-id="c6f26-113">*Копировать* \[ в окне\]</span><span class="sxs-lookup"><span data-stu-id="c6f26-113">*pY* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c6f26-114">Координата по оси y (в пикселях) щелчка мыши.</span><span class="sxs-lookup"><span data-stu-id="c6f26-114">The y-coordinate, in pixels, of a mouse click.</span></span>

</dd> <dt>

<span data-ttu-id="c6f26-115">*Отмена* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="c6f26-115">*Cancel* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="c6f26-116">Следует ли отменять событие для родительского элемента управления.</span><span class="sxs-lookup"><span data-stu-id="c6f26-116">Whether the event should be canceled for the parent control.</span></span> <span data-ttu-id="c6f26-117">Значение по умолчанию — **false**, которое указывает, что событие не должно быть отменено.</span><span class="sxs-lookup"><span data-stu-id="c6f26-117">The default value is **FALSE**, which specifies that the event should not be canceled.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c6f26-118">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="c6f26-118">Return value</span></span>

<span data-ttu-id="c6f26-119">Это событие не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="c6f26-119">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="c6f26-120">Remarks</span><span class="sxs-lookup"><span data-stu-id="c6f26-120">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="c6f26-121">Свойства *px* и *корректировки* находятся в пикселях, а не в HIMETRIC единицах, связанных с пространством рукописного ввода.</span><span class="sxs-lookup"><span data-stu-id="c6f26-121">The properties *pX* and *pY* are in pixels, and not the HIMETRIC units that are associated with the ink space.</span></span> <span data-ttu-id="c6f26-122">Это связано с тем, что это событие заменяет связанное событие мыши приложения, не поддерживающего перо, и такого типа приложения распознает только пикселы.</span><span class="sxs-lookup"><span data-stu-id="c6f26-122">This is because this event replaces the related mouse event of a pen-unaware application and this type of application understands only pixels.</span></span>

 

> [!Note]  
> <span data-ttu-id="c6f26-123">Некоторые элементы управления используют определенную связь между событиями [**MouseDown**](inkcollector-mousedown.md), [**MouseMove**](inkcollector-mousemove.md)и [**MouseUp**](inkcollector-mouseup.md) .</span><span class="sxs-lookup"><span data-stu-id="c6f26-123">Some controls rely on a specific relationship between [**MouseDown**](inkcollector-mousedown.md), [**MouseMove**](inkcollector-mousemove.md), and [**MouseUp**](inkcollector-mouseup.md) events.</span></span> <span data-ttu-id="c6f26-124">Отмена некоторых из этих событий может привести к непредвиденным результатам.</span><span class="sxs-lookup"><span data-stu-id="c6f26-124">Canceling some of these events may have unanticipated results.</span></span>

 

<span data-ttu-id="c6f26-125">Этот метод события определен в \_ \_ \_ интерфейсах диспетчеризации (DISP) иинкколлекторевентс, иинковерлайевентс и иинкпиктуривентс с идентификатором DISPID \_ ипемаусемове.</span><span class="sxs-lookup"><span data-stu-id="c6f26-125">This event method is defined in the \_IInkCollectorEvents, \_IInkOverlayEvents, and \_IInkPictureEvents dispatch-only interfaces (dispinterfaces) with an ID of DISPID\_IPEMouseMove.</span></span>

## <a name="requirements"></a><span data-ttu-id="c6f26-126">Требования</span><span class="sxs-lookup"><span data-stu-id="c6f26-126">Requirements</span></span>



| <span data-ttu-id="c6f26-127">Требование</span><span class="sxs-lookup"><span data-stu-id="c6f26-127">Requirement</span></span> | <span data-ttu-id="c6f26-128">Значение</span><span class="sxs-lookup"><span data-stu-id="c6f26-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c6f26-129">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="c6f26-129">Minimum supported client</span></span><br/> | <span data-ttu-id="c6f26-130">Только классические приложения Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="c6f26-130">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="c6f26-131">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="c6f26-131">Minimum supported server</span></span><br/> | <span data-ttu-id="c6f26-132">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="c6f26-132">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="c6f26-133">Header</span><span class="sxs-lookup"><span data-stu-id="c6f26-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="c6f26-134"><dt>Мсинкаут. h (также требуется Мсинкаут \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="c6f26-134"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="c6f26-135">Библиотека</span><span class="sxs-lookup"><span data-stu-id="c6f26-135">Library</span></span><br/>                  | <dl> <span data-ttu-id="c6f26-136"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c6f26-136"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="c6f26-137">См. также</span><span class="sxs-lookup"><span data-stu-id="c6f26-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c6f26-138">**Класс InkOverlay**</span><span class="sxs-lookup"><span data-stu-id="c6f26-138">**InkOverlay Class**</span></span>](inkoverlay-class.md)
</dt> <dt>

[<span data-ttu-id="c6f26-139">**Перечисление Инкмаусебуттон**</span><span class="sxs-lookup"><span data-stu-id="c6f26-139">**InkMouseButton Enumeration**</span></span>](/windows/desktop/api/msinkaut/ne-msinkaut-inkmousebutton)
</dt> <dt>

[<span data-ttu-id="c6f26-140">**Перечисление Инкшифткэймодифиерфлагс**</span><span class="sxs-lookup"><span data-stu-id="c6f26-140">**InkShiftKeyModifierFlags Enumeration**</span></span>](/windows/desktop/api/msinkaut/ne-msinkaut-inkshiftkeymodifierflags)
</dt> </dl>

 

 




