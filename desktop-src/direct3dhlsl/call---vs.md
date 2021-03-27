---
title: вызов — VS
description: Выполняет вызов функции в инструкцию, помеченную указанной меткой. | вызов — VS
ms.assetid: 3c1ec529-1ee4-40d9-8ce5-f8e7a61fde9c
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: c797e7ef6745f5710752fe059d2a2ff1f94a8aa3
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "104000288"
---
# <a name="call---vs"></a><span data-ttu-id="c4a79-104">вызов — VS</span><span class="sxs-lookup"><span data-stu-id="c4a79-104">call - vs</span></span>

<span data-ttu-id="c4a79-105">Выполняет вызов функции в инструкцию, помеченную указанной меткой.</span><span class="sxs-lookup"><span data-stu-id="c4a79-105">Performs a function call to the instruction marked with the provided label.</span></span>

## <a name="syntax"></a><span data-ttu-id="c4a79-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c4a79-106">Syntax</span></span>



| <span data-ttu-id="c4a79-107">вызов l\#</span><span class="sxs-lookup"><span data-stu-id="c4a79-107">call l\#</span></span> |
|----------|



 

<span data-ttu-id="c4a79-108">где l \# — [Метка — VS](label---vs.md) отмечает начало подпрограммы, которую необходимо вызвать.</span><span class="sxs-lookup"><span data-stu-id="c4a79-108">where l\# is a [label - vs](label---vs.md) marking the beginning of the subroutine to be called.</span></span>

## <a name="remarks"></a><span data-ttu-id="c4a79-109">Примечания</span><span class="sxs-lookup"><span data-stu-id="c4a79-109">Remarks</span></span>



| <span data-ttu-id="c4a79-110">Версии шейдеров вершин</span><span class="sxs-lookup"><span data-stu-id="c4a79-110">Vertex shader versions</span></span> | <span data-ttu-id="c4a79-111">1\_1</span><span class="sxs-lookup"><span data-stu-id="c4a79-111">1\_1</span></span> | <span data-ttu-id="c4a79-112">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="c4a79-112">2\_0</span></span> | <span data-ttu-id="c4a79-113">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="c4a79-113">2\_x</span></span> | <span data-ttu-id="c4a79-114">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="c4a79-114">2\_sw</span></span> | <span data-ttu-id="c4a79-115">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="c4a79-115">3\_0</span></span> | <span data-ttu-id="c4a79-116">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="c4a79-116">3\_sw</span></span> |
|------------------------|------|------|------|-------|------|-------|
| <span data-ttu-id="c4a79-117">вызывает</span><span class="sxs-lookup"><span data-stu-id="c4a79-117">call</span></span>                   |      | <span data-ttu-id="c4a79-118">x</span><span class="sxs-lookup"><span data-stu-id="c4a79-118">x</span></span>    | <span data-ttu-id="c4a79-119">x</span><span class="sxs-lookup"><span data-stu-id="c4a79-119">x</span></span>    | <span data-ttu-id="c4a79-120">x</span><span class="sxs-lookup"><span data-stu-id="c4a79-120">x</span></span>     | <span data-ttu-id="c4a79-121">x</span><span class="sxs-lookup"><span data-stu-id="c4a79-121">x</span></span>    | <span data-ttu-id="c4a79-122">x</span><span class="sxs-lookup"><span data-stu-id="c4a79-122">x</span></span>     |



 

<span data-ttu-id="c4a79-123">Эта инструкция выполняет следующие действия:</span><span class="sxs-lookup"><span data-stu-id="c4a79-123">This instruction does the following:</span></span>

1.  <span data-ttu-id="c4a79-124">Адрес принудительной отправки следующей инструкции в стек адресов возврата.</span><span class="sxs-lookup"><span data-stu-id="c4a79-124">Push address of the next instruction to the return address stack.</span></span>
2.  <span data-ttu-id="c4a79-125">Продолжить выполнение из инструкции, помеченной меткой.</span><span class="sxs-lookup"><span data-stu-id="c4a79-125">Continue execution from the instruction marked by the label.</span></span>

