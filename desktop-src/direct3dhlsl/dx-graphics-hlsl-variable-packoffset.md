---
title: паккоффсет
description: Необязательное ключевое слово упаковки константы шейдера, которое использует следующий синтаксис
ms.assetid: f0a3031b-d385-430d-83ee-7a8142334ad7
keywords:
- паккоффсет HLSL
topic_type:
- apiref
api_name:
- packoffset
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 5c92a6375f0724a1910fc0f09b47e1593614f9f1
ms.sourcegitcommit: adba238660d8a5f4fe98fc6f5d105d56aac3a400
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/09/2021
ms.locfileid: "111826083"
---
# <a name="packoffset"></a><span data-ttu-id="5a6cc-104">паккоффсет</span><span class="sxs-lookup"><span data-stu-id="5a6cc-104">packoffset</span></span>

<span data-ttu-id="5a6cc-105">Необязательное ключевое слово упаковки константы шейдера, которое использует следующий синтаксис:</span><span class="sxs-lookup"><span data-stu-id="5a6cc-105">Optional shader constant packing keyword, which uses the following syntax:</span></span>

<span data-ttu-id="5a6cc-106">: паккоффсет (компонент вспомогательного компонента в c \[ \] \[ \] )</span><span class="sxs-lookup"><span data-stu-id="5a6cc-106">: packoffset( c\[Subcomponent\]\[.component\] )</span></span>



 

## <a name="parameters"></a><span data-ttu-id="5a6cc-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="5a6cc-107">Parameters</span></span>



| <span data-ttu-id="5a6cc-108">Элемент</span><span class="sxs-lookup"><span data-stu-id="5a6cc-108">Item</span></span>                                                                                                                                                                                 | <span data-ttu-id="5a6cc-109">Описание</span><span class="sxs-lookup"><span data-stu-id="5a6cc-109">Description</span></span>                                                                                                                                          |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5a6cc-110"><span id="packoffset"></span><span id="PACKOFFSET"></span>**паккоффсет**</span><span class="sxs-lookup"><span data-stu-id="5a6cc-110"><span id="packoffset"></span><span id="PACKOFFSET"></span>**packoffset**</span></span><br/>                                                                                                  | <span data-ttu-id="5a6cc-111">Обязательное ключевое слово.</span><span class="sxs-lookup"><span data-stu-id="5a6cc-111">Required keyword.</span></span><br/>                                                                                                                         |
| <span data-ttu-id="5a6cc-112"><span id="c"></span><span id="C"></span>**ц**</span><span class="sxs-lookup"><span data-stu-id="5a6cc-112"><span id="c"></span><span id="C"></span>**c**</span></span><br/>                                                                                                                             | <span data-ttu-id="5a6cc-113">Упаковка применяется только к постоянным регистрам (c).</span><span class="sxs-lookup"><span data-stu-id="5a6cc-113">Packing applies to constant registers (c) only.</span></span> <br/>                                                                                          |
| <span data-ttu-id="5a6cc-114"><span id="_Subcomponent__.component_"></span><span id="_subcomponent__.component_"></span><span id="_SUBCOMPONENT__.COMPONENT_"></span>**\[Компонент Components \] \[ . Component\]**</span><span class="sxs-lookup"><span data-stu-id="5a6cc-114"><span id="_Subcomponent__.component_"></span><span id="_subcomponent__.component_"></span><span id="_SUBCOMPONENT__.COMPONENT_"></span>**\[Subcomponent\]\[.component\]**</span></span><br/> | <span data-ttu-id="5a6cc-115">Необязательные подкомпоненты и компоненты.</span><span class="sxs-lookup"><span data-stu-id="5a6cc-115">Optional subcomponents and components.</span></span> <span data-ttu-id="5a6cc-116">Подкомпонент — это номер регистра, который является целым числом.</span><span class="sxs-lookup"><span data-stu-id="5a6cc-116">A subcomponent is a register number, which is an integer.</span></span> <span data-ttu-id="5a6cc-117">Компонент имеет формат \[ . ксизв \] .</span><span class="sxs-lookup"><span data-stu-id="5a6cc-117">A component is in the form of \[.xyzw\].</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="5a6cc-118">Remarks</span><span class="sxs-lookup"><span data-stu-id="5a6cc-118">Remarks</span></span>

<span data-ttu-id="5a6cc-119">Используйте это ключевое слово для упаковки константы шейдера вручную при [объявлении типа переменной](dx-graphics-hlsl-variable-syntax.md).</span><span class="sxs-lookup"><span data-stu-id="5a6cc-119">Use this keyword to manually pack a shader constant when [declaring a variable type](dx-graphics-hlsl-variable-syntax.md).</span></span>

<span data-ttu-id="5a6cc-120">При упаковке константы нельзя смешивать типы констант.</span><span class="sxs-lookup"><span data-stu-id="5a6cc-120">When packing a constant, you cannot mix constant types.</span></span>

