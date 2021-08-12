---
description: использование Windows Media в DirectShow
ms.assetid: 2fae0504-d1da-413a-80dd-de7818f506ef
title: использование Windows Media в DirectShow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4fea308943d4be732c75e774d3e0c3cb09ac7c6609a8399d2e6eca4666d99e6b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118651090"
---
# <a name="using-windows-media-in-directshow"></a>использование Windows Media в DirectShow

в этом разделе описывается использование DirectShow для воспроизведения и записи файлов расширенного формата системы (ASF). файлы ASF обычно содержат аудио и видео содержимое, закодированное с помощью кодеков Windows Media audio и video. Однако ASF может содержать данные любого типа.

следующие фильтры DirectShow поддерживают чтение и запись файлов ASF.

-   [Фильтр чтения WM ASF](wm-asf-reader-filter.md). Считывает файлы ASF.
-   [Фильтр модуля записи WM ASF](wm-asf-writer-filter.md). Файлы вртиес ASF.
-   [фильтр оболочки DMO](dmo-wrapper-filter.md). создает оболочку для Windowsного кодировщика мультимедиа и декодера дмос.

### <a name="versions"></a>Версии

Фильтры модуля записи WM ASF и WM ASF упаковываются в библиотеку DLL с именем qasf.dll, а фильтры совместно называются "компонентами КАСФ". эти фильтры являются оболочками для пакета SDK для Windows Media Format. библиотека DLL (qasf.dll) была впервые опубликована в пакете sdk для DirectX, но позднее была обновлена в пакете sdk для Windows Media Format. Ниже приведен журнал версий фильтров КАСФ.

-   DirectShow 8,1 поддерживает пакет SDK Windows формата мультимедиа версии 7,0.
-   DirectShow 9,0 поддерживает пакет SDK Windows формата мультимедиа версии 7,1.
-   Windows XP с пакетом обновления 2 (sp2) поддерживает Windows пакет SDK для Media Format 9.
-   Windows Vista поддерживает пакет SDK для Windows Media Format 11.
-   Windows Пакет SDK для Media Format 9 и более поздних версий содержит соответствующие версии КАСФ.

для получения последней версии касф всегда скачайте последнюю версию пакета SDK для Windows Media Format.

### <a name="legacy-windows-media-source-filter"></a>фильтр источника Windows носителя прежних версий

в Windows XP с пакетом обновления 1 (sp1) и более ранних версиях фильтр источника по умолчанию для файлов asf (asf, wmv и wma) является устаревшим [фильтром источника мультимедиа Windows](windows-media-source-filter.md). это поведение поддерживалось для обеспечения обратной совместимости с приложениями, которые использовали проигрыватель Windows Media 6,4. Новые приложения должны использовать более новые версии КАСФ, благодаря которым модуль чтения WM ASF фильтрует фильтр по умолчанию для воспроизведения файлов ASF.

дополнительные сведения о Windows наборе носителей пакета средств разработки программного обеспечения см. в разделе [аудио и видео](../audio-and-video.md) библиотеки MDSN.

Эта статья содержит следующие разделы:

-   [Чтение файлов ASF в DirectShow](reading-asf-files-in-directshow.md)
-   [Создание файлов ASF в DirectShow](creating-asf-files-in-directshow.md)

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Использование DirectShow](using-directshow.md)
</dt> </dl>

 

 
