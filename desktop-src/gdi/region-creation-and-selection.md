---
description: Приложение создает регион, вызывая функцию, связанную с определенной фигурой. В следующей таблице показаны функции, связанные с каждой из стандартных форм.
ms.assetid: e94ae371-8365-4e42-ac8c-04c3928fcffb
title: Создание и выбор регионов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d27a7887e41a04a62015fa3fc9d82f5beeb01d6a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104984836"
---
# <a name="region-creation-and-selection"></a><span data-ttu-id="30a69-104">Создание и выбор регионов</span><span class="sxs-lookup"><span data-stu-id="30a69-104">Region Creation and Selection</span></span>

<span data-ttu-id="30a69-105">Приложение создает регион, вызывая функцию, связанную с определенной фигурой.</span><span class="sxs-lookup"><span data-stu-id="30a69-105">An application creates a region by calling a function associated with a specific shape.</span></span> <span data-ttu-id="30a69-106">В следующей таблице показаны функции, связанные с каждой из стандартных форм.</span><span class="sxs-lookup"><span data-stu-id="30a69-106">The following table shows the function(s) associated with each of the standard shapes.</span></span>



| <span data-ttu-id="30a69-107">Фигурная</span><span class="sxs-lookup"><span data-stu-id="30a69-107">Shape</span></span>                                   | <span data-ttu-id="30a69-108">Функция</span><span class="sxs-lookup"><span data-stu-id="30a69-108">Function</span></span>                                                                                                                         |
|-----------------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="30a69-109">Прямоугольная область</span><span class="sxs-lookup"><span data-stu-id="30a69-109">Rectangular region</span></span>                      | <span data-ttu-id="30a69-110">[**Креатеректргн**](/windows/desktop/api/Wingdi/nf-wingdi-createrectrgn), [**креатеректргниндирект**](/windows/desktop/api/Wingdi/nf-wingdi-createrectrgnindirect), [**сетректргн**](/windows/desktop/api/Wingdi/nf-wingdi-setrectrgn)</span><span class="sxs-lookup"><span data-stu-id="30a69-110">[**CreateRectRgn**](/windows/desktop/api/Wingdi/nf-wingdi-createrectrgn), [**CreateRectRgnIndirect**](/windows/desktop/api/Wingdi/nf-wingdi-createrectrgnindirect), [**SetRectRgn**](/windows/desktop/api/Wingdi/nf-wingdi-setrectrgn)</span></span> |
| <span data-ttu-id="30a69-111">Прямоугольная область с закругленными углами</span><span class="sxs-lookup"><span data-stu-id="30a69-111">Rectangular region with rounded corners</span></span> | [<span data-ttu-id="30a69-112">**креатераундректргн**</span><span class="sxs-lookup"><span data-stu-id="30a69-112">**CreateRoundRectRgn**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-createroundrectrgn)                                                                                 |
| <span data-ttu-id="30a69-113">Эллиптическая область</span><span class="sxs-lookup"><span data-stu-id="30a69-113">Elliptical region</span></span>                       | <span data-ttu-id="30a69-114">[**Креатиллиптикргн**](/windows/desktop/api/Wingdi/nf-wingdi-createellipticrgn), [ **креатиллиптикргниндирект**](/windows/desktop/api/Wingdi/nf-wingdi-createellipticrgnindirect)</span><span class="sxs-lookup"><span data-stu-id="30a69-114">[**CreateEllipticRgn**](/windows/desktop/api/Wingdi/nf-wingdi-createellipticrgn), [**CreateEllipticRgnIndirect**](/windows/desktop/api/Wingdi/nf-wingdi-createellipticrgnindirect)</span></span>                   |
| <span data-ttu-id="30a69-115">Многоугольная область</span><span class="sxs-lookup"><span data-stu-id="30a69-115">Polygonal region</span></span>                        | <span data-ttu-id="30a69-116">[**Креатеполигонргн**](/windows/desktop/api/Wingdi/nf-wingdi-createpolygonrgn), [ **креатеполиполигонргн**](/windows/desktop/api/Wingdi/nf-wingdi-createpolypolygonrgn)</span><span class="sxs-lookup"><span data-stu-id="30a69-116">[**CreatePolygonRgn**](/windows/desktop/api/Wingdi/nf-wingdi-createpolygonrgn), [**CreatePolyPolygonRgn**](/windows/desktop/api/Wingdi/nf-wingdi-createpolypolygonrgn)</span></span>                               |



 

<span data-ttu-id="30a69-117">Каждая функция создания региона возвращает маркер, идентифицирующий новый регион.</span><span class="sxs-lookup"><span data-stu-id="30a69-117">Each region creation function returns a handle that identifies the new region.</span></span> <span data-ttu-id="30a69-118">Приложение может использовать этот маркер для выбора региона в контексте устройства путем вызова функции [**SelectObject**](/windows/desktop/api/Wingdi/nf-wingdi-selectobject) и предоставления этого маркера в качестве второго аргумента.</span><span class="sxs-lookup"><span data-stu-id="30a69-118">An application can use this handle to select the region into a device context by calling the [**SelectObject**](/windows/desktop/api/Wingdi/nf-wingdi-selectobject) function and supplying this handle as the second argument.</span></span> <span data-ttu-id="30a69-119">После выбора региона в контексте устройства приложение может выполнять различные операции с ним.</span><span class="sxs-lookup"><span data-stu-id="30a69-119">After a region is selected into a device context, the application can perform various operations on it.</span></span>

 

 



