---
title: Запись списка команд
description: В этом разделе показано, как создать и записать список команд.
ms.assetid: f5b90dfb-0b07-432e-813b-1541efbe3de5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 712f48386e0625c58a1f11c122d105064477ca8c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103777081"
---
# <a name="how-to-record-a-command-list"></a><span data-ttu-id="e668a-103">Как записать список команд</span><span class="sxs-lookup"><span data-stu-id="e668a-103">How to: Record a Command List</span></span>

<span data-ttu-id="e668a-104">[Список](overviews-direct3d-11-render-multi-thread-command-list.md) команд — это записанный список команд подготовки к просмотру.</span><span class="sxs-lookup"><span data-stu-id="e668a-104">A [command list](overviews-direct3d-11-render-multi-thread-command-list.md) is a recorded list of rendering commands.</span></span> <span data-ttu-id="e668a-105">В этом разделе показано, как создать и записать [список команд](overviews-direct3d-11-render-multi-thread-command-list.md).</span><span class="sxs-lookup"><span data-stu-id="e668a-105">This topic shows how to create and record a [command list](overviews-direct3d-11-render-multi-thread-command-list.md).</span></span> <span data-ttu-id="e668a-106">Используйте список команд для записи команд подготовки к просмотру и их последующего воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="e668a-106">Use a command list to record render commands and play them back later.</span></span> <span data-ttu-id="e668a-107">Список команд удобно использовать для разделения задач визуализации между потоками.</span><span class="sxs-lookup"><span data-stu-id="e668a-107">A command list is convenient for splitting rendering tasks between threads.</span></span>

<span data-ttu-id="e668a-108">**Запись списка команд**</span><span class="sxs-lookup"><span data-stu-id="e668a-108">**To record a command list**</span></span>

1.  <span data-ttu-id="e668a-109">Список команд должен быть создан из отложенного контекста, который содержит состояние устройства и действия визуализации.</span><span class="sxs-lookup"><span data-stu-id="e668a-109">A command list must be created from a deferred context, which contains device state and rendering actions.</span></span> <span data-ttu-id="e668a-110">При наличии устройства создайте отложенный контекст, вызвав [**ID3D11Device:: креатедеферредконтекст**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createdeferredcontext).</span><span class="sxs-lookup"><span data-stu-id="e668a-110">Given a device, create a deferred context by calling [**ID3D11Device::CreateDeferredContext**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createdeferredcontext).</span></span>

    ```
    HRESULT hr;
    ID3D11DeviceContext* pDeferredContext = NULL;

    hr = g_pd3dDevice->CreateDeferredContext(0, &pDeferredContext);
    ```

    

2.  <span data-ttu-id="e668a-111">Используйте отложенный контекст для подготовки к просмотру.</span><span class="sxs-lookup"><span data-stu-id="e668a-111">Use the deferred context to render.</span></span>

    ```
    float ClearColor[4] = { 0.0f, 0.125f, 0.3f, 1.0f };
    pDeferredContext->ClearRenderTargetView( g_pRenderTargetView, ClearColor );
        
    // Add additional rendering commands
    ...
    ```

    

    <span data-ttu-id="e668a-112">В этом простом примере очищается целевой объект прорисовки, но можно добавить дополнительные команды рендеринга.</span><span class="sxs-lookup"><span data-stu-id="e668a-112">This simple example clears a render target, but you could add additional render commands.</span></span>

3.  <span data-ttu-id="e668a-113">Создайте или запишите список команд путем вызова [**ссылку ID3D11DeviceContext:: финишкоммандлист**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-finishcommandlist) и передачи указателя на неинициализированный интерфейс [**ID3D11CommandList**](/windows/desktop/api/D3D11/nn-d3d11-id3d11commandlist) .</span><span class="sxs-lookup"><span data-stu-id="e668a-113">Create/record a command list by calling [**ID3D11DeviceContext::FinishCommandList**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-finishcommandlist) and passing a pointer to an uninitialized [**ID3D11CommandList**](/windows/desktop/api/D3D11/nn-d3d11-id3d11commandlist) interface.</span></span>

    ```
    ID3D11CommandList* pd3dCommandList = NULL;
    HRESULT hr;
    hr = pDeferredContext->FinishCommandList(FALSE, &pd3dCommandList);
    ```

    

    <span data-ttu-id="e668a-114">При возврате из метода создается список команд, содержащий все команды рендеринга, а интерфейс возвращается приложению.</span><span class="sxs-lookup"><span data-stu-id="e668a-114">When the method returns, a command list is created containing all the render commands and an interface is returned to the application.</span></span>

    <span data-ttu-id="e668a-115">Логический параметр указывает среде выполнения, что нужно сделать с состоянием конвейера в отложенном контексте.</span><span class="sxs-lookup"><span data-stu-id="e668a-115">The boolean parameter tells the runtime what to do with the pipeline state in the deferred context.</span></span> <span data-ttu-id="e668a-116">**Значение true** означает, что при завершении записи состояние контекста устройства будет восстановлено до состояния "до команды". **значение false** означает, что состояние не изменится после записи.</span><span class="sxs-lookup"><span data-stu-id="e668a-116">**TRUE** means restore the state of the device context to its pre-command list condition when recording is completed, **FALSE** means do not change the state after recording.</span></span> <span data-ttu-id="e668a-117">Это означает, что контекст устройства будет отражать изменения состояния, содержащиеся в списке команд.</span><span class="sxs-lookup"><span data-stu-id="e668a-117">This means that the device context will reflect the state changes contained in the command list.</span></span>

<span data-ttu-id="e668a-118">Пример воспроизведения списка команд см. в разделе [как воспроизвести список команд](overviews-direct3d-11-render-multi-thread-command-list-play.md).</span><span class="sxs-lookup"><span data-stu-id="e668a-118">To see an example for playing back a command list, see [How to: Play Back a Command List](overviews-direct3d-11-render-multi-thread-command-list-play.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="e668a-119">См. также</span><span class="sxs-lookup"><span data-stu-id="e668a-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e668a-120">Список команд</span><span class="sxs-lookup"><span data-stu-id="e668a-120">Command List</span></span>](overviews-direct3d-11-render-multi-thread-command-list.md)
</dt> <dt>

[<span data-ttu-id="e668a-121">Использование Direct3D 11</span><span class="sxs-lookup"><span data-stu-id="e668a-121">How to Use Direct3D 11</span></span>](how-to-use-direct3d-11.md)
</dt> </dl>

 

 




