---
description: Класс Системконфиг — этот класс является родительским классом для событий конфигурации оборудования. Следующий синтаксис упрощен из MOF-кода.
ms.assetid: 720c2366-bd68-4895-bfaf-74aa9b64ba4a
title: Класс Системконфиг
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SystemConfig
api_type:
- NA
api_location: ''
ms.openlocfilehash: 232214aa2c33485d909525d54965f59fdc891a29
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108105872"
---
# <a name="systemconfig-class"></a><span data-ttu-id="322e4-104">Класс Системконфиг</span><span class="sxs-lookup"><span data-stu-id="322e4-104">SystemConfig class</span></span>

<span data-ttu-id="322e4-105">Этот класс является родительским классом для событий конфигурации оборудования.</span><span class="sxs-lookup"><span data-stu-id="322e4-105">This class is the parent class for hardware configuration events.</span></span>

<span data-ttu-id="322e4-106">Следующий синтаксис упрощен из MOF-кода.</span><span class="sxs-lookup"><span data-stu-id="322e4-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="322e4-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="322e4-107">Syntax</span></span>

``` syntax
[Guid("{01853a65-418f-4f36-aefc-dc0f1d2fd235}"), EventVersion(2)]
class SystemConfig : MSNT_SystemTrace
{
};
```

## <a name="members"></a><span data-ttu-id="322e4-108">Члены</span><span class="sxs-lookup"><span data-stu-id="322e4-108">Members</span></span>

<span data-ttu-id="322e4-109">Класс **системконфиг** не определяет никаких членов.</span><span class="sxs-lookup"><span data-stu-id="322e4-109">The **SystemConfig** class does not define any members.</span></span>

## <a name="remarks"></a><span data-ttu-id="322e4-110">Remarks</span><span class="sxs-lookup"><span data-stu-id="322e4-110">Remarks</span></span>

<span data-ttu-id="322e4-111">Эти события обеспечивают конфигурацию оборудования компьютера.</span><span class="sxs-lookup"><span data-stu-id="322e4-111">These events provide the hardware configuration of the computer.</span></span> <span data-ttu-id="322e4-112">В отличие от других событий средства ведения журнала ядра NT, сеанс ядра автоматически создает события конфигурации оборудования. Эти события не будут включены при запуске сеанса ведения журнала ядра NT.</span><span class="sxs-lookup"><span data-stu-id="322e4-112">Unlike other NT Kernel Logger events, the kernel session automatically generates hardware configuration events; you do not enable these events when starting the NT Kernel Logger session.</span></span>

<span data-ttu-id="322e4-113">Сведения о событиях конфигурации оборудования в Windows XP см. в разделе класс [хвконфиг](hwconfig.md) .</span><span class="sxs-lookup"><span data-stu-id="322e4-113">For hardware configuration events on Windows XP, see the [HWConfig](hwconfig.md) class.</span></span>

<span data-ttu-id="322e4-114">Потребители трассировки событий могут реализовать специальную обработку событий конфигурации оборудования, вызвав функцию [**сеттрацекаллбакк**](/windows/win32/api/evntrace/nf-evntrace-settracecallback) и указав [**евенттрацеконфиггуид**](nt-kernel-logger-constants.md) в качестве параметра *пгуид* .</span><span class="sxs-lookup"><span data-stu-id="322e4-114">Event trace consumers can implement special processing for hardware configuration events by calling the [**SetTraceCallback**](/windows/win32/api/evntrace/nf-evntrace-settracecallback) function and specifying [**EventTraceConfigGuid**](nt-kernel-logger-constants.md) as the *pGuid* parameter.</span></span> <span data-ttu-id="322e4-115">Используйте следующие типы событий для обнаружения фактического события конфигурации оборудования при использовании событий.</span><span class="sxs-lookup"><span data-stu-id="322e4-115">Use the following event types to identify the actual hardware configuration event when consuming events.</span></span>



