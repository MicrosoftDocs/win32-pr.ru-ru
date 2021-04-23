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
# <a name="loading-vds"></a><span data-ttu-id="ae2f8-103">Идет загрузка VDS</span><span class="sxs-lookup"><span data-stu-id="ae2f8-103">Loading VDS</span></span>

<span data-ttu-id="ae2f8-104">\[Начиная с Windows 8 и Windows Server 2012, интерфейс COM [службы виртуальных дисков](virtual-disk-service-portal.md) заменяется [API управления хранилищами Windows](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]</span><span class="sxs-lookup"><span data-stu-id="ae2f8-104">\[Beginning with Windows 8 and Windows Server 2012, the [Virtual Disk Service](virtual-disk-service-portal.md) COM interface is superseded by the [Windows Storage Management API](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]</span></span>

<span data-ttu-id="ae2f8-105">**Загрузка и инициализация VDS**</span><span class="sxs-lookup"><span data-stu-id="ae2f8-105">**To load and initialize VDS**</span></span>

1.  <span data-ttu-id="ae2f8-106">Выпустите интерфейсы, отличные от NULL.</span><span class="sxs-lookup"><span data-stu-id="ae2f8-106">Release non-null interfaces.</span></span>
2.  <span data-ttu-id="ae2f8-107">Вызовите функцию [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance), [**кокреатеинстанцеекс**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstanceex)или [**кожетклассобжект**](/windows/win32/api/combaseapi/nf-combaseapi-cogetclassobject) , чтобы получить указатель на объект загрузчика службы.</span><span class="sxs-lookup"><span data-stu-id="ae2f8-107">Call the [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance), [**CoCreateInstanceEx**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstanceex), or [**CoGetClassObject**](/windows/win32/api/combaseapi/nf-combaseapi-cogetclassobject) function to obtain a pointer to the service loader object.</span></span>

    <span data-ttu-id="ae2f8-108">**Клскткс \_ В \_** этом вызове невозможно указать Disable AAA.</span><span class="sxs-lookup"><span data-stu-id="ae2f8-108">**CLSCTX\_DISABLE\_AAA** cannot be specified in this call.</span></span> <span data-ttu-id="ae2f8-109">Если вызывается [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) , **еоак \_ disable \_ AAA** нельзя указывать в параметре *двкапабилитиес* .</span><span class="sxs-lookup"><span data-stu-id="ae2f8-109">If [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) is called, **EOAC\_DISABLE\_AAA** cannot be specified in the *dwCapabilities* parameter.</span></span>

3.  <span data-ttu-id="ae2f8-110">Вызовите метод [**ивдссервицелоадер:: лоадсервице**](/windows/desktop/api/Vds/nf-vds-ivdsserviceloader-loadservice) , чтобы загрузить VDS.</span><span class="sxs-lookup"><span data-stu-id="ae2f8-110">Call the [**IVdsServiceLoader::LoadService**](/windows/desktop/api/Vds/nf-vds-ivdsserviceloader-loadservice) method to load VDS.</span></span>

    <span data-ttu-id="ae2f8-111">Передача **значения NULL** в качестве первого параметра загружает и инициализирует службу VDS на локальном узле.</span><span class="sxs-lookup"><span data-stu-id="ae2f8-111">Passing **NULL** as the first parameter loads and initializes VDS on the local host.</span></span>

4.  <span data-ttu-id="ae2f8-112">Вызовите метод [**ивдссервице:: ваитфорсервицереади**](/windows/desktop/api/Vds/nf-vds-ivdsservice-waitforserviceready) , чтобы дождаться завершения инициализации службы VDS.</span><span class="sxs-lookup"><span data-stu-id="ae2f8-112">Call the [**IVdsService::WaitForServiceReady**](/windows/desktop/api/Vds/nf-vds-ivdsservice-waitforserviceready) method to wait for VDS initialization to complete.</span></span>

<span data-ttu-id="ae2f8-113">В следующем примере кода инициализируется служба, которая возвращает указатель на объект службы.</span><span class="sxs-lookup"><span data-stu-id="ae2f8-113">The following code example initializes the service that returns a pointer to the service object.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="ae2f8-114">См. также</span><span class="sxs-lookup"><span data-stu-id="ae2f8-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ae2f8-115">Использование VDS</span><span class="sxs-lookup"><span data-stu-id="ae2f8-115">Using VDS</span></span>](using-vds.md)
</dt> <dt>

[<span data-ttu-id="ae2f8-116">**Ивдссервице:: Ваитфорсервицереади**</span><span class="sxs-lookup"><span data-stu-id="ae2f8-116">**IVdsService::WaitForServiceReady**</span></span>](/windows/desktop/api/Vds/nf-vds-ivdsservice-waitforserviceready)
</dt> <dt>

[<span data-ttu-id="ae2f8-117">**Ивдссервицелоадер:: Лоадсервице**</span><span class="sxs-lookup"><span data-stu-id="ae2f8-117">**IVdsServiceLoader::LoadService**</span></span>](/windows/desktop/api/Vds/nf-vds-ivdsserviceloader-loadservice)
</dt> <dt>

[<span data-ttu-id="ae2f8-118">Объекты установки и службы</span><span class="sxs-lookup"><span data-stu-id="ae2f8-118">Setup and Service Objects</span></span>](startup-and-service-objects.md)
</dt> </dl>

 

 
