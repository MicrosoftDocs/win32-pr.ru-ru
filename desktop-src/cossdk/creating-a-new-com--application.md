---
description: Создание нового приложения COM+
ms.assetid: eec4e871-36c2-4e60-9808-1400efcfc60c
title: Создание нового приложения COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c09eb296ad0a5f2326b5d931f59a5075d001d89f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105701282"
---
# <a name="creating-a-new-com-application"></a><span data-ttu-id="3bf43-103">Создание нового приложения COM+</span><span class="sxs-lookup"><span data-stu-id="3bf43-103">Creating a New COM+ Application</span></span>

<span data-ttu-id="3bf43-104">Для создания нового приложения COM+ необходимо выполнить два основных действия, как показано ниже.</span><span class="sxs-lookup"><span data-stu-id="3bf43-104">Creating a new COM+ application requires two basic steps, as follows:</span></span>

-   <span data-ttu-id="3bf43-105">Создание пустого приложения COM+ (описывается ниже).</span><span class="sxs-lookup"><span data-stu-id="3bf43-105">Creating an empty COM+ application (described below).</span></span>
-   <span data-ttu-id="3bf43-106">Добавление компонентов в приложение.</span><span class="sxs-lookup"><span data-stu-id="3bf43-106">Adding components to the application.</span></span> <span data-ttu-id="3bf43-107">(См. статью [Установка новых компонентов](installing-new-components.md) и [Импорт компонентов](importing-components.md).)</span><span class="sxs-lookup"><span data-stu-id="3bf43-107">(See [Installing New Components](installing-new-components.md) and [Importing Components](importing-components.md).)</span></span>

<span data-ttu-id="3bf43-108">**Создание пустого приложения COM+**</span><span class="sxs-lookup"><span data-stu-id="3bf43-108">**To create an empty COM+ application**</span></span>

1.  <span data-ttu-id="3bf43-109">В дереве консоли средства администрирования "службы компонентов" выберите компьютер, на котором нужно создать приложение.</span><span class="sxs-lookup"><span data-stu-id="3bf43-109">In the console tree of the Component Services administrative tool, select the computer on which you want to create an application.</span></span>

2.  <span data-ttu-id="3bf43-110">Выберите папку **приложения COM+** для этого компьютера.</span><span class="sxs-lookup"><span data-stu-id="3bf43-110">Select the **COM+ Applications** folder for that computer.</span></span>

3.  <span data-ttu-id="3bf43-111">В меню **действие** наведите указатель на пункт **создать** и выберите пункт **приложение**.</span><span class="sxs-lookup"><span data-stu-id="3bf43-111">On the **Action** menu, point to **New**, and then click **Application**.</span></span> <span data-ttu-id="3bf43-112">Можно также щелкнуть правой кнопкой мыши папку **приложения COM+** , наведите указатель на пункт **создать** и выберите пункт **приложение**.</span><span class="sxs-lookup"><span data-stu-id="3bf43-112">You can also right-click the **COM+ Applications** folder, point to **New**, and then click **Application**.</span></span>

4.  <span data-ttu-id="3bf43-113">На странице **приветствия** мастера установки приложения COM+ нажмите кнопку **Далее**, а затем в диалоговом окне **Установка или создание нового приложения** щелкните **создать пустое приложение**.</span><span class="sxs-lookup"><span data-stu-id="3bf43-113">On the **Welcome** page of the COM+ Application Install Wizard, click **Next**, and then in the **Install or Create a New Application** dialog box, click **Create an empty application**.</span></span>

