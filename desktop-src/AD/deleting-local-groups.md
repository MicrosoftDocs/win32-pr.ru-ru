---
title: Удаление локальных групп
description: В этом разделе показано, как удалить локальную группу с рядового сервера или компьютера, работающего под Windows 2000 Professional.
ms.assetid: 030da25a-a606-4521-a243-d902c772fd00
ms.tgt_platform: multiple
keywords:
- Удаление локальных групп Active Directory
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 14b55f90a8e6ac5cb77bf878d5ac680a6da91f73
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/17/2020
ms.locfileid: "104487464"
---
# <a name="deleting-local-groups"></a><span data-ttu-id="9de4f-104">Удаление локальных групп</span><span class="sxs-lookup"><span data-stu-id="9de4f-104">Deleting Local Groups</span></span>

<span data-ttu-id="9de4f-105">В этом разделе показано, как удалить локальную группу с рядового сервера или компьютера, работающего под Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="9de4f-105">This topic shows how to delete a local group from a member server or computer running on Windows 2000 Professional.</span></span>

<span data-ttu-id="9de4f-106">**Удаление локальной группы**</span><span class="sxs-lookup"><span data-stu-id="9de4f-106">**To delete a local group**</span></span>

1.  <span data-ttu-id="9de4f-107">Выполните привязку к компьютеру, используя следующие правила.</span><span class="sxs-lookup"><span data-stu-id="9de4f-107">Bind to the computer using the following rules:</span></span>
    1.  <span data-ttu-id="9de4f-108">Используйте учетную запись с достаточными правами для доступа к этому компьютеру.</span><span class="sxs-lookup"><span data-stu-id="9de4f-108">Use an account with sufficient rights to access that computer.</span></span>
    2.  <span data-ttu-id="9de4f-109">Используйте следующий формат строки привязки с помощью поставщика WinNT, имени компьютера и дополнительного параметра, чтобы указать ADSI, что он привязывает к компьютеру: "WinNT:// <computer name> <computer> ".</span><span class="sxs-lookup"><span data-stu-id="9de4f-109">Use the following binding string format using the WinNT provider, computer name, and an extra parameter to instruct ADSI that it is binding to a computer: "WinNT://<computer name>,<computer>".</span></span> <span data-ttu-id="9de4f-110">&lt;Параметр Computer Name &gt; — это имя группы компьютеров для доступа.</span><span class="sxs-lookup"><span data-stu-id="9de4f-110">The "&lt;computer name&gt;" parameter is the name of the computer group to access.</span></span> <span data-ttu-id="9de4f-111">Этот параметр указывает ADSI, что он привязывается к компьютеру, и позволяет средству синтаксического анализа поставщика WinNT пропустить некоторые запросы разрешения неоднозначности, чтобы определить тип объекта, к которому выполняется привязка.</span><span class="sxs-lookup"><span data-stu-id="9de4f-111">This parameter instruct ADSI that it is binding to a computer and allows the WinNT provider's parser to skip some ambiguity-resolution queries to determine what type of object you are binding to.</span></span>
    3.  <span data-ttu-id="9de4f-112">Привязка к интерфейсу [**иадсконтаинер**](/windows/desktop/api/iads/nn-iads-iadscontainer) .</span><span class="sxs-lookup"><span data-stu-id="9de4f-112">Bind to the [**IADsContainer**](/windows/desktop/api/iads/nn-iads-iadscontainer) interface.</span></span>
2.  <span data-ttu-id="9de4f-113">Укажите "Group" в качестве класса с помощью [**иадсконтаинер. Delete**](/windows/desktop/api/iads/nf-iads-iadscontainer-delete), чтобы удалить группу.</span><span class="sxs-lookup"><span data-stu-id="9de4f-113">Specify "group" as the class using [**IADsContainer.Delete**](/windows/desktop/api/iads/nf-iads-iadscontainer-delete)to delete the group.</span></span>

    <span data-ttu-id="9de4f-114">Для фиксации изменений в контейнере не нужно вызывать функцию [**iAds. сетинфо**](/windows/desktop/api/iads/nf-iads-iads-setinfo) .</span><span class="sxs-lookup"><span data-stu-id="9de4f-114">You do not need to call [**IADs.SetInfo**](/windows/desktop/api/iads/nf-iads-iads-setinfo) to commit the change to the container.</span></span> <span data-ttu-id="9de4f-115">Вызов [**иадсконтаинер. Delete**](/windows/desktop/api/iads/nf-iads-iadscontainer-delete) фиксирует удаление группы непосредственно в каталоге.</span><span class="sxs-lookup"><span data-stu-id="9de4f-115">The [**IADsContainer.Delete**](/windows/desktop/api/iads/nf-iads-iadscontainer-delete) call commits the deletion of the group directly to the directory.</span></span>

 

 