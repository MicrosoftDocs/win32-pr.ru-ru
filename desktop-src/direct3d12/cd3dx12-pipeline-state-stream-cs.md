---
title: Структура CD3DX12_PIPELINE_STATE_STREAM_CS (D3dx12. h)
description: Вспомогательная структура, используемая для описания шейдера вычислений в виде одного объекта, подходящего для описания потока.
ms.assetid: B76B0CB4-FC76-4C5B-84FC-DCFF907BE2F8
keywords:
- Структура CD3DX12_PIPELINE_STATE_STREAM_CS
topic_type:
- apiref
api_name:
- CD3DX12_PIPELINE_STATE_STREAM_CS
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bda76603c6250e5a4319f54a202bffddeead28fa9baa1c4da91b2e9b290d62d7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119751934"
---
# <a name="cd3dx12_pipeline_state_stream_cs-structure"></a>\_ \_ \_ Структура CS потока состояния конвейера CD3DX12 \_

Вспомогательная структура, используемая для описания шейдера вычислений в виде одного объекта, подходящего для описания потока.

## <a name="syntax"></a>Синтаксис


```C++
struct CD3DX12_PIPELINE_STATE_STREAM_CS {
                                   CD3DX12_PIPELINE_STATE_STREAM_CS;
                                   CD3DX12_PIPELINE_STATE_STREAM_CS(D3D12_SHADER_BYTECODE const &i);
  CD3DX12_PIPELINE_STATE_STREAM_CS operator=(D3D12_SHADER_BYTECODE const& i);
                                   operator D3D12_SHADER_BYTECODE() const;
};
```



## <a name="members"></a>Члены

<dl> <dt>

**\_Поток состояния конвейера CD3DX12 \_ \_ \_ CS**
</dt> <dd>

Создает новый, неинициализированный экземпляр \_ потока состояния конвейера CD3DX12 \_ \_ \_ CS.

</dd> <dt>

**\_Поток состояния конвейера CD3DX12 \_ \_ \_ CS ( \_ \_ константа байта шейдера D3D12 &i)**
</dt> <dd>

Создает новый экземпляр \_ потока состояния конвейера CD3DX12 \_ \_ \_ , инициализируемый с типом подобъекта для типа **\_ \_ \_ подобъекта состояния \_ \_ конвейера D3D12 CS** и данными подобъекта, скопированными из *i*, структурой [**байт- \_ \_ кода шейдера D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_shader_bytecode) .

</dd> <dt>

**operator = (D3D12ный байт-код \_ шейдера \_ "i"& i)**
</dt> <dd>

Оператор присваивания копирования.

</dd> <dt>

**\_константа-код шейдера оператора D3D12 \_ () const**
</dt> <dd>

Неявное преобразование в структуру [**\_ байт- \_ кода шейдера D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_shader_bytecode) .

</dd> </dl>

## <a name="remarks"></a>Remarks

\_Поток состояния конвейера CD3DX12 \_ \_ \_ CS является специализацией typedef шаблона [**\_ \_ \_ \_ подобъекта потока состояния конвейера CD3DX12**](cd3dx12-pipeline-state-stream-subobject.md) и определяется следующим образом:


```C++
typedef CD3DX12_PIPELINE_STATE_STREAM_SUBOBJECT<D3D12_SHADER_BYTECODE, D3D12_PIPELINE_STATE_SUBOBJECT_TYPE_CS>
    CD3DX12_PIPELINE_STATE_STREAM_CS;
          
```



## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------|-------------------------------------------------------------------------------------|
| Заголовок<br/> | <dl> <dt>D3dx12. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Вспомогательные структуры для D3D12](helper-structures-for-d3d12.md)
</dt> <dt>

[**\_Подобъект \_ потока состояния КОНВЕЙЕРа CD3DX12 \_ \_**](cd3dx12-pipeline-state-stream-subobject.md)
</dt> <dt>

[**\_ \_ \_ Тип подобъекта состояния конвейера D3D12 \_**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_pipeline_state_subobject_type)
</dt> </dl>

 

