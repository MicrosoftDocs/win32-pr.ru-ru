---
description: Этот класс является классом типа событий для событий конфигурации службы.
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
ms.openlocfilehash: 6c061c6a0c4cbb3e807bcb3418155b1194fcfa28
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104349322"
---
# <a name="systemconfig_v0_services-class"></a><span data-ttu-id="d5bf1-103">\_Класс системконфиг v0 \_ Services</span><span class="sxs-lookup"><span data-stu-id="d5bf1-103">SystemConfig\_V0\_Services class</span></span>

<span data-ttu-id="d5bf1-104">Этот класс является классом типа событий для событий конфигурации службы.</span><span class="sxs-lookup"><span data-stu-id="d5bf1-104">This class is the event type class for service configuration events.</span></span>

<span data-ttu-id="d5bf1-105">Следующий синтаксис упрощен из MOF-кода.</span><span class="sxs-lookup"><span data-stu-id="d5bf1-105">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="d5bf1-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d5bf1-106">Syntax</span></span>

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

## <a name="members"></a><span data-ttu-id="d5bf1-107">Участники</span><span class="sxs-lookup"><span data-stu-id="d5bf1-107">Members</span></span>

<span data-ttu-id="d5bf1-108">Класс **системконфиг \_ v0 \_ Services** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="d5bf1-108">The **SystemConfig\_V0\_Services** class has these types of members:</span></span>

-   [<span data-ttu-id="d5bf1-109">Свойства</span><span class="sxs-lookup"><span data-stu-id="d5bf1-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="d5bf1-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="d5bf1-110">Properties</span></span>

<span data-ttu-id="d5bf1-111">Класс **системконфиг \_ v0 \_ Services** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="d5bf1-111">The **SystemConfig\_V0\_Services** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="d5bf1-112">**Отображаемое имя**</span><span class="sxs-lookup"><span data-stu-id="d5bf1-112">**DisplayName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d5bf1-113">Тип данных: массив **Char16**</span><span class="sxs-lookup"><span data-stu-id="d5bf1-113">Data type: **char16** array</span></span>
</dt> <dt>

<span data-ttu-id="d5bf1-114">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d5bf1-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d5bf1-115">Квалификаторы: **вмидатаид** (2), **Max** (256)</span><span class="sxs-lookup"><span data-stu-id="d5bf1-115">Qualifiers: **WmiDataId** (2), **Max** (256)</span></span>
</dt> </dl>

<span data-ttu-id="d5bf1-116">Отображаемое имя службы.</span><span class="sxs-lookup"><span data-stu-id="d5bf1-116">Display name of the service.</span></span> <span data-ttu-id="d5bf1-117">В диспетчере управления службами имя сохраняется с учетом регистра.</span><span class="sxs-lookup"><span data-stu-id="d5bf1-117">The name is case-preserved in the Service Control Manager.</span></span> <span data-ttu-id="d5bf1-118">Но сравнения отображаемых имен всегда выполняются без учета регистра.</span><span class="sxs-lookup"><span data-stu-id="d5bf1-118">However, display name comparisons are always case-insensitive.</span></span>

</dd> <dt>

<span data-ttu-id="d5bf1-119">**Идентификатор**</span><span class="sxs-lookup"><span data-stu-id="d5bf1-119">**ProcessId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d5bf1-120">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="d5bf1-120">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="d5bf1-121">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d5bf1-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d5bf1-122">Квалификаторы: **вмидатаид** (4)</span><span class="sxs-lookup"><span data-stu-id="d5bf1-122">Qualifiers: **WmiDataId** (4)</span></span>
</dt> </dl>

<span data-ttu-id="d5bf1-123">Идентификатор процесса, в котором выполняется служба.</span><span class="sxs-lookup"><span data-stu-id="d5bf1-123">Identifier of the process in which the service runs.</span></span>

</dd> <dt>

<span data-ttu-id="d5bf1-124">**ProcessName**</span><span class="sxs-lookup"><span data-stu-id="d5bf1-124">**ProcessName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d5bf1-125">Тип данных: массив **Char16**</span><span class="sxs-lookup"><span data-stu-id="d5bf1-125">Data type: **char16** array</span></span>
</dt> <dt>

<span data-ttu-id="d5bf1-126">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d5bf1-126">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d5bf1-127">Квалификаторы: **вмидатаид** (3), **Max** (34)</span><span class="sxs-lookup"><span data-stu-id="d5bf1-127">Qualifiers: **WmiDataId** (3), **Max** (34)</span></span>
</dt> </dl>

<span data-ttu-id="d5bf1-128">Имя процесса, в котором выполняется служба.</span><span class="sxs-lookup"><span data-stu-id="d5bf1-128">Name of the process in which the service runs.</span></span>

</dd> <dt>

<span data-ttu-id="d5bf1-129">**Служба**</span><span class="sxs-lookup"><span data-stu-id="d5bf1-129">**ServiceName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d5bf1-130">Тип данных: массив **Char16**</span><span class="sxs-lookup"><span data-stu-id="d5bf1-130">Data type: **char16** array</span></span>
</dt> <dt>

<span data-ttu-id="d5bf1-131">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d5bf1-131">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d5bf1-132">Квалификаторы: **вмидатаид** (1), **Max** (34)</span><span class="sxs-lookup"><span data-stu-id="d5bf1-132">Qualifiers: **WmiDataId** (1), **Max** (34)</span></span>
</dt> </dl>

<span data-ttu-id="d5bf1-133">Уникальный идентификатор службы.</span><span class="sxs-lookup"><span data-stu-id="d5bf1-133">Unique identifier of the service.</span></span> <span data-ttu-id="d5bf1-134">Идентификатор предоставляет сведения о функциональных возможностях, предоставляемых службой.</span><span class="sxs-lookup"><span data-stu-id="d5bf1-134">The identifier provides an indication of the functionality the service provides.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="d5bf1-135">Требования</span><span class="sxs-lookup"><span data-stu-id="d5bf1-135">Requirements</span></span>



| <span data-ttu-id="d5bf1-136">Требование</span><span class="sxs-lookup"><span data-stu-id="d5bf1-136">Requirement</span></span> | <span data-ttu-id="d5bf1-137">Значение</span><span class="sxs-lookup"><span data-stu-id="d5bf1-137">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="d5bf1-138">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="d5bf1-138">Minimum supported client</span></span><br/> | <span data-ttu-id="d5bf1-139">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="d5bf1-139">None supported</span></span><br/>                            |
| <span data-ttu-id="d5bf1-140">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="d5bf1-140">Minimum supported server</span></span><br/> | <span data-ttu-id="d5bf1-141">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="d5bf1-141">Windows Server 2003 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="d5bf1-142">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d5bf1-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d5bf1-143">**Системконфиг \_ v0**</span><span class="sxs-lookup"><span data-stu-id="d5bf1-143">**SystemConfig\_V0**</span></span>](systemconfig-v0.md)
</dt> </dl>

 

 




