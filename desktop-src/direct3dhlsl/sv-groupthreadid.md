---
title: SV_GroupThreadID
description: Индексы, для которых выполняется отдельный поток в группе потоков, в которой работает шейдер вычислений.
ms.assetid: be944592-c4ea-43c9-88bc-98a9a190a437
keywords:
- SV_GroupThreadID HLSL
topic_type:
- apiref
api_name:
- SV_GroupThreadID
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 2d36e5639b017dfa94e0f3c9f84d6725f6b6a283
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/26/2021
ms.locfileid: "107996991"
---
# <a name="sv_groupthreadid"></a>ОКП \_ граупсреадид

Индексы, для которых выполняется отдельный поток в группе потоков, в которой работает шейдер вычислений. ОКП \_ граупсреадид варьируется в пределах диапазона, указанного для шейдера вычислений в атрибуте [numthreads](sm5-attributes-numthreads.md) . Например, если задано значение numthreads (3, 2, 1), возможные значения для \_ входного значения SV граупсреадид имеют этот диапазон значений (0 – 2, 0 – 1, 0).

## <a name="type"></a>Тип



|       |
|-------|
| Тип  |
| uint3 |



 

## <a name="remarks"></a>Примечания

Это системное значение является необязательным и всегда находится внутри границ значений, передаваемых в атрибут [numthreads](sm5-attributes-numthreads.md) .

На следующем рисунке показана связь между параметрами, передаваемыми для [**диспетчеризации**](/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-dispatch), диспетчеризации (5, 3, 2), значениями, указанными в атрибуте [numthreads](sm5-attributes-numthreads.md) , numthreads (10, 8, 3), и значениями, которые будут переданы в шейдер вычислений для системных значений, связанных с потоками ([ОКП \_ граупиндекс](sv-groupindex.md),[SV \_ диспатчсреадид](sv-dispatchthreadid.md), ОКП \_ граупсреадид,[SV \_ groupId](sv-groupid.md)).

![Иллюстрация связи между диспетчеризация, группами потоков и потоками](images/threadgroupids.png)

Эта функция поддерживается в следующих типах шейдеров:



| Вершина | Поверхности | Домен | Геометрия | Пиксель | Службы вычислений |
|--------|------|--------|----------|-------|---------|
|        |      |        |          |       | x       |



 

## <a name="see-also"></a>См. также

<dl> <dt>

[Семантика](dx-graphics-hlsl-semantics.md)
</dt> <dt>

[Модель шейдера 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 
