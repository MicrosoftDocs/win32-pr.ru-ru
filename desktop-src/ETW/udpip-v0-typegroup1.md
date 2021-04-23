---
description: Этот класс является классом типа событий для событий UDP/IP. Следующий синтаксис упрощен из MOF-кода.
ms.assetid: 834a761a-089b-4b93-9a6a-a1edf752b582
title: Класс UdpIp_V0_TypeGroup1
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- UdpIp_V0_TypeGroup1
- UdpIp_V0_TypeGroup1.context
- UdpIp_V0_TypeGroup1.saddr
- UdpIp_V0_TypeGroup1.sport
- UdpIp_V0_TypeGroup1.size
- UdpIp_V0_TypeGroup1.daddr
- UdpIp_V0_TypeGroup1.dport
- UdpIp_V0_TypeGroup1.dsize
api_type:
- NA
api_location: ''
ms.openlocfilehash: 2813476bc2c820d1872e787dc047fafccd3b7d52
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103999119"
---
# <a name="udpip_v0_typegroup1-class"></a><span data-ttu-id="8e85f-104">\_Класс удпип v0 \_ TypeGroup1</span><span class="sxs-lookup"><span data-stu-id="8e85f-104">UdpIp\_V0\_TypeGroup1 class</span></span>

<span data-ttu-id="8e85f-105">Этот класс является классом типа событий для событий UDP/IP.</span><span class="sxs-lookup"><span data-stu-id="8e85f-105">This class is the event type class for UDP/IP events.</span></span>

<span data-ttu-id="8e85f-106">Следующий синтаксис упрощен из MOF-кода.</span><span class="sxs-lookup"><span data-stu-id="8e85f-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="8e85f-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="8e85f-107">Syntax</span></span>

``` syntax
[EventType{10, 11}, EventTypeName{"Send", "Recv"}]
class UdpIp_V0_TypeGroup1 : UdpIp_V0
{
  uint32 context;
  object saddr;
  object sport;
  uint16 size;
  object daddr;
  object dport;
  uint16 dsize;
};
```

## <a name="members"></a><span data-ttu-id="8e85f-108">Участники</span><span class="sxs-lookup"><span data-stu-id="8e85f-108">Members</span></span>

<span data-ttu-id="8e85f-109">Класс **удпип \_ v0 \_ TypeGroup1** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="8e85f-109">The **UdpIp\_V0\_TypeGroup1** class has these types of members:</span></span>

