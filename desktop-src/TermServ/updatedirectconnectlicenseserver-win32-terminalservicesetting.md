---
title: Метод Упдатедиректконнектлиценсесервер класса Win32_TerminalServiceSetting
description: Упдатедиректконнектлиценсесервер больше не доступен.
ms.assetid: 0b6e0dba-e23b-4c8d-8021-93d802501359
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода Упдатедиректконнектлиценсесервер
- Службы удаленных рабочих столов метода Упдатедиректконнектлиценсесервер, класс Win32_TerminalServiceSetting
- Класс Win32_TerminalServiceSetting службы удаленных рабочих столов, метод Упдатедиректконнектлиценсесервер
topic_type:
- apiref
api_name:
- Win32_TerminalServiceSetting.UpdateDirectConnectLicenseServer
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d2249dd00b44955a4e2712b8b7bf746793e89d57
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105672677"
---
# <a name="updatedirectconnectlicenseserver-method-of-the-win32_terminalservicesetting-class"></a><span data-ttu-id="4071f-106">Метод Упдатедиректконнектлиценсесервер \_ класса Win32 терминалсервицесеттинг</span><span class="sxs-lookup"><span data-stu-id="4071f-106">UpdateDirectConnectLicenseServer method of the Win32\_TerminalServiceSetting class</span></span>

<span data-ttu-id="4071f-107">\[**Упдатедиректконнектлиценсесервер** больше не доступен для использования в Windows Server 2008 R2.\]</span><span class="sxs-lookup"><span data-stu-id="4071f-107">\[**UpdateDirectConnectLicenseServer** is no longer available for use as of Windows Server 2008 R2.\]</span></span>

<span data-ttu-id="4071f-108">**Windows Server 2008:** Обновляет список серверов лицензирования обнаружения.</span><span class="sxs-lookup"><span data-stu-id="4071f-108">**Windows Server 2008:** Updates the list of discovery license servers.</span></span> <span data-ttu-id="4071f-109">Список серверов отделяется точкой с запятой (";").</span><span class="sxs-lookup"><span data-stu-id="4071f-109">The server list is delimited by semicolons (";").</span></span>

## <a name="syntax"></a><span data-ttu-id="4071f-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="4071f-110">Syntax</span></span>


```mof
uint32 UpdateDirectConnectLicenseServer(
  [in] string LicenseServerList
);
```



## <a name="parameters"></a><span data-ttu-id="4071f-111">Параметры</span><span class="sxs-lookup"><span data-stu-id="4071f-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4071f-112">*Лиценсесерверлист* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="4071f-112">*LicenseServerList* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4071f-113">Список серверов лицензирования.</span><span class="sxs-lookup"><span data-stu-id="4071f-113">List of license servers.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4071f-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="4071f-114">Return value</span></span>

<span data-ttu-id="4071f-115">Возвращает значение 0 при успешном выполнении, в противном случае возвращает код ошибки WMI.</span><span class="sxs-lookup"><span data-stu-id="4071f-115">Returns 0 on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="4071f-116">Список этих значений см. в разделе [службы удаленных рабочих столов коды ошибок поставщика WMI](terminal-services-wmi-provider-error-codes.md) .</span><span class="sxs-lookup"><span data-stu-id="4071f-116">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span>

## <a name="remarks"></a><span data-ttu-id="4071f-117">Комментарии</span><span class="sxs-lookup"><span data-stu-id="4071f-117">Remarks</span></span>

<span data-ttu-id="4071f-118">Файлы MOF-файл (MOF) содержат определения для классов инструментарий управления Windows (WMI) (WMI).</span><span class="sxs-lookup"><span data-stu-id="4071f-118">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="4071f-119">MOF-файлы не устанавливаются в составе пакета средств разработки программного обеспечения Microsoft Windows (SDK).</span><span class="sxs-lookup"><span data-stu-id="4071f-119">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="4071f-120">Они устанавливаются на сервере при добавлении связанной роли с помощью диспетчер сервера.</span><span class="sxs-lookup"><span data-stu-id="4071f-120">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="4071f-121">Дополнительные сведения о файлах MOF см. в разделе [MOF-файл (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="4071f-121">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="4071f-122">Требования</span><span class="sxs-lookup"><span data-stu-id="4071f-122">Requirements</span></span>



| <span data-ttu-id="4071f-123">Требование</span><span class="sxs-lookup"><span data-stu-id="4071f-123">Requirement</span></span> | <span data-ttu-id="4071f-124">Значение</span><span class="sxs-lookup"><span data-stu-id="4071f-124">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4071f-125">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="4071f-125">Minimum supported client</span></span><br/> | <span data-ttu-id="4071f-126">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="4071f-126">None supported</span></span><br/>                                                               |
| <span data-ttu-id="4071f-127">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="4071f-127">Minimum supported server</span></span><br/> | <span data-ttu-id="4071f-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="4071f-128">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="4071f-129">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="4071f-129">End of client support</span></span><br/>    | <span data-ttu-id="4071f-130">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="4071f-130">None supported</span></span><br/>                                                               |
| <span data-ttu-id="4071f-131">Поддержка конца сервера</span><span class="sxs-lookup"><span data-stu-id="4071f-131">End of server support</span></span><br/>    | <span data-ttu-id="4071f-132">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="4071f-132">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="4071f-133">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="4071f-133">Namespace</span></span><br/>                | <span data-ttu-id="4071f-134">Корневой \\ CIMv2 \\ терминалсервицес</span><span class="sxs-lookup"><span data-stu-id="4071f-134">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="4071f-135">MOF</span><span class="sxs-lookup"><span data-stu-id="4071f-135">MOF</span></span><br/>                      | <dl> <span data-ttu-id="4071f-136"><dt>Тскфгвми. mof</dt></span><span class="sxs-lookup"><span data-stu-id="4071f-136"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="4071f-137">DLL</span><span class="sxs-lookup"><span data-stu-id="4071f-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4071f-138"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4071f-138"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4071f-139">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="4071f-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4071f-140">**\_Терминалсервицесеттинг Win32**</span><span class="sxs-lookup"><span data-stu-id="4071f-140">**Win32\_TerminalServiceSetting**</span></span>](win32-terminalservicesetting.md)
</dt> </dl>

 

