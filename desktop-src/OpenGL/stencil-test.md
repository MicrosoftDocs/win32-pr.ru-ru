---
title: Тест набора элементов
description: Условие теста трафарета отклоняет фрагмент на основе результата сравнения значения в буфере шаблона и ссылочного значения.
ms.assetid: 967be1e5-a9a2-45cc-aae7-c33cc257ade1
keywords:
- Конвейер обработки OpenGL, тест набора элементов
- Тестирование набора элементов OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e285c3dfb1591c5ed3d95969024d2350a7517a79
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103779466"
---
# <a name="stencil-test"></a><span data-ttu-id="69fb3-105">Тест набора элементов</span><span class="sxs-lookup"><span data-stu-id="69fb3-105">Stencil Test</span></span>

<span data-ttu-id="69fb3-106">Условие теста трафарета отклоняет фрагмент на основе результата сравнения значения в буфере шаблона и ссылочного значения.</span><span class="sxs-lookup"><span data-stu-id="69fb3-106">The stencil test conditionally discards a fragment based on the outcome of a comparison between the value in the stencil buffer and a reference value.</span></span> <span data-ttu-id="69fb3-107">Функция [**глстенЦилфунк**](glstencilfunc.md) указывает функцию сравнения и ссылочное значение.</span><span class="sxs-lookup"><span data-stu-id="69fb3-107">The [**glStencilFunc**](glstencilfunc.md) function specifies the comparison function and the reference value.</span></span> <span data-ttu-id="69fb3-108">Если фрагмент передается или не проходит проверку трафарета, значение в буфере шаблона изменяется в соответствии с инструкциями, указанными в [**глстенЦилоп**](glstencilop.md).</span><span class="sxs-lookup"><span data-stu-id="69fb3-108">Whether the fragment passes or fails the stencil test, the value in the stencil buffer is modified according to the instructions specified with [**glStencilOp**](glstencilop.md).</span></span>

 

 




