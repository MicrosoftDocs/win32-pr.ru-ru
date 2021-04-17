---
description: Источник файла AVI/WAV
ms.assetid: b8abf5d8-ba7f-441d-beef-9f85859318d5
title: Источник файла AVI/WAV
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ef659d880ef570176f94ac91875291ea9d200cf5
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "105682315"
---
# <a name="aviwav-file-source"></a>Источник файла AVI/WAV

(Не рекомендуется к использованию. Для файлов AVI и WAV используйте [файл источник (асинхронный)](file-source--async--filter.md) и [средство синтаксического анализа](wave-parser-filter.md) [AVI](avi-splitter-filter.md) или Wave.)

Фильтр источника файла AVI/WAV считывает исходные файлы AVI и WAV и создает соответствующие выходные сигналы для типа файла.

Для файлов WAV фильтр создает ПИН-код вывода звука, который создает звуковой поток, который можно подключить к фильтру подготовки аудио или к фильтру преобразования звука.

Для файлов AVI фильтр создает ПИН-код для вывода видео, который создает сжатый поток AVI, подходящий для фильтра AVI-кодека, и звуковой выход, который создает звуковой поток, подходящий для фильтра рендеринга звука или промежуточного фильтра преобразования звука.

## <a name="related-topics"></a>См. также

<dl> <dt>

[Фильтры DirectShow](directshow-filters.md)
</dt> </dl>

 

 



