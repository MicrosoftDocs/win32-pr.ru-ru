---
title: Метод Сеталловтсконнектионс класса Win32_TerminalServiceSetting
description: Метод Сеталловтсконнектионс разрешает или запрещает новые подключения к удаленному рабочему столу. Этот метод соответствующим образом изменит свойство Алловтсконнектионс для класса.
ms.assetid: 6cbaea62-ced0-4788-99fb-5b36816b80a1
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода Сеталловтсконнектионс
- Службы удаленных рабочих столов метода Сеталловтсконнектионс, класс Win32_TerminalServiceSetting
- Класс Win32_TerminalServiceSetting службы удаленных рабочих столов, метод Сеталловтсконнектионс
topic_type:
- apiref
api_name:
- Win32_TerminalServiceSetting.SetAllowTSConnections
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e800f1a47567f16d916563d4d1e62c767016329a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104492726"
---
# <a name="setallowtsconnections-method-of-the-win32_terminalservicesetting-class"></a><span data-ttu-id="627cc-107">Метод Сеталловтсконнектионс \_ класса Win32 терминалсервицесеттинг</span><span class="sxs-lookup"><span data-stu-id="627cc-107">SetAllowTSConnections method of the Win32\_TerminalServiceSetting class</span></span>

<span data-ttu-id="627cc-108">Метод **сеталловтсконнектионс** разрешает или запрещает новые подключения к удаленному рабочему столу.</span><span class="sxs-lookup"><span data-stu-id="627cc-108">The **SetAllowTSConnections** method allows or denies new remote desktop connections.</span></span> <span data-ttu-id="627cc-109">Этот метод соответствующим образом изменит свойство **алловтсконнектионс** для класса.</span><span class="sxs-lookup"><span data-stu-id="627cc-109">This method will modify the **AllowTSConnections** property for the class accordingly.</span></span>

## <a name="syntax"></a><span data-ttu-id="627cc-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="627cc-110">Syntax</span></span>


```mof
uint32 SetAllowTSConnections(
  [in] uint32 AllowTSConnections,
  [in] uint32 ModifyFirewallException
);
```



## <a name="parameters"></a><span data-ttu-id="627cc-111">Параметры</span><span class="sxs-lookup"><span data-stu-id="627cc-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="627cc-112">*Алловтсконнектионс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="627cc-112">*AllowTSConnections* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="627cc-113">Указывает, разрешены ли новые подключения к удаленному рабочему столу.</span><span class="sxs-lookup"><span data-stu-id="627cc-113">Specifies whether new remote desktop connections are allowed.</span></span> <span data-ttu-id="627cc-114">Это должно быть одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="627cc-114">This must be one of the following values.</span></span>

<dt>

<span id="0"></span>

<span data-ttu-id="627cc-115"><span id="0"></span>**0,0**</span><span class="sxs-lookup"><span data-stu-id="627cc-115"><span id="0"></span>**0**</span></span>


</dt> <dd>

<span data-ttu-id="627cc-116">Новые подключения не допускаются.</span><span class="sxs-lookup"><span data-stu-id="627cc-116">New connections are not allowed.</span></span> <span data-ttu-id="627cc-117">Если параметр *модифифиреваллексцептион* имеет значение 1, то исключение брандмауэра удаленный рабочий стол отключено.</span><span class="sxs-lookup"><span data-stu-id="627cc-117">If the *ModifyFirewallException* parameter is 1, then the Remote Desktop firewall exception is disabled.</span></span>

</dd> <dt>

<span id="1"></span>

<span data-ttu-id="627cc-118"><span id="1"></span>**1**</span><span class="sxs-lookup"><span data-stu-id="627cc-118"><span id="1"></span>**1**</span></span>


</dt> <dd>

<span data-ttu-id="627cc-119">Новые подключения разрешены.</span><span class="sxs-lookup"><span data-stu-id="627cc-119">New connections are allowed.</span></span> <span data-ttu-id="627cc-120">Если параметр *модифифиреваллексцептион* имеет значение 1, то удаленный рабочий стол исключение брандмауэра включено.</span><span class="sxs-lookup"><span data-stu-id="627cc-120">If the *ModifyFirewallException* parameter is 1, then the Remote Desktop firewall exception is enabled.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="627cc-121">*Модифифиреваллексцептион* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="627cc-121">*ModifyFirewallException* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="627cc-122">Указывает, будет ли параметр исключения брандмауэра для удаленный рабочий стол изменен в состояние, указанное параметром *алловтсконнектионс* .</span><span class="sxs-lookup"><span data-stu-id="627cc-122">Specifies if the firewall exception setting for Remote Desktop will be modified to the state specified by the *AllowTSConnections* parameter.</span></span> <span data-ttu-id="627cc-123">Это должно быть одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="627cc-123">This must be one of the following values.</span></span>

