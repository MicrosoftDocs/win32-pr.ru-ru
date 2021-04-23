---
title: Палитры и диспетчер палитры
description: Диспетчер палитры Windows, который является частью GDI, специально предназначен для 8-разрядных видеоадаптеров с аппаратной палитрей 256 цветовых записей.
ms.assetid: 3bfa5077-37ac-4597-98da-f26ad1c107a1
keywords:
- OpenGL в Windows, диспетчер палитры
- OpenGL в Windows, аппаратные палитры
- Диспетчер палитр OpenGL
- аппаратные палитры OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3dac7d122ec36201e0156a141efc3291a87c7150
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "105661555"
---
# <a name="palettes-and-the-palette-manager"></a><span data-ttu-id="25da8-107">Палитры и диспетчер палитры</span><span class="sxs-lookup"><span data-stu-id="25da8-107">Palettes and the Palette Manager</span></span>

<span data-ttu-id="25da8-108">Диспетчер палитры Windows, который является частью GDI, специально предназначен для 8-разрядных видеоадаптеров с *аппаратной палитрей* 256 цветовых записей.</span><span class="sxs-lookup"><span data-stu-id="25da8-108">The Windows Palette Manager, which is part of the GDI, specifically targets 8-bit display adapters with a *hardware palette* of 256 color entries.</span></span> <span data-ttu-id="25da8-109">Пиксели на экране хранятся в виде 8-битного индекса в палитре оборудования.</span><span class="sxs-lookup"><span data-stu-id="25da8-109">Pixels on the screen are stored as an 8-bit index into the hardware palette.</span></span> <span data-ttu-id="25da8-110">Каждая запись в палитре оборудования обычно определяет 24-разрядный цвет (8 каждый из красного, зеленого и синего).</span><span class="sxs-lookup"><span data-stu-id="25da8-110">Each entry in the hardware palette usually defines a 24-bit color (8 each of red, green, and blue).</span></span>

<span data-ttu-id="25da8-111">Диспетчер палитры поддерживает *системную палитру* , которая является копией аппаратной палитры.</span><span class="sxs-lookup"><span data-stu-id="25da8-111">The Palette Manager maintains a *system palette* that is a copy of the hardware palette.</span></span> <span data-ttu-id="25da8-112">Системная палитра состоит из двух разделов: 20 зарезервированных цветов и оставшихся 236 цветов, которые можно задать с помощью диспетчера палитры.</span><span class="sxs-lookup"><span data-stu-id="25da8-112">The system palette is divided into two sections: 20 reserved colors and the remaining 236 colors, which you can set using the Palette Manager.</span></span>

<span data-ttu-id="25da8-113">Выбирается и реализуется по умолчанию *логическая палитра* из 20 цветов в контексте устройства.</span><span class="sxs-lookup"><span data-stu-id="25da8-113">A default 20-color *logical palette* is selected and realized into a device context.</span></span> <span data-ttu-id="25da8-114">Вы можете создать и использовать новую логическую палитру.</span><span class="sxs-lookup"><span data-stu-id="25da8-114">You can create and use a new logical palette.</span></span> <span data-ttu-id="25da8-115">Чтобы изменить системную палитру, выберите и реализуйте созданную логическую палитру.</span><span class="sxs-lookup"><span data-stu-id="25da8-115">To change the system palette, select and realize the logical palette you created.</span></span>

<span data-ttu-id="25da8-116">Вы, вероятно, создадите логическую палитру, чтобы указать цвета, которые должны отображаться в приложении OpenGL.</span><span class="sxs-lookup"><span data-stu-id="25da8-116">You'll probably create a logical palette to specify the colors you want displayed in your OpenGL application.</span></span> <span data-ttu-id="25da8-117">Используя определенные вызовы GDI, можно временно заменить большую часть системной палитры логической палитрой.</span><span class="sxs-lookup"><span data-stu-id="25da8-117">Using certain GDI calls, you can temporarily replace most of the system palette with a logical palette.</span></span> <span data-ttu-id="25da8-118">С помощью логической палитры можно определить цвета пикселей для GDI, используя либо RGBA, либо режим индексирования цвета.</span><span class="sxs-lookup"><span data-stu-id="25da8-118">Using a logical palette, you can define pixel colors for the GDI using either the RGBA or the color-index mode.</span></span> <span data-ttu-id="25da8-119">Максимальный размер логической палитры — 256 цветов для 8-разрядных устройств и 4 096 цветов на true-цветном устройстве (16, 24 и 32 бит).</span><span class="sxs-lookup"><span data-stu-id="25da8-119">The maximum size of a logical palette is 256 colors for 8-bit devices and 4,096 colors on a true-color device (16, 24, and 32 bits).</span></span>

<span data-ttu-id="25da8-120">Дополнительные сведения о режимах RGBA и индексов цветов см. в разделе [режим RGBA, управление палитрами Windows](rgba-mode-and-windows-palette-management.md) и [цветовые режимы OpenGL и управление палитрой Windows](opengl-color-modes-and-windows-palette-management.md).</span><span class="sxs-lookup"><span data-stu-id="25da8-120">For more information on the RGBA and color-index modes, see [RGBA Mode and Windows Palette Management](rgba-mode-and-windows-palette-management.md) and [OpenGL Color Modes and Windows Palette Management](opengl-color-modes-and-windows-palette-management.md).</span></span>

 

 




