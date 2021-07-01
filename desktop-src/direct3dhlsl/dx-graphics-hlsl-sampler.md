---
title: Тип образца
description: Используйте следующий синтаксис, чтобы объявить состояние образца, а также состояние сравнения образцов.
ms.assetid: 6534d343-d724-46e5-b300-2a29124a1a28
keywords:
- Тип образца HLSL
topic_type:
- apiref
api_name:
- Sampler Type
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: c0206f7030d3b3a05570e74273d9510bb9c2592c
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/30/2021
ms.locfileid: "113119579"
---
# <a name="sampler-type"></a><span data-ttu-id="3ab4b-104">Тип образца</span><span class="sxs-lookup"><span data-stu-id="3ab4b-104">Sampler Type</span></span>

<span data-ttu-id="3ab4b-105">Используйте следующий синтаксис, чтобы объявить состояние образца, а также состояние сравнения образцов.</span><span class="sxs-lookup"><span data-stu-id="3ab4b-105">Use the following syntax to declare sampler state as well as sampler-comparison state.</span></span>



<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="3ab4b-106">Различия между Direct3D 9 и Direct3D 10 и более поздними версиями:</span><span class="sxs-lookup"><span data-stu-id="3ab4b-106">Differences between Direct3D 9 and Direct3D 10 and later:</span></span><br/> <span data-ttu-id="3ab4b-107">Ниже приведен синтаксис для образца в Direct3D 9.</span><span class="sxs-lookup"><span data-stu-id="3ab4b-107">Here is the syntax for a sampler in Direct3D 9.</span></span><br/> 
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="3ab4b-108"><em>имя</em>образца  =  <em>самплертипе</em>{текстура = <<em>texture_variable</em> > ;   [<em>STATE_NAME = state_value;</em>]   ... };</span><span class="sxs-lookup"><span data-stu-id="3ab4b-108">sampler <em>Name</em> = <em>SamplerType</em>{   Texture = <<em>texture_variable</em>>;   [<em>state_name = state_value;</em>]   ... };</span></span></td>
</tr>
</tbody>
</table>

<p> </p>
<p><span data-ttu-id="3ab4b-109">Синтаксис образца для выборки в Direct3D 10 и более поздних версиях немного изменился для поддержки объектов текстуры и массивов выборки.</span><span class="sxs-lookup"><span data-stu-id="3ab4b-109">The syntax for a sampler in Direct3D 10 and later is changed slightly to support texture objects and sampler arrays.</span></span></p>

<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="3ab4b-110"><em>Самплертипе имя [Индекс]</em>{[<em>STATE_NAME = state_value;</em>]   ... };</span><span class="sxs-lookup"><span data-stu-id="3ab4b-110"><em>SamplerType Name[Index]</em>{   [<em>state_name = state_value;</em>]   ... };</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
</tbody>
</table>



 

## <a name="parameters"></a><span data-ttu-id="3ab4b-111">Параметры</span><span class="sxs-lookup"><span data-stu-id="3ab4b-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3ab4b-112"><span id="sampler"></span><span id="SAMPLER"></span>образец</span><span class="sxs-lookup"><span data-stu-id="3ab4b-112"><span id="sampler"></span><span id="SAMPLER"></span>sampler</span></span>
</dt> <dd>

<span data-ttu-id="3ab4b-113">Только Direct3D 9.</span><span class="sxs-lookup"><span data-stu-id="3ab4b-113">Direct3D 9 only.</span></span> <span data-ttu-id="3ab4b-114">Обязательное ключевое слово.</span><span class="sxs-lookup"><span data-stu-id="3ab4b-114">Required keyword.</span></span>

</dd> <dt>

<span data-ttu-id="3ab4b-115"><span id="Name"></span><span id="name"></span><span id="NAME"></span>*Безымян*</span><span class="sxs-lookup"><span data-stu-id="3ab4b-115"><span id="Name"></span><span id="name"></span><span id="NAME"></span>*Name*</span></span>
</dt> <dd>

