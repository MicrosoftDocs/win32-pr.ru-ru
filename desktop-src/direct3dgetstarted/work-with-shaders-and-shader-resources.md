---
title: Работа с шейдерами и ресурсами шейдера
description: Научитесь работать с шейдерами и ресурсами шейдеров в процессе разработки игры Microsoft DirectX для Windows 8.
ms.assetid: 25a11983-e3f6-4bd3-86f1-d660edc4cd4b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 26ac147971221b04b02f2a45af8e8d4f6855a5e3
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104413160"
---
# <a name="work-with-shaders-and-shader-resources"></a><span data-ttu-id="ee2db-103">Работа с шейдерами и ресурсами шейдера</span><span class="sxs-lookup"><span data-stu-id="ee2db-103">Work with shaders and shader resources</span></span>

<span data-ttu-id="ee2db-104">Научитесь работать с шейдерами и ресурсами шейдеров в процессе разработки игры Microsoft DirectX для Windows 8.</span><span class="sxs-lookup"><span data-stu-id="ee2db-104">It's time to learn how to work with shaders and shader resources in developing your Microsoft DirectX game for Windows 8.</span></span> <span data-ttu-id="ee2db-105">Мы рассмотрели, как настроить графическое устройство и ресурсы, и, возможно, вы даже начали изменять его конвейер.</span><span class="sxs-lookup"><span data-stu-id="ee2db-105">We've seen how to set up the graphics device and resources, and perhaps you've even started modifying its pipeline.</span></span> <span data-ttu-id="ee2db-106">Теперь давайте взглянем на шейдеры пикселей и вершин.</span><span class="sxs-lookup"><span data-stu-id="ee2db-106">So now let's look at pixel and vertex shaders.</span></span>

<span data-ttu-id="ee2db-107">Если вы не знакомы с языками шейдеров, можно быстро обсуждать их в порядке.</span><span class="sxs-lookup"><span data-stu-id="ee2db-107">If you aren't familiar with shader languages, a quick discussion is in order.</span></span> <span data-ttu-id="ee2db-108">Шейдеры — это небольшие программы низкого уровня, которые компилируются и выполняются на конкретных этапах конвейера графики.</span><span class="sxs-lookup"><span data-stu-id="ee2db-108">Shaders are small, low-level programs that are compiled and run at specific stages in the graphics pipeline.</span></span> <span data-ttu-id="ee2db-109">Их специальность — это очень быстрые математические операции с плавающей точкой.</span><span class="sxs-lookup"><span data-stu-id="ee2db-109">Their specialty is very fast floating-point mathematical operations.</span></span> <span data-ttu-id="ee2db-110">Наиболее распространенные программы шейдеров:</span><span class="sxs-lookup"><span data-stu-id="ee2db-110">The most common shader programs are:</span></span>

-   <span data-ttu-id="ee2db-111">**Шейдер вершин**— выполняется для каждой вершины в сцене.</span><span class="sxs-lookup"><span data-stu-id="ee2db-111">**Vertex shader**—Executed for each vertex in a scene.</span></span> <span data-ttu-id="ee2db-112">Этот шейдер работает с элементами буфера вершин, предоставленными ему вызывающим приложением, и, как минимум, приводит к постановке вектора расположения с 4 компонентами, который будет разделяться в пиксельном положении.</span><span class="sxs-lookup"><span data-stu-id="ee2db-112">This shader operates on vertex buffer elements provided to it by the calling app, and minimally results in a 4-component position vector that will be rasterized into a pixel position.</span></span>
-   <span data-ttu-id="ee2db-113">**Шейдер пикселей**— выполняется для каждого пикселя в целевом объекте прорисовки.</span><span class="sxs-lookup"><span data-stu-id="ee2db-113">**Pixel shader**—Executed for each pixel in a render target.</span></span> <span data-ttu-id="ee2db-114">Этот шейдер получает растровые координаты от предыдущих этапов шейдера (в простейших конвейерах это будет шейдер вершин) и возвращает цвет (или другое значение 4 компонентов) для этой точки в пикселях, которая затем записывается в целевой объект отрисовки.</span><span class="sxs-lookup"><span data-stu-id="ee2db-114">This shader receives rasterized coordinates from previous shader stages (in the simplest pipelines, this would be the vertex shader) and returns a color (or other 4-component value) for that pixel position, which is then written into a render target.</span></span>

<span data-ttu-id="ee2db-115">Этот пример включает очень простые шейдеры вершин и пикселей, которые рисуют только геометрию и более сложные шейдеры, добавляющие базовые вычисления освещения.</span><span class="sxs-lookup"><span data-stu-id="ee2db-115">This example includes very basic vertex and pixel shaders that only draw geometry, and more complex shaders that add basic lighting calculations.</span></span>

<span data-ttu-id="ee2db-116">Программы шейдеров написаны на языке шейдера высокого уровня (HLSL).</span><span class="sxs-lookup"><span data-stu-id="ee2db-116">Shader programs are written in Microsoft High Level Shader Language (HLSL).</span></span> <span data-ttu-id="ee2db-117">Синтаксис HLSL выглядит очень похоже на C, но без указателей.</span><span class="sxs-lookup"><span data-stu-id="ee2db-117">HLSL syntax looks a lot like C, but without the pointers.</span></span> <span data-ttu-id="ee2db-118">Программы шейдеров должны быть очень компактными и эффективными.</span><span class="sxs-lookup"><span data-stu-id="ee2db-118">Shader programs must be very compact and efficient.</span></span> <span data-ttu-id="ee2db-119">Если шейдер компилируется в слишком много инструкций, он не может быть выполнен и возвращается ошибка.</span><span class="sxs-lookup"><span data-stu-id="ee2db-119">If your shader compiles to too many instructions, it cannot be run and an error is returned.</span></span> <span data-ttu-id="ee2db-120">(Обратите внимание, что точное допустимое количество инструкций является частью [уровня функций Direct3D](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro).)</span><span class="sxs-lookup"><span data-stu-id="ee2db-120">(Note that the exact number of instructions allowed is part of the [Direct3D feature level](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro).)</span></span>

