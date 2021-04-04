---
description: Примеры спецификаций включают отправку сообщений Актиондата, когда пользовательское действие создает или удаляет учетную запись пользователя, и сообщает об ошибке, если учетная запись не может быть создана.
ms.assetid: ee90fe3d-51f4-433b-a5ce-950a03e1d8fb
title: Создание Актионтекст и таблиц ошибок
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1e20646a90ca76c159a88bdd8a6d026ff10845da
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103909071"
---
# <a name="authoring-the-actiontext-and-error-tables"></a><span data-ttu-id="1945f-103">Создание Актионтекст и таблиц ошибок</span><span class="sxs-lookup"><span data-stu-id="1945f-103">Authoring the ActionText and Error Tables</span></span>

<span data-ttu-id="1945f-104">Примеры спецификаций включают отправку сообщений Актиондата, когда пользовательское действие создает или удаляет учетную запись пользователя, и сообщает об ошибке, если учетная запись не может быть создана.</span><span class="sxs-lookup"><span data-stu-id="1945f-104">The sample specifications include sending ActionData messages when a custom action creates or removes a user account, and reporting an error if an account cannot be created.</span></span>

<span data-ttu-id="1945f-105">Введите следующие записи в таблицу Актионтекст, чтобы указать сведения, используемые сообщениями Актионтекст.</span><span class="sxs-lookup"><span data-stu-id="1945f-105">Enter the following entries into the ActionText table to provide information used by ActionText messages.</span></span>

[<span data-ttu-id="1945f-106">Таблица Актионтекст</span><span class="sxs-lookup"><span data-stu-id="1945f-106">ActionText Table</span></span>](actiontext-table.md)



| <span data-ttu-id="1945f-107">Действие</span><span class="sxs-lookup"><span data-stu-id="1945f-107">Action</span></span>            | <span data-ttu-id="1945f-108">Описание</span><span class="sxs-lookup"><span data-stu-id="1945f-108">Description</span></span>                                                       | <span data-ttu-id="1945f-109">Шаблон</span><span class="sxs-lookup"><span data-stu-id="1945f-109">Template</span></span>                          |
|-------------------|-------------------------------------------------------------------|-----------------------------------|
| <span data-ttu-id="1945f-110">процессаккаунтс</span><span class="sxs-lookup"><span data-stu-id="1945f-110">ProcessAccounts</span></span>   | <span data-ttu-id="1945f-111">Создание действий для создания учетных записей пользователей на локальном компьютере.</span><span class="sxs-lookup"><span data-stu-id="1945f-111">Generating actions to create user accounts on the local computer.</span></span> | <span data-ttu-id="1945f-112">Учетная запись: \[ 1 \] , атрибуты: \[ 2\]</span><span class="sxs-lookup"><span data-stu-id="1945f-112">Account: \[1\], Attributes: \[2\]</span></span> |
| <span data-ttu-id="1945f-113">креатеаккаунт</span><span class="sxs-lookup"><span data-stu-id="1945f-113">CreateAccount</span></span>     | <span data-ttu-id="1945f-114">Создание учетной записи пользователя на локальном компьютере.</span><span class="sxs-lookup"><span data-stu-id="1945f-114">Creating user account on the local computer.</span></span>                      | <span data-ttu-id="1945f-115">Учетная запись: \[ 1\]</span><span class="sxs-lookup"><span data-stu-id="1945f-115">Account: \[1\]</span></span>                    |
| <span data-ttu-id="1945f-116">RemoveAccount</span><span class="sxs-lookup"><span data-stu-id="1945f-116">RemoveAccount</span></span>     | <span data-ttu-id="1945f-117">Удаление учетной записи пользователя с локального компьютера.</span><span class="sxs-lookup"><span data-stu-id="1945f-117">Removing user account from the local computer.</span></span>                    | <span data-ttu-id="1945f-118">Учетная запись: \[ 1\]</span><span class="sxs-lookup"><span data-stu-id="1945f-118">Account: \[1\]</span></span>                    |
| <span data-ttu-id="1945f-119">роллбаккаккаунт</span><span class="sxs-lookup"><span data-stu-id="1945f-119">RollbackAccount</span></span>   | <span data-ttu-id="1945f-120">Откат создания учетных записей пользователей на локальном компьютере.</span><span class="sxs-lookup"><span data-stu-id="1945f-120">Rolling back the creation of user accounts on the local computer.</span></span> | <span data-ttu-id="1945f-121">Учетная запись: \[ 1\]</span><span class="sxs-lookup"><span data-stu-id="1945f-121">Account: \[1\]</span></span>                    |
| <span data-ttu-id="1945f-122">унинсталлаккаунтс</span><span class="sxs-lookup"><span data-stu-id="1945f-122">UninstallAccounts</span></span> | <span data-ttu-id="1945f-123">Создание действий для удаления учетных записей пользователей на локальном компьютере.</span><span class="sxs-lookup"><span data-stu-id="1945f-123">Generating actions to remove user accounts on the local computer.</span></span> | <span data-ttu-id="1945f-124">Учетная запись: \[ 1\]</span><span class="sxs-lookup"><span data-stu-id="1945f-124">Account: \[1\]</span></span>                    |



 

