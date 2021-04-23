---
title: инпутпатч
description: Представляет массив контрольных точек, доступных шейдеру поверхности в качестве входных данных.
ms.assetid: a2eeb45a-85b2-4ed0-b071-fcbb8abf4f2d
keywords:
- Инпутпатч HLSL
topic_type:
- apiref
api_name:
- InputPatch
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a882d032133ccb7bc98a34b3ef99551aa18fa51b
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/25/2019
ms.locfileid: "104996811"
---
# <a name="inputpatch"></a><span data-ttu-id="52287-104">инпутпатч</span><span class="sxs-lookup"><span data-stu-id="52287-104">InputPatch</span></span>

<span data-ttu-id="52287-105">Представляет массив контрольных точек, доступных шейдеру поверхности в качестве входных данных.</span><span class="sxs-lookup"><span data-stu-id="52287-105">Represents an array of control points that are available to the hull shader as inputs.</span></span>



| <span data-ttu-id="52287-106">Метод</span><span class="sxs-lookup"><span data-stu-id="52287-106">Method</span></span>                                                      | <span data-ttu-id="52287-107">Описание</span><span class="sxs-lookup"><span data-stu-id="52287-107">Description</span></span>                         |
|-------------------------------------------------------------|-------------------------------------|
| <span data-ttu-id="52287-108">[**Оператор\[\]**](sm5-object-inputpatch-operatorindex.md)</span><span class="sxs-lookup"><span data-stu-id="52287-108">[**Operator\[\]**](sm5-object-inputpatch-operatorindex.md)</span></span> | <span data-ttu-id="52287-109">Возвращает переменную ресурса, доступную только для чтения.</span><span class="sxs-lookup"><span data-stu-id="52287-109">Gets a read-only resource variable.</span></span> |



 

<span data-ttu-id="52287-110">Класс Инпутпатч также поддерживает следующие свойства:</span><span class="sxs-lookup"><span data-stu-id="52287-110">The InputPatch class also supports the following properties:</span></span>



| <span data-ttu-id="52287-111">Свойства</span><span class="sxs-lookup"><span data-stu-id="52287-111">Properties</span></span> | <span data-ttu-id="52287-112">Тип</span><span class="sxs-lookup"><span data-stu-id="52287-112">Type</span></span> | <span data-ttu-id="52287-113">Описание</span><span class="sxs-lookup"><span data-stu-id="52287-113">Description</span></span>                   |
|------------|------|-------------------------------|
| <span data-ttu-id="52287-114">Длина</span><span class="sxs-lookup"><span data-stu-id="52287-114">Length</span></span>     | <span data-ttu-id="52287-115">uint</span><span class="sxs-lookup"><span data-stu-id="52287-115">uint</span></span> | <span data-ttu-id="52287-116">Количество контрольных точек.</span><span class="sxs-lookup"><span data-stu-id="52287-116">The number of control points.</span></span> |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="52287-117">Минимальная модель шейдера</span><span class="sxs-lookup"><span data-stu-id="52287-117">Minimum Shader Model</span></span>

<span data-ttu-id="52287-118">Этот объект поддерживается в следующих моделях шейдеров.</span><span class="sxs-lookup"><span data-stu-id="52287-118">This object is supported in the following shader models.</span></span>



| <span data-ttu-id="52287-119">Модель шейдера</span><span class="sxs-lookup"><span data-stu-id="52287-119">Shader Model</span></span>                                                                | <span data-ttu-id="52287-120">Поддерживается</span><span class="sxs-lookup"><span data-stu-id="52287-120">Supported</span></span> |
|-----------------------------------------------------------------------------|-----------|
| <span data-ttu-id="52287-121">[Модели шейдера 5](d3d11-graphics-reference-sm5.md) и более поздних моделей шейдеров</span><span class="sxs-lookup"><span data-stu-id="52287-121">[Shader Model 5](d3d11-graphics-reference-sm5.md) and higher shader models</span></span> | <span data-ttu-id="52287-122">да</span><span class="sxs-lookup"><span data-stu-id="52287-122">yes</span></span>       |



 

<span data-ttu-id="52287-123">Этот объект поддерживается для следующих типов шейдеров:</span><span class="sxs-lookup"><span data-stu-id="52287-123">This object is supported for the following types of shaders:</span></span>



| <span data-ttu-id="52287-124">Вершина</span><span class="sxs-lookup"><span data-stu-id="52287-124">Vertex</span></span> | <span data-ttu-id="52287-125">Поверхности</span><span class="sxs-lookup"><span data-stu-id="52287-125">Hull</span></span> | <span data-ttu-id="52287-126">Домен</span><span class="sxs-lookup"><span data-stu-id="52287-126">Domain</span></span> | <span data-ttu-id="52287-127">Геометрия</span><span class="sxs-lookup"><span data-stu-id="52287-127">Geometry</span></span> | <span data-ttu-id="52287-128">Пиксель</span><span class="sxs-lookup"><span data-stu-id="52287-128">Pixel</span></span> | <span data-ttu-id="52287-129">Вычисления</span><span class="sxs-lookup"><span data-stu-id="52287-129">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        | <span data-ttu-id="52287-130">x</span><span class="sxs-lookup"><span data-stu-id="52287-130">x</span></span>    |        | <span data-ttu-id="52287-131">x</span><span class="sxs-lookup"><span data-stu-id="52287-131">x</span></span>        |       |         |



 

## <a name="see-also"></a><span data-ttu-id="52287-132">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="52287-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="52287-133">Объекты модели шейдеров 5</span><span class="sxs-lookup"><span data-stu-id="52287-133">Shader Model 5 Objects</span></span>](d3d11-graphics-reference-sm5-objects.md)
</dt> </dl>

 

 




