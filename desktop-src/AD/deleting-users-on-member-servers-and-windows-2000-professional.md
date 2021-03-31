---
title: Удаление пользователей на рядовых серверах и Windows 2000 Professional
description: В этом разделе показано, как удалить пользователя с рядового сервера или компьютера, работающего под Windows 2000 Professional.
ms.assetid: 0c94c08b-46cb-494e-89f8-a21bfb20e34c
ms.tgt_platform: multiple
keywords:
- Пользователи AD, удаление пользователя на рядовых серверах и Windows 2000 Professional
- Active Directory, использование, пользователи, удаление пользователей на рядовых серверах и Windows 2000 Professional
- Удаление пользователя
- сервер, удаление пользователя
- Удаление пользователей на рядовых серверах и Windows 2000 Professional AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aae4287c8b7d32e15e7df3e73f365409d7fe49a0
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/17/2020
ms.locfileid: "104069784"
---
# <a name="deleting-users-on-member-servers-and-windows-2000-professional"></a><span data-ttu-id="4ee1d-108">Удаление пользователей на рядовых серверах и Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="4ee1d-108">Deleting Users on Member Servers and Windows 2000 Professional</span></span>

<span data-ttu-id="4ee1d-109">В этом разделе показано, как удалить пользователя с рядового сервера или компьютера, работающего под Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="4ee1d-109">This topic shows how to delete a user from a member server or computer running on Windows 2000 Professional.</span></span>

<span data-ttu-id="4ee1d-110">**Удаление пользователя**</span><span class="sxs-lookup"><span data-stu-id="4ee1d-110">**To delete a user**</span></span>

1.  <span data-ttu-id="4ee1d-111">Выполните привязку к компьютеру, используя следующие правила.</span><span class="sxs-lookup"><span data-stu-id="4ee1d-111">Bind to the computer using the following rules:</span></span>
    1.  <span data-ttu-id="4ee1d-112">Используйте учетную запись с достаточными правами для доступа к этому компьютеру.</span><span class="sxs-lookup"><span data-stu-id="4ee1d-112">Use an account with sufficient rights to access that computer.</span></span>
    2.  <span data-ttu-id="4ee1d-113">Используйте следующий формат строки привязки с помощью поставщика WinNT, имени компьютера и дополнительного параметра, чтобы указать ADSI, что он привязывает к компьютеру: "WinNT:// <computer name> <computer> ".</span><span class="sxs-lookup"><span data-stu-id="4ee1d-113">Use the following binding string format using the WinNT provider, computer name, and an extra parameter to tell ADSI that it is binding to a computer: "WinNT://<computer name>,<computer>".</span></span> <span data-ttu-id="4ee1d-114">&lt;Параметр Computer Name &gt; — это имя компьютера, к которому необходимо получить доступ.</span><span class="sxs-lookup"><span data-stu-id="4ee1d-114">The "&lt;computer name&gt;" parameter is the name of the computer whose groups you want to access.</span></span> <span data-ttu-id="4ee1d-115">Этот параметр уведомляет ADSI о том, что он привязывается к компьютеру, и позволяет средству синтаксического анализа поставщика WinNT пропустить некоторые запросы разрешения неоднозначности, чтобы определить тип объекта, к которому выполняется привязка.</span><span class="sxs-lookup"><span data-stu-id="4ee1d-115">This parameter notifies ADSI that it is binding to a computer and allows the WinNT provider parser to skip some ambiguity resolution queries to determine what type of object you are binding to.</span></span>
    3.  <span data-ttu-id="4ee1d-116">Привязка к интерфейсу [**иадсконтаинер**](/windows/desktop/api/iads/nn-iads-iadscontainer) .</span><span class="sxs-lookup"><span data-stu-id="4ee1d-116">Bind to the [**IADsContainer**](/windows/desktop/api/iads/nn-iads-iadscontainer) interface.</span></span>
2.  <span data-ttu-id="4ee1d-117">Укажите "User" в качестве класса с помощью [**иадсконтаинер. Delete**](/windows/desktop/api/iads/nf-iads-iadscontainer-delete) , чтобы удалить пользователя.</span><span class="sxs-lookup"><span data-stu-id="4ee1d-117">Specify "user" as the class using [**IADsContainer.Delete**](/windows/desktop/api/iads/nf-iads-iadscontainer-delete) to delete the user.</span></span>

    <span data-ttu-id="4ee1d-118">Имейте в виду, что не нужно вызывать функцию [**iAds. сетинфо**](/windows/desktop/api/iads/nf-iads-iads-setinfo) для фиксации изменений в контейнере.</span><span class="sxs-lookup"><span data-stu-id="4ee1d-118">Be aware that you do not need to call [**IADs.SetInfo**](/windows/desktop/api/iads/nf-iads-iads-setinfo) to commit the change to the container.</span></span> <span data-ttu-id="4ee1d-119">Вызов [**иадсконтаинер. Delete**](/windows/desktop/api/iads/nf-iads-iadscontainer-delete) фиксирует удаление пользователя непосредственно в каталоге.</span><span class="sxs-lookup"><span data-stu-id="4ee1d-119">The [**IADsContainer.Delete**](/windows/desktop/api/iads/nf-iads-iadscontainer-delete) call commits the deletion of the user directly to the directory.</span></span>

 

 