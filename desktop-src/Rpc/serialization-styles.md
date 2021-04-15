---
title: Стили сериализации
description: Существует три стиля, которые можно использовать для управления дескрипторами сериализации.
ms.assetid: 40b609b2-abad-4967-a5d1-948ac26fd65c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc825c24b591cdfea96a603835f0836eda68b3ba
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104411157"
---
# <a name="serialization-styles"></a><span data-ttu-id="e0ba4-103">Стили сериализации</span><span class="sxs-lookup"><span data-stu-id="e0ba4-103">Serialization Styles</span></span>

<span data-ttu-id="e0ba4-104">Существует три стиля, которые можно использовать для управления дескрипторами сериализации.</span><span class="sxs-lookup"><span data-stu-id="e0ba4-104">There are three styles you can use to manipulate serialization handles.</span></span> <span data-ttu-id="e0ba4-105">А именно:</span><span class="sxs-lookup"><span data-stu-id="e0ba4-105">These are:</span></span>

-   [<span data-ttu-id="e0ba4-106">Фиксированная сериализация буфера</span><span class="sxs-lookup"><span data-stu-id="e0ba4-106">Fixed Buffer Serialization</span></span>](fixed-buffer-serialization.md)
-   [<span data-ttu-id="e0ba4-107">Динамическая сериализация буфера</span><span class="sxs-lookup"><span data-stu-id="e0ba4-107">Dynamic Buffer Serialization</span></span>](dynamic-buffer-serialization.md)
-   [<span data-ttu-id="e0ba4-108">Добавочная сериализация</span><span class="sxs-lookup"><span data-stu-id="e0ba4-108">Incremental Serialization</span></span>](incremental-serialization.md)

<span data-ttu-id="e0ba4-109">Независимо от используемого стиля необходимо создать обработчик сериализации, сериализовать данные, а затем освободить этот обработчик.</span><span class="sxs-lookup"><span data-stu-id="e0ba4-109">Regardless of the style you use, you must create a serialization handle, serialize the data, and then free the handle.</span></span> <span data-ttu-id="e0ba4-110">Стиль задается, когда программа создает обработчик и определяет способ манипуляции с буфером.</span><span class="sxs-lookup"><span data-stu-id="e0ba4-110">The style is set when your program creates the handle and defines the way a buffer is manipulated.</span></span> <span data-ttu-id="e0ba4-111">Этот обработчик поддерживает соответствующий контекст, связанный с каждым из трех стилей сериализации.</span><span class="sxs-lookup"><span data-stu-id="e0ba4-111">The handle maintains the appropriate context associated with each of the three serialization styles.</span></span>

 

 




