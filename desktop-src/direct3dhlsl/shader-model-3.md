---
title: Модель шейдера 3 (Справочник по HLSL)
description: Шейдеры вершин и шейдеры пикселей значительно упрощаются благодаря более ранним версиям шейдеров.
ms.assetid: 01ac85cb-b309-4169-acc2-320a929b65cb
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 2d87c791694e91de135052b4172e3bd5f55577d7
ms.sourcegitcommit: adba238660d8a5f4fe98fc6f5d105d56aac3a400
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/09/2021
ms.locfileid: "111827103"
---
# <a name="shader-model-3-hlsl-reference"></a><span data-ttu-id="bce35-103">Модель шейдера 3 (Справочник по HLSL)</span><span class="sxs-lookup"><span data-stu-id="bce35-103">Shader model 3 (HLSL reference)</span></span>

<span data-ttu-id="bce35-104">Шейдеры вершин и шейдеры пикселей значительно упрощаются благодаря более ранним версиям шейдеров.</span><span class="sxs-lookup"><span data-stu-id="bce35-104">Vertex shaders and pixel shaders are simplified considerably from earlier shader versions.</span></span> <span data-ttu-id="bce35-105">Если вы реализуете шейдеры на оборудовании, вы не можете использовать VS \_ 3 \_ 0 или PS \_ 3 \_ 0 с другими версиями шейдеров, и вы не можете использовать любой тип шейдера с фиксированным конвейером функций.</span><span class="sxs-lookup"><span data-stu-id="bce35-105">If you are implementing shaders in hardware, you may not use vs\_3\_0 or ps\_3\_0 with any other shader versions, and you may not use either shader type with the fixed function pipeline.</span></span> <span data-ttu-id="bce35-106">Эти изменения делают возможным упрощение драйверов и среды выполнения.</span><span class="sxs-lookup"><span data-stu-id="bce35-106">These changes make it possible to simplify drivers and the runtime.</span></span> <span data-ttu-id="bce35-107">Единственное исключение заключается в том, что только программные \_ \_ шейдеры VS 3 0 можно использовать с любой версией построителя текстуры.</span><span class="sxs-lookup"><span data-stu-id="bce35-107">The only exception is that software-only vs\_3\_0 shaders may be used with any pixel shader version.</span></span> <span data-ttu-id="bce35-108">Кроме того, если вы используете только программный \_ шейдер VS 3 \_ 0 с предыдущей версией шейдера пикселей, шейдер вершин может использовать только семантику вывода, совместимую с кодами гибких форматов ВЕРШИН (фвф).</span><span class="sxs-lookup"><span data-stu-id="bce35-108">In addition, if you are using a software-only vs\_3\_0 shader with a previous pixel shader version, the vertex shader can only use output semantics that are compatible with flexible vertex format (FVF) codes.</span></span>

<span data-ttu-id="bce35-109">Семантика, используемая в выходных данных шейдера вершин, должна использоваться для входных шейдеров пикселей.</span><span class="sxs-lookup"><span data-stu-id="bce35-109">The semantics used on vertex shader outputs must be used on pixel shader inputs.</span></span> <span data-ttu-id="bce35-110">Семантика используется для сопоставления выходных данных шейдера вершин с входными шейдерами пикселей, аналогично тому, как объявление вершины сопоставляется с входными регистрами вершинного шейдера и предыдущими моделями шейдеров.</span><span class="sxs-lookup"><span data-stu-id="bce35-110">The semantics are used to map the vertex shader outputs to the pixel shader inputs, similar to the way the vertex declaration is mapped to the vertex shader input registers and previous shader models.</span></span> <span data-ttu-id="bce35-111">См. раздел семантика соответствия для шейдеров VS 3,0 и PS 3,0.</span><span class="sxs-lookup"><span data-stu-id="bce35-111">See Match Semantics on vs 3.0 and ps 3.0 Shaders.</span></span>

<span data-ttu-id="bce35-112">Добавлены новые режимы рендеринга, которые охватывают возможность дополнительных координат текстуры в этой новой схеме.</span><span class="sxs-lookup"><span data-stu-id="bce35-112">Additional wrap mode render states have been added to cover the possibility of additional texture coordinates in this new scheme.</span></span> <span data-ttu-id="bce35-113">Атрибуты с D3DDECLUSAGE \_ текскурд и индексом использования от 0 до 15 интерполируются в режиме переноса при установке соответствующего [**D3DRS \_ Wrap \***](/windows/desktop/direct3d9/d3drenderstatetype) .</span><span class="sxs-lookup"><span data-stu-id="bce35-113">Attributes with D3DDECLUSAGE\_TEXCOORD and usage index from 0 to 15 are interpolated in wrap mode when the corresponding [**D3DRS\_WRAP\***](/windows/desktop/direct3d9/d3drenderstatetype) is set.</span></span>

