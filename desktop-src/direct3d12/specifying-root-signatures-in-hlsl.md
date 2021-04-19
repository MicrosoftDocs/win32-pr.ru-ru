---
title: Определение корневых подписей в HLSL
description: Указание корневых подписей в модели шейдера HLSL 5,1 является альтернативой указанию их в коде C++.
ms.assetid: 399F5E91-B017-4F5E-9037-DC055407D96F
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2dad0da9f84d68fc1acbf53332d1cae4075f0faa
ms.sourcegitcommit: 91110c16e4713ed82d7fb80562d3ddf40b5d76b2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/14/2021
ms.locfileid: "107492286"
---
# <a name="specifying-root-signatures-in-hlsl"></a><span data-ttu-id="495b1-103">Определение корневых подписей в HLSL</span><span class="sxs-lookup"><span data-stu-id="495b1-103">Specifying Root Signatures in HLSL</span></span>

<span data-ttu-id="495b1-104">Указание корневых подписей в модели шейдера HLSL 5,1 является альтернативой указанию их в коде C++.</span><span class="sxs-lookup"><span data-stu-id="495b1-104">Specifying root signatures in HLSL Shader Model 5.1 is an alternative to specifying them in C++ code.</span></span>

-   [<span data-ttu-id="495b1-105">Пример корневой подписи HLSL</span><span class="sxs-lookup"><span data-stu-id="495b1-105">An example HLSL Root Signature</span></span>](#an-example-hlsl-root-signature)
    -   [<span data-ttu-id="495b1-106">Корневая подпись версии 1,0</span><span class="sxs-lookup"><span data-stu-id="495b1-106">Root Signature Version 1.0</span></span>](#root-signature-version-10)
    -   [<span data-ttu-id="495b1-107">Корневая подпись версии 1.1</span><span class="sxs-lookup"><span data-stu-id="495b1-107">Root Signature Version 1.1</span></span>](#root-signature-version-11)
-   [<span data-ttu-id="495b1-108">рутфлагс</span><span class="sxs-lookup"><span data-stu-id="495b1-108">RootFlags</span></span>](#rootflags)
-   [<span data-ttu-id="495b1-109">Корневые константы</span><span class="sxs-lookup"><span data-stu-id="495b1-109">Root Constants</span></span>](#root-constants)
-   [<span data-ttu-id="495b1-110">Видимость</span><span class="sxs-lookup"><span data-stu-id="495b1-110">Visibility</span></span>](#visibility)
-   [<span data-ttu-id="495b1-111">CBV корневого уровня</span><span class="sxs-lookup"><span data-stu-id="495b1-111">Root-level CBV</span></span>](#root-level-cbv)
-   [<span data-ttu-id="495b1-112">SRV на корневом уровне</span><span class="sxs-lookup"><span data-stu-id="495b1-112">Root-level SRV</span></span>](#root-level-srv)
-   [<span data-ttu-id="495b1-113">UAV корневого уровня</span><span class="sxs-lookup"><span data-stu-id="495b1-113">Root-level UAV</span></span>](#root-level-uav)
-   [<span data-ttu-id="495b1-114">Таблица дескрипторов</span><span class="sxs-lookup"><span data-stu-id="495b1-114">Descriptor Table</span></span>](#descriptor-table)
-   [<span data-ttu-id="495b1-115">Статическая выборка</span><span class="sxs-lookup"><span data-stu-id="495b1-115">Static Sampler</span></span>](#static-sampler)
-   [<span data-ttu-id="495b1-116">Компиляция корневой подписи HLSL</span><span class="sxs-lookup"><span data-stu-id="495b1-116">Compiling an HLSL root signature</span></span>](#compiling-an-hlsl-root-signature)
-   [<span data-ttu-id="495b1-117">Управление корневыми сигнатурами с помощью компилятора FXC</span><span class="sxs-lookup"><span data-stu-id="495b1-117">Manipulating root signatures with the FXC compiler</span></span>](#manipulating-root-signatures-with-the-fxc-compiler)
-   [<span data-ttu-id="495b1-118">Примечания</span><span class="sxs-lookup"><span data-stu-id="495b1-118">Notes</span></span>](#notes)
-   [<span data-ttu-id="495b1-119">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="495b1-119">Related topics</span></span>](#related-topics)

## <a name="an-example-hlsl-root-signature"></a><span data-ttu-id="495b1-120">Пример корневой подписи HLSL</span><span class="sxs-lookup"><span data-stu-id="495b1-120">An example HLSL Root Signature</span></span>

<span data-ttu-id="495b1-121">Корневая подпись может быть указана в HLSL в виде строки.</span><span class="sxs-lookup"><span data-stu-id="495b1-121">A root signature can be specified in HLSL as a string.</span></span> <span data-ttu-id="495b1-122">Строка содержит коллекцию предложений с разделителями-запятыми, описывающих компоненты, составляющие корневую подпись.</span><span class="sxs-lookup"><span data-stu-id="495b1-122">The string contains a collection of comma-separated clauses that describe root signature constituent components.</span></span> <span data-ttu-id="495b1-123">Корневая подпись должна быть идентичной в шейдере для любого объекта состояния конвейера (PSO).</span><span class="sxs-lookup"><span data-stu-id="495b1-123">The root signature should be identical across shaders for any one pipeline state object (PSO).</span></span> <span data-ttu-id="495b1-124">Пример:</span><span class="sxs-lookup"><span data-stu-id="495b1-124">Here is an example:</span></span>

### <a name="root-signature-version-10"></a><span data-ttu-id="495b1-125">Корневая подпись версии 1,0</span><span class="sxs-lookup"><span data-stu-id="495b1-125">Root Signature Version 1.0</span></span>

``` syntax
#define MyRS1 "RootFlags( ALLOW_INPUT_ASSEMBLER_INPUT_LAYOUT | " \
                         "DENY_VERTEX_SHADER_ROOT_ACCESS), " \
              "CBV(b0, space = 1), " \
              "SRV(t0), " \
              "UAV(u0, visibility = SHADER_VISIBILITY_GEOMETRY), " \
              "DescriptorTable( CBV(b0), " \
                               "UAV(u1, numDescriptors = 2), " \
                               "SRV(t1, numDescriptors = unbounded)), " \
              "DescriptorTable(Sampler(s0, numDescriptors = 2)), " \
              "RootConstants(num32BitConstants=1, b9), " \
              "DescriptorTable( UAV(u3), " \
                               "UAV(u4), " \
                               "UAV(u5, offset=1)), " \

              "StaticSampler(s2)," \
              "StaticSampler(s3, " \
                             "addressU = TEXTURE_ADDRESS_CLAMP, " \
                             "filter = FILTER_MIN_MAG_MIP_LINEAR )"
```

<span data-ttu-id="495b1-126">Это определение даст следующую корневую подпись, заметив следующее:</span><span class="sxs-lookup"><span data-stu-id="495b1-126">This definition would give the following root signature, noting:</span></span>

-   <span data-ttu-id="495b1-127">Использование параметров по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="495b1-127">The use of default parameters.</span></span>
-   <span data-ttu-id="495b1-128">B0 и (B0, Space = 1) не конфликтуют</span><span class="sxs-lookup"><span data-stu-id="495b1-128">b0 and (b0, space=1) do not conflict</span></span>
-   <span data-ttu-id="495b1-129">U0 виден только для шейдера Geometry</span><span class="sxs-lookup"><span data-stu-id="495b1-129">u0 is only visible to the geometry shader</span></span>
-   <span data-ttu-id="495b1-130">U4 и U5 имеют псевдонимы для одного и того же дескриптора в куче.</span><span class="sxs-lookup"><span data-stu-id="495b1-130">u4 and u5 are aliased to the same descriptor in a heap</span></span>

![Корневая подпись, заданная с помощью языка шейдера высокого уровня](images/hlsl-root-signature.png)

### <a name="root-signature-version-11"></a><span data-ttu-id="495b1-132">Корневая подпись версии 1.1</span><span class="sxs-lookup"><span data-stu-id="495b1-132">Root Signature Version 1.1</span></span>

<span data-ttu-id="495b1-133">[Корневая подпись версии 1,1](root-signature-version-1-1.md) включает оптимизацию драйверов для дескрипторов и данных корневой подписи.</span><span class="sxs-lookup"><span data-stu-id="495b1-133">[Root Signature Version 1.1](root-signature-version-1-1.md) enables driver optimizations on root signature descriptors and data.</span></span>

``` syntax
#define MyRS1 "RootFlags( ALLOW_INPUT_ASSEMBLER_INPUT_LAYOUT | " \
                         "DENY_VERTEX_SHADER_ROOT_ACCESS), " \
              "CBV(b0, space = 1, flags = DATA_STATIC), " \
              "SRV(t0), " \
              "UAV(u0), " \
              "DescriptorTable( CBV(b1), " \
                               "SRV(t1, numDescriptors = 8, " \
                               "        flags = DESCRIPTORS_VOLATILE), " \
                               "UAV(u1, numDescriptors = unbounded, " \
                               "        flags = DESCRIPTORS_VOLATILE)), " \
              "DescriptorTable(Sampler(s0, space=1, numDescriptors = 4)), " \
              "RootConstants(num32BitConstants=3, b10), " \
              "StaticSampler(s1)," \
              "StaticSampler(s2, " \
                             "addressU = TEXTURE_ADDRESS_CLAMP, " \
                             "filter = FILTER_MIN_MAG_MIP_LINEAR )"
```

<span data-ttu-id="495b1-134">Язык подписи HLSL тесно соответствует API-интерфейсам корневой подписи C++ и имеет эквивалентную ковыразительные возможности.</span><span class="sxs-lookup"><span data-stu-id="495b1-134">The HLSL root signature language closely corresponds to the C++ root signature APIs and has equivalent expressive power.</span></span> <span data-ttu-id="495b1-135">Корневая подпись указывается как последовательность предложений, разделенных запятыми.</span><span class="sxs-lookup"><span data-stu-id="495b1-135">The root signature is specified as a sequence of clauses, separated by comma.</span></span> <span data-ttu-id="495b1-136">Порядок предложений важен, так как порядок анализа определяет расположение слота в корневой подписи.</span><span class="sxs-lookup"><span data-stu-id="495b1-136">The order of clauses is important, as the order of parsing determines the slot position in the root signature.</span></span> <span data-ttu-id="495b1-137">Каждое предложение принимает один или несколько именованных параметров.</span><span class="sxs-lookup"><span data-stu-id="495b1-137">Each clause takes one or more named parameters.</span></span> <span data-ttu-id="495b1-138">Однако порядок параметров не имеет значения.</span><span class="sxs-lookup"><span data-stu-id="495b1-138">The order of parameters is not important, however.</span></span>

## <a name="rootflags"></a><span data-ttu-id="495b1-139">рутфлагс</span><span class="sxs-lookup"><span data-stu-id="495b1-139">RootFlags</span></span>

<span data-ttu-id="495b1-140">Необязательное предложение *рутфлагс* принимает 0 (значение по умолчанию, указывающее на отсутствие флагов) или одно или несколько предопределенных значений корневых флагов, Соединенных с помощью \| оператора или.</span><span class="sxs-lookup"><span data-stu-id="495b1-140">The optional *RootFlags* clause takes either 0 (the default value to indicate no flags), or one or several of predefined root flags values, connected via the OR ‘\|’ operator.</span></span> <span data-ttu-id="495b1-141">Допустимые значения корневого флага определяются [**D3D12 \_ \_ \_ флагами корневой подписи**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_signature_flags).</span><span class="sxs-lookup"><span data-stu-id="495b1-141">The allowed root flag values are defined by [**D3D12\_ROOT\_SIGNATURE\_FLAGS**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_signature_flags).</span></span>

<span data-ttu-id="495b1-142">Пример:</span><span class="sxs-lookup"><span data-stu-id="495b1-142">For example:</span></span>

``` syntax
RootFlags(0) // default value – no flags
RootFlags(ALLOW_INPUT_ASSEMBLER_INPUT_LAYOUT)
RootFlags(ALLOW_INPUT_ASSEMBLER_INPUT_LAYOUT | DENY_VERTEX_SHADER_ROOT_ACCESS)
```

## <a name="root-constants"></a><span data-ttu-id="495b1-143">Корневые константы</span><span class="sxs-lookup"><span data-stu-id="495b1-143">Root Constants</span></span>

<span data-ttu-id="495b1-144">Предложение *рутконстантс* задает корневые константы в корневой подписи.</span><span class="sxs-lookup"><span data-stu-id="495b1-144">The *RootConstants* clause specifies root constants in the root signature.</span></span> <span data-ttu-id="495b1-145">Два обязательных параметра: *num32BitConstants* и *Брег* (регистр, соответствующий *басешадеррегистер* в API-интерфейсах C++) *кбуффер*.</span><span class="sxs-lookup"><span data-stu-id="495b1-145">Two mandatory parameters are: *num32BitConstants* and *bReg* (the register corresponding to *BaseShaderRegister* in C++ APIs) of the *cbuffer*.</span></span> <span data-ttu-id="495b1-146">Параметры Space (*регистерспаце* в API-интерфейсах C++) и Visibility (*шадервисибилити* в c++) являются необязательными, а значения по умолчанию:</span><span class="sxs-lookup"><span data-stu-id="495b1-146">The space (*RegisterSpace* in C++ APIs) and visibility (*ShaderVisibility* in C++) parameters are optional, and the default values are:</span></span>

``` syntax
RootConstants(num32BitConstants=N, bReg [, space=0, 
              visibility=SHADER_VISIBILITY_ALL ])
```

<span data-ttu-id="495b1-147">Пример:</span><span class="sxs-lookup"><span data-stu-id="495b1-147">For example:</span></span>

``` syntax
RootConstants(num32BitConstants=3, b3)
```

## <a name="visibility"></a><span data-ttu-id="495b1-148">Видимость</span><span class="sxs-lookup"><span data-stu-id="495b1-148">Visibility</span></span>

<span data-ttu-id="495b1-149">Видимость — это необязательный параметр, который может иметь одно из [**значений \_ \_ видимости шейдера D3D12**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility).</span><span class="sxs-lookup"><span data-stu-id="495b1-149">Visibility is an optional parameter that can have one of the values from [**D3D12\_SHADER\_VISIBILITY**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility).</span></span>

<span data-ttu-id="495b1-150">Видимость ШЕЙДЕРа выполняет \_ \_ широковещательную рассылку всех корневых аргументов всем шейдерам.</span><span class="sxs-lookup"><span data-stu-id="495b1-150">SHADER\_VISIBILITY\_ALL broadcasts the root arguments to all shaders.</span></span> <span data-ttu-id="495b1-151">На оборудовании это не имеет затрат, но на другом оборудовании есть затраты на разветвление данных на все этапы шейдера.</span><span class="sxs-lookup"><span data-stu-id="495b1-151">On some hardware this has no cost, but on other hardware there is a cost to fork the data to all the shader stages.</span></span> <span data-ttu-id="495b1-152">Установка одного из параметров, таких как \_ вершина видимости шейдера \_ , ограничивает корневой аргумент одним этапом шейдера.</span><span class="sxs-lookup"><span data-stu-id="495b1-152">Setting one of the options, such as SHADER\_VISIBILITY\_VERTEX, limits the root argument to a single shader stage.</span></span>

<span data-ttu-id="495b1-153">Задание для корневых аргументов одного этапа шейдера позволяет использовать одно и то же имя привязки на разных стадиях.</span><span class="sxs-lookup"><span data-stu-id="495b1-153">Setting root arguments to single shader stages allows the same bind name to be used at different stages.</span></span> <span data-ttu-id="495b1-154">Например, привязка SRV к `t0,SHADER_VISIBILITY_VERTEX` и привязке SRV для будет `t0,SHADER_VISIBILITY_PIXEL` допустимой.</span><span class="sxs-lookup"><span data-stu-id="495b1-154">For example, an SRV binding of `t0,SHADER_VISIBILITY_VERTEX` and SRV binding of `t0,SHADER_VISIBILITY_PIXEL` would be valid.</span></span> <span data-ttu-id="495b1-155">Но если параметр видимости был `t0,SHADER_VISIBILITY_ALL` для одной из привязок, корневая подпись будет недействительной.</span><span class="sxs-lookup"><span data-stu-id="495b1-155">But if the visibility setting was `t0,SHADER_VISIBILITY_ALL` for one of the bindings, the root signature would be invalid.</span></span>

## <a name="root-level-cbv"></a><span data-ttu-id="495b1-156">CBV корневого уровня</span><span class="sxs-lookup"><span data-stu-id="495b1-156">Root-level CBV</span></span>

<span data-ttu-id="495b1-157">В `CBV` предложении (представление буфера констант) указывается запись в формате буфера констант на корневом уровне b-Register.</span><span class="sxs-lookup"><span data-stu-id="495b1-157">The `CBV` (constant buffer view) clause specifies a root-level constant buffer b-register Reg entry.</span></span> <span data-ttu-id="495b1-158">Обратите внимание, что это скалярная запись; невозможно указать диапазон для корневого уровня.</span><span class="sxs-lookup"><span data-stu-id="495b1-158">Note that this is a scalar entry; it is not possible to specify a range for the root level.</span></span>

``` syntax
CBV(bReg [, space=0, visibility=SHADER_VISIBILITY_ALL ])    //   Version 1.0
CBV(bReg [, space=0, visibility=SHADER_VISIBILITY_ALL,      // Version 1.1
            flags=DATA_STATIC_WHILE_SET_AT_EXECUTE ])
```

## <a name="root-level-srv"></a><span data-ttu-id="495b1-159">SRV на корневом уровне</span><span class="sxs-lookup"><span data-stu-id="495b1-159">Root-level SRV</span></span>

<span data-ttu-id="495b1-160">`SRV`Предложение (представление ресурсов шейдера) задает запись реестра SRV t-Register на корневом уровне.</span><span class="sxs-lookup"><span data-stu-id="495b1-160">The `SRV` (shader resource view) clause specifies a root-level SRV t-register Reg entry.</span></span> <span data-ttu-id="495b1-161">Обратите внимание, что это скалярная запись; невозможно указать диапазон для корневого уровня.</span><span class="sxs-lookup"><span data-stu-id="495b1-161">Note that this is a scalar entry; it is not possible to specify a range for the root level.</span></span>

``` syntax
SRV(tReg [, space=0, visibility=SHADER_VISIBILITY_ALL ])    //   Version 1.0
SRV(tReg [, space=0, visibility=SHADER_VISIBILITY_ALL,      // Version 1.1
            flags=DATA_STATIC_WHILE_SET_AT_EXECUTE ])
```

## <a name="root-level-uav"></a><span data-ttu-id="495b1-162">UAV корневого уровня</span><span class="sxs-lookup"><span data-stu-id="495b1-162">Root-level UAV</span></span>

<span data-ttu-id="495b1-163">В `UAV` предложении (неупорядоченное представление доступа) указана запись reg UAV u-Register.</span><span class="sxs-lookup"><span data-stu-id="495b1-163">The `UAV` (unordered access view) clause specifies a root-level UAV u-register Reg entry.</span></span> <span data-ttu-id="495b1-164">Обратите внимание, что это скалярная запись; невозможно указать диапазон для корневого уровня.</span><span class="sxs-lookup"><span data-stu-id="495b1-164">Note that this is a scalar entry; it is not possible to specify a range for the root level.</span></span>

``` syntax
UAV(uReg [, space=0, visibility=SHADER_VISIBILITY_ALL ])    //   Version 1.0
UAV(uReg [, space=0, visibility=SHADER_VISIBILITY_ALL,      // Version 1.1
            flags=DATA_VOLATILE ])
```

<span data-ttu-id="495b1-165">Пример:</span><span class="sxs-lookup"><span data-stu-id="495b1-165">For example:</span></span>

``` syntax
UAV(u3)
```

## <a name="descriptor-table"></a><span data-ttu-id="495b1-166">Таблица дескрипторов</span><span class="sxs-lookup"><span data-stu-id="495b1-166">Descriptor Table</span></span>

<span data-ttu-id="495b1-167">`DescriptorTable`Предложение само по себе представляет собой список разделенных запятыми предложений табличных таблиц, а также необязательный параметр видимости.</span><span class="sxs-lookup"><span data-stu-id="495b1-167">The `DescriptorTable` clause is itself a list of comma-separated descriptor table clauses, as well as an optional visibility parameter.</span></span> <span data-ttu-id="495b1-168">Предложения *дескриптортабле* включают CBV, SRV, UAV и образец.</span><span class="sxs-lookup"><span data-stu-id="495b1-168">The *DescriptorTable* clauses include CBV, SRV, UAV, and Sampler.</span></span> <span data-ttu-id="495b1-169">Обратите внимание, что их параметры отличаются от параметров в предложениях корневого уровня.</span><span class="sxs-lookup"><span data-stu-id="495b1-169">Note that their parameters differ from those of the root-level clauses.</span></span>

``` syntax
DescriptorTable( DTClause1, [ DTClause2, … DTClauseN,
                 visibility=SHADER_VISIBILITY_ALL ] )
```

<span data-ttu-id="495b1-170">Таблица дескрипторов `CBV` имеет следующий синтаксис:</span><span class="sxs-lookup"><span data-stu-id="495b1-170">The Descriptor Table `CBV` has the following syntax:</span></span>

``` syntax
CBV(bReg [, numDescriptors=1, space=0, offset=DESCRIPTOR_RANGE_OFFSET_APPEND ])   // Version 1.0
CBV(bReg [, numDescriptors=1, space=0, offset=DESCRIPTOR_RANGE_OFFSET_APPEND      // Version 1.1
          , flags=DATA_STATIC_WHILE_SET_AT_EXECUTE ])
```

<span data-ttu-id="495b1-171">Пример:</span><span class="sxs-lookup"><span data-stu-id="495b1-171">For example:</span></span>

``` syntax
DescriptorTable(CBV(b0),SRV(t3, numDescriptors=unbounded))
```

<span data-ttu-id="495b1-172">Обязательный параметр *Брег* указывает начальный reg диапазона кбуффер.</span><span class="sxs-lookup"><span data-stu-id="495b1-172">The mandatory parameter *bReg* specifies the start Reg of the cbuffer range.</span></span> <span data-ttu-id="495b1-173">Параметр *нумдескрипторс* указывает число дескрипторов в смежном диапазоне кбуффер. значение по умолчанию — 1.</span><span class="sxs-lookup"><span data-stu-id="495b1-173">The *numDescriptors* parameter specifies the number of descriptors in the contiguous cbuffer range; the default value being 1.</span></span> <span data-ttu-id="495b1-174">Запись объявляет диапазон кбуффер ` [Reg, Reg + numDescriptors - 1]` , если *нумдескрипторс* является числом.</span><span class="sxs-lookup"><span data-stu-id="495b1-174">The entry declares a cbuffer range` [Reg, Reg + numDescriptors - 1]`, when *numDescriptors* is a number.</span></span> <span data-ttu-id="495b1-175">Если *нумдескрипторс* имеет значение "unboundd", то диапазон равен, а это `[Reg, UINT_MAX]` означает, что приложение должно убедиться, что оно не ссылается на область вне границ.</span><span class="sxs-lookup"><span data-stu-id="495b1-175">If *numDescriptors* is equal to "unbounded", the range is `[Reg, UINT_MAX]`, which means the app must ensure it is not referencing an out-of-bounds area.</span></span> <span data-ttu-id="495b1-176">Поле *offset* представляет параметр *оффсетиндескрипторсфромтаблестарт* в API-интерфейсах C++, то есть смещение (в дескрипторах) от начала таблицы.</span><span class="sxs-lookup"><span data-stu-id="495b1-176">The *offset* field represents the *OffsetInDescriptorsFromTableStart* parameter in the C++ APIs, that is, the offset (in descriptors) from the start of the table.</span></span> <span data-ttu-id="495b1-177">Если для смещения задано значение \_ «Добавление смещения диапазона дескрипторов» \_ \_ (по умолчанию), это означает, что диапазон находится непосредственно после предыдущего диапазона.</span><span class="sxs-lookup"><span data-stu-id="495b1-177">If the offset is set to DESCRIPTOR\_RANGE\_OFFSET\_APPEND (the default), it means the range is directly after the previous range.</span></span> <span data-ttu-id="495b1-178">Однако при вводе отдельных смещений диапазоны могут пересекаться друг с другом, что позволяет использовать псевдонимы регистров.</span><span class="sxs-lookup"><span data-stu-id="495b1-178">However, entering specific offsets does allow for ranges to overlap each other, allowing register aliasing.</span></span>

<span data-ttu-id="495b1-179">Таблица дескрипторов `SRV` имеет следующий синтаксис:</span><span class="sxs-lookup"><span data-stu-id="495b1-179">The Descriptor Table `SRV` has the following syntax:</span></span>

``` syntax
SRV(tReg [, numDescriptors=1, space=0, offset=DESCRIPTOR_RANGE_OFFSET_APPEND ])    // Version 1.0
SRV(tReg [, numDescriptors=1, space=0, offset=DESCRIPTOR_RANGE_OFFSET_APPEND,      // Version 1.1
            flags=DATA_STATIC_WHILE_SET_AT_EXECUTE ])
```

<span data-ttu-id="495b1-180">Это похоже на запись таблицы дескрипторов `CBV` , за исключением того, что указанный диапазон предназначен для представлений ресурсов шейдера.</span><span class="sxs-lookup"><span data-stu-id="495b1-180">This is similar to the descriptor table `CBV` entry, except the specified range is for shader resource views.</span></span>

<span data-ttu-id="495b1-181">Таблица дескрипторов `UAV` имеет следующий синтаксис:</span><span class="sxs-lookup"><span data-stu-id="495b1-181">The Descriptor Table `UAV` has the following syntax:</span></span>

``` syntax
UAV(uReg [, numDescriptors=1, space=0, offset=DESCRIPTOR_RANGE_OFFSET_APPEND ])    // Version 1.0
UAV(uReg [, numDescriptors=1, space=0, offset=DESCRIPTOR_RANGE_OFFSET_APPEND,      // Version 1.1
            flags=DATA_VOLATILE ])
```

<span data-ttu-id="495b1-182">Это похоже на запись таблицы дескрипторов `CBV` , за исключением того, что указанный диапазон предназначен для неупорядоченных представлений доступа.</span><span class="sxs-lookup"><span data-stu-id="495b1-182">This is similar to the descriptor table `CBV` entry, except the specified range is for unordered access views.</span></span>

<span data-ttu-id="495b1-183">Таблица дескрипторов `Sampler` имеет следующий синтаксис:</span><span class="sxs-lookup"><span data-stu-id="495b1-183">The Descriptor Table `Sampler` has the following syntax:</span></span>

``` syntax
Sampler(sReg [, numDescriptors=1, space=0, offset=DESCRIPTOR_RANGE_OFFSET_APPEND ])  // Version 1.0
Sampler(sReg [, numDescriptors=1, space=0, offset=DESCRIPTOR_RANGE_OFFSET_APPEND,    // Version 1.1
                flags=0 ])
```

<span data-ttu-id="495b1-184">Это похоже на запись таблицы дескрипторов `CBV` , за исключением того, что указанный диапазон предназначен для образцов шейдера.</span><span class="sxs-lookup"><span data-stu-id="495b1-184">This is similar to the descriptor table `CBV` entry, except the specified range is for shader samplers.</span></span> <span data-ttu-id="495b1-185">Обратите внимание, что пробы не могут смешиваться с другими типами дескрипторов в одной и той же таблице дескрипторов (так как они находятся в отдельной куче дескрипторов).</span><span class="sxs-lookup"><span data-stu-id="495b1-185">Note that Samplers can’t be mixed with other types of descriptors in the same descriptor table (since they are in a separate descriptor heap).</span></span>

## <a name="static-sampler"></a><span data-ttu-id="495b1-186">Статическая выборка</span><span class="sxs-lookup"><span data-stu-id="495b1-186">Static Sampler</span></span>

<span data-ttu-id="495b1-187">Статический образец представляет структуру [**D3D12 \_ статической \_ \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_static_sampler_desc) выборки.</span><span class="sxs-lookup"><span data-stu-id="495b1-187">The static sampler represents the [**D3D12\_STATIC\_SAMPLER\_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_static_sampler_desc) structure.</span></span> <span data-ttu-id="495b1-188">Обязательный параметр для *статиксамплер* — это скалярный образец s-Register reg. Другие параметры являются необязательными со значениями по умолчанию, показанными ниже.</span><span class="sxs-lookup"><span data-stu-id="495b1-188">The mandatory parameter for *StaticSampler* is a scalar, sampler s-register Reg. Other parameters are optional with default values shown below.</span></span> <span data-ttu-id="495b1-189">Большинство полей допускают набор предопределенных перечислений.</span><span class="sxs-lookup"><span data-stu-id="495b1-189">Most fields accept a set of predefined enums.</span></span>

``` syntax
StaticSampler( sReg,
              [ filter = FILTER_ANISOTROPIC, 
                addressU = TEXTURE_ADDRESS_WRAP,
                addressV = TEXTURE_ADDRESS_WRAP,
                addressW = TEXTURE_ADDRESS_WRAP,
                mipLODBias = 0.f,
                maxAnisotropy = 16,
                comparisonFunc = COMPARISON_LESS_EQUAL,
                borderColor = STATIC_BORDER_COLOR_OPAQUE_WHITE,
                minLOD = 0.f,         
                maxLOD = 3.402823466e+38f,
                space = 0, 
                visibility = SHADER_VISIBILITY_ALL ])
```

<span data-ttu-id="495b1-190">Пример:</span><span class="sxs-lookup"><span data-stu-id="495b1-190">For example:</span></span>

``` syntax
StaticSampler(s4, filter=FILTER_MIN_MAG_MIP_LINEAR)
```

<span data-ttu-id="495b1-191">Параметры параметров очень похожи на вызовы API C++, за исключением *borderColor*, который ограничен перечислением в HLSL.</span><span class="sxs-lookup"><span data-stu-id="495b1-191">The parameter options are very similar to the C++ API calls, except for *borderColor*, which is restricted to an enum in HLSL.</span></span>

<span data-ttu-id="495b1-192">Поле фильтра может быть одним из [**\_ фильтров D3D12**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_filter).</span><span class="sxs-lookup"><span data-stu-id="495b1-192">The filter field can be one of [**D3D12\_FILTER**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_filter).</span></span>

<span data-ttu-id="495b1-193">В качестве полей адреса можно использовать один из [**\_ \_ \_ режимов адресации текстуры D3D12**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_texture_address_mode).</span><span class="sxs-lookup"><span data-stu-id="495b1-193">The address fields can each be one of [**D3D12\_TEXTURE\_ADDRESS\_MODE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_texture_address_mode).</span></span>

<span data-ttu-id="495b1-194">Функция сравнения может быть одним из [**сравнения D3D12 \_ \_ Func**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_comparison_func).</span><span class="sxs-lookup"><span data-stu-id="495b1-194">The comparison function can be one of [**D3D12\_COMPARISON\_FUNC**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_comparison_func).</span></span>

<span data-ttu-id="495b1-195">Поле цвета границы может быть одним из [**D3D12 \_ статического \_ \_ цвета границы**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_static_border_color).</span><span class="sxs-lookup"><span data-stu-id="495b1-195">The border color field can be one of [**D3D12\_STATIC\_BORDER\_COLOR**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_static_border_color).</span></span>

<span data-ttu-id="495b1-196">Видимость может быть одной из [**D3D12ных \_ шейдеров \_**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility).</span><span class="sxs-lookup"><span data-stu-id="495b1-196">Visibility can be one of [**D3D12\_SHADER\_VISIBILITY**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility).</span></span>

## <a name="compiling-an-hlsl-root-signature"></a><span data-ttu-id="495b1-197">Компиляция корневой подписи HLSL</span><span class="sxs-lookup"><span data-stu-id="495b1-197">Compiling an HLSL root signature</span></span>

<span data-ttu-id="495b1-198">Существует два механизма компиляции корневой подписи HLSL.</span><span class="sxs-lookup"><span data-stu-id="495b1-198">There are two mechanisms to compile an HLSL root signature.</span></span> <span data-ttu-id="495b1-199">Во-первых, можно присоединить строку корневой подписи к конкретному шейдеру с помощью атрибута *рутсигнатуре* (в следующем примере используется точка входа **MyRS1** ):</span><span class="sxs-lookup"><span data-stu-id="495b1-199">First, it is possible to attach a root signature string to a particular shader via the *RootSignature* attribute (in the following example, using the **MyRS1** entry point):</span></span>

``` syntax
[RootSignature(MyRS1)]
float4 main(float4 coord : COORD) : SV_Target
{
…
}
```

<span data-ttu-id="495b1-200">Компилятор создаст и проверит корневой BLOB-объект подписи для шейдера и внедряет его вместе с кодом байта шейдера в большой двоичный объект шейдера.</span><span class="sxs-lookup"><span data-stu-id="495b1-200">The compiler will create and verify the root signature blob for the shader and embed it alongside the shader byte code into the shader blob.</span></span> <span data-ttu-id="495b1-201">Компилятор поддерживает синтаксис корневой подписи для модели шейдеров 5,0 и более поздних версий.</span><span class="sxs-lookup"><span data-stu-id="495b1-201">The compiler supports root signature syntax for shader model 5.0 and higher.</span></span> <span data-ttu-id="495b1-202">Если корневая подпись внедрена в шейдер модели шейдера 5,0 и что шейдер отправляется в среду выполнения D3D11, в отличие от D3D12, то часть подписи root будет автоматически пропущена D3D11.</span><span class="sxs-lookup"><span data-stu-id="495b1-202">If a root signature is embedded in a shader model 5.0 shader and that shader is sent to the D3D11 runtime, as opposed to D3D12, the root signature portion will get silently ignored by D3D11.</span></span>

<span data-ttu-id="495b1-203">Другой механизм — создать изолированный корневой BLOB-объект подписи, который может повторно использовать его с большим набором шейдеров, экономя пространство.</span><span class="sxs-lookup"><span data-stu-id="495b1-203">The other mechanism is to create a standalone root signature blob, perhaps to reuse it with a large set of shaders, saving space.</span></span> <span data-ttu-id="495b1-204">[Средство компилятора Effect](/windows/desktop/direct3dtools/fxc) (FXC) поддерживает модели шейдеров **рутсиг \_ 1 \_ 0** и **рутсиг \_ 1 \_ 1** .</span><span class="sxs-lookup"><span data-stu-id="495b1-204">The [Effect-Compiler Tool](/windows/desktop/direct3dtools/fxc) (FXC) supports both **rootsig\_1\_0** and **rootsig\_1\_1** shader models.</span></span> <span data-ttu-id="495b1-205">Имя определения строки указывается с помощью обычного аргумента/E.</span><span class="sxs-lookup"><span data-stu-id="495b1-205">The name of the define string is specified via the usual /E argument.</span></span> <span data-ttu-id="495b1-206">Пример:</span><span class="sxs-lookup"><span data-stu-id="495b1-206">For example:</span></span>

``` syntax
fxc.exe /T rootsig_1_1 MyRS1.hlsl /E MyRS1 /Fo MyRS1.fxo
```

<span data-ttu-id="495b1-207">Обратите внимание, что определение строки корневой подписи может также передаваться в командной строке, например/D MyRS1 = "...".</span><span class="sxs-lookup"><span data-stu-id="495b1-207">Note that the root signature string define can also be passed on the command line, e.g, /D MyRS1=”…”.</span></span>

## <a name="manipulating-root-signatures-with-the-fxc-compiler"></a><span data-ttu-id="495b1-208">Управление корневыми сигнатурами с помощью компилятора FXC</span><span class="sxs-lookup"><span data-stu-id="495b1-208">Manipulating root signatures with the FXC compiler</span></span>

<span data-ttu-id="495b1-209">Компилятор FXC создает побайтовый код шейдера из исходных файлов HLSL.</span><span class="sxs-lookup"><span data-stu-id="495b1-209">The FXC compiler creates shader byte-code from HLSL source files.</span></span> <span data-ttu-id="495b1-210">Существует множество необязательных параметров для этого компилятора, см. [средство компилятора Effect](/windows/desktop/direct3dtools/fxc).</span><span class="sxs-lookup"><span data-stu-id="495b1-210">There are a lot of optional parameters for this compiler, refer to the [Effect-Compiler Tool](/windows/desktop/direct3dtools/fxc).</span></span>

<span data-ttu-id="495b1-211">В следующей таблице приведены некоторые примеры использования FXC для управления HLSL, созданными корневыми сигнатурами.</span><span class="sxs-lookup"><span data-stu-id="495b1-211">For managing HLSL authored root signatures, the following table gives some examples of using FXC.</span></span>



| <span data-ttu-id="495b1-212">График</span><span class="sxs-lookup"><span data-stu-id="495b1-212">Line</span></span> | <span data-ttu-id="495b1-213">Командная строка</span><span class="sxs-lookup"><span data-stu-id="495b1-213">Command line</span></span>                                                                 | <span data-ttu-id="495b1-214">Описание</span><span class="sxs-lookup"><span data-stu-id="495b1-214">Description</span></span>                                                                                                                                                                                                                              |
|------|------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="495b1-215">1</span><span class="sxs-lookup"><span data-stu-id="495b1-215">1</span></span>    | `fxc /T ps_5_1 shaderWithRootSig.hlsl /Fo rs1.fxo`                           | <span data-ttu-id="495b1-216">Компилирует шейдер для целевого объекта шейдера Pixel 5,1, источник шейдера находится в файле Шадервисрутсиг. HLSL, который включает в себя корневую подпись.</span><span class="sxs-lookup"><span data-stu-id="495b1-216">Compiles a shader for the pixel shader 5.1 target, the shader source is in the shaderWithRootSig.hlsl file, which includes a root signature.</span></span> <span data-ttu-id="495b1-217">Шейдер и корневая подпись компилируются как отдельные большие двоичные объекты в двоичном файле RS1. фксо.</span><span class="sxs-lookup"><span data-stu-id="495b1-217">The shader and root signature are compiled as separate blobs in the rs1.fxo binary file.</span></span>    |
| <span data-ttu-id="495b1-218">2</span><span class="sxs-lookup"><span data-stu-id="495b1-218">2</span></span>    | `fxc /dumpbin rs1.fxo /extractrootsignature /Fo rs1.rs.fxo`                  | <span data-ttu-id="495b1-219">Извлекает корневую подпись из файла, созданного в строке 1, поэтому файл RS1. RS. фксо содержит только корневую подпись.</span><span class="sxs-lookup"><span data-stu-id="495b1-219">Extracts the root signature from the file created by line 1, so the rs1.rs.fxo file contains just a root signature.</span></span>                                                                                                                      |
| <span data-ttu-id="495b1-220">3</span><span class="sxs-lookup"><span data-stu-id="495b1-220">3</span></span>    | `fxc /dumpbin rs1.fxo /Qstrip_rootsignature /Fo rs1.stripped.fxo`            | <span data-ttu-id="495b1-221">Удаляет корневую подпись из файла, созданного в строке 1, поэтому файл RS1.. фксо содержит шейдер без корневой подписи.</span><span class="sxs-lookup"><span data-stu-id="495b1-221">Removes the root signature from the file created by line 1, so the rs1.stripped.fxo file contains a shader with no root signature.</span></span>                                                                                                       |
| <span data-ttu-id="495b1-222">4</span><span class="sxs-lookup"><span data-stu-id="495b1-222">4</span></span>    | `fxc /dumpbin rs1.stripped.fxo /setrootsignature rs1.rs.fxo /Fo rs1.new.fxo` | <span data-ttu-id="495b1-223">Объединяет шейдер и корневую подпись, которые находятся в отдельных файлах, в двоичный файл, содержащий оба больших двоичных объектов.</span><span class="sxs-lookup"><span data-stu-id="495b1-223">Combines a shader and root signature that are in separate files into a binary file containing both blobs.</span></span> <span data-ttu-id="495b1-224">В этом примере RS1. New. fx0 будет совпадать с RS1. fx0 в строке 1.</span><span class="sxs-lookup"><span data-stu-id="495b1-224">In this example rs1.new.fx0 would be identical to rs1.fx0 in line 1.</span></span>                                                           |
| <span data-ttu-id="495b1-225">5</span><span class="sxs-lookup"><span data-stu-id="495b1-225">5</span></span>    | `fxc /T rootsig_1_0 rootSigAndMaybeShaderInHereToo.hlsl /E RS1 /Fo rs2.fxo`  | <span data-ttu-id="495b1-226">Создает автономный двоичный файл с корневой подписью из источника, который может содержать не только корневую подпись.</span><span class="sxs-lookup"><span data-stu-id="495b1-226">Creates a stand-alone root signature binary file from a source that may contain more than just a root signature.</span></span> <span data-ttu-id="495b1-227">Обратите внимание \_ на \_ целевой объект рутсиг 1 0, который RS1 является именем строки макроса корневой подписи ( \# определения) в файле HLSL.</span><span class="sxs-lookup"><span data-stu-id="495b1-227">Note the rootsig\_1\_0 target, and that RS1 is the name of the root signature (\#define) macro string in the HLSL file.</span></span> |



 

<span data-ttu-id="495b1-228">Функциональность, доступная через FXC, также доступна программно с помощью функции [**D3DCompile**](/windows/desktop/direct3dhlsl/d3dcompile) .</span><span class="sxs-lookup"><span data-stu-id="495b1-228">The functionality available through FXC is also available programmatically using the [**D3DCompile**](/windows/desktop/direct3dhlsl/d3dcompile) function.</span></span> <span data-ttu-id="495b1-229">Этот вызов компилирует шейдер с корневой подписью или автономной корневой подписью (с указанием \_ \_ целевого объекта рутсиг 1 0).</span><span class="sxs-lookup"><span data-stu-id="495b1-229">This call compiles a shader with a root signature, or stand-alone root signature (setting the rootsig\_1\_0 target).</span></span> <span data-ttu-id="495b1-230">[**D3DGetBlobPart**](/windows/desktop/direct3dhlsl/d3dgetblobpart) и [**D3DSetBlobPart**](/windows/desktop/direct3dhlsl/d3dsetblobpart) могут извлекать и подключать корневые подписи к существующему большому двоичному объекту.</span><span class="sxs-lookup"><span data-stu-id="495b1-230">[**D3DGetBlobPart**](/windows/desktop/direct3dhlsl/d3dgetblobpart) and [**D3DSetBlobPart**](/windows/desktop/direct3dhlsl/d3dsetblobpart) can extract and attach root signatures to an existing blob.</span></span>  <span data-ttu-id="495b1-231">\_ \_ Корневая подпись BLOB \_ -объекта D3D используется для указания типа корневой части двоичного объекта подписи.</span><span class="sxs-lookup"><span data-stu-id="495b1-231">D3D\_BLOB\_ROOT\_SIGNATURE is used to specify the root signature blob part type.</span></span> <span data-ttu-id="495b1-232">[**D3DStripShader**](/windows/desktop/direct3dhlsl/d3dstripshader) удаляет корневую подпись (с помощью \_ \_ флага подписи корневой папки D3DCOMPILER \_ ) из большого двоичного объекта.</span><span class="sxs-lookup"><span data-stu-id="495b1-232">[**D3DStripShader**](/windows/desktop/direct3dhlsl/d3dstripshader) removes the root signature (using the D3DCOMPILER\_STRIP\_ROOT\_SIGNATURE flag) from the blob.</span></span>

## <a name="notes"></a><span data-ttu-id="495b1-233">Примечания</span><span class="sxs-lookup"><span data-stu-id="495b1-233">Notes</span></span>

> [!Note]  
> <span data-ttu-id="495b1-234">В то время как настоятельно рекомендуется автономная компиляция шейдеров, если шейдеры должны компилироваться во время выполнения, см. примечания для [**D3DCompile2**](/windows/desktop/direct3dhlsl/d3dcompile2).</span><span class="sxs-lookup"><span data-stu-id="495b1-234">Whereas the offline compilation of shaders is strongly recommended, if shaders have to be compiled at runtime, refer to the remarks for [**D3DCompile2**](/windows/desktop/direct3dhlsl/d3dcompile2).</span></span>

 

> [!Note]  
> <span data-ttu-id="495b1-235">Для использования существующих ресурсов HLSL не требуется изменять их, чтобы обрабатывать корневые подписи.</span><span class="sxs-lookup"><span data-stu-id="495b1-235">Existing HLSL assets do not need to be changed to handle root signatures to be used with them.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="495b1-236">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="495b1-236">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="495b1-237">Динамическое индексирование с помощью HLSL 5.1</span><span class="sxs-lookup"><span data-stu-id="495b1-237">Dynamic Indexing using HLSL 5.1</span></span>](dynamic-indexing-using-hlsl-5-1.md)
</dt> <dt>

[<span data-ttu-id="495b1-238">Функции HLSL Shader Model 5,1 для Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="495b1-238">HLSL Shader Model 5.1 Features for Direct3D 12</span></span>](/windows/desktop/direct3dhlsl/hlsl-shader-model-5-1-features-for-direct3d-12)
</dt> <dt>

[<span data-ttu-id="495b1-239">Привязка ресурсов</span><span class="sxs-lookup"><span data-stu-id="495b1-239">Resource Binding</span></span>](resource-binding.md)
</dt> <dt>

[<span data-ttu-id="495b1-240">Привязка ресурсов в HLSL</span><span class="sxs-lookup"><span data-stu-id="495b1-240">Resource Binding in HLSL</span></span>](resource-binding-in-hlsl.md)
</dt> <dt>

[<span data-ttu-id="495b1-241">Корневые подписи</span><span class="sxs-lookup"><span data-stu-id="495b1-241">Root Signatures</span></span>](root-signatures.md)
</dt> <dt>

[<span data-ttu-id="495b1-242">Модель шейдера 5,1</span><span class="sxs-lookup"><span data-stu-id="495b1-242">Shader Model 5.1</span></span>](/windows/desktop/direct3dhlsl/shader-model-5-1)
</dt> <dt>

[<span data-ttu-id="495b1-243">Контрольное значение трафарета в шейдере</span><span class="sxs-lookup"><span data-stu-id="495b1-243">Shader Specified Stencil Reference Value</span></span>](shader-specified-stencil-reference-value.md)
</dt> <dt>

[<span data-ttu-id="495b1-244">Загружаются неупорядоченные представления доступа</span><span class="sxs-lookup"><span data-stu-id="495b1-244">Typed Unordered Access View Loads</span></span>](typed-unordered-access-view-loads.md)
</dt> </dl>

 

 
