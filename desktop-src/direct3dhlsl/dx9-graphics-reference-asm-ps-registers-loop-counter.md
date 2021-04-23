---
title: Регистр счетчиков циклов (Справочник по HLSL PS)
description: Единственный регистр в этом банке — регистрация текущего цикла (aL).
ms.assetid: 36999873-a251-4939-aac0-faa7f910bc33
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 47582552b7e32ede7cd83637cbc3900494dfd611
ms.sourcegitcommit: cba7f424a292fd7f3a8518947b9466439b455419
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/23/2019
ms.locfileid: "103785076"
---
# <a name="loop-counter-register-hlsl-ps-reference"></a><span data-ttu-id="3f255-103">Регистр счетчиков циклов (Справочник по HLSL PS)</span><span class="sxs-lookup"><span data-stu-id="3f255-103">Loop counter register (HLSL PS reference)</span></span>

<span data-ttu-id="3f255-104">Единственный регистр в этом банке — регистрация текущего цикла (aL).</span><span class="sxs-lookup"><span data-stu-id="3f255-104">The only register in this bank is the current loop counter (aL) register.</span></span> <span data-ttu-id="3f255-105">Он автоматически увеличивается при каждом выполнении блока [Loop-PS](loop---ps.md) / [ендлуп-PS](endloop---ps.md) .</span><span class="sxs-lookup"><span data-stu-id="3f255-105">It automatically gets incremented in each execution of the [loop - ps](loop---ps.md)/[endloop - ps](endloop---ps.md) block.</span></span> <span data-ttu-id="3f255-106">Поэтому его можно использовать в блоке для относительной адресации, если это необходимо, и недопустимо использовать его за пределами цикла.</span><span class="sxs-lookup"><span data-stu-id="3f255-106">So it can be used in the block for relative addressing if needed and is invalid to use it outside the loop.</span></span>



| <span data-ttu-id="3f255-107">Версии шейдеров пикселей</span><span class="sxs-lookup"><span data-stu-id="3f255-107">Pixel shader versions</span></span> | <span data-ttu-id="3f255-108">1\_1</span><span class="sxs-lookup"><span data-stu-id="3f255-108">1\_1</span></span> | <span data-ttu-id="3f255-109">1\_2</span><span class="sxs-lookup"><span data-stu-id="3f255-109">1\_2</span></span> | <span data-ttu-id="3f255-110">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="3f255-110">1\_3</span></span> | <span data-ttu-id="3f255-111">1\_4</span><span class="sxs-lookup"><span data-stu-id="3f255-111">1\_4</span></span> | <span data-ttu-id="3f255-112">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="3f255-112">2\_0</span></span> | <span data-ttu-id="3f255-113">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="3f255-113">2\_sw</span></span> | <span data-ttu-id="3f255-114">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="3f255-114">2\_x</span></span> | <span data-ttu-id="3f255-115">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="3f255-115">3\_0</span></span> | <span data-ttu-id="3f255-116">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="3f255-116">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|-------|------|------|-------|
| <span data-ttu-id="3f255-117">Регистр счетчика цикла</span><span class="sxs-lookup"><span data-stu-id="3f255-117">Loop Counter Register</span></span> |      |      |      |      |      |       |      | <span data-ttu-id="3f255-118">x</span><span class="sxs-lookup"><span data-stu-id="3f255-118">x</span></span>    | <span data-ttu-id="3f255-119">x</span><span class="sxs-lookup"><span data-stu-id="3f255-119">x</span></span>     |



 

## <a name="related-topics"></a><span data-ttu-id="3f255-120">См. также</span><span class="sxs-lookup"><span data-stu-id="3f255-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3f255-121">Регистры</span><span class="sxs-lookup"><span data-stu-id="3f255-121">Registers</span></span>](dx9-graphics-reference-asm-ps-registers.md)
</dt> </dl>

 

 