<span data-ttu-id="ee2db-121">В Direct3D шейдеры не компилируются во время выполнения. они компилируются при компиляции остальной части программы.</span><span class="sxs-lookup"><span data-stu-id="ee2db-121">In Direct3D, shaders are not compiled at run time; they are compiled when the rest of the program is compiled.</span></span> <span data-ttu-id="ee2db-122">При компиляции приложения с Microsoft Visual Studio 2013 файлы HLSL компилируются в файлы CSO (. cso), которые приложение должно загрузить и поместить в память GPU перед прорисовкой.</span><span class="sxs-lookup"><span data-stu-id="ee2db-122">When you compile your app with Microsoft Visual Studio 2013, the HLSL files are compiled to CSO (.cso) files that your app must load and place in GPU memory prior to drawing.</span></span> <span data-ttu-id="ee2db-123">Убедитесь, что вы включили эти файлы CSO в свое приложение при упаковке. они представляют собой ресурсы, такие как сетки и текстуры.</span><span class="sxs-lookup"><span data-stu-id="ee2db-123">Make sure you include these CSO files with your app when you package it; they are assets just like meshes and textures.</span></span>

## <a name="understand-hlsl-semantics"></a><span data-ttu-id="ee2db-124">Общие сведения о семантике HLSL</span><span class="sxs-lookup"><span data-stu-id="ee2db-124">Understand HLSL semantics</span></span>

<span data-ttu-id="ee2db-125">Прежде чем продолжить, важно обсудить семантику HLSL, так как они часто являются предметом путаницы для новых разработчиков Direct3D.</span><span class="sxs-lookup"><span data-stu-id="ee2db-125">It's important to take a moment to discuss HLSL semantics before we continue, because they are often a point of confusion for new Direct3D developers.</span></span> <span data-ttu-id="ee2db-126">Семантика HLSL — это строки, которые определяют значение, передаваемое между приложением и программой шейдера.</span><span class="sxs-lookup"><span data-stu-id="ee2db-126">HLSL semantics are strings that identify a value passed between the app and a shader program.</span></span> <span data-ttu-id="ee2db-127">Хотя они могут быть любыми различными возможными строками, рекомендуется использовать такую строку, как `POSITION` или `COLOR` , которая указывает на использование.</span><span class="sxs-lookup"><span data-stu-id="ee2db-127">Although they can be any of a variety of possible strings, the best practice is to use a string like `POSITION` or `COLOR` that indicates the usage.</span></span> <span data-ttu-id="ee2db-128">Вы назначаете эту семантику при построении буфера констант или макета ввода.</span><span class="sxs-lookup"><span data-stu-id="ee2db-128">You assign these semantics when you are constructing a constant buffer or input layout.</span></span> <span data-ttu-id="ee2db-129">Можно также добавлять к семантике цифру от 0 до 7, чтобы использовать отдельные регистры для сходных значений.</span><span class="sxs-lookup"><span data-stu-id="ee2db-129">You can also append a number between 0 and 7 to the semantic so that you use separate registers for similar values.</span></span> <span data-ttu-id="ee2db-130">Например: COLOR0, COLOR1, COLOR2...</span><span class="sxs-lookup"><span data-stu-id="ee2db-130">For example: COLOR0, COLOR1, COLOR2...</span></span>

<span data-ttu-id="ee2db-131">Семантика с префиксом «SV \_ » — это семантика *системных значений* , записываемая программой шейдера; сама игра (работающая на ЦП) не может изменить их.</span><span class="sxs-lookup"><span data-stu-id="ee2db-131">Semantics that are prefixed with "SV\_" are *system value* semantics that are written to by your shader program; your game itself (running on the CPU) cannot modify them.</span></span> <span data-ttu-id="ee2db-132">Как правило, эти семантики содержат значения, которые являются входными или выходными данными из другого этапа шейдера в графическом конвейере или полностью созданы графическим процессором.</span><span class="sxs-lookup"><span data-stu-id="ee2db-132">Typically, these semantics contain values that are inputs or outputs from another shader stage in the graphics pipeline, or that are generated entirely by the GPU.</span></span>

<span data-ttu-id="ee2db-133">Кроме того, `SV_` семантика имеет различные поведения, когда они используются для указания входных данных или выходных данных на этапе шейдера.</span><span class="sxs-lookup"><span data-stu-id="ee2db-133">Additionally, `SV_` semantics have different behaviors when they are used to specify input to or output from a shader stage.</span></span> <span data-ttu-id="ee2db-134">Например, `SV_POSITION` (Output) содержит данные вершин, преобразованные на этапе шейдера вершин, а `SV_POSITION` (*входные* данные) содержат значения точек в пикселях, которые были интерполяции GPU во время этапа растрирования.</span><span class="sxs-lookup"><span data-stu-id="ee2db-134">For example, `SV_POSITION` (output) contains the vertex data transformed during the vertex shader stage, and `SV_POSITION` (*input*) contains the pixel position values that were interpolated by the GPU during the rasterization stage.</span></span>

<span data-ttu-id="ee2db-135">Ниже приведена общая семантика HLSL:</span><span class="sxs-lookup"><span data-stu-id="ee2db-135">Here are a few common HLSL semantics:</span></span>

