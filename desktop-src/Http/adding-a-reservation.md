---
title: Добавление резервирования
description: База данных маршрутизации содержит список резервирований.
ms.assetid: c36e731c-6a0b-42a8-bc92-106a8e017b0d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 358181cbe57a046f5af54f7adf17bdadb24c3ddc
ms.sourcegitcommit: 73417d55867c804274a55abe5ca71bcba7006119
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/20/2020
ms.locfileid: "104533587"
---
# <a name="adding-a-reservation"></a><span data-ttu-id="8433e-103">Добавление резервирования</span><span class="sxs-lookup"><span data-stu-id="8433e-103">Adding a Reservation</span></span>

<span data-ttu-id="8433e-104">База данных маршрутизации содержит список резервирований.</span><span class="sxs-lookup"><span data-stu-id="8433e-104">The routing database contains the reservation list.</span></span> <span data-ttu-id="8433e-105">Список резервирования состоит из пользователей, которым разрешен доступ к пространству имен, а также уровня доступа для каждого пользователя, указанного под зарезервированием.</span><span class="sxs-lookup"><span data-stu-id="8433e-105">The reservation list consists of the users that are allowed access to the namespace, as well as the level of access for each user listed under the reservation.</span></span> <span data-ttu-id="8433e-106">При добавлении или удалении резервирований выполняется поиск базы данных маршрутизации для определения прав доступа.</span><span class="sxs-lookup"><span data-stu-id="8433e-106">When reservations are added or deleted, the routing database is searched to determine access privileges.</span></span>

<span data-ttu-id="8433e-107">Помимо проверки идентификатора пользователя, API сервера HTTP также проверяет наличие конфликтов в существующих резервированиях перед установкой нового резервирования.</span><span class="sxs-lookup"><span data-stu-id="8433e-107">In addition to checking the users ID, the HTTP Server API also checks for conflicts in existing reservations before installing a new reservation.</span></span>

<span data-ttu-id="8433e-108">**Добавление нового резервирования**</span><span class="sxs-lookup"><span data-stu-id="8433e-108">**To add a new reservation**</span></span>

1.  <span data-ttu-id="8433e-109">Если номер порта в UrlPrefix содержит резервирования или регистрации для схемы, отличной от схемы в UrlPrefix, регистрация завершается ошибкой.</span><span class="sxs-lookup"><span data-stu-id="8433e-109">If the port number in the UrlPrefix has reservations or registrations for a scheme different from the scheme in the UrlPrefix, the registration fails.</span></span> <span data-ttu-id="8433e-110">Протоколы HTTP и HTTPS не поддерживаются в одном и том же порте.</span><span class="sxs-lookup"><span data-stu-id="8433e-110">HTTP and HTTPS cannot be supported on the same port.</span></span>
2.  <span data-ttu-id="8433e-111">Выберите соответствующий контейнер для регистрации (см. раздел [Маршрутизация входящих запросов](routing-incoming-requests.md) ) в зависимости от типа узла.</span><span class="sxs-lookup"><span data-stu-id="8433e-111">Locate the appropriate bucket for the registration (see the [Routing Incoming Requests](routing-incoming-requests.md) section), based on the host type.</span></span> <span data-ttu-id="8433e-112">Остальные шаги зависят от этого контейнера.</span><span class="sxs-lookup"><span data-stu-id="8433e-112">The remaining steps are relative to this bucket.</span></span>
3.  <span data-ttu-id="8433e-113">Выберите записи резервирования с компонентами схемы, узла и порта, которые соответствуют зарезервированному UrlPrefix.</span><span class="sxs-lookup"><span data-stu-id="8433e-113">Select reservation entries with scheme, host and port components that match the UrlPrefix being reserved.</span></span> <span data-ttu-id="8433e-114">В этом случае нахождение записи с наиболее длинным соответствующим значением *relativeUri* , не равным значению параметра relativeUri в резервировании (т. е. *родительского узла*).</span><span class="sxs-lookup"><span data-stu-id="8433e-114">From these, locate the entry with the longest matching *relativeUri* that is not equal to the relativeUri in the reservation (that is, the *parent node*).</span></span> <span data-ttu-id="8433e-115">Если запись существует, оцените права доступа на основе списка управления доступом, назначенного этой записи.</span><span class="sxs-lookup"><span data-stu-id="8433e-115">If the entry exists, then evaluate access rights based on the ACL assigned to that entry.</span></span>
4.  <span data-ttu-id="8433e-116">Если родительский узел не найден, это резервирование с пустым параметром relativeUri или *корневым резервированием*.</span><span class="sxs-lookup"><span data-stu-id="8433e-116">If a parent node was not found, this is a reservation with an empty relativeUri, or *root reservation*.</span></span> <span data-ttu-id="8433e-117">Предоставляйте права доступа только в том случае, если вызывающий объект зарегистрирован в учетных записях LocalSystem или Administrator.</span><span class="sxs-lookup"><span data-stu-id="8433e-117">Grant access rights only if the caller is registered under the LocalSystem or Administrator accounts.</span></span>
5.  <span data-ttu-id="8433e-118">Если предоставлены права доступа, проверьте наличие повторяющихся резервирований.</span><span class="sxs-lookup"><span data-stu-id="8433e-118">If access rights are granted, check for duplicate reservations.</span></span> <span data-ttu-id="8433e-119">Если запись резервирования существует с той же схемой, портом, узлом и значением relativeUri, \_ то \_ возвращается код ошибки.</span><span class="sxs-lookup"><span data-stu-id="8433e-119">If a reservation entry exists with the same scheme, port, host and relativeUri, an ERROR\_ALREADY\_EXISTS code is returned.</span></span>
    > [!Note]  
    > <span data-ttu-id="8433e-120">Обновление существующей записи должно выполняться в два этапа: удалить запись и добавить новую.</span><span class="sxs-lookup"><span data-stu-id="8433e-120">Updating an existing entry should be performed in two steps: delete the entry and add a new one.</span></span>

     