<span data-ttu-id="3ab4b-116">Строка ASCII, однозначно определяющая имя переменной образца.</span><span class="sxs-lookup"><span data-stu-id="3ab4b-116">ASCII string that uniquely identifies the sampler variable name.</span></span>

</dd> <dt>

<span data-ttu-id="3ab4b-117"><span id="_Index_"></span><span id="_index_"></span><span id="_INDEX_"></span>*\[Номер\]*</span><span class="sxs-lookup"><span data-stu-id="3ab4b-117"><span id="_Index_"></span><span id="_index_"></span><span id="_INDEX_"></span>*\[Index\]*</span></span>
</dt> <dd>

<span data-ttu-id="3ab4b-118">Только Direct3D 10 и более поздние версии.</span><span class="sxs-lookup"><span data-stu-id="3ab4b-118">Direct3D 10 and later only.</span></span> <span data-ttu-id="3ab4b-119">Необязательный размер массива; положительное целое число, которое больше или равно 1.</span><span class="sxs-lookup"><span data-stu-id="3ab4b-119">Optional array size; a positive integer greater than or equal to 1.</span></span>

</dd> <dt>

<span data-ttu-id="3ab4b-120"><span id="SamplerType"></span><span id="samplertype"></span><span id="SAMPLERTYPE"></span>*самплертипе*</span><span class="sxs-lookup"><span data-stu-id="3ab4b-120"><span id="SamplerType"></span><span id="samplertype"></span><span id="SAMPLERTYPE"></span>*SamplerType*</span></span>
</dt> <dd>

<span data-ttu-id="3ab4b-121">\[в \] поле Тип образца выберите одно из следующих: выборка,  *sampler1D*, *sampler2D*, *sampler3D*, *самплеркубе*, *\_ состояние образца*, *самплерстате*.</span><span class="sxs-lookup"><span data-stu-id="3ab4b-121">\[in\] The sampler type, which is one of the following: *sampler*, *sampler1D*, *sampler2D*, *sampler3D*, *samplerCUBE*, *sampler\_state*, *SamplerState*.</span></span>

<span data-ttu-id="3ab4b-122">Различия между Direct3D 9 и Direct3D 10 и более поздними версиями:</span><span class="sxs-lookup"><span data-stu-id="3ab4b-122">Differences between Direct3D 9 and Direct3D 10 and later:</span></span>

- <span data-ttu-id="3ab4b-123">Direct3D 10 и более поздних версий поддерживает один дополнительный тип образца: *самплеркомпарисонстате*.</span><span class="sxs-lookup"><span data-stu-id="3ab4b-123">Direct3D 10 and later supports one additional sampler type: *SamplerComparisonState*.</span></span>



 

</dd> <dt>

<span data-ttu-id="3ab4b-124"><span id="Texture____texture_variable__"></span><span id="texture____texture_variable__"></span><span id="TEXTURE____TEXTURE_VARIABLE__"></span>*Текстура* = <ая *\_ переменная текстуры*>;</span><span class="sxs-lookup"><span data-stu-id="3ab4b-124"><span id="Texture____texture_variable__"></span><span id="texture____texture_variable__"></span><span id="TEXTURE____TEXTURE_VARIABLE__"></span>*Texture* = <*texture\_variable*>;</span></span>
</dt> <dd>

<span data-ttu-id="3ab4b-125">Только Direct3D 9.</span><span class="sxs-lookup"><span data-stu-id="3ab4b-125">Direct3D 9 only.</span></span> <span data-ttu-id="3ab4b-126">Переменная текстуры.</span><span class="sxs-lookup"><span data-stu-id="3ab4b-126">A texture variable.</span></span> <span data-ttu-id="3ab4b-127">Ключевое слово *текстуры* является обязательным в левой части; имя переменной принадлежит правой части выражения в угловых скобках.</span><span class="sxs-lookup"><span data-stu-id="3ab4b-127">The *Texture* keyword is required on the left-hand side; the variable name belongs on the right-hand side of the expression within the angle brackets.</span></span>

