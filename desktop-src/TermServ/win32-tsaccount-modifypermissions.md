---
title: Метод Модифипермиссионс класса Win32_TSAccount
description: Задает разрешение для указанной учетной записи.
ms.assetid: cef36f7f-d327-4bb6-9bff-282036c1a5d5
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода Модифипермиссионс
- Службы удаленных рабочих столов метода Модифипермиссионс, класс Win32_TSAccount
- Класс Win32_TSAccount службы удаленных рабочих столов, метод Модифипермиссионс
topic_type:
- apiref
api_name:
- Win32_TSAccount.ModifyPermissions
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c4bf6147c215475314f65bb8fa426442884bc82e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105672630"
---
# <a name="modifypermissions-method-of-the-win32_tsaccount-class"></a><span data-ttu-id="18e61-106">Метод Модифипермиссионс \_ класса Win32 тсаккаунт</span><span class="sxs-lookup"><span data-stu-id="18e61-106">ModifyPermissions method of the Win32\_TSAccount class</span></span>

<span data-ttu-id="18e61-107">Задает разрешение для указанной учетной записи.</span><span class="sxs-lookup"><span data-stu-id="18e61-107">Sets a permission for the specified account.</span></span>

## <a name="syntax"></a><span data-ttu-id="18e61-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="18e61-108">Syntax</span></span>


```mof
uint32 ModifyPermissions(
  [in] uint32  PermissionMask,
  [in] boolean Allow
);
```



## <a name="parameters"></a><span data-ttu-id="18e61-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="18e61-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="18e61-110">*Пермиссионмаск* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="18e61-110">*PermissionMask* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="18e61-111">[Разрешение узла сеансов удаленный рабочий стол](terminal-services-permissions.md) для установки.</span><span class="sxs-lookup"><span data-stu-id="18e61-111">The [Remote Desktop Session Host Permission](terminal-services-permissions.md) to set.</span></span>

<span data-ttu-id="18e61-112">Допустимые значения:</span><span class="sxs-lookup"><span data-stu-id="18e61-112">The possible values are:</span></span>

<dt>

<span id="WINSTATION_QUERY"></span><span id="winstation_query"></span>

<span data-ttu-id="18e61-113"><span id="WINSTATION_QUERY"></span><span id="winstation_query"></span>**Винстатион \_ ЗАПРОС** (0)</span><span class="sxs-lookup"><span data-stu-id="18e61-113"><span id="WINSTATION_QUERY"></span><span id="winstation_query"></span>**WINSTATION\_QUERY** (0)</span></span>


</dt> <dd>

<span data-ttu-id="18e61-114">Разрешение на запрос сведений о сеансе.</span><span class="sxs-lookup"><span data-stu-id="18e61-114">Permission to query information about a session.</span></span>

</dd> <dt>

<span id="WINSTATION_SET"></span><span id="winstation_set"></span>

<span data-ttu-id="18e61-115"><span id="WINSTATION_SET"></span><span id="winstation_set"></span>**Винстатион \_ SET** (1)</span><span class="sxs-lookup"><span data-stu-id="18e61-115"><span id="WINSTATION_SET"></span><span id="winstation_set"></span>**WINSTATION\_SET** (1)</span></span>


</dt> <dd>

<span data-ttu-id="18e61-116">Разрешение на изменение параметров соединения.</span><span class="sxs-lookup"><span data-stu-id="18e61-116">Permission to modify connection parameters.</span></span>

</dd> <dt>

<span id="WINSTATION_RESET"></span><span id="winstation_reset"></span>

<span data-ttu-id="18e61-117"><span id="WINSTATION_RESET"></span><span id="winstation_reset"></span>**Винстатион \_ Сброс** (6)</span><span class="sxs-lookup"><span data-stu-id="18e61-117"><span id="WINSTATION_RESET"></span><span id="winstation_reset"></span>**WINSTATION\_RESET** (6)</span></span>


</dt> <dd>

<span data-ttu-id="18e61-118">Разрешение на сброс или завершение сеанса или соединения.</span><span class="sxs-lookup"><span data-stu-id="18e61-118">Permission to reset or end a session or connection.</span></span>

</dd> <dt>

<span id="WINSTATION_VIRTUAL___STANDARD_RIGHTS_REQUIRED"></span><span id="winstation_virtual___standard_rights_required"></span>

<span data-ttu-id="18e61-119"><span id="WINSTATION_VIRTUAL___STANDARD_RIGHTS_REQUIRED"></span><span id="winstation_virtual___standard_rights_required"></span>**Винстатион \_ \| \_ \_ Требуются права на виртуальные стандартные** (3)</span><span class="sxs-lookup"><span data-stu-id="18e61-119"><span id="WINSTATION_VIRTUAL___STANDARD_RIGHTS_REQUIRED"></span><span id="winstation_virtual___standard_rights_required"></span>**WINSTATION\_VIRTUAL \| STANDARD\_RIGHTS\_REQUIRED** (3)</span></span>


