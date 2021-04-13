---
title: Метод Жетграцепериоддайс класса Win32_TerminalServiceSetting
description: Извлекает количество дней, оставшихся в службы удаленных рабочих столов льготный период лицензирования для сервера узла сеансов удаленный рабочий стол. Нулевое значение указывает, что льготный период истек.
ms.assetid: d84d7815-ee09-43d9-a370-993d23f14898
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода Жетграцепериоддайс
- Службы удаленных рабочих столов метода Жетграцепериоддайс, класс Win32_TerminalServiceSetting
- Класс Win32_TerminalServiceSetting службы удаленных рабочих столов, метод Жетграцепериоддайс
topic_type:
- apiref
api_name:
- Win32_TerminalServiceSetting.GetGracePeriodDays
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0faaf525bb74a8ac4b0164c181e5a20cfb215d7b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104340475"
---
# <a name="getgraceperioddays-method-of-the-win32_terminalservicesetting-class"></a><span data-ttu-id="c4596-107">Метод Жетграцепериоддайс \_ класса Win32 терминалсервицесеттинг</span><span class="sxs-lookup"><span data-stu-id="c4596-107">GetGracePeriodDays method of the Win32\_TerminalServiceSetting class</span></span>

<span data-ttu-id="c4596-108">Извлекает количество дней, оставшихся в службы удаленных рабочих столов льготный период лицензирования для сервера узла сеансов удаленный рабочий стол.</span><span class="sxs-lookup"><span data-stu-id="c4596-108">Retrieves the number of days that are remaining in the Remote Desktop Services licensing grace period for a Remote Desktop Session Host (RD Session Host) server.</span></span> <span data-ttu-id="c4596-109">Нулевое значение указывает, что льготный период истек.</span><span class="sxs-lookup"><span data-stu-id="c4596-109">A zero value indicates that the grace period is over.</span></span>

## <a name="syntax"></a><span data-ttu-id="c4596-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c4596-110">Syntax</span></span>


```mof
uint32 GetGracePeriodDays(
  [out] uint32 DaysLeft
);
```



## <a name="parameters"></a><span data-ttu-id="c4596-111">Параметры</span><span class="sxs-lookup"><span data-stu-id="c4596-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c4596-112">*Дайслефт* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="c4596-112">*DaysLeft* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c4596-113">Количество дней, оставшихся в льготном периоде.</span><span class="sxs-lookup"><span data-stu-id="c4596-113">The number of days that are remaining in the grace period.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c4596-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="c4596-114">Remarks</span></span>

<span data-ttu-id="c4596-115">Чтобы подключиться к \\ корневому \\ \\ пространству имен CIMV2 терминалсервицес, уровень проверки подлинности должен включать в себя конфиденциальность пакетов.</span><span class="sxs-lookup"><span data-stu-id="c4596-115">To connect to the \\root\\CIMV2\\TerminalServices namespace, the authentication level must include packet privacy.</span></span> <span data-ttu-id="c4596-116">Для вызовов C/C++ это уровень проверки подлинности **AUTHN на \_ \_ \_ уровне \_ \_ безопасности RPC C уровня "PKT**".</span><span class="sxs-lookup"><span data-stu-id="c4596-116">For C/C++ calls, this is an authentication level of **RPC\_C\_AUTHN\_LEVEL\_PKT\_PRIVACY**.</span></span> <span data-ttu-id="c4596-117">Для Visual Basic и написания сценариев это уровень проверки подлинности **вбемаусентикатионлевелпктприваци** или "пктприваци" со значением 6.</span><span class="sxs-lookup"><span data-stu-id="c4596-117">For Visual Basic and scripting calls, this is an authentication level of **WbemAuthenticationLevelPktPrivacy** or "pktPrivacy", with a value of 6.</span></span> <span data-ttu-id="c4596-118">В следующем примере Visual Basic Scripting Edition (VBScript) показано, как подключиться к удаленному компьютеру с использованием конфиденциальности пакетов.</span><span class="sxs-lookup"><span data-stu-id="c4596-118">The following Visual Basic Scripting Edition (VBScript) example shows how to connect to a remote computer with packet privacy.</span></span>


```VB
strComputer = "RemoteServer1" 
Set objServices = GetObject( _
    "winmgmts:{authenticationLevel=pktPrivacy}!Root/CIMv2/TerminalServices")
```



<span data-ttu-id="c4596-119">Файлы MOF-файл (MOF) содержат определения для классов инструментарий управления Windows (WMI) (WMI).</span><span class="sxs-lookup"><span data-stu-id="c4596-119">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="c4596-120">MOF-файлы не устанавливаются в составе пакета средств разработки программного обеспечения Microsoft Windows (SDK).</span><span class="sxs-lookup"><span data-stu-id="c4596-120">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="c4596-121">Они устанавливаются на сервере при добавлении связанной роли с помощью диспетчер сервера.</span><span class="sxs-lookup"><span data-stu-id="c4596-121">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="c4596-122">Дополнительные сведения о файлах MOF см. в разделе [MOF-файл (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="c4596-122">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="c4596-123">Требования</span><span class="sxs-lookup"><span data-stu-id="c4596-123">Requirements</span></span>



| <span data-ttu-id="c4596-124">Требование</span><span class="sxs-lookup"><span data-stu-id="c4596-124">Requirement</span></span> | <span data-ttu-id="c4596-125">Значение</span><span class="sxs-lookup"><span data-stu-id="c4596-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c4596-126">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="c4596-126">Minimum supported client</span></span><br/> | <span data-ttu-id="c4596-127">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="c4596-127">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="c4596-128">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="c4596-128">Minimum supported server</span></span><br/> | <span data-ttu-id="c4596-129">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c4596-129">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="c4596-130">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="c4596-130">Namespace</span></span><br/>                | <span data-ttu-id="c4596-131">Корневой \\ CIMv2 \\ терминалсервицес</span><span class="sxs-lookup"><span data-stu-id="c4596-131">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="c4596-132">MOF</span><span class="sxs-lookup"><span data-stu-id="c4596-132">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c4596-133"><dt>Тскфгвми. mof</dt></span><span class="sxs-lookup"><span data-stu-id="c4596-133"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="c4596-134">DLL</span><span class="sxs-lookup"><span data-stu-id="c4596-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c4596-135"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c4596-135"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c4596-136">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c4596-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c4596-137">**\_Терминалсервицесеттинг Win32**</span><span class="sxs-lookup"><span data-stu-id="c4596-137">**Win32\_TerminalServiceSetting**</span></span>](win32-terminalservicesetting.md)
</dt> </dl>

 

