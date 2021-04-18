---
description: Идет загрузка VDS
ms.assetid: 6b75fdb2-3d4c-4419-96e8-8677439e366b
title: Идет загрузка VDS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 01c66685668641f3036739c57bd7353f72052c6f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105693278"
---
# <a name="loading-vds"></a>Идет загрузка VDS

\[Начиная с Windows 8 и Windows Server 2012, интерфейс COM [службы виртуальных дисков](virtual-disk-service-portal.md) заменяется [API управления хранилищами Windows](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]

**Загрузка и инициализация VDS**

1.  Выпустите интерфейсы, отличные от NULL.
2.  Вызовите функцию [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance), [**кокреатеинстанцеекс**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstanceex)или [**кожетклассобжект**](/windows/win32/api/combaseapi/nf-combaseapi-cogetclassobject) , чтобы получить указатель на объект загрузчика службы.

    **Клскткс \_ В \_** этом вызове невозможно указать Disable AAA. Если вызывается [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) , **еоак \_ disable \_ AAA** нельзя указывать в параметре *двкапабилитиес* .

3.  Вызовите метод [**ивдссервицелоадер:: лоадсервице**](/windows/desktop/api/Vds/nf-vds-ivdsserviceloader-loadservice) , чтобы загрузить VDS.

    Передача **значения NULL** в качестве первого параметра загружает и инициализирует службу VDS на локальном узле.

4.  Вызовите метод [**ивдссервице:: ваитфорсервицереади**](/windows/desktop/api/Vds/nf-vds-ivdsservice-waitforserviceready) , чтобы дождаться завершения инициализации службы VDS.

В следующем примере кода инициализируется служба, которая возвращает указатель на объект службы.


```C++
#include "initguid.h"
#include "vds.h"
#include <stdio.h>

#pragma comment( lib, "ole32.lib" )

//
// Simple macro to release non-null interfaces.
//
#define _SafeRelease(x) {if (NULL != x) { x->Release(); x = NULL; } }

void __cdecl main(void) 
{
    HRESULT hResult;
    IVdsService *pService = NULL;
    IVdsServiceLoader *pLoader = NULL;

    // For this, you first get a pointer to the VDS Loader
    // Launch the VDS service. 
    //

    hResult = CoInitialize(NULL);

    if (SUCCEEDED(hResult)) 
    {
    
        hResult = CoCreateInstance(CLSID_VdsLoader,
            NULL,
            CLSCTX_LOCAL_SERVER,
            IID_IVdsServiceLoader,
            (void **) &pLoader);

        // 
        // And then load VDS on the local computer.
        //
        if (SUCCEEDED(hResult)) 
        {
            hResult = pLoader->LoadService(NULL, &pService);
        }

        //
        // You're done with the Loader interface at this point.
        //
        _SafeRelease(pLoader); 
        
        if (SUCCEEDED(hResult)) 
        {
            hResult = pService->WaitForServiceReady();
            if (SUCCEEDED(hResult)) 
            {
                //
                // You obtained an interface to the service: pService.
                // This interface can now be used to query for providers 
                // and perform other operations. 
                //
                printf("VDS Service Loaded");
            }

        } 
        else 
        {
            printf("VDS Service failed hr=%x\n",hResult);
        }
    }
}

```



## <a name="related-topics"></a>См. также

<dl> <dt>

[Использование VDS](using-vds.md)
</dt> <dt>

[**Ивдссервице:: Ваитфорсервицереади**](/windows/desktop/api/Vds/nf-vds-ivdsservice-waitforserviceready)
</dt> <dt>

[**Ивдссервицелоадер:: Лоадсервице**](/windows/desktop/api/Vds/nf-vds-ivdsserviceloader-loadservice)
</dt> <dt>

[Объекты установки и службы](startup-and-service-objects.md)
</dt> </dl>

 

 
