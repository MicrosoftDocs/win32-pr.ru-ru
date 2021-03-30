---
title: Постоянный целочисленный регистр (Справочник по HLSL PS)
description: Постоянные целочисленные регистры используются только для Loop-PS и представителя-PS.
ms.assetid: 85720ec0-b6aa-4a24-910c-3ad0468300dc
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 9b03a27a95f84ae30a70147caaf5662e1949cf18
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104984037"
---
# <a name="constant-integer-register-hlsl-ps-reference"></a><span data-ttu-id="bfcc4-103">Постоянный целочисленный регистр (Справочник по HLSL PS)</span><span class="sxs-lookup"><span data-stu-id="bfcc4-103">Constant integer register (HLSL PS reference)</span></span>

<span data-ttu-id="bfcc4-104">Постоянные целочисленные регистры используются только для [Loop-PS](loop---ps.md) и [представителя-PS](rep---ps.md).</span><span class="sxs-lookup"><span data-stu-id="bfcc4-104">Constant integer registers are used only by [loop - ps](loop---ps.md) and [rep - ps](rep---ps.md).</span></span>

<span data-ttu-id="bfcc4-105">Их можно задать с помощью [дефи-PS](defi---ps.md) или [**сетпикселшадерконстанти**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setpixelshaderconstanti).</span><span class="sxs-lookup"><span data-stu-id="bfcc4-105">They can be set using [defi - ps](defi---ps.md) or [**SetPixelShaderConstantI**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setpixelshaderconstanti).</span></span>

<span data-ttu-id="bfcc4-106">При использовании в качестве аргумента для инструкции [Loop-PS](loop---ps.md) :</span><span class="sxs-lookup"><span data-stu-id="bfcc4-106">When used as an argument to the [loop - ps](loop---ps.md) instruction:</span></span>

-   <span data-ttu-id="bfcc4-107">. x — это число итераций.</span><span class="sxs-lookup"><span data-stu-id="bfcc4-107">.x is the iteration count.</span></span> <span data-ttu-id="bfcc4-108">([представитель-PS](rep---ps.md) использует только этот компонент).</span><span class="sxs-lookup"><span data-stu-id="bfcc4-108">([rep - ps](rep---ps.md) uses only this component).</span></span>
-   <span data-ttu-id="bfcc4-109">. y — это начальное значение счетчика цикла.</span><span class="sxs-lookup"><span data-stu-id="bfcc4-109">.y is the initial value for the loop counter.</span></span>
-   <span data-ttu-id="bfcc4-110">. z — шаг приращения счетчика циклов.</span><span class="sxs-lookup"><span data-stu-id="bfcc4-110">.z is the increment step for the loop counter.</span></span>



| <span data-ttu-id="bfcc4-111">Версии шейдеров пикселей</span><span class="sxs-lookup"><span data-stu-id="bfcc4-111">Pixel shader versions</span></span>     | <span data-ttu-id="bfcc4-112">1\_1</span><span class="sxs-lookup"><span data-stu-id="bfcc4-112">1\_1</span></span> | <span data-ttu-id="bfcc4-113">1\_2</span><span class="sxs-lookup"><span data-stu-id="bfcc4-113">1\_2</span></span> | <span data-ttu-id="bfcc4-114">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="bfcc4-114">1\_3</span></span> | <span data-ttu-id="bfcc4-115">1\_4</span><span class="sxs-lookup"><span data-stu-id="bfcc4-115">1\_4</span></span> | <span data-ttu-id="bfcc4-116">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="bfcc4-116">2\_0</span></span> | <span data-ttu-id="bfcc4-117">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="bfcc4-117">2\_sw</span></span> | <span data-ttu-id="bfcc4-118">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="bfcc4-118">2\_x</span></span> | <span data-ttu-id="bfcc4-119">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="bfcc4-119">3\_0</span></span> | <span data-ttu-id="bfcc4-120">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="bfcc4-120">3\_sw</span></span> |
|---------------------------|------|------|------|------|------|-------|------|------|-------|
| <span data-ttu-id="bfcc4-121">Постоянный целочисленный регистр</span><span class="sxs-lookup"><span data-stu-id="bfcc4-121">Constant Integer Register</span></span> |      |      |      |      |      |       | <span data-ttu-id="bfcc4-122">x</span><span class="sxs-lookup"><span data-stu-id="bfcc4-122">x</span></span>    | <span data-ttu-id="bfcc4-123">x</span><span class="sxs-lookup"><span data-stu-id="bfcc4-123">x</span></span>    | <span data-ttu-id="bfcc4-124">x</span><span class="sxs-lookup"><span data-stu-id="bfcc4-124">x</span></span>     |



 

<span data-ttu-id="bfcc4-125">Поведение констант шейдера изменилось между Direct3D 8 и Direct3D 9.</span><span class="sxs-lookup"><span data-stu-id="bfcc4-125">The behavior of shader constants has changed between Direct3D 8 and Direct3D 9.</span></span>

-   <span data-ttu-id="bfcc4-126">Для Direct3D 9 константы, заданные с помощью дефкс, присваивают значения константному пространству шейдера.</span><span class="sxs-lookup"><span data-stu-id="bfcc4-126">For Direct3D 9, constants set with defx assign values to the shader constant space.</span></span> <span data-ttu-id="bfcc4-127">Время существования константы, объявленной с помощью дефкс, ограничено выполнением только этого шейдера.</span><span class="sxs-lookup"><span data-stu-id="bfcc4-127">The lifetime of a constant declared with defx is confined to the execution of that shader only.</span></span> <span data-ttu-id="bfcc4-128">И наоборот, константы, заданные с помощью API-интерфейсов, Сетксксксшадерконстанткс инициализировать константы в глобальном пространстве.</span><span class="sxs-lookup"><span data-stu-id="bfcc4-128">Conversely, constants set using the APIs SetXXXShaderConstantX initialize constants in global space.</span></span> <span data-ttu-id="bfcc4-129">Константы в глобальном пространстве не копируются в локальное пространство (видимую шейдеру) до тех пор, пока не будет вызван Сетксксксшадерконстантс.</span><span class="sxs-lookup"><span data-stu-id="bfcc4-129">Constants in global space are not copied to local space (visible to the shader) until SetxxxShaderConstants is called.</span></span>
-   <span data-ttu-id="bfcc4-130">Для Direct3D 8 константы, заданные с помощью дефкс или API, присваивают значения константному пространству шейдера.</span><span class="sxs-lookup"><span data-stu-id="bfcc4-130">For Direct3D 8, constants set with defx or the APIs both assign values to the shader constant space.</span></span> <span data-ttu-id="bfcc4-131">При каждом выполнении шейдера все константы используются текущим шейдером независимо от метода, используемого для их установки.</span><span class="sxs-lookup"><span data-stu-id="bfcc4-131">Each time the shader is executed, the constants are used by the current shader regardless of the technique used to set them.</span></span>

## <a name="related-topics"></a><span data-ttu-id="bfcc4-132">См. также</span><span class="sxs-lookup"><span data-stu-id="bfcc4-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bfcc4-133">Регистры</span><span class="sxs-lookup"><span data-stu-id="bfcc4-133">Registers</span></span>](dx9-graphics-reference-asm-ps-registers.md)
</dt> </dl>

 

 