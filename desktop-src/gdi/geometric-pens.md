---
description: Измерения геометрического пера указываются в логических единицах.
ms.assetid: e7030490-d10c-4d1c-87ae-5b4cc4858ee1
title: Геометрические перья
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9725f6440f62458d4c87232400f16e27f9b978ce
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104997366"
---
# <a name="geometric-pens"></a><span data-ttu-id="19bc5-103">Геометрические перья</span><span class="sxs-lookup"><span data-stu-id="19bc5-103">Geometric Pens</span></span>

<span data-ttu-id="19bc5-104">Измерения геометрического пера указываются в логических единицах.</span><span class="sxs-lookup"><span data-stu-id="19bc5-104">The dimensions of a geometric pen are specified in logical units.</span></span> <span data-ttu-id="19bc5-105">Таким образом, линии, нарисованные с помощью геометрического пера, можно масштабировать, то есть они могут быть шире или более узки, в зависимости от текущего преобразования мира.</span><span class="sxs-lookup"><span data-stu-id="19bc5-105">Therefore, lines drawn with a geometric pen can be scaled that is, they may appear wider or narrower, depending on the current world transformation.</span></span> <span data-ttu-id="19bc5-106">Дополнительные сведения об универсальном преобразовании см. в разделе [координатные пространства и](coordinate-spaces-and-transformations.md)преобразования.</span><span class="sxs-lookup"><span data-stu-id="19bc5-106">For more information about world transformation, see [Coordinate Spaces and Transformations](coordinate-spaces-and-transformations.md).</span></span>

<span data-ttu-id="19bc5-107">Помимо трех атрибутов, совместно используемых с косметическими перьями (ширина, стиль и цвет), геометрические перья имеют следующие четыре атрибута: шаблон, необязательный штриховки, стиль конца и стиль объединения.</span><span class="sxs-lookup"><span data-stu-id="19bc5-107">In addition to the three attributes shared with cosmetic pens (width, style, and color), geometric pens possess the following four attributes: pattern, optional hatch, end style, and join style.</span></span> <span data-ttu-id="19bc5-108">Дополнительные сведения об этих атрибутах см. в разделе [атрибуты пера](pen-attributes.md).</span><span class="sxs-lookup"><span data-stu-id="19bc5-108">For more information about these attributes, see [Pen Attributes](pen-attributes.md).</span></span>

<span data-ttu-id="19bc5-109">Для создания геометрического пера приложение использует функцию [**ексткреатепен**](/windows/desktop/api/Wingdi/nf-wingdi-extcreatepen) .</span><span class="sxs-lookup"><span data-stu-id="19bc5-109">To create a geometric pen, an application uses the [**ExtCreatePen**](/windows/desktop/api/Wingdi/nf-wingdi-extcreatepen) function.</span></span> <span data-ttu-id="19bc5-110">Как и в случае с косметическими перьями, функция [**SelectObject**](/windows/desktop/api/Wingdi/nf-wingdi-selectobject) выбирает геометрический перо в контроллере домена приложения.</span><span class="sxs-lookup"><span data-stu-id="19bc5-110">As with cosmetic pens, the [**SelectObject**](/windows/desktop/api/Wingdi/nf-wingdi-selectobject) function selects a geometric pen into the application's DC.</span></span>

 

 



