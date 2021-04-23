---
title: функция DST
description: Вычисляет вектор расстояний. | функция DST
ms.assetid: 24d22743-5867-49db-8d0a-55cc3625c947
keywords:
- функция DST HLSL
topic_type:
- apiref
api_name:
- dst
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 58ce243cf9a9f3e6118763368445e5bcf26ba4cc
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "103914343"
---
# <a name="dst-function"></a><span data-ttu-id="6f421-105">функция DST</span><span class="sxs-lookup"><span data-stu-id="6f421-105">dst function</span></span>

<span data-ttu-id="6f421-106">Вычисляет вектор расстояний.</span><span class="sxs-lookup"><span data-stu-id="6f421-106">Calculates a distance vector.</span></span>

## <a name="syntax"></a><span data-ttu-id="6f421-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="6f421-107">Syntax</span></span>

``` syntax
fVector dst(
  in fVector src0,
  in fVector src1
);
```

## <a name="parameters"></a><span data-ttu-id="6f421-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="6f421-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6f421-109">*src0* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="6f421-109">*src0* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6f421-110">Тип: **[фвектор](dx-graphics-hlsl-vector.md)**</span><span class="sxs-lookup"><span data-stu-id="6f421-110">Type: **[fVector](dx-graphics-hlsl-vector.md)**</span></span>

<span data-ttu-id="6f421-111">Первый вектор.</span><span class="sxs-lookup"><span data-stu-id="6f421-111">The first vector.</span></span>

</dd> <dt>

<span data-ttu-id="6f421-112">*src1* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="6f421-112">*src1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6f421-113">Тип: **[фвектор](dx-graphics-hlsl-vector.md)**</span><span class="sxs-lookup"><span data-stu-id="6f421-113">Type: **[fVector](dx-graphics-hlsl-vector.md)**</span></span>

<span data-ttu-id="6f421-114">Второй вектор.</span><span class="sxs-lookup"><span data-stu-id="6f421-114">The second vector.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6f421-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="6f421-115">Return value</span></span>

<span data-ttu-id="6f421-116">Тип: **[фвектор](dx-graphics-hlsl-vector.md)**</span><span class="sxs-lookup"><span data-stu-id="6f421-116">Type: **[fVector](dx-graphics-hlsl-vector.md)**</span></span>

<span data-ttu-id="6f421-117">Вычисленный вектор расстояний.</span><span class="sxs-lookup"><span data-stu-id="6f421-117">The computed distance vector.</span></span>

## <a name="remarks"></a><span data-ttu-id="6f421-118">Примечания</span><span class="sxs-lookup"><span data-stu-id="6f421-118">Remarks</span></span>

<span data-ttu-id="6f421-119">Эта встроенная функция предоставляет те же функциональные возможности, что и время [летнего времени](dst---vs.md)для инструкции шейдера вершин.</span><span class="sxs-lookup"><span data-stu-id="6f421-119">This intrinsic function provides the same functionality as the Vertex Shader instruction [dst](dst---vs.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="6f421-120">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="6f421-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6f421-121">Встроенные функции</span><span class="sxs-lookup"><span data-stu-id="6f421-121">Intrinsic Functions</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

 




