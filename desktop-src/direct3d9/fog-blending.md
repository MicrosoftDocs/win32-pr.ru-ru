---
description: Смешение тумана означает применение коэффициента тумана к цветам тумана и объекта для создания окончательного цвета, отображаемого в сцене, как описано в формулах тумана (Direct3D 9).
ms.assetid: b5b43f12-bbed-4464-aebc-02ad6dab1951
title: Смешение тумана (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f60f3402daf71a3fce14af936334c3d96e928d3469452eafb94d139594bb0b19
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119894024"
---
# <a name="fog-blending-direct3d-9"></a>Смешение тумана (Direct3D 9)

Смешение тумана означает применение коэффициента тумана к цветам тумана и объекта для создания окончательного цвета, отображаемого в сцене, как описано в [формулах тумана (Direct3D 9)](fog-formulas.md). \_Состояние отрисовки D3DRS фоженабле управляет наложением тумана. Задайте для этого состояния отрисовки **значение true** , чтобы включить смешение тумана, как показано в следующем примере кода. Значение по умолчанию — **false**.


```
// For this example, g_pDevice is a valid pointer
// to an IDirect3DDevice9 interface.
HRESULT hr;
hr = g_pDevice->SetRenderState(
                    D3DRS_FOGENABLE,
                    TRUE);
if FAILED(hr)
    return hr;
```



Необходимо включить смешение тумана для пиксельного тумана и вершинного тумана. Сведения об использовании этих типов тумана см. в разделе [Pixel туман (Direct3D 9)](pixel-fog.md) и [вершинный туман (Direct3D 9)](vertex-fog.md).

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Типы туманов](fog-types.md)
</dt> </dl>

 

 



