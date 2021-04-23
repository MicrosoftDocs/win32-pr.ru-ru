---
title: Объект регистрации устройства
description: Объект регистрации устройства
ms.assetid: 6a23b314-deec-47aa-b12e-cb8f4ff71fb6
keywords:
- Windows Media Format SDK, объекты регистрации устройств
- Расширенный формат систем (ASF), объекты регистрации устройств
- ASF (Расширенный системный формат), объекты регистрации устройств
- объекты, объекты регистрации устройств
- объекты регистрации устройств
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 67ba6b72637cf7ba439d0bb38109645742cda4ac
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/19/2020
ms.locfileid: "105691446"
---
# <a name="device-registration-object"></a><span data-ttu-id="8c049-108">Объект регистрации устройства</span><span class="sxs-lookup"><span data-stu-id="8c049-108">Device Registration Object</span></span>

<span data-ttu-id="8c049-109">Объект регистрации устройства управляет базой данных регистрации устройств.</span><span class="sxs-lookup"><span data-stu-id="8c049-109">The device registration object manages the device registration database.</span></span> <span data-ttu-id="8c049-110">В этой базе данных хранятся сведения о сетевых устройствах, таких как набор видеопроигрывателей Set-Top, которые подключены к клиентскому компьютеру.</span><span class="sxs-lookup"><span data-stu-id="8c049-110">This database stores information about network devices, such as set-top video players, that are connected to the client computer.</span></span> <span data-ttu-id="8c049-111">Основной целью базы данных регистрации устройств является управление устройствами, использующими протокол Windows Media DRM 10 для сетевых устройств, для получения защищенных потоков данных.</span><span class="sxs-lookup"><span data-stu-id="8c049-111">The primary purpose of the device registration database is to manage devices that use the Windows Media DRM 10 for Network Devices protocol to receive secured data streams.</span></span>

<span data-ttu-id="8c049-112">Если приложение поддерживает Windows Media DRM 10 для сетевых устройств, необходимо использовать интерфейсы этого объекта для регистрации сетевых устройств и проверки этих устройств.</span><span class="sxs-lookup"><span data-stu-id="8c049-112">If your application supports Windows Media DRM 10 for Network Devices, you must use the interfaces of this object to register network devices, and to validate those devices.</span></span> <span data-ttu-id="8c049-113">Вы также можете использовать базу данных регистрации устройств для хранения сведений о сетевых устройствах, которые не используют Windows Media DRM 10 для сетевых устройств, хотя не все сведения в базе данных будут применяться к таким устройствам.</span><span class="sxs-lookup"><span data-stu-id="8c049-113">You can also use the device registration database to store information about network devices that do not use Windows Media DRM 10 for Network Devices, although not all of the information in the database will apply to such devices.</span></span>

<span data-ttu-id="8c049-114">Объект регистрации устройства создается функцией [**вмкреатедевицерегистратион**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatedeviceregistration) , которая устанавливает указатель на интерфейс **ивмдевицерегистратион** .</span><span class="sxs-lookup"><span data-stu-id="8c049-114">The device registration object is created by the [**WMCreateDeviceRegistration**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatedeviceregistration) function, which sets a pointer to an **IWMDeviceRegistration** interface.</span></span> <span data-ttu-id="8c049-115">Другие методы объекта регистрации устройства можно получить, вызвав метод **QueryInterface** .</span><span class="sxs-lookup"><span data-stu-id="8c049-115">The other methods of the device registration object can be obtained by calling the **QueryInterface** method.</span></span>

<span data-ttu-id="8c049-116">Объект регистрации устройства поддерживает следующие интерфейсы.</span><span class="sxs-lookup"><span data-stu-id="8c049-116">The following interfaces are supported by the device registration object.</span></span>



| <span data-ttu-id="8c049-117">Интерфейс</span><span class="sxs-lookup"><span data-stu-id="8c049-117">Interface</span></span>                                              | <span data-ttu-id="8c049-118">Описание</span><span class="sxs-lookup"><span data-stu-id="8c049-118">Description</span></span>                               |
|--------------------------------------------------------|-------------------------------------------|
| [<span data-ttu-id="8c049-119">**ивмдевицерегистратион**</span><span class="sxs-lookup"><span data-stu-id="8c049-119">**IWMDeviceRegistration**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdeviceregistration) | <span data-ttu-id="8c049-120">Управляет базой данных регистрации устройств.</span><span class="sxs-lookup"><span data-stu-id="8c049-120">Manages the device registration database.</span></span> |
| [<span data-ttu-id="8c049-121">**ивмдрммессажепарсер**</span><span class="sxs-lookup"><span data-stu-id="8c049-121">**IWMDRMMessageParser**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmmessageparser)     | <span data-ttu-id="8c049-122">Анализирует сообщения, отправленные устройствами.</span><span class="sxs-lookup"><span data-stu-id="8c049-122">Parses messages sent by devices.</span></span>          |
| [<span data-ttu-id="8c049-123">**ивмпроксимитидетектион**</span><span class="sxs-lookup"><span data-stu-id="8c049-123">**IWMProximityDetection**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmproximitydetection) | <span data-ttu-id="8c049-124">Управляет проверкой устройств.</span><span class="sxs-lookup"><span data-stu-id="8c049-124">Manages device validation.</span></span>                |



 

<span data-ttu-id="8c049-125">Для использования методов интерфейса **ивмпроксимитидетектион** в приложении должен быть реализован следующий интерфейс обратного вызова.</span><span class="sxs-lookup"><span data-stu-id="8c049-125">The following callback interface must be implemented by the application in order to use the methods of the **IWMProximityDetection** interface.</span></span>



| <span data-ttu-id="8c049-126">Интерфейс</span><span class="sxs-lookup"><span data-stu-id="8c049-126">Interface</span></span>                                      | <span data-ttu-id="8c049-127">Описание</span><span class="sxs-lookup"><span data-stu-id="8c049-127">Description</span></span>                                                                |
|------------------------------------------------|----------------------------------------------------------------------------|
| [<span data-ttu-id="8c049-128">**ивмстатускаллбакк**</span><span class="sxs-lookup"><span data-stu-id="8c049-128">**IWMStatusCallback**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstatuscallback) | <span data-ttu-id="8c049-129">Получает сообщения о состоянии от процессов, выполняемых в отдельном потоке.</span><span class="sxs-lookup"><span data-stu-id="8c049-129">Receives status messages from processes that execute in a separate thread.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="8c049-130">См. также</span><span class="sxs-lookup"><span data-stu-id="8c049-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8c049-131">**Объекты**</span><span class="sxs-lookup"><span data-stu-id="8c049-131">**Objects**</span></span>](objects.md)
</dt> </dl>

 

 




