---
description: Модуль записи приемника — это компонент для кодирования аудио-или видеофайлов.
ms.assetid: 23AF25B8-B94C-48BC-83D8-5863ACFFD4CA
title: Модуль записи приемников
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d6b30d75e369de343bae61ba56dfd05c0d5d12a4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104344385"
---
# <a name="sink-writer"></a><span data-ttu-id="94fee-103">Модуль записи приемников</span><span class="sxs-lookup"><span data-stu-id="94fee-103">Sink Writer</span></span>

<span data-ttu-id="94fee-104">Модуль записи приемника — это компонент для кодирования аудио-или видеофайлов.</span><span class="sxs-lookup"><span data-stu-id="94fee-104">The sink writer is a component for encoding audio or video files.</span></span>

<span data-ttu-id="94fee-105">На приведенной ниже схеме на высоком уровне показано, как приложение использует модуль записи приемника для кодирования и аудио-или видеофайла.</span><span class="sxs-lookup"><span data-stu-id="94fee-105">The following diagram shows, at a high level, how an application uses the sink writer to encode and audio/video file.</span></span>

![Схема, на которой показан модуль записи приемника.](images/encoding09.png)

<span data-ttu-id="94fee-107">Модуль записи приемника содержит приемник мультимедиа и, при необходимости, один или несколько кодировщиков.</span><span class="sxs-lookup"><span data-stu-id="94fee-107">The sink writer hosts a media sink and optionally one or more encoders.</span></span> <span data-ttu-id="94fee-108">Кодировщики преобразуют несжатые аудио или видео данные в закодированные битстреамс.</span><span class="sxs-lookup"><span data-stu-id="94fee-108">The encoders convert uncompressed audio or video data to encoded bitstreams.</span></span> <span data-ttu-id="94fee-109">Приемник мультимедиа выводит битстреамс в файл.</span><span class="sxs-lookup"><span data-stu-id="94fee-109">The media sink outputs the bitstreams to a file.</span></span> <span data-ttu-id="94fee-110">Модуль записи приемников выполняет следующие задачи:</span><span class="sxs-lookup"><span data-stu-id="94fee-110">The sink writer performs the following tasks:</span></span>

-   <span data-ttu-id="94fee-111">Загружает приемник мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="94fee-111">Loads the media sink.</span></span>
-   <span data-ttu-id="94fee-112">Находит и загружает кодировщики.</span><span class="sxs-lookup"><span data-stu-id="94fee-112">Finds and loads the encoders.</span></span>
-   <span data-ttu-id="94fee-113">Управляет потоком данных для кодировщиков и приемника мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="94fee-113">Manages the data flow to the encoders and the media sink.</span></span>

<span data-ttu-id="94fee-114">Приложение передает аудио-и видеоданные в модуль записи приемника в качестве входных данных.</span><span class="sxs-lookup"><span data-stu-id="94fee-114">The application passes audio/video data to the sink writer as input.</span></span> <span data-ttu-id="94fee-115">Не имеет значения, как приложение получает или создает входные данные.</span><span class="sxs-lookup"><span data-stu-id="94fee-115">It does not matter how the application obtains or generates the input data.</span></span> <span data-ttu-id="94fee-116">Один из вариантов — использовать [средство чтения исходного кода](source-reader.md), как показано на следующей схеме.</span><span class="sxs-lookup"><span data-stu-id="94fee-116">One option is to use the [Source Reader](source-reader.md), as shown in the following diagram.</span></span> <span data-ttu-id="94fee-117">Однако модуль записи приемника не требует использования модуля чтения исходного кода.</span><span class="sxs-lookup"><span data-stu-id="94fee-117">However, the sink writer does not require the use of the source reader.</span></span> <span data-ttu-id="94fee-118">Эти два компонента являются независимыми.</span><span class="sxs-lookup"><span data-stu-id="94fee-118">These two components are independent.</span></span>

![Схема, на которой показан модуль чтения исходного кода и модуль записи приемника.](images/encoding02.png)

## <a name="in-this-section"></a><span data-ttu-id="94fee-120">Содержание раздела</span><span class="sxs-lookup"><span data-stu-id="94fee-120">In this section</span></span>

-   [<span data-ttu-id="94fee-121">Использование модуля записи приемника</span><span class="sxs-lookup"><span data-stu-id="94fee-121">Using the Sink Writer</span></span>](using-the-sink-writer.md)
-   [<span data-ttu-id="94fee-122">Учебник. Использование модуля записи приемника для кодирования видео</span><span class="sxs-lookup"><span data-stu-id="94fee-122">Tutorial: Using the Sink Writer to Encode Video</span></span>](tutorial--using-the-sink-writer-to-encode-video.md)

## <a name="related-topics"></a><span data-ttu-id="94fee-123">См. также</span><span class="sxs-lookup"><span data-stu-id="94fee-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="94fee-124">Кодировка и разработка файлов</span><span class="sxs-lookup"><span data-stu-id="94fee-124">Encoding and File Authoring</span></span>](encoding-and-file-authoring.md)
</dt> <dt>

[<span data-ttu-id="94fee-125">Общие сведения о кодировке в Media Foundation</span><span class="sxs-lookup"><span data-stu-id="94fee-125">Overview of Encoding in Media Foundation</span></span>](overview-of-encoding-in-media-foundation.md)
</dt> </dl>

 

 



