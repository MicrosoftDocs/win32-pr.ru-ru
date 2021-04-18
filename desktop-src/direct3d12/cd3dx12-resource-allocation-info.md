---
title: Структура CD3DX12_RESOURCE_ALLOCATION_INFO (D3dx12. h)
description: Вспомогательная структура, позволяющая легко инициализировать \_ \_ структуру сведений о выделении ресурсов D3D12 \_ .
ms.assetid: 81FC8D0E-2C15-42D3-9E06-1FE193F707C6
keywords:
- Структура CD3DX12_RESOURCE_ALLOCATION_INFO
topic_type:
- apiref
api_name:
- CD3DX12_RESOURCE_ALLOCATION_INFO
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 08542c7460b2fadf381f85dc271167258e31fb46
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105713514"
---
# <a name="cd3dx12_resource_allocation_info-structure"></a>\_ \_ Структура сведений о выделении ресурсов CD3DX12 \_

Вспомогательная структура, позволяющая легко инициализировать структуру [**\_ \_ \_ сведений о выделении ресурсов D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_resource_allocation_info) .

## <a name="syntax"></a>Синтаксис


```C++
struct CD3DX12_RESOURCE_ALLOCATION_INFO  : public D3D12_RESOURCE_ALLOCATION_INFO{
   CD3DX12_RESOURCE_ALLOCATION_INFO();
   explicit CD3DX12_RESOURCE_ALLOCATION_INFO(const D3D12_RESOURCE_ALLOCATION_INFO& o);
   CD3DX12_RESOURCE_ALLOCATION_INFO(UINT64 size, UINT64 alignment);
   operator const D3D12_RESOURCE_ALLOCATION_INFO&() const;
};
```



## <a name="members"></a>Члены

<dl> <dt>

**\_ \_ Сведения о выделении ресурсов CD3DX12 \_ ()**
</dt> <dd>

Создает новый, неинициализированный экземпляр \_ \_ сведений о выделении ресурсов CD3DX12 \_ .

</dd> <dt>

**явные \_ \_ сведения о выделении ресурсов CD3DX12 \_ (const D3D12 \_ \_ сведения о выделении ресурсов \_& o)**
</dt> <dd>

Создает новый экземпляр \_ \_ сведений о выделении ресурсов CD3DX12 \_ , инициализируемый с помощью содержимого другой структуры [**\_ \_ \_ сведений о выделении ресурсов D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_resource_allocation_info) .

</dd> <dt>

**\_ \_ Сведения о выделении ресурсов CD3DX12 \_ (размер UINT64, выравнивание UInt64)**
</dt> <dd>

Создает новый экземпляр \_ \_ сведений о выделении ресурсов CD3DX12 \_ , инициализируя следующие параметры:

Размер UINT64

Выравнивание UINT64

</dd> <dt>

**Квалификатор operator const \_ D3D12 \_ сведения о выделении ресурсов \_& () const**
</dt> <dd>

Определяет & оператором передачи по ссылке для типа родительской структуры.

</dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------|-------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3dx12. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**\_ \_ Сведения о выделении ресурсов D3D12 \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_resource_allocation_info)
</dt> <dt>

[Вспомогательные структуры для D3D12](helper-structures-for-d3d12.md)
</dt> </dl>

 

 





