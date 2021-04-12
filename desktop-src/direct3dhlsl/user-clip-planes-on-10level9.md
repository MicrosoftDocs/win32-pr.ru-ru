---
title: Пользовательские плоскости для устройств на уровне компонентов 9
description: Начиная с Windows 8, язык шейдеров высокого уровня (Майкрософт) (HLSL) поддерживает синтаксис, который можно использовать с API Microsoft Direct3D 11 для указания плоскости-клипов пользователя на уровне компонентов 9 \_ x и выше.
ms.assetid: C51FB0E5-94C3-4E7F-AC33-E5F0F26EDC11
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 968831ca39f2501a44b00f202fd8dfda1f92d1e7
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104338057"
---
# <a name="user-clip-planes-on-feature-level-9-hardware"></a><span data-ttu-id="d7b56-103">Пользовательские плоскости для устройств на уровне компонентов 9</span><span class="sxs-lookup"><span data-stu-id="d7b56-103">User clip planes on feature level 9 hardware</span></span>

<span data-ttu-id="d7b56-104">Начиная с Windows 8, язык шейдеров высокого уровня (Майкрософт) (HLSL) поддерживает синтаксис, который можно использовать с API Microsoft Direct3D 11 для указания плоскости-клипов пользователя на [уровне компонентов](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro) 9 \_ x и выше.</span><span class="sxs-lookup"><span data-stu-id="d7b56-104">Starting with Windows 8, Microsoft High Level Shader Language (HLSL) supports a syntax that you can use with the Microsoft Direct3D 11 API to specify user clip planes on [feature level](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro) 9\_x and higher.</span></span> <span data-ttu-id="d7b56-105">Этот синтаксис Clip-плоскостей можно использовать для создания шейдера, а затем использовать этот объект шейдера с API Direct3D 11 для выполнения на всех уровнях функций Direct3D.</span><span class="sxs-lookup"><span data-stu-id="d7b56-105">You can use this clip-planes syntax to write a shader, and then use that shader object with the Direct3D 11 API to run on all Direct3D feature levels.</span></span>

