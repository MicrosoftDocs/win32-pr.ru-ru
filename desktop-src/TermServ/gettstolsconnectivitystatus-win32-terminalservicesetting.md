---
title: Метод Жеттстолсконнективитистатус класса Win32_TerminalServiceSetting
description: Определяет состояние подключения между службы удаленных рабочих столов и сервером лицензирования.
ms.assetid: 11fc5865-47e8-4be8-a526-53e29f72d0a4
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода Жеттстолсконнективитистатус
- Службы удаленных рабочих столов метода Жеттстолсконнективитистатус, класс Win32_TerminalServiceSetting
- Класс Win32_TerminalServiceSetting службы удаленных рабочих столов, метод Жеттстолсконнективитистатус
topic_type:
- apiref
api_name:
- Win32_TerminalServiceSetting.GetTStoLSConnectivityStatus
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0fb73cd62c5ab5c343f44f24bbbd8de7f6343a21
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104491340"
---
# <a name="gettstolsconnectivitystatus-method-of-the-win32_terminalservicesetting-class"></a><span data-ttu-id="0b87a-106">Метод Жеттстолсконнективитистатус \_ класса Win32 терминалсервицесеттинг</span><span class="sxs-lookup"><span data-stu-id="0b87a-106">GetTStoLSConnectivityStatus method of the Win32\_TerminalServiceSetting class</span></span>

<span data-ttu-id="0b87a-107">Определяет состояние подключения между службы удаленных рабочих столов и сервером лицензирования.</span><span class="sxs-lookup"><span data-stu-id="0b87a-107">Determines the connectivity status between Remote Desktop Services and a license server.</span></span>

## <a name="syntax"></a><span data-ttu-id="0b87a-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="0b87a-108">Syntax</span></span>


```mof
uint32 GetTStoLSConnectivityStatus(
  [in]  string ServerName,
  [out] uint32 TStoLSConnectivityStatus
);
```



## <a name="parameters"></a><span data-ttu-id="0b87a-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="0b87a-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0b87a-110">*Имя сервера* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="0b87a-110">*ServerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0b87a-111">Имя сервера лицензирования, для которого проверяется состояние подключения.</span><span class="sxs-lookup"><span data-stu-id="0b87a-111">The name of the license server to check the connectivity status of.</span></span>

</dd> <dt>

<span data-ttu-id="0b87a-112">*Тстолсконнективитистатус* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="0b87a-112">*TStoLSConnectivityStatus* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0b87a-113">Значение, указывающее состояние подключения сервера лицензирования.</span><span class="sxs-lookup"><span data-stu-id="0b87a-113">A value that indicates the connectivity status of the license server.</span></span> <span data-ttu-id="0b87a-114">Это может быть одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="0b87a-114">This can be one of the following values.</span></span>

<dt>

<span id="LS_CONNECTABLE_UNKNOWN"></span><span id="ls_connectable_unknown"></span>

<span data-ttu-id="0b87a-115"><span id="LS_CONNECTABLE_UNKNOWN"></span><span id="ls_connectable_unknown"></span>**Лат \_ Неизвестный \_ для подключения** (0)</span><span class="sxs-lookup"><span data-stu-id="0b87a-115"><span id="LS_CONNECTABLE_UNKNOWN"></span><span id="ls_connectable_unknown"></span>**LS\_CONNECTABLE\_UNKNOWN** (0)</span></span>


</dt> <dd>

<span data-ttu-id="0b87a-116">Невозможно определить состояние подключения.</span><span class="sxs-lookup"><span data-stu-id="0b87a-116">The connectivity status cannot be determined.</span></span>

</dd> <dt>

<span id="LS_CONNECTABLE_VALID_WS08R2"></span><span id="ls_connectable_valid_ws08r2"></span>

<span data-ttu-id="0b87a-117"><span id="LS_CONNECTABLE_VALID_WS08R2"></span><span id="ls_connectable_valid_ws08r2"></span>**Лат \_ Подсоединенная \_ допустимая \_ WS08R2** (1)</span><span class="sxs-lookup"><span data-stu-id="0b87a-117"><span id="LS_CONNECTABLE_VALID_WS08R2"></span><span id="ls_connectable_valid_ws08r2"></span>**LS\_CONNECTABLE\_VALID\_WS08R2** (1)</span></span>


</dt> <dd>

<span data-ttu-id="0b87a-118">Службы удаленных рабочих столов может подключиться к серверу лицензирования Windows Server 2008 R2.</span><span class="sxs-lookup"><span data-stu-id="0b87a-118">Remote Desktop Services can connect to the Windows Server 2008 R2 license server.</span></span>

