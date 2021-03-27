---
title: Специализирующиеся интерфейсы (Direct3D 11)
description: ID3DX11EffectVariable имеет ряд методов для приведения интерфейса к нужному типу интерфейса.
ms.assetid: 20892af0-7d4a-4a89-b8d7-4ef225400697
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2cb9f8adb5a5bb184473ff5679df99f0b71557fa
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103777606"
---
# <a name="specializing-interfaces-direct3d-11"></a>Специализирующиеся интерфейсы (Direct3D 11)

[**ID3DX11EffectVariable**](id3dx11effectvariable.md) имеет ряд методов для приведения интерфейса к нужному типу интерфейса. Методы имеют форму *астипе* и включают метод для каждого типа переменной Effect (например, Асбленд, асконстантбуффер и т. д.).

Например, предположим, что имеется воздействие на две глобальные переменные: время и универсальное преобразование.


```
float    g_fTime;
float4x4 g_mWorld;
```



Ниже приведен пример, в котором эти переменные получаются:


```
ID3DX11EffectVariable* g_pVariable;
ID3DX11EffectMatrixVariable* g_pmWorld;
ID3DX11EffectScalarVariable* g_pfTime;

g_pVariable = g_pEffect11->GetVariableByName("g_mWorld");
g_pmWorld = g_pVariable->AsMatrix();
g_pVariable = g_pEffect11->GetVariableByName("g_fTime");
g_pfTime = g_pVariable->AsScalar();
```



Путем специализации интерфейсов можно сократить код до одного вызова.


```
g_pmWorld = (g_pEffect11->GetVariableByName("g_mWorld"))->AsMatrix();
g_pfTime = (g_pEffect11->GetVariableByName("g_fTime"))->AsScalar();
```



Интерфейсы, которые наследуют от [**ID3DX11EffectVariable**](id3dx11effectvariable.md) , также имеют эти методы, но они были разработаны для возврата недопустимых объектов. только вызовы из **ID3DX11EffectVariable** возвращают допустимые объекты. Приложения могут проверить возвращаемый объект, чтобы проверить, является ли он допустимым, вызвав [**ID3DX11EffectVariable:: IsValid**](id3dx11effectvariable-isvalid.md).

## <a name="related-topics"></a>См. также

<dl> <dt>

[Эффекты (Direct3D 11)](d3d11-graphics-programming-guide-effects.md)
</dt> </dl>

 

 




