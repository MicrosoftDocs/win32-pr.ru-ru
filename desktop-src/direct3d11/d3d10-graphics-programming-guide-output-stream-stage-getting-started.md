---
title: Начало работы с этапом Stream-Output
description: В этом разделе описывается использование шейдера Geometry с стадией вывода потока.
ms.assetid: 37146486-5922-4833-850c-cc4a51de0957
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 909b3ba37e8b80201a4afc3e5bf18f016fed38a0
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104984029"
---
# <a name="getting-started-with-the-stream-output-stage"></a><span data-ttu-id="10bbf-103">Начало работы с этапом Stream-Output</span><span class="sxs-lookup"><span data-stu-id="10bbf-103">Getting Started with the Stream-Output Stage</span></span>

<span data-ttu-id="10bbf-104">В этом разделе описывается использование шейдера Geometry с стадией вывода потока.</span><span class="sxs-lookup"><span data-stu-id="10bbf-104">This section describes how to use a geometry shader with the stream output stage.</span></span>

## <a name="compile-a-geometry-shader"></a><span data-ttu-id="10bbf-105">Компиляция шейдера Geometry</span><span class="sxs-lookup"><span data-stu-id="10bbf-105">Compile a Geometry Shader</span></span>

<span data-ttu-id="10bbf-106">Этот шейдер геометрии (GS) вычисляет нормаль для каждого треугольника, а затем выводит положение, нормальную и текстурную координату.</span><span class="sxs-lookup"><span data-stu-id="10bbf-106">This geometry shader (GS) calculates a face normal for each triangle, and outputs position, normal and texture coordinate data.</span></span>


```
struct GSPS_INPUT
{
    float4 Pos : SV_POSITION;
    float3 Norm : TEXCOORD0;
    float2 Tex : TEXCOORD1;
};

[maxvertexcount(12)]
void GS( triangle GSPS_INPUT input[3], inout TriangleStream<GSPS_INPUT> TriStream )
{
    GSPS_INPUT output;
    
    //
    // Calculate the face normal
    //
    float3 faceEdgeA = input[1].Pos - input[0].Pos;
    float3 faceEdgeB = input[2].Pos - input[0].Pos;
    float3 faceNormal = normalize( cross(faceEdgeA, faceEdgeB) );
    float3 ExplodeAmt = faceNormal*Explode;
    
    //
    // Calculate the face center
    //
    float3 centerPos = (input[0].Pos.xyz + input[1].Pos.xyz + input[2].Pos.xyz)/3.0;
    float2 centerTex = (input[0].Tex + input[1].Tex + input[2].Tex)/3.0;
    centerPos += faceNormal*Explode;
    
    //
    // Output the pyramid
    //
    for( int i=0; i<3; i++ )
    {
        output.Pos = input[i].Pos + float4(ExplodeAmt,0);
        output.Pos = mul( output.Pos, View );
        output.Pos = mul( output.Pos, Projection );
        output.Norm = input[i].Norm;
        output.Tex = input[i].Tex;
        TriStream.Append( output );
        
        int iNext = (i+1)%3;
        output.Pos = input[iNext].Pos + float4(ExplodeAmt,0);
        output.Pos = mul( output.Pos, View );
        output.Pos = mul( output.Pos, Projection );
        output.Norm = input[iNext].Norm;
        output.Tex = input[iNext].Tex;
        TriStream.Append( output );
        
        output.Pos = float4(centerPos,1) + float4(ExplodeAmt,0);
        output.Pos = mul( output.Pos, View );
        output.Pos = mul( output.Pos, Projection );
        output.Norm = faceNormal;
        output.Tex = centerTex;
        TriStream.Append( output );
        
        TriStream.RestartStrip();
    }
    
    for( int i=2; i>=0; i-- )
    {
        output.Pos = input[i].Pos + float4(ExplodeAmt,0);
        output.Pos = mul( output.Pos, View );
        output.Pos = mul( output.Pos, Projection );
        output.Norm = -input[i].Norm;
        output.Tex = input[i].Tex;
        TriStream.Append( output );
    }
    TriStream.RestartStrip();
}
```



