---
description: SystemConfig_Services класс. Этот класс является классом типа событий для событий конфигурации службы.
ms.assetid: 7cba9992-d154-44b8-87d8-b46a8438f607
title: Класс SystemConfig_Services
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SystemConfig_Services
- SystemConfig_Services.ProcessId
- SystemConfig_Services.ServiceState
- SystemConfig_Services.SubProcessTag
- SystemConfig_Services.ServiceName
- SystemConfig_Services.DisplayName
- SystemConfig_Services.ProcessName
api_type:
- NA
api_location: ''
ms.openlocfilehash: 754b0e10c3882911c6e91fc2590c11739c3f7531
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108106062"
---
# <a name="systemconfig_services-class"></a><span data-ttu-id="92130-103">\_Класс системконфиг Services</span><span class="sxs-lookup"><span data-stu-id="92130-103">SystemConfig\_Services class</span></span>

<span data-ttu-id="92130-104">Этот класс является классом типа событий для событий конфигурации службы.</span><span class="sxs-lookup"><span data-stu-id="92130-104">This class is the event type class for service configuration events.</span></span>

<span data-ttu-id="92130-105">Следующий синтаксис упрощен из MOF-кода.</span><span class="sxs-lookup"><span data-stu-id="92130-105">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="92130-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="92130-106">Syntax</span></span>

``` syntax
[EventType(15), EventTypeName("Services")]
class SystemConfig_Services : SystemConfig
{
  uint32 ProcessId;
  uint32 ServiceState;
  uint32 SubProcessTag;
  string ServiceName[];
  string DisplayName[];
  string ProcessName[];
};
```

## <a name="members"></a><span data-ttu-id="92130-107">Члены</span><span class="sxs-lookup"><span data-stu-id="92130-107">Members</span></span>

<span data-ttu-id="92130-108">Класс **системконфиг \_ Services** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="92130-108">The **SystemConfig\_Services** class has these types of members:</span></span>

