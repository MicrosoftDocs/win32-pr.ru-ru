---
title: Метод Канакцесслиценсесервер класса Win32_TerminalServiceSetting
description: Канакцесслиценсесервер больше не доступен.
ms.assetid: b09fa901-8ae1-431e-8d97-27ee84a84779
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода Канакцесслиценсесервер
- Службы удаленных рабочих столов метода Канакцесслиценсесервер, класс Win32_TerminalServiceSetting
- Класс Win32_TerminalServiceSetting службы удаленных рабочих столов, метод Канакцесслиценсесервер
topic_type:
- apiref
api_name:
- Win32_TerminalServiceSetting.CanAccessLicenseServer
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6ffa5bd0e108c0ccceed6890adedea7901834804
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104135407"
---
# <a name="canaccesslicenseserver-method-of-the-win32_terminalservicesetting-class"></a><span data-ttu-id="8a3ad-106">Метод Канакцесслиценсесервер \_ класса Win32 терминалсервицесеттинг</span><span class="sxs-lookup"><span data-stu-id="8a3ad-106">CanAccessLicenseServer method of the Win32\_TerminalServiceSetting class</span></span>

<span data-ttu-id="8a3ad-107">\[**Канакцесслиценсесервер** больше не доступен для использования в Windows Server 2008 R2.\]</span><span class="sxs-lookup"><span data-stu-id="8a3ad-107">\[**CanAccessLicenseServer** is no longer available for use as of Windows Server 2008 R2.\]</span></span>

<span data-ttu-id="8a3ad-108">\* \* Windows Server 2008: \* \*</span><span class="sxs-lookup"><span data-stu-id="8a3ad-108">\*\*Windows Server 2008:  \*\*</span></span>

<span data-ttu-id="8a3ad-109">Определяет, может ли сервер узла сеансов удаленный рабочий стол (узел сеансов удаленных рабочих столов) запрашивать службы удаленных рабочих столов лицензий клиентского доступа (RDS CAL) с сервера лицензий удаленный рабочий стол на основе следующих данных:</span><span class="sxs-lookup"><span data-stu-id="8a3ad-109">Determines whether the Remote Desktop Session Host (RD Session Host) server is allowed to request Remote Desktop Services client access licenses (RDS CALs) from a Remote Desktop license server based on the following:</span></span>

-   <span data-ttu-id="8a3ad-110">Параметр групповой политики "Группа безопасности сервера лицензий" на сервере лицензирования удаленный рабочий стол.</span><span class="sxs-lookup"><span data-stu-id="8a3ad-110">The "license server security group" group policy setting on the Remote Desktop license server.</span></span>
-   <span data-ttu-id="8a3ad-111">Членство в локальной группе компьютеры сервера терминалов на сервере лицензирования.</span><span class="sxs-lookup"><span data-stu-id="8a3ad-111">Membership in the Terminal Server Computers local group on the license server.</span></span>

## <a name="syntax"></a><span data-ttu-id="8a3ad-112">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="8a3ad-112">Syntax</span></span>


```mof
uint32 CanAccessLicenseServer(
  [in]  string ServerName,
  [out] uint32 AccessAllowed
);
```



## <a name="parameters"></a><span data-ttu-id="8a3ad-113">Параметры</span><span class="sxs-lookup"><span data-stu-id="8a3ad-113">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8a3ad-114">*Имя сервера* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="8a3ad-114">*ServerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8a3ad-115">Имя сервера лицензий удаленный рабочий стол.</span><span class="sxs-lookup"><span data-stu-id="8a3ad-115">The name of the Remote Desktop license server.</span></span>

</dd> <dt>

<span data-ttu-id="8a3ad-116">*Акцессалловед* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="8a3ad-116">*AccessAllowed* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8a3ad-117">Разрешено ли серверу узла сеансов удаленных рабочих столов запрашивать клиентские лицензии RDS с сервера лицензирования.</span><span class="sxs-lookup"><span data-stu-id="8a3ad-117">Whether the RD Session Host server is allowed to request RDS CALs from the license server.</span></span>

