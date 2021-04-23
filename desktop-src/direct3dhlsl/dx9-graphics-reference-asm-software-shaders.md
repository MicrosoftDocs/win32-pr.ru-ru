---
title: Шейдеры программного обеспечения
description: Программные шейдеры реализованы, чтобы обеспечить разработку шейдеров без базовой поддержки оборудования. Они поддерживают полный набор функций. Поскольку они реализованы в программном обеспечении, они не дают наилучшей производительности.
ms.assetid: 0153732d-a487-473b-ad77-32ab457979f5
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: df101edd0362321847fb9c0baf7feb3cc865e2da
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104068646"
---
# <a name="software-shaders"></a><span data-ttu-id="d87d1-105">Шейдеры программного обеспечения</span><span class="sxs-lookup"><span data-stu-id="d87d1-105">Software Shaders</span></span>

<span data-ttu-id="d87d1-106">Программные шейдеры реализованы, чтобы обеспечить разработку шейдеров без базовой поддержки оборудования.</span><span class="sxs-lookup"><span data-stu-id="d87d1-106">Software shaders are implemented to allow development of shaders without underlying hardware support.</span></span> <span data-ttu-id="d87d1-107">Они поддерживают полный набор функций.</span><span class="sxs-lookup"><span data-stu-id="d87d1-107">They support the full feature set.</span></span> <span data-ttu-id="d87d1-108">Поскольку они реализованы в программном обеспечении, они не дают наилучшей производительности.</span><span class="sxs-lookup"><span data-stu-id="d87d1-108">Because they are implemented in software, they will not produce the best performance.</span></span>



| <span data-ttu-id="d87d1-109">Version</span><span class="sxs-lookup"><span data-stu-id="d87d1-109">Version</span></span>   | <span data-ttu-id="d87d1-110">Набор возможностей</span><span class="sxs-lookup"><span data-stu-id="d87d1-110">Feature Set</span></span>                  | <span data-ttu-id="d87d1-111">Требования</span><span class="sxs-lookup"><span data-stu-id="d87d1-111">Requirements</span></span>                                                         |
|-----------|------------------------------|----------------------------------------------------------------------|
| <span data-ttu-id="d87d1-112">VS \_ 2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="d87d1-112">vs\_2\_sw</span></span> | <span data-ttu-id="d87d1-113">Все функции VS \_ 2 \_ x</span><span class="sxs-lookup"><span data-stu-id="d87d1-113">All the features of vs\_2\_x</span></span> | <span data-ttu-id="d87d1-114">Поддерживается только при обработке вершин программного обеспечения и на эталонном устройстве.</span><span class="sxs-lookup"><span data-stu-id="d87d1-114">Only supported by software vertex processing and a reference device.</span></span> |
| <span data-ttu-id="d87d1-115">VS \_ 3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="d87d1-115">vs\_3\_sw</span></span> | <span data-ttu-id="d87d1-116">Все функции VS \_ 3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="d87d1-116">All the features of vs\_3\_0</span></span> | <span data-ttu-id="d87d1-117">Поддерживается только при обработке вершин программного обеспечения и на эталонном устройстве.</span><span class="sxs-lookup"><span data-stu-id="d87d1-117">Only supported by software vertex processing and a reference device.</span></span> |
| <span data-ttu-id="d87d1-118">PS \_ 2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="d87d1-118">ps\_2\_sw</span></span> | <span data-ttu-id="d87d1-119">Все функции PS \_ 2 \_ x</span><span class="sxs-lookup"><span data-stu-id="d87d1-119">All the features of ps\_2\_x</span></span> | <span data-ttu-id="d87d1-120">Поддерживается только на эталонном устройстве.</span><span class="sxs-lookup"><span data-stu-id="d87d1-120">Only supported by a reference device.</span></span>                                |
| <span data-ttu-id="d87d1-121">PS \_ 3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="d87d1-121">ps\_3\_sw</span></span> | <span data-ttu-id="d87d1-122">Все функции PS \_ 3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="d87d1-122">All the features of ps\_3\_0</span></span> | <span data-ttu-id="d87d1-123">Поддерживается только на эталонном устройстве.</span><span class="sxs-lookup"><span data-stu-id="d87d1-123">Only supported by a reference device.</span></span>                                |



 

