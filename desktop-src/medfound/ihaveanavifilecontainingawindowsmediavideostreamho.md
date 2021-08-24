---
description: у меня есть файл AVI, содержащий поток видео Windows Media.
ms.assetid: 0b4c5bf2-caa6-4e14-be5f-9e25ec918cf0
title: у меня есть файл AVI, содержащий поток видео Windows Media. Как преобразовать его в WMV-файл?
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 74dfc2a5980533487c7a1c8716806fcedda1c7147bdacaf3ea0c887acbff0f83
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119777144"
---
# <a name="i-have-an-avi-file-containing-a-windows-media-video-stream-how-can-i-convert-it-to-a-wmv-file"></a>у меня есть файл AVI, содержащий поток видео Windows Media. Как преобразовать его в WMV-файл?

интерфейсы кодеков Windows Media Audio и Video не предоставляют методы для создания файлов с использованием формата ASF, который используется для файлов WMV. если требуется преобразовать файл (с помощью любого контейнера) в файл ASF, необходимо использовать объекты пакета SDK Windows Media Format.

получите сжатые Windows примеры мультимедиа из исходного файла и передайте их в объект модуля записи как образцы потока. дополнительные сведения см. в документации по пакету SDK для серии Windows Media Format 9.

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Часто задаваемые вопросы](frequentlyaskedquestions.md)
</dt> </dl>

 

 



