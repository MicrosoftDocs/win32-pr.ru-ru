---
description: При работе с API мобильной широкополосной связи следует использовать следующий набор рекомендаций для достижения наилучшей производительности.
ms.assetid: 523e3ea4-1d4e-45d1-bc24-93aa2fb14390
title: Рекомендации по API мобильного широкополосного подключения
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 399c2ebc40a357eac9686bc3c2c9f471e3b853f8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104263180"
---
# <a name="mobile-broadband-api-best-practices"></a>Рекомендации по API мобильного широкополосного подключения

При работе с API мобильной широкополосной связи следует использовать следующий набор рекомендаций для достижения наилучшей производительности.

## <a name="do-not-cache-functional-objects"></a>Не кэшировать функциональные объекты

Функциональные объекты, такие как [**имбнинтерфаце**](/windows/desktop/api/mbnapi/nn-mbnapi-imbninterface) и другие, получаются из объектов Manager, таких как [**имбнинтерфацеманажер**](/windows/desktop/api/mbnapi/nn-mbnapi-imbninterfacemanager), с помощью метода перечисления для соответствующего объекта Manager. Не кэшировать эти функциональные объекты, так как кэшированные функциональные объекты содержат устаревшие данные. Синхронные операции, выполняемые с этими функциональными объектами, будут возвращать те же данные, пока не будут снова получены функциональные объекты.

Вместо этого закэширование объектов диспетчера и получение функциональных объектов из объекта Manager с помощью метода перечисления для соответствующего объекта Manager снова, чтобы получить актуальные данные.

В следующем примере кода демонстрируется правильный способ кэширования объектов диспетчера.


```C++
#include <atlbase.h>
#include "mbnapi.h"
#include <tchar.h>

int main()
{
    HRESULT hr = E_FAIL;
    int returnVal = 0;

    do
    {
        hr = CoInitializeEx(NULL, COINIT_MULTITHREADED);    
        if (FAILED(hr))
        {
            returnVal = hr; 
            break;
        }

        CComPtr<IMbnInterfaceManager>  g_InterfaceMgr = NULL;

        //Do the below once(cache the manager objects)
        hr = CoCreateInstance(CLSID_MbnInterfaceManager,
            NULL, 
            CLSCTX_ALL, 
            IID_IMbnInterfaceManager, 
            (void**)&g_InterfaceMgr);
        if (FAILED(hr))
        {
            returnVal = hr; 
            break;
        }

        SAFEARRAY *psa = NULL;

        //Do the below each time(do not cache functional objects)
        hr = g_InterfaceMgr->GetInterfaces(&psa);
        if (FAILED(hr))
        {
            returnVal = hr; 
            break;
        }

        LONG lLower;
        LONG lUpper;

        hr = SafeArrayGetLBound(psa, 1, &lLower);
        if (FAILED(hr))
        {
            returnVal = hr; 
            break;
        }

        hr = SafeArrayGetUBound(psa, 1, &lUpper);
        if (FAILED(hr))
        {
            returnVal = hr; 
            break;
        }

        CComPtr<IMbnInterface>  pInf = NULL;
        MBN_READY_STATE readyState;

        for (LONG l = lLower; l <= lUpper; l++)
        {
            hr = SafeArrayGetElement(psa, &l, (void*)(&pInf));
            if (FAILED(hr))
            {
                returnVal = hr; 
                break;
            }

            hr = pInf->GetReadyState(&readyState);
            if (FAILED(hr))
            {
                returnVal = hr; 
                break;
            }

            _tprintf(_T("Ready State = %d"), readyState); 
        }

        if (FAILED(hr))
        {
            break;
        }
    } while (FALSE);


    CoUninitialize();
    return returnVal;
}
```



## <a name="handle-all-notifications"></a>Обработайте все уведомления

Следуйте указаниям и обрабатывайте все уведомления, даже если они не запускаются приложением. Это необходимо для синхронизации пользовательского интерфейса с фактическим состоянием устройства.

На одном компьютере может быть установлено несколько диспетчеров соединений. Пользовательский интерфейс доступного для просмотра сетевого интерфейса, предоставляемый Windows 7, является диспетчером соединений. Любые другие диспетчеры соединений должны отвечать на все уведомления, чтобы оставаться синхронизированными с собственным ИНТЕРФЕЙСом Windows. Пользователь может выбрать выполнение некоторой операции с одним из диспетчеров соединений, что может привести к изменению состояния устройства мобильного широкополосного подключения. Однако для правильного указания измененного состояния устройства другие диспетчеры соединений должны оставаться обновленными.

