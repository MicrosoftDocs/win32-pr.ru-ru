---
title: Атрибуты с несколькими значениями (пакет SDK для формата Windows Media 11)
description: Сведения об атрибутах с несколькими значениями в пакете SDK для формата Windows Media 11. Некоторые атрибуты элемента мультимедиа могут иметь несколько значений.
ms.assetid: 2e65c5d0-6f5e-45a4-8e13-9e49da007145
keywords:
- Windows Media Format SDK, атрибуты
- Расширенный системный формат (ASF), атрибуты
- ASF (Расширенный системный формат), атрибуты
- атрибуты, несколько значений
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e9466cd3f993cc1b12f27bc162e5188e6d45404b
ms.sourcegitcommit: d0eb44d0a95f5e5efbfec3d3e9c143f5cba25bc3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/17/2021
ms.locfileid: "112262696"
---
# <a name="attributes-with-multiple-values-windows-media-format-11-sdk"></a>Атрибуты с несколькими значениями (пакет SDK для формата Windows Media 11)

Некоторым из предопределенных атрибутов может быть назначено несколько значений. Например, « **исполнитель** » — это атрибут, который может иметь несколько значений. Можно вызвать [**IWMHeaderInfo3:: аддаттрибуте**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo3-addattribute) несколько раз, чтобы добавить столько значений **исполнителей** , сколько требуется. При выполнении нескольких вызовов **аддаттрибуте** для атрибутов, которые не поддерживают несколько значений, метод может вернуть код ошибки или просто проигнорировать запрос.

В следующей таблице перечислены атрибуты, которые поддерживают несколько значений. Некоторые атрибуты могут иметь несколько значений только в ASF-файлах, а другие могут иметь несколько значений в файлах ASF и MP3.



| attribute                                                 | Поддержка нескольких значений |
|-----------------------------------------------------------|-----------------------------|
| [**Автор**](author.md)                                  | ASF, MP3                    |
| [**WM/Албумартист**](wm-albumartist.md)                  | ASF                         |
| [**WM/Албумковерурл**](wm-albumcoverurl.md)              | ASF                         |
| [**WM/Category**](wm-category.md)                        | ASF                         |
| [**WM/Composer**](wm-composer.md)                        | ASF, MP3                    |
| [**WM/проводник**](wm-conductor.md)                      | ASF                         |
| [**WM/Director**](wm-director.md)                        | ASF                         |
| [**WM/жанр**](wm-genre.md)                              | ASF                         |
| [**WM/GenreID**](wm-genreid.md)                          | ASF                         |
| [**WM/Language**](wm-language.md)                        | ASF, MP3                    |
| [**WM/ \_ синхронизированы песен**](wm-lyrics-synchronised.md) | ASF, MP3                    |
| [**WM/настроение**](wm-mood.md)                                | ASF, MP3                    |
| [**WM/Picture**](wmpicture.md)                           | ASF, MP3                    |
| [**WM/Producer**](wm-producer.md)                        | ASF                         |
| [**WM/Промотионурл**](wm-promotionurl.md)                | ASF                         |
| [**WM/Усервебурл**](wm-userweburl.md)                    | ASF, MP3                    |
| [**WM/Writer**](wm-writer.md)                            | ASF, MP3                    |



 

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[**Атрибуты**](attributes.md)
</dt> </dl>

 

 




