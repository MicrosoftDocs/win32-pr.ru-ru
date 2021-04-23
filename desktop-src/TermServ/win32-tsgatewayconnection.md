---
title: Класс Win32_TSGatewayConnection
description: Представляет подключение от клиентского компьютера к серверу шлюза удаленный рабочий стол (шлюз удаленных рабочих столов).
ms.assetid: 6e76ae25-409d-436a-8eef-8f047194c29c
ms.tgt_platform: multiple
keywords:
- Класс Win32_TSGatewayConnection службы удаленных рабочих столов
- Службы удаленных рабочих столов класса Win32_TSGatewayConnection, описание
topic_type:
- apiref
api_name:
- Win32_TSGatewayConnection
- Win32_TSGatewayConnection.ConnectionKey
- Win32_TSGatewayConnection.TunnelId
- Win32_TSGatewayConnection.ChannelId
- Win32_TSGatewayConnection.UserName
- Win32_TSGatewayConnection.FullUserName
- Win32_TSGatewayConnection.ClientAddress
- Win32_TSGatewayConnection.ConnectedTime
- Win32_TSGatewayConnection.IdleTime
- Win32_TSGatewayConnection.ConnectedResource
- Win32_TSGatewayConnection.ProtocolName
- Win32_TSGatewayConnection.ConnectedPort
- Win32_TSGatewayConnection.NumberOfKilobytesSent
- Win32_TSGatewayConnection.NumberOfKilobytesReceived
- Win32_TSGatewayConnection.ConnectionDuration
- Win32_TSGatewayConnection.TransportProtocol
api_location:
- AagWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6dbaa79213282a70b2f29e6bee9f94901700dddf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104137334"
---
# <a name="win32_tsgatewayconnection-class"></a><span data-ttu-id="02dee-105">\_Класс Win32 тсгатевайконнектион</span><span class="sxs-lookup"><span data-stu-id="02dee-105">Win32\_TSGatewayConnection class</span></span>

<span data-ttu-id="02dee-106">Представляет подключение от клиентского компьютера к серверу шлюза удаленный рабочий стол (шлюз удаленных рабочих столов).</span><span class="sxs-lookup"><span data-stu-id="02dee-106">Represents a connection from a client computer to a Remote Desktop Gateway (RD Gateway) server.</span></span>

## <a name="syntax"></a><span data-ttu-id="02dee-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="02dee-107">Syntax</span></span>

``` syntax
[dynamic, provider("AAGProvider"), AMENDMENT]
class Win32_TSGatewayConnection
{
  string ConnectionKey;
  uint64 TunnelId;
  uint32 ChannelId;
  string UserName;
  string FullUserName;
  string ClientAddress;
  string ConnectedTime;
  string IdleTime;
  string ConnectedResource;
  string ProtocolName;
  uint32 ConnectedPort;
  uint64 NumberOfKilobytesSent;
  uint64 NumberOfKilobytesReceived;
  string ConnectionDuration;
  uint32 TransportProtocol;
};
```

## <a name="members"></a><span data-ttu-id="02dee-108">Члены</span><span class="sxs-lookup"><span data-stu-id="02dee-108">Members</span></span>

<span data-ttu-id="02dee-109">Класс **Win32 \_ тсгатевайконнектион** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="02dee-109">The **Win32\_TSGatewayConnection** class has these types of members:</span></span>

