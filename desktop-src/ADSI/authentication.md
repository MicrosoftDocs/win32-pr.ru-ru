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
ms.openlocfilehash: ad32b2f32f115b20c99e47578ad76b73ad72a123
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/20/2020
ms.locfileid: "104487300"
---
# <a name="authentication-adsi"></a><span data-ttu-id="962b8-105">Проверка подлинности (ADSI)</span><span class="sxs-lookup"><span data-stu-id="962b8-105">Authentication (ADSI)</span></span>

<span data-ttu-id="962b8-106">В ADSI учетные данные, состоящие из имени пользователя и пароля, используются для предоставления или ограничения доступа к объектам в службе каталогов.</span><span class="sxs-lookup"><span data-stu-id="962b8-106">In ADSI, credentials that consist of a user name and password are used to provide or restrict access to objects in the directory service.</span></span> <span data-ttu-id="962b8-107">Функция [**адсжетобжект**](/windows/desktop/api/Adshlp/nf-adshlp-adsgetobject) использует для проверки подлинности учетные данные вызывающего потока.</span><span class="sxs-lookup"><span data-stu-id="962b8-107">The [**ADsGetObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsgetobject) function uses the credentials of the calling thread for authentication.</span></span> <span data-ttu-id="962b8-108">Функция [**ADsOpenObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsopenobject) и метод [**Иадсопендсобжект:: опендсобжект**](/windows/desktop/api/Iads/nf-iads-iadsopendsobject-opendsobject) можно использовать для указания учетных данных, отличных от методов вызывающего потока.</span><span class="sxs-lookup"><span data-stu-id="962b8-108">The [**ADsOpenObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsopenobject) function and [**IADsOpenDSObject::OpenDSObject**](/windows/desktop/api/Iads/nf-iads-iadsopendsobject-opendsobject) method can be used to specify credentials other than those of the calling thread.</span></span> <span data-ttu-id="962b8-109">Если объект привязан к пользователю, прошедшему проверку подлинности, ему предоставляется доступ к объекту, поддерживаемому базовыми требованиями к безопасности службы каталогов.</span><span class="sxs-lookup"><span data-stu-id="962b8-109">When an object is bound to with an authenticated user, the user is allowed access to the object as supported by the underlying directory service security requirements.</span></span>

> [!Note]  
> <span data-ttu-id="962b8-110">Функция [**ADsOpenObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsopenobject) и метод [**Иадсопендсобжект:: опендсобжект**](/windows/desktop/api/Iads/nf-iads-iadsopendsobject-opendsobject) не должны использоваться для проверки учетных данных пользователя.</span><span class="sxs-lookup"><span data-stu-id="962b8-110">The [**ADsOpenObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsopenobject) function and [**IADsOpenDSObject::OpenDSObject**](/windows/desktop/api/Iads/nf-iads-iadsopendsobject-opendsobject) method should not be used to validate user credentials.</span></span> <span data-ttu-id="962b8-111">Дополнительные сведения о проверке учетных данных пользователя см. в статье базы знаний Майкрософт 180548 [Практическое руководство. Проверка учетных данных пользователя в операционных системах Майкрософт](https://support.microsoft.com/kb/180548).</span><span class="sxs-lookup"><span data-stu-id="962b8-111">For more information about validating user credentials, see Microsoft Knowledge Base article 180548 [HOWTO: Validate User Credentials on Microsoft Operating Systems](https://support.microsoft.com/kb/180548).</span></span>

 

<span data-ttu-id="962b8-112">В следующем примере кода показано, как использовать метод [**опендсобжект**](/windows/desktop/api/Iads/nf-iads-iadsopendsobject-opendsobject) для проверки подлинности пользователя.</span><span class="sxs-lookup"><span data-stu-id="962b8-112">The following code example shows how to use the [**OpenDSObject**](/windows/desktop/api/Iads/nf-iads-iadsopendsobject-opendsobject) method to authenticate a user.</span></span>


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



 

 




