---
title: Структура RAS_PORT_0 (Рассапи. h)
description: '\_Структура порта RAS \_ 0 содержит сведения, описывающие порт RAS.'
ms.assetid: 750fc705-0770-427b-b7d6-7876b8b9118a
keywords:
- RAS структуры RAS_PORT_0
- RAS — указатель структуры PRAS_PORT_0
topic_type:
- apiref
api_name:
- RAS_PORT_0
api_location:
- Rassapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 80d66725415d86aea44138f23fb3748e3187820f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104534268"
---
# <a name="ras_port_0-structure"></a><span data-ttu-id="f6c38-105">\_Структура порта \_ 0 RAS</span><span class="sxs-lookup"><span data-stu-id="f6c38-105">RAS\_PORT\_0 structure</span></span>

<span data-ttu-id="f6c38-106">\[Эта версия структуры **порта RAS \_ \_ 0** не поддерживается в Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="f6c38-106">\[This version of the **RAS\_PORT\_0** structure is not supported as of Windows Vista.</span></span> <span data-ttu-id="f6c38-107">Используйте более новый [**\_ порт RAS \_ 0**](/windows/desktop/api/Mprapi/ns-mprapi-ras_port_0) , определенный в мпрапи. h.\]</span><span class="sxs-lookup"><span data-stu-id="f6c38-107">Use the newer [**RAS\_PORT\_0**](/windows/desktop/api/Mprapi/ns-mprapi-ras_port_0) defined in mprapi.h instead.\]</span></span>

<span data-ttu-id="f6c38-108">Структура **\_ порта RAS \_ 0** содержит сведения, описывающие порт RAS.</span><span class="sxs-lookup"><span data-stu-id="f6c38-108">The **RAS\_PORT\_0** structure contains information that describes a RAS port.</span></span>

## <a name="syntax"></a><span data-ttu-id="f6c38-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f6c38-109">Syntax</span></span>


```C++
typedef struct _RAS_PORT_0 {
  WCHAR wszPortName[RASSAPI_MAX_PORT_NAME];
  WCHAR wszDeviceType[RASSAPI_MAX_DEVICETYPE_NAME];
  WCHAR wszDeviceName[RASSAPI_MAX_DEVICE_NAME];
  WCHAR wszMediaName[RASSAPI_MAX_MEDIA_NAME];
  DWORD reserved;
  DWORD Flags;
  WCHAR wszUserName[UNLEN + 1];
  WCHAR wszComputer[NETBIOS_NAME_LEN];
  DWORD dwStartSessionTime;
  WCHAR wszLogonDomain[DNLEN + 1];
  BOOL  fAdvancedServer;
} RAS_PORT_0, *PRAS_PORT_0;
```



## <a name="members"></a><span data-ttu-id="f6c38-110">Члены</span><span class="sxs-lookup"><span data-stu-id="f6c38-110">Members</span></span>

<dl> <dt>

<span data-ttu-id="f6c38-111">**всзпортнаме**</span><span class="sxs-lookup"><span data-stu-id="f6c38-111">**wszPortName**</span></span>
</dt> <dd>

<span data-ttu-id="f6c38-112">Строка в Юникоде, заканчивающаяся нулем и указывающая имя порта, например COM1.</span><span class="sxs-lookup"><span data-stu-id="f6c38-112">A null-terminated Unicode string that specifies the name of the port, such as "COM1".</span></span>

</dd> <dt>

<span data-ttu-id="f6c38-113">**всздевицетипе**</span><span class="sxs-lookup"><span data-stu-id="f6c38-113">**wszDeviceType**</span></span>
</dt> <dd>

<span data-ttu-id="f6c38-114">Строка в Юникоде, заканчивающаяся нулем и указывающая тип устройства, на котором установлено соединение, например модем или ISDN.</span><span class="sxs-lookup"><span data-stu-id="f6c38-114">A null-terminated Unicode string that specifies the type of the device on which the connection was made, such as Modem or ISDN.</span></span> <span data-ttu-id="f6c38-115">Список типов устройств, которые могут быть указаны в этом члене, включает в себя все типы устройств, установленные на сервере, включая устройства сторонних производителей.</span><span class="sxs-lookup"><span data-stu-id="f6c38-115">The list of device types that might be specified in this member includes all the device types installed on the server, including third-party devices.</span></span>