</dt> <dd>

<span data-ttu-id="18e61-120">Разрешение на использование виртуальных каналов.</span><span class="sxs-lookup"><span data-stu-id="18e61-120">Permission to use virtual channels.</span></span> <span data-ttu-id="18e61-121">Виртуальные каналы обеспечивают доступ из серверной программы к клиентским устройствам.</span><span class="sxs-lookup"><span data-stu-id="18e61-121">Virtual channels provide access from a server program to client devices.</span></span>

</dd> <dt>

<span id="WINSTATION_SHADOW"></span><span id="winstation_shadow"></span>

<span data-ttu-id="18e61-122"><span id="WINSTATION_SHADOW"></span><span id="winstation_shadow"></span>**Винстатион \_ ТЕНЕВая копия** (4)</span><span class="sxs-lookup"><span data-stu-id="18e61-122"><span id="WINSTATION_SHADOW"></span><span id="winstation_shadow"></span>**WINSTATION\_SHADOW** (4)</span></span>


</dt> <dd>

<span data-ttu-id="18e61-123">Разрешение на теневое или удаленное управление сеансом другого пользователя.</span><span class="sxs-lookup"><span data-stu-id="18e61-123">Permission to shadow or remotely control another user's session.</span></span>

</dd> <dt>

<span id="WINSTATION_LOGON"></span><span id="winstation_logon"></span>

<span data-ttu-id="18e61-124"><span id="WINSTATION_LOGON"></span><span id="winstation_logon"></span>**Винстатион \_ Вход в систему** (5)</span><span class="sxs-lookup"><span data-stu-id="18e61-124"><span id="WINSTATION_LOGON"></span><span id="winstation_logon"></span>**WINSTATION\_LOGON** (5)</span></span>


</dt> <dd>

<span data-ttu-id="18e61-125">Разрешение на вход в сеанс на сервере.</span><span class="sxs-lookup"><span data-stu-id="18e61-125">Permission to log on to a session on the server.</span></span>

</dd> <dt>

<span id="WINSTATION_LOGOFF"></span><span id="winstation_logoff"></span>

<span data-ttu-id="18e61-126"><span id="WINSTATION_LOGOFF"></span><span id="winstation_logoff"></span>**Винстатион \_ Выход из системы** (2)</span><span class="sxs-lookup"><span data-stu-id="18e61-126"><span id="WINSTATION_LOGOFF"></span><span id="winstation_logoff"></span>**WINSTATION\_LOGOFF** (2)</span></span>


</dt> <dd>

<span data-ttu-id="18e61-127">Разрешение на выход пользователя из сеанса.</span><span class="sxs-lookup"><span data-stu-id="18e61-127">Permission to log off a user from a session.</span></span>

</dd> <dt>

<span id="WINSTATION_MSG"></span><span id="winstation_msg"></span>

<span data-ttu-id="18e61-128"><span id="WINSTATION_MSG"></span><span id="winstation_msg"></span>**Винстатион \_ MSG** (7)</span><span class="sxs-lookup"><span data-stu-id="18e61-128"><span id="WINSTATION_MSG"></span><span id="winstation_msg"></span>**WINSTATION\_MSG** (7)</span></span>


</dt> <dd>

<span data-ttu-id="18e61-129">Разрешение на отправку сообщений в сеанс другого пользователя.</span><span class="sxs-lookup"><span data-stu-id="18e61-129">Permission to send a message to another user's session.</span></span>

</dd> <dt>

<span id="WINSTATION_CONNECT"></span><span id="winstation_connect"></span>

<span data-ttu-id="18e61-130"><span id="WINSTATION_CONNECT"></span><span id="winstation_connect"></span>**Винстатион \_ Подключение** (8)</span><span class="sxs-lookup"><span data-stu-id="18e61-130"><span id="WINSTATION_CONNECT"></span><span id="winstation_connect"></span>**WINSTATION\_CONNECT** (8)</span></span>


</dt> <dd>

<span data-ttu-id="18e61-131">Разрешение на подключение к другому сеансу.</span><span class="sxs-lookup"><span data-stu-id="18e61-131">Permission to connect to another session.</span></span>

</dd> <dt>

<span id="WINSTATION_DISCONNECT"></span><span id="winstation_disconnect"></span>

<span data-ttu-id="18e61-132"><span id="WINSTATION_DISCONNECT"></span><span id="winstation_disconnect"></span>**Винстатион \_ ОТКЛЮЧИТЬ** (9)</span><span class="sxs-lookup"><span data-stu-id="18e61-132"><span id="WINSTATION_DISCONNECT"></span><span id="winstation_disconnect"></span>**WINSTATION\_DISCONNECT** (9)</span></span>