</dd> <dt>

<span id="LS_CONNECTABLE_VALID_WS08"></span><span id="ls_connectable_valid_ws08"></span>

<span data-ttu-id="0b87a-119"><span id="LS_CONNECTABLE_VALID_WS08"></span><span id="ls_connectable_valid_ws08"></span>**Лат \_ Подсоединенная \_ допустимая \_ WS08** (2)</span><span class="sxs-lookup"><span data-stu-id="0b87a-119"><span id="LS_CONNECTABLE_VALID_WS08"></span><span id="ls_connectable_valid_ws08"></span>**LS\_CONNECTABLE\_VALID\_WS08** (2)</span></span>


</dt> <dd>

<span data-ttu-id="0b87a-120">Службы удаленных рабочих столов может подключиться к серверу лицензий Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="0b87a-120">Remote Desktop Services can connect to the Windows Server 2008 license server.</span></span>

</dd> <dt>

<span id="LS_CONNECTABLE_BETA_RTM_MISMATCH"></span><span id="ls_connectable_beta_rtm_mismatch"></span>

<span data-ttu-id="0b87a-121"><span id="LS_CONNECTABLE_BETA_RTM_MISMATCH"></span><span id="ls_connectable_beta_rtm_mismatch"></span>**Лат \_ Несоответствие ПОДКЛЮЧАЕМого \_ бета-версии \_ RTM \_** (3)</span><span class="sxs-lookup"><span data-stu-id="0b87a-121"><span id="LS_CONNECTABLE_BETA_RTM_MISMATCH"></span><span id="ls_connectable_beta_rtm_mismatch"></span>**LS\_CONNECTABLE\_BETA\_RTM\_MISMATCH** (3)</span></span>


</dt> <dd>

<span data-ttu-id="0b87a-122">Службы удаленных рабочих столов может подключиться к серверу лицензирования, но на одном из серверов работает бета-версия операционной системы.</span><span class="sxs-lookup"><span data-stu-id="0b87a-122">Remote Desktop Services can connect to the license server, but one of the servers is running a beta version of the operating system.</span></span>

</dd> <dt>

<span id="LS_CONNECTABLE_LOWER_VERSION"></span><span id="ls_connectable_lower_version"></span>

<span data-ttu-id="0b87a-123"><span id="LS_CONNECTABLE_LOWER_VERSION"></span><span id="ls_connectable_lower_version"></span>**Лат \_ Версия с ПОДКЛЮЧЕНИЕм \_ более ранней \_ версии** (4)</span><span class="sxs-lookup"><span data-stu-id="0b87a-123"><span id="LS_CONNECTABLE_LOWER_VERSION"></span><span id="ls_connectable_lower_version"></span>**LS\_CONNECTABLE\_LOWER\_VERSION** (4)</span></span>


</dt> <dd>

<span data-ttu-id="0b87a-124">Службы удаленных рабочих столов может подключиться к серверу лицензирования, но существует несовместимость между сервером лицензирования и сервером службы удаленных рабочих столов узла.</span><span class="sxs-lookup"><span data-stu-id="0b87a-124">Remote Desktop Services can connect to the license server, but there is an incompatibility between the license server and the Remote Desktop Services host server.</span></span>

</dd> <dt>

<span id="LS_CONNECTABLE_NOT_IN_TSCGROUP"></span><span id="ls_connectable_not_in_tscgroup"></span>

<span data-ttu-id="0b87a-125"><span id="LS_CONNECTABLE_NOT_IN_TSCGROUP"></span><span id="ls_connectable_not_in_tscgroup"></span>**Лат \_ СОЕДИНЕНИЕ \_ не \_ в \_ тскграуп** (5)</span><span class="sxs-lookup"><span data-stu-id="0b87a-125"><span id="LS_CONNECTABLE_NOT_IN_TSCGROUP"></span><span id="ls_connectable_not_in_tscgroup"></span>**LS\_CONNECTABLE\_NOT\_IN\_TSCGROUP** (5)</span></span>


</dt> <dd>

<span data-ttu-id="0b87a-126">Групповая политика безопасности включена на сервере лицензирования, но службы удаленных рабочих столов не является частью групповой политики.</span><span class="sxs-lookup"><span data-stu-id="0b87a-126">Security group policy is enabled in license server, but Remote Desktop Services is not a part of the group policy.</span></span>

</dd> <dt>

<span id="LS_NOT_CONNECTABLE"></span><span id="ls_not_connectable"></span>

