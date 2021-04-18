---
description: В этом разделе представлено несколько сценариев создания блоков, демонстрирующих критерии, которые обсуждаются в разделе Выбор места для обеспечения безопасности.
ms.assetid: e9820e53-8891-4bff-a333-00ad2dbb03a4
title: Основные сценарии защиты данных в многоуровневых приложениях
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7929bcfeba96b43b7ec91513b42ffb7f46266613
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105701241"
---
# <a name="basic-scenarios-for-securing-data-in-multi-tier-applications"></a><span data-ttu-id="935ff-103">Основные сценарии защиты данных в многоуровневых приложениях</span><span class="sxs-lookup"><span data-stu-id="935ff-103">Basic Scenarios for Securing Data in Multi-Tier Applications</span></span>

<span data-ttu-id="935ff-104">В этом разделе представлено несколько сценариев создания блоков, демонстрирующих критерии, которые обсуждаются в разделе [Выбор места для обеспечения безопасности](deciding-where-to-enforce-security.md).</span><span class="sxs-lookup"><span data-stu-id="935ff-104">This topic presents a few building-block scenarios, illustrating the criteria discussed in [Deciding Where to Enforce Security](deciding-where-to-enforce-security.md).</span></span>

## <a name="trusted-server-scenario"></a><span data-ttu-id="935ff-105">Сценарий доверенного сервера</span><span class="sxs-lookup"><span data-stu-id="935ff-105">Trusted Server Scenario</span></span>

-   <span data-ttu-id="935ff-106">База данных полностью доверяет приложению COM+ для проверки подлинности и авторизации конечных пользователей для доступа к данным в базе данных.</span><span class="sxs-lookup"><span data-stu-id="935ff-106">The database fully trusts the COM+ application to authenticate and authorize end users to access data in the database.</span></span>
-   <span data-ttu-id="935ff-107">Желательно, чтобы база данных была защищена от любого доступа, за исключением приложения.</span><span class="sxs-lookup"><span data-stu-id="935ff-107">Preferably, the database is secured against any access except through the application.</span></span>
-   <span data-ttu-id="935ff-108">Приложение COM+ использует безопасность на основе ролей для авторизации пользователей.</span><span class="sxs-lookup"><span data-stu-id="935ff-108">The COM+ application uses role-based security to authorize users.</span></span>
-   <span data-ttu-id="935ff-109">Подключения открываются под удостоверением приложения COM+ и являются полностью пулами.</span><span class="sxs-lookup"><span data-stu-id="935ff-109">Connections are opened under the COM+ application's identity and are fully poolable.</span></span>
-   <span data-ttu-id="935ff-110">Аудит и ведение журнала могут выполняться приложением COM+, или эти сведения могут быть переданы приложением в базу данных.</span><span class="sxs-lookup"><span data-stu-id="935ff-110">Auditing and logging can be done by the COM+ application, or this information can be passed into the database by the application.</span></span>

<span data-ttu-id="935ff-111">Этот сценарий лучше подходит для данных, доступ к которым можно получить с помощью прогнозируемых категорий пользователей, которые могут быть инкапсулированы в роли.</span><span class="sxs-lookup"><span data-stu-id="935ff-111">This scenario works best for data that can be accessed by predictable categories of users that can be encapsulated in roles.</span></span> <span data-ttu-id="935ff-112">Например, только "руководители", "говорят" и "бухгалтеры" имеют разрешение на доступ к учетным записям.</span><span class="sxs-lookup"><span data-stu-id="935ff-112">For example, only "Managers," "Tellers," and "Accountants" have permission to access accounts.</span></span> <span data-ttu-id="935ff-113">На среднем уровне применяется бизнес-логика того, что именно для каждого из них включено.</span><span class="sxs-lookup"><span data-stu-id="935ff-113">The business logic of what precisely each is enabled to do is enforced in the middle tier.</span></span>

## <a name="impersonation-scenario"></a><span data-ttu-id="935ff-114">Сценарий олицетворения</span><span class="sxs-lookup"><span data-stu-id="935ff-114">Impersonation Scenario</span></span>

-   <span data-ttu-id="935ff-115">База данных выполняет собственную проверку подлинности и авторизацию конечных пользователей, чтобы помочь ограничить доступ к данным в базе данных.</span><span class="sxs-lookup"><span data-stu-id="935ff-115">The database does its own authentication and authorization of end users to help limit access to data in the database.</span></span>
-   <span data-ttu-id="935ff-116">Приложение COM+ олицетворяет клиентов каждый раз, когда он обращается к базе данных.</span><span class="sxs-lookup"><span data-stu-id="935ff-116">The COM+ application impersonates clients whenever it is accessing the database.</span></span>
-   <span data-ttu-id="935ff-117">Соединения устанавливаются отдельно для каждого вызова и не могут быть использованы повторно.</span><span class="sxs-lookup"><span data-stu-id="935ff-117">Connections are made on a per-call basis and can't be reused.</span></span>

<span data-ttu-id="935ff-118">Этот сценарий лучше всего подходит для данных, которые тесно связаны с очень маленькими классами пользователей.</span><span class="sxs-lookup"><span data-stu-id="935ff-118">This scenario works best for data that is closely bound to very small classes of users.</span></span> <span data-ttu-id="935ff-119">Например, каждый сотрудник может получить доступ только к своему файлу персонала, и каждый руководитель может получить доступ только к тем файлам, которые используются в отчетах.</span><span class="sxs-lookup"><span data-stu-id="935ff-119">For example, each employee can access only his own personnel file, and each manager can access only the personnel files of her reports.</span></span>

