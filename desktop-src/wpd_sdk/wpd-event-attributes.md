---
description: 'Для Windows 7 портативные устройства Windows поддерживают следующие атрибуты для событий службы устройства. Эти атрибуты возвращаются методом Ипортабледевицесервицекапабилитиес:: Жетевентаттрибутес.'
ms.assetid: 2c71c3ec-842b-44f7-b127-5750883b33ba
title: Атрибуты событий (Портабледевице. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Event
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: 68a5964a4f64899d4aa116002b1feb14ce360498
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105694430"
---
# <a name="event-attributes-portabledeviceh"></a><span data-ttu-id="02ad2-104">Атрибуты событий (Портабледевице. h)</span><span class="sxs-lookup"><span data-stu-id="02ad2-104">Event Attributes (PortableDevice.h)</span></span>

<span data-ttu-id="02ad2-105">Для Windows 7 портативные устройства Windows поддерживают следующие атрибуты для событий службы устройства.</span><span class="sxs-lookup"><span data-stu-id="02ad2-105">For Windows 7, Windows Portable Devices supports the following attributes for events of a device service.</span></span> <span data-ttu-id="02ad2-106">Эти атрибуты возвращаются методом [**ипортабледевицесервицекапабилитиес:: жетевентаттрибутес**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicecapabilities-geteventattributes) .</span><span class="sxs-lookup"><span data-stu-id="02ad2-106">These attributes are returned by the [**IPortableDeviceServiceCapabilities::GetEventAttributes**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicecapabilities-geteventattributes) method.</span></span>




| <span data-ttu-id="02ad2-107">attribute</span><span class="sxs-lookup"><span data-stu-id="02ad2-107">Attribute</span></span>                             | <span data-ttu-id="02ad2-108">VarType</span><span class="sxs-lookup"><span data-stu-id="02ad2-108">VarType</span></span>         | <span data-ttu-id="02ad2-109">Описание</span><span class="sxs-lookup"><span data-stu-id="02ad2-109">Description</span></span>                                                                                                              |
|---------------------------------------|-----------------|--------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="02ad2-110">**\_ \_ имя атрибута события \_ WPD**</span><span class="sxs-lookup"><span data-stu-id="02ad2-110">**WPD\_EVENT\_ATTRIBUTE\_NAME**</span></span>       | <span data-ttu-id="02ad2-111">**VT \_ LPWSTR**</span><span class="sxs-lookup"><span data-stu-id="02ad2-111">**VT\_LPWSTR**</span></span>  | <span data-ttu-id="02ad2-112">Строка, указывающая понятное для сценария имя события.</span><span class="sxs-lookup"><span data-stu-id="02ad2-112">A string that specifies the script-friendly name of the event.</span></span> <span data-ttu-id="02ad2-113">Допустимые символы: алфавитные буквы \[ a-zA-Z0-9 \] и " \_ ".</span><span class="sxs-lookup"><span data-stu-id="02ad2-113">Valid characters are alphanumeric \[a-zA-Z0-9\] and '\_'.</span></span> |
| <span data-ttu-id="02ad2-114">**\_ \_ параметры атрибута событий \_ WPD**</span><span class="sxs-lookup"><span data-stu-id="02ad2-114">**WPD\_EVENT\_ATTRIBUTE\_OPTIONS**</span></span>    | <span data-ttu-id="02ad2-115">**VT \_ Unknown**</span><span class="sxs-lookup"><span data-stu-id="02ad2-115">**VT\_UNKNOWN**</span></span> | <span data-ttu-id="02ad2-116">Объект [**ипортабледевицевалуес**](iportabledevicevalues.md) , содержащий параметры события.</span><span class="sxs-lookup"><span data-stu-id="02ad2-116">An [**IPortableDeviceValues**](iportabledevicevalues.md) that contains the event options.</span></span>                               |
| <span data-ttu-id="02ad2-117">**\_ \_ параметры атрибута события \_ WPD**</span><span class="sxs-lookup"><span data-stu-id="02ad2-117">**WPD\_EVENT\_ATTRIBUTE\_PARAMETERS**</span></span> | <span data-ttu-id="02ad2-118">**VT \_ Unknown**</span><span class="sxs-lookup"><span data-stu-id="02ad2-118">**VT\_UNKNOWN**</span></span> | <span data-ttu-id="02ad2-119">Объект [**ипортабледевицекэйколлектион**](iportabledevicekeycollection.md) , содержащий параметры события.</span><span class="sxs-lookup"><span data-stu-id="02ad2-119">An [**IPortableDeviceKeyCollection**](iportabledevicekeycollection.md) that contains the event parameters.</span></span>              |



 

## <a name="requirements"></a><span data-ttu-id="02ad2-120">Требования</span><span class="sxs-lookup"><span data-stu-id="02ad2-120">Requirements</span></span>



| <span data-ttu-id="02ad2-121">Требование</span><span class="sxs-lookup"><span data-stu-id="02ad2-121">Requirement</span></span> | <span data-ttu-id="02ad2-122">Значение</span><span class="sxs-lookup"><span data-stu-id="02ad2-122">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="02ad2-123">Header</span><span class="sxs-lookup"><span data-stu-id="02ad2-123">Header</span></span><br/> | <dl> <span data-ttu-id="02ad2-124"><dt>Портабледевице. h</dt></span><span class="sxs-lookup"><span data-stu-id="02ad2-124"><dt>PortableDevice.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="02ad2-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="02ad2-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="02ad2-126">**Свойства и атрибуты**</span><span class="sxs-lookup"><span data-stu-id="02ad2-126">**Properties and Attributes**</span></span>](properties-and-attributes.md)
</dt> </dl>

 

 




