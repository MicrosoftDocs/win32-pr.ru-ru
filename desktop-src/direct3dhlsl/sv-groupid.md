---
title: SV_GroupID
description: Индексы для группы потоков, в которой выполняется шейдер вычислений.
ms.assetid: 1b90ca74-a2b6-4a5f-aa4a-1ec879360593
keywords:
- SV_GroupID HLSL
topic_type:
- apiref
api_name:
- SV_GroupID
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: bce2623141329b4d750ab5add7957a7674662d7c21de9ff03e1165d341f98576
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120118164"
---
# <a name="sv_groupid"></a>SV \_ groupId

Индексы для группы потоков, в которой выполняется шейдер вычислений. Индексы относятся ко всей группе, а не к отдельному потоку. Возможные значения зависят от диапазона, передаваемого в качестве параметров для [**диспетчеризации**](/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-dispatch). Например, вызов диспетчеризации (2, 1, 1) приводит к получению возможных значений 0, 0, 0 и 1, 0, 0.

Определяет смещение группы в вызове [**диспетчеризации**](/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-dispatch) для каждого измерения вызова диспетчеризации.

## <a name="type"></a>Тип



| Тип      |
|-------|
| uint3 |



 

## <a name="remarks"></a>Remarks

Это системное значение является необязательным.

На следующем рисунке показана связь между параметрами, передаваемыми для [**диспетчеризации**](/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-dispatch), диспетчеризации (5, 3, 2), значениями, указанными в атрибуте [numthreads](sm5-attributes-numthreads.md) , numthreads (10, 8, 3), и значениями, которые будут переданы в шейдер вычислений для системных значений, связанных с потоками ([ОКП \_ граупиндекс](sv-groupindex.md),[SV \_ диспатчсреадид](sv-dispatchthreadid.md),[ОКП \_ граупсреадид](sv-groupthreadid.md), SV \_ GroupId).

![Иллюстрация связи между диспетчеризация, группами потоков и потоками](images/threadgroupids.png)

Эта функция поддерживается в следующих типах шейдеров:



| Вершина | Поверхности | Домен | Геометрия | Пиксель | Вычисления |
|--------|------|--------|----------|-------|---------|
|        |      |        |          |       | x       |



 

## <a name="see-also"></a>См. также

<dl> <dt>

[Семантика](dx-graphics-hlsl-semantics.md)
</dt> <dt>

[Модель шейдера 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 
