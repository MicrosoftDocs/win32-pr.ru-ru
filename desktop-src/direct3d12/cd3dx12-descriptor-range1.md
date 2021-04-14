---
title: Структура CD3DX12_DESCRIPTOR_RANGE1 (D3dx12. h)
description: Вспомогательная структура, позволяющая легко инициализировать \_ структуру высокое дескриптора D3D12 \_ .
ms.assetid: 9D073158-5907-4D1C-8D75-72B304277DAD
keywords:
- Структура CD3DX12_DESCRIPTOR_RANGE1
topic_type:
- apiref
api_name:
- CD3DX12_DESCRIPTOR_RANGE1
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6386d8094d573fba9cd3af44b0148215ee621e2f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105647815"
---
# <a name="cd3dx12_descriptor_range1-structure"></a>\_Структура высокое дескриптора CD3DX12 \_

Вспомогательная структура, позволяющая легко инициализировать структуру [**\_ \_ высокое дескриптора D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range1) .

## <a name="syntax"></a>Синтаксис


```C++
struct CD3DX12_DESCRIPTOR_RANGE1  : public D3D12_DESCRIPTOR_RANGE1{
       CD3DX12_DESCRIPTOR_RANGE1();
       explicit CD3DX12_DESCRIPTOR_RANGE1(const D3D12_DESCRIPTOR_RANGE1 &o);
       CD3DX12_DESCRIPTOR_RANGE1(D3D12_DESCRIPTOR_RANGE_TYPE rangeType, UINT numDescriptors, UINT baseShaderRegister, UINT registerSpace = 0, D3D12_DESCRIPTOR_RANGE_FLAGS flags = D3D12_DESCRIPTOR_RANGE_FLAG_NONE, UINT offsetInDescriptorsFromTableStart = D3D12_DESCRIPTOR_RANGE_OFFSET_APPEND);
  void inline Init(D3D12_DESCRIPTOR_RANGE_TYPE rangeType, UINT numDescriptors, UINT baseShaderRegister, UINT registerSpace = 0, D3D12_DESCRIPTOR_RANGE_FLAGS flags = D3D12_DESCRIPTOR_RANGE_FLAG_NONE, UINT offsetInDescriptorsFromTableStart = D3D12_DESCRIPTOR_RANGE_OFFSET_APPEND);
  void static inline Init(D3D12_DESCRIPTOR_RANGE1 &range, D3D12_DESCRIPTOR_RANGE_TYPE rangeType, UINT numDescriptors, UINT baseShaderRegister, UINT registerSpace = 0, D3D12_DESCRIPTOR_RANGE_FLAGS flags = D3D12_DESCRIPTOR_RANGE_FLAG_NONE, UINT offsetInDescriptorsFromTableStart = D3D12_DESCRIPTOR_RANGE_OFFSET_APPEND);
};
```



## <a name="members"></a>Члены

<dl> <dt>

**\_Высокое дескриптора CD3DX12 \_ ()**
</dt> <dd>

Создает новый, неинициализированный экземпляр CD3DX12 \_ дескриптора \_ высокое.

</dd> <dt>

**явный \_ дескриптор CD3DX12 \_ высокое (const D3D12 \_ дескриптор \_ высокое &o)**
</dt> <dd>

Создает новый экземпляр \_ дескриптора CD3DX12 \_ высокое, инициализируемый с помощью содержимого другой [**D3D12 \_ дескриптора \_ высокое**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range1) .

</dd> <dt>

**CD3DX12 \_ дескриптор \_ высокое (D3D12 \_ - \_ диапазон дескрипторов \_ РАНЖЕТИПЕ, uint НУМДЕСКРИПТОРС, uint басешадеррегистер, uint регистерспаце = 0, флаги \_ ДИАПАЗОНов D3D12 дескрипторов \_ \_ : D3D12 \_ \_ \_ \_ \_ \_ \_ \_**
</dt> <dd>

Создает новый экземпляр \_ дескриптора CD3DX12 \_ высокое, инициализируя следующие параметры:

[**D3D12 \_ Ранжетипе \_ \_ тип диапазона дескрипторов**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_descriptor_range_type)

UINT Нумдескрипторс

UINT Басешадеррегистер

UINT Регистерспаце = 0

[**D3D12 \_ Флаги флагов \_ \_ диапазона дескрипторов**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_descriptor_range_flags) = \_ \_ \_ значение флага диапазона дескрипторов D3D12 \_ None

UINT Оффсетиндескрипторсфромтаблестарт = \_ \_ \_ Добавление смещения диапазона дескрипторов D3D12 \_

</dd> <dt>

**Inline init (D3D12- \_ диапазон дескрипторов \_ \_ Ранжетипе, UINT Нумдескрипторс, UINT Басешадеррегистер, uint регистерспаце = 0, флаги \_ флагов диапазона дескрипторов D3D12 = " \_ \_ \_ \_ \_ \_ нет", uint D3D12 = \_ оффсетиндескрипторсфромтаблестарт \_ смещение диапазона дескрипторов ( \_ \_ append))**
</dt> <dd>

Задает функцию, которая инициализирует следующие параметры:

[**D3D12 \_ Ранжетипе \_ \_ тип диапазона дескрипторов**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_descriptor_range_type)

UINT Нумдескрипторс

UINT Басешадеррегистер

UINT Регистерспаце = 0

[**D3D12 \_ Флаги флагов \_ \_ диапазона дескрипторов**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_descriptor_range_flags) = \_ \_ \_ значение флага диапазона дескрипторов D3D12 \_ None

UINT Оффсетиндескрипторсфромтаблестарт = \_ \_ \_ Добавление смещения диапазона дескрипторов D3D12 \_

</dd> <dt>

**статический встроенный метод init (D3D12 \_ дескриптора \_ высокое &Range, \_ D3D12 \_ диапазоны дескрипторов \_ РАНЖЕТИПЕ, uint НУМДЕСКРИПТОРС, uint басешадеррегистер, uint регистерспаце = 0, D3D12 флагов \_ диапазона дескрипторов \_ \_ = D3D12 \_ \_ ФЛАГа диапазона дескрипторов \_ \_ None, uint оффсетиндескрипторсфромтаблестарт = D3D12, \_ \_ Добавление смещения диапазона дескрипторов \_ \_ )**
</dt> <dd>

Задает функцию, которая инициализирует следующие параметры:

[**D3D12 \_ \_Высокое дескриптора**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range1) &диапазон

[**D3D12 \_ Ранжетипе \_ \_ тип диапазона дескрипторов**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_descriptor_range_type)

UINT Нумдескрипторс

UINT Басешадеррегистер

UINT Регистерспаце = 0

[**D3D12 \_ Флаги флагов \_ \_ диапазона дескрипторов**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_descriptor_range_flags) = \_ \_ \_ значение флага диапазона дескрипторов D3D12 \_ None

UINT Оффсетиндескрипторсфромтаблестарт = \_ \_ \_ Добавление смещения диапазона дескрипторов D3D12 \_

</dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------|-------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3dx12. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**\_Высокое дескриптора D3D12 \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range1)
</dt> <dt>

[Вспомогательные структуры для D3D12](helper-structures-for-d3d12.md)
</dt> </dl>

 

 





