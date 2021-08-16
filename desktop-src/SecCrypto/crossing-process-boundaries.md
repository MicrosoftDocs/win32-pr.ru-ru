---
description: Механизм протокола Schannel выполняет подтверждение и проверку подлинности в безопасном процессе, а также в процессе приложения.
ms.assetid: bcd49aaf-b0e3-4c31-be95-986b8ad843a8
title: Пересечение границ процессов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e0f8ba4c2d7a0a80ad97e62487421b5b4a0a6f8deda9d8edb550c2d8fcddab15
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117768885"
---
# <a name="crossing-process-boundaries"></a>Пересечение границ процессов

Механизм протокола [*SChannel*](../secgloss/s-gly.md) выполняет подтверждение и проверку подлинности в безопасном [*процессе*](../secgloss/p-gly.md) , а также в процессе приложения. Это означает, что [*ключи с массовым шифрованием*](../secgloss/b-gly.md) и ключи [*Mac*](../secgloss/m-gly.md) должны быть скопированы из одного процесса в другой. Чтобы скопировать ключи из одного процесса в другой, используйте функции [**криптекспорткэй**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportkey) и [**криптимпорткэй**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptimportkey) следующим образом:

1.  Безопасный процесс экспортирует каждый ключ в [*опакуекэйблоб*](../secgloss/o-gly.md) с помощью [**криптекспорткэй**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportkey), а затем уничтожает ключ с помощью [**криптдестройкэй**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdestroykey). Обратите внимание, что если ключ хранится на оборудовании, CSP должен распознать его и не должен пытаться уничтожить ключ.
2.  Безопасный процесс передает Опакуекэйблобс в процесс приложения за пределами области этого документа.
3.  Процесс приложения импортирует каждый ОПАКУЕКЭЙБЛОБ обратно в CSP с помощью [**криптимпорткэй**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptimportkey). На этом этапе ключ должен находиться в том же [*состоянии*](../secgloss/s-gly.md) , что и при его экспорте.

 

 
