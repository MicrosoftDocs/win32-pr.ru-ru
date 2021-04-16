---
description: Интерфейс ID3D10EffectVariable имеет ряд методов для приведения интерфейса к нужному типу интерфейса.
ms.assetid: c0842a1d-b78c-44b2-89c7-452d54efe403
title: Специализирующиеся интерфейсы (Direct3D 10)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e0ce8bc29ae16ada650da7283beb1dd858948cae
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105650450"
---
# <a name="specializing-interfaces-direct3d-10"></a><span data-ttu-id="27d63-103">Специализирующиеся интерфейсы (Direct3D 10)</span><span class="sxs-lookup"><span data-stu-id="27d63-103">Specializing Interfaces (Direct3D 10)</span></span>

<span data-ttu-id="27d63-104">[**Интерфейс ID3D10EffectVariable**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectvariable) имеет ряд методов для приведения интерфейса к нужному типу интерфейса.</span><span class="sxs-lookup"><span data-stu-id="27d63-104">[**ID3D10EffectVariable Interface**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectvariable) has a number of methods for casting the interface into the particular type of interface you need.</span></span> <span data-ttu-id="27d63-105">Методы имеют форму *типа* и включают метод для каждого типа переменной Effect (например, Асбленд, асконстантбуффер и т. д.).</span><span class="sxs-lookup"><span data-stu-id="27d63-105">The methods are of the form As *Type* and include a method for each type of effect variable (such as AsBlend, AsConstantBuffer etc..)</span></span>

<span data-ttu-id="27d63-106">Например, предположим, что имеется воздействие на две глобальные переменные: время и универсальное преобразование.</span><span class="sxs-lookup"><span data-stu-id="27d63-106">For example, suppose you have an effect with two global variables: time and a world transform.</span></span>


```
float    g_fTime;
float4x4 g_mWorld;
```



<span data-ttu-id="27d63-107">Ниже приведен пример (из [примера SimpleSample10](https://msdn.microsoft.com/library/Ee416428(v=VS.85).aspx)), который получает эти переменные:</span><span class="sxs-lookup"><span data-stu-id="27d63-107">Here is an example (from [SimpleSample10 Sample](https://msdn.microsoft.com/library/Ee416428(v=VS.85).aspx)) that gets these variables:</span></span>


```
ID3D10EffectVariable* g_pVariable;
ID3D10EffectMatrixVariable* g_pmWorld;
ID3D10EffectScalarVariable* g_pfTime;

g_pVariable = g_pEffect10->GetVariableByName("g_mWorld");
g_pmWorld = g_pVariable->AsMatrix();
g_pfTime = g_pEffect10->GetVariableByName("g_fTime");
g_pfTime = g_pVariable->AsScalar();
```



<span data-ttu-id="27d63-108">Путем специализации интерфейсов можно сократить код до одного вызова.</span><span class="sxs-lookup"><span data-stu-id="27d63-108">By specializing the interfaces, you could reduce the code to a single call.</span></span>


```
g_pmWorld = (g_pEffect10->GetVariableByName("g_mWorld"))->AsMatrix();
g_pfTime = (g_pEffect10->GetVariableByName("g_fTime"))->AsScalar();
```



<span data-ttu-id="27d63-109">Интерфейсы, которые наследуют от [**интерфейса ID3D10EffectVariable**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectvariable) , также имеют эти методы, но они были разработаны для возврата недопустимых объектов. только вызовы из **интерфейса ID3D10EffectVariable** возвращают допустимые объекты.</span><span class="sxs-lookup"><span data-stu-id="27d63-109">Interfaces that inherit from [**ID3D10EffectVariable Interface**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectvariable) also have these methods, but they have been designed to return invalid objects; only calls from **ID3D10EffectVariable Interface** return valid objects.</span></span> <span data-ttu-id="27d63-110">Приложения могут проверить возвращаемый объект, чтобы проверить, является ли он допустимым, вызвав [**ID3D10EffectVariable:: IsValid**](/windows/desktop/api/D3D10Effect/nf-d3d10effect-id3d10effectvariable-isvalid).</span><span class="sxs-lookup"><span data-stu-id="27d63-110">Applications can test the returned object to see if it is valid by calling [**ID3D10EffectVariable::IsValid**](/windows/desktop/api/D3D10Effect/nf-d3d10effect-id3d10effectvariable-isvalid).</span></span>

## <a name="related-topics"></a><span data-ttu-id="27d63-111">См. также</span><span class="sxs-lookup"><span data-stu-id="27d63-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="27d63-112">Эффекты</span><span class="sxs-lookup"><span data-stu-id="27d63-112">Effects</span></span>](d3d10-graphics-programming-guide-effects.md)
</dt> </dl>

 

 



