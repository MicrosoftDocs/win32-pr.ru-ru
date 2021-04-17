---
description: '\_ \_ Тип ПЕРЕЧИСЛЕНИЯ параметры удаления объекта описывает параметры, которые поддерживаются устройством при удалении объекта.'
ms.assetid: d0e46e77-d333-498f-b2f5-26be1461a116
title: Перечисление DELETE_OBJECT_OPTIONS (Портабледевице. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DELETE_OBJECT_OPTIONS
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: 3a1fb8ce9a443c7cc93019804094dca84a635c40
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105704512"
---
# <a name="delete_object_options-enumeration"></a><span data-ttu-id="b7ea1-103">\_ \_ Перечисление параметров удаления объекта</span><span class="sxs-lookup"><span data-stu-id="b7ea1-103">DELETE\_OBJECT\_OPTIONS enumeration</span></span>

<span data-ttu-id="b7ea1-104">Тип **перечисления \_ \_ Параметры удаления объекта** описывает параметры, которые поддерживаются устройством при удалении объекта.</span><span class="sxs-lookup"><span data-stu-id="b7ea1-104">The **DELETE\_OBJECT\_OPTIONS** enumeration type describes options that are supported by a device when deleting an object.</span></span>

## <a name="syntax"></a><span data-ttu-id="b7ea1-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b7ea1-105">Syntax</span></span>


```C++
typedef enum DELETE_OBJECT_OPTIONS { 
  PORTABLE_DEVICE_DELETE_NO_RECURSION    = 0,
  PORTABLE_DEVICE_DELETE_WITH_RECURSION  = 1
} ;
```



## <a name="constants"></a><span data-ttu-id="b7ea1-106">Константы</span><span class="sxs-lookup"><span data-stu-id="b7ea1-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="b7ea1-107"><span id="PORTABLE_DEVICE_DELETE_NO_RECURSION"></span><span id="portable_device_delete_no_recursion"></span>**ПЕРЕНОСное \_ устройство \_ \_ не удаляет \_ рекурсию**</span><span class="sxs-lookup"><span data-stu-id="b7ea1-107"><span id="PORTABLE_DEVICE_DELETE_NO_RECURSION"></span><span id="portable_device_delete_no_recursion"></span>**PORTABLE\_DEVICE\_DELETE\_NO\_RECURSION**</span></span>
</dt> <dd>

<span data-ttu-id="b7ea1-108">Удалите только объект и завершите его ошибкой, если у него есть дочерние элементы.</span><span class="sxs-lookup"><span data-stu-id="b7ea1-108">Delete the object only and fail if it has children.</span></span>

</dd> <dt>

<span data-ttu-id="b7ea1-109"><span id="PORTABLE_DEVICE_DELETE_WITH_RECURSION"></span><span id="portable_device_delete_with_recursion"></span>**Удаление ПЕРЕНОСного \_ устройства \_ \_ с \_ рекурсией**</span><span class="sxs-lookup"><span data-stu-id="b7ea1-109"><span id="PORTABLE_DEVICE_DELETE_WITH_RECURSION"></span><span id="portable_device_delete_with_recursion"></span>**PORTABLE\_DEVICE\_DELETE\_WITH\_RECURSION**</span></span>
</dt> <dd>

<span data-ttu-id="b7ea1-110">Удалите объект и все его дочерние элементы.</span><span class="sxs-lookup"><span data-stu-id="b7ea1-110">Delete the object and all its children.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b7ea1-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="b7ea1-111">Remarks</span></span>

<span data-ttu-id="b7ea1-112">Приложение может получить параметры удаления, которые поддерживает устройство, вызвав [**ипортабледевицекапабилитиес:: жеткоммандоптионс**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicecapabilities-getcommandoptions) для команды **WPD \_ команда \_ \_ \_ DELETE \_ Objects** .</span><span class="sxs-lookup"><span data-stu-id="b7ea1-112">The application can retrieve the deletion options that the device supports by calling [**IPortableDeviceCapabilities::GetCommandOptions**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicecapabilities-getcommandoptions) for the **WPD\_COMMAND\_OBJECT\_MANAGEMENT\_DELETE\_OBJECTS** command.</span></span> <span data-ttu-id="b7ea1-113">Он должен проверить значение параметра типа WPD, которое **\_ \_ \_ \_ \_ \_ поддерживает рекурсивное удаление** , которое этот метод возвращает в объекте [**ипортабледевицевалуесколлектион**](iportabledevicevaluescollection.md) .</span><span class="sxs-lookup"><span data-stu-id="b7ea1-113">It should examine the **WPD\_OPTION\_OBJECT\_MANAGEMENT\_RECURSIVE\_DELETE\_SUPPORTED** option value that this method returns in an [**IPortableDeviceValuesCollection**](iportabledevicevaluescollection.md) object.</span></span>

## <a name="requirements"></a><span data-ttu-id="b7ea1-114">Требования</span><span class="sxs-lookup"><span data-stu-id="b7ea1-114">Requirements</span></span>



| <span data-ttu-id="b7ea1-115">Требование</span><span class="sxs-lookup"><span data-stu-id="b7ea1-115">Requirement</span></span> | <span data-ttu-id="b7ea1-116">Значение</span><span class="sxs-lookup"><span data-stu-id="b7ea1-116">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="b7ea1-117">Header</span><span class="sxs-lookup"><span data-stu-id="b7ea1-117">Header</span></span><br/> | <dl> <span data-ttu-id="b7ea1-118"><dt>Портабледевице. h</dt></span><span class="sxs-lookup"><span data-stu-id="b7ea1-118"><dt>PortableDevice.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b7ea1-119">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b7ea1-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b7ea1-120">**Структуры и типы перечислений**</span><span class="sxs-lookup"><span data-stu-id="b7ea1-120">**Structures and Enumeration Types**</span></span>](structures-and-enumeration-types.md)
</dt> </dl>

 

 




