---
title: Структура CD3DX12_PIPELINE_STATE_STREAM_RASTERIZER (D3dx12. h)
description: Вспомогательная структура, используемая для описания описания средства развертки в виде одного объекта, подходящего для описания потока.
ms.assetid: 650C2DA3-63FB-44D1-BE9A-E21E13DA24DB
keywords:
- Структура CD3DX12_PIPELINE_STATE_STREAM_RASTERIZER
topic_type:
- apiref
api_name:
- CD3DX12_PIPELINE_STATE_STREAM_RASTERIZER
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f656ad354430b00e757ece0aa2ce482de1f06e2e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105694093"
---
# <a name="cd3dx12_pipeline_state_stream_rasterizer-structure"></a>Структура средства программной \_ \_ \_ прорисовки потока состояния конвейера CD3DX12 \_

Вспомогательная структура, используемая для описания описания средства развертки в виде одного объекта, подходящего для описания потока.

## <a name="syntax"></a>Синтаксис


```C++
struct CD3DX12_PIPELINE_STATE_STREAM_RASTERIZER {
                                           CD3DX12_PIPELINE_STATE_STREAM_RASTERIZER;
                                           CD3DX12_PIPELINE_STATE_STREAM_RASTERIZER(CD3DX12_RASTERIZER_DESC const &i);
  CD3DX12_PIPELINE_STATE_STREAM_RASTERIZER operator=(CD3DX12_RASTERIZER_DESC const& i);
                                           operator CD3DX12_RASTERIZER_DESC() const;
};
```



## <a name="members"></a>Члены

<dl> <dt>

**Средство программной \_ \_ \_ прорисовки потока состояния конвейера CD3DX12 \_**
</dt> <dd>

Создает новый, неинициализированный экземпляр средства программной \_ \_ прорисовки потока состояния конвейера CD3DX12 \_ \_ .

</dd> <dt>

**Средство программной \_ \_ прорисовки потока состояния конвейера CD3DX12 (CD3DX12 средство программной \_ \_ \_ прорисовки \_ DESC const &i)**
</dt> <dd>

Создает новый экземпляр средства программной \_ \_ прорисовки потока состояния конвейера CD3DX12, инициализированного с типом подобъекта для типа подобъекта \_ \_ **\_ \_ состояния \_ \_ \_ конвейера D3D12** и данными подобъекта, скопированными из *i*, структурой [**\_ \_ DESC средства прорисовки CD3DX12**](cd3dx12-rasterizer-desc.md) .

</dd> <dt>

**operator = (CD3DX12 средство программной \_ прорисовки \_ DESC const& i)**
</dt> <dd>

Оператор присваивания копирования.

</dd> <dt>

**const CD3DX12 "оператор средства \_ растеризации \_ DESC ()"**
</dt> <dd>

Неявное преобразование в структуру CD3DX12 средства программной [**\_ прорисовки \_**](cd3dx12-rasterizer-desc.md) .

</dd> </dl>

## <a name="remarks"></a>Комментарии

Средство программной \_ \_ прорисовки потока состояния конвейера CD3DX12 \_ \_ является специализацией typedef шаблона [**\_ \_ \_ \_ подобъекта потока состояния конвейера CD3DX12**](cd3dx12-pipeline-state-stream-subobject.md) и определяется следующим образом:


```C++
typedef CD3DX12_PIPELINE_STATE_STREAM_SUBOBJECT<CD3DX12_RASTERIZER_DESC, D3D12_PIPELINE_STATE_SUBOBJECT_TYPE_RASTERIZER, CD3DX12_DEFAULT>
    CD3DX12_PIPELINE_STATE_STREAM_RASTERIZER;
          
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

 