</dd> <dt>

<span data-ttu-id="f6c38-116">**всздевиценаме**</span><span class="sxs-lookup"><span data-stu-id="f6c38-116">**wszDeviceName**</span></span>
</dt> <dd>

<span data-ttu-id="f6c38-117">Строка в Юникоде, заканчивающаяся нулем и указывающая имя устройства, на котором установлено соединение, например "Hayes 9600" или "PCIMACISDN1".</span><span class="sxs-lookup"><span data-stu-id="f6c38-117">A null-terminated Unicode string that specifies the name of the device on which the connection was made, such as "Hayes 9600" or "PCIMACISDN1".</span></span>

</dd> <dt>

<span data-ttu-id="f6c38-118">**всзмедианаме**</span><span class="sxs-lookup"><span data-stu-id="f6c38-118">**wszMediaName**</span></span>
</dt> <dd>

<span data-ttu-id="f6c38-119">Указывает строку в Юникоде, завершающуюся нулем, которая указывает имя носителя, используемого для соединения, например *рассер* или *растапи*.</span><span class="sxs-lookup"><span data-stu-id="f6c38-119">Specifies a null-terminated Unicode string that specifies the name of the media used for the connection, such as *rasser* or *rastapi*.</span></span>

</dd> <dt>

<span data-ttu-id="f6c38-120">**процессу**</span><span class="sxs-lookup"><span data-stu-id="f6c38-120">**reserved**</span></span>
</dt> <dd>

<span data-ttu-id="f6c38-121">Зарезервировано.</span><span class="sxs-lookup"><span data-stu-id="f6c38-121">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="f6c38-122">**Флаги**</span><span class="sxs-lookup"><span data-stu-id="f6c38-122">**Flags**</span></span>
</dt> <dd>

<span data-ttu-id="f6c38-123">Задает набор битовых флагов, указывающих характер соединения, установленного на этом порту.</span><span class="sxs-lookup"><span data-stu-id="f6c38-123">Specifies a set of bit flags that specify the nature of the connection made on this port.</span></span> <span data-ttu-id="f6c38-124">Этот член может быть сочетанием следующих флагов.</span><span class="sxs-lookup"><span data-stu-id="f6c38-124">This member can be a combination of the following flags.</span></span>



