---
description: Происходит при распознавании жеста приложения.
ms.assetid: 736715f4-c610-42cc-9fbb-c2b579da69e5
title: Событие InkEdit. жеста (with. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a61f4fce033672fde8cc4d74dced727fe60b7f97
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104265073"
---
# <a name="inkeditgesture-event"></a><span data-ttu-id="9a251-103">Событие InkEdit. жест</span><span class="sxs-lookup"><span data-stu-id="9a251-103">InkEdit.Gesture event</span></span>

<span data-ttu-id="9a251-104">Происходит при распознавании жеста приложения.</span><span class="sxs-lookup"><span data-stu-id="9a251-104">Occurs when an application gesture is recognized.</span></span>

## <a name="syntax"></a><span data-ttu-id="9a251-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="9a251-105">Syntax</span></span>


```C++
HRESULT Gesture(
  [in]      IInkCursor   *Cursor,
  [in]      IInkStrokes  *Strokes,
  [in]      VARIANT      Gestures,
  [in, out] VARIANT_BOOL *Cancel
);
```



## <a name="parameters"></a><span data-ttu-id="9a251-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="9a251-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9a251-107">*Курсор* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="9a251-107">*Cursor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9a251-108">Объект [**иинккурсор**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) , который использовался для создания этого жеста.</span><span class="sxs-lookup"><span data-stu-id="9a251-108">The [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) object that was used to create this gesture.</span></span>

</dd> <dt>

<span data-ttu-id="9a251-109">*Штрихи* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="9a251-109">*Strokes* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9a251-110">Коллекция [инкстрокес](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) , содержащая объекты [**иинкстрокедисп**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) , которые составляют этот жест.</span><span class="sxs-lookup"><span data-stu-id="9a251-110">The [InkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) collection that contains the [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) objects that make up this gesture.</span></span>

</dd> <dt>

<span data-ttu-id="9a251-111">*Жесты* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="9a251-111">*Gestures* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9a251-112">Массив объектов [**иинкжестуре**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkgesture) в порядке уверенности.</span><span class="sxs-lookup"><span data-stu-id="9a251-112">An array of [**IInkGesture**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkgesture) objects, in order of confidence.</span></span>

<span data-ttu-id="9a251-113">Дополнительные сведения о структуре вариантов см. в разделе [Использование библиотеки COM](using-the-com-library.md).</span><span class="sxs-lookup"><span data-stu-id="9a251-113">For more information about the VARIANT structure, see [Using the COM Library](using-the-com-library.md).</span></span>

</dd> <dt>

<span data-ttu-id="9a251-114">*Отмена* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="9a251-114">*Cancel* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="9a251-115">Следует ли отменять коллекцию [инкстрокес](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) , составляющую этот жест, и не стирать рукописные данные и вызывать событие [**Stroke**](inkedit-stroke.md) .</span><span class="sxs-lookup"><span data-stu-id="9a251-115">Whether the [InkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) collection that makes up this gesture should be canceled, so as not to erase the ink and to fire the [**Stroke**](inkedit-stroke.md) event.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9a251-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="9a251-116">Return value</span></span>

<span data-ttu-id="9a251-117">Если это событие завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="9a251-117">If this event succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="9a251-118">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="9a251-118">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="9a251-119">Комментарии</span><span class="sxs-lookup"><span data-stu-id="9a251-119">Remarks</span></span>

<span data-ttu-id="9a251-120">Этот метод события определен в интерфейсе **\_ иинкедитевентс** .</span><span class="sxs-lookup"><span data-stu-id="9a251-120">This event method is defined in the **\_IInkEditEvents** interface.</span></span> <span data-ttu-id="9a251-121">Интерфейс **\_ иинкедитевентс** реализует интерфейс IDispatch с идентификатором DISPID \_ иижестуре.</span><span class="sxs-lookup"><span data-stu-id="9a251-121">The **\_IInkEditEvents** interface implements the IDispatch interface with an identifier of DISPID\_IeeGesture.</span></span>

<span data-ttu-id="9a251-122">Событие **жеста** создается только в том случае, если [**Иинкстрокедисп**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) для объекта [**иинкжестуре**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkgesture) является первым объектом **иинкстрокедисп** с момента последнего вызова метода [**Recognize**](/windows/desktop/api/inked/nf-inked-iinkedit-recognize) или последнего срабатывания времени ожидания распознавания.</span><span class="sxs-lookup"><span data-stu-id="9a251-122">A **Gesture** event is raised only if the [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) for the [**IInkGesture**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkgesture) object is the first **IInkStrokeDisp** object since the last call to the [**Recognize**](/windows/desktop/api/inked/nf-inked-iinkedit-recognize) method or the last firing of the recognition timeout.</span></span>

<span data-ttu-id="9a251-123">Если событие **жеста** отменено, то для коллекции [инкстрокес](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) , вызвавшей событие **жеста** , возникает событие [**Stroke**](inkedit-stroke.md) .</span><span class="sxs-lookup"><span data-stu-id="9a251-123">If the **Gesture** event is canceled, the [**Stroke**](inkedit-stroke.md) event is raised for the [InkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) collection that raised the **Gesture** event.</span></span>

<span data-ttu-id="9a251-124">Чтобы это событие произошло, элемент управления [InkEdit](inkedit-control-reference.md) должен подписываться на набор жестов приложения.</span><span class="sxs-lookup"><span data-stu-id="9a251-124">For this event to occur, the [InkEdit](inkedit-control-reference.md) control must subscribe to a set of application gestures.</span></span> <span data-ttu-id="9a251-125">Чтобы задать интерес к элементу управления InkEdit в наборе жестов, вызовите метод [**сетжестурестатус**](/windows/desktop/api/inked/nf-inked-iinkedit-setgesturestatus) .</span><span class="sxs-lookup"><span data-stu-id="9a251-125">To set the InkEdit control's interest in a set of gestures, call the [**SetGestureStatus**](/windows/desktop/api/inked/nf-inked-iinkedit-setgesturestatus) method.</span></span>

<span data-ttu-id="9a251-126">Список жестов приложений см. в описании типа перечисления [**инкаппликатионжестуре**](/windows/desktop/api/msinkaut/ne-msinkaut-inkapplicationgesture) .</span><span class="sxs-lookup"><span data-stu-id="9a251-126">For a list of application gestures, see the [**InkApplicationGesture**](/windows/desktop/api/msinkaut/ne-msinkaut-inkapplicationgesture) enumeration type.</span></span>

<span data-ttu-id="9a251-127">Элемент управления [InkEdit](inkedit-control-reference.md) не распознает несколько жестов росчерка.</span><span class="sxs-lookup"><span data-stu-id="9a251-127">The [InkEdit](inkedit-control-reference.md) control does not recognize multiple stroke gestures.</span></span>

<span data-ttu-id="9a251-128">Элемент управления [InkEdit](inkedit-control-reference.md) подписывается на следующие жесты.</span><span class="sxs-lookup"><span data-stu-id="9a251-128">The [InkEdit](inkedit-control-reference.md) control subscribes to the following gestures.</span></span>



| <span data-ttu-id="9a251-129">жесты</span><span class="sxs-lookup"><span data-stu-id="9a251-129">Gesture</span></span>                              | <span data-ttu-id="9a251-130">Действие</span><span class="sxs-lookup"><span data-stu-id="9a251-130">Action</span></span>               |
|--------------------------------------|----------------------|
| <span data-ttu-id="9a251-131">Вниз, вниз, слева направо</span><span class="sxs-lookup"><span data-stu-id="9a251-131">Down-left ,Down-left-long</span></span><br/> | <span data-ttu-id="9a251-132">ВВОД</span><span class="sxs-lookup"><span data-stu-id="9a251-132">Enter</span></span><br/>     |
| <span data-ttu-id="9a251-133">Правый</span><span class="sxs-lookup"><span data-stu-id="9a251-133">Right</span></span><br/>                     | <span data-ttu-id="9a251-134">Пробел</span><span class="sxs-lookup"><span data-stu-id="9a251-134">Space</span></span><br/>     |
| <span data-ttu-id="9a251-135">Левый</span><span class="sxs-lookup"><span data-stu-id="9a251-135">Left</span></span><br/>                      | <span data-ttu-id="9a251-136">Отмена</span><span class="sxs-lookup"><span data-stu-id="9a251-136">Backspace</span></span><br/> |
| <span data-ttu-id="9a251-137">Вверх, справа, справа надолго</span><span class="sxs-lookup"><span data-stu-id="9a251-137">Up-right, Up-right-long</span></span><br/>   | <span data-ttu-id="9a251-138">Вкладка</span><span class="sxs-lookup"><span data-stu-id="9a251-138">Tab</span></span><br/>       |



 

<span data-ttu-id="9a251-139">Чтобы изменить действие по умолчанию для жеста, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="9a251-139">To alter the default action for a gesture:</span></span>

1.  <span data-ttu-id="9a251-140">Добавьте обработчики событий для **жестов** и событий [**Stroke**](inkedit-stroke.md) .</span><span class="sxs-lookup"><span data-stu-id="9a251-140">Add event handlers for the **Gesture** and [**Stroke**](inkedit-stroke.md) events.</span></span>
2.  <span data-ttu-id="9a251-141">В обработчике событий **жеста** отмените событие **жеста** для жеста и выполните альтернативное действие для жеста.</span><span class="sxs-lookup"><span data-stu-id="9a251-141">In the **Gesture** event handler, cancel the **Gesture** event for the gesture, and perform the alternate action for the gesture.</span></span>
3.  <span data-ttu-id="9a251-142">В обработчике событий [**Stroke**](inkedit-stroke.md) отмените событие **Stroke** для объекта [**иинкстрокедисп**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) , вызвавшего отмененное событие **жеста** .</span><span class="sxs-lookup"><span data-stu-id="9a251-142">In the [**Stroke**](inkedit-stroke.md) event handler, cancel the **Stroke** event for the [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) object that raised the canceled **Gesture** event.</span></span>

## <a name="requirements"></a><span data-ttu-id="9a251-143">Требования</span><span class="sxs-lookup"><span data-stu-id="9a251-143">Requirements</span></span>



| <span data-ttu-id="9a251-144">Требование</span><span class="sxs-lookup"><span data-stu-id="9a251-144">Requirement</span></span> | <span data-ttu-id="9a251-145">Значение</span><span class="sxs-lookup"><span data-stu-id="9a251-145">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9a251-146">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="9a251-146">Minimum supported client</span></span><br/> | <span data-ttu-id="9a251-147">Только классические приложения Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="9a251-147">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="9a251-148">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="9a251-148">Minimum supported server</span></span><br/> | <span data-ttu-id="9a251-149">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="9a251-149">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="9a251-150">Header</span><span class="sxs-lookup"><span data-stu-id="9a251-150">Header</span></span><br/>                   | <dl> <span data-ttu-id="9a251-151"><dt>«С». h (также требует \_ ввода i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="9a251-151"><dt>Inked.h (also requires inked\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="9a251-152">Библиотека</span><span class="sxs-lookup"><span data-stu-id="9a251-152">Library</span></span><br/>                  | <dl> <span data-ttu-id="9a251-153"><dt>InkEd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9a251-153"><dt>InkEd.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="9a251-154">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="9a251-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9a251-155">InkEdit</span><span class="sxs-lookup"><span data-stu-id="9a251-155">InkEdit</span></span>](inkedit-control-reference.md)
</dt> <dt>

