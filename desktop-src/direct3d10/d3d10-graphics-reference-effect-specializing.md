---
description: Интерфейс ID3D10EffectVariable имеет ряд методов для приведения интерфейса к нужному типу интерфейса.
ms.assetid: c0842a1d-b78c-44b2-89c7-452d54efe403
title: Специализирующиеся интерфейсы (Direct3D 10)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9e75c77d6d726c745ac553c6d69dc6ce29a69cc37e52c28581b6f28ade8339dd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118809274"
---
# <a name="specializing-interfaces-direct3d-10"></a>Специализирующиеся интерфейсы (Direct3D 10)

[**Интерфейс ID3D10EffectVariable**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectvariable) имеет ряд методов для приведения интерфейса к нужному типу интерфейса. Методы имеют форму *типа* и включают метод для каждого типа переменной Effect (например, Асбленд, асконстантбуффер и т. д.).

Например, предположим, что имеется воздействие на две глобальные переменные: время и универсальное преобразование.


```
float    g_fTime;
float4x4 g_mWorld;
```



Ниже приведен пример (из [примера SimpleSample10](https://msdn.microsoft.com/library/Ee416428(v=VS.85).aspx)), который получает эти переменные:


```
ID3D10EffectVariable* g_pVariable;
ID3D10EffectMatrixVariable* g_pmWorld;
ID3D10EffectScalarVariable* g_pfTime;

g_pVariable = g_pEffect10->GetVariableByName("g_mWorld");
g_pmWorld = g_pVariable->AsMatrix();
g_pfTime = g_pEffect10->GetVariableByName("g_fTime");
g_pfTime = g_pVariable->AsScalar();
```



Путем специализации интерфейсов можно сократить код до одного вызова.


```
g_pmWorld = (g_pEffect10->GetVariableByName("g_mWorld"))->AsMatrix();
g_pfTime = (g_pEffect10->GetVariableByName("g_fTime"))->AsScalar();
```



Интерфейсы, которые наследуют от [**интерфейса ID3D10EffectVariable**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectvariable) , также имеют эти методы, но они были разработаны для возврата недопустимых объектов. только вызовы из **интерфейса ID3D10EffectVariable** возвращают допустимые объекты. Приложения могут проверить возвращаемый объект, чтобы проверить, является ли он допустимым, вызвав [**ID3D10EffectVariable:: IsValid**](/windows/desktop/api/D3D10Effect/nf-d3d10effect-id3d10effectvariable-isvalid).

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Эффекты](d3d10-graphics-programming-guide-effects.md)
</dt> </dl>

 

 



