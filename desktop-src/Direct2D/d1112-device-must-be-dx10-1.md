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
ms.openlocfilehash: 24c8bf123d9e00eff90f216676ec03f7d68cbe692511118c36c1433cbf0354d3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119758114"
---
# <a name="d1112-device-must-be-dx11"></a>D1112: устройство должно быть DX11

Устройство, связанное с поверхностью DXGI, должно быть устройством D3D11.



| &nbsp;      |  &nbsp; |
|-------------|---------|
| Уровень ошибки | Предупреждение |



 

## <a name="possible-causes"></a>Возможные причины

Предпринята попытка использовать [**креатедксгисурфацерендертаржет**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createdxgisurfacerendertarget(idxgisurface_constd2d1_render_target_properties__id2d1rendertarget)) с ПОВЕРХНОСТЬю DXGI, созданной устройством, не являющимся Direct3D11.

 

 




