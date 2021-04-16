---
description: Передача DV из файла на ленту
ms.assetid: f6dd8c4b-0535-42b9-a969-89e7b9e6ee0f
title: Передача DV из файла на ленту
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 415a12f0876d3bd8e2a46de58b15f96f3eba3e2f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105664184"
---
# <a name="transmit-dv-from-file-to-tape"></a><span data-ttu-id="a40f6-103">Передача DV из файла на ленту</span><span class="sxs-lookup"><span data-stu-id="a40f6-103">Transmit DV from File to Tape</span></span>

<span data-ttu-id="a40f6-104">Передача из видео AVI-файла на ленту Втр немного усложняется тем, что файлы могут иметь тип – 1 или тип-2.</span><span class="sxs-lookup"><span data-stu-id="a40f6-104">Transmit from DV AVI file to VTR tape is complicated somewhat by the fact that files can type-1 or type-2.</span></span> <span data-ttu-id="a40f6-105">Чтобы передать DV-файл на ленту, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="a40f6-105">To transmit a DV file to tape, do the following:</span></span>

1.  <span data-ttu-id="a40f6-106">Создайте экземпляр фильтра [драйвера мсдв](msdv-driver.md) .</span><span class="sxs-lookup"><span data-stu-id="a40f6-106">Create an instance of the [MSDV Driver](msdv-driver.md) filter.</span></span> <span data-ttu-id="a40f6-107">Дополнительные сведения см. [в разделе Выбор устройства записи](selecting-a-capture-device.md).</span><span class="sxs-lookup"><span data-stu-id="a40f6-107">For more information, see [Selecting a Capture Device](selecting-a-capture-device.md).</span></span>
2.  <span data-ttu-id="a40f6-108">Убедитесь, что устройство находится в режиме Втр.</span><span class="sxs-lookup"><span data-stu-id="a40f6-108">Make sure the device is in VTR mode.</span></span> <span data-ttu-id="a40f6-109">В противном случае передать на ленту невозможно. См. раздел [режим устройства](device-mode.md).</span><span class="sxs-lookup"><span data-stu-id="a40f6-109">Otherwise, you cannot transmit to tape.See [Device Mode](device-mode.md).</span></span>
3.  <span data-ttu-id="a40f6-110">Инициализируйте построитель диаграмм записи, как описано в разделе [о построителе диаграмм записи](about-the-capture-graph-builder.md).</span><span class="sxs-lookup"><span data-stu-id="a40f6-110">Initialize the Capture Graph Builder, as described in [About the Capture Graph Builder](about-the-capture-graph-builder.md).</span></span>
4.  <span data-ttu-id="a40f6-111">Создайте граф.</span><span class="sxs-lookup"><span data-stu-id="a40f6-111">Build the graph.</span></span> <span data-ttu-id="a40f6-112">Конфигурация графа зависит от типа файла DV:</span><span class="sxs-lookup"><span data-stu-id="a40f6-112">The graph configuration depends on the DV file type:</span></span>
    -   [<span data-ttu-id="a40f6-113">Передача из файла типа-1</span><span class="sxs-lookup"><span data-stu-id="a40f6-113">Transmit from Type-1 File</span></span>](transmit-from-type-1-file.md)
    -   [<span data-ttu-id="a40f6-114">Передача из файла типа 2</span><span class="sxs-lookup"><span data-stu-id="a40f6-114">Transmit from Type-2 File</span></span>](transmit-from-type-2-file.md)
5.  <span data-ttu-id="a40f6-115">Переведите устройство в режим приостановки записи, как описано в разделе [Управление ВИДЕОкамерой](controlling-a-dv-camcorder.md).</span><span class="sxs-lookup"><span data-stu-id="a40f6-115">Put the device into record-pause mode, as described in [Controlling a DV Camcorder](controlling-a-dv-camcorder.md).</span></span>
6.  <span data-ttu-id="a40f6-116">Приостановка графа фильтра.</span><span class="sxs-lookup"><span data-stu-id="a40f6-116">Pause the filter graph.</span></span> <span data-ttu-id="a40f6-117">Пока граф фильтра приостановлен, он отправляет непрерывный поток, который повторяет первый кадр видео.</span><span class="sxs-lookup"><span data-stu-id="a40f6-117">While the filter graph is paused, it sends a continuous stream that repeats the first frame of video.</span></span>
7.  <span data-ttu-id="a40f6-118">Чтобы начать передачу, переведите устройство в режим записи, а затем запустите граф фильтра.</span><span class="sxs-lookup"><span data-stu-id="a40f6-118">To start transmitting, put the device into record mode and then run the filter graph.</span></span> <span data-ttu-id="a40f6-119">Он занимает определенное время, пока заголовку записи не удается выполнить запись, поэтому подождите около двух секунд перед выполнением графа.</span><span class="sxs-lookup"><span data-stu-id="a40f6-119">It takes the device a certain amount of time until the recording head is able to record, so wait for about two seconds before running the graph.</span></span> <span data-ttu-id="a40f6-120">Это может привести к созданию нескольких повторяющихся кадров в начале ленты, но гарантирует отсутствие потери данных.</span><span class="sxs-lookup"><span data-stu-id="a40f6-120">This might result in a few duplicated frames at the beginning of the tape, but it ensures that no data is lost.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a40f6-121">См. также</span><span class="sxs-lookup"><span data-stu-id="a40f6-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a40f6-122">Цифровое видео в DirectShow</span><span class="sxs-lookup"><span data-stu-id="a40f6-122">Digital Video in DirectShow</span></span>](digital-video-in-directshow.md)
</dt> </dl>

 

 



