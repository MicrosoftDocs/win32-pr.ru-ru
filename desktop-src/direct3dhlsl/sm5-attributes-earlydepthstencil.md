---
title: еарлидепсстенЦил
description: Принудительное тестирование трафаретной глубины перед выполнением шейдера.
ms.assetid: f8a9fee7-4a8a-4a34-bf7c-56906592caac
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: a7dd8507986970f2066538cc00b53af08807910e
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/20/2019
ms.locfileid: "104996959"
---
# <a name="earlydepthstencil"></a><span data-ttu-id="5015f-103">еарлидепсстенЦил</span><span class="sxs-lookup"><span data-stu-id="5015f-103">earlydepthstencil</span></span>

<span data-ttu-id="5015f-104">Принудительное тестирование трафаретной глубины перед выполнением шейдера.</span><span class="sxs-lookup"><span data-stu-id="5015f-104">Forces depth-stencil testing before a shader executes.</span></span>


```
earlydepthstencil   
```



## <a name="remarks"></a><span data-ttu-id="5015f-105">Примечания</span><span class="sxs-lookup"><span data-stu-id="5015f-105">Remarks</span></span>

<span data-ttu-id="5015f-106">Тестирование шаблона глубины обычно выполняется во время обработки пикселя шейдером пикселей.</span><span class="sxs-lookup"><span data-stu-id="5015f-106">Depth-stencil testing is normally done during pixel processing by a pixel shader.</span></span> <span data-ttu-id="5015f-107">Принудительное раннее тестирование набора элементов приводит к выполнению тестирования перед выполнением шейдера. Цель состоит в том, чтобы улучшить производительность на пиксель за счет отбора/уменьшения или предотвращения ненужной обработки пикселей.</span><span class="sxs-lookup"><span data-stu-id="5015f-107">Forcing early depth-stencil testing causes the testing to be done prior to the shader execution; the purpose is to improve per-pixel performance by culling/reducing/avoiding unnecessary pixel processing.</span></span>

<span data-ttu-id="5015f-108">Приложение может выполнить раннее тестирование набора элементов, указав атрибут или оборудование может выполнять раннее тестирование набора элементов, при этом не записываются значения глубины, и неупорядоченные операции доступа не выполняются в шейдере в качестве оптимизации.</span><span class="sxs-lookup"><span data-stu-id="5015f-108">An application can force early depth-stencil testing by supplying the attribute or the hardware may execute early depth-stencil testing provided no depth values are written and no unordered access operations are performed in a shader as an optimization.</span></span>

<span data-ttu-id="5015f-109">Этот атрибут поддерживается в следующих типах шейдеров:</span><span class="sxs-lookup"><span data-stu-id="5015f-109">This attribute is supported in the following types of shaders:</span></span>



| <span data-ttu-id="5015f-110">Вершина</span><span class="sxs-lookup"><span data-stu-id="5015f-110">Vertex</span></span> | <span data-ttu-id="5015f-111">Поверхности</span><span class="sxs-lookup"><span data-stu-id="5015f-111">Hull</span></span> | <span data-ttu-id="5015f-112">Домен</span><span class="sxs-lookup"><span data-stu-id="5015f-112">Domain</span></span> | <span data-ttu-id="5015f-113">Геометрия</span><span class="sxs-lookup"><span data-stu-id="5015f-113">Geometry</span></span> | <span data-ttu-id="5015f-114">Пиксель</span><span class="sxs-lookup"><span data-stu-id="5015f-114">Pixel</span></span> | <span data-ttu-id="5015f-115">Вычисления</span><span class="sxs-lookup"><span data-stu-id="5015f-115">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="5015f-116">x</span><span class="sxs-lookup"><span data-stu-id="5015f-116">x</span></span>     |         |



 

## <a name="related-topics"></a><span data-ttu-id="5015f-117">См. также</span><span class="sxs-lookup"><span data-stu-id="5015f-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5015f-118">Атрибуты модели шейдеров 5</span><span class="sxs-lookup"><span data-stu-id="5015f-118">Shader Model 5 Attributes</span></span>](d3d11-graphics-reference-sm5-attributes.md)
</dt> <dt>

[<span data-ttu-id="5015f-119">Модель шейдера 5</span><span class="sxs-lookup"><span data-stu-id="5015f-119">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




