---
description: Происходит при распознавании системного жеста.
ms.assetid: 6f82b234-2088-4207-a6b4-6c6919623d6a
title: Событие InkOverlay.SysТемжестуре (Мсинкаут. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 79b1e6ac7c02bc308856a89043bc0b1824b0fab5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105647411"
---
# <a name="inkoverlaysystemgesture-event"></a><span data-ttu-id="7b5d5-103">Событие InkOverlay.SysТемжестуре</span><span class="sxs-lookup"><span data-stu-id="7b5d5-103">InkOverlay.SystemGesture event</span></span>

<span data-ttu-id="7b5d5-104">Происходит при распознавании системного жеста.</span><span class="sxs-lookup"><span data-stu-id="7b5d5-104">Occurs when a system gesture is recognized.</span></span>

## <a name="syntax"></a><span data-ttu-id="7b5d5-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="7b5d5-105">Syntax</span></span>


```C++
void SystemGesture(
  [in] IInkCursor       *Cursor,
  [in] InkSystemGesture Id,
  [in] long             X,
  [in] long             Y,
  [in] long             Modifier,
  [in] BSTR             Character,
  [in] long             CursorMode
);
```



## <a name="parameters"></a><span data-ttu-id="7b5d5-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="7b5d5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7b5d5-107">*Курсор* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="7b5d5-107">*Cursor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7b5d5-108">Объект [**иинккурсор**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) , создавший событие [**системжестуре**](inkcollector-systemgesture.md) .</span><span class="sxs-lookup"><span data-stu-id="7b5d5-108">The [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) object that generated the [**SystemGesture**](inkcollector-systemgesture.md) event.</span></span>

</dd> <dt>

<span data-ttu-id="7b5d5-109">*Идентификатор* \[ в\]</span><span class="sxs-lookup"><span data-stu-id="7b5d5-109">*Id* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7b5d5-110">Значение системного жеста.</span><span class="sxs-lookup"><span data-stu-id="7b5d5-110">The value of the system gesture.</span></span>

</dd> <dt>

<span data-ttu-id="7b5d5-111">*X* \[ в\]</span><span class="sxs-lookup"><span data-stu-id="7b5d5-111">*X* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7b5d5-112">Координата по оси x расположения жеста.</span><span class="sxs-lookup"><span data-stu-id="7b5d5-112">The x-coordinate of the location of the gesture.</span></span>

</dd> <dt>

<span data-ttu-id="7b5d5-113">*Y* \[ в\]</span><span class="sxs-lookup"><span data-stu-id="7b5d5-113">*Y* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7b5d5-114">Координата по оси y расположения жеста.</span><span class="sxs-lookup"><span data-stu-id="7b5d5-114">The y-coordinate of the location of the gesture.</span></span>

</dd> <dt>

<span data-ttu-id="7b5d5-115">*Модификатор* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="7b5d5-115">*Modifier* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7b5d5-116">Зарезервировано.</span><span class="sxs-lookup"><span data-stu-id="7b5d5-116">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="7b5d5-117">*Символ* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="7b5d5-117">*Character* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7b5d5-118">Зарезервировано.</span><span class="sxs-lookup"><span data-stu-id="7b5d5-118">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="7b5d5-119">*Курсормоде* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="7b5d5-119">*CursorMode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7b5d5-120">Значение, указывающее, находится ли объект [**иинккурсор**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) в нормальном режиме или в режиме ластика.</span><span class="sxs-lookup"><span data-stu-id="7b5d5-120">A value that indicates whether the [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) object is in normal mode or eraser mode.</span></span> <span data-ttu-id="7b5d5-121">1 предназначен для обычного режима, а 2 — для режима стирания.</span><span class="sxs-lookup"><span data-stu-id="7b5d5-121">1 is for normal mode and 2 are for eraser mode.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7b5d5-122">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="7b5d5-122">Return value</span></span>

<span data-ttu-id="7b5d5-123">Это событие не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="7b5d5-123">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="7b5d5-124">Комментарии</span><span class="sxs-lookup"><span data-stu-id="7b5d5-124">Remarks</span></span>

<span data-ttu-id="7b5d5-125">Системные жесты полезны, поскольку они предоставляют сведения об объекте [**иинккурсор**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) , который используется для создания жеста.</span><span class="sxs-lookup"><span data-stu-id="7b5d5-125">System gestures are useful because they give information about the [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) object that is being used to create the gesture.</span></span> <span data-ttu-id="7b5d5-126">Они также предоставляют сочетания клавиш для сочетаний событий мыши и являются «более дешевыми» способами обнаружения событий мыши.</span><span class="sxs-lookup"><span data-stu-id="7b5d5-126">They also provide shortcuts to combinations of mouse events and are "cheaper" ways to detect mouse events.</span></span>

<span data-ttu-id="7b5d5-127">Например, вместо поиска пары событий [**MouseUp Event**](inkcollector-mouseup.md)  /  [**MouseDown**](inkcollector-mousedown.md) без других событий мыши в между ними можно найти системные жесты [**TAP**](/windows/desktop/api/msinkaut/ne-msinkaut-inksystemgesture) или **ригхттап** .</span><span class="sxs-lookup"><span data-stu-id="7b5d5-127">For example, instead of looking for a [**MouseUp Event**](inkcollector-mouseup.md) / [**MouseDown Event**](inkcollector-mousedown.md) pair of events with no other mouse events occurring in between, you can look for the [**Tap**](/windows/desktop/api/msinkaut/ne-msinkaut-inksystemgesture) or **RightTap** system gestures.</span></span>

<span data-ttu-id="7b5d5-128">В качестве другого примера, вместо прослушивания событий [**MouseDown**](inkcollector-mousedown.md)Event  /  [**MouseMove**](inkcollector-mousemove.md) и получения многочисленных сообщений о **событиях MouseMove** , можно наблюдать за системными жестами [**перетаскивания**](/windows/desktop/api/msinkaut/ne-msinkaut-inksystemgesture) или **ригхтдраг** , если вы не заинтересованы в координатах (x, y) каждого положения мыши.</span><span class="sxs-lookup"><span data-stu-id="7b5d5-128">As another example, instead of listening for [**MouseDown Event**](inkcollector-mousedown.md) / [**MouseMove Event**](inkcollector-mousemove.md) events and getting numerous **MouseMove Event** messages, you can watch for the [**Drag**](/windows/desktop/api/msinkaut/ne-msinkaut-inksystemgesture) or **RightDrag** system gestures as long as you're not interested in the (x, y) coordinates of every position of the mouse.</span></span> <span data-ttu-id="7b5d5-129">Это позволяет получить только одно сообщение вместо многочисленных сообщений о **событиях MouseMove** .</span><span class="sxs-lookup"><span data-stu-id="7b5d5-129">This allows you to receive only one message instead of numerous **MouseMove Event** messages.</span></span>

<span data-ttu-id="7b5d5-130">Список конкретных системных жестов см. в описании типа перечисления [**инксистемжестуре**](/windows/desktop/api/msinkaut/ne-msinkaut-inksystemgesture) .</span><span class="sxs-lookup"><span data-stu-id="7b5d5-130">For a list of specific system gestures, see the [**InkSystemGesture**](/windows/desktop/api/msinkaut/ne-msinkaut-inksystemgesture) enumeration type.</span></span> <span data-ttu-id="7b5d5-131">Дополнительные сведения о системных жестах см. в разделе [Использование жестов](using-gestures.md) и [входных данных команды на планшетном ПК](/previous-versions//dd314533(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="7b5d5-131">For more information about system gestures, see [Using Gestures](using-gestures.md) and [Command Input on the Tablet PC](/previous-versions//dd314533(v=vs.85)).</span></span>

<span data-ttu-id="7b5d5-132">Этот метод события определен в \_ \_ \_ интерфейсах диспетчеризации (DISP) иинкколлекторевентс, иинковерлайевентс и иинкпиктуривентс с идентификатором DISPID \_ ицесистемжестуре.</span><span class="sxs-lookup"><span data-stu-id="7b5d5-132">This event method is defined in the \_IInkCollectorEvents, \_IInkOverlayEvents, and \_IInkPictureEvents dispatch-only interfaces (dispinterfaces) with an ID of DISPID\_ICESystemGesture.</span></span>

## <a name="requirements"></a><span data-ttu-id="7b5d5-133">Требования</span><span class="sxs-lookup"><span data-stu-id="7b5d5-133">Requirements</span></span>



| <span data-ttu-id="7b5d5-134">Требование</span><span class="sxs-lookup"><span data-stu-id="7b5d5-134">Requirement</span></span> | <span data-ttu-id="7b5d5-135">Значение</span><span class="sxs-lookup"><span data-stu-id="7b5d5-135">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7b5d5-136">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="7b5d5-136">Minimum supported client</span></span><br/> | <span data-ttu-id="7b5d5-137">Только классические приложения Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="7b5d5-137">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="7b5d5-138">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="7b5d5-138">Minimum supported server</span></span><br/> | <span data-ttu-id="7b5d5-139">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="7b5d5-139">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="7b5d5-140">Header</span><span class="sxs-lookup"><span data-stu-id="7b5d5-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="7b5d5-141"><dt>Мсинкаут. h (также требуется Мсинкаут \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="7b5d5-141"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="7b5d5-142">Библиотека</span><span class="sxs-lookup"><span data-stu-id="7b5d5-142">Library</span></span><br/>                  | <dl> <span data-ttu-id="7b5d5-143"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7b5d5-143"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="7b5d5-144">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="7b5d5-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7b5d5-145">**Класс InkOverlay**</span><span class="sxs-lookup"><span data-stu-id="7b5d5-145">**InkOverlay Class**</span></span>](inkoverlay-class.md)
</dt> <dt>

[<span data-ttu-id="7b5d5-146">**Перечисление Инксистемжестуре**</span><span class="sxs-lookup"><span data-stu-id="7b5d5-146">**InkSystemGesture Enumeration**</span></span>](/windows/desktop/api/msinkaut/ne-msinkaut-inksystemgesture)
</dt> <dt>

[<span data-ttu-id="7b5d5-147">**Интерфейс Иинккурсор**</span><span class="sxs-lookup"><span data-stu-id="7b5d5-147">**IInkCursor Interface**</span></span>](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor)
</dt> <dt>

[<span data-ttu-id="7b5d5-148">Использование жестов</span><span class="sxs-lookup"><span data-stu-id="7b5d5-148">Using Gestures</span></span>](using-gestures.md)
</dt> <dt>

[<span data-ttu-id="7b5d5-149">Ввод, ввод и распознавание с помощью пера</span><span class="sxs-lookup"><span data-stu-id="7b5d5-149">Pen Input, Ink, and Recognition</span></span>](pen-input--ink--and-recognition.md)
</dt> <dt>

<span data-ttu-id="7b5d5-150">[Ввод команды на планшетном ПК](/previous-versions//dd314533(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="7b5d5-150">[Command Input on the Tablet PC](/previous-versions//dd314533(v=vs.85))</span></span>
</dt> </dl>

 

