---
description: Использование Windows Media в DirectShow
ms.assetid: 2fae0504-d1da-413a-80dd-de7818f506ef
title: Использование Windows Media в DirectShow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e73726f0d7251f1c19beee05cfd8f335d3fdd7a
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/03/2021
ms.locfileid: "104424126"
---
# <a name="using-windows-media-in-directshow"></a>Использование Windows Media в DirectShow

В этом разделе описывается использование DirectShow для воспроизведения и записи файлов расширенного формата системы (ASF). Файлы ASF обычно содержат аудио и видео содержимое, закодированное с помощью кодеков аудио и видео Windows Media. Однако ASF может содержать данные любого типа.

Следующие фильтры DirectShow поддерживают чтение и запись файлов ASF.

-   [Фильтр чтения WM ASF](wm-asf-reader-filter.md). Считывает файлы ASF.
-   [Фильтр модуля записи WM ASF](wm-asf-writer-filter.md). Файлы вртиес ASF.
-   [Фильтр оболочки DMO](dmo-wrapper-filter.md). Создает оболочку для кодировщика Windows Media и декодера дмос.

### <a name="versions"></a>Версии

Фильтры модуля записи WM ASF и WM ASF упаковываются в библиотеку DLL с именем qasf.dll, а фильтры совместно называются "компонентами КАСФ". Эти фильтры являются оболочками для пакета SDK Windows Media Format. Библиотека DLL (qasf.dll) была впервые опубликована в пакете SDK DirectX, но позднее была обновлена в пакете SDK формата Windows Media. Ниже приведен журнал версий фильтров КАСФ.

-   DirectShow 8,1 поддерживает пакет SDK для формата Windows Media версии 7,0.
-   DirectShow 9,0 поддерживает пакет SDK для формата Windows Media версии 7,1.
-   Пакет обновления 2 (SP2) для Windows XP поддерживает пакет SDK Windows Media Format 9.
-   Windows Vista поддерживает пакет SDK для Windows Media Format 11.
-   Пакет SDK Windows Media Format 9 и более поздние версии содержат соответствующие версии КАСФ.

Для получения последней версии КАСФ всегда Скачайте последнюю версию пакета SDK для Windows Media Format.

### <a name="legacy-windows-media-source-filter"></a>Устаревший фильтр источника Windows Media

В Windows XP с пакетом обновления 1 (SP1) и более ранних версий фильтр источника по умолчанию для файлов ASF (. ASF,. WMV и. WMA) является устаревшим [фильтром источников Windows Media](windows-media-source-filter.md). Это поведение поддерживалось для обеспечения обратной совместимости с приложениями, использующими проигрыватель Windows Media 6,4. Новые приложения должны использовать более новые версии КАСФ, благодаря которым модуль чтения WM ASF фильтрует фильтр по умолчанию для воспроизведения файлов ASF.

Дополнительные сведения о пакетах средств разработки для Windows Media Suite см. в разделе [аудио и видео](../audio-and-video.md) Библиотеки MDSN.

Эта статья содержит следующие разделы:

-   [Чтение файлов ASF в DirectShow](reading-asf-files-in-directshow.md)
-   [Создание файлов ASF в DirectShow](creating-asf-files-in-directshow.md)

## <a name="related-topics"></a>См. также

<dl> <dt>

[Использование DirectShow](using-directshow.md)
</dt> </dl>

 

 
