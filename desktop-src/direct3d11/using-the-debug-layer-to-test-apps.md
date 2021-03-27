---
title: Использование слоя отладки для отладки приложений
description: Здесь мы поговорим о том, как включить слой отладки и некоторые проблемы, которые можно предотвратить с помощью слоя отладки.
ms.assetid: 3C2B0A12-FB57-4400-BE39-05ED23F552C7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aaa3f4748da6893470e3bb6631c4228ec1ae3d48
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103773712"
---
# <a name="using-the-debug-layer-to-debug-apps"></a><span data-ttu-id="88cae-103">Использование слоя отладки для отладки приложений</span><span class="sxs-lookup"><span data-stu-id="88cae-103">Using the debug layer to debug apps</span></span>

<span data-ttu-id="88cae-104">Рекомендуется использовать [отладочный уровень](overviews-direct3d-11-devices-layers.md) для отладки приложений, чтобы гарантировать, что они будут очищать ошибки и предупреждения.</span><span class="sxs-lookup"><span data-stu-id="88cae-104">We recommend that you use the [debug layer](overviews-direct3d-11-devices-layers.md) to debug your apps to ensure that they are clean of errors and warnings.</span></span> <span data-ttu-id="88cae-105">Слой отладки помогает писать код Direct3D.</span><span class="sxs-lookup"><span data-stu-id="88cae-105">The debug layer helps you write Direct3D code.</span></span> <span data-ttu-id="88cae-106">Кроме того, производительность может увеличиться при использовании слоя отладки, поскольку можно сразу увидеть причины ошибок скрытой отрисовки или даже черные экраны в источнике.</span><span class="sxs-lookup"><span data-stu-id="88cae-106">In addition, your productivity can increase when you use the debug layer because you can immediately see the causes of obscure rendering errors or even black screens at their source.</span></span> <span data-ttu-id="88cae-107">Отладочный слой предоставляет предупреждения для многих проблем.</span><span class="sxs-lookup"><span data-stu-id="88cae-107">The debug layer provides warnings for many issues.</span></span> <span data-ttu-id="88cae-108">Например, уровень отладки выдает предупреждения для этих проблем:</span><span class="sxs-lookup"><span data-stu-id="88cae-108">For example, the debug layer provides warnings for these issues:</span></span>

-   <span data-ttu-id="88cae-109">Забыли установить текстуру, но прочесть ее в шейдере пикселей</span><span class="sxs-lookup"><span data-stu-id="88cae-109">Forgot to set a texture but read from it in your pixel shader</span></span>
-   <span data-ttu-id="88cae-110">Глубина вывода, но не имеет привязки состояния шаблона глубины</span><span class="sxs-lookup"><span data-stu-id="88cae-110">Output depth but have no depth-stencil state bound</span></span>
-   <span data-ttu-id="88cae-111">Не удалось создать текстуру с помощью INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="88cae-111">Texture creation failed with INVALIDARG</span></span>

<span data-ttu-id="88cae-112">Здесь мы поговорим о том, как включить [слой отладки](overviews-direct3d-11-devices-layers.md) и некоторые проблемы, которые можно предотвратить с помощью слоя отладки.</span><span class="sxs-lookup"><span data-stu-id="88cae-112">Here we talk about how to enable the [debug layer](overviews-direct3d-11-devices-layers.md) and some of the issues that you can prevent by using the debug layer.</span></span>

