---
description: Палитры полутонов предназначены для использования всякий раз, когда режим растяжения в контексте устройства установлен в ПОЛУТОНА.
ms.assetid: ee171379-2ab3-4c38-8e86-ff80fa63a357
title: Палитра полутонов и настройка цвета
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5b3e6708aff92387b792424f07e9b82a1f6125ff
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104544479"
---
# <a name="halftone-palette-and-color-adjustment"></a><span data-ttu-id="92d64-103">Палитра полутонов и настройка цвета</span><span class="sxs-lookup"><span data-stu-id="92d64-103">Halftone Palette and Color Adjustment</span></span>

<span data-ttu-id="92d64-104">Палитры полутонов предназначены для использования всякий раз, когда режим растяжения в контексте устройства установлен в ПОЛУТОНА.</span><span class="sxs-lookup"><span data-stu-id="92d64-104">Halftone palettes are intended to be used whenever the stretching mode of a device context is set to HALFTONE.</span></span> <span data-ttu-id="92d64-105">Приложение создает палитру полутонов с помощью функции [**креатехалфтонепалетте**](/windows/desktop/api/Wingdi/nf-wingdi-createhalftonepalette) .</span><span class="sxs-lookup"><span data-stu-id="92d64-105">An application creates a halftone palette by using the [**CreateHalftonePalette**](/windows/desktop/api/Wingdi/nf-wingdi-createhalftonepalette) function.</span></span> <span data-ttu-id="92d64-106">Приложение должно выбрать и реализовать эту палитру в контексте устройства перед вызовом функции [**стретчблт**](/windows/desktop/api/Wingdi/nf-wingdi-stretchblt) или [**стретчдибитс**](/windows/desktop/api/Wingdi/nf-wingdi-stretchdibits) .</span><span class="sxs-lookup"><span data-stu-id="92d64-106">The application must select and realize this palette into the device context before calling the [**StretchBlt**](/windows/desktop/api/Wingdi/nf-wingdi-stretchblt) or [**StretchDIBits**](/windows/desktop/api/Wingdi/nf-wingdi-stretchdibits) function.</span></span>

<span data-ttu-id="92d64-107">Система автоматически корректирует входной цвет исходных битовых рисунков каждый раз, когда приложения вызывают функции [**стретчблт**](/windows/desktop/api/Wingdi/nf-wingdi-stretchblt) и [**стретчдибитс**](/windows/desktop/api/Wingdi/nf-wingdi-stretchdibits) , а режим растяжения контекста устройства установлен в полутона.</span><span class="sxs-lookup"><span data-stu-id="92d64-107">The system automatically adjusts the input color of source bitmaps whenever applications call the [**StretchBlt**](/windows/desktop/api/Wingdi/nf-wingdi-stretchblt) and [**StretchDIBits**](/windows/desktop/api/Wingdi/nf-wingdi-stretchdibits) functions and the stretching mode of a device context is set to HALFTONE.</span></span> <span data-ttu-id="92d64-108">Эти корректировки цвета влияют на определенные атрибуты изображения, такие как контрастность и яркость.</span><span class="sxs-lookup"><span data-stu-id="92d64-108">These color adjustments affect certain attributes of the image, such as contrast and brightness.</span></span> <span data-ttu-id="92d64-109">Приложение может задать значения коррекции цвета с помощью функции [**сетколораджустмент**](/windows/desktop/api/Wingdi/nf-wingdi-setcoloradjustment) .</span><span class="sxs-lookup"><span data-stu-id="92d64-109">An application can set the color adjustment values by using the [**SetColorAdjustment**](/windows/desktop/api/Wingdi/nf-wingdi-setcoloradjustment) function.</span></span> <span data-ttu-id="92d64-110">Приложение может извлекать значения коррекции цвета для указанного контекста устройства с помощью функции [**жетколораджустмент**](/windows/desktop/api/Wingdi/nf-wingdi-getcoloradjustment) .</span><span class="sxs-lookup"><span data-stu-id="92d64-110">The application can retrieve the color adjustment values for the specified device context by using the [**GetColorAdjustment**](/windows/desktop/api/Wingdi/nf-wingdi-getcoloradjustment) function.</span></span>

 

 



