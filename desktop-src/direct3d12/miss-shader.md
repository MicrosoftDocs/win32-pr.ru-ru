---
description: Шейдер, который вызывается, когда ни один из пересечения лучей не найден или не принят.
ms.assetid: ''
title: Шейдер непопаданий
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RAY_FLAG
api_type:
- NA
ms.openlocfilehash: fe8e2ec9cdbb8ef7567b9327ae5af1128597a601
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105692036"
---
# <a name="miss-shader"></a>Шейдер непопаданий

Шейдер, который вызывается, когда ни один из пересечения лучей не найден или не принят. Это удобно для фона или штриховки.  Чтобы запланировать больше работы, шейдер может использовать [**каллшадер**](callshader-function.md) и **трацерай** .

В раскрывающемся шейдере должен быть указан параметр полезной нагрузки с определяемой пользователем структурой, соответствующий указанному в [**трацерай**](traceray-function.md).


## <a name="shader-type-attribute"></a>Атрибут типа шейдера


```
[shader("miss")]
```



## <a name="example"></a>Пример

```
[shader("anyhit")]
void miss_main(inout MyPayload payload)
{
    // Use ray system values to compute contributions of background, sky, etc...
    // Combine contributions into ray payload
    CallShader( ... );  // if desired
    TraceRay( ... );    // if desired
    // this ray query is now complete
}

```

 

 




