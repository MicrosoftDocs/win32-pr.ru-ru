---
description: Средство администрирования служб компонентов можно использовать для заполнения роли учетными записями или группами пользователей.
ms.assetid: 1cf7dc38-185a-4cc4-8f4c-44b6af4c5f4a
title: Назначение роли учетной записи пользователя или группы
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d53b37c9f0265e02c7abdf74eeaf81bd0b12e3d8
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105710763"
---
# <a name="assigning-a-user-account-or-group-to-a-role"></a><span data-ttu-id="7b4f6-103">Назначение роли учетной записи пользователя или группы</span><span class="sxs-lookup"><span data-stu-id="7b4f6-103">Assigning a User Account or Group to a Role</span></span>

<span data-ttu-id="7b4f6-104">Средство администрирования служб компонентов можно использовать для заполнения роли учетными записями или группами пользователей.</span><span class="sxs-lookup"><span data-stu-id="7b4f6-104">You can use the Component Services administrative tool to populate a role with user accounts or groups.</span></span> <span data-ttu-id="7b4f6-105">Для назначения роли учетной записи пользователя предпочтительнее назначить учетную запись пользователя группе, а затем назначить ее роли.</span><span class="sxs-lookup"><span data-stu-id="7b4f6-105">The preferred way to assign a user account to a role is to assign the user account to a group and then assign the group to the role.</span></span> <span data-ttu-id="7b4f6-106">Использование групп для заполнения ролей упрощает управление большим количеством пользователей.</span><span class="sxs-lookup"><span data-stu-id="7b4f6-106">Using groups to populate roles makes it easier for you to manage large numbers of users.</span></span> <span data-ttu-id="7b4f6-107">В интерактивной справке для средства администрирования "Управление компьютером" ознакомьтесь с разделом "Локальные пользователи и группы", чтобы получить дополнительные сведения о создании групп или назначении учетной записи пользователя в группе.</span><span class="sxs-lookup"><span data-stu-id="7b4f6-107">In the online help for the Computer Management administrative tool, see the topic "Local Users and Groups" for more information about creating groups or assigning a user account to a group.</span></span>

> [!Note]  
> <span data-ttu-id="7b4f6-108">Чтобы разрешить пользователям сети, не прошедшим проверку подлинности, запускать приложение COM+, роли приложения должны включать анонимного пользователя.</span><span class="sxs-lookup"><span data-stu-id="7b4f6-108">To allow unauthenticated network users to run a COM+ application, the application roles must include the Anonymous user.</span></span> <span data-ttu-id="7b4f6-109">Начиная с Windows Server 2003, анонимный пользователь по умолчанию не включен в группу «все».</span><span class="sxs-lookup"><span data-stu-id="7b4f6-109">Starting with Windows Server 2003, by default, the Anonymous user is not included in the Everyone group.</span></span>

 

<span data-ttu-id="7b4f6-110">После назначения учетной записи пользователя соответствующей группе Windows выполните следующие действия, чтобы присвоить группе Windows роль.</span><span class="sxs-lookup"><span data-stu-id="7b4f6-110">After you have assigned the user account to the appropriate Windows group, follow these steps to assign the Windows group to the role.</span></span>

<span data-ttu-id="7b4f6-111">**Назначение группы Windows роли безопасности**</span><span class="sxs-lookup"><span data-stu-id="7b4f6-111">**To assign a Windows group to a security role**</span></span>

1.  <span data-ttu-id="7b4f6-112">В дереве консоли средства администрирования "службы компонентов" выберите приложение COM+, содержащее роль, в которую нужно добавить учетную запись пользователя или группу.</span><span class="sxs-lookup"><span data-stu-id="7b4f6-112">In the console tree of the Component Services administrative tool, locate the COM+ application that contains the role to which you want to add the user account or group.</span></span> <span data-ttu-id="7b4f6-113">Разверните представление в дереве консоли, пока роли приложения не будут видимы.</span><span class="sxs-lookup"><span data-stu-id="7b4f6-113">Expand the view in the console tree until the application's roles are visible.</span></span>

2.  <span data-ttu-id="7b4f6-114">Выберите роль, в которую нужно добавить учетную запись пользователя или группу.</span><span class="sxs-lookup"><span data-stu-id="7b4f6-114">Locate the role to which you want to add the user account or group.</span></span>

    > [!Note]  
    > <span data-ttu-id="7b4f6-115">Если искомая роль отсутствует в папке **roles** , то роль не была добавлена в приложение.</span><span class="sxs-lookup"><span data-stu-id="7b4f6-115">If the role you are looking for is not in the **Roles** folder, the role has not been added to the application.</span></span> <span data-ttu-id="7b4f6-116">Перед тем как назначить учетным записям пользователей роль, он должен быть добавлен в приложение разработчиком.</span><span class="sxs-lookup"><span data-stu-id="7b4f6-116">It must be added to the application by the developer before you can assign user accounts to the role.</span></span>

     

3.  <span data-ttu-id="7b4f6-117">Щелкните правой кнопкой мыши папку **Пользователи** в роли, наведите указатель на пункт **создать** и выберите пункт **пользователь**.</span><span class="sxs-lookup"><span data-stu-id="7b4f6-117">Right-click the **Users** folder in the role, point to **New**, and then click **User**.</span></span>

4.  <span data-ttu-id="7b4f6-118">В нижней области окна **Выбор пользователей или групп** введите полное имя пользователя или группы, которые нужно добавить.</span><span class="sxs-lookup"><span data-stu-id="7b4f6-118">In the **Select Users or Groups** window, in the bottom pane, type the fully qualified name of the user or group you want to add.</span></span> <span data-ttu-id="7b4f6-119">Если имя неизвестно, нажмите кнопку " **Дополнительно** ", а затем нажмите кнопку " **найти** ", чтобы просмотреть список пользователей и групп в выбранном домене.</span><span class="sxs-lookup"><span data-stu-id="7b4f6-119">If you do not know the name, click the **Advanced** button and then click **Find Now** to view a list of users and groups in the selected domain.</span></span> <span data-ttu-id="7b4f6-120">Выберите пользователя или группу из списка **имя (RDN)** и нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="7b4f6-120">Select a user or group from the **Name (RDN)** list, and click **OK**.</span></span>

5.  <span data-ttu-id="7b4f6-121">Чтобы добавить дополнительные учетные записи пользователей или группы, повторите шаг 4.</span><span class="sxs-lookup"><span data-stu-id="7b4f6-121">To add more user accounts or groups, repeat step 4.</span></span>

6.  <span data-ttu-id="7b4f6-122">Завершив добавление учетных записей пользователей и групп к роли, нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="7b4f6-122">When you have finished adding user accounts and groups to the role, click **OK**.</span></span>

<span data-ttu-id="7b4f6-123">Для каждой учетной записи пользователя или группы, назначенной роли, в папке **Пользователи** появляется значок.</span><span class="sxs-lookup"><span data-stu-id="7b4f6-123">For each user account or group you have assigned to the role, an icon appears in the **Users** folder.</span></span> <span data-ttu-id="7b4f6-124">Новое членство в роли вступает в силу при следующем запуске приложения.</span><span class="sxs-lookup"><span data-stu-id="7b4f6-124">The new role membership takes effect the next time the application is started.</span></span>

 

 



