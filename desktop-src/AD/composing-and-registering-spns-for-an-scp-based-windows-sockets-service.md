---
title: Составление и регистрация имен участников-служб для службы сокетов Windows на основе SCP
description: В следующем примере кода показано, как создать и зарегистрировать имена участников-служб для службы. Вызовите этот код из установщика службы после вызова CreateService и создания точки подключения службы (SCP) службы.
ms.assetid: 3957af10-974a-415f-b8fb-d9b52ac5a82d
ms.tgt_platform: multiple
keywords:
- имена субъектов-служб AD, составление и регистрация имен участников-служб для службы сокетов Windows на основе SCP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d754d51c0ad34b1623bdc84fc8178b04d33515ed
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/17/2020
ms.locfileid: "103789613"
---
# <a name="composing-and-registering-spns-for-scp-based-windows-sockets-service"></a>Составление и регистрация имен участников-служб для службы сокетов Windows на основе SCP

В следующем примере кода показано, как создать и зарегистрировать имена участников-служб для службы. Вызовите этот код из установщика службы после вызова [**CreateService**](/windows/desktop/api/winsvc/nf-winsvc-createservicea) и создания точки подключения службы (SCP) службы.

В следующем примере кода вызываются примеры функций **спнкомпосе** и **спнрегистер** , которые создают и регистрируют имя участника-службы. Дополнительные сведения и исходный код **спнкомпосе** см. в разделе [составление имен участников-служб для службы с SCP](composing-the-spns-for-a-service-with-an-scp.md). Дополнительные сведения и исходный код **спнрегистер** см. в разделе [Регистрация имен участников-служб для службы](registering-the-spns-for-a-service.md).

В этом примере для создания имени субъекта-службы используется имя класса службы и различающееся имя его SCP. Дополнительные сведения и пример кода, демонстрирующий привязку клиента к SCP службы для получения этих строк имен, см. в разделе [как клиенты находят и используют точку подключения службы](how-clients-find-and-use-a-service-connection-point.md). Имейте в виду, что код для создания имени участника-службы зависит от типа службы и механизмов, используемых для публикации службы.

Служба регистрирует свое имя участника-службы, сохраняя ее **в атрибуте** «перечислить» объекта учетной записи службы в каталоге. Если служба выполняется под учетной записью LocalSystem, а не под учетной записью службы, она регистрирует свое имя участника-службы в объекте учетной записи локального компьютера в каталоге.


```C++
TCHAR szDNofSCP[MAX_PATH]; // DN of SCP. Initialize by querying SCP.
TCHAR szServiceClass[]=TEXT("ADSockAuth");
LPCTSTR szServiceAccountDN;   // DN of a service logon account. 
 
DWORD dwStatus;
TCHAR **pspn = NULL;
ULONG ulSpn = 1;
 
// Compose the SPNs.
dwStatus = SpnCompose(
        &pspn,              // Receives pointer to the SPN array.
        &ulSpn,             // Receives number of SPNs returned.
        szDNofSCP,          // Input: DN of the SCP.
        szServiceClass);    // Input: the service class string.
 
// Register the SPNs
if (dwStatus == NO_ERROR) 
    dwStatus = SpnRegister(
       szServiceAccountDN,  // Logon account to register SPNs on
       pspn,                // Array of SPNs
       ulSpn,               // Number of SPNs in array
       DS_SPN_ADD_SPN_OP);  // Add SPNs to the account
 
// Free the array of SPNs returned by SpnCompose.
DsFreeSpnArray(ulSpn, pspn); 
```



Аналогичный код можно использовать для отмены регистрации имен участников-служб при удалении службы. Укажите имя **субъекта-службы DS \_ \_ DELETE \_ SPN \_** вместо имени субъекта-службы **DS \_ \_ Add \_ SPN \_**.

 

 