---
title: Структура CD3DX12_PIPELINE_STATE_STREAM_IB_STRIP_CUT_VALUE (D3dx12. h)
description: Вспомогательная структура, используемая для описания значения вырезания полосы буфера индексов в виде одного объекта, подходящего для описания потока.
ms.assetid: AF8F0919-4601-4A95-832A-5E1DA0304939
keywords:
- Структура CD3DX12_PIPELINE_STATE_STREAM_IB_STRIP_CUT_VALUE
topic_type:
- apiref
api_name:
- CD3DX12_PIPELINE_STATE_STREAM_IB_STRIP_CUT_VALUE
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1e204b4f89cced7cf0bd5cdcb21702c37c241a81abfbc12d8644eafdb3c7c7ae
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119988414"
---
# <a name="cd3dx12_pipeline_state_stream_ib_strip_cut_value-structure"></a>\_ \_ \_ \_ \_ \_ Структура значения ВЫРЕЗАНного потока состояния \_ конвейера CD3DX12

Вспомогательная структура, используемая для описания значения вырезания полосы буфера индексов в виде одного объекта, подходящего для описания потока.

## <a name="syntax"></a>Синтаксис


```C++
struct CD3DX12_PIPELINE_STATE_STREAM_IB_STRIP_CUT_VALUE {
                                                   CD3DX12_PIPELINE_STATE_STREAM_IB_STRIP_CUT_VALUE;
                                                   CD3DX12_PIPELINE_STATE_STREAM_IB_STRIP_CUT_VALUE(D3D12_INDEX_BUFFER_STRIP_CUT_VALUE const &i);
  CD3DX12_PIPELINE_STATE_STREAM_IB_STRIP_CUT_VALUE operator=(D3D12_INDEX_BUFFER_STRIP_CUT_VALUE const& i);
                                                   operator D3D12_INDEX_BUFFER_STRIP_CUT_VALUE() const;
};
```



## <a name="members"></a>Члены

<dl> <dt>

**\_Поток состояния конвейера CD3DX12. \_ \_ \_ \_ \_ вырезание значения чередования \_**
</dt> <dd>

Создает новый, неинициализированный экземпляр \_ потока состояния конвейера CD3DX12, \_ \_ \_ \_ \_ вырезаемого значения полосы \_ .

</dd> <dt>

**\_Поток состояния конвейера CD3DX12 \_ \_ \_ \_ \_ : вырезание значения вырезания \_ ( \_ буфер D3D12 индексов \_ \_ \_ вырезанное \_ значение const &i)**
</dt> <dd>

Создает новый экземпляр \_ потока состояний конвейера CD3DX12, который приводит к \_ \_ \_ \_ \_ сокращению значения вырезания чередования \_ , инициализированного с типом подобъекта типа **\_ \_ подобъекта состояния конвейера D3D12 область \_ \_ \_ \_ \_ \_ вырезания** и данные подобъекта, скопированные из *i*, область [**\_ буфера D3D12 индексов \_ \_ \_ вырезанная структура \_ значения**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_index_buffer_strip_cut_value) .

</dd> <dt>

**operator = (D3D12 \_ Индекс \_ \_ полоса \_ вырезание \_ значения const& i)**
</dt> <dd>

Оператор присваивания копирования.

</dd> <dt>

**Оператор D3D12 \_ Индекс \_ \_ полоса \_ вырезанного \_ значения () const**
</dt> <dd>

Неявное преобразование в структуру [**\_ буфера D3D12 индекса \_ \_ полосы \_ вырезания \_ значений**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_index_buffer_strip_cut_value) .

</dd> </dl>

## <a name="remarks"></a>Remarks

\_ \_ \_ Значение вырезания потока состояния конвейера CD3DX12 \_ \_ \_ \_ является специализацией typedef шаблона [**\_ \_ \_ \_ подобъекта потока состояния конвейера CD3DX12**](cd3dx12-pipeline-state-stream-subobject.md) и определяется следующим образом:


```C++
typedef CD3DX12_PIPELINE_STATE_STREAM_SUBOBJECT<D3D12_INDEX_BUFFER_STRIP_CUT_VALUE, D3D12_PIPELINE_STATE_SUBOBJECT_TYPE_IB_STRIP_CUT_VALUE>
    CD3DX12_PIPELINE_STATE_STREAM_IB_STRIP_CUT_VALUE;
          
```



## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------|-------------------------------------------------------------------------------------|
| Заголовок<br/> | <dl> <dt>D3dx12. h</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[Вспомогательные структуры для D3D12](helper-structures-for-d3d12.md)
</dt> <dt>

[**\_Подобъект \_ потока состояния КОНВЕЙЕРа CD3DX12 \_ \_**](cd3dx12-pipeline-state-stream-subobject.md)
</dt> <dt>

[**\_ \_ \_ Тип подобъекта состояния конвейера D3D12 \_**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_pipeline_state_subobject_type)
</dt> </dl>

 

