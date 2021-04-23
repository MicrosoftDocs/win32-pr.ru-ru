---
description: Этот класс является классом типа событий для событий TCP/IP. Следующий синтаксис упрощен из MOF-кода.
ms.assetid: 1cde7e37-52da-4108-90ce-7647a5653f65
title: Класс TcpIp_V1_TypeGroup1
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- TcpIp_V1_TypeGroup1
- TcpIp_V1_TypeGroup1.PID
- TcpIp_V1_TypeGroup1.size
- TcpIp_V1_TypeGroup1.daddr
- TcpIp_V1_TypeGroup1.saddr
- TcpIp_V1_TypeGroup1.dport
- TcpIp_V1_TypeGroup1.sport
api_type:
- NA
api_location: ''
ms.openlocfilehash: fcd5f19eafa5308ef369a211559c6c464427b168
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104984777"
---
# <a name="tcpip_v1_typegroup1-class"></a><span data-ttu-id="cfdf1-104">\_ \_ Класс TypeGroup1 TcpIp v1</span><span class="sxs-lookup"><span data-stu-id="cfdf1-104">TcpIp\_V1\_TypeGroup1 class</span></span>

<span data-ttu-id="cfdf1-105">Этот класс является классом типа событий для событий TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="cfdf1-105">This class is the event type class for TCP/IP events.</span></span>

<span data-ttu-id="cfdf1-106">Следующий синтаксис упрощен из MOF-кода.</span><span class="sxs-lookup"><span data-stu-id="cfdf1-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="cfdf1-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="cfdf1-107">Syntax</span></span>

``` syntax
[EventType{10, 11, 12, 13, 14, 15, 16}, EventTypeName{"Send", "Recv", "Connect", "Disconnect", "Retransmit", "Accept", "Reconnect"}]
class TcpIp_V1_TypeGroup1 : TcpIp_V1
{
  uint32 PID;
  uint32 size;
  object daddr;
  object saddr;
  object dport;
  object sport;
};
```

## <a name="members"></a><span data-ttu-id="cfdf1-108">Участники</span><span class="sxs-lookup"><span data-stu-id="cfdf1-108">Members</span></span>

<span data-ttu-id="cfdf1-109">Класс **TcpIp \_ v1 \_ TypeGroup1** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="cfdf1-109">The **TcpIp\_V1\_TypeGroup1** class has these types of members:</span></span>

