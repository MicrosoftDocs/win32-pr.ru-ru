---
description: Содержит текущее состояние аккумулятора.
ms.assetid: 514906a1-9d7a-40cb-9798-84f6b93d7bfe
title: Структура BATTERY_STATUS (Покласс. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- BATTERY_STATUS
api_type:
- HeaderDef
api_location:
- Poclass.h
- Batclass.h
ms.openlocfilehash: d6e68f5cec0215687fe4fde66698ea1be0d62c6e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105663128"
---
# <a name="battery_status-structure"></a><span data-ttu-id="4c954-103">\_Структура состояния аккумулятора</span><span class="sxs-lookup"><span data-stu-id="4c954-103">BATTERY\_STATUS structure</span></span>

<span data-ttu-id="4c954-104">Содержит текущее состояние аккумулятора.</span><span class="sxs-lookup"><span data-stu-id="4c954-104">Contains the current state of the battery.</span></span> <span data-ttu-id="4c954-105">Эта структура используется кодом управления [**\_ \_ \_ состоянием запроса батареи ioctl**](ioctl-battery-query-status.md) .</span><span class="sxs-lookup"><span data-stu-id="4c954-105">This structure is used by the [**IOCTL\_BATTERY\_QUERY\_STATUS**](ioctl-battery-query-status.md) control code.</span></span>

## <a name="syntax"></a><span data-ttu-id="4c954-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="4c954-106">Syntax</span></span>


```C++
typedef struct _BATTERY_STATUS {
  ULONG PowerState;
  ULONG Capacity;
  ULONG Voltage;
  LONG  Rate;
} BATTERY_STATUS, *PBATTERY_STATUS;
```



## <a name="members"></a><span data-ttu-id="4c954-107">Члены</span><span class="sxs-lookup"><span data-stu-id="4c954-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="4c954-108">**Установлен**</span><span class="sxs-lookup"><span data-stu-id="4c954-108">**PowerState**</span></span>
</dt> <dd>

<span data-ttu-id="4c954-109">Состояние аккумулятора.</span><span class="sxs-lookup"><span data-stu-id="4c954-109">The battery state.</span></span> <span data-ttu-id="4c954-110">Этот элемент может быть равен нулю, одному или нескольким из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="4c954-110">This member can be zero, one, or more of the following values.</span></span>



| <span data-ttu-id="4c954-111">Значение</span><span class="sxs-lookup"><span data-stu-id="4c954-111">Value</span></span>                                                                                                                                                                                                                                                   | <span data-ttu-id="4c954-112">Значение</span><span class="sxs-lookup"><span data-stu-id="4c954-112">Meaning</span></span>                                                                                              |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| <span id="BATTERY_CHARGING"></span><span id="battery_charging"></span><dl> <span data-ttu-id="4c954-113"><dt>**Батарея \_ ЗАРЯДка**</dt> <dt>0x00000004</dt></span><span class="sxs-lookup"><span data-stu-id="4c954-113"><dt>**BATTERY\_CHARGING**</dt> <dt>0x00000004</dt></span></span> </dl>                  | <span data-ttu-id="4c954-114">Указывает, что батарея в настоящий момент заряжается.</span><span class="sxs-lookup"><span data-stu-id="4c954-114">Indicates that the battery is currently charging.</span></span><br/>                                         |
| <span id="BATTERY_CRITICAL"></span><span id="battery_critical"></span><dl> <span data-ttu-id="4c954-115"><dt>**Батарея \_ КРИТическая**</dt> <dt>0x00000008</dt></span><span class="sxs-lookup"><span data-stu-id="4c954-115"><dt>**BATTERY\_CRITICAL**</dt> <dt>0x00000008</dt></span></span> </dl>                  | <span data-ttu-id="4c954-116">Указывает, что сбой батареи приближается.</span><span class="sxs-lookup"><span data-stu-id="4c954-116">Indicates that battery failure is imminent.</span></span> <span data-ttu-id="4c954-117">Дополнительные сведения см. в разделе "Примечания".</span><span class="sxs-lookup"><span data-stu-id="4c954-117">See the Remarks section for more information.</span></span><br/> |
| <span id="BATTERY_DISCHARGING"></span><span id="battery_discharging"></span><dl> <span data-ttu-id="4c954-118"><dt>**Батарея \_**</dt>Выставление счетов <dt>0x00000002</dt></span><span class="sxs-lookup"><span data-stu-id="4c954-118"><dt>**BATTERY\_DISCHARGING**</dt> <dt>0x00000002</dt></span></span> </dl>         | <span data-ttu-id="4c954-119">Указывает, что батарея в настоящее время расряжается.</span><span class="sxs-lookup"><span data-stu-id="4c954-119">Indicates that the battery is currently discharging.</span></span><br/>                                      |
| <span id="BATTERY_POWER_ON_LINE"></span><span id="battery_power_on_line"></span><dl> <span data-ttu-id="4c954-120"><dt>**Батарея \_ ПИТАНИЕ \_ в \_ строке**</dt> <dt>0x00000001</dt></span><span class="sxs-lookup"><span data-stu-id="4c954-120"><dt>**BATTERY\_POWER\_ON\_LINE**</dt> <dt>0x00000001</dt></span></span> </dl> | <span data-ttu-id="4c954-121">Указывает, что система имеет доступ к питанию от сети, поэтому батарея не взимается.</span><span class="sxs-lookup"><span data-stu-id="4c954-121">Indicates that the system has access to AC power, so no batteries are being discharged.</span></span><br/>   |



 

</dd> <dt>

<span data-ttu-id="4c954-122">**Производительность**</span><span class="sxs-lookup"><span data-stu-id="4c954-122">**Capacity**</span></span>
</dt> <dd>

<span data-ttu-id="4c954-123">Текущая емкость аккумулятора в mWh (или относительное значение).</span><span class="sxs-lookup"><span data-stu-id="4c954-123">The current battery capacity, in mWh (or relative).</span></span> <span data-ttu-id="4c954-124">Это значение можно использовать для создания дисплея "датчик газа", разделив его на **фуллчаржедкапаЦити** члена структуры [**аккумулятора \_**](battery-information-str.md) .</span><span class="sxs-lookup"><span data-stu-id="4c954-124">This value can be used to generate a "gas gauge" display by dividing it by **FullChargedCapacity** member of the [**BATTERY\_INFORMATION**](battery-information-str.md) structure.</span></span> <span data-ttu-id="4c954-125">Если емкость недоступна, этот член имеет \_ неизвестную \_ емкость аккумулятора.</span><span class="sxs-lookup"><span data-stu-id="4c954-125">If the capacity is unavailable, this member is BATTERY\_UNKNOWN\_CAPACITY.</span></span>

</dd> <dt>

<span data-ttu-id="4c954-126">**Напряжение**</span><span class="sxs-lookup"><span data-stu-id="4c954-126">**Voltage**</span></span>
</dt> <dd>

<span data-ttu-id="4c954-127">Текущее напряжение батареи между батареями, в милливольтах (MV).</span><span class="sxs-lookup"><span data-stu-id="4c954-127">The current battery voltage across the battery terminals, in millivolts (mv).</span></span> <span data-ttu-id="4c954-128">Если напряжение недоступно, этот член является \_ неизвестным \_ напряжением аккумулятора.</span><span class="sxs-lookup"><span data-stu-id="4c954-128">If the voltage is unavailable, this member is BATTERY\_UNKNOWN\_VOLTAGE.</span></span>

</dd> <dt>

<span data-ttu-id="4c954-129">**Скорость**</span><span class="sxs-lookup"><span data-stu-id="4c954-129">**Rate**</span></span>
</dt> <dd>

<span data-ttu-id="4c954-130">Текущая частота зарядки аккумулятора или разрядов.</span><span class="sxs-lookup"><span data-stu-id="4c954-130">The current rate of battery charge or discharge.</span></span> <span data-ttu-id="4c954-131">Это значение будет равно МВт, если сведения о доле аккумулятора не являются относительными. в этом случае он будет находиться в произвольных единицах в час.</span><span class="sxs-lookup"><span data-stu-id="4c954-131">This value will be in milliwatts unless the battery rate information is relative, in which case it will be in arbitrary units per hour.</span></span> <span data-ttu-id="4c954-132">Чтобы определить, относительны ли сведения о батарее, проверьте относительный \_ флаг емкости аккумулятора \_ в элементе **capabilities** структуры [**\_ сведений о батарее**](battery-information-str.md) .</span><span class="sxs-lookup"><span data-stu-id="4c954-132">To determine if battery information is relative, examine the BATTERY\_CAPACITY\_RELATIVE flag in the **Capabilities** member of the [**BATTERY\_INFORMATION**](battery-information-str.md) structure.</span></span> <span data-ttu-id="4c954-133">Ненулевая положительная ставка означает оплату; отрицательная ставка указывает на отсчет расзарядки.</span><span class="sxs-lookup"><span data-stu-id="4c954-133">A nonzero, positive rate indicates charging; a negative rate indicates discharging.</span></span> <span data-ttu-id="4c954-134">Некоторые батареи сообщают только о тарифах за оплату.</span><span class="sxs-lookup"><span data-stu-id="4c954-134">Some batteries report only discharging rates.</span></span> <span data-ttu-id="4c954-135">Если скорость недоступна, этот член имеет \_ неизвестный уровень заряда аккумулятора \_ .</span><span class="sxs-lookup"><span data-stu-id="4c954-135">If the rate is unavailable, this member is BATTERY\_UNKNOWN\_RATE.</span></span> <span data-ttu-id="4c954-136">Если состояние батареи или источника питания меняется, скорость может стать доступной.</span><span class="sxs-lookup"><span data-stu-id="4c954-136">If the state of the battery or power source changes, the rate may become available.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="4c954-137">Комментарии</span><span class="sxs-lookup"><span data-stu-id="4c954-137">Remarks</span></span>

<span data-ttu-id="4c954-138">\_Флаг критической батареи в элементе **PowerState** этой структуры указывает на оборудование "критическая батарея".</span><span class="sxs-lookup"><span data-stu-id="4c954-138">The BATTERY\_CRITICAL flag in the **PowerState** member of this structure indicates a hardware "battery critical" condition.</span></span> <span data-ttu-id="4c954-139">Этот критический уровень задается производителем батареи, а не пользователем в оповещении о критической батарее.</span><span class="sxs-lookup"><span data-stu-id="4c954-139">This critical level is set by the battery manufacturer, not by the user in the "critical battery alarm."</span></span> <span data-ttu-id="4c954-140">Обычно это означает, что батарея подсчитывает, что батарея полностью обработана, а все нарисованное питание выходит за рамки ожидаемого.</span><span class="sxs-lookup"><span data-stu-id="4c954-140">It generally means that the battery system has calculated that the battery is totally drained, and any power being drawn is beyond what is expected.</span></span>

## <a name="requirements"></a><span data-ttu-id="4c954-141">Требования</span><span class="sxs-lookup"><span data-stu-id="4c954-141">Requirements</span></span>



| <span data-ttu-id="4c954-142">Требование</span><span class="sxs-lookup"><span data-stu-id="4c954-142">Requirement</span></span> | <span data-ttu-id="4c954-143">Значение</span><span class="sxs-lookup"><span data-stu-id="4c954-143">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4c954-144">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="4c954-144">Minimum supported client</span></span><br/> | <span data-ttu-id="4c954-145">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="4c954-145">Windows XP \[desktop apps only\]</span></span><br/>                                                                                                                                                                                                                         |
| <span data-ttu-id="4c954-146">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="4c954-146">Minimum supported server</span></span><br/> | <span data-ttu-id="4c954-147">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="4c954-147">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                                                                                                                                                                                |
| <span data-ttu-id="4c954-148">Header</span><span class="sxs-lookup"><span data-stu-id="4c954-148">Header</span></span><br/>                   | <dl> <span data-ttu-id="4c954-149"><dt>Покласс. h; </dt> <dt>Баткласс. h в Windows server 2008 R2, Windows 7, Windows server 2008, Windows Vista, Windows server 2003 и Windows XP</dt></span><span class="sxs-lookup"><span data-stu-id="4c954-149"><dt>Poclass.h; </dt> <dt>Batclass.h on Windows Server 2008 R2, Windows 7, Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4c954-150">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="4c954-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4c954-151">**\_сведения о батарее**</span><span class="sxs-lookup"><span data-stu-id="4c954-151">**BATTERY\_INFORMATION**</span></span>](battery-information-str.md)
</dt> <dt>

[<span data-ttu-id="4c954-152">**\_ \_ состояние запроса аккумулятора \_ ioctl**</span><span class="sxs-lookup"><span data-stu-id="4c954-152">**IOCTL\_BATTERY\_QUERY\_STATUS**</span></span>](ioctl-battery-query-status.md)
</dt> </dl>

 

 




