---
description: По умолчанию в системе отключены все исключения FP.
ms.assetid: efbea036-de9c-4f92-865a-494161da375e
title: Исключения для плавающей запятой
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e6a4db92a13a0215bb372db12d30bb11a749a0fc
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105655619"
---
# <a name="floating-point-exceptions"></a><span data-ttu-id="0347d-103">Исключения для плавающей запятой</span><span class="sxs-lookup"><span data-stu-id="0347d-103">Floating-Point Exceptions</span></span>

<span data-ttu-id="0347d-104">По умолчанию в системе отключены все исключения FP.</span><span class="sxs-lookup"><span data-stu-id="0347d-104">By default, the system has all FP exceptions turned off.</span></span> <span data-ttu-id="0347d-105">Следовательно, вычисления выводятся в виде NAN или бесконечности, а не исключения.</span><span class="sxs-lookup"><span data-stu-id="0347d-105">Therefore, computations result in NAN or INFINITY, rather than an exception.</span></span> <span data-ttu-id="0347d-106">Прежде чем можно будет перехватывать исключения с плавающей запятой (FP) с помощью структурированной обработки исключений, необходимо вызвать функцию библиотеки времени выполнения [ \_ контролфп \_ s](/previous-versions/visualstudio/visual-studio-2010/c9676k6h(v=vs.100)) , чтобы включить все возможные исключения FP.</span><span class="sxs-lookup"><span data-stu-id="0347d-106">Before you can trap floating-point (FP) exceptions using structured exception handling, you must call the [\_controlfp\_s](/previous-versions/visualstudio/visual-studio-2010/c9676k6h(v=vs.100)) C run-time library function to turn on all possible FP exceptions.</span></span> <span data-ttu-id="0347d-107">Для перехвата только определенных исключений используйте только те флаги, которые соответствуют исключениям для перехвата.</span><span class="sxs-lookup"><span data-stu-id="0347d-107">To trap only particular exceptions, use only the flags that correspond to the exceptions to be trapped.</span></span> <span data-ttu-id="0347d-108">Обратите внимание, что любой обработчик ошибок FP должен вызывать [ \_ клеарфп](/cpp/c-runtime-library/reference/clear87-clearfp?view=vs-2019) в качестве первой инструкции FP.</span><span class="sxs-lookup"><span data-stu-id="0347d-108">Note that any handler for FP errors should call [\_clearfp](/cpp/c-runtime-library/reference/clear87-clearfp?view=vs-2019) as its first FP instruction.</span></span> <span data-ttu-id="0347d-109">Эта функция очищает исключения с плавающей запятой.</span><span class="sxs-lookup"><span data-stu-id="0347d-109">This function clears floating-point exceptions.</span></span>

 

 
