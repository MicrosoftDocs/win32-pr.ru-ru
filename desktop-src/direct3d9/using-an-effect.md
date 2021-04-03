---
description: На этой странице будет показано, как создать и использовать результат.
ms.assetid: d9fdafed-5958-4995-a1b5-8881feca1291
title: Использование влияния (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1170fde625e5eee5e9665f0759d302b5f5450a41
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104140702"
---
# <a name="using-an-effect-direct3d-9"></a><span data-ttu-id="30504-103">Использование влияния (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="30504-103">Using an Effect (Direct3D 9)</span></span>

<span data-ttu-id="30504-104">На этой странице будет показано, как создать и использовать результат.</span><span class="sxs-lookup"><span data-stu-id="30504-104">This page will show you how to generate and use an effect.</span></span> <span data-ttu-id="30504-105">В этом разделе рассматриваются следующие темы:</span><span class="sxs-lookup"><span data-stu-id="30504-105">The topics covered include how to:</span></span>

-   [<span data-ttu-id="30504-106">Создание результата</span><span class="sxs-lookup"><span data-stu-id="30504-106">Create an Effect</span></span>](#create-an-effect)
-   [<span data-ttu-id="30504-107">Отрисовка результата</span><span class="sxs-lookup"><span data-stu-id="30504-107">Render an Effect</span></span>](#render-an-effect)
-   [<span data-ttu-id="30504-108">Использование семантики для поиска параметров эффектов</span><span class="sxs-lookup"><span data-stu-id="30504-108">Use Semantics to Find Effect Parameters</span></span>](#use-semantics-to-find-effect-parameters)
-   [<span data-ttu-id="30504-109">Использование дескрипторов для эффективного получения и задания параметров</span><span class="sxs-lookup"><span data-stu-id="30504-109">Use Handles to Get and Set Parameters Efficiently</span></span>](#use-handles-to-get-and-set-parameters-efficiently)
-   [<span data-ttu-id="30504-110">Добавление сведений о параметрах с заметками</span><span class="sxs-lookup"><span data-stu-id="30504-110">Add Parameter Information with Annotations</span></span>](#add-parameter-information-with-annotations)
-   [<span data-ttu-id="30504-111">Общие параметры эффектов</span><span class="sxs-lookup"><span data-stu-id="30504-111">Share Effect Parameters</span></span>](#share-effect-parameters)
-   [<span data-ttu-id="30504-112">Компиляция влияния в автономный режим</span><span class="sxs-lookup"><span data-stu-id="30504-112">Compile an Effect Offline</span></span>](#compile-an-effect-offline)
-   [<span data-ttu-id="30504-113">Повышение производительности с помощью предтеней</span><span class="sxs-lookup"><span data-stu-id="30504-113">Improve Performance with Preshaders</span></span>](#improve-performance-with-preshaders)
-   [<span data-ttu-id="30504-114">Использование блоков параметров для управления параметрами эффектов</span><span class="sxs-lookup"><span data-stu-id="30504-114">Use Parameter Blocks to Manage Effect Parameters</span></span>](#use-parameter-blocks-to-manage-effect-parameters)

## <a name="create-an-effect"></a><span data-ttu-id="30504-115">Создание результата</span><span class="sxs-lookup"><span data-stu-id="30504-115">Create an Effect</span></span>

<span data-ttu-id="30504-116">Ниже приведен пример создания действия, взятого из [примера басичлсл](../directx-sdk--august-2009-.md).</span><span class="sxs-lookup"><span data-stu-id="30504-116">Here is an example of creating an effect taken from the [BasicHLSL Sample](../directx-sdk--august-2009-.md).</span></span> <span data-ttu-id="30504-117">Код создания результатов для создания шейдера отладки — из **онкреатедевице**:</span><span class="sxs-lookup"><span data-stu-id="30504-117">The effect creation code for creating a debug shader is from **OnCreateDevice**:</span></span>


```
ID3DXEffect* g_pEffect = NULL;
DWORD dwShaderFlags = 0;

    dwShaderFlags |= D3DXSHADER_FORCE_VS_SOFTWARE_NOOPT;
    dwShaderFlags |= D3DXSHADER_FORCE_PS_SOFTWARE_NOOPT;
    dwShaderFlags |= D3DXSHADER_NO_PRESHADER;

    // Read the D3DX effect file
    WCHAR str[MAX_PATH];
    DXUTFindDXSDKMediaFileCch( str, MAX_PATH, L"BasicHLSL.fx" );

    D3DXCreateEffectFromFile( 
        pd3dDevice, 
        str, 
        NULL, // CONST D3DXMACRO* pDefines,
        NULL, // LPD3DXINCLUDE pInclude,
        dwShaderFlags, 
        NULL, // LPD3DXEFFECTPOOL pPool,
        &g_pEffect, 
        NULL );
```



<span data-ttu-id="30504-118">Эта функция принимает следующие аргументы:</span><span class="sxs-lookup"><span data-stu-id="30504-118">This function takes these arguments:</span></span>

-   <span data-ttu-id="30504-119">Устройство.</span><span class="sxs-lookup"><span data-stu-id="30504-119">The device.</span></span>
-   <span data-ttu-id="30504-120">Имя файла действия.</span><span class="sxs-lookup"><span data-stu-id="30504-120">The file name of the effect file.</span></span>
-   <span data-ttu-id="30504-121">Указатель на список определений, заканчивающийся НУЛЕМ \# , для использования при синтаксическом анализе шейдера.</span><span class="sxs-lookup"><span data-stu-id="30504-121">A pointer to a NULL-terminated list of \#defines, to be used while parsing the shader.</span></span>
-   <span data-ttu-id="30504-122">Необязательный указатель на обработчик include, написанный пользователем.</span><span class="sxs-lookup"><span data-stu-id="30504-122">An optional pointer to a user-written include handler.</span></span> <span data-ttu-id="30504-123">Обработчик вызывается процессором каждый раз, когда ему требуется разрешить \# Включение.</span><span class="sxs-lookup"><span data-stu-id="30504-123">The handler is called by the processor whenever it needs to resolve a \#include.</span></span>
-   <span data-ttu-id="30504-124">Флаг компиляции шейдера, который предоставляет указания компилятора о том, как будет использоваться шейдер.</span><span class="sxs-lookup"><span data-stu-id="30504-124">A shader compile flag that gives the compiler hints about how the shader will be used.</span></span> <span data-ttu-id="30504-125">Эти способы могут быть следующими:</span><span class="sxs-lookup"><span data-stu-id="30504-125">The options include:</span></span>
    -   <span data-ttu-id="30504-126">Пропуск проверки, если компилируются известные хорошие шейдеры.</span><span class="sxs-lookup"><span data-stu-id="30504-126">Skipping validation, if known good shaders are being compiled.</span></span>
    -   <span data-ttu-id="30504-127">Пропуск оптимизации (иногда используется, когда оптимизация усложняет отладку).</span><span class="sxs-lookup"><span data-stu-id="30504-127">Skipping optimization (sometimes used when optimizations make debugging harder).</span></span>
    -   <span data-ttu-id="30504-128">Запрос сведений об отладке для включения в шейдер, чтобы их можно было отлаживать.</span><span class="sxs-lookup"><span data-stu-id="30504-128">Requesting debug information to be included in the shader so it can be debugged.</span></span>
-   <span data-ttu-id="30504-129">Пул эффектов.</span><span class="sxs-lookup"><span data-stu-id="30504-129">The effect pool.</span></span> <span data-ttu-id="30504-130">Если один и тот же указатель пула памяти используется несколькими эффектами, то глобальные переменные в эффектах совместно используются друг с другом.</span><span class="sxs-lookup"><span data-stu-id="30504-130">If more than one effect uses the same memory pool pointer, the global variables in the effects are shared with each other.</span></span> <span data-ttu-id="30504-131">Если нет необходимости совместно использовать переменные влияния, пул памяти может иметь значение **null**.</span><span class="sxs-lookup"><span data-stu-id="30504-131">If there is no need to share effect variables, the memory pool can be set to **NULL**.</span></span>
-   <span data-ttu-id="30504-132">Указатель на новый результат.</span><span class="sxs-lookup"><span data-stu-id="30504-132">A pointer to the new effect.</span></span>
-   <span data-ttu-id="30504-133">Указатель на буфер, в который могут отправляться ошибки проверки.</span><span class="sxs-lookup"><span data-stu-id="30504-133">A pointer to a buffer to which validation errors can be sent.</span></span> <span data-ttu-id="30504-134">В этом примере параметр был установлен в **значение NULL** и не используется.</span><span class="sxs-lookup"><span data-stu-id="30504-134">In this example, the parameter was set to **NULL** and not used.</span></span>

> [!Note]  
> <span data-ttu-id="30504-135">Начиная с пакета SDK 2006 декабря, компилятор HLSL DirectX 10 теперь является компилятором по умолчанию как в DirectX 9, так и в DirectX 10.</span><span class="sxs-lookup"><span data-stu-id="30504-135">Beginning with the December 2006 SDK, the DirectX 10 HLSL compiler is now the default compiler in both DirectX 9 and DirectX 10.</span></span> <span data-ttu-id="30504-136">Дополнительные сведения см. в разделе [средство компилятора Effect](../direct3dtools/fxc.md) .</span><span class="sxs-lookup"><span data-stu-id="30504-136">See [Effect-Compiler Tool](../direct3dtools/fxc.md) for details.</span></span>

 

## <a name="render-an-effect"></a><span data-ttu-id="30504-137">Отрисовка результата</span><span class="sxs-lookup"><span data-stu-id="30504-137">Render an Effect</span></span>

<span data-ttu-id="30504-138">Последовательность вызовов для применения состояния эффектов к устройству:</span><span class="sxs-lookup"><span data-stu-id="30504-138">The sequence of calls for applying effect state to a device is:</span></span>

-   <span data-ttu-id="30504-139">[**ID3DXEffect:: Begin**](id3dxeffect--begin.md) задает активный метод.</span><span class="sxs-lookup"><span data-stu-id="30504-139">[**ID3DXEffect::Begin**](id3dxeffect--begin.md) sets the active technique.</span></span>
-   <span data-ttu-id="30504-140">[**ID3DXEffect:: бегинпасс**](id3dxeffect--beginpass.md) задает активный проход.</span><span class="sxs-lookup"><span data-stu-id="30504-140">[**ID3DXEffect::BeginPass**](id3dxeffect--beginpass.md) sets the active pass.</span></span>
-   <span data-ttu-id="30504-141">[**ID3DXEffect:: CommitChanges**](id3dxeffect--commitchanges.md) обновляет изменения любых вызовов набора в ходе передачи.</span><span class="sxs-lookup"><span data-stu-id="30504-141">[**ID3DXEffect::CommitChanges**](id3dxeffect--commitchanges.md) updates changes to any set calls in the pass.</span></span> <span data-ttu-id="30504-142">Он должен вызываться перед любым вызовом Draw.</span><span class="sxs-lookup"><span data-stu-id="30504-142">This should be called before any draw call.</span></span>
-   <span data-ttu-id="30504-143">[**ID3DXEffect:: ендпасс**](id3dxeffect--endpass.md) завершает проход.</span><span class="sxs-lookup"><span data-stu-id="30504-143">[**ID3DXEffect::EndPass**](id3dxeffect--endpass.md) ends a pass.</span></span>
-   <span data-ttu-id="30504-144">[**ID3DXEffect:: end**](id3dxeffect--end.md) завершает активный метод.</span><span class="sxs-lookup"><span data-stu-id="30504-144">[**ID3DXEffect::End**](id3dxeffect--end.md) ends the active technique.</span></span>

<span data-ttu-id="30504-145">Код рендеринга эффектов также проще, чем соответствующий код отрисовки без влияния.</span><span class="sxs-lookup"><span data-stu-id="30504-145">Effect render code is also simpler than the corresponding render code without an effect.</span></span> <span data-ttu-id="30504-146">Вот как выглядит код отрисовки:</span><span class="sxs-lookup"><span data-stu-id="30504-146">Here's the render code with an effect:</span></span>


```
// Apply the technique contained in the effect 
g_pEffect->Begin(&cPasses, 0);

for (iPass = 0; iPass < cPasses; iPass++)
{
    g_pEffect->BeginPass(iPass);

    // Only call CommitChanges if any state changes have happened
    // after BeginPass is called
    g_pEffect->CommitChanges();

    // Render the mesh with the applied technique
    g_pMesh->DrawSubset(0);

    g_pEffect->EndPass();
}
g_pEffect->End();
```



<span data-ttu-id="30504-147">Цикл рендеринга состоит из запроса к результату, чтобы увидеть, сколько их содержит, а затем вызывает все проходы для приемки.</span><span class="sxs-lookup"><span data-stu-id="30504-147">The render loop consists of querying the effect to see how many passes it contains, and then calling all the passes for a technique.</span></span> <span data-ttu-id="30504-148">Цикл рендеринга можно расширить для вызова нескольких методов, каждый из которых имеет несколько проходов.</span><span class="sxs-lookup"><span data-stu-id="30504-148">The render loop could be expanded to call multiple techniques, each with multiple passes.</span></span>

## <a name="use-semantics-to-find-effect-parameters"></a><span data-ttu-id="30504-149">Использование семантики для поиска параметров эффектов</span><span class="sxs-lookup"><span data-stu-id="30504-149">Use Semantics to Find Effect Parameters</span></span>

<span data-ttu-id="30504-150">Семантика — это идентификатор, прикрепленный к параметру Effect, позволяющий приложению искать параметр.</span><span class="sxs-lookup"><span data-stu-id="30504-150">A semantic is an identifier that is attached to an effect parameter to allow an application to search for the parameter.</span></span> <span data-ttu-id="30504-151">Параметр может иметь не более одной семантики.</span><span class="sxs-lookup"><span data-stu-id="30504-151">A parameter can have at most one semantic.</span></span> <span data-ttu-id="30504-152">Семантика находится после двоеточия (:) после имени параметра.</span><span class="sxs-lookup"><span data-stu-id="30504-152">The semantic is located following a colon (:) after the parameter name.</span></span> <span data-ttu-id="30504-153">Например:</span><span class="sxs-lookup"><span data-stu-id="30504-153">For instance:</span></span>


```
float4x4 matWorldViewProj : WORLDVIEWPROJ;
```



<span data-ttu-id="30504-154">Если вы объявили глобальную переменную Effect без использования семантической семантики, она будет выглядеть следующим образом:</span><span class="sxs-lookup"><span data-stu-id="30504-154">If you declared the effect global variable without using a semantic, it would look like this instead:</span></span>


```
float4x4 matWorldViewProj;
```



<span data-ttu-id="30504-155">Интерфейс Effect может использовать семантику для получения маркера для конкретного параметра effect.</span><span class="sxs-lookup"><span data-stu-id="30504-155">The effect interface can use a semantic to get a handle to a particular effect parameter.</span></span> <span data-ttu-id="30504-156">Например, следующий метод возвращает маркер матрицы:</span><span class="sxs-lookup"><span data-stu-id="30504-156">For instance, the following returns the handle of the matrix:</span></span>


```
D3DHANDLE handle = 
    m_pEffect->GetParameterBySemantic(NULL, "WORLDVIEWPROJ");
```



<span data-ttu-id="30504-157">Помимо поиска по семантическому имени, интерфейс Effect имеет много других методов для поиска параметров.</span><span class="sxs-lookup"><span data-stu-id="30504-157">In addition to searching by semantic name, the effect interface has many other methods to search for parameters.</span></span>

## <a name="use-handles-to-get-and-set-parameters-efficiently"></a><span data-ttu-id="30504-158">Использование дескрипторов для эффективного получения и задания параметров</span><span class="sxs-lookup"><span data-stu-id="30504-158">Use Handles to Get and Set Parameters Efficiently</span></span>

<span data-ttu-id="30504-159">Дескрипторы предоставляют эффективные средства для создания ссылок на параметры, методы, проходы и аннотации с применением эффектов.</span><span class="sxs-lookup"><span data-stu-id="30504-159">Handles provide an efficient means for referencing effect parameters, techniques, passes, and annotations with an effect.</span></span> <span data-ttu-id="30504-160">Дескрипторы (которые имеют тип D3DXHANDLE) являются строковыми указателями.</span><span class="sxs-lookup"><span data-stu-id="30504-160">Handles (which are of type D3DXHANDLE) are string pointers.</span></span> <span data-ttu-id="30504-161">Дескрипторы, передаваемые в функции, такие как Жетпараметеркскскс или Жетаннотатионкскскс, могут быть представлены в одной из трех форм:</span><span class="sxs-lookup"><span data-stu-id="30504-161">The handles that are passed into functions such as GetParameterxxx or GetAnnotationxxx can be in one of three forms:</span></span>

-   <span data-ttu-id="30504-162">Маркер, возвращаемый функцией, например Жетпараметеркскскс.</span><span class="sxs-lookup"><span data-stu-id="30504-162">A handle returned by a function such as GetParameterxxx.</span></span>
-   <span data-ttu-id="30504-163">Строка, содержащая имя параметра, метода, прохода или заметки.</span><span class="sxs-lookup"><span data-stu-id="30504-163">A string containing the name of the parameter, technique, pass, or annotation.</span></span>
-   <span data-ttu-id="30504-164">**Значение параметра handle.**</span><span class="sxs-lookup"><span data-stu-id="30504-164">A handle set to **NULL**.</span></span>

<span data-ttu-id="30504-165">В этом примере возвращается маркер для параметра, к которому прикреплена семантика ВОРЛДВИЕВПРОЖ:</span><span class="sxs-lookup"><span data-stu-id="30504-165">This example returns a handle to the parameter that has the WORLDVIEWPROJ semantic attached to it:</span></span>


```
D3DHANDLE handle = 
    m_pEffect->GetParameterBySemantic(NULL, "WORLDVIEWPROJ");
```



## <a name="add-parameter-information-with-annotations"></a><span data-ttu-id="30504-166">Добавление сведений о параметрах с заметками</span><span class="sxs-lookup"><span data-stu-id="30504-166">Add Parameter Information with Annotations</span></span>

<span data-ttu-id="30504-167">Заметки представляют собой определяемые пользователем данные, которые могут быть присоединены к любому методу, параметру Pass или.</span><span class="sxs-lookup"><span data-stu-id="30504-167">Annotations are user-specific data that can be attached to any technique, pass, or parameter.</span></span> <span data-ttu-id="30504-168">Заметка — это гибкий способ добавления сведений к отдельным параметрам.</span><span class="sxs-lookup"><span data-stu-id="30504-168">An annotation is a flexible way to add information to individual parameters.</span></span> <span data-ttu-id="30504-169">Эти сведения можно считать и использовать любым способом, выбранным приложением.</span><span class="sxs-lookup"><span data-stu-id="30504-169">The information can be read back and used any way the application chooses.</span></span> <span data-ttu-id="30504-170">Аннотация может иметь любой тип данных и может быть динамически добавлена.</span><span class="sxs-lookup"><span data-stu-id="30504-170">An annotation can be of any data type and can be added dynamically.</span></span> <span data-ttu-id="30504-171">Объявления заметок разделяются угловыми скобками.</span><span class="sxs-lookup"><span data-stu-id="30504-171">Annotation declarations are delimited by angle brackets.</span></span> <span data-ttu-id="30504-172">Аннотация содержит:</span><span class="sxs-lookup"><span data-stu-id="30504-172">An annotation contains:</span></span>

-   <span data-ttu-id="30504-173">Тип данных.</span><span class="sxs-lookup"><span data-stu-id="30504-173">A data type.</span></span>
-   <span data-ttu-id="30504-174">Имя переменной.</span><span class="sxs-lookup"><span data-stu-id="30504-174">A variable name.</span></span>
-   <span data-ttu-id="30504-175">Знак равенства (=).</span><span class="sxs-lookup"><span data-stu-id="30504-175">An equals sign (=).</span></span>
-   <span data-ttu-id="30504-176">Значение данных.</span><span class="sxs-lookup"><span data-stu-id="30504-176">The data value.</span></span>
-   <span data-ttu-id="30504-177">Конечная точка с запятой (;).</span><span class="sxs-lookup"><span data-stu-id="30504-177">A ending semicolon (;).</span></span>

<span data-ttu-id="30504-178">Например, оба приведенных выше примера в этом документе содержат следующую аннотацию:</span><span class="sxs-lookup"><span data-stu-id="30504-178">For instance, both of the previous examples in this paper contain this annotation:</span></span>


```
texture Tex0 < string name = "tiger.bmp"; >;
```



<span data-ttu-id="30504-179">Заметка присоединена к объекту текстуры и задает файл текстуры, который должен использоваться для инициализации объекта текстуры.</span><span class="sxs-lookup"><span data-stu-id="30504-179">The annotation is attached to the texture object and specifies the texture file that should be used to initialize the texture object.</span></span> <span data-ttu-id="30504-180">Заметка не инициализирует объект текстуры, это просто часть сведений о пользователе, которая присоединяется к переменной.</span><span class="sxs-lookup"><span data-stu-id="30504-180">The annotation does not initialize the texture object, it is simply a piece of user information that is attached to the variable.</span></span> <span data-ttu-id="30504-181">Приложение может прочитать заметку с помощью [**ID3DXBaseEffect::**](id3dxbaseeffect--getannotation.md) GetString или [**ID3DXBaseEffect:: жетаннотатионбинаме**](id3dxbaseeffect--getannotationbyname.md) , чтобы получить строку.</span><span class="sxs-lookup"><span data-stu-id="30504-181">An application can read the annotation with either [**ID3DXBaseEffect::GetAnnotation**](id3dxbaseeffect--getannotation.md) or [**ID3DXBaseEffect::GetAnnotationByName**](id3dxbaseeffect--getannotationbyname.md) to return the string.</span></span> <span data-ttu-id="30504-182">Заметки также могут добавляться приложением.</span><span class="sxs-lookup"><span data-stu-id="30504-182">Annotations can also be added by the application.</span></span>

<span data-ttu-id="30504-183">Каждая аннотация:</span><span class="sxs-lookup"><span data-stu-id="30504-183">Each annotation:</span></span>

-   <span data-ttu-id="30504-184">Должен быть либо числовым, либо строкой.</span><span class="sxs-lookup"><span data-stu-id="30504-184">Must be either numeric or strings.</span></span>
-   <span data-ttu-id="30504-185">Всегда должно быть инициализировано значением по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="30504-185">Must always be initialized with a default value.</span></span>
-   <span data-ttu-id="30504-186">Может быть связан с [методами и передается (Direct3D 9)](techniques-and-passes.md) и [параметрами эффектов](/previous-versions/windows/desktop/ee417539(v=vs.85))верхнего уровня.</span><span class="sxs-lookup"><span data-stu-id="30504-186">Can be associated with [Techniques and Passes (Direct3D 9)](techniques-and-passes.md) and top-level [Effect Parameters](/previous-versions/windows/desktop/ee417539(v=vs.85)).</span></span>
-   <span data-ttu-id="30504-187">Можно записывать и считывать с помощью [**ID3DXEffect**](id3dxeffect.md) или [**ID3DXEffectCompiler**](id3dxeffectcompiler.md).</span><span class="sxs-lookup"><span data-stu-id="30504-187">Can be written to and read from with either [**ID3DXEffect**](id3dxeffect.md) or [**ID3DXEffectCompiler**](id3dxeffectcompiler.md).</span></span>
-   <span data-ttu-id="30504-188">Можно добавить с помощью [**ID3DXEffect**](id3dxeffect.md).</span><span class="sxs-lookup"><span data-stu-id="30504-188">Can be added with [**ID3DXEffect**](id3dxeffect.md).</span></span>
-   <span data-ttu-id="30504-189">Не может ссылаться внутри этого результата.</span><span class="sxs-lookup"><span data-stu-id="30504-189">Cannot be referenced inside the effect.</span></span>
-   <span data-ttu-id="30504-190">Не может иметь подсемантику или поданнотации.</span><span class="sxs-lookup"><span data-stu-id="30504-190">Cannot have sub-semantics or sub-annotations.</span></span>

## <a name="share-effect-parameters"></a><span data-ttu-id="30504-191">Общие параметры эффектов</span><span class="sxs-lookup"><span data-stu-id="30504-191">Share Effect Parameters</span></span>

<span data-ttu-id="30504-192">Параметры эффектов — это все нестатические переменные, объявленные в результате.</span><span class="sxs-lookup"><span data-stu-id="30504-192">Effect parameters are all the non-static variables declared in an effect.</span></span> <span data-ttu-id="30504-193">Это могут быть глобальные переменные и заметки.</span><span class="sxs-lookup"><span data-stu-id="30504-193">This can include global variables and annotations.</span></span> <span data-ttu-id="30504-194">Параметры эффектов могут совместно использоваться различными эффектами путем объявления параметров с ключевым словом "Shared" и последующего создания эффекта с пулом эффектов.</span><span class="sxs-lookup"><span data-stu-id="30504-194">Effect parameters can be shared between different effects by declaring parameters with the "shared" keyword and then creating the effect with an effect pool.</span></span>

<span data-ttu-id="30504-195">Пул эффектов содержит общие параметры эффектов.</span><span class="sxs-lookup"><span data-stu-id="30504-195">An effect pool contains shared effect parameters.</span></span> <span data-ttu-id="30504-196">Пул создается путем вызова [**D3DXCreateEffectPool**](d3dxcreateeffectpool.md), который возвращает интерфейс [**ID3DXEffectPool**](id3dxeffectpool.md) .</span><span class="sxs-lookup"><span data-stu-id="30504-196">The pool is created by calling [**D3DXCreateEffectPool**](d3dxcreateeffectpool.md), which returns an [**ID3DXEffectPool**](id3dxeffectpool.md) interface.</span></span> <span data-ttu-id="30504-197">Интерфейс может быть указан в качестве входных данных для любой функции D3DXCreateEffectxxx при создании результата.</span><span class="sxs-lookup"><span data-stu-id="30504-197">The interface can be supplied as an input to any of the D3DXCreateEffectxxx functions when an effect is created.</span></span> <span data-ttu-id="30504-198">Чтобы параметр был совместно использоваться несколькими эффектами, параметр должен иметь одинаковое имя, тип и семантику в каждом из общих эффектов.</span><span class="sxs-lookup"><span data-stu-id="30504-198">For a parameter to be shared across multiple effects, the parameter must have the same name, type, and semantic in each of the shared effects.</span></span>


```
ID3DXEffectPool* g_pEffectPool = NULL;   // Effect pool for sharing parameters

    D3DXCreateEffectPool( &g_pEffectPool );
```



<span data-ttu-id="30504-199">Эффекты, которые совместно используют параметры, должны использовать одно и то же устройство.</span><span class="sxs-lookup"><span data-stu-id="30504-199">Effects that share parameters must use the same device.</span></span> <span data-ttu-id="30504-200">Это применяется для предотвращения совместного использования зависимых от устройства параметров (таких как шейдеры или текстуры) на разных устройствах.</span><span class="sxs-lookup"><span data-stu-id="30504-200">This is enforced to prevent the sharing of device-dependent parameters (such as shaders or textures) across different devices.</span></span> <span data-ttu-id="30504-201">Параметры удаляются из пула при выпуске эффектов, содержащих общие параметры.</span><span class="sxs-lookup"><span data-stu-id="30504-201">Parameters are deleted from the pool whenever the effects that contain the shared parameters are released.</span></span> <span data-ttu-id="30504-202">Если общий доступ к параметрам не требуется, при создании результата укажите **значение NULL** для пула эффектов.</span><span class="sxs-lookup"><span data-stu-id="30504-202">If sharing parameters is not necessary, supply **NULL** for the effect pool when an effect is created.</span></span>

<span data-ttu-id="30504-203">Клонированные эффекты используют тот же пул эффектов, что и результат клонирования.</span><span class="sxs-lookup"><span data-stu-id="30504-203">Cloned effects use the same effect pool as the effect from which they are cloned.</span></span> <span data-ttu-id="30504-204">При клонировании действия создается точная копия результата, включая глобальные переменные, методы, проходы и заметки.</span><span class="sxs-lookup"><span data-stu-id="30504-204">Cloning an effect makes an exact copy of an effect, including global variables, techniques, passes, and annotations.</span></span>

## <a name="compile-an-effect-offline"></a><span data-ttu-id="30504-205">Компиляция влияния в автономный режим</span><span class="sxs-lookup"><span data-stu-id="30504-205">Compile an Effect Offline</span></span>

<span data-ttu-id="30504-206">Вы можете компилировать эффекты во время выполнения с помощью [**D3DXCreateEffect**](d3dxcreateeffect.md), а также компилировать эффекты в автономном режиме, используя средство компилятора командной строки fxc.exe.</span><span class="sxs-lookup"><span data-stu-id="30504-206">You can compile an effect at run time with [**D3DXCreateEffect**](d3dxcreateeffect.md), or you can compile an effect offline using the command-line compiler tool fxc.exe.</span></span> <span data-ttu-id="30504-207">Результат в [примере компиледеффект](https://msdn.microsoft.com/library/Ee416326(v=VS.85).aspx) содержит Вершинный шейдер, шейдер пикселей и один прием:</span><span class="sxs-lookup"><span data-stu-id="30504-207">The effect in the [CompiledEffect Sample](https://msdn.microsoft.com/library/Ee416326(v=VS.85).aspx) contains a vertex shader, a pixel shader, and one technique:</span></span>


```
// File: CompiledEffect.fx

// Global variables
float4 g_MaterialAmbientColor;    // Material's ambient color
...

// Texture samplers
sampler RenderTargetSampler = 
   ...

// Type: Vertex shader                                      
VS_OUTPUT RenderSceneVS( float4 vPos : POSITION, 
                         float3 vNormal : NORMAL,
                         float2 vTexCoord0 : TEXCOORD0 )
{
   ...
};
// Type: Pixel shader
PS_OUTPUT RenderScenePS( VS_OUTPUT In ) 
{ 
   ...
}

// Type: Technique                                     
technique RenderScene
{
    pass P0
    {          
        ZENABLE = true;
        VertexShader = compile vs_1_1 RenderSceneVS();
        PixelShader  = compile ps_1_1 RenderScenePS();
    }
}
```



<span data-ttu-id="30504-208">Использование [средства компилятора Effect](../direct3dtools/fxc.md) для компиляции шейдера для VS 1 \_ \_ 1 создало следующие инструкции шейдера сборки:</span><span class="sxs-lookup"><span data-stu-id="30504-208">Using [Effect-Compiler Tool](../direct3dtools/fxc.md) to compile the shader for vs\_1\_1 generated the following assembly shader instructions:</span></span>


```
//
// Generated by Microsoft (R) D3DX9 Shader Compiler 4.09.02.1188
//
//   fxc /T vs_1_1 /E RenderSceneVS /Fc CompiledEffect.txt CompiledEffect.fx
//
//
// Parameters:
//
//   float4 g_LightAmbient;
//   float4 g_LightDiffuse;
//   float3 g_LightDir;
//   float4 g_MaterialAmbientColor;
//   float4 g_MaterialDiffuseColor;
//   float g_fTime;
//   float4x4 g_mWorld;
//   float4x4 g_mWorldViewProjection;
//
//
// Registers:
//
//   Name                   Reg   Size
//   ---------------------- ----- ----
//   g_mWorldViewProjection c0       4
//   g_mWorld               c4       3
//   g_MaterialAmbientColor c7       1
//   g_MaterialDiffuseColor c8       1
//   g_LightDir             c9       1
//   g_LightAmbient         c10      1
//   g_LightDiffuse         c11      1
//   g_fTime                c12      1
//
//
// Default values:
//
//   g_LightDir
//     c9   = { 0.57735, 0.57735, 0.57735, 0 };
//
//   g_LightAmbient
//     c10  = { 1, 1, 1, 1 };
//
//   g_LightDiffuse
//     c11  = { 1, 1, 1, 1 };
//

    vs_1_1
    def c13, 0.159154937, 0.25, 6.28318548, -3.14159274
    def c14, -2.52398507e-007, 2.47609005e-005, -0.00138883968, 0.0416666418
    def c15, -0.5, 1, 0.5, 0
    dcl_position v0
    dcl_normal v1
    dcl_texcoord v2
    mov r0.w, c12.x
    mad r0.w, r0.w, c13.x, c13.y
    expp r3.y, r0.w
    mov r0.w, r3.y
    mad r0.w, r0.w, c13.z, c13.w
    mul r0.w, r0.w, r0.w
    mad r1.w, r0.w, c14.x, c14.y
    mad r1.w, r0.w, r1.w, c14.z
    mad r1.w, r0.w, r1.w, c14.w
    mad r1.w, r0.w, r1.w, c15.x
    mad r0.w, r0.w, r1.w, c15.y
    mul r0.w, r0.w, v0.x
    mul r0.x, r0.w, c15.z
    dp3 r1.x, v1, c4
    dp3 r1.y, v1, c5
    dp3 r1.z, v1, c6
    mov r0.yzw, c15.w
    dp3 r2.x, r1, r1
    add r0, r0, v0
    rsq r1.w, r2.x
    dp4 oPos.x, r0, c0
    mul r1.xyz, r1, r1.w
    dp4 oPos.y, r0, c1
    dp3 r1.x, r1, c9
    dp4 oPos.z, r0, c2
    max r1.w, r1.x, c15.w
    mov r1.xyz, c8
    mul r1.xyz, r1, c11
    mov r2.xyz, c7
    mul r2.xyz, r2, c10
    dp4 oPos.w, r0, c3
    mad oD0.xyz, r1, r1.w, r2
    mov oD0.w, c15.y
    mov oT0.xy, v2

// approximately 34 instruction slots used
```



## <a name="improve-performance-with-preshaders"></a><span data-ttu-id="30504-209">Повышение производительности с помощью предтеней</span><span class="sxs-lookup"><span data-stu-id="30504-209">Improve Performance with Preshaders</span></span>

<span data-ttu-id="30504-210">Предварительный шейдер — это метод повышения эффективности шейдера путем предварительного вычисления выражений шейдеров констант.</span><span class="sxs-lookup"><span data-stu-id="30504-210">A preshader is a technique for increasing shader efficiency by pre-calculating constant shader expressions.</span></span> <span data-ttu-id="30504-211">Компилятор результатов автоматически извлекает вычисления шейдера из тела шейдера и выполняет их на ЦП до запуска шейдера.</span><span class="sxs-lookup"><span data-stu-id="30504-211">The effect compiler automatically pulls out shader computations from the body of a shader and executes them on the CPU prior to the shader running.</span></span> <span data-ttu-id="30504-212">Следовательно, предшейдеры работают только с эффектами.</span><span class="sxs-lookup"><span data-stu-id="30504-212">Consequently, preshaders only work with effects.</span></span> <span data-ttu-id="30504-213">Например, эти два выражения можно вычислить за пределами шейдера перед его запуском.</span><span class="sxs-lookup"><span data-stu-id="30504-213">For instance, these two expressions can be evaluated outside of the shader before it runs.</span></span>


```
mul(World,mul(View, Projection));
sin(time)
```



<span data-ttu-id="30504-214">Вычисления шейдеров, которые могут быть перемещены, связаны с равномерными параметрами; то есть вычисления не изменяются для каждой вершины или пикселя.</span><span class="sxs-lookup"><span data-stu-id="30504-214">Shader computations that can be moved are those associated with uniform parameters; that is, the computations do not change for each vertex or pixel.</span></span> <span data-ttu-id="30504-215">При использовании эффектов компилятор автоматически создает и выполняет предшейдер. нет флагов для включения.</span><span class="sxs-lookup"><span data-stu-id="30504-215">If you are using effects, the effect compiler automatically generates and runs a preshader for you; there are no flags to enable.</span></span> <span data-ttu-id="30504-216">Предшейдеры могут уменьшить количество инструкций на шейдер, а также сократить количество постоянных регистров, используемых шейдером.</span><span class="sxs-lookup"><span data-stu-id="30504-216">Preshaders can reduce the number of instructions per shader and can also reduce the number of constant registers a shader consumes.</span></span>

<span data-ttu-id="30504-217">Компилятор эффектов следует рассматривать как тип многопроцессорного компилятора, поскольку он компилирует код шейдера для двух типов процессоров: ЦП и GPU.</span><span class="sxs-lookup"><span data-stu-id="30504-217">Think of the effect compiler as a sort of multi-processor compiler because it compiles shader code for two types of processors: a CPU and a GPU.</span></span> <span data-ttu-id="30504-218">Кроме того, компилятор эффектов предназначен для перемещения кода из GPU в ЦП и, следовательно, для повышения производительности шейдера.</span><span class="sxs-lookup"><span data-stu-id="30504-218">In addition, the effect compiler is designed to move code from the GPU to the CPU and therefore improve shader performance.</span></span> <span data-ttu-id="30504-219">Это очень похоже на извлечение статического выражения из цикла.</span><span class="sxs-lookup"><span data-stu-id="30504-219">This is very similar to pulling a static expression out of a loop.</span></span> <span data-ttu-id="30504-220">Шейдер, который преобразует расположение из мира в пространство проекции и копирует координаты текстуры, будет выглядеть следующим образом в HLSL:</span><span class="sxs-lookup"><span data-stu-id="30504-220">A shader that transforms position from world space to projection space, and copies texture coordinates would look like this in HLSL:</span></span>


```
float4x4 g_mWorldViewProjection;    // World * View * Projection matrix
float4x4 g_mWorldInverse;           // Inverse World matrix
float3 g_LightDir;                  // Light direction in world space
float4 g_LightDiffuse;              // Diffuse color of the light

struct VS_OUTPUT
{
    float4 Position   : POSITION;   // vertex position 
    float2 TextureUV  : TEXCOORD0;  // vertex texture coords 
    float4 Diffuse    : COLOR0;     // vertex diffuse color
};

VS_OUTPUT RenderSceneVS( float4 vPos : POSITION, 
                         float3 vNormal : NORMAL,
                         float2 vTexCoord0 : TEXCOORD0)
{
    VS_OUTPUT Output;
    
    // Transform the position from object space to projection space
    Output.Position = mul(vPos, g_mWorldViewProjection);

    // Transform the light from world space to object space    
    float3 vLightObjectSpace = normalize(mul(g_LightDir, (float3x3)g_mWorldInverse)); 

    // N dot L lighting
    Output.Diffuse = max(0,dot(vNormal, vLightObjectSpace));
    
    // Copy the texture coordinate
    Output.TextureUV = vTexCoord0; 
    
    return Output;    
}
technique RenderVS
{
    pass P0
    {          
        VertexShader = compile vs_1_1 RenderSceneVS();
    }
}
```



<span data-ttu-id="30504-221">Использование [средства компилятора Effect](../direct3dtools/fxc.md) для компиляции шейдера для VS \_ 1 \_ 1 приводит к следующим инструкциям по сборке:</span><span class="sxs-lookup"><span data-stu-id="30504-221">Using [Effect-Compiler Tool](../direct3dtools/fxc.md) to compile the shader for vs\_1\_1 generates the following assembly instructions:</span></span>


```
technique RenderVS
{
    pass P0
    {
        vertexshader = 
            asm {
            //
            // Generated by Microsoft (R) D3DX9 Shader Compiler 9.15.779.0000
            //
            // Parameters:
            //
            //   float3 g_LightDir;
            //   float4x4 g_mWorldInverse;
            //   float4x4 g_mWorldViewProjection;
            //
            //
            // Registers:
            //
            //   Name                   Reg   Size
            //   ---------------------- ----- ----
            //   g_mWorldViewProjection c0       4
            //   g_mWorldInverse        c4       3
            //   g_LightDir             c7       1
            //
            
                vs_1_1
                def c8, 0, 0, 0, 0
                dcl_position v0
                dcl_normal v1
                dcl_texcoord v2
                mov r1.xyz, c7
                dp3 r0.x, r1, c4
                dp3 r0.y, r1, c5
                dp3 r0.z, r1, c6
                dp4 oPos.x, v0, c0
                dp3 r1.x, r0, r0
                dp4 oPos.y, v0, c1
                rsq r0.w, r1.x
                dp4 oPos.z, v0, c2
                mul r0.xyz, r0, r0.w
                dp4 oPos.w, v0, c3
                dp3 r0.x, v1, r0
                max oD0, r0.x, c8.x
                mov oT0.xy, v2
            
            // approximately 14 instruction slots used
            };

        //No embedded pixel shader
    }
}
```



<span data-ttu-id="30504-222">Это занимает около 14 слотов и использует 9 постоянных регистров.</span><span class="sxs-lookup"><span data-stu-id="30504-222">This uses up approximately 14 slots and consumes 9 constant registers.</span></span> <span data-ttu-id="30504-223">При использовании предшейдера компилятор перемещает статические выражения из шейдера и в предшейдер.</span><span class="sxs-lookup"><span data-stu-id="30504-223">With a preshader, the compiler moves the static expressions out of the shader and into the preshader.</span></span> <span data-ttu-id="30504-224">Один и тот же шейдер будет выглядеть следующим образом с помощью предшейдера:</span><span class="sxs-lookup"><span data-stu-id="30504-224">The same shader would look like this with a preshader:</span></span>


```
technique RenderVS
{
    pass P0
    {
        vertexshader = 
            asm {
            //
            // Generated by Microsoft (R) D3DX9 Shader Compiler 9.15.779.0000
            //
            // Parameters:
            //
            //   float3 g_LightDir;
            //   float4x4 g_mWorldInverse;
            //
            //
            // Registers:
            //
            //   Name            Reg   Size
            //   --------------- ----- ----
            //   g_mWorldInverse c0       3
            //   g_LightDir      c3       1
            //
            
                preshader
                dot r0.x, c3.xyz, c0.xyz
                dot r0.y, c3.xyz, c1.xyz
                dot r0.z, c3.xyz, c2.xyz
                dot r1.w, r0.xyz, r0.xyz
                rsq r0.w, r1.w
                mul c4.xyz, r0.w, r0.xyz
            
            // approximately 6 instructions used
            //
            // Generated by Microsoft (R) D3DX9 Shader Compiler 9.15.779.0000
            //
            // Parameters:
            //
            //   float4x4 g_mWorldViewProjection;
            //
            //
            // Registers:
            //
            //   Name                   Reg   Size
            //   ---------------------- ----- ----
            //   g_mWorldViewProjection c0       4
            //
            
                vs_1_1
                def c5, 0, 0, 0, 0
                dcl_position v0
                dcl_normal v1
                dcl_texcoord v2
                dp4 oPos.x, v0, c0
                dp4 oPos.y, v0, c1
                dp4 oPos.z, v0, c2
                dp4 oPos.w, v0, c3
                dp3 r0.x, v1, c4
                max oD0, r0.x, c5.x
                mov oT0.xy, v2
            
            // approximately 7 instruction slots used
            };

        //No embedded pixel shader
    }
}
```



<span data-ttu-id="30504-225">Перед выполнением шейдера он выполняет предварительный построитель.</span><span class="sxs-lookup"><span data-stu-id="30504-225">An effect executes a preshader just before executing a shader.</span></span> <span data-ttu-id="30504-226">Результат — это те же функциональные возможности, что и повышение производительности шейдера, поскольку было уменьшено количество инструкций, которые необходимо выполнить (для каждой вершины или пикселя в зависимости от типа шейдера).</span><span class="sxs-lookup"><span data-stu-id="30504-226">The result is the same functionality with increased shader performance because the number of instructions that need to be executed (for each vertex or pixel depending on the type of shader) has been reduced.</span></span> <span data-ttu-id="30504-227">Кроме того, шейдер использует меньше регистров констант в результате того, как статические выражения перемещаются в предшейдер.</span><span class="sxs-lookup"><span data-stu-id="30504-227">In addition, fewer constant registers are consumed by the shader as a result of the static expressions being moved to the preshader.</span></span> <span data-ttu-id="30504-228">Это означает, что шейдеры, ранее ограниченные количеством постоянных регистров, которые они требуют, теперь могут компилироваться, так как для них требуется меньше постоянных регистров.</span><span class="sxs-lookup"><span data-stu-id="30504-228">This means that shaders previously limited by the number of constant registers they required may now compile because they require fewer constant registers.</span></span> <span data-ttu-id="30504-229">Разумно рассчитывать на 5-процентный и 20-процентное улучшение производительности от предтеней.</span><span class="sxs-lookup"><span data-stu-id="30504-229">It is reasonable to expect a 5 percent and a 20 percent performance improvement from preshaders.</span></span>

<span data-ttu-id="30504-230">Помните, что входные константы отличаются от выходных констант в предшейдере.</span><span class="sxs-lookup"><span data-stu-id="30504-230">Keep in mind that the input constants are different from the output constants in a preshader.</span></span> <span data-ttu-id="30504-231">Выходные данные C1 не совпадают с входным регистром C1.</span><span class="sxs-lookup"><span data-stu-id="30504-231">The output c1 is not the same as the input c1 register.</span></span> <span data-ttu-id="30504-232">Запись в регистр константы в предшейдере фактически записывает в соответствующий входной слот шейдера (константа).</span><span class="sxs-lookup"><span data-stu-id="30504-232">Writing to a constant register in a preshader actually writes into the corresponding shader's input (constant) slot.</span></span>


```
// BaseDelta c0 1
// Refinements c1 1
preshader
mul c1.x, c0.x, (-2)
add c0.x, c0.x, c0.x
cmp c5.x, c1.x, (1), (0)
```



<span data-ttu-id="30504-233">Приведенная выше инструкция CMP будет считать значение C1, а инструкция mul будет записывать в реестры аппаратного шейдера для использования шейдером вершин.</span><span class="sxs-lookup"><span data-stu-id="30504-233">The cmp instruction above will read the preshader c1 value, while the mul instruction will write to the hardware shader registers to be used by the vertex shader.</span></span>

## <a name="use-parameter-blocks-to-manage-effect-parameters"></a><span data-ttu-id="30504-234">Использование блоков параметров для управления параметрами эффектов</span><span class="sxs-lookup"><span data-stu-id="30504-234">Use Parameter Blocks to Manage Effect Parameters</span></span>

<span data-ttu-id="30504-235">Блоки параметров — это блоки изменений состояния эффектов.</span><span class="sxs-lookup"><span data-stu-id="30504-235">Parameter blocks are blocks of effect state changes.</span></span> <span data-ttu-id="30504-236">Блок параметров может записывать изменения состояния, чтобы их можно было применить позже с помощью одного вызова.</span><span class="sxs-lookup"><span data-stu-id="30504-236">A parameter block can record state changes, so that they can be applied later on with a single call.</span></span> <span data-ttu-id="30504-237">Создайте блок параметров, вызвав [**ID3DXEffect:: бегинпараметерблокк**](id3dxeffect--beginparameterblock.md):</span><span class="sxs-lookup"><span data-stu-id="30504-237">Create a parameter block by calling [**ID3DXEffect::BeginParameterBlock**](id3dxeffect--beginparameterblock.md):</span></span>


```
    m_pEffect->SetTechnique( "RenderScene" );

    m_pEffect->BeginParameterBlock();
    D3DXVECTOR4 v4( Diffuse.r, Diffuse.g, Diffuse.b, Diffuse.a );
    m_pEffect->SetVector( "g_vDiffuse", &v4 );
    m_pEffect->SetFloat( "g_fReflectivity", fReflectivity );
    m_pEffect->SetFloat( "g_fAnimSpeed", fAnimSpeed );
    m_pEffect->SetFloat( "g_fSizeMul", fSize );
    m_hParameters = m_pEffect->EndParameterBlock();
```



<span data-ttu-id="30504-238">Блок параметров сохраняет четыре изменения, примененные вызовами API.</span><span class="sxs-lookup"><span data-stu-id="30504-238">The parameter block saves four changes applied by the API calls.</span></span> <span data-ttu-id="30504-239">Вызов [**ID3DXEffect:: бегинпараметерблокк**](id3dxeffect--beginparameterblock.md) начинает запись изменений состояния.</span><span class="sxs-lookup"><span data-stu-id="30504-239">Calling [**ID3DXEffect::BeginParameterBlock**](id3dxeffect--beginparameterblock.md) starts recording the state changes.</span></span> <span data-ttu-id="30504-240">[**ID3DXEffect:: ендпараметерблокк**](id3dxeffect--endparameterblock.md) останавливает Добавление изменений в блок параметров и возвращает маркер.</span><span class="sxs-lookup"><span data-stu-id="30504-240">[**ID3DXEffect::EndParameterBlock**](id3dxeffect--endparameterblock.md) stops adding the changes to the parameter block and returns a handle.</span></span> <span data-ttu-id="30504-241">Этот маркер будет использоваться при вызове [**ID3DXEffect:: апплипараметерблокк**](id3dxeffect--applyparameterblock.md).</span><span class="sxs-lookup"><span data-stu-id="30504-241">The handle will be used when calling [**ID3DXEffect::ApplyParameterBlock**](id3dxeffect--applyparameterblock.md).</span></span>

<span data-ttu-id="30504-242">В [примере еффектпарам](https://msdn.microsoft.com/library/Ee417535(v=VS.85).aspx)в последовательности прорисовки применяется блок параметров:</span><span class="sxs-lookup"><span data-stu-id="30504-242">In the [EffectParam Sample](https://msdn.microsoft.com/library/Ee417535(v=VS.85).aspx), the parameter block is applied in the render sequence:</span></span>


```
CObj g_aObj[NUM_OBJS];       // Object instances

    if( SUCCEEDED( pd3dDevice->BeginScene() ) )
    {
        // Set the shared parameters using the first mesh's effect.

        // Render the mesh objects
        for( int i = 0; i < NUM_OBJS; ++i )
        {
            ID3DXEffect *pEffect = g_aObj[i].m_pEffect;

            // Apply the parameters
            pEffect->ApplyParameterBlock( g_aObj[i].m_hParameters );

            ...

            pEffect->Begin( &cPasses, 0 );
            for( iPass = 0; iPass < cPasses; iPass++ )
            {
              ...
            }
            pEffect->End();
        }

        ...
        pd3dDevice->EndScene();
    }
```



<span data-ttu-id="30504-243">Блок параметров задает значения всех четырех изменений состояния непосредственно перед вызовом [**ID3DXEffect:: Begin**](id3dxeffect--begin.md) .</span><span class="sxs-lookup"><span data-stu-id="30504-243">The parameter block sets the value of all four of the state changes just before [**ID3DXEffect::Begin**](id3dxeffect--begin.md) is called.</span></span> <span data-ttu-id="30504-244">Блоки параметров — это удобный способ установки нескольких изменений состояния с помощью одного вызова API.</span><span class="sxs-lookup"><span data-stu-id="30504-244">Parameter blocks are a handy way to set multiple state changes with a single API call.</span></span>

## <a name="related-topics"></a><span data-ttu-id="30504-245">См. также</span><span class="sxs-lookup"><span data-stu-id="30504-245">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="30504-246">Эффекты</span><span class="sxs-lookup"><span data-stu-id="30504-246">Effects</span></span>](effects.md)
</dt> </dl>

 

 
