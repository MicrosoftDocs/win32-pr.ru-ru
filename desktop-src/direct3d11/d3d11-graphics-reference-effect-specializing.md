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
# <a name="specializing-interfaces-direct3d-11"></a><span data-ttu-id="d6013-103">Специализирующиеся интерфейсы (Direct3D 11)</span><span class="sxs-lookup"><span data-stu-id="d6013-103">Specializing Interfaces (Direct3D 11)</span></span>

<span data-ttu-id="d6013-104">[**ID3DX11EffectVariable**](id3dx11effectvariable.md) имеет ряд методов для приведения интерфейса к нужному типу интерфейса.</span><span class="sxs-lookup"><span data-stu-id="d6013-104">[**ID3DX11EffectVariable**](id3dx11effectvariable.md) has a number of methods for casting the interface into the particular type of interface you need.</span></span> <span data-ttu-id="d6013-105">Методы имеют форму *астипе* и включают метод для каждого типа переменной Effect (например, Асбленд, асконстантбуффер и т. д.).</span><span class="sxs-lookup"><span data-stu-id="d6013-105">The methods are of the form *AsType* and include a method for each type of effect variable (such as AsBlend, AsConstantBuffer etc..)</span></span>

<span data-ttu-id="d6013-106">Например, предположим, что имеется воздействие на две глобальные переменные: время и универсальное преобразование.</span><span class="sxs-lookup"><span data-stu-id="d6013-106">For example, suppose you have an effect with two global variables: time and a world transform.</span></span>


```
float    g_fTime;
float4x4 g_mWorld;
```



<span data-ttu-id="d6013-107">Ниже приведен пример, в котором эти переменные получаются:</span><span class="sxs-lookup"><span data-stu-id="d6013-107">Here is an example that gets these variables:</span></span>


```
ID3DX11EffectVariable* g_pVariable;
ID3DX11EffectMatrixVariable* g_pmWorld;
ID3DX11EffectScalarVariable* g_pfTime;

g_pVariable = g_pEffect11->GetVariableByName("g_mWorld");
g_pmWorld = g_pVariable->AsMatrix();
g_pVariable = g_pEffect11->GetVariableByName("g_fTime");
g_pfTime = g_pVariable->AsScalar();
```



<span data-ttu-id="d6013-108">Путем специализации интерфейсов можно сократить код до одного вызова.</span><span class="sxs-lookup"><span data-stu-id="d6013-108">By specializing the interfaces, you could reduce the code to a single call.</span></span>


```
g_pmWorld = (g_pEffect11->GetVariableByName("g_mWorld"))->AsMatrix();
g_pfTime = (g_pEffect11->GetVariableByName("g_fTime"))->AsScalar();
```



<span data-ttu-id="d6013-109">Интерфейсы, которые наследуют от [**ID3DX11EffectVariable**](id3dx11effectvariable.md) , также имеют эти методы, но они были разработаны для возврата недопустимых объектов. только вызовы из **ID3DX11EffectVariable** возвращают допустимые объекты.</span><span class="sxs-lookup"><span data-stu-id="d6013-109">Interfaces that inherit from [**ID3DX11EffectVariable**](id3dx11effectvariable.md) also have these methods, but they have been designed to return invalid objects; only calls from **ID3DX11EffectVariable** return valid objects.</span></span> <span data-ttu-id="d6013-110">Приложения могут проверить возвращаемый объект, чтобы проверить, является ли он допустимым, вызвав [**ID3DX11EffectVariable:: IsValid**](id3dx11effectvariable-isvalid.md).</span><span class="sxs-lookup"><span data-stu-id="d6013-110">Applications can test the returned object to see if it is valid by calling [**ID3DX11EffectVariable::IsValid**](id3dx11effectvariable-isvalid.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="d6013-111">См. также</span><span class="sxs-lookup"><span data-stu-id="d6013-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d6013-112">Эффекты (Direct3D 11)</span><span class="sxs-lookup"><span data-stu-id="d6013-112">Effects (Direct3D 11)</span></span>](d3d11-graphics-programming-guide-effects.md)
</dt> </dl>

 

 




