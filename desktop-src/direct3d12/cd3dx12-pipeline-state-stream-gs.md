---
title: Структура CD3DX12_PIPELINE_STATE_STREAM_GS (D3dx12. h)
description: Вспомогательная структура, используемая для описания шейдера Geometry в виде одного объекта, подходящего для описания потока.
ms.assetid: EAE81688-DAEE-4F7C-A80D-E33B364B2E8C
keywords:
- Структура CD3DX12_PIPELINE_STATE_STREAM_GS
topic_type:
- apiref
api_name:
- CD3DX12_PIPELINE_STATE_STREAM_GS
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: df5ab5854ceddfb1a969742924c8063450e611bc
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105651545"
---
# <a name="cd3dx12_pipeline_state_stream_gs-structure"></a>\_ \_ \_ Структура GS потока состояния конвейера CD3DX12 \_

Вспомогательная структура, используемая для описания шейдера Geometry в виде одного объекта, подходящего для описания потока.

## <a name="syntax"></a>Синтаксис


```C++
struct CD3DX12_PIPELINE_STATE_STREAM_GS {
                                   CD3DX12_PIPELINE_STATE_STREAM_GS;
                                   CD3DX12_PIPELINE_STATE_STREAM_GS(D3D12_SHADER_BYTECODE const &i);
  CD3DX12_PIPELINE_STATE_STREAM_GS operator=(D3D12_SHADER_BYTECODE const& i);
                                   operator D3D12_SHADER_BYTECODE() const;
};
```



## <a name="members"></a>Члены

<dl> <dt>

**\_ \_ \_ GS потока состояния конвейера CD3DX12 \_**
</dt> <dd>

Создает новый, неинициализированный экземпляр \_ потока состояния конвейера CD3DX12 \_ \_ \_ .

</dd> <dt>

**\_Поток состояния конвейера CD3DX12 \_ \_ \_ (байт-код \_ шейдера D3D12, \_ константа &i)**
</dt> <dd>

Создает новый экземпляр \_ потока состояния конвейера CD3DX12 \_ \_ \_ , инициализируемый с типом подобъекта для типа **\_ \_ \_ подобъекта \_ \_ состояния конвейера D3D12** , скопированного с *i*, структурой [**байт- \_ \_ кода шейдера D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_shader_bytecode) .

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

\_Поток состояния конвейера CD3DX12 \_ \_ \_ GS является специализацией typedef шаблона [**\_ \_ \_ \_ подобъекта потока состояния конвейера CD3DX12**](cd3dx12-pipeline-state-stream-subobject.md) и определяется следующим образом:


```C++
typedef CD3DX12_PIPELINE_STATE_STREAM_SUBOBJECT<D3D12_SHADER_BYTECODE, D3D12_PIPELINE_STATE_SUBOBJECT_TYPE_GS>
    CD3DX12_PIPELINE_STATE_STREAM_GS;
          
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

 

