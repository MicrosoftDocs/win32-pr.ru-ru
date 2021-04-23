---
title: Инициализация текстуры из файла
description: В этом разделе показано, как использовать компонент Windows Imaging Component (WIC) для создания текстуры и представления отдельно.
ms.assetid: ea3c6003-191d-47d1-8931-f43598728ad4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1bf6ba4296c2103d7f84f934899f906500e712cd
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "103987782"
---
# <a name="how-to-initialize-a-texture-from-a-file"></a><span data-ttu-id="dc1c5-103">Как инициализировать текстуру из файла</span><span class="sxs-lookup"><span data-stu-id="dc1c5-103">How to: Initialize a Texture From a File</span></span>

<span data-ttu-id="dc1c5-104">Для инициализации [текстуры](overviews-direct3d-11-resources-textures.md) из файла можно использовать API компонента работы с [образами Windows](/windows/desktop/wic/-wic-lh) .</span><span class="sxs-lookup"><span data-stu-id="dc1c5-104">You can use the [Windows Imaging Component](/windows/desktop/wic/-wic-lh) API to initialize a [texture](overviews-direct3d-11-resources-textures.md) from a file.</span></span> <span data-ttu-id="dc1c5-105">Чтобы загрузить текстуру, необходимо создать текстуру и представление текстуры.</span><span class="sxs-lookup"><span data-stu-id="dc1c5-105">To load a texture, you must create a texture and a texture view.</span></span> <span data-ttu-id="dc1c5-106">В этом разделе показано, как использовать компонент Windows Imaging Component (WIC) для создания текстуры и представления отдельно.</span><span class="sxs-lookup"><span data-stu-id="dc1c5-106">This topic shows how to use Windows Imaging Component (WIC) to create the texture and the view separately.</span></span>