</dd> <dt>

<span data-ttu-id="3ab4b-128"><span id="state_name___state_value"></span><span id="STATE_NAME___STATE_VALUE"></span>*State \_ Name = \_ значение State*</span><span class="sxs-lookup"><span data-stu-id="3ab4b-128"><span id="state_name___state_value"></span><span id="STATE_NAME___STATE_VALUE"></span>*state\_name = state\_value*</span></span>
</dt> <dd>

<span data-ttu-id="3ab4b-129">\[При \] необязательном назначении состояний.</span><span class="sxs-lookup"><span data-stu-id="3ab4b-129">\[in\] Optional state assignment(s).</span></span> <span data-ttu-id="3ab4b-130">Левая часть назначения — это имя состояния, правая часть — это значение состояния.</span><span class="sxs-lookup"><span data-stu-id="3ab4b-130">The left hand side of an assignment is a state name, the right hand side is the state value.</span></span> <span data-ttu-id="3ab4b-131">Все назначения состояний должны находиться в блоке операторов (в фигурных скобках).</span><span class="sxs-lookup"><span data-stu-id="3ab4b-131">All state assignments must appear within a statement block (in curly brackets).</span></span> <span data-ttu-id="3ab4b-132">Каждая инструкция отделяется точкой с запятой.</span><span class="sxs-lookup"><span data-stu-id="3ab4b-132">Each statement is separated with a semicolon.</span></span> <span data-ttu-id="3ab4b-133">В следующей таблице перечислены возможные имена состояний.</span><span class="sxs-lookup"><span data-stu-id="3ab4b-133">The following table lists the possible state names.</span></span>


```
// sampler state
AddressU
AddressV
AddressW
BorderColor
Filter
MaxAnisotropy
MaxLOD
MinLOD
MipLODBias

// sampler-comparison state
ComparisonFunc
```



<span data-ttu-id="3ab4b-134">Правая часть каждого выражения — это значение, присваиваемое каждому состоянию.</span><span class="sxs-lookup"><span data-stu-id="3ab4b-134">The right side of each expression is the value assigned to each state.</span></span> <span data-ttu-id="3ab4b-135">Возможные значения состояния для Direct3D 11 см. в разделе [**D3D11 \_ образец \_**](/windows/desktop/api/d3d11/ns-d3d11-d3d11_sampler_desc) в виде структуры.</span><span class="sxs-lookup"><span data-stu-id="3ab4b-135">See the [**D3D11\_SAMPLER\_DESC**](/windows/desktop/api/d3d11/ns-d3d11-d3d11_sampler_desc) structure for the possible state values for Direct3D 11.</span></span> <span data-ttu-id="3ab4b-136">Между именами состояний и элементами структуры существует одна и одна связь.</span><span class="sxs-lookup"><span data-stu-id="3ab4b-136">There is a 1 to 1 relationship between the state names and the members of the structure.</span></span> <span data-ttu-id="3ab4b-137">См. указанный ниже пример.</span><span class="sxs-lookup"><span data-stu-id="3ab4b-137">See the following example.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="3ab4b-138">Remarks</span><span class="sxs-lookup"><span data-stu-id="3ab4b-138">Remarks</span></span>

<span data-ttu-id="3ab4b-139">При реализации воздействия состояние выборки — это один из нескольких типов состояний, которые может потребоваться настроить в конвейере для подготовки к просмотру.</span><span class="sxs-lookup"><span data-stu-id="3ab4b-139">When you implement an effect, sampler state is one of several types of state that you might need to set up in the pipeline for rendering.</span></span> <span data-ttu-id="3ab4b-140">Список всех возможных состояний, которые можно установить в результате, см. в следующих статьях:</span><span class="sxs-lookup"><span data-stu-id="3ab4b-140">For a list of all the possible states that you can set in an effect, see:</span></span>

