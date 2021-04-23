---
description: 'Цвет определяется как сочетание трех основных цветов: красный, зеленый и синий.'
ms.assetid: 6e44935c-2b3b-4062-8273-f1f3e70300d2
title: Значения цвета
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 67e46cd7ee87871c660702bed120958e7096745d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104155655"
---
# <a name="color-values"></a><span data-ttu-id="fd7f5-103">Значения цвета</span><span class="sxs-lookup"><span data-stu-id="fd7f5-103">Color Values</span></span>

<span data-ttu-id="fd7f5-104">Цвет определяется как сочетание трех основных цветов: красный, зеленый и синий.</span><span class="sxs-lookup"><span data-stu-id="fd7f5-104">Color is defined as a combination of three primary colors red, green, and blue.</span></span> <span data-ttu-id="fd7f5-105">система определяет цвет, присваивая ему значение цвета (иногда называемое Triplet RGB), которое состоит из 3 8-разрядных значений, указывающих интенситиес из его компонентов цвета.</span><span class="sxs-lookup"><span data-stu-id="fd7f5-105">the system identifies a color by giving it a color value (sometimes called an RGB triplet), which consists of three 8-bit values specifying the intensities of its color components.</span></span> <span data-ttu-id="fd7f5-106">Черный цвет имеет минимальную интенсивность для красного, зеленого и синего, поэтому значение цвета "черный" равно (0, 0, 0).</span><span class="sxs-lookup"><span data-stu-id="fd7f5-106">Black has the minimum intensity for red, green, and blue, so the color value for black is (0, 0, 0).</span></span> <span data-ttu-id="fd7f5-107">Белый цвет имеет максимальную интенсивность красного, зеленого и синего, поэтому его значение цвета равно (255, 255, 255).</span><span class="sxs-lookup"><span data-stu-id="fd7f5-107">White has the maximum intensity for red, green, and blue, so its color value is (255, 255, 255).</span></span>

> [!Note]  
> <span data-ttu-id="fd7f5-108">Если сопоставление цветов изображения включено, определение цвета и значения цвета зависят от типа цветового пространства, установленного в данный момент для контекста устройства.</span><span class="sxs-lookup"><span data-stu-id="fd7f5-108">If image color matching is enabled, the definition of color and the meaning of a color value depends on the type of color space that is currently set for the device context.</span></span>

 

<span data-ttu-id="fd7f5-109">Система и приложения используют параметры и переменные, имеющие тип [COLORREF](colorref.md) для передачи и хранения значений цветов.</span><span class="sxs-lookup"><span data-stu-id="fd7f5-109">The system and applications use parameters and variables having the [COLORREF](colorref.md) type to pass and store color values.</span></span> <span data-ttu-id="fd7f5-110">Например, функция [**енумобжектс**](/windows/desktop/api/Wingdi/nf-wingdi-enumobjects) определяет цвет каждого пера, присвоив элементу **Лопнколор** в структуре [**LOGPEN**](/windows/win32/api/wingdi/ns-wingdi-logpen) значение цвета.</span><span class="sxs-lookup"><span data-stu-id="fd7f5-110">For example, the [**EnumObjects**](/windows/desktop/api/Wingdi/nf-wingdi-enumobjects) function identifies the color of each pen by setting the **lopnColor** member in a [**LOGPEN**](/windows/win32/api/wingdi/ns-wingdi-logpen) structure to a color value.</span></span> <span data-ttu-id="fd7f5-111">Приложения могут извлекать отдельные значения красного, зеленого и синего компонентов из значения цвета с помощью макросов [**rvalue**](/windows/desktop/api/Wingdi/nf-wingdi-getrvalue), [**жетгвалуе**](/windows/desktop/api/Wingdi/nf-wingdi-getgvalue)и [**жетбвалуе**](/windows/desktop/api/Wingdi/nf-wingdi-getbvalue) соответственно.</span><span class="sxs-lookup"><span data-stu-id="fd7f5-111">Applications can extract the individual values of the red, green, and blue components from a color value by using the [**GetRValue**](/windows/desktop/api/Wingdi/nf-wingdi-getrvalue), [**GetGValue**](/windows/desktop/api/Wingdi/nf-wingdi-getgvalue), and [**GetBValue**](/windows/desktop/api/Wingdi/nf-wingdi-getbvalue) macros, respectively.</span></span> <span data-ttu-id="fd7f5-112">Приложения могут создавать значения цвета из отдельных компонентов с помощью макроса [**RGB**](/windows/desktop/api/Wingdi/nf-wingdi-rgb) .</span><span class="sxs-lookup"><span data-stu-id="fd7f5-112">Applications can create a color value from individual component values by using the [**RGB**](/windows/desktop/api/Wingdi/nf-wingdi-rgb) macro.</span></span> <span data-ttu-id="fd7f5-113">При создании или проверке логической палитры приложение использует структуру [**ргбкуад**](/windows/win32/api/wingdi/ns-wingdi-rgbquad) для определения значений цвета и для проверки отдельных значений компонентов.</span><span class="sxs-lookup"><span data-stu-id="fd7f5-113">When creating or examining a logical palette, an application uses the [**RGBQUAD**](/windows/win32/api/wingdi/ns-wingdi-rgbquad) structure to define color values and to examine individual component values.</span></span>

 

 



