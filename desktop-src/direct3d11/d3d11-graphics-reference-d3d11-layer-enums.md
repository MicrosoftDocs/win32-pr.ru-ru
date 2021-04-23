---
title: Перечисления слоев
description: В этом разделе содержатся сведения о перечислении слоев.
ms.assetid: 0fd0456b-2638-4b4c-8a34-a3e104a1a034
keywords:
- перечисления, уровень Direct3D 11
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e1e1cca3fa500a529930c8d0c39005697045d18b
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/04/2020
ms.locfileid: "104984120"
---
# <a name="layer-enumerations"></a><span data-ttu-id="45817-104">Перечисления слоев</span><span class="sxs-lookup"><span data-stu-id="45817-104">Layer Enumerations</span></span>

<span data-ttu-id="45817-105">В этом разделе содержатся сведения о перечислении слоев.</span><span class="sxs-lookup"><span data-stu-id="45817-105">This section contains information about the layer enumerations.</span></span>


## <a name="in-this-section"></a><span data-ttu-id="45817-106">В этом разделе</span><span class="sxs-lookup"><span data-stu-id="45817-106">In this section</span></span>



| <span data-ttu-id="45817-107">Раздел</span><span class="sxs-lookup"><span data-stu-id="45817-107">Topic</span></span>                                                                                             | <span data-ttu-id="45817-108">Описание</span><span class="sxs-lookup"><span data-stu-id="45817-108">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
|---------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="45817-109">**\_Категория сообщений \_ D3D11**</span><span class="sxs-lookup"><span data-stu-id="45817-109">**D3D11\_MESSAGE\_CATEGORY**</span></span>](/windows/desktop/api/D3D11SDKLayers/ne-d3d11sdklayers-d3d11_message_category)<br/>                             | <span data-ttu-id="45817-110">Категории отладочных сообщений.</span><span class="sxs-lookup"><span data-stu-id="45817-110">Categories of debug messages.</span></span> <span data-ttu-id="45817-111">При этом будет определена категория сообщения при получении сообщения с помощью [**ID3D11InfoQueue::-Message**](/windows/desktop/api/D3D11SDKLayers/nf-d3d11sdklayers-id3d11infoqueue-getmessage) и при добавлении сообщения с [**ID3D11InfoQueue:: AddMessage**](/windows/desktop/api/D3D11SDKLayers/nf-d3d11sdklayers-id3d11infoqueue-addmessage).</span><span class="sxs-lookup"><span data-stu-id="45817-111">This will identify the category of a message when retrieving a message with [**ID3D11InfoQueue::GetMessage**](/windows/desktop/api/D3D11SDKLayers/nf-d3d11sdklayers-id3d11infoqueue-getmessage) and when adding a message with [**ID3D11InfoQueue::AddMessage**](/windows/desktop/api/D3D11SDKLayers/nf-d3d11sdklayers-id3d11infoqueue-addmessage).</span></span> <span data-ttu-id="45817-112">При создании [**фильтра очереди сведений**](/windows/desktop/api/D3D11SDKLayers/ns-d3d11sdklayers-d3d11_info_queue_filter)эти значения можно использовать, чтобы разрешить или запретить всем категориям сообщений проходить через фильтры хранения и извлечения.</span><span class="sxs-lookup"><span data-stu-id="45817-112">When creating an [**info queue filter**](/windows/desktop/api/D3D11SDKLayers/ns-d3d11sdklayers-d3d11_info_queue_filter), these values can be used to allow or deny any categories of messages to pass through the storage and retrieval filters.</span></span><br/> |
| [<span data-ttu-id="45817-113">**\_Идентификатор сообщения \_ D3D11**</span><span class="sxs-lookup"><span data-stu-id="45817-113">**D3D11\_MESSAGE\_ID**</span></span>](/windows/desktop/api/D3D11SDKLayers/ne-d3d11sdklayers-d3d11_message_id)<br/>                                         | <span data-ttu-id="45817-114">Сообщения отладки для настройки фильтра очереди сведений (см. раздел [**\_ \_ \_ Фильтр очереди D3D11 info**](/windows/desktop/api/D3D11SDKLayers/ns-d3d11sdklayers-d3d11_info_queue_filter)); Используйте эти сообщения, чтобы разрешить или запретить категориям сообщений проходить через фильтры хранилища и извлечения.</span><span class="sxs-lookup"><span data-stu-id="45817-114">Debug messages for setting up an info-queue filter (see [**D3D11\_INFO\_QUEUE\_FILTER**](/windows/desktop/api/D3D11SDKLayers/ns-d3d11sdklayers-d3d11_info_queue_filter)); use these messages to allow or deny message categories to pass through the storage and retrieval filters.</span></span> <span data-ttu-id="45817-115">Эти идентификаторы используются такими методами, как [**ID3D11InfoQueue:: onmessage**](/windows/desktop/api/D3D11SDKLayers/nf-d3d11sdklayers-id3d11infoqueue-getmessage) или [**ID3D11InfoQueue:: AddMessage**](/windows/desktop/api/D3D11SDKLayers/nf-d3d11sdklayers-id3d11infoqueue-addmessage).</span><span class="sxs-lookup"><span data-stu-id="45817-115">These IDs are used by methods such as [**ID3D11InfoQueue::GetMessage**](/windows/desktop/api/D3D11SDKLayers/nf-d3d11sdklayers-id3d11infoqueue-getmessage) or [**ID3D11InfoQueue::AddMessage**](/windows/desktop/api/D3D11SDKLayers/nf-d3d11sdklayers-id3d11infoqueue-addmessage).</span></span> <br/>                                                             |
| [<span data-ttu-id="45817-116">**\_ \_ Серьезность сообщения D3D11**</span><span class="sxs-lookup"><span data-stu-id="45817-116">**D3D11\_MESSAGE\_SEVERITY**</span></span>](/windows/desktop/api/D3D11SDKLayers/ne-d3d11sdklayers-d3d11_message_severity)<br/>                             | <span data-ttu-id="45817-117">Уровни серьезности отладочного сообщения для информационной очереди.</span><span class="sxs-lookup"><span data-stu-id="45817-117">Debug message severity levels for an information queue.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                      |
| [<span data-ttu-id="45817-118">**\_ \_ Флаги рлдо D3D11**</span><span class="sxs-lookup"><span data-stu-id="45817-118">**D3D11\_RLDO\_FLAGS**</span></span>](/windows/desktop/api/D3D11SDKLayers/ne-d3d11sdklayers-d3d11_rldo_flags)<br/>                                         | <span data-ttu-id="45817-119">Параметры для объема сведений, которые необходимо сообщить о времени существования объекта устройства.</span><span class="sxs-lookup"><span data-stu-id="45817-119">Options for the amount of information to report about a device object's lifetime.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                            |
| [<span data-ttu-id="45817-120">**\_Параметры отслеживания шейдера D3D11 \_ \_**</span><span class="sxs-lookup"><span data-stu-id="45817-120">**D3D11\_SHADER\_TRACKING\_OPTIONS**</span></span>](/windows/win32/api/d3d11sdklayers/ne-d3d11sdklayers-d3d11_shader_tracking_options)<br/>              | <span data-ttu-id="45817-121">Параметры, определяющие способ выполнения отслеживания отладки шейдером.</span><span class="sxs-lookup"><span data-stu-id="45817-121">Options that specify how to perform shader debug tracking.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                   |
| [<span data-ttu-id="45817-122">**\_ \_ \_ Тип ресурса отслеживания шейдера \_ D3D11**</span><span class="sxs-lookup"><span data-stu-id="45817-122">**D3D11\_SHADER\_TRACKING\_RESOURCE\_TYPE**</span></span>](/windows/desktop/api/D3D11SDKLayers/ne-d3d11sdklayers-d3d11_shader_tracking_resource_type)<br/> | <span data-ttu-id="45817-123">Указывает, какие типы ресурсов следует отслеживанию.</span><span class="sxs-lookup"><span data-stu-id="45817-123">Indicates which resource types to track.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                     |



 

## <a name="related-topics"></a><span data-ttu-id="45817-124">См. также</span><span class="sxs-lookup"><span data-stu-id="45817-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="45817-125">Ссылка на слой</span><span class="sxs-lookup"><span data-stu-id="45817-125">Layer Reference</span></span>](d3d11-graphics-reference-d3d11-layer.md)
</dt> </dl>

 

 





