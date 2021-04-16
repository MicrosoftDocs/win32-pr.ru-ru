---
description: Многоголовные карты — это общие буферы кадров и ускорители, независимые цифровые и аналоговые преобразователи (приложений уровня данных), а также мониторы выходных данных.
ms.assetid: f741cdb4-2eb6-42e9-81ea-a8c677e07582
title: Многоголовной (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4617666ca623795d33bf1dafcaafeabe73323253
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104494727"
---
# <a name="multihead-direct3d-9"></a><span data-ttu-id="d610f-103">Многоголовной (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="d610f-103">Multihead (Direct3D 9)</span></span>

<span data-ttu-id="d610f-104">Многоголовные карты — это общие буферы кадров и ускорители, независимые цифровые и аналоговые преобразователи (приложений уровня данных), а также мониторы выходных данных.</span><span class="sxs-lookup"><span data-stu-id="d610f-104">Multihead cards are those that have a common frame buffer and accelerator, independent digital-to-analog converters (DACs), and monitor outputs.</span></span> <span data-ttu-id="d610f-105">Такие устройства могут предоставлять гораздо более удобную поддержку нескольких мониторов, чем аналогичное число разнородных адаптеров отображения.</span><span class="sxs-lookup"><span data-stu-id="d610f-105">Such devices can offer much more usable multiple monitor support than a similar number of heterogeneous display adapters.</span></span>

<span data-ttu-id="d610f-106">Многоголовные карты представлены в API как одно устройство на уровне API, которое может послужить несколькими цепочками полноэкранного переключения.</span><span class="sxs-lookup"><span data-stu-id="d610f-106">Multihead cards are exposed in the API as a single API-level device that can drive several full-screen swap chains.</span></span> <span data-ttu-id="d610f-107">Следовательно, все ресурсы совместно используются всеми заголовками, и у каждого из них есть точно такие же возможности.</span><span class="sxs-lookup"><span data-stu-id="d610f-107">Consequently, all resources are shared with all the heads, and each head has exactly the same capabilities.</span></span> <span data-ttu-id="d610f-108">Для каждой головки можно задать независимые режимы экрана.</span><span class="sxs-lookup"><span data-stu-id="d610f-108">Each head can be set to independent display modes.</span></span> <span data-ttu-id="d610f-109">Для обновления каждого заголовка можно использовать отдельные вызовы [**IDirect3DSwapChain9::P.**](/windows/desktop/api)</span><span class="sxs-lookup"><span data-stu-id="d610f-109">You can use separate calls to [**IDirect3DSwapChain9::Present**](/windows/desktop/api) to refresh each head.</span></span> <span data-ttu-id="d610f-110">Для последовательного обновления каждого заголовка можно также использовать один вызов [**IDirect3DDevice9::P**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-present) .</span><span class="sxs-lookup"><span data-stu-id="d610f-110">You can also use one call to [**IDirect3DDevice9::Present**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-present) to refresh each head sequentially.</span></span>

> [!Note]  
> <span data-ttu-id="d610f-111">Обновление каждого заголовка не происходит одновременно с одним вызовом [**IDirect3DDevice9::P**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-present)повторной отправки.</span><span class="sxs-lookup"><span data-stu-id="d610f-111">The refresh of each head does not occur simultaneously with a single call to [**IDirect3DDevice9::Present**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-present).</span></span> <span data-ttu-id="d610f-112">Наличие статистики в Direct3D 9Ex может использовать структуру [**D3DPRESENTSTATS**](d3dpresentstats.md) для того, чтобы обновить каждую головку вблизи друг от друга, чтобы ограничить эффект разрывов в нескольких головах адаптеров.</span><span class="sxs-lookup"><span data-stu-id="d610f-112">Present statistics in Direct3D 9Ex can use the [**D3DPRESENTSTATS**](d3dpresentstats.md) structure to keep the refreshes to each head close to each other to limit tearing effects across multiple heads of adapters.</span></span> <span data-ttu-id="d610f-113">Сведения о синхронизации кадров в приложениях модели 9Ex для отражения Direct3D см. в разделе [улучшения Direct3D 9Ex](../direct3darticles/direct3d-9ex-improvements.md).</span><span class="sxs-lookup"><span data-stu-id="d610f-113">For information about synchronizing frames of Direct3D 9Ex flip model applications, see [Direct3D 9Ex Improvements](../direct3darticles/direct3d-9ex-improvements.md).</span></span>

 

<span data-ttu-id="d610f-114">Каждая цепочка подкачки для многоголовного устройства должна быть полноэкранной.</span><span class="sxs-lookup"><span data-stu-id="d610f-114">Each swap chain for a multihead device must be full screen.</span></span> <span data-ttu-id="d610f-115">Когда устройство перешло в многоголовной режим, оно должно оставаться в полноэкранном режиме.</span><span class="sxs-lookup"><span data-stu-id="d610f-115">When a device has entered multihead mode, it must remain full screen.</span></span> <span data-ttu-id="d610f-116">Переход обратно в оконный режим требует уничтожения устройства (за исключением обычной операции ALT + TAB-сворачивания).</span><span class="sxs-lookup"><span data-stu-id="d610f-116">The transition back to windowed mode requires the destruction of the device (except for the normal ALT+TAB-to-minimize operation).</span></span>

<span data-ttu-id="d610f-117">Старый метод разделения видеопамяти между головными элементами и разработкой каждого из них как полностью независимого ускорителя по-прежнему будет распространенным сценарием использования.</span><span class="sxs-lookup"><span data-stu-id="d610f-117">The old method of dividing video memory between the heads and treating each head as a fully independent accelerator will still be a common usage scenario.</span></span> <span data-ttu-id="d610f-118">Это предложение не заменяет этот механизм, если только приложение не было специально закодировано для работы в многоголовном режиме Direct3D 9.</span><span class="sxs-lookup"><span data-stu-id="d610f-118">This proposal does not replace that mechanism unless the application has been specifically coded to function in the Direct3D 9 multihead mode.</span></span>

<span data-ttu-id="d610f-119">Драйверам предоставлены достаточные знания для переключения между двумя режимами работы.</span><span class="sxs-lookup"><span data-stu-id="d610f-119">Drivers are given adequate knowledge to switch between the two modes of operation.</span></span>

<span data-ttu-id="d610f-120">Одна головка будет называться главным головным, а все остальные заголовки на той же карте будут называться подчиненными головками.</span><span class="sxs-lookup"><span data-stu-id="d610f-120">One head will be called the master head, and all other heads on the same card be called subordinate heads.</span></span> <span data-ttu-id="d610f-121">Если в системе имеется более одного многоголовного адаптера, главный и подчиненный адаптеры из одного многоголовного адаптера называются группой.</span><span class="sxs-lookup"><span data-stu-id="d610f-121">If more than one multihead adapter is present in a system, the master and its subordinates from one multihead adapter are called a group.</span></span> <span data-ttu-id="d610f-122">Группы обозначаются порядковым номером главного головного устройства.</span><span class="sxs-lookup"><span data-stu-id="d610f-122">Groups are denoted by the adapter ordinal of their master head.</span></span>

<span data-ttu-id="d610f-123">Структура [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) была обновлена для предоставления следующих новых аппаратных ограничений.</span><span class="sxs-lookup"><span data-stu-id="d610f-123">The [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) structure has been updated to expose the following new hardware caps.</span></span>


```
UINT NumberOfAdaptersInGroup; 
UINT MasterAdapterOrdinal; 
UINT AdapterOrdinalInGroup;
```



-   <span data-ttu-id="d610f-124">Нумберофадаптерсинграуп имеет значение 1 для стандартных адаптеров и больше 1 для главного адаптера многоголовной карты.</span><span class="sxs-lookup"><span data-stu-id="d610f-124">NumberOfAdaptersInGroup is 1 for conventional adapters, and greater than 1 for the master adapter of a multihead card.</span></span> <span data-ttu-id="d610f-125">Значение будет равно 0 для подчиненного адаптера многоголовной карты.</span><span class="sxs-lookup"><span data-stu-id="d610f-125">The value will be 0 for a subordinate adapter of a multihead card.</span></span> <span data-ttu-id="d610f-126">Каждая карточка может иметь не более одного главного сервера, но может иметь множество подчиненных.</span><span class="sxs-lookup"><span data-stu-id="d610f-126">Each card can have at most one master, but might have many subordinates.</span></span>
-   <span data-ttu-id="d610f-127">Мастерадаптерординал указывает, какое устройство является главным для этого подчиненного.</span><span class="sxs-lookup"><span data-stu-id="d610f-127">MasterAdapterOrdinal indicates which device is the master for this subordinate.</span></span>
-   <span data-ttu-id="d610f-128">Адаптерординалинграуп указывает порядок, в котором заголовки ссылаются API.</span><span class="sxs-lookup"><span data-stu-id="d610f-128">AdapterOrdinalInGroup indicates the order in which heads are referenced by the API.</span></span> <span data-ttu-id="d610f-129">У главного адаптера всегда есть Адаптерординалинграуп 0.</span><span class="sxs-lookup"><span data-stu-id="d610f-129">The master adapter always has AdapterOrdinalInGroup 0.</span></span> <span data-ttu-id="d610f-130">Эти значения не соответствуют порядковым номерам адаптеров, передаваемым методам IDirect3D9, но применяются только к заголовкам внутри группы.</span><span class="sxs-lookup"><span data-stu-id="d610f-130">These values do not correspond to the adapter ordinals passed to the IDirect3D9 methods, but apply only to heads within a group.</span></span>

<span data-ttu-id="d610f-131">Это определение позволяет многоголовным картам по прежнему представлять несколько адаптеров, как если бы они были независимыми картами, как и в DirectX 8.</span><span class="sxs-lookup"><span data-stu-id="d610f-131">This definition allows multihead cards to continue to present multiple adapters as if they were independent cards, just as they did in DirectX 8.</span></span>

<span data-ttu-id="d610f-132">Чтобы создать устройство с многоголовным заголовком, укажите флаг поведения D3DCREATE \_ адаптерграуп \_ Device в [**IDirect3D9:: креатедевице**](/windows/desktop/api).</span><span class="sxs-lookup"><span data-stu-id="d610f-132">To create a multihead device, specify the behavior flag D3DCREATE\_ADAPTERGROUP\_DEVICE in [**IDirect3D9::CreateDevice**](/windows/desktop/api).</span></span> <span data-ttu-id="d610f-133">Параметры представления (массив [**\_ параметров D3DPRESENT**](d3dpresent-parameters.md)) должны содержать элементы нумберофадаптерсинграуп.</span><span class="sxs-lookup"><span data-stu-id="d610f-133">The presentation parameters (an array of [**D3DPRESENT\_PARAMETERS**](d3dpresent-parameters.md)) should contain NumberOfAdaptersInGroup elements.</span></span> <span data-ttu-id="d610f-134">Среда выполнения будет назначать каждый элемент каждому заголовку в Адаптерординалинграуп числовом порядке.</span><span class="sxs-lookup"><span data-stu-id="d610f-134">The runtime will assign each element to each head in AdapterOrdinalInGroup numerical order.</span></span> <span data-ttu-id="d610f-135">Если \_ \_ задано устройство D3DCREATE адаптерграуп, каждый параметр презентации должен иметь следующее:</span><span class="sxs-lookup"><span data-stu-id="d610f-135">When D3DCREATE\_ADAPTERGROUP\_DEVICE is set, each presentation parameter must have:</span></span>

-   <span data-ttu-id="d610f-136">Оконный элемент **имеет значение false** (иными словами, в полноэкранном режиме).</span><span class="sxs-lookup"><span data-stu-id="d610f-136">The Windowed member set to **FALSE** (in other words, be full screen).</span></span>
-   <span data-ttu-id="d610f-137">То же значение для элемента ЕнаблеаутодепсстенЦил в [**\_ параметрах D3DPRESENT**](d3dpresent-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="d610f-137">The same value for the EnableAutoDepthStencil member of [**D3DPRESENT\_PARAMETERS**](d3dpresent-parameters.md).</span></span>

<span data-ttu-id="d610f-138">Кроме того, если ЕнаблеаутодепсстенЦил имеет **значение true**, то каждое из следующих полей должно иметь одно и то же значение для каждого [**\_ параметра D3DPRESENT**](d3dpresent-parameters.md):</span><span class="sxs-lookup"><span data-stu-id="d610f-138">In addition, if EnableAutoDepthStencil is **TRUE**, then each of the following fields must have the same value for each [**D3DPRESENT\_PARAMETERS**](d3dpresent-parameters.md):</span></span>

-   <span data-ttu-id="d610f-139">аутодепсстенЦилформат</span><span class="sxs-lookup"><span data-stu-id="d610f-139">AutoDepthStencilFormat</span></span>
-   <span data-ttu-id="d610f-140">баккбуффервидс</span><span class="sxs-lookup"><span data-stu-id="d610f-140">BackBufferWidth</span></span>
-   <span data-ttu-id="d610f-141">баккбуфферхеигхт</span><span class="sxs-lookup"><span data-stu-id="d610f-141">BackBufferHeight</span></span>
-   <span data-ttu-id="d610f-142">баккбуфферформат</span><span class="sxs-lookup"><span data-stu-id="d610f-142">BackBufferFormat</span></span>

<span data-ttu-id="d610f-143">Если установлено приложение уровня данных, дополнительные вызовы [**IDirect3DDevice9:: креатеаддитионалсвапчаин**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createadditionalswapchain) являются недопустимыми.</span><span class="sxs-lookup"><span data-stu-id="d610f-143">If DAC is set, additional calls to [**IDirect3DDevice9::CreateAdditionalSwapChain**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createadditionalswapchain) are illegal.</span></span>

<span data-ttu-id="d610f-144">Если устройство было создано с помощью DAC, [**IDirect3DDevice9:: Reset**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-reset) будет иметь массив [**\_ параметров D3DPRESENT**](d3dpresent-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="d610f-144">If the device was created with the DAC, [**IDirect3DDevice9::Reset**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-reset) will expect an array of [**D3DPRESENT\_PARAMETERS**](d3dpresent-parameters.md).</span></span>

<span data-ttu-id="d610f-145">Каждая [**Структура \_ параметров D3DPRESENT**](d3dpresent-parameters.md) , передаваемая [**IDirect3DDevice9:: Reset**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-reset) , должна быть полноэкранной.</span><span class="sxs-lookup"><span data-stu-id="d610f-145">Each [**D3DPRESENT\_PARAMETERS**](d3dpresent-parameters.md) structure passed to [**IDirect3DDevice9::Reset**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-reset) must be full screen.</span></span> <span data-ttu-id="d610f-146">Чтобы переключиться обратно в оконный режим, приложение должно уничтожить устройство и повторно создать устройство, не являющееся многоголовным, в оконном режиме.</span><span class="sxs-lookup"><span data-stu-id="d610f-146">To switch back to windowed mode, the application must destroy the device and re-create a non-multihead device in windowed mode.</span></span>

<span data-ttu-id="d610f-147">Ниже приведен простой сценарий использования.</span><span class="sxs-lookup"><span data-stu-id="d610f-147">Here is a basic usage scenario:</span></span>


```
1. Create multihead device 
2. For each swap chain of device:
   3. Call GetBackBuffer for the i-th swapchain
   4. Call SetRenderTarget 
   5. Call DrawPrimitive 
   6. Optionally call swapchain::Present (or wait until 
all swap chains are drawn and present outside of loop)
7. End the for loop
8. Optionally present all swap chains with device::Present
```



<span data-ttu-id="d610f-148">Дополнительные сведения см. в разделе [**IDirect3D9:: креатедевице**](/windows/desktop/api) and [**IDirect3DDevice9:: жетнумберофсвапчаинс**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getnumberofswapchains).</span><span class="sxs-lookup"><span data-stu-id="d610f-148">For more information, see [**IDirect3D9::CreateDevice**](/windows/desktop/api) and [**IDirect3DDevice9::GetNumberOfSwapChains**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getnumberofswapchains).</span></span>

## <a name="related-topics"></a><span data-ttu-id="d610f-149">См. также</span><span class="sxs-lookup"><span data-stu-id="d610f-149">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d610f-150">Советы по программированию</span><span class="sxs-lookup"><span data-stu-id="d610f-150">Programming Tips</span></span>](programming-tips.md)
</dt> </dl>

 

 
