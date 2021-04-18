---
title: Регистр цвета вывода
description: Выходные регистры цвета шейдера пикселей (oC) — это регистры только для записи, которые выводят результаты в несколько целевых объектов рендеринга.
ms.assetid: 88e69189-3956-47de-a336-921f1e62c025
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 316160e39ce172d56e4ecac17dfbd1d53077005b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104413457"
---
# <a name="output-color-register"></a><span data-ttu-id="8d442-103">Регистр цвета вывода</span><span class="sxs-lookup"><span data-stu-id="8d442-103">Output Color Register</span></span>

<span data-ttu-id="8d442-104">Выходные регистры цвета шейдера пикселей (oC #) — это регистры только для записи, которые выводят результаты в несколько целевых объектов рендеринга.</span><span class="sxs-lookup"><span data-stu-id="8d442-104">The pixel shader color output registers (oC#) are write-only registers that output results to multiple render targets.</span></span>

<span data-ttu-id="8d442-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="8d442-105">Syntax</span></span>



| <span data-ttu-id="8d442-106">даваемым #</span><span class="sxs-lookup"><span data-stu-id="8d442-106">oC#</span></span> |
|------|



 

<span data-ttu-id="8d442-107">Где:</span><span class="sxs-lookup"><span data-stu-id="8d442-107">Where:</span></span>



| <span data-ttu-id="8d442-108">Имя</span><span class="sxs-lookup"><span data-stu-id="8d442-108">Name</span></span> | <span data-ttu-id="8d442-109">Описание</span><span class="sxs-lookup"><span data-stu-id="8d442-109">Description</span></span>       |
|------|-------------------|
| <span data-ttu-id="8d442-110">oC0</span><span class="sxs-lookup"><span data-stu-id="8d442-110">oC0</span></span>  | <span data-ttu-id="8d442-111">Целевой объект прорисовки \# 0</span><span class="sxs-lookup"><span data-stu-id="8d442-111">render target \#0</span></span> |
| <span data-ttu-id="8d442-112">oC1</span><span class="sxs-lookup"><span data-stu-id="8d442-112">oC1</span></span>  | <span data-ttu-id="8d442-113">Целевой объект прорисовки \# 1</span><span class="sxs-lookup"><span data-stu-id="8d442-113">render target \#1</span></span> |
| <span data-ttu-id="8d442-114">oC2</span><span class="sxs-lookup"><span data-stu-id="8d442-114">oC2</span></span>  | <span data-ttu-id="8d442-115">Целевой объект прорисовки \# 2</span><span class="sxs-lookup"><span data-stu-id="8d442-115">render target \#2</span></span> |
| <span data-ttu-id="8d442-116">oC3</span><span class="sxs-lookup"><span data-stu-id="8d442-116">oC3</span></span>  | <span data-ttu-id="8d442-117">Целевой объект прорисовки \# 3</span><span class="sxs-lookup"><span data-stu-id="8d442-117">render target \#3</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="8d442-118">Примечания</span><span class="sxs-lookup"><span data-stu-id="8d442-118">Remarks</span></span>

-   <span data-ttu-id="8d442-119">Если окн записывается, но отсутствует соответствующий целевой объект прорисовки, то эта запись в окн игнорируется.</span><span class="sxs-lookup"><span data-stu-id="8d442-119">If oCn is written but there is no corresponding render target, then this write to oCn is ignored.</span></span>
-   <span data-ttu-id="8d442-120">Состояния рендеринга D3DRS \_ колорвритинабле, D3DRS \_ COLORWRITEENABLE1, D3DRS \_ COLORWRITEENABLE2 и D3DRS \_ COLORWRITEENABLE3 определяют, какие компоненты окн в конечном итоге записываются в целевой объект отрисовки (после смешения, если применимо).</span><span class="sxs-lookup"><span data-stu-id="8d442-120">The render states D3DRS\_COLORWRITEENABLE, D3DRS\_COLORWRITEENABLE1, D3DRS\_COLORWRITEENABLE2 and D3DRS\_COLORWRITEENABLE3 determine which components of oCn ultimately get written to the render target (after blend, if applicable).</span></span> <span data-ttu-id="8d442-121">Если шейдер записывает некоторые, но не все компоненты, определенные \_ \* состояниями отрисовки D3DRS колорвритинабле для заданного регистра окн, то незаписанные каналы создают неопределенные значения в соответствующем целевом объекте прорисовки.</span><span class="sxs-lookup"><span data-stu-id="8d442-121">If the shader writes some but not all of the components defined by the D3DRS\_COLORWRITEENABLE\* render states for a given oCn register, then the unwritten channels produce undefined values in the corresponding render target.</span></span> <span data-ttu-id="8d442-122">Если ни один из компонентов окн не написан, соответствующий целевой объект рендеринга не должен обновляться (как указано выше), поэтому D3DRS \_ колорвритинабле \* отрисовки не применяются.</span><span class="sxs-lookup"><span data-stu-id="8d442-122">If none of the components of an oCn are written, the corresponding render target must not be updated at all (as stated above), so the D3DRS\_COLORWRITEENABLE\* render states do not apply.</span></span>

### <a name="shader-model-2-restrictions"></a><span data-ttu-id="8d442-123">Ограничения модели шейдеров 2</span><span class="sxs-lookup"><span data-stu-id="8d442-123">Shader Model 2 Restrictions</span></span>

-   <span data-ttu-id="8d442-124">Окн можно записать только с помощью инструкции [MOV-PS](mov---ps.md) .</span><span class="sxs-lookup"><span data-stu-id="8d442-124">oCn can only be written with the [mov - ps](mov---ps.md) instruction.</span></span>
-   <span data-ttu-id="8d442-125">oC0 должен быть всегда записан в шейдер.</span><span class="sxs-lookup"><span data-stu-id="8d442-125">oC0 must be always written in the shader.</span></span>
-   <span data-ttu-id="8d442-126">Отсутствуют исходные свиззле (кроме. ксизв = Default свиззле) или модификатор источника, разрешенный при записи в любой окн.</span><span class="sxs-lookup"><span data-stu-id="8d442-126">No source swizzle (except .xyzw = default swizzle) or source modifier is allowed when writing to any oCn.</span></span>
-   <span data-ttu-id="8d442-127">Конечная маска записи (кроме. ксизв = маска по умолчанию) или модификатор инструкции разрешена при записи в любой окн.</span><span class="sxs-lookup"><span data-stu-id="8d442-127">No destination write mask (except .xyzw = default mask) or instruction modifier is allowed when writing to any oCn.</span></span>
-   <span data-ttu-id="8d442-128">Если окн записан, то необходимо также записать oC0-окн-1.</span><span class="sxs-lookup"><span data-stu-id="8d442-128">If oCn is written, then oC0 - oCn-1 must also be written.</span></span> <span data-ttu-id="8d442-129">Например, для записи в oC2 необходимо также выполнить запись в oC0 и oC1.</span><span class="sxs-lookup"><span data-stu-id="8d442-129">For example, to write to oC2, you must also write to oC0 and oC1.</span></span>
-   <span data-ttu-id="8d442-130">Допускается не более одной записи в любой неoc # на шейдер.</span><span class="sxs-lookup"><span data-stu-id="8d442-130">At most one write to any oC# per shader is allowed.</span></span>
-   <span data-ttu-id="8d442-131">Для PS \_ 2 \_ x и PS \_ 3 \_ 0 нельзя выполнять запись в регистры OC # и oD \# в динамическом управлении потоком или затенения (операции записи в OC # внутри статического управления потоком прекрасно).</span><span class="sxs-lookup"><span data-stu-id="8d442-131">For ps\_2\_x and ps\_3\_0, you cannot write to oC# and oD\# registers within dynamic flow control or predication (writes to oC# inside static flow control is fine).</span></span>

### <a name="shader-model-3-restrictions"></a><span data-ttu-id="8d442-132">Ограничения модели шейдеров 3</span><span class="sxs-lookup"><span data-stu-id="8d442-132">Shader Model 3 Restrictions</span></span>

-   <span data-ttu-id="8d442-133">Для PS \_ 3 \_ 0 выходные регистры OC # и oD \# могут записываться любое количество раз.</span><span class="sxs-lookup"><span data-stu-id="8d442-133">For ps\_3\_0, output registers oC# and oD\# can be written any number of times.</span></span> <span data-ttu-id="8d442-134">Выходные данные шейдера пикселей поступают из содержимого выходных регистров в конце выполнения шейдера.</span><span class="sxs-lookup"><span data-stu-id="8d442-134">The output of the pixel shader comes from the contents of the output registers at the end of shader execution.</span></span> <span data-ttu-id="8d442-135">Если запись в выходной регистр не происходит, возможно, из-за управления потоком или если шейдер просто не написал его, соответствующая рендертаржет также не обновляется.</span><span class="sxs-lookup"><span data-stu-id="8d442-135">If a write to an output register does not happen, perhaps due to flow control or if the shader just did not write it, the corresponding rendertarget is also not updated.</span></span> <span data-ttu-id="8d442-136">Если подмножество каналов в выходном регистре записано, то неопределенные значения будут записаны в оставшиеся каналы.</span><span class="sxs-lookup"><span data-stu-id="8d442-136">If a subset of the channels in an output register are written, then undefined values will be written to the remaining channels.</span></span>
-   <span data-ttu-id="8d442-137">Для PS \_ 3 \_ 0 регистры OC # могут быть записаны с любым вритемаскс.</span><span class="sxs-lookup"><span data-stu-id="8d442-137">For ps\_3\_0, the oC# registers can be written with any writemasks.</span></span>
-   <span data-ttu-id="8d442-138">Для PS \_ 2 \_ x и PS \_ 3 \_ 0 нельзя выполнять запись в регистры OC # и oD \# в динамическом управлении потоком или затенения (операции записи в OC # внутри статического управления потоком прекрасно).</span><span class="sxs-lookup"><span data-stu-id="8d442-138">For ps\_2\_x and ps\_3\_0, you cannot write to oC# and oD\# registers within dynamic flow control or predication (writes to oC# inside static flow control is fine).</span></span>
-   <span data-ttu-id="8d442-139">Вы не можете выполнять вычисления градиента (или операции, которые неявно вызывают такие вычисления градиента, как [текслд-PS \_ 2 \_ 0 и up](texld---ps-2-0.md), [текслдб-PS](texldb---ps.md), [текслдп-PS](texldp---ps.md)) внутри операторов управления потоком, условия ветвления которых различаются для отдельных примитивов (IE: Динамическая Инструкция по управлению потоком).</span><span class="sxs-lookup"><span data-stu-id="8d442-139">You may not perform any gradient calculations (or operations that implicitly invoke gradient calculations such as [texld - ps\_2\_0 and up](texld---ps-2-0.md), [texldb - ps](texldb---ps.md), [texldp - ps](texldp---ps.md)) inside of flow control statements whose branching conditions vary on a per-primitive basis (ie: dynamic flow control instructions).</span></span> <span data-ttu-id="8d442-140">Инструкция затенения не считается динамической системой управления потоком.</span><span class="sxs-lookup"><span data-stu-id="8d442-140">Instruction predication is not considered dynamic flow control.</span></span>

## <a name="related-topics"></a><span data-ttu-id="8d442-141">См. также</span><span class="sxs-lookup"><span data-stu-id="8d442-141">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8d442-142">Регистры</span><span class="sxs-lookup"><span data-stu-id="8d442-142">Registers</span></span>](dx9-graphics-reference-asm-ps-registers.md)
</dt> <dt>

[<span data-ttu-id="8d442-143">Несколько целевых объектов рендеринга (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="8d442-143">Multiple Render Targets (Direct3D 9)</span></span>](/windows/desktop/direct3d9/multiple-render-targets)
</dt> </dl>

 

 