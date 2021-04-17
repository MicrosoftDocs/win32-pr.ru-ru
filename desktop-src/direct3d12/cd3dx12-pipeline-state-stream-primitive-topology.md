---
title: Структура CD3DX12_PIPELINE_STATE_STREAM_PRIMITIVE_TOPOLOGY (D3dx12. h)
description: Вспомогательная структура, используемая для описания топологии примитивов в виде одного объекта, подходящего для описания потока.
ms.assetid: 7DC73B75-2B8D-4DAB-A0AA-6DF6F4039093
keywords:
- Структура CD3DX12_PIPELINE_STATE_STREAM_PRIMITIVE_TOPOLOGY
topic_type:
- apiref
api_name:
- CD3DX12_PIPELINE_STATE_STREAM_PRIMITIVE_TOPOLOGY
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e597da8ea1ed4a4291142065e8e06f89d2664e03
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105694097"
---
# <a name="cd3dx12_pipeline_state_stream_primitive_topology-structure"></a>\_ \_ \_ \_ Структура топологии примитива потока состояния конвейера CD3DX12 \_

Вспомогательная структура, используемая для описания топологии примитивов в виде одного объекта, подходящего для описания потока.

## <a name="syntax"></a>Синтаксис


```C++
struct CD3DX12_PIPELINE_STATE_STREAM_PRIMITIVE_TOPOLOGY {
                                                   CD3DX12_PIPELINE_STATE_STREAM_PRIMITIVE_TOPOLOGY;
                                                   CD3DX12_PIPELINE_STATE_STREAM_PRIMITIVE_TOPOLOGY(D3D12_PRIMITIVE_TOPOLOGY_TYPE const &i);
  CD3DX12_PIPELINE_STATE_STREAM_PRIMITIVE_TOPOLOGY operator=(D3D12_PRIMITIVE_TOPOLOGY_TYPE const& i);
                                                   operator D3D12_PRIMITIVE_TOPOLOGY_TYPE() const;
};
```



## <a name="members"></a>Члены

<dl> <dt>

**\_ \_ \_ \_ Топология примитива потока состояния конвейера CD3DX12 \_**
</dt> <dd>

Создает новый, неинициализированный экземпляр \_ \_ \_ \_ топологии примитива потока состояния конвейера CD3DX12 \_ .

</dd> <dt>

**\_ \_ \_ Топология примитива потока состояния конвейера CD3DX12 \_ \_ (тип D3D12- \_ примитива \_ \_ типа "const" &i)**
</dt> <dd>

Создает новый экземпляр \_ \_ \_ топологии примитива потока состояния конвейера \_ CD3DX12 \_ , инициализированный с типом подобъекта для типа **\_ \_ \_ подобъекта \_ типа \_ \_ подобъекта состояния конвейера D3D12** и данными подобъекта, скопированными из *i*, структурой [**\_ \_ \_ типа примитивной топологии D3D12**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_primitive_topology_type) .

</dd> <dt>

**operator = (D3D12 \_ \_ тип топологии примитива \_ типа "const"& i)**
</dt> <dd>

Оператор присваивания копирования.

</dd> <dt>

**\_ \_ константа operator D3D12 \_ тип-примитив () const**
</dt> <dd>

Неявное преобразование в структуру [**типа D3D12- \_ примитивной \_ топологии \_**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_primitive_topology_type) .

</dd> </dl>

## <a name="remarks"></a>Комментарии

\_ \_ \_ Топология примитива потока состояния конвейера CD3DX12 \_ \_ является СПЕЦИАЛИЗАЦИей typedef шаблона [**\_ \_ \_ \_ подобъекта потока состояния конвейера CD3DX12**](cd3dx12-pipeline-state-stream-subobject.md) и определяется следующим образом:


```C++
typedef CD3DX12_PIPELINE_STATE_STREAM_SUBOBJECT<D3D12_PRIMITIVE_TOPOLOGY_TYPE, D3D12_PIPELINE_STATE_SUBOBJECT_TYPE_PRIMITIVE_TOPOLOGY>
    CD3DX12_PIPELINE_STATE_STREAM_PRIMITIVE_TOPOLOGY;
          
```



## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------|-------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3dx12. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Вспомогательные структуры для D3D12](helper-structures-for-d3d12.md)
</dt> <dt>

[**\_Подобъект \_ потока состояния КОНВЕЙЕРа CD3DX12 \_ \_**](cd3dx12-pipeline-state-stream-subobject.md)
</dt> <dt>

[**\_ \_ \_ Тип подобъекта состояния конвейера D3D12 \_**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_pipeline_state_subobject_type)
</dt> </dl>

 

