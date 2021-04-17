---
title: Структура CD3DX12_PIPELINE_STATE_STREAM_SAMPLE_DESC (D3dx12. h)
description: Вспомогательная структура, используемая для описания образца описания как одного объекта, подходящего для описания потока.
ms.assetid: D84C5373-AC0F-430A-97A1-6125611869B2
keywords:
- Структура CD3DX12_PIPELINE_STATE_STREAM_SAMPLE_DESC
topic_type:
- apiref
api_name:
- CD3DX12_PIPELINE_STATE_STREAM_SAMPLE_DESC
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5fea786dc0429da28f9c26f0203b06059aff1c17
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105694313"
---
# <a name="cd3dx12_pipeline_state_stream_sample_desc-structure"></a>\_ \_ \_ \_ Структура примера потока состояния конвейера CD3DX12 \_

Вспомогательная структура, используемая для описания образца описания как одного объекта, подходящего для описания потока.

## <a name="syntax"></a>Синтаксис


```C++
struct CD3DX12_PIPELINE_STATE_STREAM_SAMPLE_DESC {
                                            CD3DX12_PIPELINE_STATE_STREAM_SAMPLE_DESC;
                                            CD3DX12_PIPELINE_STATE_STREAM_SAMPLE_DESC(DXGI_SAMPLE_DESC const &i);
  CD3DX12_PIPELINE_STATE_STREAM_SAMPLE_DESC operator=(DXGI_SAMPLE_DESC const& i);
                                            operator DXGI_SAMPLE_DESC() const;
};
```



## <a name="members"></a>Члены

<dl> <dt>

**\_ \_ \_ \_ Пример DESC потока состояния конвейера CD3DX12 \_**
</dt> <dd>

Создает новый, неинициализированный экземпляр \_ \_ примера потока состояния конвейера CD3DX12 \_ \_ \_ .

</dd> <dt>

**\_ \_ Пример DESC потока состояния конвейера CD3DX12 \_ \_ \_ ( \_ пример тестовой среды DXGI \_ const &i)**
</dt> <dd>

Создает новый экземпляр \_ \_ примера потока состояния конвейера CD3DX12 \_ \_ \_ , инициализированного с типом ПОДобъекта типа **\_ \_ подобъекта состояния конвейера D3D12 \_ \_ \_ образец \_ DESC** и данные подобъекта, скопированные из *i*, [**\_ пример \_ DESC**](https://www.bing.com/search?q=**DXGI\_SAMPLE\_DESC**) структуры для DXGI.

</dd> <dt>

**operator = (пример примера в DXGI " \_ \_ const"& i)**
</dt> <dd>

Оператор присваивания копирования.

</dd> <dt>

**оператор " \_ пример \_ DESC" для оператора DXGI () const**
</dt> <dd>

Неявное преобразование в структуру [**\_ \_ DESC образца**](https://www.bing.com/search?q=**DXGI\_SAMPLE\_DESC**) в виде DXGI.

</dd> </dl>

## <a name="remarks"></a>Комментарии

\_ \_ Пример DESC потока состояния конвейера CD3DX12 \_ \_ \_ является СПЕЦИАЛИЗАЦИей typedef шаблона [**\_ \_ \_ \_ подобъекта потока состояния конвейера CD3DX12**](cd3dx12-pipeline-state-stream-subobject.md) и определяется следующим образом:


```C++
typedef CD3DX12_PIPELINE_STATE_STREAM_SUBOBJECT<DXGI_SAMPLE_DESC, D3D12_PIPELINE_STATE_SUBOBJECT_TYPE_SAMPLE_DESC>
    CD3DX12_PIPELINE_STATE_STREAM_SAMPLE_DESC;
          
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

 

