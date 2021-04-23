---
title: Создание файла определения обложки
description: Создание файла определения обложки
ms.assetid: ea7f8e7c-a505-478d-80c3-cb3a3f67859d
keywords:
- Обложки мобильных приложений проигрывателя Windows Media, файлы определения обложки
- обложки, файлы определения обложки
- файлы для обложек, определение обложки
- файлы определения обложки, создание
- Создание обложек, сведения
- Создание обложек, проигрыватель Windows Media Mobile
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8b8a2920a08a3f57f740ff5ed3ca6e291ffd1bde
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103777258"
---
# <a name="creating-a-skin-definition-file"></a><span data-ttu-id="ee775-109">Создание файла определения обложки</span><span class="sxs-lookup"><span data-stu-id="ee775-109">Creating a Skin Definition File</span></span>

<span data-ttu-id="ee775-110">Файл определения обложки — это текстовый файл, который определяет обложку и все ее составные части.</span><span class="sxs-lookup"><span data-stu-id="ee775-110">A skin definition file is a text file that defines a skin and all its composite parts.</span></span> <span data-ttu-id="ee775-111">Расширение имени файла должно быть СКН.</span><span class="sxs-lookup"><span data-stu-id="ee775-111">The file name extension must be .skn.</span></span>

<span data-ttu-id="ee775-112">Каждый файл определения обложки должен начинаться со следующей строки, указывающей номер версии файла обложки.</span><span class="sxs-lookup"><span data-stu-id="ee775-112">Every skin definition file must start with the following line, which specifies the skin file version number.</span></span> <span data-ttu-id="ee775-113">В следующей таблице приведены версии проигрывателя Windows Media и строка кода, которая должна использоваться для определения каждого файла в файле определения обложки.</span><span class="sxs-lookup"><span data-stu-id="ee775-113">The following table shows Windows Media Player versions and the code line that should be used to identify each in a skin definition file.</span></span> <span data-ttu-id="ee775-114">Хотя некоторые числа в строках кода не являются предполагаемыми, они являются правильными, как показано в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="ee775-114">Although some of the numbers in the code lines are not what you would expect, they are correct as shown in the following table.</span></span>



| <span data-ttu-id="ee775-115">Версия проигрывателя Windows Media</span><span class="sxs-lookup"><span data-stu-id="ee775-115">Windows Media Player version</span></span> | <span data-ttu-id="ee775-116">Первая строка файла определения обложки</span><span class="sxs-lookup"><span data-stu-id="ee775-116">First line of skin definition file</span></span> |
|------------------------------|------------------------------------|
| <span data-ttu-id="ee775-117">1.01.1</span><span class="sxs-lookup"><span data-stu-id="ee775-117">1.01.1</span></span><br/>            | <span data-ttu-id="ee775-118">\[Файл обложки Pocket WMP версии 1.0\]</span><span class="sxs-lookup"><span data-stu-id="ee775-118">\[Pocket WMP Skin File v1.0\]</span></span>      |
| <span data-ttu-id="ee775-119">1.2</span><span class="sxs-lookup"><span data-stu-id="ee775-119">1.2</span></span>                          | <span data-ttu-id="ee775-120">\[Файл обложки Pocket WMP версии 1.2\]</span><span class="sxs-lookup"><span data-stu-id="ee775-120">\[Pocket WMP Skin File v1.2\]</span></span>      |
| <span data-ttu-id="ee775-121">7.0</span><span class="sxs-lookup"><span data-stu-id="ee775-121">7.0</span></span>                          | <span data-ttu-id="ee775-122">\[Файл обложки Pocket WMP версии 2.0\]</span><span class="sxs-lookup"><span data-stu-id="ee775-122">\[Pocket WMP Skin File v2.0\]</span></span>      |
| <span data-ttu-id="ee775-123">7.1</span><span class="sxs-lookup"><span data-stu-id="ee775-123">7.1</span></span>                          | <span data-ttu-id="ee775-124">\[Файл обложки Pocket WMP версии 8.0\]</span><span class="sxs-lookup"><span data-stu-id="ee775-124">\[Pocket WMP Skin File v8.0\]</span></span>      |
| <span data-ttu-id="ee775-125">Серия 9</span><span class="sxs-lookup"><span data-stu-id="ee775-125">9 Series</span></span>                     | <span data-ttu-id="ee775-126">\[Файл обложки Pocket WMP v 9.0.1\]</span><span class="sxs-lookup"><span data-stu-id="ee775-126">\[Pocket WMP Skin File v9.0.1\]</span></span>    |
| <span data-ttu-id="ee775-127">10 Mobile</span><span class="sxs-lookup"><span data-stu-id="ee775-127">10 Mobile</span></span>                    | <span data-ttu-id="ee775-128">\[Файл обложки Pocket WMP v 9.0.1\]</span><span class="sxs-lookup"><span data-stu-id="ee775-128">\[Pocket WMP Skin File v9.0.1\]</span></span>    |
| <span data-ttu-id="ee775-129">10,1 Mobile</span><span class="sxs-lookup"><span data-stu-id="ee775-129">10.1 Mobile</span></span>                  | <span data-ttu-id="ee775-130">\[Файл обложки Pocket WMP v 9.0.1\]</span><span class="sxs-lookup"><span data-stu-id="ee775-130">\[Pocket WMP Skin File v9.0.1\]</span></span>    |



 

