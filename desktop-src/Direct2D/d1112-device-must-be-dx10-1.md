---
title: Устройство D1112 должно быть DX11
ms.assetid: 39dcccaf-db56-402d-b62f-704ad4daf151
description: Устройство, связанное с поверхностью DXGI, должно быть устройством D3D11.
keywords:
- Устройство D1112 должно быть DX11 Direct2D
topic_type:
- apiref
api_name:
- D1112 Device Must Be DX11
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.custom: seodec18
ms.openlocfilehash: 68408c56710589def033c34d20d9bac81e8d4947
ms.sourcegitcommit: f848119a8faa29b27585f4df53f6e50ee9666684
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/27/2021
ms.locfileid: "110549889"
---
# <a name="d1112-device-must-be-dx11"></a><span data-ttu-id="ba0ed-104">D1112: устройство должно быть DX11</span><span class="sxs-lookup"><span data-stu-id="ba0ed-104">D1112: Device Must Be DX11</span></span>

<span data-ttu-id="ba0ed-105">Устройство, связанное с поверхностью DXGI, должно быть устройством D3D11.</span><span class="sxs-lookup"><span data-stu-id="ba0ed-105">The device associated with the DXGI surface must be a D3D11 device.</span></span>



| &nbsp;      |  &nbsp; |
|-------------|---------|
| <span data-ttu-id="ba0ed-106">Уровень ошибки</span><span class="sxs-lookup"><span data-stu-id="ba0ed-106">Error Level</span></span> | <span data-ttu-id="ba0ed-107">Предупреждение</span><span class="sxs-lookup"><span data-stu-id="ba0ed-107">Warning</span></span> |



 

## <a name="possible-causes"></a><span data-ttu-id="ba0ed-108">Возможные причины</span><span class="sxs-lookup"><span data-stu-id="ba0ed-108">Possible Causes</span></span>

<span data-ttu-id="ba0ed-109">Предпринята попытка использовать [**креатедксгисурфацерендертаржет**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createdxgisurfacerendertarget(idxgisurface_constd2d1_render_target_properties__id2d1rendertarget)) с ПОВЕРХНОСТЬю DXGI, созданной устройством, не являющимся Direct3D11.</span><span class="sxs-lookup"><span data-stu-id="ba0ed-109">There was an attempt to use the [**CreateDxgiSurfaceRenderTarget**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createdxgisurfacerendertarget(idxgisurface_constd2d1_render_target_properties__id2d1rendertarget)) with a DXGI surface created by a non-Direct3D11 device.</span></span>

 

 




