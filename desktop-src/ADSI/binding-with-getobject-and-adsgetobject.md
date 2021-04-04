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
# <a name="binding-with-getobject-and-adsgetobject"></a><span data-ttu-id="044e9-104">Привязка с помощью GetObject и Адсжетобжект</span><span class="sxs-lookup"><span data-stu-id="044e9-104">Binding With GetObject and ADsGetObject</span></span>

<span data-ttu-id="044e9-105">Функции **GetObject** и [**адсжетобжект**](/windows/desktop/api/Adshlp/nf-adshlp-adsgetobject) используются для привязки к объектам службы каталогов без проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="044e9-105">The **GetObject** and [**ADsGetObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsgetobject) functions are used to bind to directory service objects with no authentication.</span></span> <span data-ttu-id="044e9-106">Приложению не требуется предоставлять учетные данные при доступе к данным службы каталогов.</span><span class="sxs-lookup"><span data-stu-id="044e9-106">The application is not required to provide credentials when accessing directory service data.</span></span> <span data-ttu-id="044e9-107">ADSI использует контекст безопасности вызывающего потока.</span><span class="sxs-lookup"><span data-stu-id="044e9-107">ADSI uses the security context of the calling thread.</span></span> <span data-ttu-id="044e9-108">Однако при сбое безопасной проверки подлинности ADSI пытается выполнить простую привязку с нулевым именем пользователя и паролем NULL.</span><span class="sxs-lookup"><span data-stu-id="044e9-108">However, if secure authentication fails, ADSI attempts to perform a simple bind with a null user name and null password.</span></span> <span data-ttu-id="044e9-109">Если простая привязка выполнена, Пользовательский контекст привязки — гость.</span><span class="sxs-lookup"><span data-stu-id="044e9-109">If the simple bind succeeds, the user context for the binding is Guest.</span></span> <span data-ttu-id="044e9-110">В простой привязке используется проверка подлинности с открытым текстом.</span><span class="sxs-lookup"><span data-stu-id="044e9-110">A simple bind uses plaintext authentication.</span></span> <span data-ttu-id="044e9-111">Поскольку имя пользователя или пароль не передаются по сети, это не является проблемой безопасности.</span><span class="sxs-lookup"><span data-stu-id="044e9-111">Because no user name or password is transmitted over the network, this is not a security issue.</span></span>

<span data-ttu-id="044e9-112">Функция **GetObject** используется для привязки к объектам службы каталогов на языках, поддерживающих автоматизацию, например Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="044e9-112">The **GetObject** function is used to bind to directory service objects in languages that support automation, such as Visual Basic.</span></span> <span data-ttu-id="044e9-113">Для функции **GetObject** требуется строка моникера.</span><span class="sxs-lookup"><span data-stu-id="044e9-113">The **GetObject** function requires a moniker string.</span></span> <span data-ttu-id="044e9-114">В ADSI строка привязки является строкой моникера.</span><span class="sxs-lookup"><span data-stu-id="044e9-114">In ADSI, the binding string is the moniker string.</span></span>

<span data-ttu-id="044e9-115">В языках, которые напрямую не поддерживают автоматизацию, например C или C++, ADSI предоставляет функцию [**адсжетобжект**](/windows/desktop/api/Adshlp/nf-adshlp-adsgetobject) для привязки к объектам службы каталогов.</span><span class="sxs-lookup"><span data-stu-id="044e9-115">In languages that do not directly support automation, such as C or C++, ADSI provides the [**ADsGetObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsgetobject) function to bind to directory service objects.</span></span> <span data-ttu-id="044e9-116">Кроме того, функции [**мкпарседисплайнаме**](/windows/win32/api/objbase/nf-objbase-mkparsedisplayname) и [**мкпарседисплайнамикс**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775113(v=vs.85)) можно использовать для достижения того же результата, что и **GetObject**.</span><span class="sxs-lookup"><span data-stu-id="044e9-116">Alternatively, the [**MkParseDisplayName**](/windows/win32/api/objbase/nf-objbase-mkparsedisplayname) and [**MkParseDisplayNameEx**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775113(v=vs.85)) functions can be used to achieve the same result as **GetObject**.</span></span>

<span data-ttu-id="044e9-117">Для службы, работающей под учетной записью LocalSystem, контекст безопасности, используемый **GetObject** и [**адсжетобжект**](/windows/desktop/api/Adshlp/nf-adshlp-adsgetobject) , зависит от компьютера, на котором запущена служба.</span><span class="sxs-lookup"><span data-stu-id="044e9-117">For a service running under the LocalSystem account, the security context used by **GetObject** and [**ADsGetObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsgetobject) depends on the computer on which the service is running.</span></span> <span data-ttu-id="044e9-118">Если служба работает под учетной записью LocalSystem на контроллере домена, она получает полный доступ на уровне системы к Active Directory.</span><span class="sxs-lookup"><span data-stu-id="044e9-118">If the service is running as LocalSystem on a domain controller, the service has full system-level access to Active Directory.</span></span> <span data-ttu-id="044e9-119">Если служба не запущена на контроллере домена, служба имеет права доступа и привилегии, предоставленные учетной записи компьютера для компьютера, на котором запущена служба. Это значительно менее эффективно, чем доступ на уровне системы.</span><span class="sxs-lookup"><span data-stu-id="044e9-119">If the service is not running on a DC, the service has the access rights and privileges granted to the computer account for the computer on which the service is running; this is significantly less powerful than system-level access.</span></span>

## <a name="examples"></a><span data-ttu-id="044e9-120">Примеры</span><span class="sxs-lookup"><span data-stu-id="044e9-120">Examples</span></span>

<span data-ttu-id="044e9-121">В следующем Visual Basic примере кода показано, как использовать функцию **GetObject** для привязки к объекту.</span><span class="sxs-lookup"><span data-stu-id="044e9-121">The following Visual Basic code example shows how to use the **GetObject** function to bind to an object.</span></span>


```VB
Dim myUser as IADs
Set myUser = GetObject("LDAP://CN=jeffsmith,DC=fabrikam,DC=com")
```



<span data-ttu-id="044e9-122">В следующем примере кода C++ показано, как использовать функцию [**адсжетобжект**](/windows/desktop/api/Adshlp/nf-adshlp-adsgetobject) для привязки к объекту.</span><span class="sxs-lookup"><span data-stu-id="044e9-122">The following C++ code example shows how to use the [**ADsGetObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsgetobject) function to bind to an object.</span></span>


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



 

 