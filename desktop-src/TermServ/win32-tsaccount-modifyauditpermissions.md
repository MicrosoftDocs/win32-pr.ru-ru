---
title: Метод Модифяудитпермиссионс класса Win32_TSAccount
description: Подготавливает к установке более детализированного набора разрешений на аудит для указанной учетной записи.
ms.assetid: 7df44a37-257d-49c6-8193-f1e1c5ebbb57
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода Модифяудитпермиссионс
- Службы удаленных рабочих столов метода Модифяудитпермиссионс, класс Win32_TSAccount
- Класс Win32_TSAccount службы удаленных рабочих столов, метод Модифяудитпермиссионс
topic_type:
- apiref
api_name:
- Win32_TSAccount.ModifyAuditPermissions
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f19337cc6110a15b206fc437fb6ec594ded60640
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103892565"
---
# <a name="modifyauditpermissions-method-of-the-win32_tsaccount-class"></a><span data-ttu-id="9bb47-106">Метод Модифяудитпермиссионс \_ класса Win32 тсаккаунт</span><span class="sxs-lookup"><span data-stu-id="9bb47-106">ModifyAuditPermissions method of the Win32\_TSAccount class</span></span>

<span data-ttu-id="9bb47-107">Метод **модифяудитпермиссионс** готовится к установке более детального набора разрешений аудита для указанной учетной записи.</span><span class="sxs-lookup"><span data-stu-id="9bb47-107">The **ModifyAuditPermissions** method prepares to set a more granular set of audit permissions to the specified account.</span></span>

## <a name="syntax"></a><span data-ttu-id="9bb47-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="9bb47-108">Syntax</span></span>


```mof
uint32 ModifyAuditPermissions(
  [in] uint32  PermissionMask,
  [in] boolean Success
);
```



## <a name="parameters"></a><span data-ttu-id="9bb47-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="9bb47-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9bb47-110">*Пермиссионмаск* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="9bb47-110">*PermissionMask* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9bb47-111">Набор [разрешений узла сеанса удаленный рабочий стол](terminal-services-permissions.md) , связываемых с указанной учетной записью.</span><span class="sxs-lookup"><span data-stu-id="9bb47-111">The set of [Remote Desktop Session Host Permissions](terminal-services-permissions.md) to associate with the specified account.</span></span> <span data-ttu-id="9bb47-112">Значением этого параметра является точечный рисунок, и можно выбрать любое или все из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="9bb47-112">The value of this parameter is a bitmap, and any or all of the following values may be selected.</span></span>

<dt>

<span id="WINSTATION_QUERY"></span><span id="winstation_query"></span>

<span data-ttu-id="9bb47-113"><span id="WINSTATION_QUERY"></span><span id="winstation_query"></span>**Винстатион \_ ЗАПРОС** (0)</span><span class="sxs-lookup"><span data-stu-id="9bb47-113"><span id="WINSTATION_QUERY"></span><span id="winstation_query"></span>**WINSTATION\_QUERY** (0)</span></span>


</dt> <dd>

<span data-ttu-id="9bb47-114">Разрешение на запрос сведений о сеансе.</span><span class="sxs-lookup"><span data-stu-id="9bb47-114">Permission to query information about a session.</span></span>

</dd> <dt>

<span id="WINSTATION_SET"></span><span id="winstation_set"></span>

<span data-ttu-id="9bb47-115"><span id="WINSTATION_SET"></span><span id="winstation_set"></span>**Винстатион \_ SET** (1)</span><span class="sxs-lookup"><span data-stu-id="9bb47-115"><span id="WINSTATION_SET"></span><span id="winstation_set"></span>**WINSTATION\_SET** (1)</span></span>


</dt> <dd>

<span data-ttu-id="9bb47-116">Разрешение на изменение параметров соединения.</span><span class="sxs-lookup"><span data-stu-id="9bb47-116">Permission to modify connection parameters.</span></span>

</dd> <dt>

<span id="WINSTATION_RESET"></span><span id="winstation_reset"></span>

<span data-ttu-id="9bb47-117"><span id="WINSTATION_RESET"></span><span id="winstation_reset"></span>**Винстатион \_ Сброс** (6)</span><span class="sxs-lookup"><span data-stu-id="9bb47-117"><span id="WINSTATION_RESET"></span><span id="winstation_reset"></span>**WINSTATION\_RESET** (6)</span></span>


</dt> <dd>

<span data-ttu-id="9bb47-118">Разрешение на сброс или завершение сеанса или соединения.</span><span class="sxs-lookup"><span data-stu-id="9bb47-118">Permission to reset or end a session or connection.</span></span>

</dd> <dt>

<span id="WINSTATION_VIRTUAL___STANDARD_RIGHTS_REQUIRED"></span><span id="winstation_virtual___standard_rights_required"></span>

