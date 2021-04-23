---
description: Класс Хвконфиг является родительским классом для событий конфигурации оборудования в Windows XP. Следующий синтаксис упрощен из MOF-кода.
ms.assetid: 47f062c0-fdf0-4beb-906d-257571324de9
title: Класс Хвконфиг
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- HWConfig
api_type:
- NA
api_location: ''
ms.openlocfilehash: cfb194e09701dbc52b00279b624877f09ffac24b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103913536"
---
# <a name="hwconfig-class"></a><span data-ttu-id="10436-104">Класс Хвконфиг</span><span class="sxs-lookup"><span data-stu-id="10436-104">HWConfig class</span></span>

<span data-ttu-id="10436-105">Класс **хвконфиг** является родительским классом для событий конфигурации оборудования в Windows XP.</span><span class="sxs-lookup"><span data-stu-id="10436-105">The **HWConfig** class is the parent class for hardware configuration events on Windows XP.</span></span>

<span data-ttu-id="10436-106">Следующий синтаксис упрощен из MOF-кода.</span><span class="sxs-lookup"><span data-stu-id="10436-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="10436-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="10436-107">Syntax</span></span>

``` syntax
[Guid("{01853a65-418f-4f36-aefc-dc0f1d2fd235}")]
class HWConfig : MSNT_SystemTrace
{
};
```

## <a name="members"></a><span data-ttu-id="10436-108">Участники</span><span class="sxs-lookup"><span data-stu-id="10436-108">Members</span></span>

<span data-ttu-id="10436-109">Класс **хвконфиг** не определяет никаких членов.</span><span class="sxs-lookup"><span data-stu-id="10436-109">The **HWConfig** class does not define any members.</span></span>

## <a name="remarks"></a><span data-ttu-id="10436-110">Примечания</span><span class="sxs-lookup"><span data-stu-id="10436-110">Remarks</span></span>

<span data-ttu-id="10436-111">Эти события обеспечивают конфигурацию оборудования компьютера.</span><span class="sxs-lookup"><span data-stu-id="10436-111">These events provide the hardware configuration of the computer.</span></span> <span data-ttu-id="10436-112">В отличие от других событий средства ведения журнала ядра NT, сеанс ядра автоматически создает события конфигурации оборудования. Эти события не будут включены при запуске сеанса ведения журнала ядра NT.</span><span class="sxs-lookup"><span data-stu-id="10436-112">Unlike other NT Kernel Logger events, the kernel session automatically generates hardware configuration events; you do not enable these events when starting the NT Kernel Logger session.</span></span>

<span data-ttu-id="10436-113">**Windows 2000:** Не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="10436-113">**Windows 2000:** Not supported.</span></span>

<span data-ttu-id="10436-114">Сведения о событиях конфигурации оборудования в Windows Vista и Windows Server 2003 см. в разделе класс [системконфиг](systemconfig.md) .</span><span class="sxs-lookup"><span data-stu-id="10436-114">For hardware configuration events on Windows Vista and Windows Server 2003, see the [SystemConfig](systemconfig.md) class.</span></span>

<span data-ttu-id="10436-115">Потребители трассировки событий могут реализовать специальную обработку событий конфигурации оборудования, вызвав функцию [**сеттрацекаллбакк**](/windows/win32/api/evntrace/nf-evntrace-settracecallback) и указав [**евенттрацеконфиггуид**](nt-kernel-logger-constants.md) в качестве параметра *пгуид* .</span><span class="sxs-lookup"><span data-stu-id="10436-115">Event trace consumers can implement special processing for hardware configuration events by calling the [**SetTraceCallback**](/windows/win32/api/evntrace/nf-evntrace-settracecallback) function and specifying [**EventTraceConfigGuid**](nt-kernel-logger-constants.md) as the *pGuid* parameter.</span></span> <span data-ttu-id="10436-116">Используйте следующие типы событий для обнаружения фактического события конфигурации оборудования при использовании событий.</span><span class="sxs-lookup"><span data-stu-id="10436-116">Use the following event types to identify the actual hardware configuration event when consuming events.</span></span>



