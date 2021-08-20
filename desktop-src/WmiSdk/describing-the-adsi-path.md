---
description: Протокол LDAP требует, чтобы некоторые символы были экранированы с помощью обратной косой черты ( \) символ при их использовании в протоколе ldap Active Directory Service Interfaces (ADSI).
ms.assetid: bc04359c-4eda-4574-a9c2-f005a1d92dea
ms.tgt_platform: multiple
title: Описание пути ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 15c320d20d8f7f9b16e760535a2017389a2a7984440ba4d0819ba2bada0e912e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117925075"
---
# <a name="describing-the-adsi-path"></a>Описание пути ADSI

Протокол LDAP требует, чтобы некоторые символы были экранированы символом обратной косой черты ( \\ ) при их использовании в пути к интерфейсу ldap Active Directory Service Interfaces (ADSI).

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

 

 

 