<span data-ttu-id="ee775-131">Номер версии 9.0.1 предназначен для обложек, созданных специально для проигрывателя Windows Media 9 Series или более поздней версии.</span><span class="sxs-lookup"><span data-stu-id="ee775-131">The version number 9.0.1 is for skins created specifically for Windows Media Player 9 Series or later.</span></span> <span data-ttu-id="ee775-132">Обложки с более ранним номером версии открываются в проигрывателе Windows Media 9 Series или более поздней версии в режиме книжной ориентации, 96 точек на дюйм (DPI).</span><span class="sxs-lookup"><span data-stu-id="ee775-132">Skins having an earlier version number are opened by Windows Media Player 9 Series or later as portrait mode, 96 dots per inch (DPI) skins.</span></span>

<span data-ttu-id="ee775-133">Файл определения обложки состоит из нескольких разделов.</span><span class="sxs-lookup"><span data-stu-id="ee775-133">The skin definition file consists of several sections.</span></span> <span data-ttu-id="ee775-134">Каждый раздел определяет определенную область обложки.</span><span class="sxs-lookup"><span data-stu-id="ee775-134">Each section defines a particular area of the skin.</span></span> <span data-ttu-id="ee775-135">Разделы должны быть размещены в следующем порядке:</span><span class="sxs-lookup"><span data-stu-id="ee775-135">The sections must be placed in the following order:</span></span>

1.  <span data-ttu-id="ee775-136">Описание</span><span class="sxs-lookup"><span data-stu-id="ee775-136">Description</span></span>
2.  <span data-ttu-id="ee775-137">Растровые изображения</span><span class="sxs-lookup"><span data-stu-id="ee775-137">Bitmaps</span></span>
3.  <span data-ttu-id="ee775-138">Видео</span><span class="sxs-lookup"><span data-stu-id="ee775-138">Video</span></span>
4.  <span data-ttu-id="ee775-139">Кнопки</span><span class="sxs-lookup"><span data-stu-id="ee775-139">Buttons</span></span>
5.  <span data-ttu-id="ee775-140">Состояние</span><span class="sxs-lookup"><span data-stu-id="ee775-140">Status</span></span>
6.  <span data-ttu-id="ee775-141">Текст</span><span class="sxs-lookup"><span data-stu-id="ee775-141">Text</span></span>
7.  <span data-ttu-id="ee775-142">Marquee</span><span class="sxs-lookup"><span data-stu-id="ee775-142">Marquee</span></span>
8.  <span data-ttu-id="ee775-143">Линейки воспроизведения</span><span class="sxs-lookup"><span data-stu-id="ee775-143">Trackbars</span></span>

<span data-ttu-id="ee775-144">Каждый раздел начинается с имени раздела в квадратных скобках, например:</span><span class="sxs-lookup"><span data-stu-id="ee775-144">Each section starts with the name of the section in square brackets, for example:</span></span>


```C++
[ Bitmaps ]

```



> [!Note]  
> <span data-ttu-id="ee775-145">Файл определения обложки будет проанализирован неправильно, если между скобками и именем раздела не указаны пробелы.</span><span class="sxs-lookup"><span data-stu-id="ee775-145">Your skin definition file will not be parsed correctly unless you include spaces between the brackets and the name of the section.</span></span>

 

<span data-ttu-id="ee775-146">Затем одна или несколько строк определяют отдельные изображения, кнопки и т. д.</span><span class="sxs-lookup"><span data-stu-id="ee775-146">Then, one or more lines define individual images, buttons, and so on.</span></span> <span data-ttu-id="ee775-147">Например, раздел растровых изображений может включать в себя следующее:</span><span class="sxs-lookup"><span data-stu-id="ee775-147">For example, a Bitmaps section might include the following:</span></span>


```C++
    Background  Background.bmp  0,0
    Disabled    Disabled.bmp    0,0
    Pushed      Pushed.bmp      0,0
    Region      Region.bmp      0,0
    Super       Super.bmp       0,0

```



<span data-ttu-id="ee775-148">Не обязательно выровнять значения в столбцах, но это поможет сделать код более удобочитаемым.</span><span class="sxs-lookup"><span data-stu-id="ee775-148">It is not necessary to line up the values in columns, but it will help your code to be more readable.</span></span> <span data-ttu-id="ee775-149">Дополнительные сведения о каждом разделе файла определения обложки см. в [справочнике по обложкам](skin-reference.md).</span><span class="sxs-lookup"><span data-stu-id="ee775-149">For more details about each section of the skin definition file, see the [Skin Reference](skin-reference.md).</span></span>

> [!Note]  
> <span data-ttu-id="ee775-150">Не используйте символы табуляции в любом месте файла. Вместо этого используйте лишние пробелы.</span><span class="sxs-lookup"><span data-stu-id="ee775-150">Do not use tabs anywhere in the file; use extra spaces instead.</span></span> <span data-ttu-id="ee775-151">Это очень важно, поскольку нажатие клавиши TAB во время записи или редактирования файла определения обложки приведет к сбою всей обложки.</span><span class="sxs-lookup"><span data-stu-id="ee775-151">This is very important, because pressing the TAB key while writing or editing your skin definition file will cause the entire skin to fail.</span></span> <span data-ttu-id="ee775-152">Каждая строка должна быть заполнена и не может продолжаться на второй строке.</span><span class="sxs-lookup"><span data-stu-id="ee775-152">Each line must be complete and cannot continue onto a second line.</span></span> <span data-ttu-id="ee775-153">Кроме того, параметры Region и Super не рекомендуются для обложек, используемых с проигрывателем Windows Media 10 Mobile или более поздней версии.</span><span class="sxs-lookup"><span data-stu-id="ee775-153">Also, the Region and Super values are deprecated for skins used with Windows Media Player 10 Mobile or later.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="ee775-154">См. также</span><span class="sxs-lookup"><span data-stu-id="ee775-154">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ee775-155">**Файл определения обложки**</span><span class="sxs-lookup"><span data-stu-id="ee775-155">**Skin Definition File**</span></span>](skin-definition-file-mobile.md)
</dt> </dl>

 

 





