---
description: Пример MPEG1Source
ms.assetid: c9f131ff-0b79-487c-9a46-a9b1350553a1
title: Пример MPEG1Source
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9c71bd541a7bd01621ca7359eb9e229a08e91a04
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105650628"
---
# <a name="mpeg1source-sample"></a>Пример MPEG1Source

Описание процесса записи пользовательского источника мультимедиа в Microsoft Media Foundation. В примере реализуется источник мультимедиа, который анализирует потоки на уровне системы MPEG-1 и создает образцы, содержащие полезные данные MPEG-1.

## <a name="apis-demonstrated"></a>Продемонстрированные API

В этом образце демонстрируются следующие интерфейсы Media Foundation:

-   [**имфбитестреамхандлер**](/windows/desktop/api/mfidl/nn-mfidl-imfbytestreamhandler)
-   [**имфмедиасаурце**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource)
-   [**имфмедиастреам**](/windows/desktop/api/mfidl/nn-mfidl-imfmediastream)

Перед изучением этого примера может потребоваться ознакомиться с [примером вавсаурце](wavsource-sample.md), который предоставляет более простую реализацию источника мультимедиа. В примере MPEG1Source добавляются некоторые функции, которые можно найти в большинстве реальных реализаций источника мультимедиа:

-   Несколько потоков
-   Асинхронные методы
-   Асинхронный ввод-вывод

В Windows SDK для Windows Server 2008 этот пример также включает пример видеодекодера MPEG-1, который отображает код времени для каждого кадра видео. (В действительности он не расшифровывает битовый поток MPEG-1.)

Начиная с Windows SDK для Windows 7 декодер был перемещен в отдельный пример. См. [Пример декодера](decoder-sample.md).

## <a name="usage"></a>Использование

В примере MPEG1Source создается библиотека DLL, которая является сервером COM для источника мультимедиа, обработчиком потока байтов источника мультимедиа и файлом MFT декодера. Прежде чем использовать источник мультимедиа, необходимо зарегистрировать библиотеку DLL.

Чтобы использовать источник мультимедиа, можно запустить [Пример басикплайбакк](/previous-versions//bb970475(v=vs.85)). Сопоставитель источника автоматически загрузит источник мультимедиа, если для воспроизведения выбран файл MPEG-1. (При возникновении ошибки убедитесь, что библиотека DLL MPEG1Source успешно зарегистрирована.)

Можно также использовать средство Топоедит для создания топологии воспроизведения, содержащей источник мультимедиа. Дополнительные сведения о Топоедит см. в разделе [топоедит](topoedit.md).

## <a name="requirements"></a>Требования



| Продукт                                                        | Version   |
|----------------------------------------------------------------|-----------|
| [Windows SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx) | Windows 7 |



 

## <a name="downloading-the-sample"></a>Загрузка образца

Этот пример доступен в [репозитории GitHub с классическими примерами Windows](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/multimedia/mediafoundation/mpeg1source).

## <a name="related-topics"></a>См. также

<dl> <dt>

[Примеры пакетов SDK Media Foundation](media-foundation-sdk-samples.md)
</dt> <dt>

[Источники мультимедиа](media-sources.md)
</dt> <dt>

[Обработчики схем и обработчики Byte-Stream](scheme-handlers-and-byte-stream-handlers.md)
</dt> <dt>

[Учебник. запись пользовательского источника мультимедиа](tutorial--writing-a-custom-media-source.md)
</dt> <dt>

[Пример Вавсаурце](wavsource-sample.md)
</dt> </dl>

 

 
