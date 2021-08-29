---
title: Перечисления слоев
description: В этом разделе содержатся сведения о перечислении слоев.
ms.assetid: 0fd0456b-2638-4b4c-8a34-a3e104a1a034
keywords:
- перечисления, уровень Direct3D 11
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1af59a6ac6fae73cafdbee3f0d93d019d7a8ee0b472cd979e2ddcaeade387ef4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119460903"
---
# <a name="layer-enumerations"></a>Перечисления слоев

В этом разделе содержатся сведения о перечислении слоев.


## <a name="in-this-section"></a>В этом разделе



| Раздел                                                                                             | Описание                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
|---------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_Категория сообщений \_ D3D11**](/windows/desktop/api/D3D11SDKLayers/ne-d3d11sdklayers-d3d11_message_category)<br/>                             | Категории отладочных сообщений. При этом будет определена категория сообщения при получении сообщения с помощью [**ID3D11InfoQueue::-Message**](/windows/desktop/api/D3D11SDKLayers/nf-d3d11sdklayers-id3d11infoqueue-getmessage) и при добавлении сообщения с [**ID3D11InfoQueue:: AddMessage**](/windows/desktop/api/D3D11SDKLayers/nf-d3d11sdklayers-id3d11infoqueue-addmessage). При создании [**фильтра очереди сведений**](/windows/desktop/api/D3D11SDKLayers/ns-d3d11sdklayers-d3d11_info_queue_filter)эти значения можно использовать, чтобы разрешить или запретить всем категориям сообщений проходить через фильтры хранения и извлечения.<br/> |
| [**\_Идентификатор сообщения \_ D3D11**](/windows/desktop/api/D3D11SDKLayers/ne-d3d11sdklayers-d3d11_message_id)<br/>                                         | Сообщения отладки для настройки фильтра очереди сведений (см. раздел [**\_ \_ \_ Фильтр очереди D3D11 info**](/windows/desktop/api/D3D11SDKLayers/ns-d3d11sdklayers-d3d11_info_queue_filter)); Используйте эти сообщения, чтобы разрешить или запретить категориям сообщений проходить через фильтры хранилища и извлечения. Эти идентификаторы используются такими методами, как [**ID3D11InfoQueue:: onmessage**](/windows/desktop/api/D3D11SDKLayers/nf-d3d11sdklayers-id3d11infoqueue-getmessage) или [**ID3D11InfoQueue:: AddMessage**](/windows/desktop/api/D3D11SDKLayers/nf-d3d11sdklayers-id3d11infoqueue-addmessage). <br/>                                                             |
| [**\_ \_ Серьезность сообщения D3D11**](/windows/desktop/api/D3D11SDKLayers/ne-d3d11sdklayers-d3d11_message_severity)<br/>                             | Уровни серьезности отладочного сообщения для информационной очереди.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                      |
| [**\_ \_ Флаги рлдо D3D11**](/windows/desktop/api/D3D11SDKLayers/ne-d3d11sdklayers-d3d11_rldo_flags)<br/>                                         | Параметры для объема сведений, которые необходимо сообщить о времени существования объекта устройства.<br/>                                                                                                                                                                                                                                                                                                                                                                                            |
| [**\_Параметры отслеживания шейдера D3D11 \_ \_**](/windows/win32/api/d3d11sdklayers/ne-d3d11sdklayers-d3d11_shader_tracking_options)<br/>              | Параметры, определяющие способ выполнения отслеживания отладки шейдером.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                   |
| [**\_ \_ \_ Тип ресурса отслеживания шейдера \_ D3D11**](/windows/desktop/api/D3D11SDKLayers/ne-d3d11sdklayers-d3d11_shader_tracking_resource_type)<br/> | Указывает, какие типы ресурсов следует отслеживанию.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                     |



 

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Ссылка на слой](d3d11-graphics-reference-d3d11-layer.md)
</dt> </dl>

 

 





