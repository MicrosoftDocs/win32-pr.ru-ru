---
title: Маска записи целевого регистра
description: Маска записи определяет, какие компоненты регистра назначения записываются после завершения инструкции.
ms.assetid: 376a28c8-8a88-4807-a8ab-f59448d965e8
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 80f649770b84174dbb716967e9d941034c3966f5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103986845"
---
# <a name="destination-register-write-mask"></a><span data-ttu-id="af316-103">Маска записи целевого регистра</span><span class="sxs-lookup"><span data-stu-id="af316-103">Destination Register Write Mask</span></span>

<span data-ttu-id="af316-104">Маска записи определяет, какие компоненты регистра назначения записываются после завершения инструкции.</span><span class="sxs-lookup"><span data-stu-id="af316-104">A write mask controls which components of a destination register are written after an instruction is completed.</span></span> <span data-ttu-id="af316-105">Выходная маска записи разрешается, пока компоненты находятся в порядке. RGBA или. ксизв.</span><span class="sxs-lookup"><span data-stu-id="af316-105">An output write mask is allowed as long as the components are in the order of .rgba or .xyzw.</span></span> <span data-ttu-id="af316-106">То есть,. роль и. КСВ являются допустимыми масками.</span><span class="sxs-lookup"><span data-stu-id="af316-106">That is, .rba and .xw are valid masks.</span></span> <span data-ttu-id="af316-107">Регистры текстур имеют один набор правил и регистры, не связанные с текстурой, имеют еще один набор правил.</span><span class="sxs-lookup"><span data-stu-id="af316-107">Texture registers have one set of rules and non-texture registers have another set of rules.</span></span>

## <a name="syntax"></a><span data-ttu-id="af316-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="af316-108">Syntax</span></span>



| <span data-ttu-id="af316-109">DST. вритемаск</span><span class="sxs-lookup"><span data-stu-id="af316-109">dst.writemask</span></span> |
|---------------|



 

<span data-ttu-id="af316-110">где</span><span class="sxs-lookup"><span data-stu-id="af316-110">where</span></span>

-   <span data-ttu-id="af316-111">DST — это регистр назначения.</span><span class="sxs-lookup"><span data-stu-id="af316-111">dst is a destination register.</span></span>
-   <span data-ttu-id="af316-112">вритемаск — это последовательность масок из любого набора: (x, y, z, w) или (красный, зеленый, синий, альфа).</span><span class="sxs-lookup"><span data-stu-id="af316-112">writemask is a sequence of masks from either set: (x,y,z,w) or (red, green, blue, alpha).</span></span>

## <a name="remarks"></a><span data-ttu-id="af316-113">Примечания</span><span class="sxs-lookup"><span data-stu-id="af316-113">Remarks</span></span>

<span data-ttu-id="af316-114">Доступны следующие целевые маски записи.</span><span class="sxs-lookup"><span data-stu-id="af316-114">The following destination write masks are available.</span></span>



