---
title: Структура CD3DX12_PIPELINE_STATE_STREAM_VS (D3dx12. h)
description: Вспомогательная структура, используемая для описания шейдер вершин в виде одного объекта, подходящего для описания потока.
ms.assetid: 27EAB08C-D3B9-4920-B7D2-754AA3562A94
keywords:
- Структура CD3DX12_PIPELINE_STATE_STREAM_VS
topic_type:
- apiref
api_name:
- CD3DX12_PIPELINE_STATE_STREAM_VS
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bc7ea426c857893b98b25792ecc8e6c3d5803546
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105713520"
---
# <a name="cd3dx12_pipeline_state_stream_vs-structure"></a>\_ \_ \_ Структура VS потока состояния конвейера CD3DX12 \_

Вспомогательная структура, используемая для описания шейдер вершин в виде одного объекта, подходящего для описания потока.

## <a name="syntax"></a>Синтаксис


```C++
struct CD3DX12_PIPELINE_STATE_STREAM_VS {
                                   CD3DX12_PIPELINE_STATE_STREAM_VS;
                                   CD3DX12_PIPELINE_STATE_STREAM_VS(D3D12_SHADER_BYTECODE const &i);
  CD3DX12_PIPELINE_STATE_STREAM_VS operator=(D3D12_SHADER_BYTECODE const& i);
                                   operator D3D12_SHADER_BYTECODE() const;
};
```



## <a name="members"></a>Члены

<dl> <dt>

**\_Поток состояния конвейера CD3DX12 \_ \_ \_ и**
</dt> <dd>

Создает новый, неинициализированный экземпляр \_ потока состояния конвейера CD3DX12 \_ \_ \_ и

</dd> <dt>

**\_Поток состояния конвейера CD3DX12 \_ \_ \_ и ( \_ \_ константа байта шейдера D3D12 &i)**
</dt> <dd>

Создает новый экземпляр \_ потока состояния конвейера CD3DX12 \_ \_ \_ и инициализирует с типом подобъекта типа подобъекта **\_ \_ \_ \_ \_ состояния конвейера D3D12** и данными подобъекта, скопированными из *i*, структурой [**байт- \_ \_ кода шейдера D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_shader_bytecode) .

</dd> <dt>

**operator = (D3D12ный байт-код \_ шейдера \_ "i"& i)**
</dt> <dd>

Оператор присваивания копирования.

</dd> <dt>

**\_константа-код шейдера оператора D3D12 \_ () const**
</dt> <dd>

Неявное преобразование в структуру [**\_ байт- \_ кода шейдера D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_shader_bytecode) .

</dd> </dl>

## <a name="remarks"></a>Комментарии

\_Поток состояния конвейера CD3DX12 и \_ \_ \_ является специализацией typedef шаблона [**\_ \_ \_ \_ подобъекта потока состояния конвейера CD3DX12**](cd3dx12-pipeline-state-stream-subobject.md) и определяется следующим образом:


```C++
typedef CD3DX12_PIPELINE_STATE_STREAM_SUBOBJECT<D3D12_SHADER_BYTECODE, D3D12_PIPELINE_STATE_SUBOBJECT_TYPE_VS>
    CD3DX12_PIPELINE_STATE_STREAM_VS;
          
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

 

