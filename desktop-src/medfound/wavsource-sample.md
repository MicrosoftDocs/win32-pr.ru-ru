---
description: Пример Вавсаурце
ms.assetid: 905fbba5-0a04-4048-80bd-f8707c4879da
title: Пример Вавсаурце
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 050edb9df75032384f93c6e1f37c52e89f14a748
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103898690"
---
# <a name="wavsource-sample"></a>Пример Вавсаурце

Показывает, как создать пользовательский источник мультимедиа в Microsoft Media Foundation. В примере реализуется источник мультимедиа, который анализирует звуковые файлы WAV.

Этот пример является относительно простым примером источника мультимедиа:

-   Существует только один поток, поэтому нет кода для реализации выбора потоков.
-   Источник мультимедиа не реализует управление скоростью (т. е. Перемотка вперед или обратная воспроизведение).
-   Все методы источника и потока реализуются как синхронные методы.
-   Так как часть данных WAV-файла является одним блоком несжатого звука PCM, источнику мультимедиа не нужно считывать заголовки пакетов или иным образом анализировать поток во время воспроизведения, кроме считывания начального заголовка [**вавеформат**](/windows/win32/api/mmreg/ns-mmreg-waveformat) .

Более сложный пример источника мультимедиа см. в [примере MPEG1Source](mpeg1source-sample.md).

## <a name="apis-demonstrated"></a>Продемонстрированные API

В этом образце демонстрируются следующие интерфейсы Media Foundation:

-   [**имфбитестреамхандлер**](/windows/desktop/api/mfidl/nn-mfidl-imfbytestreamhandler)
-   [**имфмедиасаурце**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource)
-   [**имфмедиастреам**](/windows/desktop/api/mfidl/nn-mfidl-imfmediastream)

## <a name="usage"></a>Использование

В примере Вавсаурце создается библиотека DLL, которая является COM-сервером как для источника мультимедиа, так и для обработчика потока байтов источника мультимедиа. Прежде чем использовать источник мультимедиа, необходимо зарегистрировать библиотеку DLL.

Чтобы использовать источник мультимедиа, можно запустить [басикплайбакк](/previous-versions//bb970475(v=vs.85)). Сопоставитель источника автоматически загрузит источник мультимедиа, если выбрать WAV-файл для воспроизведения. (При возникновении ошибки убедитесь, что библиотека DLL Вавсаурце успешно зарегистрирована.)

Можно также использовать средство Топоедит для создания топологии воспроизведения, содержащей источник мультимедиа. Дополнительные сведения о Топоедит см. в разделе [топоедит](topoedit.md).

## <a name="requirements"></a>Требования



| Продукт                                                        | Version   |
|----------------------------------------------------------------|-----------|
| [Windows SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx) | Windows 7 |



 

## <a name="downloading-the-sample"></a>Загрузка образца

Этот пример доступен в [репозитории GitHub с классическими примерами Windows](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/multimedia/mediafoundation/wavsource).

## <a name="related-topics"></a>См. также

<dl> <dt>

[Примеры пакетов SDK Media Foundation](media-foundation-sdk-samples.md)
</dt> <dt>

[Источники мультимедиа](media-sources.md)
</dt> <dt>

[Пример MPEG1Source](mpeg1source-sample.md)
</dt> <dt>

[Обработчики схем и обработчики Byte-Stream](scheme-handlers-and-byte-stream-handlers.md)
</dt> <dt>

[Запись пользовательского источника мультимедиа](writing-a-custom-media-source.md)
</dt> </dl>

 

 
