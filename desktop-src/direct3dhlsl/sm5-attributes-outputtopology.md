---
title: аутпуттопологи
description: Определяет тип выходного примитива для тесселяции.
ms.assetid: 4aba65e5-b005-43fd-a844-c7fbb1b7406c
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 917a927ff80d4abe1b6509fd41281992a998c945
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/20/2019
ms.locfileid: "103987081"
---
# <a name="outputtopology"></a><span data-ttu-id="d3adc-103">аутпуттопологи</span><span class="sxs-lookup"><span data-stu-id="d3adc-103">outputtopology</span></span>

<span data-ttu-id="d3adc-104">Определяет тип выходного примитива для тесселяции.</span><span class="sxs-lookup"><span data-stu-id="d3adc-104">Defines the output primitive type for the tessellator.</span></span>


```
outputtopology(X)      
```



## <a name="remarks"></a><span data-ttu-id="d3adc-105">Примечания</span><span class="sxs-lookup"><span data-stu-id="d3adc-105">Remarks</span></span>

<span data-ttu-id="d3adc-106">X должен быть " [**точка**](dx-graphics-hlsl-geometry-shader.md)", " **линия**", " **треугольник \_**" или "треугольник" и должен быть заключен в кавычки. **\_**</span><span class="sxs-lookup"><span data-stu-id="d3adc-106">X must be either [**point**](dx-graphics-hlsl-geometry-shader.md), **line**, **triangle\_cw**, or **triangle\_ccw** and must be inside quotes.</span></span> <span data-ttu-id="d3adc-107">Ниже приведены допустимые параметры для этого атрибута.</span><span class="sxs-lookup"><span data-stu-id="d3adc-107">Here are the valid options for this attribute:</span></span>


```
[outputtopology("point")]
[outputtopology("line")]
[outputtopology("triangle_cw")]
[outputtopology("triangle_ccw")]
```



<span data-ttu-id="d3adc-108">Этот атрибут поддерживается в следующих типах шейдеров:</span><span class="sxs-lookup"><span data-stu-id="d3adc-108">This attribute is supported in the following types of shaders:</span></span>



| <span data-ttu-id="d3adc-109">Вершина</span><span class="sxs-lookup"><span data-stu-id="d3adc-109">Vertex</span></span> | <span data-ttu-id="d3adc-110">Поверхности</span><span class="sxs-lookup"><span data-stu-id="d3adc-110">Hull</span></span> | <span data-ttu-id="d3adc-111">Домен</span><span class="sxs-lookup"><span data-stu-id="d3adc-111">Domain</span></span> | <span data-ttu-id="d3adc-112">Геометрия</span><span class="sxs-lookup"><span data-stu-id="d3adc-112">Geometry</span></span> | <span data-ttu-id="d3adc-113">Пиксель</span><span class="sxs-lookup"><span data-stu-id="d3adc-113">Pixel</span></span> | <span data-ttu-id="d3adc-114">Вычисления</span><span class="sxs-lookup"><span data-stu-id="d3adc-114">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        | <span data-ttu-id="d3adc-115">x</span><span class="sxs-lookup"><span data-stu-id="d3adc-115">x</span></span>    |        |          |       |         |



 

## <a name="related-topics"></a><span data-ttu-id="d3adc-116">См. также</span><span class="sxs-lookup"><span data-stu-id="d3adc-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d3adc-117">Атрибуты модели шейдеров 5</span><span class="sxs-lookup"><span data-stu-id="d3adc-117">Shader Model 5 Attributes</span></span>](d3d11-graphics-reference-sm5-attributes.md)
</dt> <dt>

[<span data-ttu-id="d3adc-118">Модель шейдера 5</span><span class="sxs-lookup"><span data-stu-id="d3adc-118">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




