---
description: Создание топологии воспроизведения с помощью Топоедит
ms.assetid: 4d4c4ff9-dad1-4c79-a44a-2ad20f1bbca0
title: Создание топологии воспроизведения с помощью Топоедит
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f942984b3ba56ef1288566cee80e7d30026de155
ms.sourcegitcommit: 37f276b5d887a3aad04b1ba86e390dea9d87e591
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/04/2021
ms.locfileid: "105693806"
---
# <a name="building-a-playback-topology-with-topoedit"></a><span data-ttu-id="f35df-103">Создание топологии воспроизведения с помощью Топоедит</span><span class="sxs-lookup"><span data-stu-id="f35df-103">Building a Playback Topology with TopoEdit</span></span>

<span data-ttu-id="f35df-104">Топоедит может создать топологию воспроизведения для локального файла мультимедиа путем автоматического добавления и подключения исходных, преобразуемых и выходных узлов.</span><span class="sxs-lookup"><span data-stu-id="f35df-104">TopoEdit can build a playback topology for a local media file by automatically adding and connecting the source, transform, and output nodes.</span></span> <span data-ttu-id="f35df-105">Топоедит не разрешает автоматическую топологию.</span><span class="sxs-lookup"><span data-stu-id="f35df-105">TopoEdit does not automatically resolve the topology.</span></span> <span data-ttu-id="f35df-106">Чтобы воспроизвести топологию, разрешите ее, а затем используйте элементы управления транспорта.</span><span class="sxs-lookup"><span data-stu-id="f35df-106">To play the topology, resolve it and then use the transport controls.</span></span>

## <a name="to-build-and-play-a-topology-for-a-media-file"></a><span data-ttu-id="f35df-107">Создание и воспроизведение топологии для файла мультимедиа</span><span class="sxs-lookup"><span data-stu-id="f35df-107">To build and play a topology for a media file</span></span>

1.  <span data-ttu-id="f35df-108">В меню **файл** выберите команду **визуализировать файл**.</span><span class="sxs-lookup"><span data-stu-id="f35df-108">On the **File** menu, click **Render File**.</span></span>

    <span data-ttu-id="f35df-109">Откроется диалоговое окно **Выбор источника носителя** .</span><span class="sxs-lookup"><span data-stu-id="f35df-109">This opens the **Select Media Source** dialog box.</span></span>

2.  <span data-ttu-id="f35df-110">Перейдите к папке, в которой находится файл мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="f35df-110">Navigate to the folder where the media file is located.</span></span>
3.  <span data-ttu-id="f35df-111">В поле **имя файла:** введите имя файла.</span><span class="sxs-lookup"><span data-stu-id="f35df-111">In the **File name:** field, enter the name of the file.</span></span>
4.  <span data-ttu-id="f35df-112">Нажмите кнопку **Открыть**.</span><span class="sxs-lookup"><span data-stu-id="f35df-112">Click **Open**.</span></span>

    <span data-ttu-id="f35df-113">На **панели топология** отображается топология подключения.</span><span class="sxs-lookup"><span data-stu-id="f35df-113">The **Topology Pane** shows the connected topology.</span></span> <span data-ttu-id="f35df-114">На внутреннем уровне Топоедит выполняет следующие задачи:</span><span class="sxs-lookup"><span data-stu-id="f35df-114">Internally, TopoEdit performs the following tasks:</span></span>

    -   <span data-ttu-id="f35df-115">Перечисляет потоки в файле мультимедиа и создает исходные узлы.</span><span class="sxs-lookup"><span data-stu-id="f35df-115">Enumerates the streams in the media file and creates the source nodes.</span></span>
    -   <span data-ttu-id="f35df-116">В зависимости от типа носителя исходных узлов добавляет узлы преобразования, такие как декодеры.</span><span class="sxs-lookup"><span data-stu-id="f35df-116">Depending on the media type of the source nodes, adds transform nodes, such as decoders.</span></span>
    -   <span data-ttu-id="f35df-117">Добавляет приемник потокового воспроизведения (САР) для потокового воспроизведения и расширенный приемник модуля подготовки видео (Евр) для видеопотока.</span><span class="sxs-lookup"><span data-stu-id="f35df-117">Adds the Streaming Audio Renderer (SAR) sink for audio stream and the enhanced video renderer (EVR) sink for the video stream.</span></span>
    -   <span data-ttu-id="f35df-118">Подключает входные и выходные данные узла.</span><span class="sxs-lookup"><span data-stu-id="f35df-118">Connects the node inputs and the node outputs.</span></span>

5.  <span data-ttu-id="f35df-119">В меню **топология** выберите пункт **Разрешить топологию**.</span><span class="sxs-lookup"><span data-stu-id="f35df-119">On the **Topology** menu, click **Resolve Topology**.</span></span>
6.  <span data-ttu-id="f35df-120">Нажмите кнопку **Воспроизведение** на панели инструментов, чтобы воспроизвести топологию.</span><span class="sxs-lookup"><span data-stu-id="f35df-120">Click the **Play** button on the toolbar to play the topology.</span></span> На следующем рисунке показана  кнопка воспроизведения :::image type="icon" source="images/536e8908-ef44-4d25-98f1-c06b5ef37591.jpg"::: .

## <a name="related-topics"></a><span data-ttu-id="f35df-122">См. также</span><span class="sxs-lookup"><span data-stu-id="f35df-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f35df-123">Элементы управления воспроизведением в Топоедит</span><span class="sxs-lookup"><span data-stu-id="f35df-123">Playback Controls in TopoEdit</span></span>](playback-controls-in-topoedit.md)
</dt> <dt>

[<span data-ttu-id="f35df-124">Разрешение топологии с помощью Топоедит</span><span class="sxs-lookup"><span data-stu-id="f35df-124">Resolving a Topology with TopoEdit</span></span>](resolving-a-topology-with-topoedit.md)
</dt> <dt>

[<span data-ttu-id="f35df-125">топоедит</span><span class="sxs-lookup"><span data-stu-id="f35df-125">TopoEdit</span></span>](topoedit.md)
</dt> </dl>

 

 



