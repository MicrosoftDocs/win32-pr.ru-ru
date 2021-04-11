---
title: Начало работы с ТЕМОЙ и ПРЕДСТАВЛЕНИЕм
description: Начало работы с ТЕМОЙ и ПРЕДСТАВЛЕНИЕм
ms.assetid: 1ac92f3a-463a-4343-a269-5230c644b57f
keywords:
- Создание обложек, элемент THEME
- Обложки проигрывателя Windows Media, элемент THEME
- обложки, элемент THEME
- файлы определения обложки, элемент THEME
- Элемент THEME
- Создание обложек, просмотр элемента
- Обложки проигрывателя Windows Media, элемент VIEW
- обложки, элемент VIEW
- файлы определения обложки, элемент VIEW
- VIEW, элемент
- элементы, представление
- элементы, тема
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 499444ee2093e743f58174797794a50fbf74555a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103889063"
---
# <a name="start-with-theme-and-view"></a><span data-ttu-id="217b5-115">Начало работы с ТЕМОЙ и ПРЕДСТАВЛЕНИЕм</span><span class="sxs-lookup"><span data-stu-id="217b5-115">Start with THEME and VIEW</span></span>

<span data-ttu-id="217b5-116">Каждая Обложка должна иметь только один элемент **темы** и хотя бы один элемент **представления** .</span><span class="sxs-lookup"><span data-stu-id="217b5-116">Every skin must have exactly one **THEME** element and at least one **VIEW** element.</span></span>

<span data-ttu-id="217b5-117">В текстовом редакторе создайте следующий текст:</span><span class="sxs-lookup"><span data-stu-id="217b5-117">Using your text editor, create the following text:</span></span>


```C++
<THEME>
    <VIEW
        clippingColor = "#CCCC00"
        backgroundImage = "background.bmp"
        titleBar = "False">


    </VIEW>
</THEME>

```



<span data-ttu-id="217b5-118">Перед закрывающим тегом **представления** оставьте пустые строки, так как в дальнейшем будет добавлен дополнительный код.</span><span class="sxs-lookup"><span data-stu-id="217b5-118">Leave some blank lines before the closing **VIEW** tag because you'll be adding more code here later.</span></span>

<span data-ttu-id="217b5-119">Сохраните файл с любым именем файла, но убедитесь, что расширение — WMS.</span><span class="sxs-lookup"><span data-stu-id="217b5-119">Save your file with any file name you wish, but be sure that the extension is .wms.</span></span> <span data-ttu-id="217b5-120">Например, типичным именем файла может быть скиноне. WMS.</span><span class="sxs-lookup"><span data-stu-id="217b5-120">For example, a typical file name might be skinone.wms.</span></span>

<span data-ttu-id="217b5-121">Каждая Обложка должна начинаться с <THEME> и заканчиваться на </THEME>.</span><span class="sxs-lookup"><span data-stu-id="217b5-121">Every skin must start with <THEME> and end with </THEME>.</span></span> <span data-ttu-id="217b5-122">В обложке может быть только один элемент **Theme** , но он должен быть одним.</span><span class="sxs-lookup"><span data-stu-id="217b5-122">You can only have one **THEME** element in your skin, but you must have one.</span></span>

<span data-ttu-id="217b5-123">Необходимо также иметь хотя бы один элемент **представления** .</span><span class="sxs-lookup"><span data-stu-id="217b5-123">You must also have at least one **VIEW** element.</span></span> <span data-ttu-id="217b5-124">Можно использовать несколько **представлений**, но в этом примере только один.</span><span class="sxs-lookup"><span data-stu-id="217b5-124">You can have more than one **VIEW**, but this example only has one.</span></span> <span data-ttu-id="217b5-125">Необходимо открыть <VIEW> и закрыть <VIEW>. Обратите внимание, что открывающий </VIEW> тег не закрывает тег сразу же, но включает несколько атрибутов перед закрывающей угловой скобкой (>).</span><span class="sxs-lookup"><span data-stu-id="217b5-125">You must have an opening <VIEW> and a closing <VIEW>. Notice that the opening </VIEW> tag does not close the tag right away, but includes several attributes before the closing angle bracket (>).</span></span> <span data-ttu-id="217b5-126">В элементе **Theme** в этом примере используются следующие атрибуты:</span><span class="sxs-lookup"><span data-stu-id="217b5-126">The following attributes are used in the **THEME** element in this example:</span></span>

<span data-ttu-id="217b5-127">**клиппингколор**</span><span class="sxs-lookup"><span data-stu-id="217b5-127">**clippingColor**</span></span>

