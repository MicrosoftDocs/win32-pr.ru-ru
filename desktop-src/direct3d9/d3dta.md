---
description: 'Константы аргумента текстуры используются в качестве значений для следующих элементов перечисляемого типа D3DTEXTURESTAGESTATETYPE:'
ms.assetid: 36b2b715-5ced-4246-840e-8ea343521ef4
title: D3DTA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9fe6dd62ce7fc7fe4d438290af1ddb33a75813f0
ms.sourcegitcommit: b40a986d5ded926ae7617119cdd35d99b533bad9
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/24/2021
ms.locfileid: "110343019"
---
# <a name="d3dta"></a><span data-ttu-id="01f0f-103">D3DTA</span><span class="sxs-lookup"><span data-stu-id="01f0f-103">D3DTA</span></span>

<span data-ttu-id="01f0f-104">Константы аргумента текстуры используются в качестве значений для следующих элементов перечисляемого типа [**D3DTEXTURESTAGESTATETYPE**](./d3dtexturestagestatetype.md) :</span><span class="sxs-lookup"><span data-stu-id="01f0f-104">Texture argument constants are used as values for the following members of the [**D3DTEXTURESTAGESTATETYPE**](./d3dtexturestagestatetype.md) enumerated type:</span></span>

-   <span data-ttu-id="01f0f-105">D3DTSS \_ ALPHAARG0</span><span class="sxs-lookup"><span data-stu-id="01f0f-105">D3DTSS\_ALPHAARG0</span></span>
-   <span data-ttu-id="01f0f-106">D3DTSS \_ ALPHAARG1</span><span class="sxs-lookup"><span data-stu-id="01f0f-106">D3DTSS\_ALPHAARG1</span></span>
-   <span data-ttu-id="01f0f-107">D3DTSS \_ ALPHAARG2</span><span class="sxs-lookup"><span data-stu-id="01f0f-107">D3DTSS\_ALPHAARG2</span></span>
-   <span data-ttu-id="01f0f-108">D3DTSS \_ COLORARG0</span><span class="sxs-lookup"><span data-stu-id="01f0f-108">D3DTSS\_COLORARG0</span></span>
-   <span data-ttu-id="01f0f-109">D3DTSS \_ COLORARG1</span><span class="sxs-lookup"><span data-stu-id="01f0f-109">D3DTSS\_COLORARG1</span></span>
-   <span data-ttu-id="01f0f-110">D3DTSS \_ COLORARG2</span><span class="sxs-lookup"><span data-stu-id="01f0f-110">D3DTSS\_COLORARG2</span></span>
-   <span data-ttu-id="01f0f-111">D3DTSS \_ ресултарг</span><span class="sxs-lookup"><span data-stu-id="01f0f-111">D3DTSS\_RESULTARG</span></span>

<span data-ttu-id="01f0f-112">Задайте и извлеките аргументы текстуры, вызвав методы [**сеттекстурестажестате**](/windows/desktop/api) и [**жеттекстурестажестате**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-gettexturestagestate) .</span><span class="sxs-lookup"><span data-stu-id="01f0f-112">Set and retrieve texture arguments by calling the [**SetTextureStageState**](/windows/desktop/api) and [**GetTextureStageState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-gettexturestagestate) methods.</span></span>

<span data-ttu-id="01f0f-113">Флаги аргументов</span><span class="sxs-lookup"><span data-stu-id="01f0f-113">Argument flags</span></span>

<span data-ttu-id="01f0f-114">Флаг аргумента можно объединить с модификатором, но нельзя сочетать два флага аргумента.</span><span class="sxs-lookup"><span data-stu-id="01f0f-114">You can combine an argument flag with a modifier, but two argument flags cannot be combined.</span></span>