-   [<span data-ttu-id="88cae-113">Включение слоя отладки</span><span class="sxs-lookup"><span data-stu-id="88cae-113">Enabling the debug layer</span></span>](#enabling-the-debug-layer)
-   [<span data-ttu-id="88cae-114">Предотвращение ошибок в приложении с помощью слоя отладки</span><span class="sxs-lookup"><span data-stu-id="88cae-114">Preventing errors in your app with the debug layer</span></span>](#preventing-errors-in-your-app-with-the-debug-layer)
    -   [<span data-ttu-id="88cae-115">Не передавать пустые указатели в Map</span><span class="sxs-lookup"><span data-stu-id="88cae-115">Don't pass NULL pointers to Map</span></span>](#dont-pass-null-pointers-to-map)
    -   [<span data-ttu-id="88cae-116">Ограничить исходное поле в исходных и целевых ресурсах</span><span class="sxs-lookup"><span data-stu-id="88cae-116">Confine source box within source and destination resources</span></span>](#confine-source-box-within-source-and-destination-resources)
    -   [<span data-ttu-id="88cae-117">Не удалять Дискардресаурце или Дискардвиев</span><span class="sxs-lookup"><span data-stu-id="88cae-117">Don't drop DiscardResource or DiscardView</span></span>](#dont-drop-discardresource-or-discardview)
-   [<span data-ttu-id="88cae-118">См. также</span><span class="sxs-lookup"><span data-stu-id="88cae-118">Related topics</span></span>](#related-topics)

## <a name="enabling-the-debug-layer"></a><span data-ttu-id="88cae-119">Включение слоя отладки</span><span class="sxs-lookup"><span data-stu-id="88cae-119">Enabling the debug layer</span></span>

<span data-ttu-id="88cae-120">Чтобы включить [слой отладки](overviews-direct3d-11-devices-layers.md), укажите в параметре *flags* флаг [**D3D11 \_ Create \_ Device \_ Debug**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_create_device_flag) , если вызывается функция [**D3D11CreateDevice**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdevice) для создания устройства отрисовки.</span><span class="sxs-lookup"><span data-stu-id="88cae-120">To enable the [debug layer](overviews-direct3d-11-devices-layers.md), specify the [**D3D11\_CREATE\_DEVICE\_DEBUG**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_create_device_flag) flag in the *Flags* parameter when you call the [**D3D11CreateDevice**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdevice) function to create the rendering device.</span></span> <span data-ttu-id="88cae-121">В этом примере кода показано, как включить слой отладки, если проект Microsoft Visual Studio находится в отладочной сборке:</span><span class="sxs-lookup"><span data-stu-id="88cae-121">This example code shows how to enable the debug layer when your Microsoft Visual Studio project is in a debug build:</span></span>


```C++
        UINT creationFlags = D3D11_CREATE_DEVICE_BGRA_SUPPORT;
#if defined(_DEBUG)
        // If the project is in a debug build, enable the debug layer.
        creationFlags |= D3D11_CREATE_DEVICE_DEBUG;
#endif
        // Define the ordering of feature levels that Direct3D attempts to create.
        D3D_FEATURE_LEVEL featureLevels[] =
        {
            D3D_FEATURE_LEVEL_11_1,
            D3D_FEATURE_LEVEL_11_0,
            D3D_FEATURE_LEVEL_10_1,
            D3D_FEATURE_LEVEL_10_0,
            D3D_FEATURE_LEVEL_9_3,
            D3D_FEATURE_LEVEL_9_1
        };

        ComPtr<ID3D11Device> d3dDevice;
        ComPtr<ID3D11DeviceContext> d3dDeviceContext;
        DX::ThrowIfFailed(
            D3D11CreateDevice(
                nullptr,                    // specify nullptr to use the default adapter
                D3D_DRIVER_TYPE_HARDWARE,
                nullptr,                    // specify nullptr because D3D_DRIVER_TYPE_HARDWARE 
                                            // indicates that this function uses hardware
                creationFlags,              // optionally set debug and Direct2D compatibility flags
                featureLevels,
                ARRAYSIZE(featureLevels),
                D3D11_SDK_VERSION,          // always set this to D3D11_SDK_VERSION
                &d3dDevice,
                nullptr,
                &d3dDeviceContext
                )
            );
```



## <a name="preventing-errors-in-your-app-with-the-debug-layer"></a><span data-ttu-id="88cae-122">Предотвращение ошибок в приложении с помощью слоя отладки</span><span class="sxs-lookup"><span data-stu-id="88cae-122">Preventing errors in your app with the debug layer</span></span>

<span data-ttu-id="88cae-123">При неправильном использовании API Direct3D 11 или при передаче неправильных параметров отладочный вывод [слоя отладки](overviews-direct3d-11-devices-layers.md) сообщает об ошибке или предупреждении.</span><span class="sxs-lookup"><span data-stu-id="88cae-123">If you misuse the Direct3D 11 API or pass bad parameters, the debug output of the [debug layer](overviews-direct3d-11-devices-layers.md) reports an error or a warning.</span></span> <span data-ttu-id="88cae-124">После этого можно исправить ошибку.</span><span class="sxs-lookup"><span data-stu-id="88cae-124">You can then correct your mistake.</span></span> <span data-ttu-id="88cae-125">Далее мы рассмотрим некоторые проблемы с кодированием, которые могут вызвать неопределенное поведение или даже сбой операционной системы.</span><span class="sxs-lookup"><span data-stu-id="88cae-125">Next, we look at some coding issues that can cause undefined behavior or even the operating system to crash.</span></span> <span data-ttu-id="88cae-126">Можно перехватывать и предотвращать эти проблемы с помощью слоя отладки.</span><span class="sxs-lookup"><span data-stu-id="88cae-126">You can catch and prevent these issues by using the debug layer.</span></span>

### <a name="dont-pass-null-pointers-to-map"></a><span data-ttu-id="88cae-127">Не передавать пустые указатели в Map</span><span class="sxs-lookup"><span data-stu-id="88cae-127">Don't pass NULL pointers to Map</span></span>

<span data-ttu-id="88cae-128">Если **значение NULL** передается *в* параметре *Пмаппедресаурце* или в методе [**ссылку ID3D11DeviceContext:: Map**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-map) , поведение **Map** не определено.</span><span class="sxs-lookup"><span data-stu-id="88cae-128">If you pass **NULL** to the *pResource* or *pMappedResource* parameter of the [**ID3D11DeviceContext::Map**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-map) method, the behavior of **Map** is undefined.</span></span> <span data-ttu-id="88cae-129">Если вы создали устройство, которое только поддерживает [основной уровень](overviews-direct3d-11-devices-layers.md), недопустимые параметры для **Map** могут вызвать сбой операционной системы.</span><span class="sxs-lookup"><span data-stu-id="88cae-129">If you created a device that just supports the [core layer](overviews-direct3d-11-devices-layers.md), invalid parameters to **Map** can crash the operating system.</span></span> <span data-ttu-id="88cae-130">Если вы создали устройство, которое поддерживает [отладочный слой](overviews-direct3d-11-devices-layers.md), отладочный вывод сообщает об ошибке в этом неверном вызове **Map** .</span><span class="sxs-lookup"><span data-stu-id="88cae-130">If you created a device that supports the [debug layer](overviews-direct3d-11-devices-layers.md), the debug output reports an error on this invalid **Map** call.</span></span>

### <a name="confine-source-box-within-source-and-destination-resources"></a><span data-ttu-id="88cae-131">Ограничить исходное поле в исходных и целевых ресурсах</span><span class="sxs-lookup"><span data-stu-id="88cae-131">Confine source box within source and destination resources</span></span>

<span data-ttu-id="88cae-132">При вызове метода [**ссылку ID3D11DeviceContext:: кописубресаурцерегион**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-copysubresourceregion) исходное поле должно находиться в пределах исходного ресурса.</span><span class="sxs-lookup"><span data-stu-id="88cae-132">In a call to the [**ID3D11DeviceContext::CopySubresourceRegion**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-copysubresourceregion) method, the source box must be within the source resource.</span></span> <span data-ttu-id="88cae-133">Смещение назначения (x, y и z) разрешает смещение исходного поля при записи в целевой ресурс, но размеры исходного поля и смещения должны быть в пределах размера ресурса.</span><span class="sxs-lookup"><span data-stu-id="88cae-133">The destination offsets, (x, y, and z) allow the source box to be offset when writing into the destination resource, but the dimensions of the source box and the offsets must be within the size of the resource.</span></span> <span data-ttu-id="88cae-134">При попытке копирования за пределами целевого ресурса или указания исходного поля, которое больше, чем исходный ресурс, поведение **кописубресаурцерегион** не определено.</span><span class="sxs-lookup"><span data-stu-id="88cae-134">If you try to copy outside the destination resource or specify a source box that is larger than the source resource, the behavior of **CopySubresourceRegion** is undefined.</span></span> <span data-ttu-id="88cae-135">Если вы создали устройство, которое поддерживает [отладочный слой](overviews-direct3d-11-devices-layers.md), выходные данные отладки будут сообщать об ошибке в этом недействительном вызове **кописубресаурцерегион** .</span><span class="sxs-lookup"><span data-stu-id="88cae-135">If you created a device that supports the [debug layer](overviews-direct3d-11-devices-layers.md), the debug output reports an error on this invalid **CopySubresourceRegion** call.</span></span> <span data-ttu-id="88cae-136">Недопустимые параметры **кописубресаурцерегион** приводят к неопределенному поведению и могут привести к неправильной отрисовке, обрезке, отсутствию копии или даже удалению устройства отрисовки.</span><span class="sxs-lookup"><span data-stu-id="88cae-136">Invalid parameters to **CopySubresourceRegion** cause undefined behavior and might result in incorrect rendering, clipping, no copy, or even the removal of the rendering device.</span></span>

### <a name="dont-drop-discardresource-or-discardview"></a><span data-ttu-id="88cae-137">Не удалять Дискардресаурце или Дискардвиев</span><span class="sxs-lookup"><span data-stu-id="88cae-137">Don't drop DiscardResource or DiscardView</span></span>

<span data-ttu-id="88cae-138">Среда выполнения удаляет вызов [**ID3D11DeviceContext1::D искардресаурце**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11devicecontext1-discardresource) или [**ID3D11DeviceContext1::D искардвиев**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11devicecontext1-discardview) , если ресурс не был правильно создан.</span><span class="sxs-lookup"><span data-stu-id="88cae-138">The runtime drops a call to [**ID3D11DeviceContext1::DiscardResource**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11devicecontext1-discardresource) or [**ID3D11DeviceContext1::DiscardView**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11devicecontext1-discardview) unless you correctly create the resource.</span></span>

<span data-ttu-id="88cae-139">Ресурс, который передается в [**ID3D11DeviceContext1::D искардресаурце**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11devicecontext1-discardresource) , должен быть создан с помощью [**D3D11 \_ использования \_ по умолчанию**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_usage) или [**\_ \_ динамического использования D3D11**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_usage). в противном случае среда выполнения удаляет вызов **дискардресаурце**.</span><span class="sxs-lookup"><span data-stu-id="88cae-139">The resource that you pass to [**ID3D11DeviceContext1::DiscardResource**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11devicecontext1-discardresource) must have been created by using [**D3D11\_USAGE\_DEFAULT**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_usage) or [**D3D11\_USAGE\_DYNAMIC**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_usage), otherwise the runtime drops the call to **DiscardResource**.</span></span>

<span data-ttu-id="88cae-140">Ресурс, лежащий в основе представления, передаваемого в [**ID3D11DeviceContext1::D искардвиев**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11devicecontext1-discardview) , должен быть создан с помощью [**D3D11 \_ использования \_ по умолчанию**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_usage) или [**\_ \_ динамического использования D3D11**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_usage). в противном случае среда выполнения удаляет вызов **дискардвиев**.</span><span class="sxs-lookup"><span data-stu-id="88cae-140">The resource that underlies the view that you pass to [**ID3D11DeviceContext1::DiscardView**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11devicecontext1-discardview) must have been created using [**D3D11\_USAGE\_DEFAULT**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_usage) or [**D3D11\_USAGE\_DYNAMIC**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_usage), otherwise the runtime drops the call to **DiscardView**.</span></span>

<span data-ttu-id="88cae-141">Если вы создали устройство, которое поддерживает [уровень отладки](overviews-direct3d-11-devices-layers.md), отладочный вывод сообщает об ошибке в отношении удаленного вызова.</span><span class="sxs-lookup"><span data-stu-id="88cae-141">If you created a device that supports the [debug layer](overviews-direct3d-11-devices-layers.md), the debug output reports an error regarding the dropped call.</span></span>

## <a name="related-topics"></a><span data-ttu-id="88cae-142">См. также</span><span class="sxs-lookup"><span data-stu-id="88cae-142">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="88cae-143">Программные уровни</span><span class="sxs-lookup"><span data-stu-id="88cae-143">Software Layers</span></span>](overviews-direct3d-11-devices-layers.md)
</dt> </dl>

 

 




