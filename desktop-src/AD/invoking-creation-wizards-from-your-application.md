---
title: Вызов мастеров создания из приложения
description: Приложение или компонент может использовать те же мастера создания объектов службы каталогов, которые используются в оснастке администрирования консоли управления Active Directory. Это достигается с помощью интерфейса Идсадминкреатеобж.
ms.assetid: be4b6101-f795-403b-b93e-960759ac4f14
ms.tgt_platform: multiple
keywords:
- Вызов мастеров создания из приложения AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fa523d3b861d1d4a7588455b04c1a9633734253a
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/17/2020
ms.locfileid: "104487424"
---
# <a name="invoking-creation-wizards-from-your-application"></a><span data-ttu-id="7e85c-104">Вызов мастеров создания из приложения</span><span class="sxs-lookup"><span data-stu-id="7e85c-104">Invoking Creation Wizards from Your Application</span></span>

<span data-ttu-id="7e85c-105">Приложение или компонент может использовать те же мастера создания объектов службы каталогов, которые используются в оснастке администрирования консоли управления Active Directory. Это достигается с помощью интерфейса [**идсадминкреатеобж**](/windows/desktop/api/DSAdmin/nn-dsadmin-idsadmincreateobj) .</span><span class="sxs-lookup"><span data-stu-id="7e85c-105">An application or component can use the same directory service object creation wizards used by the Active Directory administrative MMC snap-ins. This is accomplished with the [**IDsAdminCreateObj**](/windows/desktop/api/DSAdmin/nn-dsadmin-idsadmincreateobj) interface.</span></span>

## <a name="using-the-idsadmincreateobj-interface"></a><span data-ttu-id="7e85c-106">Использование интерфейса Идсадминкреатеобж</span><span class="sxs-lookup"><span data-stu-id="7e85c-106">Using the IDsAdminCreateObj Interface</span></span>

<span data-ttu-id="7e85c-107">Приложение или компонент (клиент) создает экземпляр интерфейса [**идсадминкреатеобж**](/windows/desktop/api/DSAdmin/nn-dsadmin-idsadmincreateobj) , вызывая [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) с идентификатором класса **CLSID \_ дсадминкреатеобж** .</span><span class="sxs-lookup"><span data-stu-id="7e85c-107">An application or component (client) creates an instance of the [**IDsAdminCreateObj**](/windows/desktop/api/DSAdmin/nn-dsadmin-idsadmincreateobj) interface by calling [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) with the **CLSID\_DsAdminCreateObj** class identifier.</span></span> <span data-ttu-id="7e85c-108">COM должен быть инициализирован путем вызова функции [**CoInitialize**](/windows/win32/api/objbase/nf-objbase-coinitialize) перед вызовом **CoCreateInstance** .</span><span class="sxs-lookup"><span data-stu-id="7e85c-108">COM must be initialized by calling [**CoInitialize**](/windows/win32/api/objbase/nf-objbase-coinitialize) before **CoCreateInstance** is called.</span></span>

<span data-ttu-id="7e85c-109">Затем клиент вызывает [**идсадминкреатеобж:: Initialize**](/windows/desktop/api/DSAdmin/nf-dsadmin-idsadmincreateobj-initialize) для инициализации объекта [**идсадминкреатеобж**](/windows/desktop/api/DSAdmin/nn-dsadmin-idsadmincreateobj) .</span><span class="sxs-lookup"><span data-stu-id="7e85c-109">The client then calls [**IDsAdminCreateObj::Initialize**](/windows/desktop/api/DSAdmin/nf-dsadmin-idsadmincreateobj-initialize) to initialize the [**IDsAdminCreateObj**](/windows/desktop/api/DSAdmin/nn-dsadmin-idsadmincreateobj) object.</span></span> <span data-ttu-id="7e85c-110">**Идсадминкреатеобж:: Initialize** принимает указатель интерфейса [**иадсконтаинер**](/windows/desktop/api/iads/nn-iads-iadscontainer) , представляющий контейнер, в котором должен быть создан объект, и имя класса создаваемого объекта.</span><span class="sxs-lookup"><span data-stu-id="7e85c-110">**IDsAdminCreateObj::Initialize** accepts an [**IADsContainer**](/windows/desktop/api/iads/nn-iads-iadscontainer) interface pointer that represents the container that the object should be created in, and the class name of the object to be created.</span></span> <span data-ttu-id="7e85c-111">При создании объектов-пользователей можно также указать существующий объект, который будет скопирован в новый объект.</span><span class="sxs-lookup"><span data-stu-id="7e85c-111">When creating user objects, it is also possible to specify an existing object that will be copied to the new object.</span></span>

<span data-ttu-id="7e85c-112">После инициализации объекта [**идсадминкреатеобж**](/windows/desktop/api/DSAdmin/nn-dsadmin-idsadmincreateobj) клиент вызывает [**Идсадминкреатеобж:: креатемодал**](/windows/desktop/api/DSAdmin/nf-dsadmin-idsadmincreateobj-createmodal) , чтобы отобразить мастер создания объектов.</span><span class="sxs-lookup"><span data-stu-id="7e85c-112">When the [**IDsAdminCreateObj**](/windows/desktop/api/DSAdmin/nn-dsadmin-idsadmincreateobj) object has been initialized, the client calls [**IDsAdminCreateObj::CreateModal**](/windows/desktop/api/DSAdmin/nf-dsadmin-idsadmincreateobj-createmodal) to display the object creation wizard.</span></span>

