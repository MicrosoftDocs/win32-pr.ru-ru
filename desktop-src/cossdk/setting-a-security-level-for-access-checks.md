---
description: После включения проверки доступа для приложения COM+ необходимо выбрать уровень, на котором будут выполняться проверки доступа.
ms.assetid: 9c044add-7761-4378-b7eb-bf4e84e913b3
title: Настройка уровня безопасности для проверок доступа
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 646a49a4966bff7c593f12cb7481f4a4aad8859e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104142370"
---
# <a name="setting-a-security-level-for-access-checks"></a><span data-ttu-id="2754f-103">Настройка уровня безопасности для проверок доступа</span><span class="sxs-lookup"><span data-stu-id="2754f-103">Setting a Security Level for Access Checks</span></span>

<span data-ttu-id="2754f-104">После включения [проверки доступа](enabling-access-checks-for-an-application.md)для приложения COM+ необходимо выбрать уровень, на котором будут выполняться проверки доступа.</span><span class="sxs-lookup"><span data-stu-id="2754f-104">After you have enabled [access checks](enabling-access-checks-for-an-application.md), for your COM+ application, you must select the level at which you wish to have access checks performed.</span></span>

<span data-ttu-id="2754f-105">**Выбор уровня безопасности**</span><span class="sxs-lookup"><span data-stu-id="2754f-105">**To select a security level**</span></span>

1.  <span data-ttu-id="2754f-106">В дереве консоли средства администрирования "службы компонентов" щелкните правой кнопкой мыши приложение COM+, для которого требуется включить проверки доступа, и выберите пункт **Свойства**.</span><span class="sxs-lookup"><span data-stu-id="2754f-106">In the console tree of the Component Services administrative tool, right-click the COM+ application for which you want to enable access checks, and then click **Properties**.</span></span>

2.  <span data-ttu-id="2754f-107">В диалоговом окне Свойства приложения перейдите на вкладку **Безопасность** .</span><span class="sxs-lookup"><span data-stu-id="2754f-107">In the application properties dialog box, click the **Security** tab.</span></span>

3.  <span data-ttu-id="2754f-108">В разделе **уровень безопасности** выберите один из следующих параметров.</span><span class="sxs-lookup"><span data-stu-id="2754f-108">Under **Security level**, select one of the following:</span></span>

    -   <span data-ttu-id="2754f-109">**Выполнять проверки доступа только на уровне процесса**— этот параметр указывает, что пользователи в ролях, назначенных приложению, будут добавлены в дескриптор безопасности процесса.</span><span class="sxs-lookup"><span data-stu-id="2754f-109">**Perform access checks only at the process level**— This setting indicates that users in roles that are assigned to the application will be added to the process security descriptor.</span></span> <span data-ttu-id="2754f-110">Это имеет следующие последствия и последствия.</span><span class="sxs-lookup"><span data-stu-id="2754f-110">This has the following effects and implications:</span></span>

        <span data-ttu-id="2754f-111">Детальная проверка ролей отключена на уровнях компонентов, методов и интерфейсов.</span><span class="sxs-lookup"><span data-stu-id="2754f-111">Fine-grained role checking is turned off at the component, method, and interface levels.</span></span> <span data-ttu-id="2754f-112">Проверки безопасности выполняются только на уровне приложения.</span><span class="sxs-lookup"><span data-stu-id="2754f-112">Security checks are performed only at the application level.</span></span>

        <span data-ttu-id="2754f-113">Свойство безопасности не включается в контекст для всех объектов, выполняющихся в приложении.</span><span class="sxs-lookup"><span data-stu-id="2754f-113">The security property is not included on the context for any objects running within the application.</span></span> <span data-ttu-id="2754f-114">Это потенциально может повлиять на активацию объектов.</span><span class="sxs-lookup"><span data-stu-id="2754f-114">This can potentially affect how objects are activated.</span></span> <span data-ttu-id="2754f-115">См. раздел [свойство контекста безопасности](security-context-property.md).</span><span class="sxs-lookup"><span data-stu-id="2754f-115">See [Security Context Property](security-context-property.md).</span></span>

        <span data-ttu-id="2754f-116">Контекст вызова безопасности не будет доступен.</span><span class="sxs-lookup"><span data-stu-id="2754f-116">The security call context will not be made available.</span></span> <span data-ttu-id="2754f-117">Программная безопасность, основанная на сведениях о контексте вызова безопасности, не будет работать.</span><span class="sxs-lookup"><span data-stu-id="2754f-117">Programmatic security that relies on security call context information will not function.</span></span> <span data-ttu-id="2754f-118">См. раздел [сведения о контексте вызова безопасности](security-call-context-information.md).</span><span class="sxs-lookup"><span data-stu-id="2754f-118">See [Security Call Context Information](security-call-context-information.md).</span></span>

    -   <span data-ttu-id="2754f-119">**Выполнять проверки доступа на уровне процессов и компонентов**— этот параметр указывает на то, что будут выполнены проверки дескрипторов безопасности на уровне процесса и полные проверки безопасности на основе ролей.</span><span class="sxs-lookup"><span data-stu-id="2754f-119">**Perform access checks at the process and component level**—This setting indicates that process-level security descriptor checks and full role-based security checks will be performed.</span></span> <span data-ttu-id="2754f-120">Это имеет следующие последствия и последствия.</span><span class="sxs-lookup"><span data-stu-id="2754f-120">This has the following effects and implications:</span></span>

        <span data-ttu-id="2754f-121">Чтобы включить проверку ролей для конкретных компонентов, необходимо [включить проверки доступа на уровне компонента](enabling-access-checks-at-the-component-level.md).</span><span class="sxs-lookup"><span data-stu-id="2754f-121">To enable role checking for particular components, you must [enable access checks at the component level](enabling-access-checks-at-the-component-level.md).</span></span>

        <span data-ttu-id="2754f-122">Свойство безопасности включается в контекст для всех объектов, выполняющихся в приложении.</span><span class="sxs-lookup"><span data-stu-id="2754f-122">The security property is included on the context for any objects running within the application.</span></span> <span data-ttu-id="2754f-123">Это потенциально может повлиять на активацию объектов.</span><span class="sxs-lookup"><span data-stu-id="2754f-123">This can potentially affect how objects are activated.</span></span> <span data-ttu-id="2754f-124">См. раздел [свойство контекста безопасности](security-context-property.md).</span><span class="sxs-lookup"><span data-stu-id="2754f-124">See [Security Context Property](security-context-property.md).</span></span>

        <span data-ttu-id="2754f-125">Контекст вызова безопасности доступен.</span><span class="sxs-lookup"><span data-stu-id="2754f-125">The security call context is available.</span></span> <span data-ttu-id="2754f-126">Программная безопасность на основе ролей включена.</span><span class="sxs-lookup"><span data-stu-id="2754f-126">Programmatic role-based security is enabled.</span></span> <span data-ttu-id="2754f-127">См. раздел [сведения о контексте вызова безопасности](security-call-context-information.md).</span><span class="sxs-lookup"><span data-stu-id="2754f-127">See [Security Call Context Information](security-call-context-information.md).</span></span>

        > [!Note]  
        > <span data-ttu-id="2754f-128">Для приложений библиотеки COM+ необходимо выбрать проверку как на уровне процесса, так и на уровне компонентов, чтобы любая осмысленная проверка доступа работала.</span><span class="sxs-lookup"><span data-stu-id="2754f-128">For COM+ library applications, you must choose to check both at process and at component levels for any meaningful access checking to work.</span></span> <span data-ttu-id="2754f-129">Библиотечные приложения используют хост-процесс для обеспечения безопасности на уровне процесса.</span><span class="sxs-lookup"><span data-stu-id="2754f-129">Library applications rely on the host process for process-level security.</span></span> <span data-ttu-id="2754f-130">Вы можете определить, как приложение библиотеки взаимодействует с проверкой подлинности, выполняемой ведущим процессом, [настроив проверку подлинности](enabling-authentication-for-a-library-application.md).</span><span class="sxs-lookup"><span data-stu-id="2754f-130">You can determine how the library application interacts with authentication performed by the host process by [setting authentication](enabling-authentication-for-a-library-application.md).</span></span> <span data-ttu-id="2754f-131">Дополнительные сведения см. в разделе [Библиотека Application Security](library-application-security.md).</span><span class="sxs-lookup"><span data-stu-id="2754f-131">For more information, see [Library Application Security](library-application-security.md).</span></span>

         