-   [<span data-ttu-id="d7b56-106">Фон</span><span class="sxs-lookup"><span data-stu-id="d7b56-106">Background</span></span>](#background-reading)
-   [<span data-ttu-id="d7b56-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d7b56-107">Syntax</span></span>](#syntax)
-   [<span data-ttu-id="d7b56-108">Создание вырезок в пространстве клипов на уровне функций 9 и выше</span><span class="sxs-lookup"><span data-stu-id="d7b56-108">Creating clip planes in clip space on feature level 9 and higher</span></span>](#creating-clip-planes-in-clip-space-on-feature-level-9-and-higher)
    -   [<span data-ttu-id="d7b56-109">Фоновое чтение</span><span class="sxs-lookup"><span data-stu-id="d7b56-109">Background reading</span></span>](#background-reading)
    -   [<span data-ttu-id="d7b56-110">уровни компонентов 10Level9</span><span class="sxs-lookup"><span data-stu-id="d7b56-110">10Level9 feature levels</span></span>](#10level9-feature-levels)
    -   [<span data-ttu-id="d7b56-111">Математика для плоскости обрезки</span><span class="sxs-lookup"><span data-stu-id="d7b56-111">Clip plane math</span></span>](#clip-plane-math)
    -   [<span data-ttu-id="d7b56-112">Обрезка в области просмотра</span><span class="sxs-lookup"><span data-stu-id="d7b56-112">Clipping in view space</span></span>](#clipping-in-view-space)
    -   [<span data-ttu-id="d7b56-113">Матрица проекции</span><span class="sxs-lookup"><span data-stu-id="d7b56-113">Projection matrix</span></span>](#projection-matrix)
    -   [<span data-ttu-id="d7b56-114">Плоскость обрезки области обрезки</span><span class="sxs-lookup"><span data-stu-id="d7b56-114">Clip space clip plane</span></span>](#clip-space-clip-plane)
-   [<span data-ttu-id="d7b56-115">См. также</span><span class="sxs-lookup"><span data-stu-id="d7b56-115">Related topics</span></span>](#related-topics)

## <a name="background"></a><span data-ttu-id="d7b56-116">Историческая справка</span><span class="sxs-lookup"><span data-stu-id="d7b56-116">Background</span></span>

<span data-ttu-id="d7b56-117">Вы можете получить доступ к пользовательским роликам в API Microsoft Direct3D 9 с помощью методов [**IDirect3DDevice9:: сетклипплане**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-setclipplane) и [**IDirect3DDevice9:: жетклипплане**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-getclipplane) .</span><span class="sxs-lookup"><span data-stu-id="d7b56-117">You can access user clip planes in the Microsoft Direct3D 9 API via [**IDirect3DDevice9::SetClipPlane**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-setclipplane) and [**IDirect3DDevice9::GetClipPlane**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-getclipplane) methods.</span></span> <span data-ttu-id="d7b56-118">В Microsoft Direct3D 10 и более поздних версиях доступ к пользовательским роликам можно получить с помощью [ \_ клипдистанцеа SV](dx-graphics-hlsl-semantics.md) .</span><span class="sxs-lookup"><span data-stu-id="d7b56-118">In Microsoft Direct3D 10 and later, you can access user clip planes through the [SV\_ClipDistance](dx-graphics-hlsl-semantics.md) semantic.</span></span> <span data-ttu-id="d7b56-119">Но до Windows 8, ОКП \_ клипдистанце было недоступно для оборудования [уровня функции](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro) 9 \_ x в API Direct3D 10 или Direct3D 11.</span><span class="sxs-lookup"><span data-stu-id="d7b56-119">But before Windows 8, SV\_ClipDistance was not available for [feature level](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro) 9\_x hardware in the Direct3D 10 or Direct3D 11 APIs.</span></span> <span data-ttu-id="d7b56-120">Таким образом, до выхода Windows 8, единственный способ получить доступ к пользовательским плоскостям с оборудованием уровня Feature 9 \_ x с помощью API Direct3D 9.</span><span class="sxs-lookup"><span data-stu-id="d7b56-120">So, before Windows 8, the only way to access user clip planes with feature level 9\_x hardware was through the Direct3D 9 API.</span></span> <span data-ttu-id="d7b56-121">Приложения для Магазина Windows Direct3D не могут использовать API Direct3D 9.</span><span class="sxs-lookup"><span data-stu-id="d7b56-121">Direct3D Windows Store apps can't use the Direct3D 9 API.</span></span> <span data-ttu-id="d7b56-122">Здесь описывается синтаксис, который можно использовать для доступа к пользовательским роликам через API Direct3D 11 на уровне функций 9 \_ x и выше.</span><span class="sxs-lookup"><span data-stu-id="d7b56-122">Here we describe the syntax that you can use to access user clip planes through the Direct3D 11 API on feature level 9\_x and higher.</span></span>

<span data-ttu-id="d7b56-123">В приложениях для определения набора невидимых плоскостей в трехмерном мире, которые обрисуются (отбрасываются) все рисуемые примитивы, используются резкие плоскости.</span><span class="sxs-lookup"><span data-stu-id="d7b56-123">Apps use clip planes to define a set of invisible planes within the 3D world that clip (throw away) all drawn primitives.</span></span> <span data-ttu-id="d7b56-124">Windows не будет рисовать любой пиксель, находящийся на отрицательной стороне любой плоскости-отсечения.</span><span class="sxs-lookup"><span data-stu-id="d7b56-124">Windows won't draw any pixel that is on the negative side of any clip planes.</span></span> <span data-ttu-id="d7b56-125">После этого приложения могут использовать резкие плоскости для отрисовки плоских отражений.</span><span class="sxs-lookup"><span data-stu-id="d7b56-125">Apps can then use clip planes to render planar reflections.</span></span>

## <a name="syntax"></a><span data-ttu-id="d7b56-126">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d7b56-126">Syntax</span></span>

<span data-ttu-id="d7b56-127">Используйте этот синтаксис для объявления плоскостей Clip в качестве атрибутов функций в [объявлении функции](dx-graphics-hlsl-function-syntax.md).</span><span class="sxs-lookup"><span data-stu-id="d7b56-127">Use this syntax to declare clip planes as function attributes in a [function declaration](dx-graphics-hlsl-function-syntax.md).</span></span> <span data-ttu-id="d7b56-128">Например, здесь мы используем синтаксис для фрагмента шейдера вершин:</span><span class="sxs-lookup"><span data-stu-id="d7b56-128">For example, here we use the syntax on a vertex shader fragment:</span></span>

``` syntax
cbuffer ClipPlaneConstantBuffer 
{
       float4 clipPlane1;
       float4 clipPlane2;
};

[clipplanes(clipPlane1,clipPlane2)]
VertexShaderOutput main(VertexShaderInput input)
{
       // the rest of the vertex shader doesn't refer to the clip plane
 
       …
 
       return output;
}
```

<span data-ttu-id="d7b56-129">В этом примере фрагмента шейдера вершин обозначает две плоскости.</span><span class="sxs-lookup"><span data-stu-id="d7b56-129">This example for a vertex shader fragment denotes two clip planes.</span></span> <span data-ttu-id="d7b56-130">Он показывает, что необходимо поместить новый атрибут **клиппланес** в квадратные скобки непосредственно перед возвращаемым значением шейдера вершин.</span><span class="sxs-lookup"><span data-stu-id="d7b56-130">It shows that you need to place the new **clipplanes** attribute within square brackets immediately before the return value of the vertex shader.</span></span> <span data-ttu-id="d7b56-131">В скобках после атрибута **клиппланес** вы предоставляете список из до 6 констант **float4** , определяющих коэффициенты плоскости для каждой активной плоскости клипов.</span><span class="sxs-lookup"><span data-stu-id="d7b56-131">Within parentheses after the **clipplanes** attribute, you provide a list of up to 6 **float4** constants that define the plane coefficients for each active clip plane.</span></span> <span data-ttu-id="d7b56-132">В примере также показано, что коэффициенты каждой плоскости должны находиться в буфере констант.</span><span class="sxs-lookup"><span data-stu-id="d7b56-132">The example also shows that you need to make the coefficients of each plane reside in a constant buffer.</span></span>

> [!Note]  
> <span data-ttu-id="d7b56-133">Нет доступных синтаксических конструкций для динамического отключения плоскости Clip.</span><span class="sxs-lookup"><span data-stu-id="d7b56-133">There is no syntax available to disable a clip plane dynamically.</span></span> <span data-ttu-id="d7b56-134">Необходимо либо перекомпилировать другой, идентичный шейдер без атрибута **клиппланес** , либо ваше приложение может задать коэффициенты в константном буфере равными нулю, чтобы плоскость больше не влияла ни на одну геометрию.</span><span class="sxs-lookup"><span data-stu-id="d7b56-134">You must either recompile an otherwise identical shader with no **clipplanes** attribute, or your app can set the coefficients in your constant buffer to zero so that the plane no longer affects any geometry.</span></span>

 

<span data-ttu-id="d7b56-135">Этот синтаксис доступен для любой цели шейдера вершин 4,0 или более поздней версии, которая включает VS \_ 4 \_ 0 \_ уровня \_ 9 \_ 1 и VS \_ 4 \_ 0 \_ уровня \_ 9 \_ 3.</span><span class="sxs-lookup"><span data-stu-id="d7b56-135">This syntax is available for any 4.0 or later vertex shader target, which includes vs\_4\_0\_level\_9\_1 and vs\_4\_0\_level\_9\_3.</span></span>

## <a name="creating-clip-planes-in-clip-space-on-feature-level-9-and-higher"></a><span data-ttu-id="d7b56-136">Создание вырезок в пространстве клипов на уровне функций 9 и выше</span><span class="sxs-lookup"><span data-stu-id="d7b56-136">Creating clip planes in clip space on feature level 9 and higher</span></span>

<span data-ttu-id="d7b56-137">Здесь мы покажем, как создавать резкие плоскости на [уровне функций](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro) 9 \_ x и выше.</span><span class="sxs-lookup"><span data-stu-id="d7b56-137">Here we show how to create clip planes in clip space on [feature level](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro) 9\_x and higher.</span></span>

### <a name="background-reading"></a><span data-ttu-id="d7b56-138">Фоновое чтение</span><span class="sxs-lookup"><span data-stu-id="d7b56-138">Background reading</span></span>

<span data-ttu-id="d7b56-139">«Знакомство с программированием трехмерной игры с помощью DirectX 10» от Федор г. Luna объясняет графический математический график (главы 1, 2 и 3), а также различные пробелы и преобразования пробелов, происходящие в шейдере вершин (разделы 5,6 и 5,8).</span><span class="sxs-lookup"><span data-stu-id="d7b56-139">"Introduction to 3D Game Programming with DirectX 10" by Frank D. Luna explains the graphics math background (chapters 1, 2 and 3) you need, and the various spaces and space transformations that occur in the vertex shader (sections 5.6 and 5.8).</span></span>

### <a name="10level9-feature-levels"></a><span data-ttu-id="d7b56-140">уровни компонентов 10Level9</span><span class="sxs-lookup"><span data-stu-id="d7b56-140">10Level9 feature levels</span></span>

<span data-ttu-id="d7b56-141">В Direct3D 10 и более поздних версиях можно обрезать любое пространство, которое имеет смысл, часто в пространстве мира или области просмотра.</span><span class="sxs-lookup"><span data-stu-id="d7b56-141">In Direct3D 10 and later, you can clip in any space that makes sense, often in world space or view space.</span></span> <span data-ttu-id="d7b56-142">Но Direct3D 9 использует место для обрезки, что является предварительной перспективой для разделения области проекции.</span><span class="sxs-lookup"><span data-stu-id="d7b56-142">But Direct3D 9 uses clip space, which is pre perspective divide projection space.</span></span> <span data-ttu-id="d7b56-143">Векторы находятся в пространстве обрезки, когда шейдер вершин передает их этапам, которые следуют за [графическим конвейером](/windows/desktop/direct3d11/overviews-direct3d-11-graphics-pipeline).</span><span class="sxs-lookup"><span data-stu-id="d7b56-143">Vectors are in clip space when the vertex shader passes them to stages that follow in the [graphics pipeline](/windows/desktop/direct3d11/overviews-direct3d-11-graphics-pipeline).</span></span>

<span data-ttu-id="d7b56-144">При написании приложения для Магазина Windows необходимо использовать уровни компонентов 10Level9 ([уровень функций](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro) 9 \_ x), чтобы приложение можно было запускать на уровне функций 9 \_ x и более высоких аппаратных средств.</span><span class="sxs-lookup"><span data-stu-id="d7b56-144">When you write a Windows Store app, you must use 10Level9 feature levels ([feature level](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro) 9\_x) so the app can run on feature level 9\_x and higher hardware.</span></span> <span data-ttu-id="d7b56-145">Так как приложение поддерживает уровень функций 9 \_ x и более поздних версий, необходимо также использовать распространенную возможность применения плоскостей к области обрезки.</span><span class="sxs-lookup"><span data-stu-id="d7b56-145">Because your app supports feature level 9\_x and higher, you must also use the common capability of applying clip planes in clip space.</span></span>

<span data-ttu-id="d7b56-146">При компиляции шейдера вершин с VS \_ 4 0 на \_ \_ уровне \_ 9 \_ 1 или более поздней версии шейдер вершин может использовать атрибут **клиппланес** .</span><span class="sxs-lookup"><span data-stu-id="d7b56-146">When you compile a vertex shader with vs\_4\_0\_level\_9\_1 or later, that vertex shader can use the **clipplanes** attribute.</span></span> <span data-ttu-id="d7b56-147">Объект Direct3D 10 или более поздней версии имеет скалярное произведение порожденной вершины, которая содержит каждую из глобальных констант **float4** , указанных в атрибуте.</span><span class="sxs-lookup"><span data-stu-id="d7b56-147">A Direct3D 10 or later object has a dot product of the emitted vertex that contains each of the **float4** global constants specified in the attribute.</span></span> <span data-ttu-id="d7b56-148">Объект Direct3D 9 имеет достаточно метаданных, чтобы среда выполнения 10Level9 выдавала соответствующие вызовы [**IDirect3DDevice9:: сетклипплане**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-setclipplane).</span><span class="sxs-lookup"><span data-stu-id="d7b56-148">The Direct3D 9 object has enough meta data to cause the 10Level9 runtime to issue the appropriate calls to [**IDirect3DDevice9::SetClipPlane**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-setclipplane).</span></span>

### <a name="clip-plane-math"></a><span data-ttu-id="d7b56-149">Математика для плоскости обрезки</span><span class="sxs-lookup"><span data-stu-id="d7b56-149">Clip plane math</span></span>

<span data-ttu-id="d7b56-150">Плоскость обрезки определяется с помощью вектора с 4 компонентами.</span><span class="sxs-lookup"><span data-stu-id="d7b56-150">A clip plane is defined by a vector with 4 components.</span></span> <span data-ttu-id="d7b56-151">Первые три компонента определяют вектор x, y и z, основывается от источника в пространстве, которое нужно вырезать.</span><span class="sxs-lookup"><span data-stu-id="d7b56-151">The first three components define an x, y, z vector that emanates from the origin in the space we want to clip.</span></span> <span data-ttu-id="d7b56-152">Этот вектор подразумевает плоскость, перпендикулярную вектору и выполняемую через источник.</span><span class="sxs-lookup"><span data-stu-id="d7b56-152">This vector implies a plane, perpendicular to the vector and running through the origin.</span></span> <span data-ttu-id="d7b56-153">Windows сохраняет все пиксели на стороне вектора плоскости и обрезает все пиксели за плоскостью.</span><span class="sxs-lookup"><span data-stu-id="d7b56-153">Windows keeps all pixels on the vector side of the plane and clips all pixels behind the plane.</span></span> <span data-ttu-id="d7b56-154">Компонент, расположенный на этом уровне, помещает плоскость обратно и заставляет Windows обрезаться меньше (отрицательный w приводит к тому, что Windows обрезается) вдоль векторной линии.</span><span class="sxs-lookup"><span data-stu-id="d7b56-154">The forth w component pushes the plane back and causes Windows to clip less (a negative w causes Windows to clip more) along the vector line.</span></span> <span data-ttu-id="d7b56-155">Если компоненты x, y, z составляют вектор (нормализованный), w помещает на плоскости единицы w.</span><span class="sxs-lookup"><span data-stu-id="d7b56-155">If the x, y, z components compose a unit (normalized) vector, w pushes the plane w units back.</span></span>

<span data-ttu-id="d7b56-156">Математические вычисления, выполняемые графическим процессором (GPU) для определения обрезки, — это простой точечный продукт между вектором вершин (x, y, z, 1) и вектором плоскости обрезки.</span><span class="sxs-lookup"><span data-stu-id="d7b56-156">The math that the graphics processing unit (GPU) performs to determine clipping is a simple dot product between the vertex vector (x, y, z, 1) and the clipping plane vector.</span></span> <span data-ttu-id="d7b56-157">Эта математическая операция создает длину проекции на векторе плоскости Clip.</span><span class="sxs-lookup"><span data-stu-id="d7b56-157">This math operation creates a projection length on the clip plane vector.</span></span> <span data-ttu-id="d7b56-158">Отрицательная точка содержит вершину, которая расположена на обрезанной стороне плоскости.</span><span class="sxs-lookup"><span data-stu-id="d7b56-158">A negative dot product shows the vertex to be on the clipped side of the plane.</span></span>

### <a name="clipping-in-view-space"></a><span data-ttu-id="d7b56-159">Обрезка в области просмотра</span><span class="sxs-lookup"><span data-stu-id="d7b56-159">Clipping in view space</span></span>

<span data-ttu-id="d7b56-160">Вот наша вершина в пространстве для просмотра:</span><span class="sxs-lookup"><span data-stu-id="d7b56-160">Here is our vertex in view space:</span></span>

![вершина в пространстве просмотра](images/vertex-clip.png)

<span data-ttu-id="d7b56-162">Вот наша плоскость обрезки в области просмотра:</span><span class="sxs-lookup"><span data-stu-id="d7b56-162">Here is our clip plane in view space:</span></span>

![плоскость обрезки в области просмотра](images/clip-plane-view.png)

<span data-ttu-id="d7b56-164">Ниже приведена точка вершины и плоскости Clip в области просмотра:</span><span class="sxs-lookup"><span data-stu-id="d7b56-164">Here is the dot product of vertex and clip plane in view space:</span></span>

<span data-ttu-id="d7b56-165">Клипдистанце = **v** · **C**  =  *v* ₓ *c* ₓ +*v*<sub>y</sub>*c*<sub>y</sub>  +  *v*<sub>z</sub>*c*<sub>z</sub>  +  *c*<sub>w</sub></span><span class="sxs-lookup"><span data-stu-id="d7b56-165">ClipDistance = **v** · **C** = *v* ₓ *C* ₓ +*v*<sub>y</sub>*C*<sub>y</sub> + *v*<sub>z</sub>*C*<sub>z</sub> + *C*<sub>w</sub></span></span>

<span data-ttu-id="d7b56-166">Эта математическая операция работает для объекта Direct3D 10 или более поздней версии, но не будет работать для объекта Direct3D 9.</span><span class="sxs-lookup"><span data-stu-id="d7b56-166">This math operation works for a Direct3D 10 or later object but won't work for a Direct3D 9 object.</span></span> <span data-ttu-id="d7b56-167">Для Direct3D 9 сначала нужно получить преобразование проекции в область обрезки.</span><span class="sxs-lookup"><span data-stu-id="d7b56-167">For Direct3D 9, we must first get through our projection transform into clip space.</span></span>

### <a name="projection-matrix"></a><span data-ttu-id="d7b56-168">Матрица проекции</span><span class="sxs-lookup"><span data-stu-id="d7b56-168">Projection matrix</span></span>

<span data-ttu-id="d7b56-169">Матрица проекции преобразует вершину из пространства просмотра (где источником является глаз средства просмотра, + x — справа, + y — вверх), а + z — прямо вперед) в место обрезки.</span><span class="sxs-lookup"><span data-stu-id="d7b56-169">A projection matrix transforms a vertex from view space (where the origin is the viewer's eye, +x is to the right, +y is up, and +z is straight ahead) into clip space.</span></span> <span data-ttu-id="d7b56-170">Матрица проекции считывает вершину вырезки оборудования и [этапа растрирования](/windows/desktop/direct3d11/d3d10-graphics-programming-guide-rasterizer-stage).</span><span class="sxs-lookup"><span data-stu-id="d7b56-170">The projection matrix readies the vertex for hardware clipping and the [rasterization stage](/windows/desktop/direct3d11/d3d10-graphics-programming-guide-rasterizer-stage).</span></span> <span data-ttu-id="d7b56-171">Ниже приведена стандартная перспективная матрица (другие проекции, для которых требуются различные математические вычисления):</span><span class="sxs-lookup"><span data-stu-id="d7b56-171">Here is a standard perspective matrix (other projections require different math):</span></span>

<dl> <span data-ttu-id="d7b56-172">Коэффициент *r*   по ширине и высоте окна</span><span class="sxs-lookup"><span data-stu-id="d7b56-172">*r*  ratio of window width/height</span></span>  
<span data-ttu-id="d7b56-173">   угол обзора α</span><span class="sxs-lookup"><span data-stu-id="d7b56-173">*α*  viewing angle</span></span>  
<span data-ttu-id="d7b56-174">*f*   расстояние от средства просмотра до дальней плоскости</span><span class="sxs-lookup"><span data-stu-id="d7b56-174">*f*  distance from the viewer to the far plane</span></span>  
<span data-ttu-id="d7b56-175">*n*   расстояние от средства просмотра до ближайшей плоскости</span><span class="sxs-lookup"><span data-stu-id="d7b56-175">*n*  distance from the viewer to the near plane</span></span>
</dl><span data-ttu-id="d7b56-176">![матрица проекции](images/projection-matrix.png)</span><span class="sxs-lookup"><span data-stu-id="d7b56-176">![projection matrix](images/projection-matrix.png)</span></span>

<span data-ttu-id="d7b56-177">Следующая матрица является упрощенной версией предыдущей матрицы.</span><span class="sxs-lookup"><span data-stu-id="d7b56-177">The next matrix is a simplified version of the previous matrix.</span></span> <span data-ttu-id="d7b56-178">Мы видим, что матрица упрощена, поэтому мы можем использовать ее позже в операции матрицы.</span><span class="sxs-lookup"><span data-stu-id="d7b56-178">We show the matrix simplified so we can use it later in the matrix multiply operation.</span></span>

![Упрощенная матрица проекции](images/projection-matrix2.png)

<span data-ttu-id="d7b56-180">Теперь мы преобразуем вершину представления "представление" в пространство обрезки с помощью матрицы.</span><span class="sxs-lookup"><span data-stu-id="d7b56-180">Now we transform our view space vertex into clip space with a matrix multiply:</span></span>

![умножение матрицы](images/matrix-multiply.png)

<span data-ttu-id="d7b56-182">В нашей операции матрицы, наши компоненты x и y незначительно корректируются, но наши компоненты z и w довольно искажены.</span><span class="sxs-lookup"><span data-stu-id="d7b56-182">In our matrix multiply operation, our x and y components are only slightly adjusted, but our z and w components are quite mangled.</span></span> <span data-ttu-id="d7b56-183">Наша плоскость обрезки не даст нам нам, что нам нужно.</span><span class="sxs-lookup"><span data-stu-id="d7b56-183">Our clip plane won't give us what we want any more.</span></span>

### <a name="clip-space-clip-plane"></a><span data-ttu-id="d7b56-184">Плоскость обрезки области обрезки</span><span class="sxs-lookup"><span data-stu-id="d7b56-184">Clip space clip plane</span></span>

<span data-ttu-id="d7b56-185">Здесь мы хотим создать плоскость обрезки, для которой произведение точки с нашей вершиной размещения отсечения дает нам то же значение, что и **v · C** в разделе [Обрезка в области просмотра](#clipping-in-view-space) .</span><span class="sxs-lookup"><span data-stu-id="d7b56-185">Here we want to create a clip space clip plane whose dot product with our clip space vertex gives us the same value as **v · C** in the [Clipping in view space](#clipping-in-view-space) section.</span></span>

![плоскость обрезки](images/clip-space-clip-plane.png)

<span data-ttu-id="d7b56-187">**версия** · **C**  =  **v P** · **C**<sub>P</sub></span><span class="sxs-lookup"><span data-stu-id="d7b56-187">**v** · **C** = **v P** · **C**<sub>P</sub></span></span>

<span data-ttu-id="d7b56-188">*v* ₓ *c* ₓ +*v*<sub>y</sub>*c*<sub>y</sub>  +  *v*<sub>z</sub>*c*<sub>z</sub>  +  *c*<sub>w</sub>  =  *v* ₓ *P* ₓ *c*<sub>p ₓ</sub>  + *v*<sub>y</sub>*p*<sub>y</sub>*c*<sub>p <sub>y</sub></sub>  +  *v*<sub>z</sub>*A*<sub>y</sub>*c*<sub>p <sub>z</sub></sub>  +  *BC*<sub>p <sub>z</sub></sub>  +  *v*<sub>z</sub>*c*<sub>p <sub>w</sub></sub></span><span class="sxs-lookup"><span data-stu-id="d7b56-188">*v* ₓ *C* ₓ +*v*<sub>y</sub>*C*<sub>y</sub> + *v*<sub>z</sub>*C*<sub>z</sub> + *C*<sub>w</sub> = *v* ₓ *P* ₓ *C*<sub>Pₓ</sub> +*v*<sub>y</sub>*P*<sub>y</sub>*C*<sub>P <sub>y</sub></sub> + *v*<sub>z</sub>*A*<sub>y</sub>*C*<sub>P <sub>z</sub></sub> + *BC*<sub>P <sub>z</sub></sub> + *v*<sub>z</sub>*C*<sub>P<sub>w</sub></sub></span></span>

<span data-ttu-id="d7b56-189">Теперь можно прервать предыдущую математическую операцию вверх по компоненту вершины в четыре отдельных уравнения:</span><span class="sxs-lookup"><span data-stu-id="d7b56-189">Now we can break the preceding math operation up by vertex component into four separate equations:</span></span>

![компонент x вершины для продукта плоскости Clip](images/clip-space-clip-plane-equ1.png)

![Координата y для продукта плоскости Clip](images/clip-space-clip-plane-equ2.png)

![компонент вершины с вершиной продукта для плоскости Clip](images/clip-space-clip-plane-equ3.png)

![компонент координат z для продукта плоскости Clip](images/clip-space-clip-plane-equ4.png)

<span data-ttu-id="d7b56-194">Наша плоскость для просмотра и матрица проекции являются производными и дают нам нашу область клипов.</span><span class="sxs-lookup"><span data-stu-id="d7b56-194">Our view space clip plane and our projection matrix derive and give us our clip space clip plane.</span></span>

![плоскость обрезки области обрезки](images/clip-space-clip-plane-matrix.png)

## <a name="related-topics"></a><span data-ttu-id="d7b56-196">См. также</span><span class="sxs-lookup"><span data-stu-id="d7b56-196">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d7b56-197">Руководство по программированию для HLSL</span><span class="sxs-lookup"><span data-stu-id="d7b56-197">Programming Guide for HLSL</span></span>](dx-graphics-hlsl-pguide.md)
</dt> <dt>

[<span data-ttu-id="d7b56-198">Синтаксис объявления функций</span><span class="sxs-lookup"><span data-stu-id="d7b56-198">Function Declaration Syntax</span></span>](dx-graphics-hlsl-function-syntax.md)
</dt> </dl>

 

 