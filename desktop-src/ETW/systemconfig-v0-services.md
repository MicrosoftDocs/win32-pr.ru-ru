---
description: SystemConfig_V0_Services класс. Этот класс является классом типа событий для событий конфигурации службы.
ms.assetid: 1e6c2061-f1a2-4253-a0c4-4b45b2feceda
title: Класс SystemConfig_V0_Services
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SystemConfig_V0_Services
- SystemConfig_V0_Services.ServiceName
- SystemConfig_V0_Services.DisplayName
- SystemConfig_V0_Services.ProcessName
- SystemConfig_V0_Services.ProcessId
api_type:
- NA
api_location: ''
ms.openlocfilehash: b69ca7cf4ee4e16a5fbcb6a5f10c659f713ab458
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108105932"
---
# <a name="systemconfig_v0_services-class"></a><span data-ttu-id="30ba4-103">\_Класс системконфиг v0 \_ Services</span><span class="sxs-lookup"><span data-stu-id="30ba4-103">SystemConfig\_V0\_Services class</span></span>

<span data-ttu-id="30ba4-104">Этот класс является классом типа событий для событий конфигурации службы.</span><span class="sxs-lookup"><span data-stu-id="30ba4-104">This class is the event type class for service configuration events.</span></span>

<span data-ttu-id="30ba4-105">Следующий синтаксис упрощен из MOF-кода.</span><span class="sxs-lookup"><span data-stu-id="30ba4-105">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="30ba4-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="30ba4-106">Syntax</span></span>

``` syntax
[EventType(15), EventTypeName("Services")]
class SystemConfig_V0_Services : SystemConfig_V0
{
  char16 ServiceName[];
  char16 DisplayName[];
  char16 ProcessName[];
  uint32 ProcessId;
};
```

## <a name="members"></a><span data-ttu-id="30ba4-107">Члены</span><span class="sxs-lookup"><span data-stu-id="30ba4-107">Members</span></span>

<span data-ttu-id="30ba4-108">Класс **системконфиг \_ v0 \_ Services** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="30ba4-108">The **SystemConfig\_V0\_Services** class has these types of members:</span></span>