-   [<span data-ttu-id="02dee-110">Методы</span><span class="sxs-lookup"><span data-stu-id="02dee-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="02dee-111">Свойства</span><span class="sxs-lookup"><span data-stu-id="02dee-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="02dee-112">Методы</span><span class="sxs-lookup"><span data-stu-id="02dee-112">Methods</span></span>

<span data-ttu-id="02dee-113">Класс **Win32 \_ тсгатевайконнектион** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="02dee-113">The **Win32\_TSGatewayConnection** class has these methods.</span></span>



| <span data-ttu-id="02dee-114">Метод</span><span class="sxs-lookup"><span data-stu-id="02dee-114">Method</span></span>                                                                     | <span data-ttu-id="02dee-115">Описание</span><span class="sxs-lookup"><span data-stu-id="02dee-115">Description</span></span>                                                                                                                      |
|:---------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="02dee-116">**CheckStatus**</span><span class="sxs-lookup"><span data-stu-id="02dee-116">**CheckStatus**</span></span>](checkstatus-win32-tsgatewayconnection.md)               | <span data-ttu-id="02dee-117">Проверяет состояние подключения к серверу шлюза удаленных рабочих столов и указывает, настроен ли целевой сервер для балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="02dee-117">Checks the status of an RD Gateway server connection, and whether the target server is configured for load balancing.</span></span><br/> |
| [<span data-ttu-id="02dee-118">**Отключение**</span><span class="sxs-lookup"><span data-stu-id="02dee-118">**Disconnect**</span></span>](disconnect-win32-tsgatewayconnection.md)                 | <span data-ttu-id="02dee-119">Завершает соединение.</span><span class="sxs-lookup"><span data-stu-id="02dee-119">Ends the connection.</span></span><br/>                                                                                                  |
| [<span data-ttu-id="02dee-120">**дисконнектпротокол**</span><span class="sxs-lookup"><span data-stu-id="02dee-120">**DisconnectProtocol**</span></span>](disconnectprotocol-win32-tsgatewayconnection.md) | <span data-ttu-id="02dee-121">Завершает все соединения, использующие указанный протокол.</span><span class="sxs-lookup"><span data-stu-id="02dee-121">Ends all connections that use the specified protocol.</span></span><br/>                                                                 |
| [<span data-ttu-id="02dee-122">**дисконнектусер**</span><span class="sxs-lookup"><span data-stu-id="02dee-122">**DisconnectUser**</span></span>](disconnectuser-win32-tsgatewayconnection.md)         | <span data-ttu-id="02dee-123">Завершает все соединения указанного пользователя.</span><span class="sxs-lookup"><span data-stu-id="02dee-123">Ends all connections of the specified user.</span></span><br/>                                                                           |



 

### <a name="properties"></a><span data-ttu-id="02dee-124">Свойства</span><span class="sxs-lookup"><span data-stu-id="02dee-124">Properties</span></span>

<span data-ttu-id="02dee-125">Класс **Win32 \_ тсгатевайконнектион** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="02dee-125">The **Win32\_TSGatewayConnection** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="02dee-126">**ChannelId**</span><span class="sxs-lookup"><span data-stu-id="02dee-126">**ChannelId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="02dee-127">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="02dee-127">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="02dee-128">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="02dee-128">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="02dee-129">Идентификатор канала.</span><span class="sxs-lookup"><span data-stu-id="02dee-129">Channel identifier.</span></span>

</dd> <dt>

<span data-ttu-id="02dee-130">**клиентаддресс**</span><span class="sxs-lookup"><span data-stu-id="02dee-130">**ClientAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="02dee-131">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="02dee-131">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="02dee-132">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="02dee-132">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="02dee-133">IP-адрес клиента.</span><span class="sxs-lookup"><span data-stu-id="02dee-133">Client IP address.</span></span>

</dd> <dt>

<span data-ttu-id="02dee-134">**коннектедпорт**</span><span class="sxs-lookup"><span data-stu-id="02dee-134">**ConnectedPort**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="02dee-135">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="02dee-135">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="02dee-136">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="02dee-136">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="02dee-137">Порт подключенного ресурса, к которому подключен пользователь.</span><span class="sxs-lookup"><span data-stu-id="02dee-137">Port on the connected resource to which the user is connected.</span></span>

</dd> <dt>

