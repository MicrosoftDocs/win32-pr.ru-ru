---
title: Компиляция шейдеров
description: Теперь рассмотрим различные способы компиляции кода шейдера и соглашений для расширений файлов для кода шейдера.
ms.assetid: a4e6b7cd-c5cc-4165-ba73-205155e449c9
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 3ea71da99dd68769324b07d3fc76a0c5ca00009d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104337996"
---
# <a name="compiling-shaders"></a><span data-ttu-id="6b91c-103">Компиляция шейдеров</span><span class="sxs-lookup"><span data-stu-id="6b91c-103">Compiling shaders</span></span>

> [!NOTE]
> <span data-ttu-id="6b91c-104">В этом разделе описывается `FXC.EXE` компилятор, используемый для моделей шейдеров 2 – 5,1.</span><span class="sxs-lookup"><span data-stu-id="6b91c-104">This topic covers the `FXC.EXE` compiler used for Shader Models 2 through 5.1.</span></span> <span data-ttu-id="6b91c-105">Для Shader Model 6 используется `DXC.EXE` вместо, который описан в статье [Использование dxc.exe и dxcompiler.dll](https://github.com/microsoft/DirectXShaderCompiler/wiki/Using-dxc.exe-and-dxcompiler.dll).</span><span class="sxs-lookup"><span data-stu-id="6b91c-105">For Shader Model 6, you use `DXC.EXE` instead, which is documented in [Using dxc.exe and dxcompiler.dll](https://github.com/microsoft/DirectXShaderCompiler/wiki/Using-dxc.exe-and-dxcompiler.dll).</span></span>

<span data-ttu-id="6b91c-106">Microsoft Visual Studio 2012 теперь может компилировать код шейдера из \* файлов. HLSL, включаемых в проект C++.</span><span class="sxs-lookup"><span data-stu-id="6b91c-106">Microsoft Visual Studio 2012 can now compile shader code from \*.hlsl files that you include in your C++ project.</span></span>

<span data-ttu-id="6b91c-107">В рамках процесса сборки Visual Studio 2012 использует [fxc.exe](/windows/desktop/direct3dtools/fxc) компилятор кода HLSL для компиляции HLSLовых файлов в двоичные файлы шейдеров или в байтовые массивы, определенные в файлах заголовков.</span><span class="sxs-lookup"><span data-stu-id="6b91c-107">As part of the build process, Visual Studio 2012 uses the [fxc.exe](/windows/desktop/direct3dtools/fxc) HLSL code compiler to compile the .hlsl files into binary shader object files or into byte arrays that are defined in header files.</span></span> <span data-ttu-id="6b91c-108">Как компилятор кода HLSL компилирует каждый файл HLSL в проекте, зависит от того, как указать свойство **файлов выходные данные** для этого файла.</span><span class="sxs-lookup"><span data-stu-id="6b91c-108">How the HLSL code compiler compiles each .hlsl file in your project depends on how you specify the **Ouput Files** property for that file.</span></span> <span data-ttu-id="6b91c-109">Дополнительные сведения о страницах свойств HLSL см. в разделе [страницы свойств HLSL](/previous-versions/visualstudio/visual-studio-2012/jj620902(v=vs.110)).</span><span class="sxs-lookup"><span data-stu-id="6b91c-109">For more info about HLSL property pages, see [HLSL Property Pages](/previous-versions/visualstudio/visual-studio-2012/jj620902(v=vs.110)).</span></span>

<span data-ttu-id="6b91c-110">Используемый метод компиляции обычно зависит от размера \* файла HLSL.</span><span class="sxs-lookup"><span data-stu-id="6b91c-110">The compile method that you use typically depends on the size of your \*.hlsl file.</span></span> <span data-ttu-id="6b91c-111">Если включить в заголовок большой объем байтового кода, размер и начальное время загрузки приложения будут увеличены.</span><span class="sxs-lookup"><span data-stu-id="6b91c-111">If you include a large amount of byte code in a header, you increase the size and the initial load time of your app.</span></span> <span data-ttu-id="6b91c-112">Кроме того, весь байтовый код должен находиться в памяти даже после создания шейдера, что приведет к потере ресурсов.</span><span class="sxs-lookup"><span data-stu-id="6b91c-112">You also force all byte code to reside in memory even after the shader is created, which wastes resources.</span></span> <span data-ttu-id="6b91c-113">Но при включении в заголовок байтового кода можно уменьшить сложность кода и упростить создание шейдера.</span><span class="sxs-lookup"><span data-stu-id="6b91c-113">But when you include byte code in a header, you can reduce code complexity and simplify shader creation.</span></span>

<span data-ttu-id="6b91c-114">Теперь рассмотрим различные способы компиляции кода шейдера и соглашений для расширений файлов для кода шейдера.</span><span class="sxs-lookup"><span data-stu-id="6b91c-114">Let's now look at various ways to compile your shader code and conventions for file extensions for shader code.</span></span>

-   [<span data-ttu-id="6b91c-115">Использование расширений файлов кода шейдера</span><span class="sxs-lookup"><span data-stu-id="6b91c-115">Using shader code file extensions</span></span>](#using-shader-code-file-extensions)
-   [<span data-ttu-id="6b91c-116">Компиляция во время сборки в объектные файлы</span><span class="sxs-lookup"><span data-stu-id="6b91c-116">Compiling at build time to object files</span></span>](#compiling-at-build-time-to-object-files)
-   [<span data-ttu-id="6b91c-117">Компиляция во время сборки в файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="6b91c-117">Compiling at build time to header files</span></span>](#compiling-at-build-time-to-header-files)
-   [<span data-ttu-id="6b91c-118">Компиляция с помощью D3DCompileFromFile</span><span class="sxs-lookup"><span data-stu-id="6b91c-118">Compiling with D3DCompileFromFile</span></span>](#compiling-with-d3dcompilefromfile)
-   [<span data-ttu-id="6b91c-119">См. также</span><span class="sxs-lookup"><span data-stu-id="6b91c-119">Related Topics</span></span>](#related-topics)
-   [<span data-ttu-id="6b91c-120">См. также</span><span class="sxs-lookup"><span data-stu-id="6b91c-120">Related topics</span></span>](#related-topics)

## <a name="using-shader-code-file-extensions"></a><span data-ttu-id="6b91c-121">Использование расширений файлов кода шейдера</span><span class="sxs-lookup"><span data-stu-id="6b91c-121">Using shader code file extensions</span></span>

<span data-ttu-id="6b91c-122">Чтобы согласовать соглашение с Майкрософт, используйте следующие расширения файлов для кода шейдера:</span><span class="sxs-lookup"><span data-stu-id="6b91c-122">To conform to Microsoft convention, use these file extensions for your shader code:</span></span>

-   <span data-ttu-id="6b91c-123">Файл с расширением HLSL содержит исходный код на языке штриховки высокого уровня ([HLSL](dx-graphics-hlsl-reference.md)).</span><span class="sxs-lookup"><span data-stu-id="6b91c-123">A file with the .hlsl extension holds High Level Shading Language ([HLSL](dx-graphics-hlsl-reference.md)) source code.</span></span>
-   <span data-ttu-id="6b91c-124">Файл с расширением .cso содержит скомпилированный объект шейдера.</span><span class="sxs-lookup"><span data-stu-id="6b91c-124">A file with the .cso extension holds a compiled shader object.</span></span>
-   <span data-ttu-id="6b91c-125">Файл с расширением .h — это файл заголовка, но в контексте кода шейдера этот файл заголовка определяет массив байтов, содержащий данные шейдера.</span><span class="sxs-lookup"><span data-stu-id="6b91c-125">A file with the .h extension is a header file, but in a shader code context, this header file defines a byte array that holds shader data.</span></span>

## <a name="compiling-at-build-time-to-object-files"></a><span data-ttu-id="6b91c-126">Компиляция во время сборки в объектные файлы</span><span class="sxs-lookup"><span data-stu-id="6b91c-126">Compiling at build time to object files</span></span>

<span data-ttu-id="6b91c-127">При компиляции HLSL-файлов в двоичные файловые файлы шейдера приложение должно считывать данные из этих файлов объектов (. cso является расширением по умолчанию для этих объектных файлов), назначать данные байтовые массивы и создавать объекты шейдера из этих массивов байтов.</span><span class="sxs-lookup"><span data-stu-id="6b91c-127">If you compile your .hlsl files into binary shader object files, your app needs to read the data from those object files (.cso is the default extension for these object files), assign the data to byte arrays, and create shader objects from those byte arrays.</span></span> <span data-ttu-id="6b91c-128">Например, чтобы создать шейдер вершин ([**ID3D11VertexShader**](/windows/desktop/api/d3d11/nn-d3d11-id3d11vertexshader) \* \* ), вызовите метод [**ID3D11Device:: креатевертексшадер**](/windows/desktop/api/d3d11/nf-d3d11-id3d11device-createvertexshader) с массивом байтов, который содержит скомпилированный байтовый код шейдера вершин.</span><span class="sxs-lookup"><span data-stu-id="6b91c-128">For example, to create a vertex shader ([**ID3D11VertexShader**](/windows/desktop/api/d3d11/nn-d3d11-id3d11vertexshader)\*\*), call the [**ID3D11Device::CreateVertexShader**](/windows/desktop/api/d3d11/nf-d3d11-id3d11device-createvertexshader) method with a byte array that contains compiled vertex shader byte code.</span></span> <span data-ttu-id="6b91c-129">В [примере "учебник по Direct3D](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Direct3D%20tutorial%20sample) " показано, как создавать объекты шейдера из байтовых массивов, полученных из. объектно построителей двоичных файлов шейдера.</span><span class="sxs-lookup"><span data-stu-id="6b91c-129">The [Direct3D tutorial sample](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Direct3D%20tutorial%20sample) shows how to create shader objects from byte arrays that it obtained from .cso binary shader object files.</span></span> <span data-ttu-id="6b91c-130">В этом примере кода из [примера учебника по Direct3D](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Direct3D%20tutorial%20sample)свойство **выходные данные** Files для файла симплевертексшадер. HLSL определяет компиляцию в объектный файл симплевертексшадер. cso.</span><span class="sxs-lookup"><span data-stu-id="6b91c-130">In this example code from the [Direct3D tutorial sample](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Direct3D%20tutorial%20sample), the **Ouput Files** property for the SimpleVertexShader.hlsl file specifies to compile into the SimpleVertexShader.cso object file.</span></span>

```cpp
        auto vertexShaderBytecode = reader->ReadData("SimpleVertexShader.cso");
        ComPtr<ID3D11VertexShader> vertexShader;
        DX::ThrowIfFailed(
            m_d3dDevice->CreateVertexShader(
                vertexShaderBytecode->Data,
                vertexShaderBytecode->Length,
                nullptr,
                &vertexShader
                )
```

## <a name="compiling-at-build-time-to-header-files"></a><span data-ttu-id="6b91c-131">Компиляция во время сборки в файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="6b91c-131">Compiling at build time to header files</span></span>

<span data-ttu-id="6b91c-132">При компиляции HLSL файлов в байтовые массивы, определенные в файлах заголовков, необходимо включить эти файлы заголовков в код.</span><span class="sxs-lookup"><span data-stu-id="6b91c-132">If you compile your .hlsl files into byte arrays that are defined in header files, you need to include those header files in your code.</span></span> <span data-ttu-id="6b91c-133">В [примере расширений мультимедиа](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Media%20extensions%20sample) показано, как создавать объекты шейдера из массивов байтов, определенных в файлах заголовков и включаемых в проект во время компиляции.</span><span class="sxs-lookup"><span data-stu-id="6b91c-133">The [Media extensions sample](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Media%20extensions%20sample) shows how to create shader objects from byte arrays that are defined in header files and that you include in your project at compile time.</span></span> <span data-ttu-id="6b91c-134">В этом примере кода из [примера расширения мультимедиа](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Media%20extensions%20sample)свойство **выходные данные** Files для файла PixelShader. HLSL определяет компиляцию в массив байтов *g \_ Псшадер* , определенный в файле заголовка PixelShader. h.</span><span class="sxs-lookup"><span data-stu-id="6b91c-134">In this example code from the [Media extensions sample](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Media%20extensions%20sample), the **Ouput Files** property for the PixelShader.hlsl file specifies to compile into the *g\_psshader* byte array that is defined in the PixelShader.h header file.</span></span>


```C++
#       include "PixelShader.h"
        ComPtr<ID3D11PixelShader> m_pPixelShader;
        hr = pDevice->CreatePixelShader(g_psshader, sizeof(g_psshader), nullptr, &m_pPixelShader);
```



## <a name="compiling-with-d3dcompilefromfile"></a><span data-ttu-id="6b91c-135">Компиляция с помощью D3DCompileFromFile</span><span class="sxs-lookup"><span data-stu-id="6b91c-135">Compiling with D3DCompileFromFile</span></span>

<span data-ttu-id="6b91c-136">Можно также использовать функцию [**D3DCompileFromFile**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dcompilefromfile) во время выполнения для компиляции кода шейдера.</span><span class="sxs-lookup"><span data-stu-id="6b91c-136">You can also use the [**D3DCompileFromFile**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dcompilefromfile) function at run time to compile shader code.</span></span> <span data-ttu-id="6b91c-137">Дополнительные сведения о том, как это сделать, см. [в разделе инструкции. Компиляция шейдера](/windows/desktop/direct3d11/how-to--compile-a-shader).</span><span class="sxs-lookup"><span data-stu-id="6b91c-137">For more info about how to do this, see [How To: Compile a Shader](/windows/desktop/direct3d11/how-to--compile-a-shader).</span></span>

> [!Note]  
> <span data-ttu-id="6b91c-138">Приложения Магазина Windows поддерживают использование [**D3DCompileFromFile**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dcompilefromfile) для разработки, но не для развертывания.</span><span class="sxs-lookup"><span data-stu-id="6b91c-138">Windows Store apps support using [**D3DCompileFromFile**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dcompilefromfile) for development but not for deployment.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="6b91c-139">См. также</span><span class="sxs-lookup"><span data-stu-id="6b91c-139">Related Topics</span></span>

[<span data-ttu-id="6b91c-140">Руководство по программированию для HLSL</span><span class="sxs-lookup"><span data-stu-id="6b91c-140">Programming Guide for HLSL</span></span>](dx-graphics-hlsl-pguide.md)


## <a name="related-topics"></a><span data-ttu-id="6b91c-141">См. также</span><span class="sxs-lookup"><span data-stu-id="6b91c-141">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6b91c-142">Руководство по программированию для HLSL</span><span class="sxs-lookup"><span data-stu-id="6b91c-142">Programming Guide for HLSL</span></span>](dx-graphics-hlsl-pguide.md)
</dt> </dl>

 

 