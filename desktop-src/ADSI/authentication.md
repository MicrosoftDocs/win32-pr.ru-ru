---
title: Проверка подлинности (ADSI)
description: В ADSI учетные данные, состоящие из имени пользователя и пароля, используются для предоставления или ограничения доступа к объектам в службе каталогов.
ms.assetid: eef6451d-ebb8-4e22-84f4-61b8be73068a
ms.tgt_platform: multiple
keywords:
- ADSI проверки подлинности
- ADSI, использование, проверка подлинности
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 19177153d8d66f3c27db5c0c2027faa2e02b213305d760d070f5af90b6ba1058
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117840561"
---
# <a name="authentication-adsi"></a>Проверка подлинности (ADSI)

В ADSI учетные данные, состоящие из имени пользователя и пароля, используются для предоставления или ограничения доступа к объектам в службе каталогов. Функция [**адсжетобжект**](/windows/desktop/api/Adshlp/nf-adshlp-adsgetobject) использует для проверки подлинности учетные данные вызывающего потока. Функция [**ADsOpenObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsopenobject) и метод [**Иадсопендсобжект:: опендсобжект**](/windows/desktop/api/Iads/nf-iads-iadsopendsobject-opendsobject) можно использовать для указания учетных данных, отличных от методов вызывающего потока. Если объект привязан к пользователю, прошедшему проверку подлинности, ему предоставляется доступ к объекту, поддерживаемому базовыми требованиями к безопасности службы каталогов.

> [!Note]  
> Функция [**ADsOpenObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsopenobject) и метод [**Иадсопендсобжект:: опендсобжект**](/windows/desktop/api/Iads/nf-iads-iadsopendsobject-opendsobject) не должны использоваться для проверки учетных данных пользователя. Дополнительные сведения о проверке учетных данных пользователя см. в статье базы знаний Майкрософт 180548 [Практическое руководство. Проверка учетных данных пользователя в операционных системах Майкрософт](https://support.microsoft.com/kb/180548).

 

В следующем примере кода показано, как использовать метод [**опендсобжект**](/windows/desktop/api/Iads/nf-iads-iadsopendsobject-opendsobject) для проверки подлинности пользователя.


```VB
Dim MyNamespace As IADsOpenDSObject
Dim X
oUsername="MyUserName"
oPassword="MyPassword"

OnError GoTo CleanuUp
 
Set MyNamespace = GetObject("LDAP:")

' For authentication, pass a variable for the user name and password to be used for 
' authentication. For security reasons, it is recommended that you use the ADS_SECURE_AUTHENTICATION flag.
' 
Set X = MyNamespace.OpenDSObject(DN, oUserName, oPassword, ADS_SECURE_AUTHENTICATION)     

CleanUp:
    MsgBox ("An error has occurred.")
    Set MyNamespace = Nothing
    Set X = Nothing
```



 

 




