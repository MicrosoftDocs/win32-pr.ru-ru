---
title: Использование шейдеров в Direct3D 10
description: Использование шейдеров в Direct3D 10
ms.assetid: cff6f901-cb9b-44d5-a75b-9a4029a37215
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 0e19275532ce8fd034813d8574f6bdc04d72f966
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104337537"
---
# <a name="using-shaders-in-direct3d-10"></a><span data-ttu-id="e71d6-103">Использование шейдеров в Direct3D 10</span><span class="sxs-lookup"><span data-stu-id="e71d6-103">Using Shaders in Direct3D 10</span></span>

<span data-ttu-id="e71d6-104">Конвейер имеет три этапа шейдера, и каждый из них программируется с помощью шейдера HLSL.</span><span class="sxs-lookup"><span data-stu-id="e71d6-104">The pipeline has three shader stages and each one is programmed with an HLSL shader.</span></span> <span data-ttu-id="e71d6-105">Все шейдеры Direct3D 10 написаны на HLSL, нацеливание на модель шейдера 4.</span><span class="sxs-lookup"><span data-stu-id="e71d6-105">All Direct3D 10 shaders are written in HLSL, targeting shader model 4.</span></span>



|                                                                                                                                                                                                                                                                                                                                                |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e71d6-106">Различия между Direct3D 9 и Direct3D 10:</span><span class="sxs-lookup"><span data-stu-id="e71d6-106">Differences between Direct3D 9 and Direct3D 10:</span></span><br/> <span data-ttu-id="e71d6-107">В отличие от моделей шейдера Direct3D 9, которые могут быть созданы на промежуточном языке сборки, шейдеры Shader Model 4,0 созданы только в HLSL.</span><span class="sxs-lookup"><span data-stu-id="e71d6-107">Unlike Direct3D 9 shader models which could be authored in an intermediate assembly language, shader model 4.0 shaders are only authored in HLSL.</span></span> <span data-ttu-id="e71d6-108">Автономная компиляция шейдеров в байт-код с возможностью использования устройства по-прежнему поддерживается и рекомендуется для большинства сценариев.</span><span class="sxs-lookup"><span data-stu-id="e71d6-108">Offline compilation of shaders into device-consumable bytecode is still supported, and recommended for most scenarios.</span></span><br/> |



 

<span data-ttu-id="e71d6-109">В этом примере используется только шейдер вершин.</span><span class="sxs-lookup"><span data-stu-id="e71d6-109">This example uses only a vertex shader.</span></span> <span data-ttu-id="e71d6-110">Поскольку все шейдеры основаны на стандартном ядре шейдера, изучение использования шейдера вершин очень похоже на использование геометрии или шейдера пикселей.</span><span class="sxs-lookup"><span data-stu-id="e71d6-110">Because all shaders are built from the common shader core, learning how to use a vertex shader is very similar to using a geometry or pixel shader.</span></span>

<span data-ttu-id="e71d6-111">После создания шейдера HLSL (в этом примере используется Вершинный шейдер Хлслвисаутфкс. ВШ) необходимо подготовить его к конкретному этапу конвейера, который будет его использовать.</span><span class="sxs-lookup"><span data-stu-id="e71d6-111">Once you have authored an HLSL shader (this example uses the vertex shader HLSLWithoutFX.vsh), you will need to prepare it for the particular pipeline stage that will use it.</span></span> <span data-ttu-id="e71d6-112">Для этого необходимо выполнить следующие действия.</span><span class="sxs-lookup"><span data-stu-id="e71d6-112">To do this you need to:</span></span>

