---
description: Вы можете удалить учетные записи пользователей или группы из роли, когда пользователям или членам групп больше не нужно предоставлять доступ к ресурсам приложения, которым назначена роль.
ms.assetid: d2cfa5cb-a143-41de-9aa2-7af7fce10ed7
title: Перемещение учетной записи пользователя или группы в другую роль
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2401d792066212269d4eaa4eb11eadfef6e2d73e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104142385"
---
# <a name="moving-a-user-account-or-group-to-a-different-role"></a><span data-ttu-id="24e12-103">Перемещение учетной записи пользователя или группы в другую роль</span><span class="sxs-lookup"><span data-stu-id="24e12-103">Moving a User Account or Group to a Different Role</span></span>

<span data-ttu-id="24e12-104">Вы можете удалить учетные записи пользователей или группы из роли, когда пользователям или членам групп больше не нужно предоставлять доступ к ресурсам приложения, которым назначена роль.</span><span class="sxs-lookup"><span data-stu-id="24e12-104">You can remove user accounts or groups from a role when the users or members of the groups should no longer be given access to the application resources to which the role is assigned.</span></span>

<span data-ttu-id="24e12-105">**Удаление учетной записи пользователя или группы из роли**</span><span class="sxs-lookup"><span data-stu-id="24e12-105">**To remove a user account or group from a role**</span></span>

1.  <span data-ttu-id="24e12-106">В дереве консоли средства администрирования "службы компонентов" выберите приложение COM+, содержащее нужную роль.</span><span class="sxs-lookup"><span data-stu-id="24e12-106">In the console tree of the Component Services administrative tool, locate the COM+ application that contains the role you are interested in.</span></span> <span data-ttu-id="24e12-107">Разверните представление в дереве консоли, пока пользователи роли не будут видимы.</span><span class="sxs-lookup"><span data-stu-id="24e12-107">Expand the view in the console tree until the users for the role are visible.</span></span>

2.  <span data-ttu-id="24e12-108">Щелкните правой кнопкой мыши учетную запись пользователя или группу, которую необходимо удалить, и выберите команду **Удалить**.</span><span class="sxs-lookup"><span data-stu-id="24e12-108">Right-click the user account or group you want to remove, and then click **Delete**.</span></span>

3.  <span data-ttu-id="24e12-109">При появлении запроса в диалоговом окне **Подтверждение удаления элемента** нажмите кнопку **Да** , чтобы удалить учетную запись пользователя или группу.</span><span class="sxs-lookup"><span data-stu-id="24e12-109">When prompted by the **Confirm Item Delete** dialog box, click **Yes** to delete the user account or group.</span></span>

<span data-ttu-id="24e12-110">Учетная запись пользователя или группа, которая была удалена из роли, больше не отображается в папке " **Пользователи** ".</span><span class="sxs-lookup"><span data-stu-id="24e12-110">The user account or group that you have removed from the role no longer appears in the **Users** folder.</span></span> <span data-ttu-id="24e12-111">Новое членство в роли вступает в силу при следующем запуске приложения.</span><span class="sxs-lookup"><span data-stu-id="24e12-111">The new role membership takes effect the next time the application is started.</span></span> <span data-ttu-id="24e12-112">Если вы внесли изменения в **Системное приложение**, необходимо перезагрузить компьютер, чтобы изменения вступили в силу.</span><span class="sxs-lookup"><span data-stu-id="24e12-112">If you have made changes to the **System Application**, you must restart the computer for the changes to take effect.</span></span>

 

 



