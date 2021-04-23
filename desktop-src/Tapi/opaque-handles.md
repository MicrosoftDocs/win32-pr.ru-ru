---
description: Несколько типов, определенных ТСПИ, — это непрозрачные дескрипторы.
ms.assetid: e52ed691-0479-48da-9e06-c6a0d7a20e10
title: Непрозрачные дескрипторы
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2df2e0b0f608b9cefc8f0f4f538bffd452a8aab6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104542823"
---
# <a name="opaque-handles"></a><span data-ttu-id="b6b0a-103">Непрозрачные дескрипторы</span><span class="sxs-lookup"><span data-stu-id="b6b0a-103">Opaque Handles</span></span>

<span data-ttu-id="b6b0a-104">Несколько типов, определенных ТСПИ, — это непрозрачные дескрипторы.</span><span class="sxs-lookup"><span data-stu-id="b6b0a-104">A few types defined by TSPI are opaque handles.</span></span> <span data-ttu-id="b6b0a-105">Они используются в ТСПИ как открытые ссылки на закрытые структуры данных.</span><span class="sxs-lookup"><span data-stu-id="b6b0a-105">These are used in TSPI as public references to private data structures.</span></span> <span data-ttu-id="b6b0a-106">Это позволяет проверять типы параметров, предоставленных процедурам интерфейса, при этом обеспечивая меру защиты типа.</span><span class="sxs-lookup"><span data-stu-id="b6b0a-106">This allows type-checking of parameters supplied to the interface procedures while still giving a measure of type protection.</span></span> <span data-ttu-id="b6b0a-107">Только владелец закрытой структуры данных знает, как интерпретировать непрозрачный тип как ссылку на его представление структуры данных.</span><span class="sxs-lookup"><span data-stu-id="b6b0a-107">Only the owner of the private data structure knows how to interpret the opaque type as a reference to its data structure representation.</span></span> <span data-ttu-id="b6b0a-108">В качестве примера использования непрозрачных дескрипторов рассмотрим телефонное устройство.</span><span class="sxs-lookup"><span data-stu-id="b6b0a-108">As an example of how opaque handles are used, consider a phone device.</span></span> <span data-ttu-id="b6b0a-109">Как TAPI, так и поставщик услуг обычно поддерживают структуры данных, представляющие их соответствующие представления устройства.</span><span class="sxs-lookup"><span data-stu-id="b6b0a-109">Both TAPI and the service provider typically maintain data structures representing their respective views of the device.</span></span>

<span data-ttu-id="b6b0a-110">В типичных структурах данных для телефонов, поддерживаемых TAPI и поставщиком услуг, каждая из них содержит непрозрачный маркер для другой структуры данных.</span><span class="sxs-lookup"><span data-stu-id="b6b0a-110">In typical phone data structures maintained by TAPI and a service provider, each contains an opaque handle for the other data structure.</span></span> <span data-ttu-id="b6b0a-111">Они были изменены на раннем этапе инициализации.</span><span class="sxs-lookup"><span data-stu-id="b6b0a-111">These were exchanged at an early initialization step.</span></span> <span data-ttu-id="b6b0a-112">Когда TAPI вызывает функцию ТСПИ, он передает непрозрачный маркер для ссылки на устройство.</span><span class="sxs-lookup"><span data-stu-id="b6b0a-112">When TAPI calls a TSPI function, it passes the opaque handle to refer to the device.</span></span> <span data-ttu-id="b6b0a-113">Поставщик услуг знает, как разрешить это как ссылку (стрелку) на ее структуру данных.</span><span class="sxs-lookup"><span data-stu-id="b6b0a-113">The service provider knows how to resolve this as a reference (arrow) to its data structure.</span></span> <span data-ttu-id="b6b0a-114">Аналогичный процесс происходит, когда поставщик услуг вызывает функцию обратного вызова в TAPI.</span><span class="sxs-lookup"><span data-stu-id="b6b0a-114">A similar process occurs when the service provider calls a callback function in TAPI.</span></span>

 

 



