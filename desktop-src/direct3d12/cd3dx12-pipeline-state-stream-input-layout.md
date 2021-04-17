---
title: Структура CD3DX12_PIPELINE_STATE_STREAM_INPUT_LAYOUT (D3dx12. h)
description: Вспомогательная структура, используемая для описания входного макета в виде одного объекта, подходящего для описания потока.
ms.assetid: CEAD9FA6-4FB0-492E-9E81-8C4900A1FBC5
keywords:
- Структура CD3DX12_PIPELINE_STATE_STREAM_INPUT_LAYOUT
topic_type:
- apiref
api_name:
- CD3DX12_PIPELINE_STATE_STREAM_INPUT_LAYOUT
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6ba382552d700ddddee02cdc1343936e6bcf6837
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105651542"
---
# <a name="cd3dx12_pipeline_state_stream_input_layout-structure"></a>\_ \_ \_ \_ \_ Структура входной структуры потока состояния конвейера CD3DX12

Вспомогательная структура, используемая для описания входного макета в виде одного объекта, подходящего для описания потока.

## <a name="syntax"></a>Синтаксис


```C++
struct CD3DX12_PIPELINE_STATE_STREAM_INPUT_LAYOUT {
                                             CD3DX12_PIPELINE_STATE_STREAM_INPUT_LAYOUT;
                                             CD3DX12_PIPELINE_STATE_STREAM_INPUT_LAYOUT(D3D12_INPUT_LAYOUT_DESC const &i);
  CD3DX12_PIPELINE_STATE_STREAM_INPUT_LAYOUT operator=(D3D12_INPUT_LAYOUT_DESC const& i);
                                             operator D3D12_INPUT_LAYOUT_DESC() const;
};
```



## <a name="members"></a>Члены

<dl> <dt>

**\_ \_ \_ \_ Схема ввода потока состояния конвейера CD3DX12 \_**
</dt> <dd>

Создает новый, неинициализированный экземпляр \_ \_ \_ \_ входного макета потока состояния конвейера CD3DX12 \_ .

</dd> <dt>

**\_ \_ Схема ввода потока состояния конвейера CD3DX12 \_ \_ \_ (D3D12 \_ входной \_ Макет структуры данных \_ const &i)**
</dt> <dd>

Создает новый экземпляр \_ \_ \_ схемы входного потока состояния конвейера \_ CD3DX12 \_ , инициализированный с типом подобъекта для типа **\_ \_ подобъекта состояния конвейера D3D12 \_ \_ \_ \_ структура входных** данных и подобъектами, скопированными из *i*, [**D3D12 \_ ввода структуры входного \_ макета \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_input_layout_desc) .

</dd> <dt>

**operator = (D3D12 \_ входной \_ Макет структуры \_ const& i)**
</dt> <dd>

Оператор присваивания копирования.

</dd> <dt>

**\_константа D3D12 входного макета оператора operator \_ \_ () const**
</dt> <dd>

Неявное преобразование в структуру [**D3D12 \_ входных данных \_ макета \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_input_layout_desc) .

</dd> </dl>

## <a name="remarks"></a>Комментарии

\_ \_ Схема ввода потока состояния конвейера CD3DX12 \_ \_ \_ является СПЕЦИАЛИЗАЦИей typedef шаблона [**\_ \_ \_ \_ подобъекта потока состояния конвейера CD3DX12**](cd3dx12-pipeline-state-stream-subobject.md) и определяется следующим образом:


```C++
typedef CD3DX12_PIPELINE_STATE_STREAM_SUBOBJECT<D3D12_INPUT_LAYOUT_DESC, D3D12_PIPELINE_STATE_SUBOBJECT_TYPE_INPUT_LAYOUT>
    CD3DX12_PIPELINE_STATE_STREAM_INPUT_LAYOUT;
          
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

 

