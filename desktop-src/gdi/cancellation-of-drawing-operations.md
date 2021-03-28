---
description: Когда сложные приложения для рисования выполняют длительные графические операции, они потребляют ценные системные ресурсы.
ms.assetid: 3beef852-27fe-4ee2-b38b-3dc50e5d2fcf
title: Отмена операций рисования
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 98e3bdb7a57c7c427e7cd15ffddb62b1c492c25b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104997419"
---
# <a name="cancellation-of-drawing-operations"></a><span data-ttu-id="38f9c-103">Отмена операций рисования</span><span class="sxs-lookup"><span data-stu-id="38f9c-103">Cancellation of Drawing Operations</span></span>

<span data-ttu-id="38f9c-104">Когда сложные приложения для рисования выполняют длительные графические операции, они потребляют ценные системные ресурсы.</span><span class="sxs-lookup"><span data-stu-id="38f9c-104">When complex drawing applications perform lengthy graphics operations, they consume valuable system resources.</span></span> <span data-ttu-id="38f9c-105">Используя преимущества функций многозадачности системы, приложение может использовать потоки и функцию [**канцелдк**](/windows/desktop/api/Wingdi/nf-wingdi-canceldc) для управления этими операциями.</span><span class="sxs-lookup"><span data-stu-id="38f9c-105">By taking advantage of the system's multitasking features, an application can use threads and the [**CancelDC**](/windows/desktop/api/Wingdi/nf-wingdi-canceldc) function to manage these operations.</span></span> <span data-ttu-id="38f9c-106">Например, если операция графики, выполняемая потоком A, использует необходимые ресурсы, то поток B может вызвать функцию Канцелдк, чтобы остановить эту операцию.</span><span class="sxs-lookup"><span data-stu-id="38f9c-106">For example, if the graphics operation performed by thread A is consuming needed resources, thread B can call the CancelDC function to halt that operation.</span></span>

 

 



