---
title: Обновление кэша схемы
description: Вся информация, записанная на сервер Active Directory, проверяется по схеме.
ms.assetid: 948f8ec5-7207-4566-bd79-60cdd54231bf
ms.tgt_platform: multiple
keywords:
- Обновление кэша схемы Active Directory
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e2bf915d00b463b81a331ffe39b342f620a50417
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103773052"
---
# <a name="updating-the-schema-cache"></a><span data-ttu-id="a7736-104">Обновление кэша схемы</span><span class="sxs-lookup"><span data-stu-id="a7736-104">Updating the Schema Cache</span></span>

<span data-ttu-id="a7736-105">Вся информация, записанная на сервер Active Directory, проверяется по схеме.</span><span class="sxs-lookup"><span data-stu-id="a7736-105">All information that is written to an Active Directory server is validated against the schema.</span></span> <span data-ttu-id="a7736-106">Схема хранится в памяти на серверах каталогов (контроллерах домена) по соображениям производительности.</span><span class="sxs-lookup"><span data-stu-id="a7736-106">The schema is held in memory on directory servers (domain controllers) for performance reasons.</span></span> <span data-ttu-id="a7736-107">Версия в памяти обновляется автоматически после обновления версии на диске.</span><span class="sxs-lookup"><span data-stu-id="a7736-107">The in-memory version is updated automatically after the on-disk version has been updated.</span></span> <span data-ttu-id="a7736-108">Автоматическое обновление происходит через пять минут после применения последнего изменения; применение другого изменения схемы в течение 5 минут приведет к сбросу таймера в течение еще 5 минут.</span><span class="sxs-lookup"><span data-stu-id="a7736-108">The automatic update occurs five minutes after the last change was applied; applying another change to the schema in the 5-minute window resets the timer for another 5 minutes.</span></span> <span data-ttu-id="a7736-109">Такое поведение обеспечивает согласованность кэша, но может быть запутанной, поскольку изменения не отображаются в схеме до тех пор, пока кэш не будет обновлен, даже если они были применены на диске.</span><span class="sxs-lookup"><span data-stu-id="a7736-109">This behavior keeps the cache consistent, but can be confusing, because changes do not appear in the schema until the cache is updated, even though they were applied on disk.</span></span>

<span data-ttu-id="a7736-110">Чтобы обновить кэш Active Directory схемы после обновления схемы или вы хотите использовать обновление схемы сразу же для операций, не связанных с схемой, добавьте атрибут **счемаупдатенов** (он является рабочим атрибутом) в корневой DSE (пустое DN) со значением 1.</span><span class="sxs-lookup"><span data-stu-id="a7736-110">To update the Active Directory schema cache after a schema update, or if you want to use the schema update for non-schema operations immediately, add the **schemaUpdateNow** attribute (it is an operational attribute) to the root DSE (blank DN) with value 1.</span></span> <span data-ttu-id="a7736-111">Обновление кэша схемы начнется немедленно.</span><span class="sxs-lookup"><span data-stu-id="a7736-111">A schema cache update will start immediately.</span></span> <span data-ttu-id="a7736-112">Вызов блокируется.</span><span class="sxs-lookup"><span data-stu-id="a7736-112">The call is blocking.</span></span> <span data-ttu-id="a7736-113">Если вызов возвращается без ошибок, кэш обновляется и все обновления схемы готовы к использованию.</span><span class="sxs-lookup"><span data-stu-id="a7736-113">If the call returns with no error, the cache is updated and all schema updates are ready to be used.</span></span> <span data-ttu-id="a7736-114">Возврат ошибки означает, что обновление кэша завершилось неудачно.</span><span class="sxs-lookup"><span data-stu-id="a7736-114">An error return indicates the cache update was unsuccessful.</span></span> <span data-ttu-id="a7736-115">Приложения, которые должны использовать эту функцию, должны разрабатываться для блокировки записи, особенно в случае, если программа или сценарий выполняются в интерактивном режиме.</span><span class="sxs-lookup"><span data-stu-id="a7736-115">Applications that must use this feature should be designed to accommodate the blocking write, particularly in giving the user feedback, if the program or script executes interactively.</span></span>

<span data-ttu-id="a7736-116">Следующий пример кода является примером сценария LDIFDE, который показывает, как активировать перезагрузку кэша.</span><span class="sxs-lookup"><span data-stu-id="a7736-116">The following code example is a sample LDIFDE script that shows how to trigger a cache reload.</span></span>

``` syntax
dn:
changetype: modify
add: schemaUpdateNow
schemaUpdateNow: 1
-
```

<span data-ttu-id="a7736-117">Дополнительные сведения об обновлении кэша схемы программным способом см. в разделе [пример кода для обновления кэша схемы](example-code-for-updating-the-schema-cache.md).</span><span class="sxs-lookup"><span data-stu-id="a7736-117">For more information about how to update the schema cache programmatically, see [Example Code for Updating the Schema Cache](example-code-for-updating-the-schema-cache.md).</span></span>

 

 




