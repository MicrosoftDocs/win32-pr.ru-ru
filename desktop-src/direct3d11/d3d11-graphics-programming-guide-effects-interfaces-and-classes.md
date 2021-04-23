---
title: Интерфейсы и классы в эффектах
description: Существует множество способов использования классов и интерфейсов в влиянии 11.
ms.assetid: 526d477b-fc1f-4bd0-a620-ce9b78147f68
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3b067b8e03b2d43ea44ccab6164424cbc84c7237
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104413166"
---
# <a name="interfaces-and-classes-in-effects"></a><span data-ttu-id="6e302-103">Интерфейсы и классы в эффектах</span><span class="sxs-lookup"><span data-stu-id="6e302-103">Interfaces and Classes in Effects</span></span>

<span data-ttu-id="6e302-104">Существует множество способов использования классов и интерфейсов в влиянии 11.</span><span class="sxs-lookup"><span data-stu-id="6e302-104">There are many ways to use classes and interfaces in Effects 11.</span></span> <span data-ttu-id="6e302-105">Синтаксис интерфейса и класса см. в разделе [интерфейсы и классы](/windows/desktop/direct3dhlsl/overviews-direct3d-11-hlsl-dynamic-linking-class).</span><span class="sxs-lookup"><span data-stu-id="6e302-105">For interface and class syntax, see [Interfaces and Classes](/windows/desktop/direct3dhlsl/overviews-direct3d-11-hlsl-dynamic-linking-class).</span></span>

<span data-ttu-id="6e302-106">В следующих разделах подробно описано, как указать экземпляры класса для шейдера, использующего интерфейсы.</span><span class="sxs-lookup"><span data-stu-id="6e302-106">The following sections detail how to specify class instances to a shader which uses interfaces.</span></span> <span data-ttu-id="6e302-107">В примерах мы будем использовать следующий интерфейс и классы:</span><span class="sxs-lookup"><span data-stu-id="6e302-107">We will use the following interface and classes in the examples:</span></span>


```
interface IColor
{
  float4 GetColor();
};

class CRed : IColor
{
  float4 GetColor() { return float4(1,0,0,1); }
};
class CGreen : IColor
{
  float4 GetColor() { return float4(0,1,0,1); }
};

CRed pRed;
CGreen pGreen;
IColor pIColor;
IColor pIColor2 = pRed;
```



<span data-ttu-id="6e302-108">Обратите внимание, что экземпляры интерфейса можно инициализировать экземплярами класса.</span><span class="sxs-lookup"><span data-stu-id="6e302-108">Note that interface instances can be initialized to class instances.</span></span> <span data-ttu-id="6e302-109">Массивы экземпляров классов и интерфейсов также поддерживаются, и их можно инициализировать, как показано в следующем примере:</span><span class="sxs-lookup"><span data-stu-id="6e302-109">Arrays of class and interface instances are also supported and they can be initialized as in the following example:</span></span>


```
CRed pRedArray[2];
IColor pIColor3 = pRedArray[1];
IColor pIColorArray[2] = {pRed, pGreen};
IColor pIColorArray2[2] = pRedArray;
```



## <a name="uniform-interface-parameters"></a><span data-ttu-id="6e302-110">Параметры универсального интерфейса</span><span class="sxs-lookup"><span data-stu-id="6e302-110">Uniform Interface Parameters</span></span>