| <span data-ttu-id="f6c38-125">Значение</span><span class="sxs-lookup"><span data-stu-id="f6c38-125">Value</span></span>                                                                                                                                                                        | <span data-ttu-id="f6c38-126">Значение</span><span class="sxs-lookup"><span data-stu-id="f6c38-126">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                    |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GATEWAY_ACTIVE"></span><span id="gateway_active"></span><dl> <span data-ttu-id="f6c38-127"><dt>**ШЛЮЗ \_ активен**</dt></span><span class="sxs-lookup"><span data-stu-id="f6c38-127"><dt>**GATEWAY\_ACTIVE**</dt></span></span> </dl>             | <span data-ttu-id="f6c38-128">Если этот флаг установлен, шлюз NetBIOS активен на сервере.</span><span class="sxs-lookup"><span data-stu-id="f6c38-128">If this flag is set, the NetBIOS gateway is active on the server.</span></span><br/>                                                                                                                                                                                                                                                                                                               |
| <span id="MESSENGER_PRESENT"></span><span id="messenger_present"></span><dl> <span data-ttu-id="f6c38-129"><dt>**имеется программа MESSENGER \_**</dt></span><span class="sxs-lookup"><span data-stu-id="f6c38-129"><dt>**MESSENGER\_PRESENT**</dt></span></span> </dl>    | <span data-ttu-id="f6c38-130">Если этот флаг установлен, служба сообщений запущена на удаленном клиенте.</span><span class="sxs-lookup"><span data-stu-id="f6c38-130">If this flag is set, the messenger service is running on the remote client.</span></span><br/>                                                                                                                                                                                                                                                                                                     |
| <span id="PORT_MULTILINKED"></span><span id="port_multilinked"></span><dl> <span data-ttu-id="f6c38-131"><dt>**\_МНОГОканальный порт**</dt></span><span class="sxs-lookup"><span data-stu-id="f6c38-131"><dt>**PORT\_MULTILINKED**</dt></span></span> </dl>       | <span data-ttu-id="f6c38-132">Если этот флаг установлен, порт будет многоканальным с другими портами.</span><span class="sxs-lookup"><span data-stu-id="f6c38-132">If this flag is set, the port is multilinked with other ports.</span></span> <span data-ttu-id="f6c38-133">Используйте эти сведения для вывода состояния подключения в виде многоканального порта.</span><span class="sxs-lookup"><span data-stu-id="f6c38-133">Use this information to display the connection status as a multilinked port.</span></span> <br/> <span data-ttu-id="f6c38-134">Для многоканального порта структура [**\_ \_ статистики порта RAS**](ras-port-statistics-str.md) содержит два набора статистических данных: один для порта и другой для Объединенных портов в многоканальном соединении.</span><span class="sxs-lookup"><span data-stu-id="f6c38-134">For a multilinked port, the [**RAS\_PORT\_STATISTICS**](ras-port-statistics-str.md) structure contains two sets of statistics: one for the port alone, and another for the combined ports in the multilink connection.</span></span><br/> |
| <span id="PPP_CLIENT"></span><span id="ppp_client"></span><dl> <span data-ttu-id="f6c38-135"><dt>**\_клиент PPP**</dt></span><span class="sxs-lookup"><span data-stu-id="f6c38-135"><dt>**PPP\_CLIENT**</dt></span></span> </dl>                         | <span data-ttu-id="f6c38-136">Если этот флаг установлен, удаленный клиент, подключенный по протоколу PPP.</span><span class="sxs-lookup"><span data-stu-id="f6c38-136">If this flag is set, the remote client connected using PPP.</span></span> <span data-ttu-id="f6c38-137">Если этот флаг не установлен, удаленный клиент, подключенный по протоколу АМБ.</span><span class="sxs-lookup"><span data-stu-id="f6c38-137">If this flag is not set, the remote client connected using the AMB protocol.</span></span><br/>                                                                                                                                                                                                                                        |
| <span id="REMOTE_LISTEN"></span><span id="remote_listen"></span><dl> <span data-ttu-id="f6c38-138"><dt>**УДАЛЕННЫЙ \_ прослушивание**</dt></span><span class="sxs-lookup"><span data-stu-id="f6c38-138"><dt>**REMOTE\_LISTEN**</dt></span></span> </dl>                | <span data-ttu-id="f6c38-139">Если этот флаг установлен, параметр Ремотелистен шлюза NetBIOS имеет значение 1 на сервере.</span><span class="sxs-lookup"><span data-stu-id="f6c38-139">If this flag is set, the RemoteListen parameter of the NetBIOS gateway is set to 1 on the server.</span></span><br/>                                                                                                                                                                                                                                                                               |
| <span id="USER_AUTHENTICATED"></span><span id="user_authenticated"></span><dl> <span data-ttu-id="f6c38-140"><dt>**ПОЛЬЗОВАТЕЛЬ \_ прошел проверку подлинности**</dt></span><span class="sxs-lookup"><span data-stu-id="f6c38-140"><dt>**USER\_AUTHENTICATED**</dt></span></span> </dl> | <span data-ttu-id="f6c38-141">Если этот флаг установлен, удаленный клиент подключается к серверу, и пользователь прошел проверку подлинности.</span><span class="sxs-lookup"><span data-stu-id="f6c38-141">If this flag is set, a remote client is connected to the server and the user has been authenticated.</span></span> <span data-ttu-id="f6c38-142">Установите этот флажок, чтобы убедиться, что клиент фактически подключен к порту.</span><span class="sxs-lookup"><span data-stu-id="f6c38-142">Check this flag to ensure that a client is actually connected to a port.</span></span><br/>                                                                                                                                                                                                   |



 

<span data-ttu-id="f6c38-143">Если \_ \_ установлены флаги Messenger, активный шлюз и удаленный режим \_ прослушивания, используйте службу сообщений для отправки административного сообщения удаленному клиенту.</span><span class="sxs-lookup"><span data-stu-id="f6c38-143">If the MESSENGER\_PRESENT, GATEWAY\_ACTIVE, and REMOTE\_LISTEN flags are set, use the messenger service to send an administrative message to the remote client.</span></span> <span data-ttu-id="f6c38-144">Если \_ \_ настроена программа Messenger и удаленный прослушивание, но шлюз \_ активен, отправка сообщений клиенту происходит только с сервера RAS, к которому подключен клиент.</span><span class="sxs-lookup"><span data-stu-id="f6c38-144">If MESSENGER\_PRESENT and REMOTE\_LISTEN are set, but GATEWAY\_ACTIVE is not, send messages to the client only from the RAS server to which the client is connected.</span></span>

