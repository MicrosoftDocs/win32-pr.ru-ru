---
title: Добавление БУТТОНЕЛЕМЕНТ Play
description: Добавление БУТТОНЕЛЕМЕНТ Play
ms.assetid: 895850a7-7538-4581-8348-41cbb3bc9717
keywords:
- Создание обложек, элемент БУТТОНЕЛЕМЕНТ
- Обложки проигрывателя Windows Media, элемент БУТТОНЕЛЕМЕНТ
- обложки, элемент БУТТОНЕЛЕМЕНТ
- файлы определения обложки, элемент БУТТОНЕЛЕМЕНТ
- БУТТОНЕЛЕМЕНТ, элемент
- элементы, БУТТОНЕЛЕМЕНТ
- Создание обложек, кнопок воспроизведения
- Обложки проигрывателя Windows Media, кнопки воспроизведения
- обложки, кнопки воспроизведения
- файлы определения обложки, кнопки воспроизведения
- Кнопки воспроизведения
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a92b5416adf2e323043eb563ec08e1e4d2525733
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104532171"
---
# <a name="adding-the-play-buttonelement"></a><span data-ttu-id="06bd7-114">Добавление БУТТОНЕЛЕМЕНТ Play</span><span class="sxs-lookup"><span data-stu-id="06bd7-114">Adding the Play BUTTONELEMENT</span></span>

<span data-ttu-id="06bd7-115">Наконец, можно добавить элементы **буттонелемент** , которые соединяют визуальные кнопки на экране, с действиями проигрывателя Windows Media.</span><span class="sxs-lookup"><span data-stu-id="06bd7-115">Finally, you can add the **BUTTONELEMENT** elements that connect the visual buttons on the screen to Windows Media Player actions.</span></span> <span data-ttu-id="06bd7-116">Это ядро обложки, и его можно рассматривать как привязку поверхности обложки к внутреннему механизму проигрывателя Windows Media.</span><span class="sxs-lookup"><span data-stu-id="06bd7-116">This is the core of your skin and you can think of it as wiring the surface of the skin to the inner machinery of Windows Media Player.</span></span>

<span data-ttu-id="06bd7-117">**Буттонелемент** содержатся в **BUTTONGROUP**.</span><span class="sxs-lookup"><span data-stu-id="06bd7-117">**BUTTONELEMENT** s are contained within a **BUTTONGROUP**.</span></span> <span data-ttu-id="06bd7-118">В каждом **BUTTONGROUP** всегда должен быть хотя бы один **буттонелемент** .</span><span class="sxs-lookup"><span data-stu-id="06bd7-118">You must always have at least one **BUTTONELEMENT** inside each **BUTTONGROUP**.</span></span>

<span data-ttu-id="06bd7-119">Вставьте код Play **буттонелемент** после закрывающей угловой скобки **BUTTONGROUP**.</span><span class="sxs-lookup"><span data-stu-id="06bd7-119">Put the Play **BUTTONELEMENT** code after the closing angle bracket of **BUTTONGROUP**.</span></span>


```C++
        <BUTTONELEMENT
            mappingColor = "#00FF00"
            upToolTip = "Play"
            onClick = "JScript: player.URL='https://proseware.com/laure.wma';" />

```



<span data-ttu-id="06bd7-120">Для определения **буттонелемент** кнопки воспроизведения используются следующие атрибуты:</span><span class="sxs-lookup"><span data-stu-id="06bd7-120">The following attributes are used to define the **BUTTONELEMENT** for the Play button:</span></span>

<span data-ttu-id="06bd7-121">**маппингколор**</span><span class="sxs-lookup"><span data-stu-id="06bd7-121">**mappingColor**</span></span>

<span data-ttu-id="06bd7-122">Это значение цвета для региона в файле рисунка сопоставления, созданном ранее.</span><span class="sxs-lookup"><span data-stu-id="06bd7-122">This is the color value of a region in the mapping art file you created before.</span></span> <span data-ttu-id="06bd7-123">В данном случае это сплошной зеленый цвет.</span><span class="sxs-lookup"><span data-stu-id="06bd7-123">In this case it is the solid green color.</span></span> <span data-ttu-id="06bd7-124">Этот атрибут является обязательным для любого **буттонелемент**.</span><span class="sxs-lookup"><span data-stu-id="06bd7-124">This attribute is required for any **BUTTONELEMENT**.</span></span> <span data-ttu-id="06bd7-125">Определив этот цвет, вы указываете проигрывателю Windows Media связать эту цветовую область с XML-кодом этой кнопки.</span><span class="sxs-lookup"><span data-stu-id="06bd7-125">By defining this color, you are telling Windows Media Player to associate this color area with the XML code of this button.</span></span>

<span data-ttu-id="06bd7-126">**Подсказка**</span><span class="sxs-lookup"><span data-stu-id="06bd7-126">**upToolTip**</span></span>

<span data-ttu-id="06bd7-127">Определяет текст, который будет отображаться, если пользователь наведет указатель мыши на кнопку.</span><span class="sxs-lookup"><span data-stu-id="06bd7-127">This defines the text that will be displayed if the user hovers the mouse over the button.</span></span> <span data-ttu-id="06bd7-128">Не путайте это с назначением, которое будет отображаться.</span><span class="sxs-lookup"><span data-stu-id="06bd7-128">Do not confuse this with the hover art that will be displayed.</span></span> <span data-ttu-id="06bd7-129">Всплывающая подсказка — это небольшой заголовок, который занимает некоторое время.</span><span class="sxs-lookup"><span data-stu-id="06bd7-129">A ToolTip is a small balloon caption that takes a moment to appear.</span></span> <span data-ttu-id="06bd7-130">Однако изображение с наведением будет мгновенно отображаться в любом выбранном цвете и форме.</span><span class="sxs-lookup"><span data-stu-id="06bd7-130">The hover art image, however, will appear instantly in whatever color and shape you choose.</span></span>

