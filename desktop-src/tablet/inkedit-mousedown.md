---
description: Происходит, когда пользователь нажимает кнопку мыши, когда указатель мыши находится над элементом управления InkEdit.
ms.assetid: 8985fee5-7b63-46ab-b229-046e2f0ee004
title: Событие InkEdit. MouseDown (с. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 78e684fe2d75e5eaaf2b0064e8c7c78cbfe281a5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103912915"
---
# <a name="inkeditmousedown-event"></a><span data-ttu-id="0cf90-103">InkEdit. MouseDown, событие</span><span class="sxs-lookup"><span data-stu-id="0cf90-103">InkEdit.MouseDown event</span></span>

<span data-ttu-id="0cf90-104">Происходит, когда пользователь нажимает кнопку мыши, когда указатель мыши находится над элементом управления [InkEdit](inkedit-control-reference.md) .</span><span class="sxs-lookup"><span data-stu-id="0cf90-104">Occurs when the user presses a mouse button while the mouse is over the [InkEdit](inkedit-control-reference.md) control.</span></span>

## <a name="syntax"></a><span data-ttu-id="0cf90-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="0cf90-105">Syntax</span></span>


```C++
HRESULT MouseDown(
   short Button,
   short ShiftKey,
   long  xMouse,
   long  yMouse
);
```



## <a name="parameters"></a><span data-ttu-id="0cf90-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="0cf90-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0cf90-107">*Кнопка*</span><span class="sxs-lookup"><span data-stu-id="0cf90-107">*Button*</span></span> 
</dt> <dd>

<span data-ttu-id="0cf90-108">Элемент перечисления [**маусебуттон**](/windows/desktop/api/inked/ne-inked-mousebutton) , указывающий, какие кнопки мыши были нажаты.</span><span class="sxs-lookup"><span data-stu-id="0cf90-108">A member of the [**MouseButton**](/windows/desktop/api/inked/ne-inked-mousebutton) enumeration that indicates which mouse buttons were pressed.</span></span>



| <span data-ttu-id="0cf90-109">Значение</span><span class="sxs-lookup"><span data-stu-id="0cf90-109">Value</span></span>                                                                                                                                                            | <span data-ttu-id="0cf90-110">Значение</span><span class="sxs-lookup"><span data-stu-id="0cf90-110">Meaning</span></span>                                           |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------|
| <span id="NO_BUTTON_"></span><span id="no_button_"></span><dl> <span data-ttu-id="0cf90-111"><dt>**Нет \_ Кнопка "**</dt></span><span class="sxs-lookup"><span data-stu-id="0cf90-111"><dt>**NO\_BUTTON** </dt></span></span> </dl>             | <span data-ttu-id="0cf90-112">По умолчанию.</span><span class="sxs-lookup"><span data-stu-id="0cf90-112">Default.</span></span> <span data-ttu-id="0cf90-113">Никакая кнопка мыши не была нажата.</span><span class="sxs-lookup"><span data-stu-id="0cf90-113">No mouse button was pressed.</span></span> <br/> |
| <span id="LEFT_BUTTON_"></span><span id="left_button_"></span><dl> <span data-ttu-id="0cf90-114"><dt>По **левому краю \_ Кнопка "**</dt></span><span class="sxs-lookup"><span data-stu-id="0cf90-114"><dt>**LEFT\_BUTTON** </dt></span></span> </dl>       | <span data-ttu-id="0cf90-115">Была нажата левая кнопка мыши.</span><span class="sxs-lookup"><span data-stu-id="0cf90-115">The left mouse button was pressed.</span></span> <br/>    |
| <span id="RIGHT_BUTTON_"></span><span id="right_button_"></span><dl> <span data-ttu-id="0cf90-116"><dt>По **правому краю \_ Кнопка "**</dt></span><span class="sxs-lookup"><span data-stu-id="0cf90-116"><dt>**RIGHT\_BUTTON** </dt></span></span> </dl>    | <span data-ttu-id="0cf90-117">Была нажата правая кнопка мыши.</span><span class="sxs-lookup"><span data-stu-id="0cf90-117">The right mouse button was pressed.</span></span> <br/>   |
| <span id="MIDDLE_BUTTON_"></span><span id="middle_button_"></span><dl> <span data-ttu-id="0cf90-118"><dt>По **середине \_ Кнопка "**</dt></span><span class="sxs-lookup"><span data-stu-id="0cf90-118"><dt>**MIDDLE\_BUTTON** </dt></span></span> </dl> | <span data-ttu-id="0cf90-119">Была нажата средняя кнопка мыши.</span><span class="sxs-lookup"><span data-stu-id="0cf90-119">The middle mouse button was pressed.</span></span> <br/>  |



 

</dd> <dt>

<span data-ttu-id="0cf90-120">*шифткэй*</span><span class="sxs-lookup"><span data-stu-id="0cf90-120">*ShiftKey*</span></span> 
</dt> <dd>

<span data-ttu-id="0cf90-121">Член перечисления [**инкшифткэймодифиерфлагс**](/windows/desktop/api/msinkaut/ne-msinkaut-inkshiftkeymodifierflags) , указывающий, какие клавиши-модификаторы следует отменять во время события.</span><span class="sxs-lookup"><span data-stu-id="0cf90-121">A member of the [**InkShiftKeyModifierFlags**](/windows/desktop/api/msinkaut/ne-msinkaut-inkshiftkeymodifierflags) enumeration that indicates which modifier keys are depressed at the time of the event.</span></span>



| <span data-ttu-id="0cf90-122">Значение</span><span class="sxs-lookup"><span data-stu-id="0cf90-122">Value</span></span>                                                                                                                                                                                     | <span data-ttu-id="0cf90-123">Значение</span><span class="sxs-lookup"><span data-stu-id="0cf90-123">Meaning</span></span>                                                          |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------|
| <span id="IKM_Shift"></span><span id="ikm_shift"></span><span id="IKM_SHIFT"></span><dl> <span data-ttu-id="0cf90-124"><dt>**ИКМ \_ SHIFT**</dt></span><span class="sxs-lookup"><span data-stu-id="0cf90-124"><dt>**IKM\_Shift**</dt></span></span> </dl>             | <span data-ttu-id="0cf90-125">Указывает, что клавиша SHIFT использовалась как модификатор.</span><span class="sxs-lookup"><span data-stu-id="0cf90-125">Specifies that the SHIFT key was used as a modifier.</span></span> <br/> |
| <span id="IKM_Control_"></span><span id="ikm_control_"></span><span id="IKM_CONTROL_"></span><dl> <span data-ttu-id="0cf90-126"><dt>**ИКМ \_ Элемент управления**</dt></span><span class="sxs-lookup"><span data-stu-id="0cf90-126"><dt>**IKM\_Control** </dt></span></span> </dl> | <span data-ttu-id="0cf90-127">Указывает, что клавиша CTRL использовалась как модификатор.</span><span class="sxs-lookup"><span data-stu-id="0cf90-127">Specifies that the CTRL key was used as a modifier.</span></span> <br/>  |
| <span id="IKM_Alt_"></span><span id="ikm_alt_"></span><span id="IKM_ALT_"></span><dl> <span data-ttu-id="0cf90-128"><dt>**ИКМ \_ Alt**</dt></span><span class="sxs-lookup"><span data-stu-id="0cf90-128"><dt>**IKM\_Alt** </dt></span></span> </dl>                 | <span data-ttu-id="0cf90-129">Указывает, что клавиша ALT использовалась как модификатор.</span><span class="sxs-lookup"><span data-stu-id="0cf90-129">Specifies that the ALT key was used as a modifier.</span></span> <br/>   |



 

</dd> <dt>

<span data-ttu-id="0cf90-130">*ксмаусе*</span><span class="sxs-lookup"><span data-stu-id="0cf90-130">*xMouse*</span></span> 
</dt> <dd>

<span data-ttu-id="0cf90-131">Текущая Координата x (в пикселях) указателя мыши.</span><span class="sxs-lookup"><span data-stu-id="0cf90-131">The current x coordinate, in pixels, of the mouse pointer.</span></span>

</dd> <dt>

<span data-ttu-id="0cf90-132">*имаусе*</span><span class="sxs-lookup"><span data-stu-id="0cf90-132">*yMouse*</span></span> 
</dt> <dd>

<span data-ttu-id="0cf90-133">Текущая координата y (в пикселях) указателя мыши.</span><span class="sxs-lookup"><span data-stu-id="0cf90-133">The current y coordinate, in pixels, of the mouse pointer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0cf90-134">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="0cf90-134">Return value</span></span>

<span data-ttu-id="0cf90-135">Если это событие завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="0cf90-135">If this event succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="0cf90-136">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="0cf90-136">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="0cf90-137">Комментарии</span><span class="sxs-lookup"><span data-stu-id="0cf90-137">Remarks</span></span>

<span data-ttu-id="0cf90-138">При нажатии кнопки мыши в тот момент, когда указатель наведен на элемент управления [InkEdit](inkedit-control-reference.md) , этот элемент управления захватывает мышь и получает все события мыши вплоть до последнего события [**MouseUp**](inkedit-mouseup.md) .</span><span class="sxs-lookup"><span data-stu-id="0cf90-138">If a mouse button is pressed while the pointer is over an [InkEdit](inkedit-control-reference.md) control, that control captures the mouse and receives all mouse events up to and including the last [**MouseUp**](inkedit-mouseup.md) event.</span></span> <span data-ttu-id="0cf90-139">Это означает, что координаты указателя мыши (x, y), возвращаемые событием мыши, могут не всегда находиться во внутренней области объекта, получающего их.</span><span class="sxs-lookup"><span data-stu-id="0cf90-139">This implies that the (x, y) mouse-pointer coordinates returned by a mouse event may not always be in the internal area of the object that receives them.</span></span>

<span data-ttu-id="0cf90-140">Если нажата кнопка мыши, объект, который захватывает указатель мыши после первого нажатия, получает все события мыши до тех пор, пока не будут сняты все кнопки.</span><span class="sxs-lookup"><span data-stu-id="0cf90-140">If mouse buttons are pressed in succession, the object that captures the mouse after the first press receives all mouse events until all buttons are released.</span></span>

<span data-ttu-id="0cf90-141">Этот метод события определен в интерфейсе **\_ иинкедитевентс** .</span><span class="sxs-lookup"><span data-stu-id="0cf90-141">This event method is defined in the **\_IInkEditEvents** interface.</span></span> <span data-ttu-id="0cf90-142">Интерфейс **\_ иинкедитевентс** реализует интерфейс [**IDISPATCH**](/windows/win32/api/oaidl/nn-oaidl-idispatch) с идентификатором DISPID \_ иимауседовн.</span><span class="sxs-lookup"><span data-stu-id="0cf90-142">The **\_IInkEditEvents** interface implements the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface with an identifier of DISPID\_IeeMouseDown.</span></span>

## <a name="requirements"></a><span data-ttu-id="0cf90-143">Требования</span><span class="sxs-lookup"><span data-stu-id="0cf90-143">Requirements</span></span>



| <span data-ttu-id="0cf90-144">Требование</span><span class="sxs-lookup"><span data-stu-id="0cf90-144">Requirement</span></span> | <span data-ttu-id="0cf90-145">Значение</span><span class="sxs-lookup"><span data-stu-id="0cf90-145">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0cf90-146">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="0cf90-146">Minimum supported client</span></span><br/> | <span data-ttu-id="0cf90-147">Только классические приложения Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="0cf90-147">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="0cf90-148">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="0cf90-148">Minimum supported server</span></span><br/> | <span data-ttu-id="0cf90-149">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="0cf90-149">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="0cf90-150">Header</span><span class="sxs-lookup"><span data-stu-id="0cf90-150">Header</span></span><br/>                   | <dl> <span data-ttu-id="0cf90-151"><dt>«С». h (также требует \_ ввода i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="0cf90-151"><dt>Inked.h (also requires inked\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="0cf90-152">Библиотека</span><span class="sxs-lookup"><span data-stu-id="0cf90-152">Library</span></span><br/>                  | <dl> <span data-ttu-id="0cf90-153"><dt>InkEd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0cf90-153"><dt>InkEd.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="0cf90-154">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="0cf90-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0cf90-155">InkEdit</span><span class="sxs-lookup"><span data-stu-id="0cf90-155">InkEdit</span></span>](inkedit-control-reference.md)
</dt> <dt>

