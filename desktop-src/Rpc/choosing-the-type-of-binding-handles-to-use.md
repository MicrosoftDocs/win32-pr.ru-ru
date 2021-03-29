---
title: Выбор типа используемых дескрипторов привязки
description: Выбор типа используемых дескрипторов привязки
ms.assetid: b0c2c71d-c6c9-4a58-83f9-10ac9b6b214b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2dd07716b3618766b3ea8aa07fb766f154285207
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104067688"
---
# <a name="choosing-the-type-of-binding-handles-to-use"></a><span data-ttu-id="8595a-103">Выбор типа используемых дескрипторов привязки</span><span class="sxs-lookup"><span data-stu-id="8595a-103">Choosing the Type of Binding Handles to Use</span></span>

<span data-ttu-id="8595a-104">**Рекомендации:** Если известно, какой сервер будет использоваться приложением, используйте явные дескрипторы.</span><span class="sxs-lookup"><span data-stu-id="8595a-104">**Best practice:** If you know which server the application will use, use explicit handles.</span></span> <span data-ttu-id="8595a-105">В противном случае всегда используйте каждую конструкцию явных дескрипторов или используйте универсальные дескрипторы с подпрограммыми **\_ BIND** и **\_ Unbind** .</span><span class="sxs-lookup"><span data-stu-id="8595a-105">If you don't, use explicit handles construct every time, or use generic handles with **\_bind** and **\_unbind** routines.</span></span>

<span data-ttu-id="8595a-106">Не используйте неявные дескрипторы или автоматические дескрипторы.</span><span class="sxs-lookup"><span data-stu-id="8595a-106">Do not use implicit handles or auto handles.</span></span> <span data-ttu-id="8595a-107">Неявные дескрипторы не являются потокобезопасными, и даже несмотря на то, что безопасность потоков может показаться ненужной, она может быть понижена.</span><span class="sxs-lookup"><span data-stu-id="8595a-107">Implicit handles are not thread safe, and even though thread safety may seem unnecessary, it could become necessary later.</span></span> <span data-ttu-id="8595a-108">Автоматические дескрипторы имеют большие издержки и нуждаются в правильной работе программы установки.</span><span class="sxs-lookup"><span data-stu-id="8595a-108">Auto handles have large overhead and require a lot of setup to work properly.</span></span> <span data-ttu-id="8595a-109">Их возможности поиска заменены Active Directoryными службами.</span><span class="sxs-lookup"><span data-stu-id="8595a-109">Their search capabilities have been superseded by Active Directory services.</span></span>

<span data-ttu-id="8595a-110">Явные дескрипторы очень эффективны, и многие привлекательные возможности доступны только для явных дескрипторов.</span><span class="sxs-lookup"><span data-stu-id="8595a-110">Explicit handles are highly efficient, and many attractive capabilities are available only for explicit handles.</span></span> <span data-ttu-id="8595a-111">Например, если несколько вызовов RPC будут выполняться на одном и том же сервере, можно создать один и тот же обработчик привязки и выполнить все вызовы.</span><span class="sxs-lookup"><span data-stu-id="8595a-111">For example, if several RPC calls will be going to the same server, you can construct the binding handle once and make all calls with it.</span></span> <span data-ttu-id="8595a-112">Этот подход гораздо более эффективен, чем любой другой метод.</span><span class="sxs-lookup"><span data-stu-id="8595a-112">This approach is much more efficient than any other method.</span></span> <span data-ttu-id="8595a-113">Если сервер, на который будет проходить вызов, неизвестен, создайте явный дескриптор привязки для каждого вызова или используйте универсальные дескрипторы привязки.</span><span class="sxs-lookup"><span data-stu-id="8595a-113">If the server to which the call will go is unknown, construct an explicit binding handle for every call, or use generic binding handles.</span></span>

<span data-ttu-id="8595a-114">В Microsoft™ Windows XP время выполнения RPC довольно эффективно при повторном использовании и кэшировании вызовов, поэтому если вызов *n*+ 1-го первого вызова завершается на том же сервере, что и *n*-й вызов, RPC повторно использует ресурсы, выделенные для выполнения *n*– го вызова, обойти необходимость кэширования дескрипторов привязки для повышения производительности.</span><span class="sxs-lookup"><span data-stu-id="8595a-114">In Microsoft™ Windows XP, the RPC run time is quite efficient in re-using and caching calls, so if the *n*+1st call ends up on the same server as the *n* th call, RPC re-uses the resources allocated for the *n* th call, circumventing the need to cache binding handles to improve performance.</span></span>

 

 




