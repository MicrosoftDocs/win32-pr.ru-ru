---
description: Стандартный видеодрайвер для воспроизведения изображений (WIA) Windows (wiavusd.dll) поддерживает следующие свойства потокового видео-устройства.
ms.assetid: 24fa7e02-c409-49ec-b1a9-309f7c95e292
title: Константы свойств устройства WIA видео (Виадеф. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WIA_DPV_LAST_PICTURE_TAKEN
- WIA_DPV_IMAGES_DIRECTORY
- WIA_DPV_DSHOW_DEVICE_PATH
- WIA_DPF_MOUNT_POINT
api_type:
- HeaderDef
api_location:
- wiadef.h
ms.openlocfilehash: f02991cb5c2b8cc15eb89e335ef1e46442c89510
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104145340"
---
# <a name="video-wia-device-property-constants"></a><span data-ttu-id="5463d-103">Константы свойств устройства WIA видео</span><span class="sxs-lookup"><span data-stu-id="5463d-103">Video WIA Device Property Constants</span></span>

<span data-ttu-id="5463d-104">Стандартный видеодрайвер для воспроизведения изображений (WIA) Windows (wiavusd.dll) поддерживает следующие свойства потокового видео-устройства.</span><span class="sxs-lookup"><span data-stu-id="5463d-104">The standard Windows Image Acquisition (WIA) video driver (wiavusd.dll) supports the following properties for streaming video devices.</span></span>

> [!Note]  
> <span data-ttu-id="5463d-105">WIA не поддерживает видео устройства в Windows Server 2003, Windows Vista и более поздних версиях.</span><span class="sxs-lookup"><span data-stu-id="5463d-105">WIA does not support video devices in Windows Server 2003, Windows Vista, or later.</span></span> <span data-ttu-id="5463d-106">Для этих версий Windows используйте [DirectShow](/previous-versions//ms783323(v=vs.85)) для получения изображений из видео.</span><span class="sxs-lookup"><span data-stu-id="5463d-106">For those versions of the Windows, use [DirectShow](/previous-versions//ms783323(v=vs.85)) to acquire images from video.</span></span>

 

<span data-ttu-id="5463d-107">Префикс "WIA \_ ДПВ \_ " указывает свойство устройства для видеоустройств и является соглашением об именовании, используемым в C/C++.</span><span class="sxs-lookup"><span data-stu-id="5463d-107">The prefix "WIA\_DPV\_" indicates a Device Property for Video devices and is the naming convention used in C/C++.</span></span> <span data-ttu-id="5463d-108">Для сценариев эти константы используют префикс "Видеодевице" и являются частью перечислимого типа [виаитемпропертид](-wia-wiaitempropertyid.md) .</span><span class="sxs-lookup"><span data-stu-id="5463d-108">For scripting purposes these constants use the prefix "VideoDevice" and are part of the [WiaItemPropertyId](-wia-wiaitempropertyid.md) enumerated type.</span></span> <span data-ttu-id="5463d-109">Соответствующее имя элемента из этого перечисления скриптов отображается в круглых скобках рядом с именем константы C/C++ в следующем списке.</span><span class="sxs-lookup"><span data-stu-id="5463d-109">The corresponding member name from that script enumeration appears in parentheses next to the C/C++ constant name in the following list.</span></span>



| <span data-ttu-id="5463d-110">Константа/значение</span><span class="sxs-lookup"><span data-stu-id="5463d-110">Constant/value</span></span>                                                                                                                                                                                                                                                                           | <span data-ttu-id="5463d-111">Описание</span><span class="sxs-lookup"><span data-stu-id="5463d-111">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                          |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="WIA_DPV_LAST_PICTURE_TAKEN"></span><span id="wia_dpv_last_picture_taken"></span><dl> <span data-ttu-id="5463d-112"><dt>**WIA \_ ДПВ \_ Последняя \_ картинка, \_ полученная**</dt> <dt>видеодевицеластпиктуретакен</dt></span><span class="sxs-lookup"><span data-stu-id="5463d-112"><dt>**WIA\_DPV\_LAST\_PICTURE\_TAKEN**</dt> <dt>VideoDeviceLastPictureTaken</dt></span></span> </dl> | <span data-ttu-id="5463d-113">Это свойство используется для уведомления драйвера WIA о добавлении нового изображения.</span><span class="sxs-lookup"><span data-stu-id="5463d-113">This property is used to notify the WIA driver that a new image has been added.</span></span> <span data-ttu-id="5463d-114">Приложениям следует задать для этого свойства имя файла изображения, созданного в результате успешного вызова метода [**ивиавидео:: такепиктуре**](/windows/desktop/api/Wiavideo/nf-wiavideo-iwiavideo-takepicture) .</span><span class="sxs-lookup"><span data-stu-id="5463d-114">Applications should set the value of this property to the name of the image file created as the result of a successful call to the [**IWiaVideo::TakePicture**](/windows/desktop/api/Wiavideo/nf-wiavideo-iwiavideo-takepicture) method.</span></span> <br/> <span data-ttu-id="5463d-115">Тип: VT \_ BSTR, доступ: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="5463d-115">Type: VT\_BSTR, Access: Read/Write</span></span><br/>                                    |
| <span id="WIA_DPV_IMAGES_DIRECTORY"></span><span id="wia_dpv_images_directory"></span><dl> <span data-ttu-id="5463d-116"><dt>**WIA \_ \_ \_ Каталог ДПВ Images**</dt> <dt>видеодевицеимажесдиректори</dt></span><span class="sxs-lookup"><span data-stu-id="5463d-116"><dt>**WIA\_DPV\_IMAGES\_DIRECTORY**</dt> <dt>VideoDeviceImagesDirectory</dt></span></span> </dl>         | <span data-ttu-id="5463d-117">Это свойство предоставляется стандартным драйвером пользовательского режима WIA видео (wiavusd.dll).</span><span class="sxs-lookup"><span data-stu-id="5463d-117">This property is exposed by the standard WIA video user-mode driver (wiavusd.dll).</span></span> <span data-ttu-id="5463d-118">Значением этого свойства является полный путь к каталогу, в который по умолчанию драйвер WIA видео помещает изображения.</span><span class="sxs-lookup"><span data-stu-id="5463d-118">The value of this property is the full path of the directory where the WIA video driver puts images by default.</span></span> <span data-ttu-id="5463d-119">Приложения должны установить это значение для свойства [**ивиавидео:: имажесдиректори**](/windows/desktop/api/Wiavideo/nf-wiavideo-iwiavideo-get_imagesdirectory) .</span><span class="sxs-lookup"><span data-stu-id="5463d-119">Applications should set the [**IWiaVideo::ImagesDirectory**](/windows/desktop/api/Wiavideo/nf-wiavideo-iwiavideo-get_imagesdirectory) property to this value.</span></span> <br/> <span data-ttu-id="5463d-120">Тип: VT \_ BSTR, доступ: только для чтения</span><span class="sxs-lookup"><span data-stu-id="5463d-120">Type: VT\_BSTR, Access: Read Only</span></span><br/> |
| <span id="WIA_DPV_DSHOW_DEVICE_PATH"></span><span id="wia_dpv_dshow_device_path"></span><dl> <span data-ttu-id="5463d-121"><dt>**WIA \_ Видеодевицедшовдевицепас \_ \_ \_ путь к устройству ДПВ DSHOW**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="5463d-121"><dt>**WIA\_DPV\_DSHOW\_DEVICE\_PATH**</dt> <dt>VideoDeviceDShowDevicePath</dt></span></span> </dl>     | <span data-ttu-id="5463d-122">Полный путь к устройству DirectShow.</span><span class="sxs-lookup"><span data-stu-id="5463d-122">The full path of the DirectShow device.</span></span> <br/> <span data-ttu-id="5463d-123">Тип: VT \_ BSTR, доступ: только для чтения</span><span class="sxs-lookup"><span data-stu-id="5463d-123">Type: VT\_BSTR, Access: Read Only</span></span><br/>                                                                                                                                                                                                                                                                                     |
| <span id="WIA_DPF_MOUNT_POINT"></span><span id="wia_dpf_mount_point"></span><dl> <span data-ttu-id="5463d-124"><dt>**WIA \_ Филедевицемаунтпоинт \_ \_ точка подключения ДПФ**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="5463d-124"><dt>**WIA\_DPF\_MOUNT\_POINT**</dt> <dt>FileDeviceMountPoint</dt></span></span> </dl>                              | <span data-ttu-id="5463d-125">Не реализован.</span><span class="sxs-lookup"><span data-stu-id="5463d-125">Not implemented.</span></span> <br/> <span data-ttu-id="5463d-126">Тип: **VT \_ I4**, доступ: только для чтения, допустимые значения: [WIA \_ prop \_ None](-wia-property-attributes.md)</span><span class="sxs-lookup"><span data-stu-id="5463d-126">Type: **VT\_I4**, Access: Read Only, Valid values: [WIA\_PROP\_NONE](-wia-property-attributes.md)</span></span><br/>                                                                                                                                                                                                                                           |



## <a name="requirements"></a><span data-ttu-id="5463d-127">Требования</span><span class="sxs-lookup"><span data-stu-id="5463d-127">Requirements</span></span>



| <span data-ttu-id="5463d-128">Требование</span><span class="sxs-lookup"><span data-stu-id="5463d-128">Requirement</span></span> | <span data-ttu-id="5463d-129">Значение</span><span class="sxs-lookup"><span data-stu-id="5463d-129">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="5463d-130">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="5463d-130">Minimum supported client</span></span><br/> | <span data-ttu-id="5463d-131">Windows 2000 Professional, только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="5463d-131">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="5463d-132">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="5463d-132">Minimum supported server</span></span><br/> | <span data-ttu-id="5463d-133">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="5463d-133">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="5463d-134">Header</span><span class="sxs-lookup"><span data-stu-id="5463d-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="5463d-135"><dt>Виадеф. h</dt></span><span class="sxs-lookup"><span data-stu-id="5463d-135"><dt>Wiadef.h</dt></span></span> </dl> |



 

 
