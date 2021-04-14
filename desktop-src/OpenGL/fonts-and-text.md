---
title: Шрифты и текст (OpenGL)
description: Реализация OpenGL в Windows (Майкрософт) поддерживает графический интерфейс GDI в окне OpenGL с одним буфером.
ms.assetid: 25a45e1a-6c1e-416b-8993-daeefc1100f3
keywords:
- OpenGL в Windows, шрифты
- OpenGL в Windows, текст
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d6fba4ffe996bd88a6285f615ddacb31e57fc311
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/10/2020
ms.locfileid: "104414540"
---
# <a name="fonts-and-text-opengl"></a><span data-ttu-id="75ab1-105">Шрифты и текст (OpenGL)</span><span class="sxs-lookup"><span data-stu-id="75ab1-105">Fonts and Text (OpenGL)</span></span>

<span data-ttu-id="75ab1-106">Реализация OpenGL в Windows (Майкрософт) поддерживает графический интерфейс GDI в окне OpenGL с одним буфером.</span><span class="sxs-lookup"><span data-stu-id="75ab1-106">Microsoft's implementation of OpenGL in Windows supports GDI graphics in a single-buffered OpenGL window.</span></span> <span data-ttu-id="75ab1-107">Она не поддерживает графический интерфейс GDI в окне OpenGL с двойной буферизацией.</span><span class="sxs-lookup"><span data-stu-id="75ab1-107">It does not support GDI graphics in a double-buffered OpenGL window.</span></span> <span data-ttu-id="75ab1-108">Таким же путем можно вызывать только стандартные текстовые функции GDI и Text для рисования текста в однобуферном окне OpenGL. Эти функции нельзя вызывать для рисования текста в окне OpenGL с двойной буферизацией.</span><span class="sxs-lookup"><span data-stu-id="75ab1-108">Thus, you can call only the standard GDI font and text functions to draw text in a single-buffered OpenGL window; you cannot call those functions to draw text in a double-buffered OpenGL window.</span></span>

<span data-ttu-id="75ab1-109">Существует обходное решение для этого ограничения текста в окнах с двойной буферизацией: Построение списков отображения OpenGL для растровых изображений символов, а затем выполнение этих списков отображения для рисования символов.</span><span class="sxs-lookup"><span data-stu-id="75ab1-109">There is a workaround for this restriction on text in double-buffered windows: build OpenGL display lists for bitmap images of characters, and then execute those display lists to draw characters.</span></span> <span data-ttu-id="75ab1-110">Этот процесс состоит из трех основных этапов.</span><span class="sxs-lookup"><span data-stu-id="75ab1-110">There are three main steps in this process:</span></span>

1.  <span data-ttu-id="75ab1-111">Выберите шрифт для контекста устройства, задав необходимые свойства шрифта.</span><span class="sxs-lookup"><span data-stu-id="75ab1-111">Select a font for a device context, setting the font's properties as desired.</span></span>
2.  <span data-ttu-id="75ab1-112">Создание набора растровых списков отображения на основе глифов в шрифте контекста устройства — один список отображения для каждого глифа, который будет нарисован приложением.</span><span class="sxs-lookup"><span data-stu-id="75ab1-112">Create a set of bitmap display lists based on the glyphs in the device context's font, one display list for each glyph that the application will draw.</span></span>
3.  <span data-ttu-id="75ab1-113">Нарисуйте каждый знак в строке с помощью этих списков отображения растровых изображений.</span><span class="sxs-lookup"><span data-stu-id="75ab1-113">Draw each glyph in a string, using those bitmap display lists.</span></span>

<span data-ttu-id="75ab1-114">Чтобы создать списки вывода, вызовите функции [**вглусефонтбитмапс**](/windows/desktop/api/wingdi/nf-wingdi-wglusefontbitmapsa) и [**вглусефонтаутлинес**](/windows/desktop/api/wingdi/nf-wingdi-wglusefontoutlinesa) .</span><span class="sxs-lookup"><span data-stu-id="75ab1-114">To create the display lists, call the [**wglUseFontBitmaps**](/windows/desktop/api/wingdi/nf-wingdi-wglusefontbitmapsa) and [**wglUseFontOutlines**](/windows/desktop/api/wingdi/nf-wingdi-wglusefontoutlinesa) functions.</span></span> <span data-ttu-id="75ab1-115">Для рисования символов в строке с помощью этих списков отображения вызовите [**глкалллистс**](glcalllists.md).</span><span class="sxs-lookup"><span data-stu-id="75ab1-115">To draw characters in a string using those display lists, call [**glCallLists**](glcalllists.md).</span></span>

<span data-ttu-id="75ab1-116">Для создания приложений, которые просты в локализации и используют ресурсы с осторожностью, необходимо тщательно управлять созданием и хранением этих списков изображений глифов.</span><span class="sxs-lookup"><span data-stu-id="75ab1-116">To create applications that are easy to localize and that use resources sparingly, the creation and storage of these glyph image display lists must be managed carefully.</span></span> <span data-ttu-id="75ab1-117">Многие языки, в отличие от английского, имеют алфавиты, коды символов которых находятся по относительно большому набору значений.</span><span class="sxs-lookup"><span data-stu-id="75ab1-117">Many languages, unlike English, have alphabets whose character codes range over a relatively large set of values.</span></span>

## <a name="related-topics"></a><span data-ttu-id="75ab1-118">См. также</span><span class="sxs-lookup"><span data-stu-id="75ab1-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="75ab1-119">Функции шрифта и текста</span><span class="sxs-lookup"><span data-stu-id="75ab1-119">Font and Text Functions</span></span>](font-and-text-functions.md)
</dt> </dl>

 

 