<span data-ttu-id="10bbf-107">Учитывая этот код, рассмотрите, что шейдер Geometry похож на вершину или шейдер пикселей, но со следующими исключениями: типом, возвращаемым функцией, объявлением входных параметров и встроенной функцией.</span><span class="sxs-lookup"><span data-stu-id="10bbf-107">Keeping that code in mind, consider that a geometry shader looks much like a vertex or pixel shader, but with the following exceptions: the type returned by the function, the input parameter declarations, and the intrinsic function.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="10bbf-108">Элемент</span><span class="sxs-lookup"><span data-stu-id="10bbf-108">Item</span></span></th>
<th><span data-ttu-id="10bbf-109">Описание</span><span class="sxs-lookup"><span data-stu-id="10bbf-109">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="10bbf-110"><span id="Function_return_type"></span><span id="function_return_type"></span><span id="FUNCTION_RETURN_TYPE"></span>Тип возвращаемого функцией значения</span><span class="sxs-lookup"><span data-stu-id="10bbf-110"><span id="Function_return_type"></span><span id="function_return_type"></span><span id="FUNCTION_RETURN_TYPE"></span>Function return type</span></span><br/></td>
<td><span data-ttu-id="10bbf-111">Тип возвращаемых функцией функций выполняет одно действие, объявляет максимальное количество вершин, которые могут выводиться шейдером.</span><span class="sxs-lookup"><span data-stu-id="10bbf-111">The function return type does one thing, declares the maximum number of vertices that can be output by the shader.</span></span> <span data-ttu-id="10bbf-112">В этом случае <span data-codelanguage=""></span>
</span><span class="sxs-lookup"><span data-stu-id="10bbf-112">In this case, <span data-codelanguage=""></span>
</span></span><table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><pre><code>maxvertexcount(12)</code></pre></td>
</tr>
</tbody>
</table>

<span data-ttu-id="10bbf-113">Определяет, что выходное значение должно быть не более 12 вершин.</span><span class="sxs-lookup"><span data-stu-id="10bbf-113">defines the output to be a maximum of 12 vertices.</span></span></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="10bbf-114"><span id="Input_parameter_declarations"></span><span id="input_parameter_declarations"></span><span id="INPUT_PARAMETER_DECLARATIONS"></span>Объявления входных параметров</span><span class="sxs-lookup"><span data-stu-id="10bbf-114"><span id="Input_parameter_declarations"></span><span id="input_parameter_declarations"></span><span id="INPUT_PARAMETER_DECLARATIONS"></span>Input parameter declarations</span></span></p></td>
<td><p><span data-ttu-id="10bbf-115">Эта функция принимает два входных параметра:</span><span class="sxs-lookup"><span data-stu-id="10bbf-115">This function takes two input parameters:</span></span></p>
<div class="code">
<span data-codelanguage=""></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><pre><code>triangle GSPS_INPUT input[3] , inout TriangleStream<GSPS_INPUT> TriStream</code></pre></td>
</tr>
</tbody>
</table>

