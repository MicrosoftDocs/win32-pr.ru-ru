---
title: Что нового в проигрывателе Windows Media 11
description: В этом разделе перечислены новые возможности проигрывателя Windows Media 11 и пакета SDK для проигрывателя Windows Media 11.
ms.assetid: d2a6b6ce-a924-4b55-9dc7-68cc57e5651f
keywords:
- Проигрыватель Windows Media, новые возможности
- Проигрыватель Windows Media, новые функции
- пакет средств разработки программного обеспечения (SDK), проигрыватель Windows Media 11
- Пакет SDK (пакет средств разработки программного обеспечения), проигрыватель Windows Media 11
- Документация, Windows Media Player 11 SDK
- новые возможности, проигрыватель Windows Media 11
- новые возможности, проигрыватель Windows Media 11
- интерфейсы, новые возможности в проигрывателе Windows Media 11
- атрибуты, новые возможности в проигрывателе Windows Media 11
- Элемент управления ActiveX проигрывателя Windows Media, новые функции в версии 11
- Элемент управления ActiveX, новые функции в версии 11
- обложки, новые функции в проигрывателе Windows Media 11
- Обложки проигрывателя Windows Media, новые функции в версии 11
- подключаемые модули, новые функции в проигрывателе Windows Media 11
- Подключаемые модули проигрывателя Windows Media, новые возможности в версии 11
- Интернет-магазины, новые функции в проигрывателе Windows Media 11
- Интернет-магазины проигрывателя Windows Media, новые функции в версии 11
- Примеры, новые функции в проигрывателе Windows Media 11
- версии проигрывателя Windows Media, новые функции в версии 11
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 12aa728aa1552ac0e65f5825cad62d8e9e0c7300
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/25/2020
ms.locfileid: "104069697"
---
# <a name="what-was-new-in-windows-media-player-11"></a>Что нового в проигрывателе Windows Media 11

В этом разделе перечислены новые возможности проигрывателя Windows Media 11 и пакета SDK для проигрывателя Windows Media 11.

## <a name="windows-media-player-control"></a>Элемент управления проигрывателя Windows Media

Следующие интерфейсы были впервые созданы в элементе управления ActiveX проигрывателя Windows Media 11.

-   [**Интерфейс Ивмплибрари**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmplibrary)
-   [**Интерфейс Ивмплибрарисервицес**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmplibraryservices)
-   [**Интерфейс Ивмплибраришарингсервицес**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmplibrarysharingservices)
-   [**Интерфейс IWMPMediaCollection2**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpmediacollection2)
-   [**Интерфейс Ивмпкуери**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpquery)
-   [**Интерфейс IWMPStringCollection2**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpstringcollection2)
-   [**Объект Медиаколлектион**](mediacollection-object.md)
-   [**Объект запроса**](query-object.md)
-   [**Объект StringCollection**](stringcollection-object.md)
-   [**Интерфейс Ивмпкдромрип**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcdromrip)
-   [**Интерфейс Ивмпкдромбурн**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcdromburn)
-   [**Интерфейс Ивмпфолдермониторсервицес**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpfoldermonitorservices)
-   [**Интерфейс IWMPSyncDevice2**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpsyncdevice2)
-   [**Интерфейс Ивмпвидеорендерконфиг**](/previous-versions/windows/desktop/api/wmprealestate/nn-wmprealestate-iwmpvideorenderconfig)
-   [**ивмпусеревентсинк**](/previous-versions/windows/desktop/api/wmpservices/nn-wmpservices-iwmpusereventsink)
-   [**Интерфейс IWMPEvents3**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpevents3)

## <a name="windows-media-player-skins"></a>Обложки проигрывателя Windows Media

В проигрывателе Windows Media 11 появились следующие функции обложки.

-   Новые атрибуты для позиционирования элементов управления. См. раздел [**амбиентаттрибутес. Right**](ambientattributes-right.md) и [**амбиентаттрибутес. Bottom**](ambientattributes-bottom.md).
-   Новые атрибуты для перемещения и изменения размеров элементов управления. См. раздел [**амбиентаттрибутес. мовесизето**](ambientattributes-movesizeto.md) and [**амбиентаттрибутес. слидето**](ambientattributes-slideto.md).
-   Новый атрибут для указания поведения при изменении размера изображения. См. раздел [**амбиентаттрибутес. ресизеимажес**](ambientattributes-resizeimages.md).
-   Новый атрибут для указания неоднородного масштабирования элемента обложки. См. раздел [**амбиентаттрибутес. нинегридмаргинс**](ambientattributes-ninegridmargins.md).

## <a name="windows-media-player-plug-ins"></a>Подключаемые модули проигрывателя Windows Media

В пакете SDK для проигрывателя Windows Media 11 появился новый тип подключаемого модуля для преобразования форматов цифровых мультимедийных файлов. См. раздел [подключаемые модули преобразования проигрывателя Windows Media](windows-media-player-conversion-plug-ins.md).

Подключаемые модули DSP, созданные до выпуска пакета SDK для проигрывателя Windows Media 11, должны быть обновлены для работы с проигрывателем Windows Media 11. См. статью [обновление существующих подключаемых модулей DSP](updating-existing-dsp-plug-ins.md).

Мастер подключаемых модулей проигрывателя Windows Media был обновлен для создания подключаемых модулей DSP, работающих в проигрывателе Windows Media 11. Дополнительные сведения см. в разделе [обновления мастера подключаемых модулей DSP для проигрывателя Windows Media 11](updates-to-the-dsp-plug-in-wizard-for-windows-media-player-11.md).

## <a name="windows-media-player-online-stores"></a>Интернет-магазины проигрывателя Windows Media

В проигрывателе Windows Media 11 появилась новая модель интеграции каталогов Интернет-магазина в компонент библиотеки проигрывателя Windows Media. См. раздел [Type 1 Online Stores](type-1-online-stores.md).

## <a name="windows-media-player"></a>Проигрыватель Windows Media

В проигрывателе Windows Media 11 появились следующие новые возможности.

-   [Расширения устройств для создания отчетов о приобретенном содержимом](device-extensions-for-reporting-acquired-content.md)
-   [Расширения устройств для параметров объектов списков воспроизведения](device-extensions-for-playlist-object-preferences.md)

## <a name="windows-media-player-sdk-samples"></a>Примеры пакета SDK для проигрывателя Windows Media

Пример C# с именем Счемареадер был впервые использован в пакете SDK для проигрывателя Windows Media 11. В примере создается средство, использующее объектную модель проигрывателя Windows Media для получения и просмотра сведений о метаданных в библиотеке проигрывателя Windows Media или в файле цифрового носителя. Средство может сохранить результаты в текстовый файл. Средство перечисляет имена атрибутов метаданных, хранящиеся в библиотеке, для каждой поддерживаемой схемы (аудио, видео, списков воспроизведения, фотографий и т. д.). Средство также может предоставлять сведения о доступных атрибутах для списков воспроизведения в коллекции списков воспроизведения, на компакт-дисках, оглавлении компакт-дисков, на DVD-дисках, в разделах с DVD, оглавлении и отдельных файлах мультимедиа.

Пример C++ с именем ВМПМЛ был обновлен в пакете SDK для проигрывателя Windows Media 11, чтобы продемонстрировать следующие возможности:

-   Использование нового интерфейса [**IWMPStringCollection2**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpstringcollection2) для создания пользовательского интерфейса, аналогичного компоненту библиотеки проигрывателя Windows Media.
-   Использование интерфейсов [**ивмпкуери**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpquery) и [**IWMPMediaCollection2**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpmediacollection2) для создания составных запросов и вывода результатов.

 

 




