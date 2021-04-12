---
title: Основные сведения о приложениях
description: Основные сведения о приложениях
ms.assetid: 5593d27e-e97d-4f03-99ff-aee856abec8e
keywords:
- Windows Media Format SDK, основы приложений DRM
- Управление цифровыми правами (DRM), основы приложений
- DRM (Управление цифровыми правами), основы приложений
- Управление цифровыми правами (DRM), функция Вмдрмстартуп
- DRM (Управление цифровыми правами), функция Вмдрмстартуп
- вмдрмстартуп
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 182a9e54e077c174c4f4cbe74ba392aa44ce5112
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104252824"
---
# <a name="application-basics"></a><span data-ttu-id="26a3f-109">Основные сведения о приложениях</span><span class="sxs-lookup"><span data-stu-id="26a3f-109">Application Basics</span></span>

<span data-ttu-id="26a3f-110">Существует дополнительная обработка, которую необходимо выполнить для любого приложения, использующего расширенные API клиента DRM Windows Media.</span><span class="sxs-lookup"><span data-stu-id="26a3f-110">There is some extra processing that you must perform for any application that uses the Windows Media DRM Client Extended APIs.</span></span> <span data-ttu-id="26a3f-111">В этом разделе описываются требования для простого приложения.</span><span class="sxs-lookup"><span data-stu-id="26a3f-111">This topic describes the requirements for a simple application.</span></span>

<span data-ttu-id="26a3f-112">Во-первых, необходимо инициализировать расширенные API клиента DRM Windows Media, вызвав функцию [**вмдрмстартуп**](wmdrmstartup.md) .</span><span class="sxs-lookup"><span data-stu-id="26a3f-112">First, you must initialize the Windows Media DRM Client Extended APIs by calling the [**WMDRMStartup**](wmdrmstartup.md) function.</span></span> <span data-ttu-id="26a3f-113">Объекты пакета SDK являются COM-объектами, но вам не нужно вызывать **коинтиализе**, так как функция **ВМДРМСТАТУП** инициализирует COM для вас.</span><span class="sxs-lookup"><span data-stu-id="26a3f-113">The objects of the SDK are COM objects, but you do not need to call **CoIntialize**, because the **WMDRMStatup** function initializes COM for you.</span></span>

> [!Note]  
> <span data-ttu-id="26a3f-114">Пакет SDK для формата Windows Media использует только подмножество COM, поэтому при использовании COM-объектов, отличных от тех, которые находятся в расширенном API клиента DRM Windows Media, необходимо по-прежнему вызывать функцию **CoInitialize**.</span><span class="sxs-lookup"><span data-stu-id="26a3f-114">The Windows Media Format SDK uses only a subset of COM, so if you use COM objects other than those in the Windows Media DRM Client Extended API, you must still call **CoInitialize**.</span></span>

 

<span data-ttu-id="26a3f-115">Все объекты расширенных API клиента DRM Windows Media создаются с помощью вспомогательных функций и методов.</span><span class="sxs-lookup"><span data-stu-id="26a3f-115">All of the objects of the Windows Media DRM Client Extended APIs are created using helper functions and methods.</span></span> <span data-ttu-id="26a3f-116">Для создания объекта никогда не нужно вызывать **CoCreateInstance** .</span><span class="sxs-lookup"><span data-stu-id="26a3f-116">You never need to call **CoCreateInstance** to create an object.</span></span> <span data-ttu-id="26a3f-117">Первый интерфейс для создания экземпляра для любого приложения, использующего пакет SDK, — это [**ивмдрмпровидер**](iwmdrmprovider.md), который можно использовать для создания экземпляров всех других базовых интерфейсов.</span><span class="sxs-lookup"><span data-stu-id="26a3f-117">The first interface to instantiate for any application that uses the SDK is [**IWMDRMProvider**](iwmdrmprovider.md), which you can use to instantiate all of the other base interfaces.</span></span> <span data-ttu-id="26a3f-118">Чтобы получить экземпляр **ивмдрмпровидер**, необходимо вызвать либо [**Вмдрмкреатепровидер**](wmdrmcreateprovider.md) , либо [**вмдрмкреатепротектедпровидер**](wmdrmcreateprotectedprovider.md).</span><span class="sxs-lookup"><span data-stu-id="26a3f-118">To get an instance of **IWMDRMProvider**, you must call either [**WMDRMCreateProvider**](wmdrmcreateprovider.md) or [**WMDRMCreateProtectedProvider**](wmdrmcreateprotectedprovider.md).</span></span> <span data-ttu-id="26a3f-119">Разница между этими функциями заключается в том, что **вмдрмкреатепровидер** создает объект, который, в свою очередь, может создавать только те объекты, которые не поддерживают методы, требующие наличия библиотеки-заглушки.</span><span class="sxs-lookup"><span data-stu-id="26a3f-119">The difference between these functions is that **WMDRMCreateProvider** creates an object that can in turn create only objects that do not support methods that require the stub library.</span></span>