| <span data-ttu-id="322e4-116">Тип события</span><span class="sxs-lookup"><span data-stu-id="322e4-116">Event type</span></span>                                                                      | <span data-ttu-id="322e4-117">Описание</span><span class="sxs-lookup"><span data-stu-id="322e4-117">Description</span></span>                                                                                                                                                                         |
|---------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="322e4-118">**Событие \_ \_ \_ \_ ЦП конфигурации типа трассировки**(значение типа события — 10)</span><span class="sxs-lookup"><span data-stu-id="322e4-118">**EVENT\_TRACE\_TYPE\_CONFIG\_CPU**(Event type value is 10)</span></span><br/>          | <span data-ttu-id="322e4-119">Событие настройки ЦП.</span><span class="sxs-lookup"><span data-stu-id="322e4-119">CPU configuration event.</span></span> <span data-ttu-id="322e4-120">Классы [**системконфиг \_ ЦП**](systemconfig-cpu.md) (MOF) определяют данные события для этого события.</span><span class="sxs-lookup"><span data-stu-id="322e4-120">The [**SystemConfig\_CPU**](systemconfig-cpu.md) MOF classes defines the event data for this event.</span></span>                                                       |
| <span data-ttu-id="322e4-121">**Событие \_ \_ \_ \_ ИДЕЧАННЕЛ конфигурации типа трассировки**(значение типа события — 23)</span><span class="sxs-lookup"><span data-stu-id="322e4-121">**EVENT\_TRACE\_TYPE\_CONFIG\_IDECHANNEL**(Event type value is 23)</span></span><br/>   | <span data-ttu-id="322e4-122">Событие настройки основного и дополнительного каналов IDE.</span><span class="sxs-lookup"><span data-stu-id="322e4-122">Primary and secondary IDE channel configuration event.</span></span> <span data-ttu-id="322e4-123">Класс MOF classes [**системконфиг \_ идечаннел**](systemconfig-idechannel.md) определяет данные события для этого события.</span><span class="sxs-lookup"><span data-stu-id="322e4-123">The [**SystemConfig\_IDEChannel**](systemconfig-idechannel.md) MOF classes MOF class defines the event data for this event.</span></span> |
| <span data-ttu-id="322e4-124">**Событие \_ \_Конфигурация типа \_ трассировки \_ IRQ**(значение типа события — 21)</span><span class="sxs-lookup"><span data-stu-id="322e4-124">**EVENT\_TRACE\_TYPE\_CONFIG\_IRQ**(Event type value is 21)</span></span><br/>          | <span data-ttu-id="322e4-125">Событие запроса прерывания (IRQ).</span><span class="sxs-lookup"><span data-stu-id="322e4-125">Interrupt request (IRQ) event.</span></span> <span data-ttu-id="322e4-126">Класс MOF классов [**системконфиг \_ IRQ**](systemconfig-irq.md) MOF определяет данные события для этого события.</span><span class="sxs-lookup"><span data-stu-id="322e4-126">The [**SystemConfig\_IRQ**](systemconfig-irq.md) MOF classes MOF class defines the event data for this event.</span></span>                                       |
| <span data-ttu-id="322e4-127">**Событие \_ \_Конфигурация типа \_ трассировки \_ LOGICALDISK**(значение типа события — 12)</span><span class="sxs-lookup"><span data-stu-id="322e4-127">**EVENT\_TRACE\_TYPE\_CONFIG\_LOGICALDISK**(Event type value is 12)</span></span><br/>  | <span data-ttu-id="322e4-128">Событие настройки логического диска.</span><span class="sxs-lookup"><span data-stu-id="322e4-128">Logical disk configuration event.</span></span> <span data-ttu-id="322e4-129">Класс MOF classes [**системконфиг \_ логдиск**](systemconfig-logdisk.md) определяет данные события для этого события.</span><span class="sxs-lookup"><span data-stu-id="322e4-129">The [**SystemConfig\_LogDisk**](systemconfig-logdisk.md) MOF classes MOF class defines the event data for this event.</span></span>                            |
| <span data-ttu-id="322e4-130">**Событие \_ \_ \_ \_ НЕТИНФО конфигурации типа трассировки**(значение типа события — 17)</span><span class="sxs-lookup"><span data-stu-id="322e4-130">**EVENT\_TRACE\_TYPE\_CONFIG\_NETINFO**(Event type value is 17)</span></span><br/>      | <span data-ttu-id="322e4-131">Сетевое событие сведения.</span><span class="sxs-lookup"><span data-stu-id="322e4-131">Network iformation event.</span></span> <span data-ttu-id="322e4-132">Класс [**системконфиг \_ Network**](systemconfig-network.md) MOF определяет данные события для этого события.</span><span class="sxs-lookup"><span data-stu-id="322e4-132">The [**SystemConfig\_Network**](systemconfig-network.md) MOF class defines the event data for this event.</span></span>                                                |
| <span data-ttu-id="322e4-133">**Событие \_ \_ \_ \_ Сетевая карта конфигурации типа трассировки**(значение типа события 13)</span><span class="sxs-lookup"><span data-stu-id="322e4-133">**EVENT\_TRACE\_TYPE\_CONFIG\_NIC**(Event type value is 13)</span></span><br/>          | <span data-ttu-id="322e4-134">Событие настройки сетевого адаптера.</span><span class="sxs-lookup"><span data-stu-id="322e4-134">NIC configuration event.</span></span> <span data-ttu-id="322e4-135">Классы [**системконфиг \_ NIC**](systemconfig-nic.md) MOF определяют данные события для этого события.</span><span class="sxs-lookup"><span data-stu-id="322e4-135">The [**SystemConfig\_NIC**](systemconfig-nic.md) MOF classes defines the event data for this event.</span></span>                                                       |
| <span data-ttu-id="322e4-136">**Событие \_ \_Тип трассировки \_ Конфигурация \_ физический диск**(значение типа события — 11)</span><span class="sxs-lookup"><span data-stu-id="322e4-136">**EVENT\_TRACE\_TYPE\_CONFIG\_PHYSICALDISK**(Event type value is 11)</span></span><br/> | <span data-ttu-id="322e4-137">Событие конфигурации физического диска.</span><span class="sxs-lookup"><span data-stu-id="322e4-137">Physical disk configuration event.</span></span> <span data-ttu-id="322e4-138">Классы [**системконфиг \_ фидиск**](systemconfig-phydisk.md) MOF определяют данные события для этого события.</span><span class="sxs-lookup"><span data-stu-id="322e4-138">The [**SystemConfig\_PhyDisk**](systemconfig-phydisk.md) MOF classes defines the event data for this event.</span></span>                                     |
| <span data-ttu-id="322e4-139">**Событие \_ \_Конфигурация типа \_ трассировки \_ PnP**(значение типа события — 22)</span><span class="sxs-lookup"><span data-stu-id="322e4-139">**EVENT\_TRACE\_TYPE\_CONFIG\_PNP**(Event type value is 22)</span></span><br/>          | <span data-ttu-id="322e4-140">Событие Plug and Play.</span><span class="sxs-lookup"><span data-stu-id="322e4-140">Plug and play event.</span></span> <span data-ttu-id="322e4-141">Класс MOF классов [**системконфиг \_ PnP**](systemconfig-pnp.md) определяет данные события для этого события.</span><span class="sxs-lookup"><span data-stu-id="322e4-141">The [**SystemConfig\_PNP**](systemconfig-pnp.md) MOF classes MOF class defines the event data for this event.</span></span>                                                 |
| <span data-ttu-id="322e4-142">**Событие \_ \_ \_ \_ Степень конфигурации типа трассировки**(значение типа события — 16)</span><span class="sxs-lookup"><span data-stu-id="322e4-142">**EVENT\_TRACE\_TYPE\_CONFIG\_POWER**(Event type value is 16)</span></span><br/>        | <span data-ttu-id="322e4-143">Событие настройки питания.</span><span class="sxs-lookup"><span data-stu-id="322e4-143">Power configuration event.</span></span> <span data-ttu-id="322e4-144">Класс [**системконфиг \_ Power**](systemconfig-power.md) MOF определяет данные события для этого события.</span><span class="sxs-lookup"><span data-stu-id="322e4-144">The [**SystemConfig\_Power**](systemconfig-power.md) MOF class defines the event data for this event.</span></span>                                                   |
| <span data-ttu-id="322e4-145">**Событие \_ \_ \_ \_ Службы конфигурации типа трассировки**(значение типа события — 15)</span><span class="sxs-lookup"><span data-stu-id="322e4-145">**EVENT\_TRACE\_TYPE\_CONFIG\_SERVICES**(Event type value is 15)</span></span><br/>     | <span data-ttu-id="322e4-146">Событие настройки служб.</span><span class="sxs-lookup"><span data-stu-id="322e4-146">Services configuration event.</span></span> <span data-ttu-id="322e4-147">Класс [**MOF \_ служб системконфиг Services**](systemconfig-services.md) определяет данные события для этого события.</span><span class="sxs-lookup"><span data-stu-id="322e4-147">The [**SystemConfig\_Services**](systemconfig-services.md) MOF class defines the event data for this event.</span></span>                                          |
| <span data-ttu-id="322e4-148">**Событие \_ \_ \_ \_ Видео конфигурации типа трассировки**(значение типа события — 14)</span><span class="sxs-lookup"><span data-stu-id="322e4-148">**EVENT\_TRACE\_TYPE\_CONFIG\_VIDEO**(Event type value is 14)</span></span><br/>        | <span data-ttu-id="322e4-149">Событие настройки графического адаптера.</span><span class="sxs-lookup"><span data-stu-id="322e4-149">Graphics adapter configuration event.</span></span> <span data-ttu-id="322e4-150">Класс [**системконфиг \_ Video**](systemconfig-video.md) MOF определяет данные события для этого события.</span><span class="sxs-lookup"><span data-stu-id="322e4-150">The [**SystemConfig\_Video**](systemconfig-video.md) MOF class defines the event data for this event.</span></span>                                        |



 

