---
description: Событие InkCollector. жест — возникает при распознавании жеста конкретного приложения.
ms.assetid: 5830f7f8-2870-4194-ab3e-b63b71e97063
title: Событие InkCollector. жест (Мсинкаут. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0bfc2fea09060dbb206cd7681bcecfbedbc7a6b4
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108110192"
---
# <a name="inkcollectorgesture-event"></a><span data-ttu-id="d5566-103">Событие InkCollector. жест</span><span class="sxs-lookup"><span data-stu-id="d5566-103">InkCollector.Gesture event</span></span>

<span data-ttu-id="d5566-104">Происходит при распознавании жеста конкретного приложения.</span><span class="sxs-lookup"><span data-stu-id="d5566-104">Occurs when an application-specific gesture is recognized.</span></span>

## <a name="syntax"></a><span data-ttu-id="d5566-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d5566-105">Syntax</span></span>


```C++
void Gesture(
  [in]      IInkCursor   *Cursor,
  [in]      IInkStrokes  *Strokes,
  [in]      VARIANT      Gestures,
  [in, out] VARIANT_BOOL *Cancel
);
```



## <a name="parameters"></a><span data-ttu-id="d5566-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="d5566-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d5566-107">*Курсор* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="d5566-107">*Cursor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d5566-108">Объект [**иинккурсор**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) , создавший событие **жеста** .</span><span class="sxs-lookup"><span data-stu-id="d5566-108">The [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) object that generated the **Gesture** event.</span></span>

</dd> <dt>

<span data-ttu-id="d5566-109">*Штрихи* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="d5566-109">*Strokes* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d5566-110">Коллекция [иинкстрокес](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) , которую распознаватель вернул в качестве жеста.</span><span class="sxs-lookup"><span data-stu-id="d5566-110">The [IInkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) collection that the recognizer returned as the gesture.</span></span>

</dd> <dt>

<span data-ttu-id="d5566-111">*Жесты* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="d5566-111">*Gestures* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d5566-112">Массив объектов [**иинкжестуре**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkgesture) (в порядке уверенности) от распознавателя.</span><span class="sxs-lookup"><span data-stu-id="d5566-112">An array of [**IInkGesture**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkgesture) objects, in order of confidence, from the recognizer.</span></span>

<span data-ttu-id="d5566-113">Дополнительные сведения о структуре вариантов см. в разделе [Использование библиотеки COM](using-the-com-library.md).</span><span class="sxs-lookup"><span data-stu-id="d5566-113">For more information about the VARIANT structure, see [Using the COM Library](using-the-com-library.md).</span></span>

</dd> <dt>

<span data-ttu-id="d5566-114">*Отмена* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="d5566-114">*Cancel* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="d5566-115">**Вариант \_ Значение TRUE** , если этот жест следует отменить; в противном случае — **\_ значение false**.</span><span class="sxs-lookup"><span data-stu-id="d5566-115">**VARIANT\_TRUE** if this gesture should be cancelled; otherwise, **VARIANT\_FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d5566-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="d5566-116">Return value</span></span>

<span data-ttu-id="d5566-117">Это событие не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="d5566-117">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="d5566-118">Remarks</span><span class="sxs-lookup"><span data-stu-id="d5566-118">Remarks</span></span>

<span data-ttu-id="d5566-119">Этот метод события определен в \_ \_ \_ интерфейсах диспетчеризации (DISP) иинкколлекторевентс, иинковерлайевентс и иинкпиктуривентс с идентификатором DISPID \_ ицежестуре.</span><span class="sxs-lookup"><span data-stu-id="d5566-119">This event method is defined in the \_IInkCollectorEvents, \_IInkOverlayEvents, and \_IInkPictureEvents dispatch-only interfaces (dispinterfaces) with an ID of DISPID\_ICEGesture.</span></span>

<span data-ttu-id="d5566-120">Если свойство [**режиме CollectionMode**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_collectionmode) имеет значение [**жестуреонли**](/windows/desktop/api/msinkaut/ne-msinkaut-inkcollectionmode), время ожидания между добавлением пользователем жеста и событием **жеста** является фиксированным значением, которое нельзя изменить программными средствами.</span><span class="sxs-lookup"><span data-stu-id="d5566-120">When the [**CollectionMode**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_collectionmode) property is set to [**GestureOnly**](/windows/desktop/api/msinkaut/ne-msinkaut-inkcollectionmode), the timeout between when a user adds a gesture and when the **Gesture** event occurs is a fixed value that you cannot alter programmatically.</span></span> <span data-ttu-id="d5566-121">Распознавание жестов выполняется быстрее в режиме **инканджестуре** .</span><span class="sxs-lookup"><span data-stu-id="d5566-121">Gesture recognition is faster in **InkAndGesture** mode.</span></span>

<span data-ttu-id="d5566-122">Чтобы предотвратить сбор рукописных данных в режиме [**инканджестуре**](/windows/desktop/api/msinkaut/ne-msinkaut-inkcollectionmode) :</span><span class="sxs-lookup"><span data-stu-id="d5566-122">To prevent the collection of ink while in [**InkAndGesture**](/windows/desktop/api/msinkaut/ne-msinkaut-inkcollectionmode) mode:</span></span>

-   <span data-ttu-id="d5566-123">Задайте для [**режиме CollectionMode**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_collectionmode) значение [**инканджестуре**](/windows/desktop/api/msinkaut/ne-msinkaut-inkcollectionmode).</span><span class="sxs-lookup"><span data-stu-id="d5566-123">Set [**CollectionMode**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_collectionmode) to [**InkAndGesture**](/windows/desktop/api/msinkaut/ne-msinkaut-inkcollectionmode).</span></span>
-   <span data-ttu-id="d5566-124">Удалите штрих в событии [**Stroke**](inkcollector-stroke.md) .</span><span class="sxs-lookup"><span data-stu-id="d5566-124">Delete the stroke in the [**Stroke**](inkcollector-stroke.md) event.</span></span>
-   <span data-ttu-id="d5566-125">Обработка жеста в событии **жеста** .</span><span class="sxs-lookup"><span data-stu-id="d5566-125">Process the gesture in the **Gesture** event.</span></span>

<span data-ttu-id="d5566-126">Чтобы предотвратить поток рукописного ввода во время жестуринг, задайте для свойства [**Динамикрендеринг**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_dynamicrendering) **значение false**.</span><span class="sxs-lookup"><span data-stu-id="d5566-126">To prevent the flow of ink while gesturing, set [**DynamicRendering**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_dynamicrendering) property to **FALSE**.</span></span>

<span data-ttu-id="d5566-127">В дополнение к вставке рукописного ввода событие **жеста** срабатывает в режиме выборки или стирания.</span><span class="sxs-lookup"><span data-stu-id="d5566-127">In addition to when inserting ink, the **Gesture** event is fired when in select or erase mode.</span></span> <span data-ttu-id="d5566-128">Вы несете ответственность за отслеживание режима редактирования и должны знать режим перед интерпретацией события.</span><span class="sxs-lookup"><span data-stu-id="d5566-128">You are responsible for tracking the editing mode and should be aware of the mode before interpreting the event.</span></span>

> [!Note]  
> <span data-ttu-id="d5566-129">Для распознавания жестов необходимо использовать объект или элемент управления, который может выполнять накопление рукописного ввода.</span><span class="sxs-lookup"><span data-stu-id="d5566-129">To recognize gestures, you must use an object or control that can collect ink.</span></span>

 

<span data-ttu-id="d5566-130">Жесты приложения определяются как жесты, поддерживаемые в приложении.</span><span class="sxs-lookup"><span data-stu-id="d5566-130">Application gestures are defined as gestures that are supported within your application.</span></span>

<span data-ttu-id="d5566-131">Чтобы это событие произошло, объект или элемент управления должен представлять интерес в наборе жестов приложения.</span><span class="sxs-lookup"><span data-stu-id="d5566-131">For this event to occur, the object or control must have interest in a set of application gestures.</span></span> <span data-ttu-id="d5566-132">Чтобы задать объекты или элементы управления, представляющие интерес в наборе жестов, вызовите метод [**сетжестурестатус**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-setgesturestatus) объекта или элемента управления.</span><span class="sxs-lookup"><span data-stu-id="d5566-132">To set the objects or controls interest in a set of gestures, call the [**SetGestureStatus**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-setgesturestatus) method of the object or control.</span></span>

<span data-ttu-id="d5566-133">Список специальных жестов приложения см. в описании типа перечисления [**инкаппликатионжестуре**](/windows/desktop/api/msinkaut/ne-msinkaut-inkapplicationgesture) .</span><span class="sxs-lookup"><span data-stu-id="d5566-133">For a list of specific application gestures, see the [**InkApplicationGesture**](/windows/desktop/api/msinkaut/ne-msinkaut-inkapplicationgesture) enumeration type.</span></span>

## <a name="requirements"></a><span data-ttu-id="d5566-134">Требования</span><span class="sxs-lookup"><span data-stu-id="d5566-134">Requirements</span></span>



| <span data-ttu-id="d5566-135">Требование</span><span class="sxs-lookup"><span data-stu-id="d5566-135">Requirement</span></span> | <span data-ttu-id="d5566-136">Значение</span><span class="sxs-lookup"><span data-stu-id="d5566-136">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d5566-137">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="d5566-137">Minimum supported client</span></span><br/> | <span data-ttu-id="d5566-138">Только классические приложения Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="d5566-138">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="d5566-139">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="d5566-139">Minimum supported server</span></span><br/> | <span data-ttu-id="d5566-140">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="d5566-140">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="d5566-141">Header</span><span class="sxs-lookup"><span data-stu-id="d5566-141">Header</span></span><br/>                   | <dl> <span data-ttu-id="d5566-142"><dt>Мсинкаут. h (также требуется Мсинкаут \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="d5566-142"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="d5566-143">Библиотека</span><span class="sxs-lookup"><span data-stu-id="d5566-143">Library</span></span><br/>                  | <dl> <span data-ttu-id="d5566-144"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d5566-144"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="d5566-145">См. также</span><span class="sxs-lookup"><span data-stu-id="d5566-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d5566-146">**Класс InkCollector**</span><span class="sxs-lookup"><span data-stu-id="d5566-146">**InkCollector Class**</span></span>](inkcollector-class.md)
</dt> <dt>

[<span data-ttu-id="d5566-147">**Перечисление Инкаппликатионжестуре**</span><span class="sxs-lookup"><span data-stu-id="d5566-147">**InkApplicationGesture Enumeration**</span></span>](/windows/desktop/api/msinkaut/ne-msinkaut-inkapplicationgesture)
</dt> <dt>

[<span data-ttu-id="d5566-148">**Метод Сетжестурестатус**</span><span class="sxs-lookup"><span data-stu-id="d5566-148">**SetGestureStatus Method**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-setgesturestatus)
</dt> <dt>

[<span data-ttu-id="d5566-149">Использование жестов</span><span class="sxs-lookup"><span data-stu-id="d5566-149">Using Gestures</span></span>](using-gestures.md)
</dt> </dl>

 

