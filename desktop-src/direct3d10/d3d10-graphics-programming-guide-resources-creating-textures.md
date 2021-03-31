---
description: Ресурс текстуры — это структурированная коллекция данных.
ms.assetid: 4c716be8-044e-4ed4-aeca-4379440826bd
title: Создание ресурсов текстуры (Direct3D 10)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 81f2ca200b566d17b02af56c48cb1227c41106ad
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103990605"
---
# <a name="creating-texture-resources-direct3d-10"></a><span data-ttu-id="f70f6-103">Создание ресурсов текстуры (Direct3D 10)</span><span class="sxs-lookup"><span data-stu-id="f70f6-103">Creating Texture Resources (Direct3D 10)</span></span>

<span data-ttu-id="f70f6-104">Ресурс [текстуры](d3d10-graphics-programming-guide-resources-types.md) — это структурированная коллекция данных.</span><span class="sxs-lookup"><span data-stu-id="f70f6-104">A [texture](d3d10-graphics-programming-guide-resources-types.md) resource is a structured collection of data.</span></span> <span data-ttu-id="f70f6-105">Обычно значения цвета хранятся в текстурах и доступны во время отрисовки [конвейера](d3d10-graphics-programming-guide-pipeline-stages.md) на различных этапах для входа и выхода.</span><span class="sxs-lookup"><span data-stu-id="f70f6-105">Typically, color values are stored in textures and accessed during rendering by the [pipeline](d3d10-graphics-programming-guide-pipeline-stages.md) at various stages for both input and output.</span></span> <span data-ttu-id="f70f6-106">Создание текстур и определение того, как они будут использоваться, — важная часть визуализации интересных сцен в Direct3D 10.</span><span class="sxs-lookup"><span data-stu-id="f70f6-106">Creating textures and defining how they will be used is an important part of rendering interesting-looking scenes in Direct3D 10.</span></span>

<span data-ttu-id="f70f6-107">Несмотря на то, что текстуры обычно содержат сведения о цвете, создание текстур с помощью различных [**\_ форматов DXGI**](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) позволяет им хранить различные типы данных.</span><span class="sxs-lookup"><span data-stu-id="f70f6-107">Even though textures typically contain color information, creating textures using different [**DXGI\_FORMAT**](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) enables them to store different kinds of data.</span></span> <span data-ttu-id="f70f6-108">Эти данные можно затем использовать в конвейере Direct3D 10 в нетрадиционных способах.</span><span class="sxs-lookup"><span data-stu-id="f70f6-108">This data can then be leveraged by the Direct3D 10 pipeline in non-traditional ways.</span></span>

<span data-ttu-id="f70f6-109">Все текстуры имеют ограничения на объем используемой памяти и количество пикселей текстуры, которые они содержат.</span><span class="sxs-lookup"><span data-stu-id="f70f6-109">All textures have limits on how much memory they consume, and how many texels they contain.</span></span> <span data-ttu-id="f70f6-110">Эти ограничения задаются [константами ресурсов](d3d10-graphics-reference-resource-constants.md).</span><span class="sxs-lookup"><span data-stu-id="f70f6-110">These limits are specified by [resource constants](d3d10-graphics-reference-resource-constants.md).</span></span>

