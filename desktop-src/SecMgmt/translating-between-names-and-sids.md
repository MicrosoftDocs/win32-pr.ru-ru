---
description: Локальный администратор безопасности (LSA) предоставляет функции для преобразования имен пользователей, групп и локальных групп, а также соответствующих значений идентификаторов безопасности (SID).
ms.assetid: 8845b709-a8f9-4d0f-a4a6-86d23d6b01d5
title: Преобразование между именами и идентификаторами безопасности
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d5f67bd95e41a9813522d635e737f4fc528a61aebceeab205a2d40e1f44d7c8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119004812"
---
# <a name="translating-between-names-and-sids"></a>Преобразование между именами и идентификаторами безопасности

[*Локальный администратор безопасности*](/windows/desktop/SecGloss/l-gly) (LSA) предоставляет функции для преобразования имен пользователей, групп и локальных групп, а также соответствующих значений [*идентификаторов безопасности*](/windows/desktop/SecGloss/s-gly) (SID). Чтобы указать имена учетных записей, вызовите функцию [**лсалукупнамес**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsalookupnames) . Эта функция возвращает идентификатор безопасности в виде пары RID или индекса домена. Чтобы получить идентификатор безопасности в виде одного элемента, вызовите функцию [**LsaLookupNames2**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsalookupnames2) . Чтобы узнать идентификаторы SID, вызовите [**лсалукупсидс**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsalookupsids).

Эти функции могут преобразовывать сведения о имени и идентификаторе безопасности из любого домена, которому доверяет локальная система.

Прежде чем можно будет выполнить преобразование между именами учетных записей и идентификаторами безопасности, приложение должно получить обработчик для объекта локальной [**политики**](policy-object.md) , как показано при [открытии обработчика объектов политики](opening-a-policy-object-handle.md).

В следующем примере выполняется поиск идентификатора безопасности для учетной записи с учетом ее имени.


```C++
void GetSIDInformation (LPWSTR AccountName,LSA_HANDLE PolicyHandle)
{
  LSA_UNICODE_STRING lucName;
  PLSA_TRANSLATED_SID ltsTranslatedSID;
  PLSA_REFERENCED_DOMAIN_LIST lrdlDomainList;
  LSA_TRUST_INFORMATION myDomain;
  NTSTATUS ntsResult;
  PWCHAR DomainString = NULL;

  // Initialize an LSA_UNICODE_STRING with the name.
  if (!InitLsaString(&lucName, AccountName))
  {
         wprintf(L"Failed InitLsaString\n");
         return;
  }

  ntsResult = LsaLookupNames(
     PolicyHandle,     // handle to a Policy object
     1,                // number of names to look up
     &lucName,         // pointer to an array of names
     &lrdlDomainList,  // receives domain information
     &ltsTranslatedSID // receives relative SIDs
  );
  if (STATUS_SUCCESS != ntsResult) 
  {
    wprintf(L"Failed LsaLookupNames - %lu \n",
      LsaNtStatusToWinError(ntsResult));
    return;
  }

  // Get the domain the account resides in.
  myDomain = lrdlDomainList->Domains[ltsTranslatedSID->DomainIndex];
  DomainString = (PWCHAR) LocalAlloc(LPTR, myDomain.Name.Length + 1);
  wcsncpy_s(DomainString,
     myDomain.Name.Length + 1, 
     myDomain.Name.Buffer, 
     myDomain.Name.Length);

  // Display the relative Id. 
  wprintf(L"Relative Id is %lu in domain %ws.\n",
    ltsTranslatedSID->RelativeId,
    DomainString);

  LocalFree(DomainString);
  LsaFreeMemory(ltsTranslatedSID);
  LsaFreeMemory(lrdlDomainList);
}
```



В предыдущем примере функция **инитлсастринг** преобразует строку Юникода в структуру [**\_ \_ строки Юникода LSA**](/windows/desktop/api/lsalookup/ns-lsalookup-lsa_unicode_string) . Код для этой функции показан в [использовании строк Юникода в формате LSA](using-lsa-unicode-strings.md).

> [!Note]  
> Эти функции перевода в основном предоставляются для использования редакторами разрешений для вывода сведений [*списка управления доступом*](/windows/desktop/SecGloss/a-gly) (ACL). Редактор разрешений всегда должен вызывать эти функции с помощью объекта [**политики**](policy-object.md) для системы, в которой находятся имя или [*идентификатор безопасности*](/windows/desktop/SecGloss/s-gly) SID. Это гарантирует, что во время перевода будет создана ссылка на соответствующий набор доверенных доменов.

 

Windows Управление доступом также предоставляет функции, выполняющие переводы между идентификаторами безопасности и именами учетных записей: [**LookupAccountName**](/windows/desktop/api/winbase/nf-winbase-lookupaccountnamea) и [**LookupAccountSid**](/windows/desktop/api/winbase/nf-winbase-lookupaccountsida). если приложению требуется найти имя учетной записи или идентификатор безопасности и не использовать дополнительные функции политики lsa, используйте функции управления доступом Windows, а не функции политики lsa. Дополнительные сведения об этих функциях см. в разделе [Access Control](/windows/desktop/SecAuthZ/access-control).

 

 
