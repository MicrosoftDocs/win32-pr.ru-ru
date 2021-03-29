---
title: Перечисление слоев отладки
description: Следующие перечисления объявляются в d3d12sdklayers. h.
ms.assetid: 6E76C857-128E-4F0E-9711-72C4CF6C835C
ms.localizationpriority: low
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 746c0def35c8eb282264cb4ab0b40eb5c08f0f9a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "105650292"
---
# <a name="debug-layer-enumerations"></a>Перечисление слоев отладки

Следующие перечисления объявляются в d3d12sdklayers. h.

## <a name="in-this-section"></a>В этом разделе



| Раздел                                                                                                                                      | Описание                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
|--------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_ \_ \_ \_ Тип параметра списка команд отладки \_ D3D12**](/windows/desktop/api/d3d12sdklayers/ne-d3d12sdklayers-d3d12_debug_command_list_parameter_type)<br/>                                 | Указывает тип параметра отладки, используемый [**ID3D12DebugCommandList1:: сетдебугпараметер**](/windows/desktop/api/d3d12sdklayers/nf-d3d12sdklayers-id3d12debugcommandlist1-setdebugparameter) и [**ID3D12DebugCommandList1:: жетдебугпараметер**](/windows/desktop/api/d3d12sdklayers/nf-d3d12sdklayers-id3d12debugcommandlist1-getdebugparameter).<br/>                                                                                                                                                                                                      |
| [**\_ \_ \_ Тип параметра устройства отладки \_ D3D12**](/windows/desktop/api/d3d12sdklayers/ne-d3d12sdklayers-d3d12_debug_device_parameter_type)<br/>                                              | Указывает тип данных памяти, на который указывает параметр *pData* для [**ID3D12DebugDevice1:: сетдебугпараметер**](/windows/desktop/api/d3d12sdklayers/nf-d3d12sdklayers-id3d12debugdevice1-setdebugparameter) и [**ID3D12DebugDevice1:: жетдебугпараметер**](/windows/desktop/api/d3d12sdklayers/nf-d3d12sdklayers-id3d12debugdevice1-getdebugparameter).<br/>                                                                                                                                                                                        |
| [**\_Функция отладки \_ D3D12**](/windows/desktop/api/d3d12sdklayers/ne-d3d12sdklayers-d3d12_debug_feature)<br/>                                                                            | Флаги для необязательных функций отладочного слоя D3D12.<br/>                                                                                                                                                                                                                                                                                                                                                                                                       |
| [**\_ \_ \_ Флаги проверки на основе GPU \_ D3D12**](/windows/desktop/api/d3d12sdklayers/ne-d3d12sdklayers-d3d12_gpu_based_validation_flags)<br/>                                                | Описывает уровень проверки на основе GPU для выполнения во время выполнения.<br/>                                                                                                                                                                                                                                                                                                                                                                                   |
| [**\_ \_ \_ \_ \_ \_ Флаги создания состояния КОНВЕЙЕРа проверки на основе GPU \_ D3D12**](/windows/desktop/api/d3d12sdklayers/ne-d3d12sdklayers-d3d12_gpu_based_validation_pipeline_state_create_flags)<br/> | Указывает, каким образом GPU-Basedная проверка обрабатывает состояния, исправленные конвейером, во время [**ID3D12Device:: креатеграфикспипелинестате**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-creategraphicspipelinestate) и [**ID3D12Device:: креатекомпутепипелинестате**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createcomputepipelinestate).<br/>                                                                                                                                                                             |
| [**\_ \_ \_ \_ Режим исправления шейдера проверки подлинности D3D12 на основе GPU \_ \_**](/windows/desktop/api/d3d12sdklayers/ne-d3d12sdklayers-d3d12_gpu_based_validation_shader_patch_mode)<br/>                      | Указывает тип исправлений шейдера, используемый проверкой GPU-Based на уровне устройства или списка команд.<br/>                                                                                                                                                                                                                                                                                                                                       |
| [**\_Категория сообщений \_ D3D12**](/windows/desktop/api/d3d12sdklayers/ne-d3d12sdklayers-d3d12_message_category)<br/>                                                                      | Указывает категории сообщений отладки. При этом будет определена категория сообщения при получении сообщения с помощью [**ID3D12InfoQueue::-Message**](/windows/desktop/api/d3d12sdklayers/nf-d3d12sdklayers-id3d12infoqueue-getmessage) и при добавлении сообщения с [**ID3D12InfoQueue:: AddMessage**](/windows/desktop/api/d3d12sdklayers/nf-d3d12sdklayers-id3d12infoqueue-addmessage). При создании фильтра очереди сведений эти значения можно использовать, чтобы разрешить или запретить всем категориям сообщений проходить через фильтры хранения и извлечения. <br/> |
| [**\_Идентификатор сообщения \_ D3D12**](/windows/desktop/api/d3d12sdklayers/ne-d3d12sdklayers-d3d12_message_id)<br/>                                                                                  | Указывает идентификаторы сообщений отладки для настройки фильтра очереди сведений (см. раздел [**\_ \_ \_ Фильтр очереди D3D12 info**](/windows/desktop/api/d3d12sdklayers/ns-d3d12sdklayers-d3d12_info_queue_filter)); Используйте эти сообщения, чтобы разрешить или запретить всем категориям сообщений проходить через фильтры хранилища и извлечения. Эти идентификаторы используются такими методами, как [**ID3D12InfoQueue:: onmessage**](/windows/desktop/api/d3d12sdklayers/nf-d3d12sdklayers-id3d12infoqueue-getmessage) или [**ID3D12InfoQueue:: AddMessage**](/windows/desktop/api/d3d12sdklayers/nf-d3d12sdklayers-id3d12infoqueue-addmessage). <br/>                        |
| [**\_ \_ Серьезность сообщения D3D12**](/windows/desktop/api/d3d12sdklayers/ne-d3d12sdklayers-d3d12_message_severity)<br/>                                                                      | Уровни серьезности отладочного сообщения для информационной очереди.<br/>                                                                                                                                                                                                                                                                                                                                                                                              |
| [**\_ \_ Флаги рлдо D3D12**](/windows/desktop/api/d3d12sdklayers/ne-d3d12sdklayers-d3d12_rldo_flags)<br/>                                                                                  | Задает параметры, определяющие объем сведений о времени существования объекта устройства в реальном времени. <br/>                                                                                                                                                                                                                                                                                                                                                    |



 

## <a name="related-topics"></a>См. также

<dl> <dt>

[Настройка среды программирования для Direct3D 12](directx-12-programming-environment-set-up.md)
</dt> <dt>

[Справочник по слою отладки](direct3d-12-sdklayers-reference.md)
</dt> <dt>

[Справочник по Direct3D 12](direct3d-12-reference.md)
</dt> </dl>

 

 





