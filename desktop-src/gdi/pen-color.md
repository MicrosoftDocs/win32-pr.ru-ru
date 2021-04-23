---
description: Атрибут Color задает цвет пера.
ms.assetid: ce775359-65fc-40d0-8725-b392cc0464a6
title: Цвет пера
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 92d831994ac444207832574dc104a9d5c2582db8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104544426"
---
# <a name="pen-color"></a><span data-ttu-id="32a0e-103">Цвет пера</span><span class="sxs-lookup"><span data-stu-id="32a0e-103">Pen Color</span></span>

<span data-ttu-id="32a0e-104">Атрибут Color задает цвет пера.</span><span class="sxs-lookup"><span data-stu-id="32a0e-104">The color attribute specifies the pen's color.</span></span> <span data-ttu-id="32a0e-105">Приложение может создать косметический перо с уникальным цветом с помощью макроса [**RGB**](/windows/desktop/api/Wingdi/nf-wingdi-rgb) для хранения красного, зеленого, синего Triplet, указывающего нужный цвет в структуре [COLORREF](colorref.md) , и передачи адреса этой структуры в функцию [**креатепен**](/windows/desktop/api/Wingdi/nf-wingdi-createpen), [**креатепениндирект**](/windows/desktop/api/Wingdi/nf-wingdi-createpenindirect)или [**ексткреатепен**](/windows/desktop/api/Wingdi/nf-wingdi-extcreatepen) .</span><span class="sxs-lookup"><span data-stu-id="32a0e-105">An application can create a cosmetic pen with a unique color by using the [**RGB**](/windows/desktop/api/Wingdi/nf-wingdi-rgb) macro to store the red, green, blue triplet that specifies the desired color in a [COLORREF](colorref.md) structure and passing this structure's address to the [**CreatePen**](/windows/desktop/api/Wingdi/nf-wingdi-createpen), [**CreatePenIndirect**](/windows/desktop/api/Wingdi/nf-wingdi-createpenindirect), or [**ExtCreatePen**](/windows/desktop/api/Wingdi/nf-wingdi-extcreatepen) function.</span></span> <span data-ttu-id="32a0e-106">(Стандартные перья ограничены черным, белым и невидимыми.) Дополнительные сведения о триады и цветах RGB см. в разделе [цвета](colors.md).</span><span class="sxs-lookup"><span data-stu-id="32a0e-106">(The stock pens are limited to black, white, and invisible.) For more information about RGB triplets and color, see [Colors](colors.md).</span></span>

 

 



