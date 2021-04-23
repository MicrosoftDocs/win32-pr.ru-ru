---
description: Происходит при перемещении указателя мыши над объектом InkCollector или InkOverlay.
ms.assetid: 688ac7ef-dcee-44a4-8947-117966365061
title: Событие InkCollector. MouseMove (Мсинкаут. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 27ad88c35871ed73125be73b66329ede464f0c00
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105701458"
---
# <a name="inkcollectormousemove-event"></a><span data-ttu-id="a8eb1-103">Событие InkCollector. MouseMove</span><span class="sxs-lookup"><span data-stu-id="a8eb1-103">InkCollector.MouseMove event</span></span>

<span data-ttu-id="a8eb1-104">Происходит при перемещении указателя мыши над объектом [**InkCollector**](inkcollector-class.md) или [**InkOverlay**](inkoverlay-class.md) .</span><span class="sxs-lookup"><span data-stu-id="a8eb1-104">Occurs when the mouse pointer is moved over the [**InkCollector**](inkcollector-class.md) or [**InkOverlay**](inkoverlay-class.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="a8eb1-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a8eb1-105">Syntax</span></span>


```C++
void MouseMove(
  [in]      InkMouseButton           Button,
  [in]      InkShiftKeyModifierFlags Shift,
  [in]      long                     pX,
  [in]      long                     pY,
  [in, out] VARIANT_BOOL             *Cancel
);
```



## <a name="parameters"></a><span data-ttu-id="a8eb1-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="a8eb1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a8eb1-107">*Кнопка "* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="a8eb1-107">*Button* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a8eb1-108">Нажатая кнопка мыши.</span><span class="sxs-lookup"><span data-stu-id="a8eb1-108">The mouse button that was pressed.</span></span>

</dd> <dt>

<span data-ttu-id="a8eb1-109">*SHIFT* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="a8eb1-109">*Shift* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a8eb1-110">Состояние клавиши SHIFT.</span><span class="sxs-lookup"><span data-stu-id="a8eb1-110">The state of the SHIFT key.</span></span>

</dd> <dt>

<span data-ttu-id="a8eb1-111">*ПКС* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="a8eb1-111">*pX* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a8eb1-112">Координата по оси x (в пикселях) щелчка мыши.</span><span class="sxs-lookup"><span data-stu-id="a8eb1-112">The x-coordinate, in pixels, of a mouse click.</span></span>

</dd> <dt>

<span data-ttu-id="a8eb1-113">*Копировать* \[ в окне\]</span><span class="sxs-lookup"><span data-stu-id="a8eb1-113">*pY* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a8eb1-114">Координата по оси y (в пикселях) щелчка мыши.</span><span class="sxs-lookup"><span data-stu-id="a8eb1-114">The y-coordinate, in pixels, of a mouse click.</span></span>

</dd> <dt>

<span data-ttu-id="a8eb1-115">*Отмена* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="a8eb1-115">*Cancel* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="a8eb1-116">**Вариант \_ Значение TRUE** , чтобы отменить событие для родительского элемента управления; в противном случае — **\_ значение false**.</span><span class="sxs-lookup"><span data-stu-id="a8eb1-116">**VARIANT\_TRUE** to cancel the event for the parent control; otherwise, **VARIANT\_FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a8eb1-117">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="a8eb1-117">Return value</span></span>

<span data-ttu-id="a8eb1-118">Это событие не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="a8eb1-118">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="a8eb1-119">Комментарии</span><span class="sxs-lookup"><span data-stu-id="a8eb1-119">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="a8eb1-120">Свойства *px* и *корректировки* находятся в пикселях, а не в HIMETRIC единицах, связанных с пространством рукописного ввода.</span><span class="sxs-lookup"><span data-stu-id="a8eb1-120">The properties *pX* and *pY* are in pixels, and not the HIMETRIC units that are associated with the ink space.</span></span> <span data-ttu-id="a8eb1-121">Это связано с тем, что это событие заменяет связанное событие мыши приложения, не поддерживающего перо, и такого типа приложения распознает только пикселы.</span><span class="sxs-lookup"><span data-stu-id="a8eb1-121">This is because this event replaces the related mouse event of a pen-unaware application and this type of application understands only pixels.</span></span>

 

> [!Note]  
> <span data-ttu-id="a8eb1-122">Некоторые элементы управления используют определенную связь между событиями [**MouseDown**](inkcollector-mousedown.md), **MouseMove** и [**MouseUp**](inkcollector-mouseup.md) .</span><span class="sxs-lookup"><span data-stu-id="a8eb1-122">Some controls rely on a specific relationship between [**MouseDown**](inkcollector-mousedown.md), **MouseMove**, and [**MouseUp**](inkcollector-mouseup.md) events.</span></span> <span data-ttu-id="a8eb1-123">Отмена некоторых из этих событий может привести к непредвиденным результатам.</span><span class="sxs-lookup"><span data-stu-id="a8eb1-123">Canceling some of these events may have unanticipated results.</span></span>

 

<span data-ttu-id="a8eb1-124">Этот метод события определен в \_ \_ \_ интерфейсах диспетчеризации (DISP) иинкколлекторевентс, иинковерлайевентс и иинкпиктуривентс с идентификатором DISPID \_ ипемаусемове.</span><span class="sxs-lookup"><span data-stu-id="a8eb1-124">This event method is defined in the \_IInkCollectorEvents, \_IInkOverlayEvents, and \_IInkPictureEvents dispatch-only interfaces (dispinterfaces) with an ID of DISPID\_IPEMouseMove.</span></span>

## <a name="requirements"></a><span data-ttu-id="a8eb1-125">Требования</span><span class="sxs-lookup"><span data-stu-id="a8eb1-125">Requirements</span></span>



| <span data-ttu-id="a8eb1-126">Требование</span><span class="sxs-lookup"><span data-stu-id="a8eb1-126">Requirement</span></span> | <span data-ttu-id="a8eb1-127">Значение</span><span class="sxs-lookup"><span data-stu-id="a8eb1-127">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a8eb1-128">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="a8eb1-128">Minimum supported client</span></span><br/> | <span data-ttu-id="a8eb1-129">Только классические приложения Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="a8eb1-129">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="a8eb1-130">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="a8eb1-130">Minimum supported server</span></span><br/> | <span data-ttu-id="a8eb1-131">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="a8eb1-131">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="a8eb1-132">Header</span><span class="sxs-lookup"><span data-stu-id="a8eb1-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="a8eb1-133"><dt>Мсинкаут. h (также требуется Мсинкаут \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="a8eb1-133"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="a8eb1-134">Библиотека</span><span class="sxs-lookup"><span data-stu-id="a8eb1-134">Library</span></span><br/>                  | <dl> <span data-ttu-id="a8eb1-135"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a8eb1-135"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="a8eb1-136">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a8eb1-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a8eb1-137">**Класс InkCollector**</span><span class="sxs-lookup"><span data-stu-id="a8eb1-137">**InkCollector Class**</span></span>](inkcollector-class.md)
</dt> <dt>

[<span data-ttu-id="a8eb1-138">**Перечисление Инкмаусебуттон**</span><span class="sxs-lookup"><span data-stu-id="a8eb1-138">**InkMouseButton Enumeration**</span></span>](/windows/desktop/api/msinkaut/ne-msinkaut-inkmousebutton)
</dt> <dt>

[<span data-ttu-id="a8eb1-139">**Перечисление Инкшифткэймодифиерфлагс**</span><span class="sxs-lookup"><span data-stu-id="a8eb1-139">**InkShiftKeyModifierFlags Enumeration**</span></span>](/windows/desktop/api/msinkaut/ne-msinkaut-inkshiftkeymodifierflags)
</dt> </dl>

 

 




