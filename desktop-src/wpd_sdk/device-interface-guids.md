---
description: Интерфейс устройства может быть описан с помощью значения GUID. Портативные устройства Windows определяют следующий интерфейс устройства.
ms.assetid: 47b8d3dd-ea12-461d-935d-2de2c0157f88
title: Идентификаторы GUID интерфейса устройства (Портабледевице. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GUID_DEVINTERFACE_WPD
- GUID_DEVINTERFACE_WPD_PRIVATE
- GUID_DEVINTERFACE_WPD_SERVICE
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: c2f97e050f839a268048aaaabac46b9e7698ee9d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105704511"
---
# <a name="device-interface-guids"></a><span data-ttu-id="bd67e-104">Идентификаторы GUID интерфейса устройства</span><span class="sxs-lookup"><span data-stu-id="bd67e-104">Device Interface GUIDs</span></span>

<span data-ttu-id="bd67e-105">Интерфейс устройства может быть описан с помощью значения **GUID** .</span><span class="sxs-lookup"><span data-stu-id="bd67e-105">The device interface can be described by a **GUID** value.</span></span> <span data-ttu-id="bd67e-106">Портативные устройства Windows определяют следующий интерфейс устройства.</span><span class="sxs-lookup"><span data-stu-id="bd67e-106">Windows Portable Devices defines the following device interface.</span></span>



| <span data-ttu-id="bd67e-107">Константа</span><span class="sxs-lookup"><span data-stu-id="bd67e-107">Constant</span></span>                                                                                                                                                                                                        | <span data-ttu-id="bd67e-108">Описание</span><span class="sxs-lookup"><span data-stu-id="bd67e-108">Description</span></span>                                                                                                                                                                                                                                                                                   |
|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GUID_DEVINTERFACE_WPD"></span><span id="guid_devinterface_wpd"></span><dl> <span data-ttu-id="bd67e-109"><dt>**GUID \_ девинтерфаце \_ WPD**</dt></span><span class="sxs-lookup"><span data-stu-id="bd67e-109"><dt>**GUID\_DEVINTERFACE\_WPD**</dt></span></span> </dl>                          | <span data-ttu-id="bd67e-110">Определяет устройства, которые отображаются в стандартном перечислении WPD.</span><span class="sxs-lookup"><span data-stu-id="bd67e-110">Identifies devices that appear in a normal WPD enumeration.</span></span> <span data-ttu-id="bd67e-111">Любое устройство, которое регистрирует этот GUID интерфейса, будет перечисляться, когда приложение вызывает метод [**ипортабледевицеманажер::**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicemanager-getdevices) GetEnumerator.</span><span class="sxs-lookup"><span data-stu-id="bd67e-111">Any device that registers this interface GUID will be enumerated when an application calls the [**IPortableDeviceManager::GetDevices**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicemanager-getdevices) method.</span></span><br/>                                 |
| <span id="GUID_DEVINTERFACE_WPD_PRIVATE"></span><span id="guid_devinterface_wpd_private"></span><dl> <span data-ttu-id="bd67e-112"><dt>**GUID \_ девинтерфаце \_ WPD \_ Private**</dt></span><span class="sxs-lookup"><span data-stu-id="bd67e-112"><dt>**GUID\_DEVINTERFACE\_WPD\_PRIVATE**</dt></span></span> </dl> | <span data-ttu-id="bd67e-113">Определяет устройства, которые не будут отображаться в стандартном перечислении WPD.</span><span class="sxs-lookup"><span data-stu-id="bd67e-113">Identifies devices that will not appear during a normal WPD enumeration.</span></span> <span data-ttu-id="bd67e-114">Любое устройство, которое регистрирует этот GUID интерфейса, будет перечисляться только в том случае, если приложение вызывает метод [**ипортабледевицеманажер:: жетприватедевицес**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicemanager-getprivatedevices) .</span><span class="sxs-lookup"><span data-stu-id="bd67e-114">Any device that registers this interface GUID will be enumerated only when an application calls the [**IPortableDeviceManager::GetPrivateDevices**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicemanager-getprivatedevices) method.</span></span><br/> |
| <span id="GUID_DEVINTERFACE_WPD_SERVICE"></span><span id="guid_devinterface_wpd_service"></span><dl> <span data-ttu-id="bd67e-115"><dt>**GUID \_ девинтерфаце \_ WPD \_ Service**</dt></span><span class="sxs-lookup"><span data-stu-id="bd67e-115"><dt>**GUID\_DEVINTERFACE\_WPD\_SERVICE**</dt></span></span> </dl> | <span data-ttu-id="bd67e-116">В Windows 7 приложения могут перечислять все службы устройств WPD, вызывая [**ипортабледевицесервицеманажер:: жетдевицесервицес**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicemanager-getdeviceservices) и используя этот класс интерфейса в качестве идентификатора GUID типа службы.</span><span class="sxs-lookup"><span data-stu-id="bd67e-116">In Windows 7, applications can enumerate all WPD device services by calling [**IPortableDeviceServiceManager::GetDeviceServices**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicemanager-getdeviceservices) and using this interface class as the service-type GUID.</span></span><br/>                                   |



## <a name="requirements"></a><span data-ttu-id="bd67e-117">Требования</span><span class="sxs-lookup"><span data-stu-id="bd67e-117">Requirements</span></span>



| <span data-ttu-id="bd67e-118">Требование</span><span class="sxs-lookup"><span data-stu-id="bd67e-118">Requirement</span></span> | <span data-ttu-id="bd67e-119">Значение</span><span class="sxs-lookup"><span data-stu-id="bd67e-119">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="bd67e-120">Header</span><span class="sxs-lookup"><span data-stu-id="bd67e-120">Header</span></span><br/> | <dl> <span data-ttu-id="bd67e-121"><dt>Портабледевице. h</dt></span><span class="sxs-lookup"><span data-stu-id="bd67e-121"><dt>PortableDevice.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bd67e-122">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="bd67e-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bd67e-123">Справочник по программированию</span><span class="sxs-lookup"><span data-stu-id="bd67e-123">Programming Reference</span></span>](programming-reference.md)
</dt> </dl>

 

 