<span data-ttu-id="1945f-125">Введите следующие записи в таблицу ошибок, чтобы указать сведения, используемые при создании отчетов об ошибках.</span><span class="sxs-lookup"><span data-stu-id="1945f-125">Enter the following entries into the Error table to provide information used by error reporting.</span></span>

[<span data-ttu-id="1945f-126">Таблица ошибок</span><span class="sxs-lookup"><span data-stu-id="1945f-126">Error Table</span></span>](error-table.md)



| <span data-ttu-id="1945f-127">Error</span><span class="sxs-lookup"><span data-stu-id="1945f-127">Error</span></span> | <span data-ttu-id="1945f-128">Сообщение</span><span class="sxs-lookup"><span data-stu-id="1945f-128">Message</span></span>                                                                        |
|-------|--------------------------------------------------------------------------------|
| <span data-ttu-id="1945f-129">25001</span><span class="sxs-lookup"><span data-stu-id="1945f-129">25001</span></span> | <span data-ttu-id="1945f-130">Не удалось создать учетную запись пользователя " \[ 2 \] " на локальном компьютере.</span><span class="sxs-lookup"><span data-stu-id="1945f-130">Unable to create user account '\[2\]' on the local machine.</span></span> <span data-ttu-id="1945f-131">Код ошибки: \[ 3 \] .</span><span class="sxs-lookup"><span data-stu-id="1945f-131">Error Code: \[3\].</span></span> |
| <span data-ttu-id="1945f-132">25002</span><span class="sxs-lookup"><span data-stu-id="1945f-132">25002</span></span> | <span data-ttu-id="1945f-133">Учетная запись пользователя " \[ 2 \] " уже существует на локальном компьютере.</span><span class="sxs-lookup"><span data-stu-id="1945f-133">User account '\[2\]' already exists on the local machine.</span></span>                      |
| <span data-ttu-id="1945f-134">25003</span><span class="sxs-lookup"><span data-stu-id="1945f-134">25003</span></span> | <span data-ttu-id="1945f-135">Не удалось удалить учетную запись пользователя " \[ 2 \] " на локальном компьютере.</span><span class="sxs-lookup"><span data-stu-id="1945f-135">Unable to remove user account '\[2\]' on the local machine.</span></span> <span data-ttu-id="1945f-136">Код ошибки: \[ 3 \] .</span><span class="sxs-lookup"><span data-stu-id="1945f-136">Error Code: \[3\].</span></span> |
| <span data-ttu-id="1945f-137">25004</span><span class="sxs-lookup"><span data-stu-id="1945f-137">25004</span></span> | <span data-ttu-id="1945f-138">Учетная запись пользователя " \[ 2 \] " не существует на локальном компьютере.</span><span class="sxs-lookup"><span data-stu-id="1945f-138">User account '\[2\]' does not exist on the local machine.</span></span>                      |



 

<span data-ttu-id="1945f-139">Продолжайте [Создание таблицы инсталлексекутесекуенце](authoring-the-installexecutesequence-table.md).</span><span class="sxs-lookup"><span data-stu-id="1945f-139">Continue to [Authoring the InstallExecuteSequence Table](authoring-the-installexecutesequence-table.md).</span></span>

 

 



