---
title: Структуры слоя отладки
description: Следующие структуры объявляются в d3d12sdklayers. h.
ms.assetid: FE8796A7-98D1-4333-8755-2A47567560B3
ms.localizationpriority: low
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 573d49d34c4432796ebac68ce004f265259b9eb2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "105710147"
---
# <a name="debug-layer-structures"></a><span data-ttu-id="5b775-103">Структуры слоя отладки</span><span class="sxs-lookup"><span data-stu-id="5b775-103">Debug Layer Structures</span></span>

<span data-ttu-id="5b775-104">Следующие структуры объявляются в d3d12sdklayers. h.</span><span class="sxs-lookup"><span data-stu-id="5b775-104">The following structures are declared in d3d12sdklayers.h.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="5b775-105">В этом разделе</span><span class="sxs-lookup"><span data-stu-id="5b775-105">In this section</span></span>



| <span data-ttu-id="5b775-106">Раздел</span><span class="sxs-lookup"><span data-stu-id="5b775-106">Topic</span></span>                                                                                                                                      | <span data-ttu-id="5b775-107">Описание</span><span class="sxs-lookup"><span data-stu-id="5b775-107">Description</span></span>                                                                                                                          |
|--------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="5b775-108">**\_ \_ Список команд отладки \_ D3D12 \_ \_ \_ Параметры проверки на основе GPU \_**</span><span class="sxs-lookup"><span data-stu-id="5b775-108">**D3D12\_DEBUG\_COMMAND\_LIST\_GPU\_BASED\_VALIDATION\_SETTINGS**</span></span>](/windows/desktop/api/d3d12sdklayers/ns-d3d12sdklayers-d3d12_debug_command_list_gpu_based_validation_settings)<br/> | <span data-ttu-id="5b775-109">Описывает параметры списка команд, используемые для проверки GPU-Based.</span><span class="sxs-lookup"><span data-stu-id="5b775-109">Describes per-command-list settings used by GPU-Based Validation.</span></span> <br/>                                                        |
| [<span data-ttu-id="5b775-110">**\_ \_ \_ \_ Параметры проверки на основе GPU \_ для устройства отладки D3D12 \_**</span><span class="sxs-lookup"><span data-stu-id="5b775-110">**D3D12\_DEBUG\_DEVICE\_GPU\_BASED\_VALIDATION\_SETTINGS**</span></span>](/windows/desktop/api/d3d12sdklayers/ns-d3d12sdklayers-d3d12_debug_device_gpu_based_validation_settings)<br/>              | <span data-ttu-id="5b775-111">Описание параметров, используемых при проверке GPU-Based.</span><span class="sxs-lookup"><span data-stu-id="5b775-111">Describes settings used by GPU-Based Validation.</span></span> <br/>                                                                         |
| [<span data-ttu-id="5b775-112">**\_ \_ \_ \_ \_ Коэффициент снижения производительности GPU для устройства \_ отладки D3D12**</span><span class="sxs-lookup"><span data-stu-id="5b775-112">**D3D12\_DEBUG\_DEVICE\_GPU\_SLOWDOWN\_PERFORMANCE\_FACTOR**</span></span>](/windows/desktop/api/d3d12sdklayers/ns-d3d12sdklayers-d3d12_debug_device_gpu_slowdown_performance_factor)<br/>          | <span data-ttu-id="5b775-113">Описывает объем искусственного замедления, вставленный устройством отладки для имитации низкоуровневых графических адаптеров.</span><span class="sxs-lookup"><span data-stu-id="5b775-113">Describes the amount of artificial slowdown inserted by the debug device to simulate lower-performance graphics adapters.</span></span><br/> |
| [<span data-ttu-id="5b775-114">**\_ \_ Фильтр очереди D3D12 \_ info**</span><span class="sxs-lookup"><span data-stu-id="5b775-114">**D3D12\_INFO\_QUEUE\_FILTER**</span></span>](/windows/desktop/api/d3d12sdklayers/ns-d3d12sdklayers-d3d12_info_queue_filter)<br/>                                                                   | <span data-ttu-id="5b775-115">Фильтр сообщений отладки; содержит списки типов сообщений для разрешения или запрета.</span><span class="sxs-lookup"><span data-stu-id="5b775-115">Debug message filter; contains a lists of message types to allow or deny.</span></span><br/>                                                 |
| [<span data-ttu-id="5b775-116">**D3D12 \_ сведений \_ о \_ фильтре очереди \_**</span><span class="sxs-lookup"><span data-stu-id="5b775-116">**D3D12\_INFO\_QUEUE\_FILTER\_DESC**</span></span>](/windows/desktop/api/d3d12sdklayers/ns-d3d12sdklayers-d3d12_info_queue_filter_desc)<br/>                                                        | <span data-ttu-id="5b775-117">Разрешает или запрещает передачу определенных типов сообщений через фильтр.</span><span class="sxs-lookup"><span data-stu-id="5b775-117">Allow or deny certain types of messages to pass through a filter.</span></span><br/>                                                         |
| [<span data-ttu-id="5b775-118">**\_Сообщение D3D12**</span><span class="sxs-lookup"><span data-stu-id="5b775-118">**D3D12\_MESSAGE**</span></span>](/windows/desktop/api/d3d12sdklayers/ns-d3d12sdklayers-d3d12_message)<br/>                                                                                         | <span data-ttu-id="5b775-119">Сообщение отладки в информационной очереди.</span><span class="sxs-lookup"><span data-stu-id="5b775-119">A debug message in the Information Queue.</span></span><br/>                                                                                 |



 

## <a name="related-topics"></a><span data-ttu-id="5b775-120">См. также</span><span class="sxs-lookup"><span data-stu-id="5b775-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5b775-121">Настройка среды программирования для Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="5b775-121">Direct3D 12 Programming Environment Setup</span></span>](directx-12-programming-environment-set-up.md)
</dt> <dt>

[<span data-ttu-id="5b775-122">Справочник по слою отладки</span><span class="sxs-lookup"><span data-stu-id="5b775-122">Debug Layer Reference</span></span>](direct3d-12-sdklayers-reference.md)
</dt> <dt>

[<span data-ttu-id="5b775-123">Справочник по Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="5b775-123">Direct3D 12 Reference</span></span>](direct3d-12-reference.md)
</dt> </dl>

 

 





