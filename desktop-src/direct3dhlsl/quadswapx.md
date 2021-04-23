---
title: Функция Куадреадакросскс
description: Возвращает указанное локальное значение, считанное из другой полосы в данном Quad по оси X.
ms.assetid: 7A7E0623-30EC-4167-90A5-D79E10A394CC
keywords:
- Функция Куадреадакросскс HLSL
topic_type:
- apiref
api_name:
- QuadReadAcrossX
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: cd41b0bd84861d23153f02ba6328d17b70287866
ms.sourcegitcommit: f01bc6744cea55ad1aeeace7981a30b567e6fe60
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/04/2020
ms.locfileid: "104134787"
---
# <a name="quadreadacrossx-function"></a><span data-ttu-id="47461-104">Функция Куадреадакросскс</span><span class="sxs-lookup"><span data-stu-id="47461-104">QuadReadAcrossX function</span></span>

<span data-ttu-id="47461-105">Возвращает указанное локальное значение, считанное из другой полосы в данном Quad по оси X.</span><span class="sxs-lookup"><span data-stu-id="47461-105">Returns the specified local value read from the other lane in this quad in the X direction.</span></span>

## <a name="syntax"></a><span data-ttu-id="47461-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="47461-106">Syntax</span></span>

``` syntax
<type> QuadReadAcrossX(
   <type> localValue
);
```

## <a name="parameters"></a><span data-ttu-id="47461-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="47461-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="47461-108">*локалвалуе*</span><span class="sxs-lookup"><span data-stu-id="47461-108">*localValue*</span></span> 
</dt> <dd>

<span data-ttu-id="47461-109">Запрошенный тип.</span><span class="sxs-lookup"><span data-stu-id="47461-109">The requested type.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="47461-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="47461-110">Return value</span></span>

<span data-ttu-id="47461-111">Указанное локальное значение.</span><span class="sxs-lookup"><span data-stu-id="47461-111">The specified local value.</span></span> <span data-ttu-id="47461-112">Если исходная полоса неактивна, результаты будут неопределенными.</span><span class="sxs-lookup"><span data-stu-id="47461-112">If the source lane is inactive, the results are undefined.</span></span>

## <a name="remarks"></a><span data-ttu-id="47461-113">Примечания</span><span class="sxs-lookup"><span data-stu-id="47461-113">Remarks</span></span>

<span data-ttu-id="47461-114">Дополнительные сведения об четырехъядерях см. в разделе [Общие сведения о модели шейдеров 6](hlsl-shader-model-6-0-features-for-direct3d-12.md).</span><span class="sxs-lookup"><span data-stu-id="47461-114">For more information on quads, refer to [Overview of Shader Model 6](hlsl-shader-model-6-0-features-for-direct3d-12.md).</span></span>

<span data-ttu-id="47461-115">Эта функция поддерживается из модели шейдеров 6,0 только в пиксельных шейдерах и.</span><span class="sxs-lookup"><span data-stu-id="47461-115">This function is supported from shader model 6.0 only in pixel and compute shaders.</span></span>



 

## <a name="see-also"></a><span data-ttu-id="47461-116">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="47461-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="47461-117">Модель шейдеров 6</span><span class="sxs-lookup"><span data-stu-id="47461-117">Shader Model 6</span></span>](shader-model-6-0.md)
</dt> </dl>

 

 




