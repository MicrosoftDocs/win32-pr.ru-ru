---
description: Эти параметры указывают типы ресурсов запросов.
ms.assetid: d2030002-bd44-443f-8235-978919ebbda6
title: D3DUSAGE_QUERY
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0eac450ed722da26fe4885d41707483adf401f89
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/26/2021
ms.locfileid: "107994111"
---
# <a name="d3dusage_query"></a><span data-ttu-id="0481a-103">\_Запрос D3DUSAGE</span><span class="sxs-lookup"><span data-stu-id="0481a-103">D3DUSAGE\_QUERY</span></span>

<span data-ttu-id="0481a-104">Эти параметры указывают типы ресурсов запросов.</span><span class="sxs-lookup"><span data-stu-id="0481a-104">These options identify query resource types.</span></span>



| <span data-ttu-id="0481a-105">\#определенно</span><span class="sxs-lookup"><span data-stu-id="0481a-105">\#define</span></span>                                   | <span data-ttu-id="0481a-106">Описание</span><span class="sxs-lookup"><span data-stu-id="0481a-106">Description</span></span>                                                                                                                                                                                                                                                                                                                                         |
|--------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0481a-107">\_Фильтр запроса \_ D3DUSAGE</span><span class="sxs-lookup"><span data-stu-id="0481a-107">D3DUSAGE\_QUERY\_FILTER</span></span>                    | <span data-ttu-id="0481a-108">Запросите формат ресурса, чтобы узнать, поддерживает ли он типы фильтров текстур, отличных от D3DTEXF \_ Point (который всегда поддерживается).</span><span class="sxs-lookup"><span data-stu-id="0481a-108">Query the resource format to see if it supports texture filter types other than D3DTEXF\_POINT (which is always supported).</span></span>                                                                                                                                                                                                                         |
| <span data-ttu-id="0481a-109">D3DUSAGE \_ запрос \_ легацибумпмап</span><span class="sxs-lookup"><span data-stu-id="0481a-109">D3DUSAGE\_QUERY\_LEGACYBUMPMAP</span></span>             | <span data-ttu-id="0481a-110">Запрос ресурса об устаревшей карте выпуклости.</span><span class="sxs-lookup"><span data-stu-id="0481a-110">Query the resource about a legacy bump map.</span></span>                                                                                                                                                                                                                                                                                                         |
| <span data-ttu-id="0481a-111">D3DUSAGE \_ запрос \_ постпикселшадер \_ Blend</span><span class="sxs-lookup"><span data-stu-id="0481a-111">D3DUSAGE\_QUERY\_POSTPIXELSHADER\_BLENDING</span></span> | <span data-ttu-id="0481a-112">Выполните запрос к ресурсу, чтобы проверить поддержку поддержки смешения построителей текстуры.</span><span class="sxs-lookup"><span data-stu-id="0481a-112">Query the resource to verify support for post pixel shader blending support.</span></span> <span data-ttu-id="0481a-113">Если [**чеккдевицеформат**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdeviceformat) завершается с D3DUSAGE \_ запроса \_ постпикселшадер \_ Blend, то операции смешения пикселей не поддерживаются.</span><span class="sxs-lookup"><span data-stu-id="0481a-113">If [**CheckDeviceFormat**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdeviceformat) fails with D3DUSAGE\_QUERY\_POSTPIXELSHADER\_BLENDING, post pixel blending operations are not supported.</span></span> <span data-ttu-id="0481a-114">К ним относятся тестирование альфа-канала, пиксельный туман, наложение целевого объекта визуализации, включение цветовой записи и Дизеринг.</span><span class="sxs-lookup"><span data-stu-id="0481a-114">These include alpha test, pixel fog, render-target blending, color write enable, and dithering.</span></span> |
| <span data-ttu-id="0481a-115">D3DUSAGE \_ запрос \_ сргбреад</span><span class="sxs-lookup"><span data-stu-id="0481a-115">D3DUSAGE\_QUERY\_SRGBREAD</span></span>                  | <span data-ttu-id="0481a-116">Запросите ресурс, чтобы проверить, поддерживает ли текстура гамма-коррекцию во время операции чтения.</span><span class="sxs-lookup"><span data-stu-id="0481a-116">Query the resource to verify if a texture supports gamma correction during a read operation.</span></span>                                                                                                                                                                                                                                                        |
| <span data-ttu-id="0481a-117">D3DUSAGE \_ запрос \_ сргбврите</span><span class="sxs-lookup"><span data-stu-id="0481a-117">D3DUSAGE\_QUERY\_SRGBWRITE</span></span>                 | <span data-ttu-id="0481a-118">Запросите ресурс, чтобы проверить, поддерживает ли текстура гамма-коррекцию во время операции записи.</span><span class="sxs-lookup"><span data-stu-id="0481a-118">Query the resource to verify if a texture supports gamma correction during a write operation.</span></span>                                                                                                                                                                                                                                                       |
| <span data-ttu-id="0481a-119">D3DUSAGE \_ запрос \_ вертекстекстуре</span><span class="sxs-lookup"><span data-stu-id="0481a-119">D3DUSAGE\_QUERY\_VERTEXTEXTURE</span></span>             | <span data-ttu-id="0481a-120">Запросите ресурс, чтобы проверить поддержку выборки текстур шейдера вершин.</span><span class="sxs-lookup"><span data-stu-id="0481a-120">Query the resource to verify support for vertex shader texture sampling.</span></span>                                                                                                                                                                                                                                                                            |
| <span data-ttu-id="0481a-121">D3DUSAGE \_ запрос \_ врапандмип</span><span class="sxs-lookup"><span data-stu-id="0481a-121">D3DUSAGE\_QUERY\_WRAPANDMIP</span></span>                | <span data-ttu-id="0481a-122">Запросите ресурс, чтобы проверить поддержку переноса текстур и MIP-сопоставлений.</span><span class="sxs-lookup"><span data-stu-id="0481a-122">Query the resource to verify support for texture wrapping and mip-mapping.</span></span>                                                                                                                                                                                                                                                                          |



 