<span data-ttu-id="0b87a-127"><span id="LS_NOT_CONNECTABLE"></span><span id="ls_not_connectable"></span>**Лат \_ НЕ \_ подсоединено** (6)</span><span class="sxs-lookup"><span data-stu-id="0b87a-127"><span id="LS_NOT_CONNECTABLE"></span><span id="ls_not_connectable"></span>**LS\_NOT\_CONNECTABLE** (6)</span></span>


</dt> <dd>

<span data-ttu-id="0b87a-128">Службы удаленных рабочих столов не удается подключиться к серверу лицензирования.</span><span class="sxs-lookup"><span data-stu-id="0b87a-128">Remote Desktop Services cannot connect to the license server.</span></span>

</dd> <dt>

<span id="LS_CONNECTABLE_UNKNOWN_VALIDITY"></span><span id="ls_connectable_unknown_validity"></span>

<span data-ttu-id="0b87a-129"><span id="LS_CONNECTABLE_UNKNOWN_VALIDITY"></span><span id="ls_connectable_unknown_validity"></span>**Лат \_ \_Неизвестная \_ достоверность** (7)</span><span class="sxs-lookup"><span data-stu-id="0b87a-129"><span id="LS_CONNECTABLE_UNKNOWN_VALIDITY"></span><span id="ls_connectable_unknown_validity"></span>**LS\_CONNECTABLE\_UNKNOWN\_VALIDITY** (7)</span></span>


</dt> <dd>

<span data-ttu-id="0b87a-130">Сервер лицензирования может быть подключен к, но не удается определить допустимость соединения.</span><span class="sxs-lookup"><span data-stu-id="0b87a-130">The license server can be connected to, but the validity of the connection cannot be determined.</span></span>

</dd> <dt>

<span id="LS_CONNECTABLE_BUT_ACCESS_DENIED"></span><span id="ls_connectable_but_access_denied"></span>

<span data-ttu-id="0b87a-131"><span id="LS_CONNECTABLE_BUT_ACCESS_DENIED"></span><span id="ls_connectable_but_access_denied"></span>**Лат \_ ПОДКЛЮЧЕНИЕ \_ \_ разрешено, но доступ \_ запрещен** (8)</span><span class="sxs-lookup"><span data-stu-id="0b87a-131"><span id="LS_CONNECTABLE_BUT_ACCESS_DENIED"></span><span id="ls_connectable_but_access_denied"></span>**LS\_CONNECTABLE\_BUT\_ACCESS\_DENIED** (8)</span></span>


</dt> <dd>

<span data-ttu-id="0b87a-132">Службы удаленных рабочих столов может подключиться к серверу лицензирования, но учетная запись пользователя не имеет прав администратора на сервере лицензирования.</span><span class="sxs-lookup"><span data-stu-id="0b87a-132">Remote Desktop Services can connect to the license server, but the user account does not have administrator privileges on the license server.</span></span>

</dd> <dt>

<span id="LS_CONNECTABLE_VALID_WS08R2_VDI"></span><span id="ls_connectable_valid_ws08r2_vdi"></span>

<span data-ttu-id="0b87a-133"><span id="LS_CONNECTABLE_VALID_WS08R2_VDI"></span><span id="ls_connectable_valid_ws08r2_vdi"></span>**Лат \_ Подсоединенная \_ допустимая \_ WS08R2 \_ VDI** (9)</span><span class="sxs-lookup"><span data-stu-id="0b87a-133"><span id="LS_CONNECTABLE_VALID_WS08R2_VDI"></span><span id="ls_connectable_valid_ws08r2_vdi"></span>**LS\_CONNECTABLE\_VALID\_WS08R2\_VDI** (9)</span></span>


</dt> <dd>

<span data-ttu-id="0b87a-134">Службы удаленных рабочих столов может подключаться к серверу инфраструктуры виртуальных рабочих столов Windows Server 2008 R2 (VDI).</span><span class="sxs-lookup"><span data-stu-id="0b87a-134">Remote Desktop Services can connect to the Windows Server 2008 R2 Virtual Desktop Infrastructure (VDI) server.</span></span>

<span data-ttu-id="0b87a-135">**Windows Server 2008 R2:** Это значение не поддерживается до Windows Server 2012.</span><span class="sxs-lookup"><span data-stu-id="0b87a-135">**Windows Server 2008 R2:** This value is not supported before Windows Server 2012.</span></span>

</dd> <dt>

<span id="LS_CONNECTABLE_FEATURE_NOT_SUPPORTED"></span><span id="ls_connectable_feature_not_supported"></span>