<span data-ttu-id="7e85c-113">В отличие от большинства идентификаторов классов и интерфейсов, **CLSID \_ Дсадминкреатеобж** и **IID \_ адсадминкреатеобж** не определены в файле библиотеки.</span><span class="sxs-lookup"><span data-stu-id="7e85c-113">Unlike most class and interface identifiers, **CLSID\_DsAdminCreateObj** and **IID\_ADsAdminCreateObj** are not defined in a library file.</span></span> <span data-ttu-id="7e85c-114">Это означает, что необходимо определить хранилище для этих идентификаторов в приложении.</span><span class="sxs-lookup"><span data-stu-id="7e85c-114">This means you must define the storage for these identifiers within your application.</span></span> <span data-ttu-id="7e85c-115">Для этого необходимо включить файл инитгуид. h непосредственно перед включением дсадмин. h.</span><span class="sxs-lookup"><span data-stu-id="7e85c-115">To do this, you must include the file initguid.h immediately before including dsadmin.h.</span></span> <span data-ttu-id="7e85c-116">Файл инитгуид. h должен быть добавлен в приложение только один раз.</span><span class="sxs-lookup"><span data-stu-id="7e85c-116">The initguid.h file must only be included once in an application.</span></span> <span data-ttu-id="7e85c-117">В следующем примере кода показано, как включить эти файлы.</span><span class="sxs-lookup"><span data-stu-id="7e85c-117">The following code example shows how to include these files.</span></span>


```C++
#include <initguid.h>
#include <dsadmin.h>
```



<span data-ttu-id="7e85c-118">В следующем примере кода показано, как можно создать интерфейс [**идсадминкреатеобж**](/windows/desktop/api/DSAdmin/nn-dsadmin-idsadmincreateobj) и использовать его для запуска мастера создания объектов для объекта пользователя.</span><span class="sxs-lookup"><span data-stu-id="7e85c-118">The following code example shows how the [**IDsAdminCreateObj**](/windows/desktop/api/DSAdmin/nn-dsadmin-idsadmincreateobj) interface can be created and used to start the object creation wizard for a user object.</span></span>


```C++
//  Add activeds.lib to your project
//  Add adsiid.lib to your project

#include "stdafx.h"
#include <atlbase.h>
#include <atlstr.h>
#include "activeds.h"
#include <initguid.h> // Only include this in one source file
#include <dsadmin.h>

//  GetUserContainer() function binds to the user container
IADsContainer* GetUserContainer(void)
{
    IADsContainer *pUsers = NULL;
    HRESULT hr;
    IADs *pRoot;

    //  Bind to the rootDSE.
    hr = ADsGetObject(L"LDAP://rootDSE", IID_IADs, (LPVOID*)&pRoot);

    if(SUCCEEDED(hr))
    {
        VARIANT var;
        VariantInit(&var);
        CComBSTR sbstr(L"defaultNamingContext");

        //  Get the default naming context (domain) DN.
        hr = pRoot->Get(sbstr, &var);
        if(SUCCEEDED(hr) && (VT_BSTR == var.vt))
        {
            CStringW sstr(L"LDAP://CN=Users,");
            sstr += var.bstrVal;

            //  Bind to the User container.
            hr = ADsGetObject(sstr, IID_IADsContainer, (LPVOID*)&pUsers);

            VariantClear(&var);
        }
    }

    return pUsers;
}


//  The LaunchNewUserWizard() function launches the user wizard.
HRESULT LaunchNewUserWizard(IADs** ppAdsOut)
{
    if(NULL == ppAdsOut)
    {
        return E_INVALIDARG;
    }

    HRESULT hr;
    IDsAdminCreateObj* pCreateObj = NULL;

    hr = ::CoCreateInstance(CLSID_DsAdminCreateObj,
                            NULL, 
                            CLSCTX_INPROC_SERVER,
                            IID_IDsAdminCreateObj,
                            (void**)&pCreateObj);

    if(SUCCEEDED(hr))
    {
        IADsContainer *pContainer;

        pContainer = GetUserContainer();

        if(pContainer)
        {
            hr = pCreateObj->Initialize(pContainer, NULL, L"user");
            if(SUCCEEDED(hr))
            {
                HWND    hwndParent;

                hwndParent = GetDesktopWindow();

                hr = pCreateObj->CreateModal(hwndParent, ppAdsOut);
            }

            pContainer->Release();
        }

        pCreateObj->Release();
    }

    return hr;    
}

//  Entry point to the application
int main(void)
{
    HRESULT hr;
    IADs *pAds = NULL;

    CoInitialize(NULL);

    hr = LaunchNewUserWizard(&pAds);
    if((S_OK == hr) && (NULL != pAds))
    {
        pAds->Release();
    }

    CoUninitialize();

    return 0;
}
```



 

 