<span data-ttu-id="9bb47-119"><span id="WINSTATION_VIRTUAL___STANDARD_RIGHTS_REQUIRED"></span><span id="winstation_virtual___standard_rights_required"></span>**Винстатион \_ \| \_ \_ Требуются права на виртуальные стандартные** (3)</span><span class="sxs-lookup"><span data-stu-id="9bb47-119"><span id="WINSTATION_VIRTUAL___STANDARD_RIGHTS_REQUIRED"></span><span id="winstation_virtual___standard_rights_required"></span>**WINSTATION\_VIRTUAL \| STANDARD\_RIGHTS\_REQUIRED** (3)</span></span>


</dt> <dd>

<span data-ttu-id="9bb47-120">Разрешение на использование виртуальных каналов.</span><span class="sxs-lookup"><span data-stu-id="9bb47-120">Permission to use virtual channels.</span></span> <span data-ttu-id="9bb47-121">Виртуальные каналы обеспечивают доступ из серверной программы к клиентским устройствам.</span><span class="sxs-lookup"><span data-stu-id="9bb47-121">Virtual channels provide access from a server program to client devices.</span></span>

</dd> <dt>

<span id="WINSTATION_SHADOW"></span><span id="winstation_shadow"></span>

<span data-ttu-id="9bb47-122"><span id="WINSTATION_SHADOW"></span><span id="winstation_shadow"></span>**Винстатион \_ ТЕНЕВая копия** (4)</span><span class="sxs-lookup"><span data-stu-id="9bb47-122"><span id="WINSTATION_SHADOW"></span><span id="winstation_shadow"></span>**WINSTATION\_SHADOW** (4)</span></span>


</dt> <dd>

<span data-ttu-id="9bb47-123">Разрешение на теневое или удаленное управление сеансом другого пользователя.</span><span class="sxs-lookup"><span data-stu-id="9bb47-123">Permission to shadow or remotely control another user's session.</span></span>

</dd> <dt>

<span id="WINSTATION_LOGON"></span><span id="winstation_logon"></span>

<span data-ttu-id="9bb47-124"><span id="WINSTATION_LOGON"></span><span id="winstation_logon"></span>**Винстатион \_ Вход в систему** (5)</span><span class="sxs-lookup"><span data-stu-id="9bb47-124"><span id="WINSTATION_LOGON"></span><span id="winstation_logon"></span>**WINSTATION\_LOGON** (5)</span></span>


</dt> <dd>

<span data-ttu-id="9bb47-125">Разрешение на вход в сеанс на сервере.</span><span class="sxs-lookup"><span data-stu-id="9bb47-125">Permission to log on to a session on the server.</span></span>

</dd> <dt>

<span id="WINSTATION_LOGOFF"></span><span id="winstation_logoff"></span>

<span data-ttu-id="9bb47-126"><span id="WINSTATION_LOGOFF"></span><span id="winstation_logoff"></span>**Винстатион \_ Выход из системы** (2)</span><span class="sxs-lookup"><span data-stu-id="9bb47-126"><span id="WINSTATION_LOGOFF"></span><span id="winstation_logoff"></span>**WINSTATION\_LOGOFF** (2)</span></span>


</dt> <dd>

<span data-ttu-id="9bb47-127">Разрешение на выход пользователя из сеанса.</span><span class="sxs-lookup"><span data-stu-id="9bb47-127">Permission to log off a user from a session.</span></span>

</dd> <dt>

<span id="WINSTATION_MSG"></span><span id="winstation_msg"></span>

<span data-ttu-id="9bb47-128"><span id="WINSTATION_MSG"></span><span id="winstation_msg"></span>**Винстатион \_ MSG** (7)</span><span class="sxs-lookup"><span data-stu-id="9bb47-128"><span id="WINSTATION_MSG"></span><span id="winstation_msg"></span>**WINSTATION\_MSG** (7)</span></span>


</dt> <dd>

<span data-ttu-id="9bb47-129">Разрешение на отправку сообщений в сеанс другого пользователя.</span><span class="sxs-lookup"><span data-stu-id="9bb47-129">Permission to send a message to another user's session.</span></span>

</dd> <dt>

<span id="WINSTATION_CONNECT"></span><span id="winstation_connect"></span>

<span data-ttu-id="9bb47-130"><span id="WINSTATION_CONNECT"></span><span id="winstation_connect"></span>**Винстатион \_ Подключение** (8)</span><span class="sxs-lookup"><span data-stu-id="9bb47-130"><span id="WINSTATION_CONNECT"></span><span id="winstation_connect"></span>**WINSTATION\_CONNECT** (8)</span></span>


</dt> <dd>

<span data-ttu-id="9bb47-131">Разрешение на подключение к другому сеансу.</span><span class="sxs-lookup"><span data-stu-id="9bb47-131">Permission to connect to another session.</span></span>

</dd> <dt>

<span id="WINSTATION_DISCONNECT"></span><span id="winstation_disconnect"></span>

