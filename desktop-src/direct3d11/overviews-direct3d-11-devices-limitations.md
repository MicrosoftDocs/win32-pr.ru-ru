---
title: Ограничения на создание ИСКРИВЛЕНных и эталонных устройств
description: Существуют некоторые ограничения на создание ИСКРИВЛЕНных и ссылочных устройств в Direct3D 10,1 и Direct3D 11,0. В этом разделе обсуждаются эти ограничения.
ms.assetid: 7e022e5d-daa3-48fa-b9fe-4b569220e55e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e12540b1fdb8f2bc00ef2a0e596904e0b717bed1
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104337556"
---
# <a name="limitations-creating-warp-and-reference-devices"></a><span data-ttu-id="0fcd6-104">Ограничения на создание ИСКРИВЛЕНных и эталонных устройств</span><span class="sxs-lookup"><span data-stu-id="0fcd6-104">Limitations Creating WARP and Reference Devices</span></span>

<span data-ttu-id="0fcd6-105">Существуют некоторые ограничения на создание ИСКРИВЛЕНных и ссылочных устройств в Direct3D 10,1 и Direct3D 11,0.</span><span class="sxs-lookup"><span data-stu-id="0fcd6-105">Some limitations exist for creating WARP and Reference devices in Direct3D 10.1 and Direct3D 11.0.</span></span> <span data-ttu-id="0fcd6-106">В этом разделе обсуждаются эти ограничения.</span><span class="sxs-lookup"><span data-stu-id="0fcd6-106">This topic discusses those limitations.</span></span>

<span data-ttu-id="0fcd6-107">Типы драйверов типов драйвера D3D10 \_ \_ и драйвера D3D10 для типов драйверов \_ \_ \_ \_ не поддерживаются на \_ уровне компонентов D3D10 с \_ уровня \_ 9 \_ 1 до D3D10 компонентов уровня \_ \_ \_ \_ 4 3 в Direct3D 10,1.</span><span class="sxs-lookup"><span data-stu-id="0fcd6-107">The D3D10\_DRIVER\_TYPE\_WARP and D3D10\_DRIVER\_TYPE\_REFERENCE driver types are not supported on the D3D10\_FEATURE\_LEVEL\_9\_1 through D3D10\_FEATURE\_LEVEL\_9\_3 feature levels in Direct3D 10.1.</span></span> <span data-ttu-id="0fcd6-108">Кроме того, тип драйвера " \_ деформация" типа драйвера D3D \_ \_ не поддерживается на \_ уровне функции D3D \_ \_ 11 \_ 0 в Direct3D 11,0.</span><span class="sxs-lookup"><span data-stu-id="0fcd6-108">Additionally, the D3D\_DRIVER\_TYPE\_WARP driver type is not supported on D3D\_FEATURE\_LEVEL\_11\_0 in Direct3D 11.0.</span></span> <span data-ttu-id="0fcd6-109">Это значит, что при вызове [**D3D10CreateDevice1**](/windows/desktop/api/d3d10_1/nf-d3d10_1-d3d10createdevice1) для создания устройства Direct3D 10,1 или при вызове [**D3D11CreateDevice**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdevice) для создания устройства Direct3D 11,0, если указать сочетание одного из этих типов драйверов с одним из этих уровней функций в вызове, вызов будет недопустимым.</span><span class="sxs-lookup"><span data-stu-id="0fcd6-109">That is, when you call [**D3D10CreateDevice1**](/windows/desktop/api/d3d10_1/nf-d3d10_1-d3d10createdevice1) to create a Direct3D 10.1 device or when you call [**D3D11CreateDevice**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdevice) to create a Direct3D 11.0 device, if you specify a combination of one of these driver types with one of these feature levels in the call, the call is invalid.</span></span> <span data-ttu-id="0fcd6-110">Для деформации и ссылочных устройств допустимы только следующие сочетания уровней компонентов, сред выполнения и типов драйверов:</span><span class="sxs-lookup"><span data-stu-id="0fcd6-110">Only the following combinations of feature levels, runtimes, and driver types are valid for WARP and Reference devices:</span></span>

-   <span data-ttu-id="0fcd6-111">\_Тип драйвера \_ D3D \_ перекоса на всех уровнях компонентов в Direct3D 11,1, которые входят в состав Windows 8</span><span class="sxs-lookup"><span data-stu-id="0fcd6-111">D3D\_DRIVER\_TYPE\_WARP on all feature levels in Direct3D 11.1, which Windows 8 includes</span></span>

    <span data-ttu-id="0fcd6-112">\_ \_ Справочник по типам драйверов D3D \_ на всех уровнях компонентов в Direct3D 11,1</span><span class="sxs-lookup"><span data-stu-id="0fcd6-112">D3D\_DRIVER\_TYPE\_REFERENCE on all feature levels in Direct3D 11.1</span></span>

    <span data-ttu-id="0fcd6-113">При вызове [**D3D11CreateDevice**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdevice) для создания устройства Direct3D 11,1 вызов допустим, если указать сочетание одного из этих типов драйверов с одним из этих уровней.</span><span class="sxs-lookup"><span data-stu-id="0fcd6-113">When you call [**D3D11CreateDevice**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdevice) to create a Direct3D 11.1 device, the call is valid if you specify a combination of one of these driver types with one of these feature levels.</span></span>

