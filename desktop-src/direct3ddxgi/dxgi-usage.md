---
description: Флаги для параметров создания поверхности и ресурсов.
ms.assetid: b5026566-89b5-458e-b36d-a55e5f8c10c1
title: DXGI_USAGE (DXGI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e55e99d86201c76fbe2ec229b13b5831d767ff34
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105703747"
---
# <a name="dxgi_usage"></a><span data-ttu-id="4c496-103">\_Использование DXGI</span><span class="sxs-lookup"><span data-stu-id="4c496-103">DXGI\_USAGE</span></span>

<span data-ttu-id="4c496-104">Флаги для параметров создания поверхности и ресурсов.</span><span class="sxs-lookup"><span data-stu-id="4c496-104">Flags for surface and resource creation options.</span></span>



| <span data-ttu-id="4c496-105">Константа/значение</span><span class="sxs-lookup"><span data-stu-id="4c496-105">Constant/value</span></span>                                                                                                                                                                                                                                                                                  | <span data-ttu-id="4c496-106">Описание</span><span class="sxs-lookup"><span data-stu-id="4c496-106">Description</span></span>                                                                                                                                                                                                                                                                                                                     |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="DXGI_USAGE_BACK_BUFFER"></span><span id="dxgi_usage_back_buffer"></span><dl> <span data-ttu-id="4c496-107"><dt>**DXGI \_ 1L \_ использования \_ буфера обмена**</dt> <dt>" << " (2 + 4)</dt></span><span class="sxs-lookup"><span data-stu-id="4c496-107"><dt>**DXGI\_USAGE\_BACK\_BUFFER**</dt> <dt>1L << (2 + 4)</dt></span></span> </dl>                             | <span data-ttu-id="4c496-108">Поверхность или ресурс используется в качестве заднего буфера.</span><span class="sxs-lookup"><span data-stu-id="4c496-108">The surface or resource is used as a back buffer.</span></span> <span data-ttu-id="4c496-109">При создании цепочки буферов не нужно передавать **\_ \_ обратную \_ буферизацию использования DXGI** .</span><span class="sxs-lookup"><span data-stu-id="4c496-109">You don’t need to pass **DXGI\_USAGE\_BACK\_BUFFER** when you create a swap chain.</span></span> <span data-ttu-id="4c496-110">Но можно определить, принадлежит ли ресурс к цепочке подкачки при вызове [**идксгиресаурце:: Usage**](/windows/desktop/api/DXGI/nf-dxgi-idxgiresource-getusage) и получении **\_ \_ обратного \_ буфера использования DXGI**.</span><span class="sxs-lookup"><span data-stu-id="4c496-110">But you can determine whether a resource belongs to a swap chain when you call [**IDXGIResource::GetUsage**](/windows/desktop/api/DXGI/nf-dxgi-idxgiresource-getusage) and get **DXGI\_USAGE\_BACK\_BUFFER**.</span></span><br/> |
| <span id="DXGI_USAGE_DISCARD_ON_PRESENT"></span><span id="dxgi_usage_discard_on_present"></span><dl> <span data-ttu-id="4c496-111"><dt>**DXGI \_ \_Отмена использования \_ в \_ настоящее**</dt> время <dt>1L <<  (5 + 4)</dt></span><span class="sxs-lookup"><span data-stu-id="4c496-111"><dt>**DXGI\_USAGE\_DISCARD\_ON\_PRESENT**</dt> <dt>1L << (5 + 4)</dt></span></span> </dl>       | <span data-ttu-id="4c496-112">Этот флаг предназначен только для внутреннего использования.</span><span class="sxs-lookup"><span data-stu-id="4c496-112">This flag is for internal use only.</span></span><br/>                                                                                                                                                                                                                                                                                  |
| <span id="DXGI_USAGE_READ_ONLY"></span><span id="dxgi_usage_read_only"></span><dl> <span data-ttu-id="4c496-113"><dt>**DXGI \_ ИСПОЛЬЗОВАНИЕ \_ \_ только для чтения**</dt> <dt> <<  1L (4 + 4)</dt></span><span class="sxs-lookup"><span data-stu-id="4c496-113"><dt>**DXGI\_USAGE\_READ\_ONLY**</dt> <dt>1L << (4 + 4)</dt></span></span> </dl>                                   | <span data-ttu-id="4c496-114">Используйте поверхность или ресурс только для чтения.</span><span class="sxs-lookup"><span data-stu-id="4c496-114">Use the surface or resource for reading only.</span></span><br/>                                                                                                                                                                                                                                                                        |
| <span id="DXGI_USAGE_RENDER_TARGET_OUTPUT"></span><span id="dxgi_usage_render_target_output"></span><dl> <span data-ttu-id="4c496-115"><dt>**DXGI \_ \_Целевой 1L прорисовки \_ \_ данных использования**</dt> <dt> <<  (1 + 4)</dt></span><span class="sxs-lookup"><span data-stu-id="4c496-115"><dt>**DXGI\_USAGE\_RENDER\_TARGET\_OUTPUT**</dt> <dt>1L << (1 + 4)</dt></span></span> </dl> | <span data-ttu-id="4c496-116">Используйте область или ресурс в качестве целевого объекта отрисовки выходных данных.</span><span class="sxs-lookup"><span data-stu-id="4c496-116">Use the surface or resource as an output render target.</span></span><br/>                                                                                                                                                                                                                                                              |
| <span id="DXGI_USAGE_SHADER_INPUT"></span><span id="dxgi_usage_shader_input"></span><dl> <span data-ttu-id="4c496-117"><dt>**DXGI \_ \_ \_ Входные 1L <<  шейдера использования**</dt> <dt>(0 + 4)</dt></span><span class="sxs-lookup"><span data-stu-id="4c496-117"><dt>**DXGI\_USAGE\_SHADER\_INPUT**</dt> <dt>1L << (0 + 4)</dt></span></span> </dl>                          | <span data-ttu-id="4c496-118">Используйте поверхность или ресурс в качестве входных данных для шейдера.</span><span class="sxs-lookup"><span data-stu-id="4c496-118">Use the surface or resource as an input to a shader.</span></span><br/>                                                                                                                                                                                                                                                                 |
| <span id="DXGI_USAGE_SHARED"></span><span id="dxgi_usage_shared"></span><dl> <span data-ttu-id="4c496-119"><dt>**DXGI \_ ИСПОЛЬЗОВАНИЕ \_ общего**</dt> <dt>1L <<  (3 + 4)</dt></span><span class="sxs-lookup"><span data-stu-id="4c496-119"><dt>**DXGI\_USAGE\_SHARED**</dt> <dt>1L << (3 + 4)</dt></span></span> </dl>                                             | <span data-ttu-id="4c496-120">Совместное использование поверхности или ресурса.</span><span class="sxs-lookup"><span data-stu-id="4c496-120">Share the surface or resource.</span></span><br/>                                                                                                                                                                                                                                                                                       |
| <span id="DXGI_USAGE_UNORDERED_ACCESS"></span><span id="dxgi_usage_unordered_access"></span><dl> <span data-ttu-id="4c496-121"><dt>**DXGI \_ ИСПОЛЬЗОВАНИЕ \_ НЕупорядоченного \_ доступа**</dt> <dt>1L <<  (6 + 4)</dt></span><span class="sxs-lookup"><span data-stu-id="4c496-121"><dt>**DXGI\_USAGE\_UNORDERED\_ACCESS**</dt> <dt>1L << (6 + 4)</dt></span></span> </dl>              | <span data-ttu-id="4c496-122">Используйте поверхность или ресурс для неупорядоченного доступа.</span><span class="sxs-lookup"><span data-stu-id="4c496-122">Use the surface or resource for unordered access.</span></span><br/>                                                                                                                                                                                                                                                                    |



## <a name="remarks"></a><span data-ttu-id="4c496-123">Комментарии</span><span class="sxs-lookup"><span data-stu-id="4c496-123">Remarks</span></span>

<span data-ttu-id="4c496-124">Каждый флаг определяется как целое число без знака.</span><span class="sxs-lookup"><span data-stu-id="4c496-124">Each flag is defined as an unsigned integer.</span></span>

``` syntax
#define DXGI_CPU_ACCESS_NONE    ( 0 )
#define DXGI_CPU_ACCESS_DYNAMIC    ( 1 )
#define DXGI_CPU_ACCESS_READ_WRITE    ( 2 )
#define DXGI_CPU_ACCESS_SCRATCH    ( 3 )
#define DXGI_CPU_ACCESS_FIELD        15
#define DXGI_USAGE_SHADER_INPUT             ( 1L << (0 + 4) )
#define DXGI_USAGE_RENDER_TARGET_OUTPUT     ( 1L << (1 + 4) )
#define DXGI_USAGE_BACK_BUFFER              ( 1L << (2 + 4) )
#define DXGI_USAGE_SHARED                   ( 1L << (3 + 4) )
#define DXGI_USAGE_READ_ONLY                ( 1L << (4 + 4) )
#define DXGI_USAGE_DISCARD_ON_PRESENT       ( 1L << (5 + 4) )
#define DXGI_USAGE_UNORDERED_ACCESS         ( 1L << (6 + 4) )
typedef UINT DXGI_USAGE;
```

<span data-ttu-id="4c496-125">Эти параметры флага используются при вызове метода [**идксгифактори:: креатесвапчаин**](/windows/desktop/api/DXGI/nf-dxgi-idxgifactory-createswapchain), [**IDXGIFactory2:: креатесвапчаинфорхвнд**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgifactory2-createswapchainforhwnd), [**IDXGIFactory2:: Креатесвапчаинфоркоревиндов**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgifactory2-createswapchainforcorewindow)или [**IDXGIFactory2:: CreateSwapChainForComposition**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgifactory2-createswapchainforcomposition) для описания использования поверхности и параметров доступа ЦП для заднего буфера цепочки буферов.</span><span class="sxs-lookup"><span data-stu-id="4c496-125">These flag options are used in a call to the [**IDXGIFactory::CreateSwapChain**](/windows/desktop/api/DXGI/nf-dxgi-idxgifactory-createswapchain), [**IDXGIFactory2::CreateSwapChainForHwnd**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgifactory2-createswapchainforhwnd), [**IDXGIFactory2::CreateSwapChainForCoreWindow**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgifactory2-createswapchainforcorewindow), or [**IDXGIFactory2::CreateSwapChainForComposition**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgifactory2-createswapchainforcomposition) method to describe the surface usage and CPU access options for the back buffer of a swap chain.</span></span> <span data-ttu-id="4c496-126">Вы не можете использовать **\_ \_ Общие сведения об использовании DXGI**, отменять их использование, а **\_ \_ \_ на \_** **DXGI — \_ \_ \_ только чтение** значений в качестве входных данных для создания цепочки буфера обмена.</span><span class="sxs-lookup"><span data-stu-id="4c496-126">You can't use the **DXGI\_USAGE\_SHARED**, **DXGI\_USAGE\_DISCARD\_ON\_PRESENT**, and **DXGI\_USAGE\_READ\_ONLY** values as input to create a swap chain.</span></span> <span data-ttu-id="4c496-127">Однако DXGI может устанавливать **\_ \_ отмену использования DXGI \_ в \_ настоящее** время **и \_ использование \_ DXGI \_ только для чтения** для некоторых задних буферов цепочки буфера обмена от имени приложения.</span><span class="sxs-lookup"><span data-stu-id="4c496-127">However, DXGI can set **DXGI\_USAGE\_DISCARD\_ON\_PRESENT** and **DXGI\_USAGE\_READ\_ONLY** for some of the swap chain's back buffers on the application's behalf.</span></span> <span data-ttu-id="4c496-128">Чтобы получить сведения об использовании этих задних буферов, можно вызвать метод [**идксгиресаурце:: Usage**](/windows/desktop/api/DXGI/nf-dxgi-idxgiresource-getusage) .</span><span class="sxs-lookup"><span data-stu-id="4c496-128">You can call the [**IDXGIResource::GetUsage**](/windows/desktop/api/DXGI/nf-dxgi-idxgiresource-getusage) method to retrieve the usage of these back buffers.</span></span> <span data-ttu-id="4c496-129">Цепь подкачки поддерживает значение " **\_ доступ ЦП \_ DXGI \_ None** " в **поле " \_ \_ доступ к \_ ЦП** DXGI" в разделе " **\_ Использование DXGI**".</span><span class="sxs-lookup"><span data-stu-id="4c496-129">Swap chain's only support the **DXGI\_CPU\_ACCESS\_NONE** value in the **DXGI\_CPU\_ACCESS\_FIELD** part of **DXGI\_USAGE**.</span></span>

<span data-ttu-id="4c496-130">Эти параметры флагов также используются методом [**идксгидевице:: креатесурфаце**](/windows/desktop/api/DXGI/nf-dxgi-idxgidevice-createsurface) .</span><span class="sxs-lookup"><span data-stu-id="4c496-130">These flag options are also used by the [**IDXGIDevice::CreateSurface**](/windows/desktop/api/DXGI/nf-dxgi-idxgidevice-createsurface) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="4c496-131">Требования</span><span class="sxs-lookup"><span data-stu-id="4c496-131">Requirements</span></span>



| <span data-ttu-id="4c496-132">Требование</span><span class="sxs-lookup"><span data-stu-id="4c496-132">Requirement</span></span> | <span data-ttu-id="4c496-133">Значение</span><span class="sxs-lookup"><span data-stu-id="4c496-133">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="4c496-134">Header</span><span class="sxs-lookup"><span data-stu-id="4c496-134">Header</span></span><br/> | <dl> <span data-ttu-id="4c496-135"><dt>DXGI. h</dt></span><span class="sxs-lookup"><span data-stu-id="4c496-135"><dt>DXGI.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4c496-136">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="4c496-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4c496-137">Константы DXGI</span><span class="sxs-lookup"><span data-stu-id="4c496-137">DXGI Constants</span></span>](d3d10-graphics-reference-dxgi-constants.md)
</dt> </dl>

 

 




