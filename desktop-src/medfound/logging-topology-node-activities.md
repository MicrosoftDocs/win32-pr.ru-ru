---
description: Действия узла топологии ведения журнала
ms.assetid: 853b3900-1214-43b9-bf0e-e45c1159c5f1
title: Действия узла топологии ведения журнала
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 327ca83d0513b97d053e27388bd0f2a418dfb253
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104080404"
---
# <a name="logging-topology-node-activities"></a><span data-ttu-id="272c5-103">Действия узла топологии ведения журнала</span><span class="sxs-lookup"><span data-stu-id="272c5-103">Logging Topology Node Activities</span></span>

<span data-ttu-id="272c5-104">Топоедит предоставляет возможность сбора сведений о ведении журнала для узла преобразования или выходного узла топологии.</span><span class="sxs-lookup"><span data-stu-id="272c5-104">TopoEdit provides the option for collecting logging information for a transform node or an output node of a topology.</span></span>

## <a name="to-setup-logging"></a><span data-ttu-id="272c5-105">Настройка ведения журнала</span><span class="sxs-lookup"><span data-stu-id="272c5-105">To setup logging</span></span>

1.  <span data-ttu-id="272c5-106">На **панели топология** выберите узел преобразования или выходной узел, щелкнув его.</span><span class="sxs-lookup"><span data-stu-id="272c5-106">On the **Topology Pane**, select a transform node or an output node by clicking it.</span></span>

2.  <span data-ttu-id="272c5-107">В меню **Сервис** выберите пункт **Spy Selected node**.</span><span class="sxs-lookup"><span data-stu-id="272c5-107">From the **Tools** menu, click **Spy Selected Node**.</span></span>

<span data-ttu-id="272c5-108">Во время создания топологии все вызовы методов на выбранном узле записываются в текстовый файл.</span><span class="sxs-lookup"><span data-stu-id="272c5-108">During topology building, all method calls on the selected node are logged to a text file.</span></span> <span data-ttu-id="272c5-109">Он сохраняется в папке, в которой находится файл мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="272c5-109">This is saved in the folder where the media file is located.</span></span> <span data-ttu-id="272c5-110">Файл журнала сохраняется с именем узла и уникальным идентификатором узла топологии.</span><span class="sxs-lookup"><span data-stu-id="272c5-110">The log file is saved with the node name and the unique topology node identifier.</span></span> <span data-ttu-id="272c5-111">Это гарантирует, что никакие другие узлы не записываются в журнал.</span><span class="sxs-lookup"><span data-stu-id="272c5-111">This ensures that no other node writes to the log.</span></span> <span data-ttu-id="272c5-112">Чтобы получить идентификатор программным путем, вызовите метод [**имфтопологиноде:: жеттопонодеид**](/windows/desktop/api/mfidl/nf-mfidl-imftopologynode-gettoponodeid).</span><span class="sxs-lookup"><span data-stu-id="272c5-112">To get the identifier programmatically, call [**IMFTopologyNode::GetTopoNodeID**](/windows/desktop/api/mfidl/nf-mfidl-imftopologynode-gettoponodeid).</span></span>

<span data-ttu-id="272c5-113">Ниже приведен фрагмент файла журнала.</span><span class="sxs-lookup"><span data-stu-id="272c5-113">The following is an excerpt from a log file.</span></span>

`GetStreamCount(02C9F518 02C9F514) returns 0`

`GetStreamIDs(1 02729720 1 02729760) returns 80004001`

`GetInputCurrentType(0 02C9F4A4) returns c00d6d60`

`GetStreamCount(02C9F518 02C9F514) returns 0`

`GetStreamIDs(1 02729760 1 02729720) returns 80004001`

`SetInputType(0 0012F8D8 0) returns 0`

`--> Arg(2, in) Media type: Audio: MAJOR_TYPE=Audio, PREFER_WAVEFORMATEX=1, SUBTYPE=WMAudioV8, NUM_CHANNELS=2, SAMPLES_PER_SECOND=48000, BLOCK_ALIGNMENT=2048, AVG_BYTES_PER_SECOND=12000, BITS_PER_SAMPLE=16, USER_DATA=<BLOB>, {9D62927D-36BE-4CF2-B5C4-A3926E3E8711}=5760, {9D62927F-36BE-4CF2-B5C4-A3926E3E8711}=674,`

`GetStreamCount(02C9F560 02C9F55C) returns 0`

`GetStreamIDs(1 02729720 1 02729640) returns 80004001`

`GetOutputCurrentType(0 02C9F4B0) returns c00d6d60`

`GetStreamCount(02C9F560 02C9F55C) returns 0`

`GetStreamIDs(1 02729640 1 02729720) returns 80004001`

`GetOutputAvailableType(0 0 02C9F4B0) returns 0`

`--> Arg(3, out) Media type: Audio: MAJOR_TYPE=Audio, PREFER_WAVEFORMATEX=1, SUBTYPE=Float, NUM_CHANNELS=2, SAMPLES_PER_SECOND=48000, BLOCK_ALIGNMENT=8, AVG_BYTES_PER_SECOND=384000, BITS_PER_SAMPLE=32, ALL_SAMPLES_INDEPENDENT=1, FIXED_SIZE_SAMPLES=1,`

`GetStreamCount(02C9F560 02C9F55C) returns 0`

`GetStreamIDs(1 02729720 1 02729640) returns 80004001`

`GetOutputAvailableType(0 1 02C9F4B0) returns 0`

## <a name="related-topics"></a><span data-ttu-id="272c5-114">См. также</span><span class="sxs-lookup"><span data-stu-id="272c5-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="272c5-115">топоедит</span><span class="sxs-lookup"><span data-stu-id="272c5-115">TopoEdit</span></span>](topoedit.md)
</dt> </dl>

 

 



