---
title: Структура CD3DX12_PIPELINE_STATE_STREAM_SUBOBJECT (D3dx12. h)
description: Шаблонная вспомогательная структура, используемая для инкапсуляции типа подобъекта и пар данных подобъектов в виде одного объекта, подходящего для описания потока.
ms.assetid: 4C59D483-6ED8-49BD-B91B-2A912AFE2409
keywords:
- Структура CD3DX12_PIPELINE_STATE_STREAM_SUBOBJECT
topic_type:
- apiref
api_name:
- CD3DX12_PIPELINE_STATE_STREAM_SUBOBJECT
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 11353581dddc2bd0d438b955d1292b667fba39ad
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105713982"
---
# <a name="cd3dx12_pipeline_state_stream_subobject-structure"></a>\_ \_ \_ \_ Структура подобъекта потока состояния конвейера CD3DX12

Шаблонная вспомогательная структура, используемая для инкапсуляции типа подобъекта и пар данных подобъектов в виде одного объекта, подходящего для описания потока.

## <a name="syntax"></a>Синтаксис


```C++
struct CD3DX12_PIPELINE_STATE_STREAM_SUBOBJECT {
                                          CD3DX12_PIPELINE_STATE_STREAM_SUBOBJECT;
                                          CD3DX12_PIPELINE_STATE_STREAM_SUBOBJECT(InnerStructType const &i);
  CD3DX12_PIPELINE_STATE_STREAM_SUBOBJECT operator=(InnerStructType const& i);
                                          operator InnerStructType() const;
};
```



## <a name="members"></a>Члены

<dl> <dt>

**\_Подобъект \_ потока состояния КОНВЕЙЕРа CD3DX12 \_ \_**
</dt> <dd>

Создает новый, неинициализированный экземпляр \_ \_ \_ подобъекта потока состояния конвейера CD3DX12 \_ .

</dd> <dt>

**CD3DX12 \_ \_Подобъект \_ потока \_ состояния конвейера (** иннерструкттипе * * const &i) * *
</dt> <dd>

Создает \_ \_ \_ \_ экземпляр шаблона подобъекта потока состояния конвейера CD3DX12, инициализированный с типом подобъекта типа [**\_ \_ \_ подобъекта \_ состояния конвейера D3D12**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_pipeline_state_subobject_type) и данными подобъекта, скопированными из *i*. Типы подобъекта и тип данных подобъекта указаны как параметры шаблона, **Type** и **иннерструкттипе** соответственно. Дополнительные сведения см. в разделе "Примечания" ниже.

</dd> <dt>

**оператор = (** иннерструкттипе * * const& i) * *
</dt> <dd>

Оператор присваивания копирования.

</dd> <dt>

**const оператора **иннерструкттипе**()**
</dt> <dd>

Неявное преобразование в тип данных подобъекта, заданный параметром шаблона **иннерструкттипе** .

</dd> </dl>

## <a name="remarks"></a>Комментарии

\_Подобъект \_ потока состояния конвейера CD3DX12 \_ \_ — это шаблон, определенный следующим образом:


```C++
template <typename InnerStructType, D3D12_PIPELINE_STATE_SUBOBJECT_TYPE Type, typename DefaultArg = InnerStructType>
class alignas(void*) CD3DX12_PIPELINE_STATE_STREAM_SUBOBJECT
{
private:
    D3D12_PIPELINE_STATE_SUBOBJECT_TYPE _Type;
    InnerStructType _Inner;
public:
    CD3DX12_PIPELINE_STATE_STREAM_SUBOBJECT() : _Type(Type), _Inner(DefaultArg()) {}
    CD3DX12_PIPELINE_STATE_STREAM_SUBOBJECT(InnerStructType const& i) : _Type(Type), _Inner(i) {}
    CD3DX12_PIPELINE_STATE_STREAM_SUBOBJECT& operator=(InnerStructType const& i) { _Inner = i; return *this; }
    operator InnerStructType() const { return _Inner; }
};  
          
```



Параметр шаблона **иннерструкттипе** указывает тип данных подобъекта. то есть сведения о подобъекте, которые должны быть закодированы в поток. **Тип** параметра шаблона задает тип подобъекта; то есть тип структуры, заданный параметром-шаблоном **иннерструкттипе**. Параметр шаблона **дефаултарг** указывает необязательное значение, в которое будут инициализироваться данные подобъекта, когда экземпляр соответствующего шаблона создается по умолчанию. Например, чтобы создать по умолчанию [**\_ \_ поток состояния конвейера \_ CD3DX12 \_ Blend \_**](cd3dx12-pipeline-state-stream-blend-desc.md) , инициализированный с общими режимами смешения по умолчанию с использованием [**CD3DX12 \_ по умолчанию**](cd3dx12-default.md).

Ниже приведены определенные экземпляры шаблонов:

