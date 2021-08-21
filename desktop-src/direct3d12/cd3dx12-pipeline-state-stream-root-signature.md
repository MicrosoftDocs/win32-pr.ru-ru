---
title: Структура CD3DX12_PIPELINE_STATE_STREAM_ROOT_SIGNATURE (D3dx12. h)
description: Вспомогательная структура, используемая для описания корневой подписи в виде одного объекта, подходящего для описания потока.
ms.assetid: 351A78DC-9BDE-43B4-9A72-D65EE15CA441
keywords:
- Структура CD3DX12_PIPELINE_STATE_STREAM_ROOT_SIGNATURE
topic_type:
- apiref
api_name:
- CD3DX12_PIPELINE_STATE_STREAM_ROOT_SIGNATURE
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ccddd5663b6a079656823efed4cb48b3183d88d0688149c7ae05d96e8dc1cdd9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118530705"
---
# <a name="cd3dx12_pipeline_state_stream_root_signature-structure"></a>\_ \_ \_ \_ Структура подписи корневого потока состояния конвейера CD3DX12 \_

Вспомогательная структура, используемая для описания корневой подписи в виде одного объекта, подходящего для описания потока.

## <a name="syntax"></a>Синтаксис


```C++
struct CD3DX12_PIPELINE_STATE_STREAM_ROOT_SIGNATURE {
                                               CD3DX12_PIPELINE_STATE_STREAM_ROOT_SIGNATURE;
                                               CD3DX12_PIPELINE_STATE_STREAM_ROOT_SIGNATURE(ID3D12RootSignature* const &i);
  CD3DX12_PIPELINE_STATE_STREAM_ROOT_SIGNATURE operator=(ID3D12RootSignature* const& i);
                                               operator ID3D12RootSignature*() const;
};
```



## <a name="members"></a>Члены

<dl> <dt>

**\_ \_ \_ \_ Корневая подпись потока состояния конвейера CD3DX12 \_**
</dt> <dd>

Создает новый, неинициализированный экземпляр \_ \_ \_ \_ корневой подписи потока состояния конвейера CD3DX12 \_ .

</dd> <dt>

**\_ \_ Корневая подпись потока состояния конвейера CD3DX12 \_ \_ \_ (ID3D12RootSignature \* const &i)**
</dt> <dd>

Создает новый экземпляр \_ \_ \_ корневой сигнатуры потока состояния конвейера CD3DX12 \_ \_ , инициализированный с типом подобъекта для **типа \_ \_ подобъекта состояния конвейера D3D12 \_ \_ \_ корневая \_ подпись** и данные подобъекта, скопированные из *i*, структуры [**ID3D12RootSignature**](/windows/desktop/api/d3d12/nn-d3d12-id3d12rootsignature) .

</dd> <dt>

**оператор = (ID3D12RootSignature \* const& i)**
</dt> <dd>

Оператор присваивания копирования.

</dd> <dt>

**const оператора ID3D12RootSignature \* ()**
</dt> <dd>

Неявное преобразование в указатель структуры [**ID3D12RootSignature**](/windows/desktop/api/d3d12/nn-d3d12-id3d12rootsignature) .

</dd> </dl>

## <a name="remarks"></a>Remarks

\_ \_ \_ Корневая сигнатура потока состояния конвейера CD3DX12 \_ \_ является СПЕЦИАЛИЗАЦИей typedef [**шаблона \_ \_ \_ \_ подобъекта потока состояния конвейера CD3DX12**](cd3dx12-pipeline-state-stream-subobject.md) и определяется следующим образом:


```C++
typedef CD3DX12_PIPELINE_STATE_STREAM_SUBOBJECT<ID3D12RootSignature*, D3D12_PIPELINE_STATE_SUBOBJECT_TYPE_ROOT_SIGNATURE>
    CD3DX12_PIPELINE_STATE_STREAM_ROOT_SIGNATURE;
          
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

 

