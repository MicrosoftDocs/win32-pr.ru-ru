---
description: Этот класс является классом типа события для событий PnP. Следующий синтаксис упрощен из MOF-кода.
ms.assetid: 01e9a8bb-3f54-4e20-b4db-1b4bba745d4f
title: Класс SystemConfig_PnP
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SystemConfig_PnP
- SystemConfig_PnP.IDLength
- SystemConfig_PnP.DescriptionLength
- SystemConfig_PnP.FriendlyNameLength
- SystemConfig_PnP.DeviceID
- SystemConfig_PnP.DeviceDescription
- SystemConfig_PnP.FriendlyName
api_type:
- NA
api_location: ''
ms.openlocfilehash: 2bd4cdbbec5c61f453a0ef6fae3fef0bd494edac
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104497253"
---
# <a name="systemconfig_pnp-class"></a><span data-ttu-id="5ab3a-104">\_Класс системконфиг PnP</span><span class="sxs-lookup"><span data-stu-id="5ab3a-104">SystemConfig\_PnP class</span></span>

<span data-ttu-id="5ab3a-105">Этот класс является классом типа события для событий PnP.</span><span class="sxs-lookup"><span data-stu-id="5ab3a-105">This class is the event type class for PnP events.</span></span>

<span data-ttu-id="5ab3a-106">Следующий синтаксис упрощен из MOF-кода.</span><span class="sxs-lookup"><span data-stu-id="5ab3a-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="5ab3a-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="5ab3a-107">Syntax</span></span>

``` syntax
[EventType(22), EventTypeName("PnP")]
class SystemConfig_PnP : SystemConfig
{
  uint32 IDLength;
  uint32 DescriptionLength;
  uint32 FriendlyNameLength;
  string DeviceID;
  string DeviceDescription;
  string FriendlyName;
};
```

## <a name="members"></a><span data-ttu-id="5ab3a-108">Участники</span><span class="sxs-lookup"><span data-stu-id="5ab3a-108">Members</span></span>

<span data-ttu-id="5ab3a-109">Класс **системконфиг \_ PnP** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="5ab3a-109">The **SystemConfig\_PnP** class has these types of members:</span></span>

