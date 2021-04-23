---
title: Метод Адддиректконнектлиценсесервер класса Win32_TerminalServiceSetting
description: Адддиректконнектлиценсесервер больше не доступен.
ms.assetid: 7920fd28-0fa3-4f96-bec3-d9e37c97920c
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода Адддиректконнектлиценсесервер
- Службы удаленных рабочих столов метода Адддиректконнектлиценсесервер, класс Win32_TerminalServiceSetting
- Класс Win32_TerminalServiceSetting службы удаленных рабочих столов, метод Адддиректконнектлиценсесервер
topic_type:
- apiref
api_name:
- Win32_TerminalServiceSetting.AddDirectConnectLicenseServer
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: be9bba23f5c0bfc69b4c8d7951ab38eac6690b84
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104416032"
---
# <a name="adddirectconnectlicenseserver-method-of-the-win32_terminalservicesetting-class"></a><span data-ttu-id="85e3d-106">Метод Адддиректконнектлиценсесервер \_ класса Win32 терминалсервицесеттинг</span><span class="sxs-lookup"><span data-stu-id="85e3d-106">AddDirectConnectLicenseServer method of the Win32\_TerminalServiceSetting class</span></span>

<span data-ttu-id="85e3d-107">\[**Адддиректконнектлиценсесервер** больше не доступен для использования в Windows Server 2008 R2.\]</span><span class="sxs-lookup"><span data-stu-id="85e3d-107">\[**AddDirectConnectLicenseServer** is no longer available for use as of Windows Server 2008 R2.\]</span></span>

<span data-ttu-id="85e3d-108">**Windows Server 2008:** Настраивает новый сервер лицензирования и добавляет сервер лицензирования в реестр для обнаружения с помощью удаленный рабочий стол серверов узла сеансов удаленных рабочих столов.</span><span class="sxs-lookup"><span data-stu-id="85e3d-108">**Windows Server 2008:** Configures a new license server and adds the license server to the registry for discovery by Remote Desktop Session Host (RD Session Host) servers.</span></span>

## <a name="syntax"></a><span data-ttu-id="85e3d-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="85e3d-109">Syntax</span></span>


```mof
uint32 AddDirectConnectLicenseServer(
  [in] string LicenseServerName
);
```



## <a name="parameters"></a><span data-ttu-id="85e3d-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="85e3d-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="85e3d-111">*Лиценсесервернаме* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="85e3d-111">*LicenseServerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="85e3d-112">Имя добавляемого сервера лицензирования.</span><span class="sxs-lookup"><span data-stu-id="85e3d-112">Name of the license server to add.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="85e3d-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="85e3d-113">Return value</span></span>

<span data-ttu-id="85e3d-114">Возвращает значение 0 при успешном выполнении, в противном случае возвращает код ошибки WMI.</span><span class="sxs-lookup"><span data-stu-id="85e3d-114">Returns 0 on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="85e3d-115">Список этих значений см. в разделе [службы удаленных рабочих столов коды ошибок поставщика WMI](terminal-services-wmi-provider-error-codes.md) .</span><span class="sxs-lookup"><span data-stu-id="85e3d-115">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span>

## <a name="remarks"></a><span data-ttu-id="85e3d-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="85e3d-116">Remarks</span></span>

<span data-ttu-id="85e3d-117">Файлы MOF-файл (MOF) содержат определения для классов инструментарий управления Windows (WMI) (WMI).</span><span class="sxs-lookup"><span data-stu-id="85e3d-117">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="85e3d-118">MOF-файлы не устанавливаются в составе пакета средств разработки программного обеспечения Microsoft Windows (SDK).</span><span class="sxs-lookup"><span data-stu-id="85e3d-118">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="85e3d-119">Они устанавливаются на сервере при добавлении связанной роли с помощью диспетчер сервера.</span><span class="sxs-lookup"><span data-stu-id="85e3d-119">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="85e3d-120">Дополнительные сведения о файлах MOF см. в разделе [MOF-файл (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="85e3d-120">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="85e3d-121">Требования</span><span class="sxs-lookup"><span data-stu-id="85e3d-121">Requirements</span></span>



| <span data-ttu-id="85e3d-122">Требование</span><span class="sxs-lookup"><span data-stu-id="85e3d-122">Requirement</span></span> | <span data-ttu-id="85e3d-123">Значение</span><span class="sxs-lookup"><span data-stu-id="85e3d-123">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="85e3d-124">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="85e3d-124">Minimum supported client</span></span><br/> | <span data-ttu-id="85e3d-125">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="85e3d-125">None supported</span></span><br/>                                                               |
| <span data-ttu-id="85e3d-126">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="85e3d-126">Minimum supported server</span></span><br/> | <span data-ttu-id="85e3d-127">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="85e3d-127">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="85e3d-128">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="85e3d-128">End of client support</span></span><br/>    | <span data-ttu-id="85e3d-129">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="85e3d-129">None supported</span></span><br/>                                                               |
| <span data-ttu-id="85e3d-130">Поддержка конца сервера</span><span class="sxs-lookup"><span data-stu-id="85e3d-130">End of server support</span></span><br/>    | <span data-ttu-id="85e3d-131">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="85e3d-131">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="85e3d-132">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="85e3d-132">Namespace</span></span><br/>                | <span data-ttu-id="85e3d-133">Корневой \\ CIMv2 \\ терминалсервицес</span><span class="sxs-lookup"><span data-stu-id="85e3d-133">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="85e3d-134">MOF</span><span class="sxs-lookup"><span data-stu-id="85e3d-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="85e3d-135"><dt>Тскфгвми. mof</dt></span><span class="sxs-lookup"><span data-stu-id="85e3d-135"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="85e3d-136">DLL</span><span class="sxs-lookup"><span data-stu-id="85e3d-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="85e3d-137"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="85e3d-137"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="85e3d-138">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="85e3d-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="85e3d-139">**\_Терминалсервицесеттинг Win32**</span><span class="sxs-lookup"><span data-stu-id="85e3d-139">**Win32\_TerminalServiceSetting**</span></span>](win32-terminalservicesetting.md)
</dt> </dl>

 

