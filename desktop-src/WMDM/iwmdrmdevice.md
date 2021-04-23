---
title: Интерфейс Ивмдрмдевице
description: Этот интерфейс не предназначен для реализации поставщиком услуг, но предоставляется в целях полной документации. Интерфейс Ивмдрмдевице позволяет поставщику защищенного содержимого взаимодействовать с устройствами, использующими Windows Media DRM 10 для переносных устройств.
ms.assetid: ebad4acd-16cc-433f-a5e0-fcae59030f55
keywords:
- Интерфейс Ивмдрмдевице Windows Media диспетчер устройств
- Интерфейс Ивмдрмдевице Windows Media диспетчер устройств, описание
topic_type:
- apiref
api_name:
- IWMDRMDevice
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ca240f01f552dfdedb0145e49f61f2ead1f18832
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104337929"
---
# <a name="iwmdrmdevice-interface"></a><span data-ttu-id="b7374-105">Интерфейс Ивмдрмдевице</span><span class="sxs-lookup"><span data-stu-id="b7374-105">IWMDRMDevice interface</span></span>

<span data-ttu-id="b7374-106">Этот интерфейс не предназначен для реализации поставщиком услуг, но предоставляется в целях полной документации.</span><span class="sxs-lookup"><span data-stu-id="b7374-106">This interface is not intended to be implemented by a service provider, but is provided for purposes of complete documentation.</span></span>

<span data-ttu-id="b7374-107">Интерфейс **ивмдрмдевице** позволяет поставщику защищенного содержимого взаимодействовать с устройствами, использующими Windows Media DRM 10 для переносных устройств.</span><span class="sxs-lookup"><span data-stu-id="b7374-107">The **IWMDRMDevice** interface enables a secure content provider to communicate with devices that use Windows Media DRM 10 for Portable Devices.</span></span>

## <a name="members"></a><span data-ttu-id="b7374-108">Элементы</span><span class="sxs-lookup"><span data-stu-id="b7374-108">Members</span></span>