## <a name="hybrid-scenario"></a><span data-ttu-id="935ff-120"> Гибридный сценарий</span><span class="sxs-lookup"><span data-stu-id="935ff-120">Hybrid Scenario</span></span>

<span data-ttu-id="935ff-121">Сочетание двух предыдущих сценариев, где олицетворение используется только при необходимости.</span><span class="sxs-lookup"><span data-stu-id="935ff-121">A combination of the preceding two scenarios, where impersonation is used only when it is needed.</span></span>

<span data-ttu-id="935ff-122">Этот сценарий лучше подходит в тех случаях, когда используются гибридные связи пользователей и данных.</span><span class="sxs-lookup"><span data-stu-id="935ff-122">This scenario works best in situations where you have hybrid user-data relationships.</span></span> <span data-ttu-id="935ff-123">Например, у вас есть "руководители", "говорят", "бухгалтеры" и тысячи отдельных веб-клиентов, которые могут обращаться только к своим учетным записям.</span><span class="sxs-lookup"><span data-stu-id="935ff-123">For example, you have "Managers," "Tellers," "Accountants," and thousands of individual Web clients who can access just their own accounts.</span></span> <span data-ttu-id="935ff-124">Вы можете разделить логику путей с помощью приложения, потенциально с отдельными компонентами, для обработки последнего класса пользователей, особенно в тех случаях, когда предполагается, что эти пользователи отличаются по производительности.</span><span class="sxs-lookup"><span data-stu-id="935ff-124">You can separate logic paths through the application, potentially with separate components, to handle the latter class of users, particularly where performance assumptions for those users are different.</span></span>

## <a name="trusted-scenario-using-microsoft-sql-server-roles"></a><span data-ttu-id="935ff-125">Доверенный сценарий с использованием ролей Microsoft SQL Server</span><span class="sxs-lookup"><span data-stu-id="935ff-125">Trusted Scenario Using Microsoft SQL Server Roles</span></span>

-   <span data-ttu-id="935ff-126">Microsoft SQL Server 7,0 и более поздних версий может авторизовать доступ к конкретным строкам с помощью ролей, но доверяет приложению COM+ для проверки подлинности и авторизации пользователей, а также для их преобразования в соответствующие роли в базе данных.</span><span class="sxs-lookup"><span data-stu-id="935ff-126">Microsoft SQL Server 7.0 and later can authorize access to specific rows using roles but trusts the COM+ application to authenticate and authorize users and to map them to the correct roles in the database.</span></span>
-   <span data-ttu-id="935ff-127">Приложение COM+ разрешает пользователям использовать безопасность на основе ролей, а роли приложения хорошо соответствуют ролям базы данных.</span><span class="sxs-lookup"><span data-stu-id="935ff-127">The COM+ application authorizes users using role-based security, and the application roles correspond well to database roles.</span></span>
-   <span data-ttu-id="935ff-128">Можно открывать подключения, относящиеся к определенной роли базы данных.</span><span class="sxs-lookup"><span data-stu-id="935ff-128">Connections can be opened that are specific to a particular database role.</span></span> <span data-ttu-id="935ff-129">Эти соединения можно использовать повторно, если они удерживаются объектами в пуле в приложениях COM+.</span><span class="sxs-lookup"><span data-stu-id="935ff-129">These connections can be reused if they are held by pooled objects in the COM+ applications.</span></span> <span data-ttu-id="935ff-130">Дополнительные сведения о том, как это сделать, см. в статье [группирование объектов COM+](com--object-pooling.md).</span><span class="sxs-lookup"><span data-stu-id="935ff-130">For details on how to do this, see [COM+ Object Pooling](com--object-pooling.md).</span></span>
-   <span data-ttu-id="935ff-131">Аудит и ведение журнала могут выполняться приложением COM+, или эти сведения могут быть переданы в базу данных приложением.</span><span class="sxs-lookup"><span data-stu-id="935ff-131">Auditing and logging can be done by the COM+ application, or this information can be passed in to the database by the application.</span></span>

<span data-ttu-id="935ff-132">Этот сценарий лучше всего подходит для тех же типов пользователей и данных, что и в первом сценарии с надежным сервером, поскольку приложение COM+ по-прежнему является доверенным для правильной работы авторизации.</span><span class="sxs-lookup"><span data-stu-id="935ff-132">This scenario works best for generally the same kinds of users and data as in the first trusted server scenario because the COM+ application is still being largely trusted to handle authorization correctly.</span></span> <span data-ttu-id="935ff-133">Однако он помогает защитить базу данных от несанкционированного доступа, одновременно разрешая доступ из нескольких источников за пределами приложения COM+, не тратя на масштабирование и производительность в сценарии олицетворения.</span><span class="sxs-lookup"><span data-stu-id="935ff-133">However, it does help protect the database against unauthorized access while allowing access potentially from multiple sources outside the COM+ application, without incurring the scaling and performance penalties present with the impersonation scenario.</span></span>

## <a name="related-topics"></a><span data-ttu-id="935ff-134">См. также</span><span class="sxs-lookup"><span data-stu-id="935ff-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="935ff-135">Выбор места для обеспечения безопасности</span><span class="sxs-lookup"><span data-stu-id="935ff-135">Deciding Where to Enforce Security</span></span>](deciding-where-to-enforce-security.md)
</dt> <dt>

[<span data-ttu-id="935ff-136">Многоуровневая защита приложений</span><span class="sxs-lookup"><span data-stu-id="935ff-136">Multi-Tier Application Security</span></span>](multi-tier-application-security.md)
</dt> </dl>

 

 



