---
title: Запись потоков с неквадратными пикселями
description: Запись потоков с неквадратными пикселями
ms.assetid: 4af7dedc-e2b8-4dc2-add4-84424e93c297
keywords:
- Windows Media Format SDK, написание видеопотоков
- Windows Media Format SDK, потоки видео
- Пакет SDK для формата Windows Media, а не квадратные Пиксели
- Windows Media Format SDK, Пиксели (не квадратные)
- Расширенный системный формат (ASF), написание видеопотоков
- ASF (Расширенный системный формат), написание видеопотоков
- Расширенный системный формат (ASF), видеопотоки
- ASF (Расширенный системный формат), видеопотоки
- Расширенный формат систем (ASF), а не квадратные Пиксели
- ASF (Расширенный системный формат), неквадратные Пиксели
- Расширенный формат систем (ASF), пикселей (не квадратный)
- ASF (Расширенный системный формат), Пиксели (не квадратный)
- Написание видеопотоков
- видеопотоки, запись
- видеопотоки, не квадратные Пиксели
- неквадратные Пиксели
- Пиксели (не квадратные)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f1349840f151ab787ba0e0512cfab8fea08aacf1
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/19/2020
ms.locfileid: "104069561"
---
# <a name="writing-streams-with-non-square-pixels"></a>Запись потоков с неквадратными пикселями

Существует два способа создания потоков видео с неквадратными пикселями, которые будут правильно отображаться в проигрывателе Windows Media. Первый способ заключается в установке атрибутов уровня потока в заголовке файла. Второй способ включает добавление расширения единицы данных в поток в профиле, а затем задание значения для него в каждом написанном образце.

## <a name="to-use-stream-level-header-attributes-to-set-pixel-aspect-ratio"></a>Использование атрибутов заголовка уровня потока для установки пропорций в пикселях

1.  Настройте объект модуля записи. Дополнительные сведения см. в разделе [запись файлов ASF](writing-asf-files.md).
2.  Создайте или загрузите профиль с одним или несколькими потоками видео. Дополнительные сведения см. [в разделе Использование профилей с модулем записи](to-use-profiles-with-the-writer.md).
3.  Вызовите [**ивмвритер:: сетпрофиле**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-setprofile). (Всегда вызывайте этот метод перед установкой атрибутов заголовка.)
4.  Вызовите **QueryInterface** , чтобы получить интерфейс [**IWMHeaderInfo3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo3) и дважды вызвать [**аддаттрибуте**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo3-addattribute) , чтобы добавить [**аспектратиокс**](aspectratiox.md) и [**аспектратиой**](aspectratioy.md) в качестве атрибутов уровня потока видеопотока. Эти атрибуты являются значениями **типа DWORD** .
5.  Запишите файл.

## <a name="to-use-data-unit-extensions-to-set-pixel-aspect-ratio"></a>Использование модулей обработки данных для установки пропорций в пикселях

**Перед записью:**

1.  Настройте объект модуля записи. Дополнительные сведения см. в разделе [запись файлов ASF](writing-asf-files.md).
2.  Создайте или загрузите профиль с одним или несколькими потоками видео. Дополнительные сведения см. [в разделе Использование профилей с модулем записи](to-use-profiles-with-the-writer.md).
3.  Для каждого потока (любого типа мультимедиа) в профиле вызовите [**ивмстреамконфиг:: сетстреамнаме**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstreamconfig-setstreamname) , чтобы указать уникальное имя по своему усмотрению. Не присваивайте двум потокам одно и то же имя.
4.  Используйте [**IWMStreamConfig2:: адддатаунитекстенсион**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstreamconfig2-adddataunitextension) в потоке видео, чтобы добавить расширение единицы данных для пропорций в пикселях.
5.  Вызовите [**ивмвритер:: сетпрофиле**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-setprofile).
6.  Запишите файл.

**При записи:**

-   Для каждого образца вызовите [**INSSBuffer3:: SetProperty**](/previous-versions/windows/desktop/api/Wmsbuffer/nf-wmsbuffer-inssbuffer3-setproperty) и укажите свойство WM \_ сампликстенсионгуид \_ пикселаспектратио вместе с правильным значением. Значения пропорций записываются как два сцепленных двузначного значения. Например, 16:9 записывается как 1609 или 0x0649. Это всегда является 2-байтовым значением.

## <a name="related-topics"></a>См. также

<dl> <dt>

[**Чтение и запись видеопотоков с неквадратными пикселями**](to-read-and-write-video-streams-with-non-square-pixels.md)
</dt> </dl>

 

 




