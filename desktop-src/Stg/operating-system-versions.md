---
title: Версии операционной системы
description: Этот тип данных DWORD должен содержать тип операционной системы в слове высокого порядка и номер версии операционной системы в младшем слове. Возможные значения для операционной системы перечислены в следующей таблице.
ms.assetid: 318e277b-a797-45a5-87c5-25b91fdf278d
keywords:
- Структурированное хранилище версий операционной системы
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fd5de916d354a721834b9a10651c36d3bf389e28
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "105661739"
---
# <a name="operating-system-versions"></a><span data-ttu-id="948eb-105">Версии операционной системы</span><span class="sxs-lookup"><span data-stu-id="948eb-105">Operating System Versions</span></span>

<span data-ttu-id="948eb-106">Этот тип данных **DWORD** должен содержать тип операционной системы в слове высокого порядка и номер версии операционной системы в младшем слове.</span><span class="sxs-lookup"><span data-stu-id="948eb-106">This **DWORD** data type should hold the operating system type in the high-order word and the version number of the operating system in the low-order word.</span></span> <span data-ttu-id="948eb-107">Возможные значения для операционной системы перечислены в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="948eb-107">Possible values for the operating system are listed in the following table.</span></span>



| <span data-ttu-id="948eb-108">Операционная система</span><span class="sxs-lookup"><span data-stu-id="948eb-108">Operating system</span></span>       | <span data-ttu-id="948eb-109">Значение</span><span class="sxs-lookup"><span data-stu-id="948eb-109">Value</span></span>  |
|------------------------|--------|
| <span data-ttu-id="948eb-110">32-разрядная версия Windows (Win32)</span><span class="sxs-lookup"><span data-stu-id="948eb-110">32-Bit Windows (Win32)</span></span> | <span data-ttu-id="948eb-111">0x0002</span><span class="sxs-lookup"><span data-stu-id="948eb-111">0x0002</span></span> |
| <span data-ttu-id="948eb-112">Macintosh</span><span class="sxs-lookup"><span data-stu-id="948eb-112">Macintosh</span></span>              | <span data-ttu-id="948eb-113">0x0001</span><span class="sxs-lookup"><span data-stu-id="948eb-113">0x0001</span></span> |
| <span data-ttu-id="948eb-114">16-разрядная версия Windows (Win16)</span><span class="sxs-lookup"><span data-stu-id="948eb-114">16-Bit Windows (Win16)</span></span> | <span data-ttu-id="948eb-115">0x0000</span><span class="sxs-lookup"><span data-stu-id="948eb-115">0x0000</span></span> |



 

<span data-ttu-id="948eb-116">Для операционных систем Microsoft Windows версия операционной системы — это младшее слово, возвращаемое функцией [**инверсии**](/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getversion) .</span><span class="sxs-lookup"><span data-stu-id="948eb-116">For Microsoft Windows operating systems, the operating system version is the low-order word returned by the [**GetVersion**](/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getversion) function.</span></span> <span data-ttu-id="948eb-117">В следующем примере кода для Microsoft Windows правильно задается версия исходной операционной системы.</span><span class="sxs-lookup"><span data-stu-id="948eb-117">For Microsoft Windows, the following example code correctly sets the version of the originating operating system.</span></span>

``` syntax
#ifdef WIN32 
    dwOSVer = (DWORD)MAKELONG( LOWORD(GetVersion()), 2 ) ; 
#else 
    dwOSVer = (DWORD)MAKELONG( LOWORD(GetVersion()), 0 ) ; 
#endif
```

 

 