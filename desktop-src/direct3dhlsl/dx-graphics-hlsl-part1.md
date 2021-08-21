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
ms.openlocfilehash: 03e5b23f5186111719e45b8e3c0b1b5bd0227065f28489996524ffca3b38d2f7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118090991"
---
# <a name="compiling-shaders"></a>Компиляция шейдеров

> [!NOTE]
> В этом разделе описывается `FXC.EXE` компилятор, используемый для моделей шейдеров 2 – 5,1. Для Shader Model 6 используется `DXC.EXE` вместо, который описан в статье [Использование dxc.exe и dxcompiler.dll](https://github.com/microsoft/DirectXShaderCompiler/wiki/Using-dxc.exe-and-dxcompiler.dll).

Microsoft Visual Studio 2012 теперь может компилировать код шейдера из \* файлов. hlsl, включаемых в проект C++.

в рамках процесса сборки Visual Studio 2012 использует компилятор кода [fxc.exe](/windows/desktop/direct3dtools/fxc) HLSL для компиляции HLSL файлов в двоичные файловые файлы шейдеров или в байтовые массивы, определенные в файлах заголовков. Как компилятор кода HLSL компилирует каждый файл HLSL в проекте, зависит от того, как указать свойство **файлов выходные данные** для этого файла. Дополнительные сведения о страницах свойств HLSL см. в разделе [страницы свойств HLSL](/previous-versions/visualstudio/visual-studio-2012/jj620902(v=vs.110)).

Используемый метод компиляции обычно зависит от размера \* файла HLSL. Если включить в заголовок большой объем байтового кода, размер и начальное время загрузки приложения будут увеличены. Кроме того, весь байтовый код должен находиться в памяти даже после создания шейдера, что приведет к потере ресурсов. Но при включении в заголовок байтового кода можно уменьшить сложность кода и упростить создание шейдера.

Теперь рассмотрим различные способы компиляции кода шейдера и соглашений для расширений файлов для кода шейдера.

-   [Использование расширений файлов кода шейдера](#using-shader-code-file-extensions)
-   [Компиляция во время сборки в объектные файлы](#compiling-at-build-time-to-object-files)
-   [Компиляция во время сборки в файлы заголовков](#compiling-at-build-time-to-header-files)
-   [Компиляция с помощью D3DCompileFromFile](#compiling-with-d3dcompilefromfile)
-   [См. также](#related-topics)
-   [Связанные темы](#related-topics)

## <a name="using-shader-code-file-extensions"></a>Использование расширений файлов кода шейдера

Чтобы согласовать соглашение с Майкрософт, используйте следующие расширения файлов для кода шейдера:

-   Файл с расширением HLSL содержит исходный код на языке штриховки высокого уровня ([HLSL](dx-graphics-hlsl-reference.md)).
-   Файл с расширением .cso содержит скомпилированный объект шейдера.
-   Файл с расширением .h — это файл заголовка, но в контексте кода шейдера этот файл заголовка определяет массив байтов, содержащий данные шейдера.

## <a name="compiling-at-build-time-to-object-files"></a>Компиляция во время сборки в объектные файлы

При компиляции HLSL-файлов в двоичные файловые файлы шейдера приложение должно считывать данные из этих файлов объектов (. cso является расширением по умолчанию для этих объектных файлов), назначать данные байтовые массивы и создавать объекты шейдера из этих массивов байтов. Например, чтобы создать шейдер вершин ([**ID3D11VertexShader**](/windows/desktop/api/d3d11/nn-d3d11-id3d11vertexshader) \* \* ), вызовите метод [**ID3D11Device:: креатевертексшадер**](/windows/desktop/api/d3d11/nf-d3d11-id3d11device-createvertexshader) с массивом байтов, который содержит скомпилированный байтовый код шейдера вершин. В [примере "учебник по Direct3D](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Direct3D%20tutorial%20sample) " показано, как создавать объекты шейдера из байтовых массивов, полученных из. объектно построителей двоичных файлов шейдера. В этом примере кода из [примера учебника по Direct3D](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Direct3D%20tutorial%20sample)свойство **выходные данные** Files для файла симплевертексшадер. HLSL определяет компиляцию в объектный файл симплевертексшадер. cso.

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

## <a name="compiling-at-build-time-to-header-files"></a>Компиляция во время сборки в файлы заголовков

При компиляции HLSL файлов в байтовые массивы, определенные в файлах заголовков, необходимо включить эти файлы заголовков в код. В [примере расширений мультимедиа](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Media%20extensions%20sample) показано, как создавать объекты шейдера из массивов байтов, определенных в файлах заголовков и включаемых в проект во время компиляции. В этом примере кода из [примера расширения мультимедиа](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Media%20extensions%20sample)свойство **выходные данные** Files для файла PixelShader. HLSL определяет компиляцию в массив байтов *g \_ Псшадер* , определенный в файле заголовка PixelShader. h.


```C++
#       include "PixelShader.h"
        ComPtr<ID3D11PixelShader> m_pPixelShader;
        hr = pDevice->CreatePixelShader(g_psshader, sizeof(g_psshader), nullptr, &m_pPixelShader);
```



## <a name="compiling-with-d3dcompilefromfile"></a>Компиляция с помощью D3DCompileFromFile

Можно также использовать функцию [**D3DCompileFromFile**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dcompilefromfile) во время выполнения для компиляции кода шейдера. Дополнительные сведения о том, как это сделать, см. [в разделе инструкции. Компиляция шейдера](/windows/desktop/direct3d11/how-to--compile-a-shader).

> [!Note]  
> Windows Приложения Магазина поддерживают использование [**D3DCompileFromFile**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dcompilefromfile) для разработки, но не для развертывания.

 

## <a name="related-topics"></a>Связанные разделы

[Руководство по программированию для HLSL](dx-graphics-hlsl-pguide.md)


## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Руководство по программированию для HLSL](dx-graphics-hlsl-pguide.md)
</dt> </dl>

 

 