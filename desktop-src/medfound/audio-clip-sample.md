---
description: Показывает, как использовать Microsoft Media Foundation для декодирования звука из файла мультимедиа.
ms.assetid: 29822e6b-8598-4133-b181-7fb0854553b7
title: Пример аудиоклипа
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9c0e4a3e515d08e2cafd2ab2ba451a528f3d5677
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105682378"
---
# <a name="audio-clip-sample"></a><span data-ttu-id="67af6-103">Пример аудиоклипа</span><span class="sxs-lookup"><span data-stu-id="67af6-103">Audio Clip Sample</span></span>

<span data-ttu-id="67af6-104">Показывает, как использовать Microsoft Media Foundation для декодирования звука из файла мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="67af6-104">Shows how to use Microsoft Media Foundation to decode audio from a media file.</span></span>

<span data-ttu-id="67af6-105">Пример приложения для аудио-клипа считывает звуковые данные из файла мультимедиа и записывает несжатое аудио в ВОЛНовый файл.</span><span class="sxs-lookup"><span data-stu-id="67af6-105">The Audio Clip sample application reads audio data from a media file and writes the uncompressed audio to a WAVE file.</span></span>

## <a name="apis-demonstrated"></a><span data-ttu-id="67af6-106">Продемонстрированные API</span><span class="sxs-lookup"><span data-stu-id="67af6-106">APIs Demonstrated</span></span>

<span data-ttu-id="67af6-107">В этом образце демонстрируются следующие интерфейсы Media Foundation:</span><span class="sxs-lookup"><span data-stu-id="67af6-107">This sample demonstrates the following Media Foundation interfaces:</span></span>

-   [<span data-ttu-id="67af6-108">**имфсаурцереадер**</span><span class="sxs-lookup"><span data-stu-id="67af6-108">**IMFSourceReader**</span></span>](/windows/desktop/api/mfreadwrite/nn-mfreadwrite-imfsourcereader)

## <a name="usage"></a><span data-ttu-id="67af6-109">Использование</span><span class="sxs-lookup"><span data-stu-id="67af6-109">Usage</span></span>

<span data-ttu-id="67af6-110">Этот пример представляет собой приложение командной строки.</span><span class="sxs-lookup"><span data-stu-id="67af6-110">This sample is a command-line application.</span></span> <span data-ttu-id="67af6-111">Он использует следующие аргументы командной строки:</span><span class="sxs-lookup"><span data-stu-id="67af6-111">It uses the following command-line arguments:</span></span>

``` syntax
audioclip.exe inputfile outputfile.wav
```

-   <span data-ttu-id="67af6-112">inputFile: имя файла, содержащего аудиопоток.</span><span class="sxs-lookup"><span data-stu-id="67af6-112">inputfile: The name of a file that contains an audio stream.</span></span>
-   <span data-ttu-id="67af6-113">выходной_файл. WAV: Имя записываемого файла звукозаписи.</span><span class="sxs-lookup"><span data-stu-id="67af6-113">outputfile.wav: The name of the WAVE file to write.</span></span>

## <a name="requirements"></a><span data-ttu-id="67af6-114">Требования</span><span class="sxs-lookup"><span data-stu-id="67af6-114">Requirements</span></span>



| <span data-ttu-id="67af6-115">Продукт</span><span class="sxs-lookup"><span data-stu-id="67af6-115">Product</span></span>                                                        | <span data-ttu-id="67af6-116">Version</span><span class="sxs-lookup"><span data-stu-id="67af6-116">Version</span></span>   |
|----------------------------------------------------------------|-----------|
| [<span data-ttu-id="67af6-117">Windows SDK</span><span class="sxs-lookup"><span data-stu-id="67af6-117">Windows SDK</span></span>](https://msdn.microsoft.com/windowsvista/bb980924.aspx) | <span data-ttu-id="67af6-118">Windows 7</span><span class="sxs-lookup"><span data-stu-id="67af6-118">Windows 7</span></span> |



 

## <a name="downloading-the-sample"></a><span data-ttu-id="67af6-119">Загрузка образца</span><span class="sxs-lookup"><span data-stu-id="67af6-119">Downloading the Sample</span></span>

<span data-ttu-id="67af6-120">Этот пример доступен в [репозитории GitHub с классическими примерами Windows](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/multimedia/mediafoundation/AudioClip).</span><span class="sxs-lookup"><span data-stu-id="67af6-120">This sample is available in the [Windows classic samples github repository](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/multimedia/mediafoundation/AudioClip).</span></span>

## <a name="related-topics"></a><span data-ttu-id="67af6-121">См. также</span><span class="sxs-lookup"><span data-stu-id="67af6-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="67af6-122">Примеры пакетов SDK Media Foundation</span><span class="sxs-lookup"><span data-stu-id="67af6-122">Media Foundation SDK Samples</span></span>](media-foundation-sdk-samples.md)
</dt> <dt>

[<span data-ttu-id="67af6-123">Модуль чтения исходного кода</span><span class="sxs-lookup"><span data-stu-id="67af6-123">Source Reader</span></span>](source-reader.md)
</dt> <dt>

[<span data-ttu-id="67af6-124">Учебник. декодирование аудио</span><span class="sxs-lookup"><span data-stu-id="67af6-124">Tutorial: Decoding Audio</span></span>](tutorial--decoding-audio.md)
</dt> </dl>

 

 



