---
title: Структура CD3DX12_RANGE_UINT64 (D3dx12. h)
description: Вспомогательная структура, позволяющая легко инициализировать структуру D3D12 \_ диапазона \_ UINT64.
ms.assetid: 789A2C46-B7D4-462E-9C10-69FD63D27491
keywords:
- Структура CD3DX12_RANGE_UINT64
topic_type:
- apiref
api_name:
- CD3DX12_RANGE_UINT64
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 89c408197afb1254cae922c402939f6f169708d4
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105713981"
---
# <a name="cd3dx12_range_uint64-structure"></a>\_ \_ Структура UINT64 диапазона CD3DX12

Вспомогательная структура, позволяющая легко инициализировать структуру [**D3D12 \_ диапазона \_ UINT64**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_range_uint64) .

## <a name="syntax"></a>Синтаксис


```C++
struct CD3DX12_RANGE_UINT64  : public D3D12_RANGE_UINT64{
  CD3DX12_RANGE_UINT64 CD3DX12_RANGE_UINT64();
  CD3DX12_RANGE_UINT64 explicit CD3DX12_RANGE_UINT64(const D3D12_RANGE_UINT64 &o);
  CD3DX12_RANGE_UINT64 CD3DX12_RANGE_UINT64(UINT64 begin, UINT64 end);
                       operator const D3D12_RANGE_UINT64&() const;
};
```



## <a name="members"></a>Члены

<dl> <dt>

**CD3DX12 \_ диапазона \_ UINT64 ()**
</dt> <dd>

Создает новый, неинициализированный экземпляр класса \_ UINT64 диапазона CD3DX12 \_ .

</dd> <dt>

**явный CD3DX12 \_ диапазон \_ UInt64 (константа D3D12 \_ Range \_ UInt64 &o)**
</dt> <dd>

Создает новый экземпляр CD3DX12 \_ диапазона \_ UInt64, инициализируемый значениями, скопированными из структуры [**\_ \_ UINT64 диапазона D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_range_uint64) .

</dd> <dt>

**CD3DX12 \_ диапазона \_ UInt64 (начало UInt64, окончание UInt64)**
</dt> <dd>

Создает новый экземпляр CD3DX12 \_ \_ трафарета глубины \_ DESC1, инициализируемый значениями, передаваемыми в списке параметров.

</dd> <dt>

**Константа оператора const D3D12 \_ Range \_ UINT64& () const**
</dt> <dd>

Неявное преобразование в \_ структуру D3D12 диапазона \_ UINT64. Так как D3D12 \_ Range \_ UInt64 является базовым типом \_ UInt64 CD3DX12 Range \_ , объект просто возвращается в виде константы D3D12 \_ диапазона \_ UInt64 на саму себя.

</dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------|-------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3dx12. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Вспомогательные структуры для D3D12](helper-structures-for-d3d12.md)
</dt> <dt>

[**\_UINT64 диапазона \_ D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_range_uint64)
</dt> </dl>

 

 





