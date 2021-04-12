---
title: Метод Чанжемоде класса Win32_TerminalServiceSetting
description: Метод Чанжемоде задает тип лицензирования текущего сервера узла сеансов удаленный рабочий стол (узла сеансов удаленных рабочих столов).
ms.assetid: 293483ee-51ce-4cd4-ba13-6c7c02bbdbbf
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода Чанжемоде
- Службы удаленных рабочих столов метода Чанжемоде, класс Win32_TerminalServiceSetting
- Класс Win32_TerminalServiceSetting службы удаленных рабочих столов, метод Чанжемоде
topic_type:
- apiref
api_name:
- Win32_TerminalServiceSetting.ChangeMode
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 880fcab8aa68e49c6b3c00278b90635686de6168
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104415421"
---
# <a name="changemode-method-of-the-win32_terminalservicesetting-class"></a><span data-ttu-id="7c427-106">Метод Чанжемоде \_ класса Win32 терминалсервицесеттинг</span><span class="sxs-lookup"><span data-stu-id="7c427-106">ChangeMode method of the Win32\_TerminalServiceSetting class</span></span>

<span data-ttu-id="7c427-107">Метод **чанжемоде** задает тип лицензирования текущего сервера узла сеансов удаленный рабочий стол (узла сеансов удаленных рабочих столов).</span><span class="sxs-lookup"><span data-stu-id="7c427-107">The **ChangeMode** method sets the licensing type of the current Remote Desktop Session Host (RD Session Host) server.</span></span>

## <a name="syntax"></a><span data-ttu-id="7c427-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="7c427-108">Syntax</span></span>


```mof
uint32 ChangeMode(
  [in] uint32 LicensingType
);
```



## <a name="parameters"></a><span data-ttu-id="7c427-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="7c427-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7c427-110">*Лиценсингтипе* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="7c427-110">*LicensingType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7c427-111">Тип лицензирования, устанавливаемый на основе режима сервера узла сеансов удаленных рабочих столов.</span><span class="sxs-lookup"><span data-stu-id="7c427-111">The licensing type to set based on the RD Session Host server mode.</span></span>

<dt>

<span id="0"></span>

<span data-ttu-id="7c427-112"><span id="0"></span>**0,0**</span><span class="sxs-lookup"><span data-stu-id="7c427-112"><span id="0"></span>**0**</span></span>


</dt> <dd>

<span data-ttu-id="7c427-113">Сервер узла сеансов личных удаленных рабочих столов.</span><span class="sxs-lookup"><span data-stu-id="7c427-113">Personal RD Session Host server.</span></span>

</dd> <dt>

<span id="1"></span>

<span data-ttu-id="7c427-114"><span id="1"></span>**1**</span><span class="sxs-lookup"><span data-stu-id="7c427-114"><span id="1"></span>**1**</span></span>


</dt> <dd>

<span data-ttu-id="7c427-115">Удаленный рабочий стол для администрирования.</span><span class="sxs-lookup"><span data-stu-id="7c427-115">Remote desktop for administration.</span></span>

</dd> <dt>

<span id="2"></span>

<span data-ttu-id="7c427-116"><span id="2"></span>**открыт**</span><span class="sxs-lookup"><span data-stu-id="7c427-116"><span id="2"></span>**2**</span></span>


</dt> <dd>

<span data-ttu-id="7c427-117">За устройство/на рабочее место.</span><span class="sxs-lookup"><span data-stu-id="7c427-117">Per device/per seat.</span></span> <span data-ttu-id="7c427-118">Допустимо для серверов приложений.</span><span class="sxs-lookup"><span data-stu-id="7c427-118">Valid for application servers.</span></span>

</dd> <dt>

<span id="4"></span>

<span data-ttu-id="7c427-119"><span id="4"></span>**четырех**</span><span class="sxs-lookup"><span data-stu-id="7c427-119"><span id="4"></span>**4**</span></span>


</dt> <dd>

<span data-ttu-id="7c427-120">На пользователя.</span><span class="sxs-lookup"><span data-stu-id="7c427-120">Per User.</span></span> <span data-ttu-id="7c427-121">Допустимо для серверов приложений.</span><span class="sxs-lookup"><span data-stu-id="7c427-121">Valid for application servers.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7c427-122">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="7c427-122">Return value</span></span>

<span data-ttu-id="7c427-123">Возвращает значение 0 при успешном выполнении, в противном случае возвращает код ошибки WMI.</span><span class="sxs-lookup"><span data-stu-id="7c427-123">Returns 0 on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="7c427-124">Список этих значений см. в разделе [службы удаленных рабочих столов коды ошибок поставщика WMI](terminal-services-wmi-provider-error-codes.md) .</span><span class="sxs-lookup"><span data-stu-id="7c427-124">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span>

## <a name="remarks"></a><span data-ttu-id="7c427-125">Комментарии</span><span class="sxs-lookup"><span data-stu-id="7c427-125">Remarks</span></span>

<span data-ttu-id="7c427-126">Файлы MOF-файл (MOF) содержат определения для классов инструментарий управления Windows (WMI) (WMI).</span><span class="sxs-lookup"><span data-stu-id="7c427-126">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="7c427-127">MOF-файлы не устанавливаются в составе пакета средств разработки программного обеспечения Microsoft Windows (SDK).</span><span class="sxs-lookup"><span data-stu-id="7c427-127">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="7c427-128">Они устанавливаются на сервере при добавлении связанной роли с помощью диспетчер сервера.</span><span class="sxs-lookup"><span data-stu-id="7c427-128">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="7c427-129">Дополнительные сведения о файлах MOF см. в разделе [MOF-файл (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="7c427-129">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="7c427-130">Требования</span><span class="sxs-lookup"><span data-stu-id="7c427-130">Requirements</span></span>



| <span data-ttu-id="7c427-131">Требование</span><span class="sxs-lookup"><span data-stu-id="7c427-131">Requirement</span></span> | <span data-ttu-id="7c427-132">Значение</span><span class="sxs-lookup"><span data-stu-id="7c427-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="7c427-133">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="7c427-133">Minimum supported client</span></span><br/> | <span data-ttu-id="7c427-134">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="7c427-134">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="7c427-135">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="7c427-135">Minimum supported server</span></span><br/> | <span data-ttu-id="7c427-136">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="7c427-136">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="7c427-137">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="7c427-137">Namespace</span></span><br/>                | <span data-ttu-id="7c427-138">Корневой \\ CIMv2 \\ терминалсервицес</span><span class="sxs-lookup"><span data-stu-id="7c427-138">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="7c427-139">MOF</span><span class="sxs-lookup"><span data-stu-id="7c427-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="7c427-140"><dt>Тскфгвми. mof</dt></span><span class="sxs-lookup"><span data-stu-id="7c427-140"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="7c427-141">DLL</span><span class="sxs-lookup"><span data-stu-id="7c427-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7c427-142"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7c427-142"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7c427-143">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="7c427-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7c427-144">**\_Терминалсервицесеттинг Win32**</span><span class="sxs-lookup"><span data-stu-id="7c427-144">**Win32\_TerminalServiceSetting**</span></span>](win32-terminalservicesetting.md)
</dt> </dl>

 

