---
title: Интерфейсы слоя
description: В этом разделе содержатся сведения о интерфейсах слоя.
ms.assetid: 100cb66a-9bf5-4d0b-9f03-ad7c00e76d9d
keywords:
- интерфейсы, уровень Direct3D 11
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a57945866e8dea1b04c4066362105c8ac6e259a5
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/04/2020
ms.locfileid: "104997186"
---
# <a name="layer-interfaces"></a><span data-ttu-id="bbcb8-104">Интерфейсы слоя</span><span class="sxs-lookup"><span data-stu-id="bbcb8-104">Layer Interfaces</span></span>

<span data-ttu-id="bbcb8-105">В этом разделе содержатся сведения о интерфейсах слоя.</span><span class="sxs-lookup"><span data-stu-id="bbcb8-105">This section contains information about the layer interfaces.</span></span>


## <a name="in-this-section"></a><span data-ttu-id="bbcb8-106">В этом разделе</span><span class="sxs-lookup"><span data-stu-id="bbcb8-106">In this section</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="bbcb8-107">Раздел</span><span class="sxs-lookup"><span data-stu-id="bbcb8-107">Topic</span></span></th>
<th><span data-ttu-id="bbcb8-108">Описание</span><span class="sxs-lookup"><span data-stu-id="bbcb8-108">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="bbcb8-109"><a href="/windows/desktop/api/D3D11SDKLayers/nn-d3d11sdklayers-id3d11debug"><strong>ID3D11Debug</strong></a></span><span class="sxs-lookup"><span data-stu-id="bbcb8-109"><a href="/windows/desktop/api/D3D11SDKLayers/nn-d3d11sdklayers-id3d11debug"><strong>ID3D11Debug</strong></a></span></span><br/></td>
<td><span data-ttu-id="bbcb8-110">Интерфейс отладки управляет параметрами отладки, проверяет состояние конвейера и может использоваться только в том случае, если включен слой отладки.</span><span class="sxs-lookup"><span data-stu-id="bbcb8-110">A debug interface controls debug settings, validates pipeline state and can only be used if the debug layer is turned on.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="bbcb8-111"><a href="/windows/desktop/api/D3D11SDKLayers/nn-d3d11sdklayers-id3d11infoqueue"><strong>ID3D11InfoQueue</strong></a></span><span class="sxs-lookup"><span data-stu-id="bbcb8-111"><a href="/windows/desktop/api/D3D11SDKLayers/nn-d3d11sdklayers-id3d11infoqueue"><strong>ID3D11InfoQueue</strong></a></span></span><br/></td>
<td><span data-ttu-id="bbcb8-112">Интерфейс очереди информации хранит, извлекает и фильтрует сообщения отладки.</span><span class="sxs-lookup"><span data-stu-id="bbcb8-112">An information-queue interface stores, retrieves, and filters debug messages.</span></span> <span data-ttu-id="bbcb8-113">Очередь состоит из очереди сообщений, дополнительного стека фильтра хранилища и дополнительного стека фильтров получения.</span><span class="sxs-lookup"><span data-stu-id="bbcb8-113">The queue consists of a message queue, an optional storage filter stack, and a optional retrieval filter stack.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="bbcb8-114"><a href="/windows/desktop/api/D3D11SDKLayers/nn-d3d11sdklayers-id3d11refdefaulttrackingoptions"><strong>ID3D11RefDefaultTrackingOptions</strong></a></span><span class="sxs-lookup"><span data-stu-id="bbcb8-114"><a href="/windows/desktop/api/D3D11SDKLayers/nn-d3d11sdklayers-id3d11refdefaulttrackingoptions"><strong>ID3D11RefDefaultTrackingOptions</strong></a></span></span><br/></td>
<td><span data-ttu-id="bbcb8-115">Интерфейс отслеживания по умолчанию устанавливает ссылочные параметры отслеживания по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="bbcb8-115">The default tracking interface sets reference default tracking options.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="bbcb8-116"><a href="/windows/desktop/api/D3D11SDKLayers/nn-d3d11sdklayers-id3d11reftrackingoptions"><strong>ID3D11RefTrackingOptions</strong></a></span><span class="sxs-lookup"><span data-stu-id="bbcb8-116"><a href="/windows/desktop/api/D3D11SDKLayers/nn-d3d11sdklayers-id3d11reftrackingoptions"><strong>ID3D11RefTrackingOptions</strong></a></span></span><br/></td>
<td><span data-ttu-id="bbcb8-117">Интерфейс отслеживания задает параметры отслеживания ссылок.</span><span class="sxs-lookup"><span data-stu-id="bbcb8-117">The tracking interface sets reference tracking options.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="bbcb8-118"><a href="/windows/desktop/api/D3D11SDKLayers/nn-d3d11sdklayers-id3d11switchtoref"><strong>ID3D11SwitchToRef</strong></a></span><span class="sxs-lookup"><span data-stu-id="bbcb8-118"><a href="/windows/desktop/api/D3D11SDKLayers/nn-d3d11sdklayers-id3d11switchtoref"><strong>ID3D11SwitchToRef</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="bbcb8-119">Интерфейс <a href="/windows/desktop/api/D3D11SDKLayers/nn-d3d11sdklayers-id3d11switchtoref"><strong>ID3D11SwitchToRef</strong></a> и его методы не поддерживаются в Direct3D 11.</span><span class="sxs-lookup"><span data-stu-id="bbcb8-119">The <a href="/windows/desktop/api/D3D11SDKLayers/nn-d3d11sdklayers-id3d11switchtoref"><strong>ID3D11SwitchToRef</strong></a> interface and its methods are not supported in Direct3D 11.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="bbcb8-120"><a href="/windows/desktop/api/D3D11SDKLayers/nn-d3d11sdklayers-id3d11tracingdevice"><strong>ID3D11TracingDevice</strong></a></span><span class="sxs-lookup"><span data-stu-id="bbcb8-120"><a href="/windows/desktop/api/D3D11SDKLayers/nn-d3d11sdklayers-id3d11tracingdevice"><strong>ID3D11TracingDevice</strong></a></span></span><br/></td>
<td><span data-ttu-id="bbcb8-121">В интерфейсе устройства трассировки устанавливаются данные отслеживания шейдеров, что обеспечивает точное ведение журнала и воспроизведение выполнения шейдера.</span><span class="sxs-lookup"><span data-stu-id="bbcb8-121">The tracing device interface sets shader tracking information, which enables accurate logging and playback of shader execution.</span></span><br/></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a><span data-ttu-id="bbcb8-122">См. также</span><span class="sxs-lookup"><span data-stu-id="bbcb8-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bbcb8-123">Ссылка на слой</span><span class="sxs-lookup"><span data-stu-id="bbcb8-123">Layer Reference</span></span>](d3d11-graphics-reference-d3d11-layer.md)
</dt> </dl>

 

 





