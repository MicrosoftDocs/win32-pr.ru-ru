---
title: дефи-PS
description: Определяет целочисленное значение константы, которое должно быть загружено каждый раз, когда шейдер задается устройством.
ms.assetid: c51982a1-45b4-48db-a49a-93165d61efd3
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 3552d5cfe322dd384e1c6bd219e35af19b469a56
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104134311"
---
# <a name="defi---ps"></a><span data-ttu-id="f413c-103">дефи-PS</span><span class="sxs-lookup"><span data-stu-id="f413c-103">defi - ps</span></span>

<span data-ttu-id="f413c-104">Определяет целочисленное значение константы, которое должно быть загружено каждый раз, когда шейдер задается устройством.</span><span class="sxs-lookup"><span data-stu-id="f413c-104">Defines an integer constant value, which should be loaded any time a shader is set to a device.</span></span>

## <a name="syntax"></a><span data-ttu-id="f413c-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f413c-105">Syntax</span></span>



| <span data-ttu-id="f413c-106">дефи DST, Интежервалуе</span><span class="sxs-lookup"><span data-stu-id="f413c-106">defi dst, integerValue</span></span> |
|------------------------|



 

-   <span data-ttu-id="f413c-107">DST — это регистр назначения.</span><span class="sxs-lookup"><span data-stu-id="f413c-107">dst is the destination register.</span></span>
-   <span data-ttu-id="f413c-108">Интежервалуе — это постоянное целочисленное значение.</span><span class="sxs-lookup"><span data-stu-id="f413c-108">integerValue is a constant integer value.</span></span>

## <a name="remarks"></a><span data-ttu-id="f413c-109">Примечания</span><span class="sxs-lookup"><span data-stu-id="f413c-109">Remarks</span></span>



| <span data-ttu-id="f413c-110">Версии шейдеров пикселей</span><span class="sxs-lookup"><span data-stu-id="f413c-110">Pixel shader versions</span></span> | <span data-ttu-id="f413c-111">1\_1</span><span class="sxs-lookup"><span data-stu-id="f413c-111">1\_1</span></span> | <span data-ttu-id="f413c-112">1\_2</span><span class="sxs-lookup"><span data-stu-id="f413c-112">1\_2</span></span> | <span data-ttu-id="f413c-113">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="f413c-113">1\_3</span></span> | <span data-ttu-id="f413c-114">1\_4</span><span class="sxs-lookup"><span data-stu-id="f413c-114">1\_4</span></span> | <span data-ttu-id="f413c-115">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="f413c-115">2\_0</span></span> | <span data-ttu-id="f413c-116">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="f413c-116">2\_x</span></span> | <span data-ttu-id="f413c-117">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="f413c-117">2\_sw</span></span> | <span data-ttu-id="f413c-118">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="f413c-118">3\_0</span></span> | <span data-ttu-id="f413c-119">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="f413c-119">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="f413c-120">дефи</span><span class="sxs-lookup"><span data-stu-id="f413c-120">defi</span></span>                  |      |      |      |      |      | <span data-ttu-id="f413c-121">x</span><span class="sxs-lookup"><span data-stu-id="f413c-121">x</span></span>    | <span data-ttu-id="f413c-122">x</span><span class="sxs-lookup"><span data-stu-id="f413c-122">x</span></span>     | <span data-ttu-id="f413c-123">x</span><span class="sxs-lookup"><span data-stu-id="f413c-123">x</span></span>    | <span data-ttu-id="f413c-124">x</span><span class="sxs-lookup"><span data-stu-id="f413c-124">x</span></span>     |



 

<span data-ttu-id="f413c-125">Инструкция дефи определяет константу шейдера, значение которой загружается в любое время в качестве шейдера для устройства.</span><span class="sxs-lookup"><span data-stu-id="f413c-125">The defi instruction defines a shader constant whose value is loaded anytime a shader is set to a device.</span></span> <span data-ttu-id="f413c-126">Они называются прямыми константами.</span><span class="sxs-lookup"><span data-stu-id="f413c-126">These are called immediate constants.</span></span> <span data-ttu-id="f413c-127">Немедленные константы имеют приоритет над константами, заданными методом API Сетпикселшадерконстантб.</span><span class="sxs-lookup"><span data-stu-id="f413c-127">Immediate constants take precedence over constants set by the API method SetPixelShaderConstantB.</span></span>

<span data-ttu-id="f413c-128">Существует два способа задать константу в шейдере.</span><span class="sxs-lookup"><span data-stu-id="f413c-128">There are two ways to set a constant in a shader.</span></span>

1.  <span data-ttu-id="f413c-129">Используйте дефи, чтобы определить константу непосредственно внутри шейдера.</span><span class="sxs-lookup"><span data-stu-id="f413c-129">Use defi to define the constant directly inside a shader.</span></span>
2.  <span data-ttu-id="f413c-130">Используйте методы API для задания константы.</span><span class="sxs-lookup"><span data-stu-id="f413c-130">Use the API methods to set a constant.</span></span>
    -   <span data-ttu-id="f413c-131">Чтобы задать логическую константу, используйте [**сетпикселшадерконстантб**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setpixelshaderconstantb) .</span><span class="sxs-lookup"><span data-stu-id="f413c-131">Use [**SetPixelShaderConstantB**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setpixelshaderconstantb) to set a Boolean constant.</span></span>
    -   <span data-ttu-id="f413c-132">Используйте [**сетпикселшадерконстантф**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setpixelshaderconstantf) для установки константы с плавающей запятой.</span><span class="sxs-lookup"><span data-stu-id="f413c-132">Use [**SetPixelShaderConstantF**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setpixelshaderconstantf) to set a floating-point constant.</span></span>
    -   <span data-ttu-id="f413c-133">Используйте [**сетпикселшадерконстанти**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setpixelshaderconstanti) для установки целочисленной константы.</span><span class="sxs-lookup"><span data-stu-id="f413c-133">Use [**SetPixelShaderConstantI**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setpixelshaderconstanti) to set an integer constant.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f413c-134">См. также</span><span class="sxs-lookup"><span data-stu-id="f413c-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f413c-135">Инструкции шейдера пикселей</span><span class="sxs-lookup"><span data-stu-id="f413c-135">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 