<span data-ttu-id="b7374-109">Интерфейс **ивмдрмдевице** наследует от интерфейса [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="b7374-109">The **IWMDRMDevice** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="b7374-110">**Ивмдрмдевице** также имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="b7374-110">**IWMDRMDevice** also has these types of members:</span></span>

-   [<span data-ttu-id="b7374-111">Методы</span><span class="sxs-lookup"><span data-stu-id="b7374-111">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="b7374-112">Методы</span><span class="sxs-lookup"><span data-stu-id="b7374-112">Methods</span></span>

<span data-ttu-id="b7374-113">Интерфейс **ивмдрмдевице** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="b7374-113">The **IWMDRMDevice** interface has these methods.</span></span>



| <span data-ttu-id="b7374-114">Метод</span><span class="sxs-lookup"><span data-stu-id="b7374-114">Method</span></span>                                                                  | <span data-ttu-id="b7374-115">Описание</span><span class="sxs-lookup"><span data-stu-id="b7374-115">Description</span></span>                                                                                  |
|:------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b7374-116">**клеандатасторе**</span><span class="sxs-lookup"><span data-stu-id="b7374-116">**CleanDataStore**</span></span>](iwmdrmdevice-cleandatastore.md)                   | <span data-ttu-id="b7374-117">Запускает процесс очистки хранилища данных DRM на устройстве.</span><span class="sxs-lookup"><span data-stu-id="b7374-117">Starts the process of cleaning the DRM data store on the device.</span></span><br/>                  |
| [<span data-ttu-id="b7374-118">**жетдевицецертификате**</span><span class="sxs-lookup"><span data-stu-id="b7374-118">**GetDeviceCertificate**</span></span>](iwmdrmdevice-getdevicecertificate.md)       | <span data-ttu-id="b7374-119">Извлекает сертификат устройства.</span><span class="sxs-lookup"><span data-stu-id="b7374-119">Retrieves the device certificate.</span></span><br/>                                                 |
| [<span data-ttu-id="b7374-120">**жетметерчалленже**</span><span class="sxs-lookup"><span data-stu-id="b7374-120">**GetMeterChallenge**</span></span>](iwmdrmdevice-getmeterchallenge.md)             | <span data-ttu-id="b7374-121">Извлекает запрос контроля использования.</span><span class="sxs-lookup"><span data-stu-id="b7374-121">Retrieves the metering challenge.</span></span><br/>                                                 |
| [<span data-ttu-id="b7374-122">**жетсекуреклокк**</span><span class="sxs-lookup"><span data-stu-id="b7374-122">**GetSecureClock**</span></span>](iwmdrmdevice-getsecureclock.md)                   | <span data-ttu-id="b7374-123">Извлекает безопасное время.</span><span class="sxs-lookup"><span data-stu-id="b7374-123">Retrieves the secure clock.</span></span><br/>                                                       |
| [<span data-ttu-id="b7374-124">**жетсекуреклоккчалленже**</span><span class="sxs-lookup"><span data-stu-id="b7374-124">**GetSecureClockChallenge**</span></span>](iwmdrmdevice-getsecureclockchallenge.md) | <span data-ttu-id="b7374-125">Получает запрос на безопасное время.</span><span class="sxs-lookup"><span data-stu-id="b7374-125">Retrieves the secure clock challenge.</span></span><br/>                                             |
| [<span data-ttu-id="b7374-126">**жетсинклист**</span><span class="sxs-lookup"><span data-stu-id="b7374-126">**GetSyncList**</span></span>](iwmdrmdevice-getsynclist.md)                         | <span data-ttu-id="b7374-127">Извлекает список синхронизации лицензий.</span><span class="sxs-lookup"><span data-stu-id="b7374-127">Retrieves the license synchronization list.</span></span><br/>                                       |
| [<span data-ttu-id="b7374-128">**исвмдрмдевице**</span><span class="sxs-lookup"><span data-stu-id="b7374-128">**IsWMDRMDevice**</span></span>](iwmdrmdevice-iswmdrmdevice.md)                     | <span data-ttu-id="b7374-129">Определяет, поддерживает ли устройство Windows Media DRM 10 для переносных устройств.</span><span class="sxs-lookup"><span data-stu-id="b7374-129">Determines whether the device supports Windows Media DRM 10 for Portable Devices.</span></span><br/> |
| [<span data-ttu-id="b7374-130">**сетлиценсереспонсе**</span><span class="sxs-lookup"><span data-stu-id="b7374-130">**SetLicenseResponse**</span></span>](iwmdrmdevice-setlicenseresponse.md)           | <span data-ttu-id="b7374-131">Задает ответ лицензии.</span><span class="sxs-lookup"><span data-stu-id="b7374-131">Sets the license response.</span></span><br/>                                                        |
| [<span data-ttu-id="b7374-132">**сетметерреспонсе**</span><span class="sxs-lookup"><span data-stu-id="b7374-132">**SetMeterResponse**</span></span>](iwmdrmdevice-setmeterresponse.md)               | <span data-ttu-id="b7374-133">Задает ответ отслеживания.</span><span class="sxs-lookup"><span data-stu-id="b7374-133">Sets the metering response.</span></span><br/>                                                       |
| [<span data-ttu-id="b7374-134">**сетсекуреклоккреспонсе**</span><span class="sxs-lookup"><span data-stu-id="b7374-134">**SetSecureClockResponse**</span></span>](iwmdrmdevice-setsecureclockresponse.md)   | <span data-ttu-id="b7374-135">Задает отклик на безопасное время.</span><span class="sxs-lookup"><span data-stu-id="b7374-135">Sets the secure clock response.</span></span><br/>                                                   |



 

## <a name="see-also"></a><span data-ttu-id="b7374-136">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b7374-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b7374-137">**Интерфейсы для поставщиков услуг**</span><span class="sxs-lookup"><span data-stu-id="b7374-137">**Interfaces for Service Providers**</span></span>](interfaces-for-service-providers.md)
</dt> </dl>

 

