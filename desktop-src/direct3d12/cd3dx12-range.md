---
title: Структура CD3DX12_RANGE (D3dx12. h)
description: Вспомогательная структура, позволяющая упростить инициализацию \_ структуры диапазона D3D12.
ms.assetid: 5D5192BF-D14C-487B-A214-F8428E82AF0E
keywords:
- Структура CD3DX12_RANGE
topic_type:
- apiref
api_name:
- CD3DX12_RANGE
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 66b6b92cd24a981d48252f5ad457f7ac0320e2d7
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105713980"
---
# <a name="cd3dx12_range-structure"></a>\_Структура диапазона CD3DX12

Вспомогательная структура, позволяющая упростить инициализацию [**структуры \_ диапазона D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_range) .

## <a name="syntax"></a>Синтаксис


```C++
struct CD3DX12_RANGE  : public D3D12_RANGE{
   CD3DX12_RANGE();
   explicit CD3DX12_RANGE(const D3D12_RANGE &o);
   CD3DX12_RANGE(SIZE_T begin, SIZE_T end);
   operator const D3D12_RANGE&() const;
};
```



## <a name="members"></a>Члены

<dl> <dt>

**CD3DX12 \_ Range ()**
</dt> <dd>

Создает новый, неинициализированный экземпляр \_ диапазона CD3DX12.

</dd> <dt>

**явный \_ диапазон CD3DX12 (константа D3D12 \_ Range &o)**
</dt> <dd>

Создает новый экземпляр \_ диапазона CD3DX12, инициализируемый содержимым другой структуры [**\_ диапазона D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_range) .

</dd> <dt>

**\_Диапазон CD3DX12 (размер \_ t, конец и размер \_ t)**
</dt> <dd>

Создает новый экземпляр \_ диапазона CD3DX12, инициализируя следующие параметры:

РАЗМЕР \_ T начало

РАЗМЕР \_ T в конце

</dd> <dt>

**Константа оператора const D3D12 \_ RANGE& () const**
</dt> <dd>

Определяет & оператором передачи по ссылке для типа родительской структуры.

</dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------|-------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3dx12. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**\_Диапазон D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_range)
</dt> <dt>

[Вспомогательные структуры для D3D12](helper-structures-for-d3d12.md)
</dt> </dl>

 

 





