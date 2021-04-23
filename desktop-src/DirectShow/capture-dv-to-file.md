---
description: Записать DV в файл
ms.assetid: f7a8bcbb-a744-43c4-a226-354ae2d94df8
title: Записать DV в файл
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 713e49eba3016b353362c541ba31ffd6a1ae5de7
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104341915"
---
# <a name="capture-dv-to-file"></a><span data-ttu-id="6cfd1-103">Записать DV в файл</span><span class="sxs-lookup"><span data-stu-id="6cfd1-103">Capture DV to File</span></span>

<span data-ttu-id="6cfd1-104">В этом разделе описывается запись цифрового видео (DV) с цифровой камеры или с ленты Втр.</span><span class="sxs-lookup"><span data-stu-id="6cfd1-104">This section describes how to capture digital video (DV) from a DV camera or from a VTR tape.</span></span>

1.  <span data-ttu-id="6cfd1-105">Создайте экземпляр фильтра [драйвера мсдв](msdv-driver.md) .</span><span class="sxs-lookup"><span data-stu-id="6cfd1-105">Create an instance of the [MSDV Driver](msdv-driver.md) filter.</span></span> <span data-ttu-id="6cfd1-106">Дополнительные сведения см. [в разделе Выбор устройства записи](selecting-a-capture-device.md).</span><span class="sxs-lookup"><span data-stu-id="6cfd1-106">For more information, see [Selecting a Capture Device](selecting-a-capture-device.md).</span></span>
2.  <span data-ttu-id="6cfd1-107">Инициализируйте построитель диаграмм записи, как описано в разделе [о построителе диаграмм записи](about-the-capture-graph-builder.md).</span><span class="sxs-lookup"><span data-stu-id="6cfd1-107">Initialize the Capture Graph Builder, as described in [About the Capture Graph Builder](about-the-capture-graph-builder.md).</span></span>
3.  <span data-ttu-id="6cfd1-108">Создайте граф записи в зависимости от типа целевого файла:</span><span class="sxs-lookup"><span data-stu-id="6cfd1-108">Build the capture graph, depending on the target file type:</span></span>
    -   [<span data-ttu-id="6cfd1-109">Запись файла DV типа 1</span><span class="sxs-lookup"><span data-stu-id="6cfd1-109">Capture a Type-1 DV File</span></span>](capture-a-type-1-dv-file.md)
    -   [<span data-ttu-id="6cfd1-110">Запись файла DV типа 2</span><span class="sxs-lookup"><span data-stu-id="6cfd1-110">Capture a Type-2 DV File</span></span>](capture-a-type-2-dv-file.md)
    -   [<span data-ttu-id="6cfd1-111">Записать DV в Распакованный RGB</span><span class="sxs-lookup"><span data-stu-id="6cfd1-111">Capture DV to Uncompressed RGB</span></span>](capture-dv-to-uncompressed-rgb.md)
4.  <span data-ttu-id="6cfd1-112">Запустите граф.</span><span class="sxs-lookup"><span data-stu-id="6cfd1-112">Run the graph.</span></span>

<span data-ttu-id="6cfd1-113">Захват с ленты Втр работает так же, как запись живого видео с камеры, за исключением того, что необходимо воспроизвести ленту, как описано в разделе [Управление](controlling-a-dv-camcorder.md)видеокамерой.</span><span class="sxs-lookup"><span data-stu-id="6cfd1-113">Capturing from a VTR tape works just like capturing live video from the camera, except that you must play the tape, as described in [Controlling a DV Camcorder](controlling-a-dv-camcorder.md).</span></span> <span data-ttu-id="6cfd1-114">Чтобы избежать потери кадров, сначала запустите граф, а затем воспроизводите ленту.</span><span class="sxs-lookup"><span data-stu-id="6cfd1-114">To avoid losing any frames, run the graph first, and then play the tape.</span></span> <span data-ttu-id="6cfd1-115">Когда передача завершится, сначала завершите ленту, а затем закройте граф.</span><span class="sxs-lookup"><span data-stu-id="6cfd1-115">When you are done transmitting, stop the tape first and then stop the graph.</span></span>

> [!Note]  
> <span data-ttu-id="6cfd1-116">Видеокамера должна быть в режиме Втр.</span><span class="sxs-lookup"><span data-stu-id="6cfd1-116">The camcorder must be in VTR mode.</span></span> <span data-ttu-id="6cfd1-117">См. раздел [режим устройства](device-mode.md).</span><span class="sxs-lookup"><span data-stu-id="6cfd1-117">See [Device Mode](device-mode.md).</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="6cfd1-118">См. также</span><span class="sxs-lookup"><span data-stu-id="6cfd1-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6cfd1-119">Цифровое видео в DirectShow</span><span class="sxs-lookup"><span data-stu-id="6cfd1-119">Digital Video in DirectShow</span></span>](digital-video-in-directshow.md)
</dt> <dt>

[<span data-ttu-id="6cfd1-120">Файлы видео AVI типа-1 и Type-2</span><span class="sxs-lookup"><span data-stu-id="6cfd1-120">Type-1 vs. Type-2 DV AVI Files</span></span>](type-1-vs--type-2-dv-avi-files.md)
</dt> <dt>

[<span data-ttu-id="6cfd1-121">Видеозапись</span><span class="sxs-lookup"><span data-stu-id="6cfd1-121">Video Capture</span></span>](video-capture.md)
</dt> </dl>

 

 



