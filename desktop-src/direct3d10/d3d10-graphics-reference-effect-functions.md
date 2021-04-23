---
description: 'В этом разделе содержатся сведения о следующих функциях эффектов:'
ms.assetid: b76643f0-387f-49c6-80e5-4d7b406b4db7
title: Функции эффектов (Direct3D 10)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 111fdcb34bbf1d9a86a295e62f734938991dda99
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104539041"
---
# <a name="effect-functions-direct3d-10"></a><span data-ttu-id="ec5fe-103">Функции эффектов (Direct3D 10)</span><span class="sxs-lookup"><span data-stu-id="ec5fe-103">Effect Functions (Direct3D 10)</span></span>

<span data-ttu-id="ec5fe-104">В этом разделе содержатся сведения о следующих функциях эффектов:</span><span class="sxs-lookup"><span data-stu-id="ec5fe-104">This section contains information about the following effect functions:</span></span>



| <span data-ttu-id="ec5fe-105">Функции</span><span class="sxs-lookup"><span data-stu-id="ec5fe-105">Functions</span></span>                                                                      | <span data-ttu-id="ec5fe-106">Описание</span><span class="sxs-lookup"><span data-stu-id="ec5fe-106">Description</span></span>                                                         |
|--------------------------------------------------------------------------------|---------------------------------------------------------------------|
| [<span data-ttu-id="ec5fe-107">**D3D10CompileEffectFromMemory**</span><span class="sxs-lookup"><span data-stu-id="ec5fe-107">**D3D10CompileEffectFromMemory**</span></span>](/windows/desktop/api/D3D10Effect/nf-d3d10effect-d3d10compileeffectfrommemory)           | <span data-ttu-id="ec5fe-108">Компиляция результата.</span><span class="sxs-lookup"><span data-stu-id="ec5fe-108">Compile an effect.</span></span>                                                  |
| [<span data-ttu-id="ec5fe-109">**D3D10CreateEffectFromMemory**</span><span class="sxs-lookup"><span data-stu-id="ec5fe-109">**D3D10CreateEffectFromMemory**</span></span>](/windows/desktop/api/D3D10Effect/nf-d3d10effect-d3d10createeffectfrommemory)             | <span data-ttu-id="ec5fe-110">Создание результата.</span><span class="sxs-lookup"><span data-stu-id="ec5fe-110">Create an effect.</span></span>                                                   |
| [<span data-ttu-id="ec5fe-111">**D3D10CreateEffectPoolFromMemory**</span><span class="sxs-lookup"><span data-stu-id="ec5fe-111">**D3D10CreateEffectPoolFromMemory**</span></span>](/windows/desktop/api/D3D10Effect/nf-d3d10effect-d3d10createeffectpoolfrommemory)     | <span data-ttu-id="ec5fe-112">Создайте пул эффектов.</span><span class="sxs-lookup"><span data-stu-id="ec5fe-112">Create an effect pool.</span></span>                                              |
| [<span data-ttu-id="ec5fe-113">**D3D10CreateStateBlock**</span><span class="sxs-lookup"><span data-stu-id="ec5fe-113">**D3D10CreateStateBlock**</span></span>](/windows/desktop/api/D3D10Effect/nf-d3d10effect-d3d10createstateblock)                         | <span data-ttu-id="ec5fe-114">Создайте блок состояния.</span><span class="sxs-lookup"><span data-stu-id="ec5fe-114">Create a state block.</span></span>                                               |
| [<span data-ttu-id="ec5fe-115">**D3D10DisassembleEffect**</span><span class="sxs-lookup"><span data-stu-id="ec5fe-115">**D3D10DisassembleEffect**</span></span>](/windows/desktop/api/D3D10Effect/nf-d3d10effect-d3d10disassembleeffect)                       | <span data-ttu-id="ec5fe-116">Разберите скомпилированный результат в инструкции по сборке шейдера.</span><span class="sxs-lookup"><span data-stu-id="ec5fe-116">Disassemble a compiled effect into shader assembly instructions.</span></span>    |
| [<span data-ttu-id="ec5fe-117">**D3D10StateBlockMaskDifference**</span><span class="sxs-lookup"><span data-stu-id="ec5fe-117">**D3D10StateBlockMaskDifference**</span></span>](/windows/desktop/api/D3D10Effect/nf-d3d10effect-d3d10stateblockmaskdifference)         | <span data-ttu-id="ec5fe-118">Объедините две маски блоков состояния с битовой операцией XOR.</span><span class="sxs-lookup"><span data-stu-id="ec5fe-118">Combine two state-block masks with a bitwise XOR.</span></span>                   |
| [<span data-ttu-id="ec5fe-119">**D3D10StateBlockMaskDisableAll**</span><span class="sxs-lookup"><span data-stu-id="ec5fe-119">**D3D10StateBlockMaskDisableAll**</span></span>](/windows/desktop/api/D3D10Effect/nf-d3d10effect-d3d10stateblockmaskdisableall)         | <span data-ttu-id="ec5fe-120">Отключение захвата состояния.</span><span class="sxs-lookup"><span data-stu-id="ec5fe-120">Disable state capturing.</span></span>                                            |
| [<span data-ttu-id="ec5fe-121">**D3D10StateBlockMaskDisableCapture**</span><span class="sxs-lookup"><span data-stu-id="ec5fe-121">**D3D10StateBlockMaskDisableCapture**</span></span>](/windows/desktop/api/D3D10Effect/nf-d3d10effect-d3d10stateblockmaskdisablecapture) | <span data-ttu-id="ec5fe-122">Отключение захвата состояния с маской блока состояния.</span><span class="sxs-lookup"><span data-stu-id="ec5fe-122">Disable state capturing with a state-block mask.</span></span>                    |
| [<span data-ttu-id="ec5fe-123">**D3D10StateBlockMaskEnableAll**</span><span class="sxs-lookup"><span data-stu-id="ec5fe-123">**D3D10StateBlockMaskEnableAll**</span></span>](/windows/desktop/api/D3D10Effect/nf-d3d10effect-d3d10stateblockmaskenableall)           | <span data-ttu-id="ec5fe-124">Включите маску блока состояния для записи и применения всех переменных состояния.</span><span class="sxs-lookup"><span data-stu-id="ec5fe-124">Enable a state-block mask to capture and apply all state variables.</span></span> |
| [<span data-ttu-id="ec5fe-125">**D3D10StateBlockMaskEnableCapture**</span><span class="sxs-lookup"><span data-stu-id="ec5fe-125">**D3D10StateBlockMaskEnableCapture**</span></span>](/windows/desktop/api/D3D10Effect/nf-d3d10effect-d3d10stateblockmaskenablecapture)   | <span data-ttu-id="ec5fe-126">Включить диапазон значений состояния в маске блока состояния.</span><span class="sxs-lookup"><span data-stu-id="ec5fe-126">Enable a range of state values in a state block mask.</span></span>               |
| [<span data-ttu-id="ec5fe-127">**D3D10StateBlockMaskGetSetting**</span><span class="sxs-lookup"><span data-stu-id="ec5fe-127">**D3D10StateBlockMaskGetSetting**</span></span>](/windows/desktop/api/D3D10Effect/nf-d3d10effect-d3d10stateblockmaskgetsetting)         | <span data-ttu-id="ec5fe-128">Получение элемента в маске блока состояния.</span><span class="sxs-lookup"><span data-stu-id="ec5fe-128">Get an element in a state-block mask.</span></span>                               |
| [<span data-ttu-id="ec5fe-129">**D3D10StateBlockMaskIntersect**</span><span class="sxs-lookup"><span data-stu-id="ec5fe-129">**D3D10StateBlockMaskIntersect**</span></span>](/windows/desktop/api/D3D10Effect/nf-d3d10effect-d3d10stateblockmaskintersect)           | <span data-ttu-id="ec5fe-130">Объедините две маски блоков состояния с побитовой и.</span><span class="sxs-lookup"><span data-stu-id="ec5fe-130">Combine two state-block masks with a bitwise AND.</span></span>                   |
| [<span data-ttu-id="ec5fe-131">**D3D10StateBlockMaskUnion**</span><span class="sxs-lookup"><span data-stu-id="ec5fe-131">**D3D10StateBlockMaskUnion**</span></span>](/windows/desktop/api/D3D10Effect/nf-d3d10effect-d3d10stateblockmaskunion)                   | <span data-ttu-id="ec5fe-132">Объедините две маски блоков состояния с побитовой или.</span><span class="sxs-lookup"><span data-stu-id="ec5fe-132">Combine two state-block masks with a bitwise OR.</span></span>                    |



 

## <a name="related-topics"></a><span data-ttu-id="ec5fe-133">См. также</span><span class="sxs-lookup"><span data-stu-id="ec5fe-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ec5fe-134">Справочник по действиям</span><span class="sxs-lookup"><span data-stu-id="ec5fe-134">Effect Reference</span></span>](d3d10-graphics-reference-effect.md)
</dt> </dl>

 

 