-   <span data-ttu-id="ee2db-136">`POSITION`(*n*) для данных в буфере вершин.</span><span class="sxs-lookup"><span data-stu-id="ee2db-136">`POSITION`(*n*) for vertex buffer data.</span></span> <span data-ttu-id="ee2db-137">`SV_POSITION` Задает точку в пикселе шейдера пикселей и не может быть записана в игре.</span><span class="sxs-lookup"><span data-stu-id="ee2db-137">`SV_POSITION` provides a pixel position to the pixel shader and cannot be written by your game.</span></span>
-   <span data-ttu-id="ee2db-138">`NORMAL`(*n*) для обычных данных, предоставляемых буфером вершин.</span><span class="sxs-lookup"><span data-stu-id="ee2db-138">`NORMAL`(*n*) for normal data provided by the vertex buffer.</span></span>
-   <span data-ttu-id="ee2db-139">`TEXCOORD`(*n*) для данных текстуры UV-координат, предоставляемых шейдеру.</span><span class="sxs-lookup"><span data-stu-id="ee2db-139">`TEXCOORD`(*n*) for texture UV coordinate data supplied to a shader.</span></span>
-   <span data-ttu-id="ee2db-140">`COLOR`(n) для цветовых данных RGBA, предоставляемых шейдеру.</span><span class="sxs-lookup"><span data-stu-id="ee2db-140">`COLOR`(n) for RGBA color data supplied to a shader.</span></span> <span data-ttu-id="ee2db-141">Обратите внимание, что он обрабатывается одинаково для координации данных, включая интерполяцию значения во время растрирования. семантика просто помогает понять, что это данные цвета.</span><span class="sxs-lookup"><span data-stu-id="ee2db-141">Note that it is treated identically to coordinate data, including interpolating the value during rasterization; the semantic simply helps you identify that it is color data.</span></span>
-   <span data-ttu-id="ee2db-142">`SV_Target`\[n \] для записи из шейдера пикселей в целевую текстуру или другой буфер пикселей.</span><span class="sxs-lookup"><span data-stu-id="ee2db-142">`SV_Target`\[n\] for writing from a pixel shader to a target texture or other pixel buffer.</span></span>

<span data-ttu-id="ee2db-143">Мы рассмотрим некоторые примеры семантики HLSL, как мы рассмотрим пример.</span><span class="sxs-lookup"><span data-stu-id="ee2db-143">We'll see some examples of HLSL semantics as we review the example.</span></span>

## <a name="read-from-the-constant-buffers"></a><span data-ttu-id="ee2db-144">Чтение из буферов констант</span><span class="sxs-lookup"><span data-stu-id="ee2db-144">Read from the constant buffers</span></span>

<span data-ttu-id="ee2db-145">Любой шейдер может считывать из буфера констант, если этот буфер присоединен к его этапу в качестве ресурса.</span><span class="sxs-lookup"><span data-stu-id="ee2db-145">Any shader can read from a constant buffer if that buffer is attached to its stage as a resource.</span></span> <span data-ttu-id="ee2db-146">В этом примере только шейдеру вершин назначен буфер констант.</span><span class="sxs-lookup"><span data-stu-id="ee2db-146">In this example, only the vertex shader is assigned a constant buffer.</span></span>

<span data-ttu-id="ee2db-147">Буфер константы объявляется в двух местах: в коде C++ и в соответствующих файлах HLSL, которые будут обращаться к нему.</span><span class="sxs-lookup"><span data-stu-id="ee2db-147">The constant buffer is declared in two places: in the C++ code, and in the corresponding HLSL files that will access it.</span></span>

<span data-ttu-id="ee2db-148">Вот как объявляется структура буфера констант в коде C++.</span><span class="sxs-lookup"><span data-stu-id="ee2db-148">Here's how the constant buffer struct is declared in the C++ code.</span></span>


```C++
typedef struct _constantBufferStruct {
    DirectX::XMFLOAT4X4 world;
    DirectX::XMFLOAT4X4 view;
    DirectX::XMFLOAT4X4 projection;
} ConstantBufferStruct;
```



<span data-ttu-id="ee2db-149">При объявлении структуры для буфера констант в коде C++ Убедитесь, что все данные правильно выводятся по 16-байтным границам.</span><span class="sxs-lookup"><span data-stu-id="ee2db-149">When declaring the structure for the constant buffer in your C++ code, ensure that all of the data is correctly aligned along 16-byte boundaries.</span></span> <span data-ttu-id="ee2db-150">Самый простой способ сделать это — использовать типы [директксмас](/windows/desktop/dxmath/directxmath-portal) , такие как **XMFLOAT4** или **XMFLOAT4X4**, как показано в примере кода.</span><span class="sxs-lookup"><span data-stu-id="ee2db-150">The easiest way to do this is to use [DirectXMath](/windows/desktop/dxmath/directxmath-portal) types, like **XMFLOAT4** or **XMFLOAT4X4**, as seen in the example code.</span></span> <span data-ttu-id="ee2db-151">Можно также защититься от несогласованных буферов путем объявления статического утверждения:</span><span class="sxs-lookup"><span data-stu-id="ee2db-151">You can also guard against misaligned buffers by declaring a static assert:</span></span>


```C++
// Assert that the constant buffer remains 16-byte aligned.
static_assert((sizeof(ConstantBufferStruct) % 16) == 0, "Constant Buffer size must be 16-byte aligned");
```



<span data-ttu-id="ee2db-152">Эта строка кода вызовет ошибку во время компиляции, если **константбуфферструкт** не является 16-байтовым.</span><span class="sxs-lookup"><span data-stu-id="ee2db-152">This line of code will cause an error at compile time if **ConstantBufferStruct** is not 16-byte aligned.</span></span> <span data-ttu-id="ee2db-153">Дополнительные сведения о выравнивании и упаковке буфера констант см. в разделе [правила упаковки для переменных констант](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-packing-rules).</span><span class="sxs-lookup"><span data-stu-id="ee2db-153">For more information about constant buffer alignment and packing, see [Packing Rules for Constant Variables](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-packing-rules).</span></span>

<span data-ttu-id="ee2db-154">Теперь вот как объявляется буфер констант в шейдере вершин HLSL.</span><span class="sxs-lookup"><span data-stu-id="ee2db-154">Now, here's how the constant buffer is declared in the vertex shader HLSL.</span></span>


```C++
cbuffer ModelViewProjectionConstantBuffer : register(b0)
{
    matrix mWorld;      // world matrix for object
    matrix View;        // view matrix
    matrix Projection;  // projection matrix
};
```