</div>
<p><span data-ttu-id="10bbf-116">Первый параметр — это массив вершин (3 в данном случае), определенный структурой GSPS_INPUT (который определяет данные на вершину как положение, нормальную и координату текстуры).</span><span class="sxs-lookup"><span data-stu-id="10bbf-116">The first parameter is an array of vertices (3 in this case) defined by a GSPS_INPUT structure (which defines per-vertex data as a position, a normal and a texture coordinate).</span></span> <span data-ttu-id="10bbf-117">Первый параметр также использует ключевое слово треугольника, которое означает, что этап входного ассемблера должен выводить данные в шейдер Geometry как один из примитивных типов треугольников (список треугольников или полоса треугольников).</span><span class="sxs-lookup"><span data-stu-id="10bbf-117">The first parameter also uses the triangle keyword, which means the input assembler stage must output data to the geometry shader as one of the triangle primitive types (triangle list or triangle strip).</span></span></p>
<p><span data-ttu-id="10bbf-118">Вторым параметром является поток треугольника, определяемый типом Трианглестреам <GSPS_INPUT> .</span><span class="sxs-lookup"><span data-stu-id="10bbf-118">The second parameter is a triangle stream defined by the type TriangleStream<GSPS_INPUT>.</span></span> <span data-ttu-id="10bbf-119">Это означает, что параметр является массивом треугольников, каждый из которых состоит из трех вершин (которые содержат данные из членов GSPS_INPUT).</span><span class="sxs-lookup"><span data-stu-id="10bbf-119">This means the parameter is an array of triangles, each of which is made up of three vertices (that contain the data from the members of GSPS_INPUT).</span></span></p>
<p><span data-ttu-id="10bbf-120">Используйте ключевые слова треугольника и трианглестреам для обнаружения отдельных треугольников или потока треугольников в GS.</span><span class="sxs-lookup"><span data-stu-id="10bbf-120">Use the triangle and trianglestream keywords to identify individual triangles or a stream of triangles in a GS.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="10bbf-121"><span id="Intrinsic_function"></span><span id="intrinsic_function"></span><span id="INTRINSIC_FUNCTION"></span>Встроенная функция</span><span class="sxs-lookup"><span data-stu-id="10bbf-121"><span id="Intrinsic_function"></span><span id="intrinsic_function"></span><span id="INTRINSIC_FUNCTION"></span>Intrinsic function</span></span></p></td>
<td><p><span data-ttu-id="10bbf-122">Строки кода в функции шейдера используют встроенные функции Common-Shader-Core HLSL, за исключением последних двух строк, которые вызывают Append и Рестартстрип.</span><span class="sxs-lookup"><span data-stu-id="10bbf-122">The lines of code in the shader function use common-shader-core HLSL intrinsic functions except the last two lines, which call Append and RestartStrip.</span></span> <span data-ttu-id="10bbf-123">Эти функции доступны только для шейдера Geometry.</span><span class="sxs-lookup"><span data-stu-id="10bbf-123">These functions are only available to a geometry shader.</span></span> <span data-ttu-id="10bbf-124">Append информирует шейдер геометрии о добавлении выходных данных к текущей полосе. Рестартстрип создает новую ленту-примитив.</span><span class="sxs-lookup"><span data-stu-id="10bbf-124">Append informs the geometry shader to append the output to the current strip; RestartStrip creates a new primitive strip.</span></span> <span data-ttu-id="10bbf-125">Новая полоса создается неявно при каждом вызове этапа GS.</span><span class="sxs-lookup"><span data-stu-id="10bbf-125">A new strip is implicitly created in every invocation of the GS stage.</span></span></p></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="10bbf-126">Остальная часть шейдера очень похожа на вершину или шейдер пикселей.</span><span class="sxs-lookup"><span data-stu-id="10bbf-126">The rest of the shader looks very similar to a vertex or pixel shader.</span></span> <span data-ttu-id="10bbf-127">Шейдер геометрии использует структуру для объявления входных параметров и помечает элемент расположения с помощью \_ семантики позиций SV, чтобы сообщить оборудованию о том, что это данные о позиционировании.</span><span class="sxs-lookup"><span data-stu-id="10bbf-127">The geometry shader uses a structure to declare input parameters and marks the position member with the SV\_POSITION semantic to tell the hardware that this is positional data.</span></span> <span data-ttu-id="10bbf-128">Входная структура определяет другие два входных параметра как координаты текстуры (хотя один из них будет содержать нормальную часть).</span><span class="sxs-lookup"><span data-stu-id="10bbf-128">The input structure identifies the other two input parameters as texture coordinates (even though one of them will contain a face normal).</span></span> <span data-ttu-id="10bbf-129">При желании можно использовать собственную пользовательскую семантику для обычных лиц.</span><span class="sxs-lookup"><span data-stu-id="10bbf-129">You could use your own custom semantic for the face normal if you prefer.</span></span>

<span data-ttu-id="10bbf-130">Разработала шейдер Geometry, вызовите [**D3DCompile**](/windows/desktop/direct3dhlsl/d3dcompile) для компиляции, как показано в следующем примере кода.</span><span class="sxs-lookup"><span data-stu-id="10bbf-130">Having designed the geometry shader, call [**D3DCompile**](/windows/desktop/direct3dhlsl/d3dcompile) to compile as shown in the following code example.</span></span>


```
DWORD dwShaderFlags = D3DCOMPILE_ENABLE_STRICTNESS;
ID3DBlob** ppShader;

D3DCompile( pSrcData, sizeof( pSrcData ), 
  "Tutorial13.fx", NULL, NULL, "GS", "gs_4_0", 
  dwShaderFlags, 0, &ppShader, NULL );
```



<span data-ttu-id="10bbf-131">Точно так же, как шейдеры вершин и пикселей, необходим флаг шейдера, указывающий компилятору, каким образом должен компилироваться шейдер (для отладки, оптимизирована для ускорения и т. д.), функцию точки входа и модель шейдера для проверки.</span><span class="sxs-lookup"><span data-stu-id="10bbf-131">Just like vertex and pixel shaders, you need a shader flag to tell the compiler how you want the shader compiled (for debugging, optimized for speed, and so on), the entry point function, and the shader model to validate against.</span></span> <span data-ttu-id="10bbf-132">В этом примере создается шейдер Geometry, построенный на основе файла Tutorial13. FX, с помощью функции GS.</span><span class="sxs-lookup"><span data-stu-id="10bbf-132">This example creates a geometry shader built from the Tutorial13.fx file, by using the GS function.</span></span> <span data-ttu-id="10bbf-133">Шейдер компилируется для модели шейдеров 4,0.</span><span class="sxs-lookup"><span data-stu-id="10bbf-133">The shader is compiled for shader model 4.0.</span></span>

