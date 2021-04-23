---
description: Этот класс является классом типа событий для событий конфигурации службы.
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
ms.openlocfilehash: 97b4d2a56f2ed739403681875e0be4d9e21481ec
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104984396"
---
# <a name="systemconfig_services-class"></a><span data-ttu-id="5df17-103">\_Класс системконфиг Services</span><span class="sxs-lookup"><span data-stu-id="5df17-103">SystemConfig\_Services class</span></span>

<span data-ttu-id="5df17-104">Этот класс является классом типа событий для событий конфигурации службы.</span><span class="sxs-lookup"><span data-stu-id="5df17-104">This class is the event type class for service configuration events.</span></span>

<span data-ttu-id="5df17-105">Следующий синтаксис упрощен из MOF-кода.</span><span class="sxs-lookup"><span data-stu-id="5df17-105">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="5df17-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="5df17-106">Syntax</span></span>

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

## <a name="members"></a><span data-ttu-id="5df17-107">Участники</span><span class="sxs-lookup"><span data-stu-id="5df17-107">Members</span></span>

<span data-ttu-id="5df17-108">Класс **системконфиг \_ Services** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="5df17-108">The **SystemConfig\_Services** class has these types of members:</span></span>

-   [<span data-ttu-id="5df17-109">Свойства</span><span class="sxs-lookup"><span data-stu-id="5df17-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="5df17-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="5df17-110">Properties</span></span>

<span data-ttu-id="5df17-111">Класс **системконфиг \_ Services** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="5df17-111">The **SystemConfig\_Services** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="5df17-112">**Отображаемое имя**</span><span class="sxs-lookup"><span data-stu-id="5df17-112">**DisplayName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5df17-113">Тип данных: массив **строк**</span><span class="sxs-lookup"><span data-stu-id="5df17-113">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="5df17-114">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="5df17-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5df17-115">Квалификаторы: **вмидатаид** (5), **Стрингтерминатион ("NullTerminated")**, **Format ("w")**</span><span class="sxs-lookup"><span data-stu-id="5df17-115">Qualifiers: **WmiDataId** (5), **StringTermination("NullTerminated")**, **Format("w")**</span></span>
</dt> </dl>

<span data-ttu-id="5df17-116">Отображаемое имя службы.</span><span class="sxs-lookup"><span data-stu-id="5df17-116">Display name of the service.</span></span> <span data-ttu-id="5df17-117">В диспетчере управления службами имя сохраняется с учетом регистра.</span><span class="sxs-lookup"><span data-stu-id="5df17-117">The name is case-preserved in the Service Control Manager.</span></span> <span data-ttu-id="5df17-118">Но сравнения отображаемых имен всегда выполняются без учета регистра.</span><span class="sxs-lookup"><span data-stu-id="5df17-118">However, display name comparisons are always case-insensitive.</span></span>

</dd> <dt>

<span data-ttu-id="5df17-119">**Идентификатор**</span><span class="sxs-lookup"><span data-stu-id="5df17-119">**ProcessId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5df17-120">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="5df17-120">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="5df17-121">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="5df17-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5df17-122">Квалификаторы: **вмидатаид** (1), **Format ("x")**</span><span class="sxs-lookup"><span data-stu-id="5df17-122">Qualifiers: **WmiDataId** (1), **Format("x")**</span></span>
</dt> </dl>

<span data-ttu-id="5df17-123">Идентификатор процесса, в котором выполняется служба.</span><span class="sxs-lookup"><span data-stu-id="5df17-123">Identifier of the process in which the service runs.</span></span>

</dd> <dt>

<span data-ttu-id="5df17-124">**ProcessName**</span><span class="sxs-lookup"><span data-stu-id="5df17-124">**ProcessName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5df17-125">Тип данных: массив **строк**</span><span class="sxs-lookup"><span data-stu-id="5df17-125">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="5df17-126">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="5df17-126">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5df17-127">Квалификаторы: **вмидатаид** (6), **Стрингтерминатион ("NullTerminated")**, **Format ("w")**</span><span class="sxs-lookup"><span data-stu-id="5df17-127">Qualifiers: **WmiDataId** (6), **StringTermination("NullTerminated")**, **Format("w")**</span></span>
</dt> </dl>

<span data-ttu-id="5df17-128">Имя процесса, в котором выполняется служба.</span><span class="sxs-lookup"><span data-stu-id="5df17-128">Name of the process in which the service runs.</span></span>

</dd> <dt>

<span data-ttu-id="5df17-129">**Служба**</span><span class="sxs-lookup"><span data-stu-id="5df17-129">**ServiceName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5df17-130">Тип данных: массив **строк**</span><span class="sxs-lookup"><span data-stu-id="5df17-130">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="5df17-131">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="5df17-131">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5df17-132">Квалификаторы: **вмидатаид** (4), **Стрингтерминатион ("NullTerminated")**, **Format ("w")**</span><span class="sxs-lookup"><span data-stu-id="5df17-132">Qualifiers: **WmiDataId** (4), **StringTermination("NullTerminated")**, **Format("w")**</span></span>
</dt> </dl>

<span data-ttu-id="5df17-133">Уникальный идентификатор службы.</span><span class="sxs-lookup"><span data-stu-id="5df17-133">Unique identifier of the service.</span></span> <span data-ttu-id="5df17-134">Идентификатор предоставляет сведения о функциональных возможностях, предоставляемых службой.</span><span class="sxs-lookup"><span data-stu-id="5df17-134">The identifier provides an indication of the functionality the service provides.</span></span>

</dd> <dt>

<span data-ttu-id="5df17-135">**ServiceState**</span><span class="sxs-lookup"><span data-stu-id="5df17-135">**ServiceState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5df17-136">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="5df17-136">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="5df17-137">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="5df17-137">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5df17-138">Квалификаторы: **вмидатаид** (2), **Format ("x")**</span><span class="sxs-lookup"><span data-stu-id="5df17-138">Qualifiers: **WmiDataId** (2), **Format("x")**</span></span>
</dt> </dl>

<span data-ttu-id="5df17-139">Текущее состояние службы.</span><span class="sxs-lookup"><span data-stu-id="5df17-139">Current state of the service.</span></span> <span data-ttu-id="5df17-140">Возможные значения см. в разделе **двкуррентстатеing** of **Service \_ Status \_ Process**.</span><span class="sxs-lookup"><span data-stu-id="5df17-140">For possible values, see the **dwCurrentState** member of **SERVICE\_STATUS\_PROCESS**.</span></span>

</dd> <dt>

<span data-ttu-id="5df17-141">**субпроцесстаг**</span><span class="sxs-lookup"><span data-stu-id="5df17-141">**SubProcessTag**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5df17-142">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="5df17-142">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="5df17-143">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="5df17-143">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5df17-144">Квалификаторы: **вмидатаид** (3), **Format ("x")**</span><span class="sxs-lookup"><span data-stu-id="5df17-144">Qualifiers: **WmiDataId** (3), **Format("x")**</span></span>
</dt> </dl>

<span data-ttu-id="5df17-145">Идентифицирует службу.</span><span class="sxs-lookup"><span data-stu-id="5df17-145">Identifies the service.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="5df17-146">Требования</span><span class="sxs-lookup"><span data-stu-id="5df17-146">Requirements</span></span>



| <span data-ttu-id="5df17-147">Требование</span><span class="sxs-lookup"><span data-stu-id="5df17-147">Requirement</span></span> | <span data-ttu-id="5df17-148">Значение</span><span class="sxs-lookup"><span data-stu-id="5df17-148">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="5df17-149">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="5df17-149">Minimum supported client</span></span><br/> | <span data-ttu-id="5df17-150">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="5df17-150">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="5df17-151">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="5df17-151">Minimum supported server</span></span><br/> | <span data-ttu-id="5df17-152">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="5df17-152">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="5df17-153">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="5df17-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5df17-154">**системконфиг**</span><span class="sxs-lookup"><span data-stu-id="5df17-154">**SystemConfig**</span></span>](systemconfig.md)
</dt> </dl>

 

 




