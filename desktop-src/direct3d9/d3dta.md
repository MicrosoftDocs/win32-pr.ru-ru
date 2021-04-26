---
description: 'Константы аргумента текстуры используются в качестве значений для следующих элементов перечисляемого типа D3DTEXTURESTAGESTATETYPE:'
ms.assetid: 36b2b715-5ced-4246-840e-8ea343521ef4
title: D3DTA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 898e1bb66f74a1087a9da186599469bb195734ce
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/26/2021
ms.locfileid: "107995291"
---
# <a name="d3dta"></a><span data-ttu-id="42763-103">D3DTA</span><span class="sxs-lookup"><span data-stu-id="42763-103">D3DTA</span></span>

<span data-ttu-id="42763-104">Константы аргумента текстуры используются в качестве значений для следующих элементов перечисляемого типа [**D3DTEXTURESTAGESTATETYPE**](./d3dtexturestagestatetype.md) :</span><span class="sxs-lookup"><span data-stu-id="42763-104">Texture argument constants are used as values for the following members of the [**D3DTEXTURESTAGESTATETYPE**](./d3dtexturestagestatetype.md) enumerated type:</span></span>

-   <span data-ttu-id="42763-105">D3DTSS \_ ALPHAARG0</span><span class="sxs-lookup"><span data-stu-id="42763-105">D3DTSS\_ALPHAARG0</span></span>
-   <span data-ttu-id="42763-106">D3DTSS \_ ALPHAARG1</span><span class="sxs-lookup"><span data-stu-id="42763-106">D3DTSS\_ALPHAARG1</span></span>
-   <span data-ttu-id="42763-107">D3DTSS \_ ALPHAARG2</span><span class="sxs-lookup"><span data-stu-id="42763-107">D3DTSS\_ALPHAARG2</span></span>
-   <span data-ttu-id="42763-108">D3DTSS \_ COLORARG0</span><span class="sxs-lookup"><span data-stu-id="42763-108">D3DTSS\_COLORARG0</span></span>
-   <span data-ttu-id="42763-109">D3DTSS \_ COLORARG1</span><span class="sxs-lookup"><span data-stu-id="42763-109">D3DTSS\_COLORARG1</span></span>
-   <span data-ttu-id="42763-110">D3DTSS \_ COLORARG2</span><span class="sxs-lookup"><span data-stu-id="42763-110">D3DTSS\_COLORARG2</span></span>
-   <span data-ttu-id="42763-111">D3DTSS \_ ресултарг</span><span class="sxs-lookup"><span data-stu-id="42763-111">D3DTSS\_RESULTARG</span></span>

<span data-ttu-id="42763-112">Задайте и извлеките аргументы текстуры, вызвав методы [**сеттекстурестажестате**](/windows/desktop/api) и [**жеттекстурестажестате**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-gettexturestagestate) .</span><span class="sxs-lookup"><span data-stu-id="42763-112">Set and retrieve texture arguments by calling the [**SetTextureStageState**](/windows/desktop/api) and [**GetTextureStageState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-gettexturestagestate) methods.</span></span>

<span data-ttu-id="42763-113">Флаги аргументов</span><span class="sxs-lookup"><span data-stu-id="42763-113">Argument flags</span></span>

<span data-ttu-id="42763-114">Флаг аргумента можно объединить с модификатором, но нельзя сочетать два флага аргумента.</span><span class="sxs-lookup"><span data-stu-id="42763-114">You can combine an argument flag with a modifier, but two argument flags cannot be combined.</span></span>



