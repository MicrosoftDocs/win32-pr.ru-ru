---
description: Происходит при распознавании жеста конкретного приложения.
ms.assetid: a20f2d78-6cfe-4755-968e-91369021db1b
title: Событие InkPicture. жест (Мсинкаут. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 94581369554b4aef16530c9ddc8b3fd1a31ad861
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105693460"
---
# <a name="inkpicturegesture-event"></a><span data-ttu-id="a1063-103">Событие InkPicture. жест</span><span class="sxs-lookup"><span data-stu-id="a1063-103">InkPicture.Gesture event</span></span>

<span data-ttu-id="a1063-104">Происходит при распознавании *жеста* конкретного приложения.</span><span class="sxs-lookup"><span data-stu-id="a1063-104">Occurs when an application-specific *gesture* is recognized.</span></span>

## <a name="syntax"></a><span data-ttu-id="a1063-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a1063-105">Syntax</span></span>


```C++
void Gesture(
  [in]      IInkCursor   *Cursor,
  [in]      IInkStrokes  *Strokes,
  [in]      VARIANT      Gestures,
  [in, out] VARIANT_BOOL *Cancel
);
```



## <a name="parameters"></a><span data-ttu-id="a1063-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="a1063-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a1063-107">*Курсор* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="a1063-107">*Cursor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a1063-108">Объект [**иинккурсор**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) , создавший событие **жеста** .</span><span class="sxs-lookup"><span data-stu-id="a1063-108">The [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) object that generated the **Gesture** event.</span></span>

</dd> <dt>

<span data-ttu-id="a1063-109">*Штрихи* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="a1063-109">*Strokes* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a1063-110">Коллекция [иинкстрокес](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) , которую распознаватель вернул в качестве жеста.</span><span class="sxs-lookup"><span data-stu-id="a1063-110">The [IInkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) collection that the recognizer returned as the gesture.</span></span>

</dd> <dt>

<span data-ttu-id="a1063-111">*Жесты* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="a1063-111">*Gestures* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a1063-112">Массив объектов [**иинкжестуре**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkgesture) (в порядке уверенности) от распознавателя.</span><span class="sxs-lookup"><span data-stu-id="a1063-112">An array of [**IInkGesture**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkgesture) objects, in order of confidence, from the recognizer.</span></span>

<span data-ttu-id="a1063-113">Дополнительные сведения о структуре вариантов см. в разделе [Использование библиотеки COM](using-the-com-library.md).</span><span class="sxs-lookup"><span data-stu-id="a1063-113">For more information about the VARIANT structure, see [Using the COM Library](using-the-com-library.md).</span></span>

</dd> <dt>

<span data-ttu-id="a1063-114">*Отмена* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="a1063-114">*Cancel* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="a1063-115">**Вариант \_ Значение TRUE** , если это событие должно быть отменено, например не стереть рукописные данные и инициировать событие [**Stroke**](inkpicture-stroke.md) .</span><span class="sxs-lookup"><span data-stu-id="a1063-115">**VARIANT\_TRUE** if this event should be cancelled, such as not to erase the ink and to fire the [**Stroke**](inkpicture-stroke.md) event.</span></span> <span data-ttu-id="a1063-116">В противном случае — **\_ значение false**.</span><span class="sxs-lookup"><span data-stu-id="a1063-116">Otherwise, **VARIANT\_FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a1063-117">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="a1063-117">Return value</span></span>

<span data-ttu-id="a1063-118">Это событие не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="a1063-118">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="a1063-119">Комментарии</span><span class="sxs-lookup"><span data-stu-id="a1063-119">Remarks</span></span>

<span data-ttu-id="a1063-120">Этот метод события определен в интерфейсах диспетчеризации (DISP) **\_ иинкколлекторевентс**, **\_ иинковерлайевентс** и **\_ иинкпиктуривентс** с идентификатором DISPID \_ ицежестуре.</span><span class="sxs-lookup"><span data-stu-id="a1063-120">This event method is defined in the **\_IInkCollectorEvents**, **\_IInkOverlayEvents**, and **\_IInkPictureEvents** dispatch-only interfaces (dispinterfaces) with an ID of DISPID\_ICEGesture.</span></span>

<span data-ttu-id="a1063-121">Если свойство [**режиме CollectionMode**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_collectionmode) имеет значение [**жестуреонли**](/windows/desktop/api/msinkaut/ne-msinkaut-inkcollectionmode), время ожидания между добавлением пользователем жеста и событием **жеста** является фиксированным значением, которое нельзя изменить программными средствами.</span><span class="sxs-lookup"><span data-stu-id="a1063-121">When the [**CollectionMode**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_collectionmode) property is set to [**GestureOnly**](/windows/desktop/api/msinkaut/ne-msinkaut-inkcollectionmode), the timeout between when a user adds a gesture and when the **Gesture** event occurs is a fixed value that you cannot alter programmatically.</span></span> <span data-ttu-id="a1063-122">Распознавание жестов выполняется быстрее в режиме **инканджестуре** .</span><span class="sxs-lookup"><span data-stu-id="a1063-122">Gesture recognition is faster in **InkAndGesture** mode.</span></span>

<span data-ttu-id="a1063-123">Чтобы предотвратить сбор рукописных данных в режиме [**инканджестуре**](/windows/desktop/api/msinkaut/ne-msinkaut-inkcollectionmode) :</span><span class="sxs-lookup"><span data-stu-id="a1063-123">To prevent the collection of ink while in [**InkAndGesture**](/windows/desktop/api/msinkaut/ne-msinkaut-inkcollectionmode) mode:</span></span>

-   <span data-ttu-id="a1063-124">Задайте для [**режиме CollectionMode**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_collectionmode) значение [**инканджестуре**](/windows/desktop/api/msinkaut/ne-msinkaut-inkcollectionmode).</span><span class="sxs-lookup"><span data-stu-id="a1063-124">Set [**CollectionMode**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_collectionmode) to [**InkAndGesture**](/windows/desktop/api/msinkaut/ne-msinkaut-inkcollectionmode).</span></span>
-   <span data-ttu-id="a1063-125">Удалите штрих в событии [**Stroke**](inkpicture-stroke.md) .</span><span class="sxs-lookup"><span data-stu-id="a1063-125">Delete the stroke in the [**Stroke**](inkpicture-stroke.md) event.</span></span>
-   <span data-ttu-id="a1063-126">Обработка жеста в событии **жеста** .</span><span class="sxs-lookup"><span data-stu-id="a1063-126">Process the gesture in the **Gesture** event.</span></span>

<span data-ttu-id="a1063-127">Чтобы предотвратить поток рукописного ввода во время жестуринг, задайте для свойства [**Динамикрендеринг**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_dynamicrendering) **значение false**.</span><span class="sxs-lookup"><span data-stu-id="a1063-127">To prevent the flow of ink while gesturing, set [**DynamicRendering**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_dynamicrendering) property to **FALSE**.</span></span>

<span data-ttu-id="a1063-128">В дополнение к вставке рукописного ввода событие **жеста** срабатывает в режиме выборки или стирания.</span><span class="sxs-lookup"><span data-stu-id="a1063-128">In addition to when inserting ink, the **Gesture** event is fired when in select or erase mode.</span></span> <span data-ttu-id="a1063-129">Вы несете ответственность за отслеживание режима редактирования и должны знать режим перед интерпретацией события.</span><span class="sxs-lookup"><span data-stu-id="a1063-129">You are responsible for tracking the editing mode and should be aware of the mode before interpreting the event.</span></span>

> [!Note]  
> <span data-ttu-id="a1063-130">Для распознавания жестов необходимо использовать объект или элемент управления, который может выполнять накопление рукописного ввода.</span><span class="sxs-lookup"><span data-stu-id="a1063-130">To recognize gestures, you must use an object or control that can collect ink.</span></span>

 

<span data-ttu-id="a1063-131">Жесты приложения определяются как жесты, поддерживаемые в приложении.</span><span class="sxs-lookup"><span data-stu-id="a1063-131">Application gestures are defined as gestures that are supported within your application.</span></span>

<span data-ttu-id="a1063-132">Чтобы это событие произошло, объект или элемент управления должен представлять интерес в наборе жестов приложения.</span><span class="sxs-lookup"><span data-stu-id="a1063-132">For this event to occur, the object or control must have interest in a set of application gestures.</span></span> <span data-ttu-id="a1063-133">Чтобы задать объекты или элементы управления, представляющие интерес в наборе жестов, вызовите метод [**сетжестурестатус**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-setgesturestatus) объекта или элемента управления.</span><span class="sxs-lookup"><span data-stu-id="a1063-133">To set the objects or controls interest in a set of gestures, call the [**SetGestureStatus**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-setgesturestatus) method of the object or control.</span></span>

<span data-ttu-id="a1063-134">Список специальных жестов приложения см. в описании типа перечисления [**инкаппликатионжестуре**](/windows/desktop/api/msinkaut/ne-msinkaut-inkapplicationgesture) .</span><span class="sxs-lookup"><span data-stu-id="a1063-134">For a list of specific application gestures, see the [**InkApplicationGesture**](/windows/desktop/api/msinkaut/ne-msinkaut-inkapplicationgesture) enumeration type.</span></span>

## <a name="requirements"></a><span data-ttu-id="a1063-135">Требования</span><span class="sxs-lookup"><span data-stu-id="a1063-135">Requirements</span></span>



| <span data-ttu-id="a1063-136">Требование</span><span class="sxs-lookup"><span data-stu-id="a1063-136">Requirement</span></span> | <span data-ttu-id="a1063-137">Значение</span><span class="sxs-lookup"><span data-stu-id="a1063-137">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a1063-138">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="a1063-138">Minimum supported client</span></span><br/> | <span data-ttu-id="a1063-139">Только классические приложения Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="a1063-139">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="a1063-140">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="a1063-140">Minimum supported server</span></span><br/> | <span data-ttu-id="a1063-141">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="a1063-141">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="a1063-142">Header</span><span class="sxs-lookup"><span data-stu-id="a1063-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="a1063-143"><dt>Мсинкаут. h (также требуется Мсинкаут \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="a1063-143"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="a1063-144">Библиотека</span><span class="sxs-lookup"><span data-stu-id="a1063-144">Library</span></span><br/>                  | <dl> <span data-ttu-id="a1063-145"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a1063-145"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="a1063-146">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a1063-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a1063-147">InkPicture</span><span class="sxs-lookup"><span data-stu-id="a1063-147">InkPicture</span></span>](inkpicture-control-reference.md)
</dt> <dt>

[<span data-ttu-id="a1063-148">**Перечисление Инкаппликатионжестуре**</span><span class="sxs-lookup"><span data-stu-id="a1063-148">**InkApplicationGesture Enumeration**</span></span>](/windows/desktop/api/msinkaut/ne-msinkaut-inkapplicationgesture)
</dt> <dt>

[<span data-ttu-id="a1063-149">**Метод Сетжестурестатус**</span><span class="sxs-lookup"><span data-stu-id="a1063-149">**SetGestureStatus Method**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-setgesturestatus)
</dt> <dt>

[<span data-ttu-id="a1063-150">Использование жестов</span><span class="sxs-lookup"><span data-stu-id="a1063-150">Using Gestures</span></span>](using-gestures.md)
</dt> </dl>

 