| <span data-ttu-id="01f0f-115">\#определенно</span><span class="sxs-lookup"><span data-stu-id="01f0f-115">\#define</span></span>          | <span data-ttu-id="01f0f-116">Описание</span><span class="sxs-lookup"><span data-stu-id="01f0f-116">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
|-------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="01f0f-117">\_Константа D3DTA</span><span class="sxs-lookup"><span data-stu-id="01f0f-117">D3DTA\_CONSTANT</span></span>   | <span data-ttu-id="01f0f-118">Выберите константу на стадии текстуры.</span><span class="sxs-lookup"><span data-stu-id="01f0f-118">Select a constant from a texture stage.</span></span> <span data-ttu-id="01f0f-119">Значение по умолчанию — 0xFFFFFFFF.</span><span class="sxs-lookup"><span data-stu-id="01f0f-119">The default value is 0xffffffff.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| <span data-ttu-id="01f0f-120">D3DTA \_ текущий</span><span class="sxs-lookup"><span data-stu-id="01f0f-120">D3DTA\_CURRENT</span></span>    | <span data-ttu-id="01f0f-121">Аргумент текстуры является результатом предыдущего этапа смешения.</span><span class="sxs-lookup"><span data-stu-id="01f0f-121">The texture argument is the result of the previous blending stage.</span></span> <span data-ttu-id="01f0f-122">На первой стадии текстуры (этап 0) этот аргумент эквивалентен D3DTA \_ диффузии.</span><span class="sxs-lookup"><span data-stu-id="01f0f-122">In the first texture stage (stage 0), this argument is equivalent to D3DTA\_DIFFUSE.</span></span> <span data-ttu-id="01f0f-123">Если предыдущий этап наложения использует текстуру-карту выпуклости (D3DTOP \_ бумпенвмап), система выбирает текстуру из этапа перед текстурой схемы выпуклости.</span><span class="sxs-lookup"><span data-stu-id="01f0f-123">If the previous blending stage uses a bump-map texture (the D3DTOP\_BUMPENVMAP operation), the system chooses the texture from the stage before the bump-map texture.</span></span> <span data-ttu-id="01f0f-124">Если параметр s представляет текущую стадию текстуры, а s-1 содержит текстуру с картой выпуклости, то этот аргумент станет выходным результатом на этапе текстуры s-2.</span><span class="sxs-lookup"><span data-stu-id="01f0f-124">If s represents the current texture stage and s - 1 contains a bump-map texture, this argument becomes the result output by texture stage s - 2.</span></span> <span data-ttu-id="01f0f-125">Разрешения доступны для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="01f0f-125">Permissions are read/write.</span></span> |
| <span data-ttu-id="01f0f-126">D3DTA \_ диффузный</span><span class="sxs-lookup"><span data-stu-id="01f0f-126">D3DTA\_DIFFUSE</span></span>    | <span data-ttu-id="01f0f-127">Аргумент текстуры — это рассеянный цвет, интерполируются от компонентов вершины во время заливки по методу Гуро.</span><span class="sxs-lookup"><span data-stu-id="01f0f-127">The texture argument is the diffuse color interpolated from vertex components during Gouraud shading.</span></span> <span data-ttu-id="01f0f-128">Если вершина не содержит рассеянного цвета, по умолчанию используется цвет 0xFFFFFFFF.</span><span class="sxs-lookup"><span data-stu-id="01f0f-128">If the vertex does not contain a diffuse color, the default color is 0xffffffff.</span></span> <span data-ttu-id="01f0f-129">Разрешения доступны только для чтения.</span><span class="sxs-lookup"><span data-stu-id="01f0f-129">Permissions are read-only.</span></span>                                                                                                                                                                                                                                                                                          |
| <span data-ttu-id="01f0f-130">D3DTA \_ селектмаск</span><span class="sxs-lookup"><span data-stu-id="01f0f-130">D3DTA\_SELECTMASK</span></span> | <span data-ttu-id="01f0f-131">Значение маски для всех аргументов; не используется при задании аргументов текстуры.</span><span class="sxs-lookup"><span data-stu-id="01f0f-131">Mask value for all arguments; not used when setting texture arguments.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| <span data-ttu-id="01f0f-132">\_Зеркальное отражение D3DTA</span><span class="sxs-lookup"><span data-stu-id="01f0f-132">D3DTA\_SPECULAR</span></span>   | <span data-ttu-id="01f0f-133">Аргумент текстуры — это отраженный цвет, интерполируются от компонентов вершины во время заливки по методу Гуро.</span><span class="sxs-lookup"><span data-stu-id="01f0f-133">The texture argument is the specular color interpolated from vertex components during Gouraud shading.</span></span> <span data-ttu-id="01f0f-134">Если вершина не содержит отраженного цвета, по умолчанию используется цвет 0xFFFFFFFF.</span><span class="sxs-lookup"><span data-stu-id="01f0f-134">If the vertex does not contain a specular color, the default color is 0xffffffff.</span></span> <span data-ttu-id="01f0f-135">Разрешения доступны только для чтения.</span><span class="sxs-lookup"><span data-stu-id="01f0f-135">Permissions are read-only.</span></span>                                                                                                                                                                                                                                                                                        |
| <span data-ttu-id="01f0f-136">D3DTA \_ TEMP</span><span class="sxs-lookup"><span data-stu-id="01f0f-136">D3DTA\_TEMP</span></span>       | <span data-ttu-id="01f0f-137">Аргумент текстуры — это временный цвет регистров для чтения или записи.</span><span class="sxs-lookup"><span data-stu-id="01f0f-137">The texture argument is a temporary register color for read or write.</span></span> <span data-ttu-id="01f0f-138">D3DTA \_ TEMP поддерживается, если имеется возможность устройства [D3DPMISCCAPS \_ тссаргтемп](d3dpmisccaps.md) .</span><span class="sxs-lookup"><span data-stu-id="01f0f-138">D3DTA\_TEMP is supported if the [D3DPMISCCAPS\_TSSARGTEMP](d3dpmisccaps.md) device capability is present.</span></span> <span data-ttu-id="01f0f-139">По умолчанию регистр имеет значение (0,0, 0,0, 0,0, 0,0).</span><span class="sxs-lookup"><span data-stu-id="01f0f-139">The default value for the register is (0.0, 0.0, 0.0, 0.0).</span></span> <span data-ttu-id="01f0f-140">Разрешения доступны для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="01f0f-140">Permissions are read/write.</span></span>                                                                                                                                                                                                                                   |
| <span data-ttu-id="01f0f-141">\_Текстура D3DTA</span><span class="sxs-lookup"><span data-stu-id="01f0f-141">D3DTA\_TEXTURE</span></span>    | <span data-ttu-id="01f0f-142">Аргумент текстуры — это цвет текстуры для этой стадии текстуры.</span><span class="sxs-lookup"><span data-stu-id="01f0f-142">The texture argument is the texture color for this texture stage.</span></span> <span data-ttu-id="01f0f-143">Разрешения доступны только для чтения.</span><span class="sxs-lookup"><span data-stu-id="01f0f-143">Permissions are read-only.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                               |
| <span data-ttu-id="01f0f-144">D3DTA \_ тфактор</span><span class="sxs-lookup"><span data-stu-id="01f0f-144">D3DTA\_TFACTOR</span></span>    | <span data-ttu-id="01f0f-145">Аргумент текстуры — это коэффициент текстуры, заданный в предыдущем вызове [**сетрендерстате**](/windows/desktop/api) с [**D3DRS \_ текстурефактор**](./d3drenderstatetype.md) Rendering-State.</span><span class="sxs-lookup"><span data-stu-id="01f0f-145">The texture argument is the texture factor set in a previous call to the [**SetRenderState**](/windows/desktop/api) with the [**D3DRS\_TEXTUREFACTOR**](./d3drenderstatetype.md) render-state value.</span></span> <span data-ttu-id="01f0f-146">Разрешения доступны только для чтения.</span><span class="sxs-lookup"><span data-stu-id="01f0f-146">Permissions are read-only.</span></span>                                                                                                                                                                                                                                                       |



 

