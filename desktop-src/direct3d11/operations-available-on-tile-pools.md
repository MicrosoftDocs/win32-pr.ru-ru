---
title: Доступные операции с пулами плиток
description: В этом разделе перечислены операции, которые можно выполнять с пулами плиток.
ms.assetid: 69CF182B-9161-43B7-89A5-0468E1BBD6B7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4a6c9ec58e6c9197f107f47cd7fe3513f43030c0
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104260908"
---
# <a name="operations-available-on-tile-pools"></a><span data-ttu-id="9dca5-103">Доступные операции с пулами плиток</span><span class="sxs-lookup"><span data-stu-id="9dca5-103">Operations available on tile pools</span></span>

<span data-ttu-id="9dca5-104">В этом разделе перечислены операции, которые можно выполнять с пулами плиток.</span><span class="sxs-lookup"><span data-stu-id="9dca5-104">This section lists operations that you can perform on tile pools.</span></span>

-   <span data-ttu-id="9dca5-105">Жизненный цикл пулов плиток работает так же, как любой другой ресурс Direct3D, поддерживаемый подсчетом ссылок, включая в этом случае отслеживание сопоставлений из мозаичных ресурсов.</span><span class="sxs-lookup"><span data-stu-id="9dca5-105">The lifetime of tile pools works like any other Direct3D Resource, backed by reference counting, including in this case tracking of mappings from tiled resources.</span></span> <span data-ttu-id="9dca5-106">Если приложение перестает ссылаться на пул плиток и все сопоставления плиток с памятью исчезли, а доступ к графическому процессору (GPU) завершен, операционная система освободит память, выделенную пулу плиток.</span><span class="sxs-lookup"><span data-stu-id="9dca5-106">When the application no longer references a tile pool and any tile mappings to the memory are gone and graphics processing unit (GPU) accesses completed, the operating system will deallocate the tile pool.</span></span>
-   <span data-ttu-id="9dca5-107">API-интерфейсы, связанные с совместным доступом к поверхности и синхронизацией для пулов плиток (но не непосредственно на мозаичных ресурсах).</span><span class="sxs-lookup"><span data-stu-id="9dca5-107">APIs related to surface sharing and synchronization work for tile pools (but not directly on tiled resources).</span></span> <span data-ttu-id="9dca5-108">Подобно поведению для предлагаемых пулов плиток, команды Direct3D, которые обращаются к мозаичным ресурсам, которые указывают на пул плиток, удаляются, если пул плиток был открыт и в данный момент получен другим устройством и процессом.</span><span class="sxs-lookup"><span data-stu-id="9dca5-108">Similar to the behavior for offered tile pools, Direct3D commands that access tiled resources that point to a tile pool are dropped if the tile pool has been shared and is currently acquired by another device and process.</span></span>
-   <span data-ttu-id="9dca5-109">Операция [**ID3D11DeviceContext2:: ресизетилепул**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-resizetilepool)</span><span class="sxs-lookup"><span data-stu-id="9dca5-109">[**ID3D11DeviceContext2::ResizeTilePool**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-resizetilepool) operation</span></span>
-   <span data-ttu-id="9dca5-110">[**IDXGIDevice2:: офферресаурцес**](/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgidevice2-offerresources) и [**реклаимресаурцес**](/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgidevice2-reclaimresources) Operations — эти API-интерфейсы для временного получения памяти в системе выполняются для всего пула плиток (и недоступны для отдельных мозаичных ресурсов).</span><span class="sxs-lookup"><span data-stu-id="9dca5-110">[**IDXGIDevice2::OfferResources**](/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgidevice2-offerresources) and [**ReclaimResources**](/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgidevice2-reclaimresources) operations - These APIs for yielding memory temporarily to the system operate on the entire tile pool (and aren't available for individual tiled resources).</span></span> <span data-ttu-id="9dca5-111">Если мозаичный ресурс указывает на плитку в предложенном пуле плиток, то мозаичный ресурс ведет себя так, как если бы он был предложен (например, среда выполнения удаляет команды, на которые она ссылается).</span><span class="sxs-lookup"><span data-stu-id="9dca5-111">If a tiled resource points to a tile in an offered tile pool, the tiled resource behaves as if it is offered (for example, the runtime drops commands that reference it).</span></span>

<span data-ttu-id="9dca5-112">Данные невозможно скопировать в память пула плиток и из нее напрямую.</span><span class="sxs-lookup"><span data-stu-id="9dca5-112">Data can't be copied to and from tile pool memory directly.</span></span> <span data-ttu-id="9dca5-113">Доступ к памяти всегда осуществляется с помощью мозаичных ресурсов.</span><span class="sxs-lookup"><span data-stu-id="9dca5-113">Accesses to the memory are always done through tiled resources.</span></span>

## <a name="related-topics"></a><span data-ttu-id="9dca5-114">См. также</span><span class="sxs-lookup"><span data-stu-id="9dca5-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9dca5-115">Создание мозаичных ресурсов</span><span class="sxs-lookup"><span data-stu-id="9dca5-115">Creating tiled resources</span></span>](creating-tiled-resources.md)
</dt> </dl>

 

 