---
title: Передний, задний и другие буферы
description: OpenGL хранит данные пикселей и управляет ими в буфера кадров.
ms.assetid: 4af6a5e4-cc62-49e5-a4d5-e54b1348e8fe
keywords:
- OpenGL в Windows, буферы
- фрамебуфферс OpenGL
- цветовые буферы OpenGL
- буферы глубины OpenGL
- накопление буферов OpenGL
- буферы трафаретов OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fea487b73af356853bee2054db292cdfe740bd16
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104411083"
---
# <a name="front-back-and-other-buffers"></a><span data-ttu-id="2eb15-109">Передний, задний и другие буферы</span><span class="sxs-lookup"><span data-stu-id="2eb15-109">Front, Back, and Other Buffers</span></span>

<span data-ttu-id="2eb15-110">OpenGL хранит данные пикселей и управляет ими в буфера кадров.</span><span class="sxs-lookup"><span data-stu-id="2eb15-110">OpenGL stores and manipulates pixel data in a framebuffer.</span></span> <span data-ttu-id="2eb15-111">Буфера кадров состоит из набора логических буферов: цвета, глубины, накопления и буферов трафаретов.</span><span class="sxs-lookup"><span data-stu-id="2eb15-111">The framebuffer consists of a set of logical buffers: color, depth, accumulation, and stencil buffers.</span></span> <span data-ttu-id="2eb15-112">Сам буфер цвета состоит из набора логических буферов; Этот набор может включать передний левый, передний правый, задний левый порядок и некоторое количество вспомогательных буферов.</span><span class="sxs-lookup"><span data-stu-id="2eb15-112">The color buffer itself consists of a set of logical buffers; this set can include a front-left, a front-right, a back-left, a back-right, and some number of auxiliary buffers.</span></span> <span data-ttu-id="2eb15-113">В определенном формате пикселей или реализации OpenGL не все эти буферы могут быть предоставлены.</span><span class="sxs-lookup"><span data-stu-id="2eb15-113">A particular pixel format or OpenGL implementation may not supply all of these buffers.</span></span> <span data-ttu-id="2eb15-114">Например, текущая версия реализации OpenGL в Windows не поддерживает образы стереоскопик, поэтому формат пикселей не может иметь буферы нелевого и правого цвета.</span><span class="sxs-lookup"><span data-stu-id="2eb15-114">For example, the current version of Microsoft's implementation of OpenGL in Windows does not support stereoscopic images, so a pixel format cannot have left and right color buffers.</span></span> <span data-ttu-id="2eb15-115">Кроме того, текущая версия не поддерживает вспомогательные буферы.</span><span class="sxs-lookup"><span data-stu-id="2eb15-115">In addition, the current version does not support auxiliary buffers.</span></span> <span data-ttu-id="2eb15-116">Дополнительные сведения о буферах OpenGL и функциях OpenGL, которые работают с ними, см. в *справочном руководстве по OpenGL* и *руководстве по программированию OpenGL*.</span><span class="sxs-lookup"><span data-stu-id="2eb15-116">For more information on OpenGL buffers and the OpenGL functions that operate on them, see the *OpenGL Reference Manual* and the *OpenGL Programming Guide*.</span></span>

<span data-ttu-id="2eb15-117">Реализация OpenGL в Windows (Майкрософт) поддерживает двойную буферизацию изображений.</span><span class="sxs-lookup"><span data-stu-id="2eb15-117">Microsoft's implementation of OpenGL in Windows supports double buffering of images.</span></span> <span data-ttu-id="2eb15-118">Это методика, при которой приложение рисует Пиксели в буфере экрана, а затем, когда этот образ готов к отображению, копирует содержимое буфера вне экрана в буфер экрана.</span><span class="sxs-lookup"><span data-stu-id="2eb15-118">This is a technique in which an application draws pixels to an off-screen buffer, and then, when that image is ready for display, copies the contents of the off-screen buffer to an on-screen buffer.</span></span> <span data-ttu-id="2eb15-119">Двойная буферизация обеспечивает плавные изменения изображений, которые особенно важны для анимированных изображений.</span><span class="sxs-lookup"><span data-stu-id="2eb15-119">Double buffering enables smooth image changes, which are especially important for animated images.</span></span>

