---
description: 'Для Windows 7 портативные устройства Windows поддерживают следующие атрибуты для методов службы устройства. Эти атрибуты возвращаются методом Ипортабледевицесервицекапабилитиес:: Жетмесодаттрибутес.'
ms.assetid: b920e037-7737-4a18-b4f1-5c59e0a857dd
title: Атрибуты метода (Портабледевице. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Method
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: fe638bcd0d87af7b16bfb4f202f21cea97908fcd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105694888"
---
# <a name="method-attributes"></a><span data-ttu-id="7529d-104">Атрибуты метода</span><span class="sxs-lookup"><span data-stu-id="7529d-104">Method Attributes</span></span>

<span data-ttu-id="7529d-105">Для Windows 7 портативные устройства Windows поддерживают следующие атрибуты для методов службы устройства.</span><span class="sxs-lookup"><span data-stu-id="7529d-105">For Windows 7, Windows Portable Devices supports the following attributes for methods of a device service.</span></span> <span data-ttu-id="7529d-106">Эти атрибуты возвращаются методом [**ипортабледевицесервицекапабилитиес:: жетмесодаттрибутес**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicecapabilities-getmethodattributes) .</span><span class="sxs-lookup"><span data-stu-id="7529d-106">These attributes are returned by the [**IPortableDeviceServiceCapabilities::GetMethodAttributes**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicecapabilities-getmethodattributes) method.</span></span>




| <span data-ttu-id="7529d-107">attribute</span><span class="sxs-lookup"><span data-stu-id="7529d-107">Attribute</span></span>                                      | <span data-ttu-id="7529d-108">VarType</span><span class="sxs-lookup"><span data-stu-id="7529d-108">VarType</span></span>         | <span data-ttu-id="7529d-109">Описание</span><span class="sxs-lookup"><span data-stu-id="7529d-109">Description</span></span>                                                                                                               |
|------------------------------------------------|-----------------|---------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7529d-110">**\_ \_ доступ к атрибуту метода WPD \_**</span><span class="sxs-lookup"><span data-stu-id="7529d-110">**WPD\_METHOD\_ATTRIBUTE\_ACCESS**</span></span>             | <span data-ttu-id="7529d-111">**VT \_ CLSID**</span><span class="sxs-lookup"><span data-stu-id="7529d-111">**VT\_CLSID**</span></span>   | <span data-ttu-id="7529d-112">Доступ к требуемому методу.</span><span class="sxs-lookup"><span data-stu-id="7529d-112">The required method access.</span></span>                                                                                               |
| <span data-ttu-id="7529d-113">**\_ \_ \_ формат связанного атрибута метода \_ WPD**</span><span class="sxs-lookup"><span data-stu-id="7529d-113">**WPD\_METHOD\_ATTRIBUTE\_ASSOCIATED\_FORMAT**</span></span> | <span data-ttu-id="7529d-114">**VT \_ CLSID**</span><span class="sxs-lookup"><span data-stu-id="7529d-114">**VT\_CLSID**</span></span>   | <span data-ttu-id="7529d-115">Формат, связанный с методом, или **GUID \_ null** , если связанный формат отсутствует.</span><span class="sxs-lookup"><span data-stu-id="7529d-115">The format associated with the method, or **GUID\_NULL** if there is no associated format.</span></span>                                |
| <span data-ttu-id="7529d-116">**\_ \_ имя атрибута метода \_ WPD**</span><span class="sxs-lookup"><span data-stu-id="7529d-116">**WPD\_METHOD\_ATTRIBUTE\_NAME**</span></span>               | <span data-ttu-id="7529d-117">**VT \_ LPWSTR**</span><span class="sxs-lookup"><span data-stu-id="7529d-117">**VT\_LPWSTR**</span></span>  | <span data-ttu-id="7529d-118">Строка, указывающая понятное для сценария имя метода.</span><span class="sxs-lookup"><span data-stu-id="7529d-118">A string that specifies the script-friendly name of the method.</span></span> <span data-ttu-id="7529d-119">Допустимые символы: алфавитные буквы \[ a-zA-Z0-9 \] и " \_ ".</span><span class="sxs-lookup"><span data-stu-id="7529d-119">Valid characters are alphanumeric \[a-zA-Z0-9\] and '\_'.</span></span> |
| <span data-ttu-id="7529d-120">**\_ \_ параметры атрибута метода \_ WPD**</span><span class="sxs-lookup"><span data-stu-id="7529d-120">**WPD\_METHOD\_ATTRIBUTE\_PARAMETERS**</span></span>         | <span data-ttu-id="7529d-121">**VT \_ Unknown**</span><span class="sxs-lookup"><span data-stu-id="7529d-121">**VT\_UNKNOWN**</span></span> | <span data-ttu-id="7529d-122">Интерфейс [**ипортабледевицекэйколлектион**](iportabledevicekeycollection.md) , который содержит параметры метода.</span><span class="sxs-lookup"><span data-stu-id="7529d-122">An [**IPortableDeviceKeyCollection**](iportabledevicekeycollection.md) interface that contains the method parameters.</span></span>    |



 

## <a name="requirements"></a><span data-ttu-id="7529d-123">Требования</span><span class="sxs-lookup"><span data-stu-id="7529d-123">Requirements</span></span>



| <span data-ttu-id="7529d-124">Требование</span><span class="sxs-lookup"><span data-stu-id="7529d-124">Requirement</span></span> | <span data-ttu-id="7529d-125">Значение</span><span class="sxs-lookup"><span data-stu-id="7529d-125">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="7529d-126">Header</span><span class="sxs-lookup"><span data-stu-id="7529d-126">Header</span></span><br/> | <dl> <span data-ttu-id="7529d-127"><dt>Портабледевице. h</dt></span><span class="sxs-lookup"><span data-stu-id="7529d-127"><dt>PortableDevice.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7529d-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="7529d-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7529d-129">**Свойства и атрибуты**</span><span class="sxs-lookup"><span data-stu-id="7529d-129">**Properties and Attributes**</span></span>](properties-and-attributes.md)
</dt> </dl>

 

 




