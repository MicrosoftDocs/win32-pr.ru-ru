---
title: Использование элемента TextBox
description: Использование элемента TextBox
ms.assetid: e0022722-a504-47da-aa3f-62aa7fb4ac4d
keywords:
- Веб-семинар, элемент TextBox
- Разработка веб-страниц, элемент TextBox
- Язык VML (VML), элемент TextBox
- VML (язык VML), элемент TextBox
- Векторная графика, элемент TextBox
- TextBox, элемент
- Элементы VML, текстовое поле
- Фигуры VML, элемент TextBox
- Язык VML (VML), присоединение текста
- VML (язык VML), присоединение текста
- Векторная графика, присоединение текста
- Фигуры VML, присоединение текста
- присоединение текста
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5388a359ca8cf4e320f95d708b4cf7055287d424
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104488224"
---
# <a name="using-the-textbox-element"></a><span data-ttu-id="af033-116">Использование элемента TextBox</span><span class="sxs-lookup"><span data-stu-id="af033-116">Using the Textbox Element</span></span>

<span data-ttu-id="af033-117">В этом разделе описывается функция VML, которая является устаревшей в Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="af033-117">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="af033-118">Веб-страницы и приложения, использующие VML, должны быть перенесены в формат SVG или другие широко поддерживаемые стандарты.</span><span class="sxs-lookup"><span data-stu-id="af033-118">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="af033-119">По состоянию на Декабрь 2011 этот раздел был архивирован.</span><span class="sxs-lookup"><span data-stu-id="af033-119">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="af033-120">В результате он больше не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="af033-120">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="af033-121">Дополнительные сведения см. в разделе [архивированное содержимое](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="af033-121">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="af033-122">Сведения, рекомендации и рекомендации по текущей версии Windows Internet Explorer см. в [центре разработчиков Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="af033-122">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

## <a name="examples"></a><span data-ttu-id="af033-123">Примеры:</span><span class="sxs-lookup"><span data-stu-id="af033-123">Examples:</span></span>

<span data-ttu-id="af033-124">Чтобы присоединить текст к прямоугольнику, можно ввести следующие строки в `<BODY>` области веб-страницы:</span><span class="sxs-lookup"><span data-stu-id="af033-124">To attach text to a rectangle, you can type the following lines in the `<BODY>` region of your Web page:</span></span>


```HTML
<body>
<v:rect style='width:120pt;height:80pt;' fillcolor="red">
<v:textbox>
I'm attaching some text to this shape!!!
</v:textbox>
</v:rect>
</body>
```





<span data-ttu-id="af033-125">Чтобы присоединить гиперссылку к скругленному прямоугольнику, который заполнен градиентом, можно ввести следующие строки в `<BODY>` области веб-страницы:</span><span class="sxs-lookup"><span data-stu-id="af033-125">To attach a hyperlink to a rounded rectangle that is gradient-filled, you can type the following lines in the `<BODY>` region of your Web page:</span></span>

![textbox2.gif (1147 байт)](images/textbox2.gif)


```HTML
<body>
<v:roundrect style='width:80pt;height:30pt;' fillcolor="red">
<v:fill type="gradient" />
<v:textbox>
<a href="https://home.microsoft.com/"> Click here</a>
</v:textbox>
</v:roundrect>
</body>
```





<span data-ttu-id="af033-127">Дополнительные сведения об этом элементе см. в [спецификации VML](https://www.w3.org/TR/NOTE-VML#-toc416858397) .</span><span class="sxs-lookup"><span data-stu-id="af033-127">For more information about this element, see the [VML specification](https://www.w3.org/TR/NOTE-VML#-toc416858397) .</span></span>

 

 