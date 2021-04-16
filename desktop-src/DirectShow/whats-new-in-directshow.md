---
description: Новые возможности DirectShow
ms.assetid: 675a34d4-7a33-4125-86af-cd4ed73ad430
title: Новые возможности DirectShow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 74747349848a7b370cd4766113085c84d0c7a1d5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105664693"
---
# <a name="whats-new-in-directshow"></a>Новые возможности DirectShow

## <a name="whats-new-for-directshow-in-windows-7"></a>Новые возможности DirectShow в Windows 7

Новые интерфейсы:

-   [**иамасинкреадертиместампскалинг**](/windows/desktop/api/Strmif/nn-strmif-iamasyncreadertimestampscaling)
-   [**иамплугинконтрол**](/windows/desktop/api/Strmif/nn-strmif-iamplugincontrol)

Новые или обновленные фильтры:

-   [**Декодер звука Microsoft MPEG-1/DD/AAC**](microsoft-mpeg-1-dd-audio-decoder.md)
-   [**Видеодекодер Microsoft MPEG-2 видео**](microsoft-mpeg-2-video-decoder.md)

Алгоритм "Intelligent Connect" был изменен для поддержки предпочтительных и заблокированных фильтров. Дополнительные сведения см. в разделе [Intelligent Connect](intelligent-connect.md).

Воспроизведение DVD: новые параметры метода [**IDvdControl2:: SetOption**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-setoption) .

## <a name="whats-new-for-directshow-in-windows-vista"></a>Новые возможности DirectShow в Windows Vista

-   DirectShow теперь является частью Windows SDK. Заголовки, библиотеки, образцы и средства DirectShow больше не включены в пакет SDK для DirectX.
-   Ускорение видео DirectX (ДКСВА) 2,0 содержит множество улучшений от ДКСВА 1,0.

    -   Аппаратный конвейер видеопотока был значительно улучшен.
    -   Такие компоненты, как декодеры, имеют доступ к ДКСВА 2,0 напрямую без взаимодействия через модуль подготовки видео.
    -   Диспетчер устройств Direct3D позволяет компонентам совместно использовать одно и то же устройство Direct3D.

    Дополнительные сведения о ДКСВА 2,0 см. в документации по [DirectX Video Acceleration 2,0](../medfound/directx-video-acceleration-2-0.md) , которая является частью документации по [Microsoft Media Foundation](../medfound/microsoft-media-foundation-sdk.md) .

-   [**Расширенный модуль подготовки**](enhanced-video-renderer-filter.md) отчетов (Евр) — это мощный обработчик видео, который использует ту же модель подключаемых модулей, что и Media Foundationная версия Евр. Дополнительные сведения о Евр см. в документации по [Microsoft Media Foundation](../medfound/microsoft-media-foundation-sdk.md) .
-   Поддержка захвата модели драйвера экрана (WDDM) Windows Vista. Эта функция позволяет фильтрам использовать все преимущества видеоадаптеров со встроенным видеозаписью для уменьшения количества ненужных копий между видеопамятью и системной памятью. Дополнительные сведения см. [в разделе Использование захвата WDDM в DirectShow](using-wddm-capture-in-directshow.md).
-   Звуковой декодер MPEG-1 уровня II теперь использует арифметические операции с плавающей запятой для улучшения качества декодирования.
-   Усовершенствования воспроизведения DVD-дисков. Дополнительные сведения см. [в разделе улучшения воспроизведения DVD в Windows Vista](dvd-playback-enhancements-in-windows-vista.md).
    -   Улучшенная поддержка режима: плавные переходы между тарифами; переходы между прямым и обратным воспроизведением; Поддержка воспроизведения звука во время перемотки вперед и назад.
    -   Расширенное кэширование. Приложения могут задавать объем данных, которые предварительно считываются DVD-навигатором. Установка большего кэша может увеличить время работы батареи и включить автоматическое воспроизведение (после отключения диска). Дополнительные сведения см. в разделе [**DVD- \_ \_ флаг параметра**](/windows/win32/api/strmif/ne-strmif-dvd_option_flag).
-   Устройства конечных точек аудио. приложения могут связывать [Фильтр модуля подготовки отчетов DirectSound](directsound-renderer-filter.md) с конкретным устройством конечной точки. Приложения могут использовать API мультимедийного устройства (Ммдевице) для перечисления и выбора устройства конечной точки. Дополнительные сведения см. в документации по основным аудио API в Windows SDK.
-   Следующие фильтры были удалены из Windows Vista:
    -   [Фильтр IP-приемника BDA](/previous-versions/windows/desktop/mstv/bda-ip-sink-filter)
    -   [Фильтр раскадровки BDA](/previous-versions/windows/desktop/mstv/bda-slip-deframer-filter)
    -   [Фильтр декодера CC](cc-decoder-filter.md)
    -   [Фильтр кодека НАБТС/фек ВБИ](/previous-versions/windows/desktop/mstv/nabts-fec-vbi-codec-filter)
    -   [Фильтр раскомпрессоров QT](qt-decompressor-filter.md)
    -   [Фильтр синтаксического анализатора QuickTime Movie](quicktime-movie-parser-filter.md)
    -   [Фильтр кодека WST](wst-codec-filter.md)
    -   [Фильтр WST декодера](wst-decoder-filter.md)
-   Код прокси-сервера или заглушки для многих интерфейсов DirectShow был перемещен из quartz.dll в proppage.dll. Этот код был удален из quartz.dll, так как он не предназначен для использования приложениями. Однако он полезен для отладки, так как позволяет тестировать приложение удаленно подключаться к графу фильтра DirectShow в другом процессе. Чтобы использовать эту функцию в Windows Vista, необходимо сначала зарегистрировать proppage.dll. Эта библиотека DLL доступна в каталоге Windows SDK Tools. (Дополнительные сведения см. в разделе [Загрузка графа из внешнего процесса](loading-a-graph-from-an-external-process.md).)

 

 
