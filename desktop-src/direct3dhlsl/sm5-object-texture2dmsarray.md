---
title: Texture2DMSArray
description: Texture2DMSArray
ms.assetid: 4200eba8-a9e5-41ba-b04c-4ac7b20274d2
keywords:
- Texture2DMSArray HLSL
topic_type:
- apiref
api_name:
- Texture2DMSArray
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: effe4819c674a7909cc445b9e9f7b5322fae7676
ms.sourcegitcommit: 5724b38883e518ac565e1b266defa85ad0941bb2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/14/2021
ms.locfileid: "104273222"
---
# <a name="texture2dmsarray"></a><span data-ttu-id="565ed-104">Texture2DMSArray</span><span class="sxs-lookup"><span data-stu-id="565ed-104">Texture2DMSArray</span></span>

<span data-ttu-id="565ed-105">Тип Texture2DMSArray (как он существует в модели шейдеров 4) и переменные ресурсов.</span><span class="sxs-lookup"><span data-stu-id="565ed-105">Texture2DMSArray type (as it exists in Shader Model 4) plus resource variables.</span></span>



| <span data-ttu-id="565ed-106">Метод</span><span class="sxs-lookup"><span data-stu-id="565ed-106">Method</span></span>                                                                             | <span data-ttu-id="565ed-107">Описание</span><span class="sxs-lookup"><span data-stu-id="565ed-107">Description</span></span>                                        |
|------------------------------------------------------------------------------------|----------------------------------------------------|
| [<span data-ttu-id="565ed-108">**GetDimensions**</span><span class="sxs-lookup"><span data-stu-id="565ed-108">**GetDimensions**</span></span>](sm5-object-texture2dmsarray-getdimensions.md)                  | <span data-ttu-id="565ed-109">Возвращает размеры ресурсов.</span><span class="sxs-lookup"><span data-stu-id="565ed-109">Gets the resource dimensions.</span></span>                      |
| [<span data-ttu-id="565ed-110">**жетсамплепоситион**</span><span class="sxs-lookup"><span data-stu-id="565ed-110">**GetSamplePosition**</span></span>](sm5-object-texture2dmsarray-getsampleposition.md)          | <span data-ttu-id="565ed-111">Возвращает расположение указанного образца.</span><span class="sxs-lookup"><span data-stu-id="565ed-111">Gets the position of the specified sample.</span></span>         |
| [<span data-ttu-id="565ed-112">**Загрузить**</span><span class="sxs-lookup"><span data-stu-id="565ed-112">**Load**</span></span>](texture2dmsarray-load.md)                                               | <span data-ttu-id="565ed-113">Возвращает одно значение.</span><span class="sxs-lookup"><span data-stu-id="565ed-113">Gets one value.</span></span>                                    |
| <span data-ttu-id="565ed-114">[**Следующий. Станции\[\]\[\]**](sm5-object-texture2dmsarray-sampleoperatorindex.md)</span><span class="sxs-lookup"><span data-stu-id="565ed-114">[**sample.Operator\[\]\[\]**](sm5-object-texture2dmsarray-sampleoperatorindex.md)</span></span>  | <span data-ttu-id="565ed-115">Возвращает переменную ресурса, доступную только для чтения.</span><span class="sxs-lookup"><span data-stu-id="565ed-115">Gets a read-only resource variable.</span></span>                |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="565ed-116">Минимальная модель шейдера</span><span class="sxs-lookup"><span data-stu-id="565ed-116">Minimum Shader Model</span></span>

<span data-ttu-id="565ed-117">Этот объект поддерживается в следующих моделях шейдеров.</span><span class="sxs-lookup"><span data-stu-id="565ed-117">This object is supported in the following shader models.</span></span>



| <span data-ttu-id="565ed-118">Модель шейдера</span><span class="sxs-lookup"><span data-stu-id="565ed-118">Shader Model</span></span>                                                                | <span data-ttu-id="565ed-119">Поддерживается</span><span class="sxs-lookup"><span data-stu-id="565ed-119">Supported</span></span> |
|-----------------------------------------------------------------------------|-----------|
| <span data-ttu-id="565ed-120">[Модели шейдера 5](d3d11-graphics-reference-sm5.md) и более поздних моделей шейдеров</span><span class="sxs-lookup"><span data-stu-id="565ed-120">[Shader Model 5](d3d11-graphics-reference-sm5.md) and higher shader models</span></span> | <span data-ttu-id="565ed-121">да</span><span class="sxs-lookup"><span data-stu-id="565ed-121">yes</span></span>       |



 

<span data-ttu-id="565ed-122">Этот объект поддерживается для следующих типов шейдеров:</span><span class="sxs-lookup"><span data-stu-id="565ed-122">This object is supported for the following types of shaders:</span></span>



| <span data-ttu-id="565ed-123">Вершина</span><span class="sxs-lookup"><span data-stu-id="565ed-123">Vertex</span></span> | <span data-ttu-id="565ed-124">Поверхности</span><span class="sxs-lookup"><span data-stu-id="565ed-124">Hull</span></span> | <span data-ttu-id="565ed-125">Домен</span><span class="sxs-lookup"><span data-stu-id="565ed-125">Domain</span></span> | <span data-ttu-id="565ed-126">Геометрия</span><span class="sxs-lookup"><span data-stu-id="565ed-126">Geometry</span></span> | <span data-ttu-id="565ed-127">Пиксель</span><span class="sxs-lookup"><span data-stu-id="565ed-127">Pixel</span></span> | <span data-ttu-id="565ed-128">Вычисления</span><span class="sxs-lookup"><span data-stu-id="565ed-128">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="565ed-129">x</span><span class="sxs-lookup"><span data-stu-id="565ed-129">x</span></span>      | <span data-ttu-id="565ed-130">x</span><span class="sxs-lookup"><span data-stu-id="565ed-130">x</span></span>    | <span data-ttu-id="565ed-131">x</span><span class="sxs-lookup"><span data-stu-id="565ed-131">x</span></span>      | <span data-ttu-id="565ed-132">x</span><span class="sxs-lookup"><span data-stu-id="565ed-132">x</span></span>        | <span data-ttu-id="565ed-133">x</span><span class="sxs-lookup"><span data-stu-id="565ed-133">x</span></span>     | <span data-ttu-id="565ed-134">x</span><span class="sxs-lookup"><span data-stu-id="565ed-134">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="565ed-135">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="565ed-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="565ed-136">Объекты модели шейдеров 5</span><span class="sxs-lookup"><span data-stu-id="565ed-136">Shader Model 5 Objects</span></span>](d3d11-graphics-reference-sm5-objects.md)
</dt> </dl>

 

 




