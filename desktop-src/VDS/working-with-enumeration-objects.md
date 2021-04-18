---
description: Работа с объектами перечисления
ms.assetid: cb99e9fd-613c-4e38-9e0f-e1a23b72aa07
title: Работа с объектами перечисления
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0df90548ef060d537faff206e45e0cf74630cdfd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105673879"
---
# <a name="working-with-enumeration-objects"></a>Работа с объектами перечисления

\[Начиная с Windows 8 и Windows Server 2012, интерфейс COM [службы виртуальных дисков](virtual-disk-service-portal.md) заменяется [API управления хранилищами Windows](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]

В следующем примере кода показано, как вызывающий объект работает с объектами перечисления с помощью интерфейса [**иенумвдсобжект**](/windows/desktop/api/Vds/nn-vds-ienumvdsobject) . Обратите внимание, что сведения, возвращаемые объектом перечисления, являются статическими. Необходимо снова запросить объект, чтобы увидеть новые изменения конфигурации.

Функция **жетконтроллербид** принимает интерфейс [**ивдссубсистем**](/windows/desktop/api/Vds/nn-vds-ivdssubsystem) , указанный параметром *псубсистем* , и запрашивает контроллеры в подсистеме, а затем выполняет итерацию по возвращенному перечислению, в котором выполняется поиск контроллера с идентификатором GUID, совпадающим с идентификатором GUID, указанным в параметре *пконтроллерид* . Если найден соответствующий контроллер, он возвращается с помощью параметра *ппконтроллер* вместе с параметром S \_ ОК **HRESULT**.


```C++
//
// Simple macro to release non-null interfaces.
//
#include <windows.h>
#include "vds.h"
#include <stdio.h>

#define _SafeRelease(x) {if (NULL != x) { x->Release(); x = NULL; } }

HRESULT GetControllerById(
         IN IVdsSubSystem       *pSubsystem,
         IN CONST VDS_OBJECT_ID *pControllerId,
         OUT IVdsController     **ppController)
{
    VDS_CONTROLLER_PROP vdsControllerProperties;
    IEnumVdsObject      *pEnumController = NULL;
    IVdsController      *pController     = NULL;
    IUnknown            *pUnknown        = NULL;
    HRESULT             hResult          = S_OK;
    ULONG               ulFetched        = 0;
    BOOL                bDone            = FALSE;

    ZeroMemory(&vdsControllerProperties, sizeof(VDS_CONTROLLER_PROP));

    // Query for the enumeration of controllers belonging
    // to the given subsystem.
    hResult = pSubsystem->QueryControllers(&pEnumController);

    if (SUCCEEDED(hResult) && (!pEnumController)) 
    {
        hResult = E_UNEXPECTED; // Errant provider, 
        // returned S_OK 
        // with a NULL pointer.
    }

    if (SUCCEEDED(hResult)) 
    {
        // Enumerate through all the controllers this subsystem 
        // contains to find the controller of interest.
        while (!bDone) 
        {
            ulFetched = 0;
            hResult = pEnumController->Next(1, &pUnknown, &ulFetched);

            if (hResult == S_FALSE) 
            {
                hResult = E_INVALIDARG;
                break;
            }

            if (SUCCEEDED(hResult) && (!pUnknown)) 
            {
                hResult = E_UNEXPECTED; // Errant provider, 
                // returned S_OK with
                // a NULL pointer 
            }

            // Use an IVdsController interface to get the controller 
            // properties and check for the desired GUID.
            if (SUCCEEDED(hResult)) 
            {
                hResult = pUnknown->QueryInterface(IID_IVdsController,  
                    (void **) &pController);
            }

            if (SUCCEEDED(hResult) && (!pController)) 
            {
                hResult = E_UNEXPECTED; // Errant provider, 
                // returned S_OK 
                // with a NULL pointer
            }

            if (SUCCEEDED(hResult)) 
            {
                hResult = pController->  
                GetProperties( &vdsControllerProperties);
            }

            if (SUCCEEDED(hResult) 
                && IsEqualGUID(*pControllerId, vdsControllerProperties.id)) 
            {
                bDone = TRUE;
            } 
            else 
            {
                _SafeRelease(pController);
            }

            _SafeRelease(pUnknown);

            //Free the strings in the properties structure.
            if (NULL != vdsControllerProperties.pwszIdentification) 
            {
                CoTaskMemFree(vdsControllerProperties.pwszIdentification);
            }

            ZeroMemory(&vdsControllerProperties, sizeof(VDS_CONTROLLER_PROP));
        }
    }

    if (SUCCEEDED(hResult)) 
    {
        *ppController = pController;
    }

    _SafeRelease(pEnumController);
    return hResult;
}
```



## <a name="related-topics"></a>См. также

<dl> <dt>

[Использование VDS](using-vds.md)
</dt> <dt>

[Вспомогательные объекты](helper-objects.md)
</dt> <dt>

[**иенумвдсобжект**](/windows/desktop/api/Vds/nn-vds-ienumvdsobject)
</dt> <dt>

[**ивдссубсистем**](/windows/desktop/api/Vds/nn-vds-ivdssubsystem)
</dt> </dl>

 

 