</dt> <dd>

<span data-ttu-id="18e61-133">Разрешение на отключение сеанса.</span><span class="sxs-lookup"><span data-stu-id="18e61-133">Permission to disconnect a session.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="18e61-134">*Разрешить* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="18e61-134">*Allow* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="18e61-135">Указывает, разрешен или запрещен ли разрешение в параметре *пермиссионмаск* .</span><span class="sxs-lookup"><span data-stu-id="18e61-135">Specifies whether the permission in the *PermissionMask* parameter is allowed or denied.</span></span>

<span data-ttu-id="18e61-136">Допустимые значения:</span><span class="sxs-lookup"><span data-stu-id="18e61-136">The possible values are:</span></span>

<dt>

<span id="1"></span>

<span data-ttu-id="18e61-137"><span id="1"></span>**1**</span><span class="sxs-lookup"><span data-stu-id="18e61-137"><span id="1"></span>**1**</span></span>


</dt> <dd>

<span data-ttu-id="18e61-138">Указанный набор разрешений разрешен.</span><span class="sxs-lookup"><span data-stu-id="18e61-138">The specified permission set is allowed.</span></span>

</dd> <dt>

<span id="0"></span>

<span data-ttu-id="18e61-139"><span id="0"></span>**0,0**</span><span class="sxs-lookup"><span data-stu-id="18e61-139"><span id="0"></span>**0**</span></span>


</dt> <dd>

<span data-ttu-id="18e61-140">Указанный набор разрешений запрещен.</span><span class="sxs-lookup"><span data-stu-id="18e61-140">The specified permission set is denied.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="18e61-141">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="18e61-141">Return value</span></span>

<span data-ttu-id="18e61-142">Возвращает значение 0 при успешном выполнении, в противном случае возвращает код ошибки WMI.</span><span class="sxs-lookup"><span data-stu-id="18e61-142">Returns 0 on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="18e61-143">Список этих значений см. в разделе [службы удаленных рабочих столов коды ошибок поставщика WMI](terminal-services-wmi-provider-error-codes.md) .</span><span class="sxs-lookup"><span data-stu-id="18e61-143">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span>

## <a name="remarks"></a><span data-ttu-id="18e61-144">Комментарии</span><span class="sxs-lookup"><span data-stu-id="18e61-144">Remarks</span></span>

<span data-ttu-id="18e61-145">Файлы MOF-файл (MOF) содержат определения для классов инструментарий управления Windows (WMI) (WMI).</span><span class="sxs-lookup"><span data-stu-id="18e61-145">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="18e61-146">MOF-файлы не устанавливаются в составе пакета средств разработки программного обеспечения Microsoft Windows (SDK).</span><span class="sxs-lookup"><span data-stu-id="18e61-146">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="18e61-147">Они устанавливаются на сервере при добавлении связанной роли с помощью диспетчер сервера.</span><span class="sxs-lookup"><span data-stu-id="18e61-147">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="18e61-148">Дополнительные сведения о файлах MOF см. в разделе [MOF-файл (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="18e61-148">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="18e61-149">Требования</span><span class="sxs-lookup"><span data-stu-id="18e61-149">Requirements</span></span>



| <span data-ttu-id="18e61-150">Требование</span><span class="sxs-lookup"><span data-stu-id="18e61-150">Requirement</span></span> | <span data-ttu-id="18e61-151">Значение</span><span class="sxs-lookup"><span data-stu-id="18e61-151">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="18e61-152">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="18e61-152">Minimum supported client</span></span><br/> | <span data-ttu-id="18e61-153">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="18e61-153">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="18e61-154">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="18e61-154">Minimum supported server</span></span><br/> | <span data-ttu-id="18e61-155">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="18e61-155">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="18e61-156">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="18e61-156">Namespace</span></span><br/>                | <span data-ttu-id="18e61-157">Корневой \\ CIMv2 \\ терминалсервицес</span><span class="sxs-lookup"><span data-stu-id="18e61-157">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="18e61-158">MOF</span><span class="sxs-lookup"><span data-stu-id="18e61-158">MOF</span></span><br/>                      | <dl> <span data-ttu-id="18e61-159"><dt>Тскфгвми. mof</dt></span><span class="sxs-lookup"><span data-stu-id="18e61-159"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="18e61-160">DLL</span><span class="sxs-lookup"><span data-stu-id="18e61-160">DLL</span></span><br/>                      | <dl> <span data-ttu-id="18e61-161"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="18e61-161"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="18e61-162">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="18e61-162">See also</span></span>

<dl> <dt>

[<span data-ttu-id="18e61-163">**\_Тсаккаунт Win32**</span><span class="sxs-lookup"><span data-stu-id="18e61-163">**Win32\_TSAccount**</span></span>](win32-tsaccount.md)
</dt> </dl>

 

