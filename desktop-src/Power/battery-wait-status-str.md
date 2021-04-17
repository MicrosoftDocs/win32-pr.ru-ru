---
description: Содержит сведения об условиях, при которых будет получено состояние аккумулятора.
ms.assetid: 1750fe0f-ba3d-4118-938c-789c6d62c3f7
title: Структура BATTERY_WAIT_STATUS (Покласс. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- BATTERY_WAIT_STATUS
api_type:
- HeaderDef
api_location:
- Poclass.h
- Batclass.h
ms.openlocfilehash: 08d1e3b85d22122426f1e4648f47a808468bfb8f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105663127"
---
# <a name="battery_wait_status-structure"></a><span data-ttu-id="43f36-103">\_ \_ Структура состояния ожидания аккумулятора</span><span class="sxs-lookup"><span data-stu-id="43f36-103">BATTERY\_WAIT\_STATUS structure</span></span>

<span data-ttu-id="43f36-104">Содержит сведения об условиях, при которых будет получено состояние аккумулятора.</span><span class="sxs-lookup"><span data-stu-id="43f36-104">Contains information about the conditions under which the battery status is to be retrieved.</span></span> <span data-ttu-id="43f36-105">Эта структура используется кодом управления [**\_ \_ \_ состоянием запроса батареи ioctl**](ioctl-battery-query-status.md) .</span><span class="sxs-lookup"><span data-stu-id="43f36-105">This structure is used by the [**IOCTL\_BATTERY\_QUERY\_STATUS**](ioctl-battery-query-status.md) control code.</span></span>

## <a name="syntax"></a><span data-ttu-id="43f36-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="43f36-106">Syntax</span></span>


```C++
typedef struct _BATTERY_WAIT_STATUS {
  ULONG BatteryTag;
  ULONG Timeout;
  ULONG PowerState;
  ULONG LowCapacity;
  ULONG HighCapacity;
} BATTERY_WAIT_STATUS, *PBATTERY_WAIT_STATUS;
```



## <a name="members"></a><span data-ttu-id="43f36-107">Члены</span><span class="sxs-lookup"><span data-stu-id="43f36-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="43f36-108">**баттеритаг**</span><span class="sxs-lookup"><span data-stu-id="43f36-108">**BatteryTag**</span></span>
</dt> <dd>

<span data-ttu-id="43f36-109">Текущий тег батареи для аккумулятора.</span><span class="sxs-lookup"><span data-stu-id="43f36-109">The current battery tag for the battery.</span></span> <span data-ttu-id="43f36-110">Могут быть возвращены только сведения о батарее, соответствующем тегу.</span><span class="sxs-lookup"><span data-stu-id="43f36-110">Only information for a battery matching the tag can be returned.</span></span> <span data-ttu-id="43f36-111">Если это значение не соответствует текущему тегу батареи, операция [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) завершится ошибкой с кодом ошибки \_ \_ не \_ найден, что указывает вызывающему объекту, что батарея, для которой он имеет тег, больше не установлена. вызывающий объект может использовать операцию [**\_ \_ запроса \_ на батарею**](ioctl-battery-query-tag.md) , чтобы определить тег только что установленного аккумулятора (при наличии).</span><span class="sxs-lookup"><span data-stu-id="43f36-111">Whenever this value does not match the battery's current tag, the [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) operation will fail with an error code of ERROR\_FILE\_NOT\_FOUND, which indicates to the caller that the battery for which it has a tag is no longer installed The caller may opt to use the [**IOCTL\_BATTERY\_QUERY\_TAG**](ioctl-battery-query-tag.md) operation to determine the tag of the newly installed battery, if any.</span></span> <span data-ttu-id="43f36-112">Кроме того, если запрос выполняется после удаления батареи или при изменении тега, операция прерывается с состоянием " \_ файл \_ не \_ найден".</span><span class="sxs-lookup"><span data-stu-id="43f36-112">In addition, if the request is in progress when the battery is removed, or the tag changes, the operation is aborted with the status of ERROR\_FILE\_NOT\_FOUND.</span></span> <span data-ttu-id="43f36-113">(Дополнительные сведения см. в разделе " [теги батареи](battery-information.md) ".)</span><span class="sxs-lookup"><span data-stu-id="43f36-113">(See [Battery Tags](battery-information.md) for more information.)</span></span>

</dd> <dt>

<span data-ttu-id="43f36-114">**Timeout**</span><span class="sxs-lookup"><span data-stu-id="43f36-114">**Timeout**</span></span>
</dt> <dd>

<span data-ttu-id="43f36-115">Число миллисекунд, в течение которых запрос будет ожидать условие, заданное членами **PowerState**, **ловкапаЦити** и **хигхкапаЦити** , перед завершением.</span><span class="sxs-lookup"><span data-stu-id="43f36-115">The number of milliseconds the request will wait for the condition specified by the **PowerState**, **LowCapacity**, and **HighCapacity** members before completing.</span></span> <span data-ttu-id="43f36-116">Значение-1 указывает, что запрос будет ожидать неограниченное время ожидания условий.</span><span class="sxs-lookup"><span data-stu-id="43f36-116">A value of -1 indicates that the request will wait indefinitely for the conditions to be satisfied.</span></span> <span data-ttu-id="43f36-117">Нулевое значение указывает, что запрошенные сведения о батарее должны возвращаться немедленно, независимо от других условий.</span><span class="sxs-lookup"><span data-stu-id="43f36-117">A value of zero indicates that the requested battery information is to be returned immediately, regardless of the other conditions.</span></span> <span data-ttu-id="43f36-118">Любое другое значение указывает на то, что запрос должен ждать в течение времени или до тех пор, пока не будет выполнено какое-либо другое условие.</span><span class="sxs-lookup"><span data-stu-id="43f36-118">Any other value indicates that the request should wait that length of time, or until any one of the other conditions is satisfied.</span></span>

<span data-ttu-id="43f36-119">Если компьютер перешел в спящий режим, часы будут продолжать выполняться, но исчерпание счетчика не приведет к выходу компьютера из спящего режима.</span><span class="sxs-lookup"><span data-stu-id="43f36-119">If the computer has entered sleep mode, the clock will continue to run, but exhausting the count will not wake the computer up.</span></span> <span data-ttu-id="43f36-120">Если счетчик будет исчерпан, когда компьютер пробудится, и выполняются другие условия, вызов немедленно возвратится при пробуждении.</span><span class="sxs-lookup"><span data-stu-id="43f36-120">If the count is exhausted when the computer is awoken, and other conditions are satisfied, the call will return immediately on awakening.</span></span>

</dd> <dt>

<span data-ttu-id="43f36-121">**Установлен**</span><span class="sxs-lookup"><span data-stu-id="43f36-121">**PowerState**</span></span>
</dt> <dd>

<span data-ttu-id="43f36-122">Ноль, один или несколько следующих битов состояния, которые указывают состояние аккумулятора.</span><span class="sxs-lookup"><span data-stu-id="43f36-122">Zero, one, or more of the following status bits, which indicate the state of the battery.</span></span> <span data-ttu-id="43f36-123">Он идентичен элементу **PowerState** структуры [**\_ состояния аккумулятора**](battery-status-str.md) .</span><span class="sxs-lookup"><span data-stu-id="43f36-123">It is identical to the **PowerState** member of the [**BATTERY\_STATUS**](battery-status-str.md) structure.</span></span>



| <span data-ttu-id="43f36-124">Значение</span><span class="sxs-lookup"><span data-stu-id="43f36-124">Value</span></span>                                                                                                                                                                                                                                                   | <span data-ttu-id="43f36-125">Значение</span><span class="sxs-lookup"><span data-stu-id="43f36-125">Meaning</span></span>                                                                                              |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| <span id="BATTERY_CHARGING"></span><span id="battery_charging"></span><dl> <span data-ttu-id="43f36-126"><dt>**Батарея \_ ЗАРЯДка**</dt> <dt>0x00000004</dt></span><span class="sxs-lookup"><span data-stu-id="43f36-126"><dt>**BATTERY\_CHARGING**</dt> <dt>0x00000004</dt></span></span> </dl>                  | <span data-ttu-id="43f36-127">Указывает, что батарея в настоящий момент заряжается.</span><span class="sxs-lookup"><span data-stu-id="43f36-127">Indicates that the battery is currently charging.</span></span><br/>                                         |
| <span id="BATTERY_CRITICAL"></span><span id="battery_critical"></span><dl> <span data-ttu-id="43f36-128"><dt>**Батарея \_ КРИТическая**</dt> <dt>0x00000008</dt></span><span class="sxs-lookup"><span data-stu-id="43f36-128"><dt>**BATTERY\_CRITICAL**</dt> <dt>0x00000008</dt></span></span> </dl>                  | <span data-ttu-id="43f36-129">Указывает, что сбой батареи приближается.</span><span class="sxs-lookup"><span data-stu-id="43f36-129">Indicates that battery failure is imminent.</span></span> <span data-ttu-id="43f36-130">Дополнительные сведения см. в разделе "Примечания".</span><span class="sxs-lookup"><span data-stu-id="43f36-130">See the Remarks section for more information.</span></span><br/> |
| <span id="BATTERY_DISCHARGING"></span><span id="battery_discharging"></span><dl> <span data-ttu-id="43f36-131"><dt>**Батарея \_**</dt>Выставление счетов <dt>0x00000002</dt></span><span class="sxs-lookup"><span data-stu-id="43f36-131"><dt>**BATTERY\_DISCHARGING**</dt> <dt>0x00000002</dt></span></span> </dl>         | <span data-ttu-id="43f36-132">Указывает, что батарея в настоящее время расряжается.</span><span class="sxs-lookup"><span data-stu-id="43f36-132">Indicates that the battery is currently discharging.</span></span><br/>                                      |
| <span id="BATTERY_POWER_ON_LINE"></span><span id="battery_power_on_line"></span><dl> <span data-ttu-id="43f36-133"><dt>**Батарея \_ ПИТАНИЕ \_ в \_ строке**</dt> <dt>0x00000001</dt></span><span class="sxs-lookup"><span data-stu-id="43f36-133"><dt>**BATTERY\_POWER\_ON\_LINE**</dt> <dt>0x00000001</dt></span></span> </dl> | <span data-ttu-id="43f36-134">Указывает, что батарея имеет доступ к питанию от сети.</span><span class="sxs-lookup"><span data-stu-id="43f36-134">Indicates that the battery has access to AC power.</span></span><br/>                                        |



 

</dd> <dt>

<span data-ttu-id="43f36-135">**ловкапаЦити**</span><span class="sxs-lookup"><span data-stu-id="43f36-135">**LowCapacity**</span></span>
</dt> <dd>

<span data-ttu-id="43f36-136">Текущая емкость аккумулятора в mWh (или относительное значение).</span><span class="sxs-lookup"><span data-stu-id="43f36-136">The current battery capacity, in mWh (or relative).</span></span> <span data-ttu-id="43f36-137">Это значение идентично значению элемента **Capacity** структуры [**\_ состояния аккумулятора**](battery-status-str.md) .</span><span class="sxs-lookup"><span data-stu-id="43f36-137">This value is identical to the **Capacity** member of the [**BATTERY\_STATUS**](battery-status-str.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="43f36-138">**хигхкапаЦити**</span><span class="sxs-lookup"><span data-stu-id="43f36-138">**HighCapacity**</span></span>
</dt> <dd>

<span data-ttu-id="43f36-139">Текущая емкость аккумулятора в mWh (или относительное значение).</span><span class="sxs-lookup"><span data-stu-id="43f36-139">The current battery capacity, in mWh (or relative).</span></span> <span data-ttu-id="43f36-140">Это значение идентично значению элемента **Capacity** структуры [**\_ состояния аккумулятора**](battery-status-str.md) .</span><span class="sxs-lookup"><span data-stu-id="43f36-140">This value is identical to the **Capacity** member of the [**BATTERY\_STATUS**](battery-status-str.md) structure.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="43f36-141">Комментарии</span><span class="sxs-lookup"><span data-stu-id="43f36-141">Remarks</span></span>

<span data-ttu-id="43f36-142">Запросы сведений о батарее откладываются до тех пор, пока не произойдет одно из следующих событий:</span><span class="sxs-lookup"><span data-stu-id="43f36-142">Requests for battery information are postponed until one of the following occurs:</span></span>

-   <span data-ttu-id="43f36-143">Время ожидания истекает (если **время ожидания** не равно-1).</span><span class="sxs-lookup"><span data-stu-id="43f36-143">The time-out expires (assuming **Timeout** is not -1).</span></span>
-   <span data-ttu-id="43f36-144">Текущее состояние батареи не соответствует **PowerState**.</span><span class="sxs-lookup"><span data-stu-id="43f36-144">The battery's current status does not match **PowerState**.</span></span>
-   <span data-ttu-id="43f36-145">Емкость батареи ниже **ловкапаЦити**.</span><span class="sxs-lookup"><span data-stu-id="43f36-145">The battery's capacity is below **LowCapacity**.</span></span>
-   <span data-ttu-id="43f36-146">Емкость батареи выше **хигхкапаЦити**.</span><span class="sxs-lookup"><span data-stu-id="43f36-146">The battery's capacity is above **HighCapacity**.</span></span>
-   <span data-ttu-id="43f36-147">Изменился тег аккумулятора.</span><span class="sxs-lookup"><span data-stu-id="43f36-147">The battery tag changes.</span></span>

<span data-ttu-id="43f36-148">Когда выполняется какое-либо из этих условий, данные собираются и операция возвращает.</span><span class="sxs-lookup"><span data-stu-id="43f36-148">When any one of these conditions is satisfied, the data is collected and the operation returns.</span></span> <span data-ttu-id="43f36-149">Это позволяет приложениям отслеживать типичные сведения о динамических батареях без опроса устройства.</span><span class="sxs-lookup"><span data-stu-id="43f36-149">This allows applications to monitor typical dynamic battery information without polling the device.</span></span>

<span data-ttu-id="43f36-150">Прежде чем использовать одно из двух условий емкости, убедитесь, что батарея поддерживает их, используя код элемента управления [**\_ \_ \_ аккумулятора ioctl**](ioctl-battery-query-status.md) с нулевым временем ожидания.</span><span class="sxs-lookup"><span data-stu-id="43f36-150">Before using either of the two Capacity conditions, make sure the battery supports them by using the [**IOCTL\_BATTERY\_QUERY\_STATUS**](ioctl-battery-query-status.md) control code with a time-out of zero.</span></span> <span data-ttu-id="43f36-151">Проверьте результаты, чтобы определить, поддерживается ли элемент **емкости** (то есть \_ неизвестная емкость батареи \_ ).</span><span class="sxs-lookup"><span data-stu-id="43f36-151">Examine the results to determine if the **Capacity** member is supported (that is, not BATTERY\_UNKNOWN\_CAPACITY).</span></span>

## <a name="requirements"></a><span data-ttu-id="43f36-152">Требования</span><span class="sxs-lookup"><span data-stu-id="43f36-152">Requirements</span></span>



| <span data-ttu-id="43f36-153">Требование</span><span class="sxs-lookup"><span data-stu-id="43f36-153">Requirement</span></span> | <span data-ttu-id="43f36-154">Значение</span><span class="sxs-lookup"><span data-stu-id="43f36-154">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="43f36-155">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="43f36-155">Minimum supported client</span></span><br/> | <span data-ttu-id="43f36-156">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="43f36-156">Windows XP \[desktop apps only\]</span></span><br/>                                                                                                                                                                                                                         |
| <span data-ttu-id="43f36-157">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="43f36-157">Minimum supported server</span></span><br/> | <span data-ttu-id="43f36-158">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="43f36-158">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                                                                                                                                                                                |
| <span data-ttu-id="43f36-159">Header</span><span class="sxs-lookup"><span data-stu-id="43f36-159">Header</span></span><br/>                   | <dl> <span data-ttu-id="43f36-160"><dt>Покласс. h; </dt> <dt>Баткласс. h в Windows server 2008 R2, Windows 7, Windows server 2008, Windows Vista, Windows server 2003 и Windows XP</dt></span><span class="sxs-lookup"><span data-stu-id="43f36-160"><dt>Poclass.h; </dt> <dt>Batclass.h on Windows Server 2008 R2, Windows 7, Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="43f36-161">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="43f36-161">See also</span></span>

<dl> <dt>

[<span data-ttu-id="43f36-162">**\_состояние аккумулятора**</span><span class="sxs-lookup"><span data-stu-id="43f36-162">**BATTERY\_STATUS**</span></span>](battery-status-str.md)
</dt> <dt>

[<span data-ttu-id="43f36-163">**\_ \_ состояние запроса аккумулятора \_ ioctl**</span><span class="sxs-lookup"><span data-stu-id="43f36-163">**IOCTL\_BATTERY\_QUERY\_STATUS**</span></span>](ioctl-battery-query-status.md)
</dt> <dt>

[<span data-ttu-id="43f36-164">**\_тег запроса на батарею ioctl \_ \_**</span><span class="sxs-lookup"><span data-stu-id="43f36-164">**IOCTL\_BATTERY\_QUERY\_TAG**</span></span>](ioctl-battery-query-tag.md)
</dt> </dl>

 

