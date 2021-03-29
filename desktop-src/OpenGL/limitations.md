---
title: Ограничения
description: Ограничения
ms.assetid: 5f41620d-dde0-4e82-92f0-ada9d4acf127
keywords:
- OpenGL в Windows, ограничения
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 478a139326f74c236ca0109fddbbc3d4ffb46e1a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103775260"
---
# <a name="limitations"></a><span data-ttu-id="48cbe-104">Ограничения</span><span class="sxs-lookup"><span data-stu-id="48cbe-104">Limitations</span></span>

<span data-ttu-id="48cbe-105">Универсальная реализация имеет следующие ограничения.</span><span class="sxs-lookup"><span data-stu-id="48cbe-105">The generic implementation has the following limitations:</span></span>

-   <span data-ttu-id="48cbe-106">Печать.</span><span class="sxs-lookup"><span data-stu-id="48cbe-106">Printing.</span></span>

    <span data-ttu-id="48cbe-107">Изображение OpenGL можно распечатать непосредственно на принтере, используя только метафайлы.</span><span class="sxs-lookup"><span data-stu-id="48cbe-107">You can print an OpenGL image directly to a printer using metafiles only.</span></span> <span data-ttu-id="48cbe-108">Дополнительные сведения см. [в разделе Печать изображения OpenGL](printing-an-opengl-image.md).</span><span class="sxs-lookup"><span data-stu-id="48cbe-108">For more information, see [Printing an OpenGL Image](printing-an-opengl-image.md).</span></span>

-   <span data-ttu-id="48cbe-109">Графические изображения OpenGL и GDI не могут быть смешанными в окне с двойной буферизацией.</span><span class="sxs-lookup"><span data-stu-id="48cbe-109">OpenGL and GDI graphics cannot be mixed in a double-buffered window.</span></span>

    <span data-ttu-id="48cbe-110">Приложение может напрямую рисовать графические изображения OpenGL и GDI в окне с одним буфером, но не в окне двойной буферизации.</span><span class="sxs-lookup"><span data-stu-id="48cbe-110">An application can directly draw both OpenGL graphics and GDI graphics into a single-buffered window, but not into a double-buffered window.</span></span>

-   <span data-ttu-id="48cbe-111">Цветовые палитры оборудования для каждого окна отсутствуют.</span><span class="sxs-lookup"><span data-stu-id="48cbe-111">There are no per-window hardware color palettes.</span></span>

    <span data-ttu-id="48cbe-112">Windows имеет одну системную цветовую палитру, которая применяется ко всему экрану.</span><span class="sxs-lookup"><span data-stu-id="48cbe-112">Windows has a single system hardware color palette, which applies to the whole screen.</span></span> <span data-ttu-id="48cbe-113">Окно OpenGL не может иметь собственную палитру оборудования, но может иметь собственную логическую палитру.</span><span class="sxs-lookup"><span data-stu-id="48cbe-113">An OpenGL window cannot have its own hardware palette, but can have its own logical palette.</span></span> <span data-ttu-id="48cbe-114">Для этого он должен стать приложением, поддерживающим палитру.</span><span class="sxs-lookup"><span data-stu-id="48cbe-114">To do so, it must become a palette-aware application.</span></span> <span data-ttu-id="48cbe-115">Дополнительные сведения см. в разделе [режимы цвета OpenGL и управление палитрой Windows](opengl-color-modes-and-windows-palette-management.md).</span><span class="sxs-lookup"><span data-stu-id="48cbe-115">For more information, see [OpenGL Color Modes and Windows Palette Management](opengl-color-modes-and-windows-palette-management.md).</span></span>

-   <span data-ttu-id="48cbe-116">Прямой поддержки для буфера обмена, динамического обмена данными (DDE) или OLE нет.</span><span class="sxs-lookup"><span data-stu-id="48cbe-116">There is no direct support for the Clipboard, dynamic data exchange (DDE), or OLE.</span></span>

    <span data-ttu-id="48cbe-117">Окно с графическим изображением OpenGL не поддерживает эти возможности Windows напрямую.</span><span class="sxs-lookup"><span data-stu-id="48cbe-117">A window with OpenGL graphics does not directly support these Windows capabilities.</span></span> <span data-ttu-id="48cbe-118">Однако Существуют обходные пути для использования буфера обмена.</span><span class="sxs-lookup"><span data-stu-id="48cbe-118">There are workarounds, however, for using the Clipboard.</span></span> <span data-ttu-id="48cbe-119">Дополнительные сведения см. в разделе [Копирование изображения OpenGL в буфер обмена](copying-an-opengl-image-to-the-clipboard.md).</span><span class="sxs-lookup"><span data-stu-id="48cbe-119">For more information, see [Copying an OpenGL Image to the Clipboard](copying-an-opengl-image-to-the-clipboard.md).</span></span>

-   <span data-ttu-id="48cbe-120">Библиотека классов C++ инвентаризации 2,0 не включена.</span><span class="sxs-lookup"><span data-stu-id="48cbe-120">The Inventor 2.0 C++ class library is not included.</span></span>

    <span data-ttu-id="48cbe-121">Библиотека классов инвентаризации, построенная на основе OpenGL, предоставляет конструкции более высокого уровня для программирования трехмерной графики.</span><span class="sxs-lookup"><span data-stu-id="48cbe-121">The Inventor class library, built on top of OpenGL, provides higher-level constructs for programming 3-D graphics.</span></span> <span data-ttu-id="48cbe-122">Она не включена в текущую версию реализации OpenGL для Windows в корпорации Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="48cbe-122">It is not included in the current version of Microsoft's implementation of OpenGL for Windows.</span></span>

-   <span data-ttu-id="48cbe-123">Отсутствует поддержка следующих функций формата пикселей: образы стереоскопик, альфа-битпланес и вспомогательные буферы.</span><span class="sxs-lookup"><span data-stu-id="48cbe-123">There is no support for the following pixel format features: stereoscopic images, alpha bitplanes, and auxiliary buffers.</span></span>

    <span data-ttu-id="48cbe-124">Однако существует поддержка нескольких вспомогательных буферов, в том числе: буфер трафарета, буфер накопления, буфер заднего буфера (двойная буферизация), наложение и буфер плоскости ундерлай и буфер глубины (ось z).</span><span class="sxs-lookup"><span data-stu-id="48cbe-124">There is, however, support for several ancillary buffers including: stencil buffer, accumulation buffer, back buffer (double buffering), overlay and underlay plane buffer, and depth (z-axis) buffer.</span></span>

 

 




