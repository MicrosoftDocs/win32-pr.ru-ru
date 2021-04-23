---
description: Портативные устройства Windows (WPD) поддерживают следующие свойства параметров команды.
ms.assetid: 03eff101-5c36-48ea-9dcd-2c4ee29a2ac6
title: Параметры команды (Портабледевице. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Command
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: 7687488c38f95fd6d7e7b69d64ad6ae32631700d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105718027"
---
# <a name="command-parameters"></a><span data-ttu-id="717f4-103">Параметры команд</span><span class="sxs-lookup"><span data-stu-id="717f4-103">Command Parameters</span></span>

<span data-ttu-id="717f4-104">Портативные устройства Windows (WPD) поддерживают следующие свойства параметров команды.</span><span class="sxs-lookup"><span data-stu-id="717f4-104">Windows Portable Devices (WPD) supports the following properties of command parameters.</span></span>




| <span data-ttu-id="717f4-105">**Свойство**</span><span class="sxs-lookup"><span data-stu-id="717f4-105">**Property**</span></span>                                            | <span data-ttu-id="717f4-106">**VarType**</span><span class="sxs-lookup"><span data-stu-id="717f4-106">**VarType**</span></span>     | <span data-ttu-id="717f4-107">**Описание**</span><span class="sxs-lookup"><span data-stu-id="717f4-107">**Description**</span></span>                                                                                                                                                              |
|---------------------------------------------------------|-----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="717f4-108">**\_Свойства WPD \_ Общие \_ \_ сведения о клиенте**</span><span class="sxs-lookup"><span data-stu-id="717f4-108">**WPD\_PROPERTY\_COMMON\_CLIENT\_INFORMATION**</span></span>          | <span data-ttu-id="717f4-109">**VT \_ Unknown**</span><span class="sxs-lookup"><span data-stu-id="717f4-109">**VT\_UNKNOWN**</span></span> | <span data-ttu-id="717f4-110">Интерфейс [**ипортабледевицевалуес**](iportabledevicevalues.md) , используемый драйвером для обнаружения клиента.</span><span class="sxs-lookup"><span data-stu-id="717f4-110">An [**IPortableDeviceValues**](iportabledevicevalues.md) interface that the driver uses to identify the client.</span></span>                                                             |
| <span data-ttu-id="717f4-111">**\_ \_ \_ \_ контекст сведений об общем КЛИЕНТе для свойства WPD \_**</span><span class="sxs-lookup"><span data-stu-id="717f4-111">**WPD\_PROPERTY\_COMMON\_CLIENT\_INFORMATION\_CONTEXT**</span></span> | <span data-ttu-id="717f4-112">**VT \_ LPWSTR**</span><span class="sxs-lookup"><span data-stu-id="717f4-112">**VT\_LPWSTR**</span></span>  | <span data-ttu-id="717f4-113">Заданный драйвером контекст, который определяет клиента для всех последующих операций.</span><span class="sxs-lookup"><span data-stu-id="717f4-113">A driver-specified context which identifies a client for all subsequent operations.</span></span>                                                                                          |
| <span data-ttu-id="717f4-114">**\_ \_ \_ Категория общей команды \_ Свойства WPD**</span><span class="sxs-lookup"><span data-stu-id="717f4-114">**WPD\_PROPERTY\_COMMON\_COMMAND\_CATEGORY**</span></span>            | <span data-ttu-id="717f4-115">**VT \_ CLSID**</span><span class="sxs-lookup"><span data-stu-id="717f4-115">**VT\_CLSID**</span></span>   | <span data-ttu-id="717f4-116">Часть **идентификатора GUID** , относящаяся к значению **PROPERTYKEY** команды.</span><span class="sxs-lookup"><span data-stu-id="717f4-116">The **GUID** portion of the **PROPERTYKEY** value of the command.</span></span>                                                                                                            |
| <span data-ttu-id="717f4-117">**\_ \_ \_ идентификатор общей команды \_ Свойства WPD**</span><span class="sxs-lookup"><span data-stu-id="717f4-117">**WPD\_PROPERTY\_COMMON\_COMMAND\_ID**</span></span>                  | <span data-ttu-id="717f4-118">**VT \_ UI4**</span><span class="sxs-lookup"><span data-stu-id="717f4-118">**VT\_UI4**</span></span>     | <span data-ttu-id="717f4-119">Значение постоянного уникального идентификатора (PID) значения **PROPERTYKEY** команды.</span><span class="sxs-lookup"><span data-stu-id="717f4-119">The Persistent Unique ID (PID) portion of the **PROPERTYKEY** value of the command.</span></span>                                                                                          |
| <span data-ttu-id="717f4-120">**\_ \_ \_ Цель общей команды \_ для свойства WPD**</span><span class="sxs-lookup"><span data-stu-id="717f4-120">**WPD\_PROPERTY\_COMMON\_COMMAND\_TARGET**</span></span>              | <span data-ttu-id="717f4-121">**VT \_ LPWSTR**</span><span class="sxs-lookup"><span data-stu-id="717f4-121">**VT\_LPWSTR**</span></span>  | <span data-ttu-id="717f4-122">Идентификатор целевого объекта.</span><span class="sxs-lookup"><span data-stu-id="717f4-122">The target-object identifier.</span></span>                                                                                                                                                |
| <span data-ttu-id="717f4-123">**\_ \_ \_ код ошибки общего драйвера \_ для свойства WPD \_**</span><span class="sxs-lookup"><span data-stu-id="717f4-123">**WPD\_PROPERTY\_COMMON\_DRIVER\_ERROR\_CODE**</span></span>          | <span data-ttu-id="717f4-124">**VT \_ UI4**</span><span class="sxs-lookup"><span data-stu-id="717f4-124">**VT\_UI4**</span></span>     | <span data-ttu-id="717f4-125">Код ошибки, относящийся к драйверу, возвращенный драйвером WPD.</span><span class="sxs-lookup"><span data-stu-id="717f4-125">A driver-specific error code returned by a WPD driver.</span></span>                                                                                                                       |
| <span data-ttu-id="717f4-126">**Свойство WPD, \_ \_ Общее \_ значение HRESULT**</span><span class="sxs-lookup"><span data-stu-id="717f4-126">**WPD\_PROPERTY\_COMMON\_HRESULT**</span></span>                      | <span data-ttu-id="717f4-127">**\_Ошибка VT**</span><span class="sxs-lookup"><span data-stu-id="717f4-127">**VT\_ERROR**</span></span>   | <span data-ttu-id="717f4-128">Значение **HRESULT** , возвращаемое драйвером WPD для определенной операции.</span><span class="sxs-lookup"><span data-stu-id="717f4-128">The **HRESULT** value returned by a WPD driver for a particular operation.</span></span>                                                                                                   |
| <span data-ttu-id="717f4-129">**\_ \_ \_ идентификаторы общих объектов свойств WPD \_**</span><span class="sxs-lookup"><span data-stu-id="717f4-129">**WPD\_PROPERTY\_COMMON\_OBJECT\_IDS**</span></span>                  | <span data-ttu-id="717f4-130">**VT \_ Unknown**</span><span class="sxs-lookup"><span data-stu-id="717f4-130">**VT\_UNKNOWN**</span></span> | <span data-ttu-id="717f4-131">Интерфейс [**ипортабледевицепропвариантколлектион**](iportabledevicepropvariantcollection.md) типа Variant **VT \_ LPWSTR** , содержащий список идентификаторов объектов.</span><span class="sxs-lookup"><span data-stu-id="717f4-131">An [**IPortableDevicePropVariantCollection**](iportabledevicepropvariantcollection.md) interface of variant type **VT\_LPWSTR** that contains a list of object identifiers.</span></span> |
| <span data-ttu-id="717f4-132">**свойства WPD. \_ \_ Общие \_ постоянные \_ уникальные \_ идентификаторы**</span><span class="sxs-lookup"><span data-stu-id="717f4-132">**WPD\_PROPERTY\_COMMON\_PERSISTENT\_UNIQUE\_IDS**</span></span>      | <span data-ttu-id="717f4-133">**VT \_ Unknown**</span><span class="sxs-lookup"><span data-stu-id="717f4-133">**VT\_UNKNOWN**</span></span> | <span data-ttu-id="717f4-134">Интерфейс [**ипортабледевицепропвариантколлектион**](iportabledevicepropvariantcollection.md) типа Variant **VT \_ LPWSTR** , содержащий список идентификаторов PID.</span><span class="sxs-lookup"><span data-stu-id="717f4-134">An [**IPortableDevicePropVariantCollection**](iportabledevicepropvariantcollection.md) interface of variant type **VT\_LPWSTR** that contains a list of PIDs.</span></span>               |



 

## <a name="requirements"></a><span data-ttu-id="717f4-135">Требования</span><span class="sxs-lookup"><span data-stu-id="717f4-135">Requirements</span></span>



| <span data-ttu-id="717f4-136">Требование</span><span class="sxs-lookup"><span data-stu-id="717f4-136">Requirement</span></span> | <span data-ttu-id="717f4-137">Значение</span><span class="sxs-lookup"><span data-stu-id="717f4-137">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="717f4-138">Header</span><span class="sxs-lookup"><span data-stu-id="717f4-138">Header</span></span><br/> | <dl> <span data-ttu-id="717f4-139"><dt>Портабледевице. h</dt></span><span class="sxs-lookup"><span data-stu-id="717f4-139"><dt>PortableDevice.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="717f4-140">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="717f4-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="717f4-141">**Свойства и атрибуты**</span><span class="sxs-lookup"><span data-stu-id="717f4-141">**Properties and Attributes**</span></span>](properties-and-attributes.md)
</dt> </dl>

 

 