Например, при выполнении подключения с помощью одного из диспетчеров соединений состояние устройства будет изменено с "доступно для подключения". Это изменение должно быть видимым для диспетчеров соединений, которые не инициировали это действие. Все диспетчеры соединений, имеющие пользовательский интерфейс, указывающий состояние подключения устройства, должны прослушивать и обменять уведомления о состоянии соединения, чтобы правильно обновить пользовательский интерфейс.

## <a name="sending-and-receiving-bytes"></a>Отправка и получение байтов

Используйте вспомогательные функции IP [жетлфентри](/windows/win32/api/iphlpapi/nf-iphlpapi-getifentry) и [GetlfEntry2](/windows/win32/api/netioapi/nf-netioapi-getifentry2) для отправки и получения байтов.

## <a name="using-the-pin-unblock-api"></a>Использование API разблокировки ПИН-кода

Чтобы успешно вызвать [**имбнпин:: Unblock**](/windows/desktop/api/mbnapi/nf-mbnapi-imbnpin-unblock), необходимо повысить уровень вызывающего клиентского приложения. Этот метод является единственной частью API мобильной широкополосной связи, для которой требуются права администратора или NCO. Дополнительные сведения см. [в описании группы операторов конфигурации сети]( https://support.microsoft.com/kb/297938/en-us) .

## <a name="working-with-safearrays"></a>Работа с SafeArray

-   Используйте Зеромемори () перед доступом к любым элементам массива SafeArray.

-   Не следует проверять индексы SafeArray. Они могут быть отрицательными.

В следующем примере кода показано, как правильно обработайте SafeArray.


```C++
#include <atlbase.h>
#include "mbnapi.h"

void CreateVisibleProviderList(LPCWSTR interfaceID)
{
    CComPtr<IMbnInterfaceManager>  g_InterfaceMgr = NULL;
    SAFEARRAY *visibleProviders = NULL;
    long visibleLower = 0;
    long visibleUpper = 0;
    MBN_PROVIDER *pProvider = NULL;
    CComPtr<IMbnInterface> pInterface = NULL;

    HRESULT hr = CoInitializeEx(NULL, COINIT_MULTITHREADED);

    if (FAILED(hr))
    {
        goto ERROR_0;
    }

    hr = CoCreateInstance(CLSID_MbnInterfaceManager,
            NULL, 
            CLSCTX_ALL, 
            IID_IMbnInterfaceManager, 
            (void**)&g_InterfaceMgr);
    
    if (FAILED(hr))
    {
        goto ERROR_0;
    }

    hr = g_InterfaceMgr->GetInterface(interfaceID, & pInterface);
    if (FAILED(hr)) 
    {
        goto ERROR_0;
    }

    ULONG age;

    hr = pInterface->GetVisibleProviders(&age, &visibleProviders);
    if (FAILED(hr)) 
    {
        goto ERROR_0;
    }

    hr = SafeArrayGetLBound(visibleProviders, 1, &visibleLower);
    if (FAILED(hr)) 
    {
        goto ERROR_0;
    }

    hr = SafeArrayGetUBound(visibleProviders, 1, &visibleUpper);
    if (FAILED(hr)) 
    {
        goto ERROR_0;
    }

    //don't check on the indexes of safearray to be positive
    if (visibleLower > visibleUpper) 
    {
        // There are no visible providers in this case.
        hr = HRESULT_FROM_WIN32(ERROR_NOT_FOUND);
        goto ERROR_0;
    }

    DWORD size = (visibleUpper - visibleLower + 1) * sizeof(BOOL);
    DBG_UNREFERENCED_LOCAL_VARIABLE(size); 
    
    pProvider = (MBN_PROVIDER *)CoTaskMemAlloc(sizeof(MBN_PROVIDER));
    if (!pProvider) 
    {
        hr = E_OUTOFMEMORY;
        goto ERROR_0;
    }

    for (LONG vIndex = visibleLower; vIndex <= visibleUpper; vIndex++) 
    {
        //use zeromemory before accessing any elements in a safearray
        ZeroMemory(pProvider, sizeof(MBN_PROVIDER));
        hr = SafeArrayGetElement(visibleProviders, &vIndex, (void *)pProvider);
        if (FAILED(hr)) 
        {
            continue;
        }
    }

ERROR_0:
    if (visibleProviders) 
    {
        SafeArrayDestroy(visibleProviders);
        visibleProviders = NULL;
    }

    CoUninitialize();
}
```



 

 
