---
title: Структура CD3DX12_HEAP_PROPERTIES (D3dx12. h)
description: Вспомогательная структура, позволяющая легко инициализировать \_ \_ структуру свойств кучи D3D12.
ms.assetid: AC759F25-D643-412D-AA83-3A2C040BE64B
keywords:
- Структура CD3DX12_HEAP_PROPERTIES
topic_type:
- apiref
api_name:
- CD3DX12_HEAP_PROPERTIES
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 90cc5f5cee6bf70aad064396589aad8a483f2c50
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105694104"
---
# <a name="cd3dx12_heap_properties-structure"></a>\_ \_ Структура свойств кучи CD3DX12

Вспомогательная структура, позволяющая легко инициализировать структуру [**\_ \_ свойств кучи D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_heap_properties) .

## <a name="syntax"></a>Синтаксис


```C++
struct CD3DX12_HEAP_PROPERTIES  : public D3D12_HEAP_PROPERTIES{
       CD3DX12_HEAP_PROPERTIES();
       explicit CD3DX12_HEAP_PROPERTIES(const D3D12_HEAP_PROPERTIES &o);
       CD3DX12_HEAP_PROPERTIES(D3D12_CPU_PAGE_PROPERTY cpuPageProperty, D3D12_MEMORY_POOL memoryPoolPreference, UINT creationNodeMask = 1, UINT nodeMask = 1);
       explicit CD3DX12_HEAP_PROPERTIES(D3D12_HEAP_TYPE type, UINT creationNodeMask = 1, UINT nodeMask = 1);
       operator const D3D12_HEAP_PROPERTIES&() const;
  bool inline operator==( const D3D12_HEAP_PROPERTIES& l, const D3D12_HEAP_PROPERTIES& r );
  bool inline operator!=( const D3D12_HEAP_PROPERTIES& l, const D3D12_HEAP_PROPERTIES& r );
};
```



## <a name="members"></a>Члены

<dl> <dt>

**\_Свойства КУЧИ CD3DX12 \_ ()**
</dt> <dd>

Создает новый, неинициализированный экземпляр \_ свойств КУЧИ CD3DX12 \_ .

</dd> <dt>

**явные \_ Свойства КУЧИ CD3DX12 \_ (свойства const D3D12 \_ кучи \_ &o)**
</dt> <dd>

Создает новый экземпляр \_ свойств КУЧИ CD3DX12 \_ , инициализируемый с содержимым другой структуры [**\_ \_ свойств кучи D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_heap_properties) .

</dd> <dt>

**\_Свойства КУЧИ CD3DX12 \_ ( \_ свойство страницы ЦП D3D12 \_ \_ Кпупажепроперти, D3D12 \_ \_ пула памяти МЕМОРИПУЛПРЕФЕРЕНЦЕ, uint креатионнодемаск = 1, uint нодемаск = 1)**
</dt> <dd>

Создает новый экземпляр \_ свойств КУЧИ CD3DX12 \_ , инициализируя следующие параметры:

[**D3D12 \_ \_ \_ Свойство страницы ЦП**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_cpu_page_property) кпупажепроперти

[**D3D12 \_ Меморипулпреференце \_ пула памяти**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_memory_pool)

участие UINT Креатионнодемаск = 1

участие UINT Нодемаск = 1

</dd> <dt>

**явные \_ Свойства КУЧИ CD3DX12 \_ ( \_ тип КУЧИ D3D12 \_ , uint КРЕАТИОННОДЕМАСК = 1, uint нодемаск = 1)**
</dt> <dd>

Создает новый экземпляр \_ свойств КУЧИ CD3DX12 \_ , инициализируя следующие параметры:

[**D3D12 \_ Тип \_ типа кучи**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_heap_type)

участие UINT Креатионнодемаск = 1

участие UINT Нодемаск = 1

</dd> <dt>

**Константа operator const D3D12 \_ \_ свойства кучи& () const**
</dt> <dd>

Определяет & оператором передачи по ссылке для типа родительской структуры.

</dd> <dt>

**встроенный оператор = = (const D3D12 \_ Свойства кучи \_& l, константные \_ свойства кучи D3D12 \_& r)**
</dt> <dd>

Проверяет на равенство между указанными \_ \_ экземплярами свойств кучи D3D12 на основе равенства всех полей элементов.

</dd> <dt>

**встроенный оператор! = (const D3D12 \_ Свойства кучи \_& l, константные \_ свойства кучи D3D12 \_& r)**
</dt> <dd>

Проверяет наличие неравенства между указанными \_ \_ экземплярами свойств кучи D3D12. Реализуется путем взятия обратного значения **оператора = =** value.

</dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------|-------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3dx12. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**\_Свойства КУЧИ \_ D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_heap_properties)
</dt> <dt>

[Вспомогательные структуры для D3D12](helper-structures-for-d3d12.md)
</dt> </dl>

 

 





