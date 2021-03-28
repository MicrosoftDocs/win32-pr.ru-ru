---
title: Воспроизведение списка команд
description: В этом разделе показано, как воспроизвести список команд.
ms.assetid: 4e6c0a98-85ff-45ca-963b-7d5c55f47195
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8d04df73b481adea17e1f985e2c1851039fd016a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104996767"
---
# <a name="how-to-play-back-a-command-list"></a><span data-ttu-id="92e7f-103">Как воспроизвести список команд</span><span class="sxs-lookup"><span data-stu-id="92e7f-103">How to: Play Back a Command List</span></span>

<span data-ttu-id="92e7f-104">[Список](overviews-direct3d-11-render-multi-thread-command-list.md) команд — это записанный список команд подготовки к просмотру.</span><span class="sxs-lookup"><span data-stu-id="92e7f-104">A [command list](overviews-direct3d-11-render-multi-thread-command-list.md) is a recorded list of rendering commands.</span></span> <span data-ttu-id="92e7f-105">Используйте список команд для предварительной записи команд рисования и воспроизведения их позже.</span><span class="sxs-lookup"><span data-stu-id="92e7f-105">Use a command list to pre-record drawing commands and play them back later.</span></span> <span data-ttu-id="92e7f-106">В этом разделе показано, как воспроизвести [список команд](overviews-direct3d-11-render-multi-thread-command-list.md).</span><span class="sxs-lookup"><span data-stu-id="92e7f-106">This topic shows how to play back a [command list](overviews-direct3d-11-render-multi-thread-command-list.md).</span></span> <span data-ttu-id="92e7f-107">Список команд можно использовать для разделения задач визуализации между потоками.</span><span class="sxs-lookup"><span data-stu-id="92e7f-107">A command list can be used to split rendering tasks between threads.</span></span>

<span data-ttu-id="92e7f-108">В этом разделе описывается воспроизведение списка команд.</span><span class="sxs-lookup"><span data-stu-id="92e7f-108">This section describes how to play back a command list.</span></span> <span data-ttu-id="92e7f-109">Сведения о записи списка команд см. [в разделе как записать список команд](overviews-direct3d-11-render-multi-thread-command-list-record.md).</span><span class="sxs-lookup"><span data-stu-id="92e7f-109">For recording a command list, see [How to: Record a Command List](overviews-direct3d-11-render-multi-thread-command-list-record.md).</span></span>

<span data-ttu-id="92e7f-110">**Воспроизведение списка команд**</span><span class="sxs-lookup"><span data-stu-id="92e7f-110">**To play back a command list**</span></span>

-   <span data-ttu-id="92e7f-111">Вызовите [**ссылку ID3D11DeviceContext:: вызова элемента executecommandlist**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-executecommandlist) и передайте допустимый объект [**ID3D11CommandList**](/windows/desktop/api/D3D11/nn-d3d11-id3d11commandlist) .</span><span class="sxs-lookup"><span data-stu-id="92e7f-111">Call [**ID3D11DeviceContext::ExecuteCommandList**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-executecommandlist) and pass a valid [**ID3D11CommandList**](/windows/desktop/api/D3D11/nn-d3d11-id3d11commandlist) object.</span></span>
    ```
    if(g_pd3dCommandList)
    {
        g_pImmediateContext->ExecuteCommandList(g_pd3dCommandList, TRUE);
    }
    ```

    

<span data-ttu-id="92e7f-112">[**Вызова элемента executecommandlist**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-executecommandlist) должен выполняться в [непосредственных контекстах](overviews-direct3d-11-devices-intro.md) для записанных команд, которые должны выполняться в графическом процессоре.</span><span class="sxs-lookup"><span data-stu-id="92e7f-112">[**ExecuteCommandList**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-executecommandlist) must be executed on the [immediate context](overviews-direct3d-11-devices-intro.md) for recorded commands to be run on the graphics processing unit (GPU).</span></span> <span data-ttu-id="92e7f-113">Используйте непосредственный контекст для передачи команд в GPU для выполнения, используйте отложенный контекст для записи команд для воспроизведения в другой список команд.</span><span class="sxs-lookup"><span data-stu-id="92e7f-113">Use the immediate context to feed commands to the GPU for execution, use a deferred context to record commands for playback onto another command list.</span></span> <span data-ttu-id="92e7f-114">При вызове **вызова элемента executecommandlist** в другом отложенном контексте создается список отложенных команд.</span><span class="sxs-lookup"><span data-stu-id="92e7f-114">When you call **ExecuteCommandList** onto another deferred context, you create a ‘merged’ deferred command list.</span></span> <span data-ttu-id="92e7f-115">Чтобы выполнить команды в объединенном списке отложенных команд, необходимо выполнить их в непосредственных контекстах.</span><span class="sxs-lookup"><span data-stu-id="92e7f-115">To run the commands on the merged deferred command list, you need to execute them on the immediate context.</span></span>

## <a name="related-topics"></a><span data-ttu-id="92e7f-116">См. также</span><span class="sxs-lookup"><span data-stu-id="92e7f-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="92e7f-117">Список команд</span><span class="sxs-lookup"><span data-stu-id="92e7f-117">Command List</span></span>](overviews-direct3d-11-render-multi-thread-command-list.md)
</dt> <dt>

[<span data-ttu-id="92e7f-118">Использование Direct3D 11</span><span class="sxs-lookup"><span data-stu-id="92e7f-118">How to Use Direct3D 11</span></span>](how-to-use-direct3d-11.md)
</dt> </dl>

 

 




