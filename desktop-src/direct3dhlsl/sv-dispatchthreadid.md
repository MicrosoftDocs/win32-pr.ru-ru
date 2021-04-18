---
title: SV_DispatchThreadID
description: Индексы, для которых в объединенном потоке и группе потоков выполняется шейдер вычислений.
ms.assetid: bad697f6-26d9-47cd-93e5-127621a161e8
keywords:
- SV_DispatchThreadID HLSL
topic_type:
- apiref
api_name:
- SV_DispatchThreadID
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d55fcf7e291c561ecb51dd32dfac135c563974c7
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104569395"
---
# <a name="sv_dispatchthreadid"></a>ОКП \_ диспатчсреадид

Индексы, для которых в объединенном потоке и группе потоков выполняется шейдер вычислений. ОКП \_ диспатчсреадид — это сумма значений ОКП \_ groupId \* numthreads и граупсреадид. Он зависит от диапазона, указанного в поле [**Dispatch**](/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-dispatch) and [numthreads](sm5-attributes-numthreads.md). Например, если метод Dispatch (2, 2, 2) вызывается для Compute Shader с numthreads (3, 3, 3) ОКП \_ диспатчсреадид будет иметь диапазон 0.. 5 для каждого измерения.

## <a name="type"></a>Тип



|       |
|-------|
| Тип  |
| uint3 |



 

## <a name="remarks"></a>Примечания

Это системное значение является необязательным.

На следующем рисунке показана связь между параметрами, передаваемыми для [**диспетчеризации**](/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-dispatch), диспетчеризации (5, 3, 2), значениями, указанными в атрибуте [numthreads](sm5-attributes-numthreads.md) , numthreads (10, 8, 3), и значениями, которые будут переданы в шейдер вычислений для системных значений, связанных с потоками ([ОКП \_ граупиндекс](sv-groupindex.md), SV \_ диспатчсреадид,[ОКП \_ граупсреадид](sv-groupthreadid.md),[SV \_ groupId](sv-groupid.md)).

![Иллюстрация связи между диспетчеризация, группами потоков и потоками](images/threadgroupids.png)

Эта функция поддерживается в следующих типах шейдеров:



|        |      |        |          |       |         |
|--------|------|--------|----------|-------|---------|
| Вершина | Поверхности | Домен | Геометрия | Пиксель | Вычисления |
|        |      |        |          |       | x       |



 

## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Семантика](dx-graphics-hlsl-semantics.md)
</dt> <dt>

[Модель шейдера 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 