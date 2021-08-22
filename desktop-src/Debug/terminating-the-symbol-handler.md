---
description: Следующий код очищает всю память, связанную с обработкой символов, для указанного процесса с помощью Симклеануп.
ms.assetid: 270a1984-9e66-4dd2-accb-d715287f1ec0
title: Завершение обработчика символов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af49c26ffe1a80fad3bf7b03fc18699c07e9b025e8b07b5f6bb6c377cde743b7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118956943"
---
# <a name="terminating-the-symbol-handler"></a>Завершение обработчика символов

Следующий код очищает всю память, связанную с обработкой символов, для указанного процесса с помощью [**симклеануп**](/windows/desktop/api/Dbghelp/nf-dbghelp-symcleanup).


```C++
if (SymCleanup(hProcess))
{
    // SymCleanup returned success
}
else
{
    // SymCleanup failed
    DWORD error = GetLastError();
    printf("SymCleanup returned error : %d\n", error);
}
```



 

 



