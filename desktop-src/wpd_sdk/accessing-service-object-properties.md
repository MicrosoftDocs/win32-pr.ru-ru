---
description: Доступ к свойствам объекта службы
ms.assetid: 66d9802b-ad28-47a4-8151-9df7aff07d61
title: Доступ к свойствам объекта службы
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 028ffc178f29f21aa60295b137b48c0fa2357a28
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105692222"
---
# <a name="accessing-service-object-properties"></a><span data-ttu-id="431c2-103">Доступ к свойствам объекта службы</span><span class="sxs-lookup"><span data-stu-id="431c2-103">Accessing Service Object Properties</span></span>

<span data-ttu-id="431c2-104">Приложение может считывать и записывать свойства для одного объекта в службе, для нескольких объектов, идентифицируемых идентификаторами объектов, или для нескольких объектов одного типа.</span><span class="sxs-lookup"><span data-stu-id="431c2-104">An application can read and write properties for a single object on a service, for multiple objects identified by object identifiers, or for multiple objects of the same type.</span></span> <span data-ttu-id="431c2-105">В разделе [Получение свойств объекта](retrieving-content-object-properties.md) описывается чтение свойств для одного объекта службы.</span><span class="sxs-lookup"><span data-stu-id="431c2-105">The [Retrieving Object Properties](retrieving-content-object-properties.md) topic describes reading properties for a single object on a service.</span></span> <span data-ttu-id="431c2-106">В разделе « [запись свойств объекта](writing-content-object-properties.md) » описывается запись свойств для одного объекта в службе.</span><span class="sxs-lookup"><span data-stu-id="431c2-106">The [Writing Object Properties](writing-content-object-properties.md) topic describes writing properties for a single object on a service.</span></span>

<span data-ttu-id="431c2-107">Описание получения свойств для нескольких объектов см. в разделе " [Расширенные задачи](advanced-tasks.md) ".</span><span class="sxs-lookup"><span data-stu-id="431c2-107">Refer to the [Advanced Tasks](advanced-tasks.md) section for a description of property retrieval for multiple objects.</span></span>

## <a name="when-to-use-service-property-definitions"></a><span data-ttu-id="431c2-108">Когда следует использовать определения свойств службы</span><span class="sxs-lookup"><span data-stu-id="431c2-108">When to use Service Property Definitions</span></span>

<span data-ttu-id="431c2-109">Вызовы API WPD, используемые для получения и установки свойств объекта для службы, совпадают с вызовами для получения свойств объекта для устройства (например, "получение свойств для одного объекта").</span><span class="sxs-lookup"><span data-stu-id="431c2-109">The WPD API calls used for retrieving and setting object properties for a service are the same as the calls for retrieving object properties for a device (compare "Retrieving Properties for a Single Object" for an example).</span></span> <span data-ttu-id="431c2-110">Основное отличие заключается в том, что для запроса свойств объекта используется другой набор Пропертикэйс.</span><span class="sxs-lookup"><span data-stu-id="431c2-110">The key difference is that a different set of PROPERTYKEYs are used to query object properties.</span></span> <span data-ttu-id="431c2-111">Для Впдсервицеаписампле используются Пропертикэйс службы устройств (например, **\_ \_ имя PKEY женерикобж**). для впдаписампле используются WPD пропертикэйс (например, **\_ \_ имя объекта WPD**).</span><span class="sxs-lookup"><span data-stu-id="431c2-111">For the WpdServiceApiSample, device service PROPERTYKEYs are used (such as **PKEY\_GenericObj\_Name**); for the WpdApiSample, WPD PROPERTYKEYs are used (such as **WPD\_OBJECT\_NAME**).</span></span>

<span data-ttu-id="431c2-112">Пропертикэйс службы устройств определяются в Бриджедевицесервицес. h (входит в состав каждого файла заголовка службы) и представляют общий набор ПРОПЕРТИКЭЙС, используемых приложениями служб устройств и реализацией встроенного по на устройстве.</span><span class="sxs-lookup"><span data-stu-id="431c2-112">Device service PROPERTYKEYs are defined in BridgeDeviceServices.h (included by each service header file), and represent the common set of PROPERTYKEYS employed by both device services applications and the firmware implementation on the device.</span></span> <span data-ttu-id="431c2-113">Это обеспечивает согласованный набор определений в стеке устройств с минимальным переводом, группирует Пропертикэйс на основе службы и позволяет более легко определять новые службы без необходимости обновлять схему WPD.</span><span class="sxs-lookup"><span data-stu-id="431c2-113">This allows a consistent set of definitions throughout the device stack with minimal translation, groups PROPERTYKEYs based on the service, and enables new services to be more easily defined without having to update the WPD schema.</span></span>

