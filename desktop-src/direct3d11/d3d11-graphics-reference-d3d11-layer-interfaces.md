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
# <a name="layer-interfaces"></a>Интерфейсы слоя

В этом разделе содержатся сведения о интерфейсах слоя.


## <a name="in-this-section"></a>В этом разделе



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Раздел</th>
<th>Описание</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="/windows/desktop/api/D3D11SDKLayers/nn-d3d11sdklayers-id3d11debug"><strong>ID3D11Debug</strong></a><br/></td>
<td>Интерфейс отладки управляет параметрами отладки, проверяет состояние конвейера и может использоваться только в том случае, если включен слой отладки.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/D3D11SDKLayers/nn-d3d11sdklayers-id3d11infoqueue"><strong>ID3D11InfoQueue</strong></a><br/></td>
<td>Интерфейс очереди информации хранит, извлекает и фильтрует сообщения отладки. Очередь состоит из очереди сообщений, дополнительного стека фильтра хранилища и дополнительного стека фильтров получения.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/D3D11SDKLayers/nn-d3d11sdklayers-id3d11refdefaulttrackingoptions"><strong>ID3D11RefDefaultTrackingOptions</strong></a><br/></td>
<td>Интерфейс отслеживания по умолчанию устанавливает ссылочные параметры отслеживания по умолчанию.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/D3D11SDKLayers/nn-d3d11sdklayers-id3d11reftrackingoptions"><strong>ID3D11RefTrackingOptions</strong></a><br/></td>
<td>Интерфейс отслеживания задает параметры отслеживания ссылок.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/D3D11SDKLayers/nn-d3d11sdklayers-id3d11switchtoref"><strong>ID3D11SwitchToRef</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Интерфейс <a href="/windows/desktop/api/D3D11SDKLayers/nn-d3d11sdklayers-id3d11switchtoref"><strong>ID3D11SwitchToRef</strong></a> и его методы не поддерживаются в Direct3D 11.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/D3D11SDKLayers/nn-d3d11sdklayers-id3d11tracingdevice"><strong>ID3D11TracingDevice</strong></a><br/></td>
<td>В интерфейсе устройства трассировки устанавливаются данные отслеживания шейдеров, что обеспечивает точное ведение журнала и воспроизведение выполнения шейдера.<br/></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a>См. также

<dl> <dt>

[Ссылка на слой](d3d11-graphics-reference-d3d11-layer.md)
</dt> </dl>

 

 





