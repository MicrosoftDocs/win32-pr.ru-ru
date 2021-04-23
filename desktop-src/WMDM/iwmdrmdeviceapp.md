---
title: Интерфейс Ивмдрмдевицеапп
description: Интерфейс Ивмдрмдевицеапп позволяет приложению отслеживать, синхронизировать лицензии и обновлять компоненты DRM устройства.
ms.assetid: e47167c2-ea14-4173-8ce9-8d8540a0fc73
keywords:
- Интерфейс Ивмдрмдевицеапп Windows Media диспетчер устройств
- Интерфейс Ивмдрмдевицеапп Windows Media диспетчер устройств, описание
topic_type:
- apiref
api_name:
- IWMDRMDeviceApp
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 9cf44295c9972d7549eb4a82fda7c415ba81c31d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "105691626"
---
# <a name="iwmdrmdeviceapp-interface"></a><span data-ttu-id="2a299-105">Интерфейс Ивмдрмдевицеапп</span><span class="sxs-lookup"><span data-stu-id="2a299-105">IWMDRMDeviceApp interface</span></span>

<span data-ttu-id="2a299-106">\[Компонент Windows Media DRM является устаревшим и не должен использоваться.</span><span class="sxs-lookup"><span data-stu-id="2a299-106">\[The Windows Media DRM feature is deprecated and should not be used.</span></span> <span data-ttu-id="2a299-107">Вместо этого используйте [Microsoft PlayReady](/windows/uwp/audio-video-camera/playready-client-sdk) .\]</span><span class="sxs-lookup"><span data-stu-id="2a299-107">Use [Microsoft PlayReady](/windows/uwp/audio-video-camera/playready-client-sdk) instead.\]</span></span>

<span data-ttu-id="2a299-108">Интерфейс **ивмдрмдевицеапп** позволяет приложению отслеживать, синхронизировать лицензии и обновлять компоненты DRM устройства.</span><span class="sxs-lookup"><span data-stu-id="2a299-108">The **IWMDRMDeviceApp** interface enables an application to meter, synchronize licenses, and update a device's DRM components.</span></span> <span data-ttu-id="2a299-109">Этот интерфейс будет работать только с устройствами, поддерживающими Windows Media DRM 10 для переносных устройств.</span><span class="sxs-lookup"><span data-stu-id="2a299-109">This interface will only work with devices that support Windows Media DRM 10 for Portable Devices.</span></span>

<span data-ttu-id="2a299-110">Чтобы получить этот интерфейс, вызовите **CoCreateInstance**, передав CLSID \_ вмдрмдевицеапп.</span><span class="sxs-lookup"><span data-stu-id="2a299-110">To get this interface, call **CoCreateInstance**, passing in CLSID\_WMDRMDeviceApp.</span></span>

> [!Note]  
> <span data-ttu-id="2a299-111">Этот интерфейс определен в файле заголовка, созданном из Вмдрмдевицеапп. idl.</span><span class="sxs-lookup"><span data-stu-id="2a299-111">This interface is defined in the header file built from WMDRMDeviceApp.idl.</span></span> <span data-ttu-id="2a299-112">Этот заголовок **\# включает** s "вмдм. h".</span><span class="sxs-lookup"><span data-stu-id="2a299-112">This header **\#include** s "wmdm.h".</span></span> <span data-ttu-id="2a299-113">Может потребоваться изменить это имя файла в соответствии с заголовком, созданным из ВМДМ. idl.</span><span class="sxs-lookup"><span data-stu-id="2a299-113">You might need to change this file name to match the header built from WMDM.idl.</span></span>

 

## <a name="members"></a><span data-ttu-id="2a299-114">Элементы</span><span class="sxs-lookup"><span data-stu-id="2a299-114">Members</span></span>

