---
title: Специализирующиеся интерфейсы (Direct3D 11)
description: ID3DX11EffectVariable имеет ряд методов для приведения интерфейса к нужному типу интерфейса.
ms.assetid: 20892af0-7d4a-4a89-b8d7-4ef225400697
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d6e4cff9c74f7a4b4034578b7ddeec2c388f0f953534393ac27778c31ed3856c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119126078"
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

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Эффекты (Direct3D 11)](d3d11-graphics-programming-guide-effects.md)
</dt> </dl>

 

 