<dt>

<span id="0"></span>

<span data-ttu-id="627cc-124"><span id="0"></span>**0,0**</span><span class="sxs-lookup"><span data-stu-id="627cc-124"><span id="0"></span>**0**</span></span>


</dt> <dd>

<span data-ttu-id="627cc-125">Не изменяйте параметр исключения брандмауэра.</span><span class="sxs-lookup"><span data-stu-id="627cc-125">Do not modify the firewall exception setting.</span></span>

</dd> <dt>

<span id="1"></span>

<span data-ttu-id="627cc-126"><span id="1"></span>**1**</span><span class="sxs-lookup"><span data-stu-id="627cc-126"><span id="1"></span>**1**</span></span>


</dt> <dd>

<span data-ttu-id="627cc-127">Измените параметр исключения брандмауэра.</span><span class="sxs-lookup"><span data-stu-id="627cc-127">Modify the firewall exception setting.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="627cc-128">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="627cc-128">Return value</span></span>

<span data-ttu-id="627cc-129">Возвращает успешное завершение; в противном случае возвращает код ошибки WMI.</span><span class="sxs-lookup"><span data-stu-id="627cc-129">Returns Success on success; otherwise, returns a WMI error code.</span></span> <span data-ttu-id="627cc-130">Список этих значений см. в разделе [службы удаленных рабочих столов коды ошибок поставщика WMI](terminal-services-wmi-provider-error-codes.md) .</span><span class="sxs-lookup"><span data-stu-id="627cc-130">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span> <span data-ttu-id="627cc-131">Метод возвращает ошибку, если параметр находится в разделе Управление групповой политикой.</span><span class="sxs-lookup"><span data-stu-id="627cc-131">The method returns an error if the setting is under group policy control.</span></span>

## <a name="remarks"></a><span data-ttu-id="627cc-132">Комментарии</span><span class="sxs-lookup"><span data-stu-id="627cc-132">Remarks</span></span>

<span data-ttu-id="627cc-133">Файлы MOF-файл (MOF) содержат определения для классов инструментарий управления Windows (WMI) (WMI).</span><span class="sxs-lookup"><span data-stu-id="627cc-133">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="627cc-134">MOF-файлы не устанавливаются в составе пакета средств разработки программного обеспечения Microsoft Windows (SDK).</span><span class="sxs-lookup"><span data-stu-id="627cc-134">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="627cc-135">Они устанавливаются на сервере при добавлении связанной роли с помощью диспетчер сервера.</span><span class="sxs-lookup"><span data-stu-id="627cc-135">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="627cc-136">Дополнительные сведения о файлах MOF см. в разделе [MOF-файл (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="627cc-136">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="627cc-137">Требования</span><span class="sxs-lookup"><span data-stu-id="627cc-137">Requirements</span></span>



| <span data-ttu-id="627cc-138">Требование</span><span class="sxs-lookup"><span data-stu-id="627cc-138">Requirement</span></span> | <span data-ttu-id="627cc-139">Значение</span><span class="sxs-lookup"><span data-stu-id="627cc-139">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="627cc-140">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="627cc-140">Minimum supported client</span></span><br/> | <span data-ttu-id="627cc-141">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="627cc-141">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="627cc-142">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="627cc-142">Minimum supported server</span></span><br/> | <span data-ttu-id="627cc-143">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="627cc-143">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="627cc-144">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="627cc-144">Namespace</span></span><br/>                | <span data-ttu-id="627cc-145">Корневой \\ CIMv2 \\ терминалсервицес</span><span class="sxs-lookup"><span data-stu-id="627cc-145">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="627cc-146">MOF</span><span class="sxs-lookup"><span data-stu-id="627cc-146">MOF</span></span><br/>                      | <dl> <span data-ttu-id="627cc-147"><dt>Тскфгвми. mof</dt></span><span class="sxs-lookup"><span data-stu-id="627cc-147"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="627cc-148">DLL</span><span class="sxs-lookup"><span data-stu-id="627cc-148">DLL</span></span><br/>                      | <dl> <span data-ttu-id="627cc-149"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="627cc-149"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="627cc-150">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="627cc-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="627cc-151">**\_Терминалсервицесеттинг Win32**</span><span class="sxs-lookup"><span data-stu-id="627cc-151">**Win32\_TerminalServiceSetting**</span></span>](win32-terminalservicesetting.md)
</dt> </dl>

 

