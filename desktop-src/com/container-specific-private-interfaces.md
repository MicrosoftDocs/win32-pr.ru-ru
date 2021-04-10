---
title: Container-Specific закрытых интерфейсов
description: Container-Specific закрытых интерфейсов
ms.assetid: 429cf71c-9b9d-4d0b-b5de-91fbe1dde3cf
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 25c6569a79e9f1801c6fd82543bc40408903c780
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104332360"
---
# <a name="container-specific-private-interfaces"></a><span data-ttu-id="62fa3-103">Container-Specific закрытых интерфейсов</span><span class="sxs-lookup"><span data-stu-id="62fa3-103">Container-Specific Private Interfaces</span></span>

<span data-ttu-id="62fa3-104">Некоторые контейнеры предоставляют частные интерфейсы, относящиеся к контейнеру, для дополнительной функциональности или повышения производительности.</span><span class="sxs-lookup"><span data-stu-id="62fa3-104">Some containers provide container-specific private interfaces for additional functionality or improved performance.</span></span> <span data-ttu-id="62fa3-105">Элементы управления, зависящие от этих интерфейсов контейнера, должны, если это возможно, работать без этих интерфейсов, чтобы функции управления в разных контейнерах были доступны.</span><span class="sxs-lookup"><span data-stu-id="62fa3-105">Controls that rely on those container-specific interfaces should, if possible, work without those container-specific interfaces present so that the control functions in different containers.</span></span> <span data-ttu-id="62fa3-106">Например, Visual Basic реализует закрытые интерфейсы, обеспечивающие функциональность форматирования строк для элементов управления.</span><span class="sxs-lookup"><span data-stu-id="62fa3-106">For example, Visual Basic implements private interfaces that provide string formatting functionality to controls.</span></span> <span data-ttu-id="62fa3-107">Если элемент управления использует эти интерфейсы закрытого форматирования, он должен иметь возможность работать с поддержкой форматирования по умолчанию, если эти интерфейсы недоступны.</span><span class="sxs-lookup"><span data-stu-id="62fa3-107">If a control makes use of these private formatting interfaces, it should be able to run with default formatting support if these interfaces are not available.</span></span> <span data-ttu-id="62fa3-108">Если элемент управления может работать без закрытых интерфейсов, он должен выполнить соответствующее действие (например, предупредить пользователя о сниженной функциональности), но продолжить работу.</span><span class="sxs-lookup"><span data-stu-id="62fa3-108">If the control can function without the private interfaces, it should take appropriate action (such as warn the user of reduced functionality) but continue to work.</span></span> <span data-ttu-id="62fa3-109">Если это не параметр, Категория компонента должна быть зарегистрирована как обязательна, чтобы только контейнеры, поддерживающие эту функцию, могли размещать эти элементы управления.</span><span class="sxs-lookup"><span data-stu-id="62fa3-109">If this is not an option, a component category should be registered as required so that only containers supporting this functionality can host these controls.</span></span>

 

 




