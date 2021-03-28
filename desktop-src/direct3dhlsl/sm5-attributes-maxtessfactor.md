---
title: макстессфактор
description: Указывает максимальное значение, которое будет возвращаться шейдером поверхности для любого фактора тесселяции.
ms.assetid: 2c12ed56-cd64-4143-8dda-6998aa212356
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 261ab17bd40c24c19b4b929f2e8307ccc6bb9b56
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/20/2019
ms.locfileid: "103890027"
---
# <a name="maxtessfactor"></a><span data-ttu-id="b0d00-103">макстессфактор</span><span class="sxs-lookup"><span data-stu-id="b0d00-103">maxtessfactor</span></span>

<span data-ttu-id="b0d00-104">Указывает максимальное значение, которое будет возвращаться шейдером поверхности для любого фактора тесселяции.</span><span class="sxs-lookup"><span data-stu-id="b0d00-104">Indicates the maximum value that the hull shader would return for any tessellation factor.</span></span>


```
maxtessfactor(X)   
```



## <a name="remarks"></a><span data-ttu-id="b0d00-105">Примечания</span><span class="sxs-lookup"><span data-stu-id="b0d00-105">Remarks</span></span>

<span data-ttu-id="b0d00-106">Этот атрибут помещает верхнюю границу объема запрошенной тесселяции, чтобы помочь драйверу определить максимальный объем ресурсов, необходимых для тесселяции.</span><span class="sxs-lookup"><span data-stu-id="b0d00-106">This attribute puts an upper bound on the amount of tessellation requested to help a driver determine the maximum amount of resources required for tessellation.</span></span>

<span data-ttu-id="b0d00-107">Этот атрибут поддерживается в следующих типах шейдеров:</span><span class="sxs-lookup"><span data-stu-id="b0d00-107">This attribute is supported in the following types of shaders:</span></span>



| <span data-ttu-id="b0d00-108">Вершина</span><span class="sxs-lookup"><span data-stu-id="b0d00-108">Vertex</span></span> | <span data-ttu-id="b0d00-109">Поверхности</span><span class="sxs-lookup"><span data-stu-id="b0d00-109">Hull</span></span> | <span data-ttu-id="b0d00-110">Домен</span><span class="sxs-lookup"><span data-stu-id="b0d00-110">Domain</span></span> | <span data-ttu-id="b0d00-111">Геометрия</span><span class="sxs-lookup"><span data-stu-id="b0d00-111">Geometry</span></span> | <span data-ttu-id="b0d00-112">Пиксель</span><span class="sxs-lookup"><span data-stu-id="b0d00-112">Pixel</span></span> | <span data-ttu-id="b0d00-113">Вычисления</span><span class="sxs-lookup"><span data-stu-id="b0d00-113">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        | <span data-ttu-id="b0d00-114">x</span><span class="sxs-lookup"><span data-stu-id="b0d00-114">x</span></span>    |        |          |       |         |



 

## <a name="related-topics"></a><span data-ttu-id="b0d00-115">См. также</span><span class="sxs-lookup"><span data-stu-id="b0d00-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b0d00-116">Атрибуты модели шейдеров 5</span><span class="sxs-lookup"><span data-stu-id="b0d00-116">Shader Model 5 Attributes</span></span>](d3d11-graphics-reference-sm5-attributes.md)
</dt> <dt>

[<span data-ttu-id="b0d00-117">Модель шейдера 5</span><span class="sxs-lookup"><span data-stu-id="b0d00-117">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




