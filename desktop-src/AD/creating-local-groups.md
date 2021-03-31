---
title: Создание локальных групп
description: Для рядовых серверов и Windows 2000 Professional можно создавать только локальные группы.
ms.assetid: 76cbac51-d8ba-4114-9951-060273be52f3
ms.tgt_platform: multiple
keywords:
- Создание локальных групп AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 705902b0066913fcd6eed56ba7c74e299144595f
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/17/2020
ms.locfileid: "104336812"
---
# <a name="creating-local-groups"></a><span data-ttu-id="37411-104">Создание локальных групп</span><span class="sxs-lookup"><span data-stu-id="37411-104">Creating Local Groups</span></span>

<span data-ttu-id="37411-105">Для рядовых серверов и Windows 2000 Professional можно создавать только локальные группы.</span><span class="sxs-lookup"><span data-stu-id="37411-105">Only local groups can be created for member servers and Windows 2000 Professional.</span></span>

<span data-ttu-id="37411-106">**Создание локальной группы для рядового сервера или компьютера с Windows 2000 Professional**</span><span class="sxs-lookup"><span data-stu-id="37411-106">**To create a local group for a member server or computer running Windows 2000 Professional**</span></span>

1.  <span data-ttu-id="37411-107">Выполните привязку к компьютеру, используя следующие правила.</span><span class="sxs-lookup"><span data-stu-id="37411-107">Bind to the computer using the following rules:</span></span>
    1.  <span data-ttu-id="37411-108">Используйте учетную запись с достаточными правами для доступа к этому компьютеру.</span><span class="sxs-lookup"><span data-stu-id="37411-108">Use an account with sufficient rights to access that computer.</span></span>
    2.  <span data-ttu-id="37411-109">Используйте следующий формат строки привязки с помощью поставщика WinNT, имени компьютера и дополнительного параметра, чтобы указать ADSI, что он привязывает к компьютеру: "WinNT:// <computer name> <computer> ".</span><span class="sxs-lookup"><span data-stu-id="37411-109">Use the following binding string format using the WinNT provider, computer name, and an extra parameter to instruct ADSI that it is binding to a computer: "WinNT://<computer name>,<computer>".</span></span>

        <span data-ttu-id="37411-110">&lt;Параметр Computer Name &gt; — это имя групп компьютеров для доступа.</span><span class="sxs-lookup"><span data-stu-id="37411-110">The "&lt;computer name&gt;" parameter is the name of the computer groups to access.</span></span>

        <span data-ttu-id="37411-111">В строке привязки &lt; &gt; параметр Computer указывает интерфейсу ADSI, что он привязывается к компьютеру.</span><span class="sxs-lookup"><span data-stu-id="37411-111">In the binding string, the "&lt;computer&gt;" parameter instructs ADSI that it is binding to a computer.</span></span> <span data-ttu-id="37411-112">ADSI делает эти данные доступными средству синтаксического анализа поставщика WinNT, чтобы можно было пропустить некоторые запросы на разрешение неоднозначности, чтобы определить тип объекта, к которому выполняется привязка.</span><span class="sxs-lookup"><span data-stu-id="37411-112">ADSI makes this data available to the WinNT provider's parser so that it can skip some ambiguity-resolution queries to determine what type of object you are binding to.</span></span>

    3.  <span data-ttu-id="37411-113">Привязка к интерфейсу [**иадсконтаинер**](/windows/desktop/api/iads/nn-iads-iadscontainer) .</span><span class="sxs-lookup"><span data-stu-id="37411-113">Bind to the [**IADsContainer**](/windows/desktop/api/iads/nn-iads-iadscontainer) interface.</span></span>

2.  <span data-ttu-id="37411-114">Укажите "localGroup" в качестве класса с помощью [**иадсконтаинер. Create**](/windows/desktop/api/iads/nf-iads-iadscontainer-create) , чтобы добавить группу.</span><span class="sxs-lookup"><span data-stu-id="37411-114">Specify "localGroup" as the class using [**IADsContainer.Create**](/windows/desktop/api/iads/nf-iads-iadscontainer-create) to add the group.</span></span>
    > [!Note]  
    > <span data-ttu-id="37411-115">Если указать "Group" в качестве класса, ADSI использует "localGroup".</span><span class="sxs-lookup"><span data-stu-id="37411-115">If you specify "group" as the class, ADSI uses "localGroup".</span></span> <span data-ttu-id="37411-116">Не указывайте класс как "Глобалграуп".</span><span class="sxs-lookup"><span data-stu-id="37411-116">Do not specify the class as "globalGroup".</span></span> <span data-ttu-id="37411-117">Группы класса "Глобалграуп" нельзя создавать на рядовых серверах или на компьютере под управлением Windows NT Workstation или Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="37411-117">Groups of class "globalGroup" cannot be created on member servers or a computer running Windows NT Workstation/Windows 2000 Professional.</span></span> <span data-ttu-id="37411-118">Если указать "Глобалграуп", [**иадсконтаинер. Create**](/windows/desktop/api/iads/nf-iads-iadscontainer-create) создает группу в кэше свойств, но параметр [**iAds. сетинфо**](/windows/desktop/api/iads/nf-iads-iads-setinfo) не записывает группу в базу данных безопасности и не возвращает ошибку.</span><span class="sxs-lookup"><span data-stu-id="37411-118">If you specify "globalGroup", [**IADsContainer.Create**](/windows/desktop/api/iads/nf-iads-iadscontainer-create) creates the group in the property cache, but [**IADs.SetInfo**](/windows/desktop/api/iads/nf-iads-iads-setinfo) does not write the group to the security database and it does not return an error.</span></span>

     

3.  <span data-ttu-id="37411-119">Запишите группу в базу данных безопасности компьютера с помощью метода [**iAds. сетинфо**](/windows/desktop/api/iads/nf-iads-iads-setinfo).</span><span class="sxs-lookup"><span data-stu-id="37411-119">Write the group to the computer security database using [**IADs.SetInfo**](/windows/desktop/api/iads/nf-iads-iads-setinfo).</span></span>

 

 