---
title: Метод Жетвинстатиондривернамес класса Win32_TerminalServiceSetting
description: Возвращает список имен драйверов Винстатион.
ms.assetid: 578c2a07-17e7-4bd6-b520-942cd48ee40f
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода Жетвинстатиондривернамес
- Службы удаленных рабочих столов метода Жетвинстатиондривернамес, класс Win32_TerminalServiceSetting
- Класс Win32_TerminalServiceSetting службы удаленных рабочих столов, метод Жетвинстатиондривернамес
topic_type:
- apiref
api_name:
- Win32_TerminalServiceSetting.GetWinstationDriverNames
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 41bc0157f368edf129f578765c1b8d73f6f48a33
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105681840"
---
# <a name="getwinstationdrivernames-method-of-the-win32_terminalservicesetting-class"></a><span data-ttu-id="d1016-106">Метод Жетвинстатиондривернамес \_ класса Win32 терминалсервицесеттинг</span><span class="sxs-lookup"><span data-stu-id="d1016-106">GetWinstationDriverNames method of the Win32\_TerminalServiceSetting class</span></span>

<span data-ttu-id="d1016-107">Возвращает список имен драйверов Винстатион.</span><span class="sxs-lookup"><span data-stu-id="d1016-107">Retrieves a list of Winstation driver names.</span></span>

## <a name="syntax"></a><span data-ttu-id="d1016-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d1016-108">Syntax</span></span>


```mof
uint32 GetWinstationDriverNames(
  [out] string WinstaDriverNames[]
);
```



## <a name="parameters"></a><span data-ttu-id="d1016-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="d1016-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d1016-110">*Винстадривернамес* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="d1016-110">*WinstaDriverNames* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d1016-111">Список имен драйверов Винстатион.</span><span class="sxs-lookup"><span data-stu-id="d1016-111">The list of Winstation driver names.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d1016-112">Комментарии</span><span class="sxs-lookup"><span data-stu-id="d1016-112">Remarks</span></span>

<span data-ttu-id="d1016-113">Чтобы подключиться к \\ корневому \\ \\ пространству имен CIMV2 терминалсервицес, уровень проверки подлинности должен включать в себя конфиденциальность пакетов.</span><span class="sxs-lookup"><span data-stu-id="d1016-113">To connect to the \\root\\CIMV2\\TerminalServices namespace, the authentication level must include packet privacy.</span></span> <span data-ttu-id="d1016-114">Для вызовов C/C++ это уровень проверки подлинности **AUTHN на \_ \_ \_ уровне \_ \_ безопасности RPC C уровня "PKT**".</span><span class="sxs-lookup"><span data-stu-id="d1016-114">For C/C++ calls, this is an authentication level of **RPC\_C\_AUTHN\_LEVEL\_PKT\_PRIVACY**.</span></span> <span data-ttu-id="d1016-115">Для Visual Basic и написания сценариев это уровень проверки подлинности **вбемаусентикатионлевелпктприваци** или "пктприваци" со значением 6.</span><span class="sxs-lookup"><span data-stu-id="d1016-115">For Visual Basic and scripting calls, this is an authentication level of **WbemAuthenticationLevelPktPrivacy** or "pktPrivacy", with a value of 6.</span></span> <span data-ttu-id="d1016-116">В следующем примере Visual Basic Scripting Edition (VBScript) показано, как подключиться к удаленному компьютеру с использованием конфиденциальности пакетов.</span><span class="sxs-lookup"><span data-stu-id="d1016-116">The following Visual Basic Scripting Edition (VBScript) example shows how to connect to a remote computer with packet privacy.</span></span>


```VB
strComputer = "RemoteServer1" 
Set objServices = GetObject( _
    "winmgmts:{authenticationLevel=pktPrivacy}!Root/CIMv2/TerminalServices")
```



<span data-ttu-id="d1016-117">Файлы MOF-файл (MOF) содержат определения для классов инструментарий управления Windows (WMI) (WMI).</span><span class="sxs-lookup"><span data-stu-id="d1016-117">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="d1016-118">MOF-файлы не устанавливаются в составе пакета средств разработки программного обеспечения Microsoft Windows (SDK).</span><span class="sxs-lookup"><span data-stu-id="d1016-118">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="d1016-119">Они устанавливаются на сервере при добавлении связанной роли с помощью диспетчер сервера.</span><span class="sxs-lookup"><span data-stu-id="d1016-119">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="d1016-120">Дополнительные сведения о файлах MOF см. в разделе [MOF-файл (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="d1016-120">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="d1016-121">Требования</span><span class="sxs-lookup"><span data-stu-id="d1016-121">Requirements</span></span>



| <span data-ttu-id="d1016-122">Требование</span><span class="sxs-lookup"><span data-stu-id="d1016-122">Requirement</span></span> | <span data-ttu-id="d1016-123">Значение</span><span class="sxs-lookup"><span data-stu-id="d1016-123">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d1016-124">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="d1016-124">Minimum supported client</span></span><br/> | <span data-ttu-id="d1016-125">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="d1016-125">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="d1016-126">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="d1016-126">Minimum supported server</span></span><br/> | <span data-ttu-id="d1016-127">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d1016-127">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="d1016-128">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="d1016-128">Namespace</span></span><br/>                | <span data-ttu-id="d1016-129">Корневой \\ CIMv2 \\ терминалсервицес</span><span class="sxs-lookup"><span data-stu-id="d1016-129">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="d1016-130">MOF</span><span class="sxs-lookup"><span data-stu-id="d1016-130">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d1016-131"><dt>Тскфгвми. mof</dt></span><span class="sxs-lookup"><span data-stu-id="d1016-131"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="d1016-132">DLL</span><span class="sxs-lookup"><span data-stu-id="d1016-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d1016-133"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d1016-133"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d1016-134">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d1016-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d1016-135">**\_Терминалсервицесеттинг Win32**</span><span class="sxs-lookup"><span data-stu-id="d1016-135">**Win32\_TerminalServiceSetting**</span></span>](win32-terminalservicesetting.md)
</dt> </dl>

 

