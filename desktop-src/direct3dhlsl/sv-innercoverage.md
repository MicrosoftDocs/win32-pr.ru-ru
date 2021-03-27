---
title: SV_InnerCoverage
description: ОКП \_ инпутковераже представляет неполную оценочную информацию о растеризации (т. е. гарантируется, что точка полностью охватывается).
ms.assetid: 5BB3C3FB-E5ED-4395-B389-300DE67C984B
keywords:
- SV_InnerCoverage HLSL
topic_type:
- apiref
api_name:
- SV_InnerCoverage
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a2f1393a6a11a95c8c08746f57083fe193791a60
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104997142"
---
# <a name="sv_innercoverage"></a>ОКП \_ иннерковераже

ОКП \_ инпутковераже представляет неполную оценочную информацию о растеризации (т. е. гарантируется, что точка полностью охватывается).

## <a name="type"></a>Тип



|      |
|------|
| Тип |
| uint |



 

## <a name="remarks"></a>Примечания

Это значение, созданное системой, является обязательным для поддержки уровня 3 и доступно только на этом уровне. Эти входные данные являются взаимоисключающими с покрытием "ОКП" \_ . они не могут использоваться одновременно.

Чтобы получить доступ к SV \_ иннерковераже, он должен быть объявлен как отдельный компонент из одного из входных регистров шейдера пикселей. Режим интерполяции в объявлении должен быть константой (интерполяция не применяется).

Консервативная растрирование доступна как в D3D 11.3, так и в D3D12. Перейдите к

-   [11.3а в D3D, консервативная растрирование](/windows/desktop/direct3d11/conservative-rasterization)
-   [D3D12 консервативная растрирование](/windows/desktop/direct3d12/conservative-rasterization)

## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Модель шейдера 5](d3d11-graphics-reference-sm5.md)
</dt> <dt>

[Системные значения модели шейдеров 5,1](shader-model-5-1-system-values.md)
</dt> </dl>

 

 