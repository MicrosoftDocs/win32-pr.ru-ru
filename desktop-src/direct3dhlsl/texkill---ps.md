---
title: текскилл-PS
description: Отменяет отрисовку текущего пикселя, если любой из первых трех компонентов (УВВ) координат текстуры меньше нуля.
ms.assetid: 7641aef8-8931-4a19-827a-75ab17e901ac
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 4da9c6b59a3c16eeecb8755f2f19542df6ee8a7b
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/20/2019
ms.locfileid: "104335448"
---
# <a name="texkill---ps"></a><span data-ttu-id="53ba1-103">текскилл-PS</span><span class="sxs-lookup"><span data-stu-id="53ba1-103">texkill - ps</span></span>

<span data-ttu-id="53ba1-104">Отменяет отрисовку текущего пикселя, если любой из первых трех компонентов (УВВ) координат текстуры меньше нуля.</span><span class="sxs-lookup"><span data-stu-id="53ba1-104">Cancels rendering of the current pixel if any of the first three components (UVW) of the texture coordinates is less than zero.</span></span>

## <a name="syntax"></a><span data-ttu-id="53ba1-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="53ba1-105">Syntax</span></span>



| <span data-ttu-id="53ba1-106">текскилл DST</span><span class="sxs-lookup"><span data-stu-id="53ba1-106">texkill dst</span></span> |
|-------------|



 

<span data-ttu-id="53ba1-107">где</span><span class="sxs-lookup"><span data-stu-id="53ba1-107">where</span></span>

-   <span data-ttu-id="53ba1-108">DST — это регистр назначения</span><span class="sxs-lookup"><span data-stu-id="53ba1-108">dst is a destination register</span></span>

## <a name="remarks"></a><span data-ttu-id="53ba1-109">Примечания</span><span class="sxs-lookup"><span data-stu-id="53ba1-109">Remarks</span></span>



| <span data-ttu-id="53ba1-110">Версии шейдеров пикселей</span><span class="sxs-lookup"><span data-stu-id="53ba1-110">Pixel shader versions</span></span> | <span data-ttu-id="53ba1-111">1\_1</span><span class="sxs-lookup"><span data-stu-id="53ba1-111">1\_1</span></span> | <span data-ttu-id="53ba1-112">1\_2</span><span class="sxs-lookup"><span data-stu-id="53ba1-112">1\_2</span></span> | <span data-ttu-id="53ba1-113">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="53ba1-113">1\_3</span></span> | <span data-ttu-id="53ba1-114">1\_4</span><span class="sxs-lookup"><span data-stu-id="53ba1-114">1\_4</span></span> | <span data-ttu-id="53ba1-115">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="53ba1-115">2\_0</span></span> | <span data-ttu-id="53ba1-116">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="53ba1-116">2\_x</span></span> | <span data-ttu-id="53ba1-117">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="53ba1-117">2\_sw</span></span> | <span data-ttu-id="53ba1-118">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="53ba1-118">3\_0</span></span> | <span data-ttu-id="53ba1-119">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="53ba1-119">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="53ba1-120">текскилл</span><span class="sxs-lookup"><span data-stu-id="53ba1-120">texkill</span></span>               | <span data-ttu-id="53ba1-121">x</span><span class="sxs-lookup"><span data-stu-id="53ba1-121">x</span></span>    | <span data-ttu-id="53ba1-122">x</span><span class="sxs-lookup"><span data-stu-id="53ba1-122">x</span></span>    | <span data-ttu-id="53ba1-123">x</span><span class="sxs-lookup"><span data-stu-id="53ba1-123">x</span></span>    | <span data-ttu-id="53ba1-124">x</span><span class="sxs-lookup"><span data-stu-id="53ba1-124">x</span></span>    | <span data-ttu-id="53ba1-125">x</span><span class="sxs-lookup"><span data-stu-id="53ba1-125">x</span></span>    | <span data-ttu-id="53ba1-126">x</span><span class="sxs-lookup"><span data-stu-id="53ba1-126">x</span></span>    | <span data-ttu-id="53ba1-127">x</span><span class="sxs-lookup"><span data-stu-id="53ba1-127">x</span></span>     | <span data-ttu-id="53ba1-128">x</span><span class="sxs-lookup"><span data-stu-id="53ba1-128">x</span></span>    | <span data-ttu-id="53ba1-129">x</span><span class="sxs-lookup"><span data-stu-id="53ba1-129">x</span></span>     |



 

<span data-ttu-id="53ba1-130">Эта инструкция соответствует функции [**Clip**](dx-graphics-hlsl-clip.md) HLSL.</span><span class="sxs-lookup"><span data-stu-id="53ba1-130">This instruction corresponds to the HLSL's [**clip**](dx-graphics-hlsl-clip.md) function.</span></span>

