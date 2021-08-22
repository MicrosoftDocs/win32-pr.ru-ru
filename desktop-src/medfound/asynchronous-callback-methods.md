---
description: Асинхронные методы обратного вызова
ms.assetid: ea778eaa-6460-4a93-bd6a-1857ea8b6230
title: Асинхронные методы обратного вызова
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e59fec2423d6bc1b02a3f5ce05855419596bc92ea54062303ebd1315d087e489
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119606714"
---
# <a name="asynchronous-callback-methods"></a>Асинхронные методы обратного вызова

Media Foundation предоставляет единообразный способ реализации асинхронных методов с помощью интерфейса обратного вызова.

В этом разделе описывается реализация интерфейса обратного вызова и написание асинхронных методов, использующих этот интерфейс. Он содержит следующие разделы.



| Раздел                                                                                | Описание                                                                                         |
|--------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------|
| [Вызов асинхронных методов](calling-asynchronous-methods.md)                     | Как вызывать асинхронные методы в Media Foundation.                                               |
| [Реализация асинхронного обратного вызова](implementing-the-asynchronous-callback.md) | Реализация метода обратного вызова в интерфейсе [**имфасинккаллбакк**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) . |
| [Поддержка нескольких обратных вызовов](supporting-multiple-callbacks.md)                   | Поддержка нескольких обратных вызовов в одном и том же классе C++.                                        |
| [Рабочие очереди](work-queues.md)                                                       | Рабочие очереди предоставляют эффективный способ выполнения асинхронных операций в другом потоке.          |
| [Создание асинхронного метода](writing-an-asynchronous-method.md)                 | Реализация асинхронных методов в Media Foundation.                                          |
| [Пользовательские объекты асинхронных результатов](custom-asynchronous-result-objects.md)         | Как предоставить пользовательскую реализацию интерфейса [**имфасинкресулт**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasyncresult) .   |



 

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[**Интерфейс Имфасинккаллбакк**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback)
</dt> <dt>

[**Интерфейс Имфасинкресулт**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasyncresult)
</dt> <dt>

[Media Foundation API платформы](media-foundation-platform-apis.md)
</dt> </dl>

 

 