## <a name="create-a-geometry-shader-object-with-stream-output"></a><span data-ttu-id="10bbf-134">Создание объекта Geometry-Shader с выходными данными потока</span><span class="sxs-lookup"><span data-stu-id="10bbf-134">Create a Geometry-Shader Object with Stream Output</span></span>

<span data-ttu-id="10bbf-135">Когда вы узнаете, что вы будете выполнять потоковую передачу данных из геометрии и успешно откомпилирован шейдер, следующим шагом является вызов [**ID3D11Device:: креатежеометришадервисстреамаутпут**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-creategeometryshaderwithstreamoutput) для создания объекта шейдера Geometry.</span><span class="sxs-lookup"><span data-stu-id="10bbf-135">Once you know that you will be streaming the data from the geometry, and you have successfully compiled the shader, the next step is to call [**ID3D11Device::CreateGeometryShaderWithStreamOutput**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-creategeometryshaderwithstreamoutput) to create the geometry shader object.</span></span>

<span data-ttu-id="10bbf-136">Но сначала необходимо объявить входную сигнатуру Steam (SO) на этапе вывода.</span><span class="sxs-lookup"><span data-stu-id="10bbf-136">But first, you need to declare the steam output (SO) stage input signature.</span></span> <span data-ttu-id="10bbf-137">Эта сигнатура соответствует или проверяет выходные данные GS и входные данные во время создания объекта.</span><span class="sxs-lookup"><span data-stu-id="10bbf-137">This signature matches or validates the GS outputs and the SO inputs at the time of object creation.</span></span> <span data-ttu-id="10bbf-138">Следующий код является примером объявления SO.</span><span class="sxs-lookup"><span data-stu-id="10bbf-138">The following code is an example of the SO declaration.</span></span>


```
D3D11_SO_DECLARATION_ENTRY pDecl[] =
{
    // semantic name, semantic index, start component, component count, output slot
    { "SV_POSITION", 0, 0, 4, 0 },   // output all components of position
    { "TEXCOORD0", 0, 0, 3, 0 },     // output the first 3 of the normal
    { "TEXCOORD1", 0, 0, 2, 0 },     // output the first 2 texture coordinates
};

D3D11Device->CreateGeometryShaderWithStreamOut( pShaderBytecode, ShaderBytecodesize, pDecl, 
    sizeof(pDecl), NULL, 0, 0, NULL, &pStreamOutGS );
```



<span data-ttu-id="10bbf-139">Эта функция принимает несколько параметров, включая:</span><span class="sxs-lookup"><span data-stu-id="10bbf-139">This function takes several parameters including:</span></span>

-   <span data-ttu-id="10bbf-140">Указатель на скомпилированный шейдер Geometry (или шейдер вершин, если шейдер geometry не будет присутствовать, а данные будут передаваться непосредственно из шейдера вершин).</span><span class="sxs-lookup"><span data-stu-id="10bbf-140">A pointer to the compiled geometry shader (or vertex shader if no geometry shader will be present and data will be streamed out directly from the vertex shader).</span></span> <span data-ttu-id="10bbf-141">Сведения о том, как получить этот указатель, см. в разделе [Получение указателя на скомпилированный шейдер](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-using-shaders-10).</span><span class="sxs-lookup"><span data-stu-id="10bbf-141">For information about how to get this pointer, see [Getting a Pointer to a Compiled Shader](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-using-shaders-10).</span></span>
-   <span data-ttu-id="10bbf-142">Указатель на массив объявлений, описывающих входные данные для этапа вывода потока.</span><span class="sxs-lookup"><span data-stu-id="10bbf-142">A pointer to an array of declarations that describe the input data for the stream output stage.</span></span> <span data-ttu-id="10bbf-143">(См. раздел [**D3D11 \_ so, \_ \_ запись объявления**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_so_declaration_entry).) Можно предоставить до 64 объявлений, по одному для каждого типа элементов, которые будут выводиться из этого этапа.</span><span class="sxs-lookup"><span data-stu-id="10bbf-143">(See [**D3D11\_SO\_DECLARATION\_ENTRY**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_so_declaration_entry).) You can supply up to 64 declarations, one for each different type of element to be output from the SO stage.</span></span> <span data-ttu-id="10bbf-144">Массив записей объявлений описывает макет данных независимо от того, должен ли быть привязан только один буфер или несколько буферов для выходного потока.</span><span class="sxs-lookup"><span data-stu-id="10bbf-144">The array of declaration entries describes the data layout regardless of whether only a single buffer or multiple buffers are to be bound for stream output.</span></span>
-   <span data-ttu-id="10bbf-145">Количество элементов, записанных на этом этапе.</span><span class="sxs-lookup"><span data-stu-id="10bbf-145">The number of elements that are written out by the SO stage.</span></span>
-   <span data-ttu-id="10bbf-146">Указатель на созданный объект шейдера Geometry (см. [**ID3D11GeometryShader**](/windows/win32/api/d3d11/nn-d3d11-id3d11geometryshader)).</span><span class="sxs-lookup"><span data-stu-id="10bbf-146">A pointer to the geometry shader object that is created (see [**ID3D11GeometryShader**](/windows/win32/api/d3d11/nn-d3d11-id3d11geometryshader)).</span></span>