-   [<span data-ttu-id="e71d6-113">Компиляция шейдера</span><span class="sxs-lookup"><span data-stu-id="e71d6-113">Compile a Shader</span></span>](#compile-a-shader)
-   [<span data-ttu-id="e71d6-114">Создание объекта шейдера</span><span class="sxs-lookup"><span data-stu-id="e71d6-114">Create a Shader Object</span></span>](#create-a-shader-object)
-   [<span data-ttu-id="e71d6-115">Задание объекта шейдера</span><span class="sxs-lookup"><span data-stu-id="e71d6-115">Set the Shader Object</span></span>](#set-the-shader-object)
-   [<span data-ttu-id="e71d6-116">Повторить для всех 3 этапов шейдера</span><span class="sxs-lookup"><span data-stu-id="e71d6-116">Repeat for all 3 Shader Stages</span></span>](#repeat-for-all-3-shader-stages)

<span data-ttu-id="e71d6-117">Эти шаги необходимо повторить для каждого шейдера в конвейере.</span><span class="sxs-lookup"><span data-stu-id="e71d6-117">These steps need to be repeated for each shader in the pipeline.</span></span>

## <a name="compile-a-shader"></a><span data-ttu-id="e71d6-118">Компиляция шейдера</span><span class="sxs-lookup"><span data-stu-id="e71d6-118">Compile a Shader</span></span>

<span data-ttu-id="e71d6-119">Первым шагом является компиляция шейдера для проверки правильности кодирования инструкций HLSL.</span><span class="sxs-lookup"><span data-stu-id="e71d6-119">The first step is to compile the shader, to check to see that you have coded the HLSL statements correctly.</span></span> <span data-ttu-id="e71d6-120">Это делается путем вызова D3D10CompileShader и передачи его с несколькими параметрами, как показано ниже:</span><span class="sxs-lookup"><span data-stu-id="e71d6-120">This is done by calling D3D10CompileShader and supplying it with several parameters as shown here:</span></span>


```
    IPD3D10Blob * pBlob;
    
        
    // Compile the vertex shader from the file
    D3D10CompileShader( strPath, strlen( strPath ), "HLSLWithoutFX.vsh", 
        NULL, NULL, "Ripple", "vs_4_0", dwShaderFlags, &pBlob, NULL );
```



<span data-ttu-id="e71d6-121">Эта функция принимает следующие параметры:</span><span class="sxs-lookup"><span data-stu-id="e71d6-121">This function takes the following parameters:</span></span>

-   <span data-ttu-id="e71d6-122">Имя файла (и длина строки имени в байтах), которая содержит шейдер.</span><span class="sxs-lookup"><span data-stu-id="e71d6-122">The name of the file ( and length of the name string in bytes ) that contains the shader.</span></span> <span data-ttu-id="e71d6-123">В этом примере используется только шейдер вершин (в файле Хлслвисаутфкс. ВШ, где расширение файла. ВШ — это сокращение для шейдера вершин).</span><span class="sxs-lookup"><span data-stu-id="e71d6-123">This example uses a vertex shader only (in the file HLSLWithoutFX.vsh file where the file extension .vsh is an abbreviation for vertex shader).</span></span>
-   <span data-ttu-id="e71d6-124">Имя функции шейдера.</span><span class="sxs-lookup"><span data-stu-id="e71d6-124">The shader function name.</span></span> <span data-ttu-id="e71d6-125">В этом примере компилируется шейдер вершин из функции Ripple, которая принимает один вход и возвращает выходную структуру (функция из примера Хлслвисаутфкс):</span><span class="sxs-lookup"><span data-stu-id="e71d6-125">This example compiles a vertex shader from the Ripple function which takes a single input and returns an output struct (the function is from the HLSLWithoutFX sample):</span></span>
    ```
    VS_OUTPUT Ripple( in float2 vPosition : POSITION )
    ```

    

-   <span data-ttu-id="e71d6-126">Указатель на все макросы, используемые шейдером.</span><span class="sxs-lookup"><span data-stu-id="e71d6-126">A pointer to all macros used by the shader.</span></span> <span data-ttu-id="e71d6-127">\_ \_ Чтобы определить макросы, используйте макрос шейдера D3D10. просто создайте строку имени, содержащую все имена макросов (с именами, разделенными пробелами), и строку определения (с каждым телом макроса, разделенного пробелом).</span><span class="sxs-lookup"><span data-stu-id="e71d6-127">Use D3D10\_SHADER\_MACRO to help define your macros; simply create a name string that contains all the macro names (with each name separated by a space) and a definition string (with each macro body separated by a space).</span></span> <span data-ttu-id="e71d6-128">Обе строки должны завершаться нулем.</span><span class="sxs-lookup"><span data-stu-id="e71d6-128">Both strings need to be NULL terminated.</span></span>
-   <span data-ttu-id="e71d6-129">Указатель на любые другие файлы, которые необходимо добавить, чтобы получить возможность скомпилировать шейдер.</span><span class="sxs-lookup"><span data-stu-id="e71d6-129">A pointer to any other files that you need included to get your shaders to compile.</span></span> <span data-ttu-id="e71d6-130">В этом случае используется интерфейс ID3D10Include, который имеет два реализованных пользователем метода: Open и Close.</span><span class="sxs-lookup"><span data-stu-id="e71d6-130">This uses the ID3D10Include interface which has two user-implemented methods: Open and Close.</span></span> <span data-ttu-id="e71d6-131">Чтобы сделать это, необходимо реализовать тело методов Open и Close. в методе Open добавьте код, который будет использоваться для открытия любого включаемого файла. в функции Close добавьте код для закрытия файлов по завершении работы с ними.</span><span class="sxs-lookup"><span data-stu-id="e71d6-131">To make this work, you will need to implement the body of the Open and Close methods; in the Open method add the code you would use to open whatever include files you want, in the Close function add the code to close the files when you are done with them.</span></span>
-   <span data-ttu-id="e71d6-132">Имя компилируемой функции шейдера.</span><span class="sxs-lookup"><span data-stu-id="e71d6-132">The name of the shader function to compile.</span></span> <span data-ttu-id="e71d6-133">Этот шейдер компилирует функцию Ripple.</span><span class="sxs-lookup"><span data-stu-id="e71d6-133">This shader compiles the Ripple function.</span></span>
-   <span data-ttu-id="e71d6-134">Профиль шейдера, предназначенный для целевого объекта при компиляции.</span><span class="sxs-lookup"><span data-stu-id="e71d6-134">The shader profile to target when compiling.</span></span> <span data-ttu-id="e71d6-135">Поскольку вы можете компилировать функцию в вершину, геометрию или шейдер пикселей, профиль сообщает компилятору, какой тип шейдера и какая модель шейдеров следует сравнить с кодом.</span><span class="sxs-lookup"><span data-stu-id="e71d6-135">Since you can compile a function into a vertex, geometry, or pixel shader, the profile tells the compiler which type of shader and which shader model to compare the code against.</span></span>
-   <span data-ttu-id="e71d6-136">Флаги компилятора шейдеров.</span><span class="sxs-lookup"><span data-stu-id="e71d6-136">Shader compiler flags.</span></span> <span data-ttu-id="e71d6-137">Эти флаги указывают компилятору, какую информацию следует поместить в скомпилированный результат, а также способ оптимизации исходящего кода: для скорости, для отладки и т. д. Список доступных флагов см. в разделе [константы эффектов (Direct3D 10)](/windows/desktop/direct3d10/d3d10-graphics-reference-effect-constants) .</span><span class="sxs-lookup"><span data-stu-id="e71d6-137">These flags tell the compiler what information to put into the compiled output and how you want the output code optimized: for speed, for debug, etc. See [Effect Constants (Direct3D 10)](/windows/desktop/direct3d10/d3d10-graphics-reference-effect-constants) for a listing of the available flags.</span></span> <span data-ttu-id="e71d6-138">Этот пример содержит код, который можно использовать для задания значений флагов компилятора для проекта. это главным образом вопрос, нужно ли создавать отладочную информацию.</span><span class="sxs-lookup"><span data-stu-id="e71d6-138">The sample contains some code you can use to set the compiler flag values for your project - this is mainly a question of whether or not you want to generate debug information.</span></span>
-   <span data-ttu-id="e71d6-139">Указатель на буфер, содержащий скомпилированный код шейдера.</span><span class="sxs-lookup"><span data-stu-id="e71d6-139">A pointer to the buffer that contains the compiled shader code.</span></span> <span data-ttu-id="e71d6-140">Кроме того, буфер содержит все внедренные сведения об отладке и таблице символов, запрошенные флагами компилятора.</span><span class="sxs-lookup"><span data-stu-id="e71d6-140">The buffer also contains any embedded debug and symbol table information requested by the compiler flags.</span></span>
-   <span data-ttu-id="e71d6-141">Указатель на буфер, содержащий список ошибок и предупреждений, обнаруженных во время компиляции. это те же сообщения, которые отображаются в выходных данных отладки, если при компиляции шейдера выполнялся отладчик.</span><span class="sxs-lookup"><span data-stu-id="e71d6-141">A pointer to a buffer that contains a listing of errors and warnings that were encountered during the compile, which are the same messages you would see in the debug output if you were running the debugger while compiling the shader.</span></span> <span data-ttu-id="e71d6-142">Значение **null** является допустимым, если не нужно, чтобы ошибки возвращались в буфер.</span><span class="sxs-lookup"><span data-stu-id="e71d6-142">**NULL** is an acceptable value when you don't want the errors returned to a buffer.</span></span>

<span data-ttu-id="e71d6-143">Если шейдер успешно компилируется, указатель на код шейдера возвращается в виде интерфейса ID3D10Blob.</span><span class="sxs-lookup"><span data-stu-id="e71d6-143">If the shader compiles successfully, a pointer to the shader code is returned as a ID3D10Blob interface.</span></span> <span data-ttu-id="e71d6-144">Он называется интерфейсом больших двоичных объектов, так как указатель находится в расположении в памяти, которое состоит из массива DWORD.</span><span class="sxs-lookup"><span data-stu-id="e71d6-144">It is called the Blob interface because the pointer is to a location in memory that is made up of an array of DWORD's.</span></span> <span data-ttu-id="e71d6-145">Интерфейс предоставляется таким образом, чтобы можно было получить указатель на скомпилированный шейдер, который потребуется на следующем шаге.</span><span class="sxs-lookup"><span data-stu-id="e71d6-145">The interface is provided so that you can get a pointer to the compiled shader which you will need in the next step.</span></span>

<span data-ttu-id="e71d6-146">Начиная с пакета SDK 2006 декабря, компилятор HLSL DirectX 10 теперь является компилятором по умолчанию как в DirectX 9, так и в DirectX 10.</span><span class="sxs-lookup"><span data-stu-id="e71d6-146">Beginning with the December 2006 SDK, the DirectX 10 HLSL compiler is now the default compiler in both DirectX 9 and DirectX 10.</span></span> <span data-ttu-id="e71d6-147">Дополнительные сведения см. в разделе [средство компилятора Effect](/windows/desktop/direct3dtools/fxc) .</span><span class="sxs-lookup"><span data-stu-id="e71d6-147">See [Effect-Compiler Tool](/windows/desktop/direct3dtools/fxc) for details.</span></span>

### <a name="get-a-pointer-to-a-compiled-shader"></a><span data-ttu-id="e71d6-148">Получение указателя на скомпилированный шейдер</span><span class="sxs-lookup"><span data-stu-id="e71d6-148">Get a Pointer to a Compiled Shader</span></span>

<span data-ttu-id="e71d6-149">Для нескольких методов API требуется указатель на скомпилированный шейдер.</span><span class="sxs-lookup"><span data-stu-id="e71d6-149">Several API methods require a pointer to a compiled shader.</span></span> <span data-ttu-id="e71d6-150">Этот аргумент обычно называется *пшадербитекоде* , так как он указывает на скомпилированный шейдер, представленный в виде последовательности байтовых кодов.</span><span class="sxs-lookup"><span data-stu-id="e71d6-150">This argument is usually called *pShaderBytecode* because it points to a compiled shader represented as a sequence of byte codes.</span></span> <span data-ttu-id="e71d6-151">Чтобы получить указатель на скомпилированный шейдер, сначала Скомпилируйте шейдер путем вызова [**D3D10CompileShader**](/windows/desktop/api/d3d10shader/nf-d3d10shader-d3d10compileshader) или аналогичной функции.</span><span class="sxs-lookup"><span data-stu-id="e71d6-151">To get a pointer to a compiled shader, first compile the shader by calling [**D3D10CompileShader**](/windows/desktop/api/d3d10shader/nf-d3d10shader-d3d10compileshader) or a similar function.</span></span> <span data-ttu-id="e71d6-152">Если компиляция прошла успешно, то Скомпилированный шейдер возвращается в интерфейсе [**ID3D10Blob**](/windows/desktop/api/d3dcommon/nn-d3dcommon-id3d10blob) .</span><span class="sxs-lookup"><span data-stu-id="e71d6-152">If compilation is successful, the compiled shader is returned in an [**ID3D10Blob**](/windows/desktop/api/d3dcommon/nn-d3dcommon-id3d10blob) interface.</span></span> <span data-ttu-id="e71d6-153">Наконец, используйте метод [**жетбуфферпоинтер**](/windows/desktop/api/d3dcommon/nf-d3dcommon-id3d10blob-getbufferpointer) для возврата указателя.</span><span class="sxs-lookup"><span data-stu-id="e71d6-153">Finally, use the [**GetBufferPointer**](/windows/desktop/api/d3dcommon/nf-d3dcommon-id3d10blob-getbufferpointer) method to return the pointer.</span></span>

## <a name="create-a-shader-object"></a><span data-ttu-id="e71d6-154">Создание объекта шейдера</span><span class="sxs-lookup"><span data-stu-id="e71d6-154">Create a Shader Object</span></span>

<span data-ttu-id="e71d6-155">После компиляции шейдера вызовите Креатевертексшадер, чтобы создать объект шейдера:</span><span class="sxs-lookup"><span data-stu-id="e71d6-155">Once the shader is compiled, call CreateVertexShader to create the shader object:</span></span>


```
    ID3D10VertexShader ** ppVertexShader
    ID3D10Blob pBlob;


    // Create the vertex shader
    hr = pd3dDevice->CreateVertexShader( (DWORD*)pBlob->GetBufferPointer(),
        pBlob->GetBufferSize(), &ppVertexShader );

    // Release the pointer to the compiled shader once you are done with it
    pBlob->Release();
```



<span data-ttu-id="e71d6-156">Чтобы создать объект шейдера, передайте указатель на скомпилированный шейдер в Креатевертексшадер.</span><span class="sxs-lookup"><span data-stu-id="e71d6-156">To create the shader object, pass the pointer to the compiled shader into CreateVertexShader.</span></span> <span data-ttu-id="e71d6-157">Так как вам пришлось успешно скомпилировать шейдер, этот вызов почти наверняка будет пройден, если на компьютере не возникла проблема с памятью.</span><span class="sxs-lookup"><span data-stu-id="e71d6-157">Since you had to successfully compile the shader first, this call will almost certainly pass, unless you have a memory problem on your machine.</span></span>

<span data-ttu-id="e71d6-158">Вы можете создать столько объектов шейдера, сколько вам нравится, и просто сохраним указатели на них.</span><span class="sxs-lookup"><span data-stu-id="e71d6-158">You can create as many shader objects as you like and simply keep pointers to them.</span></span> <span data-ttu-id="e71d6-159">Этот же механизм работает для геометрических и пиксельных шейдеров, предполагая, что вы сопоставляете профили шейдеров (при вызове метода Compile) в именах интерфейсов (при вызове метода Create).</span><span class="sxs-lookup"><span data-stu-id="e71d6-159">This same mechanism works for geometry and pixel shaders assuming you match the shader profiles (when you call the compile method) to the interface names (when you call the create method).</span></span>

## <a name="set-the-shader-object"></a><span data-ttu-id="e71d6-160">Задание объекта шейдера</span><span class="sxs-lookup"><span data-stu-id="e71d6-160">Set the Shader Object</span></span>

<span data-ttu-id="e71d6-161">На последнем шаге задается шейдер на этапе конвейера.</span><span class="sxs-lookup"><span data-stu-id="e71d6-161">The last step is set the shader to the pipeline stage.</span></span> <span data-ttu-id="e71d6-162">Так как в конвейере есть три этапа шейдера, необходимо сделать три вызова API, по одному для каждого этапа.</span><span class="sxs-lookup"><span data-stu-id="e71d6-162">Since there are three shader stages in the pipeline, you will need to make three API calls, one for each stage.</span></span>


```
    // Set a vertex shader
    pd3dDevice->VSSetShader( g_pVS10 );
```



<span data-ttu-id="e71d6-163">Вызов Вссетшадер принимает указатель на шейдер вершин, созданный на шаге 1.</span><span class="sxs-lookup"><span data-stu-id="e71d6-163">The call to VSSetShader takes the pointer to the vertex shader created in step 1.</span></span> <span data-ttu-id="e71d6-164">Это задает шейдер на устройстве.</span><span class="sxs-lookup"><span data-stu-id="e71d6-164">This sets the shader in the device.</span></span> <span data-ttu-id="e71d6-165">Этап шейдера вершин теперь инициализируется с помощью кода шейдера вершин, все, что остается, — инициализация всех переменных шейдера.</span><span class="sxs-lookup"><span data-stu-id="e71d6-165">The vertex shader stage is now initialized with its vertex shader code, all that remains is initializing any shader variables.</span></span>

## <a name="repeat-for-all-3-shader-stages"></a><span data-ttu-id="e71d6-166">Повторить для всех 3 этапов шейдера</span><span class="sxs-lookup"><span data-stu-id="e71d6-166">Repeat for all 3 Shader Stages</span></span>

<span data-ttu-id="e71d6-167">Повторите тот же набор шагов, чтобы создать любой вершинный или пиксельный шейдер или даже шейдер Geometry, который выводит данные в шейдер пикселей.</span><span class="sxs-lookup"><span data-stu-id="e71d6-167">Repeat these same set of steps to build any vertex or pixel shader or even a geometry shader that outputs to the pixel shader.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e71d6-168">См. также</span><span class="sxs-lookup"><span data-stu-id="e71d6-168">Related Topics</span></span>

[<span data-ttu-id="e71d6-169">Компиляция шейдеров</span><span class="sxs-lookup"><span data-stu-id="e71d6-169">Compiling Shaders</span></span>](dx-graphics-hlsl-part1.md)


## <a name="related-topics"></a><span data-ttu-id="e71d6-170">См. также</span><span class="sxs-lookup"><span data-stu-id="e71d6-170">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e71d6-171">Руководство по программированию для HLSL</span><span class="sxs-lookup"><span data-stu-id="e71d6-171">Programming Guide for HLSL</span></span>](dx-graphics-hlsl-pguide.md)
</dt> </dl>

 

