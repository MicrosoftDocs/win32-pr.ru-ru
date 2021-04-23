---
description: Приложение инвертирует цвета, отображаемые в области, путем вызова функции Инвертргн.
ms.assetid: bcd9fe61-0f92-41bc-b953-a66e01e43a75
title: Инвертирование регионов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f7e3c4b4d01f9ed8f09e819d59bf3268a1ccae4a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104997343"
---
# <a name="inverting-regions"></a><span data-ttu-id="e675d-103">Инвертирование регионов</span><span class="sxs-lookup"><span data-stu-id="e675d-103">Inverting Regions</span></span>

<span data-ttu-id="e675d-104">Приложение инвертирует цвета, отображаемые в области, путем вызова функции [**инвертргн**](/windows/desktop/api/Wingdi/nf-wingdi-invertrgn) .</span><span class="sxs-lookup"><span data-stu-id="e675d-104">An application inverts the colors that appear within a region by calling the [**InvertRgn**](/windows/desktop/api/Wingdi/nf-wingdi-invertrgn) function.</span></span> <span data-ttu-id="e675d-105">Для монохромных экранов **инвертргн** делает белые Пиксели черными и черными пикселами белым цветом.</span><span class="sxs-lookup"><span data-stu-id="e675d-105">On monochrome displays, **InvertRgn** makes white pixels black and black pixels white.</span></span> <span data-ttu-id="e675d-106">На цветовых экранах эта инверсия зависит от типа технологии, используемой для создания цветов на экране.</span><span class="sxs-lookup"><span data-stu-id="e675d-106">On color screens, this inversion is dependent on the type of technology used to generate the colors for the screen.</span></span>

 

 



