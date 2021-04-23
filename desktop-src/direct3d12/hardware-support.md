---
title: Уровни оборудования
description: Уровни оборудования от уровня 1 до уровня 3 увеличивают ресурсы, доступные для конвейера.
ms.assetid: 5A640BA9-3914-4481-9A0C-E18B52BD8AFE
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 38773412d135aa4068f0f843c1a6ef64af06a841
ms.sourcegitcommit: 9d7585cb0b840d0d1a2b7fd02135181e69d0dc9d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/15/2020
ms.locfileid: "104548926"
---
# <a name="hardware-tiers"></a><span data-ttu-id="5ee0e-103">Уровни оборудования</span><span class="sxs-lookup"><span data-stu-id="5ee0e-103">Hardware Tiers</span></span>

<span data-ttu-id="5ee0e-104">Уровни оборудования от уровня 1 до уровня 3 увеличивают ресурсы, доступные для конвейера.</span><span class="sxs-lookup"><span data-stu-id="5ee0e-104">The levels of hardware from Tier 1 to Tier 3 have increasing resources available to the pipeline.</span></span>

-   [<span data-ttu-id="5ee0e-105">Ограничения, зависящие от оборудования</span><span class="sxs-lookup"><span data-stu-id="5ee0e-105">Limits dependant on hardware</span></span>](#limits-dependant-on-hardware)
-   [<span data-ttu-id="5ee0e-106">Ограничения для неизменяемых переменных</span><span class="sxs-lookup"><span data-stu-id="5ee0e-106">Invariable limits</span></span>](#invariable-limits)
-   [<span data-ttu-id="5ee0e-107">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="5ee0e-107">Related topics</span></span>](#related-topics)

## <a name="limits-dependant-on-hardware"></a><span data-ttu-id="5ee0e-108">Ограничения, зависящие от оборудования</span><span class="sxs-lookup"><span data-stu-id="5ee0e-108">Limits dependant on hardware</span></span>



| <span data-ttu-id="5ee0e-109">Ресурсы, доступные для конвейера</span><span class="sxs-lookup"><span data-stu-id="5ee0e-109">Resources Available to the Pipeline</span></span>                                                                                                              | <span data-ttu-id="5ee0e-110">Уровень 1</span><span class="sxs-lookup"><span data-stu-id="5ee0e-110">Tier 1</span></span>                                                                   | <span data-ttu-id="5ee0e-111">Уровень 2</span><span class="sxs-lookup"><span data-stu-id="5ee0e-111">Tier 2</span></span>        | <span data-ttu-id="5ee0e-112">Уровень 3</span><span class="sxs-lookup"><span data-stu-id="5ee0e-112">Tier 3</span></span>        |
|--------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|---------------|---------------|
| <span data-ttu-id="5ee0e-113">Уровни компонентов</span><span class="sxs-lookup"><span data-stu-id="5ee0e-113">Feature levels</span></span>                                                                                                                                   | <span data-ttu-id="5ee0e-114">11.0 +</span><span class="sxs-lookup"><span data-stu-id="5ee0e-114">11.0+</span></span>                                                                    | <span data-ttu-id="5ee0e-115">11.0 +</span><span class="sxs-lookup"><span data-stu-id="5ee0e-115">11.0+</span></span>         | <span data-ttu-id="5ee0e-116">11.1 +</span><span class="sxs-lookup"><span data-stu-id="5ee0e-116">11.1+</span></span>         |
| <span data-ttu-id="5ee0e-117">Максимальное число дескрипторов в представлении постоянного буфера (CBV), шейдер представление ресурсов (SRV) или неупорядоченное представление доступа (UAV), используемое для отрисовки</span><span class="sxs-lookup"><span data-stu-id="5ee0e-117">Maximum number of descriptors in a Constant Buffer View (CBV), Shader Resource View (SRV), or Unordered Access View(UAV) heap used for rendering</span></span> | <span data-ttu-id="5ee0e-118">1 000 000</span><span class="sxs-lookup"><span data-stu-id="5ee0e-118">1,000,000</span></span>                                                                | <span data-ttu-id="5ee0e-119">1 000 000</span><span class="sxs-lookup"><span data-stu-id="5ee0e-119">1,000,000</span></span>     | <span data-ttu-id="5ee0e-120">1000000 +</span><span class="sxs-lookup"><span data-stu-id="5ee0e-120">1,000,000+</span></span>    |
| <span data-ttu-id="5ee0e-121">Максимальное число представлений буфера констант во всех таблицах дескрипторов на каждый этап шейдера</span><span class="sxs-lookup"><span data-stu-id="5ee0e-121">Maximum number of Constant Buffer Views in all descriptor tables per shader stage</span></span>                                                                | <span data-ttu-id="5ee0e-122">14</span><span class="sxs-lookup"><span data-stu-id="5ee0e-122">14</span></span>                                                                       | <span data-ttu-id="5ee0e-123">14</span><span class="sxs-lookup"><span data-stu-id="5ee0e-123">14</span></span>            | <span data-ttu-id="5ee0e-124">**Полная куча**</span><span class="sxs-lookup"><span data-stu-id="5ee0e-124">**full heap**</span></span> |
| <span data-ttu-id="5ee0e-125">Максимальное число представлений ресурсов шейдера во всех таблицах дескрипторов на каждый этап шейдера</span><span class="sxs-lookup"><span data-stu-id="5ee0e-125">Maximum number of Shader Resource Views in all descriptor tables per shader stage</span></span>                                                                | <span data-ttu-id="5ee0e-126">128</span><span class="sxs-lookup"><span data-stu-id="5ee0e-126">128</span></span>                                                                      | <span data-ttu-id="5ee0e-127">**Полная куча**</span><span class="sxs-lookup"><span data-stu-id="5ee0e-127">**full heap**</span></span> | <span data-ttu-id="5ee0e-128">Полная куча</span><span class="sxs-lookup"><span data-stu-id="5ee0e-128">full heap</span></span>     |
| <span data-ttu-id="5ee0e-129">Максимальное число неупорядоченных представлений доступа во всех таблицах дескрипторов на всех этапах</span><span class="sxs-lookup"><span data-stu-id="5ee0e-129">Maximum number of Unordered Access Views in all descriptor tables across all stages</span></span>                                                              | <span data-ttu-id="5ee0e-130">64 для уровней компонентов 11.1 +</span><span class="sxs-lookup"><span data-stu-id="5ee0e-130">64 for feature levels 11.1+</span></span><br/> <span data-ttu-id="5ee0e-131">8 для уровня функции 11</span><span class="sxs-lookup"><span data-stu-id="5ee0e-131">8 for feature level 11</span></span><br/> | <span data-ttu-id="5ee0e-132">64</span><span class="sxs-lookup"><span data-stu-id="5ee0e-132">64</span></span>            | <span data-ttu-id="5ee0e-133">**Полная куча**</span><span class="sxs-lookup"><span data-stu-id="5ee0e-133">**full heap**</span></span> |
| <span data-ttu-id="5ee0e-134">Максимальное число проб во всех таблицах дескрипторов на каждый этап шейдера</span><span class="sxs-lookup"><span data-stu-id="5ee0e-134">Maximum number of Samplers in all descriptor tables per shader stage</span></span>                                                                             | <span data-ttu-id="5ee0e-135">16</span><span class="sxs-lookup"><span data-stu-id="5ee0e-135">16</span></span>                                                                       | <span data-ttu-id="5ee0e-136">**2048**</span><span class="sxs-lookup"><span data-stu-id="5ee0e-136">**2048**</span></span> | <span data-ttu-id="5ee0e-137">2048</span><span class="sxs-lookup"><span data-stu-id="5ee0e-137">2048</span></span>     |



 

<span data-ttu-id="5ee0e-138">Записи, **выделенные жирным шрифтом** , выделяют значительные улучшения на предыдущем уровне.</span><span class="sxs-lookup"><span data-stu-id="5ee0e-138">**Bold** entries highlight significant improvements over the previous tier.</span></span>

<span data-ttu-id="5ee0e-139">Существует дополнительное ограничение для оборудования уровня 1, которое применяется ко всем кучам и к оборудованию уровня 2, которое применяется к кучам CBV и UAV, что все записи кучи дескрипторов, покрываемые таблицами дескрипторов в корневой подписи, *должны* быть заполнены дескрипторами по времени выполнения шейдера, даже если в шейдере (возможно, из-за ветвления) не требуется дескриптор.</span><span class="sxs-lookup"><span data-stu-id="5ee0e-139">There is an additional restriction for Tier 1 hardware that applies to all heaps, and to Tier 2 hardware that applies to CBV and UAV heaps, that all descriptor heap entries covered by descriptor tables in the root signature *must* be populated with descriptors by the time the shader executes, even if the shader (perhaps due to branching) does not need the descriptor.</span></span> <span data-ttu-id="5ee0e-140">Такого ограничения для оборудования уровня 3 нет.</span><span class="sxs-lookup"><span data-stu-id="5ee0e-140">There is no such restriction for Tier 3 hardware.</span></span> <span data-ttu-id="5ee0e-141">Одним из рисков для этого ограничения является использование [дескрипторов NULL](descriptors.md).</span><span class="sxs-lookup"><span data-stu-id="5ee0e-141">One mitigation for this restriction is the diligent use of [Null descriptors](descriptors.md).</span></span>

## <a name="invariable-limits"></a><span data-ttu-id="5ee0e-142">Ограничения для неизменяемых переменных</span><span class="sxs-lookup"><span data-stu-id="5ee0e-142">Invariable limits</span></span>

<span data-ttu-id="5ee0e-143">Максимальное число образцов в куче видимых дескрипторов шейдера — 2048.</span><span class="sxs-lookup"><span data-stu-id="5ee0e-143">The maximum number of samplers in a shader visible descriptor heap is 2048.</span></span>

<span data-ttu-id="5ee0e-144">Максимальное число уникальных статических выборок в активных корневых форматах — 2032 (это оставляет 16 для драйверов, которым требуются собственные пробы).</span><span class="sxs-lookup"><span data-stu-id="5ee0e-144">The maximum number of unique static samplers across live root signatures is 2032 (which leaves 16 for drivers that need their own samplers).</span></span>

## <a name="related-topics"></a><span data-ttu-id="5ee0e-145">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="5ee0e-145">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5ee0e-146">Кучи дескрипторов</span><span class="sxs-lookup"><span data-stu-id="5ee0e-146">Descriptor Heaps</span></span>](descriptor-heaps.md)
</dt> <dt>

[<span data-ttu-id="5ee0e-147">Уровни компонентов оборудования</span><span class="sxs-lookup"><span data-stu-id="5ee0e-147">Hardware Feature Levels</span></span>](hardware-feature-levels.md)
</dt> </dl>

 

 