<span data-ttu-id="ee2db-155">Все буферы — константы, текстуры, образцы или другие — должны иметь определенный регистр, чтобы GPU мог получить к ним доступ.</span><span class="sxs-lookup"><span data-stu-id="ee2db-155">All buffers—constant, texture, sampler, or other—must have a register defined so the GPU can access them.</span></span> <span data-ttu-id="ee2db-156">Каждый этап шейдера поддерживает до 15 буферов констант, и каждый буфер может содержать до 4 096 переменных констант.</span><span class="sxs-lookup"><span data-stu-id="ee2db-156">Each shader stage allows up to 15 constant buffers, and each buffer can hold up to 4,096 constant variables.</span></span> <span data-ttu-id="ee2db-157">Синтаксис объявления использования регистра выглядит следующим образом:</span><span class="sxs-lookup"><span data-stu-id="ee2db-157">The register-usage declaration syntax is as follows:</span></span>

-   <span data-ttu-id="ee2db-158">**b \* \* *\#* : регистр для буфера констант (** кбуффер \* \*).</span><span class="sxs-lookup"><span data-stu-id="ee2db-158">**b\*\**\#*: A register for a constant buffer (** cbuffer\*\*).</span></span>
-   <span data-ttu-id="ee2db-159">**t \* \* *\#* : регистр для буфера текстуры (** тбуффер \* \*).</span><span class="sxs-lookup"><span data-stu-id="ee2db-159">**t\*\**\#*: A register for a texture buffer (** tbuffer\*\*).</span></span>
-   <span data-ttu-id="ee2db-160">**s \* \* \#**: регистрация для образца.</span><span class="sxs-lookup"><span data-stu-id="ee2db-160">\**s\*\*\*\#*: A register for a sampler.</span></span> <span data-ttu-id="ee2db-161">(Образец определяет поведение поиска для пикселей текстуры в ресурсе текстуры.)</span><span class="sxs-lookup"><span data-stu-id="ee2db-161">(A sampler defines the lookup behavior for texels in the texture resource.)</span></span>

<span data-ttu-id="ee2db-162">Например, HLSL для шейдера пикселей может взять текстуру и образец в качестве входных данных с объявлением, подобным этому.</span><span class="sxs-lookup"><span data-stu-id="ee2db-162">For example, the HLSL for a pixel shader might take a texture and a sampler as input with a declaration like this.</span></span>

``` syntax
Texture2D simpleTexture : register(t0);
SamplerState simpleSampler : register(s0);
```

<span data-ttu-id="ee2db-163">Вы можете назначать постоянные буферы для регистрации — при настройке конвейера вы подключаете буфер константы к тому же слоту, в котором он был назначен в файле HLSL.</span><span class="sxs-lookup"><span data-stu-id="ee2db-163">It's up to you to assign constant buffers to registers—when you set up the pipeline, you attach a constant buffer to the same slot you assigned it to in the HLSL file.</span></span> <span data-ttu-id="ee2db-164">Например, в предыдущем разделе вызов [**вссетконстантбуфферс**](/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-vssetconstantbuffers) указывает "0" для первого параметра.</span><span class="sxs-lookup"><span data-stu-id="ee2db-164">For example, in the previous topic the call to [**VSSetConstantBuffers**](/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-vssetconstantbuffers) indicates '0' for the first parameter.</span></span> <span data-ttu-id="ee2db-165">Это указывает Direct3D подключить ресурс буфера константы для регистрации 0, который соответствует назначению буфера для **регистрации (B0)** в файле HLSL.</span><span class="sxs-lookup"><span data-stu-id="ee2db-165">That tells Direct3D to attach the constant buffer resource to register 0, which matches the buffer's assignment to **register(b0)** in the HLSL file.</span></span>

## <a name="read-from-the-vertex-buffers"></a><span data-ttu-id="ee2db-166">Чтение из буферов вершин</span><span class="sxs-lookup"><span data-stu-id="ee2db-166">Read from the vertex buffers</span></span>

<span data-ttu-id="ee2db-167">Буфер вершин предоставляет данные треугольника для объектов сцены в шейдер вершин.</span><span class="sxs-lookup"><span data-stu-id="ee2db-167">The vertex buffer supplies the triangle data for the scene objects to the vertex shader(s).</span></span> <span data-ttu-id="ee2db-168">Как и в случае с буфером констант, структура буфера вершин объявляется в коде C++ с использованием аналогичных правил упаковки.</span><span class="sxs-lookup"><span data-stu-id="ee2db-168">As with the constant buffer, the vertex buffer struct is declared in the C++ code, using similar packing rules.</span></span>


```C++
typedef struct _vertexPositionColor
{
    DirectX::XMFLOAT3 pos;
    DirectX::XMFLOAT3 color;
} VertexPositionColor;
```



<span data-ttu-id="ee2db-169">В Direct3D 11 нет стандартного формата для данных вершин.</span><span class="sxs-lookup"><span data-stu-id="ee2db-169">There is no standard format for vertex data in Direct3D 11.</span></span> <span data-ttu-id="ee2db-170">Вместо этого мы определяем собственный макет данных вершин с помощью дескриптора. поля данных определяются с помощью массива структур [**D3D11 \_ \_ элемента \_ input**](/windows/desktop/api/d3d11/ns-d3d11-d3d11_input_element_desc) .</span><span class="sxs-lookup"><span data-stu-id="ee2db-170">Instead, we define our own vertex data layout using a descriptor; the data fields are defined using an array of [**D3D11\_INPUT\_ELEMENT\_DESC**](/windows/desktop/api/d3d11/ns-d3d11-d3d11_input_element_desc) structures.</span></span> <span data-ttu-id="ee2db-171">Здесь показан простой макет ввода, описывающий тот же формат вершин, что и в предыдущей структуре:</span><span class="sxs-lookup"><span data-stu-id="ee2db-171">Here, we show a simple input layout that describes the same vertex format as the preceding struct:</span></span>


