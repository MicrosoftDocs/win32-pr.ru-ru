---
description: Два режима сопоставления, определяемые приложением ( \_ исотропик и \_ "анизотропная" мм), предоставляются для режимов сопоставления, зависящих от приложения.
ms.assetid: c4c4e352-63fc-4e97-a218-a1b7deac02e8
title: Режимы сопоставления Application-Defined
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d800a3ce631ebffeef8223fc53ec505c10cb69f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104997435"
---
# <a name="application-defined-mapping-modes"></a><span data-ttu-id="e8aa3-103">Режимы сопоставления Application-Defined</span><span class="sxs-lookup"><span data-stu-id="e8aa3-103">Application-Defined Mapping Modes</span></span>

<span data-ttu-id="e8aa3-104">Два режима сопоставления, определяемые приложением ( \_ исотропик и \_ "анизотропная" мм), предоставляются для режимов сопоставления, зависящих от приложения.</span><span class="sxs-lookup"><span data-stu-id="e8aa3-104">The two application-defined mapping modes (MM\_ISOTROPIC and MM\_ANISOTROPIC) are provided for application-specific mapping modes.</span></span> <span data-ttu-id="e8aa3-105">\_Режим ИСОТРОПИК мм гарантирует, что логические единицы в направлении по оси x и в направлении оси y равны, а в \_ анизотропном режиме mm можно различать единицы.</span><span class="sxs-lookup"><span data-stu-id="e8aa3-105">The MM\_ISOTROPIC mode guarantees that logical units in the x-direction and in the y-direction are equal, while the MM\_ANISOTROPIC mode allows the units to differ.</span></span> <span data-ttu-id="e8aa3-106">Приложение САПР или чертежа может использовать преимущества \_ режима СОПОСТАВЛЕНИЯ mm исотропик, но может потребоваться указать логические устройства, которые соответствуют приращениям в масштабе инженера (1/64 дюйма).</span><span class="sxs-lookup"><span data-stu-id="e8aa3-106">A CAD or drawing application can benefit from the MM\_ISOTROPIC mapping mode but may need to specify logical units that correspond to the increments on an engineer's scale (1/64 inch).</span></span> <span data-ttu-id="e8aa3-107">Эти единицы было бы трудно получить с помощью стандартных режимов сопоставления (мм \_ хиенглиш или mm \_ HIMETRIC), однако их можно легко получить, ВЫБРАВ \_ режим мм ИСОТРОПИК (или мм \_ анизотропный).</span><span class="sxs-lookup"><span data-stu-id="e8aa3-107">These units would be difficult to obtain with the predefined mapping modes (MM\_HIENGLISH or MM\_HIMETRIC); however, they can easily be obtained by selecting the MM\_ISOTROPIC (or MM\_ANISOTROPIC) mode.</span></span> <span data-ttu-id="e8aa3-108">В следующем примере показано, как установить логические устройства в 1/64 дюйма:</span><span class="sxs-lookup"><span data-stu-id="e8aa3-108">The following example shows how to set logical units to 1/64 inch:</span></span>


```C++
SetMapMode(hDC, MM_ISOTROPIC); 
SetWindowExtEx(hDC, 64, 64, NULL); 
SetViewportExtEx(hDC, GetDeviceCaps(hDC, LOGPIXELSX), 
                      GetDeviceCaps(hDC, LOGPIXELSY), NULL); 
```



 

 



