---
title: Регистр глубины выходных данных
description: Регистр глубины выходных данных для шейдера пикселей (Одепс) является скалярной регистром только для записи с диапазоном \ 0.. 1 \, который возвращает новое значение глубины для теста глубины для буфера шаблона глубины.
ms.assetid: 47b9afd9-4520-480d-b4a2-3d9a5569defb
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 9be825d6117cf1cc14464973146dbe176d696d25
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104332603"
---
# <a name="output-depth-register"></a><span data-ttu-id="63bca-103">Регистр глубины выходных данных</span><span class="sxs-lookup"><span data-stu-id="63bca-103">Output Depth Register</span></span>

<span data-ttu-id="63bca-104">Регистр глубины выходных данных построителя текстуры (Одепс) является скалярной регистром только для записи с диапазоном \[ 0.. 1 \] , возвращающим новое значение глубины для теста глубины для буфера шаблона глубины.</span><span class="sxs-lookup"><span data-stu-id="63bca-104">The pixel shader output depth register (oDepth) is a write-only scalar register with the range \[0..1\] that returns a new depth value for a depth test against the depth-stencil buffer.</span></span>

<span data-ttu-id="63bca-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="63bca-105">Syntax</span></span>



| <span data-ttu-id="63bca-106">одепс</span><span class="sxs-lookup"><span data-stu-id="63bca-106">oDepth</span></span> |
|--------|



 

<span data-ttu-id="63bca-107">Где:</span><span class="sxs-lookup"><span data-stu-id="63bca-107">Where:</span></span>



| <span data-ttu-id="63bca-108">Имя</span><span class="sxs-lookup"><span data-stu-id="63bca-108">Name</span></span>   | <span data-ttu-id="63bca-109">Описание</span><span class="sxs-lookup"><span data-stu-id="63bca-109">Description</span></span>                                                       |
|--------|-------------------------------------------------------------------|
| <span data-ttu-id="63bca-110">одепс</span><span class="sxs-lookup"><span data-stu-id="63bca-110">oDepth</span></span> | <span data-ttu-id="63bca-111">Новое значение глубины для теста глубины в буфере шаблона глубины</span><span class="sxs-lookup"><span data-stu-id="63bca-111">New depth value for a depth test against the depth-stencil buffer</span></span> |



 

<span data-ttu-id="63bca-112">Важно помнить, что запись в Одепс приводит к утрате любых алгоритмов оптимизации буфера глубины, относящихся к оборудованию (т. е. иерархическим Z), которые ускоряют тестовую производительность.</span><span class="sxs-lookup"><span data-stu-id="63bca-112">It is important to be aware that writing to oDepth causes the loss of any hardware-specific depth buffer optimization algorithms (i.e. hierarchical Z) which accelerate depth test performance.</span></span>

<span data-ttu-id="63bca-113">При записи в Одепс требуется репликация источника свиззле (. x \| . y \| . z \| . w).</span><span class="sxs-lookup"><span data-stu-id="63bca-113">Replicate source swizzle (.x \| .y \| .z \| .w) is required when writing to oDepth.</span></span> <span data-ttu-id="63bca-114">Явные маски записи не допускаются.</span><span class="sxs-lookup"><span data-stu-id="63bca-114">Explicit write masks are not allowed.</span></span>

<span data-ttu-id="63bca-115">Запись в регистр Одепс заменяет значение глубины с интерполяцией (и игнорирует любые смещения глубины и слопескале рендерстатес).</span><span class="sxs-lookup"><span data-stu-id="63bca-115">Writing to the oDepth register replaces the interpolated depth value (and ignores any depth bias/slopescale renderstates).</span></span> <span data-ttu-id="63bca-116">Если буфер глубины не был создан или присоединен к устройству, запись в Одепс игнорируется.</span><span class="sxs-lookup"><span data-stu-id="63bca-116">If no depth buffer has been created or attached to the device, then write to oDepth is ignored.</span></span>

<span data-ttu-id="63bca-117">Если вы выполняете множественную выборку и пишите в Одепс, так как шейдер пикселей выполняется только один раз на пиксель, значение глубины реплицируется для всех охваченных вложенных примеров.</span><span class="sxs-lookup"><span data-stu-id="63bca-117">If you are multisampling and write to oDepth, since the pixel shader only runs once per pixel, your depth value is replicated for all covered sub-sample locations.</span></span> <span data-ttu-id="63bca-118">Тест глубины по-прежнему выполняется в образце, но у вас нет значения глубины для каждого образца, которое перейдет в сравнение из шейдера пикселей, например, если вы не написали Одепс.</span><span class="sxs-lookup"><span data-stu-id="63bca-118">The depth test still happens per-sample, but you don't have a per-sample depth value going into the comparison from the pixel shader like you would have if you didn't write oDepth.</span></span>

