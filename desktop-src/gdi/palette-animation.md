---
description: Анимация палитры — это метод моделирования движения путем быстрого изменения цветов выбранных записей в цветовой палитре.
ms.assetid: fc5b8061-fd4f-4751-883d-877fa32cdfcc
title: Анимация палитры
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f9761e99033e7a01fa875fce7c41e5a35cf40ab6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103811903"
---
# <a name="palette-animation"></a><span data-ttu-id="e0768-103">Анимация палитры</span><span class="sxs-lookup"><span data-stu-id="e0768-103">Palette Animation</span></span>

<span data-ttu-id="e0768-104">Анимация палитры — это метод моделирования движения путем быстрого изменения цветов выбранных записей в цветовой палитре.</span><span class="sxs-lookup"><span data-stu-id="e0768-104">Palette animation is a technique to simulate motion by rapidly changing the colors of selected entries in a color palette.</span></span> <span data-ttu-id="e0768-105">Приложение может выполнять анимацию палитры, создавая логическую палитру, содержащую "зарезервированные" записи, а затем используя функцию [**аниматепалетте**](/windows/desktop/api/Wingdi/nf-wingdi-animatepalette) для изменения цветов в этих зарезервированных записях.</span><span class="sxs-lookup"><span data-stu-id="e0768-105">An application can carry out palette animation by creating a logical palette that contains "reserved" entries and then using the [**AnimatePalette**](/windows/desktop/api/Wingdi/nf-wingdi-animatepalette) function to change colors in those reserved entries.</span></span>

<span data-ttu-id="e0768-106">Приложение создает зарезервированный элемент в логической палитре, устанавливая для элемента **пефлагс** структуры [**палеттинтри**](/previous-versions//dd162769(v=vs.85)) \_ флаг зарезервированного компьютера.</span><span class="sxs-lookup"><span data-stu-id="e0768-106">An application creates a reserved entry in a logical palette by setting the **peFlags** member of the [**PALETTEENTRY**](/previous-versions//dd162769(v=vs.85)) structure to the PC\_RESERVED flag.</span></span> <span data-ttu-id="e0768-107">После выбора и реализации этой логической палитры приложение может вызвать функцию [**аниматепалетте**](/windows/desktop/api/Wingdi/nf-wingdi-animatepalette) , чтобы изменить одну или несколько зарезервированных записей.</span><span class="sxs-lookup"><span data-stu-id="e0768-107">Once this logical palette is selected and realized, the application can call the [**AnimatePalette**](/windows/desktop/api/Wingdi/nf-wingdi-animatepalette) function to change one or more reserved entries.</span></span> <span data-ttu-id="e0768-108">Если данная палитра связана с активным окном, система немедленно обновляет цвета на экране.</span><span class="sxs-lookup"><span data-stu-id="e0768-108">If the given palette is associated with the active window, the system updates the colors on the screen immediately.</span></span>

 

 
