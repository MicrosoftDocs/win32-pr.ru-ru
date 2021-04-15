---
title: Печать изображения OpenGL
description: Вы можете печатать изображения OpenGL, подготовленные в виде расширенных метафайлов.
ms.assetid: 6099cbe2-82f9-46ec-a3ca-74486c111639
keywords:
- OpenGL в Windows, печать
- Печать изображений OpenGL OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2ca0c5260a084796915a7564f793f0e252b5228c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "105661774"
---
# <a name="printing-an-opengl-image"></a><span data-ttu-id="37e04-105">Печать изображения OpenGL</span><span class="sxs-lookup"><span data-stu-id="37e04-105">Printing an OpenGL Image</span></span>

<span data-ttu-id="37e04-106">Вы можете печатать изображения OpenGL, подготовленные в виде расширенных метафайлов.</span><span class="sxs-lookup"><span data-stu-id="37e04-106">You can print OpenGL images rendered in enhanced metafiles.</span></span> <span data-ttu-id="37e04-107">При подготовке к просмотру на устройстве печати (HDC) оно должно поддерживаться диспетчером очереди метафайлов.</span><span class="sxs-lookup"><span data-stu-id="37e04-107">When you render to a printer device (HDC) it must be backed by a metafile spooler.</span></span> <span data-ttu-id="37e04-108">OpenGL использует память для глубины, цвета и других буферов для хранения выходных данных графики на принтере.</span><span class="sxs-lookup"><span data-stu-id="37e04-108">OpenGL uses memory for depth, color, and other buffers to store graphics output to a printer.</span></span> <span data-ttu-id="37e04-109">Так как для обычного разрешения принтера требуется значительный объем памяти для хранения графических данных, печать изображения OpenGL может потребовать больше памяти, чем доступно в системе.</span><span class="sxs-lookup"><span data-stu-id="37e04-109">Because typical printer resolution requires a significant amount of memory to store the graphics output, printing an OpenGL image might require more memory than is available in the system.</span></span> <span data-ttu-id="37e04-110">Чтобы преодолеть это ограничение, текущая реализация OpenGL печатает графики OpenGL в полосах.</span><span class="sxs-lookup"><span data-stu-id="37e04-110">To overcome this limitation, the current implementation of OpenGL prints OpenGL graphics in bands.</span></span> <span data-ttu-id="37e04-111">Однако это увеличивает время, затрачиваемое на печать изображений OpenGL.</span><span class="sxs-lookup"><span data-stu-id="37e04-111">However, this increases the time it takes to print OpenGL images.</span></span>

<span data-ttu-id="37e04-112">Перед печатью образа OpenGL необходимо вызвать функцию [стартдок](/windows/desktop/api/wingdi/nf-wingdi-startdoca) для завершения инициализации контекста устройства печати (DC).</span><span class="sxs-lookup"><span data-stu-id="37e04-112">Before you print an OpenGL image, you must call the [StartDoc](/windows/desktop/api/wingdi/nf-wingdi-startdoca) function to complete the initialization of a printer device context (DC).</span></span> <span data-ttu-id="37e04-113">После вызова **стартдок** можно создать контексты отрисовки (хглрк) для подготовки к просмотру на устройстве принтера.</span><span class="sxs-lookup"><span data-stu-id="37e04-113">After calling **StartDoc**, you can create rendering contexts (HGLRC) to render to the printer device.</span></span> <span data-ttu-id="37e04-114">Если вы создаете контексты подготовки к просмотру перед вызовом **стартдок**, не существует способа определить, помещен ли в очередь метафайл.</span><span class="sxs-lookup"><span data-stu-id="37e04-114">If you create rendering contexts before calling **StartDoc**, there is no way to determine whether a metafile is spooled.</span></span>

<span data-ttu-id="37e04-115">В следующем примере кода показано, как напечатать изображение OpenGL:</span><span class="sxs-lookup"><span data-stu-id="37e04-115">The following code sample shows how to print an OpenGL image:</span></span>

``` syntax
HDC            hDC;
DOCINFO        di;
HGLRC          hglrc;

// Call StartDoc to start the document 
StartDoc( hDC, &di );

// Prepare the printer driver to accept data 
StartPage(hDC);

// Create a rendering context using the metafile DC 
hglrc = wglCreateContext ( hDCmetafile );

// Do OpenGL rendering operations here 
    . . .
wglMakeCurrent(NULL, NULL); // Get rid of rendering context 
    . . .
EndPage(hDC); // Finish writing to the page 
EndDoc(hDC); // End the print job
```

<span data-ttu-id="37e04-116">Дополнительные сведения об использовании метафайлов см. в разделе [операции расширенного метафайла](/windows/desktop/gdi/enhanced-metafile-operations).</span><span class="sxs-lookup"><span data-stu-id="37e04-116">For more information on using metafiles, see [Enhanced Metafile Operations](/windows/desktop/gdi/enhanced-metafile-operations).</span></span>

 

 