[<span data-ttu-id="0cf90-156">**Перечисление Инкмаусебуттон**</span><span class="sxs-lookup"><span data-stu-id="0cf90-156">**InkMouseButton Enumeration**</span></span>](/windows/desktop/api/msinkaut/ne-msinkaut-inkmousebutton)
</dt> <dt>

[<span data-ttu-id="0cf90-157">**Перечисление Инкшифткэймодифиерфлагс**</span><span class="sxs-lookup"><span data-stu-id="0cf90-157">**InkShiftKeyModifierFlags Enumeration**</span></span>](/windows/desktop/api/msinkaut/ne-msinkaut-inkshiftkeymodifierflags)
</dt> <dt>

<span data-ttu-id="0cf90-158">[**\[Элемент управления InkEdit для события MouseMove\]**](inkedit-mousemove.md)</span><span class="sxs-lookup"><span data-stu-id="0cf90-158">[**MouseMove Event \[InkEdit Control\]**](inkedit-mousemove.md)</span></span>
</dt> <dt>

<span data-ttu-id="0cf90-159">[**\[Элемент управления InkEdit события MouseUp\]**](inkedit-mouseup.md)</span><span class="sxs-lookup"><span data-stu-id="0cf90-159">[**MouseUp Event \[InkEdit Control\]**](inkedit-mouseup.md)</span></span>
</dt> </dl>

 

