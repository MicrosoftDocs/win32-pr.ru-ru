---
title: Texture2DMS
description: Тип Texture2DMS (как он существует в модели шейдеров 4) и переменные ресурсов.
ms.assetid: afda7324-680e-432a-a445-d90bd708e5e0
keywords:
- Texture2DMS HLSL
topic_type:
- apiref
api_name:
- Texture2DMS
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: c16c69a4fa0fd35ce7b12d69f880daa4b8345d02
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/25/2019
ms.locfileid: "104068884"
---
# <a name="texture2dms"></a><span data-ttu-id="da8f9-104">Texture2DMS</span><span class="sxs-lookup"><span data-stu-id="da8f9-104">Texture2DMS</span></span>

<span data-ttu-id="da8f9-105">Тип Texture2DMS (как он существует в модели шейдеров 4) и переменные ресурсов.</span><span class="sxs-lookup"><span data-stu-id="da8f9-105">Texture2DMS type (as it exists in Shader Model 4) plus resource variables.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="da8f9-106">В этом разделе</span><span class="sxs-lookup"><span data-stu-id="da8f9-106">In this section</span></span>



| <span data-ttu-id="da8f9-107">Раздел</span><span class="sxs-lookup"><span data-stu-id="da8f9-107">Topic</span></span>                                                                                    | <span data-ttu-id="da8f9-108">Описание</span><span class="sxs-lookup"><span data-stu-id="da8f9-108">Description</span></span>                                                                                 |
|------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| [<span data-ttu-id="da8f9-109">**GetDimensions**</span><span class="sxs-lookup"><span data-stu-id="da8f9-109">**GetDimensions**</span></span>](sm5-object-texture2dms-getdimensions.md)<br/>                 | <span data-ttu-id="da8f9-110">Возвращает размеры ресурса.</span><span class="sxs-lookup"><span data-stu-id="da8f9-110">Returns the dimensions of the resource.</span></span><br/>                                          |
| [<span data-ttu-id="da8f9-111">**жетсамплепоситион**</span><span class="sxs-lookup"><span data-stu-id="da8f9-111">**GetSamplePosition**</span></span>](sm5-object-texture2dms-getsampleposition.md)<br/>         | <span data-ttu-id="da8f9-112">Возвращает расположение образца для указанного индекса.</span><span class="sxs-lookup"><span data-stu-id="da8f9-112">Returns the sample position for the sample index provided.</span></span><br/>                       |
| [<span data-ttu-id="da8f9-113">**Методы Load**</span><span class="sxs-lookup"><span data-stu-id="da8f9-113">**Load methods**</span></span>](texture2dms-load.md)<br/>                                      | <span data-ttu-id="da8f9-114">Извлекает значение из ресурса в расположении и указанном индексе выборки.</span><span class="sxs-lookup"><span data-stu-id="da8f9-114">Retrieves a value from the resource at the location and sample index provided.</span></span><br/>   |
| <span data-ttu-id="da8f9-115">[**Следующий. Станции\[\]\[\]**](sm5-object-texture2dms-sampleoperatorindex.md)</span><span class="sxs-lookup"><span data-stu-id="da8f9-115">[**sample.Operator\[\]\[\]**](sm5-object-texture2dms-sampleoperatorindex.md)</span></span><br/> | <span data-ttu-id="da8f9-116">Извлекает значение из ресурса в расположении и указанном индексе выборки.</span><span class="sxs-lookup"><span data-stu-id="da8f9-116">Retrieves a value from the resource at the location and sample index provided.</span></span><br/>   |
| <span data-ttu-id="da8f9-117">[**Оператор\[\]**](sm5-object-texture2dms-operator1.md)</span><span class="sxs-lookup"><span data-stu-id="da8f9-117">[**Operator\[\]**](sm5-object-texture2dms-operator1.md)</span></span><br/>                      | <span data-ttu-id="da8f9-118">Извлекает значение из ресурса в расположении, указанном в примере индекса 0.</span><span class="sxs-lookup"><span data-stu-id="da8f9-118">Retrieves a value from the resource at the location provided at sample index 0.</span></span> <br/> |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="da8f9-119">Минимальная модель шейдера</span><span class="sxs-lookup"><span data-stu-id="da8f9-119">Minimum Shader Model</span></span>

<span data-ttu-id="da8f9-120">Этот объект поддерживается в следующих моделях шейдеров.</span><span class="sxs-lookup"><span data-stu-id="da8f9-120">This object is supported in the following shader models.</span></span>



| <span data-ttu-id="da8f9-121">Модель шейдера</span><span class="sxs-lookup"><span data-stu-id="da8f9-121">Shader Model</span></span>              | <span data-ttu-id="da8f9-122">Поддерживается</span><span class="sxs-lookup"><span data-stu-id="da8f9-122">Supported</span></span> |
|---------------------------|-----------|
| <span data-ttu-id="da8f9-123">Модель шейдеров 4 и выше</span><span class="sxs-lookup"><span data-stu-id="da8f9-123">Shader model 4 and higher</span></span> | <span data-ttu-id="da8f9-124">да</span><span class="sxs-lookup"><span data-stu-id="da8f9-124">yes</span></span>       |



 

<span data-ttu-id="da8f9-125">Этот объект поддерживается для следующих типов шейдеров:</span><span class="sxs-lookup"><span data-stu-id="da8f9-125">This object is supported for the following types of shaders:</span></span>



| <span data-ttu-id="da8f9-126">Вершина</span><span class="sxs-lookup"><span data-stu-id="da8f9-126">Vertex</span></span> | <span data-ttu-id="da8f9-127">Поверхности</span><span class="sxs-lookup"><span data-stu-id="da8f9-127">Hull</span></span> | <span data-ttu-id="da8f9-128">Домен</span><span class="sxs-lookup"><span data-stu-id="da8f9-128">Domain</span></span> | <span data-ttu-id="da8f9-129">Геометрия</span><span class="sxs-lookup"><span data-stu-id="da8f9-129">Geometry</span></span> | <span data-ttu-id="da8f9-130">Пиксель</span><span class="sxs-lookup"><span data-stu-id="da8f9-130">Pixel</span></span> | <span data-ttu-id="da8f9-131">Вычисления</span><span class="sxs-lookup"><span data-stu-id="da8f9-131">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="da8f9-132">x</span><span class="sxs-lookup"><span data-stu-id="da8f9-132">x</span></span>      | <span data-ttu-id="da8f9-133">x</span><span class="sxs-lookup"><span data-stu-id="da8f9-133">x</span></span>    | <span data-ttu-id="da8f9-134">x</span><span class="sxs-lookup"><span data-stu-id="da8f9-134">x</span></span>      | <span data-ttu-id="da8f9-135">x</span><span class="sxs-lookup"><span data-stu-id="da8f9-135">x</span></span>        | <span data-ttu-id="da8f9-136">x</span><span class="sxs-lookup"><span data-stu-id="da8f9-136">x</span></span>     | <span data-ttu-id="da8f9-137">x</span><span class="sxs-lookup"><span data-stu-id="da8f9-137">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="da8f9-138">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="da8f9-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="da8f9-139">Объекты модели шейдеров 5</span><span class="sxs-lookup"><span data-stu-id="da8f9-139">Shader Model 5 Objects</span></span>](d3d11-graphics-reference-sm5-objects.md)
</dt> </dl>

 

 