-   [<span data-ttu-id="30ba4-109">Свойства</span><span class="sxs-lookup"><span data-stu-id="30ba4-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="30ba4-110">Элемент Property</span><span class="sxs-lookup"><span data-stu-id="30ba4-110">Properties</span></span>

<span data-ttu-id="30ba4-111">Класс **системконфиг \_ v0 \_ Services** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="30ba4-111">The **SystemConfig\_V0\_Services** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="30ba4-112">**Отображаемое имя**</span><span class="sxs-lookup"><span data-stu-id="30ba4-112">**DisplayName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="30ba4-113">Тип данных: массив **Char16**</span><span class="sxs-lookup"><span data-stu-id="30ba4-113">Data type: **char16** array</span></span>
</dt> <dt>

<span data-ttu-id="30ba4-114">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="30ba4-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="30ba4-115">Квалификаторы: **вмидатаид** (2), **Max** (256)</span><span class="sxs-lookup"><span data-stu-id="30ba4-115">Qualifiers: **WmiDataId** (2), **Max** (256)</span></span>
</dt> </dl>

<span data-ttu-id="30ba4-116">Отображаемое имя службы.</span><span class="sxs-lookup"><span data-stu-id="30ba4-116">Display name of the service.</span></span> <span data-ttu-id="30ba4-117">В диспетчере управления службами имя сохраняется с учетом регистра.</span><span class="sxs-lookup"><span data-stu-id="30ba4-117">The name is case-preserved in the Service Control Manager.</span></span> <span data-ttu-id="30ba4-118">Но сравнения отображаемых имен всегда выполняются без учета регистра.</span><span class="sxs-lookup"><span data-stu-id="30ba4-118">However, display name comparisons are always case-insensitive.</span></span>

</dd> <dt>

<span data-ttu-id="30ba4-119">**Идентификатор**</span><span class="sxs-lookup"><span data-stu-id="30ba4-119">**ProcessId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="30ba4-120">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="30ba4-120">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="30ba4-121">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="30ba4-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="30ba4-122">Квалификаторы: **вмидатаид** (4)</span><span class="sxs-lookup"><span data-stu-id="30ba4-122">Qualifiers: **WmiDataId** (4)</span></span>
</dt> </dl>

<span data-ttu-id="30ba4-123">Идентификатор процесса, в котором выполняется служба.</span><span class="sxs-lookup"><span data-stu-id="30ba4-123">Identifier of the process in which the service runs.</span></span>

</dd> <dt>

<span data-ttu-id="30ba4-124">**ProcessName**</span><span class="sxs-lookup"><span data-stu-id="30ba4-124">**ProcessName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="30ba4-125">Тип данных: массив **Char16**</span><span class="sxs-lookup"><span data-stu-id="30ba4-125">Data type: **char16** array</span></span>
</dt> <dt>

<span data-ttu-id="30ba4-126">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="30ba4-126">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="30ba4-127">Квалификаторы: **вмидатаид** (3), **Max** (34)</span><span class="sxs-lookup"><span data-stu-id="30ba4-127">Qualifiers: **WmiDataId** (3), **Max** (34)</span></span>
</dt> </dl>

<span data-ttu-id="30ba4-128">Имя процесса, в котором выполняется служба.</span><span class="sxs-lookup"><span data-stu-id="30ba4-128">Name of the process in which the service runs.</span></span>

</dd> <dt>

<span data-ttu-id="30ba4-129">**Служба**</span><span class="sxs-lookup"><span data-stu-id="30ba4-129">**ServiceName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="30ba4-130">Тип данных: массив **Char16**</span><span class="sxs-lookup"><span data-stu-id="30ba4-130">Data type: **char16** array</span></span>
</dt> <dt>

<span data-ttu-id="30ba4-131">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="30ba4-131">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="30ba4-132">Квалификаторы: **вмидатаид** (1), **Max** (34)</span><span class="sxs-lookup"><span data-stu-id="30ba4-132">Qualifiers: **WmiDataId** (1), **Max** (34)</span></span>
</dt> </dl>

<span data-ttu-id="30ba4-133">Уникальный идентификатор службы.</span><span class="sxs-lookup"><span data-stu-id="30ba4-133">Unique identifier of the service.</span></span> <span data-ttu-id="30ba4-134">Идентификатор предоставляет сведения о функциональных возможностях, предоставляемых службой.</span><span class="sxs-lookup"><span data-stu-id="30ba4-134">The identifier provides an indication of the functionality the service provides.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="30ba4-135">Требования</span><span class="sxs-lookup"><span data-stu-id="30ba4-135">Requirements</span></span>



| <span data-ttu-id="30ba4-136">Требование</span><span class="sxs-lookup"><span data-stu-id="30ba4-136">Requirement</span></span> | <span data-ttu-id="30ba4-137">Значение</span><span class="sxs-lookup"><span data-stu-id="30ba4-137">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="30ba4-138">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="30ba4-138">Minimum supported client</span></span><br/> | <span data-ttu-id="30ba4-139">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="30ba4-139">None supported</span></span><br/>                            |
| <span data-ttu-id="30ba4-140">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="30ba4-140">Minimum supported server</span></span><br/> | <span data-ttu-id="30ba4-141">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="30ba4-141">Windows Server 2003 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="30ba4-142">См. также</span><span class="sxs-lookup"><span data-stu-id="30ba4-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="30ba4-143">**Системконфиг \_ v0**</span><span class="sxs-lookup"><span data-stu-id="30ba4-143">**SystemConfig\_V0**</span></span>](systemconfig-v0.md)
</dt> </dl>

 

 




