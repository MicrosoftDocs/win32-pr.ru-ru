---
title: Метод Create класса Win32_TSGatewayConnectionAuthorizationPolicy
description: Создает удаленный рабочий стол политику авторизации подключений (RD \ 160; CAP) с указанными значениями. Новый RD \ 160; ЗАГЛУШКа будет вставлена в начало рабочего стола \ 160; Порядок вычисления CAP со значением свойства Order, равным \ 0034; 1 \ 0034;.
ms.assetid: 0010cd2b-9c23-488a-9337-d2ed338136d3
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода Create
- Создание службы удаленных рабочих столов метода, Win32_TSGatewayConnectionAuthorizationPolicy класса
- Класс Win32_TSGatewayConnectionAuthorizationPolicy службы удаленных рабочих столов, метод Create
topic_type:
- apiref
api_name:
- Win32_TSGatewayConnectionAuthorizationPolicy.Create
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: edc027c2f7fc90318bd1af6fd1254077a860a5d8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071289"
---
# <a name="create-method-of-the-win32_tsgatewayconnectionauthorizationpolicy-class"></a><span data-ttu-id="f99fc-107">Метод Create \_ класса Win32 тсгатевайконнектионаусоризатионполици</span><span class="sxs-lookup"><span data-stu-id="f99fc-107">Create method of the Win32\_TSGatewayConnectionAuthorizationPolicy class</span></span>

<span data-ttu-id="f99fc-108">Создает удаленный рабочий стол политику авторизации подключений (RD CAP) с указанными значениями.</span><span class="sxs-lookup"><span data-stu-id="f99fc-108">Creates a Remote Desktop connection authorization policy (RD CAP) by using the specified values.</span></span> <span data-ttu-id="f99fc-109">Новое ограничение удаленных рабочих столов будет вставлено в верхней части порядка оценки авторизации подключений удаленных рабочих столов со значением "1" свойства **Order** .</span><span class="sxs-lookup"><span data-stu-id="f99fc-109">The new RD CAP will be inserted at the top of the RD CAP evaluation order, with an **Order** property value of "1".</span></span>

## <a name="syntax"></a><span data-ttu-id="f99fc-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f99fc-110">Syntax</span></span>