-   [<span data-ttu-id="f70f6-111">Создание текстуры из файла</span><span class="sxs-lookup"><span data-stu-id="f70f6-111">Create a Texture from a File</span></span>](#create-a-texture-from-a-file)
    -   [<span data-ttu-id="f70f6-112">Создание текстуры и представления отдельно</span><span class="sxs-lookup"><span data-stu-id="f70f6-112">Create Texture and View Separately</span></span>](#create-texture-and-view-separately)
    -   [<span data-ttu-id="f70f6-113">Одновременное создание текстур и представлений</span><span class="sxs-lookup"><span data-stu-id="f70f6-113">Create Texture and View Simultaneously</span></span>](#create-texture-and-view-simultaneously)
-   [<span data-ttu-id="f70f6-114">Создание пустых текстур</span><span class="sxs-lookup"><span data-stu-id="f70f6-114">Creating Empty Textures</span></span>](#creating-empty-textures)
    -   [<span data-ttu-id="f70f6-115">Подготовка к отображению текстуры</span><span class="sxs-lookup"><span data-stu-id="f70f6-115">Rendering to a texture</span></span>](#rendering-to-a-texture)
    -   [<span data-ttu-id="f70f6-116">Заполнение текстур вручную</span><span class="sxs-lookup"><span data-stu-id="f70f6-116">Filling Textures Manually</span></span>](#filling-textures-manually)
-   [<span data-ttu-id="f70f6-117">Несколько Рендертаржетс</span><span class="sxs-lookup"><span data-stu-id="f70f6-117">Multiple Rendertargets</span></span>](#multiple-rendertargets)
-   [<span data-ttu-id="f70f6-118">См. также</span><span class="sxs-lookup"><span data-stu-id="f70f6-118">Related topics</span></span>](#related-topics)

## <a name="create-a-texture-from-a-file"></a><span data-ttu-id="f70f6-119">Создание текстуры из файла</span><span class="sxs-lookup"><span data-stu-id="f70f6-119">Create a Texture from a File</span></span>

> [!Note]  
> <span data-ttu-id="f70f6-120">[Библиотека служебной программы D3DX](d3d10-graphics-reference-d3dx10.md) устарела для Windows 8 и не поддерживается для приложений Магазина Windows.</span><span class="sxs-lookup"><span data-stu-id="f70f6-120">The [D3DX utility library](d3d10-graphics-reference-d3dx10.md) is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span>

 

<span data-ttu-id="f70f6-121">При создании текстуры в Direct3D 10 необходимо также создать [представление](d3d10-graphics-programming-guide-resources-access-views.md).</span><span class="sxs-lookup"><span data-stu-id="f70f6-121">When you create a texture in Direct3D 10, you also need to create a [view](d3d10-graphics-programming-guide-resources-access-views.md).</span></span> <span data-ttu-id="f70f6-122">Представление — это объект, сообщающий устройству, как осуществляется доступ к текстуре во время подготовки к просмотру.</span><span class="sxs-lookup"><span data-stu-id="f70f6-122">A view is an object that tells the device how a texture should be accessed during rendering.</span></span> <span data-ttu-id="f70f6-123">Самый распространенный способ доступа к текстуре — чтение из него с помощью [шейдера](../direct3dhlsl/dx-graphics-hlsl.md).</span><span class="sxs-lookup"><span data-stu-id="f70f6-123">The most common way to access a texture is to read from it using a [shader](../direct3dhlsl/dx-graphics-hlsl.md).</span></span> <span data-ttu-id="f70f6-124">Представление ресурсов шейдера покажет шейдеру способ чтения из текстуры во время подготовки к просмотру.</span><span class="sxs-lookup"><span data-stu-id="f70f6-124">A shader-resource view will tell a shader how to read from a texture during rendering.</span></span> <span data-ttu-id="f70f6-125">Вид представления, который будет использоваться текстурой, должен быть указан при его создании.</span><span class="sxs-lookup"><span data-stu-id="f70f6-125">The kind of view a texture will use must be specified when you create it.</span></span>

<span data-ttu-id="f70f6-126">Создание текстуры и загрузка исходных данных можно выполнить двумя разными способами: создать текстуру и представление отдельно или одновременно создать текстуру и представление.</span><span class="sxs-lookup"><span data-stu-id="f70f6-126">Creating a texture and loading its initial data can be done in two different ways: create a texture and view separately, or create both the texture and the view at the same time.</span></span> <span data-ttu-id="f70f6-127">API предоставляет обе методики, что позволяет выбрать подходящий вариант.</span><span class="sxs-lookup"><span data-stu-id="f70f6-127">The API provides both techniques so you can choose which better suits your needs.</span></span>

### <a name="create-texture-and-view-separately"></a><span data-ttu-id="f70f6-128">Создание текстуры и представления отдельно</span><span class="sxs-lookup"><span data-stu-id="f70f6-128">Create Texture and View Separately</span></span>

<span data-ttu-id="f70f6-129">Самый простой способ создать текстуру — загрузить ее из файла изображения.</span><span class="sxs-lookup"><span data-stu-id="f70f6-129">The easiest way to create a texture is to load it from an image file.</span></span> <span data-ttu-id="f70f6-130">Чтобы создать текстуру, просто заполните одну структуру и укажите имя текстуры [**D3DX10CreateTextureFromFile**](d3dx10createtexturefromfile.md).</span><span class="sxs-lookup"><span data-stu-id="f70f6-130">To create the texture, just fill in one structure and provide the texture's name to [**D3DX10CreateTextureFromFile**](d3dx10createtexturefromfile.md).</span></span>


```
ID3D10Device *pDevice = NULL;
// Initialize D3D10 device...

D3DX10_IMAGE_LOAD_INFO loadInfo;
ZeroMemory( &loadInfo, sizeof(D3DX10_IMAGE_LOAD_INFO) );
loadInfo.BindFlags = D3D10_BIND_SHADER_RESOURCE;

ID3D10Resource *pTexture = NULL;
D3DX10CreateTextureFromFile( pDevice, L"sample.bmp", &loadInfo, NULL, &pTexture, NULL );
```



<span data-ttu-id="f70f6-131">Функция D3DX [**D3DX10CreateTextureFromFile**](d3dx10createtexturefromfile.md) выполняет три вещи: сначала создается объект текстуры Direct3D 10. Во вторых, он считывает входной файл изображения. в третьих, данные изображения сохраняются в объекте текстуры.</span><span class="sxs-lookup"><span data-stu-id="f70f6-131">The D3DX function [**D3DX10CreateTextureFromFile**](d3dx10createtexturefromfile.md) does three things: first, it creates a Direct3D 10 texture object; second, it reads the input image file; third, it stores the image data in the texture object.</span></span> <span data-ttu-id="f70f6-132">В приведенном выше примере загружается файл BMP, но функция может загружать различные типы файлов.</span><span class="sxs-lookup"><span data-stu-id="f70f6-132">In the sample above, a BMP file is loaded, but the function can load a variety of file types.</span></span>

<span data-ttu-id="f70f6-133">Флаг привязки указывает, что текстура будет создана как ресурс шейдера, что позволяет этапу шейдера считывать из текстуры во время отрисовки.</span><span class="sxs-lookup"><span data-stu-id="f70f6-133">The bind flag indicates the texture will be created as a shader resource which allows a shader stage to read from the texture during rendering.</span></span>

<span data-ttu-id="f70f6-134">В приведенном выше примере не указаны все параметры загрузки.</span><span class="sxs-lookup"><span data-stu-id="f70f6-134">The above example does not specify all of the loading parameters.</span></span> <span data-ttu-id="f70f6-135">На самом деле, часто бывает полезно просто обнулить параметры загрузки, так как это позволяет D3DX выбирать соответствующие значения на основе входного изображения.</span><span class="sxs-lookup"><span data-stu-id="f70f6-135">In fact, it's often beneficial to simply zero out the loading parameters as this enables D3DX to choose appropriate values based on the input image.</span></span> <span data-ttu-id="f70f6-136">Если вы хотите, чтобы входной образ определил все параметры, с которыми создается текстура, просто укажите **значение NULL** для параметра **лоадинфо** следующим образом:</span><span class="sxs-lookup"><span data-stu-id="f70f6-136">If you want the input image to determine all of the parameters the texture is created with, simply specify **NULL** for the **loadInfo** parameter like this:</span></span>


```
D3DX10CreateTextureFromFile( pDevice, L"sample.bmp", NULL, NULL, &pTexture, NULL );
```



<span data-ttu-id="f70f6-137">Указание **значения NULL** для сведений о загрузке является простым, но мощным ярлыком.</span><span class="sxs-lookup"><span data-stu-id="f70f6-137">Specifying **NULL** for the loading information is a simple yet powerful shortcut.</span></span>

<span data-ttu-id="f70f6-138">Теперь, когда текстура создана, необходимо создать представление шейдера, чтобы текстуру можно было привязать как входные данные для шейдера.</span><span class="sxs-lookup"><span data-stu-id="f70f6-138">Now that a texture has been created, you need to create a shader-resource view so that the texture can be bound as an input to a shader.</span></span> <span data-ttu-id="f70f6-139">Поскольку [**D3DX10CreateTextureFromFile**](d3dx10createtexturefromfile.md) возвращает указатель на ресурс, а не указатель на текстуру, необходимо определить точный тип ресурса, который был загружен, а затем создать представление "шейдер-ресурс" с помощью [**креатешадерресаурцевиев**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-createshaderresourceview).</span><span class="sxs-lookup"><span data-stu-id="f70f6-139">Since [**D3DX10CreateTextureFromFile**](d3dx10createtexturefromfile.md) returns a pointer to a resource and not a pointer to a texture, you have to determine the exact type of resource that was loaded, and then you can create a shader-resource view using [**CreateShaderResourceView**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-createshaderresourceview).</span></span>


```
D3D10_SHADER_RESOURCE_VIEW_DESC srvDesc;
D3D10_RESOURCE_DIMENSION type;
pTexture->GetType( &type );
switch( type )
{
    case D3D10_RESOURCE_DIMENSION_BUFFER:
    //...
    break;
    case D3D10_RESOURCE_DIMENSION_TEXTURE1D:
    //...
    break;
    case D3D10_RESOURCE_DIMENSION_TEXTURE2D:
    {
        D3D10_TEXTURE2D_DESC desc;
        ID3D10Texture2D *pTexture2D = (ID3D10Texture2D*)pTexture;
        pTexture2D->GetDesc( &desc );
        
        srvDesc.Format = desc.Format;
        srvDesc.ViewDimension = D3D10_SRV_DIMENSION_TEXTURE2D;
        srvDesc.Texture2D.MipLevels = desc.MipLevels;
        srvDesc.Texture2D.MostDetailedMip = desc.MipLevels -1;

    }
    break;
    case D3D10_RESOURCE_DIMENSION_TEXTURE3D:
    //...
    break;
    default:
    //...
    break;
}

ID3D10ShaderResourceView *pSRView = NULL;
pDevice->CreateShaderResourceView( pTexture, &srvDesc, &pSRView );
```



<span data-ttu-id="f70f6-140">Хотя в приведенном выше примере создается 2D-представление ресурсов, код для создания других типов представлений ресурсов шейдера очень похож.</span><span class="sxs-lookup"><span data-stu-id="f70f6-140">Although the above sample creates a 2D shader-resource view, the code to create other shader-resource view types is very similar.</span></span> <span data-ttu-id="f70f6-141">Теперь любой этап шейдера может использовать эту текстуру в качестве входных данных.</span><span class="sxs-lookup"><span data-stu-id="f70f6-141">Any shader stage can now use this texture as an input.</span></span>

<span data-ttu-id="f70f6-142">Использование [**D3DX10CreateTextureFromFile**](d3dx10createtexturefromfile.md) и [**креатешадерресаурцевиев**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-createshaderresourceview) для создания текстуры и связанного с ней представления — один из способов подготовки текстуры к привязке к этапу шейдера.</span><span class="sxs-lookup"><span data-stu-id="f70f6-142">Using [**D3DX10CreateTextureFromFile**](d3dx10createtexturefromfile.md) and [**CreateShaderResourceView**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-createshaderresourceview) to create a texture and its associated view is one way to prepare a texture to be bound to a shader stage.</span></span> <span data-ttu-id="f70f6-143">Другой способ сделать это — создать одновременно текстуру и ее представление, что рассматривается в следующем разделе.</span><span class="sxs-lookup"><span data-stu-id="f70f6-143">Another way to do so is to create both the texture and its view at the same time, which is discussed in the next section.</span></span>

### <a name="create-texture-and-view-simultaneously"></a><span data-ttu-id="f70f6-144">Одновременное создание текстур и представлений</span><span class="sxs-lookup"><span data-stu-id="f70f6-144">Create Texture and View Simultaneously</span></span>

<span data-ttu-id="f70f6-145">Для считывания из текстуры во время выполнения Direct3D 10 требуется как текстура, так и шейдер — представление ресурсов.</span><span class="sxs-lookup"><span data-stu-id="f70f6-145">Direct3D 10 requires both a texture and a shader-resource view to read from a texture during runtime.</span></span> <span data-ttu-id="f70f6-146">Так как создание текстуры и представления шейдера — это типичная задача, D3DX предоставляет [**D3DX10CreateShaderResourceViewFromFile**](d3dx10createshaderresourceviewfromfile.md) для вас.</span><span class="sxs-lookup"><span data-stu-id="f70f6-146">Since the creation of a texture and a shader-resource view is such a common task, D3DX provides the [**D3DX10CreateShaderResourceViewFromFile**](d3dx10createshaderresourceviewfromfile.md) to do it for you.</span></span>


```
D3DX10_IMAGE_LOAD_INFO loadInfo;
ZeroMemory( &loadInfo, sizeof(D3DX10_IMAGE_LOAD_INFO) );
loadInfo.BindFlags = D3D10_BIND_SHADER_RESOURCE;
loadInfo.Format = DXGI_FORMAT_BC1_UNORM;

ID3D10ShaderResourceView *pSRView = NULL;
D3DX10CreateShaderResourceViewFromFile( pDevice, L"sample.bmp", &loadInfo, NULL, &pSRView, NULL );
```



<span data-ttu-id="f70f6-147">При одном вызове D3DX создаются и текстура, и шейдер-представление ресурсов.</span><span class="sxs-lookup"><span data-stu-id="f70f6-147">With a single D3DX call, both the texture and shader-resource view are created.</span></span> <span data-ttu-id="f70f6-148">Функции параметра **лоадинфо** не изменяются; его можно использовать для настройки способа создания текстуры или получения необходимых параметров из входного файла, указав **значение NULL** для параметра **лоадинфо** .</span><span class="sxs-lookup"><span data-stu-id="f70f6-148">The functionality of the **loadInfo** parameter is unchanged; you can use it to customize how the texture is created, or derive the necessary parameters from the input file by specifying **NULL** for the **loadInfo** parameter.</span></span>

<span data-ttu-id="f70f6-149">Объект [**ID3D10ShaderResourceView**](/windows/desktop/api/d3d10/nn-d3d10-id3d10shaderresourceview) , возвращаемый функцией [**D3DX10CreateShaderResourceViewFromFile**](d3dx10createshaderresourceviewfromfile.md) , можно впоследствии использовать для получения исходного интерфейса [**ID3D10Resource**](/windows/desktop/api/D3D10/nn-d3d10-id3d10resource) , если он необходим.</span><span class="sxs-lookup"><span data-stu-id="f70f6-149">The [**ID3D10ShaderResourceView**](/windows/desktop/api/d3d10/nn-d3d10-id3d10shaderresourceview) object returned by the [**D3DX10CreateShaderResourceViewFromFile**](d3dx10createshaderresourceviewfromfile.md) function can later be used to retrieve the original [**ID3D10Resource**](/windows/desktop/api/D3D10/nn-d3d10-id3d10resource) interface if it is needed.</span></span> <span data-ttu-id="f70f6-150">Это можно [**сделать, вызвав метод метода**](/windows/desktop/api/D3D10/nf-d3d10-id3d10view-getresource) WebMethod.</span><span class="sxs-lookup"><span data-stu-id="f70f6-150">This can be done by calling the [**GetResource**](/windows/desktop/api/D3D10/nf-d3d10-id3d10view-getresource) method.</span></span>

<span data-ttu-id="f70f6-151">D3DX предоставляет единую функцию для создания текстуры и представления шейдеров в виде конвиениенце; Вы решаете решить, какой метод создания текстуры и представления лучше удовлетворять потребностям вашего приложения.</span><span class="sxs-lookup"><span data-stu-id="f70f6-151">D3DX provides a single function to create a texture and shader-resource view as a convienience; it is up to you to decide which method of creating a texture and view best suits the needs of your application.</span></span>

<span data-ttu-id="f70f6-152">Теперь, когда вы узнали, как создать текстуру и ее представление шейдеров, в следующем разделе будет показано, как можно выполнить выборку (чтение) из текстуры с помощью шейдера.</span><span class="sxs-lookup"><span data-stu-id="f70f6-152">Now that you know how to create a texture and its shader-resource view, the next section will show you how you can sample (read) from that texture using a shader.</span></span>

## <a name="creating-empty-textures"></a><span data-ttu-id="f70f6-153">Создание пустых текстур</span><span class="sxs-lookup"><span data-stu-id="f70f6-153">Creating Empty Textures</span></span>

<span data-ttu-id="f70f6-154">Иногда приложения хотят создать текстуру и вычислить данные, которые будут храниться в текстуре, или использовать графический [конвейер](d3d10-graphics-programming-guide-pipeline-stages.md) для визуализации в эту текстуру, а затем использовать результаты в другой обработке.</span><span class="sxs-lookup"><span data-stu-id="f70f6-154">Sometimes applications will want to create a texture and compute the data to be stored in the texture, or use the graphics [pipeline](d3d10-graphics-programming-guide-pipeline-stages.md) to render to this texture and later use the results in other processing.</span></span> <span data-ttu-id="f70f6-155">Эти текстуры могут быть обновлены графическим конвейером или самим приложением, в зависимости от того, какой тип [**использования**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_usage) был указан для текстуры при ее создании.</span><span class="sxs-lookup"><span data-stu-id="f70f6-155">These textures could be updated by the graphics pipeline or by the application itself, depending on what kind of [**usage**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_usage) was specified for the texture when it was created.</span></span>

### <a name="rendering-to-a-texture"></a><span data-ttu-id="f70f6-156">Подготовка к отображению текстуры</span><span class="sxs-lookup"><span data-stu-id="f70f6-156">Rendering to a texture</span></span>

<span data-ttu-id="f70f6-157">Наиболее распространенным случаем создания пустой текстуры для заполнения данными во время выполнения является ситуация, когда приложению требуется выполнить отрисовку на текстуру, а затем использовать результаты операции визуализации в последующем проходе.</span><span class="sxs-lookup"><span data-stu-id="f70f6-157">The most common case of creating an empty texture to be filled with data during runtime is the case where an application wants to render to a texture and then use the results of the rendering operation in a subsequent pass.</span></span> <span data-ttu-id="f70f6-158">Текстуры, созданные с этой целью, должны указывать [**Использование**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_usage)по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="f70f6-158">Textures created with this purpose should specify default [**usage**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_usage).</span></span>

<span data-ttu-id="f70f6-159">В следующем примере кода создается пустая текстура, которую конвейер может визуализировать и впоследствии использовать в качестве входных данных для [шейдера](../direct3dhlsl/dx-graphics-hlsl-using-shaders-10.md).</span><span class="sxs-lookup"><span data-stu-id="f70f6-159">The following code sample creates an empty texture that the pipeline can render to and subsequently use as an input to a [shader](../direct3dhlsl/dx-graphics-hlsl-using-shaders-10.md).</span></span>


```
// Create the render target texture
D3D10_TEXTURE2D_DESC desc;
ZeroMemory( &desc, sizeof(desc) );
desc.Width = 256;
desc.Height = 256;
desc.MipLevels = 1;
desc.ArraySize = 1;
desc.Format = DXGI_FORMAT_R32G32B32A32_FLOAT;
desc.SampleDesc.Count = 1;
desc.Usage = D3D10_USAGE_DEFAULT;
desc.BindFlags = D3D10_BIND_RENDER_TARGET | D3D10_BIND_SHADER_RESOURCE;

ID3D10Texture2D *pRenderTarget = NULL;
pDevice->CreateTexture2D( &desc, NULL, &pRenderTarget );
```



<span data-ttu-id="f70f6-160">Для создания текстуры приложение должно указать некоторые сведения о свойствах, которые будет иметь текстура.</span><span class="sxs-lookup"><span data-stu-id="f70f6-160">Creating the texture requires the application to specify some information about the properties the texture will have.</span></span> <span data-ttu-id="f70f6-161">Ширина и высота текстуры в пикселей текстуры заданы как 256.</span><span class="sxs-lookup"><span data-stu-id="f70f6-161">The width and height of the texture in texels is set to 256.</span></span> <span data-ttu-id="f70f6-162">Для этого целевого объекта рендеринга требуется только один уровень mipmap.</span><span class="sxs-lookup"><span data-stu-id="f70f6-162">For this render target, a single mipmap level is all we need.</span></span> <span data-ttu-id="f70f6-163">Требуется только один целевой объект рендеринга, поэтому размер массива устанавливается равным 1.</span><span class="sxs-lookup"><span data-stu-id="f70f6-163">Only one render target is required so the array size is set to 1.</span></span> <span data-ttu-id="f70f6-164">Каждый шаг текселя содержит 4 32-разрядные значения с плавающей запятой, которые можно использовать для хранения очень точной информации (см. [**\_ Формат DXGI**](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format)).</span><span class="sxs-lookup"><span data-stu-id="f70f6-164">Each texel contains four 32-bit floating point values, which can be used to store very precise information (see [**DXGI\_FORMAT**](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format)).</span></span> <span data-ttu-id="f70f6-165">Необходимо всего один пример на пиксель.</span><span class="sxs-lookup"><span data-stu-id="f70f6-165">One sample per pixel is all that will be needed.</span></span> <span data-ttu-id="f70f6-166">Для использования задано значение по умолчанию, так как это позволяет наиболее эффективно размещать целевой объект отрисовки в памяти.</span><span class="sxs-lookup"><span data-stu-id="f70f6-166">The usage is set to default because this allows for the most efficient placement of the render target in memory.</span></span> <span data-ttu-id="f70f6-167">Наконец, тот факт, что текстура будет привязана в качестве целевого объекта отрисовки и указан ресурс шейдера в разные моменты времени.</span><span class="sxs-lookup"><span data-stu-id="f70f6-167">Finally, the fact that the texture will be bound as a render target and a shader resource at different points in time is specified.</span></span>

<span data-ttu-id="f70f6-168">Текстуры невозможно привязать для отрисовки в конвейере напрямую; Используйте представление целевого объекта визуализации, как показано в следующем примере кода.</span><span class="sxs-lookup"><span data-stu-id="f70f6-168">Textures cannot be bound for rendering to the pipeline directly; use a render-target view as shown in the following code sample.</span></span>


```
D3D10_RENDER_TARGET_VIEW_DESC rtDesc;
rtDesc.Format = desc.Format;
rtDesc.ViewDimension = D3D10_RTV_DIMENSION_TEXTURE2D;
rtDesc.Texture2D.MipSlice = 0;

ID3D10RenderTargetView *pRenderTargetView = NULL;
pDevice->CreateRenderTargetView( pRenderTarget, &rtDesc, &pRenderTargetView );
```



<span data-ttu-id="f70f6-169">Формат представления «рендеринг-целевой объект» просто устанавливается в формат исходной текстуры.</span><span class="sxs-lookup"><span data-stu-id="f70f6-169">The format of the render-target view is simply set to the format of the original texture.</span></span> <span data-ttu-id="f70f6-170">Информация в ресурсе должна интерпретироваться как двухмерная текстура, и мы хотим использовать только первый уровень mipmap целевого объекта рендеринга.</span><span class="sxs-lookup"><span data-stu-id="f70f6-170">The information in the resource should be interpreted as a 2D texture, and we only want to use the first mipmap level of the render target.</span></span>

<span data-ttu-id="f70f6-171">Аналогично тому, как должно быть создано представление визуализации целевого объекта, чтобы целевой объект отрисовки мог быть привязан к потоку вывода в конвейере, необходимо создать представление шейдера, чтобы целевой объект отрисовки можно было привязать к конвейеру в качестве входных данных.</span><span class="sxs-lookup"><span data-stu-id="f70f6-171">Similarly to how a render-target view must be created so that the render target can be bound for output to the pipeline, a shader-resource view must be created so that the render target can be bound to the pipeline as an input.</span></span> <span data-ttu-id="f70f6-172">Это показано в следующем образце кода.</span><span class="sxs-lookup"><span data-stu-id="f70f6-172">The following code sample demonstrates this.</span></span>


```
// Create the shader-resource view
D3D10_SHADER_RESOURCE_VIEW_DESC srDesc;
srDesc.Format = desc.Format;
srDesc.ViewDimension = D3D10_SRV_DIMENSION_TEXTURE2D;
srDesc.Texture2D.MostDetailedMip = 0;
srDesc.Texture2D.MipLevels = 1;

ID3D10ShaderResourceView *pShaderResView = NULL;
pDevice->CreateShaderResourceView( pRenderTarget, &srDesc, &pShaderResView );
```



<span data-ttu-id="f70f6-173">Параметры описаний представления "шейдер-представление ресурсов" очень похожи на описания представления целевого объекта визуализации и были выбраны по тем же причинам.</span><span class="sxs-lookup"><span data-stu-id="f70f6-173">The parameters of shader-resource view descriptions are very similar to those of render-target view descriptions and were chosen for the same reasons.</span></span>

### <a name="filling-textures-manually"></a><span data-ttu-id="f70f6-174">Заполнение текстур вручную</span><span class="sxs-lookup"><span data-stu-id="f70f6-174">Filling Textures Manually</span></span>

<span data-ttu-id="f70f6-175">Иногда приложения хотели бы вычислять значения во время выполнения, поместив их в текстуру вручную, а затем, чтобы графический [конвейер](d3d10-graphics-programming-guide-pipeline-stages.md) использовал эту текстуру в последующих операциях визуализации.</span><span class="sxs-lookup"><span data-stu-id="f70f6-175">Sometimes applications would like to compute values at runtime, put them into a texture manually and then have the graphics [pipeline](d3d10-graphics-programming-guide-pipeline-stages.md) use this texture in later rendering operations.</span></span> <span data-ttu-id="f70f6-176">Для этого приложение должно создать пустую текстуру таким образом, чтобы ЦП может получить доступ к базовой памяти.</span><span class="sxs-lookup"><span data-stu-id="f70f6-176">To do this, the application must create an empty texture in such a way to allow the CPU to access the underlying memory.</span></span> <span data-ttu-id="f70f6-177">Это делается путем создания динамической текстуры и получения доступа к базовой памяти путем вызова определенного метода.</span><span class="sxs-lookup"><span data-stu-id="f70f6-177">This is done by creating a dynamic texture and gaining access to the underlying memory by calling a particular method.</span></span> <span data-ttu-id="f70f6-178">В следующем образце кода показано, как это сделать.</span><span class="sxs-lookup"><span data-stu-id="f70f6-178">The following code sample demonstrates how to do this.</span></span>


```
D3D10_TEXTURE2D_DESC desc;
desc.Width = 256;
desc.Height = 256;
desc.MipLevels = desc.ArraySize = 1;
desc.Format = DXGI_FORMAT_R8G8B8A8_UNORM;
desc.SampleDesc.Count = 1;
desc.Usage = D3D10_USAGE_DYNAMIC;
desc.BindFlags = D3D10_BIND_SHADER_RESOURCE;
desc.CPUAccessFlags = D3D10_CPU_ACCESS_WRITE;
ID3D10Texture2D *pTexture = NULL;
pd3dDevice->CreateTexture2D( &desc, NULL, &pTexture );
```



<span data-ttu-id="f70f6-179">Обратите внимание, что для формата задано значение 32 бит на пиксель, где каждый компонент определен 8 битами.</span><span class="sxs-lookup"><span data-stu-id="f70f6-179">Note that the format is set to a 32 bits per pixel where each component is defined by 8 bits.</span></span> <span data-ttu-id="f70f6-180">Параметр Usage имеет значение Dynamic, тогда как флаги привязки настроены на указание текстуры, к которой будет обращаться шейдер.</span><span class="sxs-lookup"><span data-stu-id="f70f6-180">The usage parameter is set to dynamic while the bind flags are set to specify the texture will be accessed by a shader.</span></span> <span data-ttu-id="f70f6-181">Оставшаяся часть описания текстуры аналогична созданию целевого объекта рендеринга.</span><span class="sxs-lookup"><span data-stu-id="f70f6-181">The rest of the texture description is similar to creating a render target.</span></span>

<span data-ttu-id="f70f6-182">Вызов [**Map**](/windows/desktop/api/D3D10/nf-d3d10-id3d10texture2d-map) позволяет приложению получить доступ к базовой памяти текстуры.</span><span class="sxs-lookup"><span data-stu-id="f70f6-182">Calling [**Map**](/windows/desktop/api/D3D10/nf-d3d10-id3d10texture2d-map) enables the application to access the underlying memory of the texture.</span></span> <span data-ttu-id="f70f6-183">Полученный указатель используется для заполнения текстурой данными.</span><span class="sxs-lookup"><span data-stu-id="f70f6-183">The pointer retrieved is then used to fill the texture with data.</span></span> <span data-ttu-id="f70f6-184">Это можно увидеть в следующем примере кода.</span><span class="sxs-lookup"><span data-stu-id="f70f6-184">This can be seen in the following code sample.</span></span>


```
D3D10_MAPPED_TEXTURE2D mappedTex;
pTexture->Map( D3D10CalcSubresource(0, 0, 1), D3D10_MAP_WRITE_DISCARD, 0, &mappedTex );

UCHAR* pTexels = (UCHAR*)mappedTex.pData;
for( UINT row = 0; row < desc.Height; row++ )
{
    UINT rowStart = row * mappedTex.RowPitch;
    for( UINT col = 0; col < desc.Width; col++ )
    {
        UINT colStart = col * 4;
        pTexels[rowStart + colStart + 0] = 255; // Red
        pTexels[rowStart + colStart + 1] = 128; // Green
        pTexels[rowStart + colStart + 2] = 64;  // Blue
        pTexels[rowStart + colStart + 3] = 32;  // Alpha
    }
}

pTexture->Unmap( D3D10CalcSubresource(0, 0, 1) );
```



## <a name="multiple-rendertargets"></a><span data-ttu-id="f70f6-185">Несколько Рендертаржетс</span><span class="sxs-lookup"><span data-stu-id="f70f6-185">Multiple Rendertargets</span></span>

<span data-ttu-id="f70f6-186">До восьми представлений представления подготовки к просмотру может быть привязано к конвейеру за раз (с [**омсетрендертаржетс**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-omsetrendertargets)).</span><span class="sxs-lookup"><span data-stu-id="f70f6-186">Up to eight render-target views can be bound to the pipeline at a time (with [**OMSetRenderTargets**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-omsetrendertargets)).</span></span> <span data-ttu-id="f70f6-187">Для каждого пикселя (или каждого образца при включенной множественной выборки) смешивание выполняется независимо для каждого представления целевого объекта рендеринга.</span><span class="sxs-lookup"><span data-stu-id="f70f6-187">For each pixel (or each sample if multisampling is enabled), blending is done independently for each render-target view.</span></span> <span data-ttu-id="f70f6-188">Две переменные состояния смешения — Бленденабле и Рендертаржетвритемаск — массивы из восьми, каждый элемент массива соответствует представлению целевого объекта визуализации.</span><span class="sxs-lookup"><span data-stu-id="f70f6-188">Two of the blend state variables - BlendEnable and RenderTargetWriteMask - are arrays of eight, each array member corresponds to a render-target view.</span></span> <span data-ttu-id="f70f6-189">При использовании нескольких целевых объектов рендеринга каждый целевой объект отрисовки должен иметь один и тот же [тип ресурса](d3d10-graphics-programming-guide-resources-types.md) (буфер, текстура 1d, массив 2D-текстуры и т. д.) и иметь одинаковое измерение (ширину, высоту, глубину для трехмерных текстур и размер массива для массивов текстуры).</span><span class="sxs-lookup"><span data-stu-id="f70f6-189">When using multiple render targets, each render target must be the same [resource type](d3d10-graphics-programming-guide-resources-types.md) (buffer, 1D texture, 2D texture array, etc.) and must have the same dimension (width, height, depth for 3D textures, and array size for texture arrays).</span></span> <span data-ttu-id="f70f6-190">Если целевые объекты отрисовки являются многовыборочными, то все они должны иметь одинаковое количество выборок на пиксель.</span><span class="sxs-lookup"><span data-stu-id="f70f6-190">If the render targets are multisampled, then they must all have the same number of samples per pixel.</span></span>

<span data-ttu-id="f70f6-191">Активным может быть только один буфер трафарета глубины, независимо от того, сколько активных объектов рендеринга активно.</span><span class="sxs-lookup"><span data-stu-id="f70f6-191">There can only be one depth-stencil buffer active, regardless of how many render targets are active.</span></span> <span data-ttu-id="f70f6-192">При использовании массивов текстуры в качестве целевых объектов рендеринга все измерения представления должны совпадать.</span><span class="sxs-lookup"><span data-stu-id="f70f6-192">When using texture arrays as render targets, all view dimensions must match.</span></span> <span data-ttu-id="f70f6-193">Целевые объекты рендеринга не должны иметь одинаковый формат текстуры.</span><span class="sxs-lookup"><span data-stu-id="f70f6-193">The render targets do not need to have the same texture format.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f70f6-194">См. также</span><span class="sxs-lookup"><span data-stu-id="f70f6-194">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f70f6-195">Ресурсы (Direct3D 10)</span><span class="sxs-lookup"><span data-stu-id="f70f6-195">Resources (Direct3D 10)</span></span>](d3d10-graphics-programming-guide-resources.md)
</dt> </dl>

 

 
