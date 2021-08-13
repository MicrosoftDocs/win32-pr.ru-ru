---
title: Пример кода для получения различающегося имени домена
description: Этот раздел содержит пример кода, который получает различающееся имя домена, членом которого является локальный компьютер, с помощью привязки бессерверных данных.
ms.assetid: 2b478c55-4683-48cd-bee9-385eea38d01d
ms.tgt_platform: multiple
keywords:
- Active Directory примеры Active Directory, получение различающегося имени домена
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 62ebf027e6c95915e34b70f942fdbf342b3f49b9695d7885c442f015d2a74077
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118693648"
---
# <a name="example-code-for-getting-the-distinguished-name-of-the-domain"></a>Пример кода для получения различающегося имени домена

Этот раздел содержит пример кода, который получает различающееся имя домена, членом которого является локальный компьютер, с помощью привязки бессерверных данных.

в следующем Visual Basic примере кода получается различающееся имя домена, членом которого является локальный компьютер, с использованием бессерверной привязки.


```VB
Dim rootDSE As IADs
Dim DistinguishedName As String
 
Set rootDSE = GetObject("LDAP://rootDSE")
DistinguishedName = "LDAP://" & rootDSE.Get("defaultNamingContext")
```



В следующем примере кода C# получается различающееся имя домена, членом которого является локальный компьютер, с использованием бессерверной привязки.


```CSharp
DirectoryEntry RootDirEntry = new DirectoryEntry("LDAP://RootDSE");
Object distinguishedName = RootDirEntry.Properties["defaultNamingContext"].Value;
```



Следующий пример кода C/C++ Возвращает различающееся имя домена, членом которого является локальный компьютер, с помощью привязки бессерверных данных.


```C++
IADs *pads;
hr = ADsGetObject(  L"LDAP://rootDSE",
                    IID_IADs, 
                    (void**)&pads);

if(SUCCEEDED(hr))
{
    VARIANT var;

    VariantInit(&var);
    
    hr = pads->Get(CComBSTR("defaultNamingContext"), &var);
    if(SUCCEEDED(hr))
    {
        if(VT_BSTR == var.vt)
        {
            wprintf(var.bstrVal);
        }
        
        VariantClear(&var);
    }
    
    pads->Release();
}
```



 

 




