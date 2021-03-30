---
title: Метод АддлстоспеЦифиедлиценсесерверлист класса Win32_TerminalServiceSetting
description: Добавляет указанный сервер лицензирования в конец списка указанных серверов лицензирования.
ms.assetid: 2aebe7c0-5ec2-4c2d-9887-7ecd2d6ec02a
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода АддлстоспеЦифиедлиценсесерверлист
- Службы удаленных рабочих столов метода АддлстоспеЦифиедлиценсесерверлист, класс Win32_TerminalServiceSetting
- Класс Win32_TerminalServiceSetting службы удаленных рабочих столов, метод АддлстоспеЦифиедлиценсесерверлист
topic_type:
- apiref
api_name:
- Win32_TerminalServiceSetting.AddLSToSpecifiedLicenseServerList
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1c53a5279523405b760addabb03e381507775e6a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988410"
---
# <a name="addlstospecifiedlicenseserverlist-method-of-the-win32_terminalservicesetting-class"></a><span data-ttu-id="67a9a-106">Метод АддлстоспеЦифиедлиценсесерверлист \_ класса Win32 терминалсервицесеттинг</span><span class="sxs-lookup"><span data-stu-id="67a9a-106">AddLSToSpecifiedLicenseServerList method of the Win32\_TerminalServiceSetting class</span></span>

<span data-ttu-id="67a9a-107">Добавляет указанный сервер лицензирования в конец списка указанных серверов лицензирования.</span><span class="sxs-lookup"><span data-stu-id="67a9a-107">Adds the given license server to the end of the list of specified license servers.</span></span>

## <a name="syntax"></a><span data-ttu-id="67a9a-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="67a9a-108">Syntax</span></span>


```mof
uint32 AddLSToSpecifiedLicenseServerList(
  [in] string LicenseServerName
);
```



## <a name="parameters"></a><span data-ttu-id="67a9a-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="67a9a-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="67a9a-110">*Лиценсесервернаме* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="67a9a-110">*LicenseServerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="67a9a-111">Имя добавляемого сервера лицензирования.</span><span class="sxs-lookup"><span data-stu-id="67a9a-111">The name of the license server to add.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="67a9a-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="67a9a-112">Return value</span></span>

<span data-ttu-id="67a9a-113">Возвращает значение 0 при успешном выполнении, в противном случае возвращает код ошибки WMI.</span><span class="sxs-lookup"><span data-stu-id="67a9a-113">Returns 0 on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="67a9a-114">Список этих значений см. в разделе [службы удаленных рабочих столов коды ошибок поставщика WMI](terminal-services-wmi-provider-error-codes.md) .</span><span class="sxs-lookup"><span data-stu-id="67a9a-114">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span>

## <a name="requirements"></a><span data-ttu-id="67a9a-115">Требования</span><span class="sxs-lookup"><span data-stu-id="67a9a-115">Requirements</span></span>



| <span data-ttu-id="67a9a-116">Требование</span><span class="sxs-lookup"><span data-stu-id="67a9a-116">Requirement</span></span> | <span data-ttu-id="67a9a-117">Значение</span><span class="sxs-lookup"><span data-stu-id="67a9a-117">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="67a9a-118">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="67a9a-118">Minimum supported client</span></span><br/> | <span data-ttu-id="67a9a-119">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="67a9a-119">None supported</span></span><br/>                                                               |
| <span data-ttu-id="67a9a-120">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="67a9a-120">Minimum supported server</span></span><br/> | <span data-ttu-id="67a9a-121">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="67a9a-121">Windows Server 2008 R2</span></span><br/>                                                       |
| <span data-ttu-id="67a9a-122">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="67a9a-122">Namespace</span></span><br/>                | <span data-ttu-id="67a9a-123">Корневой \\ CIMv2 \\ терминалсервицес</span><span class="sxs-lookup"><span data-stu-id="67a9a-123">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="67a9a-124">MOF</span><span class="sxs-lookup"><span data-stu-id="67a9a-124">MOF</span></span><br/>                      | <dl> <span data-ttu-id="67a9a-125"><dt>Тскфгвми. mof</dt></span><span class="sxs-lookup"><span data-stu-id="67a9a-125"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="67a9a-126">DLL</span><span class="sxs-lookup"><span data-stu-id="67a9a-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="67a9a-127"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="67a9a-127"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="67a9a-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="67a9a-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="67a9a-129">**\_Терминалсервицесеттинг Win32**</span><span class="sxs-lookup"><span data-stu-id="67a9a-129">**Win32\_TerminalServiceSetting**</span></span>](win32-terminalservicesetting.md)
</dt> <dt>

[<span data-ttu-id="67a9a-130">**емптиспеЦифиедлиценсесерверлист**</span><span class="sxs-lookup"><span data-stu-id="67a9a-130">**EmptySpecifiedLicenseServerList**</span></span>](emptyspecifiedlicenseserverlist-win32-terminalservicesetting.md)
</dt> <dt>

[<span data-ttu-id="67a9a-131">**жетспеЦифиедлиценсесерверлист**</span><span class="sxs-lookup"><span data-stu-id="67a9a-131">**GetSpecifiedLicenseServerList**</span></span>](getspecifiedlicenseserverlist-win32-terminalservicesetting.md)
</dt> <dt>

[<span data-ttu-id="67a9a-132">**ремовелсфромспеЦифиедлиценсесерверлист**</span><span class="sxs-lookup"><span data-stu-id="67a9a-132">**RemoveLSFromSpecifiedLicenseServerList**</span></span>](removelsfromspecifiedlicenseserverlist-win32-terminalservicesetting.md)
</dt> <dt>

[<span data-ttu-id="67a9a-133">**сетспеЦифиедлиценсесерверлист**</span><span class="sxs-lookup"><span data-stu-id="67a9a-133">**SetSpecifiedLicenseServerList**</span></span>](setspecifiedlicenseserverlist-win32-terminalservicesetting.md)
</dt> </dl>

 

 