<span data-ttu-id="0481a-123">Используйте [**чеккдевицеформат**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdeviceformat) , чтобы запросить поддержку оборудования для этих использований, а некоторые другие сведения об использовании перечислены в [D3DUSAGE](d3dusage.md).</span><span class="sxs-lookup"><span data-stu-id="0481a-123">Use [**CheckDeviceFormat**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdeviceformat) to query hardware support for these usages, and some other usages listed in [D3DUSAGE](d3dusage.md).</span></span>

## <a name="constant-information"></a><span data-ttu-id="0481a-124">Сведения о константе</span><span class="sxs-lookup"><span data-stu-id="0481a-124">Constant Information</span></span>



|                          |             |
|--------------------------|-------------|
| <span data-ttu-id="0481a-125">Header</span><span class="sxs-lookup"><span data-stu-id="0481a-125">Header</span></span>                   | <span data-ttu-id="0481a-126">d3d9types. h</span><span class="sxs-lookup"><span data-stu-id="0481a-126">d3d9types.h</span></span> |
| <span data-ttu-id="0481a-127">Минимальная операционная система</span><span class="sxs-lookup"><span data-stu-id="0481a-127">Minimum operating system</span></span> | <span data-ttu-id="0481a-128">Windows 98</span><span class="sxs-lookup"><span data-stu-id="0481a-128">Windows 98</span></span>  |



 

## <a name="related-topics"></a><span data-ttu-id="0481a-129">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="0481a-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0481a-130">Константы Direct3D</span><span class="sxs-lookup"><span data-stu-id="0481a-130">Direct3D Constants</span></span>](dx9-graphics-reference-d3d-constants.md)
</dt> </dl>

 

 
