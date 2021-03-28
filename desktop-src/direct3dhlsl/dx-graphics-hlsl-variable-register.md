---
title: регистрация
description: регистрация
ms.assetid: 45149f8c-8b76-4247-98d7-d141d7268da3
keywords:
- регистрация HLSL
topic_type:
- apiref
api_name:
- register
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 2b378cd97bc9779951d62873d393009c98d32823
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104412992"
---
# <a name="register"></a><span data-ttu-id="4cdd8-104">регистрация</span><span class="sxs-lookup"><span data-stu-id="4cdd8-104">register</span></span>

<span data-ttu-id="4cdd8-105">Необязательное ключевое слово для назначения переменной шейдера конкретному регистру, в котором используется следующий синтаксис:</span><span class="sxs-lookup"><span data-stu-id="4cdd8-105">Optional keyword for assigning a shader variable to a particular register, which uses the following syntax:</span></span>



| <span data-ttu-id="4cdd8-106">: Register ( *\[ \_ профиль \] шейдера*, \* \# \[ \] подкомпонент типа\* )</span><span class="sxs-lookup"><span data-stu-id="4cdd8-106">: register ( *\[shader\_profile\]*, *Type\#\[subcomponent\]* )</span></span> |
|----------------------------------------------------------------|



 

## <a name="parameters"></a><span data-ttu-id="4cdd8-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="4cdd8-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4cdd8-108"><span id="register"></span><span id="REGISTER"></span>зарегистрировать</span><span class="sxs-lookup"><span data-stu-id="4cdd8-108"><span id="register"></span><span id="REGISTER"></span>register</span></span>
</dt> <dd>

<span data-ttu-id="4cdd8-109">Обязательное ключевое слово.</span><span class="sxs-lookup"><span data-stu-id="4cdd8-109">Required keyword.</span></span>

</dd> <dt>

<span data-ttu-id="4cdd8-110"><span id="_shader_profile_"></span><span id="_SHADER_PROFILE_"></span>*\[Профиль шейдера \_\]*</span><span class="sxs-lookup"><span data-stu-id="4cdd8-110"><span id="_shader_profile_"></span><span id="_SHADER_PROFILE_"></span>*\[shader\_profile\]*</span></span>
</dt> <dd>

<span data-ttu-id="4cdd8-111">Необязательный [профиль шейдера](/windows/desktop/direct3dtools/dx-graphics-tools-fxc-syntax), который может быть целевым объектом шейдера или просто **PS** или **VS**.</span><span class="sxs-lookup"><span data-stu-id="4cdd8-111">Optional [shader profile](/windows/desktop/direct3dtools/dx-graphics-tools-fxc-syntax), which can be a shader target or simply **ps** or **vs**.</span></span>

</dd> <dt>

<span data-ttu-id="4cdd8-112"><span id="Type__subcomponent_"></span><span id="type__subcomponent_"></span><span id="TYPE__SUBCOMPONENT_"></span>*Подкомпонент типа \# \[\]*</span><span class="sxs-lookup"><span data-stu-id="4cdd8-112"><span id="Type__subcomponent_"></span><span id="type__subcomponent_"></span><span id="TYPE__SUBCOMPONENT_"></span>*Type\#\[subcomponent\]*</span></span>
</dt> <dd>

<span data-ttu-id="4cdd8-113">Объявление типа, числа и подкомпонентов.</span><span class="sxs-lookup"><span data-stu-id="4cdd8-113">Register type, number, and subcomponent declaration.</span></span>

-   <span data-ttu-id="4cdd8-114">Тип является одним из следующих:</span><span class="sxs-lookup"><span data-stu-id="4cdd8-114">Type is one of the following:</span></span>

    

    | <span data-ttu-id="4cdd8-115">Тип</span><span class="sxs-lookup"><span data-stu-id="4cdd8-115">Type</span></span> | <span data-ttu-id="4cdd8-116">Описание регистра</span><span class="sxs-lookup"><span data-stu-id="4cdd8-116">Register Description</span></span>       |
    |------|----------------------------|
    | <span data-ttu-id="4cdd8-117">b</span><span class="sxs-lookup"><span data-stu-id="4cdd8-117">b</span></span>    | <span data-ttu-id="4cdd8-118">Буфер констант</span><span class="sxs-lookup"><span data-stu-id="4cdd8-118">Constant buffer</span></span>            |
    | <span data-ttu-id="4cdd8-119">t</span><span class="sxs-lookup"><span data-stu-id="4cdd8-119">t</span></span>    | <span data-ttu-id="4cdd8-120">Текстура и буфер текстуры</span><span class="sxs-lookup"><span data-stu-id="4cdd8-120">Texture and texture buffer</span></span> |
    | <span data-ttu-id="4cdd8-121">c</span><span class="sxs-lookup"><span data-stu-id="4cdd8-121">c</span></span>    | <span data-ttu-id="4cdd8-122">Смещение буфера</span><span class="sxs-lookup"><span data-stu-id="4cdd8-122">Buffer offset</span></span>              |
    | <span data-ttu-id="4cdd8-123">s</span><span class="sxs-lookup"><span data-stu-id="4cdd8-123">s</span></span>    | <span data-ttu-id="4cdd8-124">Образец</span><span class="sxs-lookup"><span data-stu-id="4cdd8-124">Sampler</span></span>                    |
    | <span data-ttu-id="4cdd8-125">u</span><span class="sxs-lookup"><span data-stu-id="4cdd8-125">u</span></span>    | <span data-ttu-id="4cdd8-126">Представление неупорядоченного доступа</span><span class="sxs-lookup"><span data-stu-id="4cdd8-126">Unordered Access View</span></span>      |

    

     

-   <span data-ttu-id="4cdd8-127">*\#* номер регистра, который является целым числом.</span><span class="sxs-lookup"><span data-stu-id="4cdd8-127">*\#* is the register number, which is an integer number.</span></span>
-   <span data-ttu-id="4cdd8-128">*Подкомпонентом* является Необязательное целое число.</span><span class="sxs-lookup"><span data-stu-id="4cdd8-128">The *subcomponent* is an optional integer number.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="4cdd8-129">Примечания</span><span class="sxs-lookup"><span data-stu-id="4cdd8-129">Remarks</span></span>

<span data-ttu-id="4cdd8-130">Вы можете добавить одно или несколько назначений Register в одно и то же объявление переменной, разделяя их пробелами.</span><span class="sxs-lookup"><span data-stu-id="4cdd8-130">You may add one or more register assignments to the same variable declaration, separated by spaces.</span></span>

<span data-ttu-id="4cdd8-131">Для переменных Direct3D 10 в глобальной области ключевое слово **Register** действует так же, как и ключевое слово [ПАККОФФСЕТ (DirectX HLSL)](dx-graphics-hlsl-variable-packoffset.md) .</span><span class="sxs-lookup"><span data-stu-id="4cdd8-131">For Direct3D 10 variables in global scope, the **register** keyword acts the same as the [packoffset (DirectX HLSL)](dx-graphics-hlsl-variable-packoffset.md) keyword.</span></span>

## <a name="examples"></a><span data-ttu-id="4cdd8-132">Примеры</span><span class="sxs-lookup"><span data-stu-id="4cdd8-132">Examples</span></span>

<span data-ttu-id="4cdd8-133">Ниже приводится несколько примеров.</span><span class="sxs-lookup"><span data-stu-id="4cdd8-133">Here are some examples:</span></span>


```
sampler myVar : register( ps_5_0, s ); 
```




```
sampler myVar : register( vs, s[8] );
```




```
sampler myVar : register( ps, s[2] ) 
              : register( ps_5_0, s[0] ) 
              : register( vs, s[8] );
```



## <a name="see-also"></a><span data-ttu-id="4cdd8-134">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="4cdd8-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4cdd8-135">Синтаксис переменных</span><span class="sxs-lookup"><span data-stu-id="4cdd8-135">Variable Syntax</span></span>](dx-graphics-hlsl-variable-syntax.md)
</dt> <dt>

[<span data-ttu-id="4cdd8-136">Переменные (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="4cdd8-136">Variables (DirectX HLSL)</span></span>](dx-graphics-hlsl-variables.md)
</dt> </dl>

 

 