<span data-ttu-id="8433e-121">Если указанные выше шаги выполнены, в базу данных резервирования будет введена новая запись резервирования.</span><span class="sxs-lookup"><span data-stu-id="8433e-121">If the above steps succeed, a new reservation entry is entered into the reservation database.</span></span>

> [!Note]  
> <span data-ttu-id="8433e-122">Новая запись создается с указанным ACL и не наследует списки ACL от *родительской* записи.</span><span class="sxs-lookup"><span data-stu-id="8433e-122">The new entry is created with the specified ACL and does not inherit ACLs from the *parent* entry.</span></span>

 

<span data-ttu-id="8433e-123">В следующих примерах иллюстрируется процесс резервирования.</span><span class="sxs-lookup"><span data-stu-id="8433e-123">The following examples illustrate the reservation process.</span></span>

-   <span data-ttu-id="8433e-124">Резервирование 1. `https://+:80/vroot/subdir/` администратор пользователя а, а также пользователь в и в контейнере "+".</span><span class="sxs-lookup"><span data-stu-id="8433e-124">Reservation 1: `https://+:80/vroot/subdir/` by Admin for User A and User C succeeds and is entered into the "+" bucket.</span></span>
-   <span data-ttu-id="8433e-125">Резервирование 2. `https://adatum.com:80/vroot/` Администратор для пользователя б проходит успешную команду и входит в контейнер "явный узел".</span><span class="sxs-lookup"><span data-stu-id="8433e-125">Reservation 2: `https://adatum.com:80/vroot/` by Admin for User B succeeds and is entered into the "Explicit host" bucket.</span></span>
-   <span data-ttu-id="8433e-126">Резервирование 3. `https://adatum.com:80/vroot/subdir/otherdir/` пользователь б для пользователя C прошел из-за резервирования 2.</span><span class="sxs-lookup"><span data-stu-id="8433e-126">Reservation 3: `https://adatum.com:80/vroot/subdir/otherdir/` by User B for User C succeeds due to reservation 2.</span></span>
-   <span data-ttu-id="8433e-127">Резервирование 4. `https://+:80/vroot/subdir/otherdir/` пользователь A для пользователя E прошел из-за резервирования 1.</span><span class="sxs-lookup"><span data-stu-id="8433e-127">Reservation 4: `https://+:80/vroot/subdir/otherdir/` by User A for User E succeeds due to reservation 1.</span></span>
-   <span data-ttu-id="8433e-128">Резервирование 5. `https://adatum.com:80/vroot/subdir/otherdir/` пользователь A для пользователя E завершается ошибкой.</span><span class="sxs-lookup"><span data-stu-id="8433e-128">Reservation 5: `https://adatum.com:80/vroot/subdir/otherdir/` by User A for User E fails.</span></span> <span data-ttu-id="8433e-129">Отказано в доступе из-за резервирования 2.</span><span class="sxs-lookup"><span data-stu-id="8433e-129">Access denied due to reservation 2.</span></span>
-   <span data-ttu-id="8433e-130">Резервирование 6. `https://+:80/vroot/subdir/` администратору для пользователя A не удается.</span><span class="sxs-lookup"><span data-stu-id="8433e-130">Reservation 6: `https://+:80/vroot/subdir/` by Admin for User A fails.</span></span> <span data-ttu-id="8433e-131">Резервирование конфликтует с зарезервированным 1.</span><span class="sxs-lookup"><span data-stu-id="8433e-131">The reservation conflicts with reservation 1.</span></span>
-   <span data-ttu-id="8433e-132">Резервирование 7. `https://adatum.com:80/newroot/` пользователь a для пользователя a завершается ошибкой.</span><span class="sxs-lookup"><span data-stu-id="8433e-132">Reservation 7: `https://adatum.com:80/newroot/` by User A for User A fails.</span></span> <span data-ttu-id="8433e-133">Отказано в доступе из-за неявного корневого резервирования `https://adatum.com:80/` для LocalSystem или администратора.</span><span class="sxs-lookup"><span data-stu-id="8433e-133">Access denied due to implicit root reservation of `https://adatum.com:80/` for LocalSystem or Administrator.</span></span>

