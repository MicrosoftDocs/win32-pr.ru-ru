---
title: Метод Update класса Win32_TSGatewayConnectionAuthorizationPolicy
description: Обновляет текущую политику авторизации подключений удаленный рабочий стол (RD \ 160; CAP).
ms.assetid: 6d13d1b7-1c7d-4d22-b42c-36e0f4446e86
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода обновления
- Метод Update службы удаленных рабочих столов, класс Win32_TSGatewayConnectionAuthorizationPolicy
- Класс Win32_TSGatewayConnectionAuthorizationPolicy службы удаленных рабочих столов, метод Update
topic_type:
- apiref
api_name:
- Win32_TSGatewayConnectionAuthorizationPolicy.Update
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 87b982030170e954342dc5ff99754dcb89afd0e3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071698"
---
# <a name="update-method-of-the-win32_tsgatewayconnectionauthorizationpolicy-class"></a><span data-ttu-id="6da8c-106">Метод Update \_ класса Win32 тсгатевайконнектионаусоризатионполици</span><span class="sxs-lookup"><span data-stu-id="6da8c-106">Update method of the Win32\_TSGatewayConnectionAuthorizationPolicy class</span></span>

<span data-ttu-id="6da8c-107">Обновляет текущую политику авторизации подключений удаленный рабочий стол.</span><span class="sxs-lookup"><span data-stu-id="6da8c-107">Updates the current Remote Desktop connection authorization policy (RD CAP).</span></span>

## <a name="syntax"></a><span data-ttu-id="6da8c-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="6da8c-108">Syntax</span></span>


```mof
uint32 Update(
  [in] string  Name,
  [in] string  UserGroupNames,
  [in] string  ComputerGroupNames,
  [in] boolean SmartCard,
  [in] boolean Password,
  [in] boolean SecureId,
  [in] boolean Enabled,
  [in] uint32  DeviceRedirectionType,
  [in] boolean DiskDrivesDisabled,
  [in] boolean PrintersDisabled,
  [in] boolean SerialPortsDisabled,
  [in] boolean ClipboardDisabled,
  [in] boolean PlugAndPlayDevicesDisabled,
  [in] uint32  IdleTimeout,
  [in] uint32  SessionTimeout,
  [in] uint32  SessionTimeoutAction,
  [in] boolean AllowOnlySDRServers,
  [in] boolean CookieAuthentication
);
```



## <a name="parameters"></a><span data-ttu-id="6da8c-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="6da8c-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6da8c-110">*Имя* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="6da8c-110">*Name* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6da8c-111">Имя политики авторизации подключений к удаленному рабочему столу.</span><span class="sxs-lookup"><span data-stu-id="6da8c-111">Name of the RD CAP.</span></span> <span data-ttu-id="6da8c-112">Имя должно содержать 64 символов или меньше, уникально (регистр игнорируется) и не может включать следующие зарезервированные символы:</span><span class="sxs-lookup"><span data-stu-id="6da8c-112">The name must be 64 characters or less, unique (case is ignored), and cannot contain the following reserved characters:</span></span>

<span data-ttu-id="6da8c-113"><> :; " / \\ \| ?</span><span class="sxs-lookup"><span data-stu-id="6da8c-113"><> : ; " / \\ \| ?</span></span> <span data-ttu-id="6da8c-114">\*\[Вкладка\]</span><span class="sxs-lookup"><span data-stu-id="6da8c-114">\* \[TAB\]</span></span>

</dd> <dt>

<span data-ttu-id="6da8c-115">*Усерграупнамес* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="6da8c-115">*UserGroupNames* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6da8c-116">Список имен групп пользователей, разделенных точкой с запятой.</span><span class="sxs-lookup"><span data-stu-id="6da8c-116">List of semicolon-separated user group names.</span></span> <span data-ttu-id="6da8c-117">Имена имеют формат *домена \\ усерграупнаме*.</span><span class="sxs-lookup"><span data-stu-id="6da8c-117">The names are of the format *Domain\\UserGroupName*.</span></span> <span data-ttu-id="6da8c-118">Если пользователь принадлежит к одной из этих групп пользователей, ему будет разрешен доступ к серверу шлюза удаленных рабочих столов.</span><span class="sxs-lookup"><span data-stu-id="6da8c-118">If the user belongs to any one of these user groups, the user will be permitted access to the RD Gateway server.</span></span>

