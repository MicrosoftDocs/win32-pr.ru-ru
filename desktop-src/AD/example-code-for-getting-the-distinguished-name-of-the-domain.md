---
title: Пример кода для получения различающегося имени домена
description: Этот раздел содержит пример кода, который получает различающееся имя домена, членом которого является локальный компьютер, с помощью привязки бессерверных данных.
ms.assetid: 2b478c55-4683-48cd-bee9-385eea38d01d
ms.tgt_platform: multiple
keywords:
- Active Directory примеры Active Directory, получение различающегося имени домена
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4badd8cd356ce5adfb20470a969e6f7444c010a1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104252783"
---
# <a name="example-code-for-getting-the-distinguished-name-of-the-domain"></a>Пример кода для получения различающегося имени домена

Этот раздел содержит пример кода, который получает различающееся имя домена, членом которого является локальный компьютер, с помощью привязки бессерверных данных.

В следующем Visual Basic примере кода получается различающееся имя домена, членом которого является локальный компьютер, с использованием бессерверной привязки.


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



 

 




