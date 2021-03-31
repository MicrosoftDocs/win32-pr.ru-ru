---
title: Иажентексая версия
description: Иажентексая версия
ms.assetid: e5d55fcd-c1b4-4c9e-b3c7-4471af2f86af
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 359abb1d22e2cd34fb6b31d85012ac0110f14037
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104330856"
---
# <a name="iagentexgetversion"></a><span data-ttu-id="3cf31-103">Иажентекс::/версия</span><span class="sxs-lookup"><span data-stu-id="3cf31-103">IAgentEx::GetVersion</span></span>

<span data-ttu-id="3cf31-104">\[Microsoft Agent является устаревшим в Windows 7 и может быть недоступен в последующих версиях Windows.\]</span><span class="sxs-lookup"><span data-stu-id="3cf31-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetVersion(
   short * psMajor,  // address of major version
   short * psMinor   // address of minor version
);
```

<span data-ttu-id="3cf31-105">Возвращает номер версии сервера Microsoft Agent Server.</span><span class="sxs-lookup"><span data-stu-id="3cf31-105">Retrieves the version number of Microsoft Agent server.</span></span>

-   <span data-ttu-id="3cf31-106">Возвращает значение S \_ , чтобы указать, что операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="3cf31-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="3cf31-107"><span id="psMajor"></span><span id="psmajor"></span><span id="PSMAJOR"></span>*псмажор*</span><span class="sxs-lookup"><span data-stu-id="3cf31-107"><span id="psMajor"></span><span id="psmajor"></span><span id="PSMAJOR"></span>*psMajor*</span></span>
</dt> <dd>

<span data-ttu-id="3cf31-108">Адрес переменной, которая получает основной номер версии.</span><span class="sxs-lookup"><span data-stu-id="3cf31-108">Address of a variable that receives the major version.</span></span>

</dd> <dt>

<span data-ttu-id="3cf31-109"><span id="psMinor"></span><span id="psminor"></span><span id="PSMINOR"></span>*псминор*</span><span class="sxs-lookup"><span data-stu-id="3cf31-109"><span id="psMinor"></span><span id="psminor"></span><span id="PSMINOR"></span>*psMinor*</span></span>
</dt> <dd>

<span data-ttu-id="3cf31-110">Адрес переменной, которая получает дополнительный номер версии.</span><span class="sxs-lookup"><span data-stu-id="3cf31-110">Address of a variable that receives the minor version.</span></span>

</dd> </dl>

 

 




