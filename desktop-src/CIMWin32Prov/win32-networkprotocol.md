---
description: '&Win32 \_ NetworkProtocol \# 8194; Класс WMI представляет протокол и его характеристики сети в компьютерной системе Win32.'
ms.assetid: c864a694-d507-4629-91c5-bd26ccf397f7
ms.tgt_platform: multiple
title: Класс Win32_NetworkProtocol
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_NetworkProtocol
- Win32_NetworkProtocol.Caption
- Win32_NetworkProtocol.Description
- Win32_NetworkProtocol.InstallDate
- Win32_NetworkProtocol.Status
- Win32_NetworkProtocol.ConnectionlessService
- Win32_NetworkProtocol.GuaranteesDelivery
- Win32_NetworkProtocol.GuaranteesSequencing
- Win32_NetworkProtocol.MaximumAddressSize
- Win32_NetworkProtocol.MaximumMessageSize
- Win32_NetworkProtocol.MessageOriented
- Win32_NetworkProtocol.MinimumAddressSize
- Win32_NetworkProtocol.Name
- Win32_NetworkProtocol.PseudoStreamOriented
- Win32_NetworkProtocol.SupportsBroadcasting
- Win32_NetworkProtocol.SupportsConnectData
- Win32_NetworkProtocol.SupportsDisconnectData
- Win32_NetworkProtocol.SupportsEncryption
- Win32_NetworkProtocol.SupportsExpeditedData
- Win32_NetworkProtocol.SupportsFragmentation
- Win32_NetworkProtocol.SupportsGracefulClosing
- Win32_NetworkProtocol.SupportsGuaranteedBandwidth
- Win32_NetworkProtocol.SupportsMulticasting
- Win32_NetworkProtocol.SupportsQualityofService
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 33817fa4aa55747ecf9d4e89f5dcf406160c0c67
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104496596"
---
# <a name="win32_networkprotocol-class"></a><span data-ttu-id="33fc2-103">\_Класс Win32 NetworkProtocol</span><span class="sxs-lookup"><span data-stu-id="33fc2-103">Win32\_NetworkProtocol class</span></span>

<span data-ttu-id="33fc2-104">Класс **WMI \_ NetworkProtocol** [инструментария](../wmisdk/retrieving-a-class.md) Win32 представляет протокол и его характеристики сети в компьютерной системе Win32.</span><span class="sxs-lookup"><span data-stu-id="33fc2-104">The **Win32\_NetworkProtocol** [WMI class](../wmisdk/retrieving-a-class.md) represents a protocol and its network characteristics on a Win32 computer system.</span></span>

