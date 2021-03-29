---
title: Константы D3DCOMPILE_EFFECT (D3DCompiler. h)
description: Эти константы непосредственно описывают, как компилятор компилирует файл эффектов или как среда выполнения обрабатывает файл эффектов.
ms.assetid: AA46E5ED-92DD-4327-B852-8DD23A878562
topic_type:
- apiref
api_name:
- D3DCOMPILE_EFFECT_CHILD_EFFECT
- D3DCOMPILE_EFFECT_ALLOW_SLOW_OPS
api_location:
- D3DCompiler.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 69f0597341a331af82ed279a6030126d222b70f7
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104986795"
---
# <a name="d3dcompile_effect-constants"></a><span data-ttu-id="f8926-103">\_Константы эффектов D3DCOMPILE</span><span class="sxs-lookup"><span data-stu-id="f8926-103">D3DCOMPILE\_EFFECT Constants</span></span>

<span data-ttu-id="f8926-104">Эти константы непосредственно описывают, как компилятор компилирует файл эффектов или как среда выполнения обрабатывает файл эффектов.</span><span class="sxs-lookup"><span data-stu-id="f8926-104">These constants direct how the compiler compiles an effect file or how the runtime processes the effect file.</span></span>

<dl> <dt>

<span data-ttu-id="f8926-105"><span id="D3DCOMPILE_EFFECT_CHILD_EFFECT"></span><span id="d3dcompile_effect_child_effect"></span>**\_ \_ Дочерний \_ эффекты D3DCOMPILE**</span><span class="sxs-lookup"><span data-stu-id="f8926-105"><span id="D3DCOMPILE_EFFECT_CHILD_EFFECT"></span><span id="d3dcompile_effect_child_effect"></span>**D3DCOMPILE\_EFFECT\_CHILD\_EFFECT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f8926-106">(1 << 0)</span><span class="sxs-lookup"><span data-stu-id="f8926-106">(1 << 0)</span></span>
</dt> <dt>



<span data-ttu-id="f8926-107">Скомпилируйте файл Effects (. FX) до дочернего эффекта.</span><span class="sxs-lookup"><span data-stu-id="f8926-107">Compile the effects (.fx) file to a child effect.</span></span> <span data-ttu-id="f8926-108">Дочерние эффекты не имеют инициализаторов для общих значений, так как эти дочерние эффекты инициализируются в главном действии (пул эффектов).</span><span class="sxs-lookup"><span data-stu-id="f8926-108">Child effects have no initializers for any shared values because these child effects are initialized in the master effect (the effect pool).</span></span>

> [!Note]  
> <span data-ttu-id="f8926-109">Пулы эффектов поддерживаются эффектами 10 (FX10), но не по результатам 11 (FX11).</span><span class="sxs-lookup"><span data-stu-id="f8926-109">Effect pools are supported by Effects 10 (FX10) but not by Effects 11 (FX11).</span></span> <span data-ttu-id="f8926-110">Дополнительные сведения о различиях между пулами эффектов в Direct3D 10 и группах эффектов в Direct3D 11 см. в статье [Пулы и группы эффектов](/windows/desktop/direct3d11/d3d11-graphics-programming-guide-effects-differences).</span><span class="sxs-lookup"><span data-stu-id="f8926-110">For more info about differences between effect pools in Direct3D 10 and effect groups in Direct3D 11, see [Effect Pools and Groups](/windows/desktop/direct3d11/d3d11-graphics-programming-guide-effects-differences).</span></span>

 


</dt> </dl> </dd> <dt>

<span data-ttu-id="f8926-111"><span id="D3DCOMPILE_EFFECT_ALLOW_SLOW_OPS"></span><span id="d3dcompile_effect_allow_slow_ops"></span>**\_Эффекты D3DCOMPILE \_ разрешают выполнение \_ операций с высокой скоростью \_**</span><span class="sxs-lookup"><span data-stu-id="f8926-111"><span id="D3DCOMPILE_EFFECT_ALLOW_SLOW_OPS"></span><span id="d3dcompile_effect_allow_slow_ops"></span>**D3DCOMPILE\_EFFECT\_ALLOW\_SLOW\_OPS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f8926-112">(1 << 1)</span><span class="sxs-lookup"><span data-stu-id="f8926-112">(1 << 1)</span></span>
</dt> <dt>



<span data-ttu-id="f8926-113">Отключает режим производительности и позволяет применять изменяемые объекты состояния.</span><span class="sxs-lookup"><span data-stu-id="f8926-113">Disables performance mode and allows for mutable state objects.</span></span>

<span data-ttu-id="f8926-114">По умолчанию включен режим производительности.</span><span class="sxs-lookup"><span data-stu-id="f8926-114">By default, performance mode is enabled.</span></span> <span data-ttu-id="f8926-115">Режим производительности запрещает изменять объекты изменяемого состояния, предотвращая отображение нелитеральных выражений в определениях объектов состояния.</span><span class="sxs-lookup"><span data-stu-id="f8926-115">Performance mode disallows mutable state objects by preventing non-literal expressions from appearing in state object definitions.</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="f8926-116">Требования</span><span class="sxs-lookup"><span data-stu-id="f8926-116">Requirements</span></span>



| <span data-ttu-id="f8926-117">Требование</span><span class="sxs-lookup"><span data-stu-id="f8926-117">Requirement</span></span> | <span data-ttu-id="f8926-118">Значение</span><span class="sxs-lookup"><span data-stu-id="f8926-118">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="f8926-119">Header</span><span class="sxs-lookup"><span data-stu-id="f8926-119">Header</span></span><br/> | <dl> <span data-ttu-id="f8926-120"><dt>D3DCompiler. h</dt></span><span class="sxs-lookup"><span data-stu-id="f8926-120"><dt>D3DCompiler.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f8926-121">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f8926-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f8926-122">Константы D3DCompiler</span><span class="sxs-lookup"><span data-stu-id="f8926-122">D3DCompiler Constants</span></span>](dx-graphics-d3dcompiler-reference-constants.md)
</dt> </dl>

 

