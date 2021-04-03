---
title: Перечисление пользователей рядовых серверов и Windows 2000 Professional
description: В этом разделе показано, как перечислить всех пользователей в локальной базе данных безопасности на рядовых серверах и компьютерах под управлением Windows 2000 Professional.
ms.assetid: 56c20e8a-2861-4cd9-8058-271c89db7ec9
ms.tgt_platform: multiple
keywords:
- Перечисление пользователей рядовых серверов и Windows 2000 Professional AD
- Пользователи AD, перечисление пользователей на рядовых серверах и Windows 2000 Professional
- Active Directory, использование, пользователи, перечисление пользователей на рядовых серверах и Windows 2000 Professional
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 664af51b7feb2e0b9a683664659eefda11c9cb9d
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/17/2020
ms.locfileid: "103789564"
---
# <a name="enumerating-users-on-member-servers-and-windows-2000-professional"></a><span data-ttu-id="c8771-106">Перечисление пользователей рядовых серверов и Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="c8771-106">Enumerating Users on Member Servers and Windows 2000 Professional</span></span>

<span data-ttu-id="c8771-107">В этом разделе показано, как перечислить всех пользователей в локальной базе данных безопасности на рядовых серверах и компьютерах под управлением Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="c8771-107">This topic shows how to enumerate all users, in a local security database, on member servers and computers running on Windows 2000 Professional.</span></span>

<span data-ttu-id="c8771-108">**Перечисление пользователей**</span><span class="sxs-lookup"><span data-stu-id="c8771-108">**To enumerate the users**</span></span>

1.  <span data-ttu-id="c8771-109">Выполните привязку к компьютеру, используя следующие правила.</span><span class="sxs-lookup"><span data-stu-id="c8771-109">Bind to the computer using the following rules:</span></span>
    1.  <span data-ttu-id="c8771-110">Используйте учетную запись с достаточными правами для доступа к этому компьютеру.</span><span class="sxs-lookup"><span data-stu-id="c8771-110">Use an account that has sufficient rights to access that computer.</span></span>
    2.  <span data-ttu-id="c8771-111">Используйте следующий формат строки привязки с помощью поставщика WinNT, имени компьютера и дополнительного параметра, чтобы указать ADSI, что он привязывает к компьютеру: "WinNT:// <computer name> <computer> ".</span><span class="sxs-lookup"><span data-stu-id="c8771-111">Use the following binding string format using the WinNT provider, computer name, and an extra parameter to instruct ADSI that it is binding to a computer: "WinNT://<computer name>,<computer>".</span></span> <span data-ttu-id="c8771-112">&lt;Параметр Computer Name &gt; — это имя компьютера, к которому имеют доступ группы.</span><span class="sxs-lookup"><span data-stu-id="c8771-112">The "&lt;computer name&gt;" parameter is the name of the computer for whose groups to access.</span></span> <span data-ttu-id="c8771-113">Этот параметр указывает интерфейсу ADSI, что он привязывается к компьютеру, и позволяет средству синтаксического анализа поставщика WinNT пропустить некоторые запросы разрешения неоднозначности, чтобы определить тип объекта, к которому выполняется привязка.</span><span class="sxs-lookup"><span data-stu-id="c8771-113">This parameter instructs ADSI that it is binding to a computer and enables the WinNT provider parser to skip some ambiguity resolution queries to determine what type of object you are binding to.</span></span>
    3.  <span data-ttu-id="c8771-114">Привязка к интерфейсу [**иадсконтаинер**](/windows/desktop/api/iads/nn-iads-iadscontainer) .</span><span class="sxs-lookup"><span data-stu-id="c8771-114">Bind to the [**IADsContainer**](/windows/desktop/api/iads/nn-iads-iadscontainer) interface.</span></span>
2.  <span data-ttu-id="c8771-115">Добавьте "User" в свойство [**иадсконтаинер. Filter**](/windows/desktop/ADSI/iadscontainer-property-methods) .</span><span class="sxs-lookup"><span data-stu-id="c8771-115">Add "user" to the [**IADsContainer.Filter**](/windows/desktop/ADSI/iadscontainer-property-methods) property.</span></span> <span data-ttu-id="c8771-116">Это приводит к тому, что перечисление будет содержать только те объекты, которые имеют класс объектов User.</span><span class="sxs-lookup"><span data-stu-id="c8771-116">This causes the enumeration to only contain objects that have the "user" object class.</span></span>
3.  <span data-ttu-id="c8771-117">Перечисление объектов.</span><span class="sxs-lookup"><span data-stu-id="c8771-117">Enumerate the objects.</span></span> <span data-ttu-id="c8771-118">Для каждого объекта пользователя используйте методы интерфейса [**iAds**](/windows/desktop/api/iads/nn-iads-iads) или [**IADsUser**](/windows/desktop/api/iads/nn-iads-iadsuser) для чтения свойств пользователя.</span><span class="sxs-lookup"><span data-stu-id="c8771-118">For each user object, use the [**IADs**](/windows/desktop/api/iads/nn-iads-iads) or [**IADsUser**](/windows/desktop/api/iads/nn-iads-iadsuser) interface methods to read the user properties.</span></span>

 

 