4.  <span data-ttu-id="2754f-132">Нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="2754f-132">Click **OK**.</span></span>

<span data-ttu-id="2754f-133">При следующем запуске приложения безопасность будет автоматически проверяться на указанном уровне.</span><span class="sxs-lookup"><span data-stu-id="2754f-133">The next time the application is started, security will automatically be checked at the specified level.</span></span> <span data-ttu-id="2754f-134">Только пользователям, назначенным ролям, назначенным приложению, будет предоставлен доступ к приложению.</span><span class="sxs-lookup"><span data-stu-id="2754f-134">Only users assigned to roles assigned to the application will be given access to the application.</span></span>

## <a name="related-topics"></a><span data-ttu-id="2754f-135">См. также</span><span class="sxs-lookup"><span data-stu-id="2754f-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2754f-136">Назначение ролей компонентам, интерфейсам или методам</span><span class="sxs-lookup"><span data-stu-id="2754f-136">Assigning Roles to Components, Interfaces, or Methods</span></span>](assigning-roles-to-components--interfaces--or-methods.md)
</dt> <dt>

[<span data-ttu-id="2754f-137">Настройка безопасности Role-Based</span><span class="sxs-lookup"><span data-stu-id="2754f-137">Configuring Role-Based Security</span></span>](configuring-role-based-security.md)
</dt> <dt>

[<span data-ttu-id="2754f-138">Определение ролей для приложения</span><span class="sxs-lookup"><span data-stu-id="2754f-138">Defining Roles for an Application</span></span>](defining-roles-for-an-application.md)
</dt> <dt>

[<span data-ttu-id="2754f-139">Включение проверок доступа для приложения</span><span class="sxs-lookup"><span data-stu-id="2754f-139">Enabling Access Checks for an Application</span></span>](enabling-access-checks-for-an-application.md)
</dt> <dt>

[<span data-ttu-id="2754f-140">Включение проверок доступа на уровне компонентов</span><span class="sxs-lookup"><span data-stu-id="2754f-140">Enabling Access Checks at the Component Level</span></span>](enabling-access-checks-at-the-component-level.md)
</dt> </dl>

 

 



