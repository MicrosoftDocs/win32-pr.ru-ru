---
description: Поиск типов вывода звукового кодировщика
ms.assetid: cd47d45b-ea47-4dec-867e-d51145d7f084
title: Поиск типов выходных данных звукового кодировщика (Microsoft Media Foundation)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5389274cca1178ebc0ae03e21f7a804f73a5db48
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105701312"
---
# <a name="finding-audio-encoder-output-types-microsoft-media-foundation"></a><span data-ttu-id="37c11-103">Поиск типов выходных данных звукового кодировщика (Microsoft Media Foundation)</span><span class="sxs-lookup"><span data-stu-id="37c11-103">Finding Audio Encoder Output Types (Microsoft Media Foundation)</span></span>

<span data-ttu-id="37c11-104">Так как необходимо использовать выходной формат звукового кодировщика, перечисленный кодировщиком аудио, необходимо иметь способ найти наиболее подходящий формат.</span><span class="sxs-lookup"><span data-stu-id="37c11-104">Because you must use an audio encoder output format that is enumerated by the audio encoder, you need to have a way of finding the format that is most suited to your needs.</span></span> <span data-ttu-id="37c11-105">Количество каналов, бит на выборку и частота выборки для выбранного выхода должны соответствовать значениям для сжатого содержимого.</span><span class="sxs-lookup"><span data-stu-id="37c11-105">The number of channels, bits per sample, and sample rate of the output that you choose must match the values for the content that you compress.</span></span> <span data-ttu-id="37c11-106">Однако кодировщик может поддерживать несколько типов в этих ограничениях.</span><span class="sxs-lookup"><span data-stu-id="37c11-106">However, the encoder may support several types within these constraints.</span></span>

<span data-ttu-id="37c11-107">Выбор типа — это скорость потока в закодированном потоке; Вы хотите найти тип мультимедиа, который соответствует вашим входным данным, и имеет битовую скорость, максимально близкую к целевому значению.</span><span class="sxs-lookup"><span data-stu-id="37c11-107">The deciding factor for choosing a type is the bit rate of the encoded stream; you want to find a media type that matches your input and has a bit rate that is as close as possible to a target value.</span></span> <span data-ttu-id="37c11-108">При перечислении типов вывода с одной передачей VBR это значение качества, которое выбирает используемый тип.</span><span class="sxs-lookup"><span data-stu-id="37c11-108">If you are enumerating one-pass VBR output types, it is the quality value that will decide the type you use.</span></span> <span data-ttu-id="37c11-109">Дополнительные сведения о значениях качества в перечислимых типах вывода см. в разделе [перечисление звуковых типов для конкретных режимов кодирования](enumeratingaudiotypesforspecificencodingmodes.md).</span><span class="sxs-lookup"><span data-stu-id="37c11-109">For more information about quality values in enumerated output types, see [Enumerating Audio Types for Specific Encoding Modes](enumeratingaudiotypesforspecificencodingmodes.md).</span></span>

> [!Note]  
>    <span data-ttu-id="37c11-110">Кодировщик аудиозаписей перечисляет некоторые типы, являющиеся дубликатами других типов, практически всеми способами.</span><span class="sxs-lookup"><span data-stu-id="37c11-110">The audio encoder enumerates some types that are duplicates of other types in almost all ways.</span></span> <span data-ttu-id="37c11-111">Эти дубликаты существуют для форматов, где количество пакетов в секунду не соответствует требованиям к хранению в файлах ASF при синхронизации с видео.</span><span class="sxs-lookup"><span data-stu-id="37c11-111">These duplicates exist for formats where the number of packets per second does not meet the requirements for storage in ASF files when synchronized with video.</span></span> <span data-ttu-id="37c11-112">Звуковые файлы, синхронизированные с видео в ASF, должны содержать 3 или более пакетов в секунду для скорости передачи данных менее 32000, а 5 или более пакетов в секунду для скорости передачи данных, превышающих или равных 32000.</span><span class="sxs-lookup"><span data-stu-id="37c11-112">Audio synchronized with video in an ASF file must have 3 or more packets per second for bit rates less than 32000, and 5 or more packets per second for bit rates greater than or equal to 32000.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="37c11-113">См. также</span><span class="sxs-lookup"><span data-stu-id="37c11-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="37c11-114">Настройка кодирования звука</span><span class="sxs-lookup"><span data-stu-id="37c11-114">Configuring Audio Encoding</span></span>](configuringaudioencoding.md)
</dt> <dt>

[<span data-ttu-id="37c11-115">Перечисление типов аудио для конкретных режимов кодирования</span><span class="sxs-lookup"><span data-stu-id="37c11-115">Enumerating Audio Types for Specific Encoding Modes</span></span>](enumeratingaudiotypesforspecificencodingmodes.md)
</dt> </dl>

 

 



