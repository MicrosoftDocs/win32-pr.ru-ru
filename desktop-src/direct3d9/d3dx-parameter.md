---
description: Эти флаги предоставляют дополнительные сведения о параметрах эффектов.
ms.assetid: 7e1e4c64-56b8-4fdb-8178-50f7d61b917b
title: D3DX_PARAMETER (D3dx9effect. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX_PARAMETER_ANNOTATION
- D3DX_PARAMETER_LITERAL
- D3DX_PARAMETER_SHARED
api_type:
- HeaderDef
api_location:
- d3dx9effect.h
ms.openlocfilehash: 49df84c49fd1f7a0c1b4de9157a36e27d29d5e29
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105713753"
---
# <a name="d3dx_parameter"></a><span data-ttu-id="3f0da-103">D3DX, \_ параметр</span><span class="sxs-lookup"><span data-stu-id="3f0da-103">D3DX\_PARAMETER</span></span>

<span data-ttu-id="3f0da-104">Эти флаги предоставляют дополнительные сведения о параметрах эффектов.</span><span class="sxs-lookup"><span data-stu-id="3f0da-104">These flags provide additional information about effect parameters.</span></span>

<span data-ttu-id="3f0da-105">Константы параметров эффектов используются в [**D3DXPARAMETER \_ DESC**](d3dxparameter-desc.md).</span><span class="sxs-lookup"><span data-stu-id="3f0da-105">Effect parameter constants are used by [**D3DXPARAMETER\_DESC**](d3dxparameter-desc.md).</span></span>



| <span data-ttu-id="3f0da-106">Константа</span><span class="sxs-lookup"><span data-stu-id="3f0da-106">Constant</span></span>                                                                                                                                                                                           | <span data-ttu-id="3f0da-107">Описание</span><span class="sxs-lookup"><span data-stu-id="3f0da-107">Description</span></span>                                                                                                                                                                                                                                                                                                                             |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="D3DX_PARAMETER_ANNOTATION"></span><span id="d3dx_parameter_annotation"></span><dl> <span data-ttu-id="3f0da-108"><dt>**\_Аннотация параметра \_ D3DX**</dt></span><span class="sxs-lookup"><span data-stu-id="3f0da-108"><dt>**D3DX\_PARAMETER\_ANNOTATION**</dt></span></span> </dl> | <span data-ttu-id="3f0da-109">Этот параметр помечен как аннотация.</span><span class="sxs-lookup"><span data-stu-id="3f0da-109">This parameter is marked as an annotation.</span></span> <span data-ttu-id="3f0da-110">См. раздел [Добавление сведений, чтобы параметры вступили в действие с заметками](using-an-effect.md).</span><span class="sxs-lookup"><span data-stu-id="3f0da-110">See [Add Information to Effect Parameters with Annotations](using-an-effect.md).</span></span><br/>                                                                                                                                                                                                 |
| <span id="D3DX_PARAMETER_LITERAL"></span><span id="d3dx_parameter_literal"></span><dl> <span data-ttu-id="3f0da-111"><dt>**\_Литерал параметра \_ D3DX**</dt></span><span class="sxs-lookup"><span data-stu-id="3f0da-111"><dt>**D3DX\_PARAMETER\_LITERAL**</dt></span></span> </dl>          | <span data-ttu-id="3f0da-112">Этот параметр помечен как литеральное значение.</span><span class="sxs-lookup"><span data-stu-id="3f0da-112">This parameter is marked as a literal value.</span></span> <span data-ttu-id="3f0da-113">Параметры литерала не могут быть изменены после компиляции, что позволяет компилятору оптимизировать их использование.</span><span class="sxs-lookup"><span data-stu-id="3f0da-113">Literal parameters cannot change after compile, allowing the compiler to optimize their usage.</span></span> <span data-ttu-id="3f0da-114">Общие параметры не могут быть помечены как литералы.</span><span class="sxs-lookup"><span data-stu-id="3f0da-114">Shared parameters cannot be marked as a literal.</span></span> <span data-ttu-id="3f0da-115">См. раздел [использование и литералы (Direct3D 9)](usages-and-literals.md).</span><span class="sxs-lookup"><span data-stu-id="3f0da-115">See [Usages and Literals (Direct3D 9)](usages-and-literals.md).</span></span> <br/>                                                               |
| <span id="D3DX_PARAMETER_SHARED"></span><span id="d3dx_parameter_shared"></span><dl> <span data-ttu-id="3f0da-116"><dt>**\_Общий параметр \_ D3DX**</dt></span><span class="sxs-lookup"><span data-stu-id="3f0da-116"><dt>**D3DX\_PARAMETER\_SHARED**</dt></span></span> </dl>             | <span data-ttu-id="3f0da-117">Значение параметра будет совместно использоваться всеми эффектами в том же пространстве имен.</span><span class="sxs-lookup"><span data-stu-id="3f0da-117">The value of a parameter will be shared by all effects in the same namespace.</span></span> <span data-ttu-id="3f0da-118">Изменение значения в одном эффекте приведет к его изменению во всех общих эффектах.</span><span class="sxs-lookup"><span data-stu-id="3f0da-118">Changing the value in one effect will change it in all shared effects.</span></span> <span data-ttu-id="3f0da-119">См. раздел [Общие параметры](cloning-and-sharing.md).</span><span class="sxs-lookup"><span data-stu-id="3f0da-119">See [Sharing Parameters](cloning-and-sharing.md).</span></span> <span data-ttu-id="3f0da-120">**D3DX \_ \_Общий параметр** не может быть объединен с аннотацией параметра **D3DX \_ \_** или **\_ \_ заметкой параметра D3DX**.</span><span class="sxs-lookup"><span data-stu-id="3f0da-120">**D3DX\_PARAMETER\_SHARED** cannot be combined with **D3DX\_PARAMETER\_LITERAL** or **D3DX\_PARAMETER\_ANNOTATION**.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="3f0da-121">Требования</span><span class="sxs-lookup"><span data-stu-id="3f0da-121">Requirements</span></span>



| <span data-ttu-id="3f0da-122">Требование</span><span class="sxs-lookup"><span data-stu-id="3f0da-122">Requirement</span></span> | <span data-ttu-id="3f0da-123">Значение</span><span class="sxs-lookup"><span data-stu-id="3f0da-123">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="3f0da-124">Header</span><span class="sxs-lookup"><span data-stu-id="3f0da-124">Header</span></span><br/> | <dl> <span data-ttu-id="3f0da-125"><dt>D3dx9effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="3f0da-125"><dt>D3dx9effect.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3f0da-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="3f0da-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3f0da-127">Константы эффектов</span><span class="sxs-lookup"><span data-stu-id="3f0da-127">Effect Constants</span></span>](dx9-graphics-reference-effects-constants.md)
</dt> </dl>

 

 




