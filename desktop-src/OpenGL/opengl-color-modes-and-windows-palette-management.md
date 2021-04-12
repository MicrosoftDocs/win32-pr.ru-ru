---
title: Цветовые режимы OpenGL и управление палитрой Windows
description: 'В реализации Майкрософт OpenGL в Windows поддерживается два цветовых пиксельных режима данных: RGBA и режим индексирования. Windows предоставляет два аналогичных способа обработки цветового и управления палитрами.'
ms.assetid: 4a731119-8704-4ae1-a564-4a1955051236
keywords:
- OpenGL в Windows, цветовые режимы
- OpenGL в Windows, управление палитрами
- Управление палитрами OpenGL
- цветовые режимы OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fa3d63778301ec55b962f3f66e79d99cee09be9d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104329496"
---
# <a name="opengl-color-modes-and-windows-palette-management"></a><span data-ttu-id="c760e-108">Цветовые режимы OpenGL и управление палитрой Windows</span><span class="sxs-lookup"><span data-stu-id="c760e-108">OpenGL Color Modes and Windows Palette Management</span></span>

<span data-ttu-id="c760e-109">В реализации Майкрософт OpenGL в Windows поддерживается два цветовых пиксельных режима данных: RGBA и режим индексирования цветов.</span><span class="sxs-lookup"><span data-stu-id="c760e-109">The Microsoft implementation of OpenGL in Windows supports two color pixel data modes: RGBA and color-index modes.</span></span> <span data-ttu-id="c760e-110">Windows предоставляет два аналогичных способа обработки цвета: истинное управление цветом и палитрой.</span><span class="sxs-lookup"><span data-stu-id="c760e-110">Windows provide two analogous ways of handling color: true color and palette management.</span></span>

<span data-ttu-id="c760e-111">True — цветные устройства, способные принимать 16, 24 или более бит цветовой информации на пиксель, могут отображать десятки тысяч, десятки миллионов или больше цветов одновременно.</span><span class="sxs-lookup"><span data-stu-id="c760e-111">True-color devices, able to accept 16, 24, or more bits of color information per pixel, can display tens of thousands, tens of millions, or more colors simultaneously.</span></span> <span data-ttu-id="c760e-112">Однако сложности возникают, когда приложение должно управлять режимом RGBA или цветового индекса на устройстве типа Palette.</span><span class="sxs-lookup"><span data-stu-id="c760e-112">Complexities arise, however, when an application has to manage RGBA or color-index mode on a palette-type device.</span></span> <span data-ttu-id="c760e-113">Устройства типа "Палитра", такие как дисплей VGA 256-Color, ограничены числом цветов, которые они могут отображать одновременно.</span><span class="sxs-lookup"><span data-stu-id="c760e-113">Palette-type devices, such as a 256-color VGA display, are limited in the number of colors they can display simultaneously.</span></span> <span data-ttu-id="c760e-114">Для успешного использования устройств типа "Палитра" приложения должны работать с несколькими сложными сведениями.</span><span class="sxs-lookup"><span data-stu-id="c760e-114">Applications must handle a number of tricky details to successfully use palette-type devices.</span></span> <span data-ttu-id="c760e-115">Поскольку программы в режиме индексирования цветов не используют аппаратную палитру, они сложнее использовать с истинными цветовыми устройствами, чем программы, использующие режим RGBA.</span><span class="sxs-lookup"><span data-stu-id="c760e-115">Because color-index mode programs don't use a hardware palette, they are more difficult to use with true-color devices than programs using the RGBA mode.</span></span>

 

 