</dd> <dt>

<span data-ttu-id="6da8c-119">*Компутерграупнамес* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="6da8c-119">*ComputerGroupNames* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6da8c-120">Список имен групп компьютеров, разделенных точкой с запятой.</span><span class="sxs-lookup"><span data-stu-id="6da8c-120">List of semicolon-separated machine group names.</span></span> <span data-ttu-id="6da8c-121">Это значение может быть пустым.</span><span class="sxs-lookup"><span data-stu-id="6da8c-121">This value can be empty.</span></span> <span data-ttu-id="6da8c-122">Имена имеют формат *домена \\ компутерграупнаме*.</span><span class="sxs-lookup"><span data-stu-id="6da8c-122">The names are of the format *Domain\\ComputerGroupName*.</span></span> <span data-ttu-id="6da8c-123">Если указано значение, клиентский компьютер должен принадлежать к одной из этих групп компьютеров, чтобы пользователь был доступен на сервере шлюза удаленных рабочих столов.</span><span class="sxs-lookup"><span data-stu-id="6da8c-123">If a value is specified, the client computer must belong to one of these computer groups for the user to access the RD Gateway server.</span></span>

</dd> <dt>

<span data-ttu-id="6da8c-124">*Смарт-карта* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="6da8c-124">*SmartCard* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6da8c-125">Указывает, можно ли использовать смарт-карты для проверки подлинности на сервере шлюза удаленных рабочих столов.</span><span class="sxs-lookup"><span data-stu-id="6da8c-125">Specifies whether smart cards can be used to authenticate with the RD Gateway server.</span></span>

</dd> <dt>

<span data-ttu-id="6da8c-126">*Пароль* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="6da8c-126">*Password* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6da8c-127">Указывает, можно ли использовать пароли для проверки подлинности на сервере шлюза удаленных рабочих столов.</span><span class="sxs-lookup"><span data-stu-id="6da8c-127">Specifies whether passwords can be used to authenticate with the RD Gateway server.</span></span>

</dd> <dt>

<span data-ttu-id="6da8c-128">*SecureId* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="6da8c-128">*SecureId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6da8c-129">Этот параметр зарезервирован для использования в будущем.</span><span class="sxs-lookup"><span data-stu-id="6da8c-129">This parameter is reserved for future use.</span></span>

</dd> <dt>

<span data-ttu-id="6da8c-130">*Включено* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="6da8c-130">*Enabled* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6da8c-131">Указывает, включена ли политика авторизации подключений к удаленному рабочему столу.</span><span class="sxs-lookup"><span data-stu-id="6da8c-131">Specifies whether this RD CAP is enabled.</span></span>

</dd> <dt>

<span data-ttu-id="6da8c-132">*Девицередиректионтипе* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="6da8c-132">*DeviceRedirectionType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6da8c-133">Указывает, какие типы устройств будут перенаправляться.</span><span class="sxs-lookup"><span data-stu-id="6da8c-133">Specifies which device types will be redirected.</span></span>

<dt>

<span data-ttu-id="6da8c-134">0</span><span class="sxs-lookup"><span data-stu-id="6da8c-134">0</span></span>
</dt> <dd>

<span data-ttu-id="6da8c-135">Все устройства будут перенаправляться.</span><span class="sxs-lookup"><span data-stu-id="6da8c-135">All devices will be redirected.</span></span>

</dd> <dt>

<span data-ttu-id="6da8c-136">1</span><span class="sxs-lookup"><span data-stu-id="6da8c-136">1</span></span>
</dt> <dd>

<span data-ttu-id="6da8c-137">Устройства не будут перенаправлены.</span><span class="sxs-lookup"><span data-stu-id="6da8c-137">No devices will be redirected.</span></span>

</dd> <dt>

<span data-ttu-id="6da8c-138">2</span><span class="sxs-lookup"><span data-stu-id="6da8c-138">2</span></span>
</dt> <dd>

