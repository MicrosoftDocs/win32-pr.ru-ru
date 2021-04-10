---
description: Смешение тумана означает применение коэффициента тумана к цветам тумана и объекта для создания окончательного цвета, отображаемого в сцене, как описано в формулах тумана (Direct3D 9).
ms.assetid: b5b43f12-bbed-4464-aebc-02ad6dab1951
title: Смешение тумана (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fa918715a7bbe37b200568a0a9098135c5558b0d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104139219"
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

## <a name="related-topics"></a>См. также

<dl> <dt>

[Типы туманов](fog-types.md)
</dt> </dl>

 

 



