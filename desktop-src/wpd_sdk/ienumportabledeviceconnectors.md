---
description: Поддерживает перечисление интерфейсов Ипортабледевицеконнектор, представляющих устройства MTP и Bluetooth, связанные с компьютером.
ms.assetid: 99aa1e89-5e20-4f6e-82b5-acf63305eba0
title: Интерфейс Иенумпортабледевицеконнекторс (Девпкэй. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEnumPortableDeviceConnectors
api_type:
- COM
api_location:
- PortableDeviceGuids.lib
- PortableDeviceGuids.dll
ms.openlocfilehash: 7c5340502c7653283e2ea1f2d02e35e7d1222f35
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104264550"
---
# <a name="ienumportabledeviceconnectors-interface"></a><span data-ttu-id="45fbc-103">Интерфейс Иенумпортабледевицеконнекторс</span><span class="sxs-lookup"><span data-stu-id="45fbc-103">IEnumPortableDeviceConnectors interface</span></span>

<span data-ttu-id="45fbc-104">Интерфейс **иенумпортабледевицеконнекторс** поддерживает перечисление интерфейсов [**ипортабледевицеконнектор**](/windows/desktop/api/portabledeviceconnectapi/nn-portabledeviceconnectapi-iportabledeviceconnector) , представляющих устройства MTP и Bluetooth, которые были парны с компьютером.</span><span class="sxs-lookup"><span data-stu-id="45fbc-104">The **IEnumPortableDeviceConnectors** interface supports the enumeration of [**IPortableDeviceConnector**](/windows/desktop/api/portabledeviceconnectapi/nn-portabledeviceconnectapi-iportabledeviceconnector) interfaces, representing MTP/Bluetooth devices that were paired with the PC.</span></span> <span data-ttu-id="45fbc-105">Обратите внимание, что при этом будут получены все ранее связанные устройства, включая устройства, которые связаны, но отключены.</span><span class="sxs-lookup"><span data-stu-id="45fbc-105">Note that this will retrieve all previously-paired devices, including devices that are paired but disconnected.</span></span> <span data-ttu-id="45fbc-106">Чтобы определить, подключено ли устройство, запросите **свойство \_ девпкэй \_ мтпбс** для этого устройства.</span><span class="sxs-lookup"><span data-stu-id="45fbc-106">To determine if a device is still connected, query the **DEVPKEY\_MTPBTH\_IsConnected** property for that device.</span></span>

## <a name="members"></a><span data-ttu-id="45fbc-107">Элементы</span><span class="sxs-lookup"><span data-stu-id="45fbc-107">Members</span></span>

<span data-ttu-id="45fbc-108">Интерфейс **иенумпортабледевицеконнекторс** наследует от интерфейса [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="45fbc-108">The **IEnumPortableDeviceConnectors** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="45fbc-109">**Иенумпортабледевицеконнекторс** также имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="45fbc-109">**IEnumPortableDeviceConnectors** also has these types of members:</span></span>

-   [<span data-ttu-id="45fbc-110">Методы</span><span class="sxs-lookup"><span data-stu-id="45fbc-110">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="45fbc-111">Методы</span><span class="sxs-lookup"><span data-stu-id="45fbc-111">Methods</span></span>

<span data-ttu-id="45fbc-112">Интерфейс **иенумпортабледевицеконнекторс** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="45fbc-112">The **IEnumPortableDeviceConnectors** interface has these methods.</span></span>



| <span data-ttu-id="45fbc-113">Метод</span><span class="sxs-lookup"><span data-stu-id="45fbc-113">Method</span></span>                                               | <span data-ttu-id="45fbc-114">Описание</span><span class="sxs-lookup"><span data-stu-id="45fbc-114">Description</span></span>                                                                                                                                 |
|:-----------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="45fbc-115">**Клонировать**</span><span class="sxs-lookup"><span data-stu-id="45fbc-115">**Clone**</span></span>](ienumportabledeviceconnectors-clone.md) | <span data-ttu-id="45fbc-116">Создает копию текущего интерфейса **иенумпортабледевицеконнекторс** .</span><span class="sxs-lookup"><span data-stu-id="45fbc-116">Creates a copy of the current **IEnumPortableDeviceConnectors** interface.</span></span><br/>                                                       |
| [<span data-ttu-id="45fbc-117">**Далее**</span><span class="sxs-lookup"><span data-stu-id="45fbc-117">**Next**</span></span>](ienumportabledeviceconnectors-next.md)   | <span data-ttu-id="45fbc-118">Извлекает следующий один или несколько объектов [**ипортабледевицеконнектор**](/windows/desktop/api/portabledeviceconnectapi/nn-portabledeviceconnectapi-iportabledeviceconnector) в последовательности перечисления.</span><span class="sxs-lookup"><span data-stu-id="45fbc-118">Retrieves the next one or more [**IPortableDeviceConnector**](/windows/desktop/api/portabledeviceconnectapi/nn-portabledeviceconnectapi-iportabledeviceconnector) objects in the enumeration sequence.</span></span><br/> |
| [<span data-ttu-id="45fbc-119">**Перезапуск**</span><span class="sxs-lookup"><span data-stu-id="45fbc-119">**Reset**</span></span>](ienumportabledeviceconnectors-reset.md) | <span data-ttu-id="45fbc-120">Сбрасывает последовательность перечисления в начало.</span><span class="sxs-lookup"><span data-stu-id="45fbc-120">Resets the enumeration sequence to the beginning.</span></span><br/>                                                                                |
| [<span data-ttu-id="45fbc-121">**Пропустить**</span><span class="sxs-lookup"><span data-stu-id="45fbc-121">**Skip**</span></span>](ienumportabledeviceconnectors-skip.md)   | <span data-ttu-id="45fbc-122">Пропускает указанное число устройств в последовательности перечисления.</span><span class="sxs-lookup"><span data-stu-id="45fbc-122">Skips the specified number of devices in the enumeration sequence.</span></span><br/>                                                               |



 

## <a name="requirements"></a><span data-ttu-id="45fbc-123">Требования</span><span class="sxs-lookup"><span data-stu-id="45fbc-123">Requirements</span></span>



| <span data-ttu-id="45fbc-124">Требование</span><span class="sxs-lookup"><span data-stu-id="45fbc-124">Requirement</span></span> | <span data-ttu-id="45fbc-125">Значение</span><span class="sxs-lookup"><span data-stu-id="45fbc-125">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="45fbc-126">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="45fbc-126">Minimum supported client</span></span><br/> | <span data-ttu-id="45fbc-127">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="45fbc-127">Windows 7 \[desktop apps only\]</span></span><br/>                                                                                                                             |
| <span data-ttu-id="45fbc-128">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="45fbc-128">Minimum supported server</span></span><br/> | <span data-ttu-id="45fbc-129">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="45fbc-129">None supported</span></span><br/>                                                                                                                                              |
| <span data-ttu-id="45fbc-130">Header</span><span class="sxs-lookup"><span data-stu-id="45fbc-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="45fbc-131"><dt>Девпкэй. h; </dt> <dt>Портабледевицеконнектапи. h</dt></span><span class="sxs-lookup"><span data-stu-id="45fbc-131"><dt>Devpkey.h; </dt> <dt>Portabledeviceconnectapi.h</dt></span></span> </dl> |
| <span data-ttu-id="45fbc-132">IDL</span><span class="sxs-lookup"><span data-stu-id="45fbc-132">IDL</span></span><br/>                      | <dl> <span data-ttu-id="45fbc-133"><dt>Портабледевицеконнектапи. idl</dt></span><span class="sxs-lookup"><span data-stu-id="45fbc-133"><dt>Portabledeviceconnectapi.idl</dt></span></span> </dl>                                                                |
| <span data-ttu-id="45fbc-134">Библиотека</span><span class="sxs-lookup"><span data-stu-id="45fbc-134">Library</span></span><br/>                  | <dl> <span data-ttu-id="45fbc-135"><dt>Портабледевицегуидс. lib</dt></span><span class="sxs-lookup"><span data-stu-id="45fbc-135"><dt>PortableDeviceGuids.lib</dt></span></span> </dl>                                                                     |



 

