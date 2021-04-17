---
description: Функция CreateTimerQueue создает очередь для таймеров.
ms.assetid: ee85a6c3-3a1d-4f94-9112-cb8247b2a189
title: Очереди таймера
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 80ad2f94612c234b3ec0d1d75fa723c4e86e6fc0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105663412"
---
# <a name="timer-queues"></a>Очереди таймера

Функция [**CreateTimerQueue**](/windows/win32/api/threadpoollegacyapiset/nf-threadpoollegacyapiset-createtimerqueue) создает очередь для таймеров. Таймеры в этой очереди, известные как *таймеры очереди*, — это простые объекты, которые позволяют указать функцию обратного вызова, которая будет вызываться при наступлении указанного времени выполнения. Операция ожидания выполняется потоком в [пуле потоков](../procthread/thread-pooling.md).

Чтобы добавить таймер в очередь, вызовите функцию [**CreateTimerQueueTimer**](/windows/win32/api/threadpoollegacyapiset/nf-threadpoollegacyapiset-createtimerqueuetimer) . Чтобы обновить таймер очереди таймера, вызовите функцию [**чанжетимеркуеуетимер**](/windows/win32/api/threadpoollegacyapiset/nf-threadpoollegacyapiset-changetimerqueuetimer) . Вы можете указать функцию обратного вызова, которая будет выполняться рабочим потоком из пула потоков по истечении срока действия таймера.

Чтобы отменить ожидающий таймер, вызовите функцию [**DeleteTimerQueueTimer**](/windows/win32/api/threadpoollegacyapiset/nf-threadpoollegacyapiset-deletetimerqueuetimer) . По завершении работы с очередью таймеров вызовите функцию [**делететимеркуеуикс**](/windows/win32/api/threadpoollegacyapiset/nf-threadpoollegacyapiset-deletetimerqueueex) , чтобы удалить очередь таймера. Все ожидающие таймеры в очереди отменяются и удаляются.

## <a name="related-topics"></a>См. также

<dl> <dt>

[Использование очередей таймера](using-timer-queues.md)
</dt> </dl>

 

 
