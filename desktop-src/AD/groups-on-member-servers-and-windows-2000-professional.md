---
title: Группы на рядовых серверах и Windows 2000 Professional
description: На рядовых серверах и компьютерах под управлением Windows 2000 Professional имеется локальная база данных безопасности.
ms.assetid: 17a651e2-3650-4e12-b17e-badd3d479515
ms.tgt_platform: multiple
keywords:
- Группы на рядовых серверах и Windows 2000 Professional AD
- группы AD, группы на рядовых серверах и Windows 2000 Professional
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 530da03182d05764540a85f1c2529ced5877be5a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104328483"
---
# <a name="groups-on-member-servers-and-windows-2000-professional"></a><span data-ttu-id="318ea-105">Группы на рядовых серверах и Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="318ea-105">Groups on Member Servers and Windows 2000 Professional</span></span>

<span data-ttu-id="318ea-106">На рядовых серверах и компьютерах под управлением Windows 2000 Professional имеется локальная база данных безопасности.</span><span class="sxs-lookup"><span data-stu-id="318ea-106">On member servers and computers running on Windows 2000 Professional, there is a local security database.</span></span> <span data-ttu-id="318ea-107">Эта локальная база данных безопасности может содержать собственные локальные пользователи и локальные группы, областью действия которых является только конкретный компьютер, на котором они созданы.</span><span class="sxs-lookup"><span data-stu-id="318ea-107">This local security database can contain its own local user and local groups whose scope is only the particular computer where they are created.</span></span> <span data-ttu-id="318ea-108">При управлении этими типами пользователей и групп на рядовых серверах и компьютерах под управлением Windows NT Workstation или Windows 2000 Professional используйте поставщик WinNT.</span><span class="sxs-lookup"><span data-stu-id="318ea-108">When managing these types of users and groups on member servers and computers running on Windows NT Workstation or Windows 2000 Professional, use the WinNT provider.</span></span>

<span data-ttu-id="318ea-109">Если рядовой сервер или компьютер, работающий под Windows 2000 Professional или Windows 2000 Professional, является членом домена Windows 2000, группы или пользователи в домене можно использовать в локальной базе данных безопасности для предоставления прав на эту группу на этом конкретном компьютере.</span><span class="sxs-lookup"><span data-stu-id="318ea-109">When a member server or a computer running on Windows 2000 Professional or Windows 2000 Professional is a member of a Windows 2000 domain, the groups or users in the domain can be used in the local security database to grant rights to that group on that particular computer.</span></span>

<span data-ttu-id="318ea-110">При управлении группами в домене Windows 2000 с помощью ADSI используйте поставщик LDAP.</span><span class="sxs-lookup"><span data-stu-id="318ea-110">When managing groups on a Windows 2000 domain using ADSI, use the LDAP provider.</span></span> <span data-ttu-id="318ea-111">При управлении группами на рядовых серверах и компьютерах под управлением Windows NT Workstation или Windows 2000 Professional используйте поставщик WinNT.</span><span class="sxs-lookup"><span data-stu-id="318ea-111">When managing groups on member servers and computers running on Windows NT Workstation or Windows 2000 Professional, use the WinNT provider.</span></span>

<span data-ttu-id="318ea-112">Необходимо выполнить привязку, по крайней мере, по одному экземпляру к каждому поставщику: 1) выполните привязку к поставщику LDAP, чтобы получить путь к группе или пользователю, который требуется добавить в группу в локальной базе данных, и 2) привяжите к поставщику WinNT, чтобы добавить этого пользователя или группу в локальную группу.</span><span class="sxs-lookup"><span data-stu-id="318ea-112">You must bind, at least one instance, to each provider: 1) Bind to the LDAP provider to retrieve the ADsPath to the group or user you want to add to a group in the local database and 2) Bind to the WinNT provider to add that user or group to a local group.</span></span>

 

 




