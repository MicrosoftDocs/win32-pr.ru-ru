---
title: Создание пользователей на рядовых серверах и Windows 2000 Professional
description: В этом разделе описаны действия по созданию пользователя на рядовом сервере или компьютере с Windows 2000 Professional.
ms.assetid: 714a36d4-3407-426f-b4e9-27ec399f742a
ms.tgt_platform: multiple
keywords:
- Создание пользователей на рядовых серверах и Windows 2000 Professional AD
- Пользователи AD, создание пользователя на рядовых серверах и Windows 2000 Professional
- Active Directory, использование, пользователи, создание пользователя на рядовых серверах и Windows 2000 Professional
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3050c9e8ecf68465097f2c185d2d31e0195c25a6
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/17/2020
ms.locfileid: "104069792"
---
# <a name="creating-users-on-member-servers-and-windows-2000-professional"></a><span data-ttu-id="e23be-106">Создание пользователей на рядовых серверах и Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="e23be-106">Creating Users on Member Servers and Windows 2000 Professional</span></span>

<span data-ttu-id="e23be-107">**Создание пользователя**</span><span class="sxs-lookup"><span data-stu-id="e23be-107">**To create a user**</span></span>

1.  <span data-ttu-id="e23be-108">Выполните привязку к компьютеру, используя следующие правила.</span><span class="sxs-lookup"><span data-stu-id="e23be-108">Bind to the computer using the following rules:</span></span>
    1.  <span data-ttu-id="e23be-109">Используйте учетную запись с достаточными правами для доступа к этому компьютеру.</span><span class="sxs-lookup"><span data-stu-id="e23be-109">Use an account that has sufficient rights to access that computer.</span></span>
    2.  <span data-ttu-id="e23be-110">Используйте следующий формат строки привязки с помощью поставщика WinNT, имени компьютера и дополнительного параметра, чтобы указать ADSI, что он привязывает к компьютеру: "WinNT:// <computer name> <computer> ".</span><span class="sxs-lookup"><span data-stu-id="e23be-110">Use the following binding string format using the WinNT provider, computer name, and an extra parameter to tell ADSI that it is binding to a computer: "WinNT://<computer name>,<computer>".</span></span> <span data-ttu-id="e23be-111">Компьютер " &lt; имя компьютера &gt; " — это имя компьютера, к которому нужно получить доступ.</span><span class="sxs-lookup"><span data-stu-id="e23be-111">The "&lt;computer name&gt;" computer is the name of the computer whose groups you want to access.</span></span> <span data-ttu-id="e23be-112">Этот параметр указывает интерфейсу ADSI, что он привязывается к компьютеру, и позволяет средству синтаксического анализа поставщика WinNT пропустить некоторые запросы разрешения неоднозначности, чтобы определить тип объекта, к которому выполняется привязка.</span><span class="sxs-lookup"><span data-stu-id="e23be-112">This parameter tells ADSI that it is binding to a computer and allows the WinNT provider's parser to skip some ambiguity resolution queries to determine what type of object you are binding to.</span></span>
    3.  <span data-ttu-id="e23be-113">Привязка к интерфейсу [**иадсконтаинер**](/windows/desktop/api/iads/nn-iads-iadscontainer) .</span><span class="sxs-lookup"><span data-stu-id="e23be-113">Bind to the [**IADsContainer**](/windows/desktop/api/iads/nn-iads-iadscontainer) interface.</span></span>
2.  <span data-ttu-id="e23be-114">Укажите "User" в качестве класса с помощью [**иадсконтаинер. Create**](/windows/desktop/api/iads/nf-iads-iadscontainer-create) , чтобы добавить пользователя.</span><span class="sxs-lookup"><span data-stu-id="e23be-114">Specify "user" as the class using [**IADsContainer.Create**](/windows/desktop/api/iads/nf-iads-iadscontainer-create) to add the user.</span></span>
3.  <span data-ttu-id="e23be-115">Запишите пользователя в базу данных безопасности компьютера с помощью метода [**iAds. сетинфо**](/windows/desktop/api/iads/nf-iads-iads-setinfo).</span><span class="sxs-lookup"><span data-stu-id="e23be-115">Write the user to the computer's security database using [**IADs.SetInfo**](/windows/desktop/api/iads/nf-iads-iads-setinfo).</span></span>

 

 