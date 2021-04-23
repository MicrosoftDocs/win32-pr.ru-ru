---
description: Содержит сведения о батарее, которые необходимо задать.
ms.assetid: 535e56cb-2bab-458a-84a8-2d9a4d96412b
title: Структура BATTERY_SET_INFORMATION (Покласс. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- BATTERY_SET_INFORMATION
api_type:
- HeaderDef
api_location:
- Poclass.h
- Batclass.h
ms.openlocfilehash: 0b23489bc5a7608e2e8afb297bb4be7ba35cecb6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104156519"
---
# <a name="battery_set_information-structure"></a><span data-ttu-id="6955c-103">\_ \_ Информационная структура набора аккумулятора</span><span class="sxs-lookup"><span data-stu-id="6955c-103">BATTERY\_SET\_INFORMATION structure</span></span>

<span data-ttu-id="6955c-104">Содержит сведения о батарее, которые необходимо задать.</span><span class="sxs-lookup"><span data-stu-id="6955c-104">Contains battery information to be set.</span></span> <span data-ttu-id="6955c-105">Эта структура используется с кодом контроля [**\_ \_ \_ информации о батарее ioctl**](ioctl-battery-set-information.md) .</span><span class="sxs-lookup"><span data-stu-id="6955c-105">This structure is used with the [**IOCTL\_BATTERY\_SET\_INFORMATION**](ioctl-battery-set-information.md) control code.</span></span>

## <a name="syntax"></a><span data-ttu-id="6955c-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="6955c-106">Syntax</span></span>


```C++
typedef struct _BATTERY_SET_INFORMATION {
  ULONG                         BatteryTag;
  BATTERY_SET_INFORMATION_LEVEL InformationLevel;
  UCHAR                         Buffer[1];
} BATTERY_SET_INFORMATION, *PBATTERY_SET_INFORMATION;
```



## <a name="members"></a><span data-ttu-id="6955c-107">Члены</span><span class="sxs-lookup"><span data-stu-id="6955c-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="6955c-108">**баттеритаг**</span><span class="sxs-lookup"><span data-stu-id="6955c-108">**BatteryTag**</span></span>
</dt> <dd>

<span data-ttu-id="6955c-109">Текущий тег батареи для аккумулятора.</span><span class="sxs-lookup"><span data-stu-id="6955c-109">The current battery tag for the battery.</span></span> <span data-ttu-id="6955c-110">Информация о батарее, соответствующем тегу, может быть возвращена только.</span><span class="sxs-lookup"><span data-stu-id="6955c-110">Information for a battery matching the tag can only be returned.</span></span> <span data-ttu-id="6955c-111">Если это значение не соответствует текущему тегу батареи, запрос IOCTL будет выполнен с ошибкой \_ \_ не \_ найден файл, который указывает вызывающему объекту, что батарея, для которой у него есть тег, больше не существует.</span><span class="sxs-lookup"><span data-stu-id="6955c-111">Whenever this value does not match the battery's current tag, the IOCTL request will be completed with ERROR\_FILE\_NOT\_FOUND, which indicates to the caller that the battery for which it has a tag for no longer exists.</span></span> <span data-ttu-id="6955c-112">Вызывающий объект может использовать операцию [**запроса IOCTL \_ аккумулятора \_ \_**](ioctl-battery-query-tag.md) для определения тега вновь установленного аккумулятора, если он существует.</span><span class="sxs-lookup"><span data-stu-id="6955c-112">The caller may opt to use the [**IOCTL\_BATTERY\_QUERY\_TAG**](ioctl-battery-query-tag.md) operation to determine the tag of the newly installed battery, if one exists.</span></span> <span data-ttu-id="6955c-113">(Дополнительные сведения см. в разделе " [теги батареи](battery-information.md) ".)</span><span class="sxs-lookup"><span data-stu-id="6955c-113">(See [Battery Tags](battery-information.md) for more information.)</span></span>

<span data-ttu-id="6955c-114">При запросе сведений о запросе это значение проверяется.</span><span class="sxs-lookup"><span data-stu-id="6955c-114">When a query information request is made, this value is verified.</span></span> <span data-ttu-id="6955c-115">Кроме того, если при изменении значения этого параметра выполняется запрос, запрос прерывается с состоянием " \_ файл \_ не \_ найден".</span><span class="sxs-lookup"><span data-stu-id="6955c-115">In addition, if the request is in progress while this value changes, the request is aborted with the status of ERROR\_FILE\_NOT\_FOUND.</span></span>

</dd> <dt>

<span data-ttu-id="6955c-116">**информатионлевел**</span><span class="sxs-lookup"><span data-stu-id="6955c-116">**InformationLevel**</span></span>
</dt> <dd>

<span data-ttu-id="6955c-117">Заданные сведения о батарее.</span><span class="sxs-lookup"><span data-stu-id="6955c-117">The battery information to be set.</span></span> <span data-ttu-id="6955c-118">Тип данных в элементе **buffer** зависит от значения этого элемента.</span><span class="sxs-lookup"><span data-stu-id="6955c-118">The type of data in the **Buffer** member depends on the value of this member.</span></span> <span data-ttu-id="6955c-119">Этот элемент может принимать одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="6955c-119">This member can be one of the following values.</span></span>



| <span data-ttu-id="6955c-120">Значение</span><span class="sxs-lookup"><span data-stu-id="6955c-120">Value</span></span>                                                                                                                                                                                                                                                                       | <span data-ttu-id="6955c-121">Значение</span><span class="sxs-lookup"><span data-stu-id="6955c-121">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                              |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="BatteryCharge"></span><span id="batterycharge"></span><span id="BATTERYCHARGE"></span><dl> <span data-ttu-id="6955c-122"><dt>**Баттеричарже**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="6955c-122"><dt>**BatteryCharge**</dt> <dt>1</dt></span></span> </dl>                         | <span data-ttu-id="6955c-123">Информирует устройство аккумулятора о том, что в данный момент батарея должна быть заряжается.</span><span class="sxs-lookup"><span data-stu-id="6955c-123">Informs the battery device that the user has requested that the battery should be charging at this time.</span></span> <span data-ttu-id="6955c-124">Например, при использовании смарт-аккумулятора, зарядное устройство и селектора в приложении может взиматься плата за один аккумулятор за раз.</span><span class="sxs-lookup"><span data-stu-id="6955c-124">For example, with a smart battery/charger/selector, the application could charge one battery at a time.</span></span> <span data-ttu-id="6955c-125">Элемент **буфера** этой структуры игнорируется.</span><span class="sxs-lookup"><span data-stu-id="6955c-125">The **Buffer** member of this structure is ignored.</span></span><br/>                                                                      |
| <span id="BatteryCriticalBias"></span><span id="batterycriticalbias"></span><span id="BATTERYCRITICALBIAS"></span><dl> <span data-ttu-id="6955c-126"><dt>**Баттерикритикалбиас**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="6955c-126"><dt>**BatteryCriticalBias**</dt> <dt>0</dt></span></span> </dl> | <span data-ttu-id="6955c-127">Задает критическую коррекцию смещения батареи.</span><span class="sxs-lookup"><span data-stu-id="6955c-127">Sets the battery's critical bias adjustment.</span></span> <span data-ttu-id="6955c-128">Обратите внимание, что это значение, как правило, будет изменено программным обеспечением и представлено в интерфейсах только в качестве функции обслуживания.</span><span class="sxs-lookup"><span data-stu-id="6955c-128">Note it is not envisioned that this value would normally be changed by software, and is present in the interfaces only as a maintenance feature.</span></span> <span data-ttu-id="6955c-129">Не все батареи поддерживают такой параметр, и сведения о батарее должны быть считаны для подтверждения того, что батарея принимает параметр.</span><span class="sxs-lookup"><span data-stu-id="6955c-129">Not all batteries can maintain such a setting, and the battery information should be read to confirm that the battery accepted the setting.</span></span><br/> |
| <span id="BatteryDischarge"></span><span id="batterydischarge"></span><span id="BATTERYDISCHARGE"></span><dl> <span data-ttu-id="6955c-130"><dt>**Баттеридисчарже**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="6955c-130"><dt>**BatteryDischarge**</dt> <dt>2</dt></span></span> </dl>             | <span data-ttu-id="6955c-131">Информирует устройство аккумулятора о том, что в настоящее время батарея запросила отсчетку аккумулятора.</span><span class="sxs-lookup"><span data-stu-id="6955c-131">Informs the battery device that the user has requested that the battery be discharging at this time.</span></span> <span data-ttu-id="6955c-132">Например, это можно использовать для указания аккумулятора, которую пользователь хочет включить в систему.</span><span class="sxs-lookup"><span data-stu-id="6955c-132">For example, this could be used to indicate which battery the user currently wants to power the system.</span></span> <span data-ttu-id="6955c-133">Элемент **буфера** этой структуры игнорируется.</span><span class="sxs-lookup"><span data-stu-id="6955c-133">The **Buffer** member of this structure is ignored.</span></span><br/>                                                                          |



 

</dd> <dt>

<span data-ttu-id="6955c-134">**Буфер**</span><span class="sxs-lookup"><span data-stu-id="6955c-134">**Buffer**</span></span>
</dt> <dd>

<span data-ttu-id="6955c-135">Заданные сведения о батарее.</span><span class="sxs-lookup"><span data-stu-id="6955c-135">The battery information to be set.</span></span> <span data-ttu-id="6955c-136">Данные зависят от значения **информатионлевел**.</span><span class="sxs-lookup"><span data-stu-id="6955c-136">The data depends on the value of **InformationLevel**.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="6955c-137">Комментарии</span><span class="sxs-lookup"><span data-stu-id="6955c-137">Remarks</span></span>

<span data-ttu-id="6955c-138">**\_ \_ Информационная структура набора аккумулятора** является структурой переменной длины, и необходимо выделить буфер подходящего размера для включения данных в структуру.</span><span class="sxs-lookup"><span data-stu-id="6955c-138">The **BATTERY\_SET\_INFORMATION** structure is a variable-length structure, and you must allocate a buffer of suitable size for the information to be included in the structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="6955c-139">Требования</span><span class="sxs-lookup"><span data-stu-id="6955c-139">Requirements</span></span>



| <span data-ttu-id="6955c-140">Требование</span><span class="sxs-lookup"><span data-stu-id="6955c-140">Requirement</span></span> | <span data-ttu-id="6955c-141">Значение</span><span class="sxs-lookup"><span data-stu-id="6955c-141">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6955c-142">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="6955c-142">Minimum supported client</span></span><br/> | <span data-ttu-id="6955c-143">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="6955c-143">Windows XP \[desktop apps only\]</span></span><br/>                                                                                                                                                                                                                         |
| <span data-ttu-id="6955c-144">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="6955c-144">Minimum supported server</span></span><br/> | <span data-ttu-id="6955c-145">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="6955c-145">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                                                                                                                                                                                |
| <span data-ttu-id="6955c-146">Header</span><span class="sxs-lookup"><span data-stu-id="6955c-146">Header</span></span><br/>                   | <dl> <span data-ttu-id="6955c-147"><dt>Покласс. h; </dt> <dt>Баткласс. h в Windows server 2008 R2, Windows 7, Windows server 2008, Windows Vista, Windows server 2003 и Windows XP</dt></span><span class="sxs-lookup"><span data-stu-id="6955c-147"><dt>Poclass.h; </dt> <dt>Batclass.h on Windows Server 2008 R2, Windows 7, Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6955c-148">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="6955c-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6955c-149">**\_ \_ сведения о настройке аккумулятора ioctl \_**</span><span class="sxs-lookup"><span data-stu-id="6955c-149">**IOCTL\_BATTERY\_SET\_INFORMATION**</span></span>](ioctl-battery-set-information.md)
</dt> </dl>

 

 




