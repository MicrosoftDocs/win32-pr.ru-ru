---
description: Пакет SDK для DirectShow и пакет SDK Windows Media Format
ms.assetid: d9ac89cc-0d55-4c51-ae0a-592422d97383
title: Пакет SDK для DirectShow и пакет SDK Windows Media Format
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f85c5553c9a1cdd3f62380c9fc90d836a47a650
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/03/2021
ms.locfileid: "104351662"
---
# <a name="the-directshow-sdk-and-the-windows-media-format-sdk"></a>Пакет SDK для DirectShow и пакет SDK Windows Media Format

DirectShow и пакет SDK для Windows Media Format предлагают дополнительные решения для создания приложений, которые создают и воспроизводят потоки формата Windows Media. Дополнительные сведения см. в разделе "[аудио и видео](../audio-and-video.md)" библиотеки MSDN.

Фильтр модуля записи ASF принимает любое количество входных потоков и создает файл ASF. Фильтр использует Windows Media Format SDK для преобразования несжатых аудио-или видеофайлов в содержимое Windows Media. После этого сжатое содержимое сохраняется в формате контейнера ASF. Если содержимое имеет только аудио, файл получает расширение WMA и называется аудиофайлом Windows Media Audio. Если содержимое относится только к видео или видео и аудио, файл получает расширение WMV и называется файлом видео Windows Media. Оба типа файлов могут также включать метаданные.

Модуль записи WM ASF можно использовать в различных сценариях, включая видеозапись цифрового видео (DV), повторное сжатие звука и преобразование Audio-Video файлов мультимедиа с чередованием (AVI) или MPEG для потоковой передачи в сети. Этот фильтр предоставляет единственный способ создания файлов Microsoft® Windows Media™ Audio (WMA) и Windows Media Video (WMV) в® DirectShow. Фильтр также может создавать файлы, защищенные цифровыми Rights Management (DRM), и также может создавать содержимое MPEG-4 с помощью кодировщика Microsoft MPEG-4. Это содержимое хранится в формате контейнера ASF.

## <a name="related-topics"></a>См. также

<dl> <dt>

[Создание файлов ASF в DirectShow](creating-asf-files-in-directshow.md)
</dt> </dl>

 

 