<span data-ttu-id="d87d1-124">Некоторые проверки для шейдеров программного обеспечения нестрогие.</span><span class="sxs-lookup"><span data-stu-id="d87d1-124">Some validations are relaxed for software shaders.</span></span> <span data-ttu-id="d87d1-125">Это полезно для целей отладки и создания прототипов.</span><span class="sxs-lookup"><span data-stu-id="d87d1-125">This is useful for debugging and prototyping purposes.</span></span> <span data-ttu-id="d87d1-126">Следующие проверки являются нестрогими: (все остальные проверки остаются неизменными).</span><span class="sxs-lookup"><span data-stu-id="d87d1-126">The following validations are relaxed: (all other validations remain the same)</span></span>



| <span data-ttu-id="d87d1-127">Тип проверки</span><span class="sxs-lookup"><span data-stu-id="d87d1-127">Validation type</span></span>                                 | <span data-ttu-id="d87d1-128">Ослабление</span><span class="sxs-lookup"><span data-stu-id="d87d1-128">Relaxation</span></span>                                                                                                                                                                                                          |
|-------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d87d1-129">Число команд:</span><span class="sxs-lookup"><span data-stu-id="d87d1-129">Instruction Counts:</span></span>                             | <span data-ttu-id="d87d1-130">Это не является более строгим для VS \_ 2 \_ SW, VS \_ 3 \_ SW и PS \_ 2 \_ SW, PS \_ 3 \_ SW.</span><span class="sxs-lookup"><span data-stu-id="d87d1-130">This is relaxed for vs\_2\_sw, vs\_3\_sw and ps\_2\_sw, ps\_3\_sw.</span></span> <span data-ttu-id="d87d1-131">Разрешены неограниченные инструкции.</span><span class="sxs-lookup"><span data-stu-id="d87d1-131">Unlimited instructions are allowed.</span></span>                                                                                                              |
| <span data-ttu-id="d87d1-132">Подсчет констант float:</span><span class="sxs-lookup"><span data-stu-id="d87d1-132">Float Constant Counts:</span></span>                          | <span data-ttu-id="d87d1-133">Это не является более строгим для VS \_ 2 \_ SW, VS \_ 3 \_ SW и PS \_ 2 \_ SW, PS \_ 3 \_ SW.</span><span class="sxs-lookup"><span data-stu-id="d87d1-133">This is relaxed for vs\_2\_sw, vs\_3\_sw and ps\_2\_sw, ps\_3\_sw.</span></span> <span data-ttu-id="d87d1-134">Допускается до 8192 констант.</span><span class="sxs-lookup"><span data-stu-id="d87d1-134">Up to 8192 constants are allowed.</span></span>                                                                                                                |
| <span data-ttu-id="d87d1-135">Число целочисленных констант:</span><span class="sxs-lookup"><span data-stu-id="d87d1-135">Integer Constant Counts:</span></span>                        | <span data-ttu-id="d87d1-136">Это не является более строгим для VS \_ 2 \_ SW, VS \_ 3 \_ SW и PS \_ 2 \_ SW, PS \_ 3 \_ SW.</span><span class="sxs-lookup"><span data-stu-id="d87d1-136">This is relaxed for vs\_2\_sw, vs\_3\_sw and ps\_2\_sw, ps\_3\_sw.</span></span> <span data-ttu-id="d87d1-137">Допускается до 2048 констант.</span><span class="sxs-lookup"><span data-stu-id="d87d1-137">Up to 2048 constants are allowed.</span></span>                                                                                                                |
| <span data-ttu-id="d87d1-138">Число логических констант:</span><span class="sxs-lookup"><span data-stu-id="d87d1-138">Boolean Constant Counts:</span></span>                        | <span data-ttu-id="d87d1-139">Это не является более строгим для VS \_ 2 \_ SW, VS \_ 3 \_ SW и PS \_ 2 \_ SW, PS \_ 3 \_ SW.</span><span class="sxs-lookup"><span data-stu-id="d87d1-139">This is relaxed for vs\_2\_sw, vs\_3\_sw and ps\_2\_sw, ps\_3\_sw.</span></span> <span data-ttu-id="d87d1-140">Допускается до 2048 констант.</span><span class="sxs-lookup"><span data-stu-id="d87d1-140">Up to 2048 constants are allowed.</span></span>                                                                                                                |
| <span data-ttu-id="d87d1-141">Глубина зависимого чтения:</span><span class="sxs-lookup"><span data-stu-id="d87d1-141">Dependent-read depth:</span></span>                           | <span data-ttu-id="d87d1-142">Это неявное для PS \_ 2 \_ SW.</span><span class="sxs-lookup"><span data-stu-id="d87d1-142">This is relaxed for ps\_2\_sw.</span></span> <span data-ttu-id="d87d1-143">Как и в VS \_ 3 \_ 0 и PS \_ 3 \_ 0, неограниченное число зависимых операций чтения разрешено.</span><span class="sxs-lookup"><span data-stu-id="d87d1-143">Like in vs\_3\_0 and ps\_3\_0, unlimited dependent reads are allowed.</span></span>                                                                                                                |
| <span data-ttu-id="d87d1-144">Число инструкций и меток управления потоком:</span><span class="sxs-lookup"><span data-stu-id="d87d1-144">Number of flow control instructions and labels:</span></span> | <span data-ttu-id="d87d1-145">Это не является более строгим для VS \_ 2 \_ SW.</span><span class="sxs-lookup"><span data-stu-id="d87d1-145">This is relaxed for vs\_2\_sw.</span></span> <span data-ttu-id="d87d1-146">Неограниченное количество инструкций по управлению потоком и до 2048 меток разрешены.</span><span class="sxs-lookup"><span data-stu-id="d87d1-146">Unlimited flow control instructions and upto 2048 labels are allowed.</span></span>                                                                                                                |
| <span data-ttu-id="d87d1-147">Число циклов/начало/шаг:</span><span class="sxs-lookup"><span data-stu-id="d87d1-147">Loop count/start/step:</span></span>                          | <span data-ttu-id="d87d1-148">Они нестроги для VS \_ 2 \_ SW, VS \_ 3 \_ SW, PS \_ 2 \_ SW и PS \_ 3 \_ SW.</span><span class="sxs-lookup"><span data-stu-id="d87d1-148">These are relaxed for vs\_2\_sw, vs\_3\_sw, ps\_2\_sw and ps\_3\_sw.</span></span> <span data-ttu-id="d87d1-149">Начало итерации и размер промежуточного шага для инструкций-представительов и циклов — 32-битное подписанное интержерс.</span><span class="sxs-lookup"><span data-stu-id="d87d1-149">Iteration start and interation step size for rep and loop instructions are 32-bit signed intergers.</span></span> <span data-ttu-id="d87d1-150">Число взаимосвязей может быть не более максимального числа \_ int/64.</span><span class="sxs-lookup"><span data-stu-id="d87d1-150">Interation count can be up to MAX\_INT/64.</span></span> |
| <span data-ttu-id="d87d1-151">Ограничения для чтения и порта:</span><span class="sxs-lookup"><span data-stu-id="d87d1-151">Read-port limits:</span></span>                               | <span data-ttu-id="d87d1-152">VS \_ 2 \_ SW, VS \_ 3 \_ SW, PS \_ 2 \_ SW и PS \_ 3 \_ SW не имеют ограничения на чтение портов.</span><span class="sxs-lookup"><span data-stu-id="d87d1-152">vs\_2\_sw, vs\_3\_sw, ps\_2\_sw and ps\_3\_sw have no read-port limit.</span></span>                                                                                                                                              |
| <span data-ttu-id="d87d1-153">Число интерполяций:</span><span class="sxs-lookup"><span data-stu-id="d87d1-153">Number of interpolators:</span></span>                        | <span data-ttu-id="d87d1-154">16 [регистров — VS \_ 3 \_ 0](dx9-graphics-reference-asm-vs-registers-vs-3-0.md) (o \# ) в VS \_ 3 \_ SW и 10 [PS \_ 3 \_ 0 регистров](dx9-graphics-reference-asm-ps-registers-ps-3-0.md) (v \# ) для PS \_ 3 \_ SW.</span><span class="sxs-lookup"><span data-stu-id="d87d1-154">There are 16 [Registers - vs\_3\_0](dx9-graphics-reference-asm-vs-registers-vs-3-0.md) (o\#) in vs\_3\_sw and 10 [ps\_3\_0 Registers](dx9-graphics-reference-asm-ps-registers-ps-3-0.md) (v\#) for ps\_3\_sw.</span></span>     |



 

## <a name="related-topics"></a><span data-ttu-id="d87d1-155">См. также</span><span class="sxs-lookup"><span data-stu-id="d87d1-155">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d87d1-156">Справочник по шейдеру ASM</span><span class="sxs-lookup"><span data-stu-id="d87d1-156">Asm Shader Reference</span></span>](dx9-graphics-reference-asm.md)
</dt> </dl>

 

 




