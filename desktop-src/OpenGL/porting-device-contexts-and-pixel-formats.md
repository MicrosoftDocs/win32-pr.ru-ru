---
title: Перенос контекстов устройств и форматов пикселей
description: Перенос контекстов устройств и форматов пикселей
ms.assetid: b60cac27-1e2e-4da5-81c4-69446b92f820
keywords:
- перенос в OpenGL, ПКС
- Перенос с OpenGL, Пиксели
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d793c139c6d7a0a0fc85b2e2c36f30176ce9ab6e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "105661511"
---
# <a name="porting-device-contexts-and-pixel-formats"></a><span data-ttu-id="0fd48-105">Перенос контекстов устройств и форматов пикселей</span><span class="sxs-lookup"><span data-stu-id="0fd48-105">Porting Device Contexts and Pixel Formats</span></span>

<span data-ttu-id="0fd48-106">Каждое окно в реализации Microsoft OpenGL для Windows имеет собственный текущий формат пикселей.</span><span class="sxs-lookup"><span data-stu-id="0fd48-106">Each window in the Microsoft implementation of OpenGL for Windows has its own current pixel format.</span></span> <span data-ttu-id="0fd48-107">Формат пикселей определяется структурой данных [**пикселформатдескриптор**](/windows/win32/api/wingdi/ns-wingdi-pixelformatdescriptor) .</span><span class="sxs-lookup"><span data-stu-id="0fd48-107">A pixel format is defined by a [**PIXELFORMATDESCRIPTOR**](/windows/win32/api/wingdi/ns-wingdi-pixelformatdescriptor) data structure.</span></span> <span data-ttu-id="0fd48-108">Так как каждое окно имеет собственный формат пикселей, вы получаете контекст устройства, устанавливаете формат пикселей контекста устройства, а затем создаете контекст визуализации OpenGL для контекста устройства.</span><span class="sxs-lookup"><span data-stu-id="0fd48-108">Because each window has its own pixel format, you obtain a device context, set the pixel format of the device context, and then create an OpenGL rendering context for the device context.</span></span> <span data-ttu-id="0fd48-109">Контекст визуализации автоматически использует формат пикселей контекста устройства.</span><span class="sxs-lookup"><span data-stu-id="0fd48-109">The rendering context automatically uses the pixel format of its device context.</span></span>

<span data-ttu-id="0fd48-110">Система Window X также использует структуру данных **ксвисуалинфо** для указания свойств пикселей в окне.</span><span class="sxs-lookup"><span data-stu-id="0fd48-110">The X Window System also uses a data structure, **XVisualInfo**, to specify the properties of pixels in a window.</span></span> <span data-ttu-id="0fd48-111">Структуры **ксвисуалинфо** содержат **визуальную** структуру данных, которая описывает, как ресурсы цвета используются на конкретном экране.</span><span class="sxs-lookup"><span data-stu-id="0fd48-111">**XVisualInfo** structures contain a **Visual** data structure that describes how color resources are used in a specific screen.</span></span>

<span data-ttu-id="0fd48-112">В системе Window X **ксвисуалинфо** используется для создания окна путем задания в окне нужного формата пикселей.</span><span class="sxs-lookup"><span data-stu-id="0fd48-112">In the X Window System, **XVisualInfo** is used to create a window by setting the window to the pixel format you want.</span></span> <span data-ttu-id="0fd48-113">Возвращаемая структура используется для создания окна и контекста отрисовки.</span><span class="sxs-lookup"><span data-stu-id="0fd48-113">The returned structure is used to create the window and a rendering context.</span></span> <span data-ttu-id="0fd48-114">В Windows сначала необходимо создать окно и получить маркер контекста устройства (HDC) окна.</span><span class="sxs-lookup"><span data-stu-id="0fd48-114">In Windows, you first create a window and get a handle to a device context (HDC) of the window.</span></span> <span data-ttu-id="0fd48-115">Затем для задания формата пикселей для окна используется параметр HDC.</span><span class="sxs-lookup"><span data-stu-id="0fd48-115">The HDC is then used to set the pixel format for the window.</span></span> <span data-ttu-id="0fd48-116">Контекст визуализации использует формат пикселей окна.</span><span class="sxs-lookup"><span data-stu-id="0fd48-116">The rendering context uses the pixel format of the window.</span></span>

<span data-ttu-id="0fd48-117">В следующей таблице сравниваются система Window X и ГЛКС визуальные функции с их эквивалентными функциями формата пикселей Windows.</span><span class="sxs-lookup"><span data-stu-id="0fd48-117">The following table compares the X Window System and GLX visual functions with their equivalent Windows pixel format functions.</span></span>



