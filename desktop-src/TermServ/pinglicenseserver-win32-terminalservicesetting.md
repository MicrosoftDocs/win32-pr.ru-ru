---
title: Метод Пинглиценсесервер класса Win32_TerminalServiceSetting
description: Пинглиценсесервер больше не доступен.
ms.assetid: d2a9f273-1ff9-4391-889b-a3b9c9f95c3b
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода Пинглиценсесервер
- Службы удаленных рабочих столов метода Пинглиценсесервер, класс Win32_TerminalServiceSetting
- Класс Win32_TerminalServiceSetting службы удаленных рабочих столов, метод Пинглиценсесервер
topic_type:
- apiref
api_name:
- Win32_TerminalServiceSetting.PingLicenseServer
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2fe7277b3130c88c1aec7716c1a3bf560b81db64
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104415449"
---
# <a name="pinglicenseserver-method-of-the-win32_terminalservicesetting-class"></a><span data-ttu-id="e2772-106">Метод Пинглиценсесервер \_ класса Win32 терминалсервицесеттинг</span><span class="sxs-lookup"><span data-stu-id="e2772-106">PingLicenseServer method of the Win32\_TerminalServiceSetting class</span></span>

<span data-ttu-id="e2772-107">\[**Пинглиценсесервер** больше не доступен для использования в Windows Server 2008 R2.\]</span><span class="sxs-lookup"><span data-stu-id="e2772-107">\[**PingLicenseServer** is no longer available for use as of Windows Server 2008 R2.\]</span></span>

<span data-ttu-id="e2772-108">**Windows Server 2008:** Проверяет связь сервера лицензирования с сервером лицензий, чтобы определить, является ли он допустимым сервером лицензирования.</span><span class="sxs-lookup"><span data-stu-id="e2772-108">**Windows Server 2008:** Pings the license server to determine if it is a valid license server.</span></span>

## <a name="syntax"></a><span data-ttu-id="e2772-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e2772-109">Syntax</span></span>


```mof
uint32 PingLicenseServer(
  [in] string ServerName
);
```



## <a name="parameters"></a><span data-ttu-id="e2772-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="e2772-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e2772-111">*Имя сервера* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="e2772-111">*ServerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e2772-112">Имя сервера лицензирования.</span><span class="sxs-lookup"><span data-stu-id="e2772-112">Name of the license server.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e2772-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="e2772-113">Return value</span></span>

<dl> <dt>

<span data-ttu-id="e2772-114">**\_ОК**</span><span class="sxs-lookup"><span data-stu-id="e2772-114">**S\_OK**</span></span>
</dt> <dd>

<span data-ttu-id="e2772-115">Сервер является действительным сервером лицензирования.</span><span class="sxs-lookup"><span data-stu-id="e2772-115">The server is a valid license server.</span></span>

</dd> <dt>

<span data-ttu-id="e2772-116">**S \_ false**</span><span class="sxs-lookup"><span data-stu-id="e2772-116">**S\_FALSE**</span></span>
</dt> <dd>

<span data-ttu-id="e2772-117">Недопустимый сервер лицензирования.</span><span class="sxs-lookup"><span data-stu-id="e2772-117">The license server is not valid.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e2772-118">Комментарии</span><span class="sxs-lookup"><span data-stu-id="e2772-118">Remarks</span></span>

<span data-ttu-id="e2772-119">Файлы MOF-файл (MOF) содержат определения для классов инструментарий управления Windows (WMI) (WMI).</span><span class="sxs-lookup"><span data-stu-id="e2772-119">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="e2772-120">MOF-файлы не устанавливаются в составе пакета средств разработки программного обеспечения Microsoft Windows (SDK).</span><span class="sxs-lookup"><span data-stu-id="e2772-120">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="e2772-121">Они устанавливаются на сервере при добавлении связанной роли с помощью диспетчер сервера.</span><span class="sxs-lookup"><span data-stu-id="e2772-121">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="e2772-122">Дополнительные сведения о файлах MOF см. в разделе [MOF-файл (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="e2772-122">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="e2772-123">Требования</span><span class="sxs-lookup"><span data-stu-id="e2772-123">Requirements</span></span>



| <span data-ttu-id="e2772-124">Требование</span><span class="sxs-lookup"><span data-stu-id="e2772-124">Requirement</span></span> | <span data-ttu-id="e2772-125">Значение</span><span class="sxs-lookup"><span data-stu-id="e2772-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e2772-126">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="e2772-126">Minimum supported client</span></span><br/> | <span data-ttu-id="e2772-127">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="e2772-127">None supported</span></span><br/>                                                               |
| <span data-ttu-id="e2772-128">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="e2772-128">Minimum supported server</span></span><br/> | <span data-ttu-id="e2772-129">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e2772-129">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="e2772-130">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="e2772-130">End of client support</span></span><br/>    | <span data-ttu-id="e2772-131">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="e2772-131">None supported</span></span><br/>                                                               |
| <span data-ttu-id="e2772-132">Поддержка конца сервера</span><span class="sxs-lookup"><span data-stu-id="e2772-132">End of server support</span></span><br/>    | <span data-ttu-id="e2772-133">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e2772-133">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="e2772-134">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="e2772-134">Namespace</span></span><br/>                | <span data-ttu-id="e2772-135">Корневой \\ CIMv2 \\ терминалсервицес</span><span class="sxs-lookup"><span data-stu-id="e2772-135">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="e2772-136">MOF</span><span class="sxs-lookup"><span data-stu-id="e2772-136">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e2772-137"><dt>Тскфгвми. mof</dt></span><span class="sxs-lookup"><span data-stu-id="e2772-137"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="e2772-138">DLL</span><span class="sxs-lookup"><span data-stu-id="e2772-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e2772-139"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e2772-139"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e2772-140">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e2772-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e2772-141">**\_Терминалсервицесеттинг Win32**</span><span class="sxs-lookup"><span data-stu-id="e2772-141">**Win32\_TerminalServiceSetting**</span></span>](win32-terminalservicesetting.md)
</dt> </dl>

 

