---
description: Инициализация Media Foundation
ms.assetid: e4db81d3-7a9e-47d7-8611-6dac8026259c
title: Инициализация Media Foundation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bb876ec3493d6c4fac1c2f6d6757ef647c511a98
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/03/2021
ms.locfileid: "105674553"
---
# <a name="initializing-media-foundation"></a>Инициализация Media Foundation

Перед использованием любых Microsoft Media Foundation объектов или интерфейсов необходимо вызвать функцию [**мфстартуп**](/windows/desktop/api/mfapi/nf-mfapi-mfstartup) . Передайте постоянную **\_ версию MF**.


```C++
    hr = MFStartup(MF_VERSION);
```



Функция [**мфстартуп**](/windows/desktop/api/mfapi/nf-mfapi-mfstartup) инициализирует Media Foundationную платформу. Если **мфстартуп** возвращает MF \_ \_ неверную \_ начальную \_ версию, это означает, что приложение было скомпилировано с использованием версии Media Foundation заголовков, которые не соответствуют Media Foundationным DLL-библиотекам в системе.

Для каждого вызова [**мфстартуп**](/windows/desktop/api/mfapi/nf-mfapi-mfstartup)приложение должно вызывать [**мфшутдовн**](/windows/desktop/api/mfapi/nf-mfapi-mfshutdown).


```C++
MFShutdown();
```



## <a name="related-topics"></a>См. также

<dl> <dt>

[Архитектура Media Foundation](media-foundation-architecture.md)
</dt> <dt>

[Media Foundation API платформы](media-foundation-platform-apis.md)
</dt> </dl>

 

 



