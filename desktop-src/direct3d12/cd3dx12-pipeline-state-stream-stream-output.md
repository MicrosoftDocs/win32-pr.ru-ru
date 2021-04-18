---
title: Структура CD3DX12_PIPELINE_STATE_STREAM_STREAM_OUTPUT (D3dx12. h)
description: Вспомогательная структура, используемая для описания выходного описания потока в виде одного объекта, подходящего для описания потока.
ms.assetid: CC7E1E76-CD44-4D70-A5B8-7C2B6210468E
keywords:
- Структура CD3DX12_PIPELINE_STATE_STREAM_STREAM_OUTPUT
topic_type:
- apiref
api_name:
- CD3DX12_PIPELINE_STATE_STREAM_STREAM_OUTPUT
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: acc8f7bf059c4eee72b0b22abfc424ee82ffd2dc
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105713521"
---
# <a name="cd3dx12_pipeline_state_stream_stream_output-structure"></a>\_ \_ \_ \_ Выходная структура потока состояния конвейера CD3DX12 \_

Вспомогательная структура, используемая для описания выходного описания потока в виде одного объекта, подходящего для описания потока.

## <a name="syntax"></a>Синтаксис


```C++
struct CD3DX12_PIPELINE_STATE_STREAM_STREAM_OUTPUT {
                                              CD3DX12_PIPELINE_STATE_STREAM_STREAM_OUTPUT;
                                              CD3DX12_PIPELINE_STATE_STREAM_STREAM_OUTPUT(D3D12_STREAM_OUTPUT_DESC const &i);
  CD3DX12_PIPELINE_STATE_STREAM_STREAM_OUTPUT operator=(D3D12_STREAM_OUTPUT_DESC const& i);
                                              operator D3D12_STREAM_OUTPUT_DESC() const;
};
```



## <a name="members"></a>Члены

<dl> <dt>

**\_ \_ \_ \_ Выходные данные потока состояния конвейера \_ CD3DX12**
</dt> <dd>

Создает новый, неинициализированный экземпляр потока \_ вывода потока состояния конвейера \_ CD3DX12 \_ \_ \_ .

</dd> <dt>

**Потоковая передача потока \_ состояния конвейера CD3DX12 \_ \_ \_ \_ ( \_ потоковая передача D3D12 \_ OUTPUT \_ const &i)**
</dt> <dd>

Создает новый экземпляр потокового вывода потока \_ состояния конвейера CD3DX12 \_ \_ \_ \_ , инициализированного с типом подобъекта потока данных **о \_ \_ \_ \_ типе \_ \_ подобъекта состояния конвейера D3D12** и данных подобъекта, скопированных из *i*, [**\_ \_ выходную структуру вывода \_ потока D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_stream_output_desc) .

</dd> <dt>

**operator = (D3D12 \_ поток \_ вывода Output \_ const,& i)**
</dt> <dd>

Оператор присваивания копирования.

</dd> <dt>

**Оператор D3D12 \_ потока \_ OUTPUT \_ () const**
</dt> <dd>

Неявное преобразование в структуру [**\_ \_ вывода \_ потока D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_stream_output_desc) .

</dd> </dl>

## <a name="remarks"></a>Комментарии

\_Выходной поток потока состояния конвейера CD3DX12 \_ \_ \_ \_ является СПЕЦИАЛИЗАЦИей typedef шаблона [**\_ \_ \_ \_ подобъекта потока состояния конвейера CD3DX12**](cd3dx12-pipeline-state-stream-subobject.md) и определяется следующим образом:


```C++
typedef CD3DX12_PIPELINE_STATE_STREAM_SUBOBJECT<D3D12_STREAM_OUTPUT_DESC, D3D12_PIPELINE_STATE_SUBOBJECT_TYPE_STREAM_OUTPUT>
    CD3DX12_PIPELINE_STATE_STREAM_STREAM_OUTPUT;
          
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

 

