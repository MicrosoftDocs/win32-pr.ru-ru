---
title: Атрибуты с несколькими значениями (пакет SDK для формата Windows Media 11)
description: Атрибуты с несколькими значениями
ms.assetid: 2e65c5d0-6f5e-45a4-8e13-9e49da007145
keywords:
- Windows Media Format SDK, атрибуты
- Расширенный системный формат (ASF), атрибуты
- ASF (Расширенный системный формат), атрибуты
- атрибуты, несколько значений
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 928aee154f9f824168ce08470702b49c23ba2c0a
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/10/2020
ms.locfileid: "104070968"
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



 

## <a name="related-topics"></a>См. также

<dl> <dt>

[**Атрибуты**](attributes.md)
</dt> </dl>

 

 




