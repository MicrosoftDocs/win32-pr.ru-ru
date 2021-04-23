---
description: При вызове поставщика Active Directory через инструментарий WMI вы предоставляете пути к пространству имен LDAP и интерфейсу Active Directory служб (ADSI).
ms.assetid: 55733fba-2170-4400-a516-896f6bf9525a
ms.tgt_platform: multiple
title: Использование правильного синтаксиса Active Directory
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 33e321d6919c48103be930226cf11c4b3e82dcc9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105701933"
---
# <a name="using-the-proper-active-directory-syntax"></a><span data-ttu-id="1b014-103">Использование правильного синтаксиса Active Directory</span><span class="sxs-lookup"><span data-stu-id="1b014-103">Using the Proper Active Directory Syntax</span></span>

<span data-ttu-id="1b014-104">При вызове [поставщика Active Directory](/previous-versions/windows/desktop/dsprov/active-directory-provider) через инструментарий WMI вы предоставляете пути к пространству имен LDAP и интерфейсу Active Directory служб (ADSI).</span><span class="sxs-lookup"><span data-stu-id="1b014-104">You supply the Lightweight Directory Access Protocol (LDAP) namespace and Active Directory Services Interface (ADSI) paths when calling the [Active Directory Provider](/previous-versions/windows/desktop/dsprov/active-directory-provider) through WMI.</span></span>

<span data-ttu-id="1b014-105">В следующих разделах описывается пространство имен LDAP и путь ADSI:</span><span class="sxs-lookup"><span data-stu-id="1b014-105">The following topics describe the LDAP namespace and the ADSI path:</span></span>

-   [<span data-ttu-id="1b014-106">Описание пространства имен LDAP</span><span class="sxs-lookup"><span data-stu-id="1b014-106">Describing the LDAP Namespace</span></span>](describing-the-ldap-namespace.md)

    <span data-ttu-id="1b014-107">Путь к пространству имен описывает расположение удаленного пространства имен.</span><span class="sxs-lookup"><span data-stu-id="1b014-107">A namespace path describes the location of a remote namespace.</span></span> <span data-ttu-id="1b014-108">Используйте путь к пространству имен для удаленного подключения к пространству имен Active Directory.</span><span class="sxs-lookup"><span data-stu-id="1b014-108">Use the namespace path to connect remotely to an Active Directory namespace.</span></span>

-   [<span data-ttu-id="1b014-109">Описание пути ADSI</span><span class="sxs-lookup"><span data-stu-id="1b014-109">Describing the ADSI Path</span></span>](describing-the-adsi-path.md)

    <span data-ttu-id="1b014-110">Путь ADSI описывает расположение объекта с помощью API интерфейса ADSI.</span><span class="sxs-lookup"><span data-stu-id="1b014-110">The ADSI path describes the location of an object using the ADSI API.</span></span> <span data-ttu-id="1b014-111">Используйте путь ADSI в параметрах, передаваемый поставщиком в Active Directory.</span><span class="sxs-lookup"><span data-stu-id="1b014-111">Use the ADSI path in parameters that the provider passes onto Active Directory.</span></span>

> [!Note]  
> <span data-ttu-id="1b014-112">Дополнительные сведения о поддержке и установке этого компонента в определенной операционной системе см. в статье [доступность компонентов WMI в операционной системе](operating-system-availability-of-wmi-components.md).</span><span class="sxs-lookup"><span data-stu-id="1b014-112">For more information about support and installation of this component on a specific operating system, see [Operating System Availability of WMI Components](operating-system-availability-of-wmi-components.md).</span></span>

 

 

 
