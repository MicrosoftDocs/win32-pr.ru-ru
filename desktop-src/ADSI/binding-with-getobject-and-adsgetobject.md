---
title: Привязка с помощью GetObject и Адсжетобжект
description: Функции GetObject и Адсжетобжект используются для привязки к объектам службы каталогов без проверки подлинности.
ms.assetid: 15d8116a-8ec1-48b5-bf62-411fdff7c8b8
ms.tgt_platform: multiple
keywords:
- ADSI ADSI, использование, привязка к GetObject и Адсжетобжект
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5f61d5aba2c2c49e97ddcfc0f727d0cd4c17a164
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/21/2020
ms.locfileid: "103987871"
---
# <a name="binding-with-getobject-and-adsgetobject"></a>Привязка с помощью GetObject и Адсжетобжект

Функции **GetObject** и [**адсжетобжект**](/windows/desktop/api/Adshlp/nf-adshlp-adsgetobject) используются для привязки к объектам службы каталогов без проверки подлинности. Приложению не требуется предоставлять учетные данные при доступе к данным службы каталогов. ADSI использует контекст безопасности вызывающего потока. Однако при сбое безопасной проверки подлинности ADSI пытается выполнить простую привязку с нулевым именем пользователя и паролем NULL. Если простая привязка выполнена, Пользовательский контекст привязки — гость. В простой привязке используется проверка подлинности с открытым текстом. Поскольку имя пользователя или пароль не передаются по сети, это не является проблемой безопасности.

Функция **GetObject** используется для привязки к объектам службы каталогов на языках, поддерживающих автоматизацию, например Visual Basic. Для функции **GetObject** требуется строка моникера. В ADSI строка привязки является строкой моникера.

В языках, которые напрямую не поддерживают автоматизацию, например C или C++, ADSI предоставляет функцию [**адсжетобжект**](/windows/desktop/api/Adshlp/nf-adshlp-adsgetobject) для привязки к объектам службы каталогов. Кроме того, функции [**мкпарседисплайнаме**](/windows/win32/api/objbase/nf-objbase-mkparsedisplayname) и [**мкпарседисплайнамикс**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775113(v=vs.85)) можно использовать для достижения того же результата, что и **GetObject**.

Для службы, работающей под учетной записью LocalSystem, контекст безопасности, используемый **GetObject** и [**адсжетобжект**](/windows/desktop/api/Adshlp/nf-adshlp-adsgetobject) , зависит от компьютера, на котором запущена служба. Если служба работает под учетной записью LocalSystem на контроллере домена, она получает полный доступ на уровне системы к Active Directory. Если служба не запущена на контроллере домена, служба имеет права доступа и привилегии, предоставленные учетной записи компьютера для компьютера, на котором запущена служба. Это значительно менее эффективно, чем доступ на уровне системы.

## <a name="examples"></a>Примеры

В следующем Visual Basic примере кода показано, как использовать функцию **GetObject** для привязки к объекту.


```VB
Dim myUser as IADs
Set myUser = GetObject("LDAP://CN=jeffsmith,DC=fabrikam,DC=com")
```



В следующем примере кода C++ показано, как использовать функцию [**адсжетобжект**](/windows/desktop/api/Adshlp/nf-adshlp-adsgetobject) для привязки к объекту.


```C++
IADs *pObject;
HRESULT hr;

// Initialize COM.
CoInitialize(NULL);

hr = ADsGetObject(L"LDAP://CN=jeffsmith,DC=fabrikam,DC=com", 
        IID_IADs,
        (void**) &pObject);

if(SUCCEEDED(hr))
{
    // Use the object.

    // Release the object.
    pObject->Release()
}

// Uninitialize COM.
CoUninitialize();
```



 

 