<span data-ttu-id="8433e-134">Резервирование может повлиять на набор URL-адресов в запросах, доставленных процессу, который ранее зарегистрировал UrlPrefix.</span><span class="sxs-lookup"><span data-stu-id="8433e-134">Reservations can affect the set of URLs in requests delivered to a process that has previously registered a UrlPrefix.</span></span> <span data-ttu-id="8433e-135">Давайте рассмотрим следующий пример.</span><span class="sxs-lookup"><span data-stu-id="8433e-135">For example, consider the following scenario.</span></span>

-   <span data-ttu-id="8433e-136">Регистрация: `https://adatum.com:80/vroot/` в приложении 1 для пользователя а.</span><span class="sxs-lookup"><span data-stu-id="8433e-136">Registration: `https://adatum.com:80/vroot/` by application 1 for User A.</span></span>
-   <span data-ttu-id="8433e-137">Запрос `https://adatum.com:80/vroot/subdir/file.htm` отправляется в приложение 1.</span><span class="sxs-lookup"><span data-stu-id="8433e-137">A request for `https://adatum.com:80/vroot/subdir/file.htm` is delivered to application 1.</span></span>
-   <span data-ttu-id="8433e-138">Резервирование: `https://+:80/vroot/subdir/` для пользователя б.</span><span class="sxs-lookup"><span data-stu-id="8433e-138">Reservation: `https://+:80/vroot/subdir/` for User B.</span></span>
-   <span data-ttu-id="8433e-139">Запрос для `https://adatum.com:80/vroot/subdir/file.htm` теперь отклонен.</span><span class="sxs-lookup"><span data-stu-id="8433e-139">A request for `https://adatum.com:80/vroot/subdir/file.htm` is now rejected.</span></span>
-   <span data-ttu-id="8433e-140">Регистрация: `https://adatum.com:80/vroot/subdir/` в приложении 2 для пользователя б.</span><span class="sxs-lookup"><span data-stu-id="8433e-140">Registration: `https://adatum.com:80/vroot/subdir/` by application 2 for User B.</span></span>
-   <span data-ttu-id="8433e-141">Запрос `https://adatum.com:80/vroot/subdir/file.htm` отправляется в приложение 2.</span><span class="sxs-lookup"><span data-stu-id="8433e-141">A request for `https://adatum.com:80/vroot/subdir/file.htm` is delivered to application 2.</span></span>

 

 




