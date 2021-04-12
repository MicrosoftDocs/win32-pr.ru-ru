---
description: Происходит при перемещении указателя мыши над объектом InkCollector или InkOverlay.
ms.assetid: b25aeead-9fb1-4221-82fa-ce2d81f5fed8
title: Событие InkOverlay. MouseMove (Мсинкаут. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a9ddefd5f3b3f75b03488f74bdbd4aee222a89d9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104272314"
---
# <a name="inkoverlaymousemove-event"></a><span data-ttu-id="7b7a0-103">Событие InkOverlay. MouseMove</span><span class="sxs-lookup"><span data-stu-id="7b7a0-103">InkOverlay.MouseMove event</span></span>

<span data-ttu-id="7b7a0-104">Происходит при перемещении указателя мыши над объектом [**InkCollector**](inkcollector-class.md) или [**InkOverlay**](inkoverlay-class.md) .</span><span class="sxs-lookup"><span data-stu-id="7b7a0-104">Occurs when the mouse pointer is moved over the [**InkCollector**](inkcollector-class.md) or [**InkOverlay**](inkoverlay-class.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="7b7a0-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="7b7a0-105">Syntax</span></span>


```C++
void MouseMove(
  [in]      InkMouseButton           Button,
  [in]      InkShiftKeyModifierFlags Shift,
  [in]      long                     pX,
  [in]      long                     pY,
  [in, out] VARIANT_BOOL             *Cancel
);
```



## <a name="parameters"></a><span data-ttu-id="7b7a0-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="7b7a0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7b7a0-107">*Кнопка "* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="7b7a0-107">*Button* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7b7a0-108">Нажатая кнопка мыши.</span><span class="sxs-lookup"><span data-stu-id="7b7a0-108">The mouse button that was pressed.</span></span>

</dd> <dt>

<span data-ttu-id="7b7a0-109">*SHIFT* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="7b7a0-109">*Shift* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7b7a0-110">Состояние клавиши SHIFT.</span><span class="sxs-lookup"><span data-stu-id="7b7a0-110">The state of the SHIFT key.</span></span>

</dd> <dt>

<span data-ttu-id="7b7a0-111">*ПКС* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="7b7a0-111">*pX* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7b7a0-112">Координата по оси x (в пикселях) щелчка мыши.</span><span class="sxs-lookup"><span data-stu-id="7b7a0-112">The x-coordinate, in pixels, of a mouse click.</span></span>

</dd> <dt>

<span data-ttu-id="7b7a0-113">*Копировать* \[ в окне\]</span><span class="sxs-lookup"><span data-stu-id="7b7a0-113">*pY* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7b7a0-114">Координата по оси y (в пикселях) щелчка мыши.</span><span class="sxs-lookup"><span data-stu-id="7b7a0-114">The y-coordinate, in pixels, of a mouse click.</span></span>

</dd> <dt>

<span data-ttu-id="7b7a0-115">*Отмена* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="7b7a0-115">*Cancel* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="7b7a0-116">Следует ли отменять событие для родительского элемента управления.</span><span class="sxs-lookup"><span data-stu-id="7b7a0-116">Whether the event should be canceled for the parent control.</span></span> <span data-ttu-id="7b7a0-117">Значение по умолчанию — **false**, которое указывает, что событие не должно быть отменено.</span><span class="sxs-lookup"><span data-stu-id="7b7a0-117">The default value is **FALSE**, which specifies that the event should not be canceled.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7b7a0-118">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="7b7a0-118">Return value</span></span>

<span data-ttu-id="7b7a0-119">Это событие не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="7b7a0-119">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="7b7a0-120">Комментарии</span><span class="sxs-lookup"><span data-stu-id="7b7a0-120">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="7b7a0-121">Свойства *px* и *корректировки* находятся в пикселях, а не в HIMETRIC единицах, связанных с пространством рукописного ввода.</span><span class="sxs-lookup"><span data-stu-id="7b7a0-121">The properties *pX* and *pY* are in pixels, and not the HIMETRIC units that are associated with the ink space.</span></span> <span data-ttu-id="7b7a0-122">Это связано с тем, что это событие заменяет связанное событие мыши приложения, не поддерживающего перо, и такого типа приложения распознает только пикселы.</span><span class="sxs-lookup"><span data-stu-id="7b7a0-122">This is because this event replaces the related mouse event of a pen-unaware application and this type of application understands only pixels.</span></span>

 

> [!Note]  
> <span data-ttu-id="7b7a0-123">Некоторые элементы управления используют определенную связь между событиями [**MouseDown**](inkcollector-mousedown.md), [**MouseMove**](inkcollector-mousemove.md)и [**MouseUp**](inkcollector-mouseup.md) .</span><span class="sxs-lookup"><span data-stu-id="7b7a0-123">Some controls rely on a specific relationship between [**MouseDown**](inkcollector-mousedown.md), [**MouseMove**](inkcollector-mousemove.md), and [**MouseUp**](inkcollector-mouseup.md) events.</span></span> <span data-ttu-id="7b7a0-124">Отмена некоторых из этих событий может привести к непредвиденным результатам.</span><span class="sxs-lookup"><span data-stu-id="7b7a0-124">Canceling some of these events may have unanticipated results.</span></span>

 

<span data-ttu-id="7b7a0-125">Этот метод события определен в \_ \_ \_ интерфейсах диспетчеризации (DISP) иинкколлекторевентс, иинковерлайевентс и иинкпиктуривентс с идентификатором DISPID \_ ипемаусемове.</span><span class="sxs-lookup"><span data-stu-id="7b7a0-125">This event method is defined in the \_IInkCollectorEvents, \_IInkOverlayEvents, and \_IInkPictureEvents dispatch-only interfaces (dispinterfaces) with an ID of DISPID\_IPEMouseMove.</span></span>

## <a name="requirements"></a><span data-ttu-id="7b7a0-126">Требования</span><span class="sxs-lookup"><span data-stu-id="7b7a0-126">Requirements</span></span>



| <span data-ttu-id="7b7a0-127">Требование</span><span class="sxs-lookup"><span data-stu-id="7b7a0-127">Requirement</span></span> | <span data-ttu-id="7b7a0-128">Значение</span><span class="sxs-lookup"><span data-stu-id="7b7a0-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7b7a0-129">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="7b7a0-129">Minimum supported client</span></span><br/> | <span data-ttu-id="7b7a0-130">Только классические приложения Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="7b7a0-130">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="7b7a0-131">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="7b7a0-131">Minimum supported server</span></span><br/> | <span data-ttu-id="7b7a0-132">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="7b7a0-132">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="7b7a0-133">Header</span><span class="sxs-lookup"><span data-stu-id="7b7a0-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="7b7a0-134"><dt>Мсинкаут. h (также требуется Мсинкаут \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="7b7a0-134"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="7b7a0-135">Библиотека</span><span class="sxs-lookup"><span data-stu-id="7b7a0-135">Library</span></span><br/>                  | <dl> <span data-ttu-id="7b7a0-136"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7b7a0-136"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="7b7a0-137">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="7b7a0-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7b7a0-138">**Класс InkOverlay**</span><span class="sxs-lookup"><span data-stu-id="7b7a0-138">**InkOverlay Class**</span></span>](inkoverlay-class.md)
</dt> <dt>

[<span data-ttu-id="7b7a0-139">**Перечисление Инкмаусебуттон**</span><span class="sxs-lookup"><span data-stu-id="7b7a0-139">**InkMouseButton Enumeration**</span></span>](/windows/desktop/api/msinkaut/ne-msinkaut-inkmousebutton)
</dt> <dt>

[<span data-ttu-id="7b7a0-140">**Перечисление Инкшифткэймодифиерфлагс**</span><span class="sxs-lookup"><span data-stu-id="7b7a0-140">**InkShiftKeyModifierFlags Enumeration**</span></span>](/windows/desktop/api/msinkaut/ne-msinkaut-inkshiftkeymodifierflags)
</dt> </dl>

 

 