| <span data-ttu-id="af316-115">Версии шейдеров пикселей</span><span class="sxs-lookup"><span data-stu-id="af316-115">Pixel shader versions</span></span> | <span data-ttu-id="af316-116">1\_1</span><span class="sxs-lookup"><span data-stu-id="af316-116">1\_1</span></span> | <span data-ttu-id="af316-117">1\_2</span><span class="sxs-lookup"><span data-stu-id="af316-117">1\_2</span></span> | <span data-ttu-id="af316-118">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="af316-118">1\_3</span></span> | <span data-ttu-id="af316-119">1\_4</span><span class="sxs-lookup"><span data-stu-id="af316-119">1\_4</span></span> | <span data-ttu-id="af316-120">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="af316-120">2\_0</span></span> | <span data-ttu-id="af316-121">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="af316-121">2\_x</span></span> | <span data-ttu-id="af316-122">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="af316-122">2\_sw</span></span> | <span data-ttu-id="af316-123">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="af316-123">3\_0</span></span> | <span data-ttu-id="af316-124">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="af316-124">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="af316-125">. ксизв (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="af316-125">.xyzw (default)</span></span>       | <span data-ttu-id="af316-126">x</span><span class="sxs-lookup"><span data-stu-id="af316-126">x</span></span>    | <span data-ttu-id="af316-127">x</span><span class="sxs-lookup"><span data-stu-id="af316-127">x</span></span>    | <span data-ttu-id="af316-128">x</span><span class="sxs-lookup"><span data-stu-id="af316-128">x</span></span>    | <span data-ttu-id="af316-129">x</span><span class="sxs-lookup"><span data-stu-id="af316-129">x</span></span>    | <span data-ttu-id="af316-130">x</span><span class="sxs-lookup"><span data-stu-id="af316-130">x</span></span>    | <span data-ttu-id="af316-131">x</span><span class="sxs-lookup"><span data-stu-id="af316-131">x</span></span>    | <span data-ttu-id="af316-132">x</span><span class="sxs-lookup"><span data-stu-id="af316-132">x</span></span>     | <span data-ttu-id="af316-133">x</span><span class="sxs-lookup"><span data-stu-id="af316-133">x</span></span>    | <span data-ttu-id="af316-134">x</span><span class="sxs-lookup"><span data-stu-id="af316-134">x</span></span>     |
| <span data-ttu-id="af316-135">. XYZ</span><span class="sxs-lookup"><span data-stu-id="af316-135">.xyz</span></span>                  | <span data-ttu-id="af316-136">x</span><span class="sxs-lookup"><span data-stu-id="af316-136">x</span></span>    | <span data-ttu-id="af316-137">x</span><span class="sxs-lookup"><span data-stu-id="af316-137">x</span></span>    | <span data-ttu-id="af316-138">x</span><span class="sxs-lookup"><span data-stu-id="af316-138">x</span></span>    | <span data-ttu-id="af316-139">x</span><span class="sxs-lookup"><span data-stu-id="af316-139">x</span></span>    | <span data-ttu-id="af316-140">x</span><span class="sxs-lookup"><span data-stu-id="af316-140">x</span></span>    | <span data-ttu-id="af316-141">x</span><span class="sxs-lookup"><span data-stu-id="af316-141">x</span></span>    | <span data-ttu-id="af316-142">x</span><span class="sxs-lookup"><span data-stu-id="af316-142">x</span></span>     | <span data-ttu-id="af316-143">x</span><span class="sxs-lookup"><span data-stu-id="af316-143">x</span></span>    | <span data-ttu-id="af316-144">x</span><span class="sxs-lookup"><span data-stu-id="af316-144">x</span></span>     |
| <span data-ttu-id="af316-145">. w</span><span class="sxs-lookup"><span data-stu-id="af316-145">.w</span></span>                    | <span data-ttu-id="af316-146">x</span><span class="sxs-lookup"><span data-stu-id="af316-146">x</span></span>    | <span data-ttu-id="af316-147">x</span><span class="sxs-lookup"><span data-stu-id="af316-147">x</span></span>    | <span data-ttu-id="af316-148">x</span><span class="sxs-lookup"><span data-stu-id="af316-148">x</span></span>    | <span data-ttu-id="af316-149">x</span><span class="sxs-lookup"><span data-stu-id="af316-149">x</span></span>    | <span data-ttu-id="af316-150">x</span><span class="sxs-lookup"><span data-stu-id="af316-150">x</span></span>    | <span data-ttu-id="af316-151">x</span><span class="sxs-lookup"><span data-stu-id="af316-151">x</span></span>    | <span data-ttu-id="af316-152">x</span><span class="sxs-lookup"><span data-stu-id="af316-152">x</span></span>     | <span data-ttu-id="af316-153">x</span><span class="sxs-lookup"><span data-stu-id="af316-153">x</span></span>    | <span data-ttu-id="af316-154">x</span><span class="sxs-lookup"><span data-stu-id="af316-154">x</span></span>     |
| <span data-ttu-id="af316-155">Произвольная маска</span><span class="sxs-lookup"><span data-stu-id="af316-155">arbitrary mask</span></span>        |      |      |      | <span data-ttu-id="af316-156">x</span><span class="sxs-lookup"><span data-stu-id="af316-156">x</span></span>    | <span data-ttu-id="af316-157">x</span><span class="sxs-lookup"><span data-stu-id="af316-157">x</span></span>    | <span data-ttu-id="af316-158">x</span><span class="sxs-lookup"><span data-stu-id="af316-158">x</span></span>    | <span data-ttu-id="af316-159">x</span><span class="sxs-lookup"><span data-stu-id="af316-159">x</span></span>     | <span data-ttu-id="af316-160">x</span><span class="sxs-lookup"><span data-stu-id="af316-160">x</span></span>    | <span data-ttu-id="af316-161">x</span><span class="sxs-lookup"><span data-stu-id="af316-161">x</span></span>     |



 

<span data-ttu-id="af316-162">Произвольная маска позволяет комбинировать любой набор каналов для создания маски.</span><span class="sxs-lookup"><span data-stu-id="af316-162">The arbitrary mask allows any set of channels to be combined to produce a mask.</span></span> <span data-ttu-id="af316-163">Каналы должны быть указаны в порядке r, g, b, a, например, Register. роль, который обновляет красный, синий и альфа-каналы назначения.</span><span class="sxs-lookup"><span data-stu-id="af316-163">The channels must be listed in the order r, g, b, a - for example, register.rba, which updates the red, blue, and alpha channels of the destination.</span></span> <span data-ttu-id="af316-164">Произвольная маска доступна в версии 1 \_ 4 или более поздней.</span><span class="sxs-lookup"><span data-stu-id="af316-164">The arbitrary mask is available in version 1\_4 or higher.</span></span>

<span data-ttu-id="af316-165">Если Целевая маска записи не указана, то целевой маской записи по умолчанию является вариант RGBA.</span><span class="sxs-lookup"><span data-stu-id="af316-165">If no destination write mask is specified, the destination write mask defaults to the rgba case.</span></span> <span data-ttu-id="af316-166">Иными словами, обновляются все каналы в регистре назначения.</span><span class="sxs-lookup"><span data-stu-id="af316-166">In other words, all channels in the destination register are updated.</span></span>

<span data-ttu-id="af316-167">Для версий \_ с 1 0 по 1 \_ 3 арифметическая инструкция [DP3-PS](dp3---ps.md) DP3 может использовать только маски записи с. RGB или RGBA.</span><span class="sxs-lookup"><span data-stu-id="af316-167">For versions 1\_0 to 1\_3, the [dp3 - ps](dp3---ps.md) dp3 arithmetic instruction can use only the .rgb or .rgba output write masks.</span></span>

<span data-ttu-id="af316-168">Маски записи для регистров назначения поддерживаются только для арифметических операций.</span><span class="sxs-lookup"><span data-stu-id="af316-168">Destination register write masks are supported for arithmetic operations only.</span></span> <span data-ttu-id="af316-169">Их нельзя использовать в инструкциях адресации текстур, за исключением инструкций версии 1 \_ 4, [текскрд-PS](texcrd---ps.md) и [текслд-PS \_ 2 \_ 0 и выше](texld---ps-2-0.md).</span><span class="sxs-lookup"><span data-stu-id="af316-169">They cannot be used on texture addressing instructions, with the exception of the version 1\_4 instructions, [texcrd - ps](texcrd---ps.md) and [texld - ps\_2\_0 and up](texld---ps-2-0.md).</span></span>

<span data-ttu-id="af316-170">По умолчанию записываются все четыре цветовых канала.</span><span class="sxs-lookup"><span data-stu-id="af316-170">The default is to write all four color channels.</span></span>


```
// All four color channels can be written by explicitly listing them.
mul r0.rgba, t0, v0

// Or, the default mask can be used to write all four channels.
mul r0, t0, v0
```



<span data-ttu-id="af316-171">Маска записи альфа-канала также называется скалярной маской записи, так как она использует скалярный конвейер.</span><span class="sxs-lookup"><span data-stu-id="af316-171">The alpha write mask is also referred to as the scalar write mask, because it uses the scalar pipeline.</span></span>


```
add r0.a, t1, v1
```



<span data-ttu-id="af316-172">Таким образом, эта инструкция фактически помещает сумму альфа-компонента T1 и альфа-компонента v1 в R0. a.</span><span class="sxs-lookup"><span data-stu-id="af316-172">So this instruction effectively puts the sum of the alpha component of t1 and the alpha component of v1 into r0.a.</span></span>

<span data-ttu-id="af316-173">Маска записи цвета используется для управления записью в цветовые каналы.</span><span class="sxs-lookup"><span data-stu-id="af316-173">The color write mask is used to control writing to the color channels.</span></span>


```
// The color write mask is also referred to as the vector write mask, 
//   because it uses the vector pipeline.
mul r0.rgb, t0, v0
```



<span data-ttu-id="af316-174">Для версии 1 \_ 4 маски записи назначения можно использовать в любом сочетании, если маски упорядочены на языке r, g, b и a.</span><span class="sxs-lookup"><span data-stu-id="af316-174">For version 1\_4, destination write masks can be used in any combination as long as the masks are ordered r,g,b,a.</span></span>


```
// This example updates the red, blue, and alpha channels.
mov r0.rba, r1
```



<span data-ttu-id="af316-175">Инструкция для совместной выдачи позволяет одновременно выдавать две потенциально разные инструкции.</span><span class="sxs-lookup"><span data-stu-id="af316-175">A co-issued instruction allows two potentially different instructions to be issued simultaneously.</span></span> <span data-ttu-id="af316-176">Это достигается путем выполнения инструкций в альфа-канале и конвейере RGB.</span><span class="sxs-lookup"><span data-stu-id="af316-176">This is accomplished by executing the instructions in the alpha pipeline and the RGB pipeline.</span></span>


```
  mul r0.rgb, t0, v0
+ add r1.a,   t1, c1
```



<span data-ttu-id="af316-177">Преимущество связывания инструкций таким способом заключается в том, что она позволяет выполнять различные операции в векторном и скалярном конвейере параллельно.</span><span class="sxs-lookup"><span data-stu-id="af316-177">The advantage of pairing instructions this way is that it allows different operations to be performed in the vector and scalar pipeline in parallel.</span></span>

<span data-ttu-id="af316-178">Эти регистры выходных данных шейдера вершин ограничены следующими масками записи:</span><span class="sxs-lookup"><span data-stu-id="af316-178">These vertex shader output registers are restricted to the following write masks:</span></span>



| <span data-ttu-id="af316-179">Тип регистра</span><span class="sxs-lookup"><span data-stu-id="af316-179">Register Type</span></span> | <span data-ttu-id="af316-180">Обязательная маска записи</span><span class="sxs-lookup"><span data-stu-id="af316-180">Required Write Mask</span></span>                                              |
|---------------|------------------------------------------------------------------|
| <span data-ttu-id="af316-181">офог</span><span class="sxs-lookup"><span data-stu-id="af316-181">oFog</span></span>          | <span data-ttu-id="af316-182">для этого скалярного регистра не разрешена явная маска записи</span><span class="sxs-lookup"><span data-stu-id="af316-182">no explicit write mask is allowed on this scalar register</span></span>        |
| <span data-ttu-id="af316-183">Решает</span><span class="sxs-lookup"><span data-stu-id="af316-183">oPts</span></span>          | <span data-ttu-id="af316-184">для этого скалярного регистра не разрешена явная маска записи</span><span class="sxs-lookup"><span data-stu-id="af316-184">no explicit write mask is allowed on this scalar register</span></span>        |
| <span data-ttu-id="af316-185">oPos</span><span class="sxs-lookup"><span data-stu-id="af316-185">oPos</span></span>          | <span data-ttu-id="af316-186">. ксизв (используется по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="af316-186">.xyzw(which is the default)</span></span>                                      |
| <span data-ttu-id="af316-187">Наблюдения\#</span><span class="sxs-lookup"><span data-stu-id="af316-187">oT\#</span></span>          | <span data-ttu-id="af316-188">Объединенная маска:. x \| . XY \| . XYZ \| . ксизв (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="af316-188">combined mask: .x \| .xy \| .xyz \| .xyzw (which is the default)</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="af316-189">См. также</span><span class="sxs-lookup"><span data-stu-id="af316-189">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="af316-190">Модификаторы регистра для шейдера пикселей</span><span class="sxs-lookup"><span data-stu-id="af316-190">Pixel Shader Register Modifiers</span></span>](dx9-graphics-reference-asm-ps-registers-modifiers.md)
</dt> </dl>

 

 




