---
title: Секционирование
description: Определяет схему тесселатион, используемую в шейдере поверхности.
ms.assetid: 29dc4abb-4d29-4538-8680-a4fcbfd8235b
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 6bf0744481a123998b64693d669e9cb7255599f8
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/20/2019
ms.locfileid: "103890024"
---
# <a name="partitioning"></a><span data-ttu-id="3e036-103">Секционирование</span><span class="sxs-lookup"><span data-stu-id="3e036-103">partitioning</span></span>

<span data-ttu-id="3e036-104">Определяет схему тесселатион, используемую в шейдере поверхности.</span><span class="sxs-lookup"><span data-stu-id="3e036-104">Defines the tesselation scheme to be used in the hull shader.</span></span>


```
partitioning(X)    
```



## <a name="remarks"></a><span data-ttu-id="3e036-105">Примечания</span><span class="sxs-lookup"><span data-stu-id="3e036-105">Remarks</span></span>

<span data-ttu-id="3e036-106">Может быть **целым числом**, **дробной частью \_**, **\_ четным** или **pow2**.</span><span class="sxs-lookup"><span data-stu-id="3e036-106">Can be **integer**, **fractional\_even**, **fractional\_odd**, or **pow2**.</span></span>

<span data-ttu-id="3e036-107">Этот атрибут поддерживается в следующих типах шейдеров:</span><span class="sxs-lookup"><span data-stu-id="3e036-107">This attribute is supported in the following types of shaders:</span></span>



| <span data-ttu-id="3e036-108">Вершина</span><span class="sxs-lookup"><span data-stu-id="3e036-108">Vertex</span></span> | <span data-ttu-id="3e036-109">Поверхности</span><span class="sxs-lookup"><span data-stu-id="3e036-109">Hull</span></span> | <span data-ttu-id="3e036-110">Домен</span><span class="sxs-lookup"><span data-stu-id="3e036-110">Domain</span></span> | <span data-ttu-id="3e036-111">Геометрия</span><span class="sxs-lookup"><span data-stu-id="3e036-111">Geometry</span></span> | <span data-ttu-id="3e036-112">Пиксель</span><span class="sxs-lookup"><span data-stu-id="3e036-112">Pixel</span></span> | <span data-ttu-id="3e036-113">Вычисления</span><span class="sxs-lookup"><span data-stu-id="3e036-113">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        | <span data-ttu-id="3e036-114">x</span><span class="sxs-lookup"><span data-stu-id="3e036-114">x</span></span>    |        |          |       |         |



 

## <a name="related-topics"></a><span data-ttu-id="3e036-115">См. также</span><span class="sxs-lookup"><span data-stu-id="3e036-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3e036-116">Атрибуты модели шейдеров 5</span><span class="sxs-lookup"><span data-stu-id="3e036-116">Shader Model 5 Attributes</span></span>](d3d11-graphics-reference-sm5-attributes.md)
</dt> <dt>

[<span data-ttu-id="3e036-117">Модель шейдера 5</span><span class="sxs-lookup"><span data-stu-id="3e036-117">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




