---
title: Структура CD3DX12_HEAP_DESC (D3dx12. h)
description: Вспомогательная структура, позволяющая упростить инициализацию структуры D3D12 в \_ куче \_ .
ms.assetid: 38E0BA60-2BB0-4AC1-870A-10AB16E4C6E6
keywords:
- Структура CD3DX12_HEAP_DESC
topic_type:
- apiref
api_name:
- CD3DX12_HEAP_DESC
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 347e44a8516b48dcd779d3ac19fbc9b5bbf5d37ad565f36a0b9b10a083d395c3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119858374"
---
# <a name="cd3dx12_heap_desc-structure"></a>\_Структура CD3DX12 кучи \_

Вспомогательная структура, позволяющая упростить инициализацию структуры [**D3D12 в \_ куче \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_heap_desc) .

## <a name="syntax"></a>Синтаксис


```C++
struct CD3DX12_HEAP_DESC  : public D3D12_HEAP_DESC{
   CD3DX12_HEAP_DESC();
   explicit CD3DX12_HEAP_DESC(const D3D12_HEAP_DESC &o);
   CD3DX12_HEAP_DESC(UINT64 size, D3D12_HEAP_PROPERTIES properties, UINT64 alignment = 0, D3D12_HEAP_FLAGS flags = D3D12_HEAP_FLAG_NONE);
   CD3DX12_HEAP_DESC(UINT64 size, D3D12_HEAP_TYPE type, UINT64 alignment = 0, D3D12_HEAP_FLAGS flags = D3D12_HEAP_FLAG_NONE);
   CD3DX12_HEAP_DESC(UINT64 size, D3D12_CPU_PAGE_PROPERTY cpuPageProperty, D3D12_MEMORY_POOL memoryPoolPreference, UINT64 alignment = 0, D3D12_HEAP_FLAGS flags = D3D12_HEAP_FLAG_NONE);
   CD3DX12_HEAP_DESC(const D3D12_RESOURCE_ALLOCATION_INFO& resAllocInfo, D3D12_HEAP_PROPERTIES properties, D3D12_HEAP_FLAGS flags = D3D12_HEAP_FLAG_NONE);
   CD3DX12_HEAP_DESC(const D3D12_RESOURCE_ALLOCATION_INFO& resAllocInfo, D3D12_HEAP_TYPE type, D3D12_HEAP_FLAGS flags = D3D12_HEAP_FLAG_NONE);
   CD3DX12_HEAP_DESC(const D3D12_RESOURCE_ALLOCATION_INFO& resAllocInfo, D3D12_CPU_PAGE_PROPERTY cpuPageProperty, D3D12_MEMORY_POOL memoryPoolPreference, D3D12_HEAP_FLAGS flags = D3D12_HEAP_FLAG_NONE);
   operator const D3D12_HEAP_DESC&() const;
};
```



## <a name="members"></a>Члены

<dl> <dt>

**CD3DX12 \_ heap \_ DESC ()**
</dt> <dd>

Создает новый, не инициализированный экземпляр CD3DX12 \_ кучи \_ DESC.

</dd> <dt>

**явная \_ куча CD3DX12 \_ DESC (const D3D12 \_ heap \_ DESC &o)**
</dt> <dd>

Создает новый экземпляр CD3DX12 \_ кучи \_ DESC, инициализируемый с содержимым другой структуры [**\_ кучи \_ D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_heap_desc) .

</dd> <dt>

**CD3DX12 \_ heap \_ DESC (размер UInt64, свойства \_ кучи D3D12 \_ , выравнивание UINT64 = 0, \_ \_ Флаги флагов D3D12 кучи = \_ D3D12 \_ куча \_ None)**
</dt> <dd>

Создает новый экземпляр CD3DX12 \_ кучи \_ DESC, инициализируя следующие параметры:

Размер UINT64

[**D3D12 \_ Свойства \_ кучи**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_heap_properties)

участие UINT64 выравнивание = 0

участие [**D3D12 \_ Флаги \_ флагов кучи**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_heap_flags) = D3D12 \_ куча \_ \_ нет

</dd> <dt>

