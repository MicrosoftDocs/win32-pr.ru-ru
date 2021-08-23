---
title: Создание пользователей с помощью поставщика LDAP ADSI
description: С помощью поставщика LDAP ADSI можно создать только глобальную учетную запись пользователя.
ms.assetid: f99f85a8-9ced-4006-b95b-bd5671ba4c60
ms.tgt_platform: multiple
keywords:
- ADSI поставщика LDAP, объект User, создание пользователей
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d32d076805b9480ed0344712f7b023efab4ef0a025f367cc9c5ebb0bb7dfc0e3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119023072"
---
# <a name="user-creation-with-the-adsi-ldap-provider"></a>Создание пользователей с помощью поставщика LDAP ADSI

С помощью поставщика LDAP ADSI можно создать только глобальную учетную запись пользователя. Локальные учетные записи находятся в базе данных SAM и должны создаваться с помощью поставщика WinNT. Дополнительные сведения о создании объекта пользователя с помощью поставщика WinNT см. в разделе [объект пользователя WinNT](winnt-user-object.md).

**Создание объекта User**

1.  Выполните привязку к контейнеру, где будет располагаться объект пользователя, и получите для контейнера интерфейс [**иадсконтаинер**](/windows/desktop/api/Iads/nn-iads-iadscontainer) или [**идиректорйобжект**](/windows/desktop/api/Iads/nn-iads-idirectoryobject) .
2.  Чтобы создать объект пользователя, используйте метод [**иадсконтаинер. Create**](/windows/desktop/api/Iads/nf-iads-iadscontainer-create) или [**Идиректорйобжект:: креатедсобжект**](/windows/desktop/api/Iads/nf-iads-idirectoryobject-createdsobject) .
3.  Минимальные атрибуты, необходимые для создания объекта пользователя, зависят от используемой службы каталогов. Дополнительные сведения о создании Active Directory пользователя см. в разделе [Создание пользователя](/windows/desktop/AD/creating-a-user).
4.  Если используется интерфейс [**иадсконтаинер**](/windows/desktop/api/Iads/nn-iads-iadscontainer) , новый объект фактически не создается, пока не будет вызван метод [**iAds. сетинфо**](/windows/desktop/api/Iads/nf-iads-iads-setinfo) .

    Если используется интерфейс [**идиректорйобжект**](/windows/desktop/api/Iads/nn-iads-idirectoryobject) , то новый объект создается при вызове метода [**креатедсобжект**](/windows/desktop/api/Iads/nf-iads-idirectoryobject-createdsobject) . Минимальные атрибуты, включая [**objectClass**](/windows/desktop/ADSchema/a-objectclass), должны быть указаны в массиве [**\_ \_ сведений attr ADS**](/windows/desktop/api/Iads/ns-iads-ads_attr_info) , переданном в метод **креатедсобжект** .

## <a name="example-1"></a>Пример 1

В следующем примере кода создается учетная запись пользователя с атрибутами по умолчанию.


```VB
Dim ou As IADs
Dim usr as IADsUser

On Error GoTo Cleanup

Set ou = GetObject("LDAP://OU=Finance,DC=Fabrikam,DC=COM")
Set usr = ou.Create("user", "cn=Jeff Smith")
usr.Put "samAccountName", "jeffsmith"
usr.SetInfo

Cleanup:
   If (Err.Number <> 0) Then
      MsgBox ("An error has occurred. " &  Err.Number)
   End If
   Set ou = Nothing
   Set usr = Nothing
```



## <a name="example-2"></a>Пример 2

В следующем примере кода создается учетная запись пользователя с атрибутами по умолчанию. Для краткости проверка ошибок пропущена.


```C++
#include <activeds.h>

int main()
{
   HRESULT hr = CoInitialize(NULL);

   IADsContainer *pCont;
   IADsUser *pUser;

   LPWSTR adsPath = L"LDAP://serv1/CN=Users,dc=Fabrikam,dc=com";
   LPWSTR usrPass = NULL;
   LPWSTR usrName = NULL;

   // Add code to securely get the user name and password or leave
   // as NULL to use the current security context.

   hr = ADsOpenObject(adsPath, 
                      usrName,
                      usrPass,
                      ADS_SECURE_AUTHENTICATION,
                      IID_IADsContainer,
                      (void**)&pCont);

   IDispatch *pDisp;
   hr = pCont->Create(CComBSTR("user"), CComBSTR("cn=Jeff Smith"), &pDisp);
   pCont->Release();

   hr = pDisp->QueryInterface(IID_IADsUser,(void**)&pUser);
   pDisp->Release();

   VARIANT var;
   VariantInit(&var);
   V_BSTR(&var) = L"jeffsmith";
   V_VT(&var)=VT_BSTR;
   hr = pUser->Put(CComBSTR("samAccountName"), var);

   hr = pUser->SetInfo();

   VariantClear(&var);
   pUser->Release();

   CoUninitialize();

   return 0;
}
```



 

 