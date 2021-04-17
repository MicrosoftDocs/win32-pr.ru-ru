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
ms.openlocfilehash: 3d4d35766bdbdc2d69c98983a85f336ab784d24d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104338985"
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

 

 