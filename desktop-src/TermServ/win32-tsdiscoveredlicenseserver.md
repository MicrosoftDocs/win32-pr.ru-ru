---
title: Класс Win32_TSDiscoveredLicenseServer
description: Предоставляет сведения об обнаруженном сервере лицензирования удаленный рабочий стол.
ms.assetid: 88523f30-26ad-4f78-a214-f54b7bc1c676
ms.tgt_platform: multiple
keywords:
- Класс Win32_TSDiscoveredLicenseServer службы удаленных рабочих столов
- Службы удаленных рабочих столов класса Win32_TSDiscoveredLicenseServer, описание
topic_type:
- apiref
api_name:
- Win32_TSDiscoveredLicenseServer
- Win32_TSDiscoveredLicenseServer.LicenseServer
- Win32_TSDiscoveredLicenseServer.HowDiscovered
- Win32_TSDiscoveredLicenseServer.IsLSAvailable
- Win32_TSDiscoveredLicenseServer.IsAdminOnLS
- Win32_TSDiscoveredLicenseServer.IssuingCALs
api_location:
- TSCfgWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d633031df533068f2cf5da65f2f6820a93c78513
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104492717"
---
# <a name="win32_tsdiscoveredlicenseserver-class"></a><span data-ttu-id="ba7d9-105">\_Класс Win32 тсдисковередлиценсесервер</span><span class="sxs-lookup"><span data-stu-id="ba7d9-105">Win32\_TSDiscoveredLicenseServer class</span></span>

<span data-ttu-id="ba7d9-106">Предоставляет сведения об обнаруженном сервере лицензирования удаленный рабочий стол.</span><span class="sxs-lookup"><span data-stu-id="ba7d9-106">Provides details about the discovered Remote Desktop license server.</span></span>

## <a name="syntax"></a><span data-ttu-id="ba7d9-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ba7d9-107">Syntax</span></span>

``` syntax
[abstract, AMENDMENT]
class Win32_TSDiscoveredLicenseServer
{
  string LicenseServer;
  uint32 HowDiscovered;
  uint32 IsLSAvailable;
  uint32 IsAdminOnLS;
  uint32 IssuingCALs;
};
```

## <a name="members"></a><span data-ttu-id="ba7d9-108">Члены</span><span class="sxs-lookup"><span data-stu-id="ba7d9-108">Members</span></span>

<span data-ttu-id="ba7d9-109">Класс **Win32 \_ тсдисковередлиценсесервер** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="ba7d9-109">The **Win32\_TSDiscoveredLicenseServer** class has these types of members:</span></span>