-   [<span data-ttu-id="bce35-114">Компоненты модели шейдера вершин 3</span><span class="sxs-lookup"><span data-stu-id="bce35-114">Vertex Shader Model 3 Features</span></span>](#vertex-shader-model-3-features)
-   [<span data-ttu-id="bce35-115">Компоненты модели шейдера пикселей 3</span><span class="sxs-lookup"><span data-stu-id="bce35-115">Pixel Shader Model 3 Features</span></span>](#pixel-shader-model-3-features)
-   [<span data-ttu-id="bce35-116">Семантика соответствия для \_ \_ шейдеров VS 3 0 и PS \_ 3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="bce35-116">Match Semantics on vs\_3\_0 and ps\_3\_0 Shaders</span></span>](/windows)
-   [<span data-ttu-id="bce35-117">Изменения в режиме тумана, глубины и затенения</span><span class="sxs-lookup"><span data-stu-id="bce35-117">Fog, Depth, and Shading Mode Changes</span></span>](#fog-depth-and-shading-mode-changes)
-   [<span data-ttu-id="bce35-118">Преобразования с плавающей запятой и целых чисел</span><span class="sxs-lookup"><span data-stu-id="bce35-118">Floating Point and Integer Conversions</span></span>](#floating-point-and-integer-conversions)
-   [<span data-ttu-id="bce35-119">Указание полной или частичной точности</span><span class="sxs-lookup"><span data-stu-id="bce35-119">Specifying Full or Partial Precision</span></span>](#specifying-full-or-partial-precision)
-   [<span data-ttu-id="bce35-120">Программная вершина и шейдеры пикселей</span><span class="sxs-lookup"><span data-stu-id="bce35-120">Software Vertex and Pixel Shaders</span></span>](#software-vertex-and-pixel-shaders)

## <a name="vertex-shader-model-3-features"></a><span data-ttu-id="bce35-121">Компоненты модели шейдера вершин 3</span><span class="sxs-lookup"><span data-stu-id="bce35-121">Vertex Shader Model 3 Features</span></span>

<span data-ttu-id="bce35-122">Типы регистрации выходных шейдеров вершин свернуты в двенадцать регистров (см. раздел [выходные регистры](dx9-graphics-reference-asm-vs-registers-output.md)).</span><span class="sxs-lookup"><span data-stu-id="bce35-122">The vertex shader output register types have been collapsed into twelve registers (see [Output Registers](dx9-graphics-reference-asm-vs-registers-output.md)).</span></span> <span data-ttu-id="bce35-123">Все используемые регистры должны быть объявлены с помощью инструкции [дкл](dcl-usage---ps.md) и семантики (например, дкл \_ color0 O0. ксизв).</span><span class="sxs-lookup"><span data-stu-id="bce35-123">Each register that is used needs to be declared using the [dcl](dcl-usage---ps.md) instruction and a semantic (for example, dcl\_color0 o0.xyzw).</span></span>

<span data-ttu-id="bce35-124">3 \_ 0. модель шейдера вершин (VS \_ 3 0 \_ ) расширяет возможности VS \_ 2 \_ 0 с более мощным индексированием регистров, набором упрощенных выходных регистров, возможностью выборки текстуры в шейдере вершин и возможность управлять скоростью, с которой инициализируются входные шейдеры.</span><span class="sxs-lookup"><span data-stu-id="bce35-124">The 3\_0 vertex shader model (vs\_3\_0) expands on the features of vs\_2\_0 with more powerful register indexing, a set of simplified output registers, the ability to sample a texture in a vertex shader, and the ability to control the rate at which shader inputs are initialized.</span></span>

### <a name="index-any-register"></a><span data-ttu-id="bce35-125">Индекс любого регистра</span><span class="sxs-lookup"><span data-stu-id="bce35-125">Index Any Register</span></span>

<span data-ttu-id="bce35-126">Все регистры ( [входные](dx9-graphics-reference-asm-vs-registers-input.md) и [выходные регистры](dx9-graphics-reference-asm-vs-registers-output.md)) можно индексировать с помощью [регистра счетчика циклов](dx9-graphics-reference-asm-vs-registers-loop-counter.md) (в более ранних версиях могут индексироваться только постоянные регистры).</span><span class="sxs-lookup"><span data-stu-id="bce35-126">All registers( [Input Register](dx9-graphics-reference-asm-vs-registers-input.md) and [Output Registers](dx9-graphics-reference-asm-vs-registers-output.md)) can be indexed using [Loop Counter Register](dx9-graphics-reference-asm-vs-registers-loop-counter.md) (only constant registers could be indexed in earlier versions.)</span></span>

<span data-ttu-id="bce35-127">Перед индексированием необходимо объявить входные и выходные регистры.</span><span class="sxs-lookup"><span data-stu-id="bce35-127">You must declare input and output registers before indexing them.</span></span> <span data-ttu-id="bce35-128">Однако вы не можете индексировать выходные регистры, которые были объявлены с семантикой позиции или размера точки.</span><span class="sxs-lookup"><span data-stu-id="bce35-128">However, you may not index any output register that has been declared with a position or point size semantic.</span></span> <span data-ttu-id="bce35-129">Фактически, если используется индексирование, то семантика позиционирования и псизе должны быть объявлены в регистрах O0 и O1 соответственно.</span><span class="sxs-lookup"><span data-stu-id="bce35-129">In fact, if indexing is used the position and psize semantics have to be declared in the o0 and o1 registers respectively.</span></span>

<span data-ttu-id="bce35-130">Вы можете индексировать только непрерывный диапазон регистров. Это значит, что нельзя индексировать по регистрам, которые не были объявлены.</span><span class="sxs-lookup"><span data-stu-id="bce35-130">You are only allowed to index a continuous range of registers; that is, you cannot index across registers that have not been declared.</span></span> <span data-ttu-id="bce35-131">Хотя это ограничение может оказаться неудобным, оно позволяет выполнять аппаратную оптимизацию.</span><span class="sxs-lookup"><span data-stu-id="bce35-131">While this restriction may be inconvenient, it permits hardware optimization to take place.</span></span> <span data-ttu-id="bce35-132">Попытка индексирования по несмежным регистрам приведет к неопределенному результату.</span><span class="sxs-lookup"><span data-stu-id="bce35-132">Attempting to index across non-contiguous registers will produce undefined results.</span></span> <span data-ttu-id="bce35-133">Проверка шейдера не применяет это ограничение.</span><span class="sxs-lookup"><span data-stu-id="bce35-133">Shader validation does not enforce this restriction.</span></span>

### <a name="simplify-output-registers"></a><span data-ttu-id="bce35-134">Упрощение выходных регистров</span><span class="sxs-lookup"><span data-stu-id="bce35-134">Simplify Output Registers</span></span>

<span data-ttu-id="bce35-135">Все различные типы выходных регистров свернуты в двенадцать выходных регистров: 1 для позиции, 2 для цвета, 8 для текстуры и 1 для тумана или кегля.</span><span class="sxs-lookup"><span data-stu-id="bce35-135">All the various types of output registers have been collapsed into twelve output registers: 1 for position, 2 for color, 8 for texture, and 1 for fog or point size.</span></span> <span data-ttu-id="bce35-136">Эти регистры будут интерполируются все данные, которые они содержат, для шейдера пикселей.</span><span class="sxs-lookup"><span data-stu-id="bce35-136">These registers will interpolate any data they contain for the pixel shader.</span></span> <span data-ttu-id="bce35-137">Объявления регистров выходных данных являются обязательными, и семантика назначается каждой ККМ.</span><span class="sxs-lookup"><span data-stu-id="bce35-137">Output register declarations are required and semantics are assigned to each register.</span></span>

<span data-ttu-id="bce35-138">Регистры можно разделить следующим образом:</span><span class="sxs-lookup"><span data-stu-id="bce35-138">The registers can be broken down as follows:</span></span>

-   <span data-ttu-id="bce35-139">По крайней мере один регистр должен быть объявлен как регистр позиции с четырьмя компонентами.</span><span class="sxs-lookup"><span data-stu-id="bce35-139">At least one register must be declared as a four-component position register.</span></span> <span data-ttu-id="bce35-140">Это единственный обязательный регистр шейдера вершин.</span><span class="sxs-lookup"><span data-stu-id="bce35-140">This is the only vertex shader register that is required.</span></span>
-   <span data-ttu-id="bce35-141">Первые десять регистров, потребляемых шейдером, могут использовать не более четырех компонентов (ксизв).</span><span class="sxs-lookup"><span data-stu-id="bce35-141">The first ten registers consumed by a shader may use up to four components (xyzw) maximum.</span></span>
-   <span data-ttu-id="bce35-142">Последний (или двенадцатый) регистр может содержать только скаляр (например, размер точки).</span><span class="sxs-lookup"><span data-stu-id="bce35-142">The last (or twelfth) register may only contain a scalar (such as point size).</span></span>

<span data-ttu-id="bce35-143">Список регистров см. в разделе [регистры-VS \_ 3 \_ 0](dx9-graphics-reference-asm-vs-registers-vs-3-0.md).</span><span class="sxs-lookup"><span data-stu-id="bce35-143">For a listing of the registers, see [Registers - vs\_3\_0](dx9-graphics-reference-asm-vs-registers-vs-3-0.md).</span></span>

### <a name="texture-sample-in-a-vertex-shader"></a><span data-ttu-id="bce35-144">Пример текстуры в шейдере вершин</span><span class="sxs-lookup"><span data-stu-id="bce35-144">Texture Sample in a Vertex Shader</span></span>

<span data-ttu-id="bce35-145">Вершинный шейдер 3 \_ 0 поддерживает поиск текстур в шейдере вершин с помощью [текслдл-VS](texldl---vs.md).</span><span class="sxs-lookup"><span data-stu-id="bce35-145">Vertex shader 3\_0 supports texture lookup in the vertex shader using [texldl - vs](texldl---vs.md).</span></span>

## <a name="pixel-shader-model-3-features"></a><span data-ttu-id="bce35-146">Компоненты модели шейдера пикселей 3</span><span class="sxs-lookup"><span data-stu-id="bce35-146">Pixel Shader Model 3 Features</span></span>

<span data-ttu-id="bce35-147">В десять входных регистров был свернут цвет шейдера пикселей и регистры текстур (см. раздел [типы входных регистров](dx9-graphics-reference-asm-ps-registers-ps-3-0.md)).</span><span class="sxs-lookup"><span data-stu-id="bce35-147">The pixel shader color and texture registers have been collapsed into ten input registers (see [Input Register Types](dx9-graphics-reference-asm-ps-registers-ps-3-0.md)).</span></span> <span data-ttu-id="bce35-148">Регистрация лица является скалярной регистром с плавающей запятой.</span><span class="sxs-lookup"><span data-stu-id="bce35-148">The Face Register is a floating point scalar register.</span></span> <span data-ttu-id="bce35-149">Допустим только знак этого регистра.</span><span class="sxs-lookup"><span data-stu-id="bce35-149">Only the sign of this register is valid.</span></span> <span data-ttu-id="bce35-150">Если знак является отрицательным, примитив является обратным лицом.</span><span class="sxs-lookup"><span data-stu-id="bce35-150">If the sign is negative the primitive is a back face.</span></span> <span data-ttu-id="bce35-151">Это можно использовать внутри шейдера пикселей для достижения двустороннего освещения, например.</span><span class="sxs-lookup"><span data-stu-id="bce35-151">This can be used inside a pixel shader to achieve two-sided lighting, for instance.</span></span> <span data-ttu-id="bce35-152">Регистр позиций ссылается на текущие (x, y) Пиксели.</span><span class="sxs-lookup"><span data-stu-id="bce35-152">The Position Register references the current (x,y) pixels.</span></span>

<span data-ttu-id="bce35-153">Регистры констант шейдера можно задать с помощью:</span><span class="sxs-lookup"><span data-stu-id="bce35-153">The shader constant registers can be set using:</span></span>

-   [<span data-ttu-id="bce35-154">**сетпикселшадерконстантб**</span><span class="sxs-lookup"><span data-stu-id="bce35-154">**SetPixelShaderConstantB**</span></span>](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setpixelshaderconstantb)
-   [<span data-ttu-id="bce35-155">**сетпикселшадерконстанти**</span><span class="sxs-lookup"><span data-stu-id="bce35-155">**SetPixelShaderConstantI**</span></span>](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setpixelshaderconstanti)
-   [<span data-ttu-id="bce35-156">**сетпикселшадерконстантф**</span><span class="sxs-lookup"><span data-stu-id="bce35-156">**SetPixelShaderConstantF**</span></span>](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setpixelshaderconstantf)

## <a name="match-semantics-on-vs_3_0-and-ps_3_0-shaders"></a><span data-ttu-id="bce35-157">Семантика соответствия для \_ \_ шейдеров VS 3 0 и PS \_ 3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="bce35-157">Match Semantics on vs\_3\_0 and ps\_3\_0 Shaders</span></span>

<span data-ttu-id="bce35-158">Существуют некоторые ограничения на семантическое использование с VS \_ 3 \_ 0 и PS \_ 3 \_ 0.</span><span class="sxs-lookup"><span data-stu-id="bce35-158">There are some restrictions on semantic usage with vs\_3\_0 and ps\_3\_0.</span></span> <span data-ttu-id="bce35-159">В общем случае необходимо соблюдать осторожность при использовании семантики для входных шейдеров, которые соответствуют семантике, используемой в выходных данных шейдера.</span><span class="sxs-lookup"><span data-stu-id="bce35-159">In general, you need to be careful when using a semantic for a shader input that matches a semantic used on a shader output.</span></span>

<span data-ttu-id="bce35-160">Например, шейдер пикселей упаковывает несколько имен в один регистр:</span><span class="sxs-lookup"><span data-stu-id="bce35-160">For instance, this pixel shader packs multiple names into one register:</span></span>


```
ps_3_0 
dcl_texcoord0 v0.x 
dcl_texcoord1 v0.yz // Valid to pack multiple names into one register 
dcl_texcoord2_centroid v1.w
...
```



<span data-ttu-id="bce35-161">Каждый регистр имеет разную семантику.</span><span class="sxs-lookup"><span data-stu-id="bce35-161">Each register has a different semantic.</span></span> <span data-ttu-id="bce35-162">Обратите внимание, что можно также указать имя v0. x и v0. из с разной семантикой (несколько) из-за использования маски записи.</span><span class="sxs-lookup"><span data-stu-id="bce35-162">Notice that you can also name v0.x and v0.yz with different (multiple) semantics because of the use of the write mask.</span></span>

<span data-ttu-id="bce35-163">При наличии шейдера пикселей следующий \_ шейдер VS 3 \_ 0 не может быть связан с ним:</span><span class="sxs-lookup"><span data-stu-id="bce35-163">Given the pixel shader, the following vs\_3\_0 shader cannot be paired with it:</span></span>


```
vs_3_0 
... 
dcl_texcoord0 o5.x 
dcl_texcoord1 o6.yzw 
...
```



<span data-ttu-id="bce35-164">Эти два шейдера конфликтуют с использованием семантики [**D3DDECLUSAGE \_ TEXCOORD0**](/windows/desktop/direct3d9/d3ddeclusage) и **D3DDECLUSAGE \_ TEXCOORD1** .</span><span class="sxs-lookup"><span data-stu-id="bce35-164">These two shaders conflict with their use of the [**D3DDECLUSAGE\_TEXCOORD0**](/windows/desktop/direct3d9/d3ddeclusage) And **D3DDECLUSAGE\_TEXCOORD1** semantics.</span></span>

<span data-ttu-id="bce35-165">Перепишите шейдер вершин следующим образом, чтобы избежать семантического конфликта.</span><span class="sxs-lookup"><span data-stu-id="bce35-165">Rewrite the vertex shader like this to avoid the semantic collision:</span></span>


```
vs_3_0 
... 
dcl_texcoord2 o3 
dcl_texcoord3 o9 
...
```



<span data-ttu-id="bce35-166">Аналогично, семантическое имя, объявленное в разных входных регистрах в шейдере пикселей (v0 и v1 в построителе пикселей), не может использоваться в одном выходном регистре в этом шейдере вершин.</span><span class="sxs-lookup"><span data-stu-id="bce35-166">Similarly, a semantic name declared on different input registers in the pixel shader (v0 and v1 in the pixel shader) cannot be used in a single output register in this vertex shader.</span></span> <span data-ttu-id="bce35-167">Например, этот шейдер вершин не может быть сопряжен с шейдером Pixel Shader, так как D3DDECLUSAGE \_ TEXCOORD1 используется для входных регистров шейдера пикселей (v0, v1) и в выходной регистр шейдера вершин — O3.</span><span class="sxs-lookup"><span data-stu-id="bce35-167">For instance, this vertex shader cannot be paired with the pixel shader because D3DDECLUSAGE\_TEXCOORD1 is used for both pixel shader input registers (v0, v1) and the vertex shader output register o3.</span></span>


```
vs_3_0 
... 
dcl_texcoord0 o3.x 
dcl_texcoord1 o3.yz 

dcl_texcoord2 o3.w // BAD! Would be valid if this were not o3 
dcl_texcoord3 o9 ... 
```



<span data-ttu-id="bce35-168">С другой стороны, шейдер вершин не может быть сопряжен с шейдером пикселей, так как выходная маска для параметра с заданной семантикой не предоставляет данные, запрашиваемые шейдером пикселей:</span><span class="sxs-lookup"><span data-stu-id="bce35-168">On the other hand, this vertex shader cannot be paired with the pixel shader because the output mask for a parameter with a given semantic does not provide the data that is requested by the pixel shader:</span></span>


```
vs_3_0 
... 
dcl_texcoord0 o5.x 
dcl_texcoord1 o5.yzw 
dcl_texcoord2 o7.yz // BAD! Would be valid if w were included 
dcl_texcoord3 o9 
... 
```



<span data-ttu-id="bce35-169">Этот шейдер вершин не предоставляет выходные данные с одним из семантических имен, запрошенных шейдером пикселей, поэтому связывание шейдера является недопустимым:</span><span class="sxs-lookup"><span data-stu-id="bce35-169">This vertex shader does not provide an output with one of the semantic names requested by the pixel shader, so the shader pairing is invalid:</span></span>


```
vs_3_0 
... 
dcl_texcoord0 o5.x 
dcl_texcoord1 o5.yzw 
dcl_texcoord3 o9 
// The pixel shader wants texcoord2, with a w component, 
// but it isn't output by this vertex shader at all! 
... 
```



## <a name="fog-depth-and-shading-mode-changes"></a><span data-ttu-id="bce35-170">Изменения в режиме тумана, глубины и затенения</span><span class="sxs-lookup"><span data-stu-id="bce35-170">Fog, Depth, and Shading Mode Changes</span></span>

<span data-ttu-id="bce35-171">Если D3DRS \_ шадемоде задан для плоской заливки во время обрезки и растрирования треугольника, то атрибуты с D3DDECLUSAGE \_ цветом интерполируются как плоские оттенки.</span><span class="sxs-lookup"><span data-stu-id="bce35-171">When D3DRS\_SHADEMODE is set for flat shading during clipping and triangle rasterization, attributes with D3DDECLUSAGE\_COLOR are interpolated as flat shaded.</span></span> <span data-ttu-id="bce35-172">Если какие-либо компоненты регистра объявляются с помощью семантики цвета, но другие компоненты одного регистра имеют разную семантику, то интерполяция плоской заливки (линейная и плоская) будет неопределена для компонентов в этой регистровой семантике без семантической настройки цвета.</span><span class="sxs-lookup"><span data-stu-id="bce35-172">If any components of a register are declared with a color semantic but other components of the same register are given different semantics, flat shading interpolation (linear vs. flat) will be undefined on the components in that register without a color semantic.</span></span>

<span data-ttu-id="bce35-173">Если требуется отрисовка тумана, \_ \_ шейдеры VS 3 0 и PS \_ 3 \_ 0 должны реализовывать туман.</span><span class="sxs-lookup"><span data-stu-id="bce35-173">If fog rendering is desired, vs\_3\_0 and ps\_3\_0 shaders must implement fog.</span></span> <span data-ttu-id="bce35-174">Вычисления тумана не выполняются за пределами шейдеров.</span><span class="sxs-lookup"><span data-stu-id="bce35-174">No fog calculations are done outside of the shaders.</span></span> <span data-ttu-id="bce35-175">В VS 3 0 нет регистра тумана \_ \_ , а также добавлена дополнительная семантика D3DDECLUSAGE \_ тумана (для коэффициента смешения тумана на вершину) и \_ глубина D3DDECLUSAGE (для передачи значения глубины в шейдер пикселей для расчета коэффициента смешения тумана).</span><span class="sxs-lookup"><span data-stu-id="bce35-175">There is no fog register in vs\_3\_0, and additional semantics D3DDECLUSAGE\_FOG (for fog blend factor computed per vertex) and D3DDECLUSAGE\_DEPTH (for passing in a depth value to the pixel shader to compute the fog blend factor) have been added.</span></span>

<span data-ttu-id="bce35-176">Состояние этапа текстуры D3DTSS \_ текскурдиндекс игнорируется при использовании шейдера Pixel shader 3,0.</span><span class="sxs-lookup"><span data-stu-id="bce35-176">Texture stage state D3DTSS\_TEXCOORDINDEX is ignored when using pixel shader 3.0.</span></span>

<span data-ttu-id="bce35-177">Для поддержки этих изменений были добавлены следующие значения:</span><span class="sxs-lookup"><span data-stu-id="bce35-177">The following values have been added to accommodate these changes:</span></span>


```
// Fog and Depth usages
D3DDECLUSAGE_FOG 
D3DDECLUSAGE_DEPTH 

// Additional wrap states for vs_3_0 attributes with D3DDECLUSAGE_TEXCOORD 
D3DRS_WRAP8 
D3DRS_WRAP9 
D3DRS_WRAP10 
D3DRS_WRAP11 
D3DRS_WRAP12 
D3DRS_WRAP13 
D3DRS_WRAP14 
D3DRS_WRAP15
```



## <a name="floating-point-and-integer-conversions"></a><span data-ttu-id="bce35-178">Преобразования с плавающей запятой и целых чисел</span><span class="sxs-lookup"><span data-stu-id="bce35-178">Floating Point and Integer Conversions</span></span>

<span data-ttu-id="bce35-179">Математические операции с плавающей запятой выполняются с разной точностью и диапазонами (16-разрядные, 24-разрядные и 32-разрядные) в разных частях конвейера.</span><span class="sxs-lookup"><span data-stu-id="bce35-179">Floating point math happens at different precision and ranges (16-bit, 24-bit, and 32-bit) in different parts of the pipeline.</span></span> <span data-ttu-id="bce35-180">Значение, превышающее динамический диапазон конвейера, который входит в состав этого конвейера (например, с 32-разрядной текстурой с плавающей запятой, в 24-битный конвейер с плавающей запятой в PS \_ 2 \_ 0) создает неопределенный результат.</span><span class="sxs-lookup"><span data-stu-id="bce35-180">A value greater than the dynamic range of the pipeline that enters that pipeline (for example, a 32-bit float texture map is sampled into a 24-bit float pipeline in ps\_2\_0) creates an undefined result.</span></span> <span data-ttu-id="bce35-181">Для прогнозируемого поведения необходимо отвести к такому значению максимальное значение динамического диапазона.</span><span class="sxs-lookup"><span data-stu-id="bce35-181">For predictable behavior, you should clamp such a value to the dynamic range maximum.</span></span>

<span data-ttu-id="bce35-182">Преобразование значения с плавающей запятой в целое число происходит в нескольких местах, таких как:</span><span class="sxs-lookup"><span data-stu-id="bce35-182">Conversion from a floating point value to an integer happens in several places such as:</span></span>

-   <span data-ttu-id="bce35-183">При обнаружении инструкции [МОВА-VS](mova---vs.md) .</span><span class="sxs-lookup"><span data-stu-id="bce35-183">When encountering a [mova - vs](mova---vs.md) instruction.</span></span>
-   <span data-ttu-id="bce35-184">Во время адресации текстур.</span><span class="sxs-lookup"><span data-stu-id="bce35-184">During texture addressing.</span></span>
-   <span data-ttu-id="bce35-185">При записи в целевой объект рендеринга, не являющийся плавающей точкой.</span><span class="sxs-lookup"><span data-stu-id="bce35-185">When writing out to a non-floating point render target.</span></span>

## <a name="specifying-full-or-partial-precision"></a><span data-ttu-id="bce35-186">Указание полной или частичной точности</span><span class="sxs-lookup"><span data-stu-id="bce35-186">Specifying Full or Partial Precision</span></span>

<span data-ttu-id="bce35-187">PS \_ 3 \_ 0 и PS \_ 2 \_ имеют поддержку двух уровней точности:</span><span class="sxs-lookup"><span data-stu-id="bce35-187">Both ps\_3\_0 and ps\_2\_x provide support for two levels of precision:</span></span>



| <span data-ttu-id="bce35-188">PS \_ 3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="bce35-188">ps\_3\_0</span></span> | <span data-ttu-id="bce35-189">PS \_ 2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="bce35-189">ps\_2\_0</span></span> | <span data-ttu-id="bce35-190">Точность</span><span class="sxs-lookup"><span data-stu-id="bce35-190">Precision</span></span>         | <span data-ttu-id="bce35-191">Значение</span><span class="sxs-lookup"><span data-stu-id="bce35-191">Value</span></span>                |
|----------|----------|-------------------|----------------------|
| <span data-ttu-id="bce35-192">x</span><span class="sxs-lookup"><span data-stu-id="bce35-192">x</span></span>        |          | <span data-ttu-id="bce35-193">Полное</span><span class="sxs-lookup"><span data-stu-id="bce35-193">Full</span></span>              | <span data-ttu-id="bce35-194">FP32 или выше</span><span class="sxs-lookup"><span data-stu-id="bce35-194">fp32 or higher</span></span>       |
| <span data-ttu-id="bce35-195">x</span><span class="sxs-lookup"><span data-stu-id="bce35-195">x</span></span>        |          | <span data-ttu-id="bce35-196">Частичная точность</span><span class="sxs-lookup"><span data-stu-id="bce35-196">Partial precision</span></span> | <span data-ttu-id="bce35-197">FP16 = s10e5</span><span class="sxs-lookup"><span data-stu-id="bce35-197">fp16=s10e5</span></span>           |
| <span data-ttu-id="bce35-198">x</span><span class="sxs-lookup"><span data-stu-id="bce35-198">x</span></span>        | <span data-ttu-id="bce35-199">x</span><span class="sxs-lookup"><span data-stu-id="bce35-199">x</span></span>        | <span data-ttu-id="bce35-200">Полное</span><span class="sxs-lookup"><span data-stu-id="bce35-200">Full</span></span>              | <span data-ttu-id="bce35-201">fp24 = s16e7 или выше</span><span class="sxs-lookup"><span data-stu-id="bce35-201">fp24=s16e7 or higher</span></span> |
| <span data-ttu-id="bce35-202">x</span><span class="sxs-lookup"><span data-stu-id="bce35-202">x</span></span>        | <span data-ttu-id="bce35-203">x</span><span class="sxs-lookup"><span data-stu-id="bce35-203">x</span></span>        | <span data-ttu-id="bce35-204">Частичная точность</span><span class="sxs-lookup"><span data-stu-id="bce35-204">Partial precision</span></span> | <span data-ttu-id="bce35-205">FP16 = s10e5</span><span class="sxs-lookup"><span data-stu-id="bce35-205">fp16=s10e5</span></span>           |



 

<span data-ttu-id="bce35-206">PS \_ 3 \_ 0 поддерживает больше точности, чем PS \_ 2 \_ 0.</span><span class="sxs-lookup"><span data-stu-id="bce35-206">ps\_3\_0 supports more precision than ps\_2\_0 does.</span></span> <span data-ttu-id="bce35-207">По умолчанию все операции выполняются на полном уровне точности.</span><span class="sxs-lookup"><span data-stu-id="bce35-207">By default, all operations occur at the full precision level.</span></span>

<span data-ttu-id="bce35-208">Частичная точность (см. [модификаторы регистров построителя текстуры](dx9-graphics-reference-asm-ps-registers-modifiers.md)) запрашивается путем добавления \_ модификатора PP к коду шейдера (при условии, что базовая реализация поддерживает ее).</span><span class="sxs-lookup"><span data-stu-id="bce35-208">Partial precision (see [Pixel Shader Register Modifiers](dx9-graphics-reference-asm-ps-registers-modifiers.md)) is requested by adding the \_pp modifier to shader code (provided that the underlying implementation supports it).</span></span> <span data-ttu-id="bce35-209">Реализации всегда могут игнорировать модификатор и выполнять затронутые операции в полной точности.</span><span class="sxs-lookup"><span data-stu-id="bce35-209">Implementations are always free to ignore the modifier and perform the affected operations in full precision.</span></span>

<span data-ttu-id="bce35-210">\_Модификатор PP может находиться в двух контекстах:</span><span class="sxs-lookup"><span data-stu-id="bce35-210">The \_pp modifier can occur in two contexts:</span></span>

-   <span data-ttu-id="bce35-211">В объявлении координаты текстуры, чтобы передать координаты текстуры частичной точности в шейдер пикселей.</span><span class="sxs-lookup"><span data-stu-id="bce35-211">On a texture coordinate declaration to pass partial-precision texture coordinates to the pixel shader.</span></span> <span data-ttu-id="bce35-212">Это можно использовать, когда текстуры переправляют данные цвета в шейдер пикселей, что может выполняться быстрее с частичной точностью, чем с полной точностью в некоторых реализациях.</span><span class="sxs-lookup"><span data-stu-id="bce35-212">This could be used when texture coordinates relay color data to the pixel shader, which may be faster with partial precision than with full precision in some implementations.</span></span>
-   <span data-ttu-id="bce35-213">В любой инструкции для запроса использования частичной точности, включая инструкции по загрузке текстур.</span><span class="sxs-lookup"><span data-stu-id="bce35-213">On any instruction to request the use of partial precision, including texture load instructions.</span></span> <span data-ttu-id="bce35-214">Это означает, что реализации разрешено выполнять инструкцию с частичной точностью и сохранять результат частичной точности.</span><span class="sxs-lookup"><span data-stu-id="bce35-214">This indicates that the implementation is allowed to execute the instruction with partial precision and store a partial-precision result.</span></span> <span data-ttu-id="bce35-215">При отсутствии явного модификатора инструкция должна выполняться с полной точностью (независимо от точности входных операндов).</span><span class="sxs-lookup"><span data-stu-id="bce35-215">In the absence of an explicit modifier, the instruction must be performed at full precision (regardless of the precision of the input operands).</span></span>

<span data-ttu-id="bce35-216">Приложение может намеренно выбрать неточное снижение производительности.</span><span class="sxs-lookup"><span data-stu-id="bce35-216">An application might deliberately choose to trade off precision for performance.</span></span> <span data-ttu-id="bce35-217">Существует несколько типов входных данных шейдера, которые являются естественными кандидатами для обработки частичной точности.</span><span class="sxs-lookup"><span data-stu-id="bce35-217">There are several kinds of shader input data which are natural candidates for partial precision processing:</span></span>

-   <span data-ttu-id="bce35-218">Итераторы цвета хорошо представлены значениями частичной точности.</span><span class="sxs-lookup"><span data-stu-id="bce35-218">Color iterators are well represented by partial-precision values.</span></span>
-   <span data-ttu-id="bce35-219">Значения текстур из большинства форматов могут быть точно представлены значениями частичной точности (значения, выданные из 32-разрядных текстур формата с плавающей запятой, являются очевидным исключением).</span><span class="sxs-lookup"><span data-stu-id="bce35-219">Texture values from most formats can be accurately represented by partial-precision values (values sampled from 32-bit, floating-point format textures are an obvious exception).</span></span>
-   <span data-ttu-id="bce35-220">Константы могут быть представлены в виде представления частичной точности в соответствии с шейдером.</span><span class="sxs-lookup"><span data-stu-id="bce35-220">Constants may be represented by partial-precision representation as appropriate to the shader.</span></span>

<span data-ttu-id="bce35-221">Во всех этих случаях разработчик может указать частичную точность обработки данных, зная, что точность входных данных не будет потеряна.</span><span class="sxs-lookup"><span data-stu-id="bce35-221">In all these cases the developer may choose to specify partial precision to process the data, knowing that no input data precision is lost.</span></span> <span data-ttu-id="bce35-222">В некоторых случаях шейдер может потребовать, чтобы внутренние шаги вычисления выполнялись с полной точностью, даже если входные и конечные выходные значения не имеют более полной точности.</span><span class="sxs-lookup"><span data-stu-id="bce35-222">In some cases, a shader may require that the internal steps of a calculation be performed at full precision even when input and final output values do not have more than partial precision.</span></span>

## <a name="software-vertex-and-pixel-shaders"></a><span data-ttu-id="bce35-223">Программная вершина и шейдеры пикселей</span><span class="sxs-lookup"><span data-stu-id="bce35-223">Software Vertex and Pixel Shaders</span></span>

<span data-ttu-id="bce35-224">В реализациях программного обеспечения (время выполнения и ссылка для шейдеров вершин и ссылки для шейдеров пиксельных координат) \_ шейдеры версии 2 0 и выше имеют неограниченную проверку.</span><span class="sxs-lookup"><span data-stu-id="bce35-224">Software implementations (run-time and reference for vertex shaders and reference for pixel shaders) of version 2\_0 shaders and above have some validation relaxed.</span></span> <span data-ttu-id="bce35-225">Это полезно для целей отладки и создания прототипов.</span><span class="sxs-lookup"><span data-stu-id="bce35-225">This is useful for debugging and prototyping purposes.</span></span> <span data-ttu-id="bce35-226">Приложение указывает среде выполнения или ассемблеру, что требуется неявное применение проверки с помощью \_ флага SW в ассемблере (например, VS \_ 2 \_ SW).</span><span class="sxs-lookup"><span data-stu-id="bce35-226">The application indicates to the runtime/assembler that it needs some of the validation relaxed using the \_sw flag in the assembler (for example, vs\_2\_sw).</span></span> <span data-ttu-id="bce35-227">Программный шейдер не будет работать с оборудованием.</span><span class="sxs-lookup"><span data-stu-id="bce35-227">A software shader will not work with hardware.</span></span>

<span data-ttu-id="bce35-228">VS \_ 2 \_ SW — это ослабление с максимальным ограничением в VS \_ 2 \_ x; аналогичным образом, PS \_ 2 \_ SW — это ослабление с максимальным набором ограничений PS \_ 2 \_ x.</span><span class="sxs-lookup"><span data-stu-id="bce35-228">vs\_2\_sw is a relaxation to the maximum caps of vs\_2\_x; similarly, ps\_2\_sw is a relaxation to the maximum caps of ps\_2\_x.</span></span> <span data-ttu-id="bce35-229">В частности, следующие проверки являются нестрогими:</span><span class="sxs-lookup"><span data-stu-id="bce35-229">Specifically, the following validations are relaxed:</span></span>



| <span data-ttu-id="bce35-230">Модель шейдера</span><span class="sxs-lookup"><span data-stu-id="bce35-230">Shader model</span></span>                                           |  <span data-ttu-id="bce35-231">Ресурс</span><span class="sxs-lookup"><span data-stu-id="bce35-231">Resource</span></span>                                    |  <span data-ttu-id="bce35-232">Ограничение</span><span class="sxs-lookup"><span data-stu-id="bce35-232">Limit</span></span>                                                                                                                                  |
|--------------------------------------------|--------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bce35-233">VS \_ 2 \_ SW, VS \_ 3 \_ SW, PS \_ 2 \_ SW, PS \_ 3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="bce35-233">vs\_2\_sw, vs\_3\_sw, ps\_2\_sw, ps\_3\_sw</span></span> | <span data-ttu-id="bce35-234">Число инструкций</span><span class="sxs-lookup"><span data-stu-id="bce35-234">Instruction Counts</span></span>                   | <span data-ttu-id="bce35-235">Неограниченно</span><span class="sxs-lookup"><span data-stu-id="bce35-235">Unlimited</span></span>                                                                                                                         |
| <span data-ttu-id="bce35-236">VS \_ 2 \_ SW, VS \_ 3 \_ SW, PS \_ 2 \_ SW, PS \_ 3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="bce35-236">vs\_2\_sw, vs\_3\_sw, ps\_2\_sw, ps\_3\_sw</span></span> | <span data-ttu-id="bce35-237">Регистры констант float</span><span class="sxs-lookup"><span data-stu-id="bce35-237">Float Constant Registers</span></span>             | <span data-ttu-id="bce35-238">8192</span><span class="sxs-lookup"><span data-stu-id="bce35-238">8192</span></span>                                                                                                                              |
| <span data-ttu-id="bce35-239">VS \_ 2 \_ SW, VS \_ 3 \_ SW, PS \_ 2 \_ SW, PS \_ 3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="bce35-239">vs\_2\_sw, vs\_3\_sw, ps\_2\_sw, ps\_3\_sw</span></span> | <span data-ttu-id="bce35-240">Регистры целочисленных констант</span><span class="sxs-lookup"><span data-stu-id="bce35-240">Integer Constant Registers</span></span>           | <span data-ttu-id="bce35-241">2048</span><span class="sxs-lookup"><span data-stu-id="bce35-241">2048</span></span>                                                                                                                              |
| <span data-ttu-id="bce35-242">VS \_ 2 \_ SW, VS \_ 3 \_ SW, PS \_ 2 \_ SW, PS \_ 3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="bce35-242">vs\_2\_sw, vs\_3\_sw, ps\_2\_sw, ps\_3\_sw</span></span> | <span data-ttu-id="bce35-243">Регистры логических констант</span><span class="sxs-lookup"><span data-stu-id="bce35-243">Boolean Constant Registers</span></span>           | <span data-ttu-id="bce35-244">2048</span><span class="sxs-lookup"><span data-stu-id="bce35-244">2048</span></span>                                                                                                                              |
| <span data-ttu-id="bce35-245">PS \_ 2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="bce35-245">ps\_2\_sw</span></span>                                  | <span data-ttu-id="bce35-246">Глубина зависимого чтения</span><span class="sxs-lookup"><span data-stu-id="bce35-246">Dependent-read depth</span></span>                 | <span data-ttu-id="bce35-247">Неограниченно</span><span class="sxs-lookup"><span data-stu-id="bce35-247">Unlimited</span></span>                                                                                                                         |
| <span data-ttu-id="bce35-248">VS \_ 2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="bce35-248">vs\_2\_sw</span></span>                                  | <span data-ttu-id="bce35-249">инструкции и метки управления потоком</span><span class="sxs-lookup"><span data-stu-id="bce35-249">flow control instructions and labels</span></span> | <span data-ttu-id="bce35-250">Неограниченно</span><span class="sxs-lookup"><span data-stu-id="bce35-250">Unlimited</span></span>                                                                                                                         |
| <span data-ttu-id="bce35-251">VS \_ 2 \_ SW, VS \_ 3 \_ SW, PS \_ 2 \_ SW, PS \_ 3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="bce35-251">vs\_2\_sw, vs\_3\_sw, ps\_2\_sw, ps\_3\_sw</span></span> | <span data-ttu-id="bce35-252">Начало/шаг/количество циклов</span><span class="sxs-lookup"><span data-stu-id="bce35-252">Loop start/step/counts</span></span>               | <span data-ttu-id="bce35-253">Начало итерации и размер шага итерации для инструкций-представительов и циклов — 32-разрядные целые числа со знаком.</span><span class="sxs-lookup"><span data-stu-id="bce35-253">Iteration start and iteration step size for rep and loop instructions are 32-bit signed integers.</span></span> <span data-ttu-id="bce35-254">Число может быть до максимального числа \_ int/64.</span><span class="sxs-lookup"><span data-stu-id="bce35-254">Count can be up to MAX\_INT/64.</span></span> |
| <span data-ttu-id="bce35-255">VS \_ 2 \_ SW, VS \_ 3 \_ SW, PS \_ 2 \_ SW, PS \_ 3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="bce35-255">vs\_2\_sw, vs\_3\_sw, ps\_2\_sw, ps\_3\_sw</span></span> | <span data-ttu-id="bce35-256">Ограничения портов</span><span class="sxs-lookup"><span data-stu-id="bce35-256">Port limits</span></span>                          | <span data-ttu-id="bce35-257">Ограничения портов для всех файлов регистрации нестрогие.</span><span class="sxs-lookup"><span data-stu-id="bce35-257">Port limits for all register files are relaxed.</span></span>                                                                                   |
| <span data-ttu-id="bce35-258">VS \_ 3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="bce35-258">vs\_3\_sw</span></span>                                  | <span data-ttu-id="bce35-259">Число интерполяций</span><span class="sxs-lookup"><span data-stu-id="bce35-259">Number of interpolators</span></span>              | <span data-ttu-id="bce35-260">16 выходных регистров в VS \_ 3 \_ SW.</span><span class="sxs-lookup"><span data-stu-id="bce35-260">16 output registers in vs\_3\_sw.</span></span>                                                                                                 |
| <span data-ttu-id="bce35-261">PS \_ 3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="bce35-261">ps\_3\_sw</span></span>                                  | <span data-ttu-id="bce35-262">Число интерполяций</span><span class="sxs-lookup"><span data-stu-id="bce35-262">Number of interpolators</span></span>              | <span data-ttu-id="bce35-263">14 (16-2) входные регистры для PS \_ 3 \_ SW.</span><span class="sxs-lookup"><span data-stu-id="bce35-263">14(16-2) input registers for ps\_3\_sw.</span></span>                                                                                           |



 

## <a name="related-topics"></a><span data-ttu-id="bce35-264">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="bce35-264">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bce35-265">Модель шейдера 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="bce35-265">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md)
</dt> </dl>

 

 
