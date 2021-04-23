---
description: Определяет базовый цвет материала, который можно применить к полной сетке или к отдельным граням сетки. Сила — это отражающий показатель материала.
ms.assetid: vs|directx_sdk|~\material.htm
title: Материал
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 54c13d201152350a8a61950bb609f73cbdb2a3aa
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104494280"
---
# <a name="material"></a><span data-ttu-id="e3719-104">Материал</span><span class="sxs-lookup"><span data-stu-id="e3719-104">Material</span></span>

<span data-ttu-id="e3719-105">Определяет базовый цвет материала, который можно применить к полной сетке или к отдельным граням сетки.</span><span class="sxs-lookup"><span data-stu-id="e3719-105">Defines a basic material color that can be applied to either a complete mesh or a mesh's individual faces.</span></span> <span data-ttu-id="e3719-106">Сила — это отражающий показатель материала.</span><span class="sxs-lookup"><span data-stu-id="e3719-106">The power is the specular exponent of the material.</span></span>

``` syntax
template Material
{
    < 3D82AB4D-62DA-11CF-AB39-0020AF71E433 >
    ColorRGBA faceColor;
    FLOAT power;
    ColorRGB specularColor;
    ColorRGB emissiveColor;
    [...]
} 
```

<span data-ttu-id="e3719-107">Где:</span><span class="sxs-lookup"><span data-stu-id="e3719-107">Where:</span></span>

-   <span data-ttu-id="e3719-108">цвет Фацеколор-Face.</span><span class="sxs-lookup"><span data-stu-id="e3719-108">faceColor - Face color.</span></span> <span data-ttu-id="e3719-109">Шаблон Колорргба.</span><span class="sxs-lookup"><span data-stu-id="e3719-109">A ColorRGBA template.</span></span> <span data-ttu-id="e3719-110">См. [**колорргба**](colorrgba.md).</span><span class="sxs-lookup"><span data-stu-id="e3719-110">See [**ColorRGBA**](colorrgba.md).</span></span>
-   <span data-ttu-id="e3719-111">экспонента отраженного цвета материала для Power Material.</span><span class="sxs-lookup"><span data-stu-id="e3719-111">power - Material specular color exponent.</span></span>
-   <span data-ttu-id="e3719-112">отражающий цвет Спекуларколор-Material.</span><span class="sxs-lookup"><span data-stu-id="e3719-112">specularColor - Material specular color.</span></span> <span data-ttu-id="e3719-113">Шаблон Колорргб.</span><span class="sxs-lookup"><span data-stu-id="e3719-113">A ColorRGB template.</span></span> <span data-ttu-id="e3719-114">См. [**колорргб**](colorrgb.md).</span><span class="sxs-lookup"><span data-stu-id="e3719-114">See [**ColorRGB**](colorrgb.md).</span></span>
-   <span data-ttu-id="e3719-115">цвет Емиссивеколор-Material эмиссионный.</span><span class="sxs-lookup"><span data-stu-id="e3719-115">emissiveColor - Material emissive color.</span></span> <span data-ttu-id="e3719-116">Шаблон Колорргб.</span><span class="sxs-lookup"><span data-stu-id="e3719-116">A ColorRGB template.</span></span> <span data-ttu-id="e3719-117">См. [**колорргб**](colorrgb.md).</span><span class="sxs-lookup"><span data-stu-id="e3719-117">See [**ColorRGB**](colorrgb.md).</span></span>

> [!Note]  
> <span data-ttu-id="e3719-118">Для окружающего цвета требуется альфа-компонент.</span><span class="sxs-lookup"><span data-stu-id="e3719-118">The ambient color requires an alpha component.</span></span>

 

<span data-ttu-id="e3719-119">[**Текстурефиленаме**](texturefilename.md) — это необязательный объект данных.</span><span class="sxs-lookup"><span data-stu-id="e3719-119">[**TextureFilename**](texturefilename.md) is an optional data object.</span></span> <span data-ttu-id="e3719-120">Если этот объект отсутствует, поверхность не текстурна.</span><span class="sxs-lookup"><span data-stu-id="e3719-120">If this object is not present, the face is untextured.</span></span>

## <a name="see-also"></a><span data-ttu-id="e3719-121">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e3719-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e3719-122">Шаблоны</span><span class="sxs-lookup"><span data-stu-id="e3719-122">Templates</span></span>](dx9-graphics-reference-x-file-format-templates.md)
</dt> </dl>

 

 



