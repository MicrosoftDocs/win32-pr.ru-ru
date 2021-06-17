---
description: Дополнительные сведения о альфа-смешении. Альфа-смешение используется для вывода изображения с прозрачными или полупрозрачными пикселами.
ms.assetid: 553b0bc8-1bd8-4282-9260-cdc5f2b8788d
title: Альфа-смешение (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cd79c622778e17c5acb9b17d52b6d5db278b1508
ms.sourcegitcommit: d0eb44d0a95f5e5efbfec3d3e9c143f5cba25bc3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/17/2021
ms.locfileid: "112262006"
---
# <a name="alpha-blending-direct3d-9"></a><span data-ttu-id="433d7-104">Альфа-смешение (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="433d7-104">Alpha Blending (Direct3D 9)</span></span>

<span data-ttu-id="433d7-105">Альфа-смешение используется для вывода изображения с прозрачными или полупрозрачными пикселами.</span><span class="sxs-lookup"><span data-stu-id="433d7-105">Alpha blending is used to display an image that has transparent or semi-transparent pixels.</span></span> <span data-ttu-id="433d7-106">В дополнение к красному, зеленому и синему каналу цвета каждый пиксель в альфа-изображении имеет компонент прозрачности, известный как альфа-канал.</span><span class="sxs-lookup"><span data-stu-id="433d7-106">In addition to a red, green, and blue color channel, each pixel in an alpha bitmap has a transparency component known as its alpha channel.</span></span> <span data-ttu-id="433d7-107">Альфа-канал обычно содержит столько битов, сколько цветовой канал.</span><span class="sxs-lookup"><span data-stu-id="433d7-107">The alpha channel typically contains as many bits as a color channel.</span></span> <span data-ttu-id="433d7-108">Например, 8-разрядный канал альфа может представлять 256 уровней прозрачности, от 0 (весь пиксель прозрачен) до 255 (весь пиксель является непрозрачным).</span><span class="sxs-lookup"><span data-stu-id="433d7-108">For example, an 8-bit alpha channel can represent 256 levels of transparency, from 0 (the entire pixel is transparent) to 255 (the entire pixel is opaque).</span></span> <span data-ttu-id="433d7-109">В приведенном ниже списке показаны некоторые специальные эффекты, которые можно создать с помощью альфа-смешения.</span><span class="sxs-lookup"><span data-stu-id="433d7-109">The list below shows some special effects you can create using alpha blending.</span></span>

<span data-ttu-id="433d7-110">Цвет можно определить с помощью или без альфа-значений.</span><span class="sxs-lookup"><span data-stu-id="433d7-110">Color can be defined with or without alpha values.</span></span> <span data-ttu-id="433d7-111">Цвет без альфа — цвет RGB с альфа-каналом хранится в виде ARGB.</span><span class="sxs-lookup"><span data-stu-id="433d7-111">Color without alpha is RGB color with alpha is stored as ARGB.</span></span> <span data-ttu-id="433d7-112">Данные вершин, данные о материальных и текстурных данных можно использовать для предоставления прозрачности объекта.</span><span class="sxs-lookup"><span data-stu-id="433d7-112">Vertex data, material data and texture data can be used to give object's transparency.</span></span> <span data-ttu-id="433d7-113">Буфер кадров также можно использовать для создания эффектов прозрачности.</span><span class="sxs-lookup"><span data-stu-id="433d7-113">The frame buffer can also be used to generate transparency effects.</span></span>

-   [<span data-ttu-id="433d7-114">Вершинная альфа-версия (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="433d7-114">Vertex Alpha (Direct3D 9)</span></span>](vertex-alpha.md)
-   [<span data-ttu-id="433d7-115">Материал альфа (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="433d7-115">Material Alpha (Direct3D 9)</span></span>](material-alpha.md)
-   [<span data-ttu-id="433d7-116">Текстура Alpha (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="433d7-116">Texture Alpha (Direct3D 9)</span></span>](texture-alpha.md)
-   [<span data-ttu-id="433d7-117">Буфер кадров Alpha (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="433d7-117">Frame Buffer Alpha (Direct3D 9)</span></span>](frame-buffer-alpha.md)
-   [<span data-ttu-id="433d7-118">Целевой альфа-канал прорисовки (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="433d7-118">Render Target Alpha (Direct3D 9)</span></span>](render-target-alpha.md)

<span data-ttu-id="433d7-119">Примеры, демонстрирующие альфа, включают:</span><span class="sxs-lookup"><span data-stu-id="433d7-119">Samples that demonstrate alpha include:</span></span>

-   [<span data-ttu-id="433d7-120">Объявление (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="433d7-120">Billboarding (Direct3D 9)</span></span>](billboarding.md)
-   [<span data-ttu-id="433d7-121">Облака, состояния и Вапор (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="433d7-121">Clouds, Smoke, and Vapor Trails (Direct3D 9)</span></span>](clouds--smoke--and-vapor-trails.md)
-   [<span data-ttu-id="433d7-122">Пожар, Фларес и взрывные развертывания (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="433d7-122">Fire, Flares, and Explosions (Direct3D 9)</span></span>](fire--flares--and-explosions.md)

## <a name="related-topics"></a><span data-ttu-id="433d7-123">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="433d7-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="433d7-124">Визуализация Direct3D</span><span class="sxs-lookup"><span data-stu-id="433d7-124">Direct3D Rendering</span></span>](direct3d-rendering.md)
</dt> </dl>

 

 



