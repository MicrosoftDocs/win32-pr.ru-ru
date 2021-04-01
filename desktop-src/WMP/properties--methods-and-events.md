---
title: Свойства, методы и события
description: Свойства, методы и события
ms.assetid: 9426d13b-42db-4a20-81f2-7a849a6e1f33
keywords:
- Проигрыватель Windows Media, свойства объектной модели
- Проигрыватель Windows Media, методы для объектной модели
- Проигрыватель Windows Media, события для объектной модели
- Объектная модель проигрывателя Windows Media, свойства
- Объектная модель проигрывателя Windows Media, методы
- Объектная модель проигрывателя Windows Media, события
- Объектная модель, свойства
- Объектная модель, методы
- Объектная модель, события
- Элемент управления ActiveX проигрывателя Windows Media, свойства объектной модели
- Элемент управления ActiveX, свойства объектной модели
- Элемент управления ActiveX мобильных устройств Windows Media Player, свойства объектной модели
- Проигрыватель Windows Media Mobile, свойства объектной модели
- Элемент управления ActiveX проигрывателя Windows Media, методы для объектной модели
- Элемент управления ActiveX, методы для объектной модели
- Элемент управления ActiveX в проигрывателе Windows Media Mobile, методы для объектной модели
- Проигрыватель Windows Media Mobile, методы для объектной модели
- Элемент управления ActiveX проигрывателя Windows Media, события для объектной модели
- Элемент управления ActiveX, события для объектной модели
- Элемент управления ActiveX мобильных устройств Windows Media Player, события для объектной модели
- Проигрыватель Windows Media Mobile, события для объектной модели
- свойства, объектная модель проигрывателя Windows Media
- методы, объектная модель проигрывателя Windows Media
- события, объектная модель проигрывателя Windows Media
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e06a860d04bfc1a5ccd5b33c0604a0ef818a0127
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104132962"
---
# <a name="properties-methods-and-events"></a><span data-ttu-id="8b884-127">Свойства, методы и события</span><span class="sxs-lookup"><span data-stu-id="8b884-127">Properties, Methods and Events</span></span>

<span data-ttu-id="8b884-128">У каждого объекта есть методы и свойства, с помощью которых можно программировать элемент управления проигрывателя Windows Media.</span><span class="sxs-lookup"><span data-stu-id="8b884-128">Each object has methods and properties through which you can program the Windows Media Player control.</span></span> <span data-ttu-id="8b884-129">Метод — это действие, которое может выполнить объект.</span><span class="sxs-lookup"><span data-stu-id="8b884-129">A method is an action that the object can take.</span></span> <span data-ttu-id="8b884-130">Свойство — это значение данных, которое можно читать или изменять.</span><span class="sxs-lookup"><span data-stu-id="8b884-130">A property is a data value that you can read or change.</span></span> <span data-ttu-id="8b884-131">Например, метод **Play** запускает воспроизведение содержимого, а свойство **Частота** кадров — текущую частоту кадров содержимого, которое воспроизводится.</span><span class="sxs-lookup"><span data-stu-id="8b884-131">For example, the **Play** method starts the content playing, and the **frameRate** property indicates the current frame rate of the content that is playing.</span></span>

<span data-ttu-id="8b884-132">Кроме того, объект **Player** создает события, которые дают возможность выполнять действия в определенное время.</span><span class="sxs-lookup"><span data-stu-id="8b884-132">In addition, the **Player** object raises events that give you the opportunity to carry out actions at specific times.</span></span> <span data-ttu-id="8b884-133">Код создается в обработчике событий, который будет выполняться, когда проигрыватель Windows Media вызывает соответствующее событие.</span><span class="sxs-lookup"><span data-stu-id="8b884-133">You write code in an event handler that will execute when Windows Media Player raises the corresponding event.</span></span> <span data-ttu-id="8b884-134">Например, можно написать код в обработчике событий **плайстатечанже** , который определяет, является ли изменение состояния таким, что носитель завершился, и если да, отобразится диалоговое окно, предлагающее пользователям повторить воспроизведение мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="8b884-134">For example, you can write code in a **PlayStateChange** event handler that determines whether the change in state is that the media ended and if so display a dialog box asking users if they want to play the media again.</span></span>

> [!Note]  
> <span data-ttu-id="8b884-135">Все методы в объектной модели проигрывателя Windows Media являются асинхронными.</span><span class="sxs-lookup"><span data-stu-id="8b884-135">All of the methods in the Windows Media Player object model are asynchronous.</span></span> <span data-ttu-id="8b884-136">При вызове двух методов в одной и той же процедуре второй метод не может полагаться на первый метод, который завершил свое действие.</span><span class="sxs-lookup"><span data-stu-id="8b884-136">If you call two methods in the same procedure, the second method cannot rely on the first method having completed its action.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="8b884-137">См. также</span><span class="sxs-lookup"><span data-stu-id="8b884-137">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8b884-138">**Сведения об объектной модели проигрывателя**</span><span class="sxs-lookup"><span data-stu-id="8b884-138">**About the Player Object Model**</span></span>](about-the-player-object-model.md)
</dt> </dl>

 

 




