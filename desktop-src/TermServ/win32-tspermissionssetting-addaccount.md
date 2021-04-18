---
title: Метод Аддаккаунт класса Win32_TSPermissionsSetting (Факскомекс. h)
description: Метод Аддаккаунт готовится к добавлению учетной записи в терминал с указанным набором разрешений. Можно добавить пользователей, группы или компьютеры.
ms.assetid: da4d8f5b-7aa2-4b55-bf0f-b3e98b70a06b
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода Аддаккаунт
- Службы удаленных рабочих столов метода Аддаккаунт, класс Win32_TSPermissionsSetting
- Класс Win32_TSPermissionsSetting службы удаленных рабочих столов, метод Аддаккаунт
topic_type:
- apiref
api_name:
- Win32_TSPermissionsSetting.AddAccount
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: de89c34bd7aab20fbfbcbdedfd9d2f91bba866bc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104491589"
---
# <a name="addaccount-method-of-the-win32_tspermissionssetting-class"></a><span data-ttu-id="e91a3-107">Метод Аддаккаунт \_ класса Win32 тспермиссионссеттинг</span><span class="sxs-lookup"><span data-stu-id="e91a3-107">AddAccount method of the Win32\_TSPermissionsSetting class</span></span>

<span data-ttu-id="e91a3-108">Метод **аддаккаунт** готовится к добавлению учетной записи в терминал с указанным набором разрешений.</span><span class="sxs-lookup"><span data-stu-id="e91a3-108">The **AddAccount** method prepares to add an account to the terminal with the specified permission set.</span></span> <span data-ttu-id="e91a3-109">Можно добавить пользователей, группы или компьютеры.</span><span class="sxs-lookup"><span data-stu-id="e91a3-109">You can add users, groups, or computers.</span></span>

## <a name="syntax"></a><span data-ttu-id="e91a3-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e91a3-110">Syntax</span></span>


```mof
uint32 AddAccount(
  [in] string AccountName,
  [in] uint32 PermissionPreSet
);
```



## <a name="parameters"></a><span data-ttu-id="e91a3-111">Параметры</span><span class="sxs-lookup"><span data-stu-id="e91a3-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e91a3-112">*Имя_учетной_записи* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="e91a3-112">*AccountName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e91a3-113">Имя учетной записи, добавляемой в терминал.</span><span class="sxs-lookup"><span data-stu-id="e91a3-113">The name of the account to add to the terminal.</span></span>

</dd> <dt>

<span data-ttu-id="e91a3-114">*Пермиссионпресет* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="e91a3-114">*PermissionPreSet* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e91a3-115">Набор разрешений, связываемый с указанной учетной записью.</span><span class="sxs-lookup"><span data-stu-id="e91a3-115">The set of permissions to associate with the specified account.</span></span> <span data-ttu-id="e91a3-116">Этот параметр может быть любым или любым из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="e91a3-116">This parameter can be any or all of the following values.</span></span> <span data-ttu-id="e91a3-117">Дополнительные сведения см. в разделе [службы удаленных рабочих столов Permissions](terminal-services-permissions.md).</span><span class="sxs-lookup"><span data-stu-id="e91a3-117">For more information, see [Remote Desktop Services Permissions](terminal-services-permissions.md).</span></span>

<dt>

<span id="WINSTATION_GUEST_ACCESS"></span><span id="winstation_guest_access"></span>

<span data-ttu-id="e91a3-118"><span id="WINSTATION_GUEST_ACCESS"></span><span id="winstation_guest_access"></span>**Винстатион \_ Гостевой \_ доступ** (0)</span><span class="sxs-lookup"><span data-stu-id="e91a3-118"><span id="WINSTATION_GUEST_ACCESS"></span><span id="winstation_guest_access"></span>**WINSTATION\_GUEST\_ACCESS** (0)</span></span>


</dt> <dd>

<span data-ttu-id="e91a3-119">Учетная запись имеет разрешение на вход.</span><span class="sxs-lookup"><span data-stu-id="e91a3-119">The account has Logon permission.</span></span>

</dd> <dt>

<span id="WINSTATION_USER_ACCESS"></span><span id="winstation_user_access"></span>

<span data-ttu-id="e91a3-120"><span id="WINSTATION_USER_ACCESS"></span><span id="winstation_user_access"></span>**Винстатион \_ \_Доступ пользователей** (1)</span><span class="sxs-lookup"><span data-stu-id="e91a3-120"><span id="WINSTATION_USER_ACCESS"></span><span id="winstation_user_access"></span>**WINSTATION\_USER\_ACCESS** (1)</span></span>


</dt> <dd>

