---
description: пакет sdk для DirectShow и Windows Media Format sdk
ms.assetid: d9ac89cc-0d55-4c51-ae0a-592422d97383
title: пакет sdk для DirectShow и Windows Media Format sdk
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 993f7ea0c9ac47861547cc08662fcb7916c3587c566445960505fe05a5c3d37a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118651761"
---
# <a name="the-directshow-sdk-and-the-windows-media-format-sdk"></a>пакет sdk для DirectShow и Windows Media Format sdk

DirectShow и пакет SDK для Windows media Format предлагают дополнительные решения для написания приложений, которые создают и воспроизводят потоки формата Windows Media. дополнительные сведения см. в разделе "[аудио и видео](../audio-and-video.md)" библиотека MSDN.

Фильтр модуля записи ASF принимает любое количество входных потоков и создает файл ASF. этот фильтр использует пакет SDK Windows Media Format для преобразования несжатых аудио-или видеофайлов в Windows содержимое на основе носителя. После этого сжатое содержимое сохраняется в формате контейнера ASF. если содержимое имеет только аудио, файл получает расширение wma и называется Windowsным аудио-файлом. если содержимое относится только к видео или видео и аудио, файл получает расширение wmv и называется Windowsным видеофайлом мультимедиа. Оба типа файлов могут также включать метаданные.

Модуль записи WM ASF можно использовать в различных сценариях, включая видеозапись цифрового видео (DV), повторное сжатие звука и преобразование Audio-Video файлов мультимедиа с чередованием (AVI) или MPEG для потоковой передачи в сети. этот фильтр предоставляет единственный способ создания файлов Microsoft® Windows media™ Audio (WMA) и Windows media Video (WMV) в DirectShow®. Фильтр также может создавать файлы, защищенные цифровыми Rights Management (DRM), и также может создавать содержимое MPEG-4 с помощью кодировщика Microsoft MPEG-4. Это содержимое хранится в формате контейнера ASF.

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Создание файлов ASF в DirectShow](creating-asf-files-in-directshow.md)
</dt> </dl>

 

 