<span data-ttu-id="0b87a-136"><span id="LS_CONNECTABLE_FEATURE_NOT_SUPPORTED"></span><span id="ls_connectable_feature_not_supported"></span>**Лат \_ Возможность подключения \_ \_ не \_ поддерживается** (10)</span><span class="sxs-lookup"><span data-stu-id="0b87a-136"><span id="LS_CONNECTABLE_FEATURE_NOT_SUPPORTED"></span><span id="ls_connectable_feature_not_supported"></span>**LS\_CONNECTABLE\_FEATURE\_NOT\_SUPPORTED** (10)</span></span>


</dt> <dd>

<span data-ttu-id="0b87a-137">Эта функция не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="0b87a-137">The feature is not supported.</span></span>

<span data-ttu-id="0b87a-138">**Windows server 2008 R2 и Windows server 2008 R2 с пакетом обновления 1 (SP1):** Это значение не поддерживается до Windows Server 2012.</span><span class="sxs-lookup"><span data-stu-id="0b87a-138">**Windows Server 2008 R2 and Windows Server 2008 R2 with SP1:** This value is not supported before Windows Server 2012.</span></span>

</dd> <dt>

<span id="LS_CONNECTABLE_VALID_LS"></span><span id="ls_connectable_valid_ls"></span>

<span data-ttu-id="0b87a-139"><span id="LS_CONNECTABLE_VALID_LS"></span><span id="ls_connectable_valid_ls"></span>**Лат \_ Подсоединенная \_ допустимая \_ Ls** (11)</span><span class="sxs-lookup"><span data-stu-id="0b87a-139"><span id="LS_CONNECTABLE_VALID_LS"></span><span id="ls_connectable_valid_ls"></span>**LS\_CONNECTABLE\_VALID\_LS** (11)</span></span>


</dt> <dd>

<span data-ttu-id="0b87a-140">Сервер лицензирования является допустимым.</span><span class="sxs-lookup"><span data-stu-id="0b87a-140">The license server is valid.</span></span>

<span data-ttu-id="0b87a-141">**Windows server 2008 R2 и Windows server 2008 R2 с пакетом обновления 1 (SP1):** Это значение не поддерживается до Windows Server 2012.</span><span class="sxs-lookup"><span data-stu-id="0b87a-141">**Windows Server 2008 R2 and Windows Server 2008 R2 with SP1:** This value is not supported before Windows Server 2012.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0b87a-142">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="0b87a-142">Return value</span></span>

<span data-ttu-id="0b87a-143">Возвращает значение 0 при успешном выполнении, в противном случае возвращает код ошибки WMI.</span><span class="sxs-lookup"><span data-stu-id="0b87a-143">Returns 0 on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="0b87a-144">Список этих значений см. в разделе [службы удаленных рабочих столов коды ошибок поставщика WMI](terminal-services-wmi-provider-error-codes.md) .</span><span class="sxs-lookup"><span data-stu-id="0b87a-144">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span>

## <a name="requirements"></a><span data-ttu-id="0b87a-145">Требования</span><span class="sxs-lookup"><span data-stu-id="0b87a-145">Requirements</span></span>



| <span data-ttu-id="0b87a-146">Требование</span><span class="sxs-lookup"><span data-stu-id="0b87a-146">Requirement</span></span> | <span data-ttu-id="0b87a-147">Значение</span><span class="sxs-lookup"><span data-stu-id="0b87a-147">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="0b87a-148">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="0b87a-148">Minimum supported client</span></span><br/> | <span data-ttu-id="0b87a-149">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="0b87a-149">None supported</span></span><br/>                                                               |
| <span data-ttu-id="0b87a-150">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="0b87a-150">Minimum supported server</span></span><br/> | <span data-ttu-id="0b87a-151">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="0b87a-151">Windows Server 2008 R2</span></span><br/>                                                       |
| <span data-ttu-id="0b87a-152">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="0b87a-152">Namespace</span></span><br/>                | <span data-ttu-id="0b87a-153">Корневой \\ CIMv2 \\ терминалсервицес</span><span class="sxs-lookup"><span data-stu-id="0b87a-153">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="0b87a-154">MOF</span><span class="sxs-lookup"><span data-stu-id="0b87a-154">MOF</span></span><br/>                      | <dl> <span data-ttu-id="0b87a-155"><dt>Тскфгвми. mof</dt></span><span class="sxs-lookup"><span data-stu-id="0b87a-155"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="0b87a-156">DLL</span><span class="sxs-lookup"><span data-stu-id="0b87a-156">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0b87a-157"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0b87a-157"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0b87a-158">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="0b87a-158">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0b87a-159">**\_Терминалсервицесеттинг Win32**</span><span class="sxs-lookup"><span data-stu-id="0b87a-159">**Win32\_TerminalServiceSetting**</span></span>](win32-terminalservicesetting.md)
</dt> </dl>

 

 





