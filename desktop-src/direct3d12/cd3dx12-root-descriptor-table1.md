---
title: Структура CD3DX12_ROOT_DESCRIPTOR_TABLE1 (D3dx12. h)
description: Вспомогательная структура, позволяющая упростить инициализацию \_ \_ структуры Table1 корневого дескриптора D3D12 \_ .
ms.assetid: 82AC1948-92AA-4A4D-B443-717E9BF3046D
keywords:
- Структура CD3DX12_ROOT_DESCRIPTOR_TABLE1
topic_type:
- apiref
api_name:
- CD3DX12_ROOT_DESCRIPTOR_TABLE1
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4570629b810fb7a088c7cfd88e3626412d5580beb1891a1a30daf9ffabede5d2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117733996"
---
# <a name="cd3dx12_root_descriptor_table1-structure"></a>\_ \_ Структура Table1 корневого ДЕСКРИПТОРа CD3DX12 \_

Вспомогательная структура, позволяющая упростить инициализацию [**структуры \_ \_ \_ Table1 корневого дескриптора D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_descriptor_table1) .

## <a name="syntax"></a>Синтаксис


```C++
struct CD3DX12_ROOT_DESCRIPTOR_TABLE1  : public D3D12_ROOT_DESCRIPTOR_TABLE1{
       CD3DX12_ROOT_DESCRIPTOR_TABLE1();
       explicit CD3DX12_ROOT_DESCRIPTOR_TABLE1(const D3D12_ROOT_DESCRIPTOR_TABLE1 &o);
       CD3DX12_ROOT_DESCRIPTOR_TABLE1(UINT numDescriptorRanges, const D3D12_DESCRIPTOR_RANGE1* _pDescriptorRanges);
  void inline Init(UINT numDescriptorRanges, const D3D12_DESCRIPTOR_RANGE1* _pDescriptorRanges);
  void static inline Init(D3D12_ROOT_DESCRIPTOR_TABLE1 &rootDescriptorTable, UINT numDescriptorRanges, const D3D12_DESCRIPTOR_RANGE1* _pDescriptorRanges);
};
```



## <a name="members"></a>Члены

<dl> <dt>

**\_Корневой \_ дескриптор CD3DX12 \_ Table1 ()**
</dt> <dd>

Создает новый, неинициализированный экземпляр CD3DX12 \_ корневого \_ дескриптора \_ Table1.

</dd> <dt>

**явный CD3DX12 \_ корневого \_ дескриптора \_ Table1 (const D3D12 \_ root \_ дескриптора \_ Table1 &o)**
</dt> <dd>

Создает новый экземпляр CD3DX12 \_ корневого \_ дескриптора \_ Table1, инициализированного с содержимым другой структуры [**D3D12 \_ корневого \_ дескриптора \_ Table1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_descriptor_table1) .

</dd> <dt>

**CD3DX12 \_ root \_ дескриптора \_ Table1 (uint НУМДЕСКРИПТОРРАНЖЕС, const D3D12 \_ дескриптор \_ высокое \* \_ пдескрипторранжес)**
</dt> <dd>

Создает новый экземпляр CD3DX12 \_ корневого \_ дескриптора \_ Table1, инициализируя следующие параметры:

UINT Нумдескрипторранжес

const [**D3D12 \_ дескриптор \_ высокое**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range1) \* \_ пдескрипторранжес

</dd> <dt>

**Inline init (UINT Нумдескрипторранжес, const D3D12 \_ дескриптора \_ высокое \* \_ пдескрипторранжес)**
</dt> <dd>

Задает функцию, которая инициализирует следующие параметры:

UINT Нумдескрипторранжес

const [**D3D12 \_ дескриптор \_ высокое**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range1) \* \_ пдескрипторранжес

</dd> <dt>

**статический встроенный метод init (D3D12 \_ root \_ дескриптора \_ Table1 &Рутдескриптортабле, uint НУМДЕСКРИПТОРРАНЖЕС, const D3D12 \_ дескриптор \_ высокое \* \_ пдескрипторранжес)**
</dt> <dd>

Задает функцию, которая инициализирует следующие параметры:

[**D3D12 \_ КОРНЕВой \_ дескриптор \_ Table1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_descriptor_table1) &рутдескриптортабле

UINT Нумдескрипторранжес

const [**D3D12 \_ дескриптор \_ высокое**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range1) \* \_ пдескрипторранжес

</dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------|-------------------------------------------------------------------------------------|
| Заголовок<br/> | <dl> <dt>D3dx12. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**\_Корневой \_ дескриптор D3D12 \_ Таблица1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_descriptor_table1)
</dt> <dt>

[Вспомогательные структуры для D3D12](helper-structures-for-d3d12.md)
</dt> </dl>

 

 