<span data-ttu-id="431c2-114">Используемый набор Пропертикэйс будет зависеть от потребностей вашего приложения:</span><span class="sxs-lookup"><span data-stu-id="431c2-114">The set of PROPERTYKEYs used will depend on your application's needs:</span></span>

-   <span data-ttu-id="431c2-115">Если приложение взаимодействует с устройством путем вызова [**ипортабледевице:: Open**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-open), используйте пропертикэйс, определенный в портабледевице. h.</span><span class="sxs-lookup"><span data-stu-id="431c2-115">If your application is communicating with the device by calling [**IPortableDevice::Open**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-open), use the PROPERTYKEYs defined in PortableDevice.h.</span></span> <span data-ttu-id="431c2-116">Примером такого приложения является Впдаписампле.</span><span class="sxs-lookup"><span data-stu-id="431c2-116">An example of such an application is the WpdApiSample.</span></span>
-   <span data-ttu-id="431c2-117">Если приложение взаимодействует со службами устройств путем вызова [**ипортабледевицесервице:: Open**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservice-open), используйте пропертикэйс, определенный в бриджедевицесервицес. h.</span><span class="sxs-lookup"><span data-stu-id="431c2-117">If your application is communicating with device services by calling [**IPortableDeviceService::Open**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservice-open), use the PROPERTYKEYS defined in BridgeDeviceServices.h.</span></span> <span data-ttu-id="431c2-118">Примером такого приложения является Впдсервицесаписампле.</span><span class="sxs-lookup"><span data-stu-id="431c2-118">An example of such an application is the WpdServicesApiSample.</span></span>
-   <span data-ttu-id="431c2-119">Если вы создаете сложное приложение, которое должно поддерживать гибридные службы устройств и устройства (это означает, что приложение вызывает и **ипортабледевице:: Open** и **Ипортабледевицесервице:: Open**), то при использовании ипортабледевице и его производных интерфейсов необходимо использовать пропертикэйс WPD, а служба устройств Пропертикэйс — при использовании [IPortableDeviceService](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservice) и ее производных интерфейсов.</span><span class="sxs-lookup"><span data-stu-id="431c2-119">If you are writing a complex application that needs to support a hybrid of both device services and the device (this means your application calls both **IPortableDevice::Open** and **IPortableDeviceService::Open**), you will need to use the WPD PROPERTYKEYs when using IPortableDevice and its derived interfaces, and device service PROPERTYKEYs when using [IPortableDeviceService](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservice) and its derived interfaces.</span></span>

<span data-ttu-id="431c2-120">Большинство приложений WPD должны относиться к первой или второй категории.</span><span class="sxs-lookup"><span data-stu-id="431c2-120">Most WPD applications should fall into the first or second category.</span></span>

## <a name="related-topics"></a><span data-ttu-id="431c2-121">См. также</span><span class="sxs-lookup"><span data-stu-id="431c2-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="431c2-122">**IPortableDeviceContent2**</span><span class="sxs-lookup"><span data-stu-id="431c2-122">**IPortableDeviceContent2**</span></span>](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledevicecontent2)
</dt> <dt>

[<span data-ttu-id="431c2-123">**ипортабледевицепропертиес**</span><span class="sxs-lookup"><span data-stu-id="431c2-123">**IPortableDeviceProperties**</span></span>](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledeviceproperties)
</dt> <dt>

[<span data-ttu-id="431c2-124">Получение свойств объекта</span><span class="sxs-lookup"><span data-stu-id="431c2-124">Retrieving Object Properties</span></span>](retrieving-content-object-properties.md)
</dt> <dt>

[<span data-ttu-id="431c2-125">Запись свойств объекта</span><span class="sxs-lookup"><span data-stu-id="431c2-125">Writing Object Properties</span></span>](writing-content-object-properties.md)
</dt> <dt>

[<span data-ttu-id="431c2-126">впдсервицесаписампле</span><span class="sxs-lookup"><span data-stu-id="431c2-126">WpdServicesApiSample</span></span>](wpdapisample-sample-service-application.md)
</dt> </dl>

 

 



