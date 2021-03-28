---
title: дефи — VS
description: Определяет целочисленное значение константы, которое должно быть загружено в любое время, когда шейдер задается устройством.
ms.assetid: d6067a7d-58fb-4553-a42f-192c29bf78b7
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 897a544cc9974b8ffa727f2d39219cfeab82d52a
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104533392"
---
# <a name="defi---vs"></a><span data-ttu-id="b8bba-103">дефи — VS</span><span class="sxs-lookup"><span data-stu-id="b8bba-103">defi - vs</span></span>

<span data-ttu-id="b8bba-104">Определяет целочисленное значение константы, которое должно быть загружено в любое время, когда шейдер задается устройством.</span><span class="sxs-lookup"><span data-stu-id="b8bba-104">Defines an integer constant value, which should be loaded anytime a shader is set to a device.</span></span>

## <a name="syntax"></a><span data-ttu-id="b8bba-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b8bba-105">Syntax</span></span>



| <span data-ttu-id="b8bba-106">дефи DST, integerValue0, integerValue1, integerValue2, integerValue3</span><span class="sxs-lookup"><span data-stu-id="b8bba-106">defi dst, integerValue0, integerValue1, integerValue2, integerValue3</span></span> |
|----------------------------------------------------------------------|



 

-   <span data-ttu-id="b8bba-107">DST — это регистр назначения.</span><span class="sxs-lookup"><span data-stu-id="b8bba-107">dst is the destination register.</span></span>
-   <span data-ttu-id="b8bba-108">Интежервалуе \# — это постоянное целочисленное значение.</span><span class="sxs-lookup"><span data-stu-id="b8bba-108">integerValue\# is a constant integer value.</span></span>

## <a name="remarks"></a><span data-ttu-id="b8bba-109">Примечания</span><span class="sxs-lookup"><span data-stu-id="b8bba-109">Remarks</span></span>



| <span data-ttu-id="b8bba-110">Версии шейдеров вершин</span><span class="sxs-lookup"><span data-stu-id="b8bba-110">Vertex shader versions</span></span> | <span data-ttu-id="b8bba-111">1\_1</span><span class="sxs-lookup"><span data-stu-id="b8bba-111">1\_1</span></span> | <span data-ttu-id="b8bba-112">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="b8bba-112">2\_0</span></span> | <span data-ttu-id="b8bba-113">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="b8bba-113">2\_x</span></span> | <span data-ttu-id="b8bba-114">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="b8bba-114">2\_sw</span></span> | <span data-ttu-id="b8bba-115">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="b8bba-115">3\_0</span></span> | <span data-ttu-id="b8bba-116">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="b8bba-116">3\_sw</span></span> |
|------------------------|------|------|------|-------|------|-------|
| <span data-ttu-id="b8bba-117">дефи</span><span class="sxs-lookup"><span data-stu-id="b8bba-117">defi</span></span>                   |      | <span data-ttu-id="b8bba-118">x</span><span class="sxs-lookup"><span data-stu-id="b8bba-118">x</span></span>    | <span data-ttu-id="b8bba-119">x</span><span class="sxs-lookup"><span data-stu-id="b8bba-119">x</span></span>    | <span data-ttu-id="b8bba-120">x</span><span class="sxs-lookup"><span data-stu-id="b8bba-120">x</span></span>     | <span data-ttu-id="b8bba-121">x</span><span class="sxs-lookup"><span data-stu-id="b8bba-121">x</span></span>    | <span data-ttu-id="b8bba-122">x</span><span class="sxs-lookup"><span data-stu-id="b8bba-122">x</span></span>     |



 

<span data-ttu-id="b8bba-123">Инструкция дефи определяет константу целочисленного шейдера, значение которой загружается в любое время в качестве шейдера для устройства.</span><span class="sxs-lookup"><span data-stu-id="b8bba-123">The defi instruction defines an integer shader constant whose value is loaded anytime a shader is set to a device.</span></span> <span data-ttu-id="b8bba-124">Они называются прямыми константами.</span><span class="sxs-lookup"><span data-stu-id="b8bba-124">These are called immediate constants.</span></span> <span data-ttu-id="b8bba-125">Немедленные константы имеют приоритет над константами, заданными методом API Сетвертексшадерконстанти.</span><span class="sxs-lookup"><span data-stu-id="b8bba-125">Immediate constants take precedence over constants set by the API method SetVertexShaderConstantI.</span></span>

<span data-ttu-id="b8bba-126">Существует два способа задать целочисленную константу в шейдере.</span><span class="sxs-lookup"><span data-stu-id="b8bba-126">There are two ways to set an integer constant in a shader.</span></span>

1.  <span data-ttu-id="b8bba-127">Используйте дефи, чтобы определить целочисленный константный вектор непосредственно внутри шейдера.</span><span class="sxs-lookup"><span data-stu-id="b8bba-127">Use defi to define the integer constant vector directly inside a shader.</span></span>
2.  <span data-ttu-id="b8bba-128">Используйте методы API для задания константы.</span><span class="sxs-lookup"><span data-stu-id="b8bba-128">Use the API methods to set a constant.</span></span>
    -   <span data-ttu-id="b8bba-129">Используйте [**сетвертексшадерконстанти**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setvertexshaderconstanti) для установки целочисленной константы.</span><span class="sxs-lookup"><span data-stu-id="b8bba-129">Use [**SetVertexShaderConstantI**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setvertexshaderconstanti) to set an integer constant.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b8bba-130">См. также</span><span class="sxs-lookup"><span data-stu-id="b8bba-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b8bba-131">Инструкции шейдера вершин</span><span class="sxs-lookup"><span data-stu-id="b8bba-131">Vertex Shader Instructions</span></span>](dx9-graphics-reference-asm-vs-instructions.md)
</dt> <dt>

[<span data-ttu-id="b8bba-132">Сравнение DEF и</span><span class="sxs-lookup"><span data-stu-id="b8bba-132">def - vs</span></span>](def---vs.md)
</dt> <dt>

[<span data-ttu-id="b8bba-133">дефб — VS</span><span class="sxs-lookup"><span data-stu-id="b8bba-133">defb - vs</span></span>](defb---vs.md)
</dt> </dl>

 

 