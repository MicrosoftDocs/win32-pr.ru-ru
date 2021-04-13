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
# <a name="describing-the-adsi-path"></a>Описание пути ADSI

Протокол LDAP требует, чтобы некоторые символы были экранированы с помощью обратной косой черты ( \) символ при их использовании в протоколе ldap Active Directory Service Interfaces (ADSI).

, = +<>\# ; \\ "

Escape-символ требуется только для значения свойства **адсипас** .

В следующем примере показано, как определить свойство **адсипас** . Обратите внимание, что \# символ в значении свойства **CN** ABC \# преобразуется в escape-последовательность.


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
> Дополнительные сведения о поддержке и установке этого компонента в определенной операционной системе см. в статье [доступность компонентов WMI в операционной системе](operating-system-availability-of-wmi-components.md).

 

 

 