-   [<span data-ttu-id="92130-109">Свойства</span><span class="sxs-lookup"><span data-stu-id="92130-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="92130-110">Элемент Property</span><span class="sxs-lookup"><span data-stu-id="92130-110">Properties</span></span>

<span data-ttu-id="92130-111">Класс **системконфиг \_ Services** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="92130-111">The **SystemConfig\_Services** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="92130-112">**Отображаемое имя**</span><span class="sxs-lookup"><span data-stu-id="92130-112">**DisplayName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="92130-113">Тип данных: массив **строк**</span><span class="sxs-lookup"><span data-stu-id="92130-113">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="92130-114">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="92130-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="92130-115">Квалификаторы: **вмидатаид** (5), **Стрингтерминатион ("NullTerminated")**, **Format ("w")**</span><span class="sxs-lookup"><span data-stu-id="92130-115">Qualifiers: **WmiDataId** (5), **StringTermination("NullTerminated")**, **Format("w")**</span></span>
</dt> </dl>

<span data-ttu-id="92130-116">Отображаемое имя службы.</span><span class="sxs-lookup"><span data-stu-id="92130-116">Display name of the service.</span></span> <span data-ttu-id="92130-117">В диспетчере управления службами имя сохраняется с учетом регистра.</span><span class="sxs-lookup"><span data-stu-id="92130-117">The name is case-preserved in the Service Control Manager.</span></span> <span data-ttu-id="92130-118">Но сравнения отображаемых имен всегда выполняются без учета регистра.</span><span class="sxs-lookup"><span data-stu-id="92130-118">However, display name comparisons are always case-insensitive.</span></span>

</dd> <dt>

<span data-ttu-id="92130-119">**Идентификатор**</span><span class="sxs-lookup"><span data-stu-id="92130-119">**ProcessId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="92130-120">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="92130-120">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="92130-121">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="92130-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="92130-122">Квалификаторы: **вмидатаид** (1), **Format ("x")**</span><span class="sxs-lookup"><span data-stu-id="92130-122">Qualifiers: **WmiDataId** (1), **Format("x")**</span></span>
</dt> </dl>

<span data-ttu-id="92130-123">Идентификатор процесса, в котором выполняется служба.</span><span class="sxs-lookup"><span data-stu-id="92130-123">Identifier of the process in which the service runs.</span></span>

</dd> <dt>

<span data-ttu-id="92130-124">**ProcessName**</span><span class="sxs-lookup"><span data-stu-id="92130-124">**ProcessName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="92130-125">Тип данных: массив **строк**</span><span class="sxs-lookup"><span data-stu-id="92130-125">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="92130-126">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="92130-126">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="92130-127">Квалификаторы: **вмидатаид** (6), **Стрингтерминатион ("NullTerminated")**, **Format ("w")**</span><span class="sxs-lookup"><span data-stu-id="92130-127">Qualifiers: **WmiDataId** (6), **StringTermination("NullTerminated")**, **Format("w")**</span></span>
</dt> </dl>

<span data-ttu-id="92130-128">Имя процесса, в котором выполняется служба.</span><span class="sxs-lookup"><span data-stu-id="92130-128">Name of the process in which the service runs.</span></span>

</dd> <dt>

<span data-ttu-id="92130-129">**Служба**</span><span class="sxs-lookup"><span data-stu-id="92130-129">**ServiceName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="92130-130">Тип данных: массив **строк**</span><span class="sxs-lookup"><span data-stu-id="92130-130">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="92130-131">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="92130-131">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="92130-132">Квалификаторы: **вмидатаид** (4), **Стрингтерминатион ("NullTerminated")**, **Format ("w")**</span><span class="sxs-lookup"><span data-stu-id="92130-132">Qualifiers: **WmiDataId** (4), **StringTermination("NullTerminated")**, **Format("w")**</span></span>
</dt> </dl>

<span data-ttu-id="92130-133">Уникальный идентификатор службы.</span><span class="sxs-lookup"><span data-stu-id="92130-133">Unique identifier of the service.</span></span> <span data-ttu-id="92130-134">Идентификатор предоставляет сведения о функциональных возможностях, предоставляемых службой.</span><span class="sxs-lookup"><span data-stu-id="92130-134">The identifier provides an indication of the functionality the service provides.</span></span>

</dd> <dt>

<span data-ttu-id="92130-135">**ServiceState**</span><span class="sxs-lookup"><span data-stu-id="92130-135">**ServiceState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="92130-136">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="92130-136">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="92130-137">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="92130-137">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="92130-138">Квалификаторы: **вмидатаид** (2), **Format ("x")**</span><span class="sxs-lookup"><span data-stu-id="92130-138">Qualifiers: **WmiDataId** (2), **Format("x")**</span></span>
</dt> </dl>

<span data-ttu-id="92130-139">Текущее состояние службы.</span><span class="sxs-lookup"><span data-stu-id="92130-139">Current state of the service.</span></span> <span data-ttu-id="92130-140">Возможные значения см. в разделе **двкуррентстатеing** of **Service \_ Status \_ Process**.</span><span class="sxs-lookup"><span data-stu-id="92130-140">For possible values, see the **dwCurrentState** member of **SERVICE\_STATUS\_PROCESS**.</span></span>

</dd> <dt>

<span data-ttu-id="92130-141">**субпроцесстаг**</span><span class="sxs-lookup"><span data-stu-id="92130-141">**SubProcessTag**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="92130-142">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="92130-142">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="92130-143">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="92130-143">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="92130-144">Квалификаторы: **вмидатаид** (3), **Format ("x")**</span><span class="sxs-lookup"><span data-stu-id="92130-144">Qualifiers: **WmiDataId** (3), **Format("x")**</span></span>
</dt> </dl>

<span data-ttu-id="92130-145">Идентифицирует службу.</span><span class="sxs-lookup"><span data-stu-id="92130-145">Identifies the service.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="92130-146">Требования</span><span class="sxs-lookup"><span data-stu-id="92130-146">Requirements</span></span>



| <span data-ttu-id="92130-147">Требование</span><span class="sxs-lookup"><span data-stu-id="92130-147">Requirement</span></span> | <span data-ttu-id="92130-148">Значение</span><span class="sxs-lookup"><span data-stu-id="92130-148">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="92130-149">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="92130-149">Minimum supported client</span></span><br/> | <span data-ttu-id="92130-150">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="92130-150">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="92130-151">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="92130-151">Minimum supported server</span></span><br/> | <span data-ttu-id="92130-152">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="92130-152">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="92130-153">См. также</span><span class="sxs-lookup"><span data-stu-id="92130-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="92130-154">**системконфиг**</span><span class="sxs-lookup"><span data-stu-id="92130-154">**SystemConfig**</span></span>](systemconfig.md)
</dt> </dl>

 

 