<span data-ttu-id="6da8c-139">Указанные устройства не будут перенаправляться.</span><span class="sxs-lookup"><span data-stu-id="6da8c-139">Specified devices will not be redirected.</span></span> <span data-ttu-id="6da8c-140">Параметры *дискдривесдисаблед*, *принтерсдисаблед*, *сериалпортсдисаблед*, *клипбоарддисаблед* и *плугандплайдевицесдисаблед* определяют, какие устройства не будут перенаправляться.</span><span class="sxs-lookup"><span data-stu-id="6da8c-140">The *DiskDrivesDisabled*, *PrintersDisabled*, *SerialPortsDisabled*, *ClipboardDisabled*, and *PlugAndPlayDevicesDisabled* parameters control which devices will not be redirected.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="6da8c-141">*Дискдривесдисаблед* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="6da8c-141">*DiskDrivesDisabled* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6da8c-142">Указывает, следует ли отключать перенаправление диска, если параметр *девицередиректионтипе* имеет значение 2.</span><span class="sxs-lookup"><span data-stu-id="6da8c-142">Specifies whether to disable disk drive redirection if the *DeviceRedirectionType* parameter is "2".</span></span>

</dd> <dt>

<span data-ttu-id="6da8c-143">*Принтерсдисаблед* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="6da8c-143">*PrintersDisabled* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6da8c-144">Указывает, следует ли отключать перенаправление принтера, если параметр *девицередиректионтипе* имеет значение 2.</span><span class="sxs-lookup"><span data-stu-id="6da8c-144">Specifies whether to disable printer redirection if the *DeviceRedirectionType* parameter is "2".</span></span>

</dd> <dt>

<span data-ttu-id="6da8c-145">*Сериалпортсдисаблед* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="6da8c-145">*SerialPortsDisabled* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6da8c-146">Указывает, следует ли отключить перенаправление последовательного порта, если параметр *девицередиректионтипе* имеет значение 2.</span><span class="sxs-lookup"><span data-stu-id="6da8c-146">Specifies whether to disable serial port redirection if the *DeviceRedirectionType* parameter is "2".</span></span>

</dd> <dt>

<span data-ttu-id="6da8c-147">*Клипбоарддисаблед* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="6da8c-147">*ClipboardDisabled* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6da8c-148">Указывает, следует ли отключить перенаправление буфера обмена, если параметр *девицередиректионтипе* имеет значение 2.</span><span class="sxs-lookup"><span data-stu-id="6da8c-148">Specifies whether to disable clipboard redirection if the *DeviceRedirectionType* parameter is "2".</span></span>

</dd> <dt>

<span data-ttu-id="6da8c-149">*Плугандплайдевицесдисаблед* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="6da8c-149">*PlugAndPlayDevicesDisabled* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6da8c-150">Указывает, следует ли отключать перенаправление устройств самонастраивающийся, если параметр *девицередиректионтипе* имеет значение 2.</span><span class="sxs-lookup"><span data-stu-id="6da8c-150">Specifies whether to disable redirection of Plug and Play devices if the *DeviceRedirectionType* parameter is "2".</span></span>

</dd> <dt>

<span data-ttu-id="6da8c-151">*IdleTimeout* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="6da8c-151">*IdleTimeout* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6da8c-152">Значение времени ожидания простоя в минутах</span><span class="sxs-lookup"><span data-stu-id="6da8c-152">Idle timeout value in minutes</span></span>

</dd> <dt>

<span data-ttu-id="6da8c-153">*SessionTimeout* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="6da8c-153">*SessionTimeout* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6da8c-154">Значение времени ожидания сеанса в минутах</span><span class="sxs-lookup"><span data-stu-id="6da8c-154">Session timeout value in minutes</span></span>

</dd> <dt>

<span data-ttu-id="6da8c-155">*Сессионтимеаутактион* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="6da8c-155">*SessionTimeoutAction* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6da8c-156">Действие времени ожидания сеанса (в минутах)</span><span class="sxs-lookup"><span data-stu-id="6da8c-156">Session timeout action in minutes</span></span>

</dd> <dt>

