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
ms.openlocfilehash: ff35124a8c88108082544b270aa4d9813ff67ea9
ms.sourcegitcommit: b04e152a7f51618fc174ffa872654623fe088db2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/21/2020
ms.locfileid: "103789169"
---
# <a name="enumerating-sinks"></a>Перечисление приемников

С модулем записи может быть связано несколько приемников. Можно перечислить приемники, добавленные в модуль записи, с помощью [**ивмвритерадванцед:: жетсинккаунт**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmwriteradvanced-getsinkcount) и [**Ивмвритерадванцед:: Sink**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced-getsink).

В примере кода в [сообщениях об ошибках из приемника](getting-error-messages-from-a-sink.md) демонстрируется перечисление приемника.

> [!Note]  
> При перечислении приемников файл по умолчанию, созданный в ответ на вызов [**ивмвритер:: сетаутпутфиленаме**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-setoutputfilename) , будет перечислен вместе с другими добавленными приемниками. Если вы используете только приемник файлов по умолчанию, вы можете получить к нему доступ, вызвав метод **sink** для индекса приемника 0.

 

## <a name="related-topics"></a>См. также

<dl> <dt>

[**Интерфейс Ивмвритерадванцед**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriteradvanced)
</dt> <dt>

[**Работа с приемниками модуля записи**](working-with-writer-sinks.md)
</dt> </dl>

 

 




