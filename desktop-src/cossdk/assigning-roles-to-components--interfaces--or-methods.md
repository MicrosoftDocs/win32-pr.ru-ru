---
description: Назначение ролей компонентам, интерфейсам или методам
ms.assetid: 687d5692-4a83-4de8-b99d-859aaaddd16d
title: Назначение ролей компонентам, интерфейсам или методам
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5efb66c9de865cbfcdc6e9cb047af92c95f6bc0a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104423410"
---
# <a name="assigning-roles-to-components-interfaces-or-methods"></a><span data-ttu-id="fa813-103">Назначение ролей компонентам, интерфейсам или методам</span><span class="sxs-lookup"><span data-stu-id="fa813-103">Assigning Roles to Components, Interfaces, or Methods</span></span>

<span data-ttu-id="fa813-104">Можно явно назначить роль любому элементу в приложении COM+, видимому при помощи средства администрирования "службы компонентов".</span><span class="sxs-lookup"><span data-stu-id="fa813-104">You can explicitly assign a role to any item within a COM+ application that is visible through the Component Services administrative tool.</span></span> <span data-ttu-id="fa813-105">Это гарантирует, что всем пользователям, которые являются членами роли, будет разрешен доступ к этому элементу и другим содержащимся в нем элементам.</span><span class="sxs-lookup"><span data-stu-id="fa813-105">Doing so ensures that any users that are members of the role will be permitted access to that item and any other items that it contains.</span></span> <span data-ttu-id="fa813-106">Например, если присвоить компоненту роль "Читатели", то любой член "Читатели" сможет получить доступ к этому компоненту, а также к любым интерфейсам и методам, которые он предоставляет.</span><span class="sxs-lookup"><span data-stu-id="fa813-106">For example, if you assign the role "Readers" to a component, any member of "Readers" is allowed access to that component and any interfaces and methods it exposes.</span></span> <span data-ttu-id="fa813-107">"Читатели" будут отображаться как Наследуемая роль для любого из этих интерфейсов и методов.</span><span class="sxs-lookup"><span data-stu-id="fa813-107">"Readers" will show up as an Inherited role for any of those interfaces and methods.</span></span>

<span data-ttu-id="fa813-108">Метод доступен для вызывающих объектов только в том случае, если ему назначена роль путем явного присваивания роли непосредственно методу или путем назначения роли интерфейсу или компоненту метода. в этом случае роль будет наследоваться методом.</span><span class="sxs-lookup"><span data-stu-id="fa813-108">A method is accessible to callers only if you assign a role to it, either by explicitly assigning the role directly to the method or by assigning a role to the method's interface or the method's component, in which case the role will be inherited by the method.</span></span> <span data-ttu-id="fa813-109">Если ни одна роль не назначена и проверки доступа включены, все вызовы метода завершатся ошибкой.</span><span class="sxs-lookup"><span data-stu-id="fa813-109">If no role is assigned and if access checks are enabled, all calls to the method will fail.</span></span>

<span data-ttu-id="fa813-110">Прежде чем назначить роль, необходимо [определить](defining-roles-for-an-application.md) ее для приложения.</span><span class="sxs-lookup"><span data-stu-id="fa813-110">Before you can assign a role, you must [define](defining-roles-for-an-application.md) it for the application.</span></span> <span data-ttu-id="fa813-111">Все роли, определенные для приложения, отображаются в окне **роли, явно заданные для выбранных элементов** на вкладке **Безопасность** для всех компонентов, методов и интерфейсов в приложении.</span><span class="sxs-lookup"><span data-stu-id="fa813-111">All roles defined for the application will appear in the **Roles explicitly set for selected item(s)** window on the **Security** tab for any components, methods, and interfaces within the application.</span></span>

<span data-ttu-id="fa813-112">**Назначение ролей компоненту, методу или интерфейсу**</span><span class="sxs-lookup"><span data-stu-id="fa813-112">**To assign roles to a component, method, or interface**</span></span>

1.  <span data-ttu-id="fa813-113">В дереве консоли средства администрирования "службы компонентов" выберите приложение COM+, для которого определена роль.</span><span class="sxs-lookup"><span data-stu-id="fa813-113">In the console tree of the Component Services administrative tool, locate the COM+ application for which the role has been defined.</span></span> <span data-ttu-id="fa813-114">Разверните дерево, чтобы просмотреть компоненты, интерфейсы или методы приложения, в зависимости от того, к чему вы назначаете роль.</span><span class="sxs-lookup"><span data-stu-id="fa813-114">Expand the tree to view the application's components, interfaces, or methods, depending on what you are assigning the role to.</span></span>

2.  <span data-ttu-id="fa813-115">Щелкните правой кнопкой мыши элемент, которому нужно назначить роль, и выберите пункт **Свойства**.</span><span class="sxs-lookup"><span data-stu-id="fa813-115">Right-click the item to which you want to assign the role, and then click **Properties**.</span></span>

3.  <span data-ttu-id="fa813-116">В диалоговом окне Свойства перейдите на вкладку **Безопасность** .</span><span class="sxs-lookup"><span data-stu-id="fa813-116">In the properties dialog box, click the **Security** tab.</span></span>

4.  <span data-ttu-id="fa813-117">В поле **роли, явно заданные для выбранных элементов** выберите роли, которые необходимо назначить элементу.</span><span class="sxs-lookup"><span data-stu-id="fa813-117">In the **Roles explicitly set for selected item(s)** box, select the roles that you want to assign to the item.</span></span>

5.  <span data-ttu-id="fa813-118">Нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="fa813-118">Click **OK**.</span></span>

<span data-ttu-id="fa813-119">Все роли, явно заданные для элемента, будут наследоваться всеми элементами более низкого уровня, которые он содержит, и будут отображаться в окне **роли, наследуемые выбранными** элементами для этих элементов.</span><span class="sxs-lookup"><span data-stu-id="fa813-119">Any roles that you have explicitly set for an item will be inherited by any lower-level items it contains and will show up in the **Roles inherited by selected item(s)** window for those items.</span></span>

## <a name="related-topics"></a><span data-ttu-id="fa813-120">См. также</span><span class="sxs-lookup"><span data-stu-id="fa813-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fa813-121">Настройка безопасности Role-Based</span><span class="sxs-lookup"><span data-stu-id="fa813-121">Configuring Role-Based Security</span></span>](configuring-role-based-security.md)
</dt> <dt>

[<span data-ttu-id="fa813-122">Определение ролей для приложения</span><span class="sxs-lookup"><span data-stu-id="fa813-122">Defining Roles for an Application</span></span>](defining-roles-for-an-application.md)
</dt> <dt>

[<span data-ttu-id="fa813-123">Включение проверок доступа для приложения</span><span class="sxs-lookup"><span data-stu-id="fa813-123">Enabling Access Checks for an Application</span></span>](enabling-access-checks-for-an-application.md)
</dt> <dt>

[<span data-ttu-id="fa813-124">Включение проверок доступа на уровне компонентов</span><span class="sxs-lookup"><span data-stu-id="fa813-124">Enabling Access Checks at the Component Level</span></span>](enabling-access-checks-at-the-component-level.md)
</dt> <dt>

[<span data-ttu-id="fa813-125">Настройка уровня безопасности для проверок доступа</span><span class="sxs-lookup"><span data-stu-id="fa813-125">Setting a Security Level for Access Checks</span></span>](setting-a-security-level-for-access-checks.md)
</dt> </dl>

 

 



