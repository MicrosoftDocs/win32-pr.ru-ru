---
description: Разрешение топологии с помощью Топоедит
ms.assetid: da3e2bbc-7c9f-4a15-8842-c1bb00662cd2
title: Разрешение топологии с помощью Топоедит
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8397e380b19a6f45736c06e859d2a80456aad079
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104263492"
---
# <a name="resolving-a-topology-with-topoedit"></a><span data-ttu-id="43a70-103">Разрешение топологии с помощью Топоедит</span><span class="sxs-lookup"><span data-stu-id="43a70-103">Resolving a Topology with TopoEdit</span></span>

<span data-ttu-id="43a70-104">Существует два типа топологий:</span><span class="sxs-lookup"><span data-stu-id="43a70-104">There are two types of topologies:</span></span>

-   <span data-ttu-id="43a70-105">Частичная топология.</span><span class="sxs-lookup"><span data-stu-id="43a70-105">Partial Topology.</span></span> <span data-ttu-id="43a70-106">Исходный узел подключен непосредственно к выходному узлу.</span><span class="sxs-lookup"><span data-stu-id="43a70-106">The source node is connected directly to the output node.</span></span> <span data-ttu-id="43a70-107">В некоторых случаях частичная топология может иметь некоторые узлы промежуточного преобразования, такие как эффекты, но не все.</span><span class="sxs-lookup"><span data-stu-id="43a70-107">In some cases, a partial topology can have some intermediate transform nodes, such as effects, but not all.</span></span> <span data-ttu-id="43a70-108">Узлы преобразования, которые опущены, обычно являются декодерами или преобразованием форматов МФТС, такими как преобразователи цветов и звуковые фильтры.</span><span class="sxs-lookup"><span data-stu-id="43a70-108">The transform nodes that are omitted are typically decoders or format conversion MFTs, such as color converters and audio resamplers.</span></span>

-   <span data-ttu-id="43a70-109">Полная топология.</span><span class="sxs-lookup"><span data-stu-id="43a70-109">Full Topology.</span></span> <span data-ttu-id="43a70-110">Исходный узел подключен к выходному узлу через узел преобразования.</span><span class="sxs-lookup"><span data-stu-id="43a70-110">The source node is connected to the output node through a transform node.</span></span> <span data-ttu-id="43a70-111">Этот тип топологии должен содержать каждый узел для обработки данных.</span><span class="sxs-lookup"><span data-stu-id="43a70-111">This type of topology must have every node to process data.</span></span>

<span data-ttu-id="43a70-112">Топоедит может играть только полные топологии.</span><span class="sxs-lookup"><span data-stu-id="43a70-112">TopoEdit can only play full topologies.</span></span> <span data-ttu-id="43a70-113">Топоедит использует объект-загрузчик топологии, предоставляемый Media Foundation, для преобразования частичной топологии в полную топологию путем вставки необходимых преобразований.</span><span class="sxs-lookup"><span data-stu-id="43a70-113">TopoEdit uses the topology loader object, provided by Media Foundation, to convert a partial topology into a full topology by inserting the required transforms.</span></span> <span data-ttu-id="43a70-114">Процесс создания полной топологии называется разрешением топологии.</span><span class="sxs-lookup"><span data-stu-id="43a70-114">The process of creating a full topology is called resolving a topology.</span></span>

<span data-ttu-id="43a70-115">Сведения о типах топологий см. в разделе "частичные топологии" статьи [о топологиях](about-topologies.md).</span><span class="sxs-lookup"><span data-stu-id="43a70-115">For information about topology types, see the Partial Topologies section in [About Topologies](about-topologies.md).</span></span>

<span data-ttu-id="43a70-116">Перед разрешением топологии убедитесь в том, что:</span><span class="sxs-lookup"><span data-stu-id="43a70-116">Before you resolve a topology ensure that:</span></span>

-   <span data-ttu-id="43a70-117">Топология содержит исходный узел и выходной узел.</span><span class="sxs-lookup"><span data-stu-id="43a70-117">The topology contains a source node and an output node.</span></span>

-   <span data-ttu-id="43a70-118">Исходный и выходной узлы соединены допустимым соединением с узлом.</span><span class="sxs-lookup"><span data-stu-id="43a70-118">The source and the output nodes are connected by a valid node connection.</span></span> <span data-ttu-id="43a70-119">Во время разрешения топологии загрузчик топологии проверяет тип носителя узлов на совместимость.</span><span class="sxs-lookup"><span data-stu-id="43a70-119">During topology resolution, the topology loader checks the media type of the nodes for compatibility.</span></span> <span data-ttu-id="43a70-120">Если соединение с недопустимым узлом существует, то процесс завершается ошибкой и выводится сообщение об ошибке.</span><span class="sxs-lookup"><span data-stu-id="43a70-120">If an invalid node connection exists, then the process fails and an error message is displayed.</span></span>

<span data-ttu-id="43a70-121">Чтобы разрешить топологию, в меню **топология** выберите пункт **Разрешить топологию**.</span><span class="sxs-lookup"><span data-stu-id="43a70-121">To resolve a topology, from the **Topology** menu, click **Resolve Topology**.</span></span>

<span data-ttu-id="43a70-122">На панели инструментов отображается состояние топологии: **\[ разрешено \]** или **\[ не \] разрешено**.</span><span class="sxs-lookup"><span data-stu-id="43a70-122">The toolbar indicates the topology status: **\[Resolved\]** or **\[Not Resolved\]**.</span></span>

<span data-ttu-id="43a70-123">Если Топоедит разрешает топологию успешно, **состояние топологии** устанавливается как **\[ разрешенное \]** , а элементы управления воспроизведением — включены.</span><span class="sxs-lookup"><span data-stu-id="43a70-123">If TopoEdit resolves a topology successfully, **Topology Status** is set to **\[Resolved\]** and the playback controls are enabled.</span></span>

<span data-ttu-id="43a70-124">Каждый раз при внесении изменений в топологию **состояние топологии** устанавливается в значение " **\[ не \] разрешено** ", что указывает на необходимость повторного разрешения.</span><span class="sxs-lookup"><span data-stu-id="43a70-124">Each time you make changes to the topology, **Topology Status** is set to **\[Not Resolved\]** which indicates that it must be resolved again.</span></span>

## <a name="related-topics"></a><span data-ttu-id="43a70-125">См. также</span><span class="sxs-lookup"><span data-stu-id="43a70-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="43a70-126">Создание топологий с помощью Топоедит</span><span class="sxs-lookup"><span data-stu-id="43a70-126">Building Topologies by Using TopoEdit</span></span>](building-topologies-by-using-topoedit.md)
</dt> <dt>

[<span data-ttu-id="43a70-127">топоедит</span><span class="sxs-lookup"><span data-stu-id="43a70-127">TopoEdit</span></span>](topoedit.md)
</dt> </dl>

 

 



