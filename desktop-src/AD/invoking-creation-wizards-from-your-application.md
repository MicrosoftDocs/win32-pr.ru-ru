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
# <a name="invoking-creation-wizards-from-your-application"></a>Вызов мастеров создания из приложения

Приложение или компонент может использовать те же мастера создания объектов службы каталогов, которые используются в оснастке администрирования консоли управления Active Directory. Это достигается с помощью интерфейса [**идсадминкреатеобж**](/windows/desktop/api/DSAdmin/nn-dsadmin-idsadmincreateobj) .

## <a name="using-the-idsadmincreateobj-interface"></a>Использование интерфейса Идсадминкреатеобж

Приложение или компонент (клиент) создает экземпляр интерфейса [**идсадминкреатеобж**](/windows/desktop/api/DSAdmin/nn-dsadmin-idsadmincreateobj) , вызывая [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) с идентификатором класса **CLSID \_ дсадминкреатеобж** . COM должен быть инициализирован путем вызова функции [**CoInitialize**](/windows/win32/api/objbase/nf-objbase-coinitialize) перед вызовом **CoCreateInstance** .

Затем клиент вызывает [**идсадминкреатеобж:: Initialize**](/windows/desktop/api/DSAdmin/nf-dsadmin-idsadmincreateobj-initialize) для инициализации объекта [**идсадминкреатеобж**](/windows/desktop/api/DSAdmin/nn-dsadmin-idsadmincreateobj) . **Идсадминкреатеобж:: Initialize** принимает указатель интерфейса [**иадсконтаинер**](/windows/desktop/api/iads/nn-iads-iadscontainer) , представляющий контейнер, в котором должен быть создан объект, и имя класса создаваемого объекта. При создании объектов-пользователей можно также указать существующий объект, который будет скопирован в новый объект.

После инициализации объекта [**идсадминкреатеобж**](/windows/desktop/api/DSAdmin/nn-dsadmin-idsadmincreateobj) клиент вызывает [**Идсадминкреатеобж:: креатемодал**](/windows/desktop/api/DSAdmin/nf-dsadmin-idsadmincreateobj-createmodal) , чтобы отобразить мастер создания объектов.

В отличие от большинства идентификаторов классов и интерфейсов, **CLSID \_ Дсадминкреатеобж** и **IID \_ адсадминкреатеобж** не определены в файле библиотеки. Это означает, что необходимо определить хранилище для этих идентификаторов в приложении. Для этого необходимо включить файл инитгуид. h непосредственно перед включением дсадмин. h. Файл инитгуид. h должен быть добавлен в приложение только один раз. В следующем примере кода показано, как включить эти файлы.


```C++
#include <initguid.h>
#include <dsadmin.h>
```



В следующем примере кода показано, как можно создать интерфейс [**идсадминкреатеобж**](/windows/desktop/api/DSAdmin/nn-dsadmin-idsadmincreateobj) и использовать его для запуска мастера создания объектов для объекта пользователя.


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



 

 