<dt>

<span data-ttu-id="8a3ad-118">0</span><span class="sxs-lookup"><span data-stu-id="8a3ad-118">0</span></span>
</dt> <dd>

<span data-ttu-id="8a3ad-119">Запрос разрешен.</span><span class="sxs-lookup"><span data-stu-id="8a3ad-119">The request is allowed.</span></span>

</dd> <dt>

<span data-ttu-id="8a3ad-120">1</span><span class="sxs-lookup"><span data-stu-id="8a3ad-120">1</span></span>
</dt> <dd>

<span data-ttu-id="8a3ad-121">Запрос не разрешен.</span><span class="sxs-lookup"><span data-stu-id="8a3ad-121">The request is not allowed.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8a3ad-122">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="8a3ad-122">Return value</span></span>

<span data-ttu-id="8a3ad-123">Возвращает **значение \_ ОК** , если сервер узла сеансов удаленных рабочих столов имеет доступ к серверу лицензирования.</span><span class="sxs-lookup"><span data-stu-id="8a3ad-123">Returns **S\_OK** if the RD Session Host server has access to the license server.</span></span> <span data-ttu-id="8a3ad-124">Возвращает **\_ значение false** , если сервер узла сеансов удаленных рабочих столов не имеет доступа к серверу лицензирования.</span><span class="sxs-lookup"><span data-stu-id="8a3ad-124">Returns **S\_FALSE** if the RD Session Host server does not have access to the license server.</span></span>

## <a name="remarks"></a><span data-ttu-id="8a3ad-125">Комментарии</span><span class="sxs-lookup"><span data-stu-id="8a3ad-125">Remarks</span></span>

<span data-ttu-id="8a3ad-126">Параметр политики "Группа безопасности сервера лицензий" позволяет указать серверы узла сеансов удаленных рабочих столов, которым разрешено обращаться к серверу лицензирования для получения клиентских лицензий служб удаленных рабочих столов.</span><span class="sxs-lookup"><span data-stu-id="8a3ad-126">The "license server security group" policy setting allows you to specify the RD Session Host servers that are permitted to contact the license server to obtain RDS CALs.</span></span> <span data-ttu-id="8a3ad-127">Если на сервере лицензирования включен параметр политики, сервер лицензирования будет отвечать только на запросы клиентских лицензий служб удаленных рабочих столов, которые являются членами локальной группы "компьютеры сервера терминалов" на сервере лицензирования.</span><span class="sxs-lookup"><span data-stu-id="8a3ad-127">If the policy setting is enabled on the license server, the license server will only respond to RDS CAL requests from RD Session Host servers whose computer accounts are members of the Terminal Server Computers local group on the license server.</span></span>

<span data-ttu-id="8a3ad-128">Чтобы подключиться к \\ корневому \\ \\ пространству имен CIMV2 терминалсервицес, уровень проверки подлинности должен включать в себя конфиденциальность пакетов.</span><span class="sxs-lookup"><span data-stu-id="8a3ad-128">To connect to the \\root\\CIMV2\\TerminalServices namespace, the authentication level must include packet privacy.</span></span> <span data-ttu-id="8a3ad-129">Для вызовов C/C++ это уровень проверки подлинности **AUTHN на \_ \_ \_ уровне \_ \_ безопасности RPC C уровня "PKT**".</span><span class="sxs-lookup"><span data-stu-id="8a3ad-129">For C/C++ calls, this is an authentication level of **RPC\_C\_AUTHN\_LEVEL\_PKT\_PRIVACY**.</span></span> <span data-ttu-id="8a3ad-130">Для Visual Basic и написания сценариев это уровень проверки подлинности **вбемаусентикатионлевелпктприваци** или "пктприваци" со значением 6.</span><span class="sxs-lookup"><span data-stu-id="8a3ad-130">For Visual Basic and scripting calls, this is an authentication level of **WbemAuthenticationLevelPktPrivacy** or "pktPrivacy", with a value of 6.</span></span> <span data-ttu-id="8a3ad-131">В следующем примере Visual Basic Scripting Edition (VBScript) показано, как подключиться к удаленному компьютеру с использованием конфиденциальности пакетов.</span><span class="sxs-lookup"><span data-stu-id="8a3ad-131">The following Visual Basic Scripting Edition (VBScript) example shows how to connect to a remote computer with packet privacy.</span></span>