<span data-ttu-id="6e302-111">Как и другие однородные типы данных, параметры универсального интерфейса должны быть указаны в вызове Компилешадер.</span><span class="sxs-lookup"><span data-stu-id="6e302-111">Just like other uniform data types, uniform interface parameters must be specified in the CompileShader call.</span></span> <span data-ttu-id="6e302-112">Параметры интерфейса могут быть назначены глобальным экземплярам интерфейса или экземплярам глобальных классов.</span><span class="sxs-lookup"><span data-stu-id="6e302-112">Interface parameters can be assigned to global interface instances or global class instances.</span></span> <span data-ttu-id="6e302-113">При назначении глобальному экземпляру интерфейса шейдер будет иметь зависимость от экземпляра интерфейса, что означает, что для него должен быть задан экземпляр класса.</span><span class="sxs-lookup"><span data-stu-id="6e302-113">When assigned to a global interface instance, the shader will have a dependency on the interface instance, which means that it must be set to a class instance.</span></span> <span data-ttu-id="6e302-114">При назначении экземплярам глобального класса компилятор специализирует шейдер (как с другими универсальными типами данных) для использования этого класса.</span><span class="sxs-lookup"><span data-stu-id="6e302-114">When assigned to global class instances, the compiler specializes the shader (as with other uniform data types) to use that class.</span></span> <span data-ttu-id="6e302-115">Это важно для двух сценариев:</span><span class="sxs-lookup"><span data-stu-id="6e302-115">This is important for two scenarios:</span></span>

1.  <span data-ttu-id="6e302-116">Шейдеры с \_ целевым объектом 4 x могут использовать параметры интерфейса, если эти параметры являются универсальными и назначены глобальным экземплярам класса (поэтому динамическая компоновка не используется).</span><span class="sxs-lookup"><span data-stu-id="6e302-116">Shaders with a 4\_x target can use interface parameters if these parameters are uniform and assigned to global class instances (so no dynamic linkage is used).</span></span>
2.  <span data-ttu-id="6e302-117">Пользователи могут принимать решение о наличии многих скомпилированных, специализированных шейдеров без динамической компоновки или нескольких скомпилированных шейдеров с динамической компоновкой.</span><span class="sxs-lookup"><span data-stu-id="6e302-117">Users can decide to have many compiled, specialized shaders with no dynamic linkage or few compiled shaders with dynamic linkage.</span></span>


```
float4 PSUniform( uniform IColor color ) : SV_Target
{
  return color;
}

technique11
{
  pass
  {
    SetPixelShader( CompileShader( ps_4_0, PSUniform(pRed) ) );
  }
  pass
  {
    SetPixelShader( CompileShader( ps_5_0, PSUniform(pIColor2) ) );
  }
}
```



<span data-ttu-id="6e302-118">Если pIColor2 остается неизменным через API, то предыдущие два прохода функционально эквивалентны, но первый использует \_ статический шейдер PS 4 0, \_ а второй использует \_ шейдер PS 5 \_ 0 с динамической компоновкой.</span><span class="sxs-lookup"><span data-stu-id="6e302-118">If pIColor2 remains unchanged through the API, then the previous two passes are functionally equivalent, but the first uses a ps\_4\_0 static shader while the second uses a ps\_5\_0 shader with dynamic linkage.</span></span> <span data-ttu-id="6e302-119">Если pIColor2 изменяется с помощью API Effects (см. раздел Установка экземпляров класса ниже), то поведение шейдера пикселей во втором проходе может измениться.</span><span class="sxs-lookup"><span data-stu-id="6e302-119">If pIColor2 is changed through the effects API (see Setting Class Instances below), then the behavior of the pixel shader in the second pass may change.</span></span>

## <a name="non-uniform-interface-parameters"></a><span data-ttu-id="6e302-120">Параметры неоднородного интерфейса</span><span class="sxs-lookup"><span data-stu-id="6e302-120">Non-Uniform Interface Parameters</span></span>

<span data-ttu-id="6e302-121">Параметры неоднородного интерфейса создают зависимости интерфейсов для шейдеров.</span><span class="sxs-lookup"><span data-stu-id="6e302-121">Non-uniform interface parameters create interface dependencies for the shaders.</span></span> <span data-ttu-id="6e302-122">При применении шейдера с параметрами интерфейса эти параметры должны быть назначены в вызове Биндинтерфацес.</span><span class="sxs-lookup"><span data-stu-id="6e302-122">When applying a shader with interface parameters, these parameters must be assigned in with the BindInterfaces call.</span></span> <span data-ttu-id="6e302-123">Экземпляры глобальных интерфейсов и экземпляры глобальных классов можно указать в вызове Биндинтерфацес.</span><span class="sxs-lookup"><span data-stu-id="6e302-123">Global interface instances and global class instances can be specified in the BindInterfaces call.</span></span>