<span data-ttu-id="63bca-119">Если в приложении в качестве буфера глубины задано значение w-buffer, то при записи в Одепс необходимо учитывать это.</span><span class="sxs-lookup"><span data-stu-id="63bca-119">If an application has a w-buffer set as its depth buffer, then it needs to take that into account while writing to oDepth.</span></span> <span data-ttu-id="63bca-120">Возможно, необходимо отправить сведения о диапазоне в шейдер пикселей и вычислить w-Range, чтобы масштабировать значения w-Values, записанные в Одепс.</span><span class="sxs-lookup"><span data-stu-id="63bca-120">It potentially needs to send w-range information to the pixel shader and compute the w-range to scale the w-values written out to oDepth.</span></span>

### <a name="ps_2_0-and-ps_2_x-restrictions"></a><span data-ttu-id="63bca-121">\_ограничения PS 2 \_ и PS \_ 2 \_ x</span><span class="sxs-lookup"><span data-stu-id="63bca-121">ps\_2\_0 and ps\_2\_x Restrictions</span></span>

-   <span data-ttu-id="63bca-122">Одепс может быть написан только с помощью инструкции [MOV-PS](mov---ps.md) и может быть выполнен только один раз.</span><span class="sxs-lookup"><span data-stu-id="63bca-122">oDepth can only be written with the [mov - ps](mov---ps.md) instruction and can only be done once.</span></span>
-   <span data-ttu-id="63bca-123">Не допускается использование модификатора источника при записи в Одепс.</span><span class="sxs-lookup"><span data-stu-id="63bca-123">No source modifier is allowed when writing to oDepth.</span></span>
-   <span data-ttu-id="63bca-124">Не допускается использование модификатора инструкции при записи в Одепс.</span><span class="sxs-lookup"><span data-stu-id="63bca-124">No instruction modifier is allowed when writing to oDepth.</span></span>
-   <span data-ttu-id="63bca-125">Нет записи в Одепс из конструкции управления потоком или при использовании затенения.</span><span class="sxs-lookup"><span data-stu-id="63bca-125">No writing to oDepth from within a flow control construct, or when using predication.</span></span>

### <a name="ps_3_0-restrictions"></a><span data-ttu-id="63bca-126">\_ограничения PS 3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="63bca-126">ps\_3\_0 Restrictions</span></span>

-   <span data-ttu-id="63bca-127">Для PS \_ 3 \_ 0 выходные регистры OC # и oD \# могут записываться любое количество раз.</span><span class="sxs-lookup"><span data-stu-id="63bca-127">For ps\_3\_0, output registers oC# and oD\# can be written any number of times.</span></span> <span data-ttu-id="63bca-128">Выходные данные шейдера пикселей поступают из содержимого выходных регистров в конце выполнения шейдера.</span><span class="sxs-lookup"><span data-stu-id="63bca-128">The output of the pixel shader comes from the contents of the output registers at the end of shader execution.</span></span> <span data-ttu-id="63bca-129">Если запись в выходной регистр не происходит, возможно, из-за управления потоком или если шейдер только что не записал его, то соответствующий целевой объект прорисовки также не обновляется.</span><span class="sxs-lookup"><span data-stu-id="63bca-129">If a write to an output register does not happen, perhaps due to flow control or if the shader just did not write it, the corresponding render target is also not updated.</span></span> <span data-ttu-id="63bca-130">Если подмножество каналов в выходном регистре записано, то неопределенные значения будут записаны в оставшиеся каналы.</span><span class="sxs-lookup"><span data-stu-id="63bca-130">If a subset of the channels in an output register are written, then undefined values will be written to the remaining channels.</span></span>
-   <span data-ttu-id="63bca-131">Можно выполнить запись в Одепс в элементе управления потоком или затенения, если все возможные пути в конечном итоге записываются в регистр.</span><span class="sxs-lookup"><span data-stu-id="63bca-131">You can write to oDepth within flow control or predication as long as all possible paths eventually write into the register.</span></span>
-   <span data-ttu-id="63bca-132">Вы не можете выполнять вычисления градиента (или операции, которые неявно вызывают такие вычисления градиента, как [текслд-PS \_ 2 \_ 0 и up](texld---ps-2-0.md), [текслдб-PS](texldb---ps.md), [текслдп-PS](texldp---ps.md)) внутри операторов управления потоком, условия ветвления которых различаются для отдельных примитивов (IE: Динамическая Инструкция по управлению потоком).</span><span class="sxs-lookup"><span data-stu-id="63bca-132">You may not perform any gradient calculations (or operations that implicitly invoke gradient calculations such as [texld - ps\_2\_0 and up](texld---ps-2-0.md), [texldb - ps](texldb---ps.md), [texldp - ps](texldp---ps.md)) inside of flow control statements whose branching conditions vary on a per-primitive basis (ie: dynamic flow control instructions).</span></span> <span data-ttu-id="63bca-133">Инструкция затенения не считается динамической системой управления потоком.</span><span class="sxs-lookup"><span data-stu-id="63bca-133">Instruction predication is not considered dynamic flow control.</span></span>

## <a name="related-topics"></a><span data-ttu-id="63bca-134">См. также</span><span class="sxs-lookup"><span data-stu-id="63bca-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="63bca-135">Регистры</span><span class="sxs-lookup"><span data-stu-id="63bca-135">Registers</span></span>](dx9-graphics-reference-asm-ps-registers.md)
</dt> </dl>

 

 