> [!Note]  
> <span data-ttu-id="dc1c5-107">Этот раздел полезен для изображений, создаваемых в виде простых 2D-текстур.</span><span class="sxs-lookup"><span data-stu-id="dc1c5-107">This topic is useful for images that you create as simple 2D textures.</span></span> <span data-ttu-id="dc1c5-108">Для более сложных ресурсов используйте [DDS](/windows/desktop/direct3ddds/dx-graphics-dds).</span><span class="sxs-lookup"><span data-stu-id="dc1c5-108">For more complex resources, use [DDS](/windows/desktop/direct3ddds/dx-graphics-dds).</span></span> <span data-ttu-id="dc1c5-109">Сведения о полнофункциональном модуле чтения, записи и конвейера обработки текстур см. в разделе [директкстекс](https://github.com/Microsoft/DirectXTex) и [директкстк](https://github.com/Microsoft/DirectXTK).</span><span class="sxs-lookup"><span data-stu-id="dc1c5-109">For a full-featured DDS file reader, writer, and texture processing pipeline, see [DirectXTex](https://github.com/Microsoft/DirectXTex) and [DirectXTK](https://github.com/Microsoft/DirectXTK).</span></span>

 

<span data-ttu-id="dc1c5-110">В конце этого раздела вы найдете полный пример кода.</span><span class="sxs-lookup"><span data-stu-id="dc1c5-110">At the end of this topic, you'll find the full example code.</span></span> <span data-ttu-id="dc1c5-111">В разделе описываются части примера кода, который создает текстуру и представление.</span><span class="sxs-lookup"><span data-stu-id="dc1c5-111">The topic describes the parts of the example code that create the texture and the view.</span></span>

<span data-ttu-id="dc1c5-112">**Для инициализации текстуры и представления отдельно.**</span><span class="sxs-lookup"><span data-stu-id="dc1c5-112">**To initialize a texture and view separately.**</span></span>

1.  <span data-ttu-id="dc1c5-113">Вызовите [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) , чтобы создать интерфейс фабрики изображений ([**IWICImagingFactory**](/windows/desktop/api/wincodec/nn-wincodec-iwicimagingfactory)).</span><span class="sxs-lookup"><span data-stu-id="dc1c5-113">Call [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) to create the imaging factory interface ([**IWICImagingFactory**](/windows/desktop/api/wincodec/nn-wincodec-iwicimagingfactory)).</span></span>
2.  <span data-ttu-id="dc1c5-114">Вызовите метод [**IWICImagingFactory:: креатедекодерфромфиленаме**](/windows/desktop/api/wincodec/nf-wincodec-iwicimagingfactory-createdecoderfromfilename) , чтобы создать объект [**ивикбитмапдекодер**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapdecoder) на основе имени файла изображения.</span><span class="sxs-lookup"><span data-stu-id="dc1c5-114">Call the [**IWICImagingFactory::CreateDecoderFromFilename**](/windows/desktop/api/wincodec/nf-wincodec-iwicimagingfactory-createdecoderfromfilename) method to create a [**IWICBitmapDecoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapdecoder) object from an image file name.</span></span>
3.  <span data-ttu-id="dc1c5-115">Вызовите метод [**ивикбитмапдекодер:: noframes**](/windows/desktop/api/wincodec/nf-wincodec-iwicbitmapdecoder-getframe) , чтобы получить интерфейс [**IWICBitmapFrameDecode**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapframedecode) для кадра изображения.</span><span class="sxs-lookup"><span data-stu-id="dc1c5-115">Call the [**IWICBitmapDecoder::GetFrame**](/windows/desktop/api/wincodec/nf-wincodec-iwicbitmapdecoder-getframe) method to retrieve the [**IWICBitmapFrameDecode**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapframedecode) interface for the frame of the image.</span></span>
4.  <span data-ttu-id="dc1c5-116">Вызовите метод [**IWICBitmapSource:: жетпикселформат**](/windows/desktop/api/wincodec/nf-wincodec-iwicbitmapsource-getpixelformat) (интерфейс [**IWICBitmapFrameDecode**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapframedecode) наследует от [**IWICBitmapSource**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapsource)), чтобы получить формат пикселей изображения.</span><span class="sxs-lookup"><span data-stu-id="dc1c5-116">Call the [**IWICBitmapSource::GetPixelFormat**](/windows/desktop/api/wincodec/nf-wincodec-iwicbitmapsource-getpixelformat) method ([**IWICBitmapFrameDecode**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapframedecode) interface inherits from [**IWICBitmapSource**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapsource)) to get the pixel format of the image.</span></span>
5.  <span data-ttu-id="dc1c5-117">Преобразуйте формат пикселей в тип [**\_ формата DXGI**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) в соответствии с этой таблицей:</span><span class="sxs-lookup"><span data-stu-id="dc1c5-117">Convert the pixel format to a [**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) type according to this table:</span></span>

    | <span data-ttu-id="dc1c5-118">Формат пикселей WIC</span><span class="sxs-lookup"><span data-stu-id="dc1c5-118">WIC pixel format</span></span>                                  | <span data-ttu-id="dc1c5-119">Эквивалентный [ **\_ Формат DXGI**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)</span><span class="sxs-lookup"><span data-stu-id="dc1c5-119">Equivalent [**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)</span></span> |
    |---------------------------------------------------|---------------------------------------------------------|
    | <span data-ttu-id="dc1c5-120">GUID \_ WICPixelFormat128bppRGBAFloat</span><span class="sxs-lookup"><span data-stu-id="dc1c5-120">GUID\_WICPixelFormat128bppRGBAFloat</span></span>               | <span data-ttu-id="dc1c5-121">\_Формат DXGI \_ R32G32B32A32 \_ float</span><span class="sxs-lookup"><span data-stu-id="dc1c5-121">DXGI\_FORMAT\_R32G32B32A32\_FLOAT</span></span>                       |
    | <span data-ttu-id="dc1c5-122">GUID \_ WICPixelFormat64bppRGBAHalf</span><span class="sxs-lookup"><span data-stu-id="dc1c5-122">GUID\_WICPixelFormat64bppRGBAHalf</span></span>                 | <span data-ttu-id="dc1c5-123">\_Формат DXGI \_ R16G16B16A16 \_ float</span><span class="sxs-lookup"><span data-stu-id="dc1c5-123">DXGI\_FORMAT\_R16G16B16A16\_FLOAT</span></span>                       |
    | <span data-ttu-id="dc1c5-124">GUID \_ WICPixelFormat64bppRGBA</span><span class="sxs-lookup"><span data-stu-id="dc1c5-124">GUID\_WICPixelFormat64bppRGBA</span></span>                     | <span data-ttu-id="dc1c5-125">\_Формат DXGI \_ R16G16B16A16 \_ UNORM</span><span class="sxs-lookup"><span data-stu-id="dc1c5-125">DXGI\_FORMAT\_R16G16B16A16\_UNORM</span></span>                       |
    | <span data-ttu-id="dc1c5-126">GUID \_ WICPixelFormat32bppRGBA</span><span class="sxs-lookup"><span data-stu-id="dc1c5-126">GUID\_WICPixelFormat32bppRGBA</span></span>                     | <span data-ttu-id="dc1c5-127">\_Формат DXGI \_ R8G8B8A8 \_ UNORM</span><span class="sxs-lookup"><span data-stu-id="dc1c5-127">DXGI\_FORMAT\_R8G8B8A8\_UNORM</span></span>                           |
    | <span data-ttu-id="dc1c5-128">GUID \_ WICPixelFormat32bppBGRA</span><span class="sxs-lookup"><span data-stu-id="dc1c5-128">GUID\_WICPixelFormat32bppBGRA</span></span>                     | <span data-ttu-id="dc1c5-129">\_Формат DXGI \_ B8G8R8A8 \_ UNORM (DXGI 1,1)</span><span class="sxs-lookup"><span data-stu-id="dc1c5-129">DXGI\_FORMAT\_B8G8R8A8\_UNORM (DXGI 1.1)</span></span>                |
    | <span data-ttu-id="dc1c5-130">GUID \_ WICPixelFormat32bppBGR</span><span class="sxs-lookup"><span data-stu-id="dc1c5-130">GUID\_WICPixelFormat32bppBGR</span></span>                      | <span data-ttu-id="dc1c5-131">\_Формат DXGI \_ B8G8R8X8 \_ UNORM (DXGI 1,1)</span><span class="sxs-lookup"><span data-stu-id="dc1c5-131">DXGI\_FORMAT\_B8G8R8X8\_UNORM (DXGI 1.1)</span></span>                |
    | <span data-ttu-id="dc1c5-132">GUID \_ WICPixelFormat32bppRGBA1010102XR</span><span class="sxs-lookup"><span data-stu-id="dc1c5-132">GUID\_WICPixelFormat32bppRGBA1010102XR</span></span>            | <span data-ttu-id="dc1c5-133">\_Формат DXGI \_ R10G10B10 \_ XR \_ смещение \_ a2 \_ UNORM (DXGI 1,1)</span><span class="sxs-lookup"><span data-stu-id="dc1c5-133">DXGI\_FORMAT\_R10G10B10\_XR\_BIAS\_A2\_UNORM (DXGI 1.1)</span></span> |
    | <span data-ttu-id="dc1c5-134">GUID \_ WICPixelFormat32bppRGBA1010102</span><span class="sxs-lookup"><span data-stu-id="dc1c5-134">GUID\_WICPixelFormat32bppRGBA1010102</span></span>              | <span data-ttu-id="dc1c5-135">\_Формат DXGI \_ R10G10B10A2 \_ UNORM</span><span class="sxs-lookup"><span data-stu-id="dc1c5-135">DXGI\_FORMAT\_R10G10B10A2\_UNORM</span></span>                        |
    | <span data-ttu-id="dc1c5-136">GUID \_ WICPixelFormat32bppRGBE</span><span class="sxs-lookup"><span data-stu-id="dc1c5-136">GUID\_WICPixelFormat32bppRGBE</span></span>                     | <span data-ttu-id="dc1c5-137">\_Формат DXGI \_ R9G9B9E5 \_ шаредексп</span><span class="sxs-lookup"><span data-stu-id="dc1c5-137">DXGI\_FORMAT\_R9G9B9E5\_SHAREDEXP</span></span>                       |
    | <span data-ttu-id="dc1c5-138">GUID \_ WICPixelFormat16bppBGRA5551</span><span class="sxs-lookup"><span data-stu-id="dc1c5-138">GUID\_WICPixelFormat16bppBGRA5551</span></span>                 | <span data-ttu-id="dc1c5-139">\_Формат DXGI \_ B5G5R5A1 \_ UNORM (DXGI 1,2)</span><span class="sxs-lookup"><span data-stu-id="dc1c5-139">DXGI\_FORMAT\_B5G5R5A1\_UNORM (DXGI 1.2)</span></span>                |
    | <span data-ttu-id="dc1c5-140">GUID \_ WICPixelFormat16bppBGR565</span><span class="sxs-lookup"><span data-stu-id="dc1c5-140">GUID\_WICPixelFormat16bppBGR565</span></span>                   | <span data-ttu-id="dc1c5-141">\_Формат DXGI \_ B5G6R5 \_ UNORM (DXGI 1,2)</span><span class="sxs-lookup"><span data-stu-id="dc1c5-141">DXGI\_FORMAT\_B5G6R5\_UNORM (DXGI 1.2)</span></span>                  |
    | <span data-ttu-id="dc1c5-142">GUID \_ WICPixelFormat32bppGrayFloat</span><span class="sxs-lookup"><span data-stu-id="dc1c5-142">GUID\_WICPixelFormat32bppGrayFloat</span></span>                | <span data-ttu-id="dc1c5-143">\_Формат DXGI \_ R32 \_ float\*</span><span class="sxs-lookup"><span data-stu-id="dc1c5-143">DXGI\_FORMAT\_R32\_FLOAT\*</span></span>                              |
    | <span data-ttu-id="dc1c5-144">GUID \_ WICPixelFormat16bppGrayHalf</span><span class="sxs-lookup"><span data-stu-id="dc1c5-144">GUID\_WICPixelFormat16bppGrayHalf</span></span>                 | <span data-ttu-id="dc1c5-145">\_Формат DXGI \_ R16 \_ float\*</span><span class="sxs-lookup"><span data-stu-id="dc1c5-145">DXGI\_FORMAT\_R16\_FLOAT\*</span></span>                              |
    | <span data-ttu-id="dc1c5-146">GUID \_ WICPixelFormat16bppGray</span><span class="sxs-lookup"><span data-stu-id="dc1c5-146">GUID\_WICPixelFormat16bppGray</span></span>                     | <span data-ttu-id="dc1c5-147">\_Формат DXGI \_ R16 \_ UNORM\*</span><span class="sxs-lookup"><span data-stu-id="dc1c5-147">DXGI\_FORMAT\_R16\_UNORM\*</span></span>                              |
    | <span data-ttu-id="dc1c5-148">GUID \_ WICPixelFormat8bppGray</span><span class="sxs-lookup"><span data-stu-id="dc1c5-148">GUID\_WICPixelFormat8bppGray</span></span>                      | <span data-ttu-id="dc1c5-149">\_Формат DXGI \_ R8 \_ UNORM\*</span><span class="sxs-lookup"><span data-stu-id="dc1c5-149">DXGI\_FORMAT\_R8\_UNORM\*</span></span>                               |
    | <span data-ttu-id="dc1c5-150">GUID \_ WICPixelFormat8bppAlpha</span><span class="sxs-lookup"><span data-stu-id="dc1c5-150">GUID\_WICPixelFormat8bppAlpha</span></span>                     | <span data-ttu-id="dc1c5-151">\_Формат DXGI \_ a8 \_ UNORM</span><span class="sxs-lookup"><span data-stu-id="dc1c5-151">DXGI\_FORMAT\_A8\_UNORM</span></span>                                 |
    | <span data-ttu-id="dc1c5-152">GUID \_ WICPixelFormat96bppRGBFloat (компонент WIC для Windows 8)</span><span class="sxs-lookup"><span data-stu-id="dc1c5-152">GUID\_WICPixelFormat96bppRGBFloat (Windows 8 WIC)</span></span> | <span data-ttu-id="dc1c5-153">\_Формат DXGI \_ R32G32B32 \_ float</span><span class="sxs-lookup"><span data-stu-id="dc1c5-153">DXGI\_FORMAT\_R32G32B32\_FLOAT</span></span>                          |

    

     

    <span data-ttu-id="dc1c5-154">\* Одноканальные форматы DXGI — это все красные каналы, поэтому для их отображения в виде градаций серого требуется HLSL шейдер свиззлес, например. РРР.</span><span class="sxs-lookup"><span data-stu-id="dc1c5-154">\* The single-channel DXGI formats are all red channel, so you need HLSL shader swizzles such as .rrr to render these as grayscale.</span></span>

6.  <span data-ttu-id="dc1c5-155">Вызовите метод [**IWICBitmapSource:: CopyPixels**](/windows/desktop/api/wincodec/nf-wincodec-iwicbitmapsource-copypixels) , чтобы скопировать Пиксели изображения в буфер.</span><span class="sxs-lookup"><span data-stu-id="dc1c5-155">Call the [**IWICBitmapSource::CopyPixels**](/windows/desktop/api/wincodec/nf-wincodec-iwicbitmapsource-copypixels) method to copy the image pixels into a buffer.</span></span> <span data-ttu-id="dc1c5-156">Используйте тип [**\_ формата DXGI**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) и буфер для инициализации ресурса двухмерной текстуры и объекта построителя текстуры-Resource-View.</span><span class="sxs-lookup"><span data-stu-id="dc1c5-156">Use the [**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) type and the buffer to initialize the 2D texture resource and shader-resource-view object.</span></span>
7.  <span data-ttu-id="dc1c5-157">Вызовите метод [**ID3D11Device:: CreateTexture2D**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createtexture2d) для инициализации ресурса текстуры 2D.</span><span class="sxs-lookup"><span data-stu-id="dc1c5-157">Call the [**ID3D11Device::CreateTexture2D**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createtexture2d) method to initialize the 2D texture resource.</span></span> <span data-ttu-id="dc1c5-158">В этом вызове передайте адрес указателя интерфейса [**ID3D11Texture2D**](/windows/desktop/api/D3D11/nn-d3d11-id3d11texture2d) .</span><span class="sxs-lookup"><span data-stu-id="dc1c5-158">In this call, pass the address of an [**ID3D11Texture2D**](/windows/desktop/api/D3D11/nn-d3d11-id3d11texture2d) interface pointer.</span></span>

    ```C++
        // Create texture
        D3D11_TEXTURE2D_DESC desc;
        desc.Width = width;
        desc.Height = height;
        desc.MipLevels = 1;
        desc.ArraySize = 1;
        desc.Format = format;
        desc.SampleDesc.Count = 1;
        desc.SampleDesc.Quality = 0;
        desc.Usage = D3D11_USAGE_DEFAULT;
        desc.BindFlags = D3D11_BIND_SHADER_RESOURCE;
        desc.CPUAccessFlags = 0;
        desc.MiscFlags = 0;

        D3D11_SUBRESOURCE_DATA initData;
        initData.pSysMem = temp.get();
        initData.SysMemPitch = static_cast<UINT>( rowPitch );
        initData.SysMemSlicePitch = static_cast<UINT>( imageSize );

        ID3D11Texture2D* tex = nullptr;
        hr = d3dDevice->CreateTexture2D( &desc, &initData, &tex );
    
    ```

    

8.  <span data-ttu-id="dc1c5-159">Вызовите метод [**ID3D11Device:: креатешадерресаурцевиев**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createshaderresourceview) , чтобы инициализировать объект Shader-Resource-View.</span><span class="sxs-lookup"><span data-stu-id="dc1c5-159">Call the [**ID3D11Device::CreateShaderResourceView**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createshaderresourceview) method to initialize a shader-resource-view object.</span></span> <span data-ttu-id="dc1c5-160">Передайте **пустое** описание (для получения представления с параметрами по умолчанию) или его описание (для получения представления с параметрами, отличными **от значений по** умолчанию).</span><span class="sxs-lookup"><span data-stu-id="dc1c5-160">Pass either a **NULL** shader-resource-view description (to get a view with default parameters) or a non-**NULL** shader-resource-view description (to get a view with non-default parameters).</span></span> <span data-ttu-id="dc1c5-161">При необходимости определите тип текстуры, вызвав [**ID3D11Resource:: GetType**](/windows/desktop/api/D3D11/nf-d3d11-id3d11resource-gettype) и формат текстуры, вызвав [**ID3D11ShaderResourceView:: DESC**](/windows/desktop/api/D3D11/nf-d3d11-id3d11shaderresourceview-getdesc).</span><span class="sxs-lookup"><span data-stu-id="dc1c5-161">If necessary, determine the texture type by calling [**ID3D11Resource::GetType**](/windows/desktop/api/D3D11/nf-d3d11-id3d11resource-gettype) and the texture format by calling [**ID3D11ShaderResourceView::GetDesc**](/windows/desktop/api/D3D11/nf-d3d11-id3d11shaderresourceview-getdesc).</span></span>
    ```C++
        if ( SUCCEEDED(hr) && tex != 0 )
        {
            if (textureView != 0)
            {
                D3D11_SHADER_RESOURCE_VIEW_DESC SRVDesc;
                memset( &SRVDesc, 0, sizeof( SRVDesc ) );
                SRVDesc.Format = format;
                SRVDesc.ViewDimension = D3D11_SRV_DIMENSION_TEXTURE2D;
                SRVDesc.Texture2D.MipLevels = 1;

                hr = d3dDevice->CreateShaderResourceView( tex, &SRVDesc, textureView );
                if ( FAILED(hr) )
                {
                    tex->Release();
                    return hr;
                }
            }
       }
    ```

    

<span data-ttu-id="dc1c5-162">В предыдущем примере кода предполагается, что переменная *d3dDevice* является объектом [**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device) , который ранее был инициализирован.</span><span class="sxs-lookup"><span data-stu-id="dc1c5-162">The preceding example code assumes that the *d3dDevice* variable is an [**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device) object that has been previously initialized.</span></span>

<span data-ttu-id="dc1c5-163">Ниже приведен заголовок, который можно включить в приложение.</span><span class="sxs-lookup"><span data-stu-id="dc1c5-163">Here is the header that you can include in your app.</span></span> <span data-ttu-id="dc1c5-164">В заголовке объявляются функции **креатевиктекстурефромфиле** и **креатевиктекстурефроммемори** , которые можно вызывать в приложении для создания текстуры из файла и из памяти.</span><span class="sxs-lookup"><span data-stu-id="dc1c5-164">The header declares the **CreateWICTextureFromFile** and **CreateWICTextureFromMemory** functions that you can call in your app to create a texture from a file and from memory.</span></span>


```C++
//--------------------------------------------------------------------------------------
// File: WICTextureLoader.h
//
// Function for loading a WIC image and creating a Direct3D 11 runtime texture for it
// (auto-generating mipmaps if possible)
//
// Note: Assumes application has already called CoInitializeEx
//
// Warning: CreateWICTexture* functions are not thread-safe if given a d3dContext instance for
//          auto-gen mipmap support.
//
// Note these functions are useful for images created as simple 2D textures. For
// more complex resources, DDSTextureLoader is an excellent light-weight runtime loader.
// For a full-featured DDS file reader, writer, and texture processing pipeline see
// the 'Texconv' sample and the 'DirectXTex' library.
//
// THIS CODE AND INFORMATION IS PROVIDED "AS IS" WITHOUT WARRANTY OF
// ANY KIND, EITHER EXPRESSED OR IMPLIED, INCLUDING BUT NOT LIMITED TO
// THE IMPLIED WARRANTIES OF MERCHANTABILITY AND/OR FITNESS FOR A
// PARTICULAR PURPOSE.
//
// Copyright (c) Microsoft Corporation. All rights reserved.
//
// https://go.microsoft.com/fwlink/?LinkId=248926
// https://go.microsoft.com/fwlink/?LinkId=248929
//--------------------------------------------------------------------------------------

#ifdef _MSC_VER
#pragma once
#endif

#include <d3d11.h>

#pragma warning(push)
#pragma warning(disable : 4005)
#include <stdint.h>
#pragma warning(pop)

HRESULT CreateWICTextureFromMemory( _In_ ID3D11Device* d3dDevice,
                                    _In_opt_ ID3D11DeviceContext* d3dContext,
                                    _In_bytecount_(wicDataSize) const uint8_t* wicData,
                                    _In_ size_t wicDataSize,
                                    _Out_opt_ ID3D11Resource** texture,
                                    _Out_opt_ ID3D11ShaderResourceView** textureView,
                                    _In_ size_t maxsize = 0
                                  );

HRESULT CreateWICTextureFromFile( _In_ ID3D11Device* d3dDevice,
                                  _In_opt_ ID3D11DeviceContext* d3dContext,
                                  _In_z_ const wchar_t* szFileName,
                                  _Out_opt_ ID3D11Resource** texture,
                                  _Out_opt_ ID3D11ShaderResourceView** textureView,
                                  _In_ size_t maxsize = 0
                                );
```



<span data-ttu-id="dc1c5-165">Ниже приведен полный источник, который можно использовать в приложении.</span><span class="sxs-lookup"><span data-stu-id="dc1c5-165">Here is the full source that you can use in your app.</span></span> <span data-ttu-id="dc1c5-166">В источнике реализованы функции **креатевиктекстурефромфиле** и **креатевиктекстурефроммемори** .</span><span class="sxs-lookup"><span data-stu-id="dc1c5-166">The source implements the **CreateWICTextureFromFile** and **CreateWICTextureFromMemory** functions.</span></span>


```C++
//--------------------------------------------------------------------------------------
// File: WICTextureLoader.cpp
//
// Function for loading a WIC image and creating a Direct3D 11 runtime texture for it
// (auto-generating mipmaps if possible)
//
// Note: Assumes application has already called CoInitializeEx
//
// Warning: CreateWICTexture* functions are not thread-safe if given a d3dContext instance for
//          auto-gen mipmap support.
//
// Note these functions are useful for images created as simple 2D textures. For
// more complex resources, DDSTextureLoader is an excellent light-weight runtime loader.
// For a full-featured DDS file reader, writer, and texture processing pipeline see
// the 'Texconv' sample and the 'DirectXTex' library.
//
// THIS CODE AND INFORMATION IS PROVIDED "AS IS" WITHOUT WARRANTY OF
// ANY KIND, EITHER EXPRESSED OR IMPLIED, INCLUDING BUT NOT LIMITED TO
// THE IMPLIED WARRANTIES OF MERCHANTABILITY AND/OR FITNESS FOR A
// PARTICULAR PURPOSE.
//
// Copyright (c) Microsoft Corporation. All rights reserved.
//
// https://go.microsoft.com/fwlink/?LinkId=248926
// https://go.microsoft.com/fwlink/?LinkId=248929
//--------------------------------------------------------------------------------------

// We could load multi-frame images (TIFF/GIF) into a texture array.
// For now, we just load the first frame (note: DirectXTex supports multi-frame images)

#include <dxgiformat.h>
#include <assert.h>

#pragma warning(push)
#pragma warning(disable : 4005)
#include <wincodec.h>
#pragma warning(pop)

#include <memory>

#include "WICTextureLoader.h"

#if (_WIN32_WINNT >= 0x0602 /*_WIN32_WINNT_WIN8*/) && !defined(DXGI_1_2_FORMATS)
#define DXGI_1_2_FORMATS
#endif

//---------------------------------------------------------------------------------
template<class T> class ScopedObject
{
public:
    explicit ScopedObject( T *p = 0 ) : _pointer(p) {}
    ~ScopedObject()
    {
        if ( _pointer )
        {
            _pointer->Release();
            _pointer = nullptr;
        }
    }

    bool IsNull() const { return (!_pointer); }

    T& operator*() { return *_pointer; }
    T* operator->() { return _pointer; }
    T** operator&() { return &_pointer; }

    void Reset(T *p = 0) { if ( _pointer ) { _pointer->Release(); } _pointer = p; }

    T* Get() const { return _pointer; }

private:
    ScopedObject(const ScopedObject&);
    ScopedObject& operator=(const ScopedObject&);
        
    T* _pointer;
};

//-------------------------------------------------------------------------------------
// WIC Pixel Format Translation Data
//-------------------------------------------------------------------------------------
struct WICTranslate
{
    GUID                wic;
    DXGI_FORMAT         format;
};

static WICTranslate g_WICFormats[] = 
{
    { GUID_WICPixelFormat128bppRGBAFloat,       DXGI_FORMAT_R32G32B32A32_FLOAT },

    { GUID_WICPixelFormat64bppRGBAHalf,         DXGI_FORMAT_R16G16B16A16_FLOAT },
    { GUID_WICPixelFormat64bppRGBA,             DXGI_FORMAT_R16G16B16A16_UNORM },

    { GUID_WICPixelFormat32bppRGBA,             DXGI_FORMAT_R8G8B8A8_UNORM },
    { GUID_WICPixelFormat32bppBGRA,             DXGI_FORMAT_B8G8R8A8_UNORM }, // DXGI 1.1
    { GUID_WICPixelFormat32bppBGR,              DXGI_FORMAT_B8G8R8X8_UNORM }, // DXGI 1.1

    { GUID_WICPixelFormat32bppRGBA1010102XR,    DXGI_FORMAT_R10G10B10_XR_BIAS_A2_UNORM }, // DXGI 1.1
    { GUID_WICPixelFormat32bppRGBA1010102,      DXGI_FORMAT_R10G10B10A2_UNORM },
    { GUID_WICPixelFormat32bppRGBE,             DXGI_FORMAT_R9G9B9E5_SHAREDEXP },

#ifdef DXGI_1_2_FORMATS

    { GUID_WICPixelFormat16bppBGRA5551,         DXGI_FORMAT_B5G5R5A1_UNORM },
    { GUID_WICPixelFormat16bppBGR565,           DXGI_FORMAT_B5G6R5_UNORM },

#endif // DXGI_1_2_FORMATS

    { GUID_WICPixelFormat32bppGrayFloat,        DXGI_FORMAT_R32_FLOAT },
    { GUID_WICPixelFormat16bppGrayHalf,         DXGI_FORMAT_R16_FLOAT },
    { GUID_WICPixelFormat16bppGray,             DXGI_FORMAT_R16_UNORM },
    { GUID_WICPixelFormat8bppGray,              DXGI_FORMAT_R8_UNORM },

    { GUID_WICPixelFormat8bppAlpha,             DXGI_FORMAT_A8_UNORM },

#if (_WIN32_WINNT >= 0x0602 /*_WIN32_WINNT_WIN8*/)
    { GUID_WICPixelFormat96bppRGBFloat,         DXGI_FORMAT_R32G32B32_FLOAT },
#endif
};

//-------------------------------------------------------------------------------------
// WIC Pixel Format nearest conversion table
//-------------------------------------------------------------------------------------

struct WICConvert
{
    GUID        source;
    GUID        target;
};

static WICConvert g_WICConvert[] = 
{
    // Note target GUID in this conversion table must be one of those directly supported formats (above).

    { GUID_WICPixelFormatBlackWhite,            GUID_WICPixelFormat8bppGray }, // DXGI_FORMAT_R8_UNORM

    { GUID_WICPixelFormat1bppIndexed,           GUID_WICPixelFormat32bppRGBA }, // DXGI_FORMAT_R8G8B8A8_UNORM 
    { GUID_WICPixelFormat2bppIndexed,           GUID_WICPixelFormat32bppRGBA }, // DXGI_FORMAT_R8G8B8A8_UNORM 
    { GUID_WICPixelFormat4bppIndexed,           GUID_WICPixelFormat32bppRGBA }, // DXGI_FORMAT_R8G8B8A8_UNORM 
    { GUID_WICPixelFormat8bppIndexed,           GUID_WICPixelFormat32bppRGBA }, // DXGI_FORMAT_R8G8B8A8_UNORM 

    { GUID_WICPixelFormat2bppGray,              GUID_WICPixelFormat8bppGray }, // DXGI_FORMAT_R8_UNORM 
    { GUID_WICPixelFormat4bppGray,              GUID_WICPixelFormat8bppGray }, // DXGI_FORMAT_R8_UNORM 

    { GUID_WICPixelFormat16bppGrayFixedPoint,   GUID_WICPixelFormat16bppGrayHalf }, // DXGI_FORMAT_R16_FLOAT 
    { GUID_WICPixelFormat32bppGrayFixedPoint,   GUID_WICPixelFormat32bppGrayFloat }, // DXGI_FORMAT_R32_FLOAT 

#ifdef DXGI_1_2_FORMATS

    { GUID_WICPixelFormat16bppBGR555,           GUID_WICPixelFormat16bppBGRA5551 }, // DXGI_FORMAT_B5G5R5A1_UNORM

#else

    { GUID_WICPixelFormat16bppBGR555,           GUID_WICPixelFormat32bppRGBA }, // DXGI_FORMAT_R8G8B8A8_UNORM
    { GUID_WICPixelFormat16bppBGRA5551,         GUID_WICPixelFormat32bppRGBA }, // DXGI_FORMAT_R8G8B8A8_UNORM
    { GUID_WICPixelFormat16bppBGR565,           GUID_WICPixelFormat32bppRGBA }, // DXGI_FORMAT_R8G8B8A8_UNORM

#endif // DXGI_1_2_FORMATS

    { GUID_WICPixelFormat32bppBGR101010,        GUID_WICPixelFormat32bppRGBA1010102 }, // DXGI_FORMAT_R10G10B10A2_UNORM

    { GUID_WICPixelFormat24bppBGR,              GUID_WICPixelFormat32bppRGBA }, // DXGI_FORMAT_R8G8B8A8_UNORM 
    { GUID_WICPixelFormat24bppRGB,              GUID_WICPixelFormat32bppRGBA }, // DXGI_FORMAT_R8G8B8A8_UNORM 
    { GUID_WICPixelFormat32bppPBGRA,            GUID_WICPixelFormat32bppRGBA }, // DXGI_FORMAT_R8G8B8A8_UNORM 
    { GUID_WICPixelFormat32bppPRGBA,            GUID_WICPixelFormat32bppRGBA }, // DXGI_FORMAT_R8G8B8A8_UNORM 

    { GUID_WICPixelFormat48bppRGB,              GUID_WICPixelFormat64bppRGBA }, // DXGI_FORMAT_R16G16B16A16_UNORM
    { GUID_WICPixelFormat48bppBGR,              GUID_WICPixelFormat64bppRGBA }, // DXGI_FORMAT_R16G16B16A16_UNORM
    { GUID_WICPixelFormat64bppBGRA,             GUID_WICPixelFormat64bppRGBA }, // DXGI_FORMAT_R16G16B16A16_UNORM
    { GUID_WICPixelFormat64bppPRGBA,            GUID_WICPixelFormat64bppRGBA }, // DXGI_FORMAT_R16G16B16A16_UNORM
    { GUID_WICPixelFormat64bppPBGRA,            GUID_WICPixelFormat64bppRGBA }, // DXGI_FORMAT_R16G16B16A16_UNORM

    { GUID_WICPixelFormat48bppRGBFixedPoint,    GUID_WICPixelFormat64bppRGBAHalf }, // DXGI_FORMAT_R16G16B16A16_FLOAT 
    { GUID_WICPixelFormat48bppBGRFixedPoint,    GUID_WICPixelFormat64bppRGBAHalf }, // DXGI_FORMAT_R16G16B16A16_FLOAT 
    { GUID_WICPixelFormat64bppRGBAFixedPoint,   GUID_WICPixelFormat64bppRGBAHalf }, // DXGI_FORMAT_R16G16B16A16_FLOAT 
    { GUID_WICPixelFormat64bppBGRAFixedPoint,   GUID_WICPixelFormat64bppRGBAHalf }, // DXGI_FORMAT_R16G16B16A16_FLOAT 
    { GUID_WICPixelFormat64bppRGBFixedPoint,    GUID_WICPixelFormat64bppRGBAHalf }, // DXGI_FORMAT_R16G16B16A16_FLOAT 
    { GUID_WICPixelFormat64bppRGBHalf,          GUID_WICPixelFormat64bppRGBAHalf }, // DXGI_FORMAT_R16G16B16A16_FLOAT 
    { GUID_WICPixelFormat48bppRGBHalf,          GUID_WICPixelFormat64bppRGBAHalf }, // DXGI_FORMAT_R16G16B16A16_FLOAT 

    { GUID_WICPixelFormat96bppRGBFixedPoint,    GUID_WICPixelFormat128bppRGBAFloat }, // DXGI_FORMAT_R32G32B32A32_FLOAT 
    { GUID_WICPixelFormat128bppPRGBAFloat,      GUID_WICPixelFormat128bppRGBAFloat }, // DXGI_FORMAT_R32G32B32A32_FLOAT 
    { GUID_WICPixelFormat128bppRGBFloat,        GUID_WICPixelFormat128bppRGBAFloat }, // DXGI_FORMAT_R32G32B32A32_FLOAT 
    { GUID_WICPixelFormat128bppRGBAFixedPoint,  GUID_WICPixelFormat128bppRGBAFloat }, // DXGI_FORMAT_R32G32B32A32_FLOAT 
    { GUID_WICPixelFormat128bppRGBFixedPoint,   GUID_WICPixelFormat128bppRGBAFloat }, // DXGI_FORMAT_R32G32B32A32_FLOAT 

    { GUID_WICPixelFormat32bppCMYK,             GUID_WICPixelFormat32bppRGBA }, // DXGI_FORMAT_R8G8B8A8_UNORM 
    { GUID_WICPixelFormat64bppCMYK,             GUID_WICPixelFormat64bppRGBA }, // DXGI_FORMAT_R16G16B16A16_UNORM
    { GUID_WICPixelFormat40bppCMYKAlpha,        GUID_WICPixelFormat64bppRGBA }, // DXGI_FORMAT_R16G16B16A16_UNORM
    { GUID_WICPixelFormat80bppCMYKAlpha,        GUID_WICPixelFormat64bppRGBA }, // DXGI_FORMAT_R16G16B16A16_UNORM

#if (_WIN32_WINNT >= 0x0602 /*_WIN32_WINNT_WIN8*/)
    { GUID_WICPixelFormat32bppRGB,              GUID_WICPixelFormat32bppRGBA }, // DXGI_FORMAT_R8G8B8A8_UNORM
    { GUID_WICPixelFormat64bppRGB,              GUID_WICPixelFormat64bppRGBA }, // DXGI_FORMAT_R16G16B16A16_UNORM
    { GUID_WICPixelFormat64bppPRGBAHalf,        GUID_WICPixelFormat64bppRGBAHalf }, // DXGI_FORMAT_R16G16B16A16_FLOAT 
#endif

    // We don't support n-channel formats
};

//--------------------------------------------------------------------------------------
static IWICImagingFactory* _GetWIC()
{
    static IWICImagingFactory* s_Factory = nullptr;

    if ( s_Factory )
        return s_Factory;

    HRESULT hr = CoCreateInstance(
        CLSID_WICImagingFactory,
        nullptr,
        CLSCTX_INPROC_SERVER,
        __uuidof(IWICImagingFactory),
        (LPVOID*)&s_Factory
        );

    if ( FAILED(hr) )
    {
        s_Factory = nullptr;
        return nullptr;
    }

    return s_Factory;
}

//---------------------------------------------------------------------------------
static DXGI_FORMAT _WICToDXGI( const GUID& guid )
{
    for( size_t i=0; i < _countof(g_WICFormats); ++i )
    {
        if ( memcmp( &g_WICFormats[i].wic, &guid, sizeof(GUID) ) == 0 )
            return g_WICFormats[i].format;
    }

    return DXGI_FORMAT_UNKNOWN;
}

//---------------------------------------------------------------------------------
static size_t _WICBitsPerPixel( REFGUID targetGuid )
{
    IWICImagingFactory* pWIC = _GetWIC();
    if ( !pWIC )
        return 0;
 
    ScopedObject<IWICComponentInfo> cinfo;
    if ( FAILED( pWIC->CreateComponentInfo( targetGuid, &cinfo ) ) )
        return 0;

    WICComponentType type;
    if ( FAILED( cinfo->GetComponentType( &type ) ) )
        return 0;

    if ( type != WICPixelFormat )
        return 0;

    ScopedObject<IWICPixelFormatInfo> pfinfo;
    if ( FAILED( cinfo->QueryInterface( __uuidof(IWICPixelFormatInfo), reinterpret_cast<void**>( &pfinfo )  ) ) )
        return 0;

    UINT bpp;
    if ( FAILED( pfinfo->GetBitsPerPixel( &bpp ) ) )
        return 0;

    return bpp;
}

//---------------------------------------------------------------------------------
static HRESULT CreateTextureFromWIC( _In_ ID3D11Device* d3dDevice,
                                     _In_opt_ ID3D11DeviceContext* d3dContext,
                                     _In_ IWICBitmapFrameDecode *frame,
                                     _Out_opt_ ID3D11Resource** texture,
                                     _Out_opt_ ID3D11ShaderResourceView** textureView,
                                     _In_ size_t maxsize )
{
    UINT width, height;
    HRESULT hr = frame->GetSize( &width, &height );
    if ( FAILED(hr) )
        return hr;

    assert( width > 0 && height > 0 );

    if ( !maxsize )
    {
        // This is a bit conservative because the hardware could support larger textures than
        // the Feature Level defined minimums, but doing it this way is much easier and more
        // performant for WIC than the 'fail and retry' model used by DDSTextureLoader

        switch( d3dDevice->GetFeatureLevel() )
        {
            case D3D_FEATURE_LEVEL_9_1:
            case D3D_FEATURE_LEVEL_9_2:
                maxsize = 2048 /*D3D_FL9_1_REQ_TEXTURE2D_U_OR_V_DIMENSION*/;
                break;

            case D3D_FEATURE_LEVEL_9_3:
                maxsize = 4096 /*D3D_FL9_3_REQ_TEXTURE2D_U_OR_V_DIMENSION*/;
                break;

            case D3D_FEATURE_LEVEL_10_0:
            case D3D_FEATURE_LEVEL_10_1:
                maxsize = 8192 /*D3D10_REQ_TEXTURE2D_U_OR_V_DIMENSION*/;
                break;

            default:
                maxsize = D3D11_REQ_TEXTURE2D_U_OR_V_DIMENSION;
                break;
        }
    }

    assert( maxsize > 0 );

    UINT twidth, theight;
    if ( width > maxsize || height > maxsize )
    {
        float ar = static_cast<float>(height) / static_cast<float>(width);
        if ( width > height )
        {
            twidth = static_cast<UINT>( maxsize );
            theight = static_cast<UINT>( static_cast<float>(maxsize) * ar );
        }
        else
        {
            theight = static_cast<UINT>( maxsize );
            twidth = static_cast<UINT>( static_cast<float>(maxsize) / ar );
        }
        assert( twidth <= maxsize && theight <= maxsize );
    }
    else
    {
        twidth = width;
        theight = height;
    }

    // Determine format
    WICPixelFormatGUID pixelFormat;
    hr = frame->GetPixelFormat( &pixelFormat );
    if ( FAILED(hr) )
        return hr;

    WICPixelFormatGUID convertGUID;
    memcpy( &convertGUID, &pixelFormat, sizeof(WICPixelFormatGUID) );

    size_t bpp = 0;

    DXGI_FORMAT format = _WICToDXGI( pixelFormat );
    if ( format == DXGI_FORMAT_UNKNOWN )
    {
        for( size_t i=0; i < _countof(g_WICConvert); ++i )
        {
            if ( memcmp( &g_WICConvert[i].source, &pixelFormat, sizeof(WICPixelFormatGUID) ) == 0 )
            {
                memcpy( &convertGUID, &g_WICConvert[i].target, sizeof(WICPixelFormatGUID) );

                format = _WICToDXGI( g_WICConvert[i].target );
                assert( format != DXGI_FORMAT_UNKNOWN );
                bpp = _WICBitsPerPixel( convertGUID );
                break;
            }
        }

        if ( format == DXGI_FORMAT_UNKNOWN )
            return HRESULT_FROM_WIN32( ERROR_NOT_SUPPORTED );
    }
    else
    {
        bpp = _WICBitsPerPixel( pixelFormat );
    }

    if ( !bpp )
        return E_FAIL;

    // Verify our target format is supported by the current device
    // (handles WDDM 1.0 or WDDM 1.1 device driver cases as well as DirectX 11.0 Runtime without 16bpp format support)
    UINT support = 0;
    hr = d3dDevice->CheckFormatSupport( format, &support );
    if ( FAILED(hr) || !(support & D3D11_FORMAT_SUPPORT_TEXTURE2D) )
    {
        // Fallback to RGBA 32-bit format which is supported by all devices
        memcpy( &convertGUID, &GUID_WICPixelFormat32bppRGBA, sizeof(WICPixelFormatGUID) );
        format = DXGI_FORMAT_R8G8B8A8_UNORM;
        bpp = 32;
    }

    // Allocate temporary memory for image
    size_t rowPitch = ( twidth * bpp + 7 ) / 8;
    size_t imageSize = rowPitch * theight;

    std::unique_ptr<uint8_t[]> temp( new uint8_t[ imageSize ] );

    // Load image data
    if ( memcmp( &convertGUID, &pixelFormat, sizeof(GUID) ) == 0
         && twidth == width
         && theight == height )
    {
        // No format conversion or resize needed
        hr = frame->CopyPixels( 0, static_cast<UINT>( rowPitch ), static_cast<UINT>( imageSize ), temp.get() );  
        if ( FAILED(hr) )
            return hr;
    }
    else if ( twidth != width || theight != height )
    {
        // Resize
        IWICImagingFactory* pWIC = _GetWIC();
        if ( !pWIC )
            return E_NOINTERFACE;

        ScopedObject<IWICBitmapScaler> scaler;
        hr = pWIC->CreateBitmapScaler( &scaler );
        if ( FAILED(hr) )
            return hr;

        hr = scaler->Initialize( frame, twidth, theight, WICBitmapInterpolationModeFant );
        if ( FAILED(hr) )
            return hr;

        WICPixelFormatGUID pfScaler;
        hr = scaler->GetPixelFormat( &pfScaler );
        if ( FAILED(hr) )
            return hr;

        if ( memcmp( &convertGUID, &pfScaler, sizeof(GUID) ) == 0 )
        {
            // No format conversion needed
            hr = scaler->CopyPixels( 0, static_cast<UINT>( rowPitch ), static_cast<UINT>( imageSize ), temp.get() );  
            if ( FAILED(hr) )
                return hr;
        }
        else
        {
            ScopedObject<IWICFormatConverter> FC;
            hr = pWIC->CreateFormatConverter( &FC );
            if ( FAILED(hr) )
                return hr;

            hr = FC->Initialize( scaler.Get(), convertGUID, WICBitmapDitherTypeErrorDiffusion, 0, 0, WICBitmapPaletteTypeCustom );
            if ( FAILED(hr) )
                return hr;

            hr = FC->CopyPixels( 0, static_cast<UINT>( rowPitch ), static_cast<UINT>( imageSize ), temp.get() );  
            if ( FAILED(hr) )
                return hr;
        }
    }
    else
    {
        // Format conversion but no resize
        IWICImagingFactory* pWIC = _GetWIC();
        if ( !pWIC )
            return E_NOINTERFACE;

        ScopedObject<IWICFormatConverter> FC;
        hr = pWIC->CreateFormatConverter( &FC );
        if ( FAILED(hr) )
            return hr;

        hr = FC->Initialize( frame, convertGUID, WICBitmapDitherTypeErrorDiffusion, 0, 0, WICBitmapPaletteTypeCustom );
        if ( FAILED(hr) )
            return hr;

        hr = FC->CopyPixels( 0, static_cast<UINT>( rowPitch ), static_cast<UINT>( imageSize ), temp.get() );  
        if ( FAILED(hr) )
            return hr;
    }

    // See if format is supported for auto-gen mipmaps (varies by feature level)
    bool autogen = false;
    if ( d3dContext != 0 && textureView != 0 ) // Must have context and shader-view to auto generate mipmaps
    {
        UINT fmtSupport = 0;
        hr = d3dDevice->CheckFormatSupport( format, &fmtSupport );
        if ( SUCCEEDED(hr) && ( fmtSupport & D3D11_FORMAT_SUPPORT_MIP_AUTOGEN ) )
        {
            autogen = true;
        }
    }

    // Create texture
    D3D11_TEXTURE2D_DESC desc;
    desc.Width = twidth;
    desc.Height = theight;
    desc.MipLevels = (autogen) ? 0 : 1;
    desc.ArraySize = 1;
    desc.Format = format;
    desc.SampleDesc.Count = 1;
    desc.SampleDesc.Quality = 0;
    desc.Usage = D3D11_USAGE_DEFAULT;
    desc.BindFlags = (autogen) ? (D3D11_BIND_SHADER_RESOURCE | D3D11_BIND_RENDER_TARGET) : (D3D11_BIND_SHADER_RESOURCE);
    desc.CPUAccessFlags = 0;
    desc.MiscFlags = (autogen) ? D3D11_RESOURCE_MISC_GENERATE_MIPS : 0;

    D3D11_SUBRESOURCE_DATA initData;
    initData.pSysMem = temp.get();
    initData.SysMemPitch = static_cast<UINT>( rowPitch );
    initData.SysMemSlicePitch = static_cast<UINT>( imageSize );

    ID3D11Texture2D* tex = nullptr;
    hr = d3dDevice->CreateTexture2D( &desc, (autogen) ? nullptr : &initData, &tex );
    if ( SUCCEEDED(hr) && tex != 0 )
    {
        if (textureView != 0)
        {
            D3D11_SHADER_RESOURCE_VIEW_DESC SRVDesc;
            memset( &SRVDesc, 0, sizeof( SRVDesc ) );
            SRVDesc.Format = format;
            SRVDesc.ViewDimension = D3D11_SRV_DIMENSION_TEXTURE2D;
            SRVDesc.Texture2D.MipLevels = (autogen) ? -1 : 1;

            hr = d3dDevice->CreateShaderResourceView( tex, &SRVDesc, textureView );
            if ( FAILED(hr) )
            {
                tex->Release();
                return hr;
            }

            if ( autogen )
            {
                assert( d3dContext != 0 );
                d3dContext->UpdateSubresource( tex, 0, nullptr, temp.get(), static_cast<UINT>(rowPitch), static_cast<UINT>(imageSize) );
                d3dContext->GenerateMips( *textureView );
            }
        }

        if (texture != 0)
        {
            *texture = tex;
        }
        else
        {
#if defined(_DEBUG) || defined(PROFILE)
            tex->SetPrivateData( WKPDID_D3DDebugObjectName,
                                 sizeof("WICTextureLoader")-1,
                                 "WICTextureLoader"
                               );
#endif
            tex->Release();
        }
    }

    return hr;
}

//--------------------------------------------------------------------------------------
HRESULT CreateWICTextureFromMemory( _In_ ID3D11Device* d3dDevice,
                                    _In_opt_ ID3D11DeviceContext* d3dContext,
                                    _In_bytecount_(wicDataSize) const uint8_t* wicData,
                                    _In_ size_t wicDataSize,
                                    _Out_opt_ ID3D11Resource** texture,
                                    _Out_opt_ ID3D11ShaderResourceView** textureView,
                                    _In_ size_t maxsize
                                  )
{
    if (!d3dDevice || !wicData || (!texture && !textureView))
    {
        return E_INVALIDARG;
    }

    if ( !wicDataSize )
    {
        return E_FAIL;
    }

#ifdef _M_AMD64
    if ( wicDataSize > 0xFFFFFFFF )
        return HRESULT_FROM_WIN32( ERROR_FILE_TOO_LARGE );
#endif

    IWICImagingFactory* pWIC = _GetWIC();
    if ( !pWIC )
        return E_NOINTERFACE;

    // Create input stream for memory
    ScopedObject<IWICStream> stream;
    HRESULT hr = pWIC->CreateStream( &stream );
    if ( FAILED(hr) )
        return hr;

    hr = stream->InitializeFromMemory( const_cast<uint8_t*>( wicData ), static_cast<DWORD>( wicDataSize ) );
    if ( FAILED(hr) )
        return hr;

    // Initialize WIC
    ScopedObject<IWICBitmapDecoder> decoder;
    hr = pWIC->CreateDecoderFromStream( stream.Get(), 0, WICDecodeMetadataCacheOnDemand, &decoder );
    if ( FAILED(hr) )
        return hr;

    ScopedObject<IWICBitmapFrameDecode> frame;
    hr = decoder->GetFrame( 0, &frame );
    if ( FAILED(hr) )
        return hr;

    hr = CreateTextureFromWIC( d3dDevice, d3dContext, frame.Get(), texture, textureView, maxsize );
    if ( FAILED(hr)) 
        return hr;

#if defined(_DEBUG) || defined(PROFILE)
    if (texture != 0 && *texture != 0)
    {
        (*texture)->SetPrivateData( WKPDID_D3DDebugObjectName,
                                    sizeof("WICTextureLoader")-1,
                                    "WICTextureLoader"
                                  );
    }

    if (textureView != 0 && *textureView != 0)
    {
        (*textureView)->SetPrivateData( WKPDID_D3DDebugObjectName,
                                        sizeof("WICTextureLoader")-1,
                                        "WICTextureLoader"
                                      );
    }
#endif

    return hr;
}

//--------------------------------------------------------------------------------------
HRESULT CreateWICTextureFromFile( _In_ ID3D11Device* d3dDevice,
                                  _In_opt_ ID3D11DeviceContext* d3dContext,
                                  _In_z_ const wchar_t* fileName,
                                  _Out_opt_ ID3D11Resource** texture,
                                  _Out_opt_ ID3D11ShaderResourceView** textureView,
                                  _In_ size_t maxsize )
{
    if (!d3dDevice || !fileName || (!texture && !textureView))
    {
        return E_INVALIDARG;
    }

    IWICImagingFactory* pWIC = _GetWIC();
    if ( !pWIC )
        return E_NOINTERFACE;

    // Initialize WIC
    ScopedObject<IWICBitmapDecoder> decoder;
    HRESULT hr = pWIC->CreateDecoderFromFilename( fileName, 0, GENERIC_READ, WICDecodeMetadataCacheOnDemand, &decoder );
    if ( FAILED(hr) )
        return hr;

    ScopedObject<IWICBitmapFrameDecode> frame;
    hr = decoder->GetFrame( 0, &frame );
    if ( FAILED(hr) )
        return hr;

    hr = CreateTextureFromWIC( d3dDevice, d3dContext, frame.Get(), texture, textureView, maxsize );
    if ( FAILED(hr)) 
        return hr;

#if defined(_DEBUG) || defined(PROFILE)
    if (texture != 0 || textureView != 0)
    {
        CHAR strFileA[MAX_PATH];
        WideCharToMultiByte( CP_ACP,
                             WC_NO_BEST_FIT_CHARS,
                             fileName,
                             -1,
                             strFileA,
                             MAX_PATH,
                             nullptr,
                             FALSE
                           );
        const CHAR* pstrName = strrchr( strFileA, '\\' );
        if (!pstrName)
        {
            pstrName = strFileA;
        }
        else
        {
            pstrName++;
        }

        if (texture != 0 && *texture != 0)
        {
            (*texture)->SetPrivateData( WKPDID_D3DDebugObjectName,
                                        static_cast<UINT>( strnlen_s(pstrName, MAX_PATH) ),
                                        pstrName
                                      );
        }

        if (textureView != 0 && *textureView != 0 )
        {
            (*textureView)->SetPrivateData( WKPDID_D3DDebugObjectName,
                                            static_cast<UINT>( strnlen_s(pstrName, MAX_PATH) ),
                                            pstrName
                                          );
        }
    }
#endif

    return hr;
}
```



## <a name="related-topics"></a><span data-ttu-id="dc1c5-167">См. также</span><span class="sxs-lookup"><span data-stu-id="dc1c5-167">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="dc1c5-168">Использование Direct3D 11</span><span class="sxs-lookup"><span data-stu-id="dc1c5-168">How to Use Direct3D 11</span></span>](how-to-use-direct3d-11.md)
</dt> <dt>

[<span data-ttu-id="dc1c5-169">Текстуры</span><span class="sxs-lookup"><span data-stu-id="dc1c5-169">Textures</span></span>](overviews-direct3d-11-resources-textures.md)
</dt> </dl>

 

 