<span data-ttu-id="33fc2-105">Следующий пример синтаксиса — упрощенный MOF-код, который включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="33fc2-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="33fc2-106">Свойства и методы имеют алфавитный порядок, а не порядок MOF.</span><span class="sxs-lookup"><span data-stu-id="33fc2-106">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="33fc2-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="33fc2-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C4D8-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_NetworkProtocol : CIM_LogicalElement
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Status;
  boolean  ConnectionlessService;
  boolean  GuaranteesDelivery;
  boolean  GuaranteesSequencing;
  uint32   MaximumAddressSize;
  uint32   MaximumMessageSize;
  boolean  MessageOriented;
  uint32   MinimumAddressSize;
  string   Name;
  boolean  PseudoStreamOriented;
  boolean  SupportsBroadcasting;
  boolean  SupportsConnectData;
  boolean  SupportsDisconnectData;
  boolean  SupportsEncryption;
  boolean  SupportsExpeditedData;
  boolean  SupportsFragmentation;
  boolean  SupportsGracefulClosing;
  boolean  SupportsGuaranteedBandwidth;
  boolean  SupportsMulticasting;
  boolean  SupportsQualityofService;
};
```

## <a name="members"></a><span data-ttu-id="33fc2-108">Члены</span><span class="sxs-lookup"><span data-stu-id="33fc2-108">Members</span></span>

<span data-ttu-id="33fc2-109">Класс **Win32 \_ NetworkProtocol** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="33fc2-109">The **Win32\_NetworkProtocol** class has these types of members:</span></span>

-   [<span data-ttu-id="33fc2-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="33fc2-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="33fc2-111">Свойства</span><span class="sxs-lookup"><span data-stu-id="33fc2-111">Properties</span></span>

<span data-ttu-id="33fc2-112">Класс **Win32 \_ NetworkProtocol** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="33fc2-112">The **Win32\_NetworkProtocol** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="33fc2-113">**Заголовок**</span><span class="sxs-lookup"><span data-stu-id="33fc2-113">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="33fc2-114">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="33fc2-114">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="33fc2-115">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="33fc2-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="33fc2-116">Квалификаторы: [**maxlen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="33fc2-116">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="33fc2-117">Краткое текстовое описание объекта.</span><span class="sxs-lookup"><span data-stu-id="33fc2-117">A short textual description of the object.</span></span>

<span data-ttu-id="33fc2-118">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="33fc2-118">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="33fc2-119">**коннектионлесссервице**</span><span class="sxs-lookup"><span data-stu-id="33fc2-119">**ConnectionlessService**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="33fc2-120">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="33fc2-120">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="33fc2-121">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="33fc2-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="33fc2-122">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32 \_ API \| Windows сокеты структурные \| \_ сведения о протоколе \| двсервицефлагс \| XP1 \_ без подключения")</span><span class="sxs-lookup"><span data-stu-id="33fc2-122">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32\_API\|Windows Sockets Structures\|PROTOCOL\_INFO\|dwServiceFlags\|XP1\_CONNECTIONLESS")</span></span>
</dt> </dl>

<span data-ttu-id="33fc2-123">Протокол поддерживает службу без подключения.</span><span class="sxs-lookup"><span data-stu-id="33fc2-123">Protocol supports connectionless service.</span></span> <span data-ttu-id="33fc2-124">Служба без подключения (Datagram) описывает протокол связи или транспорт, в котором пакеты данных направляются независимо друг от друга и могут следовать разным маршрутам и поступать в порядке, отличном от того, в котором они были отправлены.</span><span class="sxs-lookup"><span data-stu-id="33fc2-124">A connectionless (datagram) service describes a communications protocol or transport in which data packets are routed independently of each other and may follow different routes and arrive in a different order from that in which they were sent.</span></span> <span data-ttu-id="33fc2-125">И наоборот, служба, ориентированная на подключение, предоставляет виртуальный канал, через который пакеты данных получаются в том же порядке, в котором они были переданы.</span><span class="sxs-lookup"><span data-stu-id="33fc2-125">Conversely, a connection-oriented service provides a virtual circuit through which data packets are received in the same order they were transmitted.</span></span> <span data-ttu-id="33fc2-126">Если подключение между компьютерами завершается сбоем, приложение получает уведомления.</span><span class="sxs-lookup"><span data-stu-id="33fc2-126">If the connection between computers fails, the application is notified.</span></span>

</dd> <dt>

<span data-ttu-id="33fc2-127">**Описание**</span><span class="sxs-lookup"><span data-stu-id="33fc2-127">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="33fc2-128">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="33fc2-128">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="33fc2-129">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="33fc2-129">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="33fc2-130">Квалификаторы: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Описание")</span><span class="sxs-lookup"><span data-stu-id="33fc2-130">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="33fc2-131">Текстовое описание объекта.</span><span class="sxs-lookup"><span data-stu-id="33fc2-131">A textual description of the object.</span></span>

<span data-ttu-id="33fc2-132">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="33fc2-132">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="33fc2-133">**гуарантисделивери**</span><span class="sxs-lookup"><span data-stu-id="33fc2-133">**GuaranteesDelivery**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="33fc2-134">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="33fc2-134">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="33fc2-135">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="33fc2-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="33fc2-136">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("платформа Win32 \_ API \| Windows: \| сведения о протоколе \_ \| двсервицефлагс \| XP \_ — гарантированная \_ Доставка")</span><span class="sxs-lookup"><span data-stu-id="33fc2-136">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32\_API\|Windows Sockets Structures\|PROTOCOL\_INFO\|dwServiceFlags\|XP\_GUARANTEED\_DELIVERY")</span></span>
</dt> </dl>

<span data-ttu-id="33fc2-137">Протокол поддерживает доставку пакетов данных.</span><span class="sxs-lookup"><span data-stu-id="33fc2-137">Protocol supports delivery of data packets.</span></span> <span data-ttu-id="33fc2-138">Если этот флаг имеет **значение false**, это не значит, что все отправленные данные будут достигать предполагаемого назначения.</span><span class="sxs-lookup"><span data-stu-id="33fc2-138">If this flag is **FALSE**, it is uncertain that all of the data sent will reach the intended destination.</span></span>

</dd> <dt>

<span data-ttu-id="33fc2-139">**гуарантиссекуенЦинг**</span><span class="sxs-lookup"><span data-stu-id="33fc2-139">**GuaranteesSequencing**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="33fc2-140">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="33fc2-140">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="33fc2-141">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="33fc2-141">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="33fc2-142">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("платформа Win32 \_ API \| Windows. \| сведения о протоколе \_ \| двсервицефлагс \| XP \_ — гарантированный \_ порядок")</span><span class="sxs-lookup"><span data-stu-id="33fc2-142">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32\_API\|Windows Sockets Structures\|PROTOCOL\_INFO\|dwServiceFlags\|XP\_GUARANTEED\_ORDER")</span></span>
</dt> </dl>

<span data-ttu-id="33fc2-143">Протокол гарантирует, что данные будут поступать в том порядке, в котором они были отправлены.</span><span class="sxs-lookup"><span data-stu-id="33fc2-143">Protocol ensures that data will arrive in the order in which it was sent.</span></span> <span data-ttu-id="33fc2-144">Имейте в виду, что эта характеристика не гарантирует доставку данных, а только их порядок.</span><span class="sxs-lookup"><span data-stu-id="33fc2-144">Be aware that this characteristic does not ensure delivery of the data, only its order.</span></span>

</dd> <dt>

<span data-ttu-id="33fc2-145">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="33fc2-145">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="33fc2-146">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="33fc2-146">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="33fc2-147">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="33fc2-147">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="33fc2-148">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) (MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](../wmisdk/standard-qualifiers.md) (" Дата установки ")</span><span class="sxs-lookup"><span data-stu-id="33fc2-148">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="33fc2-149">Указывает, когда был установлен объект.</span><span class="sxs-lookup"><span data-stu-id="33fc2-149">Indicates when the object was installed.</span></span> <span data-ttu-id="33fc2-150">Отсутствие значения не означает, что объект не установлен.</span><span class="sxs-lookup"><span data-stu-id="33fc2-150">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="33fc2-151">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="33fc2-151">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="33fc2-152">**максимумаддресссизе**</span><span class="sxs-lookup"><span data-stu-id="33fc2-152">**MaximumAddressSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="33fc2-153">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="33fc2-153">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="33fc2-154">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="33fc2-154">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="33fc2-155">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) (" \_ интерфейс Win32 API \| Windows-структура \| \_ сведения о протоколе \| имакссоккаддр"), [**единицы**](../wmisdk/standard-qualifiers.md) ("символы")</span><span class="sxs-lookup"><span data-stu-id="33fc2-155">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32\_API\|Windows Sockets Structures\|PROTOCOL\_INFO\|iMaxSockAddr"), [**units**](../wmisdk/standard-qualifiers.md) ("characters")</span></span>
</dt> </dl>

<span data-ttu-id="33fc2-156">Максимальная длина адреса сокета, поддерживаемого протоколом.</span><span class="sxs-lookup"><span data-stu-id="33fc2-156">Maximum length of a socket address supported by the protocol.</span></span> <span data-ttu-id="33fc2-157">Адресами сокетов могут быть такие элементы, как URL-адрес ( `www.microsoft.com` ) или IP-адрес ( `130.215.24.1` ).</span><span class="sxs-lookup"><span data-stu-id="33fc2-157">Socket addresses may be items such as a URL (`www.microsoft.com`) or an IP address (`130.215.24.1`).</span></span>

</dd> <dt>

<span data-ttu-id="33fc2-158">**максимуммессажесизе**</span><span class="sxs-lookup"><span data-stu-id="33fc2-158">**MaximumMessageSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="33fc2-159">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="33fc2-159">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="33fc2-160">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="33fc2-160">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="33fc2-161">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) (" \_ интерфейс Win32 API \| Windows-структура \| \_ сведения о протоколе \| двмессажесизе"), [**единицы**](../wmisdk/standard-qualifiers.md) ("символы")</span><span class="sxs-lookup"><span data-stu-id="33fc2-161">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32\_API\|Windows Sockets Structures\|PROTOCOL\_INFO\|dwMessageSize"), [**units**](../wmisdk/standard-qualifiers.md) ("characters")</span></span>
</dt> </dl>

<span data-ttu-id="33fc2-162">Максимальный размер сообщения, поддерживаемый протоколом.</span><span class="sxs-lookup"><span data-stu-id="33fc2-162">Maximum message size supported by the protocol.</span></span> <span data-ttu-id="33fc2-163">Это максимальный размер сообщения, которое может быть отправлено или получено узлом.</span><span class="sxs-lookup"><span data-stu-id="33fc2-163">This is the maximum size of a message that can be sent from or received by the host.</span></span> <span data-ttu-id="33fc2-164">Для протоколов, которые не поддерживают Кадрирование сообщений, фактический максимальный размер сообщения, который может быть отправлен на указанный адрес, может быть меньше этого значения.</span><span class="sxs-lookup"><span data-stu-id="33fc2-164">For protocols that do not support message framing, the actual maximum size of a message that can be sent to a given address may be less than this value.</span></span>

</dd> <dt>

<span data-ttu-id="33fc2-165">**мессажеориентед**</span><span class="sxs-lookup"><span data-stu-id="33fc2-165">**MessageOriented**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="33fc2-166">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="33fc2-166">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="33fc2-167">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="33fc2-167">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="33fc2-168">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("платформа Win32 \_ API \| Windows \| \_ сведения о протоколе \| двсервицефлагс \| XP с \_ ориентацией на сообщения \_ ")</span><span class="sxs-lookup"><span data-stu-id="33fc2-168">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32\_API\|Windows Sockets Structures\|PROTOCOL\_INFO\|dwServiceFlags\|XP\_MESSAGE\_ORIENTED")</span></span>
</dt> </dl>

<span data-ttu-id="33fc2-169">Протокол является ориентированным на сообщения.</span><span class="sxs-lookup"><span data-stu-id="33fc2-169">Protocol is message-oriented.</span></span> <span data-ttu-id="33fc2-170">Протокол, ориентированный на сообщения, использует пакеты данных для пересылки информации.</span><span class="sxs-lookup"><span data-stu-id="33fc2-170">A message-oriented protocol uses packets of data to transfer information.</span></span> <span data-ttu-id="33fc2-171">И наоборот, протоколы, ориентированные на потоковую передачу данных, передаются в виде непрерывного потока байтов.</span><span class="sxs-lookup"><span data-stu-id="33fc2-171">Conversely, stream-oriented protocols transfer data as a continuous stream of bytes.</span></span>

</dd> <dt>

<span data-ttu-id="33fc2-172">**минимумаддресссизе**</span><span class="sxs-lookup"><span data-stu-id="33fc2-172">**MinimumAddressSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="33fc2-173">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="33fc2-173">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="33fc2-174">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="33fc2-174">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="33fc2-175">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) (" \_ интерфейс Win32 API \| Windows-структура \| \_ сведения о протоколе \| иминсоккаддр"), [**единицы**](../wmisdk/standard-qualifiers.md) ("символы")</span><span class="sxs-lookup"><span data-stu-id="33fc2-175">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32\_API\|Windows Sockets Structures\|PROTOCOL\_INFO\|iMinSockAddr "), [**units**](../wmisdk/standard-qualifiers.md) ("characters")</span></span>
</dt> </dl>

<span data-ttu-id="33fc2-176">Минимальная длина адреса сокета, поддерживаемого протоколом.</span><span class="sxs-lookup"><span data-stu-id="33fc2-176">Minimum length of a socket address supported by the protocol.</span></span>

</dd> <dt>

<span data-ttu-id="33fc2-177">**Name**</span><span class="sxs-lookup"><span data-stu-id="33fc2-177">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="33fc2-178">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="33fc2-178">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="33fc2-179">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="33fc2-179">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="33fc2-180">Квалификаторы: [**ключ**](../wmisdk/key-qualifier.md), [**Переопределение**](../wmisdk/standard-qualifiers.md) ("имя"), [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32 \_ API \| Windows сокеты-структура \| сведения о протоколе \_ \| лппротокол")</span><span class="sxs-lookup"><span data-stu-id="33fc2-180">Qualifiers: [**key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("Name"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32\_API\|Windows Sockets Structures\|PROTOCOL\_INFO\|lpProtocol")</span></span>
</dt> </dl>

<span data-ttu-id="33fc2-181">Имя протокола.</span><span class="sxs-lookup"><span data-stu-id="33fc2-181">Name for the protocol.</span></span>

<span data-ttu-id="33fc2-182">Пример: "TCP/IP"</span><span class="sxs-lookup"><span data-stu-id="33fc2-182">Example: "TCP/IP"</span></span>

</dd> <dt>

<span data-ttu-id="33fc2-183">**псеудостреамориентед**</span><span class="sxs-lookup"><span data-stu-id="33fc2-183">**PseudoStreamOriented**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="33fc2-184">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="33fc2-184">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="33fc2-185">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="33fc2-185">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="33fc2-186">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("платформа Win32 \_ API \| Windows \| \_ сведения о протоколе \| двсервицефлагс \| XP \_ псевдо \_ -Stream")</span><span class="sxs-lookup"><span data-stu-id="33fc2-186">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32\_API\|Windows Sockets Structures\|PROTOCOL\_INFO\|dwServiceFlags\|XP\_PSEUDO\_STREAM")</span></span>
</dt> </dl>

<span data-ttu-id="33fc2-187">Протокол — это протокол, ориентированный на сообщения, который может принимать пакеты данных переменной длины или потоковые данные для всех операций получения.</span><span class="sxs-lookup"><span data-stu-id="33fc2-187">Protocol is a message-oriented protocol that can receive variable-length data packets or streamed data for all receive operations.</span></span> <span data-ttu-id="33fc2-188">Эта необязательная возможность полезна, когда приложению не требуется, чтобы протокол закадрового сообщения, и требует характеристик, ориентированных на поток.</span><span class="sxs-lookup"><span data-stu-id="33fc2-188">This optional ability is useful when an application does not want the protocol to frame messages, and requires stream-oriented characteristics.</span></span> <span data-ttu-id="33fc2-189">Если **значение равно true**, то протокол является псевдо-ориентированным.</span><span class="sxs-lookup"><span data-stu-id="33fc2-189">If **TRUE**, the protocol is pseudo stream-oriented.</span></span>

</dd> <dt>

<span data-ttu-id="33fc2-190">**Состояние**</span><span class="sxs-lookup"><span data-stu-id="33fc2-190">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="33fc2-191">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="33fc2-191">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="33fc2-192">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="33fc2-192">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="33fc2-193">Квалификаторы: [**maxlen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("состояние")</span><span class="sxs-lookup"><span data-stu-id="33fc2-193">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="33fc2-194">Строка, указывающая текущее состояние объекта.</span><span class="sxs-lookup"><span data-stu-id="33fc2-194">String that indicates the current status of the object.</span></span> <span data-ttu-id="33fc2-195">Можно определить операционное и нерабочее состояние.</span><span class="sxs-lookup"><span data-stu-id="33fc2-195">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="33fc2-196">Оперативное состояние может включать "ОК", "деградация" и "пред Fail".</span><span class="sxs-lookup"><span data-stu-id="33fc2-196">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="33fc2-197">"Пред-Fail" указывает, что элемент работает правильно, но прогнозирует сбой (например, жесткий диск с поддержкой SMART).</span><span class="sxs-lookup"><span data-stu-id="33fc2-197">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="33fc2-198">Нерабочее состояние может включать "Error", "starting", "остановка" и "обслуживание".</span><span class="sxs-lookup"><span data-stu-id="33fc2-198">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="33fc2-199">"Служба" может применяться при зеркальном отображении дисков, перезагрузке списка разрешений пользователя или выполнении других административных задач.</span><span class="sxs-lookup"><span data-stu-id="33fc2-199">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="33fc2-200">Не вся такая работа находится в оперативном режиме, но управляемый элемент не является ни "ОК", ни в одном из других состояний.</span><span class="sxs-lookup"><span data-stu-id="33fc2-200">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="33fc2-201">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="33fc2-201">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="33fc2-202">В эти значения входят:</span><span class="sxs-lookup"><span data-stu-id="33fc2-202">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="33fc2-203">**ОК** ("ОК")</span><span class="sxs-lookup"><span data-stu-id="33fc2-203">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="33fc2-204">**Ошибка** ("ошибка")</span><span class="sxs-lookup"><span data-stu-id="33fc2-204">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="33fc2-205">**Пониженная работоспособность** (пониженная работоспособность)</span><span class="sxs-lookup"><span data-stu-id="33fc2-205">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="33fc2-206">**Неизвестно** ("неизвестно")</span><span class="sxs-lookup"><span data-stu-id="33fc2-206">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="33fc2-207">**Пред-ошибка** ("пред Fail")</span><span class="sxs-lookup"><span data-stu-id="33fc2-207">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="33fc2-208">**Запуск** ("Запуск")</span><span class="sxs-lookup"><span data-stu-id="33fc2-208">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="33fc2-209">**Остановка** ("остановка")</span><span class="sxs-lookup"><span data-stu-id="33fc2-209">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="33fc2-210">**Служба** ("служба")</span><span class="sxs-lookup"><span data-stu-id="33fc2-210">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="33fc2-211">**Пренапряжению** ("напряжению")</span><span class="sxs-lookup"><span data-stu-id="33fc2-211">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="33fc2-212">**Невосстановление** ("невосстановление")</span><span class="sxs-lookup"><span data-stu-id="33fc2-212">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="33fc2-213">**Нет контакта** ("нет контакта")</span><span class="sxs-lookup"><span data-stu-id="33fc2-213">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="33fc2-214">**Потеря** связи ("потеря связи")</span><span class="sxs-lookup"><span data-stu-id="33fc2-214">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="33fc2-215">**суппортсброадкастинг**</span><span class="sxs-lookup"><span data-stu-id="33fc2-215">**SupportsBroadcasting**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="33fc2-216">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="33fc2-216">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="33fc2-217">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="33fc2-217">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="33fc2-218">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("платформа Win32 \_ API \| Windows \| \_ сведения о протоколе \| двсервицефлагс \| XP \_ поддерживает \_ трансляцию")</span><span class="sxs-lookup"><span data-stu-id="33fc2-218">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32\_API\|Windows Sockets Structures\|PROTOCOL\_INFO\|dwServiceFlags\|XP\_SUPPORTS\_BROADCAST")</span></span>
</dt> </dl>

<span data-ttu-id="33fc2-219">Протокол поддерживает механизм вещания сообщений по сети.</span><span class="sxs-lookup"><span data-stu-id="33fc2-219">Protocol supports a mechanism for broadcasting messages across the network.</span></span>

</dd> <dt>

<span data-ttu-id="33fc2-220">**суппортсконнектдата**</span><span class="sxs-lookup"><span data-stu-id="33fc2-220">**SupportsConnectData**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="33fc2-221">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="33fc2-221">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="33fc2-222">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="33fc2-222">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="33fc2-223">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("платформа Win32 \_ API \| Windows \| \_ сведения о протоколе \| двсервицефлагс \| XP \_ Connect \_ Data")</span><span class="sxs-lookup"><span data-stu-id="33fc2-223">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32\_API\|Windows Sockets Structures\|PROTOCOL\_INFO\|dwServiceFlags\|XP\_CONNECT\_DATA")</span></span>
</dt> </dl>

<span data-ttu-id="33fc2-224">Протокол позволяет подключать данные по сети.</span><span class="sxs-lookup"><span data-stu-id="33fc2-224">Protocol allows data to be connected across the network.</span></span>

</dd> <dt>

<span data-ttu-id="33fc2-225">**суппортсдисконнектдата**</span><span class="sxs-lookup"><span data-stu-id="33fc2-225">**SupportsDisconnectData**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="33fc2-226">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="33fc2-226">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="33fc2-227">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="33fc2-227">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="33fc2-228">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("платформа Win32 \_ API \| Windows \| \_ сведения о протоколе \| двсервицефлагс \| XP \_ Disconnect \_ Data")</span><span class="sxs-lookup"><span data-stu-id="33fc2-228">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32\_API\|Windows Sockets Structures\|PROTOCOL\_INFO\|dwServiceFlags\|XP\_DISCONNECT\_DATA")</span></span>
</dt> </dl>

<span data-ttu-id="33fc2-229">Протокол позволяет отключать данные по сети.</span><span class="sxs-lookup"><span data-stu-id="33fc2-229">Protocol allows data to be disconnected across the network.</span></span>

</dd> <dt>

<span data-ttu-id="33fc2-230">**суппортсенкриптион**</span><span class="sxs-lookup"><span data-stu-id="33fc2-230">**SupportsEncryption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="33fc2-231">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="33fc2-231">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="33fc2-232">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="33fc2-232">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="33fc2-233">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("платформа Win32 \_ API \| Windows: \| сведения о протоколе \_ \| двсервицефлагс \| XP \_ encrypted")</span><span class="sxs-lookup"><span data-stu-id="33fc2-233">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32\_API\|Windows Sockets Structures\|PROTOCOL\_INFO\|dwServiceFlags\|XP\_ENCRYPTS")</span></span>
</dt> </dl>

<span data-ttu-id="33fc2-234">Протокол поддерживает шифрование данных.</span><span class="sxs-lookup"><span data-stu-id="33fc2-234">Protocol supports data encryption.</span></span>

</dd> <dt>

<span data-ttu-id="33fc2-235">**суппортсекспедитеддата**</span><span class="sxs-lookup"><span data-stu-id="33fc2-235">**SupportsExpeditedData**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="33fc2-236">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="33fc2-236">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="33fc2-237">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="33fc2-237">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="33fc2-238">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("платформа Win32 \_ API \| Windows: \| сведения о протоколе двсервицефлагс, \_ \| \| \_ срочные \_ данные")</span><span class="sxs-lookup"><span data-stu-id="33fc2-238">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32\_API\|Windows Sockets Structures\|PROTOCOL\_INFO\|dwServiceFlags\|XP\_EXPEDITED\_DATA")</span></span>
</dt> </dl>

<span data-ttu-id="33fc2-239">Протокол поддерживает срочные данные (также называемые срочными данными) по сети.</span><span class="sxs-lookup"><span data-stu-id="33fc2-239">Protocol supports expedited data (also known as urgent data) across the network.</span></span> <span data-ttu-id="33fc2-240">Срочные данные могут обходить управление потоком и получить приоритет над обычными пакетами данных.</span><span class="sxs-lookup"><span data-stu-id="33fc2-240">Expedited data can bypass flow control and receive priority over normal data packets.</span></span>

</dd> <dt>

<span data-ttu-id="33fc2-241">**суппортсфрагментатион**</span><span class="sxs-lookup"><span data-stu-id="33fc2-241">**SupportsFragmentation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="33fc2-242">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="33fc2-242">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="33fc2-243">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="33fc2-243">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="33fc2-244">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("платформа Win32 \_ API \| Windows: \| сведения о протоколе \_ \| двсервицефлагс \| XP \_ ")</span><span class="sxs-lookup"><span data-stu-id="33fc2-244">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32\_API\|Windows Sockets Structures\|PROTOCOL\_INFO\|dwServiceFlags\|XP\_FRAGMENTATION")</span></span>
</dt> </dl>

<span data-ttu-id="33fc2-245">Протокол поддерживает передачу данных во фрагментах.</span><span class="sxs-lookup"><span data-stu-id="33fc2-245">Protocol supports transmitting the data in fragments.</span></span> <span data-ttu-id="33fc2-246">Максимальная физическая сеть (MTU) скрыта от приложений.</span><span class="sxs-lookup"><span data-stu-id="33fc2-246">Physical network maximum transfer unit (MTU) is hidden from applications.</span></span> <span data-ttu-id="33fc2-247">Для каждого типа носителя не может быть превышен максимальный размер кадра.</span><span class="sxs-lookup"><span data-stu-id="33fc2-247">Each media type has a maximum frame size that cannot be exceeded.</span></span> <span data-ttu-id="33fc2-248">Слой ссылок обнаруживает MTU и сообщает об используемых протоколах.</span><span class="sxs-lookup"><span data-stu-id="33fc2-248">The link layer discovers the MTU and reports it to the protocols used.</span></span>

</dd> <dt>

<span data-ttu-id="33fc2-249">**суппортсграцефулклосинг**</span><span class="sxs-lookup"><span data-stu-id="33fc2-249">**SupportsGracefulClosing**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="33fc2-250">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="33fc2-250">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="33fc2-251">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="33fc2-251">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="33fc2-252">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("платформа Win32 \_ API \| Windows \| \_ сведения о протоколе \| двсервицефлагс \| XP \_ \_ " — корректное закрытие ")</span><span class="sxs-lookup"><span data-stu-id="33fc2-252">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32\_API\|Windows Sockets Structures\|PROTOCOL\_INFO\|dwServiceFlags\|XP\_GRACEFUL\_CLOSE")</span></span>
</dt> </dl>

<span data-ttu-id="33fc2-253">Протокол поддерживает операции поэтапного закрытия, также называемые «операциями мягкого закрытия».</span><span class="sxs-lookup"><span data-stu-id="33fc2-253">Protocol supports two-phase close operations, also known as "graceful close operations".</span></span> <span data-ttu-id="33fc2-254">В противном случае протокол поддерживает только операции закрытия с прерываниями.</span><span class="sxs-lookup"><span data-stu-id="33fc2-254">If not, the protocol supports only abortive close operations.</span></span>

</dd> <dt>

<span data-ttu-id="33fc2-255">**суппортсгуарантидбандвидс**</span><span class="sxs-lookup"><span data-stu-id="33fc2-255">**SupportsGuaranteedBandwidth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="33fc2-256">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="33fc2-256">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="33fc2-257">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="33fc2-257">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="33fc2-258">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("платформа Win32 \_ API \| Windows: \| сведения о протоколе двсервицефлагс, \_ \| \| \_ распределение пропускной способности XP \_ ")</span><span class="sxs-lookup"><span data-stu-id="33fc2-258">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32\_API\|Windows Sockets Structures\|PROTOCOL\_INFO\|dwServiceFlags\|XP\_BANDWIDTH\_ALLOCATION")</span></span>
</dt> </dl>

<span data-ttu-id="33fc2-259">Протокол имеет механизм для установления и поддержания пропускной способности.</span><span class="sxs-lookup"><span data-stu-id="33fc2-259">Protocol has a mechanism to establish and maintain a bandwidth.</span></span>

</dd> <dt>

<span data-ttu-id="33fc2-260">**суппортсмултикастинг**</span><span class="sxs-lookup"><span data-stu-id="33fc2-260">**SupportsMulticasting**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="33fc2-261">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="33fc2-261">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="33fc2-262">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="33fc2-262">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="33fc2-263">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("платформа Win32 \_ API \| Windows \| \_ сведения о протоколе \| двсервицефлагс \| XP \_ поддерживает \_ многоадресную рассылку")</span><span class="sxs-lookup"><span data-stu-id="33fc2-263">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32\_API\|Windows Sockets Structures\|PROTOCOL\_INFO\|dwServiceFlags\|XP\_SUPPORTS\_MULTICAST")</span></span>
</dt> </dl>

<span data-ttu-id="33fc2-264">Протокол поддерживает многоадресную рассылку.</span><span class="sxs-lookup"><span data-stu-id="33fc2-264">Protocol supports multicasting.</span></span>

</dd> <dt>

<span data-ttu-id="33fc2-265">**суппортскуалитйофсервице**</span><span class="sxs-lookup"><span data-stu-id="33fc2-265">**SupportsQualityofService**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="33fc2-266">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="33fc2-266">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="33fc2-267">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="33fc2-267">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="33fc2-268">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32 \_ API \| Windows: структуры \| всапротокол \_ info \| dwServiceFlags1 \| XP1 \_ QoS \_ ")</span><span class="sxs-lookup"><span data-stu-id="33fc2-268">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32\_API\|Windows Sockets Structures\|WSAPROTOCOL\_INFO\|dwServiceFlags1\|XP1\_QOS\_SUPPORTED")</span></span>
</dt> </dl>

<span data-ttu-id="33fc2-269">Протокол поддерживает качество обслуживания (QoS) в базовом поставщике многоуровневой службы или транспортном перевозчике.</span><span class="sxs-lookup"><span data-stu-id="33fc2-269">Protocol is capable of Quality of Service (QoS) support by the underlying layered service provider or transport carrier.</span></span> <span data-ttu-id="33fc2-270">Качество обслуживания — это набор компонентов, которые позволяют различать и сохранятся подмножества данных, передаваемых по сети.</span><span class="sxs-lookup"><span data-stu-id="33fc2-270">QoS is a collection of components that enable differentiation and preferential treatment for subsets of data transmitted over the network.</span></span> <span data-ttu-id="33fc2-271">Качество обслуживания означает, что подмножества данных получают более высокий приоритет или гарантированную службу при прохождении по сети.</span><span class="sxs-lookup"><span data-stu-id="33fc2-271">QoS means subsets of data get higher priority or guaranteed service when traversing a network.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="33fc2-272">Комментарии</span><span class="sxs-lookup"><span data-stu-id="33fc2-272">Remarks</span></span>

<span data-ttu-id="33fc2-273">Класс **Win32 \_ NetworkProtocol** является производным от [**CIM \_ логикалелемент**](cim-logicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="33fc2-273">The **Win32\_NetworkProtocol** class is derived from [**CIM\_LogicalElement**](cim-logicalelement.md).</span></span>

## <a name="examples"></a><span data-ttu-id="33fc2-274">Примеры</span><span class="sxs-lookup"><span data-stu-id="33fc2-274">Examples</span></span>

<span data-ttu-id="33fc2-275">В следующем примере кода VBScript показано, как получить список выполняющихся служб из экземпляров **Win32 \_ NetworkProtocol**.</span><span class="sxs-lookup"><span data-stu-id="33fc2-275">The following VBScript code sample demonstrates how to retrieve a list of running services from instances of **Win32\_NetworkProtocol**.</span></span>


```VB
Set ProtocolSet = GetObject("winmgmts:").ExecQuery("select * from Win32_NetworkProtocol")

