---
description: Microsoft Media Foundation был введен в Windows Vista в качестве замены DirectShow. конечно, DirectShow по-прежнему поддерживается в Windows 7, но разработчикам рекомендуется использовать Media Foundation в своих новых цифровых мультимедийных приложениях.
ms.assetid: c345c0d9-5325-4f73-b9ec-1673ad10e3e4
title: Новые возможности для Media Foundation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2fd2cd2b70ce23968ba9a302e4ab4e825914931ebffff651b534ee0974d75cee
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120012064"
---
# <a name="whats-new-for-media-foundation"></a>Новые возможности для Media Foundation

Microsoft Media Foundation был введен в Windows Vista в качестве замены DirectShow. конечно, DirectShow по-прежнему поддерживается в Windows 7, но разработчикам рекомендуется использовать Media Foundation в своих новых цифровых мультимедийных приложениях.

Улучшения Media Foundation можно суммировать следующим образом.

-   Улучшенная поддержка формата, включая MPEG-4
-   Поддержка устройств захвата и аппаратных кодеков
-   Упрощенная модель программирования
-   Улучшения платформы

## <a name="better-format-support"></a>Улучшенная поддержка формата

Media Foundationный конвейер аудио/видео был реализован в Windows Vista, но поддерживал ограниченный набор форматов и контейнеров файлов, что означало, что некоторые приложения должны возвращаться к старым технологиям, таким как DirectShow. в Windows 7 Media Foundation содержит следующие новые кодеки, источники мультимедиа и приемники мультимедиа:

-   Декодер AAC
-   Кодировщик AAC
-   Источник AVI/WAVE File
-   Видеодекодер DV
-   Декодер видео H. 264
-   Кодировщик видео H. 264
-   Декодер МЖПЕГ
-   Приемник файлов в формате MP3\*
-   Источник файла MP4/3GP
-   Приемник файла MP4/3GP

> [!Note]  
> Приемник файлов в формате MP3 не включает кодировщик аудио MP3.

 

Дополнительные сведения см. [в разделе Поддерживаемые форматы мультимедиа в Media Foundation](supported-media-formats-in-media-foundation.md).

## <a name="hardware-device-support"></a>Поддержка аппаратных устройств

Media Foundation теперь поддерживает следующие типы аппаратных устройств в конвейере аудио/видео:

-   Устройства видеозаписи УВК 1,1, например, камеры
-   Устройства записи звука
-   Аппаратные кодировщики и декодеры
-   Аппаратные видеопроцессоры, например Преобразователи цветового пространства

Аппаратные кодеки могут выполнять очень быстрое перекодирование видео. например, приложение может передавать Windows файлы мультимедиа видео (WMV) на сотовый телефон, который поддерживает только файлы 3GP. С помощью аппаратного кодировщика приложение может перекодировать файл в баккгаунд, непосредственно перед его передачей на устройство.

Аппаратные устройства представлены в Media Foundation прокси-объектом и используются в конвейере так же, как программные компоненты.

## <a name="simplified-programming-model"></a>Упрощенная модель программирования

в Windows Vista Media Foundation представляет собой набор интерфейсов api относительно низкого уровня. Эти API являются гибкими, но слишком сложны для простых задач. Windows 7 добавляет новые высокоуровневые api, упрощающие написание мультимедийных приложений на C++. Ниже приведены новые высокоуровневые API-интерфейсы.



| API                                | Описание                                                                                                                                                                                                                                                                                                    |
|------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Модуль чтения исходного кода](source-reader.md) | Модуль чтения исходного кода извлекает необработанные или декодированные данные из файла мультимедиа. Например, средство чтения исходного кода можно использовать для получения растровых изображений из видеофайла или для анализа данных волны в звуковом файле. Кроме того, средство чтения исходного кода можно использовать для получения динамических данных с аудио или видеозаписи. <br/> |
| [Модуль записи приемников](sink-writer.md)     | Модуль записи приемника позволяет создавать файлы мультимедиа путем передачи несжатых или закодированных данных. Например, его можно использовать для повторной кодировки видеофайла или записи видео с веб-камеры в файл.                                                                                                         |
| [API перекодирования](transcode-api.md) | Эта функция поддерживает самые распространенные сценарии кодирования аудио и видео.<br/>                                                                                                                                                                                                                               |



 

Вы по-прежнему можете использовать низкоуровневые API в Media Foundation. Это можно сделать, если вам нужен больший контроль над конвейером аудио/видео.

## <a name="platform-improvements"></a>Усовершенствования платформы

Windows 7 включает многочисленные улучшения для базовых api-интерфейсов Media Foundationной платформы. Расширенные приложения могут использовать эти API напрямую; другие приложения будут косвенно получать преимущества. В них сочетаются все лучшие возможности веб-заданий, а также добавлены некоторые улучшения, среди которых:

