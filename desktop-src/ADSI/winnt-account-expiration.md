---
title: Истечение срока действия учетной записи (поставщик WinNT)
description: При использовании поставщика WinNT Дата истечения срока действия учетной записи может быть задана с помощью свойства IADsUser. Аккаунтекспиратиондате.
ms.assetid: 1d887a33-a3ae-4c61-88fa-2764a6bbf6bf
ms.tgt_platform: multiple
keywords:
- Истечение срока действия учетной записи ADSI, поставщик WinNT
- Службы WinNT Provider ADSI, примеры управления пользователями, истечение срока действия учетной записи
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4936004cbd68c853f5e6d5c76a405f2a8340d22a
ms.sourcegitcommit: 6515eef99ca0d1bbe3e27d4575e9986f5255f277
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/10/2021
ms.locfileid: "105656817"
---
# <a name="account-expiration-winnt-provider"></a>Истечение срока действия учетной записи (поставщик WinNT)

При использовании поставщика WinNT Дата истечения срока действия учетной записи может быть задана с помощью свойства [**IADsUser. аккаунтекспиратиондате**](iadsuser-property-methods.md) .

Чтобы задать дату окончания срока действия учетной записи, задайте для свойства [**IADsUser. аккаунтекспиратиондате**](iadsuser-property-methods.md) требуемое значение даты. Чтобы задать срок действия учетной записи без ограничения срока действия, присвойте этому свойству значение "1 января 1970".

## <a name="example-1"></a>Пример 1

В следующем примере кода показано, как задать дату истечения срока действия учетной записи с помощью Visual Basic с ADSI.


```VB
Dim usr As IADsUser

Set usr = GetObject("WinNT://Fabrikam/JeffSmith")
usr.AccountExpirationDate = "05/06/1998"
usr.SetInfo
 
' Set the account to never expire.
usr.AccountExpirationDate = "01/01/1970"
usr.SetInfo
```



## <a name="example-2"></a>Пример 2

В следующем примере кода показано, как задать дату истечения срока действия учетной записи с помощью C++ и ADSI.


```C++
void SetUserAccountExpirationDate(IADsUser *pUser, DATE date)
{
   if(!pUser) return;

   HRESULT hr = S_OK;
   hr = pUser->put_AccountExpirationDate(date); // Set the account to expires on date.
   
   hr = pUser->SetInfo();
   hr = pUser->Release();
   return;
}
```



 

 




