---
description: Происходит при движении колесика мыши, когда объект InkCollector или InkOverlay имеет фокус.
ms.assetid: b7269e07-7001-48ca-8e20-a39cb02f3719
title: Событие InkOverlay. Маусевхил (Мсинкаут. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7bbd919fdf02d85c32efa2a1a923d5de7ebe4f5b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103912911"
---
# <a name="inkoverlaymousewheel-event"></a><span data-ttu-id="3f55e-103">Событие InkOverlay. Маусевхил</span><span class="sxs-lookup"><span data-stu-id="3f55e-103">InkOverlay.MouseWheel event</span></span>

<span data-ttu-id="3f55e-104">Происходит при движении колесика мыши, когда объект [**InkCollector**](inkcollector-class.md) или [**InkOverlay**](inkoverlay-class.md) имеет фокус.</span><span class="sxs-lookup"><span data-stu-id="3f55e-104">Occurs when the mouse wheel moves while the [**InkCollector**](inkcollector-class.md) or [**InkOverlay**](inkoverlay-class.md) object has focus.</span></span>

## <a name="syntax"></a><span data-ttu-id="3f55e-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="3f55e-105">Syntax</span></span>


```C++
void MouseWheel(
  [in]      InkMouseButton           Button,
  [in]      InkShiftKeyModifierFlags Shift,
  [in]      long                     Delta,
  [in]      long                     x,
  [in]      long                     y,
  [in, out] VARIANT_BOOL             *Cancel
);
```



## <a name="parameters"></a><span data-ttu-id="3f55e-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="3f55e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3f55e-107">*Кнопка "* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="3f55e-107">*Button* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3f55e-108">Нажатая кнопка мыши.</span><span class="sxs-lookup"><span data-stu-id="3f55e-108">The mouse button that was pressed.</span></span>

</dd> <dt>

<span data-ttu-id="3f55e-109">*SHIFT* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="3f55e-109">*Shift* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3f55e-110">Состояние клавиши SHIFT.</span><span class="sxs-lookup"><span data-stu-id="3f55e-110">The state of the SHIFT key.</span></span>

</dd> <dt>

<span data-ttu-id="3f55e-111">*Дельта* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="3f55e-111">*Delta* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3f55e-112">Число со знаком для числа поворотов, повернутых колесиком мыши.</span><span class="sxs-lookup"><span data-stu-id="3f55e-112">A signed count of the number of detents the mouse wheel has rotated.</span></span> <span data-ttu-id="3f55e-113">Делением называется один зубец колесика мыши.</span><span class="sxs-lookup"><span data-stu-id="3f55e-113">A detent is one notch of the mouse wheel.</span></span>

</dd> <dt>

<span data-ttu-id="3f55e-114">*x* \[ в\]</span><span class="sxs-lookup"><span data-stu-id="3f55e-114">*x* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3f55e-115">Координата по оси x (в пикселях) щелчка мыши.</span><span class="sxs-lookup"><span data-stu-id="3f55e-115">The x-coordinate, in pixels, of a mouse click.</span></span>

</dd> <dt>

<span data-ttu-id="3f55e-116">*y* \[ в\]</span><span class="sxs-lookup"><span data-stu-id="3f55e-116">*y* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3f55e-117">Координата по оси y (в пикселях) щелчка мыши.</span><span class="sxs-lookup"><span data-stu-id="3f55e-117">The y-coordinate, in pixels, of a mouse click.</span></span>

</dd> <dt>

<span data-ttu-id="3f55e-118">*Отмена* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="3f55e-118">*Cancel* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="3f55e-119">Следует ли отменять событие для родительского элемента управления.</span><span class="sxs-lookup"><span data-stu-id="3f55e-119">Whether the event should be canceled for the parent control.</span></span> <span data-ttu-id="3f55e-120">Значение по умолчанию — **false**, которое указывает, что событие не должно быть отменено.</span><span class="sxs-lookup"><span data-stu-id="3f55e-120">The default value is **FALSE**, which specifies that the event should not be canceled.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3f55e-121">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="3f55e-121">Return value</span></span>

<span data-ttu-id="3f55e-122">Это событие не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="3f55e-122">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="3f55e-123">Комментарии</span><span class="sxs-lookup"><span data-stu-id="3f55e-123">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="3f55e-124">Свойства *px* и *корректировки* находятся в пикселях, а не в HIMETRIC единицах, связанных с пространством рукописного ввода.</span><span class="sxs-lookup"><span data-stu-id="3f55e-124">The properties *pX* and *pY* are in pixels, and not the HIMETRIC units that are associated with the ink space.</span></span> <span data-ttu-id="3f55e-125">Это связано с тем, что это событие заменяет связанное событие мыши приложения, не поддерживающего перо, и такого типа приложения распознает только пикселы.</span><span class="sxs-lookup"><span data-stu-id="3f55e-125">This is because this event replaces the related mouse event of a pen-unaware application and this type of application understands only pixels.</span></span>

 

<span data-ttu-id="3f55e-126">Этот метод события определен в \_ \_ \_ интерфейсах диспетчеризации (DISP) иинкколлекторевентс, иинковерлайевентс и иинкпиктуривентс с идентификатором DISPID \_ ипемаусевхил.</span><span class="sxs-lookup"><span data-stu-id="3f55e-126">This event method is defined in the \_IInkCollectorEvents, \_IInkOverlayEvents, and \_IInkPictureEvents dispatch-only interfaces (dispinterfaces) with an ID of DISPID\_IPEMouseWheel.</span></span>

## <a name="requirements"></a><span data-ttu-id="3f55e-127">Требования</span><span class="sxs-lookup"><span data-stu-id="3f55e-127">Requirements</span></span>



| <span data-ttu-id="3f55e-128">Требование</span><span class="sxs-lookup"><span data-stu-id="3f55e-128">Requirement</span></span> | <span data-ttu-id="3f55e-129">Значение</span><span class="sxs-lookup"><span data-stu-id="3f55e-129">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3f55e-130">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="3f55e-130">Minimum supported client</span></span><br/> | <span data-ttu-id="3f55e-131">Только классические приложения Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="3f55e-131">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="3f55e-132">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="3f55e-132">Minimum supported server</span></span><br/> | <span data-ttu-id="3f55e-133">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="3f55e-133">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="3f55e-134">Header</span><span class="sxs-lookup"><span data-stu-id="3f55e-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="3f55e-135"><dt>Мсинкаут. h (также требуется Мсинкаут \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="3f55e-135"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="3f55e-136">Библиотека</span><span class="sxs-lookup"><span data-stu-id="3f55e-136">Library</span></span><br/>                  | <dl> <span data-ttu-id="3f55e-137"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3f55e-137"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="3f55e-138">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="3f55e-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3f55e-139">**Класс InkOverlay**</span><span class="sxs-lookup"><span data-stu-id="3f55e-139">**InkOverlay Class**</span></span>](inkoverlay-class.md)
</dt> <dt>

[<span data-ttu-id="3f55e-140">**Перечисление Инкмаусебуттон**</span><span class="sxs-lookup"><span data-stu-id="3f55e-140">**InkMouseButton Enumeration**</span></span>](/windows/desktop/api/msinkaut/ne-msinkaut-inkmousebutton)
</dt> <dt>

[<span data-ttu-id="3f55e-141">**Перечисление Инкшифткэймодифиерфлагс**</span><span class="sxs-lookup"><span data-stu-id="3f55e-141">**InkShiftKeyModifierFlags Enumeration**</span></span>](/windows/desktop/api/msinkaut/ne-msinkaut-inkshiftkeymodifierflags)
</dt> </dl>

 

 




