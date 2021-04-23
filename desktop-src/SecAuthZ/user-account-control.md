---
description: Позволяет пользователям выполнять стандартные задачи, не являющиеся администраторами, называемые обычными пользователями, и администраторами без необходимости переключения пользователей, выхода из системы или использования запуска от имени.
ms.assetid: 8a7ba726-c2a6-4b7b-b664-3c6fcfbfb221
title: Управление учетными записями пользователей (авторизация)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: be7f3cd8f31dda8f1b15145bc4003fc9ede8782c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103999230"
---
# <a name="user-account-control-authorization"></a><span data-ttu-id="01e4b-103">Управление учетными записями пользователей (авторизация)</span><span class="sxs-lookup"><span data-stu-id="01e4b-103">User Account Control (Authorization)</span></span>

<span data-ttu-id="01e4b-104">Контроль учетных записей (UAC) позволяет пользователям выполнять типичные задачи, не являющиеся администраторами, называемые обычными пользователями, и администраторами без необходимости переключения пользователей, выхода из системы или использования **запуска от имени**.</span><span class="sxs-lookup"><span data-stu-id="01e4b-104">User Account Control (UAC) enables users to perform common tasks as nonadministrators, called standard users, and as administrators without having to switch users, log off, or use **Run As**.</span></span> <span data-ttu-id="01e4b-105">Поведение UAC для параметра "никогда не уведомлять" больше не отключает контроль учетных записей.</span><span class="sxs-lookup"><span data-stu-id="01e4b-105">The behavior of UAC for the "Never notify" setting no longer disables UAC.</span></span> <span data-ttu-id="01e4b-106">Параметр "никогда не уведомлять" предоставляет маркер разбиения и всегда автоматически повышает необходимый уровень привилегий.</span><span class="sxs-lookup"><span data-stu-id="01e4b-106">The "Never notify" setting gives you a split token and always automatically elevates the privilege required.</span></span> <span data-ttu-id="01e4b-107">Эта тонкость может привести к проблемам совместимости приложения.</span><span class="sxs-lookup"><span data-stu-id="01e4b-107">This subtlety may cause your app to have compatibility problems.</span></span> <span data-ttu-id="01e4b-108">Вы по-прежнему можете отключить UAC с помощью групповых политик или вручную задавая раздел реестра.</span><span class="sxs-lookup"><span data-stu-id="01e4b-108">You can still disable UAC by using Group Policies or manually setting the registry key.</span></span>

<span data-ttu-id="01e4b-109">**Windows server 2008 R2, Windows 7, Windows Server 2008 и Windows Vista:** Параметр "никогда не уведомлять" отключает контроль учетных записей.</span><span class="sxs-lookup"><span data-stu-id="01e4b-109">**Windows Server 2008 R2, Windows 7, Windows Server 2008 and Windows Vista:** The "Never notify" setting disables UAC.</span></span>

<span data-ttu-id="01e4b-110">Например, если вы выполните следующие действия, чтобы изменить параметр "никогда не уведомлять", при попытке создать файл в папке, для которой требуются повышенные привилегии, будут получены разные результаты.</span><span class="sxs-lookup"><span data-stu-id="01e4b-110">For example, if you perform the following steps to change the "Never notify" setting, you get different outcomes when you attempt to create a file in a folder that requires elevated privileges.</span></span> <span data-ttu-id="01e4b-111">Поведение Windows 8 заключается в запрете доступа.</span><span class="sxs-lookup"><span data-stu-id="01e4b-111">The Windows 8 behavior is to deny access.</span></span> <span data-ttu-id="01e4b-112">Поведение Windows 7 позволяет создать файл File.txt.</span><span class="sxs-lookup"><span data-stu-id="01e4b-112">The Windows 7 behavior allows you to create the File.txt file.</span></span>