```
float4 PSAbstract( IColor color ) : SV_Target
{
  return color;
}

PixelShader pPSAbstract = CompileShader( ps_5_0, PSAbstract(pRed) );

technique11
{
  pass
  {
    SetPixelShader( BindInterfaces( pPSAbstract, pRed ) );
  }
  pass
  {
    SetPixelShader( BindInterfaces( pPSAbstract, pIColor2 ) );
  }
}
```



<span data-ttu-id="6e302-124">Если pIColor2 остается неизменным через API, предыдущие два прохода функционально эквивалентны и используют динамическую компоновку.</span><span class="sxs-lookup"><span data-stu-id="6e302-124">If pIColor2 remains unchanged through the API, then the previous two passes are functionally equivalent and both use dynamic linkage.</span></span> <span data-ttu-id="6e302-125">Если pIColor2 изменяется с помощью API Effects (см. раздел Установка экземпляров класса ниже), то поведение шейдера пикселей во втором проходе может измениться.</span><span class="sxs-lookup"><span data-stu-id="6e302-125">If pIColor2 is changed through the effects API (see Setting Class Instances below), then the behavior of the pixel shader in the second pass may change.</span></span>

## <a name="setting-class-instances"></a><span data-ttu-id="6e302-126">Установка экземпляров класса</span><span class="sxs-lookup"><span data-stu-id="6e302-126">Setting Class Instances</span></span>

<span data-ttu-id="6e302-127">При настройке шейдера с помощью динамической компоновки шейдера для устройства Direct3D 11 необходимо также указать экземпляры класса.</span><span class="sxs-lookup"><span data-stu-id="6e302-127">When setting a shader with dynamic shader linkage to the Direct3D 11 device, class instances must also be specified.</span></span> <span data-ttu-id="6e302-128">При задании такого шейдера с **пустым** экземпляром класса возникает ошибка.</span><span class="sxs-lookup"><span data-stu-id="6e302-128">It is an error to set such a shader with a **NULL** class instance.</span></span> <span data-ttu-id="6e302-129">Таким образом, все экземпляры интерфейса, на которые ссылается шейдер, должны иметь связанный экземпляр класса.</span><span class="sxs-lookup"><span data-stu-id="6e302-129">Therefore, all interface instances which a shader references must have an associated class instance.</span></span>

<span data-ttu-id="6e302-130">В следующем примере показано, как получить переменную экземпляра класса из действия и задать ее для переменной интерфейса:</span><span class="sxs-lookup"><span data-stu-id="6e302-130">The following example shows how to get a class instance variable from an effect and set it to an interface variable:</span></span>


```
ID3DX11EffectPass* pPass = pEffect->GetTechniqueByIndex(0)->GetPassByIndex(1);

ID3DX11EffectInterfaceVariable* pIface = pEffect->GetVariableByName( "pIColor2" )->AsInterface();
ID3DX11EffectClassInstanceVariable* pCI = pEffect->GetVariableByName( "pGreen" )->AsClassInstance();
pIface->SetClassInstance( pCI );
pPass->Apply( 0, pDeviceContext );

// Apply the same pass with a different class instance
pCI = pEffect->GetVariableByName( "pRedArray" )->GetElement(1)->AsClassInstance();
pIface->SetClassInstance( pCI );
pPass->Apply( 0, pDeviceContext );
```



## <a name="related-topics"></a><span data-ttu-id="6e302-131">См. также</span><span class="sxs-lookup"><span data-stu-id="6e302-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6e302-132">Эффекты (Direct3D 11)</span><span class="sxs-lookup"><span data-stu-id="6e302-132">Effects (Direct3D 11)</span></span>](d3d11-graphics-programming-guide-effects.md)
</dt> </dl>

 

 