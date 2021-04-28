---
description: UdpIp_V0_TypeGroup1 класс — этот класс является классом типа события для событий UDP/IP. Следующий синтаксис упрощен из MOF-кода.
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
ms.openlocfilehash: 78243a49e4504fd9e132407feebe98d9b48f7bdd
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108105502"
---
# <a name="udpip_v0_typegroup1-class"></a><span data-ttu-id="7577c-104">\_Класс удпип v0 \_ TypeGroup1</span><span class="sxs-lookup"><span data-stu-id="7577c-104">UdpIp\_V0\_TypeGroup1 class</span></span>

<span data-ttu-id="7577c-105">Этот класс является классом типа событий для событий UDP/IP.</span><span class="sxs-lookup"><span data-stu-id="7577c-105">This class is the event type class for UDP/IP events.</span></span>

<span data-ttu-id="7577c-106">Следующий синтаксис упрощен из MOF-кода.</span><span class="sxs-lookup"><span data-stu-id="7577c-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="7577c-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="7577c-107">Syntax</span></span>

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

## <a name="members"></a><span data-ttu-id="7577c-108">Члены</span><span class="sxs-lookup"><span data-stu-id="7577c-108">Members</span></span>

<span data-ttu-id="7577c-109">Класс **удпип \_ v0 \_ TypeGroup1** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="7577c-109">The **UdpIp\_V0\_TypeGroup1** class has these types of members:</span></span>