<span data-ttu-id="2a299-115">Интерфейс **ивмдрмдевицеапп** наследует от интерфейса [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="2a299-115">The **IWMDRMDeviceApp** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="2a299-116">**Ивмдрмдевицеапп** также имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="2a299-116">**IWMDRMDeviceApp** also has these types of members:</span></span>

-   [<span data-ttu-id="2a299-117">Методы</span><span class="sxs-lookup"><span data-stu-id="2a299-117">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="2a299-118">Методы</span><span class="sxs-lookup"><span data-stu-id="2a299-118">Methods</span></span>

<span data-ttu-id="2a299-119">Интерфейс **ивмдрмдевицеапп** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="2a299-119">The **IWMDRMDeviceApp** interface has these methods.</span></span>



| <span data-ttu-id="2a299-120">Метод</span><span class="sxs-lookup"><span data-stu-id="2a299-120">Method</span></span>                                                                   | <span data-ttu-id="2a299-121">Описание</span><span class="sxs-lookup"><span data-stu-id="2a299-121">Description</span></span>                                                                                                                                |
|:-------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="2a299-122">**аккуиредевицедата**</span><span class="sxs-lookup"><span data-stu-id="2a299-122">**AcquireDeviceData**</span></span>](iwmdrmdeviceapp-acquiredevicedata.md)           | <span data-ttu-id="2a299-123">Инициализирует или сбрасывает защищенные часы устройства</span><span class="sxs-lookup"><span data-stu-id="2a299-123">Initializes or resets a device secure clock</span></span><br/>                                                                                     |
| [<span data-ttu-id="2a299-124">**женератеметерчалленже**</span><span class="sxs-lookup"><span data-stu-id="2a299-124">**GenerateMeterChallenge**</span></span>](iwmdrmdeviceapp-generatemeterchallenge.md) | <span data-ttu-id="2a299-125">Получение данных отслеживания использования с устройства.</span><span class="sxs-lookup"><span data-stu-id="2a299-125">Acquires metering data from a device.</span></span><br/>                                                                                           |
| [<span data-ttu-id="2a299-126">**процессметерреспонсе**</span><span class="sxs-lookup"><span data-stu-id="2a299-126">**ProcessMeterResponse**</span></span>](iwmdrmdeviceapp-processmeterresponse.md)     | <span data-ttu-id="2a299-127">Сбрасывает некоторые или все счетчики контроля использования на устройстве, после того как данные с устройства отправлены и обработаны сервером.</span><span class="sxs-lookup"><span data-stu-id="2a299-127">Resets some or all of the metering counts on a device, after data from the device has been sent to and processed by the server.</span></span><br/> |
| [<span data-ttu-id="2a299-128">**куеридевицестатус**</span><span class="sxs-lookup"><span data-stu-id="2a299-128">**QueryDeviceStatus**</span></span>](iwmdrmdeviceapp-querydevicestatus.md)           | <span data-ttu-id="2a299-129">Запрашивает у устройства текущее состояние DRM и возможности.</span><span class="sxs-lookup"><span data-stu-id="2a299-129">Queries a device for its current DRM status and capabilities.</span></span><br/>                                                                   |
| [<span data-ttu-id="2a299-130">**синчронизелиценсес**</span><span class="sxs-lookup"><span data-stu-id="2a299-130">**SynchronizeLicenses**</span></span>](iwmdrmdeviceapp-synchronizelicenses.md)       | <span data-ttu-id="2a299-131">Обновляет лицензии на устройстве, когда срок их действия скоро истечет.</span><span class="sxs-lookup"><span data-stu-id="2a299-131">Updates licenses on a device when they are close to expiring.</span></span><br/>                                                                   |



 

## <a name="see-also"></a><span data-ttu-id="2a299-132">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="2a299-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2a299-133">**Обработка защищенного содержимого в приложении**</span><span class="sxs-lookup"><span data-stu-id="2a299-133">**Handling Protected Content in the Application**</span></span>](handling-protected-content-in-the-application.md)
</dt> <dt>

[<span data-ttu-id="2a299-134">**Интерфейсы для приложений**</span><span class="sxs-lookup"><span data-stu-id="2a299-134">**Interfaces for Applications**</span></span>](interfaces-for-applications.md)
</dt> <dt>

[<span data-ttu-id="2a299-135">**Использование содержимого измерения**</span><span class="sxs-lookup"><span data-stu-id="2a299-135">**Metering Content Usage**</span></span>](metering-content-usage.md)
</dt> </dl>

 