```C++
D3D11_INPUT_ELEMENT_DESC iaDesc [] =
{
    { "POSITION", 0, DXGI_FORMAT_R32G32B32_FLOAT,
    0, 0, D3D11_INPUT_PER_VERTEX_DATA, 0 },

    { "COLOR", 0, DXGI_FORMAT_R32G32B32_FLOAT,
    0, 12, D3D11_INPUT_PER_VERTEX_DATA, 0 },
};

hr = device->CreateInputLayout(
    iaDesc,
    ARRAYSIZE(iaDesc),
    bytes,
    bytesRead,
    &m_pInputLayout
    );
```



<span data-ttu-id="ee2db-172">Если вы добавляете данные в формат вершины при изменении кода примера, не забудьте также обновить макет ввода, или шейдер не сможет его интерпретировать.</span><span class="sxs-lookup"><span data-stu-id="ee2db-172">If you add data to the vertex format when modifying the example code, be sure to update the input layout as well, or the shader will not be able to interpret it.</span></span> <span data-ttu-id="ee2db-173">Вы можете изменить макет вершин следующим образом:</span><span class="sxs-lookup"><span data-stu-id="ee2db-173">You might modify the vertex layout like this:</span></span>


```C++
typedef struct _vertexPositionColorTangent
{
    DirectX::XMFLOAT3 pos;
    DirectX::XMFLOAT3 normal;
    DirectX::XMFLOAT3 tangent;
} VertexPositionColorTangent;
```



<span data-ttu-id="ee2db-174">В этом случае необходимо изменить определение макета ввода следующим образом.</span><span class="sxs-lookup"><span data-stu-id="ee2db-174">In that case, you'd modify the input-layout definition as follows.</span></span>


```C++
D3D11_INPUT_ELEMENT_DESC iaDescExtended[] =
{
    { "POSITION", 0, DXGI_FORMAT_R32G32B32_FLOAT,
    0, 0, D3D11_INPUT_PER_VERTEX_DATA, 0 },

    { "NORMAL", 0, DXGI_FORMAT_R32G32B32_FLOAT,
    0, 12, D3D11_INPUT_PER_VERTEX_DATA, 0 },

    { "TANGENT", 0, DXGI_FORMAT_R32G32B32_FLOAT,
    0, 12, D3D11_INPUT_PER_VERTEX_DATA, 0 },
};

hr = device->CreateInputLayout(
    iaDesc,
    ARRAYSIZE(iaDesc),
    bytes,
    bytesRead,
    &m_pInputLayoutExtended
    );
```



<span data-ttu-id="ee2db-175">Каждый из определений элементов входной компоновки имеет префикс String, например "положение" или "нормальный", который описан ранее в этом разделе.</span><span class="sxs-lookup"><span data-stu-id="ee2db-175">Each of the input-layout element definitions is prefixed with a string, like "POSITION" or "NORMAL"—that is the semantic we discussed earlier in this topic.</span></span> <span data-ttu-id="ee2db-176">Он подобен обработчику, который позволяет графическому процессору обозначать этот элемент при обработке вершины.</span><span class="sxs-lookup"><span data-stu-id="ee2db-176">It's like a handle that helps the GPU identify that element when processing the vertex.</span></span> <span data-ttu-id="ee2db-177">Выберите Общие, понятные имена для элементов вершин.</span><span class="sxs-lookup"><span data-stu-id="ee2db-177">Choose common, meaningful names for your vertex elements.</span></span>

<span data-ttu-id="ee2db-178">Точно так же, как и в случае с буфером констант, Вершинный шейдер имеет соответствующее определение буфера для входящих элементов вершины.</span><span class="sxs-lookup"><span data-stu-id="ee2db-178">Just as with the constant buffer, the vertex shader has a corresponding buffer definition for incoming vertex elements.</span></span> <span data-ttu-id="ee2db-179">(По этой причине мы предоставили ссылку на ресурс шейдера вершин при создании структуры входных данных. Direct3D проверяет компоновку с использованием входной структуры шейдера.) Обратите внимание, что семантика совпадает с определением входного макета и объявлением буфера HLSL.</span><span class="sxs-lookup"><span data-stu-id="ee2db-179">(That's why we provided a reference to the vertex shader resource when creating the input layout - Direct3D validates the per-vertex data layout with the shader's input struct.) Note how the semantics match between the input layout definition and this HLSL buffer declaration.</span></span> <span data-ttu-id="ee2db-180">При этом `COLOR` к нему добавляется "0".</span><span class="sxs-lookup"><span data-stu-id="ee2db-180">However, `COLOR` has a "0" appended to it.</span></span> <span data-ttu-id="ee2db-181">Нет необходимости добавлять 0, если `COLOR` в макете объявлен только один элемент, но рекомендуется добавлять его в тот случай, если вы решили добавить дополнительные элементы цвета в будущем.</span><span class="sxs-lookup"><span data-stu-id="ee2db-181">It isn't necessary to add the 0 if you have only one `COLOR` element declared in the layout, but it's a good practice to append it in case you you choose to add more color elements in the future.</span></span>


```C++
struct VS_INPUT
{
    float3 vPos   : POSITION;
    float3 vColor : COLOR0;
};
```



## <a name="pass-data-between-shaders"></a><span data-ttu-id="ee2db-182">Передача данных между шейдерами</span><span class="sxs-lookup"><span data-stu-id="ee2db-182">Pass data between shaders</span></span>

