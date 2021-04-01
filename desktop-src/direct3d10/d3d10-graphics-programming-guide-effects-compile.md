---
description: После создания результата сначала необходимо скомпилировать код для проверки синтаксических ошибок.
ms.assetid: b8d8a0b7-b520-44e4-8691-6eb46202c092
title: Компиляция эффекта (Direct3D 10)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ab6183f2f71b07c482fa24efc4f9fed199216d75
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104262563"
---
# <a name="compile-an-effect-direct3d-10"></a><span data-ttu-id="0df92-103">Компиляция эффекта (Direct3D 10)</span><span class="sxs-lookup"><span data-stu-id="0df92-103">Compile an Effect (Direct3D 10)</span></span>

<span data-ttu-id="0df92-104">После создания результата сначала необходимо скомпилировать код для проверки синтаксических ошибок.</span><span class="sxs-lookup"><span data-stu-id="0df92-104">Once an effect has been authored, the first step is to compile the code to check for syntax problems.</span></span> <span data-ttu-id="0df92-105">Это делается путем вызова одного из API-интерфейсов компиляции (например, D3DX10CompileEffectFromFile, D3DX10CompileEffectFromResource, D3DX10CompileEffectFromMemory).</span><span class="sxs-lookup"><span data-stu-id="0df92-105">This is done by calling one of the compile APIs (like D3DX10CompileEffectFromFile, D3DX10CompileEffectFromResource, D3DX10CompileEffectFromMemory).</span></span> <span data-ttu-id="0df92-106">Эти API вызывают компилятор эффектов, fxc.exe который является компилятором, используемым для компиляции кода HLSL.</span><span class="sxs-lookup"><span data-stu-id="0df92-106">These API's invoke the effect compiler fxc.exe which is the compiler used to compile HLSL code.</span></span> <span data-ttu-id="0df92-107">Именно поэтому синтаксис кода в результате выглядит очень похожим на код HLSL (существует несколько исключений, которые будут обработаны позже).</span><span class="sxs-lookup"><span data-stu-id="0df92-107">This is why the syntax for code in an effect looks very much like HLSL code (there are a few exceptions that will be handled later).</span></span> <span data-ttu-id="0df92-108">Кстати, компилятор эффектов компилятора и HLSL (fxc.exe) находится в пакете SDK в папке служебных программ, чтобы можно было компилировать шейдер (или эффекты) в автономном режиме при выборе.</span><span class="sxs-lookup"><span data-stu-id="0df92-108">By the way, the effect compiler/hlsl compiler (fxc.exe) is in the SDK in the utilities folder so that you can compile your shaders (or effects) offline if you choose.</span></span> <span data-ttu-id="0df92-109">См. документацию по запуску компилятора из командной строки.</span><span class="sxs-lookup"><span data-stu-id="0df92-109">See the documentation for running the compiler from the command line.</span></span>

