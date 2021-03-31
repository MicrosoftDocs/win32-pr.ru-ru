---
description: Использование сжатых текстур (Direct3D 9)
ms.assetid: 60892a8b-93f4-43ba-87ef-d5c7cc6fb8c6
title: Использование сжатых текстур (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 643b0618043f12ff3e1a84b806c86edb780ad929
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "103806851"
---
# <a name="using-compressed-textures-direct3d-9"></a><span data-ttu-id="35580-103">Использование сжатых текстур (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="35580-103">Using Compressed Textures (Direct3D 9)</span></span>

## <a name="determining-support-for-compressed-textures"></a><span data-ttu-id="35580-104">Определение поддержки для сжатых текстур</span><span class="sxs-lookup"><span data-stu-id="35580-104">Determining Support for Compressed Textures</span></span>

<span data-ttu-id="35580-105">Чтобы проверить адаптер, укажите любой формат пикселей, использующий DXT1, DXT2, DXT3, DXT4 или DXT5.</span><span class="sxs-lookup"><span data-stu-id="35580-105">To test the adapter, specify any pixel format that uses the DXT1, DXT2, DXT3, DXT4, or DXT5.</span></span> <span data-ttu-id="35580-106">Если [**IDirect3D9:: чеккдевицеформат**](/windows/desktop/api) возвращает D3D \_ ОК, устройство может создать текстуру непосредственно из сжатой текстурной поверхности, использующей этот формат.</span><span class="sxs-lookup"><span data-stu-id="35580-106">If [**IDirect3D9::CheckDeviceFormat**](/windows/desktop/api) returns D3D\_OK, the device can create texture directly from a compressed texture surface that uses that format.</span></span> <span data-ttu-id="35580-107">Если это так, можно использовать сжатые поверхности текстуры непосредственно с Direct3D, вызвав метод [**IDirect3DDevice9:: сеттекстуре**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture) .</span><span class="sxs-lookup"><span data-stu-id="35580-107">If so, you can use compressed texture surfaces directly with Direct3D by calling the [**IDirect3DDevice9::SetTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture) method.</span></span> <span data-ttu-id="35580-108">В следующем примере кода показано, как определить, поддерживает ли адаптер формат сжатой текстуры.</span><span class="sxs-lookup"><span data-stu-id="35580-108">The following code example shows how to determine if the adapter supports a compressed texture format.</span></span>


```
BOOL IsCompressedTextureFormatOk( D3DFORMAT TextureFormat, 
                                  D3DFORMAT AdapterFormat ) 
{
    HRESULT hr = pD3D->CheckDeviceFormat( D3DADAPTER_DEFAULT,
                                          D3DDEVTYPE_HAL,
                                          AdapterFormat,
                                          0,
                                          D3DRTYPE_TEXTURE,
                                          TextureFormat);

    return SUCCEEDED( hr );
}
```



<span data-ttu-id="35580-109">Если устройство не поддерживает ускорение текстур из сжатых поверхностей текстуры, вы по-прежнему можете хранить данные текстуры в сжатой области формата, но перед тем, как их можно будет использовать для текстурирования, необходимо преобразовать все сжатые текстуры в поддерживаемый формат.</span><span class="sxs-lookup"><span data-stu-id="35580-109">If the device does not support texturing from compressed texture surfaces, you can still store texture data in a compressed format surface, but you must convert any compressed textures to a supported format before they can be used for texturing.</span></span>

## <a name="creating-compressed-textures"></a><span data-ttu-id="35580-110">Создание сжатых текстур</span><span class="sxs-lookup"><span data-stu-id="35580-110">Creating Compressed Textures</span></span>

<span data-ttu-id="35580-111">После создания устройства, поддерживающего формат сжатой текстуры на адаптере, можно создать сжатый ресурс текстуры.</span><span class="sxs-lookup"><span data-stu-id="35580-111">After creating a device that supports a compressed texture format on the adapter, you can create a compressed texture resource.</span></span> <span data-ttu-id="35580-112">Вызовите метод [**IDirect3DDevice9:: креатетекстуре**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createtexture) и укажите формат сжатой текстуры для параметра format.</span><span class="sxs-lookup"><span data-stu-id="35580-112">Call [**IDirect3DDevice9::CreateTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createtexture) and specify a compressed texture format for the Format parameter.</span></span>

<span data-ttu-id="35580-113">Перед загрузкой изображения в объект текстуры извлеките указатель на поверхность текстуры, вызвав метод [**IDirect3DTexture9:: жетсурфацелевел**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dtexture9-getsurfacelevel) .</span><span class="sxs-lookup"><span data-stu-id="35580-113">Before loading an image into a texture object, retrieve a pointer to the texture surface by calling the [**IDirect3DTexture9::GetSurfaceLevel**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dtexture9-getsurfacelevel) method.</span></span>

<span data-ttu-id="35580-114">Теперь можно использовать любую функцию D3DXLoadSurfacexxx для загрузки изображения на поверхность, полученную с помощью [**IDirect3DTexture9:: жетсурфацелевел**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dtexture9-getsurfacelevel).</span><span class="sxs-lookup"><span data-stu-id="35580-114">Now you can use any D3DXLoadSurfacexxx function to load an image to the surface that was retrieved by using [**IDirect3DTexture9::GetSurfaceLevel**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dtexture9-getsurfacelevel).</span></span> <span data-ttu-id="35580-115">Эти функции обработают преобразование в форматы и из сжатых текстур текстуры.</span><span class="sxs-lookup"><span data-stu-id="35580-115">These functions handle conversion to and from compressed texture formats.</span></span>

<span data-ttu-id="35580-116">Вы можете создавать и преобразовывать сжатые файлы текстур (DDS) с помощью редактора текстур DirectX (Dxtex.exe), предоставляемого с пакетом SDK DirectX.</span><span class="sxs-lookup"><span data-stu-id="35580-116">You can create and convert compressed texture (DDS) files using the DirectX Texture Editor (Dxtex.exe) supplied with the DirectX SDK.</span></span> <span data-ttu-id="35580-117">Вы можете получить Dxtex.exe и узнать о нем из пакета SDK DirectX.</span><span class="sxs-lookup"><span data-stu-id="35580-117">You can get Dxtex.exe and learn about it from the DirectX SDK.</span></span> <span data-ttu-id="35580-118">Сведения о пакете SDK для DirectX см. в разделе [где находится пакет DirectX SDK?](../directx-sdk--august-2009-.md).</span><span class="sxs-lookup"><span data-stu-id="35580-118">For info about the DirectX SDK, see [Where is the DirectX SDK?](../directx-sdk--august-2009-.md).</span></span>

<span data-ttu-id="35580-119">Преимущество такого поведения заключается в том, что приложение может скопировать содержимое сжатой области в файл, не подчисляя объем хранилища, необходимый для поверхности определенной ширины и высоты в определенном формате.</span><span class="sxs-lookup"><span data-stu-id="35580-119">The advantage of this behavior is that an application can copy the contents of a compressed surface to a file without calculating how much storage is required for a surface of a particular width and height in the specific format.</span></span>

<span data-ttu-id="35580-120">В следующей таблице показаны пять типов сжатых текстур.</span><span class="sxs-lookup"><span data-stu-id="35580-120">The following table shows the five types of compressed textures.</span></span> <span data-ttu-id="35580-121">Дополнительные сведения о хранении данных см. в разделе [форматы сжатых текстур (Direct3D 9)](compressed-texture-formats.md).</span><span class="sxs-lookup"><span data-stu-id="35580-121">For more information about how the data is stored, see [Compressed Texture Formats (Direct3D 9)](compressed-texture-formats.md).</span></span> <span data-ttu-id="35580-122">Эти сведения понадобятся только при написании собственных подпрограмм сжатия.</span><span class="sxs-lookup"><span data-stu-id="35580-122">You only need this information if you are writing your own compression routines.</span></span>



| <span data-ttu-id="35580-123">FOURCC</span><span class="sxs-lookup"><span data-stu-id="35580-123">FOURCC</span></span> | <span data-ttu-id="35580-124">Описание</span><span class="sxs-lookup"><span data-stu-id="35580-124">Description</span></span>        | <span data-ttu-id="35580-125">Альфа-канал был предварительно умножен?</span><span class="sxs-lookup"><span data-stu-id="35580-125">Alpha premultiplied?</span></span> |
|--------|--------------------|----------------------|
| <span data-ttu-id="35580-126">DXT1</span><span class="sxs-lookup"><span data-stu-id="35580-126">DXT1</span></span>   | <span data-ttu-id="35580-127">Непрозрачный/1-разрядный альфа</span><span class="sxs-lookup"><span data-stu-id="35580-127">Opaque/1-bit alpha</span></span> | <span data-ttu-id="35580-128">Н/Д</span><span class="sxs-lookup"><span data-stu-id="35580-128">N/A</span></span>                  |
| <span data-ttu-id="35580-129">DXT2</span><span class="sxs-lookup"><span data-stu-id="35580-129">DXT2</span></span>   | <span data-ttu-id="35580-130">Явное альфа-канал</span><span class="sxs-lookup"><span data-stu-id="35580-130">Explicit alpha</span></span>     | <span data-ttu-id="35580-131">Да</span><span class="sxs-lookup"><span data-stu-id="35580-131">Yes</span></span>                  |
| <span data-ttu-id="35580-132">DXT3</span><span class="sxs-lookup"><span data-stu-id="35580-132">DXT3</span></span>   | <span data-ttu-id="35580-133">Явное альфа-канал</span><span class="sxs-lookup"><span data-stu-id="35580-133">Explicit alpha</span></span>     | <span data-ttu-id="35580-134">Нет</span><span class="sxs-lookup"><span data-stu-id="35580-134">No</span></span>                   |
| <span data-ttu-id="35580-135">DXT4</span><span class="sxs-lookup"><span data-stu-id="35580-135">DXT4</span></span>   | <span data-ttu-id="35580-136">Альфа-канал с интерполяцией</span><span class="sxs-lookup"><span data-stu-id="35580-136">Interpolated alpha</span></span> | <span data-ttu-id="35580-137">Да</span><span class="sxs-lookup"><span data-stu-id="35580-137">Yes</span></span>                  |
| <span data-ttu-id="35580-138">DXT5</span><span class="sxs-lookup"><span data-stu-id="35580-138">DXT5</span></span>   | <span data-ttu-id="35580-139">Альфа-канал с интерполяцией</span><span class="sxs-lookup"><span data-stu-id="35580-139">Interpolated alpha</span></span> | <span data-ttu-id="35580-140">Нет</span><span class="sxs-lookup"><span data-stu-id="35580-140">No</span></span>                   |



 

<span data-ttu-id="35580-141">При переносе данных из формата нонпремултиплиед в предварительно умноженный формат Direct3D масштабирует цвета на основе альфа-значений.</span><span class="sxs-lookup"><span data-stu-id="35580-141">When you transfer data from a nonpremultiplied format to a premultiplied format, Direct3D scales the colors based on the alpha values.</span></span> <span data-ttu-id="35580-142">Передача данных из предварительно умноженного формата в формат нонпремултиплиед не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="35580-142">Transferring data from a premultiplied format to a nonpremultiplied format is not supported.</span></span> <span data-ttu-id="35580-143">При попытке переместить данные из предварительно умноженного альфа-источника в назначение нонпремултиплиед Alpha метод возвращает D3DERR \_ инвалидкалл.</span><span class="sxs-lookup"><span data-stu-id="35580-143">If you try to transfer data from a premultiplied alpha source to a nonpremultiplied alpha destination, the method returns D3DERR\_INVALIDCALL.</span></span> <span data-ttu-id="35580-144">При переносе данных из предварительно умноженного альфа-источника в место назначения, не имеющее альфа-канала, исходные компоненты цвета, которые были масштабированы по альфа, копируются как есть.</span><span class="sxs-lookup"><span data-stu-id="35580-144">If you transfer data from a premultiplied alpha source to a destination that has no alpha, the source color components, which have been scaled by alpha, are copied as is.</span></span>

## <a name="decompressing-compressed-texture-surfaces"></a><span data-ttu-id="35580-145">Распаковка поверхностей сжатой текстуры</span><span class="sxs-lookup"><span data-stu-id="35580-145">Decompressing Compressed Texture Surfaces</span></span>

<span data-ttu-id="35580-146">Как и при сжатии текстурной поверхности, распаковка сжатой текстуры выполняется с помощью Direct3D-копирования служб.</span><span class="sxs-lookup"><span data-stu-id="35580-146">As with compressing a texture surface, decompressing a compressed texture is performed through Direct3D copying services.</span></span>

<span data-ttu-id="35580-147">Чтобы скопировать сжатую текстурную поверхность в несжатую текстуру, используйте функцию [**D3DXLoadSurfaceFromSurface**](d3dxloadsurfacefromsurface.md).</span><span class="sxs-lookup"><span data-stu-id="35580-147">To copy a compressed texture surface to a uncompressed texture surface, use the function [**D3DXLoadSurfaceFromSurface**](d3dxloadsurfacefromsurface.md).</span></span> <span data-ttu-id="35580-148">Эта функция обрабатывает сжатие в и из сжатых и несжатых поверхностей.</span><span class="sxs-lookup"><span data-stu-id="35580-148">This functions handles compression to and from compressed and uncompressed surfaces.</span></span>

## <a name="related-topics"></a><span data-ttu-id="35580-149">См. также</span><span class="sxs-lookup"><span data-stu-id="35580-149">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="35580-150">Сжатые ресурсы текстуры</span><span class="sxs-lookup"><span data-stu-id="35580-150">Compressed Texture Resources</span></span>](compressed-texture-resources.md)
</dt> </dl>

 

 
