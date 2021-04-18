---
title: Структура CD3DX12_PIPELINE_STATE_STREAM_BLEND_DESC (D3dx12. h)
description: Вспомогательная структура, используемая для описания описания смешения в виде одного объекта, подходящего для описания потока.
ms.assetid: A629B05D-0A70-4C96-9F66-1508F2667BF6
keywords:
- Структура CD3DX12_PIPELINE_STATE_STREAM_BLEND_DESC
topic_type:
- apiref
api_name:
- CD3DX12_PIPELINE_STATE_STREAM_BLEND_DESC
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d251be9cc1423babc58e1d3c3be87c5345308874
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105694103"
---
# <a name="cd3dx12_pipeline_state_stream_blend_desc-structure"></a>\_Структура по \_ потоку состояния конвейера CD3DX12 \_ \_ Blend \_

Вспомогательная структура, используемая для описания описания смешения в виде одного объекта, подходящего для описания потока.

## <a name="syntax"></a>Синтаксис


```C++
struct CD3DX12_PIPELINE_STATE_STREAM_BLEND_DESC {
                                           CD3DX12_PIPELINE_STATE_STREAM_BLEND_DESC;
                                           CD3DX12_PIPELINE_STATE_STREAM_BLEND_DESC(CD3DX12_BLEND_DESC const &i);
  CD3DX12_PIPELINE_STATE_STREAM_BLEND_DESC operator=(CD3DX12_BLEND_DESC const& i);
                                           operator CD3DX12_BLEND_DESC() const;
};
```



## <a name="members"></a>Члены

<dl> <dt>

**CD3DX12 \_ конвейера \_ состояния \_ потока \_ Blend \_**
</dt> <dd>

Создает новый, неинициализированный экземпляр \_ потока состояния конвейера CD3DX12 \_ \_ \_ Blend \_ .

</dd> <dt>

**\_Поток состояния конвейера CD3DX12 \_ \_ \_ Blend \_ (desc, CD3DX12 \_ Blend, \_ const &i)**
</dt> <dd>

Создает новый экземпляр \_ потока состояния конвейера CD3DX12 \_ \_ \_ Blend \_ , инициализированного с типом подобъекта для типа данных **\_ \_ \_ подобъекта состояния \_ \_ конвейера D3D12 "Blend** " и "подобъект", скопированных из *i*, структуры [**CD3DX12 \_ Blend \_ DESC**](cd3dx12-blend-desc.md) .

</dd> <dt>

**оператор = (CD3DX12 \_ Blend \_ DESC const& i)**
</dt> <dd>

Оператор присваивания копирования.

</dd> <dt>

**Оператор CD3DX12 \_ Blend \_ DESC () const**
</dt> <dd>

Неявное преобразование в структуру [**\_ \_ DESC CD3DX12 Blend**](cd3dx12-blend-desc.md) .

</dd> </dl>

## <a name="remarks"></a>Комментарии

\_Поток состояния конвейера CD3DX12 \_ \_ \_ Blend \_ является СПЕЦИАЛИЗАЦИей typedef шаблона [**\_ \_ \_ \_ подобъекта потока состояния конвейера CD3DX12**](cd3dx12-pipeline-state-stream-subobject.md) и определяется следующим образом:


```C++
typedef CD3DX12_PIPELINE_STATE_STREAM_SUBOBJECT<CD3DX12_BLEND_DESC, D3D12_PIPELINE_STATE_SUBOBJECT_TYPE_BLEND, CD3DX12_DEFAULT>
    CD3DX12_PIPELINE_STATE_STREAM_BLEND_DESC;
          
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

 

