---
description: Источник файла AVI/WAV
ms.assetid: b8abf5d8-ba7f-441d-beef-9f85859318d5
title: Источник файла AVI/WAV
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: de8c99de9eed21afa716c4f3ee81a5d1cc4e9731739526f7c9531c758b30a22a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119689364"
---
# <a name="aviwav-file-source"></a>Источник файла AVI/WAV

(Не рекомендуется к использованию. Для файлов AVI и WAV используйте [файл источник (асинхронный)](file-source--async--filter.md) и [средство синтаксического анализа](wave-parser-filter.md) [AVI](avi-splitter-filter.md) или Wave.)

Фильтр источника файла AVI/WAV считывает исходные файлы AVI и WAV и создает соответствующие выходные сигналы для типа файла.

Для файлов WAV фильтр создает ПИН-код вывода звука, который создает звуковой поток, который можно подключить к фильтру подготовки аудио или к фильтру преобразования звука.

Для файлов AVI фильтр создает ПИН-код для вывода видео, который создает сжатый поток AVI, подходящий для фильтра AVI-кодека, и звуковой выход, который создает звуковой поток, подходящий для фильтра рендеринга звука или промежуточного фильтра преобразования звука.

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[DirectShow Фильтрующ](directshow-filters.md)
</dt> </dl>

 

 