</dd> <dt>

<span data-ttu-id="f6c38-145">**всзусернаме**</span><span class="sxs-lookup"><span data-stu-id="f6c38-145">**wszUserName**</span></span>
</dt> <dd>

<span data-ttu-id="f6c38-146">Строка в Юникоде, заканчивающаяся нулем и указывающая имя удаленного пользователя, подключенного к этому порту.</span><span class="sxs-lookup"><span data-stu-id="f6c38-146">A null-terminated Unicode string that specifies the name of the remote user connected to this port.</span></span>

</dd> <dt>

<span data-ttu-id="f6c38-147">**всзкомпутер**</span><span class="sxs-lookup"><span data-stu-id="f6c38-147">**wszComputer**</span></span>
</dt> <dd>

<span data-ttu-id="f6c38-148">Строка в Юникоде, заканчивающаяся нулем и указывающая имя удаленного клиентского компьютера.</span><span class="sxs-lookup"><span data-stu-id="f6c38-148">A null-terminated Unicode string that specifies the name of the remote client computer.</span></span>

</dd> <dt>

<span data-ttu-id="f6c38-149">**двстартсессионтиме**</span><span class="sxs-lookup"><span data-stu-id="f6c38-149">**dwStartSessionTime**</span></span>
</dt> <dd>

<span data-ttu-id="f6c38-150">Указывает время в секундах с 1 января 1970, которое клиент подключился к серверу RAS в этом порте.</span><span class="sxs-lookup"><span data-stu-id="f6c38-150">Specifies the time, in seconds from January 1, 1970, that the client connected to the RAS server on this port.</span></span> <span data-ttu-id="f6c38-151">Используйте стандартные функции времени, чтобы отформатировать это значение для вывода.</span><span class="sxs-lookup"><span data-stu-id="f6c38-151">Use the standard time functions to format this value for display.</span></span>

</dd> <dt>

<span data-ttu-id="f6c38-152">**всзлогондомаин**</span><span class="sxs-lookup"><span data-stu-id="f6c38-152">**wszLogonDomain**</span></span>
</dt> <dd>

<span data-ttu-id="f6c38-153">Указывает строку в Юникоде, завершающуюся нулем, которая указывает имя домена, в котором прошел проверку подлинности удаленного пользователя.</span><span class="sxs-lookup"><span data-stu-id="f6c38-153">Specifies a null-terminated Unicode string that specifies the name of the domain on which the remote user was authenticated.</span></span> <span data-ttu-id="f6c38-154">Эта строка является только доменным именем, без \\ \\ префикса "".</span><span class="sxs-lookup"><span data-stu-id="f6c38-154">This string is the domain name only, with no "\\\\" prefix.</span></span>

</dd> <dt>

<span data-ttu-id="f6c38-155">**фадванцедсервер**</span><span class="sxs-lookup"><span data-stu-id="f6c38-155">**fAdvancedServer**</span></span>
</dt> <dd>

