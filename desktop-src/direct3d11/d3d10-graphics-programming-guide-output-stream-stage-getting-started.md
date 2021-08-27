---
title: Начало работы с этапом Stream-Output
description: В этом разделе описывается использование шейдера Geometry с стадией вывода потока.
ms.assetid: 37146486-5922-4833-850c-cc4a51de0957
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5f00b469b28601322358f348de98354f15263483
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2021
ms.locfileid: "122621880"
---
# <a name="getting-started-with-the-stream-output-stage"></a>Начало работы с этапом Stream-Output

В этом разделе описывается использование шейдера Geometry с стадией вывода потока.

## <a name="compile-a-geometry-shader"></a>Компиляция шейдера Geometry

Этот шейдер геометрии (GS) вычисляет нормаль для каждого треугольника, а затем выводит положение, нормальную и текстурную координату.


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



Учитывая этот код, рассмотрите, что шейдер Geometry похож на вершину или шейдер пикселей, но со следующими исключениями: типом, возвращаемым функцией, объявлением входных параметров и встроенной функцией.



<table>
<colgroup>
<col  />
<col  />
</colgroup>
<thead>
<tr class="header">
<th>Элемент</th>
<th>Описание:</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span id="Function_return_type"></span><span id="function_return_type"></span><span id="FUNCTION_RETURN_TYPE"></span>Тип возвращаемого функцией значения<br/></td>
<td>Тип возвращаемых функцией функций выполняет одно действие, объявляет максимальное количество вершин, которые могут выводиться шейдером. В этом случае <span data-codelanguage=""></span>
<table>
<colgroup>
<col  />
</colgroup>
<tbody>
<tr class="odd">
<td><pre><code>maxvertexcount(12)</code></pre></td>
</tr>
</tbody>
</table>

Определяет, что выходное значение должно быть не более 12 вершин.</td>
</tr>
<tr class="even">
<td><p><span id="Input_parameter_declarations"></span><span id="input_parameter_declarations"></span><span id="INPUT_PARAMETER_DECLARATIONS"></span>Объявления входных параметров</p></td>
<td><p>Эта функция принимает два входных параметра:</p>
<div class="code">
<span data-codelanguage=""></span>
<table>
<colgroup>
<col  />
</colgroup>
<tbody>
<tr class="odd">
<td><pre><code>triangle GSPS_INPUT input[3] , inout TriangleStream&lt;GSPS_INPUTT&gt; TriStream</code></pre></td>
</tr>
</tbody>
</table>

</div>
<p>Первый параметр — это массив вершин (3 в данном случае), определенный структурой GSPS_INPUT (который определяет данные на вершину как положение, нормальную и координату текстуры). Первый параметр также использует ключевое слово треугольника, которое означает, что этап входного ассемблера должен выводить данные в шейдер Geometry как один из примитивных типов треугольников (список треугольников или полоса треугольников).</p>
<p>Вторым параметром является поток треугольника, определяемый типом Трианглестреам &lt; GSPS_INPUTT &gt; . Это означает, что параметр является массивом треугольников, каждый из которых состоит из трех вершин (которые содержат данные из членов GSPS_INPUT).</p>
<p>Используйте ключевые слова треугольника и трианглестреам для обнаружения отдельных треугольников или потока треугольников в GS.</p></td>
</tr>
<tr class="odd">
<td><p><span id="Intrinsic_function"></span><span id="intrinsic_function"></span><span id="INTRINSIC_FUNCTION"></span>Встроенная функция</p></td>
<td><p>Строки кода в функции шейдера используют встроенные функции Common-Shader-Core HLSL, за исключением последних двух строк, которые вызывают Append и Рестартстрип. Эти функции доступны только для шейдера Geometry. Append информирует шейдер геометрии о добавлении выходных данных к текущей полосе. Рестартстрип создает новую ленту-примитив. Новая полоса создается неявно при каждом вызове этапа GS.</p></td>
</tr>
</tbody>
</table>



 

Остальная часть шейдера очень похожа на вершину или шейдер пикселей. Шейдер геометрии использует структуру для объявления входных параметров и помечает элемент расположения с помощью \_ семантики позиций SV, чтобы сообщить оборудованию о том, что это данные о позиционировании. Входная структура определяет другие два входных параметра как координаты текстуры (хотя один из них будет содержать нормальную часть). При желании можно использовать собственную пользовательскую семантику для обычных лиц.

Разработала шейдер Geometry, вызовите [**D3DCompile**](/windows/desktop/direct3dhlsl/d3dcompile) для компиляции, как показано в следующем примере кода.


```
DWORD dwShaderFlags = D3DCOMPILE_ENABLE_STRICTNESS;
ID3DBlob** ppShader;

D3DCompile( pSrcData, sizeof( pSrcData ), 
  "Tutorial13.fx", NULL, NULL, "GS", "gs_4_0", 
  dwShaderFlags, 0, &ppShader, NULL );
```