## <a name="requirements"></a><span data-ttu-id="322e4-151">Требования</span><span class="sxs-lookup"><span data-stu-id="322e4-151">Requirements</span></span>



| <span data-ttu-id="322e4-152">Требование</span><span class="sxs-lookup"><span data-stu-id="322e4-152">Requirement</span></span> | <span data-ttu-id="322e4-153">Значение</span><span class="sxs-lookup"><span data-stu-id="322e4-153">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="322e4-154">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="322e4-154">Minimum supported client</span></span><br/> | <span data-ttu-id="322e4-155">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="322e4-155">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="322e4-156">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="322e4-156">Minimum supported server</span></span><br/> | <span data-ttu-id="322e4-157">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="322e4-157">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="322e4-158">См. также</span><span class="sxs-lookup"><span data-stu-id="322e4-158">See also</span></span>

<dl> <dt>

[<span data-ttu-id="322e4-159">**МСНТ \_ системтраце**</span><span class="sxs-lookup"><span data-stu-id="322e4-159">**MSNT\_SystemTrace**</span></span>](msnt-systemtrace.md)
</dt> <dt>

[<span data-ttu-id="322e4-160">**\_ЦП системконфиг**</span><span class="sxs-lookup"><span data-stu-id="322e4-160">**SystemConfig\_CPU**</span></span>](systemconfig-cpu.md)
</dt> <dt>

