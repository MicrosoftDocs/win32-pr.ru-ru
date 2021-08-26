---
title: Структура CD3DX12_SUBRESOURCE_RANGE_UINT64 (D3dx12. h)
description: Вспомогательная структура, позволяющая упростить инициализацию \_ структуры диапазона ПОДРЕСУРСОВ D3D12 \_ \_ .
ms.assetid: 607A60ED-98D2-4A77-9A7A-6B54342EA101
keywords:
- Структура CD3DX12_SUBRESOURCE_RANGE_UINT64
topic_type:
- apiref
api_name:
- CD3DX12_SUBRESOURCE_RANGE_UINT64
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: df38d5b2e7a4230d023aeba6c8c3517fbd2b9f4e35a09b5e4439269b228eb82e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119987994"
---
# <a name="cd3dx12_subresource_range_uint64-structure"></a>\_ \_ Структура UINT64 диапазона ПОДресурсов CD3DX12 \_

Вспомогательная структура, позволяющая упростить инициализацию [**структуры \_ \_ диапазона \_ подресурсов D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_range_uint64) .

## <a name="syntax"></a>Синтаксис


```C++
struct CD3DX12_SUBRESOURCE_RANGE_UINT64  : public D3D12_SUBRESOURCE_RANGE_UINT64{
  CD3DX12_SUBRESOURCE_RANGE_UINT64 CD3DX12_SUBRESOURCE_RANGE_UINT64();
  CD3DX12_SUBRESOURCE_RANGE_UINT64 explicit CD3DX12_SUBRESOURCE_RANGE_UINT64(const D3D12_SUBRESOURCE_RANGE_UINT64 &o);
  CD3DX12_SUBRESOURCE_RANGE_UINT64 CD3DX12_SUBRESOURCE_RANGE_UINT64(UINT subresource, const D3D12_RANGE_UINT64& range);
  CD3DX12_SUBRESOURCE_RANGE_UINT64 CD3DX12_SUBRESOURCE_RANGE_UINT64(UINT subresource, UINT64 begin, UINT64 end);
                                   operator const D3D12_SUBRESOURCE_RANGE_UINT64&() const;
};
```



## <a name="members"></a>Члены

<dl> <dt>

**\_UINT64 диапазона ПОДРЕСУРСОВ CD3DX12 \_ \_ ()**
</dt> <dd>

Создает новый, неинициализированный экземпляр значения \_ UINT64 диапазона ПОДРЕСУРСОВ CD3DX12 \_ \_ .

</dd> <dt>

**явный CD3DX12 \_ диапазон ПОДресурсов, \_ \_ UInt64 (константа D3D12 \_ диапазон подресурсов, \_ \_ UInt64 &o)**
</dt> <dd>

Создает новый экземпляр класса CD3DX12 \_ \_ с диапазоном \_ UInt64, инициализируемый значениями, скопированными из структуры [**\_ \_ \_ UINT64 диапазона подресурсов D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_range_uint64) .

</dd> <dt>

**CD3DX12 диапазона \_ подресурсов \_ \_ ("подресурс uint", константа D3D12 \_ диапазона \_ UInt64&)**
</dt> <dd>

Создает новый экземпляр CD3DX12 \_ \_ трафарета глубины \_ DESC1, инициализируемый значениями, передаваемыми в списке параметров.

</dd> <dt>

**\_UINT64 диапазона ПОДРЕСУРСОВ CD3DX12 \_ \_ (подресурс uint, начало UINT64, конец UInt64)**
</dt> <dd>

Создает новый экземпляр CD3DX12 \_ \_ трафарета глубины \_ DESC1, инициализируемый значениями, передаваемыми в списке параметров.

</dd> <dt>

**Константа оператора const D3D12 \_ диапазон подресурсов \_ \_ UINT64& () const**
</dt> <dd>

Неявное преобразование в \_ структуру D3D12 \_ диапазона подресурсов \_ . Так как D3D12 \_ диапазона подресурсов \_ \_ является базовым типом для \_ диапазона CD3DX12 \_ \_ , то объект просто возвращается в виде константы D3D12 \_ \_ трафарета глубины \_ DESC1 ссылку на себя.

</dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------|-------------------------------------------------------------------------------------|
| Заголовок<br/> | <dl> <dt>D3dx12. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Вспомогательные структуры для D3D12](helper-structures-for-d3d12.md)
</dt> <dt>

[**\_UINT64 диапазона ПОДРЕСУРСОВ D3D12 \_ \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_range_uint64)
</dt> </dl>

 

 





