---
description: Этот класс является классом типа событий для сетевых событий. Следующий синтаксис упрощен из MOF-кода.
ms.assetid: afa994ef-dd1c-4909-a6cd-7021be4fff40
title: Класс SystemConfig_Network
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SystemConfig_Network
- SystemConfig_Network.TcbTablePartitions
- SystemConfig_Network.MaxHashTableSize
- SystemConfig_Network.MaxUserPort
- SystemConfig_Network.TcpTimedWaitDelay
api_type:
- NA
api_location: ''
ms.openlocfilehash: 23b469c31645c6a5b04319f91b758ee19beb935c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104984452"
---
# <a name="systemconfig_network-class"></a><span data-ttu-id="2e7f0-104">\_Класс системконфиг Network</span><span class="sxs-lookup"><span data-stu-id="2e7f0-104">SystemConfig\_Network class</span></span>

<span data-ttu-id="2e7f0-105">Этот класс является классом типа событий для сетевых событий.</span><span class="sxs-lookup"><span data-stu-id="2e7f0-105">This class is the event type class for network events.</span></span>

<span data-ttu-id="2e7f0-106">Следующий синтаксис упрощен из MOF-кода.</span><span class="sxs-lookup"><span data-stu-id="2e7f0-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="2e7f0-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="2e7f0-107">Syntax</span></span>

``` syntax
[EventType(17), EventTypeName("Network")]
class SystemConfig_Network : SystemConfig
{
  uint32 TcbTablePartitions;
  uint32 MaxHashTableSize;
  uint32 MaxUserPort;
  uint32 TcpTimedWaitDelay;
};
```

## <a name="members"></a><span data-ttu-id="2e7f0-108">Участники</span><span class="sxs-lookup"><span data-stu-id="2e7f0-108">Members</span></span>

<span data-ttu-id="2e7f0-109">Класс **системконфиг \_ Network** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="2e7f0-109">The **SystemConfig\_Network** class has these types of members:</span></span>

