---
title: Структура CD3DX12_TILED_RESOURCE_COORDINATE (D3dx12. h)
description: Вспомогательная структура, позволяющая легко инициализировать \_ структуру координат D3D12 мозаичного \_ ресурса \_ .
ms.assetid: B337ED04-E2C6-4B89-80F1-92C0854A6AF2
keywords:
- Структура CD3DX12_TILED_RESOURCE_COORDINATE
topic_type:
- apiref
api_name:
- CD3DX12_TILED_RESOURCE_COORDINATE
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 784955545fe8e71227ffae6c5eec54acfd65b4a0ab0867f5c7de99a148976861
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119987854"
---
# <a name="cd3dx12_tiled_resource_coordinate-structure"></a>\_ \_ Структура координат мозаичного ресурса CD3DX12 \_

Вспомогательная структура, позволяющая легко инициализировать структуру [**\_ \_ \_ координат D3D12 мозаичного ресурса**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tiled_resource_coordinate) .

## <a name="syntax"></a>Синтаксис


```C++
struct CD3DX12_TILED_RESOURCE_COORDINATE  : public D3D12_TILED_RESOURCE_COORDINATE{
   CD3DX12_TILED_RESOURCE_COORDINATE();
   explicit CD3DX12_TILED_RESOURCE_COORDINATE(const D3D12_TILED_RESOURCE_COORDINATE &o);
   CD3DX12_TILED_RESOURCE_COORDINATE(UINT x, UINT y, UINT z, UINT subresource);
   operator const D3D12_TILED_RESOURCE_COORDINATE&() const;
};
```



## <a name="members"></a>Члены

<dl> <dt>

**CD3DX12 \_ Мозаичное \_ \_ координата ресурса ()**
</dt> <dd>

Создает новый, неинициализированный экземпляр \_ координаты CD3DX12 мозаичного \_ ресурса \_ .

</dd> <dt>

**явная CD3DX12 \_ \_ координата мозаичного ресурса \_ (const D3D12 \_ мозаичная \_ \_ координата ресурса &o)**
</dt> <dd>

Создает новый экземпляр \_ \_ координатного мозаичного ресурса CD3DX12 \_ , инициализируемый с помощью содержимого другой [**D3D12 \_ мозаичной структуры \_ \_ координат ресурсов**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tiled_resource_coordinate) .

</dd> <dt>

**CD3DX12 \_ мозаичная \_ \_ координата ресурса (UINT x, UINT y, uint z, подресурсе uint)**
</dt> <dd>

Создает новый экземпляр \_ координат ресурсов мозаичного заполнения \_ CD3DX12 \_ , инициализируя следующие параметры:

UINT x

UINT y

UINT z

Подресурс UINT

</dd> <dt>

**Константа "оператор Const D3D12" \_ координата незаполненного \_ ресурса \_& () const**
</dt> <dd>

Определяет & оператором передачи по ссылке для типа родительской структуры.

</dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------|-------------------------------------------------------------------------------------|
| Заголовок<br/> | <dl> <dt>D3dx12. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**\_ \_ Координата мозаичного ресурса D3D12 \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tiled_resource_coordinate)
</dt> <dt>

[Вспомогательные структуры для D3D12](helper-structures-for-d3d12.md)
</dt> </dl>

 

 