<span data-ttu-id="53ba1-131">текскилл не выполняет выборку текстуры.</span><span class="sxs-lookup"><span data-stu-id="53ba1-131">texkill does not sample any texture.</span></span> <span data-ttu-id="53ba1-132">Он работает на первых трех компонентах координат текстуры, заданных номером регистра назначения.</span><span class="sxs-lookup"><span data-stu-id="53ba1-132">It operates on the first three components of the texture coordinates given by the destination register number.</span></span> <span data-ttu-id="53ba1-133">Для PS \_ 1 \_ 4 текскилл работает с данными в первых трех компонентах регистра назначения.</span><span class="sxs-lookup"><span data-stu-id="53ba1-133">For ps\_1\_4, texkill operates on the data in the first three components of the destination register.</span></span>

<span data-ttu-id="53ba1-134">Эту инструкцию можно использовать для реализации произвольных роликовых плоскостей в средстве программной прорисовки.</span><span class="sxs-lookup"><span data-stu-id="53ba1-134">You can use this instruction to implement arbitrary clip planes in the rasterizer.</span></span>

<span data-ttu-id="53ba1-135">При использовании шейдеров вершин приложение отвечает за применение преобразования перспективы.</span><span class="sxs-lookup"><span data-stu-id="53ba1-135">When using vertex shaders, the application is responsible for applying the perspective transform.</span></span> <span data-ttu-id="53ba1-136">Это может вызвать проблемы для произвольных обтравочных плоскостей, так как если она содержит коэффициенты масштабирования анисоморфик, необходимо также преобразовать плоскости Clip.</span><span class="sxs-lookup"><span data-stu-id="53ba1-136">This can cause problems for the arbitrary clipping planes because if it contains anisomorphic scale factors, the clip planes need to be transformed as well.</span></span> <span data-ttu-id="53ba1-137">Поэтому лучше предоставить непроецированную точку на вершину для использования в произвольном Clipper, который является набором координат текстуры, определяемым оператором текскилл.</span><span class="sxs-lookup"><span data-stu-id="53ba1-137">Therefore, it is best to provide an unprojected vertex position to use in the arbitrary clipper, which is the texture coordinate set identified by the texkill operator.</span></span>

<span data-ttu-id="53ba1-138">Эта инструкция используется следующим образом:</span><span class="sxs-lookup"><span data-stu-id="53ba1-138">This instruction is used as follows:</span></span>

<dl> <span data-ttu-id="53ba1-139">текскилл тн</span><span class="sxs-lookup"><span data-stu-id="53ba1-139">texkill tn</span></span>  
<span data-ttu-id="53ba1-140">Маскирование пикселей выполняется следующим образом:</span><span class="sxs-lookup"><span data-stu-id="53ba1-140">// The pixel masking is accomplished as follows:</span></span>  
<span data-ttu-id="53ba1-141">Если (компоненты x, y, z TextureCoordinates (этап n)<sub>уввк</sub>< 0)</span><span class="sxs-lookup"><span data-stu-id="53ba1-141">if ( the x,y,z components of TextureCoordinates(stage n)<sub>UVWQ</sub>< 0 )</span></span>  
<span data-ttu-id="53ba1-142">Отмена отрисовки пикселей</span><span class="sxs-lookup"><span data-stu-id="53ba1-142">cancel pixel render</span></span>
</dl>

<span data-ttu-id="53ba1-143">Для построителя текстуры 1 \_ 1, 1 \_ 2 и 1 \_ 3 текскилл работает с набором координат текстуры, заданным номером регистра назначения.</span><span class="sxs-lookup"><span data-stu-id="53ba1-143">For pixel shader 1\_1, 1\_2, and 1\_3, texkill operates on the texture coordinate set given by the destination register number.</span></span> <span data-ttu-id="53ba1-144">Однако в версии 1 \_ 4 текскилл работает с данными, содержащимися в [регистре координат текстуры](dx9-graphics-reference-asm-ps-registers-texture-coordinate.md) (тн) или во временном регистре (RN), который был указан в качестве назначения.</span><span class="sxs-lookup"><span data-stu-id="53ba1-144">In version 1\_4, however, texkill operates on the data contained in the [Texture Coordinate Register](dx9-graphics-reference-asm-ps-registers-texture-coordinate.md) (tn) or in the temporary register (rn) that has been specified as the destination.</span></span>

