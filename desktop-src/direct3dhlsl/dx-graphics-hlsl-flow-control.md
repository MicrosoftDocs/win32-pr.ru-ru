---
title: Управление потоком
description: Большинство аппаратных средств предназначены для выполнения кода шейдера построчно, каждый раз выполняя каждую инструкцию HLSL.
ms.assetid: 94f22e39-8e71-424b-8ca1-bafc843f843f
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 70bb7706e520818c86286947acfba6cae0759b4d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104329256"
---
# <a name="flow-control"></a><span data-ttu-id="fbc0a-103">Управление потоком</span><span class="sxs-lookup"><span data-stu-id="fbc0a-103">Flow Control</span></span>

<span data-ttu-id="fbc0a-104">Большинство аппаратных средств предназначены для выполнения кода шейдера построчно, каждый раз выполняя каждую инструкцию HLSL.</span><span class="sxs-lookup"><span data-stu-id="fbc0a-104">Most hardware is designed to run shader code line by line, executing each HLSL statement once.</span></span> <span data-ttu-id="fbc0a-105">Оператор управления потоком во время выполнения определяет блок инструкций HLSL, которые нужно выполнить следующим.</span><span class="sxs-lookup"><span data-stu-id="fbc0a-105">A flow-control statement determines at run time which block of HLSL statements to execute next.</span></span> <span data-ttu-id="fbc0a-106">С помощью оператора управления потоком шейдер может циклически прокручивать набор инструкций или переходить (ветвь) к инструкции, отличной от той, которая находится на следующей строке.</span><span class="sxs-lookup"><span data-stu-id="fbc0a-106">Using a flow-control statement, a shader can loop through a set of statements, or jump (branch) to an instruction other than the one on the next line.</span></span> <span data-ttu-id="fbc0a-107">Некоторые операторы управления потоком поддерживают статический элемент управления, заданный во время компиляции. другие предлагают элемент управления с предикатами, который является решением для каждого компонента, сделанным во время выполнения, и по-прежнему поддерживает динамическое управление, которое является решением, выполняемым во время выполнения на основе содержимого переменной.</span><span class="sxs-lookup"><span data-stu-id="fbc0a-107">Some flow-control statements support static control that is specified at compile time; others offer predicated control which is a per-component decision made at runtime, and still others support dynamic control which is a decision made at run time based on the contents of a variable.</span></span>

<span data-ttu-id="fbc0a-108">HLSL поддерживает следующие инструкции управления потоком.</span><span class="sxs-lookup"><span data-stu-id="fbc0a-108">HLSL supports the following flow-control statements.</span></span>

-   [<span data-ttu-id="fbc0a-109">break</span><span class="sxs-lookup"><span data-stu-id="fbc0a-109">break</span></span>](dx-graphics-hlsl-break.md)
-   [<span data-ttu-id="fbc0a-110">continue</span><span class="sxs-lookup"><span data-stu-id="fbc0a-110">continue</span></span>](dx-graphics-hlsl-continue.md)
-   [<span data-ttu-id="fbc0a-111">исключить</span><span class="sxs-lookup"><span data-stu-id="fbc0a-111">discard</span></span>](dx-graphics-hlsl-discard.md)
-   [<span data-ttu-id="fbc0a-112">do</span><span class="sxs-lookup"><span data-stu-id="fbc0a-112">do</span></span>](dx-graphics-hlsl-do.md)
-   [<span data-ttu-id="fbc0a-113">for</span><span class="sxs-lookup"><span data-stu-id="fbc0a-113">for</span></span>](dx-graphics-hlsl-for.md)
-   [<span data-ttu-id="fbc0a-114">if</span><span class="sxs-lookup"><span data-stu-id="fbc0a-114">if</span></span>](dx-graphics-hlsl-if.md)
-   [<span data-ttu-id="fbc0a-115">switch</span><span class="sxs-lookup"><span data-stu-id="fbc0a-115">switch</span></span>](dx-graphics-hlsl-switch.md)
-   [<span data-ttu-id="fbc0a-116">while</span><span class="sxs-lookup"><span data-stu-id="fbc0a-116">while</span></span>](dx-graphics-hlsl-while.md)

## <a name="related-topics"></a><span data-ttu-id="fbc0a-117">См. также</span><span class="sxs-lookup"><span data-stu-id="fbc0a-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fbc0a-118">Синтаксис языка (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="fbc0a-118">Language Syntax (DirectX HLSL)</span></span>](dx-graphics-hlsl-language-syntax.md)
</dt> </dl>

 

 




