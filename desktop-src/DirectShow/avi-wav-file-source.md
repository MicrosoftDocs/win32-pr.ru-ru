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
# <a name="aviwav-file-source"></a><span data-ttu-id="fb880-103">Источник файла AVI/WAV</span><span class="sxs-lookup"><span data-stu-id="fb880-103">AVI/WAV File Source</span></span>

<span data-ttu-id="fb880-104">(Не рекомендуется к использованию.</span><span class="sxs-lookup"><span data-stu-id="fb880-104">(Deprecated.</span></span> <span data-ttu-id="fb880-105">Для файлов AVI и WAV используйте [файл источник (асинхронный)](file-source--async--filter.md) и [средство синтаксического анализа](wave-parser-filter.md) [AVI](avi-splitter-filter.md) или Wave.)</span><span class="sxs-lookup"><span data-stu-id="fb880-105">For AVI and WAV files, use the [File Source (Async)](file-source--async--filter.md) and the [AVI Splitter](avi-splitter-filter.md) or [WAVE Parser](wave-parser-filter.md).)</span></span>

<span data-ttu-id="fb880-106">Фильтр источника файла AVI/WAV считывает исходные файлы AVI и WAV и создает соответствующие выходные сигналы для типа файла.</span><span class="sxs-lookup"><span data-stu-id="fb880-106">The AVI/WAV File Source filter reads AVI and WAV source files and generates the appropriate output pins for the file type.</span></span>

<span data-ttu-id="fb880-107">Для файлов WAV фильтр создает ПИН-код вывода звука, который создает звуковой поток, который можно подключить к фильтру подготовки аудио или к фильтру преобразования звука.</span><span class="sxs-lookup"><span data-stu-id="fb880-107">For WAV files, the filter creates an audio output pin, which produces an audio stream that can be connected to an audio rendering filter or intervening audio transform filter.</span></span>

<span data-ttu-id="fb880-108">Для файлов AVI фильтр создает ПИН-код для вывода видео, который создает сжатый поток AVI, подходящий для фильтра AVI-кодека, и звуковой выход, который создает звуковой поток, подходящий для фильтра рендеринга звука или промежуточного фильтра преобразования звука.</span><span class="sxs-lookup"><span data-stu-id="fb880-108">For AVI files, the filter creates a video output pin, which produces a compressed AVI stream suitable for the AVI codec filter, and an audio output pin, which produces an audio stream suitable for an audio rendering filter or an intervening audio transform filter.</span></span>

## <a name="related-topics"></a><span data-ttu-id="fb880-109">См. также</span><span class="sxs-lookup"><span data-stu-id="fb880-109">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fb880-110">Фильтры DirectShow</span><span class="sxs-lookup"><span data-stu-id="fb880-110">DirectShow Filters</span></span>](directshow-filters.md)
</dt> </dl>

 

 



