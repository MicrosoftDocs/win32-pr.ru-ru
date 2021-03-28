---
description: Атрибут pattern задает шаблон геометрического пера.
ms.assetid: 5a330416-3b83-4f0f-825c-80e47903966e
title: Шаблон пера
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 577b5e2cb31e44a4631760c82e678af069322cbc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104544423"
---
# <a name="pen-pattern"></a><span data-ttu-id="9b89c-103">Шаблон пера</span><span class="sxs-lookup"><span data-stu-id="9b89c-103">Pen Pattern</span></span>

<span data-ttu-id="9b89c-104">Атрибут pattern задает шаблон геометрического пера.</span><span class="sxs-lookup"><span data-stu-id="9b89c-104">The pattern attribute specifies the pattern of a geometric pen.</span></span>

<span data-ttu-id="9b89c-105">На следующем рисунке показаны линии, рисуемые различными геометрическими перьями.</span><span class="sxs-lookup"><span data-stu-id="9b89c-105">The following illustration shows lines drawn with different geometric pens.</span></span> <span data-ttu-id="9b89c-106">Каждое перо было создано с использованием другого атрибута шаблона.</span><span class="sxs-lookup"><span data-stu-id="9b89c-106">Each pen was created using a different pattern attribute.</span></span>

![Иллюстрация, показывающая четыре линии, каждая из которых заполнена другим пером](images/cspen-02.png)

<span data-ttu-id="9b89c-108">Первая строка на предыдущем рисунке рисуется с использованием одного из шести доступных шаблонов штриховки; Дополнительные сведения о шаблонах штриховки см. в разделе [штриховка пера](pen-hatch.md).</span><span class="sxs-lookup"><span data-stu-id="9b89c-108">The first line in the previous illustration is drawn using one of the six available hatch patterns; for more information about hatch patterns, see [Pen Hatch](pen-hatch.md).</span></span> <span data-ttu-id="9b89c-109">Следующая строка рисуется с использованием пустого шаблона, идентичного шаблону null.</span><span class="sxs-lookup"><span data-stu-id="9b89c-109">The next line is drawn using the hollow pattern, identical to the null pattern.</span></span> <span data-ttu-id="9b89c-110">Третья линия рисуется с помощью пользовательского шаблона, созданного на основе точечного рисунка размером 8 в 8 пикселей.</span><span class="sxs-lookup"><span data-stu-id="9b89c-110">The third line is drawn using a custom pattern created from an 8-by-8-pixel bitmap.</span></span> <span data-ttu-id="9b89c-111">(Дополнительные сведения о растровых изображениях и их создании см. в разделе [точечные рисунки](bitmaps.md).) Последняя строка рисуется с помощью сплошного шаблона.</span><span class="sxs-lookup"><span data-stu-id="9b89c-111">(For more information about bitmaps and their creation, see [Bitmaps](bitmaps.md).) The last line is drawn using a solid pattern.</span></span> <span data-ttu-id="9b89c-112">Создание кисти и передача ее дескриптора в функцию [**ексткреатепен**](/windows/desktop/api/Wingdi/nf-wingdi-extcreatepen) создает шаблон.</span><span class="sxs-lookup"><span data-stu-id="9b89c-112">Creating a brush and passing its handle to the [**ExtCreatePen**](/windows/desktop/api/Wingdi/nf-wingdi-extcreatepen) function creates a pattern.</span></span>

 

 



