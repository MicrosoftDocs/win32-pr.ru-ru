---
description: Функция CreateTimerQueue создает очередь для таймеров.
ms.assetid: ee85a6c3-3a1d-4f94-9112-cb8247b2a189
title: Очереди таймера
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d16e0ae30e02ad9fbc8889c0d7b1094895ebec27c3db8b67acf509ee02e9da85
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118885882"
---
# <a name="timer-queues"></a>Очереди таймера

Функция [**CreateTimerQueue**](/windows/win32/api/threadpoollegacyapiset/nf-threadpoollegacyapiset-createtimerqueue) создает очередь для таймеров. Таймеры в этой очереди, известные как *таймеры очереди*, — это простые объекты, которые позволяют указать функцию обратного вызова, которая будет вызываться при наступлении указанного времени выполнения. Операция ожидания выполняется потоком в [пуле потоков](../procthread/thread-pooling.md).

Чтобы добавить таймер в очередь, вызовите функцию [**CreateTimerQueueTimer**](/windows/win32/api/threadpoollegacyapiset/nf-threadpoollegacyapiset-createtimerqueuetimer) . Чтобы обновить таймер очереди таймера, вызовите функцию [**чанжетимеркуеуетимер**](/windows/win32/api/threadpoollegacyapiset/nf-threadpoollegacyapiset-changetimerqueuetimer) . Вы можете указать функцию обратного вызова, которая будет выполняться рабочим потоком из пула потоков по истечении срока действия таймера.

Чтобы отменить ожидающий таймер, вызовите функцию [**DeleteTimerQueueTimer**](/windows/win32/api/threadpoollegacyapiset/nf-threadpoollegacyapiset-deletetimerqueuetimer) . По завершении работы с очередью таймеров вызовите функцию [**делететимеркуеуикс**](/windows/win32/api/threadpoollegacyapiset/nf-threadpoollegacyapiset-deletetimerqueueex) , чтобы удалить очередь таймера. Все ожидающие таймеры в очереди отменяются и удаляются.

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Использование очередей таймера](using-timer-queues.md)
</dt> </dl>

 

 
