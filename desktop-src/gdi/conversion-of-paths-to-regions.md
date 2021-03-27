---
description: Приложение может преобразовать путь в регион, вызвав функцию Пасторегион.
ms.assetid: c4261516-7872-4118-99e2-138f0ac3c38a
title: Преобразование путей в регионы
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc3a576f04035f6e29bb37a23de956322639daf1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103812005"
---
# <a name="conversion-of-paths-to-regions"></a><span data-ttu-id="607c7-103">Преобразование путей в регионы</span><span class="sxs-lookup"><span data-stu-id="607c7-103">Conversion of Paths to Regions</span></span>

<span data-ttu-id="607c7-104">Приложение может преобразовать путь в регион, вызвав функцию [**пасторегион**](/windows/desktop/api/Wingdi/nf-wingdi-pathtoregion) .</span><span class="sxs-lookup"><span data-stu-id="607c7-104">An application can convert a path into a region by calling the [**PathToRegion**](/windows/desktop/api/Wingdi/nf-wingdi-pathtoregion) function.</span></span> <span data-ttu-id="607c7-105">Как и [**селектклиппас**](/windows/desktop/api/Wingdi/nf-wingdi-selectclippath), **пасторегион** полезен при создании специальных графических эффектов.</span><span class="sxs-lookup"><span data-stu-id="607c7-105">Like [**SelectClipPath**](/windows/desktop/api/Wingdi/nf-wingdi-selectclippath), **PathToRegion** is useful in the creation of special graphics effects.</span></span> <span data-ttu-id="607c7-106">Например, отсутствуют функции, позволяющие приложению смещать путь. Однако существует функция, позволяющая приложению смещать регион ([**оффсетргн**](/windows/desktop/api/Wingdi/nf-wingdi-offsetrgn)).</span><span class="sxs-lookup"><span data-stu-id="607c7-106">For example, there are no functions that allow an application to offset a path; however, there is a function that enables an application to offset a region ([**OffsetRgn**](/windows/desktop/api/Wingdi/nf-wingdi-offsetrgn)).</span></span> <span data-ttu-id="607c7-107">С помощью **пасторегион** приложение может создавать эффекты анимации сложной фигуры путем создания пути, определяющего фигуру, преобразования пути в область (путем вызова **пасторегион**), а затем многократного рисования, перемещения и стирания области (путем вызова функций в последовательности, например [**филлргн**](/windows/desktop/api/Wingdi/nf-wingdi-fillrgn), **оффсетргн** и **филлргн**).</span><span class="sxs-lookup"><span data-stu-id="607c7-107">Using **PathToRegion** , an application can create the effect of animating a complex shape by creating a path that defines the shape, converting the path into a region (by calling **PathToRegion**), and then repeatedly painting, moving, and erasing the region (by calling functions in a sequence, such as [**FillRgn**](/windows/desktop/api/Wingdi/nf-wingdi-fillrgn), **OffsetRgn** , and **FillRgn**).</span></span>

 

 