-   [**\_ \_ \_ Флаги потока состояния конвейера CD3DX12 \_**](cd3dx12-pipeline-state-stream-flags.md)
-   [**\_ \_ \_ \_ Маска узла потока состояния конвейера CD3DX12 \_**](cd3dx12-pipeline-state-stream-node-mask.md)
-   [**\_ \_ \_ \_ Корневая подпись потока состояния конвейера CD3DX12 \_**](cd3dx12-pipeline-state-stream-root-signature.md)
-   [**\_ \_ \_ \_ Схема ввода потока состояния конвейера CD3DX12 \_**](cd3dx12-pipeline-state-stream-input-layout.md)
-   [**\_Поток состояния конвейера CD3DX12. \_ \_ \_ \_ \_ вырезание значения чередования \_**](cd3dx12-pipeline-state-stream-ib-strip-cut-value.md)
-   [**\_ \_ \_ \_ Топология примитива потока состояния конвейера CD3DX12 \_**](cd3dx12-pipeline-state-stream-primitive-topology.md)
-   [**\_Поток состояния конвейера CD3DX12 \_ \_ \_ и**](cd3dx12-pipeline-state-stream-vs.md)
-   [**\_ \_ \_ GS потока состояния конвейера CD3DX12 \_**](cd3dx12-pipeline-state-stream-gs.md)
-   [**\_ \_ \_ \_ Выходные данные потока состояния конвейера \_ CD3DX12**](cd3dx12-pipeline-state-stream-stream-output.md)
-   [**\_Поток состояния конвейера CD3DX12 — \_ \_ \_ HS**](cd3dx12-pipeline-state-stream-hs.md)
-   [**\_ \_ \_ DS потока состояния конвейера CD3DX12 \_**](cd3dx12-pipeline-state-stream-ds.md)
-   [**\_Поток состояния конвейера CD3DX12 \_ \_ \_ PS**](cd3dx12-pipeline-state-stream-ps.md)
-   [**\_Поток состояния конвейера CD3DX12 \_ \_ \_ CS**](cd3dx12-pipeline-state-stream-cs.md)
-   [**CD3DX12 \_ конвейера \_ состояния \_ потока \_ Blend \_**](cd3dx12-pipeline-state-stream-blend-desc.md)
-   [**\_ \_ \_ \_ Трафарет глубины потока состояния конвейера CD3DX12 \_**](cd3dx12-pipeline-state-stream-depth-stencil.md)
-   [**\_ \_ Глубина потока состояния конвейера CD3DX12 \_ \_ \_ STENCIL1**](cd3dx12-pipeline-state-stream-depth-stencil1.md)
-   [**\_ \_ \_ \_ \_ Формат трафарета глубины потока состояния конвейера CD3DX12 \_**](cd3dx12-pipeline-state-stream-depth-stencil-format.md)
-   [**Средство программной \_ \_ \_ прорисовки потока состояния конвейера CD3DX12 \_**](cd3dx12-pipeline-state-stream-rasterizer.md)
-   [**\_ \_ \_ \_ \_ Форматы целевого объекта подготовки потока состояния конвейера CD3DX12 \_**](cd3dx12-pipeline-state-stream-render-target-formats.md)
-   [**\_ \_ \_ \_ Пример DESC потока состояния конвейера CD3DX12 \_**](cd3dx12-pipeline-state-stream-sample-desc.md)
-   [**\_ \_ \_ \_ Образец маски потока состояния конвейера CD3DX12 \_**](cd3dx12-pipeline-state-stream-sample-mask.md)
-   [**\_Поток состояния конвейера CD3DX12, \_ \_ \_ кэшированный \_ PSO**](cd3dx12-pipeline-state-stream-cached-pso.md)

Структура потока состояния конвейера [**CD3DX12 \_ \_ \_ \_ Blend \_**](cd3dx12-pipeline-state-stream-blend-desc.md), [**\_ \_ \_ \_ \_ набор элементов глубины потока состояния конвейера CD3DX12**](cd3dx12-pipeline-state-stream-depth-stencil.md), [**\_ \_ глубина потока состояния конвейера CD3DX12 STENCIL1 \_ \_ \_**](cd3dx12-pipeline-state-stream-depth-stencil1.md)и [**CD3DX12 \_ \_ поток состояния конвейера \_ потока \_**](cd3dx12-pipeline-state-stream-rasterizer.md) состояний позволяют инициализировать данные вложенных объектов с общими значениями по умолчанию, используя [**CD3DX12 \_ по умолчанию**](cd3dx12-default.md).

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------|-------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3dx12. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Вспомогательные структуры для D3D12](helper-structures-for-d3d12.md)
</dt> <dt>

[**\_ \_ \_ Тип подобъекта состояния конвейера D3D12 \_**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_pipeline_state_subobject_type)
</dt> </dl>

 