| <span data-ttu-id="0fd48-118">Визуальная функция X Window/ГЛКС</span><span class="sxs-lookup"><span data-stu-id="0fd48-118">X window/GLX visual function</span></span>                                                                                     | <span data-ttu-id="0fd48-119">Функция формата пикселей Windows</span><span class="sxs-lookup"><span data-stu-id="0fd48-119">Windows pixel format function</span></span>                                                                                                      |
|------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0fd48-120">Ксвисуалинфо \* **глксчусевисуал**(экран *\* ДПИ*, int *Screen*, int *\* аттриблист*)</span><span class="sxs-lookup"><span data-stu-id="0fd48-120">XVisualInfo\***glXChooseVisual**( Display *\*dpy*,int *screen*,int *\*attribList*)</span></span>                               | <span data-ttu-id="0fd48-121">int [**чусепикселформат**](/windows/desktop/api/wingdi/nf-wingdi-choosepixelformat)(HDC *HDC*, пикселформатдескриптор *\* ппфд*)</span><span class="sxs-lookup"><span data-stu-id="0fd48-121">int [**ChoosePixelFormat**](/windows/desktop/api/wingdi/nf-wingdi-choosepixelformat)( HDC *hdc*,PIXELFORMATDESCRIPTOR *\*ppfd*)</span></span>                                      |
| <span data-ttu-id="0fd48-122">int **глксжетконфиг**(отображение *\* ДПИ*, ксвисуалинфо *\* обратитесь*, int *\* аттриблист*, int *\* value*)</span><span class="sxs-lookup"><span data-stu-id="0fd48-122">int **glXGetConfig**( Display *\*dpy*,XVisualInfo *\*vis*,int *\*attribList*,int *\*value*)</span></span>                      | <span data-ttu-id="0fd48-123">int [**дескрибепикселформат**](/windows/desktop/api/wingdi/nf-wingdi-describepixelformat)(HDC *HDC*, int *ипикселформат*, uint *nBytes*, лппикселформатдескриптор *ппфд*)</span><span class="sxs-lookup"><span data-stu-id="0fd48-123">int [**DescribePixelFormat**](/windows/desktop/api/wingdi/nf-wingdi-describepixelformat)( HDC *hdc*,int *iPixelFormat*,UINT *nBytes*,LPPIXELFORMATDESCRIPTOR *ppfd*)</span></span> |
| <span data-ttu-id="0fd48-124">Ксвисуалинфо \* **ксжетвисуалинфо**(отображение *\* ДПИ*, длинная *Винфо \_ Маска*, ксвисуалинфо *\* Винфо \_ TEMP*, int *\* нитемс*)</span><span class="sxs-lookup"><span data-stu-id="0fd48-124">XVisualInfo\***XGetVisualInfo**( Display *\*dpy*,long *vinfo\_mask*,XVisualInfo *\*vinfo\_templ*,int *\*nitems*)</span></span> | <span data-ttu-id="0fd48-125">int [**жетпикселформат**](/windows/desktop/api/wingdi/nf-wingdi-getpixelformat)(HDC *HDC*)</span><span class="sxs-lookup"><span data-stu-id="0fd48-125">int [**GetPixelFormat**](/windows/desktop/api/wingdi/nf-wingdi-getpixelformat)( HDC *hdc*)</span></span>                                                                           |
| <span data-ttu-id="0fd48-126">*Визуальный* элемент, возвращаемый функцией **глксчусевисуал** , используется при создании окна.</span><span class="sxs-lookup"><span data-stu-id="0fd48-126">The *visual* returned by **glxChooseVisual** is used when a window is created.</span></span>                                   | <span data-ttu-id="0fd48-127">BOOL [**сетпикселформат**](/windows/desktop/api/wingdi/nf-wingdi-setpixelformat)(HDC *HDC*, int *ипикселформат*, пикселформатдескриптор *\* ппфд*)</span><span class="sxs-lookup"><span data-stu-id="0fd48-127">BOOL [**SetPixelFormat**](/windows/desktop/api/wingdi/nf-wingdi-setpixelformat)( HDC *hdc*,int *iPixelFormat*,PIXELFORMATDESCRIPTOR *\*ppfd*)</span></span>                        |



 

<span data-ttu-id="0fd48-128">В следующих разделах приведены примеры фрагментов кода формата пикселей для программы X Window System и того же кода после переноса в Windows.</span><span class="sxs-lookup"><span data-stu-id="0fd48-128">The following sections give examples of pixel format code fragments for an X Window System program, and the same code after it has been ported to Windows.</span></span>

-   [<span data-ttu-id="0fd48-129">Пример кода формата пикселей ГЛКС</span><span class="sxs-lookup"><span data-stu-id="0fd48-129">GLX Pixel Format Code Sample</span></span>](glx-pixel-format-code-sample.md)
-   [<span data-ttu-id="0fd48-130">Пример кода формата пикселей Windows</span><span class="sxs-lookup"><span data-stu-id="0fd48-130">Windows Pixel Format Code Sample</span></span>](win32-pixel-format-code-sample.md)

<span data-ttu-id="0fd48-131">Дополнительные сведения о форматах пикселей см. в разделе [форматы пикселей](pixel-formats.md).</span><span class="sxs-lookup"><span data-stu-id="0fd48-131">For more information on pixel formats, see [Pixel Formats](pixel-formats.md).</span></span>

 

 




