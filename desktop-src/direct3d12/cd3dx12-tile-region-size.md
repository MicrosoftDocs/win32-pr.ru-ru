---
title: Структура CD3DX12_TILE_REGION_SIZE (D3dx12. h)
description: Вспомогательная структура, позволяющая упростить инициализацию \_ \_ структуры размера области мозаики D3D12 \_ .
ms.assetid: 07D2D8DE-C35C-48EE-8E9E-36545B60C594
keywords:
- Структура CD3DX12_TILE_REGION_SIZE
topic_type:
- apiref
api_name:
- CD3DX12_TILE_REGION_SIZE
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 40f64046f2a7efa32af8b43adbcf7349f43b6ec3
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105703672"
---
# <a name="cd3dx12_tile_region_size-structure"></a>\_ \_ Структура размера области плитки CD3DX12 \_

Вспомогательная структура, позволяющая упростить инициализацию [**структуры \_ \_ \_ размера области мозаики D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tile_region_size) .

## <a name="syntax"></a>Синтаксис


```C++
struct CD3DX12_TILE_REGION_SIZE  : public D3D12_TILE_REGION_SIZE{
   CD3DX12_TILE_REGION_SIZE();
   explicit CD3DX12_TILE_REGION_SIZE(const D3D12_TILE_REGION_SIZE &o);
   CD3DX12_TILE_REGION_SIZE(UINT numTiles, BOOL useBox, UINT width, UINT16 height, UINT16 depth);
   operator const D3D12_TILE_REGION_SIZE&() const;
};
```



## <a name="members"></a>Члены

<dl> <dt>

**\_ \_ Размер области плитки CD3DX12 \_ ()**
</dt> <dd>

Создает новый, неинициализированный экземпляр CD3DX12 \_ \_ размера области мозаики \_ .

</dd> <dt>

**явный \_ \_ Размер области плитки CD3DX12 \_ (const D3D12 \_ \_ область плитки \_ Размер &o)**
</dt> <dd>

Создает новый экземпляр CD3DX12 \_ размера области мозаики \_ \_ , инициализируемый содержимым другой структуры [**\_ \_ \_ размера области плитки D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tile_region_size) .

</dd> <dt>

**\_ \_ Размер области плитки CD3DX12 \_ (uint Нумтилес, bool УСЕБОКС, ширина uint, высота UINT16, глубина UInt16)**
</dt> <dd>

Создает новый экземпляр \_ \_ размера области плитки CD3DX12 \_ , инициализируя следующие параметры:

UINT Нумтилес

BOOL Усебокс

Ширина UINT

Высота UINT16

Глубина UINT16

</dd> <dt>

**D3D12 \_ () размер области плитки оператора const константы \_ \_& () const**
</dt> <dd>

Определяет & оператором передачи по ссылке для типа родительской структуры.

</dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------|-------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3dx12. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**\_ \_ Размер области плитки \_ D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tile_region_size)
</dt> <dt>

[Вспомогательные структуры для D3D12](helper-structures-for-d3d12.md)
</dt> </dl>

 

 





