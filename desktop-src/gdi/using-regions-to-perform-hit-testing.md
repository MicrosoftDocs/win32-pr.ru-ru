---
description: В примере кистей используются регионы для имитации &\# 0034; с масштабированием&\# 0034; представление растрового изображения размером 8 в 8 пикселей.
ms.assetid: a8e0cbfe-f05b-46ae-b420-ae34a5efbff3
title: Использование регионов для проверки попадания
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bb50ca1f837213b85619af381b86c2bd76efcbb9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104264126"
---
# <a name="using-regions-to-perform-hit-testing"></a><span data-ttu-id="3314b-103">Использование регионов для проверки попадания</span><span class="sxs-lookup"><span data-stu-id="3314b-103">Using Regions to Perform Hit Testing</span></span>

<span data-ttu-id="3314b-104">В примере в [кистях](brushes.md) используются регионы для имитации "масштабированного" изображения с монохромным изображением размером 8 пикселей.</span><span class="sxs-lookup"><span data-stu-id="3314b-104">The example in [Brushes](brushes.md) uses regions to simulate a "zoomed" view of an 8- by 8-pixel monochrome bitmap.</span></span> <span data-ttu-id="3314b-105">Щелкая Пиксели в этом битовом рисунке, пользователь создает пользовательскую кисть, подходящую для операций рисования.</span><span class="sxs-lookup"><span data-stu-id="3314b-105">By clicking on the pixels in this bitmap, the user creates a custom brush suitable for drawing operations.</span></span> <span data-ttu-id="3314b-106">В примере показано, как использовать функцию [**птинрегион**](/windows/desktop/api/Wingdi/nf-wingdi-ptinregion) для проверки попадания и функции [**инвертргн**](/windows/desktop/api/Wingdi/nf-wingdi-invertrgn) для инвертирования цветов в области.</span><span class="sxs-lookup"><span data-stu-id="3314b-106">The example shows how to use the [**PtInRegion**](/windows/desktop/api/Wingdi/nf-wingdi-ptinregion) function to perform hit testing and the [**InvertRgn**](/windows/desktop/api/Wingdi/nf-wingdi-invertrgn) function to invert the colors in a region.</span></span>

 

 