<span data-ttu-id="ee2db-183">Шейдеры принимают входные типы и возвращают выходные типы из своих основных функций при выполнении.</span><span class="sxs-lookup"><span data-stu-id="ee2db-183">Shaders take input types and return output types from their main functions upon execution.</span></span> <span data-ttu-id="ee2db-184">Для шейдера вершин, определенного в предыдущем разделе, тип входных данных был \_ структурой ввода VS, и мы определили соответствующий макет входных данных и структуру C++.</span><span class="sxs-lookup"><span data-stu-id="ee2db-184">For the vertex shader defined in the previous section, the input type was the VS\_INPUT structure, and we defined a matching input layout and C++ struct.</span></span> <span data-ttu-id="ee2db-185">Массив этой структуры используется для создания буфера вершин в методе **CreateCube** .</span><span class="sxs-lookup"><span data-stu-id="ee2db-185">An array of this struct is used to create a vertex buffer in the **CreateCube** method.</span></span>

<span data-ttu-id="ee2db-186">Шейдер вершин возвращает \_ входную структуру PS, которая должна быть минимально содержать конечную точку вершины 4 компонента (float4).</span><span class="sxs-lookup"><span data-stu-id="ee2db-186">The vertex shader returns a PS\_INPUT structure, which must minimally contain the 4-component (float4) final vertex position.</span></span> <span data-ttu-id="ee2db-187">Значение этой должности должно иметь семантику системного значения, `SV_POSITION` , объявленную для нее, чтобы GPU имел данные, необходимые для выполнения следующего шага рисования.</span><span class="sxs-lookup"><span data-stu-id="ee2db-187">This position value must have the system value semantic, `SV_POSITION`, declared for it so the GPU has the data it needs to perform the next drawing step.</span></span> <span data-ttu-id="ee2db-188">Обратите внимание, что отсутствует соответствие 1:1 между выходным шейдером вершин и входными данными шейдера пикселей. Шейдер вершин возвращает одну структуру для каждой указанной вершины, но шейдер пикселей выполняется один раз для каждого пикселя.</span><span class="sxs-lookup"><span data-stu-id="ee2db-188">Notice that there is not a 1:1 correspondence between vertex shader output and pixel shader input; the vertex shader returns one structure for each vertex it is given, but the pixel shader runs once for each pixel.</span></span> <span data-ttu-id="ee2db-189">Это обусловлено тем, что данные на вершине сначала проходят через этап растрирования.</span><span class="sxs-lookup"><span data-stu-id="ee2db-189">That's because the per-vertex data first passes through the rasterization stage.</span></span> <span data-ttu-id="ee2db-190">Этот этап определяет, на каких пикселях размещается геометрическая геометрия, вычисление интерполяции данных на вершину для каждого пикселя, а затем вызывает шейдер пикселей один раз для каждого из этих пикселов.</span><span class="sxs-lookup"><span data-stu-id="ee2db-190">This stage decides which pixels "cover" the geometry you're drawing, computes interpolated per-vertex data for each pixel, and then calls the pixel shader once for each of those pixels.</span></span> <span data-ttu-id="ee2db-191">Интерполяция является поведением по умолчанию при растрировании выходных значений и является обязательным в частности для правильной обработки данных вектора вывода (светлое векторы, нормали к вершинам, касательные и др.).</span><span class="sxs-lookup"><span data-stu-id="ee2db-191">Interpolation is the default behavior when rasterizing output values, and is essential in particular for the correct processing of output vector data (light vectors, per-vertex normals and tangents, and others).</span></span>


```C++
struct PS_INPUT
{
    float4 Position : SV_POSITION;  // interpolated vertex position (system value)
    float4 Color    : COLOR0;       // interpolated diffuse color
};
```



## <a name="review-the-vertex-shader"></a><span data-ttu-id="ee2db-192">Проверка шейдера вершин</span><span class="sxs-lookup"><span data-stu-id="ee2db-192">Review the vertex shader</span></span>

<span data-ttu-id="ee2db-193">Пример шейдера вершин очень прост: Возьмите вершину (расположение и цвет), преобразуйте позиции из координат модели в перспективные проецированные координаты и верните ее (вместе с цветом) в средство программной прорисовки.</span><span class="sxs-lookup"><span data-stu-id="ee2db-193">The example vertex shader is very simple: take in a vertex (position and color), transform the position from model coordinates into perspective projected coordinates, and return it (along with the color) to the rasterizer.</span></span> <span data-ttu-id="ee2db-194">Обратите внимание, что значение цвета интерполяции выполняется справа вместе с данными о положении, что дает разные значения для каждого пикселя, несмотря на то, что шейдер вершин не выполняет вычисления по значению цвета.</span><span class="sxs-lookup"><span data-stu-id="ee2db-194">Notice that the color value is interpolated right along with the position data, providing a different value for each pixel even though the vertex shader didn't perform any calculations on the color value.</span></span>


```C++
VS_OUTPUT main(VS_INPUT input) // main is the default function name
{
    VS_OUTPUT Output;

    float4 pos = float4(input.vPos, 1.0f);

    // Transform the position from object space to homogeneous projection space
    pos = mul(pos, mWorld);
    pos = mul(pos, View);
    pos = mul(pos, Projection);
    Output.Position = pos;

    // Just pass through the color data
    Output.Color = float4(input.vColor, 1.0f);

    return Output;
}
```



<span data-ttu-id="ee2db-195">Более сложный шейдер вершин, например, который настраивает вершины объекта для заливки по методу Фонга, может выглядеть примерно так.</span><span class="sxs-lookup"><span data-stu-id="ee2db-195">A more complex vertex shader, such as one that sets up an object's vertices for Phong shading, might look more like this.</span></span> <span data-ttu-id="ee2db-196">В этом случае мы используем тот факт, что векторы и нормали интерполируются для приблизительной привлекательной поверхности.</span><span class="sxs-lookup"><span data-stu-id="ee2db-196">In this case, we're taking advantage of the fact that the vectors and normals are interpolated to approximate a smooth-looking surface.</span></span>