-   [<span data-ttu-id="0df92-110">Том</span><span class="sxs-lookup"><span data-stu-id="0df92-110">Includes</span></span>](#includes)
-   [<span data-ttu-id="0df92-111">Макросы</span><span class="sxs-lookup"><span data-stu-id="0df92-111">Macros</span></span>](#macros)
-   [<span data-ttu-id="0df92-112">Флаги шейдера HLSL</span><span class="sxs-lookup"><span data-stu-id="0df92-112">HLSL Shader Flags</span></span>](#hlsl-shader-flags)
-   [<span data-ttu-id="0df92-113">Флаги FX</span><span class="sxs-lookup"><span data-stu-id="0df92-113">FX Flags</span></span>](#fx-flags)
-   [<span data-ttu-id="0df92-114">Проверка ошибок</span><span class="sxs-lookup"><span data-stu-id="0df92-114">Checking Errors</span></span>](#checking-errors)
-   [<span data-ttu-id="0df92-115">См. также</span><span class="sxs-lookup"><span data-stu-id="0df92-115">Related topics</span></span>](#related-topics)

<span data-ttu-id="0df92-116">Ниже приведен пример компиляции файла эффектов (из образца BasicHLSL10).</span><span class="sxs-lookup"><span data-stu-id="0df92-116">Here's an example of compiling an effect file (from the BasicHLSL10 sample).</span></span>


```
WCHAR str[MAX_PATH];
DXUTFindDXSDKMediaFileCch( str, MAX_PATH, L"BasicHLSL10.fx" );

hr = D3DX10CompileEffectFromFile( str, NULL, NULL, "fx_4_0", 
    D3D10_SHADER_ENABLE_STRICTNESS, 0, pd3dDevice, NULL, NULL, 
    &l_pBlob_Effect, &l_pBlob_Errors, NULL );
```



## <a name="includes"></a><span data-ttu-id="0df92-117">Includes</span><span class="sxs-lookup"><span data-stu-id="0df92-117">Includes</span></span>

<span data-ttu-id="0df92-118">Один из параметров — это интерфейс include.</span><span class="sxs-lookup"><span data-stu-id="0df92-118">One parameter is an include interface.</span></span> <span data-ttu-id="0df92-119">Создайте один из них, если необходимо включить настраиваемое поведение при чтении включаемого файла.</span><span class="sxs-lookup"><span data-stu-id="0df92-119">Generate one of these if you want to include a customized behavior when reading an include file.</span></span> <span data-ttu-id="0df92-120">Это пользовательское поведение выполняется каждый раз при создании действия (использующего указатель включения) или при компиляции действия (которое использует указатель включения).</span><span class="sxs-lookup"><span data-stu-id="0df92-120">This custom behavior is executed each time an effect (that uses the include pointer) is created or when an effect (that uses the include pointer) is compiled.</span></span> <span data-ttu-id="0df92-121">Чтобы реализовать пользовательское поведение включения, создайте класс, производный от интерфейса include.</span><span class="sxs-lookup"><span data-stu-id="0df92-121">To implement customized include behavior, derive a class from the Include interface.</span></span> <span data-ttu-id="0df92-122">Это предоставляет классу два метода: Open и Close.</span><span class="sxs-lookup"><span data-stu-id="0df92-122">This provides your class two methods: Open and Close.</span></span> <span data-ttu-id="0df92-123">Реализуйте пользовательское поведение в методах Open и Close.</span><span class="sxs-lookup"><span data-stu-id="0df92-123">Implement the custom behavior in the Open and Close methods.</span></span>

## <a name="macros"></a><span data-ttu-id="0df92-124">Макросы</span><span class="sxs-lookup"><span data-stu-id="0df92-124">Macros</span></span>

<span data-ttu-id="0df92-125">Компиляция эффектов также может принимать указатель на макросы, определенные в других местах.</span><span class="sxs-lookup"><span data-stu-id="0df92-125">Effect compilation can also take a pointer to macros that are defined elsewhere.</span></span> <span data-ttu-id="0df92-126">Например, предположим, что вы изменили воздействие на BasicHLSL10, чтобы использовать два макроса: ноль и один.</span><span class="sxs-lookup"><span data-stu-id="0df92-126">For example, suppose you were to modify the effect in BasicHLSL10, to use two macros: zero and one.</span></span> <span data-ttu-id="0df92-127">Здесь показан код влияния, использующий два макроса.</span><span class="sxs-lookup"><span data-stu-id="0df92-127">The effect code that uses the two macros is shown here.</span></span>


```
if( bAnimate )
    vAnimatedPos += float4(vNormal, zero) *  
        (sin(g_fTime+5.5)+0.5)*5;
        
    Output.Diffuse.a = one;         
```



<span data-ttu-id="0df92-128">Ниже приведено объявление для двух макросов.</span><span class="sxs-lookup"><span data-stu-id="0df92-128">Here is the declaration for the two macros.</span></span>


```
D3D_SHADER_MACRO Shader_Macros[3] = { "zero", "0", "one", "1.0f", NULL, NULL };
```



<span data-ttu-id="0df92-129">Макросы — это массив макросов, заканчивающийся нулем; где каждый макрос определяется структурой [**\_ \_ макроса D3D шейдера**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro) .</span><span class="sxs-lookup"><span data-stu-id="0df92-129">The macros are a NULL terminated array of macros; where each macro is defined with a [**D3D\_SHADER\_MACRO**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro) struct.</span></span>

<span data-ttu-id="0df92-130">Наконец, измените вызов действия Compile, чтобы получить указатель на макросы.</span><span class="sxs-lookup"><span data-stu-id="0df92-130">Lastly, modify the compile effect call to take a pointer to the macros.</span></span>


```
D3DX10CreateEffectFromFile( str, Shader_Macros, NULL, 
    D3D10_SHADER_ENABLE_STRICTNESS, 0, pd3dDevice, NULL, NULL, 
    &g_pEffect10, NULL );
```



## <a name="hlsl-shader-flags"></a><span data-ttu-id="0df92-131">Флаги шейдера HLSL</span><span class="sxs-lookup"><span data-stu-id="0df92-131">HLSL Shader Flags</span></span>

<span data-ttu-id="0df92-132">Флаги шейдера определяют ограничения шейдера компилятором HLSL.</span><span class="sxs-lookup"><span data-stu-id="0df92-132">Shader flags specify shader constraints to the HLSL compiler.</span></span> <span data-ttu-id="0df92-133">Эти флаги влияют на код, созданный компилятором шейдера, в том числе:</span><span class="sxs-lookup"><span data-stu-id="0df92-133">These flags impact the code generated by the shader compiler including:</span></span>

-   <span data-ttu-id="0df92-134">Рекомендации по размеру. Оптимизируйте код.</span><span class="sxs-lookup"><span data-stu-id="0df92-134">Size considerations: optimize the code.</span></span>
-   <span data-ttu-id="0df92-135">Вопросы отладки: Включение отладочной информации, запрет управления потоком.</span><span class="sxs-lookup"><span data-stu-id="0df92-135">Debug considerations: including debug information, preventing flow control.</span></span>
-   <span data-ttu-id="0df92-136">Рекомендации по оборудованию: Цель компиляции и возможность запуска шейдера на устаревшем оборудовании.</span><span class="sxs-lookup"><span data-stu-id="0df92-136">Hardware considerations: the compile target and whether or not a shader can run on legacy hardware.</span></span>

<span data-ttu-id="0df92-137">Как правило, эти флаги могут быть логически объединены, предполагая, что не указаны две конфликтующие характеристики.</span><span class="sxs-lookup"><span data-stu-id="0df92-137">In general, these flags can be logically combined, assuming you have not specified two conflicting characteristics.</span></span> <span data-ttu-id="0df92-138">Список флагов см. в разделе [константы эффектов (Direct3D 10)](d3d10-graphics-reference-effect-constants.md).</span><span class="sxs-lookup"><span data-stu-id="0df92-138">For a listing of the flags see [Effect Constants (Direct3D 10)](d3d10-graphics-reference-effect-constants.md).</span></span>

## <a name="fx-flags"></a><span data-ttu-id="0df92-139">Флаги FX</span><span class="sxs-lookup"><span data-stu-id="0df92-139">FX Flags</span></span>

<span data-ttu-id="0df92-140">Эти флаги используются при создании эффектов для определения поведения компиляции или поведения воздействия на среду выполнения.</span><span class="sxs-lookup"><span data-stu-id="0df92-140">These flags used when creating an effect to define either compilation behavior or runtime effect behavior.</span></span> <span data-ttu-id="0df92-141">Список флагов см. в разделе [константы эффектов (Direct3D 10)](d3d10-graphics-reference-effect-constants.md).</span><span class="sxs-lookup"><span data-stu-id="0df92-141">For a listing of the flags see [Effect Constants (Direct3D 10)](d3d10-graphics-reference-effect-constants.md).</span></span>

## <a name="checking-errors"></a><span data-ttu-id="0df92-142">Проверка ошибок</span><span class="sxs-lookup"><span data-stu-id="0df92-142">Checking Errors</span></span>

<span data-ttu-id="0df92-143">Если во время компиляции возникает ошибка, API возвращает интерфейс, который содержит ошибки, возвращенные компилятором влияния.</span><span class="sxs-lookup"><span data-stu-id="0df92-143">If during compilation, an error occurs, the API returns an interface which contains the errors returned from the effect compiler.</span></span> <span data-ttu-id="0df92-144">Этот интерфейс называется ID3D10Blob.</span><span class="sxs-lookup"><span data-stu-id="0df92-144">This interface is called ID3D10Blob.</span></span> <span data-ttu-id="0df92-145">Однако он не читается напрямую, но возвращает указатель на буфер, содержащий данные (которые являются строкой), можно увидеть любые ошибки компиляции.</span><span class="sxs-lookup"><span data-stu-id="0df92-145">It is not directly readable, however, by returning a pointer to the buffer that contains the data (which is a string), you can see any compilation errors.</span></span>

<span data-ttu-id="0df92-146">В этом примере в результат Басичлсл. FX было введено сообщение об ошибке, которое дважды копирует объявление первой переменной.</span><span class="sxs-lookup"><span data-stu-id="0df92-146">In this example, an error was introduced into the BasicHLSL.fx effect by copying the first variable declaration twice.</span></span>


```
//-------------------------------------------------------------------
// Global variables
//-------------------------------------------------------------------
float4 g_MaterialAmbientColor;      // Material's ambient color

// Declare the same variable twice
float4 g_MaterialAmbientColor;      // Material's ambient color
```



<span data-ttu-id="0df92-147">Эта ошибка привела к возвращению компилятором следующей ошибки, как показано на следующем снимке экрана окна контрольных значений в Microsoft Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="0df92-147">This error caused the compiler to return the following error, as shown in the following screen shot of the watch window in Microsoft Visual Studio.</span></span>

![снимок экрана окна "контрольные значения Visual Studio"](images/effect-compile-errors-2.jpg)

<span data-ttu-id="0df92-149">Так как ошибка возвращается в указатель ЛПВОИД, приведите ее к символьной строке в окне Контрольные значения.</span><span class="sxs-lookup"><span data-stu-id="0df92-149">Since the error is returned in a LPVOID pointer, cast it to a character string in the watch window.</span></span>

<span data-ttu-id="0df92-150">Ниже приведен код, который используется для возврата ошибки из-за неудачной компиляции.</span><span class="sxs-lookup"><span data-stu-id="0df92-150">Here is the code used to return the error from the failed compile.</span></span>


```
// Read the D3DX effect file
WCHAR str[MAX_PATH];
ID3D10Blob* l_pBlob_Effect = NULL;
ID3D10Blob* l_pBlob_Errors = NULL;
hr = DXUTFindDXSDKMediaFileCch( str, MAX_PATH, L"BasicHLSL10.fx" );
hr = D3DX10CompileEffectFromFile( str, NULL, NULL, 
    D3D10_SHADER_ENABLE_STRICTNESS, 0, NULL, 
    &l_pBlob_Effect, &l_pBlob_Errors );

LPVOID l_pError = NULL;
if( l_pBlob_Errors )
{
    l_pError = l_pBlob_Errors->GetBufferPointer();
    // then cast to a char* to see it in the locals window
}
```



## <a name="related-topics"></a><span data-ttu-id="0df92-151">См. также</span><span class="sxs-lookup"><span data-stu-id="0df92-151">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0df92-152">Отрисовка влияния (Direct3D 10)</span><span class="sxs-lookup"><span data-stu-id="0df92-152">Rendering an Effect (Direct3D 10)</span></span>](d3d10-graphics-programming-guide-effects-render.md)
</dt> </dl>

 

 



