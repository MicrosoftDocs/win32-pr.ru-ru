---
title: Дескрипторы сериализации
description: Приложение использует процедуры сериализации или процедуры поддержки сериализации, созданные компилятором MIDL, в сочетании с набором библиотечных функций для управления маркером сериализации.
ms.assetid: 39859846-5b94-447a-a71b-a08b8eb2c4c1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 12995144e44fa6b4b91f021d544b53c03d732df22d46489ccc2cefe8d34c0fa1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118925487"
---
# <a name="serialization-handles"></a>Дескрипторы сериализации

Приложение использует процедуры сериализации или процедуры поддержки сериализации, созданные компилятором MIDL, в сочетании с набором библиотечных функций для управления маркером сериализации. Вместе эти функции предоставляют механизм для настройки способа сериализации данных приложением.

Для любой операции сериализации требуется дескриптор сериализации, и все дескрипторы сериализации должны явно управляться вами. Для этого сначала создайте допустимый обработчик, вызвав одну из следующих подпрограмм:

-   [**месдекодебуфферхандлекреате**](/windows/desktop/api/Midles/nf-midles-mesdecodebufferhandlecreate)
-   [**месдекодеинкременталхандлекреате**](/windows/desktop/api/Midles/nf-midles-mesdecodeincrementalhandlecreate)
-   [**месенкодединбуфферхандлекреате**](/windows/desktop/api/Midles/nf-midles-mesencodedynbufferhandlecreate)
-   [**месенкодефикседбуфферхандлекреате**](/windows/desktop/api/Midles/nf-midles-mesencodefixedbufferhandlecreate)
-   [**месенкодеинкременталхандлекреате**](/windows/desktop/api/Midles/nf-midles-mesencodeincrementalhandlecreate)

Вы освобождаете маркер с помощью вызова [**мешандлефри**](/windows/desktop/api/Midles/nf-midles-meshandlefree). После создания или повторной инициализации обработчика он представляет допустимый контекст сериализации и может использоваться для кодирования или декодирования в зависимости от типа маркера.

В этом разделе описываются дескрипторы сериализации и их использование в следующих разделах:

-   [Явные и неявные дескрипторы](implicit-versus-explicit-handles.md)
-   [Стили сериализации](serialization-styles.md)
-   [Получение удостоверения кодировки](obtaining-an-encoding-identity.md)

 

 




