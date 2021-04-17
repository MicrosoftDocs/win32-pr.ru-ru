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
# <a name="callable-shader"></a><span data-ttu-id="ce1d4-103">Вызываемый шейдер</span><span class="sxs-lookup"><span data-stu-id="ce1d4-103">Callable Shader</span></span>

<span data-ttu-id="ce1d4-104">Шейдер, который вызывается из другого шейдера с встроенной функцией [**каллшадер**](callshader-function.md) .</span><span class="sxs-lookup"><span data-stu-id="ce1d4-104">A shader that is invoked from another shader with the [**CallShader**](callshader-function.md) intrinsic.</span></span>

<span data-ttu-id="ce1d4-105">Существует структура параметра, предоставляемая на сайте вызова **каллшадер** , которая должна соответствовать структуре параметров, используемой в вызываемом шейдере, на которую указывает запрошенный индекс в таблице вызываемого шейдера, предоставляемой методом [**диспатчрайс**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist4-dispatchrays) .</span><span class="sxs-lookup"><span data-stu-id="ce1d4-105">There is a parameter structure supplied at the **CallShader** call site that must match the parameter structure used in the callable shader pointed to by the requested index into the callable shader table supplied through the [**DispatchRays**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist4-dispatchrays) method.</span></span>  <span data-ttu-id="ce1d4-106">Вызываемый шейдер должен объявлять этот параметр как *InOut*.</span><span class="sxs-lookup"><span data-stu-id="ce1d4-106">The callable shader must declare this parameter as *inout*.</span></span>  <span data-ttu-id="ce1d4-107">Кроме того, вызываемый шейдер может считывать входные данные индекса и измерения.</span><span class="sxs-lookup"><span data-stu-id="ce1d4-107">Additionally, the callable shader may read launch index and dimension inputs.</span></span> <span data-ttu-id="ce1d4-108">Дополнительные сведения см. в разделе [**встроенные функции системных значений**](direct3d-12-raytracing-hlsl-system-value-intrinsics.md).</span><span class="sxs-lookup"><span data-stu-id="ce1d4-108">For more information, see [**System Value Intrinsics**](direct3d-12-raytracing-hlsl-system-value-intrinsics.md).</span></span> 


## <a name="shader-type-attribute"></a><span data-ttu-id="ce1d4-109">Атрибут типа шейдера</span><span class="sxs-lookup"><span data-stu-id="ce1d4-109">Shader Type attribute</span></span>


```
[shader("callable")]
```



## <a name="example"></a><span data-ttu-id="ce1d4-110">Пример</span><span class="sxs-lookup"><span data-stu-id="ce1d4-110">Example</span></span>

```
[shader("callable")]
void callable_main(inout MyParams params)
{
    // Perform some common operations and update params
    CallShader( ... );  // maybe
}

```

 

 