5.  <span data-ttu-id="3bf43-114">В заданном поле введите имя нового приложения.</span><span class="sxs-lookup"><span data-stu-id="3bf43-114">In the box provided, type a name for the new application.</span></span> <span data-ttu-id="3bf43-115">(Обратите внимание, что следующие специальные символы не могут использоваться в именах приложений: \\ ,/, ~,!, @, \# ,%, ^, &, \* , (,), \| ,}, {, \] , \[ , ",", >, <,.,?,: и;.) В разделе **тип активации** выберите **приложение библиотеки** или **серверное приложение**.</span><span class="sxs-lookup"><span data-stu-id="3bf43-115">(Note that the following special characters cannot be used in an application name: \\, /, ~, !, @, \#, %, ^, &, \*, (, ), \|, }, {, \], \[, ', ", >, <, ., ?, :, and ;.) Under **Activation type**, click **Library application** or **Server application**.</span></span> <span data-ttu-id="3bf43-116">Нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="3bf43-116">Click **Next**.</span></span>

    > [!Note]  
    > <span data-ttu-id="3bf43-117">Серверное приложение выполняется в собственном процессе.</span><span class="sxs-lookup"><span data-stu-id="3bf43-117">A server application runs in its own process.</span></span> <span data-ttu-id="3bf43-118">Серверные приложения могут поддерживать все службы COM+.</span><span class="sxs-lookup"><span data-stu-id="3bf43-118">Server applications can support all COM+ services.</span></span> <span data-ttu-id="3bf43-119">Приложение библиотеки выполняется в процессе клиента, который его создает.</span><span class="sxs-lookup"><span data-stu-id="3bf43-119">A library application runs in the process of the client that creates it.</span></span> <span data-ttu-id="3bf43-120">Библиотечные приложения могут использовать безопасность на основе ролей, но не поддерживают удаленный доступ или компоненты, поставленные в очередь.</span><span class="sxs-lookup"><span data-stu-id="3bf43-120">Library applications can use role-based security but do not support remote access or queued components.</span></span>

     

6.  <span data-ttu-id="3bf43-121">В диалоговом окне **задать удостоверение приложения** выберите удостоверение, под которым будет выполняться приложение.</span><span class="sxs-lookup"><span data-stu-id="3bf43-121">In the **Set Application Identity** dialog box, choose an identity under which the application will run.</span></span> <span data-ttu-id="3bf43-122">При выборе **этого пользователя** введите имя пользователя и пароль.</span><span class="sxs-lookup"><span data-stu-id="3bf43-122">If you select **This user**, type the user name and password.</span></span> <span data-ttu-id="3bf43-123">Также необходимо повторно ввести пароль в поле **Подтверждение пароля** .</span><span class="sxs-lookup"><span data-stu-id="3bf43-123">You must also retype the password in the **Confirm password** box.</span></span> <span data-ttu-id="3bf43-124">Нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="3bf43-124">Click **Next**.</span></span> <span data-ttu-id="3bf43-125">(По умолчанию для удостоверения приложения выбран **Интерактивный пользователь**.</span><span class="sxs-lookup"><span data-stu-id="3bf43-125">(The default selection for application identity is **Interactive User**.</span></span> <span data-ttu-id="3bf43-126">Интерактивным пользователем является пользователь, вошедший в систему на сервере в любое заданное время.</span><span class="sxs-lookup"><span data-stu-id="3bf43-126">The interactive user is the user logged on to the server computer at any given time.</span></span> <span data-ttu-id="3bf43-127">Можно выбрать другого пользователя, выбрав **этого пользователя** и введя конкретного пользователя или группу.)</span><span class="sxs-lookup"><span data-stu-id="3bf43-127">You can select a different user by selecting **This user** and entering a specific user or group.)</span></span>

    > [!Note]  
    > <span data-ttu-id="3bf43-128">Диалоговое окно **Задание удостоверения приложения** появляется только в том случае, если в предыдущем диалоговом окне мастера установки приложения COM выбран параметр **серверное приложение** для нового типа активации приложения.</span><span class="sxs-lookup"><span data-stu-id="3bf43-128">The **Set Application Identity** dialog box appears only if you selected **Server application** for the new application's activation type in the COM Application Install Wizard's preceding dialog box.</span></span> <span data-ttu-id="3bf43-129">Свойство Identity не используется для библиотечных приложений.</span><span class="sxs-lookup"><span data-stu-id="3bf43-129">The identity property is not used for library applications.</span></span>

     

7.  <span data-ttu-id="3bf43-130">В диалоговом окне **Добавление ролей приложений** добавьте роли, которые необходимо связать с приложением.</span><span class="sxs-lookup"><span data-stu-id="3bf43-130">In the **Add Application Roles** dialog box, add any roles you want to associate with the application.</span></span> <span data-ttu-id="3bf43-131">По умолчанию определена только роль **креаторовнер** .</span><span class="sxs-lookup"><span data-stu-id="3bf43-131">By default, only the **CreatorOwner** role is defined.</span></span> <span data-ttu-id="3bf43-132">Сведения о ролях см. в разделе [Администрирование безопасности на основе ролей](role-based-security-administration.md).</span><span class="sxs-lookup"><span data-stu-id="3bf43-132">For information on roles, see [Role-Based Security Administration](role-based-security-administration.md).</span></span>

8.  <span data-ttu-id="3bf43-133">В диалоговом окне **Добавление пользователей в роли** заполните каждую роль, созданную на последнем шаге, с помощью пользователей, групп или встроенных участников безопасности, которым необходимо предоставить привилегии, связанные с этой ролью.</span><span class="sxs-lookup"><span data-stu-id="3bf43-133">In the **Add Users to Roles** dialog box, populate each role you created in the last step with the users, groups, or built-in security principals to which you want to grant the privileges associated with that role.</span></span> <span data-ttu-id="3bf43-134">По умолчанию Интерактивный пользователь помещается в роль **креаторовнер** .</span><span class="sxs-lookup"><span data-stu-id="3bf43-134">By default, the interactive user is placed in the **CreatorOwner** role.</span></span>

9.  <span data-ttu-id="3bf43-135">Нажмите кнопку **Готово**.</span><span class="sxs-lookup"><span data-stu-id="3bf43-135">Click **Finish**.</span></span>

<span data-ttu-id="3bf43-136">Новое приложение будет отображаться в папке **приложения COM+** в дереве консоли средства администрирования "службы компонентов".</span><span class="sxs-lookup"><span data-stu-id="3bf43-136">The new application will now be displayed under the **COM+ Applications** folder in the console tree of the Component Services administrative tool.</span></span>

> [!Note]  
> <span data-ttu-id="3bf43-137">Начиная с Windows Server 2003, проверки доступа по умолчанию включены при создании приложения COM+.</span><span class="sxs-lookup"><span data-stu-id="3bf43-137">As of Windows Server 2003, access checks are enabled by default when creating a COM+ application.</span></span> <span data-ttu-id="3bf43-138">В предыдущих версиях проверки доступа по умолчанию отключены на уровне приложения.</span><span class="sxs-lookup"><span data-stu-id="3bf43-138">In previous versions, access checks were disabled by default at the application level.</span></span> <span data-ttu-id="3bf43-139">По умолчанию доступ к приложению COM+ разрешен только пользователям, которые находятся в ролях, связанных с приложением.</span><span class="sxs-lookup"><span data-stu-id="3bf43-139">The result is that by default, access to a COM+ application is allowed only to users that are in the roles associated with the application.</span></span> <span data-ttu-id="3bf43-140">(См. раздел [Администрирование безопасности на основе ролей](role-based-security-administration.md).) Кроме того, можно разрешить доступ всем пользователям, отключив проверки доступа к приложению COM+.</span><span class="sxs-lookup"><span data-stu-id="3bf43-140">(See [Role-Based Security Administration](role-based-security-administration.md).) Alternatively, you can allow access to all users by disabling access checks on a COM+ application.</span></span> <span data-ttu-id="3bf43-141">(См. раздел [Включение проверок доступа для приложения](enabling-access-checks-for-an-application.md).)</span><span class="sxs-lookup"><span data-stu-id="3bf43-141">(See [Enabling Access Checks for an Application](enabling-access-checks-for-an-application.md).)</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="3bf43-142">См. также</span><span class="sxs-lookup"><span data-stu-id="3bf43-142">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3bf43-143">Копирование компонентов</span><span class="sxs-lookup"><span data-stu-id="3bf43-143">Copying Components</span></span>](copying-components.md)
</dt> <dt>

[<span data-ttu-id="3bf43-144">Удаление приложения COM+</span><span class="sxs-lookup"><span data-stu-id="3bf43-144">Deleting a COM+ Application</span></span>](deleting-a-com--application.md)
</dt> <dt>

[<span data-ttu-id="3bf43-145">Импорт компонентов</span><span class="sxs-lookup"><span data-stu-id="3bf43-145">Importing Components</span></span>](importing-components.md)
</dt> <dt>

[<span data-ttu-id="3bf43-146">Установка новых компонентов</span><span class="sxs-lookup"><span data-stu-id="3bf43-146">Installing New Components</span></span>](installing-new-components.md)
</dt> <dt>

[<span data-ttu-id="3bf43-147">Перемещение компонентов</span><span class="sxs-lookup"><span data-stu-id="3bf43-147">Moving Components</span></span>](moving-components.md)
</dt> <dt>

[<span data-ttu-id="3bf43-148">Удаление компонента из приложения COM+</span><span class="sxs-lookup"><span data-stu-id="3bf43-148">Removing a Component from a COM+ Application</span></span>](removing-a-component-from-a-com--application.md)
</dt> </dl>

 

 