``` syntax
// A constant buffer that stores the three basic column-major matrices for composing geometry.
cbuffer ModelViewProjectionConstantBuffer : register(b0)
{
    matrix model;
    matrix view;
    matrix projection;
};

cbuffer LightConstantBuffer : register(b1)
{
    float4 lightPos;
};

struct VertexShaderInput
{
    float3 pos : POSITION;
    float3 normal : NORMAL;
};

// Per-pixel color data passed through the pixel shader.

struct PixelShaderInput
{
    float4 position : SV_POSITION; 
    float3 outVec : POSITION0;
    float3 outNormal : NORMAL0;
    float3 outLightVec : POSITION1;
};

PixelShaderInput main(VertexShaderInput input)
{
    // Inefficient -- doing this only for instruction. Normally, you would
 // premultiply them on the CPU and place them in the cbuffer.
    matrix mvMatrix = mul(model, view);
    matrix mvpMatrix = mul(mvMatrix, projection);

    PixelShaderInput output;

    float4 pos = float4(input.pos, 1.0f);
    float4 normal = float4(input.normal, 1.0f);
    float4 light = float4(lightPos.xyz, 1.0f);

    // 
    float4 eye = float4(0.0f, 0.0f, -2.0f, 1.0f);

    // Transform the vertex position into projected space.
    output.gl_Position = mul(pos, mvpMatrix);
    output.outNormal = mul(normal, mvMatrix).xyz;
    output.outVec = -(eye - mul(pos, mvMatrix)).xyz;
    output.outLightVec = mul(light, mvMatrix).xyz;

    return output;
}
```

## <a name="review-the-pixel-shader"></a><span data-ttu-id="ee2db-197">Проверка построителя текстуры</span><span class="sxs-lookup"><span data-stu-id="ee2db-197">Review the pixel shader</span></span>

<span data-ttu-id="ee2db-198">Этот построитель текстуры в этом примере довольно, возможно, является абсолютным минимальным объемом кода, который можно использовать в шейдере пикселей.</span><span class="sxs-lookup"><span data-stu-id="ee2db-198">This pixel shader in this example is quite possibly the absolute minimum amount of code you can have in a pixel shader.</span></span> <span data-ttu-id="ee2db-199">Он принимает данные цвета с интерполяцией пикселя, созданные во время растрирования, и возвращает их в виде выходных данных, где они будут записаны в целевой объект отрисовки.</span><span class="sxs-lookup"><span data-stu-id="ee2db-199">It takes the interpolated pixel color data generated during rasterization and returns it as output, where it will be written to a render target.</span></span> <span data-ttu-id="ee2db-200">Насколько скучными!</span><span class="sxs-lookup"><span data-stu-id="ee2db-200">How boring!</span></span>


```C++
PS_OUTPUT main(PS_INPUT In)
{
    PS_OUTPUT Output;

    Output.RGBColor = In.Color;

    return Output;
}
```



<span data-ttu-id="ee2db-201">Важной частью является `SV_TARGET` семантика системного значения для возвращаемого значения.</span><span class="sxs-lookup"><span data-stu-id="ee2db-201">The important part is the `SV_TARGET` system-value semantic on the return value.</span></span> <span data-ttu-id="ee2db-202">Он указывает, что выходные данные должны быть записаны в основной целевой объект отрисовки, который является буфером текстуры, переданным в цепочку подкачки для отображения.</span><span class="sxs-lookup"><span data-stu-id="ee2db-202">It indicates that the output is to be written to the primary render target, which is the texture buffer supplied to the swap chain for display.</span></span> <span data-ttu-id="ee2db-203">Это требуется для шейдеров пикселей — без цветовых данных из шейдера пикселей в Direct3D ничего не отображается!</span><span class="sxs-lookup"><span data-stu-id="ee2db-203">This is required for pixel shaders - without the color data from the pixel shader, Direct3D wouldn't have anything to display!</span></span>

<span data-ttu-id="ee2db-204">Пример более сложного шейдера пикселей для выполнения заливки по методу Фонга может выглядеть следующим образом.</span><span class="sxs-lookup"><span data-stu-id="ee2db-204">An example of a more complex pixel shader to perform Phong shading might look like this.</span></span> <span data-ttu-id="ee2db-205">Так как векторы и нормали были интерполируются, нам не нужно вычислять их на основе каждого пикселя.</span><span class="sxs-lookup"><span data-stu-id="ee2db-205">Since the vectors and normals were interpolated, we don't have to compute them on a per-pixel basis.</span></span> <span data-ttu-id="ee2db-206">Однако нам придется повторно нормализовать их из-за того, как работает интерполяция. по сути, нам нужно постепенно «прокрутить» вектор от направления к концу а к направлению на вершину B, сохранив его длину — вхерас интерполяцию, а не горизонтальную линию между двумя конечными точками вектора.</span><span class="sxs-lookup"><span data-stu-id="ee2db-206">However, we do have to re-normalize them because of how interpolation works; conceptually, we need to gradually "spin" the vector from direction at vertex A to direction at vertex B, maintaining its length—wheras interpolation instead cuts across a straight line between the two vector endpoints.</span></span>

``` syntax
cbuffer MaterialConstantBuffer : register(b2)
{
    float4 lightColor;
    float4 Ka;
    float4 Kd;
    float4 Ks;
    float4 shininess;
};

struct PixelShaderInput
{
    float4 position : SV_POSITION;
    float3 outVec : POSITION0;
    float3 normal : NORMAL0;
    float3 light : POSITION1;
};

float4 main(PixelShaderInput input) : SV_TARGET
{
    float3 L = normalize(input.light);
    float3 V = normalize(input.outVec);
    float3 R = normalize(reflect(L, input.normal));

    float4 diffuse = Ka + (lightColor * Kd * max(dot(input.normal, L), 0.0f));
    diffuse = saturate(diffuse);

    float4 specular = Ks * pow(max(dot(R, V), 0.0f), shininess.x - 50.0f);
    specular = saturate(specular);

    float4 finalColor = diffuse + specular;

    return finalColor;
}
```

