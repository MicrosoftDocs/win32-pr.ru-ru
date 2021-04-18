---
description: Альфа-смешение используется для вывода изображения с прозрачными или полупрозрачными пикселами.
ms.assetid: 553b0bc8-1bd8-4282-9260-cdc5f2b8788d
title: Альфа-смешение (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4f4ae2883c7a9a92ba1b62306dc26bf09d0d9947
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104142136"
---
# <a name="alpha-blending-direct3d-9"></a><span data-ttu-id="fed86-103">Альфа-смешение (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="fed86-103">Alpha Blending (Direct3D 9)</span></span>

<span data-ttu-id="fed86-104">Альфа-смешение используется для вывода изображения с прозрачными или полупрозрачными пикселами.</span><span class="sxs-lookup"><span data-stu-id="fed86-104">Alpha blending is used to display an image that has transparent or semi-transparent pixels.</span></span> <span data-ttu-id="fed86-105">В дополнение к красному, зеленому и синему каналу цвета каждый пиксель в альфа-изображении имеет компонент прозрачности, известный как альфа-канал.</span><span class="sxs-lookup"><span data-stu-id="fed86-105">In addition to a red, green, and blue color channel, each pixel in an alpha bitmap has a transparency component known as its alpha channel.</span></span> <span data-ttu-id="fed86-106">Альфа-канал обычно содержит столько битов, сколько цветовой канал.</span><span class="sxs-lookup"><span data-stu-id="fed86-106">The alpha channel typically contains as many bits as a color channel.</span></span> <span data-ttu-id="fed86-107">Например, 8-разрядный канал альфа может представлять 256 уровней прозрачности, от 0 (весь пиксель прозрачен) до 255 (весь пиксель является непрозрачным).</span><span class="sxs-lookup"><span data-stu-id="fed86-107">For example, an 8-bit alpha channel can represent 256 levels of transparency, from 0 (the entire pixel is transparent) to 255 (the entire pixel is opaque).</span></span> <span data-ttu-id="fed86-108">В приведенном ниже списке показаны некоторые специальные эффекты, которые можно создать с помощью альфа-смешения.</span><span class="sxs-lookup"><span data-stu-id="fed86-108">The list below shows some special effects you can create using alpha blending.</span></span>

<span data-ttu-id="fed86-109">Цвет можно определить с помощью или без альфа-значений.</span><span class="sxs-lookup"><span data-stu-id="fed86-109">Color can be defined with or without alpha values.</span></span> <span data-ttu-id="fed86-110">Цвет без альфа — цвет RGB с альфа-каналом хранится в виде ARGB.</span><span class="sxs-lookup"><span data-stu-id="fed86-110">Color without alpha is RGB color with alpha is stored as ARGB.</span></span> <span data-ttu-id="fed86-111">Данные вершин, данные о материальных и текстурных данных можно использовать для предоставления прозрачности объекта.</span><span class="sxs-lookup"><span data-stu-id="fed86-111">Vertex data, material data and texture data can be used to give object's transparency.</span></span> <span data-ttu-id="fed86-112">Буфер кадров также можно использовать для создания эффектов прозрачности.</span><span class="sxs-lookup"><span data-stu-id="fed86-112">The frame buffer can also be used to generate transparency effects.</span></span>

-   [<span data-ttu-id="fed86-113">Вершинная альфа-версия (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="fed86-113">Vertex Alpha (Direct3D 9)</span></span>](vertex-alpha.md)
-   [<span data-ttu-id="fed86-114">Материал альфа (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="fed86-114">Material Alpha (Direct3D 9)</span></span>](material-alpha.md)
-   [<span data-ttu-id="fed86-115">Текстура Alpha (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="fed86-115">Texture Alpha (Direct3D 9)</span></span>](texture-alpha.md)
-   [<span data-ttu-id="fed86-116">Буфер кадров Alpha (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="fed86-116">Frame Buffer Alpha (Direct3D 9)</span></span>](frame-buffer-alpha.md)
-   [<span data-ttu-id="fed86-117">Целевой альфа-канал прорисовки (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="fed86-117">Render Target Alpha (Direct3D 9)</span></span>](render-target-alpha.md)

<span data-ttu-id="fed86-118">Примеры, демонстрирующие альфа, включают:</span><span class="sxs-lookup"><span data-stu-id="fed86-118">Samples that demonstrate alpha include:</span></span>

-   [<span data-ttu-id="fed86-119">Объявление (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="fed86-119">Billboarding (Direct3D 9)</span></span>](billboarding.md)
-   [<span data-ttu-id="fed86-120">Облака, состояния и Вапор (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="fed86-120">Clouds, Smoke, and Vapor Trails (Direct3D 9)</span></span>](clouds--smoke--and-vapor-trails.md)
-   [<span data-ttu-id="fed86-121">Пожар, Фларес и взрывные развертывания (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="fed86-121">Fire, Flares, and Explosions (Direct3D 9)</span></span>](fire--flares--and-explosions.md)

## <a name="related-topics"></a><span data-ttu-id="fed86-122">См. также</span><span class="sxs-lookup"><span data-stu-id="fed86-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fed86-123">Визуализация Direct3D</span><span class="sxs-lookup"><span data-stu-id="fed86-123">Direct3D Rendering</span></span>](direct3d-rendering.md)
</dt> </dl>

 

 



