---
description: При изменении привилегий пользователя или при добавлении ролей в приложение можно переместить учетную запись из одной роли в другую.
ms.assetid: 2d81a45a-9762-48b9-8395-3c3a4dcd5e8c
title: Удаление учетной записи пользователя или группы из роли
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 176272aef16af0d0a65d90f6a1d7628a5af232fc
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105710792"
---
# <a name="removing-a-user-account-or-group-from-a-role"></a><span data-ttu-id="a70a8-103">Удаление учетной записи пользователя или группы из роли</span><span class="sxs-lookup"><span data-stu-id="a70a8-103">Removing a User Account or Group from a Role</span></span>

<span data-ttu-id="a70a8-104">При изменении прав пользователя или добавлении ролей в приложение можно переместить учетную запись из одной роли в другую.</span><span class="sxs-lookup"><span data-stu-id="a70a8-104">If a user's privileges change or if roles are added to an application, you can move an account from one role to another role.</span></span> <span data-ttu-id="a70a8-105">Чтобы переместить учетную запись пользователя или группу пользователей из одной роли в другую, необходимо удалить учетную запись пользователя или группу из текущей роли, а затем назначить ее новой роли.</span><span class="sxs-lookup"><span data-stu-id="a70a8-105">To move a user account or group of users from one role to another, you must remove the user account or group from its current role and then assign it to the new role.</span></span>

<span data-ttu-id="a70a8-106">**Перемещение учетной записи пользователя или группы из одной роли в другую**</span><span class="sxs-lookup"><span data-stu-id="a70a8-106">**To move a user account or group from one role to another**</span></span>

1.  <span data-ttu-id="a70a8-107">Удалите учетную запись пользователя или группу из роли, которой она больше не должна принадлежать, следующим образом:</span><span class="sxs-lookup"><span data-stu-id="a70a8-107">Remove the user account or group from the role that it should no longer belong to, as follows:</span></span>

    1.  <span data-ttu-id="a70a8-108">В дереве консоли средства администрирования "службы компонентов" выберите приложение COM+, содержащее нужную роль.</span><span class="sxs-lookup"><span data-stu-id="a70a8-108">In the console tree of the Component Services administrative tool, locate the COM+ application that contains the role you are interested in.</span></span> <span data-ttu-id="a70a8-109">Разверните представление в дереве консоли, пока пользователи роли не будут видимы.</span><span class="sxs-lookup"><span data-stu-id="a70a8-109">Expand the view in the console tree until the users for the role are visible.</span></span>

    2.  <span data-ttu-id="a70a8-110">Щелкните правой кнопкой мыши учетную запись пользователя или группу, которую необходимо удалить, и выберите команду **Удалить**.</span><span class="sxs-lookup"><span data-stu-id="a70a8-110">Right-click the user account or group you want to remove, and then click **Delete**.</span></span>

    3.  <span data-ttu-id="a70a8-111">При появлении запроса в диалоговом окне **Подтверждение удаления элемента** нажмите кнопку **Да** , чтобы удалить учетную запись пользователя или группу.</span><span class="sxs-lookup"><span data-stu-id="a70a8-111">When prompted by the **Confirm Item Delete** dialog box, click **Yes** to delete the user account or group.</span></span>

    <span data-ttu-id="a70a8-112">Учетная запись пользователя или группа, которая была удалена из роли, больше не отображается в папке " **Пользователи** ".</span><span class="sxs-lookup"><span data-stu-id="a70a8-112">The user account or group that you have removed from the role no longer appears in the **Users** folder.</span></span>

2.  <span data-ttu-id="a70a8-113">Назначьте учетную запись пользователя или группу, которые были удалены в роли, которым будет назначен пользователь или группа, следующим образом:</span><span class="sxs-lookup"><span data-stu-id="a70a8-113">Assign the user account or group you have removed to the roles that the user or group should be assigned to, as follows:</span></span>

    1.  <span data-ttu-id="a70a8-114">В дереве консоли средства администрирования "службы компонентов" выберите приложение COM+, содержащее роль, в которую нужно добавить учетную запись пользователя или группу.</span><span class="sxs-lookup"><span data-stu-id="a70a8-114">In the console tree of the Component Services administrative tool, locate the COM+ application that contains the role to which you want to add the user account or group.</span></span> <span data-ttu-id="a70a8-115">Разверните представление в дереве консоли, пока роли приложения не будут видимы.</span><span class="sxs-lookup"><span data-stu-id="a70a8-115">Expand the view in the console tree until the application's roles are visible.</span></span>

    2.  <span data-ttu-id="a70a8-116">Выберите роль, в которую нужно добавить учетную запись пользователя или группу.</span><span class="sxs-lookup"><span data-stu-id="a70a8-116">Locate the role to which you want to add the user account or group.</span></span>

        > [!Note]  
        > <span data-ttu-id="a70a8-117">Если искомая роль отсутствует в папке **roles** , то роль не была добавлена в приложение.</span><span class="sxs-lookup"><span data-stu-id="a70a8-117">If the role you are looking for is not in the **Roles** folder, the role has not been added to the application.</span></span> <span data-ttu-id="a70a8-118">Перед тем как назначить учетным записям пользователей роль, он должен быть добавлен в приложение разработчиком.</span><span class="sxs-lookup"><span data-stu-id="a70a8-118">It must be added to the application by the developer before you can assign user accounts to the role.</span></span>

         

    3.  <span data-ttu-id="a70a8-119">Щелкните правой кнопкой мыши папку **Пользователи** в роли, наведите указатель на пункт **создать** и выберите пункт **пользователь**.</span><span class="sxs-lookup"><span data-stu-id="a70a8-119">Right-click the **Users** folder in the role, point to **New**, and then click **User**.</span></span>

    4.  <span data-ttu-id="a70a8-120">В нижней области окна **Выбор пользователей или групп** введите полное имя пользователя или группы, которые нужно добавить.</span><span class="sxs-lookup"><span data-stu-id="a70a8-120">In the **Select Users or Groups** window, in the bottom pane, type the fully qualified name of the user or group you want to add.</span></span> <span data-ttu-id="a70a8-121">Если имя неизвестно, нажмите кнопку " **Дополнительно** ", а затем нажмите кнопку " **найти** ", чтобы просмотреть список пользователей и групп в выбранном домене.</span><span class="sxs-lookup"><span data-stu-id="a70a8-121">If you do not know the name, click the **Advanced** button and then click **Find Now** to view a list of users and groups in the selected domain.</span></span> <span data-ttu-id="a70a8-122">Выберите пользователя или группу из списка **имя (RDN)** и нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="a70a8-122">Select a user or group from the **Name (RDN)** list and click **OK**.</span></span>

    5.  <span data-ttu-id="a70a8-123">Завершив добавление учетной записи пользователя или группы к роли, нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="a70a8-123">When you have finished adding the user account or group to the role, click **OK**.</span></span>

    <span data-ttu-id="a70a8-124">Для каждой учетной записи пользователя или группы, назначенной роли, в папке **Пользователи** появляется значок.</span><span class="sxs-lookup"><span data-stu-id="a70a8-124">For each user account or group you have assigned to the role, an icon appears in the **Users** folder.</span></span>

<span data-ttu-id="a70a8-125">Измененное членство в роли для учетной записи пользователя или группы вступает в силу при следующем запуске приложения.</span><span class="sxs-lookup"><span data-stu-id="a70a8-125">The changed role membership for the user account or group takes effect the next time the application is started.</span></span>

 

 



