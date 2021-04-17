---
title: Структура CD3DX12_TEXTURE_COPY_LOCATION (D3dx12. h)
description: Вспомогательная структура, позволяющая легко инициализировать \_ \_ структуру расположения копирования текстуры D3D12 \_ .
ms.assetid: 8BA93729-2FFB-4C09-88B0-779049BAF385
keywords:
- Структура CD3DX12_TEXTURE_COPY_LOCATION
topic_type:
- apiref
api_name:
- CD3DX12_TEXTURE_COPY_LOCATION
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f5143137f92e38662660588dd89a527f59644126
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105703673"
---
# <a name="cd3dx12_texture_copy_location-structure"></a>\_ \_ Структура расположения для копирования текстур CD3DX12 \_

Вспомогательная структура, позволяющая легко инициализировать структуру [**\_ \_ \_ расположения копирования текстуры D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_texture_copy_location) .

## <a name="syntax"></a>Синтаксис


```C++
struct CD3DX12_TEXTURE_COPY_LOCATION  : public D3D12_TEXTURE_COPY_LOCATION{
   CD3DX12_TEXTURE_COPY_LOCATION();
   explicit CD3DX12_TEXTURE_COPY_LOCATION(const D3D12_TEXTURE_COPY_LOCATION &o);
   CD3DX12_TEXTURE_COPY_LOCATION(ID3D12Resource* pRes);
   CD3DX12_TEXTURE_COPY_LOCATION(ID3D12Resource* pRes, D3D12_PLACED_SUBRESOURCE_FOOTPRINT const& Footprint);
   CD3DX12_TEXTURE_COPY_LOCATION(ID3D12Resource* pRes, UINT Sub);
};
```



## <a name="members"></a>Члены

<dl> <dt>

**\_ \_ Расположение копирования текстуры CD3DX12 \_ ()**
</dt> <dd>

Создает новый, неинициализированный экземпляр \_ расположения для копирования текстуры CD3DX12 \_ \_ .

</dd> <dt>

**явное \_ \_ Расположение копии текстуры CD3DX12 \_ (константа D3D12 \_ \_ Расположение копирования текстуры \_ &o)**
</dt> <dd>

Создает новый экземпляр \_ расположения для копирования текстуры CD3DX12 \_ \_ , который инициализируется с содержимым другой структуры [**\_ \_ \_ расположения D3D12 текстуры**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_texture_copy_location) .

</dd> <dt>

**\_ \_ Расположение копии текстуры CD3DX12 \_ (ID3D12Resource \* прес)**
</dt> <dd>

Создает новый экземпляр \_ расположения для копирования текстуры CD3DX12 \_ \_ , инициализируя следующие параметры:

[**ID3D12Resource**](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource) \* прес

</dd> <dt>

**\_Расположение для \_ копирования текстур CD3DX12 \_ (ID3D12RESOURCE \* прес, D3D12 \_ размещенного в \_ подресурсе \_& объемы памяти)**
</dt> <dd>

Создает новый экземпляр \_ расположения для копирования текстуры CD3DX12 \_ \_ , инициализируя следующие параметры:

[**ID3D12Resource**](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource) \* прес

[**D3D12 \_ При РАЗМЕЩЕНии в \_ ПОДресурсе \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_placed_subresource_footprint)& объемы константы

</dd> <dt>

**\_ \_ Расположение копии текстуры CD3DX12 \_ (ID3D12Resource \* прес, подсистема uint)**
</dt> <dd>

Создает новый экземпляр \_ расположения для копирования текстуры CD3DX12 \_ \_ , инициализируя следующие параметры:

[**ID3D12Resource**](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource) \* прес

Подсистема UINT

</dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------|-------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3dx12. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**\_ \_ Расположение копии текстуры \_ D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_texture_copy_location)
</dt> <dt>

[Вспомогательные структуры для D3D12](helper-structures-for-d3d12.md)
</dt> </dl>

 

 





