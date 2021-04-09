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
ms.openlocfilehash: b4204e04332876db9145baba9888dbb2d339eff9
ms.sourcegitcommit: c2a1c4314550ea9bd202d28adfcc7bfe6180932f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2020
ms.locfileid: "104069714"
---
# <a name="d1112-device-must-be-dx11"></a>D1112: устройство должно быть DX11

Устройство, связанное с поверхностью DXGI, должно быть устройством D3D11.



|             |         |
|-------------|---------|
| Уровень ошибки | Предупреждение |



 

## <a name="possible-causes"></a>Возможные причины

Предпринята попытка использовать [**креатедксгисурфацерендертаржет**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createdxgisurfacerendertarget(idxgisurface_constd2d1_render_target_properties__id2d1rendertarget)) с ПОВЕРХНОСТЬю DXGI, созданной устройством, не являющимся Direct3D11.

 

 