<span data-ttu-id="01f0f-147">Флаги модификатора</span><span class="sxs-lookup"><span data-stu-id="01f0f-147">Modifier flags</span></span>

<span data-ttu-id="01f0f-148">Флаг аргумента может сочетаться с одним из следующих флагов модификатора.</span><span class="sxs-lookup"><span data-stu-id="01f0f-148">An argument flag may be combined with one of the following modifier flags.</span></span>



| <span data-ttu-id="01f0f-149">\#определенно</span><span class="sxs-lookup"><span data-stu-id="01f0f-149">\#define</span></span>              | <span data-ttu-id="01f0f-150">Описание</span><span class="sxs-lookup"><span data-stu-id="01f0f-150">Description</span></span>                                                                                                    |
|-----------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="01f0f-151">D3DTA \_ алфарепликате</span><span class="sxs-lookup"><span data-stu-id="01f0f-151">D3DTA\_ALPHAREPLICATE</span></span> | <span data-ttu-id="01f0f-152">Реплицирует альфа-информацию во все каналы цветов до завершения операции.</span><span class="sxs-lookup"><span data-stu-id="01f0f-152">Replicate the alpha information to all color channels before the operation completes.</span></span> <span data-ttu-id="01f0f-153">Это модификатор чтения.</span><span class="sxs-lookup"><span data-stu-id="01f0f-153">This is a read modifier.</span></span> |
| <span data-ttu-id="01f0f-154">\_Дополнение D3DTA</span><span class="sxs-lookup"><span data-stu-id="01f0f-154">D3DTA\_COMPLEMENT</span></span>     | <span data-ttu-id="01f0f-155">Выполните дополнение аргумента x, (1,0-x).</span><span class="sxs-lookup"><span data-stu-id="01f0f-155">Take the complement of the argument x, (1.0 - x).</span></span> <span data-ttu-id="01f0f-156">Это модификатор чтения.</span><span class="sxs-lookup"><span data-stu-id="01f0f-156">This is a read modifier.</span></span>                                     |



 

