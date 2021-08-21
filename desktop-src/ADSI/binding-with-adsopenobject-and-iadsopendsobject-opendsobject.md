---
title: Привязка с помощью ADsOpenObject и Иадсопендсобжект Опендсобжект
description: Функция ADsOpenObject и метод Иадсопендсобжект Опендсобжект используются для привязки к объектам службы каталогов, когда необходимо указать альтернативные учетные данные и требуется шифрование данных.
ms.assetid: 7b8ded11-e04f-40f5-a82a-5972c4df9dea
ms.tgt_platform: multiple
keywords:
- Привязка с помощью ADsOpenObject и Иадсопендсобжект Опендсобжект ADSI
- ADSI ADSI, использование, привязка с помощью ADsOpenObject и Иадсопендсобжект Опендсобжект
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d41ffe1e9ad0b8a78d1a8c563de250851a894012938682c4cfd0d0fd713f99bf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119082778"
---
# <a name="binding-with-adsopenobject-and-iadsopendsobjectopendsobject"></a>Привязка с ADsOpenObject и Иадсопендсобжект:: Опендсобжект

Функция [**ADsOpenObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsopenobject) и метод [**Иадсопендсобжект:: опендсобжект**](/windows/desktop/api/Iads/nf-iads-iadsopendsobject-opendsobject) используются для привязки к объектам службы каталогов, если необходимо указать альтернативные учетные данные и требуется шифрование данных.

По возможности следует использовать учетные данные вызывающего потока. Однако, если необходимо использовать альтернативные учетные данные, необходимо использовать функцию [**ADsOpenObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsopenobject) или метод [**Иадсопендсобжект:: опендсобжект**](/windows/desktop/api/Iads/nf-iads-iadsopendsobject-opendsobject) . Если используются альтернативные учетные данные, важно не кэшировать пароль. Можно выполнить несколько операций привязки, указав имя пользователя и пароль для первой операции привязки, а затем указав только имя пользователя в последующих привязках. Система настраивает сеанс при первом вызове и использует тот же сеанс при последующих вызовах привязки при условии, что выполняются следующие условия.

-   Одно и то же имя пользователя в каждой операции привязки.
-   Реализуйте бессерверную привязку или привяжите к одному и тому же серверу в каждой операции привязки.
-   Сохраните открытый сеанс, нажимая на ссылку на объект в одной из операций привязки. Сеанс закрывается при освобождении последней ссылки на объект.

[**ADsOpenObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsopenobject) и [**иадсопендсобжект:: опендсобжект**](/windows/desktop/api/Iads/nf-iads-iadsopendsobject-opendsobject) используют Windows NT [интерфейсы поставщика поддержки безопасности (SSPI)](/windows/desktop/SecAuthN/sspi) для обеспечения гибкости параметров проверки подлинности. Основным преимуществом использования этих интерфейсов является предоставление различных типов проверки подлинности для Active Directory клиентов и шифрования сеанса. В настоящее время ADSI не разрешает передачу сертификатов. Таким образом, можно использовать SSL для шифрования, а затем Kerberos, NTLM или простую проверку подлинности в зависимости от того, как установлены флаги в параметре *двресервед* .

В ADSI нельзя запрашивать конкретный поставщик SSPI, хотя всегда получается самый высокий приоритет. в случае привязки клиента Windows к компьютеру, на котором выполняется Windows, используется протокол Kerberos. Не разрешайте проверку подлинности сертификата в случае веб-страницы, так как проверка подлинности выполняется перед запуском веб-страницы.

Хотя открытые операции позволяют указать пользователя и пароль, делать это не следует. Вместо этого не указывайте учетные данные и неявно используйте учетные данные контекста безопасности вызывающего объекта. Чтобы выполнить привязку к объекту каталога с помощью учетных данных вызывающего объекта с [**ADsOpenObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsopenobject) или [**Иадсопендсобжект:: Опендсобжект**](/windows/desktop/api/Iads/nf-iads-iadsopendsobject-opendsobject), укажите **значение NULL** как для имени пользователя, так и для пароля.

Наконец, чтобы выполнить привязку без проверки подлинности, используйте флаг **\_ без \_ проверки подлинности ADS** . Без проверки подлинности указывает, что ADSI пытается выполнить привязку в качестве анонимного пользователя к целевому объекту и не выполняет проверку подлинности. Это эквивалентно запросу анонимной привязки в протоколе LDAP и показывает, что все пользователи включены в контекст безопасности.

Если флаги проверки подлинности имеют значение 0, ADSI выполняет простую привязку, отправку в виде открытого текста.

> [!Caution]  
> Если имя пользователя и пароль указаны без указания флагов проверки подлинности, имя пользователя и пароль передаются по сети в виде открытого текста, что является угрозой безопасности. Не указывайте имя пользователя и пароль, не указывая флаги проверки подлинности.

 

## <a name="examples"></a>Примеры

в следующем Visual Basic примере кода показано, как использовать метод [**иадсопендсобжект:: опендсобжект**](/windows/desktop/api/Iads/nf-iads-iadsopendsobject-opendsobject) .


```VB
Dim openDS As IADsOpenDSObject
Dim usr As IADsUser
 
Set openDS = GetObject("LDAP:")
 
openDS.OpenDSObject("LDAP://CN=jeffsmith,DC=fabrikam,DC=com",
    NULL, 
    NULL,
    ADS_SECURE_AUTHENTICATION)
```



В следующем примере кода C++ показано, как использовать функцию [**ADsOpenObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsopenobject) .


```C++
IADs *pObject;
HRESULT hr;

hr = ADsOpenObject(L"LDAP://CN=jeffsmith,DC=fabrikam,DC=com",
    NULL, 
    NULL,
    ADS_SECURE_AUTHENTICATION, 
    IID_IADs,
    (void**)&pObject);
if(SUCCEEDED(hr))
{
    // Use the object.

    // Release the object.
    pObject->Release()
}
```



Интерфейс [**иадсопендсобжект**](/windows/desktop/api/Iads/nn-iads-iadsopendsobject) также можно использовать в C++, но дублирует функцию [**ADsOpenObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsopenobject) .

В следующем примере кода C++ показано, как использовать интерфейс [**иадсопендсобжект**](/windows/desktop/api/Iads/nn-iads-iadsopendsobject) для выполнения той же операции привязки, что и в приведенном выше примере кода.


```C++
IADsOpenDSObject *pDSO;
HRESULT hr;
 
hr = ADsGetObject(L"LDAP:", IID_IADsOpenDSObject, (void**)&pDSO);
if(SUCCEEDED(hr))
{
    IDispatch *pDisp;

    hr = pDSO->OpenDSObject(CComBSTR("LDAP://CN=jeffsmith,DC=fabrikam,DC=com"),
        NULL,
        NULL,
        ADS_SECURE_AUTHENTICATION, 
        &pDisp);
    if(SUCCEEDED(hr))
    {
        IADs *pObject;

        hr = pDisp->QueryInterface(IID_IADs, (void**) &pObject);
        if(SUCCEEDED(hr))
        {
            // Use the object.

            // Release the object.
            pObject->Release();
        }

        pDisp->Release();
    }
    
    pDSO->Release();
}
```



 

 