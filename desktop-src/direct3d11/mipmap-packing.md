---
title: Упаковка MIP-карт
description: В зависимости от уровня поддержки мозаичных ресурсов MIP-карты с определенными измерениями не соответствуют стандартным фигурам мозаики, и все они обрабатываются вместе друг с другом так, как непрозрачно для приложения.
ms.assetid: 3B416324-7656-495F-9BA9-8F5BE475ABC1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0db4cd6f70129f46495673dfc82b5d261210ab21
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104067684"
---
# <a name="mipmap-packing"></a><span data-ttu-id="0451c-103">Упаковка MIP-карт</span><span class="sxs-lookup"><span data-stu-id="0451c-103">Mipmap packing</span></span>

<span data-ttu-id="0451c-104">В зависимости от [уровня](tiled-resources-features-tiers.md) поддержки мозаичных ресурсов MIP-карты с определенными измерениями не соответствуют стандартным фигурам мозаики, и все они обрабатываются вместе друг с другом так, как непрозрачно для приложения.</span><span class="sxs-lookup"><span data-stu-id="0451c-104">Depending on the [tier](tiled-resources-features-tiers.md) of tiled resources support, mipmaps with certain dimensions don't follow the standard tile shapes and are considered to all be packed together with one another in a manner that is opaque to the application.</span></span> <span data-ttu-id="0451c-105">Высокие уровни поддержки имеют более широкие гарантии в отношении того, какие типы размеров поверхностей помещаются в стандартные формы плиток (и, соответственно, могут по отдельности сопоставляться приложениями).</span><span class="sxs-lookup"><span data-stu-id="0451c-105">Higher tiers of support have broader guarantees about what types of surface dimensions fit in the standard tile shapes (and can therefore be individually mapped by applications).</span></span>

<span data-ttu-id="0451c-106">Различия между реализациями зависят от того, что при наличии измерений мозаичного ресурса, формата, числа MIP-карты и срезов массива — некоторые числа M из MIPS (для каждого среза массива) можно упаковывать в несколько плиток числа N.</span><span class="sxs-lookup"><span data-stu-id="0451c-106">What can vary between implementations is that—given a tiled resource's dimensions, format, number of mipmaps, and array slices—some number M of mips (per array slice) can be packed into some number N tiles.</span></span> <span data-ttu-id="0451c-107">API-интерфейс [**ID3D11Device2:: жетресаурцетилинг**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11device2-getresourcetiling) существует, чтобы разрешить драйверу сообщать приложению о том, какие M и N (помимо других сведений о том, что эти отчеты API являются стандартными и не зависят от поставщика оборудования).</span><span class="sxs-lookup"><span data-stu-id="0451c-107">The [**ID3D11Device2::GetResourceTiling**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11device2-getresourcetiling) API exists to allow the driver to report to the application what M and N are (among other details about the surface that this API reports that are standard and don't vary by hardware vendor).</span></span> <span data-ttu-id="0451c-108">Набор плиток для упакованных MIP-карт по-прежнему занимает 64 КБ и может быть отдельно сопоставлен в различных местах в пуле плиток.</span><span class="sxs-lookup"><span data-stu-id="0451c-108">The set of tiles for the packed mips are still 64KB and can be individually mapped into disparate locations in a tile pool.</span></span> <span data-ttu-id="0451c-109">Однако форма пикселей в плитках и то, как MIP-карты размещаются в рамках набора плитки, зависит от поставщика оборудования, и этот вопрос слишком сложен для рассмотрения здесь.</span><span class="sxs-lookup"><span data-stu-id="0451c-109">But the pixel shape of the tiles and how the mipmaps fit across the set of tiles is specific to a hardware vendor and too complex to expose.</span></span> <span data-ttu-id="0451c-110">Таким образом, в один момент времени приложения должны либо сопоставлять все плитки, обозначенные как упакованные, либо не сопоставлять их вообще.</span><span class="sxs-lookup"><span data-stu-id="0451c-110">So, applications are required to either map all of the tiles that are designated as packed, or none of them, at a time.</span></span> <span data-ttu-id="0451c-111">В противном случае поведение при доступе к мозаичному ресурсу не определено.</span><span class="sxs-lookup"><span data-stu-id="0451c-111">Otherwise, the behavior for accessing the tiled resource is undefined.</span></span>

<span data-ttu-id="0451c-112">Для поверхностей в массиве набор упакованных MIP-карт и количество упакованных плиток, в которых хранятся эти MIP-карты (M и N согласно описанию выше), применяется по отдельности для каждого фрагмента массива.</span><span class="sxs-lookup"><span data-stu-id="0451c-112">For arrayed surfaces, the set of packed mips and the number of packed tiles storing those mips (M and N described preceding) applies individually for each array slice.</span></span>

<span data-ttu-id="0451c-113">Выделенные API для копирования плиток ([**ID3D11DeviceContext2:: копитилес**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-copytiles) и [**ID3D11DeviceContext2:: упдатетилес**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-updatetiles)) не могут получить доступ к упакованному MIPS.</span><span class="sxs-lookup"><span data-stu-id="0451c-113">Dedicated APIs for copying tiles ([**ID3D11DeviceContext2::CopyTiles**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-copytiles) and [**ID3D11DeviceContext2::UpdateTiles**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-updatetiles)) can't access packed mips.</span></span> <span data-ttu-id="0451c-114">Приложения, которые хотят копировать данные в Упакованные MIPS и обратно, могут сделать это с помощью всех API-интерфейсов, отличных от мозаичного, для копирования и отрисовки на поверхностях.</span><span class="sxs-lookup"><span data-stu-id="0451c-114">Applications that want to copy data to and from packed mips can do so using all the non-tiled resource specific APIs for copying and rendering to surfaces.</span></span>

## <a name="related-topics"></a><span data-ttu-id="0451c-115">См. также</span><span class="sxs-lookup"><span data-stu-id="0451c-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0451c-116">Мозаичное заполнение области мозаичного ресурса</span><span class="sxs-lookup"><span data-stu-id="0451c-116">How a tiled resource's area is tiled</span></span>](how-a-tiled-resource-s-area-is-tiled.md)
</dt> </dl>

 

 




