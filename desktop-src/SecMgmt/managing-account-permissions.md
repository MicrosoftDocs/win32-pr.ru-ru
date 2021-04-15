---
description: LSA предоставляет несколько функций, которые могут вызываться приложениями для перечисления или установки привилегий для учетных записей пользователей, групп и локальных групп.
ms.assetid: c28c03f0-4638-42ed-8dad-1e934cf99273
title: Управление разрешениями учетной записи
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d4dc22a4088986abbdaa98d8cdde43415af84905
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104497193"
---
# <a name="managing-account-permissions"></a>Управление разрешениями учетной записи

LSA предоставляет несколько функций, которые могут вызываться приложениями для перечисления или установки [*привилегий*](/windows/desktop/SecGloss/p-gly) для учетных записей пользователей, групп и локальных групп.

Прежде чем можно будет управлять сведениями об учетной записи, приложение должно получить обработчик для объекта локальной [**политики**](policy-object.md) , как показано при [открытии обработчика объектов политики](opening-a-policy-object-handle.md). Кроме того, чтобы перечислить или изменить разрешения для учетной записи, необходимо иметь [*идентификатор безопасности*](/windows/desktop/SecGloss/s-gly) (SID) для этой учетной записи. Приложение может располагать идентификатор безопасности, используя имя учетной записи, как описано в разделе [Преобразование имен в идентификаторы безопасности и](translating-between-names-and-sids.md)т. д.

Чтобы получить доступ ко всем учетным записям с определенным разрешением, вызовите [**лсаенумератеаккаунтсвисусерригхт**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsaenumerateaccountswithuserright). Эта функция заполняет массив идентификаторами безопасности всех учетных записей, имеющих указанное разрешение.

После получения идентификатора безопасности учетной записи можно изменить ее разрешения. Вызовите [**лсааддаккаунтригхтс**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsaaddaccountrights) , чтобы добавить разрешения для учетной записи. Если указанная учетная запись не существует, **лсааддаккаунтригхтс** ее создает. Чтобы удалить разрешения из учетной записи, вызовите [**лсаремовеаккаунтригхтс**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsaremoveaccountrights). Если удалить все разрешения из учетной записи, **лсаремовеаккаунтригхтс** также удалит учетную запись.

Приложение может проверить разрешения, назначенные учетной записи в данный момент, вызвав [**лсаенумератеаккаунтригхтс**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsaenumerateaccountrights). Эта функция заполняет массив [**строковых структур Юникода в \_ формате \_ LSA**](/windows/desktop/api/lsalookup/ns-lsalookup-lsa_unicode_string) . Каждая структура содержит имя привилегии, удерживаемой указанной учетной записью.

В следующем примере к учетной записи добавляется разрешение SeServiceLogonRight. В этом примере переменная AccountSID указывает идентификатор безопасности учетной записи. Дополнительные сведения о поиске SID учетной записи см. в разделе [Преобразование имен и идентификаторов безопасности](translating-between-names-and-sids.md).


```C++
#include <windows.h>
#include <ntsecapi.h>

void AddPrivileges(PSID AccountSID, LSA_HANDLE PolicyHandle)
{
  LSA_UNICODE_STRING lucPrivilege;
  NTSTATUS ntsResult;

  // Create an LSA_UNICODE_STRING for the privilege names.
  if (!InitLsaString(&lucPrivilege, L"SeServiceLogonRight"))
  {
         wprintf(L"Failed InitLsaString\n");
         return;
  }

  ntsResult = LsaAddAccountRights(
    PolicyHandle,  // An open policy handle.
    AccountSID,    // The target SID.
    &lucPrivilege, // The privileges.
    1              // Number of privileges.
  );                
  if (ntsResult == STATUS_SUCCESS) 
  {
    wprintf(L"Privilege added.\n");
  }
  else
  {
    wprintf(L"Privilege was not added - %lu \n",
      LsaNtStatusToWinError(ntsResult));
  }
} 
```



В предыдущем примере функция Инитлсастринг преобразует строку [*Юникода*](/windows/desktop/SecGloss/u-gly) в структуру [**\_ \_ строки Юникода LSA**](/windows/desktop/api/lsalookup/ns-lsalookup-lsa_unicode_string) . Код для этой функции показан в [использовании строк Юникода в формате LSA](using-lsa-unicode-strings.md).

 

 
