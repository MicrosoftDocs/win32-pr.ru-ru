---
description: Сравнение типа 1 и
ms.assetid: 3f1cf981-f678-46a6-9784-ffb389438b6d
title: Файлы видео AVI типа-1 и Type-2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0000b81e94e25749b5590287145a88a28280e16d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103998699"
---
# <a name="type-1-vs-type-2-dv-avi-files"></a><span data-ttu-id="6d2ec-103">Файлы видео AVI типа-1 и Type-2</span><span class="sxs-lookup"><span data-stu-id="6d2ec-103">Type-1 vs. Type-2 DV AVI Files</span></span>

<span data-ttu-id="6d2ec-104">Видеокамеры создают чередование аудио-видео; в каждом кадре видео также содержатся звуковые данные.</span><span class="sxs-lookup"><span data-stu-id="6d2ec-104">DV cameras produce interleaved audio-video; each frame of video also contains the audio information.</span></span> <span data-ttu-id="6d2ec-105">При сохранении DV-данных в файл AVI можно выбрать следующее:</span><span class="sxs-lookup"><span data-stu-id="6d2ec-105">If you save DV data to an AVI file, you have a choice:</span></span>

-   <span data-ttu-id="6d2ec-106">Храните данные с чередованием в виде одного потока в файле AVI.</span><span class="sxs-lookup"><span data-stu-id="6d2ec-106">Store the interleaved data as one stream in the AVI file.</span></span> <span data-ttu-id="6d2ec-107">Это называется файлом типа 1.</span><span class="sxs-lookup"><span data-stu-id="6d2ec-107">This is known as a type-1 file.</span></span>
-   <span data-ttu-id="6d2ec-108">Разделите чередующиеся данные на отдельные потоки аудио и видео.</span><span class="sxs-lookup"><span data-stu-id="6d2ec-108">Split the interleaved data into separate audio and video streams.</span></span> <span data-ttu-id="6d2ec-109">Это называется файлом типа 2.</span><span class="sxs-lookup"><span data-stu-id="6d2ec-109">This is known as a type-2 file.</span></span>

<span data-ttu-id="6d2ec-110">Для видеозаписи, где максимальная пропускная способность очень важна, лучше использовать файл типа 1, так как файлы типа 2 содержат избыточные звуковые данные.</span><span class="sxs-lookup"><span data-stu-id="6d2ec-110">For video capture, where maximum throughput is crucial, it is better to use a type-1 file, because type-2 files carry redundant audio data.</span></span> <span data-ttu-id="6d2ec-111">(В потоке видео по-прежнему есть звуковые данные.</span><span class="sxs-lookup"><span data-stu-id="6d2ec-111">(The video stream still has the audio data.</span></span> <span data-ttu-id="6d2ec-112">Звук просто скрыт, помечая поток как видео.) Кроме того, при написании файла типа 2 требуется дополнительное процессорное время для разделения потока с чередованием.</span><span class="sxs-lookup"><span data-stu-id="6d2ec-112">The audio is simply hidden by labeling the stream as video.) Also, writing a type-2 file requires some additional processor time to split the interleaved stream.</span></span>

<span data-ttu-id="6d2ec-113">С другой стороны, файлы типа-1 менее эффективны для редактирования в режиме реального времени.</span><span class="sxs-lookup"><span data-stu-id="6d2ec-113">On the other hand, type-1 files are less efficient for real-time editing.</span></span> <span data-ttu-id="6d2ec-114">Приложение должно извлекать звук из потока с чередованием, вносить изменения и переносить данные в промежутке.</span><span class="sxs-lookup"><span data-stu-id="6d2ec-114">The application must extract the audio from the interleaved stream, make the edits, and interleave the data again.</span></span> <span data-ttu-id="6d2ec-115">Кроме того, формат Type-1 несовместим с Microsoft® Video для Windows® (VFW).</span><span class="sxs-lookup"><span data-stu-id="6d2ec-115">Also, the type-1 format is not compatible with Microsoft® Video for Windows® (VFW).</span></span> <span data-ttu-id="6d2ec-116">DirectShow может работать с файлами обоих типов.</span><span class="sxs-lookup"><span data-stu-id="6d2ec-116">DirectShow can handle both types of files.</span></span>

<span data-ttu-id="6d2ec-117">Файл типа 2 можно преобразовать в тип-1 с помощью фильтра [DV мультиплексор](dv-muxer-filter.md) .</span><span class="sxs-lookup"><span data-stu-id="6d2ec-117">A type-2 file can be converted to type-1 using the [DV Muxer](dv-muxer-filter.md) filter.</span></span> <span data-ttu-id="6d2ec-118">Файл типа 1 можно преобразовать в тип-2 с помощью фильтра [разделителя DV](dv-splitter-filter.md) .</span><span class="sxs-lookup"><span data-stu-id="6d2ec-118">A type-1 file can be converted to type-2 using the [DV Splitter](dv-splitter-filter.md) filter.</span></span> <span data-ttu-id="6d2ec-119">На следующей схеме показано различие между двумя форматами.</span><span class="sxs-lookup"><span data-stu-id="6d2ec-119">The following diagram illustrates the difference between the two formats.</span></span>

![Преобразование между типами-1 и типом-2 DV](images/dv-filters3.png)

## <a name="related-topics"></a><span data-ttu-id="6d2ec-121">См. также</span><span class="sxs-lookup"><span data-stu-id="6d2ec-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6d2ec-122">Цифровое видео в DirectShow</span><span class="sxs-lookup"><span data-stu-id="6d2ec-122">Digital Video in DirectShow</span></span>](digital-video-in-directshow.md)
</dt> <dt>

[<span data-ttu-id="6d2ec-123">Данные DV в формате AVI</span><span class="sxs-lookup"><span data-stu-id="6d2ec-123">DV Data in the AVI File Format</span></span>](dv-data-in-the-avi-file-format.md)
</dt> </dl>

 

 