<span data-ttu-id="02dee-138">**коннектедресаурце**</span><span class="sxs-lookup"><span data-stu-id="02dee-138">**ConnectedResource**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="02dee-139">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="02dee-139">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="02dee-140">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="02dee-140">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="02dee-141">Имя компьютера (или кластера), к которому подключен клиент.</span><span class="sxs-lookup"><span data-stu-id="02dee-141">Name of the computer (or cluster) to which the client is connected.</span></span>

</dd> <dt>

<span data-ttu-id="02dee-142">**коннектедтиме**</span><span class="sxs-lookup"><span data-stu-id="02dee-142">**ConnectedTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="02dee-143">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="02dee-143">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="02dee-144">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="02dee-144">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="02dee-145">Метка времени, когда было установлено соединение.</span><span class="sxs-lookup"><span data-stu-id="02dee-145">The time stamp for when the connection was established.</span></span> <span data-ttu-id="02dee-146">Это время сбрасывается при сбросе соединения, даже если оно автоматически повторно подключено.</span><span class="sxs-lookup"><span data-stu-id="02dee-146">This time is reset when the connection is reset, even if it is automatically reconnected.</span></span>

</dd> <dt>

<span data-ttu-id="02dee-147">**коннектиондуратион**</span><span class="sxs-lookup"><span data-stu-id="02dee-147">**ConnectionDuration**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="02dee-148">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="02dee-148">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="02dee-149">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="02dee-149">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="02dee-150">Время, истекшее с момента времени подключения.</span><span class="sxs-lookup"><span data-stu-id="02dee-150">The time that has elapsed since the connected time.</span></span>

</dd> <dt>

<span data-ttu-id="02dee-151">**коннектионкэй**</span><span class="sxs-lookup"><span data-stu-id="02dee-151">**ConnectionKey**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="02dee-152">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="02dee-152">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="02dee-153">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="02dee-153">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="02dee-154">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="02dee-154">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="02dee-155">Идентификатор соединения в формате "Туннелид: channelID".</span><span class="sxs-lookup"><span data-stu-id="02dee-155">Connection identifier in the format "tunnelId:channelID".</span></span>

</dd> <dt>

<span data-ttu-id="02dee-156">**фуллусернаме**</span><span class="sxs-lookup"><span data-stu-id="02dee-156">**FullUserName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="02dee-157">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="02dee-157">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="02dee-158">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="02dee-158">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="02dee-159">Полное имя пользователя подключенного пользователя.</span><span class="sxs-lookup"><span data-stu-id="02dee-159">Full user name of the connected user.</span></span>

</dd> <dt>

<span data-ttu-id="02dee-160">**идлетиме**</span><span class="sxs-lookup"><span data-stu-id="02dee-160">**IdleTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="02dee-161">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="02dee-161">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="02dee-162">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="02dee-162">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="02dee-163">Время простоя соединения.</span><span class="sxs-lookup"><span data-stu-id="02dee-163">Idle time of the connection.</span></span>

</dd> <dt>

<span data-ttu-id="02dee-164">**нумберофкилобитесрецеивед**</span><span class="sxs-lookup"><span data-stu-id="02dee-164">**NumberOfKilobytesReceived**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="02dee-165">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="02dee-165">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="02dee-166">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="02dee-166">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="02dee-167">Число килобайт, полученных с клиентского компьютера сервером шлюза удаленных рабочих столов.</span><span class="sxs-lookup"><span data-stu-id="02dee-167">Number of kilobytes received from the client computer by the RD Gateway server.</span></span>

</dd> <dt>

<span data-ttu-id="02dee-168">**нумберофкилобитессент**</span><span class="sxs-lookup"><span data-stu-id="02dee-168">**NumberOfKilobytesSent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="02dee-169">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="02dee-169">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="02dee-170">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="02dee-170">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="02dee-171">Число килобайт, отправленных на клиентский компьютер сервером шлюза удаленных рабочих столов.</span><span class="sxs-lookup"><span data-stu-id="02dee-171">Number of kilobytes sent to the client computer by the RD Gateway server.</span></span>

