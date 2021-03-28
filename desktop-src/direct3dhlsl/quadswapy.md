---
title: Функция Куадреадакросси
description: Возвращает указанное исходное значение, считанное из другой полосы в данном Quad по оси Y.
ms.assetid: 6C03D1E6-433F-4CCA-A5EA-C3F34BB2B93B
keywords:
- Функция Куадреадакросси HLSL
topic_type:
- apiref
api_name:
- QuadReadAcrossY
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 72b5ede0df733e60ba4b1bcc01a04f1daaedc708
ms.sourcegitcommit: f01bc6744cea55ad1aeeace7981a30b567e6fe60
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/04/2020
ms.locfileid: "104984100"
---
# <a name="quadreadacrossy-function"></a><span data-ttu-id="101ae-104">Функция Куадреадакросси</span><span class="sxs-lookup"><span data-stu-id="101ae-104">QuadReadAcrossY function</span></span>

<span data-ttu-id="101ae-105">Возвращает указанное исходное значение, считанное из другой полосы в данном Quad по оси Y.</span><span class="sxs-lookup"><span data-stu-id="101ae-105">Returns the specified source value read from the other lane in this quad in the Y direction.</span></span>

## <a name="syntax"></a><span data-ttu-id="101ae-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="101ae-106">Syntax</span></span>

``` syntax
<type> QuadReadAcrossY(
   <type> localValue
);
```

## <a name="parameters"></a><span data-ttu-id="101ae-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="101ae-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="101ae-108">*локалвалуе*</span><span class="sxs-lookup"><span data-stu-id="101ae-108">*localValue*</span></span> 
</dt> <dd>

<span data-ttu-id="101ae-109">Запрошенный тип.</span><span class="sxs-lookup"><span data-stu-id="101ae-109">The requested type.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="101ae-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="101ae-110">Return value</span></span>

<span data-ttu-id="101ae-111">Указанное исходное значение.</span><span class="sxs-lookup"><span data-stu-id="101ae-111">The specified source value.</span></span> <span data-ttu-id="101ae-112">Если исходная полоса неактивна, результаты будут неопределенными.</span><span class="sxs-lookup"><span data-stu-id="101ae-112">If the source lane is inactive, the results are undefined.</span></span>

## <a name="remarks"></a><span data-ttu-id="101ae-113">Примечания</span><span class="sxs-lookup"><span data-stu-id="101ae-113">Remarks</span></span>

<span data-ttu-id="101ae-114">Дополнительные сведения об четырехъядерях см. в разделе [Общие сведения о модели шейдеров 6](hlsl-shader-model-6-0-features-for-direct3d-12.md).</span><span class="sxs-lookup"><span data-stu-id="101ae-114">For more information on quads, refer to [Overview of Shader Model 6](hlsl-shader-model-6-0-features-for-direct3d-12.md).</span></span>

<span data-ttu-id="101ae-115">Эта функция поддерживается из модели шейдеров 6,0 только в пиксельных шейдерах и.</span><span class="sxs-lookup"><span data-stu-id="101ae-115">This function is supported from shader model 6.0 only in pixel and compute shaders.</span></span>



 

## <a name="see-also"></a><span data-ttu-id="101ae-116">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="101ae-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="101ae-117">Модель шейдеров 6</span><span class="sxs-lookup"><span data-stu-id="101ae-117">Shader Model 6</span></span>](shader-model-6-0.md)
</dt> </dl>

 

 




