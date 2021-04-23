---
title: аутпутпатч
description: аутпутпатч
ms.assetid: 24841938-6c84-4e1f-ba8a-a81b589bdd51
keywords:
- Аутпутпатч HLSL
topic_type:
- apiref
api_name:
- OutputPatch
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 4c77a30a2ff23bdc292d45df6514ef00fab53463
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/25/2019
ms.locfileid: "104068844"
---
# <a name="outputpatch"></a><span data-ttu-id="e7631-104">аутпутпатч</span><span class="sxs-lookup"><span data-stu-id="e7631-104">OutputPatch</span></span>

<span data-ttu-id="e7631-105">Представляет массив контрольных точек вывода, доступных для функции исправления и константы поверхности шейдера, а также шейдера домена.</span><span class="sxs-lookup"><span data-stu-id="e7631-105">Represents an array of output control points that are available to the hull shader's patch-constant function as well as the domain shader.</span></span>



| <span data-ttu-id="e7631-106">Метод</span><span class="sxs-lookup"><span data-stu-id="e7631-106">Method</span></span>                                                       | <span data-ttu-id="e7631-107">Описание</span><span class="sxs-lookup"><span data-stu-id="e7631-107">Description</span></span>                         |
|--------------------------------------------------------------|-------------------------------------|
| <span data-ttu-id="e7631-108">[**Оператор\[\]**](sm5-object-outputpatch-operatorindex.md)</span><span class="sxs-lookup"><span data-stu-id="e7631-108">[**Operator\[\]**](sm5-object-outputpatch-operatorindex.md)</span></span> | <span data-ttu-id="e7631-109">Возвращает переменную ресурса, доступную только для чтения.</span><span class="sxs-lookup"><span data-stu-id="e7631-109">Gets a read-only resource variable.</span></span> |



 

<span data-ttu-id="e7631-110">Кроме того, класс Инпутпатч поддерживает следующие свойства:</span><span class="sxs-lookup"><span data-stu-id="e7631-110">In addition, the InputPatch class supports the following properties:</span></span>



| <span data-ttu-id="e7631-111">Свойства</span><span class="sxs-lookup"><span data-stu-id="e7631-111">Properties</span></span> | <span data-ttu-id="e7631-112">Тип</span><span class="sxs-lookup"><span data-stu-id="e7631-112">Type</span></span> | <span data-ttu-id="e7631-113">Описание</span><span class="sxs-lookup"><span data-stu-id="e7631-113">Description</span></span>                   |
|------------|------|-------------------------------|
| <span data-ttu-id="e7631-114">Длина</span><span class="sxs-lookup"><span data-stu-id="e7631-114">Length</span></span>     | <span data-ttu-id="e7631-115">uint</span><span class="sxs-lookup"><span data-stu-id="e7631-115">uint</span></span> | <span data-ttu-id="e7631-116">Количество контрольных точек.</span><span class="sxs-lookup"><span data-stu-id="e7631-116">The number of control points.</span></span> |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="e7631-117">Минимальная модель шейдера</span><span class="sxs-lookup"><span data-stu-id="e7631-117">Minimum Shader Model</span></span>

<span data-ttu-id="e7631-118">Этот объект поддерживается в следующих моделях шейдеров.</span><span class="sxs-lookup"><span data-stu-id="e7631-118">This object is supported in the following shader models.</span></span>



| <span data-ttu-id="e7631-119">Модель шейдера</span><span class="sxs-lookup"><span data-stu-id="e7631-119">Shader Model</span></span>                                                                | <span data-ttu-id="e7631-120">Поддерживается</span><span class="sxs-lookup"><span data-stu-id="e7631-120">Supported</span></span> |
|-----------------------------------------------------------------------------|-----------|
| <span data-ttu-id="e7631-121">[Модели шейдера 5](d3d11-graphics-reference-sm5.md) и более поздних моделей шейдеров</span><span class="sxs-lookup"><span data-stu-id="e7631-121">[Shader Model 5](d3d11-graphics-reference-sm5.md) and higher shader models</span></span> | <span data-ttu-id="e7631-122">да</span><span class="sxs-lookup"><span data-stu-id="e7631-122">yes</span></span>       |



 

<span data-ttu-id="e7631-123">Этот объект поддерживается для следующих типов шейдеров:</span><span class="sxs-lookup"><span data-stu-id="e7631-123">This object is supported for the following types of shaders:</span></span>



| <span data-ttu-id="e7631-124">Вершина</span><span class="sxs-lookup"><span data-stu-id="e7631-124">Vertex</span></span> | <span data-ttu-id="e7631-125">Поверхности</span><span class="sxs-lookup"><span data-stu-id="e7631-125">Hull</span></span> | <span data-ttu-id="e7631-126">Домен</span><span class="sxs-lookup"><span data-stu-id="e7631-126">Domain</span></span> | <span data-ttu-id="e7631-127">Геометрия</span><span class="sxs-lookup"><span data-stu-id="e7631-127">Geometry</span></span> | <span data-ttu-id="e7631-128">Пиксель</span><span class="sxs-lookup"><span data-stu-id="e7631-128">Pixel</span></span> | <span data-ttu-id="e7631-129">Вычисления</span><span class="sxs-lookup"><span data-stu-id="e7631-129">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        | <span data-ttu-id="e7631-130">x</span><span class="sxs-lookup"><span data-stu-id="e7631-130">x</span></span>    | <span data-ttu-id="e7631-131">x</span><span class="sxs-lookup"><span data-stu-id="e7631-131">x</span></span>      |          |       |         |



 

## <a name="see-also"></a><span data-ttu-id="e7631-132">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e7631-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e7631-133">Объекты модели шейдеров 5</span><span class="sxs-lookup"><span data-stu-id="e7631-133">Shader Model 5 Objects</span></span>](d3d11-graphics-reference-sm5-objects.md)
</dt> </dl>

 

 