| <span data-ttu-id="10436-117">Тип события</span><span class="sxs-lookup"><span data-stu-id="10436-117">Event type</span></span>                                                                      | <span data-ttu-id="10436-118">Описание</span><span class="sxs-lookup"><span data-stu-id="10436-118">Description</span></span>                                                                                                                                      |
|---------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="10436-119">**Событие \_ \_ \_ \_ ЦП конфигурации типа трассировки**(значение типа события — 10)</span><span class="sxs-lookup"><span data-stu-id="10436-119">**EVENT\_TRACE\_TYPE\_CONFIG\_CPU**(Event type value is 10)</span></span><br/>          | <span data-ttu-id="10436-120">Событие настройки ЦП.</span><span class="sxs-lookup"><span data-stu-id="10436-120">CPU configuration event.</span></span> <span data-ttu-id="10436-121">Классы [**хвконфиг \_ ЦП**](hwconfig-cpu.md) (MOF) определяют данные события для этого события.</span><span class="sxs-lookup"><span data-stu-id="10436-121">The [**HWConfig\_CPU**](hwconfig-cpu.md) MOF classes defines the event data for this event.</span></span>                            |
| <span data-ttu-id="10436-122">**Событие \_ \_Конфигурация типа \_ трассировки \_ LOGICALDISK**(значение типа события — 12)</span><span class="sxs-lookup"><span data-stu-id="10436-122">**EVENT\_TRACE\_TYPE\_CONFIG\_LOGICALDISK**(Event type value is 12)</span></span><br/>  | <span data-ttu-id="10436-123">Событие настройки логического диска.</span><span class="sxs-lookup"><span data-stu-id="10436-123">Logical disk configuration event.</span></span> <span data-ttu-id="10436-124">Класс MOF classes [**хвконфиг \_ логдиск**](hwconfig-logdisk.md) определяет данные события для этого события.</span><span class="sxs-lookup"><span data-stu-id="10436-124">The [**HWConfig\_LogDisk**](hwconfig-logdisk.md) MOF classes MOF class defines the event data for this event.</span></span> |
| <span data-ttu-id="10436-125">**Событие \_ \_ \_ \_ Сетевая карта конфигурации типа трассировки**(значение типа события 13)</span><span class="sxs-lookup"><span data-stu-id="10436-125">**EVENT\_TRACE\_TYPE\_CONFIG\_NIC**(Event type value is 13)</span></span><br/>          | <span data-ttu-id="10436-126">Событие настройки сетевого адаптера.</span><span class="sxs-lookup"><span data-stu-id="10436-126">NIC configuration event.</span></span> <span data-ttu-id="10436-127">Классы [**хвконфиг \_ NIC**](hwconfig-nic.md) MOF определяют данные события для этого события.</span><span class="sxs-lookup"><span data-stu-id="10436-127">The [**HWConfig\_NIC**](hwconfig-nic.md) MOF classes defines the event data for this event.</span></span>                            |
| <span data-ttu-id="10436-128">**Событие \_ \_Тип трассировки \_ Конфигурация \_ физический диск**(значение типа события — 11)</span><span class="sxs-lookup"><span data-stu-id="10436-128">**EVENT\_TRACE\_TYPE\_CONFIG\_PHYSICALDISK**(Event type value is 11)</span></span><br/> | <span data-ttu-id="10436-129">Событие конфигурации физического диска.</span><span class="sxs-lookup"><span data-stu-id="10436-129">Physical disk configuration event.</span></span> <span data-ttu-id="10436-130">Классы [**хвконфиг \_ фидиск**](hwconfig-phydisk.md) MOF определяют данные события для этого события.</span><span class="sxs-lookup"><span data-stu-id="10436-130">The [**HWConfig\_PhyDisk**](hwconfig-phydisk.md) MOF classes defines the event data for this event.</span></span>          |



 

## <a name="requirements"></a><span data-ttu-id="10436-131">Требования</span><span class="sxs-lookup"><span data-stu-id="10436-131">Requirements</span></span>



| <span data-ttu-id="10436-132">Требование</span><span class="sxs-lookup"><span data-stu-id="10436-132">Requirement</span></span> | <span data-ttu-id="10436-133">Значение</span><span class="sxs-lookup"><span data-stu-id="10436-133">Value</span></span> |
|-------------------------------------|---------------------------------------------|
| <span data-ttu-id="10436-134">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="10436-134">Minimum supported client</span></span><br/> | <span data-ttu-id="10436-135">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="10436-135">Windows XP \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="10436-136">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="10436-136">Minimum supported server</span></span><br/> | <span data-ttu-id="10436-137">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="10436-137">None supported</span></span><br/>                   |



## <a name="see-also"></a><span data-ttu-id="10436-138">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="10436-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="10436-139">**МСНТ \_ системтраце**</span><span class="sxs-lookup"><span data-stu-id="10436-139">**MSNT\_SystemTrace**</span></span>](msnt-systemtrace.md)
</dt> <dt>

[<span data-ttu-id="10436-140">**\_ЦП хвконфиг**</span><span class="sxs-lookup"><span data-stu-id="10436-140">**HWConfig\_CPU**</span></span>](hwconfig-cpu.md)
</dt> <dt>

[<span data-ttu-id="10436-141">**Хвконфиг \_ логдиск**</span><span class="sxs-lookup"><span data-stu-id="10436-141">**HWConfig\_LogDisk**</span></span>](hwconfig-logdisk.md)
</dt> <dt>

[<span data-ttu-id="10436-142">**\_Сетевой адаптер хвконфиг**</span><span class="sxs-lookup"><span data-stu-id="10436-142">**HWConfig\_NIC**</span></span>](hwconfig-nic.md)
</dt> <dt>

[<span data-ttu-id="10436-143">**Хвконфиг \_ фидиск**</span><span class="sxs-lookup"><span data-stu-id="10436-143">**HWConfig\_PhyDisk**</span></span>](hwconfig-phydisk.md)
</dt> </dl>

 

 