| <span data-ttu-id="42763-115">\#определенно</span><span class="sxs-lookup"><span data-stu-id="42763-115">\#define</span></span>          | <span data-ttu-id="42763-116">Описание</span><span class="sxs-lookup"><span data-stu-id="42763-116">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
|-------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="42763-117">\_Константа D3DTA</span><span class="sxs-lookup"><span data-stu-id="42763-117">D3DTA\_CONSTANT</span></span>   | <span data-ttu-id="42763-118">Выберите константу на стадии текстуры.</span><span class="sxs-lookup"><span data-stu-id="42763-118">Select a constant from a texture stage.</span></span> <span data-ttu-id="42763-119">Значение по умолчанию — 0xFFFFFFFF.</span><span class="sxs-lookup"><span data-stu-id="42763-119">The default value is 0xffffffff.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| <span data-ttu-id="42763-120">D3DTA \_ текущий</span><span class="sxs-lookup"><span data-stu-id="42763-120">D3DTA\_CURRENT</span></span>    | <span data-ttu-id="42763-121">Аргумент текстуры является результатом предыдущего этапа смешения.</span><span class="sxs-lookup"><span data-stu-id="42763-121">The texture argument is the result of the previous blending stage.</span></span> <span data-ttu-id="42763-122">На первой стадии текстуры (этап 0) этот аргумент эквивалентен D3DTA \_ диффузии.</span><span class="sxs-lookup"><span data-stu-id="42763-122">In the first texture stage (stage 0), this argument is equivalent to D3DTA\_DIFFUSE.</span></span> <span data-ttu-id="42763-123">Если предыдущий этап наложения использует текстуру-карту выпуклости (D3DTOP \_ бумпенвмап), система выбирает текстуру из этапа перед текстурой схемы выпуклости.</span><span class="sxs-lookup"><span data-stu-id="42763-123">If the previous blending stage uses a bump-map texture (the D3DTOP\_BUMPENVMAP operation), the system chooses the texture from the stage before the bump-map texture.</span></span> <span data-ttu-id="42763-124">Если параметр s представляет текущую стадию текстуры, а s-1 содержит текстуру с картой выпуклости, то этот аргумент станет выходным результатом на этапе текстуры s-2.</span><span class="sxs-lookup"><span data-stu-id="42763-124">If s represents the current texture stage and s - 1 contains a bump-map texture, this argument becomes the result output by texture stage s - 2.</span></span> <span data-ttu-id="42763-125">Разрешения доступны для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="42763-125">Permissions are read/write.</span></span> |
| <span data-ttu-id="42763-126">D3DTA \_ диффузный</span><span class="sxs-lookup"><span data-stu-id="42763-126">D3DTA\_DIFFUSE</span></span>    | <span data-ttu-id="42763-127">Аргумент текстуры — это рассеянный цвет, интерполируются от компонентов вершины во время заливки по методу Гуро.</span><span class="sxs-lookup"><span data-stu-id="42763-127">The texture argument is the diffuse color interpolated from vertex components during Gouraud shading.</span></span> <span data-ttu-id="42763-128">Если вершина не содержит рассеянного цвета, по умолчанию используется цвет 0xFFFFFFFF.</span><span class="sxs-lookup"><span data-stu-id="42763-128">If the vertex does not contain a diffuse color, the default color is 0xffffffff.</span></span> <span data-ttu-id="42763-129">Разрешения доступны только для чтения.</span><span class="sxs-lookup"><span data-stu-id="42763-129">Permissions are read-only.</span></span>                                                                                                                                                                                                                                                                                          |
| <span data-ttu-id="42763-130">D3DTA \_ селектмаск</span><span class="sxs-lookup"><span data-stu-id="42763-130">D3DTA\_SELECTMASK</span></span> | <span data-ttu-id="42763-131">Значение маски для всех аргументов; не используется при задании аргументов текстуры.</span><span class="sxs-lookup"><span data-stu-id="42763-131">Mask value for all arguments; not used when setting texture arguments.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| <span data-ttu-id="42763-132">\_Зеркальное отражение D3DTA</span><span class="sxs-lookup"><span data-stu-id="42763-132">D3DTA\_SPECULAR</span></span>   | <span data-ttu-id="42763-133">Аргумент текстуры — это отраженный цвет, интерполируются от компонентов вершины во время заливки по методу Гуро.</span><span class="sxs-lookup"><span data-stu-id="42763-133">The texture argument is the specular color interpolated from vertex components during Gouraud shading.</span></span> <span data-ttu-id="42763-134">Если вершина не содержит отраженного цвета, по умолчанию используется цвет 0xFFFFFFFF.</span><span class="sxs-lookup"><span data-stu-id="42763-134">If the vertex does not contain a specular color, the default color is 0xffffffff.</span></span> <span data-ttu-id="42763-135">Разрешения доступны только для чтения.</span><span class="sxs-lookup"><span data-stu-id="42763-135">Permissions are read-only.</span></span>                                                                                                                                                                                                                                                                                        |
| <span data-ttu-id="42763-136">D3DTA \_ TEMP</span><span class="sxs-lookup"><span data-stu-id="42763-136">D3DTA\_TEMP</span></span>       | <span data-ttu-id="42763-137">Аргумент текстуры — это временный цвет регистров для чтения или записи.</span><span class="sxs-lookup"><span data-stu-id="42763-137">The texture argument is a temporary register color for read or write.</span></span> <span data-ttu-id="42763-138">D3DTA \_ TEMP поддерживается, если имеется возможность устройства [D3DPMISCCAPS \_ тссаргтемп](d3dpmisccaps.md) .</span><span class="sxs-lookup"><span data-stu-id="42763-138">D3DTA\_TEMP is supported if the [D3DPMISCCAPS\_TSSARGTEMP](d3dpmisccaps.md) device capability is present.</span></span> <span data-ttu-id="42763-139">По умолчанию регистр имеет значение (0,0, 0,0, 0,0, 0,0).</span><span class="sxs-lookup"><span data-stu-id="42763-139">The default value for the register is (0.0, 0.0, 0.0, 0.0).</span></span> <span data-ttu-id="42763-140">Разрешения доступны для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="42763-140">Permissions are read/write.</span></span>                                                                                                                                                                                                                                   |
| <span data-ttu-id="42763-141">\_Текстура D3DTA</span><span class="sxs-lookup"><span data-stu-id="42763-141">D3DTA\_TEXTURE</span></span>    | <span data-ttu-id="42763-142">Аргумент текстуры — это цвет текстуры для этой стадии текстуры.</span><span class="sxs-lookup"><span data-stu-id="42763-142">The texture argument is the texture color for this texture stage.</span></span> <span data-ttu-id="42763-143">Разрешения доступны только для чтения.</span><span class="sxs-lookup"><span data-stu-id="42763-143">Permissions are read-only.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                               |
| <span data-ttu-id="42763-144">D3DTA \_ тфактор</span><span class="sxs-lookup"><span data-stu-id="42763-144">D3DTA\_TFACTOR</span></span>    | <span data-ttu-id="42763-145">Аргумент текстуры — это коэффициент текстуры, заданный в предыдущем вызове [**сетрендерстате**](/windows/desktop/api) с [**D3DRS \_ текстурефактор**](./d3drenderstatetype.md) Rendering-State.</span><span class="sxs-lookup"><span data-stu-id="42763-145">The texture argument is the texture factor set in a previous call to the [**SetRenderState**](/windows/desktop/api) with the [**D3DRS\_TEXTUREFACTOR**](./d3drenderstatetype.md) render-state value.</span></span> <span data-ttu-id="42763-146">Разрешения доступны только для чтения.</span><span class="sxs-lookup"><span data-stu-id="42763-146">Permissions are read-only.</span></span>                                                                                                                                                                                                                                                       |



 

