---
description: 'Вы можете использовать сборщик рукописных данных (InkCollector, InkOverlay или InkPicture) для прямого доступа к распознавателю Microsoft жеста по умолчанию. Чтобы использовать сборщик рукописных данных для доступа к распознавателю жестов: задайте для свойства режиме CollectionMode сборщика рукописных данных значение Инканджестуре mode или Жестуреонли Mode. inkOverlay. режиме CollectionMode = режиме CollectionMode. Жестуреонли; Выберите жест, который требуется поддерживать. inkOverlay. Сетжестурестатус (ApplicationGesture. Аллжестурес, true); реализуйте обработчик событий, который получает уведомления о жестах. В обработчике событий необходимо реализовать действие, соответствующее каждому полученному событию. Примечание. смешанный режим поддерживает только жесты с одним росчерком. Режим жестов поддерживает несколько жестов росчерка. inkOverlay. жест + = New Инкколлекторжестуривенсандлер ( \_ жест inkOverlay); в режиме инканджестуре каждый отдельный росчерк отправляется распознавателю жестов Майкрософт. Если он распознан как включенный жест, отправляется уведомление о событии. Если приложение принимает уведомление о событии, штрих удаляется. Если приложение не принимает уведомление или если штрих не распознается как жест, штрих сохраняется в объекте рукописного ввода. В режиме Жестуреонли штрихи разделяются с помощью времени ожидания до и после штрихов. Штрихи, собранные в течение времени ожидания, отправляются распознавателю. Если штрихи распознаны как включенный жест, отправляется уведомление о событии. Приложение может принять или отклонить событие, что приведет к соответствующему действию. В режиме только жестов штрихи никогда не сохраняются в объекте рукописного ввода.'
ms.assetid: 3f5f00a3-1f2c-4fa2-9738-bc5fb56e2208
title: Использование только распознавателя жестов Майкрософт
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 80504e8b32c0b9596936bb4f07d029cd4ea8ddbd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103897258"
---
# <a name="using-the-microsoft-gesture-recognizer-only"></a><span data-ttu-id="3e126-113">Использование только распознавателя жестов Майкрософт</span><span class="sxs-lookup"><span data-stu-id="3e126-113">Using the Microsoft Gesture Recognizer Only</span></span>

<span data-ttu-id="3e126-114">Вы можете использовать сборщик рукописных данных ([**InkCollector**](inkcollector-class.md), [**InkOverlay**](inkoverlay-class.md)или [InkPicture](inkpicture-control-reference.md)) для прямого доступа к распознавателю Microsoft жеста по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="3e126-114">You can use an ink collector ([**InkCollector**](inkcollector-class.md), [**InkOverlay**](inkoverlay-class.md), or [InkPicture](inkpicture-control-reference.md)) to access the default Microsoft gesture recognizer directly.</span></span>

<span data-ttu-id="3e126-115">Чтобы использовать сборщик рукописных данных для доступа к распознавателю жестов, сделайте следующее:</span><span class="sxs-lookup"><span data-stu-id="3e126-115">To use an ink collector to access the gesture recognizer:</span></span>

-   <span data-ttu-id="3e126-116">Задайте для свойства [**режиме CollectionMode**](/windows/desktop/api/msinkaut/ne-msinkaut-inkcollectionmode) сборщика рукописного ввода значение режим **инканджестуре** или **жестуреонли** .</span><span class="sxs-lookup"><span data-stu-id="3e126-116">Set the [**CollectionMode**](/windows/desktop/api/msinkaut/ne-msinkaut-inkcollectionmode) property of the ink collector to either **InkAndGesture** mode or **GestureOnly** mode.</span></span>

`inkOverlay.CollectionMode = CollectionMode.GestureOnly;`

-   <span data-ttu-id="3e126-117">Выберите жест, который требуется поддерживать.</span><span class="sxs-lookup"><span data-stu-id="3e126-117">Choose the gesture that you want to support.</span></span>

`inkOverlay.SetGestureStatus(ApplicationGesture.AllGestures, true);`