## <a name="constant-information"></a><span data-ttu-id="01f0f-157">Сведения о константе</span><span class="sxs-lookup"><span data-stu-id="01f0f-157">Constant Information</span></span>



|   <span data-ttu-id="01f0f-158">Требование</span><span class="sxs-lookup"><span data-stu-id="01f0f-158">Requirement</span></span>                       |  <span data-ttu-id="01f0f-159">Значение</span><span class="sxs-lookup"><span data-stu-id="01f0f-159">Value</span></span>           |
|--------------------------|-------------|
| <span data-ttu-id="01f0f-160">Заголовок</span><span class="sxs-lookup"><span data-stu-id="01f0f-160">Header</span></span>                   | <span data-ttu-id="01f0f-161">d3d9types. h</span><span class="sxs-lookup"><span data-stu-id="01f0f-161">d3d9types.h</span></span> |
| <span data-ttu-id="01f0f-162">Минимальная операционная система</span><span class="sxs-lookup"><span data-stu-id="01f0f-162">Minimum operating system</span></span> | <span data-ttu-id="01f0f-163">Windows 98</span><span class="sxs-lookup"><span data-stu-id="01f0f-163">Windows 98</span></span>  |



 

## <a name="related-topics"></a><span data-ttu-id="01f0f-164">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="01f0f-164">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="01f0f-165">Константы Direct3D</span><span class="sxs-lookup"><span data-stu-id="01f0f-165">Direct3D Constants</span></span>](dx9-graphics-reference-d3d-constants.md)
</dt> </dl>

 

 
