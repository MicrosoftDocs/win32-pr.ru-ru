---
description: Добавление выходных узлов с помощью Топоедит
ms.assetid: 23d60fc7-547b-4ef5-b334-5f1b38e58e92
title: Добавление выходных узлов с помощью Топоедит
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a84dc30631332e8138b35e4bbc0ccde75ec9b0cd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105701467"
---
# <a name="adding-output-nodes-with-topoedit"></a><span data-ttu-id="6383b-103">Добавление выходных узлов с помощью Топоедит</span><span class="sxs-lookup"><span data-stu-id="6383b-103">Adding Output Nodes with TopoEdit</span></span>

<span data-ttu-id="6383b-104">В топологии выходной узел представляет приемник мультимедиа, который получает медиа-данные из узла преобразования и представляет его для воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="6383b-104">In a topology, an output node represents a media sink that receives media data from a transform node and presents it for playback.</span></span> <span data-ttu-id="6383b-105">Тип выходного узла зависит от типа носителя исходного узла.</span><span class="sxs-lookup"><span data-stu-id="6383b-105">The type of output node depends on the media type of the source node.</span></span>

<span data-ttu-id="6383b-106">В следующей таблице показана команда меню или панели инструментов для добавления выходного узла в топологию.</span><span class="sxs-lookup"><span data-stu-id="6383b-106">The following table shows the menu/toolbar command for adding an output node to the topology.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="6383b-107">Тип исходного носителя</span><span class="sxs-lookup"><span data-stu-id="6383b-107">Source media type</span></span></th>
<th><span data-ttu-id="6383b-108">Команда меню или панели инструментов</span><span class="sxs-lookup"><span data-stu-id="6383b-108">Menu/Toolbar Command</span></span></th>
<th><span data-ttu-id="6383b-109">Описание</span><span class="sxs-lookup"><span data-stu-id="6383b-109">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="6383b-110">Аудиопоток</span><span class="sxs-lookup"><span data-stu-id="6383b-110">Audio stream</span></span></td>
<td><span data-ttu-id="6383b-111">В меню <strong>топология</strong> выберите пункт <strong>Добавить САР</strong>.</span><span class="sxs-lookup"><span data-stu-id="6383b-111">On the <strong>Topology</strong> menu, click <strong>Add SAR</strong>.</span></span></td>
<td><span data-ttu-id="6383b-112">Создает выходной узел для обработчика потоковой передачи звука (САР), который воспроизводит звуковой поток через звуковое устройство, например звуковую карту.</span><span class="sxs-lookup"><span data-stu-id="6383b-112">Creates an output node for the Streaming Audio Renderer (SAR) that plays an audio stream through an audio device such as a sound card.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6383b-113">Поток видео</span><span class="sxs-lookup"><span data-stu-id="6383b-113">Video stream</span></span></td>
<td><span data-ttu-id="6383b-114">В меню <strong>топология</strong> выберите команду <strong>Добавить Евр</strong>.</span><span class="sxs-lookup"><span data-stu-id="6383b-114">On the <strong>Topology</strong> menu, click <strong>Add EVR</strong>.</span></span></td>
<td><span data-ttu-id="6383b-115">Создает выходной узел для расширенного обработчика видео (Евр), который отображает кадры для видеопотока.</span><span class="sxs-lookup"><span data-stu-id="6383b-115">Creates an output node for the enhanced video renderer (EVR) that displays frames for a video stream.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6383b-116">Пользовательский приемник мультимедиа</span><span class="sxs-lookup"><span data-stu-id="6383b-116">Custom media sink</span></span></td>
<td><ol>
<li><span data-ttu-id="6383b-117">В меню <strong>топология</strong> выберите команду <strong>Добавить пользовательский приемник</strong>.</span><span class="sxs-lookup"><span data-stu-id="6383b-117">On the <strong>Topology</strong> menu, click <strong>Add Custom Sink</strong>.</span></span><br/> <span data-ttu-id="6383b-118">Откроется диалоговое окно <strong>Ввод ПОЛЬЗОВАТЕЛЬСКОГО GUID</strong> .</span><span class="sxs-lookup"><span data-stu-id="6383b-118">The <strong>Input Custom GUID</strong> dialog box opens.</span></span><br/></li>
<li><p><span data-ttu-id="6383b-119">В поле <strong>GUID:</strong> введите идентификатор GUID пользовательского приемника, который требуется добавить в топологию.</span><span class="sxs-lookup"><span data-stu-id="6383b-119">In the <strong>GUID:</strong> field, enter the GUID of your custom sink that you want to add to the topology.</span></span><br/></p>
<blockquote>
[!Note]<br />
<span data-ttu-id="6383b-120">Топоедит принимает идентификатор GUID в формате &quot; {XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX} &quot; .</span><span class="sxs-lookup"><span data-stu-id="6383b-120">TopoEdit expects the GUID in the format &quot;{xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx}&quot;.</span></span> <span data-ttu-id="6383b-121">В противном случае он не сможет добавить узел и выведет &quot; неверное &quot; сообщение об ошибке GUID.</span><span class="sxs-lookup"><span data-stu-id="6383b-121">Otherwise, it fails to add the node and displays an &quot;Invalid GUID&quot; error message.</span></span>
</blockquote>
<p><br/></p></li>
<li><span data-ttu-id="6383b-122">Нажмите кнопку <strong>ОК</strong>.</span><span class="sxs-lookup"><span data-stu-id="6383b-122">Click <strong>OK</strong>.</span></span><br/></li>
</ol></td>
<td><span data-ttu-id="6383b-123">Создает выходной узел для приемника потока для пользовательского источника мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="6383b-123">Creates an output node for the stream sink for a custom media source.</span></span><br/> <span data-ttu-id="6383b-124">Пользовательский приемник должен поддерживать <strong>CoCreateInstance</strong> , чтобы приемник можно было указать с помощью идентификатора CLSID.</span><span class="sxs-lookup"><span data-stu-id="6383b-124">The custom sink must support <strong>CoCreateInstance</strong> so that the sink can be specified with a CLSID.</span></span><br/></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="6383b-125">Топоедит создает указанный выходной узел.</span><span class="sxs-lookup"><span data-stu-id="6383b-125">TopoEdit creates the specified output node.</span></span> <span data-ttu-id="6383b-126">На **панели топология** отображается узел вывода в виде зеленого прямоугольника, в котором отображается имя приемника потока.</span><span class="sxs-lookup"><span data-stu-id="6383b-126">The **Topology Pane** shows the output node as a green box that shows the name of the stream sink.</span></span>

