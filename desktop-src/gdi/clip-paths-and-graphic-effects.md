---
description: Приложение может использовать отсечение и пути для создания специальных графических эффектов. На следующем рисунке показана строка текста, нарисованного с помощью большого шрифта Arial.
ms.assetid: fda0d627-406c-44f9-9061-7aea3e2d7f66
title: Контуры клипов и графические эффекты
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8156a8670747175502b2385e6c24a340345a54f9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104544546"
---
# <a name="clip-paths-and-graphic-effects"></a><span data-ttu-id="0c624-104">Контуры клипов и графические эффекты</span><span class="sxs-lookup"><span data-stu-id="0c624-104">Clip Paths and Graphic Effects</span></span>

<span data-ttu-id="0c624-105">Приложение может использовать отсечение и пути для создания специальных графических эффектов.</span><span class="sxs-lookup"><span data-stu-id="0c624-105">An application can use clipping and paths to create special graphic effects.</span></span> <span data-ttu-id="0c624-106">На следующем рисунке показана строка текста, нарисованного с помощью большого шрифта Arial.</span><span class="sxs-lookup"><span data-stu-id="0c624-106">The following illustration shows a string of text drawn with a large Arial font.</span></span>

![Иллюстрация, демонстрирующая черный текст на белом фоне](images/cspth-02.png)

<span data-ttu-id="0c624-108">На следующем рисунке показан результат выбора текста в качестве пути обрезки и рисования радиальных линий для круга, центр которого находится над строкой и слева от нее.</span><span class="sxs-lookup"><span data-stu-id="0c624-108">The next illustration shows the result of selecting the text as a clip path and drawing radial lines for a circle whose center is located above and left of the string.</span></span>

![Иллюстрация, показывающая тот же текст, но с линиями, а не сплошным черным](images/cspth-03.png)

> [!Note]  
> <span data-ttu-id="0c624-110">Перед тем, как интерфейс графических устройств (GDI) добавляет текст, созданный с помощью растрового шрифта, к контуру, он преобразует шрифт в контур или векторный шрифт.</span><span class="sxs-lookup"><span data-stu-id="0c624-110">Before graphics device interface (GDI) adds text created with a bitmapped font to a path, it converts the font to an outline or vector font.</span></span>

 

<span data-ttu-id="0c624-111">Приложение создает путь отсечения путем создания скобки пути и последующего вызова функции [**селектклиппас**](/windows/desktop/api/Wingdi/nf-wingdi-selectclippath) .</span><span class="sxs-lookup"><span data-stu-id="0c624-111">An application creates a clip path by generating a path bracket and then calling the [**SelectClipPath**](/windows/desktop/api/Wingdi/nf-wingdi-selectclippath) function.</span></span> <span data-ttu-id="0c624-112">После выбора контура клипа в контроллере домена выходные данные отображаются только в границах пути.</span><span class="sxs-lookup"><span data-stu-id="0c624-112">After a clip path is selected into a DC, output only appears within the borders of the path.</span></span>

<span data-ttu-id="0c624-113">Помимо создания специальных графических эффектов, пути обрезки также полезны в приложениях, которые сохраняют изображения в виде расширенных метафайлов.</span><span class="sxs-lookup"><span data-stu-id="0c624-113">In addition to creating special graphics effects, clip paths are also useful in applications that save images as enhanced metafiles.</span></span> <span data-ttu-id="0c624-114">С помощью пути обрезки приложение может обеспечить независимость от устройства, так как единицы, используемые для указания пути, — это логические единицы.</span><span class="sxs-lookup"><span data-stu-id="0c624-114">By using a clip path, an application is able to ensure device independence because the units used to specify a path are logical units.</span></span>

 

 