Точно так же, как шейдеры вершин и пикселей, необходим флаг шейдера, указывающий компилятору, каким образом должен компилироваться шейдер (для отладки, оптимизирована для ускорения и т. д.), функцию точки входа и модель шейдера для проверки. В этом примере создается шейдер Geometry, построенный на основе файла Tutorial13. FX, с помощью функции GS. Шейдер компилируется для модели шейдеров 4,0.

## <a name="create-a-geometry-shader-object-with-stream-output"></a>Создание объекта Geometry-Shader с выходными данными потока

Когда вы узнаете, что вы будете выполнять потоковую передачу данных из геометрии и успешно откомпилирован шейдер, следующим шагом является вызов [**ID3D11Device:: креатежеометришадервисстреамаутпут**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-creategeometryshaderwithstreamoutput) для создания объекта шейдера Geometry.

Но сначала необходимо объявить входную сигнатуру Steam (SO) на этапе вывода. Эта сигнатура соответствует или проверяет выходные данные GS и входные данные во время создания объекта. Следующий код является примером объявления SO.


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



Эта функция принимает несколько параметров, включая:

-   Указатель на скомпилированный шейдер Geometry (или шейдер вершин, если шейдер geometry не будет присутствовать, а данные будут передаваться непосредственно из шейдера вершин). Сведения о том, как получить этот указатель, см. в разделе [Получение указателя на скомпилированный шейдер](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-using-shaders-10).
-   Указатель на массив объявлений, описывающих входные данные для этапа вывода потока. (См. раздел [**D3D11 \_ so, \_ \_ запись объявления**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_so_declaration_entry).) Можно предоставить до 64 объявлений, по одному для каждого типа элементов, которые будут выводиться из этого этапа. Массив записей объявлений описывает макет данных независимо от того, должен ли быть привязан только один буфер или несколько буферов для выходного потока.
-   Количество элементов, записанных на этом этапе.
-   Указатель на созданный объект шейдера Geometry (см. [**ID3D11GeometryShader**](/windows/win32/api/d3d11/nn-d3d11-id3d11geometryshader)).

В этой ситуации буфер STRIDE имеет значение NULL, индекс потока, отправляемого в средство программной прорисовки, равен 0, а интерфейс компоновки класса имеет значение NULL.

В объявлении вывода потока определяется способ, которым данные записываются в буферный ресурс. В объявление вывода можно добавить столько компонентов, сколько необходимо. Используйте этот этап для записи в один буферный ресурс или несколько ресурсов буфера. Для одного буфера этот этап может записывать множество различных элементов на вершину. Для нескольких буферов такой этап может записывать только один элемент данных на вершину в каждый буфер.

Чтобы использовать этот этап без использования шейдера Geometry, вызовите [**ID3D11Device:: креатежеометришадервисстреамаутпут**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-creategeometryshaderwithstreamoutput) и передайте указатель на шейдер вершин в параметр *пшадербитекоде* .

## <a name="set-the-output-targets"></a>Задание выходных целевых объектов

Последним шагом является установка этих буферов. Данные можно передавать в один или несколько буферов в памяти для последующего использования. В следующем коде показано, как создать один буфер, который можно использовать для данных вершин, а также для потоковой передачи данных в.


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



Создайте буфер, вызвав [**ID3D11Device:: CreateBuffer**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createbuffer). В этом примере показано использование по умолчанию, что типично для ресурса буфера, который должен обновляться очень часто, чем ЦП. Флаг привязки определяет этап конвейера, к которому может быть привязан ресурс. Все ресурсы, используемые на этом этапе, также должны создаваться с флагом привязки \_ D3D10 \_ \_ Output Stream.

После успешного создания буфера задайте для него текущее устройство, вызвав [**ссылку ID3D11DeviceContext:: сосеттаржетс**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-sosettargets):


```
UINT offset[1] = 0;
D3D11Device->SOSetTargets( 1, &m_pBuffer, offset );
```



Этот вызов принимает количество буферов, указатель на буферы и массив смещений (по одному смещению в каждый буфер, указывающий, откуда начать запись данных). Данные будут записываться в эти буферы потокового вывода при вызове функции Draw. Внутренняя переменная отслеживает позицию, с которой начинается запись данных в буферы потокового вывода, и эти переменные будут по-прежнему увеличиваться до тех пор, пока не будет вызвана [**сосеттаржетс**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-sosettargets) , и указано новое значение смещения.

Все данные, записываемые в целевые буферы, будут содержать 32-битные значения.

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Стадия вывода потока](d3d10-graphics-programming-guide-output-stream-stage.md)
</dt> </dl>

 

