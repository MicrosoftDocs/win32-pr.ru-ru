---
description: Подпрограммы обратного вызова очереди по умолчанию можно указать для обработки уведомлений, отправляемых Сетупкоммитфилекуеуе, или вызывать с помощью пользовательской подпрограммы обратного вызова, которая основана на функциональных возможностях подпрограммы обратного вызова очереди по умолчанию.
ms.assetid: df8ae7b5-f3a2-4343-a603-440ab5c02b88
title: Использование подпрограммы обратного вызова очереди по умолчанию
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f51bceadf309257b9faf2b3ce3b8a12771572664
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105663089"
---
# <a name="using-the-default-queue-callback-routine"></a><span data-ttu-id="7dc06-103">Использование подпрограммы обратного вызова очереди по умолчанию</span><span class="sxs-lookup"><span data-stu-id="7dc06-103">Using the Default Queue Callback Routine</span></span>

<span data-ttu-id="7dc06-104">Подпрограммы обратного вызова очереди по умолчанию можно указать для обработки уведомлений, отправляемых [**сетупкоммитфилекуеуе**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea), или вызывать с помощью пользовательской подпрограммы обратного вызова, которая основана на функциональных возможностях подпрограммы обратного вызова очереди по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="7dc06-104">The default queue callback routine can be specified to handle notifications sent by [**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea), or it can be called by a custom callback routine that builds on the functionality of the default queue callback routine.</span></span>

<span data-ttu-id="7dc06-105">В следующих разделах описывается инициализация и завершение контекста, используемого подпрограммыми обратного вызова очереди по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="7dc06-105">The following sections explain how to initialize and terminate the context used by a default queue callback routine.</span></span> <span data-ttu-id="7dc06-106">В разделах также описывается использование подпрограммы обратного вызова очереди по умолчанию с [**сетупкоммитфилекуеуе**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea) или пользовательской подпрограммы обратного вызова.</span><span class="sxs-lookup"><span data-stu-id="7dc06-106">The sections also describe how to use the default queue callback routine with [**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea) or a custom callback routine.</span></span>

-   [<span data-ttu-id="7dc06-107">Инициализация и завершение контекста обратного вызова</span><span class="sxs-lookup"><span data-stu-id="7dc06-107">Initializing and Terminating the Callback Context</span></span>](initializing-and-terminating-the-callback-context.md)
-   [<span data-ttu-id="7dc06-108">Вызов подпрограммы обратного вызова очереди по умолчанию</span><span class="sxs-lookup"><span data-stu-id="7dc06-108">Calling the Default Queue Callback Routine</span></span>](calling-the-default-queue-callback-routine.md)

 

 



