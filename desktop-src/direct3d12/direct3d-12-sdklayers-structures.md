---
title: Структуры слоя отладки
description: Следующие структуры объявляются в d3d12sdklayers. h.
ms.assetid: FE8796A7-98D1-4333-8755-2A47567560B3
ms.localizationpriority: low
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a14bc7ab299c9f01979be1bb7f0ca446e64ba8b482215920b075be96da91807c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118529754"
---
# <a name="debug-layer-structures"></a>Структуры слоя отладки

Следующие структуры объявляются в d3d12sdklayers. h.

## <a name="in-this-section"></a>В этом разделе



| Раздел                                                                                                                                      | Описание                                                                                                                          |
|--------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------|
| [**\_ \_ Список команд отладки \_ D3D12 \_ \_ \_ Параметры проверки на основе GPU \_**](/windows/desktop/api/d3d12sdklayers/ns-d3d12sdklayers-d3d12_debug_command_list_gpu_based_validation_settings)<br/> | Описывает параметры списка команд, используемые для проверки GPU-Based. <br/>                                                        |
| [**\_ \_ \_ \_ Параметры проверки на основе GPU \_ для устройства отладки D3D12 \_**](/windows/desktop/api/d3d12sdklayers/ns-d3d12sdklayers-d3d12_debug_device_gpu_based_validation_settings)<br/>              | Описание параметров, используемых при проверке GPU-Based. <br/>                                                                         |
| [**\_ \_ \_ \_ \_ Коэффициент снижения производительности GPU для устройства \_ отладки D3D12**](/windows/desktop/api/d3d12sdklayers/ns-d3d12sdklayers-d3d12_debug_device_gpu_slowdown_performance_factor)<br/>          | Описывает объем искусственного замедления, вставленный устройством отладки для имитации низкоуровневых графических адаптеров.<br/> |
| [**\_ \_ Фильтр очереди D3D12 \_ info**](/windows/desktop/api/d3d12sdklayers/ns-d3d12sdklayers-d3d12_info_queue_filter)<br/>                                                                   | Фильтр сообщений отладки; содержит списки типов сообщений для разрешения или запрета.<br/>                                                 |
| [**D3D12 \_ сведений \_ о \_ фильтре очереди \_**](/windows/desktop/api/d3d12sdklayers/ns-d3d12sdklayers-d3d12_info_queue_filter_desc)<br/>                                                        | Разрешает или запрещает передачу определенных типов сообщений через фильтр.<br/>                                                         |
| [**\_Сообщение D3D12**](/windows/desktop/api/d3d12sdklayers/ns-d3d12sdklayers-d3d12_message)<br/>                                                                                         | Сообщение отладки в информационной очереди.<br/>                                                                                 |



 

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Настройка среды программирования для Direct3D 12](directx-12-programming-environment-set-up.md)
</dt> <dt>

[Справочник по слою отладки](direct3d-12-sdklayers-reference.md)
</dt> <dt>

[Справочник по Direct3D 12](direct3d-12-reference.md)
</dt> </dl>

 

 





