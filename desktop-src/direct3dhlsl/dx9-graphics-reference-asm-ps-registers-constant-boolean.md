---
title: Константный логический регистр (Справочник по HLSL PS)
description: Этот регистр представляет собой коллекцию битов, используемых в инструкциях статического управления потоком (например, если bool-PS-else-PS-endif-PS).
ms.assetid: fb4abe19-d0cf-48ac-866e-4be60cc86bd6
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 4868be7c22ce5a6a1881ad7db8acf0af65330c04
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "103793014"
---
# <a name="constant-boolean-register-hlsl-ps-reference"></a><span data-ttu-id="a9a62-103">Константный логический регистр (Справочник по HLSL PS)</span><span class="sxs-lookup"><span data-stu-id="a9a62-103">Constant Boolean register (HLSL PS reference)</span></span>

<span data-ttu-id="a9a62-104">Этот регистр представляет собой коллекцию битов, используемых в инструкциях статического управления потоком (например, [Если bool-PS](if-bool---ps.md)  -  [else-PS](else---ps.md)  -  [endif-PS](endif---ps.md)).</span><span class="sxs-lookup"><span data-stu-id="a9a62-104">This register is a collection of bits used in static flow control instructions (for example, [if bool - ps](if-bool---ps.md) - [else - ps](else---ps.md) - [endif - ps](endif---ps.md)).</span></span> <span data-ttu-id="a9a62-105">Это 16 из них, поэтому шейдер может иметь 16 независимых условий ветвления.</span><span class="sxs-lookup"><span data-stu-id="a9a62-105">There are 16 of them, therefore, a shader can have 16 independent branch conditions.</span></span> <span data-ttu-id="a9a62-106">Их можно задать с помощью [дефб-PS](defb---ps.md) или [**сетпикселшадерконстантб**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setpixelshaderconstantb).</span><span class="sxs-lookup"><span data-stu-id="a9a62-106">They can be set using [defb - ps](defb---ps.md) or [**SetPixelShaderConstantB**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setpixelshaderconstantb).</span></span>

<span data-ttu-id="a9a62-107">Поведение констант шейдера изменилось между Direct3D 8 и Direct3D 9.</span><span class="sxs-lookup"><span data-stu-id="a9a62-107">The behavior of shader constants has changed between Direct3D 8 and Direct3D 9.</span></span>

-   <span data-ttu-id="a9a62-108">Для Direct3D 9 константы, заданные с помощью дефкс, присваивают значения константному пространству шейдера.</span><span class="sxs-lookup"><span data-stu-id="a9a62-108">For Direct3D 9, constants set with defx assign values to the shader constant space.</span></span> <span data-ttu-id="a9a62-109">Время существования константы, объявленной с помощью дефкс, ограничено выполнением только этого шейдера.</span><span class="sxs-lookup"><span data-stu-id="a9a62-109">The lifetime of a constant declared with defx is confined to the execution of that shader only.</span></span> <span data-ttu-id="a9a62-110">И наоборот, константы, заданные с помощью API-интерфейсов, Сетксксксшадерконстанткс инициализировать константы в глобальном пространстве.</span><span class="sxs-lookup"><span data-stu-id="a9a62-110">Conversely, constants set using the APIs SetXXXShaderConstantX initialize constants in global space.</span></span> <span data-ttu-id="a9a62-111">Константы в глобальном пространстве не копируются в локальное пространство (видимую шейдеру) до тех пор, пока не будет вызван Сетксксксшадерконстантс.</span><span class="sxs-lookup"><span data-stu-id="a9a62-111">Constants in global space are not copied to local space (visible to the shader) until SetxxxShaderConstants is called.</span></span>
-   <span data-ttu-id="a9a62-112">Для Direct3D 8 константы, заданные с помощью дефкс или API, присваивают значения константному пространству шейдера.</span><span class="sxs-lookup"><span data-stu-id="a9a62-112">For Direct3D 8, constants set with defx or the APIs both assign values to the shader constant space.</span></span> <span data-ttu-id="a9a62-113">При каждом выполнении шейдера все константы используются текущим шейдером независимо от метода, используемого для их установки.</span><span class="sxs-lookup"><span data-stu-id="a9a62-113">Each time the shader is executed, the constants are used by the current shader regardless of the technique used to set them.</span></span>



| <span data-ttu-id="a9a62-114">Версии шейдеров пикселей</span><span class="sxs-lookup"><span data-stu-id="a9a62-114">Pixel shader versions</span></span>     | <span data-ttu-id="a9a62-115">1\_1</span><span class="sxs-lookup"><span data-stu-id="a9a62-115">1\_1</span></span> | <span data-ttu-id="a9a62-116">1\_2</span><span class="sxs-lookup"><span data-stu-id="a9a62-116">1\_2</span></span> | <span data-ttu-id="a9a62-117">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="a9a62-117">1\_3</span></span> | <span data-ttu-id="a9a62-118">1\_4</span><span class="sxs-lookup"><span data-stu-id="a9a62-118">1\_4</span></span> | <span data-ttu-id="a9a62-119">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="a9a62-119">2\_0</span></span> | <span data-ttu-id="a9a62-120">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="a9a62-120">2\_sw</span></span> | <span data-ttu-id="a9a62-121">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="a9a62-121">2\_x</span></span> | <span data-ttu-id="a9a62-122">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="a9a62-122">3\_0</span></span> | <span data-ttu-id="a9a62-123">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="a9a62-123">3\_sw</span></span> |
|---------------------------|------|------|------|------|------|-------|------|------|-------|
| <span data-ttu-id="a9a62-124">Постоянный логический регистр</span><span class="sxs-lookup"><span data-stu-id="a9a62-124">Constant Boolean register</span></span> |      |      |      |      |      |       | <span data-ttu-id="a9a62-125">x</span><span class="sxs-lookup"><span data-stu-id="a9a62-125">x</span></span>    | <span data-ttu-id="a9a62-126">x</span><span class="sxs-lookup"><span data-stu-id="a9a62-126">x</span></span>    | <span data-ttu-id="a9a62-127">x</span><span class="sxs-lookup"><span data-stu-id="a9a62-127">x</span></span>     |



 

## <a name="related-topics"></a><span data-ttu-id="a9a62-128">См. также</span><span class="sxs-lookup"><span data-stu-id="a9a62-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a9a62-129">Регистры</span><span class="sxs-lookup"><span data-stu-id="a9a62-129">Registers</span></span>](dx9-graphics-reference-asm-ps-registers.md)
</dt> </dl>

 

 