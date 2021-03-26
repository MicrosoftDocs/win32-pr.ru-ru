---
title: Плитки в буфере
description: Ресурс буфера разделен на плитки размером 64 КБ, причем в последней плитке имеется пустое пространство на случай, если размер не будет кратен 64 КБ.
ms.assetid: 979EFCF3-1FE1-412A-A19D-F1B1CF86423B
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 061fafa009e554499822c90c8fb6c0c8f34e47f9
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "103890708"
---
# <a name="buffer-tiling"></a>Плитки в буфере

Ресурс [буфера](overviews-direct3d-11-resources-buffers.md) делится на 64 КБ, при этом некоторое пустое пространство на последнем плитке, если размер не КРАТЕН 64 КБ.

Для разделения структурированных буферов на плитки буферы не должны иметь ограничений шага. Однако можно пожертвовать возможной оптимизацией производительности оборудования для использования объекта [**StructuredBuffers**](/windows/desktop/direct3dhlsl/sm5-object-structuredbuffer), если все равно разделить буферы на плитки.

## <a name="related-topics"></a>См. также

<dl> <dt>

[Мозаичное заполнение области мозаичного ресурса](how-a-tiled-resource-s-area-is-tiled.md)
</dt> </dl>

 

 