-   <span data-ttu-id="0fcd6-114">\_Тип драйвера D3D. \_ \_ деформация на \_ уровне компонента D3D \_ \_ 9 \_ 1 через \_ уровни компонентов D3D \_ уровня \_ 10 \_ 1 в Direct3D 11</span><span class="sxs-lookup"><span data-stu-id="0fcd6-114">D3D\_DRIVER\_TYPE\_WARP on D3D\_FEATURE\_LEVEL\_9\_1 through D3D\_FEATURE\_LEVEL\_10\_1 feature levels in Direct3D 11</span></span>

    <span data-ttu-id="0fcd6-115">\_ \_ Справочник по типам драйверов D3D \_ на \_ уровне D3D-функции \_ \_ 9 с на \_ уровнях компонентов D3D \_ \_ уровня \_ 11 \_ 0 в Direct3D 11</span><span class="sxs-lookup"><span data-stu-id="0fcd6-115">D3D\_DRIVER\_TYPE\_REFERENCE on D3D\_FEATURE\_LEVEL\_9\_1 through D3D\_FEATURE\_LEVEL\_11\_0 feature levels in Direct3D 11</span></span>

    <span data-ttu-id="0fcd6-116">При вызове [**D3D11CreateDevice**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdevice) для создания устройства Direct3D 11 вызов допустим, если указать сочетание одного из этих типов драйверов с одним из этих уровней.</span><span class="sxs-lookup"><span data-stu-id="0fcd6-116">When you call [**D3D11CreateDevice**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdevice) to create a Direct3D 11 device, the call is valid if you specify a combination of one of these driver types with one of these feature levels.</span></span>

-   <span data-ttu-id="0fcd6-117">\_Тип драйвера D3D10. \_ \_ \_ \_ Справочник по типам драйверов D3D10 \_ для D3D10 \_ на \_ уровне \_ 10 \_ 0 до D3D10 уровня компонентов 10 \_ \_ \_ \_ 1 в Direct3D 10,1</span><span class="sxs-lookup"><span data-stu-id="0fcd6-117">D3D10\_DRIVER\_TYPE\_WARP and D3D10\_DRIVER\_TYPE\_REFERENCE on D3D10\_FEATURE\_LEVEL\_10\_0 through D3D10\_FEATURE\_LEVEL\_10\_1 feature levels in Direct3D 10.1</span></span>

    <span data-ttu-id="0fcd6-118">При вызове [**D3D10CreateDevice1**](/windows/desktop/api/d3d10_1/nf-d3d10_1-d3d10createdevice1) для создания устройства Direct3D 10,1 вызов допустим, если указать сочетание одного из этих типов драйверов с одним из этих уровней.</span><span class="sxs-lookup"><span data-stu-id="0fcd6-118">When you call [**D3D10CreateDevice1**](/windows/desktop/api/d3d10_1/nf-d3d10_1-d3d10createdevice1) to create a Direct3D 10.1 device, the call is valid if you specify a combination of one of these driver types with one of these feature levels.</span></span>

## <a name="related-topics"></a><span data-ttu-id="0fcd6-119">См. также</span><span class="sxs-lookup"><span data-stu-id="0fcd6-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0fcd6-120">Устройства</span><span class="sxs-lookup"><span data-stu-id="0fcd6-120">Devices</span></span>](overviews-direct3d-11-devices.md)
</dt> <dt>

[<span data-ttu-id="0fcd6-121">Введение в Direct3D 11 на оборудовании нижнего уровня</span><span class="sxs-lookup"><span data-stu-id="0fcd6-121">Introduction to Direct3D 11 on Downlevel Hardware</span></span>](overviews-direct3d-11-devices-downlevel-intro.md)
</dt> <dt>

[<span data-ttu-id="0fcd6-122">Как создать устройство деформации</span><span class="sxs-lookup"><span data-stu-id="0fcd6-122">How To: Create a WARP Device</span></span>](overviews-direct3d-11-devices-create-warp.md)
</dt> <dt>

[<span data-ttu-id="0fcd6-123">Как создать эталонное устройство</span><span class="sxs-lookup"><span data-stu-id="0fcd6-123">How To: Create a Reference Device</span></span>](overviews-direct3d-11-devices-create-ref.md)
</dt> <dt>

[<span data-ttu-id="0fcd6-124">**\_Тип драйвера \_ D3D10**</span><span class="sxs-lookup"><span data-stu-id="0fcd6-124">**D3D10\_DRIVER\_TYPE**</span></span>](/windows/desktop/api/d3d10misc/ne-d3d10misc-d3d10_driver_type)
</dt> <dt>

[<span data-ttu-id="0fcd6-125">**D3D10 \_ функция \_ level1**</span><span class="sxs-lookup"><span data-stu-id="0fcd6-125">**D3D10\_FEATURE\_LEVEL1**</span></span>](/windows/desktop/api/d3d10_1/ne-d3d10_1-d3d10_feature_level1)
</dt> <dt>

[<span data-ttu-id="0fcd6-126">**\_Тип драйвера \_ D3D**</span><span class="sxs-lookup"><span data-stu-id="0fcd6-126">**D3D\_DRIVER\_TYPE**</span></span>](/windows/desktop/api/D3DCommon/ne-d3dcommon-d3d_driver_type)
</dt> <dt>

[<span data-ttu-id="0fcd6-127">**\_Уровень компонента \_ D3D**</span><span class="sxs-lookup"><span data-stu-id="0fcd6-127">**D3D\_FEATURE\_LEVEL**</span></span>](/windows/desktop/api/D3DCommon/ne-d3dcommon-d3d_feature_level)
</dt> </dl>

 

 