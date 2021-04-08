---
title: Как служба формирует свои имена участников-служб
description: Служба может использовать две функции для составления своих имен субъектов-служб Дсжетспн — универсальная функция для составления имен субъектов-служб, а Дссерверрегистерспн — специализированная функция для составления и регистрации простых имен участников-служб для службы на основе узла.
ms.assetid: 8710409a-67b1-45e5-9cd7-5125443ab921
ms.tgt_platform: multiple
keywords:
- имя субъекта-службы AD, создание службы
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5611527cc3c240eebc195058ce39daab71aeef23
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103887664"
---
# <a name="how-a-service-composes-its-spns"></a><span data-ttu-id="bc081-104">Как служба формирует свои имена участников-служб</span><span class="sxs-lookup"><span data-stu-id="bc081-104">How a Service Composes its SPNs</span></span>

<span data-ttu-id="bc081-105">Служба может использовать две функции для создания своих имен участников-служб: [**дсжетспн**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsgetspna) — это функция общего назначения для составления имен субъектов-служб, а [**дссерверрегистерспн**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsserverregisterspna) — специализированная функция для составления и регистрации простых имен участников-служб для службы на основе узла.</span><span class="sxs-lookup"><span data-stu-id="bc081-105">A service can use two functions to compose its SPNs: [**DsGetSpn**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsgetspna) is a general-purpose function for composing SPNs and [**DsServerRegisterSpn**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsserverregisterspna) is a specialized function for composing and registering simple SPNs for a host-based service.</span></span>

<span data-ttu-id="bc081-106">Установщик службы обычно использует функцию [**дсжетспн**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsgetspna) для создания имен участников-служб, которые затем регистрируются в учетной записи входа службы с помощью функции [**дсвритеаккаунтспн**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dswriteaccountspna) .</span><span class="sxs-lookup"><span data-stu-id="bc081-106">A service installer typically uses the [**DsGetSpn**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsgetspna) function to compose SPNs, which it then registers on the service's logon account using the [**DsWriteAccountSpn**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dswriteaccountspna) function.</span></span> <span data-ttu-id="bc081-107">**Дсжетспн** может выполнять следующие функции.</span><span class="sxs-lookup"><span data-stu-id="bc081-107">The **DsGetSpn** can perform the following functions.</span></span>

-   <span data-ttu-id="bc081-108">Создайте простое имя субъекта-службы с <service class> / <host> форматом "" для службы на основе узла.</span><span class="sxs-lookup"><span data-stu-id="bc081-108">Create a simple SPN with the "<service class>/<host>" format for a host-based service.</span></span>
-   <span data-ttu-id="bc081-109">Создайте сложное имя субъекта-службы, которое включает &lt; компонент "имя службы &gt; ", используемый реплицируемыми службами или &lt; компонент "Port &gt; ", который различает несколько экземпляров службы на одном узле.</span><span class="sxs-lookup"><span data-stu-id="bc081-109">Create a complex SPN that includes the "&lt;service name&gt;" component used by replicable services or the "&lt;port&gt;" component that distinguishes multiple instances of a service on a single host.</span></span>
-   <span data-ttu-id="bc081-110">Создайте отдельное имя субъекта-службы с &lt; &gt; компонентом "узел", установленным в значение по умолчанию — либо название указанного узла, либо имя локального компьютера.</span><span class="sxs-lookup"><span data-stu-id="bc081-110">Create a single SPN with the "&lt;host&gt;" component set to either the name of a specified host or the name of the local computer by default.</span></span>
-   <span data-ttu-id="bc081-111">Создайте массив имен участников-служб для нескольких экземпляров службы, которые будут выполняться на нескольких узлах в пределах леса.</span><span class="sxs-lookup"><span data-stu-id="bc081-111">Create an array of SPNs for multiple service instances that will run on multiple hosts throughout the forest.</span></span> <span data-ttu-id="bc081-112">В каждом имени субъекта-службы указывается имя узла для экземпляра службы.</span><span class="sxs-lookup"><span data-stu-id="bc081-112">Each SPN specifies the name of the host for a service instance.</span></span>
-   <span data-ttu-id="bc081-113">Создайте массив имен участников-служб для нескольких экземпляров службы, которые будут выполняться на одном узле.</span><span class="sxs-lookup"><span data-stu-id="bc081-113">Create an array of SPNs for multiple service instances that will run on the same host.</span></span> <span data-ttu-id="bc081-114">В каждом имени субъекта-службы указывается имя узла и номер порта для экземпляра службы.</span><span class="sxs-lookup"><span data-stu-id="bc081-114">Each SPN specifies the name of the host and a port number for a service instance.</span></span>

<span data-ttu-id="bc081-115">Массив имен, возвращаемых функцией [**дсжетспн**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsgetspna) , должен быть освобожден путем вызова функции [**дсфриспнаррай**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsfreespnarraya) .</span><span class="sxs-lookup"><span data-stu-id="bc081-115">The array of names returned by [**DsGetSpn**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsgetspna) must be freed by calling the [**DsFreeSpnArray**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsfreespnarraya) function.</span></span>

<span data-ttu-id="bc081-116">Имейте в виду, что функции [**дсжетспн**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsgetspna), [**дсвритеаккаунтспн**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dswriteaccountspna)и [**дссерверрегистерспн**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsserverregisterspna) не проверяют уникальность имен участников-служб.</span><span class="sxs-lookup"><span data-stu-id="bc081-116">Be aware that the [**DsGetSpn**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsgetspna), [**DsWriteAccountSpn**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dswriteaccountspna), and [**DsServerRegisterSpn**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsserverregisterspna) functions do not verify that SPNs are unique.</span></span> <span data-ttu-id="bc081-117">Так как взаимная проверка подлинности завершается неудачей, если клиент предоставляет имя SPN, которое не является уникальным, проверьте уникальность перед регистрацией имени участника-службы</span><span class="sxs-lookup"><span data-stu-id="bc081-117">Because mutual authentication fails if a client presents an SPN that is not unique, verify uniqueness before registering an SPN.</span></span> <span data-ttu-id="bc081-118">**Для этого выполните поиск атрибутов глобального** каталога (GC), соответствующих имени субъекта-службы.</span><span class="sxs-lookup"><span data-stu-id="bc081-118">To do this, search the global catalog (GC) for **servicePrincipalName** attributes that match your SPN.</span></span> <span data-ttu-id="bc081-119">Дополнительные сведения о поиске в GC см. [в разделе Поиск в глобальном каталоге](searching-global-catalog-contents.md).</span><span class="sxs-lookup"><span data-stu-id="bc081-119">For more information about searching the GC, see [Searching the Global Catalog](searching-global-catalog-contents.md).</span></span>

 

 




