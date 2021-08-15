---
title: SV_GroupIndex
description: '\ 0034; плоская \ 0034; Индекс вычисленного потока шейдера в группе потоков, который превращает многомерное ОКП \_ граупсреадид в значение 1d. ОКП \_ граупиндекс меняется от 0 до (нумсреадскс \ нумсреадси \ нумсреадсз) \ 8211; одного.'
ms.assetid: e793be10-7c83-478c-859a-4b0a2c537570
keywords:
- SV_GroupIndex HLSL
topic_type:
- apiref
api_name:
- SV_GroupIndex
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: fd8c10212a2dd91e4ecbe7fd48a427e4019b2cd79b3d56457635ab9ef9d9262a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118508254"
---
# <a name="sv_groupindex"></a>ОКП \_ граупиндекс

"Плоский" индекс потока вычислений для шейдера в группе потоков, который превращает многомерное ОКП \_ граупсреадид в значение 1d. ОКП \_ граупиндекс варьируется от 0 до (нумсреадскс \* нумсреадси \* нумсреадсз) – 1.

## <a name="type"></a>Тип



| Тип |
|------|
| uint |



 

## <a name="remarks"></a>Remarks


```
SV_GroupIndex = SV_GroupThreadID.z*dimx*dimy + 
                      SV_GroupThreadID.y*dimx + 
                      SV_GroupThreadID.x
```



где димкс и Дими — это измерения, указанные в атрибуте [numthreads](sm5-attributes-numthreads.md) для точки входа.

Это системное значение является необязательным. Однако его использование гарантирует, что поток записывается только в назначенную ему область памяти в переменной граупшаред.

На следующем рисунке показана связь между параметрами, передаваемыми в [**ссылку ID3D11DeviceContext::D диспетчеризации**](/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-dispatch), диспетчеризации (5, 3, 2), значениями, указанными в атрибуте [numthreads](sm5-attributes-numthreads.md) , numthreads (10, 8, 3) и значениями, которые будут переданы в шейдер вычислений для системных значений, связанных с потоками (ОКП \_ граупиндекс,[SV \_ диспатчсреадид](sv-dispatchthreadid.md),[ОКП \_ граупсреадид](sv-groupthreadid.md),[SV \_ groupId](sv-groupid.md)).

![Иллюстрация связи между диспетчеризация, группами потоков и потоками](images/threadgroupids.png)

Эта функция поддерживается в следующих типах шейдеров:



| Вершина | Поверхности | Домен | Геометрия | Пиксель | Службы вычислений |
|--------|------|--------|----------|-------|---------|
|        |      |        |          |       | x       |



 

## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Семантика](dx-graphics-hlsl-semantics.md)
</dt> <dt>

[Модель шейдера 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 