<span data-ttu-id="6da8c-157">*Алловонлисдрсерверс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="6da8c-157">*AllowOnlySDRServers* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6da8c-158">Разрешены ли подключения только к серверам служб терминалов SDR</span><span class="sxs-lookup"><span data-stu-id="6da8c-158">Whether connections allowed only to SDR TS servers</span></span>

</dd> <dt>

<span data-ttu-id="6da8c-159">*Кукиеаусентикатион* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="6da8c-159">*CookieAuthentication* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6da8c-160">Указывает, можно ли использовать проверку подлинности файлов cookie для подключения к серверу шлюза служб терминалов</span><span class="sxs-lookup"><span data-stu-id="6da8c-160">Indicates whether cookie authentication can be used to connect to TS Gateway server</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6da8c-161">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="6da8c-161">Return value</span></span>

<span data-ttu-id="6da8c-162">Если метод завершается с ошибкой, он возвращает ноль.</span><span class="sxs-lookup"><span data-stu-id="6da8c-162">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="6da8c-163">Если метод завершился неудачно, он возвращает ненулевое значение.</span><span class="sxs-lookup"><span data-stu-id="6da8c-163">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="6da8c-164">Список кодов ошибок см. в разделе [службы удаленных рабочих столов коды ошибок поставщика WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="6da8c-164">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="6da8c-165">Комментарии</span><span class="sxs-lookup"><span data-stu-id="6da8c-165">Remarks</span></span>

<span data-ttu-id="6da8c-166">Для вызова этого метода необходимо быть членом группы администраторов.</span><span class="sxs-lookup"><span data-stu-id="6da8c-166">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="6da8c-167">Файлы MOF-файл (MOF) содержат определения для классов инструментарий управления Windows (WMI) (WMI).</span><span class="sxs-lookup"><span data-stu-id="6da8c-167">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="6da8c-168">MOF-файлы не устанавливаются в составе пакета средств разработки программного обеспечения Microsoft Windows (SDK).</span><span class="sxs-lookup"><span data-stu-id="6da8c-168">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="6da8c-169">Они устанавливаются на сервере при добавлении связанной роли с помощью диспетчер сервера.</span><span class="sxs-lookup"><span data-stu-id="6da8c-169">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="6da8c-170">Дополнительные сведения о файлах MOF см. в разделе [MOF-файл (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="6da8c-170">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="6da8c-171">Требования</span><span class="sxs-lookup"><span data-stu-id="6da8c-171">Requirements</span></span>



| <span data-ttu-id="6da8c-172">Требование</span><span class="sxs-lookup"><span data-stu-id="6da8c-172">Requirement</span></span> | <span data-ttu-id="6da8c-173">Значение</span><span class="sxs-lookup"><span data-stu-id="6da8c-173">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="6da8c-174">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="6da8c-174">Minimum supported client</span></span><br/> | <span data-ttu-id="6da8c-175">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="6da8c-175">None supported</span></span><br/>                                                                |
| <span data-ttu-id="6da8c-176">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="6da8c-176">Minimum supported server</span></span><br/> | <span data-ttu-id="6da8c-177">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="6da8c-177">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="6da8c-178">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="6da8c-178">Namespace</span></span><br/>                | <span data-ttu-id="6da8c-179">Корневой \\ CIMv2 \\ терминалсервицес</span><span class="sxs-lookup"><span data-stu-id="6da8c-179">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="6da8c-180">MOF</span><span class="sxs-lookup"><span data-stu-id="6da8c-180">MOF</span></span><br/>                      | <dl> <span data-ttu-id="6da8c-181"><dt>TSGateway. mof</dt></span><span class="sxs-lookup"><span data-stu-id="6da8c-181"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="6da8c-182">DLL</span><span class="sxs-lookup"><span data-stu-id="6da8c-182">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6da8c-183"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6da8c-183"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="6da8c-184">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="6da8c-184">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6da8c-185">**\_Тсгатевайконнектионаусоризатионполици Win32**</span><span class="sxs-lookup"><span data-stu-id="6da8c-185">**Win32\_TSGatewayConnectionAuthorizationPolicy**</span></span>](win32-tsgatewayconnectionauthorizationpolicy.md)
</dt> </dl>

 