[<span data-ttu-id="9a251-156">**Перечисление Инкаппликатионжестуре**</span><span class="sxs-lookup"><span data-stu-id="9a251-156">**InkApplicationGesture Enumeration**</span></span>](/windows/desktop/api/msinkaut/ne-msinkaut-inkapplicationgesture)
</dt> <dt>

<span data-ttu-id="9a251-157">[**\[Элемент управления InkEdit метода сетжестурестатус\]**](/windows/desktop/api/inked/nf-inked-iinkedit-setgesturestatus)</span><span class="sxs-lookup"><span data-stu-id="9a251-157">[**SetGestureStatus Method \[InkEdit Control\]**](/windows/desktop/api/inked/nf-inked-iinkedit-setgesturestatus)</span></span>
</dt> <dt>

[<span data-ttu-id="9a251-158">**Рекотимеаут, свойство**</span><span class="sxs-lookup"><span data-stu-id="9a251-158">**RecoTimeout Property**</span></span>](/windows/desktop/api/inked/nf-inked-iinkedit-get_recognitiontimeout)
</dt> <dt>

<span data-ttu-id="9a251-159">[**\[Элемент управления InkEdit для события Stroke\]**](inkedit-stroke.md)</span><span class="sxs-lookup"><span data-stu-id="9a251-159">[**Stroke Event \[InkEdit Control\]**](inkedit-stroke.md)</span></span>
</dt> <dt>

[<span data-ttu-id="9a251-160">Использование жестов</span><span class="sxs-lookup"><span data-stu-id="9a251-160">Using Gestures</span></span>](using-gestures.md)
</dt> </dl>

 