</dd> <dt>

<span data-ttu-id="02dee-172">**ProtocolName**</span><span class="sxs-lookup"><span data-stu-id="02dee-172">**ProtocolName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="02dee-173">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="02dee-173">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="02dee-174">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="02dee-174">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="02dee-175">Протокол, используемый для подключения к серверу шлюза удаленных рабочих столов.</span><span class="sxs-lookup"><span data-stu-id="02dee-175">Protocol that is used to connect to the RD Gateway server.</span></span>

<dt>

<span data-ttu-id="02dee-176">RDP</span><span class="sxs-lookup"><span data-stu-id="02dee-176">"RDP"</span></span>
</dt> <dd>

<span data-ttu-id="02dee-177">Протокол для сервера шлюза удаленных рабочих столов.</span><span class="sxs-lookup"><span data-stu-id="02dee-177">The protocol for the RD Gateway server.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="02dee-178">**транспортпротокол**</span><span class="sxs-lookup"><span data-stu-id="02dee-178">**TransportProtocol**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="02dee-179">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="02dee-179">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="02dee-180">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="02dee-180">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="02dee-181">Указывает тип транспорта для соединения.</span><span class="sxs-lookup"><span data-stu-id="02dee-181">Specifies the transport type for the connection.</span></span> <span data-ttu-id="02dee-182">Это должно быть одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="02dee-182">This must be one of the following values.</span></span>

<dt>

<span data-ttu-id="02dee-183">0</span><span class="sxs-lookup"><span data-stu-id="02dee-183">0</span></span>
</dt> <dd>

<span data-ttu-id="02dee-184">Транспорт RPC через HTTP.</span><span class="sxs-lookup"><span data-stu-id="02dee-184">RPC over HTTP transport.</span></span>

</dd> <dt>

<span data-ttu-id="02dee-185">1</span><span class="sxs-lookup"><span data-stu-id="02dee-185">1</span></span>
</dt> <dd>

<span data-ttu-id="02dee-186">Транспорт HTTP.</span><span class="sxs-lookup"><span data-stu-id="02dee-186">HTTP transport.</span></span>

</dd> <dt>

<span data-ttu-id="02dee-187">2</span><span class="sxs-lookup"><span data-stu-id="02dee-187">2</span></span>
</dt> <dd>

<span data-ttu-id="02dee-188">Транспорт UDP.</span><span class="sxs-lookup"><span data-stu-id="02dee-188">UDP transport.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="02dee-189">**туннелид**</span><span class="sxs-lookup"><span data-stu-id="02dee-189">**TunnelId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="02dee-190">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="02dee-190">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="02dee-191">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="02dee-191">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="02dee-192">Идентификатор туннеля.</span><span class="sxs-lookup"><span data-stu-id="02dee-192">Tunnel identifier.</span></span>

</dd> <dt>

<span data-ttu-id="02dee-193">**UserName**</span><span class="sxs-lookup"><span data-stu-id="02dee-193">**UserName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="02dee-194">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="02dee-194">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="02dee-195">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="02dee-195">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="02dee-196">Имя пользователя, подключенное к серверу шлюза удаленных рабочих столов.</span><span class="sxs-lookup"><span data-stu-id="02dee-196">User name connected to the RD Gateway server.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="02dee-197">Комментарии</span><span class="sxs-lookup"><span data-stu-id="02dee-197">Remarks</span></span>

<span data-ttu-id="02dee-198">Для использования этого класса необходимо быть членом группы администраторов.</span><span class="sxs-lookup"><span data-stu-id="02dee-198">You must be a member of the Administrators group to use this class.</span></span>

