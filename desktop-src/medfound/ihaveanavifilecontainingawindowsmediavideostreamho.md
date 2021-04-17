---
description: У меня есть файл AVI, содержащий поток видео Windows Media.
ms.assetid: 0b4c5bf2-caa6-4e14-be5f-9e25ec918cf0
title: У меня есть файл AVI, содержащий поток видео Windows Media. Как преобразовать его в WMV-файл?
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 08c770a8355e92c6cfe052d86a17c6638a7a9948
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/03/2021
ms.locfileid: "105703429"
---
# <a name="i-have-an-avi-file-containing-a-windows-media-video-stream-how-can-i-convert-it-to-a-wmv-file"></a>У меня есть файл AVI, содержащий поток видео Windows Media. Как преобразовать его в WMV-файл?

Интерфейсы кодеков аудио и видео Windows Media не предоставляют методы для создания файлов с использованием формата ASF, который используется для файлов WMV. Если требуется преобразовать файл (с помощью любого контейнера) в файл ASF, необходимо использовать объекты пакета SDK Windows Media Format.

Получите сжатые образцы Windows Media из исходного файла и передайте их в объект модуля записи в виде потоковых примеров. Дополнительные сведения см. в документации по пакету SDK серии Windows Media Format 9.

## <a name="related-topics"></a>См. также

<dl> <dt>

[Часто задаваемые вопросы](frequentlyaskedquestions.md)
</dt> </dl>

 

 



