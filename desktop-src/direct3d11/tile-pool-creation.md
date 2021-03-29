---
title: Создание пула плиток
description: Пул плиток создается через API ID3D11Device CreateBuffer, передавая \_ \_ \_ флаг пула плиток ресурсов D3D11 \_ в ЭЛЕМЕНТЕ мискфлагс в \_ структуре D3D11 buffer \_ , на которую указывает параметр пдеск.
ms.assetid: 751A64A6-C9B6-4797-BA1C-B3BEF655DF32
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1f3b66a9a548d27382f8cbb4e447516beea6eca8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104996734"
---
# <a name="tile-pool-creation"></a><span data-ttu-id="f31a3-103">Создание пула плиток</span><span class="sxs-lookup"><span data-stu-id="f31a3-103">Tile pool creation</span></span>

<span data-ttu-id="f31a3-104">Пул плиток создается с помощью API-интерфейса [**ID3D11Device:: CreateBuffer**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createbuffer) путем передачи флага [**\_ \_ \_ \_ пула плиток ресурсов D3D11**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_resource_misc_flag) в элементе **мискфлагс** в структуре [**D3D11 \_ buffer \_**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_buffer_desc) , на которую указывает параметр *пдеск* .</span><span class="sxs-lookup"><span data-stu-id="f31a3-104">A tile pool is created via the [**ID3D11Device::CreateBuffer**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createbuffer) API by passing the [**D3D11\_RESOURCE\_MISC\_TILE\_POOL**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_resource_misc_flag) flag in the **MiscFlags** member of the [**D3D11\_BUFFER\_DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_buffer_desc) structure that the *pDesc* parameter points to.</span></span>

<span data-ttu-id="f31a3-105">Приложения могут создавать один или несколько пулов плиток для каждого устройства Direct3D.</span><span class="sxs-lookup"><span data-stu-id="f31a3-105">Applications can create one or more tile pools per Direct3D device.</span></span> <span data-ttu-id="f31a3-106">Общий размер каждого пула плиток ограничен предельным размером ресурсов Direct3D 11, который равен примерно 1/4 ОЗУ графического процессора (GPU).</span><span class="sxs-lookup"><span data-stu-id="f31a3-106">The total size of each tile pool is restricted to Direct3D 11's resource size limit, which is roughly 1/4 of graphics processing unit (GPU) RAM.</span></span>

<span data-ttu-id="f31a3-107">Пул плиток состоит из плиток по 64 КБ, но операционная система (видеодрайвер) управляет всем пулом как одним или несколькими выделениями памяти незаметно — разбивка недоступна приложениям.</span><span class="sxs-lookup"><span data-stu-id="f31a3-107">A tile pool is made of 64KB tiles, but the operating system (display driver) manages the entire pool as one or more allocations behind the scenes—the breakdown is not visible to applications.</span></span> <span data-ttu-id="f31a3-108">Мозаичные ресурсы определяют содержимое, указывая плитки в пуле плиток.</span><span class="sxs-lookup"><span data-stu-id="f31a3-108">Tiled resources define content by pointing at tiles within a tile pool.</span></span> <span data-ttu-id="f31a3-109">Отменить сопоставление плитки из мозаичного ресурса можно, поместив плитку в **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="f31a3-109">Unmapping a tile from a tiled resource is done by pointing the tile to **NULL**.</span></span> <span data-ttu-id="f31a3-110">Такие несопоставленные плитки имеют правила поведения операций чтения или записи.</span><span class="sxs-lookup"><span data-stu-id="f31a3-110">Such unmapped tiles have rules about the behavior of reads or writes.</span></span> <span data-ttu-id="f31a3-111">Сведения см. в разделе [Отслеживание опасности и ресурсы пула плиток](hazard-tracking-versus-tile-pool-resources.md).</span><span class="sxs-lookup"><span data-stu-id="f31a3-111">For info, see [Hazard tracking versus tile pool resources](hazard-tracking-versus-tile-pool-resources.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="f31a3-112">См. также</span><span class="sxs-lookup"><span data-stu-id="f31a3-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f31a3-113">Сопоставления в пуле плиток</span><span class="sxs-lookup"><span data-stu-id="f31a3-113">Mappings are into a tile pool</span></span>](mappings-are-into-a-tile-pool.md)
</dt> </dl>

 

 




