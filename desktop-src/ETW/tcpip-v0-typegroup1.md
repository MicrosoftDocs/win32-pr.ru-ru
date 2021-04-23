---
description: Этот класс является классом типа событий для событий TCP/IP. Следующий синтаксис упрощен из MOF-кода.
ms.assetid: 007f0744-8b74-4c57-85bc-f6bdb20bffa7
title: Класс TcpIp_V0_TypeGroup1
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- TcpIp_V0_TypeGroup1
- TcpIp_V0_TypeGroup1.daddr
- TcpIp_V0_TypeGroup1.saddr
- TcpIp_V0_TypeGroup1.dport
- TcpIp_V0_TypeGroup1.sport
- TcpIp_V0_TypeGroup1.size
- TcpIp_V0_TypeGroup1.PID
api_type:
- NA
api_location: ''
ms.openlocfilehash: c21025990fe3e21cd5322b651e543472fa8d48c5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104344552"
---
# <a name="tcpip_v0_typegroup1-class"></a><span data-ttu-id="22e86-104">\_Класс TcpIp v0 \_ TypeGroup1</span><span class="sxs-lookup"><span data-stu-id="22e86-104">TcpIp\_V0\_TypeGroup1 class</span></span>

<span data-ttu-id="22e86-105">Этот класс является классом типа событий для событий TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="22e86-105">This class is the event type class for TCP/IP events.</span></span>

<span data-ttu-id="22e86-106">Следующий синтаксис упрощен из MOF-кода.</span><span class="sxs-lookup"><span data-stu-id="22e86-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="22e86-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="22e86-107">Syntax</span></span>

``` syntax
[EventType{10, 11, 12, 13, 14, 15}, EventTypeName{"Send", "Recv", "Connect", "Disconnect", "Retransmit", "Accept"}]
class TcpIp_V0_TypeGroup1 : TcpIp_V0
{
  object daddr;
  object saddr;
  object dport;
  object sport;
  uint32 size;
  uint32 PID;
};
```

## <a name="members"></a><span data-ttu-id="22e86-108">Участники</span><span class="sxs-lookup"><span data-stu-id="22e86-108">Members</span></span>

<span data-ttu-id="22e86-109">Класс **TcpIp \_ v0 \_ TypeGroup1** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="22e86-109">The **TcpIp\_V0\_TypeGroup1** class has these types of members:</span></span>

