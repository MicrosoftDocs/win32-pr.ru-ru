---
description: Протокол LDAP требует, чтобы некоторые символы были экранированы с помощью обратной косой черты ( \) символ при их использовании в протоколе ldap Active Directory Service Interfaces (ADSI).
ms.assetid: bc04359c-4eda-4574-a9c2-f005a1d92dea
ms.tgt_platform: multiple
title: Описание пути ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 51a6f3f28ffa5faa80dbd9f3d7906bba542e47e1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104544839"
---
# <a name="describing-the-adsi-path"></a><span data-ttu-id="f7e2f-103">Описание пути ADSI</span><span class="sxs-lookup"><span data-stu-id="f7e2f-103">Describing the ADSI Path</span></span>

<span data-ttu-id="f7e2f-104">Протокол LDAP требует, чтобы некоторые символы были экранированы с помощью обратной косой черты ( \) символ при их использовании в протоколе ldap Active Directory Service Interfaces (ADSI).</span><span class="sxs-lookup"><span data-stu-id="f7e2f-104">The Lightweight Directory Access Protocol (LDAP) requires that you escape some characters with a backslash (\) character when you use them in an LDAP Active Directory Service Interfaces (ADSI) path.</span></span>

<span data-ttu-id="f7e2f-105">, = +<>\# ; \\ "</span><span class="sxs-lookup"><span data-stu-id="f7e2f-105">,=+<>\#;\\"</span></span>

<span data-ttu-id="f7e2f-106">Escape-символ требуется только для значения свойства **адсипас** .</span><span class="sxs-lookup"><span data-stu-id="f7e2f-106">The escape character is only required for the **ADSIPath** property value.</span></span>

<span data-ttu-id="f7e2f-107">В следующем примере показано, как определить свойство **адсипас** .</span><span class="sxs-lookup"><span data-stu-id="f7e2f-107">The following example shows how to define the **ADSIPath** property.</span></span> <span data-ttu-id="f7e2f-108">Обратите внимание, что \# символ в значении свойства **CN** ABC \# преобразуется в escape-последовательность.</span><span class="sxs-lookup"><span data-stu-id="f7e2f-108">Note that the \# character in the **CN** property value of abc\# is escaped.</span></span>


```C++
// #include <windows.h> for this code to compile

BSTR strObjPath = 
    SysAllocString(L"ds_user.ADSIPath=\"LDAP://CN=abc\#,"
                   L"CN=Users,DC=dsprovider,DC=nttest,"
                   L"DC=microsoft,DC=com\"");

// Use strObjectPath here.

SysFreeString(strObjPath); // Free memory resources.
```



> [!Note]  
> <span data-ttu-id="f7e2f-109">Дополнительные сведения о поддержке и установке этого компонента в определенной операционной системе см. в статье [доступность компонентов WMI в операционной системе](operating-system-availability-of-wmi-components.md).</span><span class="sxs-lookup"><span data-stu-id="f7e2f-109">For more information about support and installation of this component on a specific operating system, see [Operating System Availability of WMI Components](operating-system-availability-of-wmi-components.md).</span></span>

 

 

 