-   [<span data-ttu-id="2e7f0-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="2e7f0-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="2e7f0-111">Свойства</span><span class="sxs-lookup"><span data-stu-id="2e7f0-111">Properties</span></span>

<span data-ttu-id="2e7f0-112">Класс **системконфиг \_ Network** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="2e7f0-112">The **SystemConfig\_Network** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="2e7f0-113">**MaxHashTableSize**</span><span class="sxs-lookup"><span data-stu-id="2e7f0-113">**MaxHashTableSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2e7f0-114">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="2e7f0-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="2e7f0-115">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="2e7f0-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2e7f0-116">Квалификаторы: Вмидатаид (2)</span><span class="sxs-lookup"><span data-stu-id="2e7f0-116">Qualifiers: WmiDataId(2)</span></span>
</dt> </dl>

<span data-ttu-id="2e7f0-117">Размер хэш-таблицы, в которой хранятся управляющие блоки TCP (Ткбс).</span><span class="sxs-lookup"><span data-stu-id="2e7f0-117">The size of the hash table in which TCP control blocks (TCBs) are stored.</span></span> <span data-ttu-id="2e7f0-118">Протокол TCP хранит управляющие блоки в хэш-таблице, что позволяет быстро найти их.</span><span class="sxs-lookup"><span data-stu-id="2e7f0-118">TCP stores control blocks in a hash table so it can find them very quickly.</span></span>

</dd> <dt>

<span data-ttu-id="2e7f0-119">**MaxUserPort**</span><span class="sxs-lookup"><span data-stu-id="2e7f0-119">**MaxUserPort**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2e7f0-120">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="2e7f0-120">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="2e7f0-121">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="2e7f0-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2e7f0-122">Квалификаторы: Вмидатаид (3)</span><span class="sxs-lookup"><span data-stu-id="2e7f0-122">Qualifiers: WmiDataId(3)</span></span>
</dt> </dl>

<span data-ttu-id="2e7f0-123">Порт с наибольшим номером TCP может быть назначен, когда приложение запрашивает доступный порт пользователя из системы.</span><span class="sxs-lookup"><span data-stu-id="2e7f0-123">The highest port number TCP can assign when an application requests an available user port from the system.</span></span> <span data-ttu-id="2e7f0-124">Обычно временные порты (которые используются ненадолго) выделяются на номера портов 1024 – 5000.</span><span class="sxs-lookup"><span data-stu-id="2e7f0-124">Typically, ephemeral ports (those used briefly) are allocated to port numbers 1024 through 5000.</span></span>

<span data-ttu-id="2e7f0-125">Значение для самого высокого номера порта пользователя, которое может назначать TCP, управляется параметром реестра.</span><span class="sxs-lookup"><span data-stu-id="2e7f0-125">The value for the highest user port number TCP can assign is controlled by a registry setting.</span></span> <span data-ttu-id="2e7f0-126">Дополнительные сведения см. в разделе [MaxUserPort](/previous-versions/windows/it-pro/windows-2000-server/cc938196(v=technet.10)).</span><span class="sxs-lookup"><span data-stu-id="2e7f0-126">For more information, see [MaxUserPort](/previous-versions/windows/it-pro/windows-2000-server/cc938196(v=technet.10)).</span></span>

</dd> <dt>

<span data-ttu-id="2e7f0-127">**ткбтаблепартитионс**</span><span class="sxs-lookup"><span data-stu-id="2e7f0-127">**TcbTablePartitions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2e7f0-128">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="2e7f0-128">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="2e7f0-129">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="2e7f0-129">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2e7f0-130">Квалификаторы: Вмидатаид (1)</span><span class="sxs-lookup"><span data-stu-id="2e7f0-130">Qualifiers: WmiDataId(1)</span></span>
</dt> </dl>

<span data-ttu-id="2e7f0-131">Количество секций в таблице блоков управления транспортом.</span><span class="sxs-lookup"><span data-stu-id="2e7f0-131">The number of partitions in the Transport Control Block table.</span></span> <span data-ttu-id="2e7f0-132">Секционирование таблицы управления транспортным блоком уменьшает состязание за доступ к таблицам.</span><span class="sxs-lookup"><span data-stu-id="2e7f0-132">Partitioning the Transport Control Block table minimizes contention for table access.</span></span> <span data-ttu-id="2e7f0-133">Это особенно удобно в многопроцессорных системах.</span><span class="sxs-lookup"><span data-stu-id="2e7f0-133">This is especially useful on multiprocessor systems.</span></span>

</dd> <dt>

<span data-ttu-id="2e7f0-134">**TcpTimedWaitDelay**</span><span class="sxs-lookup"><span data-stu-id="2e7f0-134">**TcpTimedWaitDelay**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2e7f0-135">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="2e7f0-135">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="2e7f0-136">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="2e7f0-136">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2e7f0-137">Квалификаторы: Вмидатаид (4)</span><span class="sxs-lookup"><span data-stu-id="2e7f0-137">Qualifiers: WmiDataId(4)</span></span>
</dt> </dl>

<span data-ttu-id="2e7f0-138">Время, которое должно пройти до того, как TCP сможет освободить закрытое подключение и повторно использовать его ресурсы.</span><span class="sxs-lookup"><span data-stu-id="2e7f0-138">The time that must elapse before TCP can release a closed connection and reuse its resources.</span></span> <span data-ttu-id="2e7f0-139">Этот интервал между замыканием и выпуском называется \_ состоянием времени ожидания или состоянием 2MSL.</span><span class="sxs-lookup"><span data-stu-id="2e7f0-139">This interval between closure and release is known as the TIME\_WAIT state or 2MSL state.</span></span> <span data-ttu-id="2e7f0-140">В течение этого времени подключение можно повторно открыть на клиенте и сервере гораздо реже, чем устанавливать новое соединение.</span><span class="sxs-lookup"><span data-stu-id="2e7f0-140">During this time, the connection can be reopened at much less cost to the client and server than establishing a new connection.</span></span>

<span data-ttu-id="2e7f0-141">RFC 793, опубликованный IETF, требует, чтобы протокол TCP не превышал установленное соединение в два раза больше, чем максимальное время существования сегмента (2MSL) сети.</span><span class="sxs-lookup"><span data-stu-id="2e7f0-141">RFC 793 published by the IETF requires that TCP maintains a closed connection for an interval at least equal to twice the maximum segment lifetime (2MSL) of the network.</span></span> <span data-ttu-id="2e7f0-142">При освобождении подключения его пара сокетов и управляющий блок TCP (TCB) можно использовать для поддержки другого подключения.</span><span class="sxs-lookup"><span data-stu-id="2e7f0-142">When a connection is released, its socket pair and TCP control block (TCB) can be used to support another connection.</span></span> <span data-ttu-id="2e7f0-143">По умолчанию язык MSL определяется как 120 секунд, а значение этой записи равно двум MSLs или 4 минутам.</span><span class="sxs-lookup"><span data-stu-id="2e7f0-143">By default, the MSL is defined to be 120 seconds, and the value of this entry is equal to two MSLs, or 4 minutes.</span></span> <span data-ttu-id="2e7f0-144">Дополнительные сведения см. в [документе RFC 793](https://tools.ietf.org/html/rfc973).</span><span class="sxs-lookup"><span data-stu-id="2e7f0-144">For more information, see [RFC 793](https://tools.ietf.org/html/rfc973).</span></span>

<span data-ttu-id="2e7f0-145">Уменьшение значения этой записи с помощью параметра реестра позволяет TCP освобождать закрытые подключения быстрее, предоставляя дополнительные ресурсы для новых подключений.</span><span class="sxs-lookup"><span data-stu-id="2e7f0-145">Reducing the value of this entry using a registry setting allows TCP to release closed connections faster, providing more resources for new connections.</span></span> <span data-ttu-id="2e7f0-146">Однако если значение слишком мало, TCP может освободить ресурсы подключения до завершения подключения, что потребует от сервера использовать дополнительные ресурсы для повторного установления соединения.</span><span class="sxs-lookup"><span data-stu-id="2e7f0-146">However, if the value is too low, TCP might release connection resources before the connection is complete, requiring the server to use additional resources to reestablish the connection.</span></span>

<span data-ttu-id="2e7f0-147">Как правило, протокол TCP не освобождает закрытые подключения до тех пор, пока не истечет значение этой записи.</span><span class="sxs-lookup"><span data-stu-id="2e7f0-147">Normally, TCP does not release closed connections until the value of this entry expires.</span></span> <span data-ttu-id="2e7f0-148">Однако TCP может освободить подключения до истечения срока действия этого значения, если в нем исключаются управляющие блоки TCP (Ткбс).</span><span class="sxs-lookup"><span data-stu-id="2e7f0-148">However, TCP can release connections before this value expires if it is running out of TCP control blocks (TCBs).</span></span> <span data-ttu-id="2e7f0-149">Число Ткбс, создаваемых системой, управляется параметром реестра.</span><span class="sxs-lookup"><span data-stu-id="2e7f0-149">The number of TCBs the system creates is controlled by a registry setting.</span></span> <span data-ttu-id="2e7f0-150">Дополнительные сведения см. в разделе [наибольше](/previous-versions/windows/it-pro/windows-2000-server/cc938178(v=technet.10)).</span><span class="sxs-lookup"><span data-stu-id="2e7f0-150">For more information, see [MaxFreeTCBs](/previous-versions/windows/it-pro/windows-2000-server/cc938178(v=technet.10)).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="2e7f0-151">Требования</span><span class="sxs-lookup"><span data-stu-id="2e7f0-151">Requirements</span></span>



| <span data-ttu-id="2e7f0-152">Требование</span><span class="sxs-lookup"><span data-stu-id="2e7f0-152">Requirement</span></span> | <span data-ttu-id="2e7f0-153">Значение</span><span class="sxs-lookup"><span data-stu-id="2e7f0-153">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="2e7f0-154">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="2e7f0-154">Minimum supported client</span></span><br/> | <span data-ttu-id="2e7f0-155">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="2e7f0-155">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="2e7f0-156">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="2e7f0-156">Minimum supported server</span></span><br/> | <span data-ttu-id="2e7f0-157">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="2e7f0-157">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="2e7f0-158">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="2e7f0-158">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2e7f0-159">**системконфиг**</span><span class="sxs-lookup"><span data-stu-id="2e7f0-159">**SystemConfig**</span></span>](systemconfig.md)
</dt> </dl>

 

 
