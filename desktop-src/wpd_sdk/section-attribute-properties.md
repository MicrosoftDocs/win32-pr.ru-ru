---
description: Портативные устройства Windows поддерживают следующие свойства данных раздела.
ms.assetid: 8760d963-fc07-4b54-aa24-5725f4b95ed2
title: Свойства атрибута раздела (Портабледевице. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Section
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: 383e2e50aa5d2a922ad50609e316b3dc9905cc38
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105718117"
---
# <a name="section-attribute-properties"></a><span data-ttu-id="f24ca-103">Свойства атрибута раздела</span><span class="sxs-lookup"><span data-stu-id="f24ca-103">Section Attribute Properties</span></span>

<span data-ttu-id="f24ca-104">Портативные устройства Windows поддерживают следующие свойства данных раздела.</span><span class="sxs-lookup"><span data-stu-id="f24ca-104">Windows Portable Devices supports the following section data properties.</span></span>



| <span data-ttu-id="f24ca-105">Свойство</span><span class="sxs-lookup"><span data-stu-id="f24ca-105">Property</span></span>                                             | <span data-ttu-id="f24ca-106">VarType</span><span class="sxs-lookup"><span data-stu-id="f24ca-106">VarType</span></span>         | <span data-ttu-id="f24ca-107">Описание</span><span class="sxs-lookup"><span data-stu-id="f24ca-107">Description</span></span>                                                                                                                                                                                                                                                                                                                                 |
|------------------------------------------------------|-----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f24ca-108">**\_ \_ Длина данных раздела \_ WPD**</span><span class="sxs-lookup"><span data-stu-id="f24ca-108">**WPD\_SECTION\_DATA\_LENGTH**</span></span>                       | <span data-ttu-id="f24ca-109">**VT \_ UI8**</span><span class="sxs-lookup"><span data-stu-id="f24ca-109">**VT\_UI8**</span></span>     | <span data-ttu-id="f24ca-110">Задает длину упоминаемого объекта.</span><span class="sxs-lookup"><span data-stu-id="f24ca-110">Specifies the length of the referenced object.</span></span>                                                                                                                                                                                                                                                                                              |
| <span data-ttu-id="f24ca-111">**\_ \_ смещение данных раздела \_ WPD**</span><span class="sxs-lookup"><span data-stu-id="f24ca-111">**WPD\_SECTION\_DATA\_OFFSET**</span></span>                       | <span data-ttu-id="f24ca-112">**VT \_ UI8**</span><span class="sxs-lookup"><span data-stu-id="f24ca-112">**VT\_UI8**</span></span>     | <span data-ttu-id="f24ca-113">Задает отсчитываемое от нуля смещение данных для упоминаемого объекта.</span><span class="sxs-lookup"><span data-stu-id="f24ca-113">Specifies the zero-based offset of the data for the referenced object.</span></span>                                                                                                                                                                                                                                                                      |
| <span data-ttu-id="f24ca-114">**\_ \_ \_ \_ объектный ресурс ссылок на данные раздела WPD \_**</span><span class="sxs-lookup"><span data-stu-id="f24ca-114">**WPD\_SECTION\_DATA\_REFERENCED\_OBJECT\_RESOURCE**</span></span> | <span data-ttu-id="f24ca-115">**VT \_ Unknown**</span><span class="sxs-lookup"><span data-stu-id="f24ca-115">**VT\_UNKNOWN**</span></span> | <span data-ttu-id="f24ca-116">Объект [**ипортабледевицекэйколлектион**](iportabledevicekeycollection.md) , содержащий одно значение, указывающее ключ для данного ресурса. Этот ресурс представляет собой объект, на который \_ ссылается \_ смещение данных раздела WPD \_ и \_ \_ Длина данных раздела WPD \_ .</span><span class="sxs-lookup"><span data-stu-id="f24ca-116">An [**IPortableDeviceKeyCollection**](iportabledevicekeycollection.md) containing a single value that specifies the key for a given resource.This resource is the object referenced by WPD\_SECTION\_DATA\_OFFSET and WPD\_SECTION\_DATA\_LENGTH.</span></span><br/> <span data-ttu-id="f24ca-117">Если это свойство не существует, \_ \_ предполагается значение по умолчанию для ресурса WPD.</span><span class="sxs-lookup"><span data-stu-id="f24ca-117">If this property doesn't exist, WPD\_RESOURCE\_DEFAULT is assumed.</span></span><br/> |
| <span data-ttu-id="f24ca-118">**\_ \_ единицы данных раздела \_ WPD**</span><span class="sxs-lookup"><span data-stu-id="f24ca-118">**WPD\_SECTION\_DATA\_UNITS**</span></span>                        | <span data-ttu-id="f24ca-119">**VT \_ UI4**</span><span class="sxs-lookup"><span data-stu-id="f24ca-119">**VT\_UI4**</span></span>     | <span data-ttu-id="f24ca-120">Указывает единицы, используемые для смещения, например байты, миллисекунды и т. д. Возможные значения этого свойства определяются в перечислении **\_ \_ \_ \_ значений единиц измерения данных раздела WPD** в файле портабледевице. h.</span><span class="sxs-lookup"><span data-stu-id="f24ca-120">Specifies the units used for this offset, for example, bytes, milliseconds, and so on.The possible values for this property are defined in the **WPD\_SECTION\_DATA\_UNITS\_VALUES** enumeration in the file PortableDevice.h.</span></span><br/> <span data-ttu-id="f24ca-121">Если единицы не указаны, предполагается использование байтов.</span><span class="sxs-lookup"><span data-stu-id="f24ca-121">If no units are specified, bytes are assumed.</span></span><br/>                                          |



 

## <a name="requirements"></a><span data-ttu-id="f24ca-122">Требования</span><span class="sxs-lookup"><span data-stu-id="f24ca-122">Requirements</span></span>



| <span data-ttu-id="f24ca-123">Требование</span><span class="sxs-lookup"><span data-stu-id="f24ca-123">Requirement</span></span> | <span data-ttu-id="f24ca-124">Значение</span><span class="sxs-lookup"><span data-stu-id="f24ca-124">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="f24ca-125">Header</span><span class="sxs-lookup"><span data-stu-id="f24ca-125">Header</span></span><br/> | <dl> <span data-ttu-id="f24ca-126"><dt>Портабледевице. h</dt></span><span class="sxs-lookup"><span data-stu-id="f24ca-126"><dt>PortableDevice.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f24ca-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f24ca-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f24ca-128">**Свойства и атрибуты WPD**</span><span class="sxs-lookup"><span data-stu-id="f24ca-128">**WPD Properties and Attributes**</span></span>](properties-and-attributes.md)
</dt> </dl>

 

 




