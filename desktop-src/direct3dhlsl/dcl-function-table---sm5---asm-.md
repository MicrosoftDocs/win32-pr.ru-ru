---
title: dcl_function_table (SM5-ASM)
description: Объявите таблицу функций.
ms.assetid: 3693A03F-5E4B-40E8-B436-2FE3462C8DB8
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0710f53171ad2a86097dca96afb2756b1b067fef
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/20/2019
ms.locfileid: "104996994"
---
# <a name="dcl_function_table-sm5---asm"></a><span data-ttu-id="d7599-103">\_Таблица функций дкл \_ (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="d7599-103">dcl\_function\_table (sm5 - asm)</span></span>

<span data-ttu-id="d7599-104">Объявите таблицу функций.</span><span class="sxs-lookup"><span data-stu-id="d7599-104">Declare a function table.</span></span>



| <span data-ttu-id="d7599-105">дкл \_ функция \_ таблицы ft \# = {FB \# , FB \# ,...}</span><span class="sxs-lookup"><span data-stu-id="d7599-105">dcl\_function\_table ft\# = {fb\#, fb\#, ...}</span></span> |
|-----------------------------------------------|



 



| <span data-ttu-id="d7599-106">Элемент</span><span class="sxs-lookup"><span data-stu-id="d7599-106">Item</span></span>                                                      | <span data-ttu-id="d7599-107">Описание</span><span class="sxs-lookup"><span data-stu-id="d7599-107">Description</span></span>                                   |
|-----------------------------------------------------------|-----------------------------------------------|
| <span data-ttu-id="d7599-108"><span id="ft"></span><span id="FT"></span>*ФТ*</span><span class="sxs-lookup"><span data-stu-id="d7599-108"><span id="ft"></span><span id="FT"></span>*ft*</span></span><br/> | <span data-ttu-id="d7599-109">\[в \] записях таблицы функций.</span><span class="sxs-lookup"><span data-stu-id="d7599-109">\[in\] The function table entries.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="d7599-110">Примечания</span><span class="sxs-lookup"><span data-stu-id="d7599-110">Remarks</span></span>

<span data-ttu-id="d7599-111">Эта функция объявляет таблицу функций как набор частей тела функции, объявленных ранее.</span><span class="sxs-lookup"><span data-stu-id="d7599-111">This function declares a function table as a set of function bodies that have been declared earlier.</span></span>

<span data-ttu-id="d7599-112">Это аналогично виртуальной таблицей с + #, за исключением наличия записи для каждого узла вызова интерфейса, а не для каждого метода.</span><span class="sxs-lookup"><span data-stu-id="d7599-112">This is like a C++ vtable except there is an entry per call site for an interface instead of per method.</span></span>

<span data-ttu-id="d7599-113">В таблице функций не предусмотрено ограничений на количество основных частей функций.</span><span class="sxs-lookup"><span data-stu-id="d7599-113">There is no limit to how many function bodies can be listed in a function table.</span></span>

<span data-ttu-id="d7599-114">\#В одной или нескольких таблицах функций допускается несколько ссылок на FB тела функции, что позволяет совместно использовать общий код.</span><span class="sxs-lookup"><span data-stu-id="d7599-114">It is valid for a given function body fb\# to be referenced multiple times in one or more function tables, as a way of sharing common code.</span></span>

<span data-ttu-id="d7599-115">Эта инструкция применяется к следующим этапам шейдера:</span><span class="sxs-lookup"><span data-stu-id="d7599-115">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="d7599-116">Вершина</span><span class="sxs-lookup"><span data-stu-id="d7599-116">Vertex</span></span> | <span data-ttu-id="d7599-117">Поверхности</span><span class="sxs-lookup"><span data-stu-id="d7599-117">Hull</span></span> | <span data-ttu-id="d7599-118">Домен</span><span class="sxs-lookup"><span data-stu-id="d7599-118">Domain</span></span> | <span data-ttu-id="d7599-119">Геометрия</span><span class="sxs-lookup"><span data-stu-id="d7599-119">Geometry</span></span> | <span data-ttu-id="d7599-120">Пиксель</span><span class="sxs-lookup"><span data-stu-id="d7599-120">Pixel</span></span> | <span data-ttu-id="d7599-121">Вычисления</span><span class="sxs-lookup"><span data-stu-id="d7599-121">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="d7599-122">X</span><span class="sxs-lookup"><span data-stu-id="d7599-122">X</span></span>      | <span data-ttu-id="d7599-123">X</span><span class="sxs-lookup"><span data-stu-id="d7599-123">X</span></span>    | <span data-ttu-id="d7599-124">X</span><span class="sxs-lookup"><span data-stu-id="d7599-124">X</span></span>      | <span data-ttu-id="d7599-125">X</span><span class="sxs-lookup"><span data-stu-id="d7599-125">X</span></span>        | <span data-ttu-id="d7599-126">X</span><span class="sxs-lookup"><span data-stu-id="d7599-126">X</span></span>     | <span data-ttu-id="d7599-127">X</span><span class="sxs-lookup"><span data-stu-id="d7599-127">X</span></span>       |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="d7599-128">Минимальная модель шейдера</span><span class="sxs-lookup"><span data-stu-id="d7599-128">Minimum Shader Model</span></span>

<span data-ttu-id="d7599-129">Эта инструкция поддерживается в следующих моделях шейдеров:</span><span class="sxs-lookup"><span data-stu-id="d7599-129">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="d7599-130">Модель шейдера</span><span class="sxs-lookup"><span data-stu-id="d7599-130">Shader Model</span></span>                                              | <span data-ttu-id="d7599-131">Поддерживается</span><span class="sxs-lookup"><span data-stu-id="d7599-131">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="d7599-132">Модель шейдера 5</span><span class="sxs-lookup"><span data-stu-id="d7599-132">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="d7599-133">да</span><span class="sxs-lookup"><span data-stu-id="d7599-133">yes</span></span>       |
| [<span data-ttu-id="d7599-134">Модель шейдера 4,1</span><span class="sxs-lookup"><span data-stu-id="d7599-134">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="d7599-135">Нет</span><span class="sxs-lookup"><span data-stu-id="d7599-135">no</span></span>        |
| [<span data-ttu-id="d7599-136">Модель шейдера 4</span><span class="sxs-lookup"><span data-stu-id="d7599-136">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="d7599-137">Нет</span><span class="sxs-lookup"><span data-stu-id="d7599-137">no</span></span>        |
| [<span data-ttu-id="d7599-138">Модель шейдера 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="d7599-138">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="d7599-139">Нет</span><span class="sxs-lookup"><span data-stu-id="d7599-139">no</span></span>        |
| [<span data-ttu-id="d7599-140">Модель шейдера 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="d7599-140">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="d7599-141">Нет</span><span class="sxs-lookup"><span data-stu-id="d7599-141">no</span></span>        |
| [<span data-ttu-id="d7599-142">Модель шейдера 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="d7599-142">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="d7599-143">Нет</span><span class="sxs-lookup"><span data-stu-id="d7599-143">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="d7599-144">См. также</span><span class="sxs-lookup"><span data-stu-id="d7599-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d7599-145">Сборка Shader Model 5 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="d7599-145">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





