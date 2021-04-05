---
title: Рекомендации по расширению имени файла
description: Рекомендации по расширению имени файла
ms.assetid: 71189ed8-4140-446f-a765-d72f35dd3d88
keywords:
- Windows Media Format SDK, расширения имен файлов
- Расширенный формат систем (ASF), расширения имен файлов
- ASF (Расширенный системный формат), расширения имен файлов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5bed1fb59379644711a3954dc5eb82707e0e42f8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103986430"
---
# <a name="file-name-extension-guidelines"></a><span data-ttu-id="f4428-106">Рекомендации по расширению имени файла</span><span class="sxs-lookup"><span data-stu-id="f4428-106">File Name Extension Guidelines</span></span>

<span data-ttu-id="f4428-107">Расширение имени файла предоставляет независимому поставщику программного обеспечения сведения о требованиях к подготовке к просмотру приложения, использующего это конкретное расширение.</span><span class="sxs-lookup"><span data-stu-id="f4428-107">A file name extension provides an independent software vendor with information about the rendering requirements of an application that uses that particular extension.</span></span>

<span data-ttu-id="f4428-108">Расширение имени файла, которое необходимо использовать для файла, созданного приложением на основе пакета SDK формата Windows Media, определяется типом содержимого файла.</span><span class="sxs-lookup"><span data-stu-id="f4428-108">The file name extension you must use for a file created by an application based on the Windows Media Format SDK is determined by the type of content in the file.</span></span> <span data-ttu-id="f4428-109">Используйте следующую логику, чтобы определить расширение имени файла, которое необходимо использовать.</span><span class="sxs-lookup"><span data-stu-id="f4428-109">Use the following logic to determine the file name extension you must use.</span></span>

<span data-ttu-id="f4428-110">Если файл содержит потоки, закодированные сторонними кодеками или неподдерживаемые несжатые данные (включая произвольные данные), файл должен использовать расширение ASF.</span><span class="sxs-lookup"><span data-stu-id="f4428-110">If the file contains any streams encoded with third-party codecs or any unsupported uncompressed data (including arbitrary data), the file must use the .asf extension.</span></span>

<span data-ttu-id="f4428-111">Если файл не содержит неподдерживаемых потоков и содержит один или несколько видеопотоков, несжатых или закодированных с помощью видеокодека Windows Media, то файл должен использовать расширение WMV.</span><span class="sxs-lookup"><span data-stu-id="f4428-111">If the file contains no unsupported streams and contains one or more video streams either uncompressed or encoded with any Windows Media video codec, the file must use the .wmv extension.</span></span> <span data-ttu-id="f4428-112">Эти файлы также могут включать звуковые потоки PCM, звуковые потоки, закодированные с помощью любого кодека Windows Media Audio, потоков сценариев и веб-потоков.</span><span class="sxs-lookup"><span data-stu-id="f4428-112">These files may also include PCM audio streams, audio streams encoded with any Windows Media audio codec, script streams, and Web streams.</span></span>

<span data-ttu-id="f4428-113">Если файл не содержит неподдерживаемых потоков и не поддерживает видеопотокы и содержит один или несколько звуковых потоков либо несжатый PCM, либо закодированы с помощью любого кодека Windows Media Audio, файл должен использовать расширение WMA.</span><span class="sxs-lookup"><span data-stu-id="f4428-113">If the file contains no unsupported streams and no supported video streams, and contains one or more audio streams either uncompressed PCM or encoded with any Windows Media audio codec, the file must use the .wma extension.</span></span> <span data-ttu-id="f4428-114">Эти файлы также могут содержать потоки скриптов и веб-потоки.</span><span class="sxs-lookup"><span data-stu-id="f4428-114">These files may also contain script streams, and Web streams.</span></span>

<span data-ttu-id="f4428-115">Если файл содержит только потоки, не являющиеся ни звуком, ни видео, необходимо использовать расширение ASF.</span><span class="sxs-lookup"><span data-stu-id="f4428-115">If the file contains only streams that are neither audio nor video, it must use the .asf extension.</span></span>

<span data-ttu-id="f4428-116">Поддерживаются несжатые типы видео: RGB8, RGB565, RGB555, RGB24, RGB32, I420, ИЙУВ, YV12, YUY2, UYVY, ИВЮ и YVU9.</span><span class="sxs-lookup"><span data-stu-id="f4428-116">Supported uncompressed video types include RGB8, RGB565, RGB555, RGB24, RGB32, I420, IYUV, YV12, YUY2, UYVY, YVYU, and YVU9.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f4428-117">См. также</span><span class="sxs-lookup"><span data-stu-id="f4428-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f4428-118">**Рекомендации по проекту**</span><span class="sxs-lookup"><span data-stu-id="f4428-118">**Project Considerations**</span></span>](project-considerations.md)
</dt> </dl>

 

 