<span data-ttu-id="f6c38-156">Указывает ненулевый флаг, если сервер RAS, связанный с этим портом, является дополнительным сервером, например Windows 2000 Advanced Server.</span><span class="sxs-lookup"><span data-stu-id="f6c38-156">Specifies a flag that is nonzero if the RAS server associated with this port is an advanced server such as Windows 2000 Advanced Server.</span></span> <span data-ttu-id="f6c38-157">Используйте эти сведения для определения имени сервера, на котором находится база данных учетных записей пользователей.</span><span class="sxs-lookup"><span data-stu-id="f6c38-157">Use this information to determine the name of the server that has the user account database.</span></span> <span data-ttu-id="f6c38-158">Если сервер RAS является дополнительным сервером, получите имя сервера учетных записей пользователей, объединив префикс " \\ \\ " с именем, возвращенным в члене **всзлогондомаин** .</span><span class="sxs-lookup"><span data-stu-id="f6c38-158">If the RAS server is an advanced server, get the name of the user account server by concatenating the prefix "\\\\" to the name returned in the **wszLogonDomain** member.</span></span> <span data-ttu-id="f6c38-159">Это связано с тем, что для расширенного сервера доменное имя локального входа совпадает с именем сервера.</span><span class="sxs-lookup"><span data-stu-id="f6c38-159">This is because for an advanced server the local logon domain name is the same as the server name.</span></span> <span data-ttu-id="f6c38-160">Если сервер удаленного доступа является рабочей станцией, используйте функцию [**расадминжетусераккаунтсервер**](rasadmingetuseraccountserver.md) , чтобы получить имя сервера учетных записей пользователей.</span><span class="sxs-lookup"><span data-stu-id="f6c38-160">If the RAS server is a workstation, use the [**RasAdminGetUserAccountServer**](rasadmingetuseraccountserver.md) function to get the name of the user account server.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="f6c38-161">Требования</span><span class="sxs-lookup"><span data-stu-id="f6c38-161">Requirements</span></span>



| <span data-ttu-id="f6c38-162">Требование</span><span class="sxs-lookup"><span data-stu-id="f6c38-162">Requirement</span></span> | <span data-ttu-id="f6c38-163">Значение</span><span class="sxs-lookup"><span data-stu-id="f6c38-163">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="f6c38-164">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="f6c38-164">Minimum supported client</span></span><br/> | <span data-ttu-id="f6c38-165">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="f6c38-165">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="f6c38-166">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="f6c38-166">Minimum supported server</span></span><br/> | <span data-ttu-id="f6c38-167">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="f6c38-167">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="f6c38-168">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="f6c38-168">End of client support</span></span><br/>    | <span data-ttu-id="f6c38-169">Windows XP</span><span class="sxs-lookup"><span data-stu-id="f6c38-169">Windows XP</span></span><br/>                                                                |
| <span data-ttu-id="f6c38-170">Поддержка конца сервера</span><span class="sxs-lookup"><span data-stu-id="f6c38-170">End of server support</span></span><br/>    | <span data-ttu-id="f6c38-171">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="f6c38-171">Windows Server 2003</span></span><br/>                                                       |
| <span data-ttu-id="f6c38-172">Header</span><span class="sxs-lookup"><span data-stu-id="f6c38-172">Header</span></span><br/>                   | <dl> <span data-ttu-id="f6c38-173"><dt>Рассапи. h</dt></span><span class="sxs-lookup"><span data-stu-id="f6c38-173"><dt>Rassapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f6c38-174">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f6c38-174">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f6c38-175">Обзор службы удаленного доступа (RAS)</span><span class="sxs-lookup"><span data-stu-id="f6c38-175">Remote Access Service (RAS) Overview</span></span>](about-remote-access-service.md)
</dt> <dt>

[<span data-ttu-id="f6c38-176">Структуры администрирования сервера RAS</span><span class="sxs-lookup"><span data-stu-id="f6c38-176">RAS Server Administration Structures</span></span>](ras-server-administration-structures.md)
</dt> <dt>

[<span data-ttu-id="f6c38-177">**\_Порт RAS \_ 1**</span><span class="sxs-lookup"><span data-stu-id="f6c38-177">**RAS\_PORT\_1**</span></span>](ras-port-1-str.md)
</dt> <dt>

[<span data-ttu-id="f6c38-178">**\_Статистика порта \_ RAS**</span><span class="sxs-lookup"><span data-stu-id="f6c38-178">**RAS\_PORT\_STATISTICS**</span></span>](ras-port-statistics-str.md)
</dt> <dt>

[<span data-ttu-id="f6c38-179">**расадминжетусераккаунтсервер**</span><span class="sxs-lookup"><span data-stu-id="f6c38-179">**RasAdminGetUserAccountServer**</span></span>](rasadmingetuseraccountserver.md)
</dt> <dt>

[<span data-ttu-id="f6c38-180">**расадминпортенум**</span><span class="sxs-lookup"><span data-stu-id="f6c38-180">**RasAdminPortEnum**</span></span>](rasadminportenum.md)
</dt> </dl>

 

 