<span data-ttu-id="2eb15-120">Для приложений, использующих двойную буферизацию, доступны два цветовых буфера: интерфейсный буфер и задний буфер.</span><span class="sxs-lookup"><span data-stu-id="2eb15-120">Two color buffers are available to applications that use double buffering: a front buffer and a back buffer.</span></span> <span data-ttu-id="2eb15-121">По умолчанию команды рисования направляются в задний буфер (буфер, расположенный за пределами экрана), а внешний буфер отображается на экране.</span><span class="sxs-lookup"><span data-stu-id="2eb15-121">By default, drawing commands are directed to the back buffer (the off-screen buffer), while the front buffer is displayed on the screen.</span></span> <span data-ttu-id="2eb15-122">Когда буфер экрана готов для отображения, вызывается [**свапбуфферс**](/windows/desktop/api/wingdi/nf-wingdi-swapbuffers), и Windows копирует содержимое буфера из экрана в буфер экрана.</span><span class="sxs-lookup"><span data-stu-id="2eb15-122">When the off-screen buffer is ready for display, you call [**SwapBuffers**](/windows/desktop/api/wingdi/nf-wingdi-swapbuffers), and Windows copies the contents of the off-screen buffer to the on-screen buffer.</span></span>

<span data-ttu-id="2eb15-123">Универсальная реализация использует аппаратно-независимый точечный рисунок (DIB) в качестве заднего буфера, а экран отображается как интерфейсный буфер.</span><span class="sxs-lookup"><span data-stu-id="2eb15-123">The generic implementation uses a device-independent bitmap (DIB) as the back buffer and the screen display as the front buffer.</span></span> <span data-ttu-id="2eb15-124">Аппаратные устройства и их драйверы могут использовать разные подходы.</span><span class="sxs-lookup"><span data-stu-id="2eb15-124">Hardware devices and their drivers may use different approaches.</span></span>

<span data-ttu-id="2eb15-125">Двойная буферизация — это свойство в формате пикселей.</span><span class="sxs-lookup"><span data-stu-id="2eb15-125">Double buffering is a pixel-format property.</span></span> <span data-ttu-id="2eb15-126">Чтобы запросить двойную буферизацию для формата пикселей, установите флаг ПФД \_ даублебуффер в структуре данных [**пикселформатдескриптор**](/windows/win32/api/wingdi/ns-wingdi-pixelformatdescriptor) в вызове [**чусепикселформат**](/windows/desktop/api/wingdi/nf-wingdi-choosepixelformat).</span><span class="sxs-lookup"><span data-stu-id="2eb15-126">To request double buffering for a pixel format, set the PFD\_DOUBLEBUFFER flag in the [**PIXELFORMATDESCRIPTOR**](/windows/win32/api/wingdi/ns-wingdi-pixelformatdescriptor) data structure in a call to [**ChoosePixelFormat**](/windows/desktop/api/wingdi/nf-wingdi-choosepixelformat).</span></span>

<span data-ttu-id="2eb15-127">Функция OpenGL Core, [**глдравбуффер**](gldrawbuffer.md), выбирает буферы для записи и очистки.</span><span class="sxs-lookup"><span data-stu-id="2eb15-127">The OpenGL core function, [**glDrawBuffer**](gldrawbuffer.md), selects buffers for writing and clearing.</span></span>

## <a name="related-topics"></a><span data-ttu-id="2eb15-128">См. также</span><span class="sxs-lookup"><span data-stu-id="2eb15-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2eb15-129">Функции буфера</span><span class="sxs-lookup"><span data-stu-id="2eb15-129">Buffer Functions</span></span>](buffer-functions.md)
</dt> </dl>

 

 




