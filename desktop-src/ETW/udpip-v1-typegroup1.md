---
description: Этот класс является классом типа событий для событий UDP/IP. Следующий синтаксис упрощен из MOF-кода.
ms.assetid: c0ef6679-3852-4992-9fc2-114620eae14e
title: Класс UdpIp_V1_TypeGroup1
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- UdpIp_V1_TypeGroup1
- UdpIp_V1_TypeGroup1.PID
- UdpIp_V1_TypeGroup1.size
- UdpIp_V1_TypeGroup1.daddr
- UdpIp_V1_TypeGroup1.saddr
- UdpIp_V1_TypeGroup1.dport
- UdpIp_V1_TypeGroup1.sport
api_type:
- NA
api_location: ''
ms.openlocfilehash: 58f7506aefa79c3bc9136d2e3e76d662f545a921
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104984213"
---
# <a name="udpip_v1_typegroup1-class"></a><span data-ttu-id="a7fd3-104">\_ \_ Класс TypeGroup1 удпип v1</span><span class="sxs-lookup"><span data-stu-id="a7fd3-104">UdpIp\_V1\_TypeGroup1 class</span></span>

<span data-ttu-id="a7fd3-105">Этот класс является классом типа событий для событий UDP/IP.</span><span class="sxs-lookup"><span data-stu-id="a7fd3-105">This class is the event type class for UDP/IP events.</span></span>

<span data-ttu-id="a7fd3-106">Следующий синтаксис упрощен из MOF-кода.</span><span class="sxs-lookup"><span data-stu-id="a7fd3-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="a7fd3-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a7fd3-107">Syntax</span></span>

``` syntax
[EventType{10, 11}, EventTypeName{"Send", "Recv"}]
class UdpIp_V1_TypeGroup1 : UdpIp_V1
{
  uint32 PID;
  uint32 size;
  object daddr;
  object saddr;
  object dport;
  object sport;
};
```

## <a name="members"></a><span data-ttu-id="a7fd3-108">Участники</span><span class="sxs-lookup"><span data-stu-id="a7fd3-108">Members</span></span>

<span data-ttu-id="a7fd3-109">Класс **удпип \_ v1 \_ TypeGroup1** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="a7fd3-109">The **UdpIp\_V1\_TypeGroup1** class has these types of members:</span></span>