<span data-ttu-id="42763-147">Флаги модификатора</span><span class="sxs-lookup"><span data-stu-id="42763-147">Modifier flags</span></span>

<span data-ttu-id="42763-148">Флаг аргумента может сочетаться с одним из следующих флагов модификатора.</span><span class="sxs-lookup"><span data-stu-id="42763-148">An argument flag may be combined with one of the following modifier flags.</span></span>



| <span data-ttu-id="42763-149">\#определенно</span><span class="sxs-lookup"><span data-stu-id="42763-149">\#define</span></span>              | <span data-ttu-id="42763-150">Описание</span><span class="sxs-lookup"><span data-stu-id="42763-150">Description</span></span>                                                                                                    |
|-----------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="42763-151">D3DTA \_ алфарепликате</span><span class="sxs-lookup"><span data-stu-id="42763-151">D3DTA\_ALPHAREPLICATE</span></span> | <span data-ttu-id="42763-152">Реплицирует альфа-информацию во все каналы цветов до завершения операции.</span><span class="sxs-lookup"><span data-stu-id="42763-152">Replicate the alpha information to all color channels before the operation completes.</span></span> <span data-ttu-id="42763-153">Это модификатор чтения.</span><span class="sxs-lookup"><span data-stu-id="42763-153">This is a read modifier.</span></span> |
| <span data-ttu-id="42763-154">\_Дополнение D3DTA</span><span class="sxs-lookup"><span data-stu-id="42763-154">D3DTA\_COMPLEMENT</span></span>     | <span data-ttu-id="42763-155">Выполните дополнение аргумента x, (1,0-x).</span><span class="sxs-lookup"><span data-stu-id="42763-155">Take the complement of the argument x, (1.0 - x).</span></span> <span data-ttu-id="42763-156">Это модификатор чтения.</span><span class="sxs-lookup"><span data-stu-id="42763-156">This is a read modifier.</span></span>                                     |



 

## <a name="constant-information"></a><span data-ttu-id="42763-157">Сведения о константе</span><span class="sxs-lookup"><span data-stu-id="42763-157">Constant Information</span></span>



|                          |             |
|--------------------------|-------------|
| <span data-ttu-id="42763-158">Header</span><span class="sxs-lookup"><span data-stu-id="42763-158">Header</span></span>                   | <span data-ttu-id="42763-159">d3d9types. h</span><span class="sxs-lookup"><span data-stu-id="42763-159">d3d9types.h</span></span> |
| <span data-ttu-id="42763-160">Минимальная операционная система</span><span class="sxs-lookup"><span data-stu-id="42763-160">Minimum operating system</span></span> | <span data-ttu-id="42763-161">Windows 98</span><span class="sxs-lookup"><span data-stu-id="42763-161">Windows 98</span></span>  |



 

## <a name="related-topics"></a><span data-ttu-id="42763-162">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="42763-162">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="42763-163">Константы Direct3D</span><span class="sxs-lookup"><span data-stu-id="42763-163">Direct3D Constants</span></span>](dx9-graphics-reference-d3d-constants.md)
</dt> </dl>

 

 
