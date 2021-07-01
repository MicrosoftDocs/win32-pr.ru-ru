---
title: Модели шейдеров и профили шейдеров
description: Модели шейдеров и профили шейдеров
ms.assetid: 6224f05e-20b1-42ea-96fb-63dd0edb720e
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 963e68d5875c3ee512e7e0d6ee7c243db72f4400
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/30/2021
ms.locfileid: "113119619"
---
# <a name="shader-models-vs-shader-profiles"></a><span data-ttu-id="3d1c4-103">Модели шейдеров и профили шейдеров</span><span class="sxs-lookup"><span data-stu-id="3d1c4-103">Shader Models vs Shader Profiles</span></span>

<span data-ttu-id="3d1c4-104">Язык заливки высокого уровня для DirectX реализует ряд моделей шейдеров.</span><span class="sxs-lookup"><span data-stu-id="3d1c4-104">The High Level Shading Language for DirectX implements a series of shader models.</span></span> <span data-ttu-id="3d1c4-105">С помощью HLSL можно создавать программируемые шейдеры C-LIKE для конвейера Direct3D.</span><span class="sxs-lookup"><span data-stu-id="3d1c4-105">Using HLSL, you can create C-like programmable shaders for the Direct3D pipeline.</span></span> <span data-ttu-id="3d1c4-106">Каждая модель шейдеров основана на возможностях модели до нее, реализуя дополнительные функции с меньшим количеством ограничений.</span><span class="sxs-lookup"><span data-stu-id="3d1c4-106">Each shader model builds on the capabilities of the model before it, implementing more functionality with fewer restrictions.</span></span>

<span data-ttu-id="3d1c4-107">Модель шейдеров 1 запущена с DirectX 8 и включенными инструкциями на уровне сборки и C.</span><span class="sxs-lookup"><span data-stu-id="3d1c4-107">Shader model 1 started with DirectX 8 and included assembly level and C-like instructions.</span></span> <span data-ttu-id="3d1c4-108">Эта модель имеет множество ограничений, вызванных ранним программируемым оборудованием шейдера.</span><span class="sxs-lookup"><span data-stu-id="3d1c4-108">This model has many limitations caused by early programmable shader hardware.</span></span> <span data-ttu-id="3d1c4-109">Модели шейдеров 2 и 3 значительно расширены на количество инструкций, а шейдеры констант могут использовать.</span><span class="sxs-lookup"><span data-stu-id="3d1c4-109">Shader model 2 and 3 greatly expanded on the number of instructions, and constants shaders could use.</span></span> <span data-ttu-id="3d1c4-110">Они гораздо более эффективны, чем модель шейдера 1, но по-прежнему имеют некоторые ограничения первой модели шейдера.</span><span class="sxs-lookup"><span data-stu-id="3d1c4-110">They are much more powerful than shader model 1, but still carry some of the existing limitations of the first shader model.</span></span>

<span data-ttu-id="3d1c4-111">Начиная с Windows Vista, модель шейдеров 4 полностью перерабатывается.</span><span class="sxs-lookup"><span data-stu-id="3d1c4-111">Starting with Windows Vista, shader model 4 is a complete redesign.</span></span> <span data-ttu-id="3d1c4-112">Она позволяет неограниченные инструкции и константы (в пределах аппаратных ограничений компьютера) иметь шаблонные объекты для очистки текстуры и повышения эффективности, а также минимальные ограничения любой модели шейдера.</span><span class="sxs-lookup"><span data-stu-id="3d1c4-112">It allows unlimited instructions and constants (within hardware constraints of your machine), has templated objects to make texture sampling cleaner and more efficient, and has the fewest restrictions of any shader model.</span></span> <span data-ttu-id="3d1c4-113">Однако для этого требуется WDM, который доступен только в операционной системе Windows Vista (или более поздней версии).</span><span class="sxs-lookup"><span data-stu-id="3d1c4-113">It does however require the Windows Driver Model which is only available on the Windows Vista (or later) operating system.</span></span>

## <a name="shader-profiles"></a><span data-ttu-id="3d1c4-114">Профили шейдеров</span><span class="sxs-lookup"><span data-stu-id="3d1c4-114">Shader Profiles</span></span>

<span data-ttu-id="3d1c4-115">Профиль шейдера является целевым объектом для компиляции шейдера; в этой таблице перечислены профили шейдеров, поддерживаемые каждой моделью шейдера.</span><span class="sxs-lookup"><span data-stu-id="3d1c4-115">A shader profile is the target for compiling a shader; this table lists the shader profiles that are supported by each shader model.</span></span>