1.  <span data-ttu-id="01e4b-113">Нажмите кнопку **Пуск**.</span><span class="sxs-lookup"><span data-stu-id="01e4b-113">Click or tap **Start**.</span></span> <span data-ttu-id="01e4b-114">В поле поиска введите "изменение параметров управления учетными записями пользователей".</span><span class="sxs-lookup"><span data-stu-id="01e4b-114">In the search box, type "Change User Account Control settings".</span></span>
2.  <span data-ttu-id="01e4b-115">Нажмите кнопку **изменить параметры контроля учетных записей** , чтобы открыть ее.</span><span class="sxs-lookup"><span data-stu-id="01e4b-115">Click or tap **Change User Account Control settings** to open it.</span></span>
3.  <span data-ttu-id="01e4b-116">Переместите ползунок, чтобы **не уведомлять**.</span><span class="sxs-lookup"><span data-stu-id="01e4b-116">Move the slider to **Never notify**.</span></span>
4.  <span data-ttu-id="01e4b-117">Нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="01e4b-117">Click or tap **OK**.</span></span>
5.  <span data-ttu-id="01e4b-118">Перезапустите компьютер.</span><span class="sxs-lookup"><span data-stu-id="01e4b-118">Restart your computer.</span></span>
6.  <span data-ttu-id="01e4b-119">Нажмите кнопку **Пуск** , **а затем — запустить.**</span><span class="sxs-lookup"><span data-stu-id="01e4b-119">Click or tap **Start** and then **Run**.</span></span> <span data-ttu-id="01e4b-120">В поле **Открыть** введите "Cmd.exe".</span><span class="sxs-lookup"><span data-stu-id="01e4b-120">In the **Open** box, type "Cmd.exe".</span></span> <span data-ttu-id="01e4b-121">Обратите внимание, что заголовок окна не содержит строку «Administrator».</span><span class="sxs-lookup"><span data-stu-id="01e4b-121">Note that the title of the window doesn't contain the string "Administrator".</span></span>
7.  <span data-ttu-id="01e4b-122">Введите "Echo >% WINDIR% \\ system32 \\File.txt".</span><span class="sxs-lookup"><span data-stu-id="01e4b-122">Type "echo > %windir%\\system32\\File.txt".</span></span>

<span data-ttu-id="01e4b-123">UAC был добавлен в Windows Server 2008 и Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="01e4b-123">UAC was added in Windows Server 2008 and Windows Vista.</span></span> <span data-ttu-id="01e4b-124">Учетная запись обычного пользователя является синонимом учетной записи пользователя в Windows XP.</span><span class="sxs-lookup"><span data-stu-id="01e4b-124">A standard user account is synonymous with a user account in Windows XP.</span></span> <span data-ttu-id="01e4b-125">Учетные записи пользователей, входящие в группу локальных администраторов, будут запускать большинство приложений в качестве обычного пользователя.</span><span class="sxs-lookup"><span data-stu-id="01e4b-125">User accounts that are members of the local Administrators group will run most applications as a standard user.</span></span>

<span data-ttu-id="01e4b-126">Дополнительные сведения о контроле учетных записей см. в следующих разделах.</span><span class="sxs-lookup"><span data-stu-id="01e4b-126">For information about UAC, see the following topics.</span></span>



| <span data-ttu-id="01e4b-127">Раздел</span><span class="sxs-lookup"><span data-stu-id="01e4b-127">Topic</span></span>                                                                                                                                        | <span data-ttu-id="01e4b-128">Описание</span><span class="sxs-lookup"><span data-stu-id="01e4b-128">Description</span></span>                                                                                                                                   |
|----------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="01e4b-129">[Рекомендации по управлению учетными записями пользователей в разработке пользовательского интерфейса](https://msdn.microsoft.com/library/aa511445(l=en-us,v=MSDN.10).aspx)</span><span class="sxs-lookup"><span data-stu-id="01e4b-129">[Guidelines for User Account Control in UI Development](https://msdn.microsoft.com/library/aa511445(l=en-us,v=MSDN.10).aspx)</span></span><br/> | <span data-ttu-id="01e4b-130">Общие сведения о контроле учетных записей.</span><span class="sxs-lookup"><span data-stu-id="01e4b-130">General information about UAC.</span></span><br/>                                                                                                     |
| [<span data-ttu-id="01e4b-131">Разработка приложений, требующих прав администратора</span><span class="sxs-lookup"><span data-stu-id="01e4b-131">Developing Applications that Require Administrator Privilege</span></span>](developing-applications-that-require-administrator-privilege.md)<br/>  | <span data-ttu-id="01e4b-132">Модели для разработки приложений, выполняющих операции, требующие прав администратора, но выполняемые от имени обычного пользователя.</span><span class="sxs-lookup"><span data-stu-id="01e4b-132">Models for developing applications that perform operations that require administrative privilege, but that run as a standard user.</span></span><br/> |
| [<span data-ttu-id="01e4b-133">Справочник по авторизации</span><span class="sxs-lookup"><span data-stu-id="01e4b-133">Authorization Reference</span></span>](authorization-reference.md)<br/>                                                                            | <span data-ttu-id="01e4b-134">Подробные сведения о функциях авторизации, интерфейсах, структурах и других программных элементах.</span><span class="sxs-lookup"><span data-stu-id="01e4b-134">Detailed information about authorization functions, interfaces, structures, and other programming elements.</span></span><br/>                        |



 

 

 