-   <span data-ttu-id="3ab4b-141">В Direct3D 10 используются [группы состояний](/windows/desktop/direct3d10/d3d10-effect-states).</span><span class="sxs-lookup"><span data-stu-id="3ab4b-141">Direct3D 10 uses [state groups](/windows/desktop/direct3d10/d3d10-effect-states).</span></span>
-   <span data-ttu-id="3ab4b-142">Direct3D 9 использует индивидуальные [состояния](/windows/desktop/direct3d9/effect-states).</span><span class="sxs-lookup"><span data-stu-id="3ab4b-142">Direct3D 9 uses individual [states](/windows/desktop/direct3d9/effect-states).</span></span>

## <a name="example"></a><span data-ttu-id="3ab4b-143">Пример</span><span class="sxs-lookup"><span data-stu-id="3ab4b-143">Example</span></span>



<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="3ab4b-144">Различия между Direct3D 9 и Direct3D 10:</span><span class="sxs-lookup"><span data-stu-id="3ab4b-144">Differences between Direct3D 9 and Direct3D 10:</span></span><br/> <span data-ttu-id="3ab4b-145">Ниже приведен частичный пример образца Direct3D 9 из <a href="https://msdn.microsoft.com/library/Ee416223(v=VS.85).aspx">примера басичлсл</a>.</span><span class="sxs-lookup"><span data-stu-id="3ab4b-145">Here is a partial example of a Direct3D 9 sampler from <a href="https://msdn.microsoft.com/library/Ee416223(v=VS.85).aspx">BasicHLSL Sample</a>.</span></span><br/> <span data-codelanguage=""></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><pre><code>sampler MeshTextureSampler = 
sampler_state
{
    Texture = <g_MeshTexture>;
    MipFilter = LINEAR;
    MinFilter = LINEAR;
    MagFilter = LINEAR;
};</code></pre></td>
</tr>
</tbody>
</table>

<p><span data-ttu-id="3ab4b-146">Ниже приведен частичный пример образца Direct3D 10 из <a href="https://msdn.microsoft.com/library/Ee416395(v=VS.85).aspx">примера BasicHLSL10</a>.</span><span class="sxs-lookup"><span data-stu-id="3ab4b-146">Here is a partial example of a Direct3D 10 sampler from <a href="https://msdn.microsoft.com/library/Ee416395(v=VS.85).aspx">BasicHLSL10 Sample</a>.</span></span></p>
<div class="code">
<span data-codelanguage=""></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><pre><code>SamplerState MeshTextureSampler
{
    Filter = MIN_MAG_MIP_LINEAR;
    AddressU = Wrap;
    AddressV = Wrap;
};</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="3ab4b-147">Ниже приведен частичный пример объявления состояния сравнения образцов и вызова образца сравнения в Direct3D 10.</span><span class="sxs-lookup"><span data-stu-id="3ab4b-147">Here is a partial example of declaring sampler-comparison state, and calling a comparison sampler in Direct3D 10.</span></span>


```
SamplerComparisonState ShadowSampler
{
   // sampler state
   Filter = COMPARISON_MIN_MAG_LINEAR_MIP_POINT;
   AddressU = MIRROR;
   AddressV = MIRROR;

   // sampler comparison state
   ComparisonFunc = LESS;
};
        
float3 vModProjUV;
  ...
float fShadow = g_ShadowMap.SampleCmpLevelZero( ShadowSampler, vModProjUV.xy, vModProjUV.z);
```



## <a name="see-also"></a><span data-ttu-id="3ab4b-148">См. также</span><span class="sxs-lookup"><span data-stu-id="3ab4b-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3ab4b-149">Типы данных (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="3ab4b-149">Data Types (DirectX HLSL)</span></span>](dx-graphics-hlsl-data-types.md)
</dt> </dl>

 

