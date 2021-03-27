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
ms.openlocfilehash: 952a94378a0570d5bb7bc4f08959074bc8a4da4d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "103792283"
---
# <a name="sv_groupindex"></a>ОКП \_ граупиндекс

"Плоский" индекс потока вычислений для шейдера в группе потоков, который превращает многомерное ОКП \_ граупсреадид в значение 1d. ОКП \_ граупиндекс варьируется от 0 до (нумсреадскс \* нумсреадси \* нумсреадсз) – 1.

## <a name="type"></a>Тип



| Тип |
|------|
| uint |



 

## <a name="remarks"></a>Примечания


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



| Вершина | Поверхности | Домен | Геометрия | Пиксель | Вычисления |
|--------|------|--------|----------|-------|---------|
|        |      |        |          |       | x       |



 

## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Семантика](dx-graphics-hlsl-semantics.md)
</dt> <dt>

[Модель шейдера 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 