-   Изменения в конвейере видео для уменьшения энергопотребления и использования видеопамяти.
-   [Дксва-HD](dxva-hd.md): High Definition (ДКСВА-HD) с ускорением видео Microsoft DirectX — это новый API для обработки видео с аппаратным ускорением. ДКСВА-HD предлагает более гибкую модель компоновки, чем предыдущий API ДКСВА Video Processing и лучше подходит для видеоформатов высокой четкости.
-   Новый механизм перечисления источников и декодеров, включающий в себя значения и список предпочтительных или заблокированных. Эта функция повышает общую надежность системы. Дополнительные сведения см. в следующих разделах:
    -   [**мфтенумекс**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex)
    -   [**имфплугинконтрол**](/windows/desktop/api/mfobjects/nn-mfobjects-imfplugincontrol)
    -   [Успешный кодек](codec-merit.md)

## <a name="sdk-changes"></a>Изменения пакета SDK

-   Новые заголовки и файлы библиотек: [Media Foundation заголовков и библиотек](media-foundation-headers-and-libraries.md)
-   изменения библиотек DLL и. lib: [изменения библиотеки в Windows 7](media-foundation-headers-and-libraries.md)
-   Новые примеры SDK:
    -   [Пример аудиоклипа](audio-clip-sample.md)
    -   [Пример ДКСВА-HD](dxva-hd-sample.md)
    -   [Пример MFCaptureD3D](mfcaptured3d-sample.md)
    -   [Пример Мфкаптуретофиле](mfcapturetofile-sample.md)
    -   [Пример перекодирования](transcode-sample.md)
    -   [Пример Видеосумбнаил](videothumbnail-sample.md)
-   Усовершенствования в [топоедит](topoedit.md):
    -   Поддержка перекодирования. См. раздел Создание [топологии перекодирования с помощью топоедит](building-a-transcode-topology-with-topoedit.md).
    -   Поддержка захвата аудио и видео. См. [меню Topology](topology-menu.md).

## <a name="new-in-windows-8"></a>Новые Windows 8

некоторые из новых обновлений для Media Foundation с Windows 8:

-   [**Имфкаптурингине**](/windows/desktop/api/mfcaptureengine/nn-mfcaptureengine-imfcaptureengine) управляет одним или несколькими устройствами записи. Список атрибутов см. в разделе [атрибуты подсистемы захвата](capture-engine-attributes.md) . Другие новые интерфейсы, связанные с записью мультимедиа, — это [**имфкаптурефотосинк**](/windows/desktop/api/mfcaptureengine/nn-mfcaptureengine-imfcapturephotosink), [**имфкаптурепревиевсинк**](/windows/desktop/api/mfcaptureengine/nn-mfcaptureengine-imfcapturepreviewsink), [**имфкаптуререкордсинк**](/windows/desktop/api/mfcaptureengine/nn-mfcaptureengine-imfcapturerecordsink), [**имфкаптуресинк**](/windows/desktop/api/mfcaptureengine/nn-mfcaptureengine-imfcapturesink)и [**имфкаптуресаурце**](/windows/desktop/api/mfcaptureengine/nn-mfcaptureengine-imfcapturesource).
-   Следующие расширения классов Media Foundation являются новыми для Windows 8:
    -   [**имфмедиаенгиникс**](/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediaengineex)
    -   [**имфмедиасаурцеекс**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasourceex)
    -   [**имфреалтимеклиентекс**](/windows/desktop/api/mfidl/nn-mfidl-imfrealtimeclientex)
    -   [**имфсинквритерекс**](/windows/desktop/api/mfreadwrite/nn-mfreadwrite-imfsinkwriterex)
    -   [**имфсаурцереадерекс**](/windows/desktop/api/mfreadwrite/nn-mfreadwrite-imfsourcereaderex)
    -   [**имфвидеосамплеаллокаторекс**](/windows/desktop/api/mfidl/nn-mfidl-imfvideosampleallocatorex)
    -   [**имфворккуеуесервицесекс**](/windows/desktop/api/mfidl/nn-mfidl-imfworkqueueservicesex)
-   [API видео Direct3D 11](direct3d-11-video-apis.md) является новым для Windows 8. Windows 8 классические приложения по-прежнему могут использовать [видео api direct3d 9](direct3d-video-apis.md), но Windows приложения магазина должны использовать новый api-интерфейс direct3d 11. Дополнительные сведения о видео Microsoft Direct3D 11 см. [в статье поддержка декодирования видео Direct3D 11 в Media Foundation](supporting-direct3d-11-video-decoding-in-media-foundation.md).
-   Существуют обновления и улучшения Media Foundation рабочих очередях. Дополнительные сведения см. [в разделе улучшения рабочей очереди и потоков](media-foundation-work-queue-and-threading-improvements.md) .
-   [H. 264 увк 1,5. кодировщики камеры](camera-encoder-h264-uvc-1-5.md).
-   список Media Foundation API, который можно использовать с приложениями для магазина Windows, см. в разделе [Win32 и COM для Windows приложений магазина (мультимедиа)](media-foundation-headers-and-libraries.md).
-   Media Foundation не входит в выпуски N и KN Windows 8. дополнительные сведения см. в [статье пакет дополнительных компонентов для Microsoft Windows Media для версий N и KN всех выпусков Windows 8](https://support.microsoft.com/kb/2703761).

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[О Media Foundation](about-the-media-foundation-sdk.md)
</dt> <dt>

[Microsoft Media Foundation](microsoft-media-foundation-sdk.md)
</dt> </dl>

 

 




