---
title: Структура CD3DX12_TILE_SHAPE (D3dx12. h)
description: Вспомогательная структура, позволяющая легко инициализировать \_ структуру фигур мозаики D3D12 \_ .
ms.assetid: 0A5963F1-8CE5-4B03-B69F-83B2B801CC21
keywords:
- Структура CD3DX12_TILE_SHAPE
topic_type:
- apiref
api_name:
- CD3DX12_TILE_SHAPE
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0b02f699ab06ef93f3eeace3ce515b0947030e4824e2cb0fa51034c3e33f51dc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119987874"
---
# <a name="cd3dx12_tile_shape-structure"></a>\_Структура фигур мозаики CD3DX12 \_

Вспомогательная структура, позволяющая легко инициализировать структуру [**\_ \_ фигур мозаики D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tile_shape) .

## <a name="syntax"></a>Синтаксис


```C++
struct CD3DX12_TILE_SHAPE  : public D3D12_TILE_SHAPE{
   CD3DX12_TILE_SHAPE();
   explicit CD3DX12_TILE_SHAPE(const D3D12_TILE_SHAPE &o);
   CD3DX12_TILE_SHAPE(UINT widthInTexels, UINT heightInTexels, UINT depthInTexels);
   operator const D3D12_TILE_SHAPE&() const;
};
```



## <a name="members"></a>Члены

<dl> <dt>

**\_Фигура плитки CD3DX12 \_ ()**
</dt> <dd>

Создает новый, неинициализированный экземпляр \_ фигуры мозаики CD3DX12 \_ .

</dd> <dt>

**явная \_ фигура CD3DX12 \_ (элемент const D3D12 \_ , \_ фигура плитки &o)**
</dt> <dd>

Создает новый экземпляр \_ фигуры мозаики CD3DX12 \_ , инициализируемый с помощью содержимого другой структуры [**\_ \_ фигур плитки D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tile_shape) .

</dd> <dt>

**\_Фигура плитки CD3DX12 \_ (uint ВИДСИНТЕКСЕЛС, uint ХЕИГХТИНТЕКСЕЛС, uint депсинтекселс)**
</dt> <dd>

Создает новый экземпляр \_ фигуры плитки CD3DX12 \_ , инициализируя следующие параметры:

UINT Видсинтекселс

UINT Хеигхтинтекселс

UINT Депсинтекселс

</dd> <dt>

**\_фигурная плитка оператора const D3D12 \_& () const**
</dt> <dd>

Определяет & оператором передачи по ссылке для типа родительской структуры.

</dd> </dl>

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------|-------------------------------------------------------------------------------------|
| Заголовок<br/> | <dl> <dt>D3dx12. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**\_Фигура плитки \_ D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tile_shape)
</dt> <dt>

[Вспомогательные структуры для D3D12](helper-structures-for-d3d12.md)
</dt> </dl>

 

 





