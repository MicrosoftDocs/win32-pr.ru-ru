---
description: Инициализация Media Foundation
ms.assetid: e4db81d3-7a9e-47d7-8611-6dac8026259c
title: Инициализация Media Foundation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 202ab57db5821b252001a723eb8765493eb86362111da5c54e5e16e9fca4219a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119268924"
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



## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Архитектура Media Foundation](media-foundation-architecture.md)
</dt> <dt>

[Media Foundation API платформы](media-foundation-platform-apis.md)
</dt> </dl>

 

 