<span data-ttu-id="ee2db-207">В другом примере шейдер пикселей принимает собственные буферы констант, которые содержат сведения о легких и материальных точках.</span><span class="sxs-lookup"><span data-stu-id="ee2db-207">In another example, the pixel shader takes its own constant buffers that contain light and material information.</span></span> <span data-ttu-id="ee2db-208">Входной макет шейдера вершин будет расширен, чтобы включить обычные данные, а выходные данные этого шейдера вершин должны включать преобразованные векторы для вершины, освещение и нормальную вершину в системе координат представления.</span><span class="sxs-lookup"><span data-stu-id="ee2db-208">The input layout in the vertex shader would be expanded to include normal data, and the output from that vertex shader is expected to include transformed vectors for the vertex, the light, and the vertex normal in the view coordinate system.</span></span>

<span data-ttu-id="ee2db-209">Если у вас есть буферы текстур и пробы с назначенными регистрами (**t** и **s** соответственно), к ним можно обращаться также в шейдере пикселей.</span><span class="sxs-lookup"><span data-stu-id="ee2db-209">If you have texture buffers and samplers with assigned registers (**t** and **s**, respectively), you can access them in the pixel shader also.</span></span>

``` syntax
Texture2D simpleTexture : register(t0);
SamplerState simpleSampler : register(s0);

struct PixelShaderInput
{
    float4 pos : SV_POSITION;
    float3 norm : NORMAL;
    float2 tex : TEXCOORD0;
};

float4 SimplePixelShader(PixelShaderInput input) : SV_TARGET
{
    float3 lightDirection = normalize(float3(1, -1, 0));
    float4 texelColor = simpleTexture.Sample(simpleSampler, input.tex);
    float lightMagnitude = 0.8f * saturate(dot(input.norm, -lightDirection)) + 0.2f;
    return texelColor * lightMagnitude;
}
```

<span data-ttu-id="ee2db-210">Шейдеры — это мощные средства, которые можно использовать для создания процедурных ресурсов, таких как теневые карты или текстуры шума.</span><span class="sxs-lookup"><span data-stu-id="ee2db-210">Shaders are very powerful tools that can be used to generate procedural resources like shadow maps or noise textures.</span></span> <span data-ttu-id="ee2db-211">На самом деле, для расширенных методик требуется, чтобы текстуры были более абстрактными, а не как визуальные элементы, но как буферы.</span><span class="sxs-lookup"><span data-stu-id="ee2db-211">In fact, advanced techniques require that you think of textures more abstractly, not as visual elements but as buffers.</span></span> <span data-ttu-id="ee2db-212">Они хранят данные, такие как сведения о высоте, или другие данные, которые могут быть выделены в заключительном фрагменте шейдера пикселей, или в этом конкретном кадре в составе многоэтапных эффектов.</span><span class="sxs-lookup"><span data-stu-id="ee2db-212">They hold data like height information, or other data that can be sampled in the final pixel shader pass or in that particular frame as part of a multi-stage effects pass.</span></span> <span data-ttu-id="ee2db-213">Множественная выборка — это мощный инструмент и основа многих современных визуальных эффектов.</span><span class="sxs-lookup"><span data-stu-id="ee2db-213">Multi-sampling is a powerful tool and the backbone of many modern visual effects.</span></span>

## <a name="next-steps"></a><span data-ttu-id="ee2db-214">Дальнейшие шаги</span><span class="sxs-lookup"><span data-stu-id="ee2db-214">Next steps</span></span>

<span data-ttu-id="ee2db-215">Надеюсь, вы уже знакомы с DirectX 11at на этом этапе и готовы приступить к работе над проектом.</span><span class="sxs-lookup"><span data-stu-id="ee2db-215">Hopefully, you're comfortable with DirectX 11at this point and are ready to start working on your project.</span></span> <span data-ttu-id="ee2db-216">Ниже приведены ссылки на другие вопросы, которые могут возникнуть при разработке с помощью DirectX и C++.</span><span class="sxs-lookup"><span data-stu-id="ee2db-216">Here are some links to help answer other questions you may have about development with DirectX and C++:</span></span>

-   <span data-ttu-id="ee2db-217">[Разработка игр](/previous-versions/windows/apps/hh452744(v=win.10))</span><span class="sxs-lookup"><span data-stu-id="ee2db-217">[Developing games](/previous-versions/windows/apps/hh452744(v=win.10))</span></span>
-   <span data-ttu-id="ee2db-218">[Использование средств Visual Studio для программирования игр DirectX](/previous-versions/windows/apps/dn166877(v=win.10))</span><span class="sxs-lookup"><span data-stu-id="ee2db-218">[Use Visual Studio tools for DirectX game programming](/previous-versions/windows/apps/dn166877(v=win.10))</span></span>
-   <span data-ttu-id="ee2db-219">[Разработка игр DirectX и примеры пошаговых руководств](/previous-versions/windows/apps/hh465149(v=win.10))</span><span class="sxs-lookup"><span data-stu-id="ee2db-219">[DirectX game development and sample walkthroughs](/previous-versions/windows/apps/hh465149(v=win.10))</span></span>
-   <span data-ttu-id="ee2db-220">[Дополнительные ресурсы по программированию игр](/previous-versions/windows/apps/dn194515(v=win.10))</span><span class="sxs-lookup"><span data-stu-id="ee2db-220">[Additional game programming resources](/previous-versions/windows/apps/dn194515(v=win.10))</span></span>

## <a name="related-topics"></a><span data-ttu-id="ee2db-221">См. также</span><span class="sxs-lookup"><span data-stu-id="ee2db-221">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ee2db-222">Работа с ресурсами устройств DirectX</span><span class="sxs-lookup"><span data-stu-id="ee2db-222">Work with DirectX device resources</span></span>](work-with-dxgi.md)
</dt> <dt>

[<span data-ttu-id="ee2db-223">Общие сведения о конвейере визуализации Direct3D 11</span><span class="sxs-lookup"><span data-stu-id="ee2db-223">Understand the Direct3D 11 rendering pipeline</span></span>](understand-the-directx-11-2-graphics-pipeline.md)
</dt> </dl>

 

 