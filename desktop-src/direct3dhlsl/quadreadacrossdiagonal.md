---
title: Функция Куадреадакроссдиагонал
description: Возвращает заданное локальное значение, которое считывается с диагонального противоположного полосы в данном Quad.
ms.assetid: 2914F1F9-5CE2-437A-ADDB-4955D2C1490B
keywords:
- Функция Куадреадакроссдиагонал HLSL
topic_type:
- apiref
api_name:
- QuadReadAcrossDiagonal
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 0e208a022f339e69ea63120db1f67070fa4dfed7
ms.sourcegitcommit: f01bc6744cea55ad1aeeace7981a30b567e6fe60
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/04/2020
ms.locfileid: "104997182"
---
# <a name="quadreadacrossdiagonal-function"></a><span data-ttu-id="1a91e-104">Функция Куадреадакроссдиагонал</span><span class="sxs-lookup"><span data-stu-id="1a91e-104">QuadReadAcrossDiagonal function</span></span>

<span data-ttu-id="1a91e-105">Возвращает заданное локальное значение, которое считывается с диагонального противоположного полосы в данном Quad.</span><span class="sxs-lookup"><span data-stu-id="1a91e-105">Returns the specified local value which is read from the diagonally opposite lane in this quad.</span></span>

## <a name="syntax"></a><span data-ttu-id="1a91e-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="1a91e-106">Syntax</span></span>


``` syntax
<type> QuadReadAcrossDiagonal(
   <type> localValue
);
```



## <a name="parameters"></a><span data-ttu-id="1a91e-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="1a91e-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1a91e-108">*локалвалуе*</span><span class="sxs-lookup"><span data-stu-id="1a91e-108">*localValue*</span></span> 
</dt> <dd>

<span data-ttu-id="1a91e-109">Запрошенный тип.</span><span class="sxs-lookup"><span data-stu-id="1a91e-109">The requested type.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1a91e-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="1a91e-110">Return value</span></span>

<span data-ttu-id="1a91e-111">Заданное локальное значение, которое считывается с диагонального противоположного полосы в данном Quad.</span><span class="sxs-lookup"><span data-stu-id="1a91e-111">The specified local value which is read from the diagonally opposite lane in this quad.</span></span>

## <a name="remarks"></a><span data-ttu-id="1a91e-112">Примечания</span><span class="sxs-lookup"><span data-stu-id="1a91e-112">Remarks</span></span>

<span data-ttu-id="1a91e-113">Дополнительные сведения об четырехъядерях см. в разделе [Общие сведения о модели шейдеров 6](hlsl-shader-model-6-0-features-for-direct3d-12.md).</span><span class="sxs-lookup"><span data-stu-id="1a91e-113">For more information on quads, refer to [Overview of Shader Model 6](hlsl-shader-model-6-0-features-for-direct3d-12.md).</span></span>

<span data-ttu-id="1a91e-114">Эта функция поддерживается из модели шейдеров 6,0 только в пиксельных шейдерах и.</span><span class="sxs-lookup"><span data-stu-id="1a91e-114">This function is supported from shader model 6.0 only in pixel and compute shaders.</span></span>



 

## <a name="see-also"></a><span data-ttu-id="1a91e-115">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="1a91e-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1a91e-116">Модель шейдеров 6</span><span class="sxs-lookup"><span data-stu-id="1a91e-116">Shader Model 6</span></span>](shader-model-6-0.md)
</dt> </dl>

 

 