-   [<span data-ttu-id="ba7d9-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="ba7d9-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="ba7d9-111">Свойства</span><span class="sxs-lookup"><span data-stu-id="ba7d9-111">Properties</span></span>

<span data-ttu-id="ba7d9-112">Класс **Win32 \_ тсдисковередлиценсесервер** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="ba7d9-112">The **Win32\_TSDiscoveredLicenseServer** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="ba7d9-113">**ховдисковеред**</span><span class="sxs-lookup"><span data-stu-id="ba7d9-113">**HowDiscovered**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ba7d9-114">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="ba7d9-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ba7d9-115">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ba7d9-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ba7d9-116">Квалификаторы: не [ **рекомендуется**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="ba7d9-116">Qualifiers: [**DEPRECATED**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="ba7d9-117">Это свойство более не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="ba7d9-117">This property is no longer supported.</span></span>

<span data-ttu-id="ba7d9-118">**Windows Server 2008:** Метод обнаружения сервера лицензий удаленный рабочий стол.</span><span class="sxs-lookup"><span data-stu-id="ba7d9-118">**Windows Server 2008:** The Remote Desktop license server discovery method.</span></span>

<dt>

<span id="GroupPolicyConfigured"></span><span id="grouppolicyconfigured"></span><span id="GROUPPOLICYCONFIGURED"></span>

<span data-ttu-id="ba7d9-119"><span id="GroupPolicyConfigured"></span><span id="grouppolicyconfigured"></span><span id="GROUPPOLICYCONFIGURED"></span>**Граупполициконфигуред** (0)</span><span class="sxs-lookup"><span data-stu-id="ba7d9-119"><span id="GroupPolicyConfigured"></span><span id="grouppolicyconfigured"></span><span id="GROUPPOLICYCONFIGURED"></span>**GroupPolicyConfigured** (0)</span></span>


</dt> <dd>

<span data-ttu-id="ba7d9-120">Сервер лицензирования обнаружен с помощью групповой политики.</span><span class="sxs-lookup"><span data-stu-id="ba7d9-120">The license server was discovered by using group policy.</span></span>

</dd> <dt>

<span id="RegistryConfigured"></span><span id="registryconfigured"></span><span id="REGISTRYCONFIGURED"></span>

<span data-ttu-id="ba7d9-121"><span id="RegistryConfigured"></span><span id="registryconfigured"></span><span id="REGISTRYCONFIGURED"></span>**Регистриконфигуред** (1)</span><span class="sxs-lookup"><span data-stu-id="ba7d9-121"><span id="RegistryConfigured"></span><span id="registryconfigured"></span><span id="REGISTRYCONFIGURED"></span>**RegistryConfigured** (1)</span></span>


</dt> <dd>

<span data-ttu-id="ba7d9-122">Сервер лицензирования обнаружен с помощью параметра реестра.</span><span class="sxs-lookup"><span data-stu-id="ba7d9-122">The license server was discovered by using a registry setting.</span></span>

</dd> <dt>

<span id="WorkgroupDiscovery"></span><span id="workgroupdiscovery"></span><span id="WORKGROUPDISCOVERY"></span>

<span data-ttu-id="ba7d9-123"><span id="WorkgroupDiscovery"></span><span id="workgroupdiscovery"></span><span id="WORKGROUPDISCOVERY"></span>**Воркграупдисковери** (2)</span><span class="sxs-lookup"><span data-stu-id="ba7d9-123"><span id="WorkgroupDiscovery"></span><span id="workgroupdiscovery"></span><span id="WORKGROUPDISCOVERY"></span>**WorkgroupDiscovery** (2)</span></span>


</dt> <dd>

<span data-ttu-id="ba7d9-124">Сервер лицензирования обнаружен с помощью области обнаружения рабочих групп.</span><span class="sxs-lookup"><span data-stu-id="ba7d9-124">The license server was discovered by using the workgroup discovery scope.</span></span>

</dd> <dt>

<span id="DomainDiscovery"></span><span id="domaindiscovery"></span><span id="DOMAINDISCOVERY"></span>

<span data-ttu-id="ba7d9-125"><span id="DomainDiscovery"></span><span id="domaindiscovery"></span><span id="DOMAINDISCOVERY"></span>**Домаиндисковери** (3)</span><span class="sxs-lookup"><span data-stu-id="ba7d9-125"><span id="DomainDiscovery"></span><span id="domaindiscovery"></span><span id="DOMAINDISCOVERY"></span>**DomainDiscovery** (3)</span></span>


</dt> <dd>

<span data-ttu-id="ba7d9-126">Сервер лицензирования обнаружен с помощью области обнаружения доменов.</span><span class="sxs-lookup"><span data-stu-id="ba7d9-126">The license server was discovered by using the domain discovery scope.</span></span>

</dd> <dt>

<span id="EnterpriseDiscovery"></span><span id="enterprisediscovery"></span><span id="ENTERPRISEDISCOVERY"></span>

<span data-ttu-id="ba7d9-127"><span id="EnterpriseDiscovery"></span><span id="enterprisediscovery"></span><span id="ENTERPRISEDISCOVERY"></span>**Ентерприседисковери** (4)</span><span class="sxs-lookup"><span data-stu-id="ba7d9-127"><span id="EnterpriseDiscovery"></span><span id="enterprisediscovery"></span><span id="ENTERPRISEDISCOVERY"></span>**EnterpriseDiscovery** (4)</span></span>


</dt> <dd>

<span data-ttu-id="ba7d9-128">Сервер лицензирования обнаружен с помощью области обнаружения в лесах.</span><span class="sxs-lookup"><span data-stu-id="ba7d9-128">The license server was discovered by using the forest discovery scope.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="ba7d9-129">**исадминонлс**</span><span class="sxs-lookup"><span data-stu-id="ba7d9-129">**IsAdminOnLS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ba7d9-130">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="ba7d9-130">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ba7d9-131">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ba7d9-131">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ba7d9-132">Указывает, имеет ли учетная запись, используемая для запуска скрипта или EXE-файла, использование класса **Win32 \_ тсдисковередлиценсесервер** , доступ администратора к серверу лицензирования.</span><span class="sxs-lookup"><span data-stu-id="ba7d9-132">Indicates whether the account that is being used to run the script or .exe file that is using the **Win32\_TSDiscoveredLicenseServer** class has administrator access to the license server.</span></span>

<dt>

<span id="No"></span><span id="no"></span><span id="NO"></span>

<span data-ttu-id="ba7d9-133"><span id="No"></span><span id="no"></span><span id="NO"></span>**Нет** (0)</span><span class="sxs-lookup"><span data-stu-id="ba7d9-133"><span id="No"></span><span id="no"></span><span id="NO"></span>**No** (0)</span></span>


</dt> <dd>

<span data-ttu-id="ba7d9-134">Используемая учетная запись не имеет прав администратора на доступ к серверу лицензирования.</span><span class="sxs-lookup"><span data-stu-id="ba7d9-134">The account that is being used does not have administrator access to the license server.</span></span>

</dd> <dt>

<span id="Yes"></span><span id="yes"></span><span id="YES"></span>

<span data-ttu-id="ba7d9-135"><span id="Yes"></span><span id="yes"></span><span id="YES"></span>**Да** (1)</span><span class="sxs-lookup"><span data-stu-id="ba7d9-135"><span id="Yes"></span><span id="yes"></span><span id="YES"></span>**Yes** (1)</span></span>


</dt> <dd>

<span data-ttu-id="ba7d9-136">Используемая учетная запись имеет права администратора для доступа к серверу лицензирования.</span><span class="sxs-lookup"><span data-stu-id="ba7d9-136">The account that is being used has administrator access to the license server.</span></span>

</dd> <dt>

<span id="Dont_know"></span><span id="dont_know"></span><span id="DONT_KNOW"></span>

<span data-ttu-id="ba7d9-137"><span id="Dont_know"></span><span id="dont_know"></span><span id="DONT_KNOW"></span>**Не, знание** (2)</span><span class="sxs-lookup"><span data-stu-id="ba7d9-137"><span id="Dont_know"></span><span id="dont_know"></span><span id="DONT_KNOW"></span>**Dont know** (2)</span></span>


</dt> <dd>

<span data-ttu-id="ba7d9-138">Невозможно определить, имеет ли используемая учетная запись права администратора для доступа к серверу лицензирования.</span><span class="sxs-lookup"><span data-stu-id="ba7d9-138">It cannot be determined whether the account that is being used has administrator access to the license server.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="ba7d9-139">**ислсаваилабле**</span><span class="sxs-lookup"><span data-stu-id="ba7d9-139">**IsLSAvailable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ba7d9-140">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="ba7d9-140">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ba7d9-141">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ba7d9-141">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ba7d9-142">Указывает, доступен ли сервер лицензирования (удаленно ли RPC-подключение удаленного вызова процедур \[ \] к серверу).</span><span class="sxs-lookup"><span data-stu-id="ba7d9-142">Indicates whether the license server is available (whether a remote procedure call \[RPC\] connection can be made to the server).</span></span>

<dt>

<span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>

<span data-ttu-id="ba7d9-143"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Недоступно** (0)</span><span class="sxs-lookup"><span data-stu-id="ba7d9-143"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (0)</span></span>


</dt> <dd>

<span data-ttu-id="ba7d9-144">Сервер лицензирования недоступен.</span><span class="sxs-lookup"><span data-stu-id="ba7d9-144">The license server is not available.</span></span>

</dd> <dt>

<span id="Available"></span><span id="available"></span><span id="AVAILABLE"></span>

<span data-ttu-id="ba7d9-145"><span id="Available"></span><span id="available"></span><span id="AVAILABLE"></span>**Доступно** (1)</span><span class="sxs-lookup"><span data-stu-id="ba7d9-145"><span id="Available"></span><span id="available"></span><span id="AVAILABLE"></span>**Available** (1)</span></span>


</dt> <dd>

<span data-ttu-id="ba7d9-146">Сервер лицензирования доступен.</span><span class="sxs-lookup"><span data-stu-id="ba7d9-146">The license server is available.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="ba7d9-147">**иссуингкалс**</span><span class="sxs-lookup"><span data-stu-id="ba7d9-147">**IssuingCALs**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ba7d9-148">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="ba7d9-148">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ba7d9-149">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ba7d9-149">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ba7d9-150">Указывает, разрешено ли серверу лицензирования выдавать службы удаленных рабочих столов клиентские лицензии RDS на сервер узла сеансов удаленных рабочих столов.</span><span class="sxs-lookup"><span data-stu-id="ba7d9-150">Indicates whether the license server is allowed to issue Remote Desktop Services client access licenses (RDS CALs) to the RD Session Host server.</span></span>

<dt>

<span id="Not_Allowed"></span><span id="not_allowed"></span><span id="NOT_ALLOWED"></span>

<span data-ttu-id="ba7d9-151"><span id="Not_Allowed"></span><span id="not_allowed"></span><span id="NOT_ALLOWED"></span>**Не разрешено** (0)</span><span class="sxs-lookup"><span data-stu-id="ba7d9-151"><span id="Not_Allowed"></span><span id="not_allowed"></span><span id="NOT_ALLOWED"></span>**Not Allowed** (0)</span></span>


</dt> <dd>

<span data-ttu-id="ba7d9-152">Серверу лицензирования не разрешено выдавать клиентские лицензии RDS серверу узла сеансов удаленных рабочих столов.</span><span class="sxs-lookup"><span data-stu-id="ba7d9-152">The license server is not allowed to issue RDS CALs to the RD Session Host server.</span></span>

</dd> <dt>

<span id="Allowed"></span><span id="allowed"></span><span id="ALLOWED"></span>

<span data-ttu-id="ba7d9-153"><span id="Allowed"></span><span id="allowed"></span><span id="ALLOWED"></span>**Разрешено** (1)</span><span class="sxs-lookup"><span data-stu-id="ba7d9-153"><span id="Allowed"></span><span id="allowed"></span><span id="ALLOWED"></span>**Allowed** (1)</span></span>


</dt> <dd>

<span data-ttu-id="ba7d9-154">Серверу лицензирования разрешено выдавать клиентские лицензии RDS серверу узла сеансов удаленных рабочих столов.</span><span class="sxs-lookup"><span data-stu-id="ba7d9-154">The license server is allowed to issue RDS CALs to the RD Session Host server.</span></span>

</dd> <dt>

<span id="Dont_know"></span><span id="dont_know"></span><span id="DONT_KNOW"></span>

<span data-ttu-id="ba7d9-155"><span id="Dont_know"></span><span id="dont_know"></span><span id="DONT_KNOW"></span>**Не, знание** (2)</span><span class="sxs-lookup"><span data-stu-id="ba7d9-155"><span id="Dont_know"></span><span id="dont_know"></span><span id="DONT_KNOW"></span>**Dont know** (2)</span></span>


</dt> <dd>

<span data-ttu-id="ba7d9-156">Невозможно определить, может ли сервер лицензирования выдавать клиентские лицензии RDS серверу узла сеансов удаленных рабочих столов.</span><span class="sxs-lookup"><span data-stu-id="ba7d9-156">It cannot be determined whether the license server is allowed to issue RDS CALs to the RD Session Host server.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="ba7d9-157">**лиценсесервер**</span><span class="sxs-lookup"><span data-stu-id="ba7d9-157">**LicenseServer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ba7d9-158">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="ba7d9-158">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ba7d9-159">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ba7d9-159">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ba7d9-160">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="ba7d9-160">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="ba7d9-161">Имя обнаруженного сервера лицензирования удаленный рабочий стол.</span><span class="sxs-lookup"><span data-stu-id="ba7d9-161">Name of the discovered Remote Desktop license server.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ba7d9-162">Комментарии</span><span class="sxs-lookup"><span data-stu-id="ba7d9-162">Remarks</span></span>

<span data-ttu-id="ba7d9-163">Чтобы подключиться к \\ корневому \\ \\ пространству имен CIMV2 терминалсервицес, уровень проверки подлинности должен включать в себя конфиденциальность пакетов.</span><span class="sxs-lookup"><span data-stu-id="ba7d9-163">To connect to the \\root\\CIMV2\\TerminalServices namespace, the authentication level must include packet privacy.</span></span> <span data-ttu-id="ba7d9-164">Для вызовов C/C++ это уровень проверки подлинности **AUTHN на \_ \_ \_ уровне \_ \_ безопасности RPC C уровня "PKT**".</span><span class="sxs-lookup"><span data-stu-id="ba7d9-164">For C/C++ calls, this is an authentication level of **RPC\_C\_AUTHN\_LEVEL\_PKT\_PRIVACY**.</span></span> <span data-ttu-id="ba7d9-165">Для Visual Basic и написания сценариев это уровень проверки подлинности **вбемаусентикатионлевелпктприваци** или "пктприваци" со значением 6.</span><span class="sxs-lookup"><span data-stu-id="ba7d9-165">For Visual Basic and scripting calls, this is an authentication level of **WbemAuthenticationLevelPktPrivacy** or "pktPrivacy", with a value of 6.</span></span> <span data-ttu-id="ba7d9-166">В следующем примере Visual Basic Scripting Edition (VBScript) показано, как подключиться к удаленному компьютеру с использованием конфиденциальности пакетов.</span><span class="sxs-lookup"><span data-stu-id="ba7d9-166">The following Visual Basic Scripting Edition (VBScript) example shows how to connect to a remote computer with packet privacy.</span></span>


```VB
strComputer = "RemoteServer1" 
Set objServices = GetObject( _
    "winmgmts:{authenticationLevel=pktPrivacy}!Root/CIMv2/TerminalServices")
```



<span data-ttu-id="ba7d9-167">Файлы MOF-файл (MOF) содержат определения для классов инструментарий управления Windows (WMI) (WMI).</span><span class="sxs-lookup"><span data-stu-id="ba7d9-167">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="ba7d9-168">MOF-файлы не устанавливаются в составе пакета средств разработки программного обеспечения Microsoft Windows (SDK).</span><span class="sxs-lookup"><span data-stu-id="ba7d9-168">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="ba7d9-169">Они устанавливаются на сервере при добавлении связанной роли с помощью диспетчер сервера.</span><span class="sxs-lookup"><span data-stu-id="ba7d9-169">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="ba7d9-170">Дополнительные сведения о файлах MOF см. в разделе [MOF-файл (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="ba7d9-170">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="ba7d9-171">Требования</span><span class="sxs-lookup"><span data-stu-id="ba7d9-171">Requirements</span></span>



| <span data-ttu-id="ba7d9-172">Требование</span><span class="sxs-lookup"><span data-stu-id="ba7d9-172">Requirement</span></span> | <span data-ttu-id="ba7d9-173">Значение</span><span class="sxs-lookup"><span data-stu-id="ba7d9-173">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ba7d9-174">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="ba7d9-174">Minimum supported client</span></span><br/> | <span data-ttu-id="ba7d9-175">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="ba7d9-175">None supported</span></span><br/>                                                               |
| <span data-ttu-id="ba7d9-176">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="ba7d9-176">Minimum supported server</span></span><br/> | <span data-ttu-id="ba7d9-177">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ba7d9-177">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="ba7d9-178">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="ba7d9-178">Namespace</span></span><br/>                | <span data-ttu-id="ba7d9-179">Корневой \\ CIMv2 \\ терминалсервицес</span><span class="sxs-lookup"><span data-stu-id="ba7d9-179">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="ba7d9-180">MOF</span><span class="sxs-lookup"><span data-stu-id="ba7d9-180">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ba7d9-181"><dt>Тскфгвми. mof</dt></span><span class="sxs-lookup"><span data-stu-id="ba7d9-181"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="ba7d9-182">DLL</span><span class="sxs-lookup"><span data-stu-id="ba7d9-182">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ba7d9-183"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ba7d9-183"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



 

