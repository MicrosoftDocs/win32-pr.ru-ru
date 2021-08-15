---
title: Использование обратного вызова события для обработки сообщений драйвера
description: Использование обратного вызова события для обработки сообщений драйвера
ms.assetid: 5b17ff93-ed00-46ee-828c-baf716c9257c
keywords:
- звуковая волна, обратный вызов события
- блоки звуковых данных, обратный вызов события
- звуковая волна, обработка сообщений драйвера
- блоки звуковых данных, обработка сообщений драйверов
- Обработка сообщений драйвера
- Функция CreateEvent
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 70c5bdbfe46fed9fa9124a031e90af3bfefb983caf6743415d90c645afc42c6e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117801204"
---
# <a name="using-an-event-callback-to-process-driver-messages"></a>Использование обратного вызова события для обработки сообщений драйвера

Чтобы использовать обратный вызов события, используйте функцию [**CreateEvent**](/windows/desktop/api/synchapi/nf-synchapi-createeventa) для создания события ручного сброса. В вызове функции [**вавеаутопен**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutopen) укажите **\_ событие обратного вызова** для параметра *фдвопен* . После вызова функции [**вавеаутпрепарехеадер**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutprepareheader) , но перед отправкой данных аудио-сигнала на устройство, переведите событие в несигнальное состояние, вызвав функцию [**ресетевент**](/windows/desktop/api/synchapi/nf-synchapi-resetevent) . Затем внутри цикла, который проверяет, установлен ли **флаг вхдр \_ done** в элементе **dwFlags** структуры [**вавехдр**](/windows/win32/api/mmeapi/ns-mmeapi-wavehdr) , вызовите функцию [WaitForSingleObject](/windows/win32/api/synchapi/nf-synchapi-waitforsingleobject) , указав в качестве параметров маркер события и значение времени ожидания.

Поскольку обратные вызовы событий не получают конкретных закрытых, готовых или открытых уведомлений, приложению может потребоваться проверить состояние процесса, ожидающего выполнения после наступления события. Возможно, число задач было завершено в момент возвращения объекта [**WaitForSingleObject**](/windows/desktop/api/synchapi/nf-synchapi-waitforsingleobject) .

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Звуковые блоки данных](audio-data-blocks.md)
</dt> </dl>

 

 