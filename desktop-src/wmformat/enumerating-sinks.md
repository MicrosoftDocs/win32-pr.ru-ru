---
title: Перечисление приемников
description: Перечисление приемников
ms.assetid: 1b635cd8-6bdd-4592-bfb5-bcdcf7818e18
keywords:
- Расширенный формат систем (ASF), перечисление приемников
- ASF (Расширенный системный формат), перечисление приемников
- Расширенный формат систем (ASF), приемники
- ASF (Расширенный системный формат), приемники
- приемники, перечисление
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4b51b46f3efdf95902b1ca5b359227da845292c4b0f23dbf0bd52039fba151cd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118029076"
---
# <a name="enumerating-sinks"></a>Перечисление приемников

С модулем записи может быть связано несколько приемников. Можно перечислить приемники, добавленные в модуль записи, с помощью [**ивмвритерадванцед:: жетсинккаунт**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmwriteradvanced-getsinkcount) и [**Ивмвритерадванцед:: Sink**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced-getsink).

В примере кода в [сообщениях об ошибках из приемника](getting-error-messages-from-a-sink.md) демонстрируется перечисление приемника.

> [!Note]  
> При перечислении приемников файл по умолчанию, созданный в ответ на вызов [**ивмвритер:: сетаутпутфиленаме**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-setoutputfilename) , будет перечислен вместе с другими добавленными приемниками. Если вы используете только приемник файлов по умолчанию, вы можете получить к нему доступ, вызвав метод **sink** для индекса приемника 0.

 

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[**Интерфейс Ивмвритерадванцед**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriteradvanced)
</dt> <dt>

[**Работа с приемниками модуля записи**](working-with-writer-sinks.md)
</dt> </dl>

 

 