| <span data-ttu-id="3d1c4-116">Модель шейдера</span><span class="sxs-lookup"><span data-stu-id="3d1c4-116">Shader model</span></span>                                                   | <span data-ttu-id="3d1c4-117">Профили шейдеров</span><span class="sxs-lookup"><span data-stu-id="3d1c4-117">Shader profiles</span></span>                                                                                                                                                                                                                                                                                                      |
|----------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="3d1c4-118">Модель шейдера 1</span><span class="sxs-lookup"><span data-stu-id="3d1c4-118">Shader Model 1</span></span>](dx-graphics-hlsl-sm1.md)         | <span data-ttu-id="3d1c4-119">VS \_ 1 \_ 1</span><span class="sxs-lookup"><span data-stu-id="3d1c4-119">vs\_1\_1</span></span>                                                                                                                                                                                                                                                                                              |
| [<span data-ttu-id="3d1c4-120">Модель шейдера 2</span><span class="sxs-lookup"><span data-stu-id="3d1c4-120">Shader Model 2</span></span>](dx-graphics-hlsl-sm2.md)         | <span data-ttu-id="3d1c4-121">PS \_ 2 \_ 0, PS \_ 2 \_ x, VS \_ 2 \_ 0, VS \_ 2 \_ x, PS \_ 4 \_ 0 \_ Level \_ 9 \_ 0, PS \_ 4 \_ 0 \_ уровня \_ 9 \_ 1, PS \_ 4 \_ 0 \_ уровня \_ 9 \_ 3, VS \_ 4 \_ 0 \_ уровня \_ 9 \_ 0, VS \_ 4 \_ 0 \_ уровня 9 1, \_ VS \_ \_ 4 \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ 0 уровня 9 3, 9 3 (lib 4 0)</span><span class="sxs-lookup"><span data-stu-id="3d1c4-121">ps\_2\_0, ps\_2\_x, vs\_2\_0, vs\_2\_x, ps\_4\_0\_level\_9\_0, ps\_4\_0\_level\_9\_1, ps\_4\_0\_level\_9\_3, vs\_4\_0\_level\_9\_0, vs\_4\_0\_level\_9\_1, vs\_4\_0\_level\_9\_3, lib\_4\_0\_level\_9\_1, lib\_4\_0\_level\_9\_3</span></span>                                                                      |
| [<span data-ttu-id="3d1c4-122">Модель шейдера 3</span><span class="sxs-lookup"><span data-stu-id="3d1c4-122">Shader Model 3</span></span>](dx-graphics-hlsl-sm3.md)         | <span data-ttu-id="3d1c4-123">PS \_ 3 \_ 0, VS \_ 3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="3d1c4-123">ps\_3\_0, vs\_3\_0</span></span>                                                                                                                                                                                                                                                                                    |
| [<span data-ttu-id="3d1c4-124">Модель шейдера 4</span><span class="sxs-lookup"><span data-stu-id="3d1c4-124">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)         | <span data-ttu-id="3d1c4-125">CS \_ 4 \_ 0, GS \_ 4 \_ 0, PS \_ 4 \_ 0, VS \_ 4 \_ 0, CS \_ 4 \_ 1, GS \_ 4 \_ 1, PS \_ 4 \_ 1, VS \_ 4 \_ 1, lib \_ 4 \_ 0, lib \_ 4 \_ 1</span><span class="sxs-lookup"><span data-stu-id="3d1c4-125">cs\_4\_0, gs\_4\_0, ps\_4\_0, vs\_4\_0, cs\_4\_1, gs\_4\_1, ps\_4\_1, vs\_4\_1, lib\_4\_0, lib\_4\_1</span></span>                                                                                                                                                                                                  |
| [<span data-ttu-id="3d1c4-126">Модель шейдера 5</span><span class="sxs-lookup"><span data-stu-id="3d1c4-126">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md) | <span data-ttu-id="3d1c4-127">CS \_ 5 \_ 0, DS \_ 5 \_ 0, GS \_ 5 \_ 0, HS \_ 5 0, \_ PS \_ 5 \_ 0, VS \_ 5 \_ 0, lib \_ 5 \_ 0 (хотя GS \_ 4 \_ 0, GS \_ 4 \_ 1, PS \_ 4 \_ 0, PS \_ 4 \_ 1, VS \_ 4 \_ 0 и VS \_ 4 \_ 1 были введены в модель шейдера 4,0, в модели шейдера 5 добавлена поддержка этих профилей шейдеров для структурированных буферов и буферов байтового адреса.)</span><span class="sxs-lookup"><span data-stu-id="3d1c4-127">cs\_5\_0, ds\_5\_0, gs\_5\_0, hs\_5\_0, ps\_5\_0, vs\_5\_0, lib\_5\_0 (Although gs\_4\_0, gs\_4\_1, ps\_4\_0, ps\_4\_1, vs\_4\_0, and vs\_4\_1 were introduced in shader model 4.0, shader model 5 adds support to these shader profiles for structured buffers and byte address buffers.)</span></span><br/> |
| [<span data-ttu-id="3d1c4-128">Модель шейдеров 6</span><span class="sxs-lookup"><span data-stu-id="3d1c4-128">Shader Model 6</span></span>](shader-model-6-0.md)             | <span data-ttu-id="3d1c4-129">CS \_ 6 \_ 0, DS \_ 6 \_ 0, GS \_ 6 \_ 0, HS \_ 6 \_ 0, PS \_ 6 \_ 0, VS \_ 6 \_ 0, lib \_ 6 \_ 0</span><span class="sxs-lookup"><span data-stu-id="3d1c4-129">cs\_6\_0, ds\_6\_0, gs\_6\_0, hs\_6\_0, ps\_6\_0, vs\_6\_0, lib\_6\_0</span></span>                                                                                                                                                                                                                                 |

