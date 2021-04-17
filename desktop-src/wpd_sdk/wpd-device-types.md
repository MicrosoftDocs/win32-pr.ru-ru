---
description: '\_ \_ Тип перечисления типы устройств WPD описывает различные типы портативных устройств Windows (WPD), обычно используемые для определения базовой классификации и внешнего вида портативного устройства.'
ms.assetid: 51714e0f-e9b7-4474-a8bb-da3875ef5399
title: Перечисление WPD_DEVICE_TYPES (Портабледевице. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WPD_DEVICE_TYPES
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: 3e71acf200a95bba05b7298a5824bfa353e4a90b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105694432"
---
# <a name="wpd_device_types-enumeration"></a><span data-ttu-id="39fa8-103">\_ \_ Перечисление типов устройств WPD</span><span class="sxs-lookup"><span data-stu-id="39fa8-103">WPD\_DEVICE\_TYPES enumeration</span></span>

<span data-ttu-id="39fa8-104">Тип **перечисления \_ \_ типы устройств WPD** описывает различные типы портативных устройств Windows (WPD), обычно используемые для определения базовой классификации и внешнего вида портативного устройства.</span><span class="sxs-lookup"><span data-stu-id="39fa8-104">The **WPD\_DEVICE\_TYPES** enumeration type describes the different Windows Portable Device (WPD) types commonly used to determine the basic classification and visual appearance of a portable device.</span></span>

## <a name="syntax"></a><span data-ttu-id="39fa8-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="39fa8-105">Syntax</span></span>


```C++
typedef enum tagWPD_DEVICE_TYPES { 
  WPD_DEVICE_TYPE_GENERIC                       = 0,
  WPD_DEVICE_TYPE_CAMERA                        = 1,
  WPD_DEVICE_TYPE_MEDIA_PLAYER                  = 2,
  WPD_DEVICE_TYPE_PHONE                         = 3,
  WPD_DEVICE_TYPE_VIDEO                         = 4,
  WPD_DEVICE_TYPE_PERSONAL_INFORMATION_MANAGER  = 5,
  WPD_DEVICE_TYPE_AUDIO_RECORDER                = 6
} WPD_DEVICE_TYPES;
```



## <a name="constants"></a><span data-ttu-id="39fa8-106">Константы</span><span class="sxs-lookup"><span data-stu-id="39fa8-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="39fa8-107"><span id="WPD_DEVICE_TYPE_GENERIC"></span><span id="wpd_device_type_generic"></span>**\_ \_ универсальный тип устройства типа WPD \_**</span><span class="sxs-lookup"><span data-stu-id="39fa8-107"><span id="WPD_DEVICE_TYPE_GENERIC"></span><span id="wpd_device_type_generic"></span>**WPD\_DEVICE\_TYPE\_GENERIC**</span></span>
</dt> <dd>

<span data-ttu-id="39fa8-108">Универсальный WPD, включающий в себя Многофункциональные устройства, которые не входят в одно из значений перечисления других [**\_ \_ типов устройств типа WPD**](wpd-device-types.md) .</span><span class="sxs-lookup"><span data-stu-id="39fa8-108">A generic WPD that includes multifunction devices that do not fall into one of the other [**WPD\_DEVICE\_TYPES**](wpd-device-types.md) enumeration values.</span></span>

</dd> <dt>

<span data-ttu-id="39fa8-109"><span id="WPD_DEVICE_TYPE_CAMERA"></span><span id="wpd_device_type_camera"></span>**\_тип устройства \_ WPD \_ Camera**</span><span class="sxs-lookup"><span data-stu-id="39fa8-109"><span id="WPD_DEVICE_TYPE_CAMERA"></span><span id="wpd_device_type_camera"></span>**WPD\_DEVICE\_TYPE\_CAMERA**</span></span>
</dt> <dd>

<span data-ttu-id="39fa8-110">Устройство камеры, например цифровая камера.</span><span class="sxs-lookup"><span data-stu-id="39fa8-110">A camera device, such as a digital still camera.</span></span>

</dd> <dt>

<span data-ttu-id="39fa8-111"><span id="WPD_DEVICE_TYPE_MEDIA_PLAYER"></span><span id="wpd_device_type_media_player"></span>**\_тип устройства \_ WPD \_ \_ проигрыватель мультимедиа**</span><span class="sxs-lookup"><span data-stu-id="39fa8-111"><span id="WPD_DEVICE_TYPE_MEDIA_PLAYER"></span><span id="wpd_device_type_media_player"></span>**WPD\_DEVICE\_TYPE\_MEDIA\_PLAYER**</span></span>
</dt> <dd>

<span data-ttu-id="39fa8-112">Устройство проигрывателя мультимедиа, которое поддерживает воспроизведение аудио, видео или просмотр изображений, например портативный музыкальный проигрыватель или портативный Media Center.</span><span class="sxs-lookup"><span data-stu-id="39fa8-112">A media player device that supports playing audio, video, or viewing pictures, such as a portable music player or portable media center.</span></span> <span data-ttu-id="39fa8-113">Не все эти функции классифицируются как \_ устройства типа "устройство WPD \_ " \_ \_ проигрывателя мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="39fa8-113">Not all of this functionally is classified as a WPD\_DEVICE\_TYPE\_MEDIA\_PLAYER.</span></span> <span data-ttu-id="39fa8-114">Например, устройства с портативным музыкальным проигрывателем классифицируются как \_ устройства \_ типа WPD \_ Media \_ Player.</span><span class="sxs-lookup"><span data-stu-id="39fa8-114">For example, portable music player devices are classified as WPD\_DEVICE\_TYPE\_MEDIA\_PLAYER.</span></span>

</dd> <dt>

<span data-ttu-id="39fa8-115"><span id="WPD_DEVICE_TYPE_PHONE"></span><span id="wpd_device_type_phone"></span>**устройство типа "WPD" \_ \_ \_ Телефон**</span><span class="sxs-lookup"><span data-stu-id="39fa8-115"><span id="WPD_DEVICE_TYPE_PHONE"></span><span id="wpd_device_type_phone"></span>**WPD\_DEVICE\_TYPE\_PHONE**</span></span>
</dt> <dd>

<span data-ttu-id="39fa8-116">Телефонное устройство, например мобильный телефон.</span><span class="sxs-lookup"><span data-stu-id="39fa8-116">A phone device, such as a mobile phone.</span></span>

</dd> <dt>

<span data-ttu-id="39fa8-117"><span id="WPD_DEVICE_TYPE_VIDEO"></span><span id="wpd_device_type_video"></span>**\_ \_ видео типа устройства \_ WPD**</span><span class="sxs-lookup"><span data-stu-id="39fa8-117"><span id="WPD_DEVICE_TYPE_VIDEO"></span><span id="wpd_device_type_video"></span>**WPD\_DEVICE\_TYPE\_VIDEO**</span></span>
</dt> <dd>

<span data-ttu-id="39fa8-118">Видеоустройство.</span><span class="sxs-lookup"><span data-stu-id="39fa8-118">A video device.</span></span>

</dd> <dt>

<span data-ttu-id="39fa8-119"><span id="WPD_DEVICE_TYPE_PERSONAL_INFORMATION_MANAGER"></span><span id="wpd_device_type_personal_information_manager"></span>**\_тип устройства \_ WPD \_ \_ Диспетчер персональных данных \_**</span><span class="sxs-lookup"><span data-stu-id="39fa8-119"><span id="WPD_DEVICE_TYPE_PERSONAL_INFORMATION_MANAGER"></span><span id="wpd_device_type_personal_information_manager"></span>**WPD\_DEVICE\_TYPE\_PERSONAL\_INFORMATION\_MANAGER**</span></span>
</dt> <dd>

<span data-ttu-id="39fa8-120">Устройство диспетчера персональных данных.</span><span class="sxs-lookup"><span data-stu-id="39fa8-120">A personal information manager device.</span></span>

</dd> <dt>

<span data-ttu-id="39fa8-121"><span id="WPD_DEVICE_TYPE_AUDIO_RECORDER"></span><span id="wpd_device_type_audio_recorder"></span>**\_устройство типа "устройства WPD" \_ \_ Audio \_ Record**</span><span class="sxs-lookup"><span data-stu-id="39fa8-121"><span id="WPD_DEVICE_TYPE_AUDIO_RECORDER"></span><span id="wpd_device_type_audio_recorder"></span>**WPD\_DEVICE\_TYPE\_AUDIO\_RECORDER**</span></span>
</dt> <dd>

<span data-ttu-id="39fa8-122">Устройство записи звука.</span><span class="sxs-lookup"><span data-stu-id="39fa8-122">An audio recorder device.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="39fa8-123">Комментарии</span><span class="sxs-lookup"><span data-stu-id="39fa8-123">Remarks</span></span>

<span data-ttu-id="39fa8-124">**WPD \_ Чтение \_ типов устройств** осуществляется с помощью интерфейса [**ипортабледевицеманажер**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevicemanager) .</span><span class="sxs-lookup"><span data-stu-id="39fa8-124">**WPD\_DEVICE\_TYPES** are read using the [**IPortableDeviceManager**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevicemanager) interface.</span></span> <span data-ttu-id="39fa8-125">Приложения WPD могут использовать эти значения для определения универсального внешнего вида устройства.</span><span class="sxs-lookup"><span data-stu-id="39fa8-125">WPD applications may use these values to determine the generic visual appearance of the device.</span></span> <span data-ttu-id="39fa8-126">Это значит, что для устройств, подобных камере, отображается изображение камеры, изображение мобильного телефона отображается для устройств, подобных телефонам, и т. д.</span><span class="sxs-lookup"><span data-stu-id="39fa8-126">That is, a camera picture is displayed for camera-like devices, a mobile phone picture is displayed for phone-like devices, and so on.</span></span>

> [!Note]  
> <span data-ttu-id="39fa8-127">Приложения WPD должны использовать возможности портативного устройства для определения функций, а не для **\_ \_ типов устройств типа WPD** .</span><span class="sxs-lookup"><span data-stu-id="39fa8-127">WPD applications must use the capabilities of the portable device to determine functionally, not the **WPD\_DEVICE\_TYPES** value.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="39fa8-128">Требования</span><span class="sxs-lookup"><span data-stu-id="39fa8-128">Requirements</span></span>



| <span data-ttu-id="39fa8-129">Требование</span><span class="sxs-lookup"><span data-stu-id="39fa8-129">Requirement</span></span> | <span data-ttu-id="39fa8-130">Значение</span><span class="sxs-lookup"><span data-stu-id="39fa8-130">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="39fa8-131">Header</span><span class="sxs-lookup"><span data-stu-id="39fa8-131">Header</span></span><br/> | <dl> <span data-ttu-id="39fa8-132"><dt>Портабледевице. h</dt></span><span class="sxs-lookup"><span data-stu-id="39fa8-132"><dt>PortableDevice.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="39fa8-133">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="39fa8-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="39fa8-134">**Структуры и типы перечислений**</span><span class="sxs-lookup"><span data-stu-id="39fa8-134">**Structures and Enumeration Types**</span></span>](structures-and-enumeration-types.md)
</dt> </dl>

 

 




