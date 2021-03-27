---
title: Компиляция результата (Direct3D 11)
description: После создания результата необходимо скомпилировать код для проверки синтаксических ошибок.
ms.assetid: 7624d55e-6466-4156-8f31-30f0d25a2883
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c3df304a7b657af19984008bd90a1be4bfe5219c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "103987627"
---
# <a name="compile-an-effect-direct3d-11"></a><span data-ttu-id="58c32-103">Компиляция результата (Direct3D 11)</span><span class="sxs-lookup"><span data-stu-id="58c32-103">Compile an Effect (Direct3D 11)</span></span>

<span data-ttu-id="58c32-104">После создания результата необходимо скомпилировать код для проверки синтаксических ошибок.</span><span class="sxs-lookup"><span data-stu-id="58c32-104">After an effect has been authored, the next step is to compile the code to check for syntax problems.</span></span>

<span data-ttu-id="58c32-105">Это можно сделать, вызвав один из API-интерфейсов компиляции ([**D3DX11CompileFromFile**](d3dx11compilefromfile.md), [**D3DX11CompileFromMemory**](d3dx11compilefrommemory.md)или [**D3DX11CompileFromResource**](d3dx11compilefromresource.md) ).</span><span class="sxs-lookup"><span data-stu-id="58c32-105">You do so by calling one of the compile APIs ([**D3DX11CompileFromFile**](d3dx11compilefromfile.md), [**D3DX11CompileFromMemory**](d3dx11compilefrommemory.md), or [**D3DX11CompileFromResource**](d3dx11compilefromresource.md) ).</span></span> <span data-ttu-id="58c32-106">Эти API вызывают компилятор эффектов fxc.exe, который компилирует код HLSL.</span><span class="sxs-lookup"><span data-stu-id="58c32-106">These APIs invoke the effect compiler fxc.exe, which compiles HLSL code.</span></span> <span data-ttu-id="58c32-107">Именно поэтому синтаксис кода в результате выглядит очень похожим на код HLSL.</span><span class="sxs-lookup"><span data-stu-id="58c32-107">This is why the syntax for code in an effect looks very much like HLSL code.</span></span> <span data-ttu-id="58c32-108">(Существует несколько исключений, которые будут обработаны позже).</span><span class="sxs-lookup"><span data-stu-id="58c32-108">(There are a few exceptions that will be handled later).</span></span> <span data-ttu-id="58c32-109">Компилятор компилятора HLSL, fxc.exe, доступен в пакете SDK в папке Служебные программы, чтобы шейдеры (или эффекты) можно было компилировать в автономном режиме при выборе.</span><span class="sxs-lookup"><span data-stu-id="58c32-109">The effect compiler/hlsl compiler, fxc.exe, is available in the SDK in the utilities folder so that shaders (or effects) can be compiled offline if you choose.</span></span> <span data-ttu-id="58c32-110">См. документацию по запуску компилятора из командной строки.</span><span class="sxs-lookup"><span data-stu-id="58c32-110">See the documentation for running the compiler from the command line.</span></span>

