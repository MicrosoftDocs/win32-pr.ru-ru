---
title: Функция Куадреадланеат
description: Возвращает указанное исходное значение из полосы, определяемой ИДЕНТИФИКАТОРом полосы в текущем объекте Quad.
ms.assetid: 5CD7EE4C-E64E-46A3-ABDC-1BF65D0F96BE
keywords:
- Функция Куадреадланеат HLSL
topic_type:
- apiref
api_name:
- QuadReadLaneAt
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ddc772c2dca66873891483431eab14ad504da77e
ms.sourcegitcommit: f01bc6744cea55ad1aeeace7981a30b567e6fe60
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/04/2020
ms.locfileid: "104488535"
---
# <a name="quadreadlaneat-function"></a><span data-ttu-id="f10b4-104">Функция Куадреадланеат</span><span class="sxs-lookup"><span data-stu-id="f10b4-104">QuadReadLaneAt function</span></span>

<span data-ttu-id="f10b4-105">Возвращает указанное исходное значение из полосы, определяемой ИДЕНТИФИКАТОРом полосы в текущем объекте Quad.</span><span class="sxs-lookup"><span data-stu-id="f10b4-105">Returns the specified source value from the lane identified by the lane ID within the current quad.</span></span>

## <a name="syntax"></a><span data-ttu-id="f10b4-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f10b4-106">Syntax</span></span>


``` syntax
<type> QuadReadLaneAt(
   <type> sourceValue,
   uint   quadLaneID  
);
```



## <a name="parameters"></a><span data-ttu-id="f10b4-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="f10b4-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f10b4-108">*саурцевалуе*</span><span class="sxs-lookup"><span data-stu-id="f10b4-108">*sourceValue*</span></span> 
</dt> <dd>

<span data-ttu-id="f10b4-109">Запрошенный тип.</span><span class="sxs-lookup"><span data-stu-id="f10b4-109">The requested type.</span></span>

</dd> <dt>

<span data-ttu-id="f10b4-110">*куадланеид*</span><span class="sxs-lookup"><span data-stu-id="f10b4-110">*quadLaneID*</span></span> 
</dt> <dd>

<span data-ttu-id="f10b4-111">Идентификатор полосы; оно будет иметь значение от 0 до 3.</span><span class="sxs-lookup"><span data-stu-id="f10b4-111">The lane ID; this will be a value from 0 to 3.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f10b4-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="f10b4-112">Return value</span></span>

<span data-ttu-id="f10b4-113">Указанное исходное значение.</span><span class="sxs-lookup"><span data-stu-id="f10b4-113">The specified source value.</span></span> <span data-ttu-id="f10b4-114">Результат этой функции является единообразным по отношению к четырем.</span><span class="sxs-lookup"><span data-stu-id="f10b4-114">The result of this function is uniform across the quad.</span></span> <span data-ttu-id="f10b4-115">Если исходная полоса неактивна, результаты будут неопределенными.</span><span class="sxs-lookup"><span data-stu-id="f10b4-115">If the source lane is inactive, the results are undefined.</span></span>

## <a name="remarks"></a><span data-ttu-id="f10b4-116">Примечания</span><span class="sxs-lookup"><span data-stu-id="f10b4-116">Remarks</span></span>

<span data-ttu-id="f10b4-117">Дополнительные сведения об четырехъядерях см. в разделе [Общие сведения о модели шейдеров 6](hlsl-shader-model-6-0-features-for-direct3d-12.md).</span><span class="sxs-lookup"><span data-stu-id="f10b4-117">For more information on quads, refer to [Overview of Shader Model 6](hlsl-shader-model-6-0-features-for-direct3d-12.md).</span></span>

<span data-ttu-id="f10b4-118">Эта функция поддерживается из модели шейдеров 6,0 только в пиксельных шейдерах и.</span><span class="sxs-lookup"><span data-stu-id="f10b4-118">This function is supported from shader model 6.0 only in pixel and compute shaders.</span></span>



 

## <a name="see-also"></a><span data-ttu-id="f10b4-119">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f10b4-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f10b4-120">Модель шейдеров 6</span><span class="sxs-lookup"><span data-stu-id="f10b4-120">Shader Model 6</span></span>](shader-model-6-0.md)
</dt> </dl>

 

 




