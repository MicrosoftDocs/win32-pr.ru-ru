---
description: Эти флаги используются для управления тем, как D3DX10ComputeNormalMap создает нормальные карты. Любое число этих флагов может быть или в любом сочетании.
ms.assetid: 307936c1-3137-41fe-8bea-7a82e6db0867
title: Перечисление D3DX10_NORMALMAP_FLAG (D3DX10Tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10_NORMALMAP_FLAG
api_type:
- HeaderDef
api_location:
- D3DX10Tex.h
ms.openlocfilehash: c4b6962561007fbc3e64b471c045e98b2f8328b4
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105720918"
---
# <a name="d3dx10_normalmap_flag-enumeration"></a>\_ \_ Перечисление флагов нормалмап D3DX10

Эти флаги используются для управления тем, как [**D3DX10ComputeNormalMap**](d3dx10computenormalmap.md) создает нормальные карты. Любое число этих флагов может быть или в любом сочетании.

## <a name="syntax"></a>Синтаксис


```C++
typedef enum D3DX10_NORMALMAP_FLAG { 
  D3DX10_NORMALMAP_MIRROR_U           = (1 << 16),
  D3DX10_NORMALMAP_MIRROR_V           = (2 << 16),
  D3DX10_NORMALMAP_MIRROR             = (3 << 16),
  D3DX10_NORMALMAP_INVERTSIGN         = (8 << 16),
  D3DX10_NORMALMAP_COMPUTE_OCCLUSION  = (16 << 16)
} D3DX10_NORMALMAP_FLAG, *LPD3DX10_NORMALMAP_FLAG;
```



## <a name="constants"></a>Константы

<dl> <dt>

<span id="D3DX10_NORMALMAP_MIRROR_U"></span><span id="d3dx10_normalmap_mirror_u"></span>**\_ \_ Зеркальная копия D3DX10 нормалмап \_ U**
</dt> <dd>

Указывает, что пиксели от края текстуры на оси U должны быть зеркально отображены, а не переноситься в оболочку.

</dd> <dt>

<span id="D3DX10_NORMALMAP_MIRROR_V"></span><span id="d3dx10_normalmap_mirror_v"></span>**D3DX10 \_ нормалмап \_ Mirror \_ V**
</dt> <dd>

Указывает, что пиксели с края текстуры на оси V должны быть зеркально отображены, а не переноситься в оболочку.

</dd> <dt>

<span id="D3DX10_NORMALMAP_MIRROR"></span><span id="d3dx10_normalmap_mirror"></span>**\_Зеркало D3DX10 нормалмап \_**
</dt> <dd>

То же, что и D3DX10 \_ нормалмап \_ Mirror \_ U \| D3DX10 \_ нормалмап \_ Mirror \_ V.

</dd> <dt>

<span id="D3DX10_NORMALMAP_INVERTSIGN"></span><span id="d3dx10_normalmap_invertsign"></span>**D3DX10 \_ нормалмап \_ инвертсигн**
</dt> <dd>

Инвертирует направление каждого нормального.

</dd> <dt>

<span id="D3DX10_NORMALMAP_COMPUTE_OCCLUSION"></span><span id="d3dx10_normalmap_compute_occlusion"></span>**D3DX10 \_ нормалмап \_ COMPUTE \_ перекрытия**
</dt> <dd>

Выполняет вычисление Терма перекрытия на пиксель и кодирует его в альфа-канал. Значение альфа, равное 1, означает, что пиксел не закрывается каким-либо образом, а значение альфа, равное 0, означает, что пиксель полностью скрыт.

</dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------|----------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3DX10Tex. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Перечисления D3DX](d3d10-graphics-reference-d3dx10-enums.md)
</dt> </dl>

 

 




