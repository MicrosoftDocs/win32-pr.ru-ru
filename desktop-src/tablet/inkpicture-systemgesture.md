---
description: Происходит при распознавании системного жеста.
ms.assetid: 36e2ac5a-dc91-47c2-a8e5-e555437c0a5d
title: Событие InkPicture.SysТемжестуре (Мсинкаут. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 918198e4d18a854bb4238ce9d878dc70ab1f2f82
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105712977"
---
# <a name="inkpicturesystemgesture-event"></a><span data-ttu-id="801a8-103">Событие InkPicture.SysТемжестуре</span><span class="sxs-lookup"><span data-stu-id="801a8-103">InkPicture.SystemGesture event</span></span>

<span data-ttu-id="801a8-104">Происходит при распознавании системного жеста.</span><span class="sxs-lookup"><span data-stu-id="801a8-104">Occurs when a system gesture is recognized.</span></span>

## <a name="syntax"></a><span data-ttu-id="801a8-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="801a8-105">Syntax</span></span>


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



## <a name="parameters"></a><span data-ttu-id="801a8-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="801a8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="801a8-107">*Курсор* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="801a8-107">*Cursor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="801a8-108">Объект [**иинккурсор**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) , создавший событие **системжестуре** .</span><span class="sxs-lookup"><span data-stu-id="801a8-108">The [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) object that generated the **SystemGesture** event.</span></span>

</dd> <dt>

<span data-ttu-id="801a8-109">*Идентификатор* \[ в\]</span><span class="sxs-lookup"><span data-stu-id="801a8-109">*Id* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="801a8-110">Значение системного жеста.</span><span class="sxs-lookup"><span data-stu-id="801a8-110">The value of the system gesture.</span></span>

</dd> <dt>

<span data-ttu-id="801a8-111">*X* \[ в\]</span><span class="sxs-lookup"><span data-stu-id="801a8-111">*X* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="801a8-112">Координата по оси x расположения жеста.</span><span class="sxs-lookup"><span data-stu-id="801a8-112">The x-coordinate of the location of the gesture.</span></span>

</dd> <dt>

<span data-ttu-id="801a8-113">*Y* \[ в\]</span><span class="sxs-lookup"><span data-stu-id="801a8-113">*Y* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="801a8-114">Координата по оси y расположения жеста.</span><span class="sxs-lookup"><span data-stu-id="801a8-114">The y-coordinate of the location of the gesture.</span></span>

</dd> <dt>

<span data-ttu-id="801a8-115">*Модификатор* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="801a8-115">*Modifier* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="801a8-116">Зарезервировано.</span><span class="sxs-lookup"><span data-stu-id="801a8-116">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="801a8-117">*Символ* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="801a8-117">*Character* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="801a8-118">Зарезервировано.</span><span class="sxs-lookup"><span data-stu-id="801a8-118">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="801a8-119">*Курсормоде* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="801a8-119">*CursorMode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="801a8-120">Значение, указывающее, находится ли объект [**иинккурсор**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) в нормальном режиме или в режиме ластика.</span><span class="sxs-lookup"><span data-stu-id="801a8-120">A value that indicates whether the [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) object is in normal mode or eraser mode.</span></span> <span data-ttu-id="801a8-121">1 предназначен для обычного режима, а 2 — для режима стирания.</span><span class="sxs-lookup"><span data-stu-id="801a8-121">1 is for normal mode and 2 are for eraser mode.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="801a8-122">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="801a8-122">Return value</span></span>

<span data-ttu-id="801a8-123">Это событие не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="801a8-123">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="801a8-124">Комментарии</span><span class="sxs-lookup"><span data-stu-id="801a8-124">Remarks</span></span>

<span data-ttu-id="801a8-125">Системные жесты предоставляют сведения об объекте [**иинккурсор**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) , который используется для создания жеста.</span><span class="sxs-lookup"><span data-stu-id="801a8-125">System gestures give information about the [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) object that is being used to create the gesture.</span></span> <span data-ttu-id="801a8-126">Они также предоставляют сочетания клавиш для сочетания событий мыши и способы обнаружения событий мыши с меньшим влиянием на производительность.</span><span class="sxs-lookup"><span data-stu-id="801a8-126">They also provide shortcuts to combinations of mouse events and are ways to detect mouse events with less impact on performance.</span></span>

<span data-ttu-id="801a8-127">Например, вместо поиска пары событий «кнопка [**вверх события «вверх» \[ \] элемента**](inkpicture-mouseup.md)управления InkPicture / [**\[ \]**](inkpicture-mousedown.md) «кнопка вверх» с другими событиями мыши в промежутке между ними можно искать жесты в системе TAP или ригхттап.</span><span class="sxs-lookup"><span data-stu-id="801a8-127">For example, instead of looking for a [**MouseUp Event \[InkPicture Control\]**](inkpicture-mouseup.md)/[**MouseDown Event \[InkPicture Control\]**](inkpicture-mousedown.md) pair of events with no other mouse events occurring in between, you can look for the Tap or RightTap system gestures.</span></span>

<span data-ttu-id="801a8-128">В качестве другого примера вместо прослушивания события [**MouseDown \[ \]**](inkpicture-mousedown.md)для элемента управления / [**MouseMove \[ \]**](inkpicture-mousemove.md) Event InkPicture и получения многочисленных **\[ управляющих \] сообщений события MouseMove** можно наблюдать за системными жестами перетаскивания или ригхтдраг, если вы не заинтересованы в координатах (x, y) каждого положения мыши.</span><span class="sxs-lookup"><span data-stu-id="801a8-128">As another example, instead of listening for [**MouseDown Event \[InkPicture Control\]**](inkpicture-mousedown.md)/[**MouseMove Event \[InkPicture Control\]**](inkpicture-mousemove.md) events and getting numerous **MouseMove Event \[InkPicture Control\]** messages, you can watch for the Drag or RightDrag system gestures as long as you're not interested in the (x, y) coordinates of every position of the mouse.</span></span> <span data-ttu-id="801a8-129">Это позволяет получить только одно сообщение вместо многочисленных **\[ управляющих \] сообщений MouseMove Event InkPicture** .</span><span class="sxs-lookup"><span data-stu-id="801a8-129">This allows you to receive only one message instead of numerous **MouseMove Event \[InkPicture Control\]** messages.</span></span>

<span data-ttu-id="801a8-130">Список конкретных системных жестов см. в описании типа перечисления [**инксистемжестуре**](/windows/desktop/api/msinkaut/ne-msinkaut-inksystemgesture) .</span><span class="sxs-lookup"><span data-stu-id="801a8-130">For a list of specific system gestures, see the [**InkSystemGesture**](/windows/desktop/api/msinkaut/ne-msinkaut-inksystemgesture) enumeration type.</span></span> <span data-ttu-id="801a8-131">Дополнительные сведения о системных жестах см. в разделе [Использование жестов](using-gestures.md) и [входных данных команды на планшетном ПК](/previous-versions//dd314533(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="801a8-131">For more information about system gestures, see [Using Gestures](using-gestures.md) and [Command Input on the Tablet PC](/previous-versions//dd314533(v=vs.85)).</span></span>

<span data-ttu-id="801a8-132">Этот метод события определен в интерфейсах диспетчеризации (DISP) **\_ иинкколлекторевентс**, **\_ иинковерлайевентс** и **\_ иинкпиктуривентс** с идентификатором DISPID \_ ицесистемжестуре.</span><span class="sxs-lookup"><span data-stu-id="801a8-132">This event method is defined in the **\_IInkCollectorEvents**, **\_IInkOverlayEvents**, and **\_IInkPictureEvents** dispatch-only interfaces (dispinterfaces) with an ID of DISPID\_ICESystemGesture.</span></span>

## <a name="requirements"></a><span data-ttu-id="801a8-133">Требования</span><span class="sxs-lookup"><span data-stu-id="801a8-133">Requirements</span></span>



| <span data-ttu-id="801a8-134">Требование</span><span class="sxs-lookup"><span data-stu-id="801a8-134">Requirement</span></span> | <span data-ttu-id="801a8-135">Значение</span><span class="sxs-lookup"><span data-stu-id="801a8-135">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="801a8-136">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="801a8-136">Minimum supported client</span></span><br/> | <span data-ttu-id="801a8-137">Только классические приложения Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="801a8-137">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="801a8-138">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="801a8-138">Minimum supported server</span></span><br/> | <span data-ttu-id="801a8-139">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="801a8-139">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="801a8-140">Header</span><span class="sxs-lookup"><span data-stu-id="801a8-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="801a8-141"><dt>Мсинкаут. h (также требуется Мсинкаут \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="801a8-141"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="801a8-142">Библиотека</span><span class="sxs-lookup"><span data-stu-id="801a8-142">Library</span></span><br/>                  | <dl> <span data-ttu-id="801a8-143"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="801a8-143"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="801a8-144">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="801a8-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="801a8-145">InkPicture</span><span class="sxs-lookup"><span data-stu-id="801a8-145">InkPicture</span></span>](inkpicture-control-reference.md)
</dt> <dt>

[<span data-ttu-id="801a8-146">**Перечисление Инксистемжестуре**</span><span class="sxs-lookup"><span data-stu-id="801a8-146">**InkSystemGesture Enumeration**</span></span>](/windows/desktop/api/msinkaut/ne-msinkaut-inksystemgesture)
</dt> <dt>

[<span data-ttu-id="801a8-147">Использование жестов</span><span class="sxs-lookup"><span data-stu-id="801a8-147">Using Gestures</span></span>](using-gestures.md)
</dt> </dl>

 