```mof
uint32 Create(
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



## <a name="parameters"></a><span data-ttu-id="f99fc-111">Параметры</span><span class="sxs-lookup"><span data-stu-id="f99fc-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f99fc-112">*Имя* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="f99fc-112">*Name* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f99fc-113">Имя политики авторизации подключений к удаленному рабочему столу.</span><span class="sxs-lookup"><span data-stu-id="f99fc-113">Name of the RD CAP.</span></span> <span data-ttu-id="f99fc-114">Имя должно содержать 64 символов или меньше, уникально (регистр игнорируется) и не может включать следующие зарезервированные символы:</span><span class="sxs-lookup"><span data-stu-id="f99fc-114">The name must be 64 characters or less, unique (case is ignored), and cannot contain the following reserved characters:</span></span>

<span data-ttu-id="f99fc-115"><> :; " / \\ \| ?</span><span class="sxs-lookup"><span data-stu-id="f99fc-115"><> : ; " / \\ \| ?</span></span> <span data-ttu-id="f99fc-116">\*\[Вкладка\]</span><span class="sxs-lookup"><span data-stu-id="f99fc-116">\* \[TAB\]</span></span>

</dd> <dt>

<span data-ttu-id="f99fc-117">*Усерграупнамес* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="f99fc-117">*UserGroupNames* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f99fc-118">Список имен групп пользователей, разделенных точкой с запятой, для новой политики авторизации подключений к удаленному рабочему столу.</span><span class="sxs-lookup"><span data-stu-id="f99fc-118">List of user group names, separated by semicolons, for the new RD CAP.</span></span>

</dd> <dt>

<span data-ttu-id="f99fc-119">*Компутерграупнамес* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="f99fc-119">*ComputerGroupNames* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f99fc-120">Список имен групп компьютеров, разделенных точкой с запятой, для новой политики авторизации подключений к удаленному рабочему столу.</span><span class="sxs-lookup"><span data-stu-id="f99fc-120">List of computer group names, separated by semicolons, for the new RD CAP.</span></span>

</dd> <dt>

<span data-ttu-id="f99fc-121">*Смарт-карта* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="f99fc-121">*SmartCard* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f99fc-122">Указывает, можно ли использовать смарт-карты для проверки подлинности на сервере шлюза удаленных рабочих столов.</span><span class="sxs-lookup"><span data-stu-id="f99fc-122">Specifies whether smart cards can be used to authenticate with the RD Gateway server.</span></span>

</dd> <dt>

<span data-ttu-id="f99fc-123">*Пароль* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="f99fc-123">*Password* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f99fc-124">Указывает, можно ли использовать пароли для проверки подлинности на сервере шлюза удаленных рабочих столов.</span><span class="sxs-lookup"><span data-stu-id="f99fc-124">Specifies whether passwords can be used to authenticate with the RD Gateway server.</span></span>

</dd> <dt>

<span data-ttu-id="f99fc-125">*SecureId* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="f99fc-125">*SecureId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f99fc-126">Этот параметр зарезервирован для использования в будущем.</span><span class="sxs-lookup"><span data-stu-id="f99fc-126">This parameter is reserved for future use.</span></span>

</dd> <dt>

<span data-ttu-id="f99fc-127">*Включено* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="f99fc-127">*Enabled* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f99fc-128">Указывает, включена ли политика авторизации подключений к удаленному рабочему столу.</span><span class="sxs-lookup"><span data-stu-id="f99fc-128">Specifies whether this RD CAP is enabled.</span></span>

</dd> <dt>

<span data-ttu-id="f99fc-129">*Девицередиректионтипе* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="f99fc-129">*DeviceRedirectionType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f99fc-130">Указывает, какие типы устройств будут перенаправляться.</span><span class="sxs-lookup"><span data-stu-id="f99fc-130">Specifies which device types will be redirected.</span></span>

<dt>

<span data-ttu-id="f99fc-131">0</span><span class="sxs-lookup"><span data-stu-id="f99fc-131">0</span></span>
</dt> <dd>

<span data-ttu-id="f99fc-132">Все устройства будут перенаправляться.</span><span class="sxs-lookup"><span data-stu-id="f99fc-132">All devices will be redirected.</span></span>

</dd> <dt>

<span data-ttu-id="f99fc-133">1</span><span class="sxs-lookup"><span data-stu-id="f99fc-133">1</span></span>
</dt> <dd>

<span data-ttu-id="f99fc-134">Устройства не будут перенаправлены.</span><span class="sxs-lookup"><span data-stu-id="f99fc-134">No devices will be redirected.</span></span>

</dd> <dt>

<span data-ttu-id="f99fc-135">2</span><span class="sxs-lookup"><span data-stu-id="f99fc-135">2</span></span>
</dt> <dd>

<span data-ttu-id="f99fc-136">Указанные устройства не будут перенаправляться.</span><span class="sxs-lookup"><span data-stu-id="f99fc-136">Specified devices will not be redirected.</span></span> <span data-ttu-id="f99fc-137">Параметры *дискдривесдисаблед*, *принтерсдисаблед*, *сериалпортсдисаблед*, *клипбоарддисаблед* и *плугандплайдевицесдисаблед* определяют, какие устройства не будут перенаправляться.</span><span class="sxs-lookup"><span data-stu-id="f99fc-137">The *DiskDrivesDisabled*, *PrintersDisabled*, *SerialPortsDisabled*, *ClipboardDisabled*, and *PlugAndPlayDevicesDisabled* parameters control which devices will not be redirected.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="f99fc-138">*Дискдривесдисаблед* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="f99fc-138">*DiskDrivesDisabled* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f99fc-139">Указывает, следует ли отключать перенаправление диска, если параметр *девицередиректионтипе* имеет значение 2.</span><span class="sxs-lookup"><span data-stu-id="f99fc-139">Specifies whether to disable disk drive redirection if the *DeviceRedirectionType* parameter is "2".</span></span>

</dd> <dt>

<span data-ttu-id="f99fc-140">*Принтерсдисаблед* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="f99fc-140">*PrintersDisabled* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f99fc-141">Указывает, следует ли отключать перенаправление принтера, если параметр *девицередиректионтипе* имеет значение 2.</span><span class="sxs-lookup"><span data-stu-id="f99fc-141">Specifies whether to disable printer redirection if the *DeviceRedirectionType* parameter is "2".</span></span>

</dd> <dt>

<span data-ttu-id="f99fc-142">*Сериалпортсдисаблед* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="f99fc-142">*SerialPortsDisabled* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f99fc-143">Указывает, следует ли отключить перенаправление последовательного порта, если параметр *девицередиректионтипе* имеет значение 2.</span><span class="sxs-lookup"><span data-stu-id="f99fc-143">Specifies whether to disable serial port redirection if the *DeviceRedirectionType* parameter is "2".</span></span>

</dd> <dt>

<span data-ttu-id="f99fc-144">*Клипбоарддисаблед* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="f99fc-144">*ClipboardDisabled* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f99fc-145">Указывает, следует ли отключить перенаправление буфера обмена, если параметр *девицередиректионтипе* имеет значение 2.</span><span class="sxs-lookup"><span data-stu-id="f99fc-145">Specifies whether to disable clipboard redirection if the *DeviceRedirectionType* parameter is "2".</span></span>

</dd> <dt>

<span data-ttu-id="f99fc-146">*Плугандплайдевицесдисаблед* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="f99fc-146">*PlugAndPlayDevicesDisabled* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f99fc-147">Указывает, следует ли отключать перенаправление устройств самонастраивающийся, если параметр *девицередиректионтипе* имеет значение 2.</span><span class="sxs-lookup"><span data-stu-id="f99fc-147">Specifies whether to disable redirection of Plug and Play devices if the *DeviceRedirectionType* parameter is "2".</span></span>

</dd> <dt>

<span data-ttu-id="f99fc-148">*IdleTimeout* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="f99fc-148">*IdleTimeout* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f99fc-149">Значение времени ожидания простоя в минутах</span><span class="sxs-lookup"><span data-stu-id="f99fc-149">Idle timeout value in minutes</span></span>

</dd> <dt>

<span data-ttu-id="f99fc-150">*SessionTimeout* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="f99fc-150">*SessionTimeout* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f99fc-151">Значение времени ожидания сеанса в минутах</span><span class="sxs-lookup"><span data-stu-id="f99fc-151">Session timeout value in minutes</span></span>

</dd> <dt>

<span data-ttu-id="f99fc-152">*Сессионтимеаутактион* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="f99fc-152">*SessionTimeoutAction* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f99fc-153">Действие времени ожидания сеанса (в минутах)</span><span class="sxs-lookup"><span data-stu-id="f99fc-153">Session timeout action in minutes</span></span>

</dd> <dt>

<span data-ttu-id="f99fc-154">*Алловонлисдрсерверс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="f99fc-154">*AllowOnlySDRServers* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f99fc-155">Разрешены ли подключения только к серверам служб терминалов SDR</span><span class="sxs-lookup"><span data-stu-id="f99fc-155">Whether connections allowed only to SDR TS servers</span></span>

</dd> <dt>

<span data-ttu-id="f99fc-156">*Кукиеаусентикатион* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="f99fc-156">*CookieAuthentication* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f99fc-157">Указывает, можно ли использовать проверку подлинности файлов cookie для подключения к серверу шлюза служб терминалов</span><span class="sxs-lookup"><span data-stu-id="f99fc-157">Indicates whether cookie authentication can be used to connect to TS Gateway server</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f99fc-158">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="f99fc-158">Return value</span></span>

<span data-ttu-id="f99fc-159">Если метод завершается с ошибкой, он возвращает ноль.</span><span class="sxs-lookup"><span data-stu-id="f99fc-159">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="f99fc-160">Если метод завершился неудачно, он возвращает ненулевое значение.</span><span class="sxs-lookup"><span data-stu-id="f99fc-160">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="f99fc-161">Список кодов ошибок см. в разделе [службы удаленных рабочих столов коды ошибок поставщика WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="f99fc-161">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="f99fc-162">Комментарии</span><span class="sxs-lookup"><span data-stu-id="f99fc-162">Remarks</span></span>

<span data-ttu-id="f99fc-163">Для вызова этого метода необходимо быть членом группы администраторов.</span><span class="sxs-lookup"><span data-stu-id="f99fc-163">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="f99fc-164">Файлы MOF-файл (MOF) содержат определения для классов инструментарий управления Windows (WMI) (WMI).</span><span class="sxs-lookup"><span data-stu-id="f99fc-164">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="f99fc-165">MOF-файлы не устанавливаются в составе пакета средств разработки программного обеспечения Microsoft Windows (SDK).</span><span class="sxs-lookup"><span data-stu-id="f99fc-165">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="f99fc-166">Они устанавливаются на сервере при добавлении связанной роли с помощью диспетчер сервера.</span><span class="sxs-lookup"><span data-stu-id="f99fc-166">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="f99fc-167">Дополнительные сведения о файлах MOF см. в разделе [MOF-файл (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="f99fc-167">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="f99fc-168">Требования</span><span class="sxs-lookup"><span data-stu-id="f99fc-168">Requirements</span></span>



| <span data-ttu-id="f99fc-169">Требование</span><span class="sxs-lookup"><span data-stu-id="f99fc-169">Requirement</span></span> | <span data-ttu-id="f99fc-170">Значение</span><span class="sxs-lookup"><span data-stu-id="f99fc-170">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="f99fc-171">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="f99fc-171">Minimum supported client</span></span><br/> | <span data-ttu-id="f99fc-172">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="f99fc-172">None supported</span></span><br/>                                                                |
| <span data-ttu-id="f99fc-173">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="f99fc-173">Minimum supported server</span></span><br/> | <span data-ttu-id="f99fc-174">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f99fc-174">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="f99fc-175">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="f99fc-175">Namespace</span></span><br/>                | <span data-ttu-id="f99fc-176">Корневой \\ CIMv2 \\ терминалсервицес</span><span class="sxs-lookup"><span data-stu-id="f99fc-176">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="f99fc-177">MOF</span><span class="sxs-lookup"><span data-stu-id="f99fc-177">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f99fc-178"><dt>TSGateway. mof</dt></span><span class="sxs-lookup"><span data-stu-id="f99fc-178"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="f99fc-179">DLL</span><span class="sxs-lookup"><span data-stu-id="f99fc-179">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f99fc-180"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f99fc-180"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="f99fc-181">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f99fc-181">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f99fc-182">**\_Тсгатевайконнектионаусоризатионполици Win32**</span><span class="sxs-lookup"><span data-stu-id="f99fc-182">**Win32\_TSGatewayConnectionAuthorizationPolicy**</span></span>](win32-tsgatewayconnectionauthorizationpolicy.md)
</dt> </dl>

 

