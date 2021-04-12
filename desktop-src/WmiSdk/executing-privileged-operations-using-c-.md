---
description: Специальные клиентские приложения могут вызывать привилегированные операции.
ms.assetid: e09fcadc-282f-4f07-b69c-b15bfdb07a7d
ms.tgt_platform: multiple
title: Выполнение привилегированных операций с помощью C++
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8fbc0468fef7531586020f55032bff94c977c4ac
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104344915"
---
# <a name="executing-privileged-operations-using-c"></a>Выполнение привилегированных операций с помощью C++

Специальные клиентские приложения могут вызывать привилегированные операции. Например, приложение может позволить диспетчеру перезагружать Неотвечающий компьютер с Office. С помощью инструментарий управления Windows (WMI) (WMI) можно выполнить привилегированную операцию, вызвав поставщик WMI для привилегированной операции.

Следующая процедура описывает, как вызвать поставщик для привилегированной операции.

**Вызов поставщика для привилегированной операции**

1.  Получите разрешения на выполнение привилегированной операции для клиентского процесса.

    Как правило, администратор устанавливает разрешения с помощью средств администрирования системы, прежде чем выполнять процесс.

2.  Получите разрешение для процесса поставщика, чтобы включить привилегированную операцию.

    Как правило, разрешения поставщика можно задать с помощью вызова функции [**AdjustTokenPrivileges**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-adjusttokenprivileges) .

3.  Получите разрешение для клиентского процесса, чтобы включить привилегированную операцию.

    Этот шаг необходим только в том случае, если поставщик является локальным для клиента. Если клиент и поставщик существуют на одном компьютере, клиент должен специально включить привилегированную операцию с помощью одного из следующих методов:

    -   Если этот процесс принадлежит клиенту, клиент может использовать [**AdjustTokenPrivileges**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-adjusttokenprivileges) для настройки маркера процесса перед ВЫЗОВом инструментария WMI. В этом случае вам больше не нужно выполнять код.
    -   Если клиенту не удается получить доступ к маркеру клиента, клиент может использовать следующую процедуру, чтобы создать токен потока и использовать [**AdjustTokenPrivileges**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-adjusttokenprivileges) для этого маркера.

В следующей процедуре описывается создание токена потока и использование [**AdjustTokenPrivileges**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-adjusttokenprivileges) для этого маркера.

**Создание токена потока и использование AdjustTokenPrivileges для этого токена**

1.  Создайте копию токена процесса, вызвав [**имперсонатеселф**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-impersonateself).
2.  Получите только что созданный токен потока путем вызова [**GetTokenInformation**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-gettokeninformation).
3.  Включите привилегированную операцию с помощью вызова [**AdjustTokenPrivileges**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-adjusttokenprivileges) для нового маркера.
4.  Получите указатель на [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices).
5.  Маскировка указателя на [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) с помощью вызова [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket).
6.  Повторите шаги с 1 по 5 при каждом вызове инструментария WMI.

    > [!Note]  
    > Необходимо повторить шаги, так как COM кэширует маркеры неправильно.

     

В примере кода в этом разделе \# для правильной компиляции требуется следующая инструкция include.


```C++
#include <wbemidl.h>
```



В следующем примере кода показано, как включить привилегии на локальном компьютере.


```C++
// Get the privileges 
// The token has been obtained outside the scope of this code sample
// ================== 
DWORD dwLen;
bool bRes;
HANDLE hToken;

// obtain dwLen
bRes = GetTokenInformation(
  hToken, 
  TokenPrivileges, 
  NULL, 
  0,
  &dwLen
); 

BYTE* pBuffer = new BYTE[dwLen];
if(pBuffer == NULL)
{
  CloseHandle(hToken);
  return WBEM_E_OUT_OF_MEMORY;
} 

bRes = GetTokenInformation(
  hToken, 
  TokenPrivileges, 
  pBuffer,     
  dwLen,        
  &dwLen
);

if (!bRes)
{
  CloseHandle(hToken);
  delete [] pBuffer;
  return WBEM_E_ACCESS_DENIED;
} 

// Iterate through all the privileges and enable them all
// ====================================================== 
TOKEN_PRIVILEGES* pPrivs = (TOKEN_PRIVILEGES*)pBuffer;
for (DWORD i = 0; i < pPrivs->PrivilegeCount; i++)
{
  pPrivs->Privileges[i].Attributes |= SE_PRIVILEGE_ENABLED;
} 
// Store the information back in the token
// ========================================= 
bRes = AdjustTokenPrivileges(
  hToken, 
  FALSE, 
  pPrivs, 
  0, NULL, NULL
);

delete [] pBuffer;
CloseHandle(hToken); 

if (!bRes)
  return WBEM_E_ACCESS_DENIED;
else
  return WBEM_S_NO_ERROR;
```



 

 
