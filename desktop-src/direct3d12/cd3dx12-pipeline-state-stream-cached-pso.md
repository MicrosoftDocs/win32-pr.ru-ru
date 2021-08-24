---
title: Структура CD3DX12_PIPELINE_STATE_STREAM_CACHED_PSO (D3dx12. h)
description: Вспомогательная структура, используемая для описания кэшированного PSO в виде одного объекта, подходящего для описания потока.
ms.assetid: 86CDC60A-275D-4B71-BE6D-C863C72E9C05
keywords:
- Структура CD3DX12_PIPELINE_STATE_STREAM_CACHED_PSO
topic_type:
- apiref
api_name:
- CD3DX12_PIPELINE_STATE_STREAM_CACHED_PSO
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a11cb4e7a784b89a825f1e1b64083c50cc77731bbadf84d248106d69da9cf737
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119751924"
---
# <a name="cd3dx12_pipeline_state_stream_cached_pso-structure"></a>\_ \_ \_ \_ Структура PSO кэшированного потока состояния конвейера CD3DX12 \_

Вспомогательная структура, используемая для описания кэшированного PSO в виде одного объекта, подходящего для описания потока.

## <a name="syntax"></a>Синтаксис


```C++
struct CD3DX12_PIPELINE_STATE_STREAM_CACHED_PSO {
                                           CD3DX12_PIPELINE_STATE_STREAM_CACHED_PSO;
                                           CD3DX12_PIPELINE_STATE_STREAM_CACHED_PSO(D3D12_CACHED_PIPELINE_STATE const &i);
  CD3DX12_PIPELINE_STATE_STREAM_CACHED_PSO operator=(D3D12_CACHED_PIPELINE_STATE const& i);
                                           operator D3D12_CACHED_PIPELINE_STATE() const;
};
```



## <a name="members"></a>Члены

<dl> <dt>

**\_Поток состояния конвейера CD3DX12, \_ \_ \_ кэшированный \_ PSO**
</dt> <dd>

Создает новый, неинициализированный экземпляр \_ потока состояния конвейера CD3DX12, \_ \_ \_ кэшированного \_ PSO.

</dd> <dt>

**\_Поток состояния конвейера CD3DX12, \_ \_ \_ кэшированный \_ PSO (D3D12 \_ кэшированного \_ состояния конвейера, \_ const &i)**
</dt> <dd>

Создает новый экземпляр \_ потока состояния конвейера CD3DX12 \_ \_ \_ с кэшированием \_ PSO, инициализированный с типом ПОДобъекта типа **\_ \_ подобъекта состояния конвейера D3D12 \_ \_ \_ кэшированные \_ PSO** и данные подобъектов, скопированные из *i*, структуры [**\_ \_ \_ состояния конвейера с кэшированием D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_cached_pipeline_state) .

</dd> <dt>

**operator = (D3D12 \_ кэшированного \_ состояния конвейера \_ const& i)**
</dt> <dd>

Оператор присваивания копирования.

</dd> <dt>

**\_константа "оператор D3D12 кэшированное \_ состояние конвейера \_ ()"**
</dt> <dd>

Неявное преобразование в структуру [**\_ \_ \_ состояния кэшированного конвейера D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_cached_pipeline_state) .

</dd> </dl>

## <a name="remarks"></a>Remarks

\_Поток состояния конвейера CD3DX12 \_ \_ \_ , кэшированный \_ PSO, является СПЕЦИАЛИЗАЦИей typedef шаблона [**\_ \_ \_ \_ подобъекта потока состояния конвейера CD3DX12**](cd3dx12-pipeline-state-stream-subobject.md) и определяется следующим образом:


```C++
typedef CD3DX12_PIPELINE_STATE_STREAM_SUBOBJECT<D3D12_CACHED_PIPELINE_STATE, D3D12_PIPELINE_STATE_SUBOBJECT_TYPE_CACHED_PSO>
    CD3DX12_PIPELINE_STATE_STREAM_CACHED_PSO;
          
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

 

