---
title: Форматы пикселей
description: Форматы пикселей
ms.assetid: 2e179340-c487-4b72-a22e-078b800af11d
keywords:
- OpenGL в Windows, ПКС
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7d16f9f78edc0cf935fb602de8d88792091588ce
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "105661643"
---
# <a name="pixel-formats"></a><span data-ttu-id="cc485-104">Форматы пикселей</span><span class="sxs-lookup"><span data-stu-id="cc485-104">Pixel Formats</span></span>

<span data-ttu-id="cc485-105">*Формат пикселей* определяет несколько свойств поверхности рисования OpenGL.</span><span class="sxs-lookup"><span data-stu-id="cc485-105">A *pixel format* specifies several properties of an OpenGL drawing surface.</span></span> <span data-ttu-id="cc485-106">Некоторые свойства, заданные в формате пикселей:</span><span class="sxs-lookup"><span data-stu-id="cc485-106">Some of the properties specified by a pixel format are:</span></span>

-   <span data-ttu-id="cc485-107">Указывает, является ли точечный буфер одиночным или двойным буфером.</span><span class="sxs-lookup"><span data-stu-id="cc485-107">Whether the pixel buffer is single- or double-buffered.</span></span>
-   <span data-ttu-id="cc485-108">Указывает, находятся ли данные пикселей в форме RGBA или цветового индекса.</span><span class="sxs-lookup"><span data-stu-id="cc485-108">Whether the pixel data is in RGBA or color-index form.</span></span>
-   <span data-ttu-id="cc485-109">Число битов, используемых для хранения данных цвета.</span><span class="sxs-lookup"><span data-stu-id="cc485-109">The number of bits used to store color data.</span></span>
-   <span data-ttu-id="cc485-110">Число битов, используемых для глубины (оси z).</span><span class="sxs-lookup"><span data-stu-id="cc485-110">The number of bits used for the depth (z-axis) buffer.</span></span>
-   <span data-ttu-id="cc485-111">Число битов, используемых для буфера шаблона.</span><span class="sxs-lookup"><span data-stu-id="cc485-111">The number of bits used for the stencil buffer.</span></span>
-   <span data-ttu-id="cc485-112">Число плоскостей и ундерлай плоскости.</span><span class="sxs-lookup"><span data-stu-id="cc485-112">The number of overlay and underlay planes.</span></span>
-   <span data-ttu-id="cc485-113">Различные маски видимости.</span><span class="sxs-lookup"><span data-stu-id="cc485-113">Various visibility masks.</span></span>

<span data-ttu-id="cc485-114">Реализация OpenGL для Windows в корпорации Майкрософт использует структуру данных [**пикселформатдескриптор**](/windows/win32/api/wingdi/ns-wingdi-pixelformatdescriptor) для передачи данных в формате пикселей.</span><span class="sxs-lookup"><span data-stu-id="cc485-114">Microsoft's implementation of OpenGL for Windows uses the [**PIXELFORMATDESCRIPTOR**](/windows/win32/api/wingdi/ns-wingdi-pixelformatdescriptor) data structure to convey pixel format data.</span></span> <span data-ttu-id="cc485-115">Члены структуры задают предыдущие свойства и несколько других.</span><span class="sxs-lookup"><span data-stu-id="cc485-115">The structure's members specify the preceding properties and several others.</span></span>

<span data-ttu-id="cc485-116">Данный контекст устройства может поддерживать несколько форматов пикселей.</span><span class="sxs-lookup"><span data-stu-id="cc485-116">A given device context can support several pixel formats.</span></span> <span data-ttu-id="cc485-117">Windows определяет форматы пикселей, которые поддерживает контекст устройства, с последовательными значениями индекса, основанными на единицах (1, 2, 3, 4 и т. д.).</span><span class="sxs-lookup"><span data-stu-id="cc485-117">Windows identifies the pixel formats that a device context supports with consecutive one-based index values (1, 2, 3, 4, and so on).</span></span> <span data-ttu-id="cc485-118">Контекст устройства может иметь только один текущий формат пикселей, выбранный из набора поддерживаемых форматами пикселей.</span><span class="sxs-lookup"><span data-stu-id="cc485-118">A device context can have just one current pixel format, chosen from the set of pixel formats it supports.</span></span>

<span data-ttu-id="cc485-119">Каждое окно имеет собственный текущий формат пикселей в OpenGL в Windows.</span><span class="sxs-lookup"><span data-stu-id="cc485-119">Each window has its own current pixel format in OpenGL in Windows.</span></span> <span data-ttu-id="cc485-120">Это означает, например, что приложение может одновременно отображать RGBA и индексируемые окна OpenGL, а также одностраничные окна OpenGL или одиночные и двойные буферы.</span><span class="sxs-lookup"><span data-stu-id="cc485-120">This means, for example, that an application can simultaneously display RGBA and color-index OpenGL windows, or single- and double-buffered OpenGL windows.</span></span> <span data-ttu-id="cc485-121">Возможность использования формата пикселей для каждого окна ограничена окнами OpenGL.</span><span class="sxs-lookup"><span data-stu-id="cc485-121">This per-window pixel format capability is limited to OpenGL windows.</span></span>

<span data-ttu-id="cc485-122">Как правило, вы получаете контекст устройства, устанавливаете формат пикселей контекста устройства, а затем создаете контекст визуализации OpenGL, подходящий для этого устройства.</span><span class="sxs-lookup"><span data-stu-id="cc485-122">Typically, you obtain a device context, set the device context's pixel format, and then create an OpenGL rendering context suitable for that device.</span></span>

> [!Note]  
> <span data-ttu-id="cc485-123">Перед созданием контекста отрисовки необходимо задать формат пикселей, так как контекст визуализации наследует формат пикселей контекста устройства.</span><span class="sxs-lookup"><span data-stu-id="cc485-123">You set the pixel format before creating a rendering context because the rendering context inherits the device context's pixel format.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="cc485-124">См. также</span><span class="sxs-lookup"><span data-stu-id="cc485-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cc485-125">Функции формата пикселей</span><span class="sxs-lookup"><span data-stu-id="cc485-125">Pixel Format Functions</span></span>](pixel-format-functions.md)
</dt> </dl>

 

 




