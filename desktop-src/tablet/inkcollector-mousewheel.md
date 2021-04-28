---
description: Событие InkCollector. Маусевхил — происходит при движении колесика мыши, когда объект InkCollector или InkOverlay имеет фокус.
ms.assetid: 418cf67c-0ec0-49e3-a17f-9eaeb40bb602
title: Событие InkCollector. Маусевхил (Мсинкаут. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 851a017af4bb71917c88e2194db86eec64218771
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108110142"
---
# <a name="inkcollectormousewheel-event"></a><span data-ttu-id="ac30f-103">Событие InkCollector. Маусевхил</span><span class="sxs-lookup"><span data-stu-id="ac30f-103">InkCollector.MouseWheel event</span></span>

<span data-ttu-id="ac30f-104">Происходит при движении колесика мыши, когда объект [**InkCollector**](inkcollector-class.md) или [**InkOverlay**](inkoverlay-class.md) имеет фокус.</span><span class="sxs-lookup"><span data-stu-id="ac30f-104">Occurs when the mouse wheel moves while the [**InkCollector**](inkcollector-class.md) or [**InkOverlay**](inkoverlay-class.md) object has focus.</span></span>

## <a name="syntax"></a><span data-ttu-id="ac30f-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ac30f-105">Syntax</span></span>


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



## <a name="parameters"></a><span data-ttu-id="ac30f-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="ac30f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ac30f-107">*Кнопка "* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="ac30f-107">*Button* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ac30f-108">Нажатая кнопка мыши.</span><span class="sxs-lookup"><span data-stu-id="ac30f-108">The mouse button that was pressed.</span></span>

</dd> <dt>

<span data-ttu-id="ac30f-109">*SHIFT* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="ac30f-109">*Shift* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ac30f-110">Состояние клавиши SHIFT.</span><span class="sxs-lookup"><span data-stu-id="ac30f-110">The state of the SHIFT key.</span></span>

</dd> <dt>

<span data-ttu-id="ac30f-111">*Дельта* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="ac30f-111">*Delta* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ac30f-112">Число со знаком для числа поворотов, повернутых колесиком мыши.</span><span class="sxs-lookup"><span data-stu-id="ac30f-112">A signed count of the number of detents the mouse wheel has rotated.</span></span> <span data-ttu-id="ac30f-113">Делением называется один зубец колесика мыши.</span><span class="sxs-lookup"><span data-stu-id="ac30f-113">A detent is one notch of the mouse wheel.</span></span>

</dd> <dt>

<span data-ttu-id="ac30f-114">*x* \[ в\]</span><span class="sxs-lookup"><span data-stu-id="ac30f-114">*x* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ac30f-115">Координата по оси x (в пикселях) щелчка мыши.</span><span class="sxs-lookup"><span data-stu-id="ac30f-115">The x-coordinate, in pixels, of a mouse click.</span></span>

</dd> <dt>

<span data-ttu-id="ac30f-116">*y* \[ в\]</span><span class="sxs-lookup"><span data-stu-id="ac30f-116">*y* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ac30f-117">Координата по оси y (в пикселях) щелчка мыши.</span><span class="sxs-lookup"><span data-stu-id="ac30f-117">The y-coordinate, in pixels, of a mouse click.</span></span>

</dd> <dt>

<span data-ttu-id="ac30f-118">*Отмена* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="ac30f-118">*Cancel* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="ac30f-119">**Вариант \_ Значение TRUE** , чтобы отменить событие для родительского элемента управления; в противном случае — **\_ значение false**.</span><span class="sxs-lookup"><span data-stu-id="ac30f-119">**VARIANT\_TRUE** to cancel the event for the parent control; otherwise, **VARIANT\_FALSE**.</span></span> <span data-ttu-id="ac30f-120">Значение по умолчанию — **Variant \_ false**.</span><span class="sxs-lookup"><span data-stu-id="ac30f-120">The default value is **VARIANT\_FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ac30f-121">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="ac30f-121">Return value</span></span>

<span data-ttu-id="ac30f-122">Это событие не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="ac30f-122">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="ac30f-123">Remarks</span><span class="sxs-lookup"><span data-stu-id="ac30f-123">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="ac30f-124">Свойства *px* и *корректировки* находятся в пикселях, а не в HIMETRIC единицах, связанных с пространством рукописного ввода.</span><span class="sxs-lookup"><span data-stu-id="ac30f-124">The properties *pX* and *pY* are in pixels, and not the HIMETRIC units that are associated with the ink space.</span></span> <span data-ttu-id="ac30f-125">Это связано с тем, что это событие заменяет связанное событие мыши приложения, не поддерживающего перо, и такого типа приложения распознает только пикселы.</span><span class="sxs-lookup"><span data-stu-id="ac30f-125">This is because this event replaces the related mouse event of a pen-unaware application and this type of application understands only pixels.</span></span>

 

<span data-ttu-id="ac30f-126">Этот метод события определен в \_ \_ \_ интерфейсах диспетчеризации (DISP) иинкколлекторевентс, иинковерлайевентс и иинкпиктуривентс с идентификатором DISPID \_ ипемаусевхил.</span><span class="sxs-lookup"><span data-stu-id="ac30f-126">This event method is defined in the \_IInkCollectorEvents, \_IInkOverlayEvents, and \_IInkPictureEvents dispatch-only interfaces (dispinterfaces) with an ID of DISPID\_IPEMouseWheel.</span></span>

## <a name="requirements"></a><span data-ttu-id="ac30f-127">Требования</span><span class="sxs-lookup"><span data-stu-id="ac30f-127">Requirements</span></span>



| <span data-ttu-id="ac30f-128">Требование</span><span class="sxs-lookup"><span data-stu-id="ac30f-128">Requirement</span></span> | <span data-ttu-id="ac30f-129">Значение</span><span class="sxs-lookup"><span data-stu-id="ac30f-129">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ac30f-130">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="ac30f-130">Minimum supported client</span></span><br/> | <span data-ttu-id="ac30f-131">Только классические приложения Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="ac30f-131">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="ac30f-132">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="ac30f-132">Minimum supported server</span></span><br/> | <span data-ttu-id="ac30f-133">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="ac30f-133">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="ac30f-134">Header</span><span class="sxs-lookup"><span data-stu-id="ac30f-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="ac30f-135"><dt>Мсинкаут. h (также требуется Мсинкаут \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="ac30f-135"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="ac30f-136">Библиотека</span><span class="sxs-lookup"><span data-stu-id="ac30f-136">Library</span></span><br/>                  | <dl> <span data-ttu-id="ac30f-137"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ac30f-137"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="ac30f-138">См. также</span><span class="sxs-lookup"><span data-stu-id="ac30f-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ac30f-139">**Класс InkCollector**</span><span class="sxs-lookup"><span data-stu-id="ac30f-139">**InkCollector Class**</span></span>](inkcollector-class.md)
</dt> <dt>

[<span data-ttu-id="ac30f-140">**Перечисление Инкмаусебуттон**</span><span class="sxs-lookup"><span data-stu-id="ac30f-140">**InkMouseButton Enumeration**</span></span>](/windows/desktop/api/msinkaut/ne-msinkaut-inkmousebutton)
</dt> <dt>

[<span data-ttu-id="ac30f-141">**Перечисление Инкшифткэймодифиерфлагс**</span><span class="sxs-lookup"><span data-stu-id="ac30f-141">**InkShiftKeyModifierFlags Enumeration**</span></span>](/windows/desktop/api/msinkaut/ne-msinkaut-inkshiftkeymodifierflags)
</dt> </dl>

 

 