<span data-ttu-id="3d1c4-130">Различия между Direct3D 9 и Direct3D 10:</span><span class="sxs-lookup"><span data-stu-id="3d1c4-130">Differences between Direct3D 9 and Direct3D 10:</span></span>

- <span data-ttu-id="3d1c4-131">В Direct3D 9 появились модели шейдеров 1, 2 и 3.</span><span class="sxs-lookup"><span data-stu-id="3d1c4-131">Direct3D 9 introduced shader models 1, 2, and 3.</span></span>
- <span data-ttu-id="3d1c4-132">В Direct3D 10 появилась модель шейдера 4.</span><span class="sxs-lookup"><span data-stu-id="3d1c4-132">Direct3D 10 introduced shader model 4.</span></span>
- <span data-ttu-id="3d1c4-133">В Direct3D 10,1 появилась модель шейдера 4,1.</span><span class="sxs-lookup"><span data-stu-id="3d1c4-133">Direct3D 10.1 introduced shader model 4.1.</span></span>



 

## <a name="effect-profiles"></a><span data-ttu-id="3d1c4-134">Профили эффектов</span><span class="sxs-lookup"><span data-stu-id="3d1c4-134">Effect Profiles</span></span>

<span data-ttu-id="3d1c4-135">Профиль эффектов является целевым объектом для компиляции эффектов и шейдеров. в этой таблице перечислены профили эффектов, поддерживаемые каждой версией Direct3D.</span><span class="sxs-lookup"><span data-stu-id="3d1c4-135">An effect profile is the target for compiling an effect/shader; this table lists the effect profiles that are supported by each version of Direct3D.</span></span>

<span data-ttu-id="3d1c4-136">Различия между Direct3D 9 и Direct3D 10:</span><span class="sxs-lookup"><span data-stu-id="3d1c4-136">Differences between Direct3D 9 and Direct3D 10:</span></span>

- <span data-ttu-id="3d1c4-137">В Direct3D 9 появился результат: Framework Profiles FX \_ 1 \_ 0 и FX \_ 2 \_ 0.</span><span class="sxs-lookup"><span data-stu-id="3d1c4-137">Direct3D 9 introduced effect-framework profiles fx\_1\_0 and fx\_2\_0.</span></span>
- <span data-ttu-id="3d1c4-138">В Direct3D 10 появился результат — профиль платформы FX \_ 4 \_ 0.</span><span class="sxs-lookup"><span data-stu-id="3d1c4-138">Direct3D 10 introduced effect-framework profile fx\_4\_0.</span></span>
- <span data-ttu-id="3d1c4-139">В Direct3D 10,1 появился результат — профиль платформы FX \_ 4 \_ 1.</span><span class="sxs-lookup"><span data-stu-id="3d1c4-139">Direct3D 10.1 introduced effect-framework profile fx\_4\_1.</span></span>
- <span data-ttu-id="3d1c4-140">Появившийся результат Direct3D 11 — профиль платформы FX \_ 5 \_ 0.</span><span class="sxs-lookup"><span data-stu-id="3d1c4-140">Direct3D 11 introduced effect-framework profile fx\_5\_0.</span></span>

> [!Note]  
> <span data-ttu-id="3d1c4-141">Эти профили устаревших эффектов являются устаревшими.</span><span class="sxs-lookup"><span data-stu-id="3d1c4-141">These legacy effects profiles are deprecated.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="3d1c4-142">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="3d1c4-142">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3d1c4-143">Справочник по HLSL</span><span class="sxs-lookup"><span data-stu-id="3d1c4-143">Reference for HLSL</span></span>](dx-graphics-hlsl-reference.md)
</dt> </dl>

 

 