-   [<span data-ttu-id="cfdf1-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="cfdf1-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="cfdf1-111">Свойства</span><span class="sxs-lookup"><span data-stu-id="cfdf1-111">Properties</span></span>

<span data-ttu-id="cfdf1-112">Класс **TcpIp \_ v1 \_ TypeGroup1** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="cfdf1-112">The **TcpIp\_V1\_TypeGroup1** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="cfdf1-113">даддр</span><span class="sxs-lookup"><span data-stu-id="cfdf1-113">daddr</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cfdf1-114">Тип данных: **объект**</span><span class="sxs-lookup"><span data-stu-id="cfdf1-114">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="cfdf1-115">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="cfdf1-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cfdf1-116">Квалификаторы: Вмидатаид (3), Extension ("reduce")</span><span class="sxs-lookup"><span data-stu-id="cfdf1-116">Qualifiers: WmiDataId(3), Extension("IPAddr")</span></span>
</dt> </dl>

<span data-ttu-id="cfdf1-117">Конечный IP-адрес.</span><span class="sxs-lookup"><span data-stu-id="cfdf1-117">Destination IP address.</span></span>

</dd> <dt>

<span data-ttu-id="cfdf1-118">дпорт</span><span class="sxs-lookup"><span data-stu-id="cfdf1-118">dport</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cfdf1-119">Тип данных: **объект**</span><span class="sxs-lookup"><span data-stu-id="cfdf1-119">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="cfdf1-120">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="cfdf1-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cfdf1-121">Квалификаторы: Вмидатаид (5), Extension ("порт")</span><span class="sxs-lookup"><span data-stu-id="cfdf1-121">Qualifiers: WmiDataId(5), Extension("Port")</span></span>
</dt> </dl>

<span data-ttu-id="cfdf1-122">Номер порта назначения.</span><span class="sxs-lookup"><span data-stu-id="cfdf1-122">Destination port number.</span></span>

</dd> <dt>

<span data-ttu-id="cfdf1-123">ИД процесса</span><span class="sxs-lookup"><span data-stu-id="cfdf1-123">PID</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cfdf1-124">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="cfdf1-124">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="cfdf1-125">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="cfdf1-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cfdf1-126">Квалификаторы: Вмидатаид (1)</span><span class="sxs-lookup"><span data-stu-id="cfdf1-126">Qualifiers: WmiDataId(1)</span></span>
</dt> </dl>

<span data-ttu-id="cfdf1-127">Идентификатор процесса, связанного с запросом.</span><span class="sxs-lookup"><span data-stu-id="cfdf1-127">Identifier of the process associated with the request.</span></span>

</dd> <dt>

<span data-ttu-id="cfdf1-128">саддр</span><span class="sxs-lookup"><span data-stu-id="cfdf1-128">saddr</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cfdf1-129">Тип данных: **объект**</span><span class="sxs-lookup"><span data-stu-id="cfdf1-129">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="cfdf1-130">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="cfdf1-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cfdf1-131">Квалификаторы: Вмидатаид (4), Extension ("reduce")</span><span class="sxs-lookup"><span data-stu-id="cfdf1-131">Qualifiers: WmiDataId(4), Extension("IPAddr")</span></span>
</dt> </dl>

<span data-ttu-id="cfdf1-132">Исходный IP-адрес.</span><span class="sxs-lookup"><span data-stu-id="cfdf1-132">Source IP address.</span></span>

</dd> <dt>

<span data-ttu-id="cfdf1-133">size</span><span class="sxs-lookup"><span data-stu-id="cfdf1-133">size</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cfdf1-134">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="cfdf1-134">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="cfdf1-135">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="cfdf1-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cfdf1-136">Квалификаторы: Вмидатаид (2)</span><span class="sxs-lookup"><span data-stu-id="cfdf1-136">Qualifiers: WmiDataId(2)</span></span>
</dt> </dl>

<span data-ttu-id="cfdf1-137">Размер пакета.</span><span class="sxs-lookup"><span data-stu-id="cfdf1-137">Size of the packet.</span></span>

</dd> <dt>

<span data-ttu-id="cfdf1-138">назван</span><span class="sxs-lookup"><span data-stu-id="cfdf1-138">sport</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cfdf1-139">Тип данных: **объект**</span><span class="sxs-lookup"><span data-stu-id="cfdf1-139">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="cfdf1-140">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="cfdf1-140">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cfdf1-141">Квалификаторы: Вмидатаид (6), Extension ("порт")</span><span class="sxs-lookup"><span data-stu-id="cfdf1-141">Qualifiers: WmiDataId(6), Extension("Port")</span></span>
</dt> </dl>

<span data-ttu-id="cfdf1-142">Номер исходного порта.</span><span class="sxs-lookup"><span data-stu-id="cfdf1-142">Source port number.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="cfdf1-143">Требования</span><span class="sxs-lookup"><span data-stu-id="cfdf1-143">Requirements</span></span>



| <span data-ttu-id="cfdf1-144">Требование</span><span class="sxs-lookup"><span data-stu-id="cfdf1-144">Requirement</span></span> | <span data-ttu-id="cfdf1-145">Значение</span><span class="sxs-lookup"><span data-stu-id="cfdf1-145">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="cfdf1-146">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="cfdf1-146">Minimum supported client</span></span><br/> | <span data-ttu-id="cfdf1-147">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="cfdf1-147">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="cfdf1-148">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="cfdf1-148">Minimum supported server</span></span><br/> | <span data-ttu-id="cfdf1-149">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="cfdf1-149">Windows Server 2003 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="cfdf1-150">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="cfdf1-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cfdf1-151">**TcpIp \_ v1**</span><span class="sxs-lookup"><span data-stu-id="cfdf1-151">**TcpIp\_V1**</span></span>](tcpip-v1.md)
</dt> </dl>

 

 




