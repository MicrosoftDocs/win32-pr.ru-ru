---
description: Портативные устройства Windows поддерживают следующие свойства атрибутов ресурсов.
ms.assetid: 9b90db8a-e833-48cf-b484-70ac5ac32a76
title: Свойства атрибута ресурса (Портабледевице. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Resource
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: 64f4f394fcd91d50f323a8e46a9556daa6a8dbff
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105718103"
---
# <a name="resource-attribute-properties"></a><span data-ttu-id="35dac-103">Свойства атрибута ресурса</span><span class="sxs-lookup"><span data-stu-id="35dac-103">Resource Attribute Properties</span></span>

<span data-ttu-id="35dac-104">Портативные устройства Windows поддерживают следующие свойства атрибутов ресурсов.</span><span class="sxs-lookup"><span data-stu-id="35dac-104">Windows Portable Devices supports the following resource attribute properties.</span></span>



| <span data-ttu-id="35dac-105">Свойство</span><span class="sxs-lookup"><span data-stu-id="35dac-105">Property</span></span>                                    | <span data-ttu-id="35dac-106">VarType</span><span class="sxs-lookup"><span data-stu-id="35dac-106">VarType</span></span>         | <span data-ttu-id="35dac-107">Описание</span><span class="sxs-lookup"><span data-stu-id="35dac-107">Description</span></span>                                                                                                                                                               |
|---------------------------------------------|-----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="35dac-108">**\_ \_ \_ ключ ресурса атрибута ресурса \_ WPD**</span><span class="sxs-lookup"><span data-stu-id="35dac-108">**WPD\_RESOURCE\_ATTRIBUTE\_RESOURCE\_KEY**</span></span> | <span data-ttu-id="35dac-109">**VT \_ Unknown**</span><span class="sxs-lookup"><span data-stu-id="35dac-109">**VT\_UNKNOWN**</span></span> | <span data-ttu-id="35dac-110">Это [**ипортабледевицекэйколлектион**](iportabledevicekeycollection.md) , содержащий одно значение, которое является ключом, идентифицирующим ресурс.</span><span class="sxs-lookup"><span data-stu-id="35dac-110">This is an [**IPortableDeviceKeyCollection**](iportabledevicekeycollection.md) containing a single value, which is the key identifying the resource.</span></span>                     |
| <span data-ttu-id="35dac-111">**\_ \_ Формат атрибута ресурса \_ WPD**</span><span class="sxs-lookup"><span data-stu-id="35dac-111">**WPD\_RESOURCE\_ATTRIBUTE\_FORMAT**</span></span>        | <span data-ttu-id="35dac-112">**VT \_ CLSID**</span><span class="sxs-lookup"><span data-stu-id="35dac-112">**VT\_CLSID**</span></span>   | <span data-ttu-id="35dac-113">Значение идентификатора GUID, указывающее формат ресурса.</span><span class="sxs-lookup"><span data-stu-id="35dac-113">A GUID value that specifies the format of the resource.</span></span> <span data-ttu-id="35dac-114">Список форматов, определяемых портативными устройствами Windows, см. в разделе [форматы объектов](object-format-guids.md) .</span><span class="sxs-lookup"><span data-stu-id="35dac-114">See [Object Formats](object-format-guids.md) for a list of formats that are defined by Windows Portable Devices.</span></span> |
| <span data-ttu-id="35dac-115">**\_ \_ \_ Общий \_ Размер атрибута ресурса WPD**</span><span class="sxs-lookup"><span data-stu-id="35dac-115">**WPD\_RESOURCE\_ATTRIBUTE\_TOTAL\_SIZE**</span></span>   | <span data-ttu-id="35dac-116">**VT \_ UI8**</span><span class="sxs-lookup"><span data-stu-id="35dac-116">**VT\_UI8**</span></span>     | <span data-ttu-id="35dac-117">Общий размер данных ресурса в байтах.</span><span class="sxs-lookup"><span data-stu-id="35dac-117">The total size of the resource data, in bytes.</span></span>                                                                                                                            |



 

## <a name="remarks"></a><span data-ttu-id="35dac-118">Комментарии</span><span class="sxs-lookup"><span data-stu-id="35dac-118">Remarks</span></span>

<span data-ttu-id="35dac-119">Эти атрибуты возвращаются методом [**ипортабледевицересаурцес:: жетресаурцеаттрибутес**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledeviceresources-getresourceattributes) .</span><span class="sxs-lookup"><span data-stu-id="35dac-119">These attributes are returned by the [**IPortableDeviceResources::GetResourceAttributes**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledeviceresources-getresourceattributes) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="35dac-120">Требования</span><span class="sxs-lookup"><span data-stu-id="35dac-120">Requirements</span></span>



| <span data-ttu-id="35dac-121">Требование</span><span class="sxs-lookup"><span data-stu-id="35dac-121">Requirement</span></span> | <span data-ttu-id="35dac-122">Значение</span><span class="sxs-lookup"><span data-stu-id="35dac-122">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="35dac-123">Header</span><span class="sxs-lookup"><span data-stu-id="35dac-123">Header</span></span><br/> | <dl> <span data-ttu-id="35dac-124"><dt>Портабледевице. h</dt></span><span class="sxs-lookup"><span data-stu-id="35dac-124"><dt>PortableDevice.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="35dac-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="35dac-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="35dac-126">**Ипортабледевицересаурцес:: Жетресаурцеаттрибутес**</span><span class="sxs-lookup"><span data-stu-id="35dac-126">**IPortableDeviceResources::GetResourceAttributes**</span></span>](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledeviceresources-getresourceattributes)
</dt> <dt>

[<span data-ttu-id="35dac-127">**Свойства и атрибуты WPD**</span><span class="sxs-lookup"><span data-stu-id="35dac-127">**WPD Properties and Attributes**</span></span>](properties-and-attributes.md)
</dt> </dl>

 

 




