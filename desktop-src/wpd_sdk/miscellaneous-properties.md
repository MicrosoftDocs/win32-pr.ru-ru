---
description: Портативные устройства Windows поддерживают следующие прочие свойства.
ms.assetid: 0f2a5684-a94f-4a51-8f72-527204e4ebfa
title: Прочие свойства (Портабледевице. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Miscellaneous
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: 6bc5f90bb04c2ee0d018d03ee07b6cd7436e6593
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105665389"
---
# <a name="miscellaneous-properties"></a><span data-ttu-id="57ff8-103">Прочие свойства</span><span class="sxs-lookup"><span data-stu-id="57ff8-103">Miscellaneous Properties</span></span>

<span data-ttu-id="57ff8-104">Портативные устройства Windows поддерживают следующие прочие свойства.</span><span class="sxs-lookup"><span data-stu-id="57ff8-104">Windows Portable Devices supports the following miscellaneous properties.</span></span>



| <span data-ttu-id="57ff8-105">Свойство</span><span class="sxs-lookup"><span data-stu-id="57ff8-105">Property</span></span>                                       | <span data-ttu-id="57ff8-106">VarType</span><span class="sxs-lookup"><span data-stu-id="57ff8-106">VarType</span></span>         | <span data-ttu-id="57ff8-107">Описание</span><span class="sxs-lookup"><span data-stu-id="57ff8-107">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
|------------------------------------------------|-----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="57ff8-108">**\_параметр API-интерфейса WPD \_ \_ использование \_ \_ потока очистки данных \_**</span><span class="sxs-lookup"><span data-stu-id="57ff8-108">**WPD\_API\_OPTION\_USE\_CLEAR\_DATA\_STREAM**</span></span> | <span data-ttu-id="57ff8-109">**Логическое значение VT \_**</span><span class="sxs-lookup"><span data-stu-id="57ff8-109">**VT\_BOOL**</span></span>    | <span data-ttu-id="57ff8-110">Логическое значение, указывающее, будет ли поток данных, созданный для передачи данных, понятным, то есть не задействованным в DRM. Клиенты могут установить этот параметр, добавив его в свойства объекта, передаваемые в [**ипортабледевицеконтент:: креатеобжектвиспропертиесанддата**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicecontent-createobjectwithpropertiesanddata).</span><span class="sxs-lookup"><span data-stu-id="57ff8-110">A Boolean value that specifies whether the data stream created for data transfer will be clear, that is, DRM is not involved.Clients can set this option by adding it to the object properties passed to [**IPortableDeviceContent::CreateObjectWithPropertiesAndData**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicecontent-createobjectwithpropertiesanddata).</span></span><br/>                                                                                                                                                   |
| <span data-ttu-id="57ff8-111">**\_версия службы \_ WPD**</span><span class="sxs-lookup"><span data-stu-id="57ff8-111">**WPD\_SERVICE\_VERSION**</span></span>                      | <span data-ttu-id="57ff8-112">**VT \_ LPWSTR**</span><span class="sxs-lookup"><span data-stu-id="57ff8-112">**VT\_LPWSTR**</span></span>  | <span data-ttu-id="57ff8-113">Строка, указывающая версию реализации данной службы устройства.</span><span class="sxs-lookup"><span data-stu-id="57ff8-113">A string that specifies the implementation version of a given device service.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                        |
| <span data-ttu-id="57ff8-114">**\_ \_ \_ Допустимые типы содержимого папки WPD \_**</span><span class="sxs-lookup"><span data-stu-id="57ff8-114">**WPD\_FOLDER\_CONTENT\_TYPES\_ALLOWED**</span></span>       | <span data-ttu-id="57ff8-115">**VT \_ Unknown**</span><span class="sxs-lookup"><span data-stu-id="57ff8-115">**VT\_UNKNOWN**</span></span> | <span data-ttu-id="57ff8-116">Значение типа, указывающее типы объектов, которые могут быть прямыми дочерними элементами этой папки.</span><span class="sxs-lookup"><span data-stu-id="57ff8-116">A value that specifies the object types that can be direct children of this folder.</span></span> <span data-ttu-id="57ff8-117">Дочерние папки могут иметь различные возможности. Это свойство является [**ипортабледевицепропвариантколлектион**](iportabledevicepropvariantcollection.md) \_ , содержащим значения VT CLSID, которые указывают разрешенные типы объектов.</span><span class="sxs-lookup"><span data-stu-id="57ff8-117">Child folders can have different capabilities.This property is an [**IPortableDevicePropVariantCollection**](iportabledevicepropvariantcollection.md) holding VT\_CLSID values that specify permitted object types.</span></span><br/> <span data-ttu-id="57ff8-118">Список типов объектов, определенных портативными устройствами Windows, см. в разделе [требования для объектов](requirements-for-objects.md).</span><span class="sxs-lookup"><span data-stu-id="57ff8-118">For a list of object types defined by Windows Portable Devices, see [Requirements for Objects](requirements-for-objects.md).</span></span><br/>                                         |
| <span data-ttu-id="57ff8-119">**\_Категория функционального \_ объекта WPD \_**</span><span class="sxs-lookup"><span data-stu-id="57ff8-119">**WPD\_FUNCTIONAL\_OBJECT\_CATEGORY**</span></span>          | <span data-ttu-id="57ff8-120">**VT \_ CLSID**</span><span class="sxs-lookup"><span data-stu-id="57ff8-120">**VT\_CLSID**</span></span>   | <span data-ttu-id="57ff8-121">Значение типа, указывающее функциональную категорию объекта.</span><span class="sxs-lookup"><span data-stu-id="57ff8-121">A value that specifies the object's functional category.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| <span data-ttu-id="57ff8-122">**\_ \_ информационные профили модуля обработки данных \_**</span><span class="sxs-lookup"><span data-stu-id="57ff8-122">**WPD\_RENDERING\_INFORMATION\_PROFILES**</span></span>      | <span data-ttu-id="57ff8-123">**VT \_ Unknown**</span><span class="sxs-lookup"><span data-stu-id="57ff8-123">**VT\_UNKNOWN**</span></span> | <span data-ttu-id="57ff8-124">Объект [**ипортабледевицевалуесколлектион**](iportabledevicevaluescollection.md) , содержащий несколько интерфейсов [**ипортабледевицевалуес**](iportabledevicevalues.md) , каждый из которых содержит настройки свойств для профиля, поддерживаемого объектом.</span><span class="sxs-lookup"><span data-stu-id="57ff8-124">An [**IPortableDeviceValuesCollection**](iportabledevicevaluescollection.md) that holds multiple [**IPortableDeviceValues**](iportabledevicevalues.md) interfaces, each of which contains the property settings for a profile that the object supports.</span></span>                                                                                                                                                                                                                                            |
| <span data-ttu-id="57ff8-125">**\_ \_ \_ имя расположения подсказки \_ \_ для объекта WPD**</span><span class="sxs-lookup"><span data-stu-id="57ff8-125">**WPD\_OBJECT\_HINT\_LOCATION\_DISPLAY\_NAME**</span></span> | <span data-ttu-id="57ff8-126">**VT \_ LPWSTR**</span><span class="sxs-lookup"><span data-stu-id="57ff8-126">**VT\_LPWSTR**</span></span>  | <span data-ttu-id="57ff8-127">Если объект является расположением указания, это свойство указывает имя, связанное с указанием, которое будет отображаться пользователю вместо имени объекта. Драйверы могут задавать указания расположения для различных типов объектов.</span><span class="sxs-lookup"><span data-stu-id="57ff8-127">If an object is a hint location, this property indicates the hint-specific name to display to the user instead of the object name.Drivers can specify location hints for various object types.</span></span> <span data-ttu-id="57ff8-128">Это предпочтительные места хранения для папок, содержащих определенный тип объекта.</span><span class="sxs-lookup"><span data-stu-id="57ff8-128">These are preferred storage locations for folders that hold a particular object type.</span></span> <span data-ttu-id="57ff8-129">Эквивалентом будет папка «Мои рисунки» для файлов изображений в Windows.</span><span class="sxs-lookup"><span data-stu-id="57ff8-129">An equivalent would be the My Pictures folder for image files in Windows.</span></span> <span data-ttu-id="57ff8-130">Если это свойство не существует, вместо него используется [ \_ \_ имя объекта WPD](object-properties.md) .</span><span class="sxs-lookup"><span data-stu-id="57ff8-130">If this property does not exist, typically the [WPD\_OBJECT\_NAME](object-properties.md) is used instead.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="57ff8-131">Требования</span><span class="sxs-lookup"><span data-stu-id="57ff8-131">Requirements</span></span>



| <span data-ttu-id="57ff8-132">Требование</span><span class="sxs-lookup"><span data-stu-id="57ff8-132">Requirement</span></span> | <span data-ttu-id="57ff8-133">Значение</span><span class="sxs-lookup"><span data-stu-id="57ff8-133">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="57ff8-134">Header</span><span class="sxs-lookup"><span data-stu-id="57ff8-134">Header</span></span><br/> | <dl> <span data-ttu-id="57ff8-135"><dt>Портабледевице. h</dt></span><span class="sxs-lookup"><span data-stu-id="57ff8-135"><dt>PortableDevice.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="57ff8-136">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="57ff8-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="57ff8-137">**Свойства и атрибуты WPD**</span><span class="sxs-lookup"><span data-stu-id="57ff8-137">**WPD Properties and Attributes**</span></span>](properties-and-attributes.md)
</dt> </dl>

 

 




