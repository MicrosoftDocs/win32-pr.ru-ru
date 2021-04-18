---
title: Структура CD3DX12_PIPELINE_STATE_STREAM_SAMPLE_MASK (D3dx12. h)
description: Вспомогательная структура, используемая для описания образца маски в виде одного объекта, подходящего для описания потока.
ms.assetid: 20116DA1-F56D-42CA-A846-42509FAF88C1
keywords:
- Структура CD3DX12_PIPELINE_STATE_STREAM_SAMPLE_MASK
topic_type:
- apiref
api_name:
- CD3DX12_PIPELINE_STATE_STREAM_SAMPLE_MASK
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 868a498bec1bbf8c4f55f320765272d04cbdd81c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105694312"
---
# <a name="cd3dx12_pipeline_state_stream_sample_mask-structure"></a>\_ \_ \_ \_ Структура маски образца потока состояния конвейера CD3DX12 \_

Вспомогательная структура, используемая для описания образца маски в виде одного объекта, подходящего для описания потока.

## <a name="syntax"></a>Синтаксис


```C++
struct CD3DX12_PIPELINE_STATE_STREAM_SAMPLE_MASK {
                                            CD3DX12_PIPELINE_STATE_STREAM_SAMPLE_MASK;
                                            CD3DX12_PIPELINE_STATE_STREAM_SAMPLE_MASK(UINT const &i);
  CD3DX12_PIPELINE_STATE_STREAM_SAMPLE_MASK operator=(UINT const& i);
                                            operator UINT() const;
};
```



## <a name="members"></a>Члены

<dl> <dt>

**\_ \_ \_ \_ Образец маски потока состояния конвейера CD3DX12 \_**
</dt> <dd>

Создает новый, неинициализированный экземпляр \_ \_ \_ образца маски потока состояния конвейера CD3DX12 \_ \_ .

</dd> <dt>

**\_ \_ Пример маски потока состояния конвейера CD3DX12 \_ \_ \_ (uint const &i)**
</dt> <dd>

Создает новый экземпляр \_ \_ образца маски потока состояния конвейера \_ CD3DX12 \_ \_ , инициализированный с типом ПОДобъекта типа **\_ \_ \_ подобъекта состояния конвейера D3D12 \_ \_ образец \_ маски** и данных подобъекта, скопированных из *i*, с помощью образца маски **uint** .

</dd> <dt>

**operator = (Конст const& i)**
</dt> <dd>

Оператор присваивания копирования.

</dd> <dt>

**const оператора UINT ()**
</dt> <dd>

Неявное преобразование в образец маски **uint** .

</dd> </dl>

## <a name="remarks"></a>Комментарии

\_ \_ Пример маски потока состояния конвейера CD3DX12 \_ \_ \_ является СПЕЦИАЛИЗАЦИей typedef шаблона [**\_ \_ \_ \_ подобъекта потока состояния конвейера CD3DX12**](cd3dx12-pipeline-state-stream-subobject.md) и определяется следующим образом:


```C++
typedef CD3DX12_PIPELINE_STATE_STREAM_SUBOBJECT<UINT, D3D12_PIPELINE_STATE_SUBOBJECT_TYPE_SAMPLE_MASK>
    CD3DX12_PIPELINE_STATE_STREAM_SAMPLE_MASK;
          
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

 

