---
title: Структура CD3DX12_PIPELINE_STATE_STREAM_DEPTH_STENCIL (D3dx12. h)
description: Вспомогательная структура, используемая для описания описания трафарета глубины в виде одного объекта, подходящего для описания потока. | Структура CD3DX12_PIPELINE_STATE_STREAM_DEPTH_STENCIL (D3dx12. h)
ms.assetid: 4FB54EA5-FCC6-4B64-A747-27DFE4C1D2DC
keywords:
- Структура CD3DX12_PIPELINE_STATE_STREAM_DEPTH_STENCIL
topic_type:
- apiref
api_name:
- CD3DX12_PIPELINE_STATE_STREAM_DEPTH_STENCIL
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e0b9cc7ba6b37858ae355d9470f321f991e8329f5fbf7aabd23b6f8bcfe7d8fa
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119858184"
---
# <a name="cd3dx12_pipeline_state_stream_depth_stencil-structure"></a>\_ \_ \_ \_ \_ Структура набора элементов глубины потока состояния конвейера CD3DX12

Вспомогательная структура, используемая для описания описания трафарета глубины в виде одного объекта, подходящего для описания потока.

## <a name="syntax"></a>Синтаксис


```C++
struct CD3DX12_PIPELINE_STATE_STREAM_DEPTH_STENCIL {
                                              CD3DX12_PIPELINE_STATE_STREAM_DEPTH_STENCIL;
                                              CD3DX12_PIPELINE_STATE_STREAM_DEPTH_STENCIL(CD3DX12_DEPTH_STENCIL_DESC const &i);
  CD3DX12_PIPELINE_STATE_STREAM_DEPTH_STENCIL operator=(CD3DX12_DEPTH_STENCIL_DESC const& i);
                                              operator CD3DX12_DEPTH_STENCIL_DESC() const;
};
```



## <a name="members"></a>Члены

<dl> <dt>

**\_ \_ \_ \_ Трафарет глубины потока состояния конвейера CD3DX12 \_**
</dt> <dd>

Создает новый, неинициализированный экземпляр \_ \_ \_ \_ набора элементов глубины потока состояния конвейера CD3DX12 \_ .

</dd> <dt>

**\_ \_ Трафарет глубины потока состояния конвейера CD3DX12 \_ \_ \_ ( \_ набор элементов глубины CD3DX12, \_ \_ появляющееся константой DESC &i)**
</dt> <dd>

Создает новый экземпляр \_ \_ \_ трафарета глубины потока состояния конвейера \_ CD3DX12 \_ , инициализированный с типом подобъекта для типа **\_ контейнера \_ \_ \_ \_ глубины \_ конвейера "состояние** подобъекта", и данные подобъекта, скопированные из *i*, структура [**\_ \_ трафарета \_ глубины CD3DX12**](cd3dx12-depth-stencil-desc.md) .

</dd> <dt>

**operator = (CD3DX12 \_ \_ набор элементов глубины, \_ const& i)**
</dt> <dd>

Оператор присваивания копирования.

</dd> <dt>

**\_ \_ константа CD3DX12 шаблона глубины набора элементов \_ "оператор"**
</dt> <dd>

Неявное преобразование в структуру [**CD3DX12 \_ \_ набора элементов \_ глубины**](cd3dx12-depth-stencil-desc.md) .

</dd> </dl>

## <a name="remarks"></a>Remarks

\_ \_ \_ Набор элементов глубины потока состояния конвейера CD3DX12 \_ \_ является СПЕЦИАЛИЗАЦИей typedef [**шаблона \_ \_ \_ \_ подобъекта потока состояния конвейера CD3DX12**](cd3dx12-pipeline-state-stream-subobject.md) и определяется следующим образом:


```C++
typedef CD3DX12_PIPELINE_STATE_STREAM_SUBOBJECT<CD3DX12_DEPTH_STENCIL_DESC, D3D12_PIPELINE_STATE_SUBOBJECT_TYPE_DEPTH_STENCIL, CD3DX12_DEFAULT>
    CD3DX12_PIPELINE_STATE_STREAM_DEPTH_STENCIL;
          
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

 