```VB
strComputer = "RemoteServer1" 
Set objServices = GetObject( _
    "winmgmts:{authenticationLevel=pktPrivacy}!Root/CIMv2/TerminalServices")
```



<span data-ttu-id="8a3ad-132">Файлы MOF-файл (MOF) содержат определения для классов инструментарий управления Windows (WMI) (WMI).</span><span class="sxs-lookup"><span data-stu-id="8a3ad-132">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="8a3ad-133">MOF-файлы не устанавливаются в составе пакета средств разработки программного обеспечения Microsoft Windows (SDK).</span><span class="sxs-lookup"><span data-stu-id="8a3ad-133">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="8a3ad-134">Они устанавливаются на сервере при добавлении связанной роли с помощью диспетчер сервера.</span><span class="sxs-lookup"><span data-stu-id="8a3ad-134">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="8a3ad-135">Дополнительные сведения о файлах MOF см. в разделе [MOF-файл (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="8a3ad-135">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="8a3ad-136">Требования</span><span class="sxs-lookup"><span data-stu-id="8a3ad-136">Requirements</span></span>



| <span data-ttu-id="8a3ad-137">Требование</span><span class="sxs-lookup"><span data-stu-id="8a3ad-137">Requirement</span></span> | <span data-ttu-id="8a3ad-138">Значение</span><span class="sxs-lookup"><span data-stu-id="8a3ad-138">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="8a3ad-139">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="8a3ad-139">Minimum supported client</span></span><br/> | <span data-ttu-id="8a3ad-140">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="8a3ad-140">None supported</span></span><br/>                                                               |
| <span data-ttu-id="8a3ad-141">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="8a3ad-141">Minimum supported server</span></span><br/> | <span data-ttu-id="8a3ad-142">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="8a3ad-142">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="8a3ad-143">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="8a3ad-143">End of client support</span></span><br/>    | <span data-ttu-id="8a3ad-144">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="8a3ad-144">None supported</span></span><br/>                                                               |
| <span data-ttu-id="8a3ad-145">Поддержка конца сервера</span><span class="sxs-lookup"><span data-stu-id="8a3ad-145">End of server support</span></span><br/>    | <span data-ttu-id="8a3ad-146">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="8a3ad-146">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="8a3ad-147">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="8a3ad-147">Namespace</span></span><br/>                | <span data-ttu-id="8a3ad-148">Корневой \\ CIMv2 \\ терминалсервицес</span><span class="sxs-lookup"><span data-stu-id="8a3ad-148">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="8a3ad-149">MOF</span><span class="sxs-lookup"><span data-stu-id="8a3ad-149">MOF</span></span><br/>                      | <dl> <span data-ttu-id="8a3ad-150"><dt>Тскфгвми. mof</dt></span><span class="sxs-lookup"><span data-stu-id="8a3ad-150"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="8a3ad-151">DLL</span><span class="sxs-lookup"><span data-stu-id="8a3ad-151">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8a3ad-152"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8a3ad-152"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8a3ad-153">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="8a3ad-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8a3ad-154">**\_Терминалсервицесеттинг Win32**</span><span class="sxs-lookup"><span data-stu-id="8a3ad-154">**Win32\_TerminalServiceSetting**</span></span>](win32-terminalservicesetting.md)
</dt> </dl>

 

