---
title: Структура CD3DX12_ROOT_DESCRIPTOR_TABLE (D3dx12. h)
description: Вспомогательная структура, позволяющая упростить инициализацию \_ \_ структуры таблицы дескрипторов D3D12 root \_ .
ms.assetid: 154B4C50-4E94-471C-A44E-F120A84F007C
keywords:
- Структура CD3DX12_ROOT_DESCRIPTOR_TABLE
topic_type:
- apiref
api_name:
- CD3DX12_ROOT_DESCRIPTOR_TABLE
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 158f1d52be9502f3f886aebd3f0eb60a66d9b389367919bd5b941b880e2556ec
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118098463"
---
# <a name="cd3dx12_root_descriptor_table-structure"></a>\_ \_ Структура таблицы дескрипторов CD3DX12 root \_

Вспомогательная структура, позволяющая упростить инициализацию [**структуры \_ \_ \_ таблицы дескрипторов D3D12 root**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_descriptor_table) .

## <a name="syntax"></a>Синтаксис


```C++
struct CD3DX12_ROOT_DESCRIPTOR_TABLE  : public D3D12_ROOT_DESCRIPTOR_TABLE{
       CD3DX12_ROOT_DESCRIPTOR_TABLE();
       explicit CD3DX12_ROOT_DESCRIPTOR_TABLE(const D3D12_ROOT_DESCRIPTOR_TABLE &o);
       CD3DX12_ROOT_DESCRIPTOR_TABLE(UINT numDescriptorRanges, const D3D12_DESCRIPTOR_RANGE* _pDescriptorRanges);
  void inline Init(UINT numDescriptorRanges, const D3D12_DESCRIPTOR_RANGE* _pDescriptorRanges);
  void static inline Init(D3D12_ROOT_DESCRIPTOR_TABLE &rootDescriptorTable, UINT numDescriptorRanges, const D3D12_DESCRIPTOR_RANGE* _pDescriptorRanges);
};
```



## <a name="members"></a>Члены

<dl> <dt>

**CD3DX12 \_ корневая \_ Таблица дескрипторов \_ ()**
</dt> <dd>

Создает новый, неинициализированный экземпляр \_ \_ таблицы дескриптора CD3DX12 root \_ .

</dd> <dt>

**явная CD3DX12 \_ корневая \_ Таблица дескрипторов \_ (const \_ D3D12 \_ Таблица дескрипторов корня \_ &o)**
</dt> <dd>

Создает новый экземпляр CD3DX12 \_ корневой \_ таблицы дескрипторов \_ , инициализируемый содержимым другой структуры [**\_ \_ \_ таблицы дескриптора root D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_descriptor_table) .

</dd> <dt>

**CD3DX12 \_ корневая \_ Таблица дескрипторов \_ (uint нумдескрипторранжес, константный \_ диапазон дескрипторов D3D12 \_ \* \_ пдескрипторранжес)**
</dt> <dd>

Создает новый экземпляр CD3DX12 \_ корневой \_ таблицы дескрипторов \_ , инициализируя следующие параметры:

UINT Нумдескрипторранжес

[**D3D12 \_ Пдескрипторранжес \_ диапазона дескрипторов**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range) \* \_

</dd> <dt>

**Inline init (UINT Нумдескрипторранжес, const D3D12 \_ \_ диапазон дескрипторов \* \_ пдескрипторранжес)**
</dt> <dd>

Задает функцию, которая инициализирует следующие параметры:

UINT Нумдескрипторранжес

[**D3D12 \_ Пдескрипторранжес \_ диапазона дескрипторов**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range) \* \_

</dd> <dt>

**Статическая встроенная init (D3D12 \_ \_ , таблица дескрипторов root \_ &Рутдескриптортабле, uint НУМДЕСКРИПТОРРАНЖЕС, const D3D12 \_ диапазон дескрипторов \_ \* \_ пдескрипторранжес)**
</dt> <dd>

Задает функцию, которая инициализирует следующие параметры:

[**D3D12 \_ \_ \_ Таблица дескрипторов root**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_descriptor_table) &рутдескриптортабле

UINT Нумдескрипторранжес

[**D3D12 \_ Пдескрипторранжес \_ диапазона дескрипторов**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range) \* \_

</dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------|-------------------------------------------------------------------------------------|
| Заголовок<br/> | <dl> <dt>D3dx12. h</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**D3D12 \_ корневая \_ Таблица дескрипторов \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_descriptor_table)
</dt> <dt>

[Вспомогательные структуры для D3D12](helper-structures-for-d3d12.md)
</dt> </dl>

 

 





