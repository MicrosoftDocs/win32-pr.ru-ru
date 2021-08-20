---
description: Значения ширины, высоты и глубины из структуры D3D12_DISPATCH_RAYS_DESC, указанной в исходном вызове Диспатчрайс.
ms.assetid: ''
title: DispatchRaysDimensions
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DispatchRaysDimensions
api_type:
- NA
ms.openlocfilehash: 4f68b7bdd5f5ea92074b366b9f981f490a9801079b29def17ba66770abd3c5f1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118989494"
---
# <a name="dispatchraysdimensions"></a>DispatchRaysDimensions

Значения ширины, высоты и глубины из структуры **\_ \_ \_ DESC D3D12 диспетчеризации** , указанной в исходном вызове [**диспатчрайс**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist4-dispatchrays) .

## <a name="syntax"></a>Синтаксис

```
uint3 DispatchRaysDimensions();
```

## <a name="remarks"></a>Remarks

Эту функцию можно вызывать из следующих типов шейдеров райтраЦинг:

* [**Шейдер любых попаданий**](any-hit-shader.md)
* [**Вызываемый шейдер**](callable-shader.md)
* [**Шейдер ближайшего попадания**](closest-hit-shader.md)
* [**Шейдер пересечения**](intersection-shader.md)
* [**Шейдер непопаданий**](miss-shader.md)
* [**Шейдер создания лучей**](ray-generation-shader.md)

## <a name="see-also"></a>См. также раздел

* [Справочник по HLSL для трассировки лучей в Direct3D 12](direct3d-12-raytracing-hlsl-reference.md)
