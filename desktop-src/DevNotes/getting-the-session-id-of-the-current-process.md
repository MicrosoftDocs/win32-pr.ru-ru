---
description: Следующий пример кода сборки x86 получает идентификатор сеанса служб терминалов, связанный с текущим процессом.
ms.assetid: 9fcb35cb-6813-46a5-aa38-e102f1b6b7dc
title: Получение идентификатора сеанса текущего процесса
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4326020f145c98544132703611fbd783edac9ae9eb89a5c69f44b67dc997ca30
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118955983"
---
# <a name="getting-the-session-id-of-the-current-process"></a>Получение идентификатора сеанса текущего процесса

\[Адреса памяти, указанные в этом примере кода, могут измениться в следующих выпусках Windows. Чтобы обеспечить правильную работу приложения в будущем, приложение должно вызвать [**жеткуррентпроцессид**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getcurrentprocessid) , а затем [**процессидтосессионид**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-processidtosessionid) вместо следующего примера кода.\]

Следующий пример кода сборки x86 получает идентификатор сеанса служб терминалов, связанный с текущим процессом.

``` syntax
mov     eax,fs:[00000018]
mov     eax,[eax+0x30]
mov     eax,[eax+0x1d4]
```

 

 
