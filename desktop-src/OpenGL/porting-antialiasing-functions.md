---
title: Перенос функций сглаживания
description: Перенос функций сглаживания
ms.assetid: 7f79f0fa-4a08-4678-bc73-8611e8d9e91a
keywords:
- Перенос GL в ГК, сглаживание
- Перенос из ДИАФРАГМы в ГК, сглаживание
- перенос в OpenGL из IRI GL, сглаживание
- Перенос по стандарту OpenGL из IRI GL, сглаживание
- сглаживание
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9ec2fcae4fe7b6909e00efb0fb892821a5c12765
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104411372"
---
# <a name="porting-antialiasing-functions"></a><span data-ttu-id="1063a-108">Перенос функций сглаживания</span><span class="sxs-lookup"><span data-stu-id="1063a-108">Porting Antialiasing Functions</span></span>

<span data-ttu-id="1063a-109">В OpenGL режим подточки всегда включен, следовательно **, функция IRI** GL (**true**) не требуется и не имеет эквивалента OpenGL.</span><span class="sxs-lookup"><span data-stu-id="1063a-109">In OpenGL the subpixel mode is always on, consequently the IRIS GL function **subpixel**(**TRUE**) is not necessary and has no OpenGL equivalent.</span></span> <span data-ttu-id="1063a-110">В следующих разделах описаны аспекты переноса кода для сглаживания в ГК.</span><span class="sxs-lookup"><span data-stu-id="1063a-110">The following topics describe aspects of porting IRIS GL antialiasing code.</span></span>

-   [<span data-ttu-id="1063a-111">Перенос кода смешения</span><span class="sxs-lookup"><span data-stu-id="1063a-111">Porting Blending Code</span></span>](porting-blending-code.md)
-   [<span data-ttu-id="1063a-112">Перенос тестовых функций афунктион</span><span class="sxs-lookup"><span data-stu-id="1063a-112">Porting afunction Test Functions</span></span>](porting-afunction-test-functions.md)
-   [<span data-ttu-id="1063a-113">Использование функций сглаживания</span><span class="sxs-lookup"><span data-stu-id="1063a-113">Using Antialiasing Functions</span></span>](using-antialiasing-functions.md)

 

 




