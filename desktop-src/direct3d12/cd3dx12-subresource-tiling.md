---
title: Структура CD3DX12_SUBRESOURCE_TILING (D3dx12. h)
description: Вспомогательная структура, позволяющая легко инициализировать \_ \_ структуру разбиения подресурсов D3D12.
ms.assetid: 102E5E25-300B-40F2-A953-E40AD7EE61AD
keywords:
- Структура CD3DX12_SUBRESOURCE_TILING
topic_type:
- apiref
api_name:
- CD3DX12_SUBRESOURCE_TILING
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 07677c8a8367f58016a0236cf0b5558b852bef01
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105713499"
---
# <a name="cd3dx12_subresource_tiling-structure"></a>\_ \_ Структура разбиения ПОДресурсов CD3DX12

Вспомогательная структура, позволяющая легко инициализировать структуру [**\_ \_ разбиения подресурсов D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_tiling) .

## <a name="syntax"></a>Синтаксис


```C++
struct CD3DX12_SUBRESOURCE_TILING  : public D3D12_SUBRESOURCE_TILING{
   CD3DX12_SUBRESOURCE_TILING();
   explicit CD3DX12_SUBRESOURCE_TILING(const D3D12_SUBRESOURCE_TILING &o);
   CD3DX12_SUBRESOURCE_TILING(UINT widthInTiles, UINT16 heightInTiles, UINT16 depthInTiles, UINT startTileIndexInOverallResource);
   operator const D3D12_SUBRESOURCE_TILING&() const;
};
```



## <a name="members"></a>Члены

<dl> <dt>

**\_Разбиение ПОДРЕСУРСОВ CD3DX12 \_ ()**
</dt> <dd>

Создает новый, неинициализированный экземпляр \_ ПОДресурса CD3DX12 \_ .

</dd> <dt>

**прямое \_ разбиение ПОДРЕСУРСОВ CD3DX12 \_ (const D3D12 \_ подресурсов \_ &o)**
</dt> <dd>

Создает новый экземпляр подкласса CD3DX12 \_ \_ , инициализируемый с помощью содержимого другой структуры подмассива [**D3D12 \_ \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_tiling) .

</dd> <dt>

**\_Разбиение ПОДРЕСУРСОВ CD3DX12 \_ (uint ВИДСИНТИЛЕС, UInt16 ХЕИГХТИНТИЛЕС, UINT16 ДЕПСИНТИЛЕС, uint старттилеиндексиновераллресаурце)**
</dt> <dd>

Создает новый экземпляр \_ ПОДРЕСУРСА CD3DX12 \_ , инициализируя следующие параметры:

UINT Видсинтилес

UINT16 Хеигхтинтилес

UINT16 Депсинтилес

UINT Старттилеиндексиновераллресаурце

</dd> <dt>

**D3D12 "operator const" \_ \_ разбиение подресурсов& () const**
</dt> <dd>

Определяет & оператором передачи по ссылке для типа родительской структуры.

</dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------|-------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3dx12. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**\_Разбиение ПОДРЕСУРСОВ D3D12 \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_tiling)
</dt> <dt>

[Вспомогательные структуры для D3D12](helper-structures-for-d3d12.md)
</dt> </dl>

 

 