<span data-ttu-id="10bbf-147">В этой ситуации буфер STRIDE имеет значение NULL, индекс потока, отправляемого в средство программной прорисовки, равен 0, а интерфейс компоновки класса имеет значение NULL.</span><span class="sxs-lookup"><span data-stu-id="10bbf-147">In this situation, the buffer stride is NULL, the index of the stream to be sent to the rasterizer is 0, and the class linkage interface is NULL.</span></span>

<span data-ttu-id="10bbf-148">В объявлении вывода потока определяется способ, которым данные записываются в буферный ресурс.</span><span class="sxs-lookup"><span data-stu-id="10bbf-148">The stream output declaration defines the way that data is written to a buffer resource.</span></span> <span data-ttu-id="10bbf-149">В объявление вывода можно добавить столько компонентов, сколько необходимо.</span><span class="sxs-lookup"><span data-stu-id="10bbf-149">You can add as many components as you want to the output declaration.</span></span> <span data-ttu-id="10bbf-150">Используйте этот этап для записи в один буферный ресурс или несколько ресурсов буфера.</span><span class="sxs-lookup"><span data-stu-id="10bbf-150">Use the SO stage to write to a single buffer resource or many buffer resources.</span></span> <span data-ttu-id="10bbf-151">Для одного буфера этот этап может записывать множество различных элементов на вершину.</span><span class="sxs-lookup"><span data-stu-id="10bbf-151">For a single buffer, the SO stage can write many different elements per-vertex.</span></span> <span data-ttu-id="10bbf-152">Для нескольких буферов такой этап может записывать только один элемент данных на вершину в каждый буфер.</span><span class="sxs-lookup"><span data-stu-id="10bbf-152">For multiple buffers, the SO stage can only write a single element of per-vertex data to each buffer.</span></span>

<span data-ttu-id="10bbf-153">Чтобы использовать этот этап без использования шейдера Geometry, вызовите [**ID3D11Device:: креатежеометришадервисстреамаутпут**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-creategeometryshaderwithstreamoutput) и передайте указатель на шейдер вершин в параметр *пшадербитекоде* .</span><span class="sxs-lookup"><span data-stu-id="10bbf-153">To use the SO stage without using a geometry shader, call [**ID3D11Device::CreateGeometryShaderWithStreamOutput**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-creategeometryshaderwithstreamoutput) and pass a pointer to a vertex shader to the *pShaderBytecode* parameter.</span></span>

## <a name="set-the-output-targets"></a><span data-ttu-id="10bbf-154">Задание выходных целевых объектов</span><span class="sxs-lookup"><span data-stu-id="10bbf-154">Set the Output Targets</span></span>

<span data-ttu-id="10bbf-155">Последним шагом является установка этих буферов.</span><span class="sxs-lookup"><span data-stu-id="10bbf-155">The last step is to set the SO stage buffers.</span></span> <span data-ttu-id="10bbf-156">Данные можно передавать в один или несколько буферов в памяти для последующего использования.</span><span class="sxs-lookup"><span data-stu-id="10bbf-156">Data can be streamed into one or more buffers in memory for use later.</span></span> <span data-ttu-id="10bbf-157">В следующем коде показано, как создать один буфер, который можно использовать для данных вершин, а также для потоковой передачи данных в.</span><span class="sxs-lookup"><span data-stu-id="10bbf-157">The following code shows how to create a single buffer that can be used for vertex data, as well as for the SO stage to stream data into.</span></span>


