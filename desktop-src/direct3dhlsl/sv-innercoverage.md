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
ms.openlocfilehash: 172ee60cb85e69568c8cb226aa19fa325686726f42fc27c7aa21231b1a55ef28
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117724382"
---
# <a name="sv_innercoverage"></a>ОКП \_ иннерковераже

ОКП \_ инпутковераже представляет неполную оценочную информацию о растеризации (т. е. гарантируется, что точка полностью охватывается).

## <a name="type"></a>Тип



| Тип     |
|------|
| uint |



 

## <a name="remarks"></a>Remarks

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

 

 