<span data-ttu-id="217b5-128">Атрибут **клиппингколор** не всегда нужен, если края обложки являются прямоугольными.</span><span class="sxs-lookup"><span data-stu-id="217b5-128">You will not always need the **clippingColor** attribute if the edges of your skin are rectangular.</span></span> <span data-ttu-id="217b5-129">Обложка в этом примере является овалом, поэтому требуется обрезать цвет для частей обложки, которые должны отображаться на рабочем столе; фактически все части за пределами овала.</span><span class="sxs-lookup"><span data-stu-id="217b5-129">The skin in this example is oval-shaped, so you need a clipping color for the parts of the skin that you want to see the desktop through; essentially all parts outside the oval.</span></span> <span data-ttu-id="217b5-130">В этом примере обложки мы будем использовать темно-желтый цвет, заданный как « \# CCCC00» в формате Web.</span><span class="sxs-lookup"><span data-stu-id="217b5-130">In this example skin, we will use a dark yellow, specified as "\#CCCC00" in Web format.</span></span> <span data-ttu-id="217b5-131">Причины этого выбора задаются при [создании основного файла изображения](creating-the-primary-art-file.md).</span><span class="sxs-lookup"><span data-stu-id="217b5-131">The reasons for this choice are given in [Creating the Primary Art File](creating-the-primary-art-file.md).</span></span> <span data-ttu-id="217b5-132">По сути, это значение всегда будет числом, полученным от художественной программы.</span><span class="sxs-lookup"><span data-stu-id="217b5-132">Essentially, this value will always be a number that you get from your art program.</span></span>

<span data-ttu-id="217b5-133">**backgroundImage**</span><span class="sxs-lookup"><span data-stu-id="217b5-133">**backgroundImage**</span></span>

<span data-ttu-id="217b5-134">Это имя основного файла изображения.</span><span class="sxs-lookup"><span data-stu-id="217b5-134">This is the name of the primary art file.</span></span> <span data-ttu-id="217b5-135">Это должно быть точное имя файла и путь к основному файлу изображения.</span><span class="sxs-lookup"><span data-stu-id="217b5-135">It should be the exact file name and path of your primary art file.</span></span> <span data-ttu-id="217b5-136">Поддерживаются только файлы BMP, JPG, GIF и PNG, поэтому рекомендуется использовать формат BMP.</span><span class="sxs-lookup"><span data-stu-id="217b5-136">Only BMP, JPG, GIF, and PNG files are supported, and BMP is recommended.</span></span>

<span data-ttu-id="217b5-137">**titleBar**</span><span class="sxs-lookup"><span data-stu-id="217b5-137">**titleBar**</span></span>

<span data-ttu-id="217b5-138">Эта Обложка не имеет **заголовка**, поэтому значение будет "false".</span><span class="sxs-lookup"><span data-stu-id="217b5-138">This skin does not have a **titleBar**, so the value will be "false".</span></span> <span data-ttu-id="217b5-139">Заголовок будет отображаться только в том случае, если вы хотите, чтобы у обложки был цвет фона и он был прямоугольным.</span><span class="sxs-lookup"><span data-stu-id="217b5-139">You will only want a title bar if you want your skin to have a background color and be rectangular.</span></span>

<span data-ttu-id="217b5-140">Не забудьте поставить закрывающую угловую скобку (>) после значения в **строке заголовка** , чтобы указать, что определение **представления** завершено.</span><span class="sxs-lookup"><span data-stu-id="217b5-140">Be sure that you put the closing angle bracket (>) after the **titleBar** value to indicate that you are finished defining the **VIEW**.</span></span> <span data-ttu-id="217b5-141">Перед закрывающим **представлением** и тегами **темы** оставьте несколько пустых строк.</span><span class="sxs-lookup"><span data-stu-id="217b5-141">Leave a few blank lines before the closing **VIEW** and **THEME** tags.</span></span> <span data-ttu-id="217b5-142">Вам понадобятся строки кода, которые будут добавлены позже.</span><span class="sxs-lookup"><span data-stu-id="217b5-142">You will need the lines for code that you will add later.</span></span>

## <a name="related-topics"></a><span data-ttu-id="217b5-143">См. также</span><span class="sxs-lookup"><span data-stu-id="217b5-143">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="217b5-144">**Создание файла определения обложки**</span><span class="sxs-lookup"><span data-stu-id="217b5-144">**Creating the Skin Definition File**</span></span>](creating-the-skin-definition-file.md)
</dt> </dl>

 

 




