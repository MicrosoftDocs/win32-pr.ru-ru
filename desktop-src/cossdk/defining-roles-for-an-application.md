---
description: Вы определяете политику безопасности для приложения, определяя необходимые привилегии безопасности.
ms.assetid: 0348684f-aebd-4d2d-a69b-85fea551c0cd
title: Определение ролей для приложения
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3f8e46eb2cb857a2b2dee2aabe41cb571e12ed98
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105701174"
---
# <a name="defining-roles-for-an-application"></a><span data-ttu-id="8f60a-103">Определение ролей для приложения</span><span class="sxs-lookup"><span data-stu-id="8f60a-103">Defining Roles for an Application</span></span>

<span data-ttu-id="8f60a-104">Вы определяете политику безопасности для приложения, определяя необходимые привилегии безопасности.</span><span class="sxs-lookup"><span data-stu-id="8f60a-104">You determine a security policy for an application by defining the security privileges that it requires.</span></span> <span data-ttu-id="8f60a-105">Для этого вы объявляете символьный уровень привилегий в качестве роли, то есть определяете роль для приложения, а затем [назначаете роль](assigning-roles-to-components--interfaces--or-methods.md) определенным ресурсам в приложении.</span><span class="sxs-lookup"><span data-stu-id="8f60a-105">To do this you declare a symbolic level of privilege as a role—that is, define the role for the application—and then [assign the role](assigning-roles-to-components--interfaces--or-methods.md) to specific resources within the application.</span></span> <span data-ttu-id="8f60a-106">Такая схема выполняется при развертывании приложения, и системные администраторы заполняют роль реальными пользователями и группами пользователей.</span><span class="sxs-lookup"><span data-stu-id="8f60a-106">This design is fulfilled when the application is deployed and system administrators populate the role with actual users and user groups.</span></span> <span data-ttu-id="8f60a-107">Более подробные сведения см. в разделе [Администрирование безопасности на основе ролей](role-based-security-administration.md).</span><span class="sxs-lookup"><span data-stu-id="8f60a-107">For greater detail, see [Role-Based Security Administration](role-based-security-administration.md).</span></span>

<span data-ttu-id="8f60a-108">**Добавление роли в приложение**</span><span class="sxs-lookup"><span data-stu-id="8f60a-108">**To add a role to an application**</span></span>

1.  <span data-ttu-id="8f60a-109">В дереве консоли средства администрирования "службы компонентов" выберите приложение COM+, к которому нужно добавить роль.</span><span class="sxs-lookup"><span data-stu-id="8f60a-109">In the console tree of the Component Services administrative tool, locate the COM+ application to which you want to add the role.</span></span> <span data-ttu-id="8f60a-110">Разверните дерево, чтобы просмотреть папки для приложения.</span><span class="sxs-lookup"><span data-stu-id="8f60a-110">Expand the tree to view the folders for the application.</span></span>

2.  <span data-ttu-id="8f60a-111">Щелкните правой кнопкой мыши папку **роли** для приложения, наведите указатель на пункт **создать** и выберите **роль**.</span><span class="sxs-lookup"><span data-stu-id="8f60a-111">Right-click the **Roles** folder for the application, point to **New**, and then click **Role**.</span></span>

3.  <span data-ttu-id="8f60a-112">В диалоговом окне **роль** введите имя новой роли в указанном поле.</span><span class="sxs-lookup"><span data-stu-id="8f60a-112">In the **Role** dialog box, type the name of the new role in the box provided.</span></span>

4.  <span data-ttu-id="8f60a-113">Нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="8f60a-113">Click **OK**.</span></span>

> [!Note]  
> <span data-ttu-id="8f60a-114">После добавления ролей в приложение необходимо назначить роли соответствующим компонентам, интерфейсам и методам.</span><span class="sxs-lookup"><span data-stu-id="8f60a-114">After adding roles to the application, you must be sure to assign the roles to the appropriate components, interfaces, and methods.</span></span> <span data-ttu-id="8f60a-115">В противном случае, если безопасность на основе ролей выбрана и включена, и если роли были добавлены, но не назначены, все вызовы приложения завершатся ошибкой.</span><span class="sxs-lookup"><span data-stu-id="8f60a-115">Otherwise, if role-based security has been chosen and enabled and if roles have been added but not assigned, all calls to the application will fail.</span></span> <span data-ttu-id="8f60a-116">Дополнительные сведения см. в разделе [назначение ролей компонентам, интерфейсам или методам](assigning-roles-to-components--interfaces--or-methods.md).</span><span class="sxs-lookup"><span data-stu-id="8f60a-116">For more information, see [Assigning Roles to Components, Interfaces, or Methods](assigning-roles-to-components--interfaces--or-methods.md).</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="8f60a-117">См. также</span><span class="sxs-lookup"><span data-stu-id="8f60a-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8f60a-118">Назначение ролей компонентам, интерфейсам или методам</span><span class="sxs-lookup"><span data-stu-id="8f60a-118">Assigning Roles to Components, Interfaces, or Methods</span></span>](assigning-roles-to-components--interfaces--or-methods.md)
</dt> <dt>

[<span data-ttu-id="8f60a-119">Настройка безопасности Role-Based</span><span class="sxs-lookup"><span data-stu-id="8f60a-119">Configuring Role-Based Security</span></span>](configuring-role-based-security.md)
</dt> <dt>

[<span data-ttu-id="8f60a-120">Включение проверок доступа для приложения</span><span class="sxs-lookup"><span data-stu-id="8f60a-120">Enabling Access Checks for an Application</span></span>](enabling-access-checks-for-an-application.md)
</dt> <dt>

[<span data-ttu-id="8f60a-121">Включение проверок доступа на уровне компонентов</span><span class="sxs-lookup"><span data-stu-id="8f60a-121">Enabling Access Checks at the Component Level</span></span>](enabling-access-checks-at-the-component-level.md)
</dt> <dt>

[<span data-ttu-id="8f60a-122">Настройка уровня безопасности для проверок доступа</span><span class="sxs-lookup"><span data-stu-id="8f60a-122">Setting a Security Level for Access Checks</span></span>](setting-a-security-level-for-access-checks.md)
</dt> </dl>

 

 



