---
title: Добавление Close БУТТОНЕЛЕМЕНТ
description: Добавление Close БУТТОНЕЛЕМЕНТ
ms.assetid: 18f0ee9d-b0d4-4134-8dd6-6ece480b2818
keywords:
- Создание обложек, элемент БУТТОНЕЛЕМЕНТ
- Обложки проигрывателя Windows Media, элемент БУТТОНЕЛЕМЕНТ
- обложки, элемент БУТТОНЕЛЕМЕНТ
- файлы определения обложки, элемент БУТТОНЕЛЕМЕНТ
- БУТТОНЕЛЕМЕНТ, элемент
- элементы, БУТТОНЕЛЕМЕНТ
- Создание обложек, кнопки закрытия
- Обложки проигрывателя Windows Media, кнопки закрытия
- обложки, кнопки закрытия
- файлы определения обложки, кнопки закрытия
- Кнопки закрытия
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 40716d4094d23eaf6ab86414f37c0778cc8d89cf
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104258510"
---
# <a name="adding-the-close-buttonelement"></a><span data-ttu-id="82fac-114">Добавление Close БУТТОНЕЛЕМЕНТ</span><span class="sxs-lookup"><span data-stu-id="82fac-114">Adding the Close BUTTONELEMENT</span></span>

<span data-ttu-id="82fac-115">Кнопка Закрыть аналогична кнопке воспроизвести, но имеет разные коды и цвета.</span><span class="sxs-lookup"><span data-stu-id="82fac-115">The Close button is similar in concept to the Play button, but has different codes and colors.</span></span>

<span data-ttu-id="82fac-116">Вставьте код закрытия **буттонелемент** после закрывающей угловой скобки **буттонелемент** Play.</span><span class="sxs-lookup"><span data-stu-id="82fac-116">Put the Close **BUTTONELEMENT** code after the closing angle bracket of the Play **BUTTONELEMENT**.</span></span>


```C++
        <BUTTONELEMENT
            mappingColor = "#FF0000"
            upToolTip = "Close"
            onClick="JScript: view.close();" />

```



<span data-ttu-id="82fac-117">Для определения **буттонелемент** для кнопки Close используются следующие атрибуты:</span><span class="sxs-lookup"><span data-stu-id="82fac-117">The following attributes are used to define the **BUTTONELEMENT** for the Close button:</span></span>

<span data-ttu-id="82fac-118">**маппингколор**</span><span class="sxs-lookup"><span data-stu-id="82fac-118">**mappingColor**</span></span>

<span data-ttu-id="82fac-119">Это значение цвета для региона в файле рисунка сопоставления, созданном ранее.</span><span class="sxs-lookup"><span data-stu-id="82fac-119">This is the color value of the region in the mapping art file you created before.</span></span> <span data-ttu-id="82fac-120">В данном случае это сплошной красный цвет.</span><span class="sxs-lookup"><span data-stu-id="82fac-120">In this case it is the solid red color.</span></span> <span data-ttu-id="82fac-121">Этот атрибут является обязательным для любого **буттонелемент**.</span><span class="sxs-lookup"><span data-stu-id="82fac-121">This attribute is required for any **BUTTONELEMENT**.</span></span> <span data-ttu-id="82fac-122">Определив этот цвет, вы указываете проигрывателю Windows Media связать эту цветовую область с XML-кодом этой кнопки.</span><span class="sxs-lookup"><span data-stu-id="82fac-122">By defining this color, you are telling Windows Media Player to associate this color area with the XML code of this button.</span></span>

<span data-ttu-id="82fac-123">**Подсказка**</span><span class="sxs-lookup"><span data-stu-id="82fac-123">**upToolTip**</span></span>

<span data-ttu-id="82fac-124">Определяет текст, который будет отображаться, когда пользователь наводит указатель мыши на кнопку.</span><span class="sxs-lookup"><span data-stu-id="82fac-124">This defines the text that will be displayed when the user hovers the mouse over the button.</span></span> <span data-ttu-id="82fac-125">Это то же самое, что кнопка воспроизведения, за исключением того, что она помечена как «Close» (закрыть).</span><span class="sxs-lookup"><span data-stu-id="82fac-125">This is the same as the Play button except that it is labeled "Close".</span></span>

<span data-ttu-id="82fac-126">**onClick**</span><span class="sxs-lookup"><span data-stu-id="82fac-126">**onClick**</span></span>

<span data-ttu-id="82fac-127">Определяет событие, возникающее при нажатии кнопки мыши.</span><span class="sxs-lookup"><span data-stu-id="82fac-127">This defines the event that occurs when the mouse clicks on the button.</span></span> <span data-ttu-id="82fac-128">Значение этого атрибута события называется обработчиком событий и будет либо строкой кода Microsoft JScript, либо функцией JScript во внешнем текстовом файле, который загружается атрибутом **Лоадскрипт** **представления**.</span><span class="sxs-lookup"><span data-stu-id="82fac-128">The value of this event attribute is called an event handler and will be either a line of Microsoft JScript code, or a JScript function in an external text file that is loaded by the **loadScript** attribute of a **VIEW**.</span></span> <span data-ttu-id="82fac-129">В этом случае код JScript вызывает метод **Close** элемента **View** с помощью **представления** глобальных атрибутов, который закрывает представление и завершает работу проигрывателя Windows Media.</span><span class="sxs-lookup"><span data-stu-id="82fac-129">In this case, the JScript code calls the **close** method of the **VIEW** element using the global attribute **view**, which closes the view and shuts down Windows Media Player.</span></span>

## <a name="related-topics"></a><span data-ttu-id="82fac-130">См. также</span><span class="sxs-lookup"><span data-stu-id="82fac-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="82fac-131">**Создание файла определения обложки**</span><span class="sxs-lookup"><span data-stu-id="82fac-131">**Creating the Skin Definition File**</span></span>](creating-the-skin-definition-file.md)
</dt> </dl>

 

 




