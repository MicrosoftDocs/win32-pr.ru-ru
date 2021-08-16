---
title: Плитки в буфере
description: Ресурс буфера разделен на плитки размером 64 КБ, причем в последней плитке имеется пустое пространство на случай, если размер не будет кратен 64 КБ.
ms.assetid: 979EFCF3-1FE1-412A-A19D-F1B1CF86423B
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f36352f492efb88bf220035d737b5767ef086e74ab91ffb4228d7734f838425b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117734246"
---
# <a name="buffer-tiling"></a>Плитки в буфере

Ресурс [буфера](overviews-direct3d-11-resources-buffers.md) делится на 64 КБ, при этом некоторое пустое пространство на последнем плитке, если размер не КРАТЕН 64 КБ.

Для разделения структурированных буферов на плитки буферы не должны иметь ограничений шага. Однако можно пожертвовать возможной оптимизацией производительности оборудования для использования объекта [**StructuredBuffers**](/windows/desktop/direct3dhlsl/sm5-object-structuredbuffer), если все равно разделить буферы на плитки.

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Мозаичное заполнение области мозаичного ресурса](how-a-tiled-resource-s-area-is-tiled.md)
</dt> </dl>

 

 