[<span data-ttu-id="322e4-161">**Системконфиг \_ идечаннел**</span><span class="sxs-lookup"><span data-stu-id="322e4-161">**SystemConfig\_IDEChannel**</span></span>](systemconfig-idechannel.md)
</dt> <dt>

[<span data-ttu-id="322e4-162">**Системконфиг \_ IRQ**</span><span class="sxs-lookup"><span data-stu-id="322e4-162">**SystemConfig\_IRQ**</span></span>](systemconfig-irq.md)
</dt> <dt>

[<span data-ttu-id="322e4-163">**Системконфиг \_ логдиск**</span><span class="sxs-lookup"><span data-stu-id="322e4-163">**SystemConfig\_LogDisk**</span></span>](systemconfig-logdisk.md)
</dt> <dt>

[<span data-ttu-id="322e4-164">**Системконфиг \_ сеть**</span><span class="sxs-lookup"><span data-stu-id="322e4-164">**SystemConfig\_Network**</span></span>](systemconfig-network.md)
</dt> <dt>

[<span data-ttu-id="322e4-165">**\_Сетевой адаптер системконфиг**</span><span class="sxs-lookup"><span data-stu-id="322e4-165">**SystemConfig\_NIC**</span></span>](systemconfig-nic.md)
</dt> <dt>

[<span data-ttu-id="322e4-166">**Системконфиг \_ фидиск**</span><span class="sxs-lookup"><span data-stu-id="322e4-166">**SystemConfig\_PhyDisk**</span></span>](systemconfig-phydisk.md)
</dt> <dt>

[<span data-ttu-id="322e4-167">**Системконфиг \_ PnP**</span><span class="sxs-lookup"><span data-stu-id="322e4-167">**SystemConfig\_PNP**</span></span>](systemconfig-pnp.md)
</dt> <dt>

[<span data-ttu-id="322e4-168">**Системконфиг \_**</span><span class="sxs-lookup"><span data-stu-id="322e4-168">**SystemConfig\_Power**</span></span>](systemconfig-power.md)
</dt> <dt>

[<span data-ttu-id="322e4-169">**Системконфиг \_ Services**</span><span class="sxs-lookup"><span data-stu-id="322e4-169">**SystemConfig\_Services**</span></span>](systemconfig-services.md)
</dt> <dt>

[<span data-ttu-id="322e4-170">**\_Видео системконфиг**</span><span class="sxs-lookup"><span data-stu-id="322e4-170">**SystemConfig\_Video**</span></span>](systemconfig-video.md)
</dt> <dt>

[<span data-ttu-id="322e4-171">**Системконфиг \_ v0**</span><span class="sxs-lookup"><span data-stu-id="322e4-171">**SystemConfig\_V0**</span></span>](systemconfig-v0.md)
</dt> </dl>

 

 