-   [<span data-ttu-id="a7fd3-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="a7fd3-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="a7fd3-111">Свойства</span><span class="sxs-lookup"><span data-stu-id="a7fd3-111">Properties</span></span>

<span data-ttu-id="a7fd3-112">Класс **удпип \_ v1 \_ TypeGroup1** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="a7fd3-112">The **UdpIp\_V1\_TypeGroup1** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="a7fd3-113">даддр</span><span class="sxs-lookup"><span data-stu-id="a7fd3-113">daddr</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a7fd3-114">Тип данных: **объект**</span><span class="sxs-lookup"><span data-stu-id="a7fd3-114">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="a7fd3-115">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="a7fd3-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a7fd3-116">Квалификаторы: Вмидатаид (3), Extension ("reduce")</span><span class="sxs-lookup"><span data-stu-id="a7fd3-116">Qualifiers: WmiDataId(3), Extension("IPAddr")</span></span>
</dt> </dl>

<span data-ttu-id="a7fd3-117">Конечный IP-адрес.</span><span class="sxs-lookup"><span data-stu-id="a7fd3-117">Destination IP address.</span></span>

</dd> <dt>

<span data-ttu-id="a7fd3-118">дпорт</span><span class="sxs-lookup"><span data-stu-id="a7fd3-118">dport</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a7fd3-119">Тип данных: **объект**</span><span class="sxs-lookup"><span data-stu-id="a7fd3-119">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="a7fd3-120">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="a7fd3-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a7fd3-121">Квалификаторы: Вмидатаид (5), Extension ("порт")</span><span class="sxs-lookup"><span data-stu-id="a7fd3-121">Qualifiers: WmiDataId(5), Extension("Port")</span></span>
</dt> </dl>

<span data-ttu-id="a7fd3-122">Номер порта назначения.</span><span class="sxs-lookup"><span data-stu-id="a7fd3-122">Destination port number.</span></span>

</dd> <dt>

<span data-ttu-id="a7fd3-123">ИД процесса</span><span class="sxs-lookup"><span data-stu-id="a7fd3-123">PID</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a7fd3-124">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="a7fd3-124">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="a7fd3-125">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="a7fd3-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a7fd3-126">Квалификаторы: Вмидатаид (1)</span><span class="sxs-lookup"><span data-stu-id="a7fd3-126">Qualifiers: WmiDataId(1)</span></span>
</dt> </dl>

<span data-ttu-id="a7fd3-127">Идентификатор процесса, связанного с запросом.</span><span class="sxs-lookup"><span data-stu-id="a7fd3-127">Identifier of the process associated with the request.</span></span>

</dd> <dt>

<span data-ttu-id="a7fd3-128">саддр</span><span class="sxs-lookup"><span data-stu-id="a7fd3-128">saddr</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a7fd3-129">Тип данных: **объект**</span><span class="sxs-lookup"><span data-stu-id="a7fd3-129">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="a7fd3-130">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="a7fd3-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a7fd3-131">Квалификаторы: Вмидатаид (4), Extension ("reduce")</span><span class="sxs-lookup"><span data-stu-id="a7fd3-131">Qualifiers: WmiDataId(4), Extension("IPAddr")</span></span>
</dt> </dl>

<span data-ttu-id="a7fd3-132">Исходный IP-адрес.</span><span class="sxs-lookup"><span data-stu-id="a7fd3-132">Source IP address.</span></span>

</dd> <dt>

<span data-ttu-id="a7fd3-133">size</span><span class="sxs-lookup"><span data-stu-id="a7fd3-133">size</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a7fd3-134">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="a7fd3-134">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="a7fd3-135">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="a7fd3-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a7fd3-136">Квалификаторы: Вмидатаид (2)</span><span class="sxs-lookup"><span data-stu-id="a7fd3-136">Qualifiers: WmiDataId(2)</span></span>
</dt> </dl>

<span data-ttu-id="a7fd3-137">Размер пакета.</span><span class="sxs-lookup"><span data-stu-id="a7fd3-137">Size of the packet.</span></span>

</dd> <dt>

<span data-ttu-id="a7fd3-138">назван</span><span class="sxs-lookup"><span data-stu-id="a7fd3-138">sport</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a7fd3-139">Тип данных: **объект**</span><span class="sxs-lookup"><span data-stu-id="a7fd3-139">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="a7fd3-140">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="a7fd3-140">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a7fd3-141">Квалификаторы: Вмидатаид (6), Extension ("порт")</span><span class="sxs-lookup"><span data-stu-id="a7fd3-141">Qualifiers: WmiDataId(6), Extension("Port")</span></span>
</dt> </dl>

<span data-ttu-id="a7fd3-142">Номер исходного порта.</span><span class="sxs-lookup"><span data-stu-id="a7fd3-142">Source port number.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="a7fd3-143">Требования</span><span class="sxs-lookup"><span data-stu-id="a7fd3-143">Requirements</span></span>



| <span data-ttu-id="a7fd3-144">Требование</span><span class="sxs-lookup"><span data-stu-id="a7fd3-144">Requirement</span></span> | <span data-ttu-id="a7fd3-145">Значение</span><span class="sxs-lookup"><span data-stu-id="a7fd3-145">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="a7fd3-146">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="a7fd3-146">Minimum supported client</span></span><br/> | <span data-ttu-id="a7fd3-147">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="a7fd3-147">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="a7fd3-148">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="a7fd3-148">Minimum supported server</span></span><br/> | <span data-ttu-id="a7fd3-149">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="a7fd3-149">Windows Server 2003 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="a7fd3-150">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a7fd3-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a7fd3-151">**Удпип \_ v1**</span><span class="sxs-lookup"><span data-stu-id="a7fd3-151">**UdpIp\_V1**</span></span>](udpip-v1.md)
</dt> <dt>

[<span data-ttu-id="a7fd3-152">**удпип**</span><span class="sxs-lookup"><span data-stu-id="a7fd3-152">**UdpIp**</span></span>](udpip.md)
</dt> </dl>

 

 




