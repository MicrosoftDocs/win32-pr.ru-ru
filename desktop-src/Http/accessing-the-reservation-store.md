---
title: Доступ к хранилищу резервирования
description: API сервера HTTP поддерживает список резервирования пространства имен для всех пользователей компьютера.
ms.assetid: 4b1291fc-cc62-4d4f-9150-18cbb1f6e5c0
keywords:
- Доступ к хранилищу данных резервирования по протоколу HTTP
- Протокол HTTP хранилища резервирования, доступ
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a138a0a2385e6338877e5e8623527a64a6eca796
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104410962"
---
# <a name="accessing-the-reservation-store"></a><span data-ttu-id="28e44-105">Доступ к хранилищу резервирования</span><span class="sxs-lookup"><span data-stu-id="28e44-105">Accessing the Reservation Store</span></span>

<span data-ttu-id="28e44-106">API сервера HTTP поддерживает список резервирования пространства имен для всех пользователей компьютера.</span><span class="sxs-lookup"><span data-stu-id="28e44-106">The HTTP Server API maintains the namespace reservation list for all users on the computer.</span></span> <span data-ttu-id="28e44-107">Запись резервирования состоит из [UrlPrefix](urlprefix-strings.md) и соответствующего списка ACL.</span><span class="sxs-lookup"><span data-stu-id="28e44-107">A reservation entry consists of a [UrlPrefix](urlprefix-strings.md) and corresponding ACL.</span></span> <span data-ttu-id="28e44-108">Каждый UrlPrefix в хранилище содержит список ACL, в котором перечислены все пользователи, которым разрешено регистрироваться для получения запросов к пространству имен.</span><span class="sxs-lookup"><span data-stu-id="28e44-108">Each UrlPrefix in the store has an ACL that lists all the users that are permitted to register to receive requests for the namespace.</span></span> <span data-ttu-id="28e44-109">Пользователи с привилегиями делегирования могут делегировать поддеревья пространства имен, принадлежащие другим пользователям, или удалять существующие резервирования с помощью API-интерфейсов конфигурации.</span><span class="sxs-lookup"><span data-stu-id="28e44-109">Users with delegation privileges can delegate subtrees of the namespace that they own to other users or delete existing reservations using the configuration APIs.</span></span>

<span data-ttu-id="28e44-110">Чтобы добавить резервирование в постоянное хранилище резервирования, приложение вызывает функцию [**хттпсетсервицеконфигуратион**](/windows/desktop/api/Http/nf-http-httpsetserviceconfiguration) с параметром ID конфигурации, имеющим значение **хттпсервицеконфигурлаклинфо** .</span><span class="sxs-lookup"><span data-stu-id="28e44-110">To add a reservation to the persistent reservation store, the application calls the [**HttpSetServiceConfiguration**](/windows/desktop/api/Http/nf-http-httpsetserviceconfiguration) function with the configuration ID parameter set to the **HttpServiceConfigUrlAclInfo** value.</span></span> <span data-ttu-id="28e44-111">API сервера HTTP проверяет владение пространством имен и ИДЕНТИФИКАТОРом пользователя перед добавлением резервирования в хранилище.</span><span class="sxs-lookup"><span data-stu-id="28e44-111">The HTTP Server API verifies the ownership of the namespace and the user ID before adding a reservation to the store.</span></span>

<span data-ttu-id="28e44-112">API сервера HTTP также предоставляет функции для запроса и удаления конфигураций службы для пространств имен URL-адресов.</span><span class="sxs-lookup"><span data-stu-id="28e44-112">The HTTP Server API also supplies functions to query and delete the Service configurations for URL namespaces.</span></span> <span data-ttu-id="28e44-113">Функция [**хттпкуерисервицеконфигуратион**](/windows/desktop/api/Http/nf-http-httpqueryserviceconfiguration) , вызываемая с параметром ID конфигурации, для которого заданы запросы значений **хттпсервицеконфигурлаклинфо** , а функция [**хттпделетесервицеконфигуратион**](/windows/desktop/api/Http/nf-http-httpdeleteserviceconfiguration) удаляет в хранилище пространства имен URL-адресов.</span><span class="sxs-lookup"><span data-stu-id="28e44-113">The [**HttpQueryServiceConfiguration**](/windows/desktop/api/Http/nf-http-httpqueryserviceconfiguration) function called with the configuration ID parameter set to the **HttpServiceConfigUrlAclInfo** value queries, and the [**HttpDeleteServiceConfiguration**](/windows/desktop/api/Http/nf-http-httpdeleteserviceconfiguration) function deletes on the URL namespace store.</span></span>

 

 




