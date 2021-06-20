---
title: Регистр счетчиков циклов (Справочник по HLSL PS)
description: Ознакомьтесь с регистром счетчиков циклов для шейдеров пикселей. Единственный регистр в этом банке — регистрация текущего цикла (aL).
ms.assetid: 36999873-a251-4939-aac0-faa7f910bc33
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: b2a2f7f42c83308fa72ceae2875c35c600dfd7db
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/19/2021
ms.locfileid: "112405517"
---
# <a name="loop-counter-register-hlsl-ps-reference"></a><span data-ttu-id="295f3-104">Регистр счетчиков циклов (Справочник по HLSL PS)</span><span class="sxs-lookup"><span data-stu-id="295f3-104">Loop counter register (HLSL PS reference)</span></span>

<span data-ttu-id="295f3-105">Единственный регистр в этом банке — регистрация текущего цикла (aL).</span><span class="sxs-lookup"><span data-stu-id="295f3-105">The only register in this bank is the current loop counter (aL) register.</span></span> <span data-ttu-id="295f3-106">Он автоматически увеличивается при каждом выполнении блока [Loop-PS](loop---ps.md) / [ендлуп-PS](endloop---ps.md) .</span><span class="sxs-lookup"><span data-stu-id="295f3-106">It automatically gets incremented in each execution of the [loop - ps](loop---ps.md)/[endloop - ps](endloop---ps.md) block.</span></span> <span data-ttu-id="295f3-107">Поэтому его можно использовать в блоке для относительной адресации, если это необходимо, и недопустимо использовать его за пределами цикла.</span><span class="sxs-lookup"><span data-stu-id="295f3-107">So it can be used in the block for relative addressing if needed and is invalid to use it outside the loop.</span></span>



| <span data-ttu-id="295f3-108">Версии шейдеров пикселей</span><span class="sxs-lookup"><span data-stu-id="295f3-108">Pixel shader versions</span></span> | <span data-ttu-id="295f3-109">1\_1</span><span class="sxs-lookup"><span data-stu-id="295f3-109">1\_1</span></span> | <span data-ttu-id="295f3-110">1\_2</span><span class="sxs-lookup"><span data-stu-id="295f3-110">1\_2</span></span> | <span data-ttu-id="295f3-111">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="295f3-111">1\_3</span></span> | <span data-ttu-id="295f3-112">1\_4</span><span class="sxs-lookup"><span data-stu-id="295f3-112">1\_4</span></span> | <span data-ttu-id="295f3-113">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="295f3-113">2\_0</span></span> | <span data-ttu-id="295f3-114">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="295f3-114">2\_sw</span></span> | <span data-ttu-id="295f3-115">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="295f3-115">2\_x</span></span> | <span data-ttu-id="295f3-116">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="295f3-116">3\_0</span></span> | <span data-ttu-id="295f3-117">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="295f3-117">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|-------|------|------|-------|
| <span data-ttu-id="295f3-118">Регистр счетчика цикла</span><span class="sxs-lookup"><span data-stu-id="295f3-118">Loop Counter Register</span></span> |      |      |      |      |      |       |      | <span data-ttu-id="295f3-119">x</span><span class="sxs-lookup"><span data-stu-id="295f3-119">x</span></span>    | <span data-ttu-id="295f3-120">x</span><span class="sxs-lookup"><span data-stu-id="295f3-120">x</span></span>     |



 

## <a name="related-topics"></a><span data-ttu-id="295f3-121">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="295f3-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="295f3-122">Регистры</span><span class="sxs-lookup"><span data-stu-id="295f3-122">Registers</span></span>](dx9-graphics-reference-asm-ps-registers.md)
</dt> </dl>

 

 




