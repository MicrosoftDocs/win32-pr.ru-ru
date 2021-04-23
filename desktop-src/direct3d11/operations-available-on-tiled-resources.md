---
title: Операции, доступные для мозаичных ресурсов
description: В этом разделе перечислены операции, которые можно выполнять с мозаичными ресурсами.
ms.assetid: 1CF42A18-B6EA-4BA9-BEDE-9A8CC083CBAF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d45d051943816502fd0bafb77e67241026f31498
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104068398"
---
# <a name="operations-available-on-tiled-resources"></a><span data-ttu-id="f3508-103">Операции, доступные для мозаичных ресурсов</span><span class="sxs-lookup"><span data-stu-id="f3508-103">Operations available on tiled resources</span></span>

<span data-ttu-id="f3508-104">В этом разделе перечислены операции, которые можно выполнять с мозаичными ресурсами.</span><span class="sxs-lookup"><span data-stu-id="f3508-104">This section lists operations that you can perform on tiled resources.</span></span>

-   <span data-ttu-id="f3508-105">void [**ID3D11DeviceContext2:: упдатетилемаппингс**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-updatetilemappings) and [**ID3D11DeviceContext2:: копитилемаппингс**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-copytilemappings) Operations — эти расположения плиток точек в мозаичном ресурсе для размещения в пулах плиток, а также для значений NULL или для обоих.</span><span class="sxs-lookup"><span data-stu-id="f3508-105">void [**ID3D11DeviceContext2::UpdateTileMappings**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-updatetilemappings) and [**ID3D11DeviceContext2::CopyTileMappings**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-copytilemappings) operations - These operations point tile locations in a tiled resource to locations in tile pools, or to NULL, or to both.</span></span> <span data-ttu-id="f3508-106">Эти операции могут обновлять раздельные подмножества указателей плиток.</span><span class="sxs-lookup"><span data-stu-id="f3508-106">These operations can update a disjoint subset of the tile pointers.</span></span>
-   <span data-ttu-id="f3508-107">\*Операции копирования () и Update \* () — все API-интерфейсы, которые могут копировать данные в рабочую область пула по умолчанию (например, [**ID3D11DeviceContext1:: CopySubresourceRegion1**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11devicecontext1-copysubresourceregion1) и [**ID3D11DeviceContext1:: UpdateSubresource1**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11devicecontext1-updatesubresource1)), работают для мозаичных ресурсов.</span><span class="sxs-lookup"><span data-stu-id="f3508-107">Copy\*() and Update\*() operations - All the APIs that can copy data to and from a default pool surface (for example, [**ID3D11DeviceContext1::CopySubresourceRegion1**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11devicecontext1-copysubresourceregion1) and [**ID3D11DeviceContext1::UpdateSubresource1**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11devicecontext1-updatesubresource1)) work for tiled resources.</span></span> <span data-ttu-id="f3508-108">Чтение из несопоставленных плиток дает 0, а операции записи в несопоставленные плитки не выполняются.</span><span class="sxs-lookup"><span data-stu-id="f3508-108">Reading from unmapped tiles produces 0 and writes to unmapped tiles are dropped.</span></span>
-   <span data-ttu-id="f3508-109">Операции [**ID3D11DeviceContext2:: копитилес**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-copytiles) и [**ID3D11DeviceContext2:: упдатетилес**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-updatetiles) . Эти операции существуют для копирования плиток по степени гранулярности 64 КБ на детализацию и из любого ресурса-буфера в каноническом макете памяти.</span><span class="sxs-lookup"><span data-stu-id="f3508-109">[**ID3D11DeviceContext2::CopyTiles**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-copytiles) and [**ID3D11DeviceContext2::UpdateTiles**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-updatetiles) operations - These operations exist for copying tiles at 64KB granularity to and from any tiled resource and a buffer resource in a canonical memory layout.</span></span> <span data-ttu-id="f3508-110">Видеодрайвер и оборудование выполняют любую память "группирующие", необходимую для мозаичного ресурса.</span><span class="sxs-lookup"><span data-stu-id="f3508-110">The display driver and hardware perform any memory "swizzling" necessary for the tiled resource.</span></span>
-   <span data-ttu-id="f3508-111">Привязки конвейера Direct3D и представления и привязки представлений, которые будут работать с ресурсами, не являющимися мозаичными, работают и для мозаичных ресурсов.</span><span class="sxs-lookup"><span data-stu-id="f3508-111">Direct3D pipeline bindings and view creations / bindings that would work on non-tiled resources work on tiled resources as well.</span></span>

<span data-ttu-id="f3508-112">Элементы управления плиткой доступны в немедленных и отложенных контекстах (так же, как и обновления типичных ресурсов) и после выполнения влияют на последующие обращения к плиткам (но не ранее отправленные операции).</span><span class="sxs-lookup"><span data-stu-id="f3508-112">Tile controls are available on immediate or deferred contexts (just like updates to typical resources) and upon execution impact subsequent accesses to the tiles (not previously submitted operations).</span></span>

## <a name="related-topics"></a><span data-ttu-id="f3508-113">См. также</span><span class="sxs-lookup"><span data-stu-id="f3508-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f3508-114">Создание мозаичных ресурсов</span><span class="sxs-lookup"><span data-stu-id="f3508-114">Creating tiled resources</span></span>](creating-tiled-resources.md)
</dt> </dl>

 

 




