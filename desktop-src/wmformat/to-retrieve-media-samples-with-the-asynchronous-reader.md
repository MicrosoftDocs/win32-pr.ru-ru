---
title: Получение примеров мультимедиа с помощью асинхронного модуля чтения
description: Получение примеров мультимедиа с помощью асинхронного модуля чтения
ms.assetid: 0d8c3099-f068-4074-b717-2f5b9ed9eeb8
keywords:
- Расширенный формат систем (ASF), получение примеров мультимедиа
- ASF (Расширенный системный формат), получение примеров мультимедиа
- Расширенный системный формат (ASF), асинхронный читатель
- ASF (Расширенный системный формат), асинхронный читатель
- асинхронные читатели, получение примеров мультимедиа
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fb0419619ea99bd3734db67f8e658b1f3ff058a3
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/19/2020
ms.locfileid: "104069553"
---
# <a name="to-retrieve-media-samples-with-the-asynchronous-reader"></a>Получение примеров мультимедиа с помощью асинхронного модуля чтения

После получения \_ сообщения о состоянии Open ВМТ в реализации [**ивмстатускаллбакк:: OnStatus**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstatuscallback-onstatus)можно начать получать примеры, вызвав [**ивмреадер:: Start**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-start). Асинхронный читатель предоставляет примеры для реализации [**ивмреадеркаллбакк:: OnSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreadercallback-onsample). Образцы предоставляются в порядке, определенном во время презентации.

**Start** — это асинхронный вызов. Он возвратит практически сразу и продолжит работу в отдельных потоках. Асинхронный модуль чтения использует несколько потоков при декодировании содержимого и доставке образцов. По достижении конца файла средство чтения отправляет \_ сообщение о состоянии ВМТ EOF в реализацию обратного вызова **OnStatus** . При \_ отправке ВМТ EOF модуль чтения останавливает собственную обработку; вам не нужно отвечать на ВМТ \_ EOF с вызовом [**Ивмреадер:: Stop**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-stop).

## <a name="related-topics"></a>См. также

<dl> <dt>

[**Интерфейс Ивмреадер**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreader)
</dt> <dt>

[**Реализация сообщений модуля чтения в обратном вызове OnStatus**](to-implement-reader-messages-in-the-onstatus-callback.md)
</dt> <dt>

[**Реализация обратного вызова OnSample**](to-implement-the-onsample-callback.md)
</dt> </dl>

 

 




