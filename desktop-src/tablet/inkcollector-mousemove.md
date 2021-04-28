---
description: Событие InkCollector. MouseMove — возникает при перемещении указателя мыши по объекту InkCollector или InkOverlay.
ms.assetid: 688ac7ef-dcee-44a4-8947-117966365061
title: Событие InkCollector. MouseMove (Мсинкаут. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3392f2022af39600cb24461b26d37e5d624f4cb4
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108110162"
---
# <a name="inkcollectormousemove-event"></a><span data-ttu-id="d0e60-103">Событие InkCollector. MouseMove</span><span class="sxs-lookup"><span data-stu-id="d0e60-103">InkCollector.MouseMove event</span></span>

<span data-ttu-id="d0e60-104">Происходит при перемещении указателя мыши над объектом [**InkCollector**](inkcollector-class.md) или [**InkOverlay**](inkoverlay-class.md) .</span><span class="sxs-lookup"><span data-stu-id="d0e60-104">Occurs when the mouse pointer is moved over the [**InkCollector**](inkcollector-class.md) or [**InkOverlay**](inkoverlay-class.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="d0e60-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d0e60-105">Syntax</span></span>


```C++
void MouseMove(
  [in]      InkMouseButton           Button,
  [in]      InkShiftKeyModifierFlags Shift,
  [in]      long                     pX,
  [in]      long                     pY,
  [in, out] VARIANT_BOOL             *Cancel
);
```



## <a name="parameters"></a><span data-ttu-id="d0e60-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="d0e60-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d0e60-107">*Кнопка "* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="d0e60-107">*Button* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d0e60-108">Нажатая кнопка мыши.</span><span class="sxs-lookup"><span data-stu-id="d0e60-108">The mouse button that was pressed.</span></span>

</dd> <dt>

<span data-ttu-id="d0e60-109">*SHIFT* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="d0e60-109">*Shift* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d0e60-110">Состояние клавиши SHIFT.</span><span class="sxs-lookup"><span data-stu-id="d0e60-110">The state of the SHIFT key.</span></span>

</dd> <dt>

<span data-ttu-id="d0e60-111">*ПКС* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="d0e60-111">*pX* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d0e60-112">Координата по оси x (в пикселях) щелчка мыши.</span><span class="sxs-lookup"><span data-stu-id="d0e60-112">The x-coordinate, in pixels, of a mouse click.</span></span>

</dd> <dt>

<span data-ttu-id="d0e60-113">*Копировать* \[ в окне\]</span><span class="sxs-lookup"><span data-stu-id="d0e60-113">*pY* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d0e60-114">Координата по оси y (в пикселях) щелчка мыши.</span><span class="sxs-lookup"><span data-stu-id="d0e60-114">The y-coordinate, in pixels, of a mouse click.</span></span>

</dd> <dt>

<span data-ttu-id="d0e60-115">*Отмена* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="d0e60-115">*Cancel* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="d0e60-116">**Вариант \_ Значение TRUE** , чтобы отменить событие для родительского элемента управления; в противном случае — **\_ значение false**.</span><span class="sxs-lookup"><span data-stu-id="d0e60-116">**VARIANT\_TRUE** to cancel the event for the parent control; otherwise, **VARIANT\_FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d0e60-117">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="d0e60-117">Return value</span></span>

<span data-ttu-id="d0e60-118">Это событие не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="d0e60-118">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="d0e60-119">Remarks</span><span class="sxs-lookup"><span data-stu-id="d0e60-119">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="d0e60-120">Свойства *px* и *корректировки* находятся в пикселях, а не в HIMETRIC единицах, связанных с пространством рукописного ввода.</span><span class="sxs-lookup"><span data-stu-id="d0e60-120">The properties *pX* and *pY* are in pixels, and not the HIMETRIC units that are associated with the ink space.</span></span> <span data-ttu-id="d0e60-121">Это связано с тем, что это событие заменяет связанное событие мыши приложения, не поддерживающего перо, и такого типа приложения распознает только пикселы.</span><span class="sxs-lookup"><span data-stu-id="d0e60-121">This is because this event replaces the related mouse event of a pen-unaware application and this type of application understands only pixels.</span></span>

 

> [!Note]  
> <span data-ttu-id="d0e60-122">Некоторые элементы управления используют определенную связь между событиями [**MouseDown**](inkcollector-mousedown.md), **MouseMove** и [**MouseUp**](inkcollector-mouseup.md) .</span><span class="sxs-lookup"><span data-stu-id="d0e60-122">Some controls rely on a specific relationship between [**MouseDown**](inkcollector-mousedown.md), **MouseMove**, and [**MouseUp**](inkcollector-mouseup.md) events.</span></span> <span data-ttu-id="d0e60-123">Отмена некоторых из этих событий может привести к непредвиденным результатам.</span><span class="sxs-lookup"><span data-stu-id="d0e60-123">Canceling some of these events may have unanticipated results.</span></span>

 

<span data-ttu-id="d0e60-124">Этот метод события определен в \_ \_ \_ интерфейсах диспетчеризации (DISP) иинкколлекторевентс, иинковерлайевентс и иинкпиктуривентс с идентификатором DISPID \_ ипемаусемове.</span><span class="sxs-lookup"><span data-stu-id="d0e60-124">This event method is defined in the \_IInkCollectorEvents, \_IInkOverlayEvents, and \_IInkPictureEvents dispatch-only interfaces (dispinterfaces) with an ID of DISPID\_IPEMouseMove.</span></span>

## <a name="requirements"></a><span data-ttu-id="d0e60-125">Требования</span><span class="sxs-lookup"><span data-stu-id="d0e60-125">Requirements</span></span>



| <span data-ttu-id="d0e60-126">Требование</span><span class="sxs-lookup"><span data-stu-id="d0e60-126">Requirement</span></span> | <span data-ttu-id="d0e60-127">Значение</span><span class="sxs-lookup"><span data-stu-id="d0e60-127">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d0e60-128">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="d0e60-128">Minimum supported client</span></span><br/> | <span data-ttu-id="d0e60-129">Только классические приложения Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="d0e60-129">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="d0e60-130">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="d0e60-130">Minimum supported server</span></span><br/> | <span data-ttu-id="d0e60-131">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="d0e60-131">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="d0e60-132">Header</span><span class="sxs-lookup"><span data-stu-id="d0e60-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="d0e60-133"><dt>Мсинкаут. h (также требуется Мсинкаут \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="d0e60-133"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="d0e60-134">Библиотека</span><span class="sxs-lookup"><span data-stu-id="d0e60-134">Library</span></span><br/>                  | <dl> <span data-ttu-id="d0e60-135"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d0e60-135"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="d0e60-136">См. также</span><span class="sxs-lookup"><span data-stu-id="d0e60-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d0e60-137">**Класс InkCollector**</span><span class="sxs-lookup"><span data-stu-id="d0e60-137">**InkCollector Class**</span></span>](inkcollector-class.md)
</dt> <dt>

[<span data-ttu-id="d0e60-138">**Перечисление Инкмаусебуттон**</span><span class="sxs-lookup"><span data-stu-id="d0e60-138">**InkMouseButton Enumeration**</span></span>](/windows/desktop/api/msinkaut/ne-msinkaut-inkmousebutton)
</dt> <dt>

[<span data-ttu-id="d0e60-139">**Перечисление Инкшифткэймодифиерфлагс**</span><span class="sxs-lookup"><span data-stu-id="d0e60-139">**InkShiftKeyModifierFlags Enumeration**</span></span>](/windows/desktop/api/msinkaut/ne-msinkaut-inkshiftkeymodifierflags)
</dt> </dl>

 

 




