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
# <a name="example-code-for-getting-the-distinguished-name-of-the-domain"></a><span data-ttu-id="00002-104">Пример кода для получения различающегося имени домена</span><span class="sxs-lookup"><span data-stu-id="00002-104">Example Code for Getting the Distinguished Name of the Domain</span></span>

<span data-ttu-id="00002-105">Этот раздел содержит пример кода, который получает различающееся имя домена, членом которого является локальный компьютер, с помощью привязки бессерверных данных.</span><span class="sxs-lookup"><span data-stu-id="00002-105">This topic includes a code example that gets the distinguished name of the domain that the local computer is a member of by using serverless binding.</span></span>

<span data-ttu-id="00002-106">В следующем Visual Basic примере кода получается различающееся имя домена, членом которого является локальный компьютер, с использованием бессерверной привязки.</span><span class="sxs-lookup"><span data-stu-id="00002-106">The following Visual Basic code example gets the distinguished name of the domain that the local computer is a member of by using serverless binding.</span></span>


```VB
Dim rootDSE As IADs
Dim DistinguishedName As String
 
Set rootDSE = GetObject("LDAP://rootDSE")
DistinguishedName = "LDAP://" & rootDSE.Get("defaultNamingContext")
```



<span data-ttu-id="00002-107">В следующем примере кода C# получается различающееся имя домена, членом которого является локальный компьютер, с использованием бессерверной привязки.</span><span class="sxs-lookup"><span data-stu-id="00002-107">The following C# code example gets the distinguished name of the domain that the local computer is a member of by using serverless binding.</span></span>


```CSharp
DirectoryEntry RootDirEntry = new DirectoryEntry("LDAP://RootDSE");
Object distinguishedName = RootDirEntry.Properties["defaultNamingContext"].Value;
```



<span data-ttu-id="00002-108">Следующий пример кода C/C++ Возвращает различающееся имя домена, членом которого является локальный компьютер, с помощью привязки бессерверных данных.</span><span class="sxs-lookup"><span data-stu-id="00002-108">The following C/C++ code example gets the distinguished name of the domain that the local computer is a member of by using serverless binding.</span></span>


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



 

 




