---
title: Перечисление локальных групп
description: На рядовых серверах и компьютерах под управлением Windows 2000 Professional можно перечислить все локальные группы.
ms.assetid: edbabbe5-13e1-42f6-8e73-f8e18ba4866b
ms.tgt_platform: multiple
keywords:
- Перечисление AD локальных групп
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a6e106fc2517cfedd8fb5fa40e4b99798ee32de8
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/17/2020
ms.locfileid: "103789565"
---
# <a name="enumerating-local-groups"></a><span data-ttu-id="71969-104">Перечисление локальных групп</span><span class="sxs-lookup"><span data-stu-id="71969-104">Enumerating Local Groups</span></span>

<span data-ttu-id="71969-105">На рядовых серверах и компьютерах под управлением Windows 2000 Professional можно перечислить все локальные группы.</span><span class="sxs-lookup"><span data-stu-id="71969-105">On member servers and computers running on Windows 2000 Professional, you can enumerate all local groups.</span></span>

<span data-ttu-id="71969-106">На рядовых серверах и Windows 2000 Professional можно создавать только локальные группы.</span><span class="sxs-lookup"><span data-stu-id="71969-106">Only local groups can be created on member servers and Windows 2000 Professional.</span></span> <span data-ttu-id="71969-107">Однако эти локальные группы могут содержать:</span><span class="sxs-lookup"><span data-stu-id="71969-107">However, those local groups can contain:</span></span>

-   <span data-ttu-id="71969-108">Универсальные и глобальные группы из леса, содержащего домен, членом которого является компьютер.</span><span class="sxs-lookup"><span data-stu-id="71969-108">Universal and Global groups from the forest that contains the domain to which the computer is a member.</span></span>
-   <span data-ttu-id="71969-109">Локальные группы домена из домена этого компьютера.</span><span class="sxs-lookup"><span data-stu-id="71969-109">Domain local groups from that computer's domain.</span></span>
-   <span data-ttu-id="71969-110">Пользователи из любого домена в лесу.</span><span class="sxs-lookup"><span data-stu-id="71969-110">Users from any domain in the forest.</span></span>

<span data-ttu-id="71969-111">**Перечисление локальных групп на рядовом сервере или компьютере с Windows 2000 Professional**</span><span class="sxs-lookup"><span data-stu-id="71969-111">**To enumerate the local groups on a member server or computer running Windows 2000 Professional**</span></span>

1.  <span data-ttu-id="71969-112">Выполните привязку к компьютеру, используя следующие правила.</span><span class="sxs-lookup"><span data-stu-id="71969-112">Bind to the computer using the following rules:</span></span>
    1.  <span data-ttu-id="71969-113">Используйте учетную запись с достаточными правами для доступа к этому компьютеру.</span><span class="sxs-lookup"><span data-stu-id="71969-113">Use an account with sufficient rights to access that computer.</span></span>
    2.  <span data-ttu-id="71969-114">Используйте следующий формат строки привязки с помощью поставщика WinNT, имени компьютера и дополнительного параметра, чтобы указать ADSI, что он привязывает к компьютеру: "WinNT:// <computer name> <computer> ".</span><span class="sxs-lookup"><span data-stu-id="71969-114">Use the following binding string format using the WinNT provider, computer name, and an extra parameter to instruct ADSI that it is binding to a computer: "WinNT://<computer name>,<computer>".</span></span>

        <span data-ttu-id="71969-115"><computer name>Параметр — это имя группы компьютеров для доступа.</span><span class="sxs-lookup"><span data-stu-id="71969-115">"The <computer name>" parameter is the name of the computer group to access.</span></span> <span data-ttu-id="71969-116">Этот параметр указывает ADSI, что он привязывается к компьютеру, и позволяет средству синтаксического анализа поставщика WinNT пропустить некоторые запросы разрешения неоднозначности, чтобы определить тип объекта, к которому выполняется привязка.</span><span class="sxs-lookup"><span data-stu-id="71969-116">This parameter instruct ADSI that it is binding to a computer and allows the WinNT provider's parser to skip some ambiguity-resolution queries to determine what type of object you are binding to.</span></span>

    3.  <span data-ttu-id="71969-117">Привязка к интерфейсу [**иадсконтаинер**](/windows/desktop/api/iads/nn-iads-iadscontainer) .</span><span class="sxs-lookup"><span data-stu-id="71969-117">Bind to the [**IADsContainer**](/windows/desktop/api/iads/nn-iads-iadscontainer) interface.</span></span>

2.  <span data-ttu-id="71969-118">Установите фильтр, содержащий "groups", с помощью свойства [**иадсконтаинер. Filter**](/windows/desktop/api/iads/nn-iads-iadscontainer) .</span><span class="sxs-lookup"><span data-stu-id="71969-118">Set a filter that contains "groups" using the [**IADsContainer.Filter**](/windows/desktop/api/iads/nn-iads-iadscontainer) property.</span></span> <span data-ttu-id="71969-119">Это позволяет перечислить контейнер и получить только группы.</span><span class="sxs-lookup"><span data-stu-id="71969-119">This enables you to enumerate the container and retrieve only groups.</span></span>
3.  <span data-ttu-id="71969-120">Перечислите объекты группы с помощью метода [**иадсконтаинер:: Get \_ \_ NewEnum**](/windows/desktop/api/iads/nf-iads-iadscontainer-get__newenum) .</span><span class="sxs-lookup"><span data-stu-id="71969-120">Enumerate the group objects, using the [**IADsContainer::get\_\_NewEnum**](/windows/desktop/api/iads/nf-iads-iadscontainer-get__newenum) method.</span></span>
4.  <span data-ttu-id="71969-121">Для каждого объекта группы используйте интерфейс [**иадсграуп**](/windows/desktop/api/iads/nn-iads-iadsgroup) для чтения имени и членов группы.</span><span class="sxs-lookup"><span data-stu-id="71969-121">For each the group object, use the [**IADsGroup**](/windows/desktop/api/iads/nn-iads-iadsgroup) interface to read the name and members of the group.</span></span>

 

 