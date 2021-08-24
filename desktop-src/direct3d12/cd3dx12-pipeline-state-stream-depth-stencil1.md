---
title: Структура CD3DX12_PIPELINE_STATE_STREAM_DEPTH_STENCIL1 (D3dx12. h)
description: Вспомогательная структура, используемая для описания описания трафарета глубины в виде одного объекта, подходящего для описания потока. | Структура CD3DX12_PIPELINE_STATE_STREAM_DEPTH_STENCIL1 (D3dx12. h)
ms.assetid: 7D3554D9-610D-43B5-94F0-68167E966A86
keywords:
- Структура CD3DX12_PIPELINE_STATE_STREAM_DEPTH_STENCIL1
topic_type:
- apiref
api_name:
- CD3DX12_PIPELINE_STATE_STREAM_DEPTH_STENCIL1
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3f04064a7ab4a7ca100e48da2446501d4415b693ce6abdf213f121952cc8f198
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119632533"
---
# <a name="cd3dx12_pipeline_state_stream_depth_stencil1-structure"></a>\_ \_ \_ \_ Структура STENCIL1 глубины потока состояния конвейера CD3DX12 \_

Вспомогательная структура, используемая для описания описания трафарета глубины в виде одного объекта, подходящего для описания потока.

## <a name="syntax"></a>Синтаксис


```C++
struct CD3DX12_PIPELINE_STATE_STREAM_DEPTH_STENCIL1 {
                                               CD3DX12_PIPELINE_STATE_STREAM_DEPTH_STENCIL1;
                                               CD3DX12_PIPELINE_STATE_STREAM_DEPTH_STENCIL1(CD3DX12_DEPTH_STENCIL_DESC1 const &i);
  CD3DX12_PIPELINE_STATE_STREAM_DEPTH_STENCIL1 operator=(CD3DX12_DEPTH_STENCIL_DESC1 const& i);
                                               operator CD3DX12_DEPTH_STENCIL_DESC1() const;
};
```



## <a name="members"></a>Члены

<dl> <dt>

**\_ \_ Глубина потока состояния конвейера CD3DX12 \_ \_ \_ STENCIL1**
</dt> <dd>

Создает новый, неинициализированный экземпляр CD3DX12 \_ \_ глубины потока состояния конвейера \_ \_ \_ STENCIL1.

</dd> <dt>

**\_ \_ Глубина потока состояния конвейера CD3DX12 \_ \_ \_ STENCIL1 ( \_ \_ набор элементов глубины CD3DX12 \_ DESC1 const &i)**
</dt> <dd>

Создает новый экземпляр CD3DX12 \_ \_ глубины потока состояния конвейера \_ \_ \_ (STENCIL1), инициализируемый с типом подобъекта для типа **\_ \_ \_ \_ \_ вложенного \_ объекта состояния конвейера D3D12** , который копируется STENCIL1 и данные подобъектов, скопированные из *i*, CD3DX12 структуру [**\_ \_ набора элементов \_ глубины**](cd3dx12-depth-stencil-desc1.md) DESC1.

</dd> <dt>

**operator = (CD3DX12 \_ \_ набор элементов глубины \_ DESC1 const& i)**
</dt> <dd>

Оператор присваивания копирования.

</dd> <dt>

**\_ \_ константа CD3DX12 шаблона глубины \_ DESC1 () const**
</dt> <dd>

Неявное преобразование в структуру [**\_ \_ \_ DESC1 шаблона глубины CD3DX12**](cd3dx12-depth-stencil-desc1.md) .

</dd> </dl>

## <a name="remarks"></a>Remarks

\_ \_ Глубина потока состояния конвейера CD3DX12 \_ \_ \_ STENCIL1 является СПЕЦИАЛИЗАЦИей typedef шаблона [**\_ \_ \_ \_ подобъекта потока состояния конвейера CD3DX12**](cd3dx12-pipeline-state-stream-subobject.md) и определяется следующим образом:


```C++
typedef CD3DX12_PIPELINE_STATE_STREAM_SUBOBJECT<CD3DX12_DEPTH_STENCIL_DESC1, D3D12_PIPELINE_STATE_SUBOBJECT_TYPE_DEPTH_STENCIL1, CD3DX12_DEFAULT>
    CD3DX12_PIPELINE_STATE_STREAM_DEPTH_STENCIL1;
          
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

 