for each Protocol in ProtocolSet
 WScript.Echo Protocol.Name
next
```



<span data-ttu-id="33fc2-276">В следующем образце кода Perl показано, как получить список выполняющихся служб из экземпляров **Win32 \_ NetworkProtocol**.</span><span class="sxs-lookup"><span data-stu-id="33fc2-276">The following Perl code sample demonstrates how to retrieve a list of running services from instances of **Win32\_NetworkProtocol**.</span></span>


```
use strict;
use Win32::OLE;

my ( $ProtocolSet, $Protocol );

eval { $ProtocolSet = Win32::OLE->GetObject("winmgmts:{impersonationLevel=impersonate}!\\\\.\\root\\cimv2")->
 ExecQuery("SELECT * FROM Win32_NetworkProtocol"); };
unless($@)
{
 print "\n";
 foreach $Protocol (in $ProtocolSet) 
 {
  print $Protocol->{Name}, "\n";
 }
}
else
{
 print STDERR Win32::OLE->LastError, "\n";
}
```



## <a name="requirements"></a><span data-ttu-id="33fc2-277">Требования</span><span class="sxs-lookup"><span data-stu-id="33fc2-277">Requirements</span></span>



| <span data-ttu-id="33fc2-278">Требование</span><span class="sxs-lookup"><span data-stu-id="33fc2-278">Requirement</span></span> | <span data-ttu-id="33fc2-279">Значение</span><span class="sxs-lookup"><span data-stu-id="33fc2-279">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="33fc2-280">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="33fc2-280">Minimum supported client</span></span><br/> | <span data-ttu-id="33fc2-281">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="33fc2-281">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="33fc2-282">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="33fc2-282">Minimum supported server</span></span><br/> | <span data-ttu-id="33fc2-283">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="33fc2-283">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="33fc2-284">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="33fc2-284">Namespace</span></span><br/>                | <span data-ttu-id="33fc2-285">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="33fc2-285">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="33fc2-286">MOF</span><span class="sxs-lookup"><span data-stu-id="33fc2-286">MOF</span></span><br/>                      | <dl> <span data-ttu-id="33fc2-287"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="33fc2-287"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="33fc2-288">DLL</span><span class="sxs-lookup"><span data-stu-id="33fc2-288">DLL</span></span><br/>                      | <dl> <span data-ttu-id="33fc2-289"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="33fc2-289"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="33fc2-290">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="33fc2-290">See also</span></span>

<dl> <dt>

[<span data-ttu-id="33fc2-291">**\_ЛОГИКАЛЕЛЕМЕНТ CIM**</span><span class="sxs-lookup"><span data-stu-id="33fc2-291">**CIM\_LogicalElement**</span></span>](cim-logicalelement.md)
</dt> <dt>

[<span data-ttu-id="33fc2-292">Классы операционной системы</span><span class="sxs-lookup"><span data-stu-id="33fc2-292">Operating System Classes</span></span>](./operating-system-classes.md)
</dt> </dl>

 

 
