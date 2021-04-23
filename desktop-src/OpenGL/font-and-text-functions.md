---
title: Функции шрифтов и текста (OpenGL)
description: Для управления шрифтами и текстом можно использовать следующие функции.
ms.assetid: 42e16967-1eeb-4d37-bbd6-33c473eb2757
keywords:
- Функции ВГЛ, текст
- Функции ВГЛ, шрифт
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e205549346cccc2c44b7670db91530cfbc24017d
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/10/2020
ms.locfileid: "104414541"
---
# <a name="font-and-text-functions-opengl"></a><span data-ttu-id="89dc0-105">Функции шрифтов и текста (OpenGL)</span><span class="sxs-lookup"><span data-stu-id="89dc0-105">Font and Text Functions (OpenGL)</span></span>

<span data-ttu-id="89dc0-106">Для управления шрифтами и текстом можно использовать следующие функции.</span><span class="sxs-lookup"><span data-stu-id="89dc0-106">The following functions can be used to manage fonts and text.</span></span>



| <span data-ttu-id="89dc0-107">Функция Windows</span><span class="sxs-lookup"><span data-stu-id="89dc0-107">Windows Function</span></span>                                 | <span data-ttu-id="89dc0-108">Описание</span><span class="sxs-lookup"><span data-stu-id="89dc0-108">Description</span></span>                                                                                                                                                                                                                      |
|--------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="89dc0-109">**вглусефонтбитмапс**</span><span class="sxs-lookup"><span data-stu-id="89dc0-109">**wglUseFontBitmaps**</span></span>](/windows/desktop/api/wingdi/nf-wingdi-wglusefontbitmapsa)   | <span data-ttu-id="89dc0-110">Создает набор списков вывода точечных рисунков символов.</span><span class="sxs-lookup"><span data-stu-id="89dc0-110">Creates a set of character bitmap display lists.</span></span> <span data-ttu-id="89dc0-111">Символы берутся из текущего шрифта указанного контекста устройства.</span><span class="sxs-lookup"><span data-stu-id="89dc0-111">Characters come from a specified device context's current font.</span></span> <span data-ttu-id="89dc0-112">Символы указываются в виде последовательных запусков в наборе глифов шрифта.</span><span class="sxs-lookup"><span data-stu-id="89dc0-112">Characters are specified as a consecutive run within the font's glyph set.</span></span>                                      |
| [<span data-ttu-id="89dc0-113">**вглусефонтаутлинес**</span><span class="sxs-lookup"><span data-stu-id="89dc0-113">**wglUseFontOutlines**</span></span>](/windows/desktop/api/wingdi/nf-wingdi-wglusefontoutlinesa) | <span data-ttu-id="89dc0-114">Создает набор списков отображения на основе глифов текущего выбранного шрифта контекста устройства для использования с текущим контекстом отрисовки.</span><span class="sxs-lookup"><span data-stu-id="89dc0-114">Creates a set of display lists, based on the glyphs of the currently selected outline font of a device context, for use with the current rendering context.</span></span> <span data-ttu-id="89dc0-115">Списки отображения используются для рисования трехмерных символов шрифтов TrueType.</span><span class="sxs-lookup"><span data-stu-id="89dc0-115">The display lists are used to draw 3-D characters of TrueType fonts.</span></span> |



 

<span data-ttu-id="89dc0-116">Функции **вглусефонтбитмапс** и **вглусефонтаутлинес** принимают маркер контекста устройства и используют текущий шрифт контекста устройства в качестве источника растровых изображений.</span><span class="sxs-lookup"><span data-stu-id="89dc0-116">The **wglUseFontBitmaps** and **wglUseFontOutlines** functions take a handle to a device context, and use that device context's current font as a source for the bitmaps.</span></span> <span data-ttu-id="89dc0-117">Поэтому необходимо задать шрифт контекста устройства и свойства шрифта перед вызовом **вглусефонтбитмапс** или **вглусефонтаутлинес**.</span><span class="sxs-lookup"><span data-stu-id="89dc0-117">It is therefore necessary to set the device context's font and the font's properties before calling **wglUseFontBitmaps** or **wglUseFontOutlines**.</span></span>

<span data-ttu-id="89dc0-118">Функции [**вглусефонтбитмапс**](/windows/desktop/api/wingdi/nf-wingdi-wglusefontbitmapsa) и [**вглусефонтаутлинес**](/windows/desktop/api/wingdi/nf-wingdi-wglusefontoutlinesa) также принимают параметр, который превращает первый глиф в шрифте в список отображения растрового изображения, и параметр, указывающий количество глифов для включения в списки отображения.</span><span class="sxs-lookup"><span data-stu-id="89dc0-118">The [**wglUseFontBitmaps**](/windows/desktop/api/wingdi/nf-wingdi-wglusefontbitmapsa) and [**wglUseFontOutlines**](/windows/desktop/api/wingdi/nf-wingdi-wglusefontoutlinesa) functions also take a parameter that turns the first glyph in the font into a bitmap display list, and a parameter that specifies how many glyphs to turn into display lists.</span></span> <span data-ttu-id="89dc0-119">Затем функция создает списки вывода для указанного последовательно выполняемого выполнения глифов.</span><span class="sxs-lookup"><span data-stu-id="89dc0-119">The function then creates display lists for the specified consecutive run of glyphs.</span></span> <span data-ttu-id="89dc0-120">Пример:</span><span class="sxs-lookup"><span data-stu-id="89dc0-120">For example:</span></span>