<span data-ttu-id="06bd7-131">**onClick**</span><span class="sxs-lookup"><span data-stu-id="06bd7-131">**onClick**</span></span>

<span data-ttu-id="06bd7-132">Определяет событие, возникающее при нажатии кнопки мыши.</span><span class="sxs-lookup"><span data-stu-id="06bd7-132">This defines the event that occurs when the mouse clicks on the button.</span></span> <span data-ttu-id="06bd7-133">Значение этого атрибута события называется обработчиком событий и будет либо строкой кода Microsoft JScript, либо функцией JScript во внешнем текстовом файле, который загружается атрибутом **Лоадскрипт** **представления**.</span><span class="sxs-lookup"><span data-stu-id="06bd7-133">The value of this event attribute is called an event handler and will be either a line of Microsoft JScript code, or a JScript function in an external text file that is loaded by the **loadScript** attribute of a **VIEW**.</span></span> <span data-ttu-id="06bd7-134">В этом случае код JScript вызывает метод **URL-адреса** проигрывателя Windows Media, который загружает и начинает воспроизводить файл с именем «Лауре. WMA».</span><span class="sxs-lookup"><span data-stu-id="06bd7-134">In this case, the JScript code calls the **URL** method of Windows Media Player, which loads and starts playing a file named "laure.wma".</span></span> <span data-ttu-id="06bd7-135">Обратите внимание, что строка заканчивается точкой с запятой внутри кавычек, что является хорошей практикой написания кода в JScript.</span><span class="sxs-lookup"><span data-stu-id="06bd7-135">Note that the line ends with a semicolon inside the quotes, which is good JScript coding practice.</span></span> <span data-ttu-id="06bd7-136">Обратите внимание также на то, что в двойных кавычках используется одинарные кавычки для задания имени файла.</span><span class="sxs-lookup"><span data-stu-id="06bd7-136">Note also the use of single quotes inside the double quotes to set off the file name.</span></span> <span data-ttu-id="06bd7-137">Дополнительные сведения о JScript см. в статье [Использование JScript](using-jscript.md) в разделе "сведения о обложках" этого пакета SDK.</span><span class="sxs-lookup"><span data-stu-id="06bd7-137">For more information about JScript, see [Using JScript](using-jscript.md) in the About Skins section of this SDK.</span></span>

<span data-ttu-id="06bd7-138">Обратите внимание, что отсутствует конечный тег **буттонелемент** .</span><span class="sxs-lookup"><span data-stu-id="06bd7-138">Notice that there is no ending **BUTTONELEMENT** tag.</span></span> <span data-ttu-id="06bd7-139">Если элемент не заключает другой элемент, его можно закрыть с помощью косой черты прямо перед закрывающей угловой скобкой.</span><span class="sxs-lookup"><span data-stu-id="06bd7-139">If an element does not enclose another element, you can close it off with the forward slash just before the closing angle bracket.</span></span> <span data-ttu-id="06bd7-140">Это говорит о том, что XML завершен с этим элементом.</span><span class="sxs-lookup"><span data-stu-id="06bd7-140">This tells XML that you are finished with that element.</span></span> <span data-ttu-id="06bd7-141">Например,</span><span class="sxs-lookup"><span data-stu-id="06bd7-141">For example,</span></span>


```C++
<BUTTONELEMENT></BUTTONELEMENT>
```



<span data-ttu-id="06bd7-142">и</span><span class="sxs-lookup"><span data-stu-id="06bd7-142">and</span></span>


```C++
<BUTTONELEMENT/>
```



<span data-ttu-id="06bd7-143">передает те же сведения в формате XML.</span><span class="sxs-lookup"><span data-stu-id="06bd7-143">convey the same information in XML.</span></span>

<span data-ttu-id="06bd7-144">Возможности обложек обусловлены использованием обработчиков событий.</span><span class="sxs-lookup"><span data-stu-id="06bd7-144">The power of skins comes from using event handlers.</span></span> <span data-ttu-id="06bd7-145">Если пользователь делает что-то с помощью мыши, это событие можно обменять с помощью JScript.</span><span class="sxs-lookup"><span data-stu-id="06bd7-145">If the user does something with a mouse, you can handle that event with JScript.</span></span> <span data-ttu-id="06bd7-146">Код может быть единственной строкой, которая делает проигрыватель Windows Media простым, например Play, или полноценным приложением, написанным на языке JScript.</span><span class="sxs-lookup"><span data-stu-id="06bd7-146">Your code can be a single line that makes Windows Media Player do something simple like play, or it can be a complete application written in JScript.</span></span>

## <a name="related-topics"></a><span data-ttu-id="06bd7-147">См. также</span><span class="sxs-lookup"><span data-stu-id="06bd7-147">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="06bd7-148">**Создание файла определения обложки**</span><span class="sxs-lookup"><span data-stu-id="06bd7-148">**Creating the Skin Definition File**</span></span>](creating-the-skin-definition-file.md)
</dt> </dl>

 

 




