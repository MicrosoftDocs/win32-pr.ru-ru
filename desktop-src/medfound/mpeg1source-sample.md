---
description: Пример MPEG1Source
ms.assetid: c9f131ff-0b79-487c-9a46-a9b1350553a1
title: Пример MPEG1Source
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 652a58877267eaa92f906de88d40e614ce5b598220d4b76030caffa2187c8626
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118058842"
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

в Windows SDK для Windows Server 2008 этот пример также включает пример видеодекодера MPEG-1, который отображает код времени для каждого кадра видео. (В действительности он не расшифровывает битовый поток MPEG-1.)

начиная с Windows SDK для Windows 7 декодер был перемещен в отдельный пример. См. [Пример декодера](decoder-sample.md).

## <a name="usage"></a>Использование

В примере MPEG1Source создается библиотека DLL, которая является сервером COM для источника мультимедиа, обработчиком потока байтов источника мультимедиа и файлом MFT декодера. Прежде чем использовать источник мультимедиа, необходимо зарегистрировать библиотеку DLL.

Чтобы использовать источник мультимедиа, можно запустить [Пример басикплайбакк](/previous-versions//bb970475(v=vs.85)). Сопоставитель источника автоматически загрузит источник мультимедиа, если для воспроизведения выбран файл MPEG-1. (При возникновении ошибки убедитесь, что библиотека DLL MPEG1Source успешно зарегистрирована.)

Можно также использовать средство Топоедит для создания топологии воспроизведения, содержащей источник мультимедиа. Дополнительные сведения о Топоедит см. в разделе [топоедит](topoedit.md).

## <a name="requirements"></a>Требования



| Продукт                                                        | Version   |
|----------------------------------------------------------------|-----------|
| [Windows SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx) | Windows 7 |



 

## <a name="downloading-the-sample"></a>Загрузка образца

этот пример доступен в [репозитории github для классических примеров Windows](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/multimedia/mediafoundation/mpeg1source).

## <a name="related-topics"></a>Связанные темы

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

 

 