-   <span data-ttu-id="3e126-118">Реализуйте обработчик событий, который получает уведомления о жестах.</span><span class="sxs-lookup"><span data-stu-id="3e126-118">Implement an event handler that receives gesture notifications.</span></span> <span data-ttu-id="3e126-119">В обработчике событий необходимо реализовать действие, соответствующее каждому полученному событию.</span><span class="sxs-lookup"><span data-stu-id="3e126-119">In the event handler, you need to implement the action corresponding to each event received.</span></span>
    > [!Note]  
    > <span data-ttu-id="3e126-120">Смешанный режим поддерживает только жесты с одним росчерком.</span><span class="sxs-lookup"><span data-stu-id="3e126-120">Mixed mode supports only single-stroke gestures.</span></span> <span data-ttu-id="3e126-121">Режим жестов поддерживает несколько жестов росчерка.</span><span class="sxs-lookup"><span data-stu-id="3e126-121">Gesture mode supports multiple stroke gestures.</span></span>

     

`inkOverlay.Gesture += new InkCollectorGestureEventHandler(inkOverlay_Gesture);`

<span data-ttu-id="3e126-122">В режиме **инканджестуре** каждый отдельный штрих отправляется распознавателю жестов Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="3e126-122">In **InkAndGesture** mode, each individual stroke is sent to the Microsoft gesture recognizer.</span></span> <span data-ttu-id="3e126-123">Если он распознан как включенный жест, отправляется уведомление о событии.</span><span class="sxs-lookup"><span data-stu-id="3e126-123">If it is recognized as a gesture that you have enabled, an event notification is sent.</span></span> <span data-ttu-id="3e126-124">Если приложение принимает уведомление о событии, штрих удаляется.</span><span class="sxs-lookup"><span data-stu-id="3e126-124">If the application accepts the event notification, the stroke is erased.</span></span> <span data-ttu-id="3e126-125">Если приложение не принимает уведомление или если штрих не распознается как жест, штрих сохраняется в объекте [**рукописного ввода**](inkdisp-class.md) .</span><span class="sxs-lookup"><span data-stu-id="3e126-125">If the application does not accept the notification or if the stroke is not recognized to be a gesture, the stroke is stored in the [**Ink**](inkdisp-class.md) object.</span></span>

<span data-ttu-id="3e126-126">В режиме **жестуреонли** штрихи разделяются с помощью времени ожидания до и после штрихов.</span><span class="sxs-lookup"><span data-stu-id="3e126-126">In **GestureOnly** mode, the strokes are delimited by timeouts before and after the strokes.</span></span> <span data-ttu-id="3e126-127">Штрихи, собранные в течение времени ожидания, отправляются распознавателю.</span><span class="sxs-lookup"><span data-stu-id="3e126-127">The strokes collected within the timeout are sent to the recognizer.</span></span> <span data-ttu-id="3e126-128">Если штрихи распознаны как включенный жест, отправляется уведомление о событии.</span><span class="sxs-lookup"><span data-stu-id="3e126-128">If the strokes are recognized as a gesture that you have enabled, an event notification is sent.</span></span> <span data-ttu-id="3e126-129">Приложение может принять или отклонить событие, что приведет к соответствующему действию.</span><span class="sxs-lookup"><span data-stu-id="3e126-129">The application may accept or reject the event, effecting the corresponding action or not.</span></span> <span data-ttu-id="3e126-130">В режиме только жестов штрихи никогда не сохраняются в объекте [**рукописного ввода**](inkdisp-class.md) .</span><span class="sxs-lookup"><span data-stu-id="3e126-130">In gesture-only mode, the strokes are never saved in the [**Ink**](inkdisp-class.md) object.</span></span>

## <a name="related-topics"></a><span data-ttu-id="3e126-131">См. также</span><span class="sxs-lookup"><span data-stu-id="3e126-131">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="3e126-132">[Microsoft. Ink. InkCollector. режиме CollectionMode](/previous-versions/ms836497(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="3e126-132">[Microsoft.Ink.InkCollector.CollectionMode](/previous-versions/ms836497(v=msdn.10))</span></span>
</dt> <dt>

<span data-ttu-id="3e126-133">[Microsoft. Ink. InkOverlay. режиме CollectionMode](/previous-versions/ms833092(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="3e126-133">[Microsoft.Ink.InkOverlay.CollectionMode](/previous-versions/ms833092(v=msdn.10))</span></span>
</dt> <dt>

<span data-ttu-id="3e126-134">[Microsoft. Ink. InkPicture. режиме CollectionMode](/previous-versions/ms582182(v=vs.100))</span><span class="sxs-lookup"><span data-stu-id="3e126-134">[Microsoft.Ink.InkPicture.CollectionMode](/previous-versions/ms582182(v=vs.100))</span></span>
</dt> </dl>

 

 