<span data-ttu-id="9bb47-132"><span id="WINSTATION_DISCONNECT"></span><span id="winstation_disconnect"></span>**Винстатион \_ ОТКЛЮЧИТЬ** (9)</span><span class="sxs-lookup"><span data-stu-id="9bb47-132"><span id="WINSTATION_DISCONNECT"></span><span id="winstation_disconnect"></span>**WINSTATION\_DISCONNECT** (9)</span></span>


</dt> <dd>

<span data-ttu-id="9bb47-133">Разрешение на отключение сеанса.</span><span class="sxs-lookup"><span data-stu-id="9bb47-133">Permission to disconnect a session.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="9bb47-134">*Успешное завершение* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="9bb47-134">*Success* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9bb47-135">Указывает, разрешен или запрещен набор разрешений, заданный значением параметра *пермиссионмаск* .</span><span class="sxs-lookup"><span data-stu-id="9bb47-135">Specifies if the permission set specified by the value of the *PermissionMask* parameter is allowed or denied.</span></span>

<dt>

<span id="1"></span>

<span data-ttu-id="9bb47-136"><span id="1"></span>**1**</span><span class="sxs-lookup"><span data-stu-id="9bb47-136"><span id="1"></span>**1**</span></span>


</dt> <dd>

<span data-ttu-id="9bb47-137">Указанный набор разрешений разрешен.</span><span class="sxs-lookup"><span data-stu-id="9bb47-137">The specified permission set is allowed.</span></span>

</dd> <dt>

<span id="0"></span>

<span data-ttu-id="9bb47-138"><span id="0"></span>**0,0**</span><span class="sxs-lookup"><span data-stu-id="9bb47-138"><span id="0"></span>**0**</span></span>


</dt> <dd>

<span data-ttu-id="9bb47-139">Указанный набор разрешений запрещен.</span><span class="sxs-lookup"><span data-stu-id="9bb47-139">The specified permission set is denied.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9bb47-140">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="9bb47-140">Return value</span></span>

<span data-ttu-id="9bb47-141">Возвращает значение 0 при успешном выполнении, в противном случае возвращает код ошибки WMI.</span><span class="sxs-lookup"><span data-stu-id="9bb47-141">Returns 0 on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="9bb47-142">Список этих значений см. в разделе [службы удаленных рабочих столов коды ошибок поставщика WMI](terminal-services-wmi-provider-error-codes.md) .</span><span class="sxs-lookup"><span data-stu-id="9bb47-142">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span>

## <a name="remarks"></a><span data-ttu-id="9bb47-143">Комментарии</span><span class="sxs-lookup"><span data-stu-id="9bb47-143">Remarks</span></span>

<span data-ttu-id="9bb47-144">Файлы MOF-файл (MOF) содержат определения для классов инструментарий управления Windows (WMI) (WMI).</span><span class="sxs-lookup"><span data-stu-id="9bb47-144">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="9bb47-145">MOF-файлы не устанавливаются в составе пакета средств разработки программного обеспечения Microsoft Windows (SDK).</span><span class="sxs-lookup"><span data-stu-id="9bb47-145">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="9bb47-146">Они устанавливаются на сервере при добавлении связанной роли с помощью диспетчер сервера.</span><span class="sxs-lookup"><span data-stu-id="9bb47-146">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="9bb47-147">Дополнительные сведения о файлах MOF см. в разделе [MOF-файл (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="9bb47-147">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="9bb47-148">Требования</span><span class="sxs-lookup"><span data-stu-id="9bb47-148">Requirements</span></span>



| <span data-ttu-id="9bb47-149">Требование</span><span class="sxs-lookup"><span data-stu-id="9bb47-149">Requirement</span></span> | <span data-ttu-id="9bb47-150">Значение</span><span class="sxs-lookup"><span data-stu-id="9bb47-150">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="9bb47-151">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="9bb47-151">Minimum supported client</span></span><br/> | <span data-ttu-id="9bb47-152">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="9bb47-152">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="9bb47-153">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="9bb47-153">Minimum supported server</span></span><br/> | <span data-ttu-id="9bb47-154">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="9bb47-154">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="9bb47-155">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="9bb47-155">Namespace</span></span><br/>                | <span data-ttu-id="9bb47-156">Корневой \\ CIMv2 \\ терминалсервицес</span><span class="sxs-lookup"><span data-stu-id="9bb47-156">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="9bb47-157">MOF</span><span class="sxs-lookup"><span data-stu-id="9bb47-157">MOF</span></span><br/>                      | <dl> <span data-ttu-id="9bb47-158"><dt>Тскфгвми. mof</dt></span><span class="sxs-lookup"><span data-stu-id="9bb47-158"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="9bb47-159">DLL</span><span class="sxs-lookup"><span data-stu-id="9bb47-159">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9bb47-160"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9bb47-160"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9bb47-161">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="9bb47-161">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9bb47-162">**\_Тсаккаунт Win32**</span><span class="sxs-lookup"><span data-stu-id="9bb47-162">**Win32\_TSAccount**</span></span>](win32-tsaccount.md)
</dt> </dl>

 