<span data-ttu-id="5a6cc-121">Компилятор ведет себя несколько иначе для глобальных констант и универсальных констант:</span><span class="sxs-lookup"><span data-stu-id="5a6cc-121">The compiler behaves slightly differently for global constants and uniform constants:</span></span>

-   <span data-ttu-id="5a6cc-122">Глобальная константа.</span><span class="sxs-lookup"><span data-stu-id="5a6cc-122">A global constant.</span></span> <span data-ttu-id="5a6cc-123">Глобальная переменная добавляется в качестве глобальной константы в *$Global* кбуффер компилятором.</span><span class="sxs-lookup"><span data-stu-id="5a6cc-123">A global variable is added as a global constant to a *$Global* cbuffer by the compiler.</span></span> <span data-ttu-id="5a6cc-124">Автоматически Упакованные элементы (объявленные без паккоффсет) будут отображаться после последней перефасованной переменной вручную.</span><span class="sxs-lookup"><span data-stu-id="5a6cc-124">Automatically packed elements (those declared without packoffset) will appear after the last manually packed variable.</span></span> <span data-ttu-id="5a6cc-125">Вы можете смешивать типы при упаковке глобальных констант.</span><span class="sxs-lookup"><span data-stu-id="5a6cc-125">You may mix types when packing global constants.</span></span>
-   <span data-ttu-id="5a6cc-126">Универсальная константа.</span><span class="sxs-lookup"><span data-stu-id="5a6cc-126">A uniform constant.</span></span> <span data-ttu-id="5a6cc-127">Универсальный параметр в списке параметров функции будет добавлен в *$param* буфер константы компилятором при компиляции шейдера вне платформы Effects.</span><span class="sxs-lookup"><span data-stu-id="5a6cc-127">A uniform parameter in the parameter list of a function will be added to a *$Param* constant buffer by the compiler when the shader is compiled outside of the effects framework.</span></span> <span data-ttu-id="5a6cc-128">При компиляции внутри платформы Effects универсальная константа должна разрешаться в универсальную переменную, определенную в глобальной области.</span><span class="sxs-lookup"><span data-stu-id="5a6cc-128">When compiled inside the effect framework, a uniform constant must resolve to a uniform variable defined in global scope.</span></span> <span data-ttu-id="5a6cc-129">Однородная константа не может быть смещена вручную; их рекомендуется использовать только для специализации шейдеров, где они применяют псевдоним к глобальным, а не к средствам передачи данных приложения в шейдер.</span><span class="sxs-lookup"><span data-stu-id="5a6cc-129">A uniform constant cannot be manually offset; their recommend use is only for specialization of shaders where they alias back to globals, not as a means of passing application data into the shader.</span></span>

<span data-ttu-id="5a6cc-130">Ниже приведены некоторые дополнительные примеры: [константы упаковки с использованием модели шейдеров 4](dx-graphics-hlsl-packing-rules.md).</span><span class="sxs-lookup"><span data-stu-id="5a6cc-130">Here are some additional examples: [packing constants using shader model 4](dx-graphics-hlsl-packing-rules.md).</span></span>

## <a name="examples"></a><span data-ttu-id="5a6cc-131">Примеры</span><span class="sxs-lookup"><span data-stu-id="5a6cc-131">Examples</span></span>

<span data-ttu-id="5a6cc-132">Ниже приведено несколько примеров констант шейдера упаковки вручную.</span><span class="sxs-lookup"><span data-stu-id="5a6cc-132">Here are several examples of manually packing shader constants.</span></span>

<span data-ttu-id="5a6cc-133">Упаковка подкомпонентов векторов и скаляров, размер которых достаточно велик для предотвращения пересечения границ регистров.</span><span class="sxs-lookup"><span data-stu-id="5a6cc-133">Pack subcomponents of vectors and scalars whose size is large enough to prevent crossing register boundaries.</span></span> <span data-ttu-id="5a6cc-134">Например, все они допустимы:</span><span class="sxs-lookup"><span data-stu-id="5a6cc-134">For example, these are all valid:</span></span>


```
cbuffer MyBuffer
{
    float4 Element1 : packoffset(c0);
    float1 Element2 : packoffset(c1);
    float1 Element3 : packoffset(c1.y);
}
```



## <a name="see-also"></a><span data-ttu-id="5a6cc-135">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="5a6cc-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5a6cc-136">Синтаксис переменных</span><span class="sxs-lookup"><span data-stu-id="5a6cc-136">Variable Syntax</span></span>](dx-graphics-hlsl-variable-syntax.md)
</dt> <dt>

[<span data-ttu-id="5a6cc-137">Переменные (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="5a6cc-137">Variables (DirectX HLSL)</span></span>](dx-graphics-hlsl-variables.md)
</dt> </dl>

 

 