```
ID3D11Buffer *m_pBuffer;
int m_nBufferSize = 1000000;

D3D11_BUFFER_DESC bufferDesc =
{
    m_nBufferSize,
    D3D11_USAGE_DEFAULT,
    D3D11_BIND_STREAM_OUTPUT,
    0,
    0,
    0
};
D3D11Device->CreateBuffer( &bufferDesc, NULL, &m_pBuffer );
```



<span data-ttu-id="10bbf-158">Создайте буфер, вызвав [**ID3D11Device:: CreateBuffer**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createbuffer).</span><span class="sxs-lookup"><span data-stu-id="10bbf-158">Create a buffer by calling [**ID3D11Device::CreateBuffer**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createbuffer).</span></span> <span data-ttu-id="10bbf-159">В этом примере показано использование по умолчанию, что типично для ресурса буфера, который должен обновляться очень часто, чем ЦП.</span><span class="sxs-lookup"><span data-stu-id="10bbf-159">This example illustrates default usage, which is typical for a buffer resource that is expected to be updated fairly frequently by the CPU.</span></span> <span data-ttu-id="10bbf-160">Флаг привязки определяет этап конвейера, к которому может быть привязан ресурс.</span><span class="sxs-lookup"><span data-stu-id="10bbf-160">The binding flag identifies the pipeline stage that the resource can be bound to.</span></span> <span data-ttu-id="10bbf-161">Все ресурсы, используемые на этом этапе, также должны создаваться с флагом привязки \_ D3D10 \_ \_ Output Stream.</span><span class="sxs-lookup"><span data-stu-id="10bbf-161">Any resource used by the SO stage must also be created with the bind flag D3D10\_BIND\_STREAM\_OUTPUT.</span></span>

<span data-ttu-id="10bbf-162">После успешного создания буфера задайте для него текущее устройство, вызвав [**ссылку ID3D11DeviceContext:: сосеттаржетс**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-sosettargets):</span><span class="sxs-lookup"><span data-stu-id="10bbf-162">Once the buffer is successfully created, set it to the current device by calling [**ID3D11DeviceContext::SOSetTargets**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-sosettargets):</span></span>


```
UINT offset[1] = 0;
D3D11Device->SOSetTargets( 1, &m_pBuffer, offset );
```



<span data-ttu-id="10bbf-163">Этот вызов принимает количество буферов, указатель на буферы и массив смещений (по одному смещению в каждый буфер, указывающий, откуда начать запись данных).</span><span class="sxs-lookup"><span data-stu-id="10bbf-163">This call takes the number of buffers, a pointer to the buffers, and an array of offsets (one offset into each of the buffers that indicates where to begin writing data).</span></span> <span data-ttu-id="10bbf-164">Данные будут записываться в эти буферы потокового вывода при вызове функции Draw.</span><span class="sxs-lookup"><span data-stu-id="10bbf-164">Data will be written to these streaming-output buffers when a draw function is called.</span></span> <span data-ttu-id="10bbf-165">Внутренняя переменная отслеживает позицию, с которой начинается запись данных в буферы потокового вывода, и эти переменные будут по-прежнему увеличиваться до тех пор, пока не будет вызвана [**сосеттаржетс**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-sosettargets) , и указано новое значение смещения.</span><span class="sxs-lookup"><span data-stu-id="10bbf-165">An internal variable keeps track of the position for where to begin writing data to the streaming-output buffers, and that variables will continue to increment until [**SOSetTargets**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-sosettargets) is called again and a new offset value is specified.</span></span>

<span data-ttu-id="10bbf-166">Все данные, записываемые в целевые буферы, будут содержать 32-битные значения.</span><span class="sxs-lookup"><span data-stu-id="10bbf-166">All data written out to the target buffers will be 32-bit values.</span></span>

## <a name="related-topics"></a><span data-ttu-id="10bbf-167">См. также</span><span class="sxs-lookup"><span data-stu-id="10bbf-167">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="10bbf-168">Стадия вывода потока</span><span class="sxs-lookup"><span data-stu-id="10bbf-168">Stream-Output Stage</span></span>](d3d10-graphics-programming-guide-output-stream-stage.md)
</dt> </dl>

 

