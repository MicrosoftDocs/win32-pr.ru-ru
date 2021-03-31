---
title: Иажентчарактерексая версия
description: Иажентчарактерексая версия
ms.assetid: 78f6d7b6-f72d-4af8-a014-3acd185926f0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0f5c72d9304aa689cda83117d57f26c2da776c9f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104067787"
---
# <a name="iagentcharacterexgetversion"></a><span data-ttu-id="493fb-103">Иажентчарактерекс::/версия</span><span class="sxs-lookup"><span data-stu-id="493fb-103">IAgentCharacterEx::GetVersion</span></span>

<span data-ttu-id="493fb-104">\[Microsoft Agent является устаревшим в Windows 7 и может быть недоступен в последующих версиях Windows.\]</span><span class="sxs-lookup"><span data-stu-id="493fb-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetVersion(
   short * psMajor,  // address of major version
   short * psMinor   // address of minor version
);
```

<span data-ttu-id="493fb-105">Возвращает номер версии набора стандартных анимаций символов.</span><span class="sxs-lookup"><span data-stu-id="493fb-105">Retrieves the version number of the character standard animation set.</span></span>

-   <span data-ttu-id="493fb-106">Возвращает значение S \_ , чтобы указать, что операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="493fb-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="493fb-107"><span id="psMajor"></span><span id="psmajor"></span><span id="PSMAJOR"></span>*псмажор*</span><span class="sxs-lookup"><span data-stu-id="493fb-107"><span id="psMajor"></span><span id="psmajor"></span><span id="PSMAJOR"></span>*psMajor*</span></span>
</dt> <dd>

<span data-ttu-id="493fb-108">Адрес переменной, которая получает основной номер версии.</span><span class="sxs-lookup"><span data-stu-id="493fb-108">Address of a variable that receives the major version.</span></span>

</dd> <dt>

<span data-ttu-id="493fb-109"><span id="psMinor"></span><span id="psminor"></span><span id="PSMINOR"></span>*псминор*</span><span class="sxs-lookup"><span data-stu-id="493fb-109"><span id="psMinor"></span><span id="psminor"></span><span id="PSMINOR"></span>*psMinor*</span></span>
</dt> <dd>

<span data-ttu-id="493fb-110">Адрес переменной, которая получает дополнительный номер версии.</span><span class="sxs-lookup"><span data-stu-id="493fb-110">Address of a variable that receives the minor version.</span></span>

</dd> </dl>

<span data-ttu-id="493fb-111">Номер версии стандартного набора анимации автоматически задается при сборке с помощью редактора символов Microsoft Agent.</span><span class="sxs-lookup"><span data-stu-id="493fb-111">The standard animation set version number is automatically set when you build it with the Microsoft Agent Character Editor.</span></span>

 

 




