---
description: 'Интерфейс Ивпдсериализер используется драйвером устройства для сериализации интерфейсов Ипортабледевицевалуес в необработанные буферы данных, используемые для взаимодействия с приложением. Приложениям не требуется использовать этот интерфейс, так как данные сериализуются и десериализуются автоматически при вызове Ипортабледевице:: Сендкомманд. чтобы получить этот интерфейс, вызовите CoCreateInstance и передайте IID \_ ивпдсериализер.'
ms.assetid: 837bd850-6e27-4f8e-a612-d16f61b92b1d
title: Интерфейс Ивпдсериализер (Портабледевицетипес. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWpdSerializer
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: dde4bfeea596ccc2691323d484f5583d55ade621
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105668948"
---
# <a name="iwpdserializer-interface"></a><span data-ttu-id="49cf5-103">Интерфейс Ивпдсериализер</span><span class="sxs-lookup"><span data-stu-id="49cf5-103">IWpdSerializer interface</span></span>

<span data-ttu-id="49cf5-104">Интерфейс **ивпдсериализер** используется драйвером устройства для сериализации интерфейсов [**ипортабледевицевалуес**](iportabledevicevalues.md) в необработанные буферы данных, используемые для взаимодействия с приложением.</span><span class="sxs-lookup"><span data-stu-id="49cf5-104">The **IWpdSerializer** interface is used by the device driver to serialize [**IPortableDeviceValues**](iportabledevicevalues.md) interfaces to and from the raw data buffers used to communicate with the application.</span></span>

<span data-ttu-id="49cf5-105">Приложениям не требуется использовать этот интерфейс, так как данные сериализуются и десериализуются автоматически при вызове [**ипортабледевице:: сендкомманд**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-sendcommand).</span><span class="sxs-lookup"><span data-stu-id="49cf5-105">Applications do not need to use this interface, because the data is serialized and deserialized automatically when calling [**IPortableDevice::SendCommand**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-sendcommand).</span></span>

<span data-ttu-id="49cf5-106">Чтобы получить этот интерфейс, вызовите **CoCreateInstance** и передайте **IID \_ ивпдсериализер**.</span><span class="sxs-lookup"><span data-stu-id="49cf5-106">To get this interface, call **CoCreateInstance** and pass in **IID\_IWpdSerializer**.</span></span>

## <a name="members"></a><span data-ttu-id="49cf5-107">Элементы</span><span class="sxs-lookup"><span data-stu-id="49cf5-107">Members</span></span>

<span data-ttu-id="49cf5-108">Интерфейс **ивпдсериализер** наследует от интерфейса [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="49cf5-108">The **IWpdSerializer** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="49cf5-109">**Ивпдсериализер** также имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="49cf5-109">**IWpdSerializer** also has these types of members:</span></span>

-   [<span data-ttu-id="49cf5-110">Методы</span><span class="sxs-lookup"><span data-stu-id="49cf5-110">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="49cf5-111">Методы</span><span class="sxs-lookup"><span data-stu-id="49cf5-111">Methods</span></span>

<span data-ttu-id="49cf5-112">Интерфейс **ивпдсериализер** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="49cf5-112">The **IWpdSerializer** interface has these methods.</span></span>



| <span data-ttu-id="49cf5-113">Метод</span><span class="sxs-lookup"><span data-stu-id="49cf5-113">Method</span></span>                                                                                          | <span data-ttu-id="49cf5-114">Описание</span><span class="sxs-lookup"><span data-stu-id="49cf5-114">Description</span></span>                                                                                                      |
|:------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="49cf5-115">**жетбуфферфромипортабледевицевалуес**</span><span class="sxs-lookup"><span data-stu-id="49cf5-115">**GetBufferFromIPortableDeviceValues**</span></span>](iwpdserializer-getbufferfromiportabledevicevalues.md) | <span data-ttu-id="49cf5-116">Сериализует отправленный интерфейс **ипортабледевицевалуес** в выделенный массив байтов.</span><span class="sxs-lookup"><span data-stu-id="49cf5-116">Serializes a submitted **IPortableDeviceValues** interface to an allocated byte array.</span></span><br/>                |
| [<span data-ttu-id="49cf5-117">**жетипортабледевицевалуесфромбуффер**</span><span class="sxs-lookup"><span data-stu-id="49cf5-117">**GetIPortableDeviceValuesFromBuffer**</span></span>](iwpdserializer-getiportabledevicevaluesfrombuffer.md) | <span data-ttu-id="49cf5-118">Десериализует массив байтов в интерфейс **ипортабледевицевалуес** .</span><span class="sxs-lookup"><span data-stu-id="49cf5-118">Deserializes a byte array to an **IPortableDeviceValues** interface.</span></span><br/>                                  |
| [<span data-ttu-id="49cf5-119">**жетсериализедсизе**</span><span class="sxs-lookup"><span data-stu-id="49cf5-119">**GetSerializedSize**</span></span>](iwpdserializer-getserializedsize.md)                                   | <span data-ttu-id="49cf5-120">Вычисляет размер буфера, необходимого для хранения сериализованного интерфейса **ипортабледевицевалуес** .</span><span class="sxs-lookup"><span data-stu-id="49cf5-120">Calculates the buffer size that is required to hold a serialized **IPortableDeviceValues** interface.</span></span><br/> |
| [<span data-ttu-id="49cf5-121">**вритеипортабледевицевалуестобуффер**</span><span class="sxs-lookup"><span data-stu-id="49cf5-121">**WriteIPortableDeviceValuesToBuffer**</span></span>](iwpdserializer-writeiportabledevicevaluestobuffer.md) | <span data-ttu-id="49cf5-122">Сериализует интерфейс **ипортабледевицевалуес** в выделенный вызывающим объектом массив байтов.</span><span class="sxs-lookup"><span data-stu-id="49cf5-122">Serializes an **IPortableDeviceValues** interface to a caller-allocated byte array.</span></span><br/>                   |



 

## <a name="requirements"></a><span data-ttu-id="49cf5-123">Требования</span><span class="sxs-lookup"><span data-stu-id="49cf5-123">Requirements</span></span>



| <span data-ttu-id="49cf5-124">Требование</span><span class="sxs-lookup"><span data-stu-id="49cf5-124">Requirement</span></span> | <span data-ttu-id="49cf5-125">Значение</span><span class="sxs-lookup"><span data-stu-id="49cf5-125">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="49cf5-126">Header</span><span class="sxs-lookup"><span data-stu-id="49cf5-126">Header</span></span><br/>  | <dl> <span data-ttu-id="49cf5-127"><dt>Портабледевицетипес. h</dt></span><span class="sxs-lookup"><span data-stu-id="49cf5-127"><dt>PortableDeviceTypes.h</dt></span></span> </dl>   |
| <span data-ttu-id="49cf5-128">Библиотека</span><span class="sxs-lookup"><span data-stu-id="49cf5-128">Library</span></span><br/> | <dl> <span data-ttu-id="49cf5-129"><dt>Портабледевицегуидс. lib</dt></span><span class="sxs-lookup"><span data-stu-id="49cf5-129"><dt>PortableDeviceGUIDs.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="49cf5-130">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="49cf5-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="49cf5-131">**Интерфейсы драйвера**</span><span class="sxs-lookup"><span data-stu-id="49cf5-131">**Driver Interfaces**</span></span>](driver-interfaces.md)
</dt> </dl>

 