**CD3DX12 \_ heap \_ DESC (размер UInt64, \_ \_ тип типа КУЧИ D3D12, выравнивание UINT64 = 0, D3D12 флаги { \_ heap \_ = \_ D3D12 \_ кучи \_ None)**
</dt> <dd>

Создает новый экземпляр CD3DX12 \_ кучи \_ DESC, инициализируя следующие параметры:

Размер UINT64

[**D3D12 \_ Тип \_ типа кучи**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_heap_type)

участие UINT64 выравнивание = 0

участие [**D3D12 \_ Флаги \_ флагов кучи**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_heap_flags) = D3D12 \_ куча \_ \_ нет

</dd> <dt>

**CD3DX12 \_ heap \_ DESC (размер UINT64, \_ \_ свойство страницы ЦП D3D12 \_ Кпупажепроперти, D3D12 \_ \_ пула памяти МЕМОРИПУЛПРЕФЕРЕНЦЕ, выравнивание UINT64 = 0, D3D12 флаги \_ flags в куче \_ = D3D12 \_ \_ флаг кучи \_ None)**
</dt> <dd>

Создает новый экземпляр CD3DX12 \_ кучи \_ DESC, инициализируя следующие параметры:

Размер UINT64

[**D3D12 \_ \_ \_ Свойство страницы ЦП**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_cpu_page_property) кпупажепроперти

[**D3D12 \_ Меморипулпреференце \_ пула памяти**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_memory_pool)

участие UINT64 выравнивание = 0

участие [**D3D12 \_ Флаги \_ флагов кучи**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_heap_flags) = D3D12 \_ куча \_ \_ нет

</dd> <dt>

**CD3DX12 \_ heap \_ DESC (const D3D12 \_ \_ сведения о выделении ресурсов \_& ресаллоЦинфо, СВОЙСТВАх D3D12 \_ кучи, D3D12 флаги \_ \_ \_ флагов кучи = D3D12 \_ heap \_ флаг \_ None)**
</dt> <dd>

Создает новый экземпляр CD3DX12 \_ кучи \_ DESC, инициализируя следующие параметры:

[**D3D12 \_ \_ \_ Сведения о выделении ресурсов**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_resource_allocation_info)& ресаллоЦинфо

[**D3D12 \_ Свойства \_ кучи**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_heap_properties)

участие [**D3D12 \_ Флаги \_ флагов кучи**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_heap_flags) = D3D12 \_ куча \_ \_ нет

</dd> <dt>

**CD3DX12 \_ heap \_ DESC (const D3D12 \_ \_ сведения о выделении ресурсов \_& РЕСАЛЛОЦИНФО, тип \_ типа кучи D3D12 \_ , D3D12 флаги \_ \_ флагов кучи = D3D12 \_ heap \_ флаг \_ None)**
</dt> <dd>

Создает новый экземпляр CD3DX12 \_ кучи \_ DESC, инициализируя следующие параметры:

[**D3D12 \_ \_ \_ Сведения о выделении ресурсов**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_resource_allocation_info)& ресаллоЦинфо

[**D3D12 \_ Тип \_ типа кучи**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_heap_type)

участие [**D3D12 \_ Флаги \_ флагов кучи**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_heap_flags) = D3D12 \_ куча \_ \_ нет

</dd> <dt>

**CD3DX12 \_ heap \_ DESC (const D3D12 \_ \_ сведения о выделении ресурсов \_& ресаллоЦинфо, D3D12 \_ \_ Свойства страницы ЦП \_ кпупажепроперти, D3D12 \_ пула памяти меморипулпреференце, флаги флагов D3D12 кучи \_ , \_ \_ flags = D3D12 \_ heap \_ флаг \_ None)**
</dt> <dd>

Создает новый экземпляр CD3DX12 \_ кучи \_ DESC, инициализируя следующие параметры:

[**D3D12 \_ \_ \_ Сведения о выделении ресурсов**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_resource_allocation_info)& ресаллоЦинфо

[**D3D12 \_ \_ \_ Свойство страницы ЦП**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_cpu_page_property) кпупажепроперти

[**D3D12 \_ Меморипулпреференце \_ пула памяти**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_memory_pool)

участие [**D3D12 \_ Флаги \_ флагов кучи**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_heap_flags) = D3D12 \_ куча \_ \_ нет

</dd> <dt>

**const константа D3D12 \_& heap для оператора const \_**
</dt> <dd>

Определяет & оператором передачи по ссылке для \_ \_ типа структуры кучи CD3DX12.

</dd> </dl>

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------|-------------------------------------------------------------------------------------|
| Заголовок<br/> | <dl> <dt>D3dx12. h</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**\_DESC КУЧИ \_ D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_heap_desc)
</dt> <dt>

[Вспомогательные структуры для D3D12](helper-structures-for-d3d12.md)
</dt> </dl>

 

 





