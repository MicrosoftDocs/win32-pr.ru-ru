---
description: Из-за того, что существуют статически связываемые DLL, следует избегать использования Microsoft Foundation Classes (Мфкс) для написания эксперта.
ms.assetid: 634852fd-d0e0-42a7-90af-e93cc0e4ac84
title: Использование Microsoft Foundation Classes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 097c4baea2ec109933d52eed420042528e9eea76
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103815176"
---
# <a name="using-microsoft-foundation-classes"></a><span data-ttu-id="e8959-103">Использование Microsoft Foundation Classes</span><span class="sxs-lookup"><span data-stu-id="e8959-103">Using Microsoft Foundation Classes</span></span>

<span data-ttu-id="e8959-104">Из-за того, что существуют статически связываемые DLL, следует избегать использования Microsoft Foundation Classes (Мфкс) для написания эксперта.</span><span class="sxs-lookup"><span data-stu-id="e8959-104">Because of the footprint of statically linked DLLs, you should avoid using Microsoft Foundation Classes (MFCs) to write an expert.</span></span> <span data-ttu-id="e8959-105">Однако при использовании MFC Обеспечьте доступ к любому из ресурсов библиотеки DLL MFC, включив следующий код сразу после записи:</span><span class="sxs-lookup"><span data-stu-id="e8959-105">However, if you use the MFC, ensure access to any of the MFC DLL resources by including the following code immediately upon entry:</span></span>

``` syntax
#ifdef _AFXDLL
      AFX_MANAGE_STATE(AfxGetStaticModuleState());
#endif
```

 

 



