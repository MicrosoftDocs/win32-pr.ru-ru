---
description: Следующий код очищает всю память, связанную с обработкой символов, для указанного процесса с помощью Симклеануп.
ms.assetid: 270a1984-9e66-4dd2-accb-d715287f1ec0
title: Завершение обработчика символов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9147ed15c0dc03b76c822a38ccd7ac3c5d326454
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104141535"
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



 

 



