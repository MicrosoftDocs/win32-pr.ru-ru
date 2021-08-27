---
title: Структура CD3DX12_PIPELINE_STATE_STREAM_NODE_MASK (D3dx12. h)
description: Вспомогательная структура, используемая для описания маски узла в виде одного объекта, подходящего для описания потока.
ms.assetid: 5C770D9A-D692-46CF-8D60-EE5EB04998C8
keywords:
- Структура CD3DX12_PIPELINE_STATE_STREAM_NODE_MASK
topic_type:
- apiref
api_name:
- CD3DX12_PIPELINE_STATE_STREAM_NODE_MASK
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0f4850ff986f2006c506d79a8ece1ced873529c2a4939869cd704a4b7c3c4b03
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120119684"
---
# <a name="cd3dx12_pipeline_state_stream_node_mask-structure"></a>\_ \_ \_ \_ Структура маски узла потока состояния конвейера CD3DX12 \_

Вспомогательная структура, используемая для описания маски узла в виде одного объекта, подходящего для описания потока.

## <a name="syntax"></a>Синтаксис


```C++
struct CD3DX12_PIPELINE_STATE_STREAM_NODE_MASK {
                                          CD3DX12_PIPELINE_STATE_STREAM_NODE_MASK;
                                          CD3DX12_PIPELINE_STATE_STREAM_NODE_MASK(UINT const &i);
  CD3DX12_PIPELINE_STATE_STREAM_NODE_MASK operator=(UINT const& i);
                                          operator UINT() const;
};
```



## <a name="members"></a>Члены

<dl> <dt>

**\_ \_ \_ \_ Маска узла потока состояния конвейера CD3DX12 \_**
</dt> <dd>

Создает новый, неинициализированный экземпляр \_ \_ \_ маски узла потока состояния конвейера CD3DX12 \_ \_ .

</dd> <dt>

**CD3DX12 \_ \_ \_ Маска узла потока состояния конвейера \_ \_ (uint const &i)**
</dt> <dd>

Создает новый экземпляр \_ \_ маски узла потока состояния конвейера \_ CD3DX12 \_ \_ , инициализированный с типом подобъекта для типа **\_ \_ подобъекта состояния конвейера D3D12 " \_ \_ \_ \_ Маска узла** " и "данные подобъекта", скопированные из *i*, маску узла **uint** .

</dd> <dt>

**operator = (Конст const& i)**
</dt> <dd>

Оператор присваивания копирования.

</dd> <dt>

**const оператора UINT ()**
</dt> <dd>

Неявное преобразование в маску узла **uint** .

</dd> </dl>

## <a name="remarks"></a>Remarks

\_ \_ Маска узла потока состояния конвейера CD3DX12 \_ \_ \_ является СПЕЦИАЛИЗАЦИей typedef шаблона [**\_ \_ \_ \_ подобъекта потока состояния конвейера CD3DX12**](cd3dx12-pipeline-state-stream-subobject.md) и определяется следующим образом:


```C++
typedef CD3DX12_PIPELINE_STATE_STREAM_SUBOBJECT<UINT, D3D12_PIPELINE_STATE_SUBOBJECT_TYPE_NODE_MASK>
    CD3DX12_PIPELINE_STATE_STREAM_NODE_MASK;
          
```



## <a name="requirements"></a>Требования



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

 