<span data-ttu-id="e91a3-121">Учетная запись имеет следующие разрешения: вход в систему, сведения о запросе, отправка сообщения и подключение.</span><span class="sxs-lookup"><span data-stu-id="e91a3-121">The account has the following permissions: Logon, Query Information, Send Message, and Connect.</span></span>

</dd> <dt>

<span id="WINSTATION_ALL_ACCESS"></span><span id="winstation_all_access"></span>

<span data-ttu-id="e91a3-122"><span id="WINSTATION_ALL_ACCESS"></span><span id="winstation_all_access"></span>**Винстатион \_ ВСЕ \_ доступ** (2)</span><span class="sxs-lookup"><span data-stu-id="e91a3-122"><span id="WINSTATION_ALL_ACCESS"></span><span id="winstation_all_access"></span>**WINSTATION\_ALL\_ACCESS** (2)</span></span>


</dt> <dd>

<span data-ttu-id="e91a3-123">Учетная запись имеет все разрешения службы удаленных рабочих столов.</span><span class="sxs-lookup"><span data-stu-id="e91a3-123">The account has all Remote Desktop Services Permissions.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e91a3-124">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="e91a3-124">Return value</span></span>

<span data-ttu-id="e91a3-125">Возвращает значение 0 при успешном выполнении, в противном случае возвращает код ошибки WMI.</span><span class="sxs-lookup"><span data-stu-id="e91a3-125">Returns 0 on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="e91a3-126">Список этих значений см. в разделе [службы удаленных рабочих столов коды ошибок поставщика WMI](terminal-services-wmi-provider-error-codes.md) .</span><span class="sxs-lookup"><span data-stu-id="e91a3-126">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span>

## <a name="remarks"></a><span data-ttu-id="e91a3-127">Комментарии</span><span class="sxs-lookup"><span data-stu-id="e91a3-127">Remarks</span></span>

<span data-ttu-id="e91a3-128">Файлы MOF-файл (MOF) содержат определения для классов инструментарий управления Windows (WMI) (WMI).</span><span class="sxs-lookup"><span data-stu-id="e91a3-128">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="e91a3-129">MOF-файлы не устанавливаются в составе пакета средств разработки программного обеспечения Microsoft Windows (SDK).</span><span class="sxs-lookup"><span data-stu-id="e91a3-129">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="e91a3-130">Они устанавливаются на сервере при добавлении связанной роли с помощью диспетчер сервера.</span><span class="sxs-lookup"><span data-stu-id="e91a3-130">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="e91a3-131">Дополнительные сведения о файлах MOF см. в разделе [MOF-файл (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="e91a3-131">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="e91a3-132">Требования</span><span class="sxs-lookup"><span data-stu-id="e91a3-132">Requirements</span></span>



| <span data-ttu-id="e91a3-133">Требование</span><span class="sxs-lookup"><span data-stu-id="e91a3-133">Requirement</span></span> | <span data-ttu-id="e91a3-134">Значение</span><span class="sxs-lookup"><span data-stu-id="e91a3-134">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e91a3-135">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="e91a3-135">Minimum supported client</span></span><br/> | <span data-ttu-id="e91a3-136">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e91a3-136">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="e91a3-137">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="e91a3-137">Minimum supported server</span></span><br/> | <span data-ttu-id="e91a3-138">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e91a3-138">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="e91a3-139">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="e91a3-139">Namespace</span></span><br/>                | <span data-ttu-id="e91a3-140">Корневой \\ CIMv2 \\ терминалсервицес</span><span class="sxs-lookup"><span data-stu-id="e91a3-140">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="e91a3-141">Header</span><span class="sxs-lookup"><span data-stu-id="e91a3-141">Header</span></span><br/>                   | <dl> <span data-ttu-id="e91a3-142"><dt>Факскомекс. h</dt></span><span class="sxs-lookup"><span data-stu-id="e91a3-142"><dt>Faxcomex.h</dt></span></span> </dl>   |
| <span data-ttu-id="e91a3-143">MOF</span><span class="sxs-lookup"><span data-stu-id="e91a3-143">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e91a3-144"><dt>Тскфгвми. mof</dt></span><span class="sxs-lookup"><span data-stu-id="e91a3-144"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="e91a3-145">DLL</span><span class="sxs-lookup"><span data-stu-id="e91a3-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e91a3-146"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e91a3-146"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e91a3-147">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e91a3-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e91a3-148">**\_Тспермиссионссеттинг Win32**</span><span class="sxs-lookup"><span data-stu-id="e91a3-148">**Win32\_TSPermissionsSetting**</span></span>](win32-tspermissionssetting.md)
</dt> </dl>

 

