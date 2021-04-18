---
title: Регистр счетчиков циклов (Справочник по HLSL VS)
description: Единственный регистр в этом банке — регистрация текущего цикла (aL).
ms.assetid: b32fabf8-38d3-446c-bb80-c647d5aa028d
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: b12f57ba3fcfcb41aaff3827be39dbd1b6b07df1
ms.sourcegitcommit: cba7f424a292fd7f3a8518947b9466439b455419
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/23/2019
ms.locfileid: "104412262"
---
# <a name="loop-counter-register-hlsl-vs-reference"></a><span data-ttu-id="88de3-103">Регистр счетчиков циклов (Справочник по HLSL VS)</span><span class="sxs-lookup"><span data-stu-id="88de3-103">Loop Counter Register (HLSL VS reference)</span></span>

<span data-ttu-id="88de3-104">Единственный регистр в этом банке — регистрация текущего цикла (aL).</span><span class="sxs-lookup"><span data-stu-id="88de3-104">The only register in this bank is the current loop counter (aL) register.</span></span> <span data-ttu-id="88de3-105">Он автоматически увеличивается при каждом выполнении [цикла-VS](loop---vs.md).. блок [ендлуп-VS](endloop---vs.md) .</span><span class="sxs-lookup"><span data-stu-id="88de3-105">It automatically gets incremented in each execution of the [loop - vs](loop---vs.md)...[endloop - vs](endloop---vs.md) block.</span></span> <span data-ttu-id="88de3-106">Поэтому его можно использовать в блоке для относительной адресации, если это необходимо, и недопустимо использовать его за пределами цикла.</span><span class="sxs-lookup"><span data-stu-id="88de3-106">So it can be used in the block for relative addressing if needed and is invalid to use it outside the loop.</span></span>

## <a name="related-topics"></a><span data-ttu-id="88de3-107">См. также</span><span class="sxs-lookup"><span data-stu-id="88de3-107">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="88de3-108">Регистры шейдеров вершин</span><span class="sxs-lookup"><span data-stu-id="88de3-108">Vertex Shader Registers</span></span>](dx9-graphics-reference-asm-vs-registers.md)
</dt> </dl>

 

 




