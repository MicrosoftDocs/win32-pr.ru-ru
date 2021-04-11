---
description: Если приложение COM+ использует безопасность на основе ролей, необходимо выполнить несколько задач.
ms.assetid: f53b9945-cd34-4afc-a03a-dd72b0af160d
title: Настройка безопасности Role-Based
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9eafa71430dfa13f497b0e4f7f7cea45229a422e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104342142"
---
# <a name="configuring-role-based-security"></a><span data-ttu-id="baff5-103">Настройка безопасности Role-Based</span><span class="sxs-lookup"><span data-stu-id="baff5-103">Configuring Role-Based Security</span></span>

<span data-ttu-id="baff5-104">Если приложение COM+ использует безопасность на основе ролей, необходимо выполнить несколько задач.</span><span class="sxs-lookup"><span data-stu-id="baff5-104">If your COM+ application uses role-based security, there are several tasks that need to be completed.</span></span> <span data-ttu-id="baff5-105">При проектировании компонентов в приложении необходимо определить роли, необходимые для защиты доступа к этим компонентам.</span><span class="sxs-lookup"><span data-stu-id="baff5-105">When designing the components in your application, you define the roles that are necessary to help protect access to those components.</span></span> <span data-ttu-id="baff5-106">Вы также решаете, какие роли следует назначить компонентам, интерфейсам и методам приложения.</span><span class="sxs-lookup"><span data-stu-id="baff5-106">You also decide which roles to assign to the application's components, interfaces, and methods.</span></span> <span data-ttu-id="baff5-107">Во время интеграции приложений с помощью средства администрирования служб компонентов можно добавить определенные роли в приложение и назначить каждую роль соответствующим компонентам, интерфейсам и методам.</span><span class="sxs-lookup"><span data-stu-id="baff5-107">During application integration, you use the Component Services administrative tool to add the defined roles to the application and assign each role to the appropriate components, interfaces, and methods.</span></span>

<span data-ttu-id="baff5-108">При настройке безопасности на основе ролей необходимо выполнить следующие действия.</span><span class="sxs-lookup"><span data-stu-id="baff5-108">In configuring role-based security, you perform the following steps:</span></span>

1.  <span data-ttu-id="baff5-109">Включите проверки доступа на уровне приложения.</span><span class="sxs-lookup"><span data-stu-id="baff5-109">Enable access checks at the application level.</span></span> <span data-ttu-id="baff5-110">Включение проверки безопасности для приложения.</span><span class="sxs-lookup"><span data-stu-id="baff5-110">To turn on security checking for an application.</span></span> <span data-ttu-id="baff5-111">Дополнительные сведения о том, как выполнить этот шаг, см. в разделе [Включение проверок доступа для приложения](enabling-access-checks-for-an-application.md) .</span><span class="sxs-lookup"><span data-stu-id="baff5-111">See [Enabling Access Checks for an Application](enabling-access-checks-for-an-application.md) for details on how to perform this step.</span></span>
2.  <span data-ttu-id="baff5-112">Задайте уровень безопасности для проверок доступа.</span><span class="sxs-lookup"><span data-stu-id="baff5-112">Set security level for access checks.</span></span> <span data-ttu-id="baff5-113">Для настройки безопасности в процессе или на уровне процесса и компонента.</span><span class="sxs-lookup"><span data-stu-id="baff5-113">To set security either at process or at process and component level.</span></span> <span data-ttu-id="baff5-114">Дополнительные сведения о том, как выполнить этот шаг, см. в разделе [Настройка уровня безопасности для проверок доступа](setting-a-security-level-for-access-checks.md) .</span><span class="sxs-lookup"><span data-stu-id="baff5-114">See [Setting a Security Level for Access Checks](setting-a-security-level-for-access-checks.md) for details on how to perform this step.</span></span>
3.  <span data-ttu-id="baff5-115">Включите проверки доступа на уровне компонентов.</span><span class="sxs-lookup"><span data-stu-id="baff5-115">Enable access checks at the component level.</span></span> <span data-ttu-id="baff5-116">Для включения проверки безопасности на уровнях компонентов, интерфейсов и методов.</span><span class="sxs-lookup"><span data-stu-id="baff5-116">To turn on security checking at the component, interface, and method levels.</span></span> <span data-ttu-id="baff5-117">Дополнительные сведения о том, как выполнить этот шаг, см. в разделе [Включение проверок доступа на уровне компонентов](enabling-access-checks-at-the-component-level.md) .</span><span class="sxs-lookup"><span data-stu-id="baff5-117">See [Enabling Access Checks at the Component Level](enabling-access-checks-at-the-component-level.md) for details on how to perform this step.</span></span>
4.  <span data-ttu-id="baff5-118">Определите роли для приложения.</span><span class="sxs-lookup"><span data-stu-id="baff5-118">Define roles for an application.</span></span> <span data-ttu-id="baff5-119">Создание ролей для приложения.</span><span class="sxs-lookup"><span data-stu-id="baff5-119">To create roles for an application.</span></span> <span data-ttu-id="baff5-120">Подробные сведения о том, как выполнить этот шаг, см. в разделе [Определение ролей для приложения](defining-roles-for-an-application.md) .</span><span class="sxs-lookup"><span data-stu-id="baff5-120">See [Defining Roles for an Application](defining-roles-for-an-application.md) for details on how to perform this step.</span></span>
5.  <span data-ttu-id="baff5-121">Назначение ролей компонентам, интерфейсам или методам.</span><span class="sxs-lookup"><span data-stu-id="baff5-121">Assign roles to components, interfaces, or methods.</span></span> <span data-ttu-id="baff5-122">Назначение ролей конкретным ресурсам в приложении.</span><span class="sxs-lookup"><span data-stu-id="baff5-122">To assign roles to specific resources within an application.</span></span> <span data-ttu-id="baff5-123">Дополнительные сведения о том, как выполнить этот шаг, см. в разделе [назначение ролей компонентам, интерфейсам или методам](assigning-roles-to-components--interfaces--or-methods.md) .</span><span class="sxs-lookup"><span data-stu-id="baff5-123">See [Assigning Roles to Components, Interfaces, or Methods](assigning-roles-to-components--interfaces--or-methods.md) for details on how to perform this step.</span></span>

## <a name="related-topics"></a><span data-ttu-id="baff5-124">См. также</span><span class="sxs-lookup"><span data-stu-id="baff5-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="baff5-125">Настройка политики ограниченного использования программ</span><span class="sxs-lookup"><span data-stu-id="baff5-125">Configuring the Software Restriction Policy</span></span>](configuring-the-software-restriction-policy.md)
</dt> <dt>

[<span data-ttu-id="baff5-126">Установка уровня олицетворения</span><span class="sxs-lookup"><span data-stu-id="baff5-126">Setting an Impersonation Level</span></span>](setting-an-impersonation-level.md)
</dt> </dl>

 

 



