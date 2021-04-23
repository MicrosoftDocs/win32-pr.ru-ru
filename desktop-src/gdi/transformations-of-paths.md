---
description: Пути определяются с помощью логических устройств и текущих преобразований.
ms.assetid: a5a426ec-25e8-4fe1-985c-d078227e8aba
title: Преобразования путей
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1eb2c033b5769a4edff29beba6cccbd80cfd26de
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104985808"
---
# <a name="transformations-of-paths"></a><span data-ttu-id="61c4f-103">Преобразования путей</span><span class="sxs-lookup"><span data-stu-id="61c4f-103">Transformations of Paths</span></span>

<span data-ttu-id="61c4f-104">Пути определяются с помощью логических устройств и текущих преобразований.</span><span class="sxs-lookup"><span data-stu-id="61c4f-104">Paths are defined using logical units and current transformations.</span></span> <span data-ttu-id="61c4f-105">(Если была вызвана функция [**сетворлдтрансформ**](/windows/desktop/api/Wingdi/nf-wingdi-setworldtransform) , логические устройства являются универсальными единицами. в противном случае логические устройства являются единицами страниц.) Приложение может использовать мировые преобразования для масштабирования, вращения, наклона, преобразования и отражения линий и кривых Безье, определяющих контур.</span><span class="sxs-lookup"><span data-stu-id="61c4f-105">(If the [**SetWorldTransform**](/windows/desktop/api/Wingdi/nf-wingdi-setworldtransform) function has been called, the logical units are world units; otherwise, the logical units are page units.) An application can use world transformations to scale, rotate, shear, translate, and reflect the lines and Bézier curves that define a path.</span></span>

> [!Note]  
> <span data-ttu-id="61c4f-106">Преобразование мира в скобках пути влияет только на линии и кривые, рисуемые после того, как было задано преобразование.</span><span class="sxs-lookup"><span data-stu-id="61c4f-106">A world transformation within a path bracket only affects those lines and curves drawn after the transformation was set.</span></span> <span data-ttu-id="61c4f-107">Это не повлияет на линии и кривые, которые были выведены до того, как она была задана.</span><span class="sxs-lookup"><span data-stu-id="61c4f-107">It will have no affect on those lines and curves that were drawn before it was set.</span></span> <span data-ttu-id="61c4f-108">Описание универсального преобразования см. в разделе [координатные пространства и преобразования](coordinate-spaces-and-transformations.md).</span><span class="sxs-lookup"><span data-stu-id="61c4f-108">For a description of the world transformation, see [Coordinate Spaces and Transformations](coordinate-spaces-and-transformations.md).</span></span>

 

<span data-ttu-id="61c4f-109">Приложение также может использовать [**сетворлдтрансформ**](/windows/desktop/api/Wingdi/nf-wingdi-setworldtransform) , чтобы структурировать форму пера, используемой для структурирования контура, если перо является геометрическим пером.</span><span class="sxs-lookup"><span data-stu-id="61c4f-109">An application can also use [**SetWorldTransform**](/windows/desktop/api/Wingdi/nf-wingdi-setworldtransform) to outline the shape of the pen used to outline a path if the pen is a geometric pen.</span></span> <span data-ttu-id="61c4f-110">Описание геометрических перьев см. в разделе [перья](pens.md).</span><span class="sxs-lookup"><span data-stu-id="61c4f-110">For a description of geometric pens, see [Pens](pens.md).</span></span>

 

 



