---
description: Шейдер, который вызывается из другого шейдера с встроенной функцией Каллшадер.
ms.assetid: ''
title: Вызываемый шейдер
ms.date: 05/31/2018
ms.localizationpriority: low
ms.topic: reference
topic_type:
- APIRef
- kbSyntax
api_name:
- Callable Shader
api_type:
- NA
ms.openlocfilehash: 65df547c5e40a46cc4c35361b88ceb797c2e8852
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105710695"
---
# <a name="callable-shader"></a>Вызываемый шейдер

Шейдер, который вызывается из другого шейдера с встроенной функцией [**каллшадер**](callshader-function.md) .

Существует структура параметра, предоставляемая на сайте вызова **каллшадер** , которая должна соответствовать структуре параметров, используемой в вызываемом шейдере, на которую указывает запрошенный индекс в таблице вызываемого шейдера, предоставляемой методом [**диспатчрайс**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist4-dispatchrays) .  Вызываемый шейдер должен объявлять этот параметр как *InOut*.  Кроме того, вызываемый шейдер может считывать входные данные индекса и измерения. Дополнительные сведения см. в разделе [**встроенные функции системных значений**](direct3d-12-raytracing-hlsl-system-value-intrinsics.md). 


## <a name="shader-type-attribute"></a>Атрибут типа шейдера


```
[shader("callable")]
```



## <a name="example"></a>Пример

```
[shader("callable")]
void callable_main(inout MyParams params)
{
    // Perform some common operations and update params
    CallShader( ... );  // maybe
}

```

 

 




