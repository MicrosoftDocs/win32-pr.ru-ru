---
title: Структура CD3DX12_DESCRIPTOR_RANGE (D3dx12. h)
description: Вспомогательная структура, позволяющая упростить инициализацию \_ структуры диапазона дескрипторов D3D12 \_ .
ms.assetid: F066ECA5-5E52-4483-B773-B43C5F12809B
keywords:
- Структура CD3DX12_DESCRIPTOR_RANGE
topic_type:
- apiref
api_name:
- CD3DX12_DESCRIPTOR_RANGE
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b511af1766daaefa7f92d33b71841b3a69c99927
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105647816"
---
# <a name="cd3dx12_descriptor_range-structure"></a>\_Структура диапазона дескрипторов CD3DX12 \_

Вспомогательная структура, позволяющая упростить инициализацию [**структуры \_ \_ диапазона дескрипторов D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range) .

## <a name="syntax"></a>Синтаксис


```C++
struct CD3DX12_DESCRIPTOR_RANGE  : public D3D12_DESCRIPTOR_RANGE{
       CD3DX12_DESCRIPTOR_RANGE();
       explicit CD3DX12_DESCRIPTOR_RANGE(const D3D12_DESCRIPTOR_RANGE &o);
       CD3DX12_DESCRIPTOR_RANGE(D3D12_DESCRIPTOR_RANGE_TYPE rangeType, UINT numDescriptors, UINT baseShaderRegister, UINT registerSpace = 0, UINT offsetInDescriptorsFromTableStart = D3D12_DESCRIPTOR_RANGE_OFFSET_APPEND);
  void inline Init(D3D12_DESCRIPTOR_RANGE_TYPE rangeType, UINT numDescriptors, UINT baseShaderRegister, UINT registerSpace = 0, UINT offsetInDescriptorsFromTableStart = D3D12_DESCRIPTOR_RANGE_OFFSET_APPEND);
  void static inline Init(D3D12_DESCRIPTOR_RANGE &range, D3D12_DESCRIPTOR_RANGE_TYPE rangeType, UINT numDescriptors, UINT baseShaderRegister, UINT registerSpace = 0, UINT offsetInDescriptorsFromTableStart = D3D12_DESCRIPTOR_RANGE_OFFSET_APPEND);
};
```



## <a name="members"></a>Члены

<dl> <dt>

**\_Диапазон дескрипторов CD3DX12 \_ ()**
</dt> <dd>

Создает новый, неинициализированный экземпляр \_ диапазона дескрипторов D3DX12 \_ .

</dd> <dt>

**явный \_ диапазон дескрипторов CD3DX12 \_ (константный \_ диапазон дескрипторов D3D12 \_ &o)**
</dt> <dd>

Создает новый экземпляр \_ диапазона дескрипторов D3DX12 \_ , инициализируемый с помощью содержимого другой структуры [**\_ \_ диапазона дескрипторов D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range) .

</dd> <dt>

**\_Диапазон дескрипторов CD3DX12 \_ ( \_ тип диапазона дескрипторов D3D12 \_ \_ ранжетипе, uint НУМДЕСКРИПТОРС, uint басешадеррегистер, UINT Регистерспаце = 0, uint оффсетиндескрипторсфромтаблестарт = D3D12, \_ \_ Добавление смещения диапазона дескрипторов \_ \_ )**
</dt> <dd>

Создает новый экземпляр \_ диапазона дескрипторов D3DX12 \_ , инициализируя следующие параметры:

[**D3D12 \_ Ранжетипе \_ \_ тип диапазона дескрипторов**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_descriptor_range_type)

UINT Нумдескрипторс

UINT Басешадеррегистер

UINT Регистерспаце = 0

UINT Оффсетиндескрипторсфромтаблестарт = \_ \_ \_ Добавление смещения диапазона дескрипторов D3D12 \_

</dd> <dt>

**Inline init (D3D12- \_ \_ тип диапазона дескрипторов \_ Ранжетипе, UINT Нумдескрипторс, UINT Басешадеррегистер, uint регистерспаце = 0, uint оффсетиндескрипторсфромтаблестарт = D3D12, \_ \_ Добавление смещения диапазона дескрипторов \_ \_ )**
</dt> <dd>

Задает функцию, которая инициализирует следующие параметры:

[**D3D12 \_ Ранжетипе \_ \_ тип диапазона дескрипторов**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_descriptor_range_type)

UINT Нумдескрипторс

UINT Басешадеррегистер

UINT Регистерспаце = 0

UINT Оффсетиндескрипторсфромтаблестарт = \_ \_ \_ Добавление смещения диапазона дескрипторов D3D12 \_

</dd> <dt>

**static Inline init (диапазон D3D12- \_ дескрипторов &, диапазон дескрипторов \_ D3D12, \_ \_ \_ тип РАНЖЕТИПЕ, uint НУМДЕСКРИПТОРС, uint басешадеррегистер, UINT Регистерспаце = 0, uint оффсетиндескрипторсфромтаблестарт = D3D12 \_ смещение диапазона дескрипторов ( \_ \_ \_ append))**
</dt> <dd>

Задает функцию, которая инициализирует следующие параметры:

[**D3D12 \_ Диапазон \_ дескрипторов**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range) &диапазона

[**D3D12 \_ Ранжетипе \_ \_ тип диапазона дескрипторов**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_descriptor_range_type)

UINT Нумдескрипторс

UINT Басешадеррегистер

UINT Регистерспаце = 0

UINT Оффсетиндескрипторсфромтаблестарт = \_ \_ \_ Добавление смещения диапазона дескрипторов D3D12 \_

</dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------|-------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3dx12. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**\_Диапазон дескрипторов D3D12 \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range)
</dt> <dt>

[Вспомогательные структуры для D3D12](helper-structures-for-d3d12.md)
</dt> </dl>

 

 





