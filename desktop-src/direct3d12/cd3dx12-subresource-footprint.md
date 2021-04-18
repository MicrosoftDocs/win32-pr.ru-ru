---
title: Структура CD3DX12_SUBRESOURCE_FOOTPRINT (D3dx12. h)
description: Вспомогательная структура, позволяющая упростить инициализацию \_ структуры, занимаемой ПОДресурсом D3D12 \_ .
ms.assetid: 17266FB0-41B5-4A70-A896-206B54F5E76F
keywords:
- Структура CD3DX12_SUBRESOURCE_FOOTPRINT
topic_type:
- apiref
api_name:
- CD3DX12_SUBRESOURCE_FOOTPRINT
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ab58e9a007d736222d9525d7a064456a1a9a7f14
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105713502"
---
# <a name="cd3dx12_subresource_footprint-structure"></a>\_Структура для ПОДресурсов CD3DX12 \_

Вспомогательная структура, позволяющая упростить инициализацию структуры, [**\_ \_ ЗАНИМАЕМой подресурсом D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_footprint) .

## <a name="syntax"></a>Синтаксис


```C++
struct CD3DX12_SUBRESOURCE_FOOTPRINT  : public D3D12_SUBRESOURCE_FOOTPRINT{
   CD3DX12_SUBRESOURCE_FOOTPRINT();
   explicit CD3DX12_SUBRESOURCE_FOOTPRINT(const D3D12_SUBRESOURCE_FOOTPRINT &o);
   CD3DX12_SUBRESOURCE_FOOTPRINT(DXGI_FORMAT format, UINT width, UINT height, UINT depth, UINT rowPitch);
   explicit CD3DX12_SUBRESOURCE_FOOTPRINT(const D3D12_RESOURCE_DESC& resDesc, UINT rowPitch);
   operator const D3D12_SUBRESOURCE_FOOTPRINT&() const;
};
```



## <a name="members"></a>Члены

<dl> <dt>

**\_Объем ПОДРЕСУРСОВ CD3DX12 \_ ()**
</dt> <dd>

Создает новый, неинициализированный экземпляр CD3DX12 \_ ПОДресурса \_ .

</dd> <dt>

**явное CD3DX12 \_ ПОДресурсного \_ пространства (D3D12 \_ \_ &o)**
</dt> <dd>

Создает новый экземпляр \_ ПОДресурса CD3DX12 \_ , который инициализируется с помощью содержимого другой структуры, [**\_ \_ занимаемой подресурсом D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_footprint) .

</dd> <dt>

**CD3DX12 \_ подресурсов \_ ( \_ Формат формата DXGI, ширина UINT, высота UINT, глубина uint, uint ровпитч)**
</dt> <dd>

Создает новый экземпляр \_ ПОДресурса CD3DX12, который задается при \_ инициализации следующих параметров:

[**DXGI \_ Формат формата**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)

Ширина UINT

Высота UINT

Глубина UINT

UINT Ровпитч

</dd> <dt>

**явное CD3DX12 ресурсов \_ \_ (const D3D12 \_ Resource \_ DESC& ресдеск, uint ровпитч)**
</dt> <dd>

Создает новый экземпляр \_ ПОДресурса CD3DX12, который задается при \_ инициализации следующих параметров:

[**D3D12 \_ RESOURCE \_ DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_resource_desc)& ресдеск

UINT Ровпитч

</dd> <dt>

**\_константа оператора const D3D12 \_& () const**
</dt> <dd>

Определяет & оператором передачи по ссылке для типа родительской структуры.

</dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------|-------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3dx12. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**\_Объем ПОДРЕСУРСОВ \_ D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_footprint)
</dt> <dt>

[Вспомогательные структуры для D3D12](helper-structures-for-d3d12.md)
</dt> </dl>

 