-   [<span data-ttu-id="8e85f-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="8e85f-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="8e85f-111">Свойства</span><span class="sxs-lookup"><span data-stu-id="8e85f-111">Properties</span></span>

<span data-ttu-id="8e85f-112">Класс **удпип \_ v0 \_ TypeGroup1** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="8e85f-112">The **UdpIp\_V0\_TypeGroup1** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="8e85f-113">контекст</span><span class="sxs-lookup"><span data-stu-id="8e85f-113">context</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8e85f-114">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="8e85f-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="8e85f-115">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="8e85f-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8e85f-116">Квалификаторы: Вмидатаид (1), Pointer</span><span class="sxs-lookup"><span data-stu-id="8e85f-116">Qualifiers: WmiDataId(1), pointer</span></span>
</dt> </dl>

<span data-ttu-id="8e85f-117">Идентификатор процесса для объекта Address, который сделал или получил запрос.</span><span class="sxs-lookup"><span data-stu-id="8e85f-117">Process identifier for the Address Object that made or received the request.</span></span>

</dd> <dt>

<span data-ttu-id="8e85f-118">даддр</span><span class="sxs-lookup"><span data-stu-id="8e85f-118">daddr</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8e85f-119">Тип данных: **объект**</span><span class="sxs-lookup"><span data-stu-id="8e85f-119">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="8e85f-120">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="8e85f-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8e85f-121">Квалификаторы: Вмидатаид (5), Extension ("reduce")</span><span class="sxs-lookup"><span data-stu-id="8e85f-121">Qualifiers: WmiDataId(5), Extension("IPAddr")</span></span>
</dt> </dl>

<span data-ttu-id="8e85f-122">Конечный IP-адрес.</span><span class="sxs-lookup"><span data-stu-id="8e85f-122">Destination IP address.</span></span>

</dd> <dt>

<span data-ttu-id="8e85f-123">дпорт</span><span class="sxs-lookup"><span data-stu-id="8e85f-123">dport</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8e85f-124">Тип данных: **объект**</span><span class="sxs-lookup"><span data-stu-id="8e85f-124">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="8e85f-125">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="8e85f-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8e85f-126">Квалификаторы: Вмидатаид (6), Extension ("порт")</span><span class="sxs-lookup"><span data-stu-id="8e85f-126">Qualifiers: WmiDataId(6), Extension("Port")</span></span>
</dt> </dl>

<span data-ttu-id="8e85f-127">Номер порта назначения.</span><span class="sxs-lookup"><span data-stu-id="8e85f-127">Destination port number.</span></span>

</dd> <dt>

<span data-ttu-id="8e85f-128">дсизе</span><span class="sxs-lookup"><span data-stu-id="8e85f-128">dsize</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8e85f-129">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="8e85f-129">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="8e85f-130">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="8e85f-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8e85f-131">Квалификаторы: Вмидатаид (7)</span><span class="sxs-lookup"><span data-stu-id="8e85f-131">Qualifiers: WmiDataId(7)</span></span>
</dt> </dl>

<span data-ttu-id="8e85f-132">Размер пакета назначения.</span><span class="sxs-lookup"><span data-stu-id="8e85f-132">Size of the destination packet.</span></span>

</dd> <dt>

<span data-ttu-id="8e85f-133">саддр</span><span class="sxs-lookup"><span data-stu-id="8e85f-133">saddr</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8e85f-134">Тип данных: **объект**</span><span class="sxs-lookup"><span data-stu-id="8e85f-134">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="8e85f-135">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="8e85f-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8e85f-136">Квалификаторы: Вмидатаид (2), Extension ("reduce")</span><span class="sxs-lookup"><span data-stu-id="8e85f-136">Qualifiers: WmiDataId(2), Extension("IPAddr")</span></span>
</dt> </dl>

<span data-ttu-id="8e85f-137">Исходный IP-адрес.</span><span class="sxs-lookup"><span data-stu-id="8e85f-137">Source IP address.</span></span>

</dd> <dt>

<span data-ttu-id="8e85f-138">size</span><span class="sxs-lookup"><span data-stu-id="8e85f-138">size</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8e85f-139">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="8e85f-139">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="8e85f-140">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="8e85f-140">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8e85f-141">Квалификаторы: Вмидатаид (4)</span><span class="sxs-lookup"><span data-stu-id="8e85f-141">Qualifiers: WmiDataId(4)</span></span>
</dt> </dl>

<span data-ttu-id="8e85f-142">Размер исходного пакета.</span><span class="sxs-lookup"><span data-stu-id="8e85f-142">Size of the source packet.</span></span>

</dd> <dt>

<span data-ttu-id="8e85f-143">назван</span><span class="sxs-lookup"><span data-stu-id="8e85f-143">sport</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8e85f-144">Тип данных: **объект**</span><span class="sxs-lookup"><span data-stu-id="8e85f-144">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="8e85f-145">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="8e85f-145">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8e85f-146">Квалификаторы: Вмидатаид (3), расширение ("порт")</span><span class="sxs-lookup"><span data-stu-id="8e85f-146">Qualifiers: WmiDataId(3), Extension("Port")</span></span>
</dt> </dl>

<span data-ttu-id="8e85f-147">Номер исходного порта.</span><span class="sxs-lookup"><span data-stu-id="8e85f-147">Source port number.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="8e85f-148">Требования</span><span class="sxs-lookup"><span data-stu-id="8e85f-148">Requirements</span></span>



| <span data-ttu-id="8e85f-149">Требование</span><span class="sxs-lookup"><span data-stu-id="8e85f-149">Requirement</span></span> | <span data-ttu-id="8e85f-150">Значение</span><span class="sxs-lookup"><span data-stu-id="8e85f-150">Value</span></span> |
|-------------------------------------|---------------------------------------------|
| <span data-ttu-id="8e85f-151">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="8e85f-151">Minimum supported client</span></span><br/> | <span data-ttu-id="8e85f-152">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="8e85f-152">Windows XP \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="8e85f-153">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="8e85f-153">Minimum supported server</span></span><br/> | <span data-ttu-id="8e85f-154">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="8e85f-154">None supported</span></span><br/>                   |



## <a name="see-also"></a><span data-ttu-id="8e85f-155">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="8e85f-155">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8e85f-156">**Удпип \_ v0**</span><span class="sxs-lookup"><span data-stu-id="8e85f-156">**UdpIp\_V0**</span></span>](udpip-v0.md)
</dt> </dl>

 

 