<span data-ttu-id="53ba1-145">Если включена многовыборочная выборка, любые эффекты сглаживания, полученные на краях многоугольников из-за множественной выборки, не будут достигаться на границе, созданной текскилл.</span><span class="sxs-lookup"><span data-stu-id="53ba1-145">When multisampling is enabled, any antialiasing effect achieved on polygon edges due to multisampling will not be achieved along any edge that has been generated by texkill.</span></span> <span data-ttu-id="53ba1-146">Шейдер пикселей выполняется один раз на пиксель.</span><span class="sxs-lookup"><span data-stu-id="53ba1-146">The pixel shader runs once per pixel.</span></span>

<span data-ttu-id="53ba1-147">Данный пример служит только для демонстрационных целей.</span><span class="sxs-lookup"><span data-stu-id="53ba1-147">This example is for illustration only.</span></span>

<span data-ttu-id="53ba1-148">Этот пример маскирует Пиксели с отрицательными координатами текстуры.</span><span class="sxs-lookup"><span data-stu-id="53ba1-148">This example masks out pixels that have negative texture coordinates.</span></span> <span data-ttu-id="53ba1-149">Цвета пикселов интерполируются на основе цветов вершин, предоставленных в данных вершин.</span><span class="sxs-lookup"><span data-stu-id="53ba1-149">The pixel colors are interpolated from vertex colors provided in the vertex data.</span></span>


```
ps_1_1       // Version instruction
texkill t0   // Mask out pixel using texture coordinates from stage 0
mov r0, v0   // Move the diffuse color in v0 to r0

// The rendered output from the pixel shader is shown below
```



<span data-ttu-id="53ba1-150">Координаты текстуры находятся в диапазоне от-0,5 до 0,5 в u, а 0,0 – 1,0 в v.</span><span class="sxs-lookup"><span data-stu-id="53ba1-150">The texture coordinates range from -0.5 to 0.5 in u, and 0.0 to 1.0 in v.</span></span> <span data-ttu-id="53ba1-151">Эта инструкция приводит к раскрытию отрицательных значений u. На первой иллюстрации показан цвет вершины, примененный к четырем без примененной инструкции текскилл.</span><span class="sxs-lookup"><span data-stu-id="53ba1-151">This instruction causes the negative u values to get masked out. The first illustration below shows the vertex color applied to the quad without the texkill instruction applied.</span></span> <span data-ttu-id="53ba1-152">На втором рисунке ниже показан результат выполнения инструкции текскилл.</span><span class="sxs-lookup"><span data-stu-id="53ba1-152">The second illustration below shows the result of the texkill instruction.</span></span> <span data-ttu-id="53ba1-153">Цвета пикселей из координат текстуры, приведенные ниже 0 (где x переходит от-0,5 к 0,0), маскируются. Цвет фона (белый) используется, когда цвет пикселя замаскирован.</span><span class="sxs-lookup"><span data-stu-id="53ba1-153">The pixel colors from the texture coordinates below 0 (where x goes from -0.5 to 0.0) are masked out. The background color (white) is used where the pixel color is masked.</span></span>

![Иллюстрация вывода с цветом вершины, примененным к четырем без инструкции текскилл](images/pstexkill-in.jpg)![Иллюстрация выходных данных с примененной инструкцией текскилл](images/pstexkill-out.jpg)

<span data-ttu-id="53ba1-156">Данные координаты текстуры объявляются в объявлении данных вершин в этом примере.</span><span class="sxs-lookup"><span data-stu-id="53ba1-156">The texture coordinate data is declared in the vertex data declaration in this example.</span></span>


```
   
struct CUSTOMVERTEX
{
    FLOAT x, y, z;
    DWORD color;
    FLOAT tu1, tv1;
};

#define D3DFVF_CUSTOMVERTEX (D3DFVF_XYZ|D3DFVF_DIFFUSE|D3DFVF_TEX1|D3DTEXCOORD2(0))

static CUSTOMVERTEX g_Vertices[]=
{
    //  x      y     z    color         u1,    v1  
    { -1.0f, -1.0f, 0.0f, 0xffff0000, -0.5f,  1.0f, },
    {  1.0f, -1.0f, 0.0f, 0xff00ff00,  0.5f,  1.0f, },
    {  1.0f,  1.0f, 0.0f, 0xff0000ff,  0.5f,  0.0f, },
    { -1.0f,  1.0f, 0.0f, 0xffffffff, -0.5f,  0.0f, },

};
```



## <a name="related-topics"></a><span data-ttu-id="53ba1-157">См. также</span><span class="sxs-lookup"><span data-stu-id="53ba1-157">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="53ba1-158">Инструкции шейдера пикселей</span><span class="sxs-lookup"><span data-stu-id="53ba1-158">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