-   <span data-ttu-id="89dc0-121">Чтобы создать набор из 224 растровых списков вывода для всех глифов набора символов Windows, установите эти два параметра равными 32 и 224 соответственно.</span><span class="sxs-lookup"><span data-stu-id="89dc0-121">To create a set of 224 bitmap display lists for all of the Windows character set glyphs, set these two parameters to 32 and 224, respectively.</span></span>
-   <span data-ttu-id="89dc0-122">Чтобы создать набор из 256 растровых списков вывода для всех глифов набора символов OEM, задайте для этих двух параметров значение 0 и 256 соответственно.</span><span class="sxs-lookup"><span data-stu-id="89dc0-122">To create a set of 256 bitmap display lists for all of the OEM character set glyphs, set these two parameters to 0 and 256, respectively.</span></span>
-   <span data-ttu-id="89dc0-123">Чтобы создать один растровый список для одного глифа набора символов, задайте для второго из этих параметров значение 1.</span><span class="sxs-lookup"><span data-stu-id="89dc0-123">To create a single bitmap display list for any single character set glyph, set the second of these parameters to 1.</span></span>

<span data-ttu-id="89dc0-124">Функции **вглусефонтбитмапс** и **вглусефонтаутлинес** представляют нулевой глиф в шрифте с пустым списком отображения.</span><span class="sxs-lookup"><span data-stu-id="89dc0-124">The **wglUseFontBitmaps** and **wglUseFontOutlines** functions represent a null glyph in a font with an empty display list.</span></span>

<span data-ttu-id="89dc0-125">Списки отображений, созданные при вызове **вглусефонтбитмапс** или **вглусефонтаутлинес** , автоматически нумеруются последовательно.</span><span class="sxs-lookup"><span data-stu-id="89dc0-125">The display lists created by a call to **wglUseFontBitmaps** or **wglUseFontOutlines** are automatically numbered consecutively.</span></span>

<span data-ttu-id="89dc0-126">После вызова функции [**вглусефонтбитмапс**](/windows/desktop/api/wingdi/nf-wingdi-wglusefontbitmapsa) или [**Вглусефонтаутлинес**](/windows/desktop/api/wingdi/nf-wingdi-wglusefontoutlinesa) вызовите [**глкалллистс**](glcalllists.md) , чтобы нарисовать строку символов.</span><span class="sxs-lookup"><span data-stu-id="89dc0-126">After calling the [**wglUseFontBitmaps**](/windows/desktop/api/wingdi/nf-wingdi-wglusefontbitmapsa) or [**wglUseFontOutlines**](/windows/desktop/api/wingdi/nf-wingdi-wglusefontoutlinesa) function, call [**glCallLists**](glcalllists.md) to draw a string of characters.</span></span> <span data-ttu-id="89dc0-127">Пример кода см. [в разделе Рисование текста в Double-Buffered окне OpenGL](drawing-text-in-a-double-buffered-opengl-window.md) .</span><span class="sxs-lookup"><span data-stu-id="89dc0-127">See [Drawing Text in a Double-Buffered OpenGL Window](drawing-text-in-a-double-buffered-opengl-window.md) for sample code.</span></span> <span data-ttu-id="89dc0-128">В этом контексте **глкалллистс** использует каждый символ в строке в качестве индекса в массиве последовательно пронумерованных списков вывода, созданных **вглусефонтбитмапс** или **вглусефонтаутлинес**.</span><span class="sxs-lookup"><span data-stu-id="89dc0-128">In this context, **glCallLists** uses each character in a string as an index into the array of consecutively numbered display lists created by **wglUseFontBitmaps** or **wglUseFontOutlines**.</span></span>

<span data-ttu-id="89dc0-129">После завершения рисования текста вызовите функцию [**глделетелистс**](gldeletelists.md) , чтобы освободить непрерывный набор списков отображения, созданных **вглусефонтбитмапс** и **вглусефонтаутлинес**.</span><span class="sxs-lookup"><span data-stu-id="89dc0-129">When you finish drawing text, call the [**glDeleteLists**](gldeletelists.md) function to release the contiguous set of display lists created by **wglUseFontBitmaps** and **wglUseFontOutlines**.</span></span>

 

 