-   [<span data-ttu-id="58c32-111">Пример</span><span class="sxs-lookup"><span data-stu-id="58c32-111">Example</span></span>](#example)
-   [<span data-ttu-id="58c32-112">Том</span><span class="sxs-lookup"><span data-stu-id="58c32-112">Includes</span></span>](#includes)
-   [<span data-ttu-id="58c32-113">Поиск включаемых файлов</span><span class="sxs-lookup"><span data-stu-id="58c32-113">Searching for Include Files</span></span>](#searching-for-include-files)
-   [<span data-ttu-id="58c32-114">Макросы</span><span class="sxs-lookup"><span data-stu-id="58c32-114">Macros</span></span>](#macros)
-   [<span data-ttu-id="58c32-115">Флаги шейдера HLSL</span><span class="sxs-lookup"><span data-stu-id="58c32-115">HLSL Shader Flags</span></span>](#hlsl-shader-flags)
-   [<span data-ttu-id="58c32-116">Флаги FX</span><span class="sxs-lookup"><span data-stu-id="58c32-116">FX Flags</span></span>](#fx-flags)
-   [<span data-ttu-id="58c32-117">Проверка ошибок</span><span class="sxs-lookup"><span data-stu-id="58c32-117">Checking Errors</span></span>](#checking-errors)
-   [<span data-ttu-id="58c32-118">См. также</span><span class="sxs-lookup"><span data-stu-id="58c32-118">Related topics</span></span>](#related-topics)

## <a name="example"></a><span data-ttu-id="58c32-119">Например, .</span><span class="sxs-lookup"><span data-stu-id="58c32-119">Example</span></span>

<span data-ttu-id="58c32-120">Ниже приведен пример компиляции файла эффектов.</span><span class="sxs-lookup"><span data-stu-id="58c32-120">Here's an example of compiling an effect file.</span></span>


```
WCHAR str[MAX_PATH];
DXUTFindDXSDKMediaFileCch( str, MAX_PATH, L"BasicHLSL10.fx" );

hr = D3DX11CompileFromFile( str, NULL, NULL, pFunctionName, pProfile, D3D10_SHADER_ENABLE_STRICTNESS, NULL, NULL, &pBlob, &pErrorBlob, NULL );
```



## <a name="includes"></a><span data-ttu-id="58c32-121">Includes</span><span class="sxs-lookup"><span data-stu-id="58c32-121">Includes</span></span>

<span data-ttu-id="58c32-122">Одним из параметров API-интерфейсов компиляции является интерфейс include.</span><span class="sxs-lookup"><span data-stu-id="58c32-122">One parameter of the compile APIs is an include interface.</span></span> <span data-ttu-id="58c32-123">Создайте один из них, если необходимо включить настраиваемое поведение, когда компилятор считывает включаемый файл.</span><span class="sxs-lookup"><span data-stu-id="58c32-123">Generate one of these if you want to include a customized behavior when the compiler reads an include file.</span></span> <span data-ttu-id="58c32-124">Компилятор выполняет это пользовательское поведение каждый раз при создании или компиляции влияния (которое использует указатель include).</span><span class="sxs-lookup"><span data-stu-id="58c32-124">The compiler executes this custom behavior each time it creates or compiles an effect (that uses the include pointer).</span></span> <span data-ttu-id="58c32-125">Чтобы реализовать пользовательское поведение включения, создайте класс, производный от интерфейса [**ID3DInclude**](/windows/desktop/api/D3Dcommon/nn-d3dcommon-id3dinclude) .</span><span class="sxs-lookup"><span data-stu-id="58c32-125">To implement customized include behavior, derive a class from the [**ID3DInclude**](/windows/desktop/api/D3Dcommon/nn-d3dcommon-id3dinclude) interface.</span></span> <span data-ttu-id="58c32-126">Это предоставляет классу два метода: [**Open**](/windows/desktop/api/D3DCommon/nf-d3dcommon-id3dinclude-open) и [**Close**](/windows/desktop/api/D3DCommon/nf-d3dcommon-id3dinclude-close).</span><span class="sxs-lookup"><span data-stu-id="58c32-126">This provides your class with two methods: [**Open**](/windows/desktop/api/D3DCommon/nf-d3dcommon-id3dinclude-open) and [**Close**](/windows/desktop/api/D3DCommon/nf-d3dcommon-id3dinclude-close).</span></span> <span data-ttu-id="58c32-127">Реализуйте пользовательское поведение в этих методах.</span><span class="sxs-lookup"><span data-stu-id="58c32-127">Implement the custom behavior in these methods.</span></span>

## <a name="searching-for-include-files"></a><span data-ttu-id="58c32-128">Поиск включаемых файлов</span><span class="sxs-lookup"><span data-stu-id="58c32-128">Searching for Include Files</span></span>

<span data-ttu-id="58c32-129">Указатель, переданный компилятором в параметр *ппарентдата* в метод [**Open**](/windows/desktop/api/D3DCommon/nf-d3dcommon-id3dinclude-open) обработчика include, может не указывать на контейнер, включающий \# включаемый файл, который компилятору необходимо скомпилировать в код шейдера.</span><span class="sxs-lookup"><span data-stu-id="58c32-129">The pointer that the compiler passes in the *pParentData* parameter to your include handler's [**Open**](/windows/desktop/api/D3DCommon/nf-d3dcommon-id3dinclude-open) method might not point to the container that includes the \#include file that the compiler needs to compile your shader code.</span></span> <span data-ttu-id="58c32-130">То есть компилятор может передать **значение NULL** в *ппарентдата*.</span><span class="sxs-lookup"><span data-stu-id="58c32-130">That is, the compiler might pass **NULL** in *pParentData*.</span></span> <span data-ttu-id="58c32-131">Поэтому рекомендуется выполнять поиск по своему собственному списку включаемых расположений для содержимого.</span><span class="sxs-lookup"><span data-stu-id="58c32-131">Therefore, we recommend that your include handler search its own list of include locations for content.</span></span> <span data-ttu-id="58c32-132">Обработчик include может динамически добавлять новые расположения для включения, так как они получают эти расположения в вызовах метода **Open** .</span><span class="sxs-lookup"><span data-stu-id="58c32-132">Your include handler can dynamically add new include locations as it receives those locations in calls to its **Open** method.</span></span>

<span data-ttu-id="58c32-133">В следующем примере предположим, что включаемые файлы кода шейдера хранятся в каталоге *сомевхерилсе* .</span><span class="sxs-lookup"><span data-stu-id="58c32-133">In the following example, suppose that the shader code's include files are both stored in the *somewhereelse* directory.</span></span> <span data-ttu-id="58c32-134">Когда компилятор вызывает метод [**Open**](/windows/desktop/api/D3DCommon/nf-d3dcommon-id3dinclude-open) обработчика include для открытия и чтения содержимого *сомевхерилсе \\ foo. h*, обработчик include может сохранить расположение каталога **сомевхерилсе** .</span><span class="sxs-lookup"><span data-stu-id="58c32-134">When the compiler calls the include handler's [**Open**](/windows/desktop/api/D3DCommon/nf-d3dcommon-id3dinclude-open) method to open and read the contents of *somewhereelse\\foo.h*, the include handler can save the location of the **somewhereelse** directory.</span></span> <span data-ttu-id="58c32-135">Позже, когда компилятор вызывает метод **Open** обработчика include для открытия и чтения содержимого файла *Bar. h*, обработчик include может автоматически искать в каталоге *сомевхерилсе* для *Bar. h*.</span><span class="sxs-lookup"><span data-stu-id="58c32-135">Later, when the compiler calls the include handler's **Open** method to open and read the contents of *bar.h*, the include handler can automatically search in the *somewhereelse* directory for *bar.h*.</span></span>


```
Main.hlsl:
#include "somewhereelse\foo.h"

Foo.h:
#include "bar.h"
```



## <a name="macros"></a><span data-ttu-id="58c32-136">Макросы</span><span class="sxs-lookup"><span data-stu-id="58c32-136">Macros</span></span>

<span data-ttu-id="58c32-137">Компиляция эффектов также может принимать указатель на макросы, определенные в других местах.</span><span class="sxs-lookup"><span data-stu-id="58c32-137">Effect compilation can also take a pointer to macros that are defined elsewhere.</span></span> <span data-ttu-id="58c32-138">Например, предположим, что вы хотите изменить результат в BasicHLSL10, чтобы использовать два макроса: ноль и один.</span><span class="sxs-lookup"><span data-stu-id="58c32-138">For example, suppose you want to modify the effect in BasicHLSL10, to use two macros: zero and one.</span></span> <span data-ttu-id="58c32-139">Здесь показан код влияния, использующий два макроса.</span><span class="sxs-lookup"><span data-stu-id="58c32-139">The effect code that uses the two macros is shown here.</span></span>


```
if( bAnimate )
    vAnimatedPos += float4(vNormal, zero) *  
        (sin(g_fTime+5.5)+0.5)*5;
        
    Output.Diffuse.a = one;         
```



<span data-ttu-id="58c32-140">Ниже приведено объявление для двух макросов.</span><span class="sxs-lookup"><span data-stu-id="58c32-140">Here is the declaration for the two macros.</span></span>


```
D3D10_SHADER_MACRO Shader_Macros[3] = { "zero", "0", "one", "1.0f", NULL, NULL };
```



<span data-ttu-id="58c32-141">Макросы — это массив макросов, заканчивающийся нулем; где каждый макрос определяется с помощью структуры [**\_ \_ макроса D3D10 шейдера**](/windows/desktop/api/d3dcommon/ns-d3dcommon-d3d_shader_macro) .</span><span class="sxs-lookup"><span data-stu-id="58c32-141">The macros are a NULL-terminated array of macros; where each macro is defined by using a [**D3D10\_SHADER\_MACRO**](/windows/desktop/api/d3dcommon/ns-d3dcommon-d3d_shader_macro) struct.</span></span>

<span data-ttu-id="58c32-142">Измените вызов действия Compile, чтобы получить указатель на макросы.</span><span class="sxs-lookup"><span data-stu-id="58c32-142">Modify the compile effect call to take a pointer to the macros.</span></span>


```
D3DX11CompileFromFile( str, Shader_Macros, NULL, pFunctionName, 
                       pProfile, D3D10_SHADER_ENABLE_STRICTNESS, NULL, 
                       NULL, &pBlob, &pErrorBlob, NULL );    
```



## <a name="hlsl-shader-flags"></a><span data-ttu-id="58c32-143">Флаги шейдера HLSL</span><span class="sxs-lookup"><span data-stu-id="58c32-143">HLSL Shader Flags</span></span>

<span data-ttu-id="58c32-144">Флаги шейдера определяют ограничения шейдера компилятором HLSL.</span><span class="sxs-lookup"><span data-stu-id="58c32-144">Shader flags specify shader constraints to the HLSL compiler.</span></span> <span data-ttu-id="58c32-145">Эти флаги влияют на код, создаваемый компилятором шейдера следующими способами.</span><span class="sxs-lookup"><span data-stu-id="58c32-145">These flags affect the code generated by the shader compiler in the following ways:</span></span>

-   <span data-ttu-id="58c32-146">Оптимизируйте размер кода.</span><span class="sxs-lookup"><span data-stu-id="58c32-146">Optimize the code size.</span></span>
-   <span data-ttu-id="58c32-147">Включая отладочную информацию, которая предотвращает управление потоком.</span><span class="sxs-lookup"><span data-stu-id="58c32-147">Including debug information, which prevents flow control.</span></span>
-   <span data-ttu-id="58c32-148">Влияет на цель компиляции и возможность запуска шейдера на устаревшем оборудовании.</span><span class="sxs-lookup"><span data-stu-id="58c32-148">Affects the compile target and whether a shader can run on legacy hardware.</span></span>

<span data-ttu-id="58c32-149">Эти флаги могут быть логически объединены, если не указаны две конфликтующие характеристики.</span><span class="sxs-lookup"><span data-stu-id="58c32-149">These flags can be logically combined if you have not specified two conflicting characteristics.</span></span> <span data-ttu-id="58c32-150">Список флагов см. в разделе [ \_ константы шейдера D3D10](/windows/desktop/direct3d10/d3d10-shader).</span><span class="sxs-lookup"><span data-stu-id="58c32-150">For a listing of the flags see [D3D10\_SHADER Constants](/windows/desktop/direct3d10/d3d10-shader).</span></span>

## <a name="fx-flags"></a><span data-ttu-id="58c32-151">Флаги FX</span><span class="sxs-lookup"><span data-stu-id="58c32-151">FX Flags</span></span>

<span data-ttu-id="58c32-152">Используйте эти флаги при создании эффектов для определения поведения компиляции или поведения воздействия на среду выполнения.</span><span class="sxs-lookup"><span data-stu-id="58c32-152">Use these flags when you create an effect to define either compilation behavior or runtime effect behavior.</span></span> <span data-ttu-id="58c32-153">Список флагов см. в разделе [ \_ константы D3D10 Effect](/windows/desktop/direct3d10/d3d10-effect).</span><span class="sxs-lookup"><span data-stu-id="58c32-153">For a listing of the flags see [D3D10\_EFFECT Constants](/windows/desktop/direct3d10/d3d10-effect).</span></span>

## <a name="checking-errors"></a><span data-ttu-id="58c32-154">Проверка ошибок</span><span class="sxs-lookup"><span data-stu-id="58c32-154">Checking Errors</span></span>

<span data-ttu-id="58c32-155">Если во время компиляции возникает ошибка, API возвращает интерфейс, который содержит ошибки от компилятора эффектов.</span><span class="sxs-lookup"><span data-stu-id="58c32-155">If during compilation an error occurs, the API returns an interface that contains the errors from the effect compiler.</span></span> <span data-ttu-id="58c32-156">Этот интерфейс называется [**ID3DBlob**](/previous-versions/windows/desktop/legacy/ff728743(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="58c32-156">This interface is called [**ID3DBlob**](/previous-versions/windows/desktop/legacy/ff728743(v=vs.85)).</span></span> <span data-ttu-id="58c32-157">Он не читается напрямую; Однако, возвращая указатель на буфер, содержащий данные (которые являются строкой), можно увидеть ошибки компиляции.</span><span class="sxs-lookup"><span data-stu-id="58c32-157">It is not directly readable; however, by returning a pointer to the buffer that contains the data (which is a string), you can see any compilation errors.</span></span>

<span data-ttu-id="58c32-158">Этот пример содержит ошибку в Басичлсл. FX, первое объявление переменной возникает дважды.</span><span class="sxs-lookup"><span data-stu-id="58c32-158">This example contains an error in the BasicHLSL.fx, the first variable declaration occurs twice.</span></span>


```
//-------------------------------------------------------------------
// Global variables
//-------------------------------------------------------------------
float4 g_MaterialAmbientColor;      // Material's ambient color

// Declare the same variable twice
float4 g_MaterialAmbientColor;      // Material's ambient color
```



<span data-ttu-id="58c32-159">Эта ошибка приводит к тому, что компилятор возвращает следующую ошибку, как показано на следующем снимке экрана окно контрольных значений в Microsoft Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="58c32-159">This error causes the compiler to return the following error, as shown in the following screen shot of the Watch window in Microsoft Visual Studio.</span></span>

![снимок экрана окна "контрольные значения Visual Studio" с ошибкой 0x01997fb8](images/effect-compile-errors-2.jpg)

<span data-ttu-id="58c32-161">Так как компилятор возвращает ошибку в ЛПВОИД указателе, приведите его к символьной строке в окно контрольных значений.</span><span class="sxs-lookup"><span data-stu-id="58c32-161">Because the compiler returns the error in a LPVOID pointer, cast it to a character string in the Watch window.</span></span>

<span data-ttu-id="58c32-162">Ниже приведен код, который возвращает ошибку из-за неудачной компиляции.</span><span class="sxs-lookup"><span data-stu-id="58c32-162">Here is the code that returns the error from the failed compile.</span></span>


```
// Read the D3DX effect file
WCHAR str[MAX_PATH];
ID3DBlob*   l_pBlob_Effect = NULL;
ID3DBlob*   l_pBlob_Errors = NULL;
hr = DXUTFindDXSDKMediaFileCch( str, MAX_PATH, L"BasicHLSL10.fx" );
hr = D3DX11CompileFromFile( str, NULL, NULL, pFunctionName, 
                       pProfile, D3D10_SHADER_ENABLE_STRICTNESS, NULL, 
                       NULL, &pBlob, &pErrorBlob, NULL );      

LPVOID l_pError = NULL;
if( pErrorBlob )
{
    l_pError = pErrorBlob->GetBufferPointer();
    // then cast to a char* to see it in the locals window
}
```



## <a name="related-topics"></a><span data-ttu-id="58c32-163">См. также</span><span class="sxs-lookup"><span data-stu-id="58c32-163">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="58c32-164">Отрисовка результата (Direct3D 11)</span><span class="sxs-lookup"><span data-stu-id="58c32-164">Rendering an Effect (Direct3D 11)</span></span>](d3d11-graphics-programming-guide-effects-render.md)
</dt> </dl>

 

 