-   [<span data-ttu-id="22e86-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="22e86-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="22e86-111">Свойства</span><span class="sxs-lookup"><span data-stu-id="22e86-111">Properties</span></span>

<span data-ttu-id="22e86-112">Класс **TcpIp \_ v0 \_ TypeGroup1** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="22e86-112">The **TcpIp\_V0\_TypeGroup1** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="22e86-113">даддр</span><span class="sxs-lookup"><span data-stu-id="22e86-113">daddr</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22e86-114">Тип данных: **объект**</span><span class="sxs-lookup"><span data-stu-id="22e86-114">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="22e86-115">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="22e86-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="22e86-116">Квалификаторы: Вмидатаид (1), Extension ("reduce")</span><span class="sxs-lookup"><span data-stu-id="22e86-116">Qualifiers: WmiDataId(1), Extension("IPAddr")</span></span>
</dt> </dl>

<span data-ttu-id="22e86-117">Конечный IP-адрес.</span><span class="sxs-lookup"><span data-stu-id="22e86-117">Destination IP address.</span></span>

</dd> <dt>

<span data-ttu-id="22e86-118">дпорт</span><span class="sxs-lookup"><span data-stu-id="22e86-118">dport</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22e86-119">Тип данных: **объект**</span><span class="sxs-lookup"><span data-stu-id="22e86-119">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="22e86-120">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="22e86-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="22e86-121">Квалификаторы: Вмидатаид (3), расширение ("порт")</span><span class="sxs-lookup"><span data-stu-id="22e86-121">Qualifiers: WmiDataId(3), Extension("Port")</span></span>
</dt> </dl>

<span data-ttu-id="22e86-122">Номер порта назначения.</span><span class="sxs-lookup"><span data-stu-id="22e86-122">Destination port number.</span></span>

</dd> <dt>

<span data-ttu-id="22e86-123">ИД процесса</span><span class="sxs-lookup"><span data-stu-id="22e86-123">PID</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22e86-124">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="22e86-124">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="22e86-125">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="22e86-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="22e86-126">Квалификаторы: Вмидатаид (6)</span><span class="sxs-lookup"><span data-stu-id="22e86-126">Qualifiers: WmiDataId(6)</span></span>
</dt> </dl>

<span data-ttu-id="22e86-127">Идентификатор процесса, связанного с запросом.</span><span class="sxs-lookup"><span data-stu-id="22e86-127">Identifier of the process associated with the request.</span></span>

</dd> <dt>

<span data-ttu-id="22e86-128">саддр</span><span class="sxs-lookup"><span data-stu-id="22e86-128">saddr</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22e86-129">Тип данных: **объект**</span><span class="sxs-lookup"><span data-stu-id="22e86-129">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="22e86-130">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="22e86-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="22e86-131">Квалификаторы: Вмидатаид (2), Extension ("reduce")</span><span class="sxs-lookup"><span data-stu-id="22e86-131">Qualifiers: WmiDataId(2), Extension("IPAddr")</span></span>
</dt> </dl>

<span data-ttu-id="22e86-132">Исходный IP-адрес.</span><span class="sxs-lookup"><span data-stu-id="22e86-132">Source IP address.</span></span>

</dd> <dt>

<span data-ttu-id="22e86-133">size</span><span class="sxs-lookup"><span data-stu-id="22e86-133">size</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22e86-134">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="22e86-134">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="22e86-135">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="22e86-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="22e86-136">Квалификаторы: Вмидатаид (5)</span><span class="sxs-lookup"><span data-stu-id="22e86-136">Qualifiers: WmiDataId(5)</span></span>
</dt> </dl>

<span data-ttu-id="22e86-137">Размер пакета.</span><span class="sxs-lookup"><span data-stu-id="22e86-137">Size of the packet.</span></span>

</dd> <dt>

<span data-ttu-id="22e86-138">назван</span><span class="sxs-lookup"><span data-stu-id="22e86-138">sport</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22e86-139">Тип данных: **объект**</span><span class="sxs-lookup"><span data-stu-id="22e86-139">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="22e86-140">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="22e86-140">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="22e86-141">Квалификаторы: Вмидатаид (4), расширение ("порт")</span><span class="sxs-lookup"><span data-stu-id="22e86-141">Qualifiers: WmiDataId(4), Extension("Port")</span></span>
</dt> </dl>

<span data-ttu-id="22e86-142">Номер исходного порта.</span><span class="sxs-lookup"><span data-stu-id="22e86-142">Source port number.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="22e86-143">Требования</span><span class="sxs-lookup"><span data-stu-id="22e86-143">Requirements</span></span>



| <span data-ttu-id="22e86-144">Требование</span><span class="sxs-lookup"><span data-stu-id="22e86-144">Requirement</span></span> | <span data-ttu-id="22e86-145">Значение</span><span class="sxs-lookup"><span data-stu-id="22e86-145">Value</span></span> |
|-------------------------------------|---------------------------------------------|
| <span data-ttu-id="22e86-146">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="22e86-146">Minimum supported client</span></span><br/> | <span data-ttu-id="22e86-147">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="22e86-147">Windows XP \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="22e86-148">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="22e86-148">Minimum supported server</span></span><br/> | <span data-ttu-id="22e86-149">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="22e86-149">None supported</span></span><br/>                   |



## <a name="see-also"></a><span data-ttu-id="22e86-150">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="22e86-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="22e86-151">**TCP/IP \_ v0**</span><span class="sxs-lookup"><span data-stu-id="22e86-151">**TcpIp\_V0**</span></span>](tcpip-v0.md)
</dt> </dl>

 

 




