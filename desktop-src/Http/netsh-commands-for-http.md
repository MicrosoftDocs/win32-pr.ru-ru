---
title: Команды Netsh для HTTP
description: Для запроса и настройки параметров HTTP.sys и параметров можно использовать контекстные команды Netsh для протокола HTTP.
ms.assetid: 695c309c-ab43-4c6a-b5f6-5bb9f715bf71
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 55f6e0fdd0813284e36d2fb9fb826929c67df63c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103778071"
---
# <a name="netsh-commands-for-http"></a><span data-ttu-id="a32a1-103">Команды Netsh для HTTP</span><span class="sxs-lookup"><span data-stu-id="a32a1-103">Netsh commands for HTTP</span></span>

<span data-ttu-id="a32a1-104">Для запроса и настройки параметров HTTP.sys и параметров можно использовать контекстные команды Netsh для протокола HTTP.</span><span class="sxs-lookup"><span data-stu-id="a32a1-104">You can use the Netsh commands for HTTP context to query and configure HTTP.sys settings and parameters.</span></span>

<span data-ttu-id="a32a1-105">Эти команды можно выполнить из командной строки в операционной системе Windows Vista или в командной строке для контекста **netsh http** .</span><span class="sxs-lookup"><span data-stu-id="a32a1-105">You can run these commands at the command prompt in the Windows Vista operating system or at the command prompt for the **netsh http** context.</span></span> <span data-ttu-id="a32a1-106">Чтобы эти команды работали в командной строке Windows Vista, необходимо ввести команду **netsh http** перед вводом команд и параметров, как показано в приведенном ниже синтаксисе.</span><span class="sxs-lookup"><span data-stu-id="a32a1-106">For these commands to work at the command prompt in Windows Vista, you must type **netsh http** before typing commands and parameters as they appear in the syntax below.</span></span> <span data-ttu-id="a32a1-107">Чтобы просмотреть справку для команды в командной строке, введите \* CommandName \***/?**, где *CommandName* — имя команды.</span><span class="sxs-lookup"><span data-stu-id="a32a1-107">To view help for a command at the command prompt, type \*CommandName\***/?**, where *CommandName* is the name of the command.</span></span>

<span data-ttu-id="a32a1-108">Чтобы просмотреть синтаксис команды, см. команды:</span><span class="sxs-lookup"><span data-stu-id="a32a1-108">To view the command syntax, see the commands:</span></span>

-   [<span data-ttu-id="a32a1-109">**add iplisten**</span><span class="sxs-lookup"><span data-stu-id="a32a1-109">**add iplisten**</span></span>](add-iplisten.md)
-   [<span data-ttu-id="a32a1-110">**add sslcert**</span><span class="sxs-lookup"><span data-stu-id="a32a1-110">**add sslcert**</span></span>](add-sslcert.md)
-   [<span data-ttu-id="a32a1-111">**add timeout**</span><span class="sxs-lookup"><span data-stu-id="a32a1-111">**add timeout**</span></span>](add-timeout.md)
-   [<span data-ttu-id="a32a1-112">**add urlacl**</span><span class="sxs-lookup"><span data-stu-id="a32a1-112">**add urlacl**</span></span>](add-urlacl.md)
-   [<span data-ttu-id="a32a1-113">**delete cache**</span><span class="sxs-lookup"><span data-stu-id="a32a1-113">**delete cache**</span></span>](delete-cache.md)
-   [<span data-ttu-id="a32a1-114">**delete iplisten**</span><span class="sxs-lookup"><span data-stu-id="a32a1-114">**delete iplisten**</span></span>](delete-iplisten.md)
-   [<span data-ttu-id="a32a1-115">**delete sslcert**</span><span class="sxs-lookup"><span data-stu-id="a32a1-115">**delete sslcert**</span></span>](delete-sslcert.md)
-   [<span data-ttu-id="a32a1-116">**delete timeout**</span><span class="sxs-lookup"><span data-stu-id="a32a1-116">**delete timeout**</span></span>](delete-timeout.md)
-   [<span data-ttu-id="a32a1-117">**delete urlacl**</span><span class="sxs-lookup"><span data-stu-id="a32a1-117">**delete urlacl**</span></span>](delete-urlacl.md)
-   [<span data-ttu-id="a32a1-118">**flush logbuffer**</span><span class="sxs-lookup"><span data-stu-id="a32a1-118">**flush logbuffer**</span></span>](flush-logbuffer.md)
-   [<span data-ttu-id="a32a1-119">**show cachestate**</span><span class="sxs-lookup"><span data-stu-id="a32a1-119">**show cachestate**</span></span>](show-cachestate.md)
-   [<span data-ttu-id="a32a1-120">**show iplisten**</span><span class="sxs-lookup"><span data-stu-id="a32a1-120">**show iplisten**</span></span>](show-iplisten.md)
-   [<span data-ttu-id="a32a1-121">**show servicestate**</span><span class="sxs-lookup"><span data-stu-id="a32a1-121">**show servicestate**</span></span>](show-servicestate.md)
-   [<span data-ttu-id="a32a1-122">**show sslcert**</span><span class="sxs-lookup"><span data-stu-id="a32a1-122">**show sslcert**</span></span>](show-sslcert.md)
-   [<span data-ttu-id="a32a1-123">**show timeout**</span><span class="sxs-lookup"><span data-stu-id="a32a1-123">**show timeout**</span></span>](show-timeout.md)
-   [<span data-ttu-id="a32a1-124">**show urlacl**</span><span class="sxs-lookup"><span data-stu-id="a32a1-124">**show urlacl**</span></span>](show-urlacl.md)

 

 




