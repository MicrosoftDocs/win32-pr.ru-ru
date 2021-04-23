---
title: Как получить уровень функций устройства
description: В этом разделе показано, как получить максимальный уровень функций, поддерживаемый устройством.
ms.assetid: 5eb7dd5b-3be3-4b7f-bcc7-20027fdfe6b5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4e587ad488a84641a92f0058d201014030e3467e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103888936"
---
# <a name="how-to-get-the-device-feature-level"></a><span data-ttu-id="cb55b-103">Как получить уровень функций устройства</span><span class="sxs-lookup"><span data-stu-id="cb55b-103">How To: Get the Device Feature Level</span></span>

<span data-ttu-id="cb55b-104">В этом разделе показано, как получить максимальный [уровень функций](overviews-direct3d-11-devices-downlevel-intro.md) , поддерживаемый [устройством](overviews-direct3d-11-devices-intro.md).</span><span class="sxs-lookup"><span data-stu-id="cb55b-104">This topics shows how to get the highest [feature level](overviews-direct3d-11-devices-downlevel-intro.md) supported by a [device](overviews-direct3d-11-devices-intro.md).</span></span> <span data-ttu-id="cb55b-105">Устройства Direct3D 11 поддерживают фиксированный набор уровней функций, определенных в перечислении [**\_ \_ уровня функций D3D**](/windows/desktop/api/D3DCommon/ne-d3dcommon-d3d_feature_level) .</span><span class="sxs-lookup"><span data-stu-id="cb55b-105">Direct3D 11 devices support a fixed set of feature levels that are defined in the [**D3D\_FEATURE\_LEVEL**](/windows/desktop/api/D3DCommon/ne-d3dcommon-d3d_feature_level) enumeration.</span></span> <span data-ttu-id="cb55b-106">Когда вы узнаете о высшем [уровне функций](overviews-direct3d-11-devices-downlevel-intro.md) , поддерживаемом устройством, вы можете использовать пути кода, подходящие для этого устройства.</span><span class="sxs-lookup"><span data-stu-id="cb55b-106">When you know the highest [feature level](overviews-direct3d-11-devices-downlevel-intro.md) supported by a device, you can run code paths that are appropriate for that device.</span></span>

<span data-ttu-id="cb55b-107">**Получение уровня функций устройства**</span><span class="sxs-lookup"><span data-stu-id="cb55b-107">**To get the device feature level**</span></span>

1.  <span data-ttu-id="cb55b-108">Вызовите либо функцию [**D3D11CreateDevice**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdevice) , либо функции [**D3D11CreateDeviceAndSwapChain**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdeviceandswapchain) , указав **значение NULL** для параметра *ппдевице* .</span><span class="sxs-lookup"><span data-stu-id="cb55b-108">Call either the [**D3D11CreateDevice**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdevice) function or the [**D3D11CreateDeviceAndSwapChain**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdeviceandswapchain) functions while specifying **NULL** for the *ppDevice* parameter.</span></span> <span data-ttu-id="cb55b-109">Это можно сделать до создания устройства.</span><span class="sxs-lookup"><span data-stu-id="cb55b-109">You can do this before device creation.</span></span>

    <span data-ttu-id="cb55b-110">\- или -</span><span class="sxs-lookup"><span data-stu-id="cb55b-110">\- or -</span></span>

    <span data-ttu-id="cb55b-111">Вызовите [**ID3D11Device:: жетфеатурелевел**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-getfeaturelevel) после создания устройства.</span><span class="sxs-lookup"><span data-stu-id="cb55b-111">Call [**ID3D11Device::GetFeatureLevel**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-getfeaturelevel) after device creation.</span></span>

2.  <span data-ttu-id="cb55b-112">Изучите значение возвращенного [**перечисления \_ \_ уровня функций D3D**](/windows/desktop/api/D3DCommon/ne-d3dcommon-d3d_feature_level) из последнего шага, чтобы определить поддерживаемый уровень компонентов.</span><span class="sxs-lookup"><span data-stu-id="cb55b-112">Examine the value of the returned [**D3D\_FEATURE\_LEVEL**](/windows/desktop/api/D3DCommon/ne-d3dcommon-d3d_feature_level) enumeration from the last step to determine the supported feature level.</span></span>

<span data-ttu-id="cb55b-113">В следующем примере кода показано, как определить максимальный поддерживаемый уровень компонентов, вызвав функцию [**D3D11CreateDevice**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdevice) .</span><span class="sxs-lookup"><span data-stu-id="cb55b-113">The following code example demonstrates how to determine the highest supported feature level by calling the [**D3D11CreateDevice**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdevice) function.</span></span> <span data-ttu-id="cb55b-114">**D3D11CreateDevice** сохраняет максимальный поддерживаемый уровень компонентов в переменной феатурелевел.</span><span class="sxs-lookup"><span data-stu-id="cb55b-114">**D3D11CreateDevice** stores the highest supported feature level in the FeatureLevel variable.</span></span> <span data-ttu-id="cb55b-115">Этот код можно использовать для проверки значения перечислимого типа на [**\_ \_ уровне компонента D3D**](/windows/desktop/api/D3DCommon/ne-d3dcommon-d3d_feature_level) , возвращаемого **D3D11CreateDevice** .</span><span class="sxs-lookup"><span data-stu-id="cb55b-115">You can use this code to examine the value of the [**D3D\_FEATURE\_LEVEL**](/windows/desktop/api/D3DCommon/ne-d3dcommon-d3d_feature_level) enumerated type that **D3D11CreateDevice** returns.</span></span> <span data-ttu-id="cb55b-116">Обратите внимание, что этот код перечисляет все уровни функций явным образом (для Direct3D 11,1 и Direct3D 11,2).</span><span class="sxs-lookup"><span data-stu-id="cb55b-116">Note that this code lists all feature levels explicitly (for Direct3D 11.1 and Direct3D 11.2).</span></span>

