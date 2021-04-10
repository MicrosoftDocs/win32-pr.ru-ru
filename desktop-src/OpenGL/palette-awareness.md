---
title: Поддержка палитры
description: Приложение должно реагировать на \_ сообщения WM палеттечанжед, WM \_ КУЕРИНЕВПАЛЕТТЕ и WM Activate, \_ чтобы иметь возможность учитывать и использовать палитры. Разработайте приложение, чтобы выбрать и реализовать палитры в ответ на эти сообщения.
ms.assetid: 0670e929-dfdb-44d2-bda2-c532d1739d8e
keywords:
- OpenGL в Windows, поддержка палитры
- Поддержка палитры OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 67ceab4c27f63c12977d072f84e789d1800b6557
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "103891025"
---
# <a name="palette-awareness"></a><span data-ttu-id="65878-106">Поддержка палитры</span><span class="sxs-lookup"><span data-stu-id="65878-106">Palette Awareness</span></span>

<span data-ttu-id="65878-107">Приложение должно реагировать на сообщения [WM \_ палеттечанжед](/windows/desktop/gdi/wm-palettechanged), [WM \_ куериневпалетте](/windows/desktop/gdi/wm-querynewpalette)и [WM \_ Activate](../inputdev/wm-activate.md) , чтобы иметь возможность учитывать и использовать палитры.</span><span class="sxs-lookup"><span data-stu-id="65878-107">Your application must respond to the [WM\_PALETTECHANGED](/windows/desktop/gdi/wm-palettechanged), [WM\_QUERYNEWPALETTE](/windows/desktop/gdi/wm-querynewpalette), and [WM\_ACTIVATE](../inputdev/wm-activate.md) messages to be aware of and use palettes.</span></span> <span data-ttu-id="65878-108">Разработайте приложение, чтобы выбрать и реализовать палитры в ответ на эти сообщения.</span><span class="sxs-lookup"><span data-stu-id="65878-108">Design your application to select and realize palettes in response to these messages.</span></span>

<span data-ttu-id="65878-109">Дополнительные сведения о палитрах и поддержке палитры см. в статьях «Поддержка палитры» и «диспетчер палитры: как и почему» на компактных дисках библиотеки разработки Microsoft Developer Network.</span><span class="sxs-lookup"><span data-stu-id="65878-109">For more information on palettes and palette awareness, see the articles "Palette Awareness," and "The Palette Manager: How and Why" on the Microsoft Developer Network Development Library compact discs.</span></span>

 

 