-   [<span data-ttu-id="5ab3a-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="5ab3a-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="5ab3a-111">Свойства</span><span class="sxs-lookup"><span data-stu-id="5ab3a-111">Properties</span></span>

<span data-ttu-id="5ab3a-112">Класс **системконфиг \_ PnP** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="5ab3a-112">The **SystemConfig\_PnP** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="5ab3a-113">**дескриптионленгс**</span><span class="sxs-lookup"><span data-stu-id="5ab3a-113">**DescriptionLength**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5ab3a-114">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="5ab3a-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="5ab3a-115">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="5ab3a-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5ab3a-116">Квалификаторы: Вмидатаид (2)</span><span class="sxs-lookup"><span data-stu-id="5ab3a-116">Qualifiers: WmiDataId(2)</span></span>
</dt> </dl>

<span data-ttu-id="5ab3a-117">Длина строки DeviceDescription в символах.</span><span class="sxs-lookup"><span data-stu-id="5ab3a-117">Length, in characters, of the DeviceDescription string.</span></span>

</dd> <dt>

<span data-ttu-id="5ab3a-118">**DeviceDescription**</span><span class="sxs-lookup"><span data-stu-id="5ab3a-118">**DeviceDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5ab3a-119">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="5ab3a-119">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5ab3a-120">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="5ab3a-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5ab3a-121">Квалификаторы: Вмидатаид (5), Стрингтерминатион ("NullTerminated"), Format ("w")</span><span class="sxs-lookup"><span data-stu-id="5ab3a-121">Qualifiers: WmiDataId(5), StringTermination("NullTerminated"), Format("w")</span></span>
</dt> </dl>

<span data-ttu-id="5ab3a-122">Описание устройства PnP.</span><span class="sxs-lookup"><span data-stu-id="5ab3a-122">Description of the PnP device.</span></span>

</dd> <dt>

<span data-ttu-id="5ab3a-123">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="5ab3a-123">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5ab3a-124">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="5ab3a-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5ab3a-125">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="5ab3a-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5ab3a-126">Квалификаторы: Вмидатаид (4), Стрингтерминатион ("NullTerminated"), Format ("w")</span><span class="sxs-lookup"><span data-stu-id="5ab3a-126">Qualifiers: WmiDataId(4), StringTermination("NullTerminated"), Format("w")</span></span>
</dt> </dl>

<span data-ttu-id="5ab3a-127">Определяет устройство PnP.</span><span class="sxs-lookup"><span data-stu-id="5ab3a-127">Identifies the PnP device.</span></span>

</dd> <dt>

<span data-ttu-id="5ab3a-128">**FriendlyName**</span><span class="sxs-lookup"><span data-stu-id="5ab3a-128">**FriendlyName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5ab3a-129">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="5ab3a-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5ab3a-130">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="5ab3a-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5ab3a-131">Квалификаторы: Вмидатаид (6), Стрингтерминатион ("NullTerminated"), Format ("w")</span><span class="sxs-lookup"><span data-stu-id="5ab3a-131">Qualifiers: WmiDataId(6), StringTermination("NullTerminated"), Format("w")</span></span>
</dt> </dl>

<span data-ttu-id="5ab3a-132">Имя устройства PnP, которое будет использоваться в пользовательском интерфейсе.</span><span class="sxs-lookup"><span data-stu-id="5ab3a-132">Name of the PnP device to use in a user interface.</span></span>

</dd> <dt>

<span data-ttu-id="5ab3a-133">**фриендлинамеленгс**</span><span class="sxs-lookup"><span data-stu-id="5ab3a-133">**FriendlyNameLength**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5ab3a-134">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="5ab3a-134">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="5ab3a-135">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="5ab3a-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5ab3a-136">Квалификаторы: Вмидатаид (3)</span><span class="sxs-lookup"><span data-stu-id="5ab3a-136">Qualifiers: WmiDataId(3)</span></span>
</dt> </dl>

<span data-ttu-id="5ab3a-137">Длина строки FriendlyName в символах.</span><span class="sxs-lookup"><span data-stu-id="5ab3a-137">Length, in characters, of the FriendlyName string.</span></span>

</dd> <dt>

<span data-ttu-id="5ab3a-138">**идленгс**</span><span class="sxs-lookup"><span data-stu-id="5ab3a-138">**IDLength**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5ab3a-139">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="5ab3a-139">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="5ab3a-140">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="5ab3a-140">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5ab3a-141">Квалификаторы: Вмидатаид (1)</span><span class="sxs-lookup"><span data-stu-id="5ab3a-141">Qualifiers: WmiDataId(1)</span></span>
</dt> </dl>

<span data-ttu-id="5ab3a-142">Длина строки DeviceID в символах.</span><span class="sxs-lookup"><span data-stu-id="5ab3a-142">Length, in characters, of the DeviceID string.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="5ab3a-143">Требования</span><span class="sxs-lookup"><span data-stu-id="5ab3a-143">Requirements</span></span>



| <span data-ttu-id="5ab3a-144">Требование</span><span class="sxs-lookup"><span data-stu-id="5ab3a-144">Requirement</span></span> | <span data-ttu-id="5ab3a-145">Значение</span><span class="sxs-lookup"><span data-stu-id="5ab3a-145">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="5ab3a-146">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="5ab3a-146">Minimum supported client</span></span><br/> | <span data-ttu-id="5ab3a-147">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="5ab3a-147">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="5ab3a-148">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="5ab3a-148">Minimum supported server</span></span><br/> | <span data-ttu-id="5ab3a-149">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="5ab3a-149">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="5ab3a-150">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="5ab3a-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5ab3a-151">**системконфиг**</span><span class="sxs-lookup"><span data-stu-id="5ab3a-151">**SystemConfig**</span></span>](systemconfig.md)
</dt> </dl>

 

 




