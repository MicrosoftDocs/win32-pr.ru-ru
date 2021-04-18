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
# <a name="working-with-enumeration-objects"></a><span data-ttu-id="e0996-103">Работа с объектами перечисления</span><span class="sxs-lookup"><span data-stu-id="e0996-103">Working with Enumeration Objects</span></span>

<span data-ttu-id="e0996-104">\[Начиная с Windows 8 и Windows Server 2012, интерфейс COM [службы виртуальных дисков](virtual-disk-service-portal.md) заменяется [API управления хранилищами Windows](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]</span><span class="sxs-lookup"><span data-stu-id="e0996-104">\[Beginning with Windows 8 and Windows Server 2012, the [Virtual Disk Service](virtual-disk-service-portal.md) COM interface is superseded by the [Windows Storage Management API](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]</span></span>

<span data-ttu-id="e0996-105">В следующем примере кода показано, как вызывающий объект работает с объектами перечисления с помощью интерфейса [**иенумвдсобжект**](/windows/desktop/api/Vds/nn-vds-ienumvdsobject) .</span><span class="sxs-lookup"><span data-stu-id="e0996-105">The code example that follows demonstrates how a caller works with enumeration objects using the [**IEnumVdsObject**](/windows/desktop/api/Vds/nn-vds-ienumvdsobject) interface.</span></span> <span data-ttu-id="e0996-106">Обратите внимание, что сведения, возвращаемые объектом перечисления, являются статическими.</span><span class="sxs-lookup"><span data-stu-id="e0996-106">Note that the information that is returned by a enumeration object is static.</span></span> <span data-ttu-id="e0996-107">Необходимо снова запросить объект, чтобы увидеть новые изменения конфигурации.</span><span class="sxs-lookup"><span data-stu-id="e0996-107">You must query the object again to see new configuration changes.</span></span>

<span data-ttu-id="e0996-108">Функция **жетконтроллербид** принимает интерфейс [**ивдссубсистем**](/windows/desktop/api/Vds/nn-vds-ivdssubsystem) , указанный параметром *псубсистем* , и запрашивает контроллеры в подсистеме, а затем выполняет итерацию по возвращенному перечислению, в котором выполняется поиск контроллера с идентификатором GUID, совпадающим с идентификатором GUID, указанным в параметре *пконтроллерид* .</span><span class="sxs-lookup"><span data-stu-id="e0996-108">The **GetControllerById** function takes an [**IVdsSubSystem**](/windows/desktop/api/Vds/nn-vds-ivdssubsystem) interface, specified by the *pSubsystem* parameter, and queries for the controllers in the subsystem, then iterates through the returned enumeration searching for a controller with a GUID that matches the GUID that is specified by the *pControllerId* parameter.</span></span> <span data-ttu-id="e0996-109">Если найден соответствующий контроллер, он возвращается с помощью параметра *ппконтроллер* вместе с параметром S \_ ОК **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="e0996-109">If a matching controller is found, it is returned by the *ppController* parameter along with an S\_OK **HRESULT**.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="e0996-110">См. также</span><span class="sxs-lookup"><span data-stu-id="e0996-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e0996-111">Использование VDS</span><span class="sxs-lookup"><span data-stu-id="e0996-111">Using VDS</span></span>](using-vds.md)
</dt> <dt>

[<span data-ttu-id="e0996-112">Вспомогательные объекты</span><span class="sxs-lookup"><span data-stu-id="e0996-112">Helper Objects</span></span>](helper-objects.md)
</dt> <dt>

[<span data-ttu-id="e0996-113">**иенумвдсобжект**</span><span class="sxs-lookup"><span data-stu-id="e0996-113">**IEnumVdsObject**</span></span>](/windows/desktop/api/Vds/nn-vds-ienumvdsobject)
</dt> <dt>

[<span data-ttu-id="e0996-114">**ивдссубсистем**</span><span class="sxs-lookup"><span data-stu-id="e0996-114">**IVdsSubSystem**</span></span>](/windows/desktop/api/Vds/nn-vds-ivdssubsystem)
</dt> </dl>

 

 