<span data-ttu-id="02dee-199">Файлы MOF-файл (MOF) содержат определения для классов инструментарий управления Windows (WMI) (WMI).</span><span class="sxs-lookup"><span data-stu-id="02dee-199">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="02dee-200">MOF-файлы не устанавливаются в составе пакета средств разработки программного обеспечения Microsoft Windows (SDK).</span><span class="sxs-lookup"><span data-stu-id="02dee-200">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="02dee-201">Они устанавливаются на сервере при добавлении связанной роли с помощью диспетчер сервера.</span><span class="sxs-lookup"><span data-stu-id="02dee-201">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="02dee-202">Дополнительные сведения о файлах MOF см. в разделе [MOF-файл (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="02dee-202">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="02dee-203">Требования</span><span class="sxs-lookup"><span data-stu-id="02dee-203">Requirements</span></span>



| <span data-ttu-id="02dee-204">Требование</span><span class="sxs-lookup"><span data-stu-id="02dee-204">Requirement</span></span> | <span data-ttu-id="02dee-205">Значение</span><span class="sxs-lookup"><span data-stu-id="02dee-205">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="02dee-206">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="02dee-206">Minimum supported client</span></span><br/> | <span data-ttu-id="02dee-207">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="02dee-207">None supported</span></span><br/>                                                                |
| <span data-ttu-id="02dee-208">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="02dee-208">Minimum supported server</span></span><br/> | <span data-ttu-id="02dee-209">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="02dee-209">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="02dee-210">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="02dee-210">Namespace</span></span><br/>                | <span data-ttu-id="02dee-211">Корневой \\ CIMv2 \\ терминалсервицес</span><span class="sxs-lookup"><span data-stu-id="02dee-211">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="02dee-212">MOF</span><span class="sxs-lookup"><span data-stu-id="02dee-212">MOF</span></span><br/>                      | <dl> <span data-ttu-id="02dee-213"><dt>TSGateway. mof</dt></span><span class="sxs-lookup"><span data-stu-id="02dee-213"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="02dee-214">DLL</span><span class="sxs-lookup"><span data-stu-id="02dee-214">DLL</span></span><br/>                      | <dl> <span data-ttu-id="02dee-215"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="02dee-215"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="02dee-216">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="02dee-216">See also</span></span>

<dl> <dt>

[<span data-ttu-id="02dee-217">**\_Тсгатевайконнектионаусоризатионполици Win32**</span><span class="sxs-lookup"><span data-stu-id="02dee-217">**Win32\_TSGatewayConnectionAuthorizationPolicy**</span></span>](win32-tsgatewayconnectionauthorizationpolicy.md)
</dt> <dt>

[<span data-ttu-id="02dee-218">**\_Тсгатевайлоадбаланцер Win32**</span><span class="sxs-lookup"><span data-stu-id="02dee-218">**Win32\_TSGatewayLoadBalancer**</span></span>](win32-tsgatewayloadbalancer.md)
</dt> <dt>

[<span data-ttu-id="02dee-219">**\_Тсгатевайрадиуссервер Win32**</span><span class="sxs-lookup"><span data-stu-id="02dee-219">**Win32\_TSGatewayRADIUSServer**</span></span>](win32-tsgatewayradiusserver.md)
</dt> <dt>

[<span data-ttu-id="02dee-220">**\_Тсгатевайресаурцеаусоризатионполици Win32**</span><span class="sxs-lookup"><span data-stu-id="02dee-220">**Win32\_TSGatewayResourceAuthorizationPolicy**</span></span>](win32-tsgatewayresourceauthorizationpolicy.md)
</dt> <dt>

[<span data-ttu-id="02dee-221">**\_Тсгатевайресаурцеграуп Win32**</span><span class="sxs-lookup"><span data-stu-id="02dee-221">**Win32\_TSGatewayResourceGroup**</span></span>](win32-tsgatewayresourcegroup.md)
</dt> <dt>

[<span data-ttu-id="02dee-222">**\_Тсгатевайсерверсеттингс Win32**</span><span class="sxs-lookup"><span data-stu-id="02dee-222">**Win32\_TSGatewayServerSettings**</span></span>](win32-tsgatewayserversettings.md)
</dt> </dl>

 

