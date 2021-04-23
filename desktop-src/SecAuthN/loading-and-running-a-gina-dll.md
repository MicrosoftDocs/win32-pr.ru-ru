---
description: Windows загружает и выполняет стандартную библиотеку DLL Microsoft GINA (MSGina.dll). Чтобы загрузить другую GINA, необходимо изменить значение раздела реестра.
ms.assetid: 408511af-4430-4dd7-a2a1-c32b375821c4
title: Загрузка и запуск библиотеки DLL GINA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f6242ac0124d85d280d951cbc0bfbdbe748fde0b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105650838"
---
# <a name="loading-and-running-a-gina-dll"></a><span data-ttu-id="52c0a-104">Загрузка и запуск библиотеки DLL GINA</span><span class="sxs-lookup"><span data-stu-id="52c0a-104">Loading and Running a GINA DLL</span></span>

<span data-ttu-id="52c0a-105">Windows загружает и выполняет стандартную библиотеку DLL Microsoft GINA (MSGina.dll).</span><span class="sxs-lookup"><span data-stu-id="52c0a-105">Windows loads and executes the standard Microsoft GINA DLL (MSGina.dll).</span></span> <span data-ttu-id="52c0a-106">Чтобы загрузить другую [*GINA*](../secgloss/g-gly.md), необходимо изменить следующее значение раздела реестра:</span><span class="sxs-lookup"><span data-stu-id="52c0a-106">To load a different [*GINA*](../secgloss/g-gly.md), you must alter the following registry key value:</span></span>

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows NT
            CurrentVersion
               Winlogon
                  GinaDLL<dl>
<dt>

                  Data type
</dt>
<dd>                  REG_SZ</dd>
</dl>
```

<span data-ttu-id="52c0a-107">Если значение ключа Гинадлл имеется, оно должно содержать имя библиотеки DLL GINA, которая будет загружаться и использоваться [*Winlogon*](../secgloss/w-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="52c0a-107">If the GinaDLL key value is present, it must contain the name of a GINA DLL, which [*Winlogon*](../secgloss/w-gly.md) will load and use.</span></span>

## <a name="related-topics"></a><span data-ttu-id="52c0a-108">См. также</span><span class="sxs-lookup"><span data-stu-id="52c0a-108">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="52c0a-109">Создание и тестирование библиотеки DLL GINA</span><span class="sxs-lookup"><span data-stu-id="52c0a-109">Building and Testing a GINA DLL</span></span>](building-and-testing-a-gina-dll.md)
</dt> <dt>

[<span data-ttu-id="52c0a-110">Функции экспорта GINA</span><span class="sxs-lookup"><span data-stu-id="52c0a-110">GINA Export Functions</span></span>](authentication-functions.md)
</dt> <dt>

[<span data-ttu-id="52c0a-111">Структуры GINA</span><span class="sxs-lookup"><span data-stu-id="52c0a-111">GINA Structures</span></span>](authentication-structures.md)
</dt> <dt>

[<span data-ttu-id="52c0a-112">Функции GINA служб терминалов</span><span class="sxs-lookup"><span data-stu-id="52c0a-112">Terminal Services GINA Functions</span></span>](terminal-services-gina-functions.md)
</dt> </dl>

 

 
