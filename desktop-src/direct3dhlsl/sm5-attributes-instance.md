---
title: экземпляр
description: Используйте этот атрибут для экземпляра шейдера Geometry.
ms.assetid: 0e487e52-53d0-4193-99b2-fd018a061b42
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 4749e11db00b38e5e223e11315de86656b2f6488
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/20/2019
ms.locfileid: "104069365"
---
# <a name="instance"></a><span data-ttu-id="8b0e7-103">экземпляр</span><span class="sxs-lookup"><span data-stu-id="8b0e7-103">instance</span></span>

<span data-ttu-id="8b0e7-104">Используйте этот атрибут для экземпляра шейдера Geometry.</span><span class="sxs-lookup"><span data-stu-id="8b0e7-104">Use this attribute to instance a geometry shader.</span></span>


```
instance(X)   
```



## <a name="remarks"></a><span data-ttu-id="8b0e7-105">Примечания</span><span class="sxs-lookup"><span data-stu-id="8b0e7-105">Remarks</span></span>

<span data-ttu-id="8b0e7-106">X — это целочисленный индекс, указывающий количество экземпляров, которые должны быть выполнены для каждого рисуемого элемента (например, для каждого треугольника).</span><span class="sxs-lookup"><span data-stu-id="8b0e7-106">X is an integer index that indicates the number of instances to be executed for each drawn item (for example, for each triangle).</span></span> <span data-ttu-id="8b0e7-107">При использовании этого атрибута используйте [SV \_ гсинстанцеид](sv-gsinstanceid.md) , чтобы указать, какой экземпляр шейдера Geometry выполняется.</span><span class="sxs-lookup"><span data-stu-id="8b0e7-107">When using this attribute, use [SV\_GSInstanceID](sv-gsinstanceid.md) to identify which instance of a geometry shader is being executed.</span></span>

<span data-ttu-id="8b0e7-108">Этот атрибут поддерживается в следующих типах шейдеров:</span><span class="sxs-lookup"><span data-stu-id="8b0e7-108">This attribute is supported in the following types of shaders:</span></span>



| <span data-ttu-id="8b0e7-109">Вершина</span><span class="sxs-lookup"><span data-stu-id="8b0e7-109">Vertex</span></span> | <span data-ttu-id="8b0e7-110">Поверхности</span><span class="sxs-lookup"><span data-stu-id="8b0e7-110">Hull</span></span> | <span data-ttu-id="8b0e7-111">Домен</span><span class="sxs-lookup"><span data-stu-id="8b0e7-111">Domain</span></span> | <span data-ttu-id="8b0e7-112">Геометрия</span><span class="sxs-lookup"><span data-stu-id="8b0e7-112">Geometry</span></span> | <span data-ttu-id="8b0e7-113">Пиксель</span><span class="sxs-lookup"><span data-stu-id="8b0e7-113">Pixel</span></span> | <span data-ttu-id="8b0e7-114">Вычисления</span><span class="sxs-lookup"><span data-stu-id="8b0e7-114">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        | <span data-ttu-id="8b0e7-115">x</span><span class="sxs-lookup"><span data-stu-id="8b0e7-115">x</span></span>        |       |         |



 

## <a name="related-topics"></a><span data-ttu-id="8b0e7-116">См. также</span><span class="sxs-lookup"><span data-stu-id="8b0e7-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8b0e7-117">Атрибуты модели шейдеров 5</span><span class="sxs-lookup"><span data-stu-id="8b0e7-117">Shader Model 5 Attributes</span></span>](d3d11-graphics-reference-sm5-attributes.md)
</dt> <dt>

[<span data-ttu-id="8b0e7-118">Модель шейдера 5</span><span class="sxs-lookup"><span data-stu-id="8b0e7-118">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




