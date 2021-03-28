---
title: Многопоточности
description: В Direct3D 11 реализована поддержка создания и отрисовки объектов с помощью нескольких потоков.
ms.assetid: 1bf50927-268b-4471-b059-819adf2189a9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8a4de7ca3e7e00ffba0c728aef334f21efc18899
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104258734"
---
# <a name="multithreading"></a><span data-ttu-id="5b216-103">Многопоточности</span><span class="sxs-lookup"><span data-stu-id="5b216-103">MultiThreading</span></span>

<span data-ttu-id="5b216-104">В Direct3D 11 реализована поддержка создания и отрисовки объектов с помощью нескольких потоков.</span><span class="sxs-lookup"><span data-stu-id="5b216-104">Direct3D 11 implements support for object creation and rendering using multiple threads.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="5b216-105">В этом разделе</span><span class="sxs-lookup"><span data-stu-id="5b216-105">In this section</span></span>



| <span data-ttu-id="5b216-106">Раздел</span><span class="sxs-lookup"><span data-stu-id="5b216-106">Topic</span></span>                                                                                                                   | <span data-ttu-id="5b216-107">Описание</span><span class="sxs-lookup"><span data-stu-id="5b216-107">Description</span></span>                                                                                                                                                                                                                          |
|-------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="5b216-108">Вводные сведения о многопоточности в Direct3D 11</span><span class="sxs-lookup"><span data-stu-id="5b216-108">Introduction to Multithreading in Direct3D 11</span></span>](overviews-direct3d-11-render-multi-thread-intro.md)<br/>         | <span data-ttu-id="5b216-109">Многопоточность разработана для повышения производительности за счет выполнения работы с использованием одного или нескольких потоков одновременно.</span><span class="sxs-lookup"><span data-stu-id="5b216-109">Multithreading is designed to improve performance by performing work using one or more threads at the same time.</span></span> <br/>                                                                                                         |
| [<span data-ttu-id="5b216-110">Создание объектов с использованием многопоточности</span><span class="sxs-lookup"><span data-stu-id="5b216-110">Object Creation with Multithreading</span></span>](overviews-direct3d-11-render-multi-thread-create.md)<br/>                  | <span data-ttu-id="5b216-111">Используйте интерфейс [**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device) для создания ресурсов и объектов, используйте [**ссылку ID3D11DeviceContext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext) для [отрисовки](overviews-direct3d-11-render-multi-thread-render.md).</span><span class="sxs-lookup"><span data-stu-id="5b216-111">Use the [**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device) interface to create resources and objects, use the [**ID3D11DeviceContext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext) for [rendering](overviews-direct3d-11-render-multi-thread-render.md).</span></span><br/> |
| [<span data-ttu-id="5b216-112">Немедленное и отложенное отображение</span><span class="sxs-lookup"><span data-stu-id="5b216-112">Immediate and Deferred Rendering</span></span>](overviews-direct3d-11-render-multi-thread-render.md)<br/>                     | <span data-ttu-id="5b216-113">Direct3D 11 поддерживает два типа отрисовки: немедленное и отложенное.</span><span class="sxs-lookup"><span data-stu-id="5b216-113">Direct3D 11 supports two types of rendering: immediate and deferred.</span></span> <span data-ttu-id="5b216-114">Оба метода реализуются с помощью интерфейса [**ссылку ID3D11DeviceContext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext) .</span><span class="sxs-lookup"><span data-stu-id="5b216-114">Both are implemented by using the [**ID3D11DeviceContext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext) interface.</span></span><br/>                                                      |
| [<span data-ttu-id="5b216-115">Список команд</span><span class="sxs-lookup"><span data-stu-id="5b216-115">Command List</span></span>](overviews-direct3d-11-render-multi-thread-command-list.md)<br/>                                   | <span data-ttu-id="5b216-116">Список команд — это последовательность команд GPU, которые можно записать и воспроизвести.</span><span class="sxs-lookup"><span data-stu-id="5b216-116">A command list is a sequence of GPU commands that can be recorded and played back.</span></span> <span data-ttu-id="5b216-117">Список команд может повысить производительность, уменьшая объем издержек, создаваемых средой выполнения.</span><span class="sxs-lookup"><span data-stu-id="5b216-117">A command list may improve performance by reducing the amount of overhead generated by the runtime.</span></span><br/>                                    |
| [<span data-ttu-id="5b216-118">Различия в потоках между версиями Direct3D</span><span class="sxs-lookup"><span data-stu-id="5b216-118">Threading Differences between Direct3D Versions</span></span>](overviews-direct3d-11-render-multi-thread-differences.md)<br/> | <span data-ttu-id="5b216-119">Многие многопоточные модели программирования используют примитивы синхронизации (такие как мьютексы) для создания критических разделов и предотвращения доступа к коду более чем одним потоком за раз.</span><span class="sxs-lookup"><span data-stu-id="5b216-119">Many multi-threaded programming models make use of synchronization primitives (such as mutexes) to create critical sections and prevent code from being accessed by more than one thread at a time.</span></span><br/>                       |



 

## <a name="related-topics"></a><span data-ttu-id="5b216-120">См. также</span><span class="sxs-lookup"><span data-stu-id="5b216-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5b216-121">Как проверить наличие поддержки драйверов</span><span class="sxs-lookup"><span data-stu-id="5b216-121">How To: Check for Driver Support</span></span>](overviews-direct3d-11-render-multi-thread-support.md)
</dt> <dt>

[<span data-ttu-id="5b216-122">Отрисовка</span><span class="sxs-lookup"><span data-stu-id="5b216-122">Rendering</span></span>](overviews-direct3d-11-render.md)
</dt> </dl>

 

 