<span data-ttu-id="26a3f-120">После создания экземпляра **ивмдрмпровидер** можно создать другие необходимые объекты, вызвав [**Ивмдрмпровидер:: CreateObject**](iwmdrmprovider-createobject.md).</span><span class="sxs-lookup"><span data-stu-id="26a3f-120">After you have an instance of **IWMDRMProvider**, you can create the other objects that you need by calling [**IWMDRMProvider::CreateObject**](iwmdrmprovider-createobject.md).</span></span>

<span data-ttu-id="26a3f-121">Когда вы будете готовы выйти из приложения, необходимо освободить ресурсы подсистемы DRM, вызвав функцию [**вмдрмшутдовн**](wmdrmshutdown.md) .</span><span class="sxs-lookup"><span data-stu-id="26a3f-121">When you are ready to exit your application, you must release the DRM subsystem resources by calling the [**WMDRMShutdown**](wmdrmshutdown.md) function.</span></span> <span data-ttu-id="26a3f-122">Эта функция также завершает работу COM.</span><span class="sxs-lookup"><span data-stu-id="26a3f-122">This function also shuts down COM for you.</span></span>

<span data-ttu-id="26a3f-123">В следующем примере кода показано, как инициализировать и завершить приложение, которое использует расширенные API клиента DRM Windows Media.</span><span class="sxs-lookup"><span data-stu-id="26a3f-123">The following code example demonstrates how to initialize and conclude an application that uses the Windows Media DRM Client Extended APIs.</span></span>


```C++
#include <wmdrmsdk.h>
// TODO: Include other headers here as needed.

// This example demonstrates the code required in a single, simple
// main function. You will most likely break this code up into appropriate
// functions.
void main(void)
{
    HRESULT hr = S_OK;

    IWMDRMProvider*     pProvider     = NULL;
    // For the sake of example, this code will instantiate the
    //  IWMDRMLicenseQuery interface. The process is the same for the
    //  other base interfaces.
    IWMDRMLicenseQuery* pLicenseQuery = NULL;

    // Initialize the DRM subsystem.
    hr = WMDRMStartup();

    // Create a provider object, that can be used to create the other
    //  objects.
    if (SUCCEEDED(hr))
    {
        hr = WMDRMCreateProvider(&pProvider);
    }

    if(SUCCEEDED(hr))
    {
        hr = pProvider->CreateObject(
            IID_IWMDRMLicenseQuery, 
            (void**)&pLicenseQuery);
    }

    // TODO: Use the methods of IWMDRMLicenseQuery as required.

    // Cleanup and shutdown.
    SAFE_RELEASE(pLicenseQuery);
    SAFE_RELEASE(pProvider);

    hr = WMDRMShutdown();
}
```



## <a name="related-topics"></a><span data-ttu-id="26a3f-124">См. также</span><span class="sxs-lookup"><span data-stu-id="26a3f-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="26a3f-125">**начало работы**</span><span class="sxs-lookup"><span data-stu-id="26a3f-125">**Getting Started**</span></span>](drm-getting-started.md)
</dt> </dl>

 

 




