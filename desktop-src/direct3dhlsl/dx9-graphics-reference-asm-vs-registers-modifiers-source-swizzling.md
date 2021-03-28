---
title: Исходный регистр группирующие (HLSL VS Reference)
description: Перед выполнением инструкции данные в исходном регистре копируются во временную регистрацию. Группирующие означает возможность копирования любого компонента регистрации источника в любой временный компонент регистрации. Группирующие не влияет на данные регистра источника.
ms.assetid: 6271d846-c68d-467c-a110-be3279e0c11a
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: c075d8ff47b1f76adf378b6a583cd4d675651a87
ms.sourcegitcommit: cba7f424a292fd7f3a8518947b9466439b455419
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/23/2019
ms.locfileid: "104412261"
---
# <a name="source-register-swizzling-hlsl-vs-reference"></a><span data-ttu-id="95d03-105">Исходный регистр группирующие (HLSL VS Reference)</span><span class="sxs-lookup"><span data-stu-id="95d03-105">Source Register Swizzling (HLSL VS reference)</span></span>

<span data-ttu-id="95d03-106">Перед выполнением инструкции данные в исходном регистре копируются во временную регистрацию.</span><span class="sxs-lookup"><span data-stu-id="95d03-106">Before an instruction runs, the data in a source register is copied to a temporary register.</span></span> <span data-ttu-id="95d03-107">Группирующие означает возможность копирования любого компонента регистрации источника в любой временный компонент регистрации.</span><span class="sxs-lookup"><span data-stu-id="95d03-107">Swizzling refers to the ability to copy any source register component to any temporary register component.</span></span> <span data-ttu-id="95d03-108">Группирующие не влияет на данные регистра источника.</span><span class="sxs-lookup"><span data-stu-id="95d03-108">Swizzling does not affect the source register data.</span></span>

## <a name="component-swizzling"></a><span data-ttu-id="95d03-109">Группирующие компонентов</span><span class="sxs-lookup"><span data-stu-id="95d03-109">Component Swizzling</span></span>

<span data-ttu-id="95d03-110">Как показано в следующей таблице, группирующие можно применить к отдельным компонентам исходных данных регистра (где — это один из допустимых входных реестров шейдера вершин [— VS \_ 1 \_ 1](dx9-graphics-reference-asm-vs-registers-vs-1-1.md)).</span><span class="sxs-lookup"><span data-stu-id="95d03-110">As shown in the following table, swizzling can be applied to the individual components of the source register data (where r is one of the valid vertex shader input [Registers - vs\_1\_1](dx9-graphics-reference-asm-vs-registers-vs-1-1.md)).</span></span>



| <span data-ttu-id="95d03-111">Модификатор компонента</span><span class="sxs-lookup"><span data-stu-id="95d03-111">Component modifier</span></span>                 | <span data-ttu-id="95d03-112">Описание</span><span class="sxs-lookup"><span data-stu-id="95d03-112">Description</span></span>    |
|------------------------------------|----------------|
| <span data-ttu-id="95d03-113">r. \[ ксизв \] \[ ксизв \] \[ ксизв \] \[ ксизв\]</span><span class="sxs-lookup"><span data-stu-id="95d03-113">r.\[xyzw\]\[xyzw\]\[xyzw\]\[xyzw\]</span></span> | <span data-ttu-id="95d03-114">Исходный свиззле</span><span class="sxs-lookup"><span data-stu-id="95d03-114">Source swizzle</span></span> |



 

-   <span data-ttu-id="95d03-115">Все четыре компонента всегда копируются.</span><span class="sxs-lookup"><span data-stu-id="95d03-115">All four components are always copied.</span></span> <span data-ttu-id="95d03-116">Если указано менее четырех компонентов, последний компонент повторяется (XY означает. КсИИИ).</span><span class="sxs-lookup"><span data-stu-id="95d03-116">If fewer than four components are specified, the last component is repeated (xy means .xyyy).</span></span> <span data-ttu-id="95d03-117">Если компоненты не указаны, x повторяется (. xxxx).</span><span class="sxs-lookup"><span data-stu-id="95d03-117">If no components are specified, x is repeated (.xxxx).</span></span>
-   <span data-ttu-id="95d03-118">Компоненты могут отображаться в любом порядке.</span><span class="sxs-lookup"><span data-stu-id="95d03-118">The components can appear in any order.</span></span> <span data-ttu-id="95d03-119">v0. ивкс приводит к v0. ивкскс.</span><span class="sxs-lookup"><span data-stu-id="95d03-119">v0.ywx results in v0.ywxx.</span></span>
-   <span data-ttu-id="95d03-120">Компоненты RGBA можно использовать соответственно для ксизв (r для x, g для b и т. д.).</span><span class="sxs-lookup"><span data-stu-id="95d03-120">The rgba components can be used respectively for xyzw (r for x, g for b, etc.).</span></span>
-   <span data-ttu-id="95d03-121">Эти инструкции реализуют один компонент свиззлес: EXP, експп, log, логп, pow, rcp, РСК.</span><span class="sxs-lookup"><span data-stu-id="95d03-121">These instructions implement source-register single component swizzles: exp, expp, log, logp, pow, rcp, rsq.</span></span> <span data-ttu-id="95d03-122">Результат этих инструкций копируется во все четыре компонента регистрации назначения.</span><span class="sxs-lookup"><span data-stu-id="95d03-122">The result of these instructions is copied to all four destination register components.</span></span>

<span data-ttu-id="95d03-123">Группирующие нельзя использовать в инструкциях [m3x2-VS](m3x2---vs.md), [m3x3-VS](m3x3---vs.md), [m4x3-VS](m4x3---vs.md)и [m4x4-VS](m4x4---vs.md) .</span><span class="sxs-lookup"><span data-stu-id="95d03-123">Swizzling cannot be used on the [m3x2 - vs](m3x2---vs.md), [m3x3 - vs](m3x3---vs.md), [m4x3 - vs](m4x3---vs.md), and [m4x4 - vs](m4x4---vs.md) instructions.</span></span>

## <a name="related-topics"></a><span data-ttu-id="95d03-124">См. также</span><span class="sxs-lookup"><span data-stu-id="95d03-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="95d03-125">Модификаторы регистра для шейдера вершин</span><span class="sxs-lookup"><span data-stu-id="95d03-125">Vertex Shader Register Modifiers</span></span>](dx9-graphics-reference-asm-vs-registers-modifiers.md)
</dt> </dl>

 

 




