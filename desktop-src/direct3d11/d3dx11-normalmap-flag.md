---
title: Перечисление D3DX11_NORMALMAP_FLAG (D3DX11tex. h)
description: Обратите внимание, что библиотека служебной программы D3DX (D3DX 9, D3DX 10 и D3DX 11) является устаревшей для Windows 8 и не поддерживается для приложений Магазина Windows. Стандартные параметры карт. Любое число этих флагов можно объединить с помощью побитовой операции или.
ms.assetid: cc9c8a54-be1e-4594-8274-9955562a6fa8
keywords:
- Перечисление D3DX11_NORMALMAP_FLAG Direct3D 11
- Указатель перечисления LPD3DX11_NORMALMAP_FLAG Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11_NORMALMAP_FLAG
api_location:
- D3DX11tex.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 37f5d9669370e6df03d783ae1cb82a5eeb5a9142
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104273964"
---
# <a name="d3dx11_normalmap_flag-enumeration"></a>\_ \_ Перечисление флагов нормалмап D3DX11

> [!Note]  
> Библиотека служебной программы D3DX (D3DX 9, D3DX 10 и D3DX 11) является устаревшей для Windows 8 и не поддерживается для приложений Магазина Windows.

 

Стандартные параметры карт. Любое число этих флагов можно объединить с помощью побитовой операции или.

## <a name="syntax"></a>Синтаксис


```C++
typedef enum D3DX11_NORMALMAP_FLAG { 
  D3DX11_NORMALMAP_MIRROR_U           = (1 << 16),
  D3DX11_NORMALMAP_MIRROR_V           = (2 << 16),
  D3DX11_NORMALMAP_MIRROR             = (3 << 16),
  D3DX11_NORMALMAP_INVERTSIGN         = (8 << 16),
  D3DX11_NORMALMAP_COMPUTE_OCCLUSION  = (16 << 16)
} D3DX11_NORMALMAP_FLAG, *LPD3DX11_NORMALMAP_FLAG;
```



## <a name="constants"></a>Константы

<dl> <dt>

<span id="D3DX11_NORMALMAP_MIRROR_U"></span><span id="d3dx11_normalmap_mirror_u"></span>**\_ \_ Зеркальная копия D3DX11 нормалмап \_ U**
</dt> <dd>

Указывает, что пиксели от края текстуры на оси U должны быть зеркально отображены, а не переноситься в оболочку.

</dd> <dt>

<span id="D3DX11_NORMALMAP_MIRROR_V"></span><span id="d3dx11_normalmap_mirror_v"></span>**D3DX11 \_ нормалмап \_ Mirror \_ V**
</dt> <dd>

Указывает, что пиксели с края текстуры на оси V должны быть зеркально отображены, а не переноситься в оболочку.

</dd> <dt>

<span id="D3DX11_NORMALMAP_MIRROR"></span><span id="d3dx11_normalmap_mirror"></span>**\_Зеркало D3DX11 нормалмап \_**
</dt> <dd>

То же, что и D3DX11 \_ нормалмап \_ Mirror \_ U \| D3DX11 \_ нормалмап \_ Mirror \_ V.

</dd> <dt>

<span id="D3DX11_NORMALMAP_INVERTSIGN"></span><span id="d3dx11_normalmap_invertsign"></span>**D3DX11 \_ нормалмап \_ инвертсигн**
</dt> <dd>

Инвертирует направление каждого нормального.

</dd> <dt>

<span id="D3DX11_NORMALMAP_COMPUTE_OCCLUSION"></span><span id="d3dx11_normalmap_compute_occlusion"></span>**D3DX11 \_ нормалмап \_ COMPUTE \_ перекрытия**
</dt> <dd>

Выполняет вычисление Терма перекрытия на пиксель и кодирует его в альфа-канал. Значение альфа, равное 1, означает, что пиксел не закрывается каким-либо образом, а значение альфа, равное 0, означает, что пиксель полностью скрыт.

</dd> </dl>

## <a name="remarks"></a>Примечания

Эти флаги используются [**D3DX11ComputeNormalMap**](d3dx11computenormalmap.md).

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------|----------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3DX11tex. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Перечисления D3DX](d3d11-graphics-reference-d3dx11-enums.md)
</dt> </dl>

 

 