-   [<span data-ttu-id="7577c-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="7577c-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="7577c-111">Элемент Property</span><span class="sxs-lookup"><span data-stu-id="7577c-111">Properties</span></span>

<span data-ttu-id="7577c-112">Класс **удпип \_ v0 \_ TypeGroup1** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="7577c-112">The **UdpIp\_V0\_TypeGroup1** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="7577c-113">контекст</span><span class="sxs-lookup"><span data-stu-id="7577c-113">context</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7577c-114">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="7577c-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="7577c-115">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="7577c-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7577c-116">Квалификаторы: Вмидатаид (1), Pointer</span><span class="sxs-lookup"><span data-stu-id="7577c-116">Qualifiers: WmiDataId(1), pointer</span></span>
</dt> </dl>

<span data-ttu-id="7577c-117">Идентификатор процесса для объекта Address, который сделал или получил запрос.</span><span class="sxs-lookup"><span data-stu-id="7577c-117">Process identifier for the Address Object that made or received the request.</span></span>

</dd> <dt>

<span data-ttu-id="7577c-118">даддр</span><span class="sxs-lookup"><span data-stu-id="7577c-118">daddr</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7577c-119">Тип данных: **объект**</span><span class="sxs-lookup"><span data-stu-id="7577c-119">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="7577c-120">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="7577c-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7577c-121">Квалификаторы: Вмидатаид (5), Extension ("reduce")</span><span class="sxs-lookup"><span data-stu-id="7577c-121">Qualifiers: WmiDataId(5), Extension("IPAddr")</span></span>
</dt> </dl>

<span data-ttu-id="7577c-122">Конечный IP-адрес.</span><span class="sxs-lookup"><span data-stu-id="7577c-122">Destination IP address.</span></span>

</dd> <dt>

<span data-ttu-id="7577c-123">дпорт</span><span class="sxs-lookup"><span data-stu-id="7577c-123">dport</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7577c-124">Тип данных: **объект**</span><span class="sxs-lookup"><span data-stu-id="7577c-124">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="7577c-125">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="7577c-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7577c-126">Квалификаторы: Вмидатаид (6), Extension ("порт")</span><span class="sxs-lookup"><span data-stu-id="7577c-126">Qualifiers: WmiDataId(6), Extension("Port")</span></span>
</dt> </dl>

<span data-ttu-id="7577c-127">Номер порта назначения.</span><span class="sxs-lookup"><span data-stu-id="7577c-127">Destination port number.</span></span>

</dd> <dt>

<span data-ttu-id="7577c-128">дсизе</span><span class="sxs-lookup"><span data-stu-id="7577c-128">dsize</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7577c-129">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="7577c-129">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="7577c-130">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="7577c-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7577c-131">Квалификаторы: Вмидатаид (7)</span><span class="sxs-lookup"><span data-stu-id="7577c-131">Qualifiers: WmiDataId(7)</span></span>
</dt> </dl>

<span data-ttu-id="7577c-132">Размер пакета назначения.</span><span class="sxs-lookup"><span data-stu-id="7577c-132">Size of the destination packet.</span></span>

</dd> <dt>

<span data-ttu-id="7577c-133">саддр</span><span class="sxs-lookup"><span data-stu-id="7577c-133">saddr</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7577c-134">Тип данных: **объект**</span><span class="sxs-lookup"><span data-stu-id="7577c-134">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="7577c-135">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="7577c-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7577c-136">Квалификаторы: Вмидатаид (2), Extension ("reduce")</span><span class="sxs-lookup"><span data-stu-id="7577c-136">Qualifiers: WmiDataId(2), Extension("IPAddr")</span></span>
</dt> </dl>

<span data-ttu-id="7577c-137">Исходный IP-адрес.</span><span class="sxs-lookup"><span data-stu-id="7577c-137">Source IP address.</span></span>

</dd> <dt>

<span data-ttu-id="7577c-138">размер;</span><span class="sxs-lookup"><span data-stu-id="7577c-138">size</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7577c-139">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="7577c-139">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="7577c-140">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="7577c-140">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7577c-141">Квалификаторы: Вмидатаид (4)</span><span class="sxs-lookup"><span data-stu-id="7577c-141">Qualifiers: WmiDataId(4)</span></span>
</dt> </dl>

<span data-ttu-id="7577c-142">Размер исходного пакета.</span><span class="sxs-lookup"><span data-stu-id="7577c-142">Size of the source packet.</span></span>

</dd> <dt>

<span data-ttu-id="7577c-143">назван</span><span class="sxs-lookup"><span data-stu-id="7577c-143">sport</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7577c-144">Тип данных: **объект**</span><span class="sxs-lookup"><span data-stu-id="7577c-144">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="7577c-145">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="7577c-145">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7577c-146">Квалификаторы: Вмидатаид (3), расширение ("порт")</span><span class="sxs-lookup"><span data-stu-id="7577c-146">Qualifiers: WmiDataId(3), Extension("Port")</span></span>
</dt> </dl>

<span data-ttu-id="7577c-147">Номер исходного порта.</span><span class="sxs-lookup"><span data-stu-id="7577c-147">Source port number.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="7577c-148">Требования</span><span class="sxs-lookup"><span data-stu-id="7577c-148">Requirements</span></span>



| <span data-ttu-id="7577c-149">Требование</span><span class="sxs-lookup"><span data-stu-id="7577c-149">Requirement</span></span> | <span data-ttu-id="7577c-150">Значение</span><span class="sxs-lookup"><span data-stu-id="7577c-150">Value</span></span> |
|-------------------------------------|---------------------------------------------|
| <span data-ttu-id="7577c-151">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="7577c-151">Minimum supported client</span></span><br/> | <span data-ttu-id="7577c-152">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="7577c-152">Windows XP \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="7577c-153">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="7577c-153">Minimum supported server</span></span><br/> | <span data-ttu-id="7577c-154">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="7577c-154">None supported</span></span><br/>                   |



## <a name="see-also"></a><span data-ttu-id="7577c-155">См. также</span><span class="sxs-lookup"><span data-stu-id="7577c-155">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7577c-156">**Удпип \_ v0**</span><span class="sxs-lookup"><span data-stu-id="7577c-156">**UdpIp\_V0**</span></span>](udpip-v0.md)
</dt> </dl>

 

 