<span data-ttu-id="c4a79-126">В шейдере вершин 2 \_ 0 вызовы вложений запрещены.</span><span class="sxs-lookup"><span data-stu-id="c4a79-126">In vertex shader 2\_0, nesting calls are not allowed.</span></span>

<span data-ttu-id="c4a79-127">В шейдере вершин 2 \_ x глубина вложения ограничена элементом статикфловконтролдепс структуры [**D3DVSHADERCAPS2 \_ 0**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dvshadercaps2_0) .</span><span class="sxs-lookup"><span data-stu-id="c4a79-127">In vertex shader 2\_x, the nesting depth is limited by the StaticFlowControlDepth element of the [**D3DVSHADERCAPS2\_0**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dvshadercaps2_0) structure.</span></span> <span data-ttu-id="c4a79-128">Дополнительные сведения см. в разделе [**жетдевицекапс**](/windows/desktop/api/d3d9/nf-d3d9-idirect3d9-getdevicecaps).</span><span class="sxs-lookup"><span data-stu-id="c4a79-128">For more information, see [**GetDeviceCaps**](/windows/desktop/api/d3d9/nf-d3d9-idirect3d9-getdevicecaps).</span></span>

<span data-ttu-id="c4a79-129">В шейдере вершин 3 \_ 0 разрешено использовать четыре уровня вложенности вызовов.</span><span class="sxs-lookup"><span data-stu-id="c4a79-129">In vertex shader 3\_0, four levels of call nesting are allowed.</span></span>

<span data-ttu-id="c4a79-130">Допускаются только прямые вызовы.</span><span class="sxs-lookup"><span data-stu-id="c4a79-130">Only forward calls are allowed.</span></span> <span data-ttu-id="c4a79-131">Это означает, что расположение метки внутри шейдера вершин должно быть после инструкции вызова, ссылающейся на него.</span><span class="sxs-lookup"><span data-stu-id="c4a79-131">This means that the location of the label inside the vertex shader should be after the call instruction referencing it.</span></span>

<span data-ttu-id="c4a79-132">Если инструкция вызова вызывается внутри [цикла](loop---vs.md)... блок [ендлуп](endloop---vs.md) . значение [регистра счетчика циклов](dx9-graphics-reference-asm-vs-registers-loop-counter.md) (Al) доступно внутри подпрограммы.</span><span class="sxs-lookup"><span data-stu-id="c4a79-132">If a call instruction is invoked inside [loop](loop---vs.md)...[endloop](endloop---vs.md) block, the value of the [Loop Counter Register](dx9-graphics-reference-asm-vs-registers-loop-counter.md) (aL) is accessible inside the subroutine.</span></span>

<span data-ttu-id="c4a79-133">Если подпрограмма ссылается на [регистр счетчиков циклов](dx9-graphics-reference-asm-vs-registers-loop-counter.md) (Al), расположенный за пределами подпрограммы, каждый экземпляр вызова этой подпрограммы должен быть заключен в [цикл](loop---vs.md)... блок [ендлуп](endloop---vs.md) .</span><span class="sxs-lookup"><span data-stu-id="c4a79-133">If a subroutine is referencing the [Loop Counter Register](dx9-graphics-reference-asm-vs-registers-loop-counter.md) (aL) located outside of the subroutine, every instance of the call to this subroutine should be surrounded by a [loop](loop---vs.md)...[endloop](endloop---vs.md) block.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c4a79-134">См. также</span><span class="sxs-lookup"><span data-stu-id="c4a79-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c4a79-135">Инструкции шейдера вершин</span><span class="sxs-lookup"><span data-stu-id="c4a79-135">Vertex Shader Instructions</span></span>](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 
