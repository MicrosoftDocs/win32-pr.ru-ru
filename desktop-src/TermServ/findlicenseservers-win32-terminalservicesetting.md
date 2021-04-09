---
title: Метод Финдлиценсесерверс класса Win32_TerminalServiceSetting
description: Перечисляет все серверы лицензий удаленный рабочий стол и метод обнаружения.
ms.assetid: 0de2ee6f-6c56-4293-84da-131b433c6a9d
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода Финдлиценсесерверс
- Службы удаленных рабочих столов метода Финдлиценсесерверс, класс Win32_TerminalServiceSetting
- Класс Win32_TerminalServiceSetting службы удаленных рабочих столов, метод Финдлиценсесерверс
topic_type:
- apiref
api_name:
- Win32_TerminalServiceSetting.FindLicenseServers
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b83376876009a691fed233cf723f04dcc3bc3c8e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103989252"
---
# <a name="findlicenseservers-method-of-the-win32_terminalservicesetting-class"></a><span data-ttu-id="c69fc-106">Метод Финдлиценсесерверс \_ класса Win32 терминалсервицесеттинг</span><span class="sxs-lookup"><span data-stu-id="c69fc-106">FindLicenseServers method of the Win32\_TerminalServiceSetting class</span></span>

<span data-ttu-id="c69fc-107">Перечисляет все серверы лицензий удаленный рабочий стол и метод обнаружения.</span><span class="sxs-lookup"><span data-stu-id="c69fc-107">Enumerates all of the Remote Desktop license servers, and the method of discovery.</span></span>

## <a name="syntax"></a><span data-ttu-id="c69fc-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c69fc-108">Syntax</span></span>


```mof
uint32 FindLicenseServers(
  [out] Win32_TSDiscoveredLicenseServer LicenseServersList[],
  [out] uint32                          Count
);
```



## <a name="parameters"></a><span data-ttu-id="c69fc-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="c69fc-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c69fc-110">*Лиценсесерверслист* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="c69fc-110">*LicenseServersList* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c69fc-111">Список объектов [**Win32 \_ тсдисковередлиценсесервер**](win32-tsdiscoveredlicenseserver.md) .</span><span class="sxs-lookup"><span data-stu-id="c69fc-111">The list of [**Win32\_TSDiscoveredLicenseServer**](win32-tsdiscoveredlicenseserver.md) objects.</span></span> <span data-ttu-id="c69fc-112">Каждый объект в списке выходных данных имеет имя сервера лицензирования удаленный рабочий стол и метод обнаружения.</span><span class="sxs-lookup"><span data-stu-id="c69fc-112">Each object in the output list has the name of the Remote Desktop license server, and the method of discovery.</span></span>

</dd> <dt>

<span data-ttu-id="c69fc-113">*Количество* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="c69fc-113">*Count* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c69fc-114">Общее число обнаруженных серверов лицензий удаленный рабочий стол в списке выходных данных.</span><span class="sxs-lookup"><span data-stu-id="c69fc-114">The total number of discovered Remote Desktop license servers in the output list.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c69fc-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="c69fc-115">Remarks</span></span>

<span data-ttu-id="c69fc-116">Чтобы подключиться к \\ корневому \\ \\ пространству имен CIMV2 терминалсервицес, уровень проверки подлинности должен включать в себя конфиденциальность пакетов.</span><span class="sxs-lookup"><span data-stu-id="c69fc-116">To connect to the \\root\\CIMV2\\TerminalServices namespace, the authentication level must include packet privacy.</span></span> <span data-ttu-id="c69fc-117">Для вызовов C/C++ это уровень проверки подлинности **AUTHN на \_ \_ \_ уровне \_ \_ безопасности RPC C уровня "PKT**".</span><span class="sxs-lookup"><span data-stu-id="c69fc-117">For C/C++ calls, this is an authentication level of **RPC\_C\_AUTHN\_LEVEL\_PKT\_PRIVACY**.</span></span> <span data-ttu-id="c69fc-118">Для Visual Basic и написания сценариев это уровень проверки подлинности **вбемаусентикатионлевелпктприваци** или "пктприваци" со значением 6.</span><span class="sxs-lookup"><span data-stu-id="c69fc-118">For Visual Basic and scripting calls, this is an authentication level of **WbemAuthenticationLevelPktPrivacy** or "pktPrivacy", with a value of 6.</span></span> <span data-ttu-id="c69fc-119">В следующем примере Visual Basic Scripting Edition (VBScript) показано, как подключиться к удаленному компьютеру с использованием конфиденциальности пакетов.</span><span class="sxs-lookup"><span data-stu-id="c69fc-119">The following Visual Basic Scripting Edition (VBScript) example shows how to connect to a remote computer with packet privacy.</span></span>


```VB
strComputer = "RemoteServer1" 
Set objServices = GetObject( _
    "winmgmts:{authenticationLevel=pktPrivacy}!Root/CIMv2/TerminalServices")
```



<span data-ttu-id="c69fc-120">Файлы MOF-файл (MOF) содержат определения для классов инструментарий управления Windows (WMI) (WMI).</span><span class="sxs-lookup"><span data-stu-id="c69fc-120">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="c69fc-121">MOF-файлы не устанавливаются в составе пакета средств разработки программного обеспечения Microsoft Windows (SDK).</span><span class="sxs-lookup"><span data-stu-id="c69fc-121">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="c69fc-122">Они устанавливаются на сервере при добавлении связанной роли с помощью диспетчер сервера.</span><span class="sxs-lookup"><span data-stu-id="c69fc-122">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="c69fc-123">Дополнительные сведения о файлах MOF см. в разделе [MOF-файл (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="c69fc-123">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="c69fc-124">Требования</span><span class="sxs-lookup"><span data-stu-id="c69fc-124">Requirements</span></span>



| <span data-ttu-id="c69fc-125">Требование</span><span class="sxs-lookup"><span data-stu-id="c69fc-125">Requirement</span></span> | <span data-ttu-id="c69fc-126">Значение</span><span class="sxs-lookup"><span data-stu-id="c69fc-126">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c69fc-127">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="c69fc-127">Minimum supported client</span></span><br/> | <span data-ttu-id="c69fc-128">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="c69fc-128">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="c69fc-129">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="c69fc-129">Minimum supported server</span></span><br/> | <span data-ttu-id="c69fc-130">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c69fc-130">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="c69fc-131">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="c69fc-131">Namespace</span></span><br/>                | <span data-ttu-id="c69fc-132">Корневой \\ CIMv2 \\ терминалсервицес</span><span class="sxs-lookup"><span data-stu-id="c69fc-132">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="c69fc-133">MOF</span><span class="sxs-lookup"><span data-stu-id="c69fc-133">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c69fc-134"><dt>Тскфгвми. mof</dt></span><span class="sxs-lookup"><span data-stu-id="c69fc-134"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="c69fc-135">DLL</span><span class="sxs-lookup"><span data-stu-id="c69fc-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c69fc-136"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c69fc-136"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c69fc-137">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c69fc-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c69fc-138">**\_Терминалсервицесеттинг Win32**</span><span class="sxs-lookup"><span data-stu-id="c69fc-138">**Win32\_TerminalServiceSetting**</span></span>](win32-terminalservicesetting.md)
</dt> </dl>

 

