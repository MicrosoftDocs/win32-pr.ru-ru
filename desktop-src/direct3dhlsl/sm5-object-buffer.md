---
title: Буфер
description: Буфер
ms.assetid: 7f552b9b-c5fb-4bc2-a7ae-61983379db38
keywords:
- HLSL буфера
topic_type:
- apiref
api_name:
- Buffer
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ce1754272fd90cedc5a806543dd83a99cdcd9455
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/25/2019
ms.locfileid: "104411891"
---
# <a name="buffer"></a><span data-ttu-id="ddc27-104">Буфер</span><span class="sxs-lookup"><span data-stu-id="ddc27-104">Buffer</span></span>

<span data-ttu-id="ddc27-105">Тип буфера в том виде, в котором он существует в модели шейдеров 4, а также переменные ресурсов и сведения о буфере.</span><span class="sxs-lookup"><span data-stu-id="ddc27-105">Buffer type as it exists in Shader Model 4 plus resource variables and buffer info.</span></span>



| <span data-ttu-id="ddc27-106">Метод</span><span class="sxs-lookup"><span data-stu-id="ddc27-106">Method</span></span>                                                   | <span data-ttu-id="ddc27-107">Описание</span><span class="sxs-lookup"><span data-stu-id="ddc27-107">Description</span></span>                         |
|----------------------------------------------------------|-------------------------------------|
| [<span data-ttu-id="ddc27-108">**GetDimensions**</span><span class="sxs-lookup"><span data-stu-id="ddc27-108">**GetDimensions**</span></span>](sm5-object-buffer-getdimensions.md) | <span data-ttu-id="ddc27-109">Возвращает размеры ресурсов.</span><span class="sxs-lookup"><span data-stu-id="ddc27-109">Gets the resource dimensions.</span></span>       |
| [<span data-ttu-id="ddc27-110">**Загрузить**</span><span class="sxs-lookup"><span data-stu-id="ddc27-110">**Load**</span></span>](buffer-load.md)                              | <span data-ttu-id="ddc27-111">Считывает данные буфера.</span><span class="sxs-lookup"><span data-stu-id="ddc27-111">Reads buffer data.</span></span>                  |
| <span data-ttu-id="ddc27-112">[**Оператор\[\]**](sm5-object-buffer-operatorindex.md)</span><span class="sxs-lookup"><span data-stu-id="ddc27-112">[**Operator\[\]**](sm5-object-buffer-operatorindex.md)</span></span>  | <span data-ttu-id="ddc27-113">Возвращает переменную ресурса, доступную только для чтения.</span><span class="sxs-lookup"><span data-stu-id="ddc27-113">Gets a read-only resource variable.</span></span> |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="ddc27-114">Минимальная модель шейдера</span><span class="sxs-lookup"><span data-stu-id="ddc27-114">Minimum Shader Model</span></span>

<span data-ttu-id="ddc27-115">Этот объект поддерживается в следующих моделях шейдеров.</span><span class="sxs-lookup"><span data-stu-id="ddc27-115">This object is supported in the following shader models.</span></span>



| <span data-ttu-id="ddc27-116">Модель шейдера</span><span class="sxs-lookup"><span data-stu-id="ddc27-116">Shader Model</span></span>                                                                | <span data-ttu-id="ddc27-117">Поддерживается</span><span class="sxs-lookup"><span data-stu-id="ddc27-117">Supported</span></span> |
|-----------------------------------------------------------------------------|-----------|
| <span data-ttu-id="ddc27-118">[Модели шейдера 5](d3d11-graphics-reference-sm5.md) и более поздних моделей шейдеров</span><span class="sxs-lookup"><span data-stu-id="ddc27-118">[Shader Model 5](d3d11-graphics-reference-sm5.md) and higher shader models</span></span> | <span data-ttu-id="ddc27-119">да</span><span class="sxs-lookup"><span data-stu-id="ddc27-119">yes</span></span>       |



 

<span data-ttu-id="ddc27-120">Этот объект поддерживается для следующих типов шейдеров:</span><span class="sxs-lookup"><span data-stu-id="ddc27-120">This object is supported for the following types of shaders:</span></span>



| <span data-ttu-id="ddc27-121">Вершина</span><span class="sxs-lookup"><span data-stu-id="ddc27-121">Vertex</span></span> | <span data-ttu-id="ddc27-122">Поверхности</span><span class="sxs-lookup"><span data-stu-id="ddc27-122">Hull</span></span> | <span data-ttu-id="ddc27-123">Домен</span><span class="sxs-lookup"><span data-stu-id="ddc27-123">Domain</span></span> | <span data-ttu-id="ddc27-124">Геометрия</span><span class="sxs-lookup"><span data-stu-id="ddc27-124">Geometry</span></span> | <span data-ttu-id="ddc27-125">Пиксель</span><span class="sxs-lookup"><span data-stu-id="ddc27-125">Pixel</span></span> | <span data-ttu-id="ddc27-126">Вычисления</span><span class="sxs-lookup"><span data-stu-id="ddc27-126">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="ddc27-127">x</span><span class="sxs-lookup"><span data-stu-id="ddc27-127">x</span></span>      | <span data-ttu-id="ddc27-128">x</span><span class="sxs-lookup"><span data-stu-id="ddc27-128">x</span></span>    | <span data-ttu-id="ddc27-129">x</span><span class="sxs-lookup"><span data-stu-id="ddc27-129">x</span></span>      | <span data-ttu-id="ddc27-130">x</span><span class="sxs-lookup"><span data-stu-id="ddc27-130">x</span></span>        | <span data-ttu-id="ddc27-131">x</span><span class="sxs-lookup"><span data-stu-id="ddc27-131">x</span></span>     | <span data-ttu-id="ddc27-132">x</span><span class="sxs-lookup"><span data-stu-id="ddc27-132">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="ddc27-133">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ddc27-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ddc27-134">Объекты модели шейдеров 5</span><span class="sxs-lookup"><span data-stu-id="ddc27-134">Shader Model 5 Objects</span></span>](d3d11-graphics-reference-sm5-objects.md)
</dt> </dl>

 

 




