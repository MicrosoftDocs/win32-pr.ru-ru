---
title: Поддержка раннего связывания
description: В следующем примере кода представлен сценарий с поддержкой раннего связывания на месте.
ms.assetid: 3ca955cc-a9cd-4309-8617-89fe50b65c3d
ms.tgt_platform: multiple
keywords:
- расширения ADSI, поддержка раннего связывания
- Привязка AD, поддержка раннего связывания
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: be6980edb0395ad0139f9cf2e4a1f9cde3ff6077
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/21/2020
ms.locfileid: "104134574"
---
# <a name="early-binding-support"></a>Поддержка раннего связывания

В следующем примере кода представлен сценарий с поддержкой раннего связывания на месте.


```VB
Dim x as IADsUser
Dim y as IADsExt1
Dim z as IADsExt2
 
Set x = GetObject("LDAP://CN=JeffSmith, OU=Sales, 
                   DC=Fabrikam,DC=COM")
x.SetPassword("newPassword")
 
Set y = x
y.MyNewMethod( "\\srv\public")
y.MyProperty = "Hello World"
 
Set z = y
z.OtherMethod()
z.OtherProperty = 4362
 
Debug.Print x.LastName
 
Set z = GetObject("LDAP://CN=Jeff,OU=Engr, 
                   DC=Fabrikam,DC=COM")
z.OtherProperty = 5323
```



В этом примере кода два компонента расширения расширяют объект **пользователя** . Каждое расширение публикует свой собственный интерфейс. Каждое расширение не распознает другой интерфейс расширения; только интерфейсы ADSI распознают существование обоих расширений. Каждое расширение делегирует свой [**IUnknown интерфейсу**](/windows/win32/api/unknwn/nn-unknwn-iunknown) ADSI. ADSI выступает в качестве агрегатора для обоих расширений и любых других расширений будущего. Запрос интерфейса из любого расширения или из ADSI дает одинаковый результат.

В следующей процедуре описывается создание расширения.

## <a name="step-1-add-aggregation-to-your-component"></a>Шаг 1. Добавление агрегата в компонент

Следуйте спецификации COM, чтобы добавить статистическую функцию в компонент. В заключение необходимо принять запросы *pUnknown* к компоненту во время выполнения **CreateInstance** и делегировать *pUnknown* в [**IUnknown-интерфейс**](/windows/win32/api/unknwn/nn-unknwn-iunknown) агрегатора, если компонент является агрегатным.

## <a name="step-2-register-your-extension"></a>Шаг 2. Регистрация расширения

Теперь необходимо выбрать класс каталога для расширения. Для этого нельзя использовать одни и те же интерфейсы, которые будут использоваться для интерфейса ADSI, например [**IADsUser**](/windows/desktop/api/Iads/nn-iads-iadsuser), [**иадскомпутер**](/windows/desktop/api/Iads/nn-iads-iadscomputer). Объекты каталога сохраняются в каталоге, в то время как расширение и ADSI выполняются на клиентском компьютере. Примерами объектов каталога являются **User**, **Computer**, **очередь печати**, **serviceConnectionPoint** и **нтдссервице**. Вы можете добавить новый класс в Active Directory и создать новое расширение для этого нового класса.

С помощью разделов реестра можно связать имя класса каталога с компонентами расширения ADSI. На следующем рисунке представлена существующая структура реестра, а также новые ключи.

-   Новый ключ, именуемый **Extensions**, содержит список ключей, каждый из которых представляет класс в каталоге. Каждый класс, например **пользователь**, **очередь печати** или **компьютер**, хранит список подразделов.
-   Каждый подраздел содержит идентификатор CLSID компонента расширения ADSI.
-   Каждый подраздел CLSID содержит запись строки, которая допускает несколько значений. Необходимо только перечислить интерфейсы, участвующие в статистической обработке.

> [!Note]  
> Объекты расширения по-прежнему необходимы для регистрации стандартных ключей COM.

 

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         ADS
            Providers
               LDAP
                  Extensions
                     ClassNameA
                        CLSID of ExtensionA1
                           Interfaces = List of interfaces
                        CLSID of ExtensionA2
                           Interfaces = List of interfaces
                     ClassNameB
                        CLSID of ExtensionB1
                           Interfaces = List of interfaces
                        CLSID of ExtensionB2
                           Interfaces = List of interfaces
```

## <a name="example"></a>Пример

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Microsoft
         ADs
            Providers
               LDAP
                  Extensions
                     printQueue
                        {9f37f39c-6f49-11d1-8c18-00c04fd8d503}
                           Interfaces = {466841B0-E531-11d1-8718-00C04FD44407}
                                        {466841B1-E531-11d1-8718-00C04FD44407}
```

Список интерфейсов из Extension1 может отличаться от "Extension2". Объект, если он активен, поддерживает интерфейсы агрегатора (ADSI) и все интерфейсы, предоставляемые Extension1 и Extension2 агрегата. Разрешение конфликтующих интерфейсов (тот же интерфейс, который поддерживается как агрегатором, так и агрегатами или несколькими агрегатами) определяется приоритетами расширений.

Вы также можете связать расширение CLSID с несколькими именами классов объектов. Например, расширение может расширять как объекты **пользователя** , так и **Контакты** .

> [!Note]  
> Поведение расширения добавляется в класс каждого объекта, а не на экземпляр объекта.

 

Рекомендуется зарегистрировать расширения, как и любые другие компоненты COM, с помощью вызова функции **дллрегистерсвр** . Кроме того, предоставьте возможность отмены регистрации расширения с помощью функции **DllUnregisterServer** .

В следующем примере кода показано, как зарегистрировать расширение.


```C++
/////
// Register the class.
///////////////////////
hr = RegCreateKeyEx( HKEY_LOCAL_MACHINE,
                 _T("SOFTWARE\\Microsoft\\ADs\\Providers\\LDAP\\Extensions\\User\\{E1E3EDF8-48D1-11D2-B22B-0000F87A6B50}"),
 0,
 NULL,
 REG_OPTION_NON_VOLATILE,
 KEY_WRITE,
 NULL,
 &hKey,
 &dwDisposition );
 
///////////////////////////
// Register the Interface.
///////////////////////////
const TCHAR szIf[] = _T("{E1E3EDF7-48D1-11D2-B22B-0000F87A6B50}");
 
hr = RegSetValueEx( hKey, _T("Interfaces"), 0, REG_BINARY, (const BYTE *) szIf, sizeof(szIf) );
 
RegCloseKey(hKey);
return S_OK;
 
}
```



 

 