<span data-ttu-id="6383b-127">Сведения о добавлении выходных узлов программным путем с помощью Media Foundation API-интерфейсов см. в разделе [Создание выходных узлов](creating-output-nodes.md).</span><span class="sxs-lookup"><span data-stu-id="6383b-127">For information about adding output nodes programmatically by using Media Foundation APIs, see [Creating Output Nodes](creating-output-nodes.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="6383b-128">См. также</span><span class="sxs-lookup"><span data-stu-id="6383b-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6383b-129">Создание топологий с помощью Топоедит</span><span class="sxs-lookup"><span data-stu-id="6383b-129">Building Topologies by Using TopoEdit</span></span>](building-topologies-by-using-topoedit.md)
</dt> <dt>

[<span data-ttu-id="6383b-130">Потоковая прорисовка звука</span><span class="sxs-lookup"><span data-stu-id="6383b-130">Streaming Audio Renderer</span></span>](streaming-audio-renderer.md)
</dt> <dt>

[<span data-ttu-id="6383b-131">Улучшенный модуль подготовки видео</span><span class="sxs-lookup"><span data-stu-id="6383b-131">Enhanced Video Renderer</span></span>](enhanced-video-renderer.md)
</dt> <dt>

[<span data-ttu-id="6383b-132">топоедит</span><span class="sxs-lookup"><span data-stu-id="6383b-132">TopoEdit</span></span>](topoedit.md)
</dt> </dl>

 

 




