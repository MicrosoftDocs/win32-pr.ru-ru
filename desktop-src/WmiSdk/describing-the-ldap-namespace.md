---
description: При удаленном подключении к Active Directory серверу, отличному от того, который используется в текущем домене, необходимо указать имя компьютера, который уже является членом домена, принадлежащего нужному Active Directory.
ms.assetid: f1478b9d-4a92-4340-8721-1f443eb6ace2
ms.tgt_platform: multiple
title: Описание пространства имен LDAP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fe1f27c3e2ebc48a0dfa14563822e34bc06d6223
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104081274"
---
# <a name="describing-the-ldap-namespace"></a><span data-ttu-id="e6d94-103">Описание пространства имен LDAP</span><span class="sxs-lookup"><span data-stu-id="e6d94-103">Describing the LDAP Namespace</span></span>

<span data-ttu-id="e6d94-104">При удаленном подключении к Active Directory серверу, отличному от того, который используется в текущем домене, необходимо указать имя компьютера, который уже является членом домена, принадлежащего нужному Active Directory.</span><span class="sxs-lookup"><span data-stu-id="e6d94-104">When connecting remotely to an Active Directory server other than the one in your current domain, you must specify the name of a computer that is already a member of the domain belonging to the Active Directory you want.</span></span>

<span data-ttu-id="e6d94-105">Чтобы удаленно подключиться к компьютеру, который уже является членом домена, принадлежащего серверу Active Directory, введите следующую команду.</span><span class="sxs-lookup"><span data-stu-id="e6d94-105">To remotely connect to a computer that is already a member of the domain belonging to the Active Directory server, type the following command.</span></span>

<span data-ttu-id="e6d94-106">**\\\\\\LDAP корневого \\ каталога ремотекомпутер \\**</span><span class="sxs-lookup"><span data-stu-id="e6d94-106">**\\\\RemoteComputer\\root\\directory\\LDAP**</span></span>

<span data-ttu-id="e6d94-107">В этом примере показано, что состоит из двух частей, составляющих полное имя пространства имен.</span><span class="sxs-lookup"><span data-stu-id="e6d94-107">This example shows that there are two parts that make up a fully qualified namespace name.</span></span> <span data-ttu-id="e6d94-108">Первая часть ( \\ \\ ремотекомпутер) представляет компьютер, который уже является членом домена, принадлежащего нужному серверу Active Directory.</span><span class="sxs-lookup"><span data-stu-id="e6d94-108">The first part (\\\\RemoteComputer) represents the computer that is already a member of the domain belonging to the Active Directory server you want.</span></span> <span data-ttu-id="e6d94-109">Вторая часть ( \\ LDAP корневого \\ каталога \\ ) представляет схему Active Directory в поставщике служб каталогов.</span><span class="sxs-lookup"><span data-stu-id="e6d94-109">The second part (\\root\\directory\\LDAP) represents the Active Directory schema in the Directory Services Provider.</span></span>

> [!Note]  
> <span data-ttu-id="e6d94-110">Дополнительные сведения о поддержке и установке этого компонента в определенной операционной системе см. в статье [доступность компонентов WMI в операционной системе](operating-system-availability-of-wmi-components.md).</span><span class="sxs-lookup"><span data-stu-id="e6d94-110">For more information about support and installation of this component on a specific operating system, see [Operating System Availability of WMI Components](operating-system-availability-of-wmi-components.md).</span></span>

 

 

 