> [!Note]  
> <span data-ttu-id="cb55b-117">Если на компьютере установлена среда выполнения Direct3D 11,1, а *пфеатурелевелс* имеет значение **null**, эта функция не создает устройство D3D с [**\_ уровнем " \_ \_ 11 \_ 1**](/windows/desktop/api/D3DCommon/ne-d3dcommon-d3d_feature_level) ".</span><span class="sxs-lookup"><span data-stu-id="cb55b-117">If the Direct3D 11.1 runtime is present on the computer and *pFeatureLevels* is set to **NULL**, this function won't create a [**D3D\_FEATURE\_LEVEL\_11\_1**](/windows/desktop/api/D3DCommon/ne-d3dcommon-d3d_feature_level) device.</span></span> <span data-ttu-id="cb55b-118">Чтобы создать устройство **с \_ \_ уровнем D3D \_ 11 \_ 1** , необходимо явным образом предоставить массив **\_ \_ уровня компонентов D3D** , включающий **\_ уровень компонента D3D \_ \_ 11 \_ 1**.</span><span class="sxs-lookup"><span data-stu-id="cb55b-118">To create a **D3D\_FEATURE\_LEVEL\_11\_1** device, you must explicitly provide a **D3D\_FEATURE\_LEVEL** array that includes **D3D\_FEATURE\_LEVEL\_11\_1**.</span></span> <span data-ttu-id="cb55b-119">Если вы предоставляете **массив \_ \_ уровня функций D3D** , содержащий **\_ уровень D3D \_ уровня \_ 11 \_ 1** на компьютере, на котором не установлена среда выполнения Direct3D 11,1, эта функция немедленно завершается с параметром E \_ INVALIDARG.</span><span class="sxs-lookup"><span data-stu-id="cb55b-119">If you provide a **D3D\_FEATURE\_LEVEL** array that contains **D3D\_FEATURE\_LEVEL\_11\_1** on a computer that doesn't have the Direct3D 11.1 runtime installed, this function immediately fails with E\_INVALIDARG.</span></span>

 


```C++
HRESULT hr = E_FAIL;
D3D_FEATURE_LEVEL MaxSupportedFeatureLevel = D3D_FEATURE_LEVEL_9_1;
D3D_FEATURE_LEVEL FeatureLevels[] = {
    D3D_FEATURE_LEVEL_11_1,
    D3D_FEATURE_LEVEL_11_0,
    D3D_FEATURE_LEVEL_10_1,
    D3D_FEATURE_LEVEL_10_0,
    D3D_FEATURE_LEVEL_9_3,
    D3D_FEATURE_LEVEL_9_2,
    D3D_FEATURE_LEVEL_9_1
    };

hr = D3D11CreateDevice(
    NULL,
    D3D_DRIVER_TYPE_HARDWARE,
    NULL, 
    0, 
    &FeatureLevels, 
    ARRAYSIZE(FeatureLevels), 
    D3D11_SDK_VERSION, 
    NULL, 
    &MaxSupportedFeatureLevel, 
    NULL 
    );

if(FAILED(hr))
{
    return hr;
}
```



<span data-ttu-id="cb55b-120">В разделе [справочника 10Level9](d3d11-graphics-reference-10level9.md) перечислены различия между различными методами [**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device) и [**ссылку ID3D11DeviceContext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext) на различных уровнях функций 10Level9.</span><span class="sxs-lookup"><span data-stu-id="cb55b-120">The [10Level9 Reference](d3d11-graphics-reference-10level9.md) section lists the differences between how various [**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device) and [**ID3D11DeviceContext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext) methods behave at various 10Level9 feature levels.</span></span>

## <a name="related-topics"></a><span data-ttu-id="cb55b-121">См. также</span><span class="sxs-lookup"><span data-stu-id="cb55b-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cb55b-122">Direct3D 11 на оборудовании нижнего уровня</span><span class="sxs-lookup"><span data-stu-id="cb55b-122">Direct3D 11 on Downlevel Hardware</span></span>](overviews-direct3d-11-devices-downlevel.md)
</dt> <dt>

[<span data-ttu-id="cb55b-123">Использование Direct3D 11</span><span class="sxs-lookup"><span data-stu-id="cb55b-123">How to Use Direct3D 11</span></span>](how-to-use-direct3d-11.md)
</dt> </dl>

 

 




