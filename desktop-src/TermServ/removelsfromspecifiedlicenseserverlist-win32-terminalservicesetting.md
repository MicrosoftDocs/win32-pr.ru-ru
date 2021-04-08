---
title: Метод РемовелсфромспеЦифиедлиценсесерверлист класса Win32_TerminalServiceSetting
description: Удаляет указанный сервер лицензирования из списка указанных серверов лицензирования.
ms.assetid: c25eebf9-3a21-41a0-bb7d-c3f909cd8087
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода РемовелсфромспеЦифиедлиценсесерверлист
- Службы удаленных рабочих столов метода РемовелсфромспеЦифиедлиценсесерверлист, класс Win32_TerminalServiceSetting
- Класс Win32_TerminalServiceSetting службы удаленных рабочих столов, метод РемовелсфромспеЦифиедлиценсесерверлист
topic_type:
- apiref
api_name:
- Win32_TerminalServiceSetting.RemoveLSFromSpecifiedLicenseServerList
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 901c2676748e819290855df2de51e5d7936dc793
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103891937"
---
# <a name="removelsfromspecifiedlicenseserverlist-method-of-the-win32_terminalservicesetting-class"></a><span data-ttu-id="e5a5f-106">Метод РемовелсфромспеЦифиедлиценсесерверлист \_ класса Win32 терминалсервицесеттинг</span><span class="sxs-lookup"><span data-stu-id="e5a5f-106">RemoveLSFromSpecifiedLicenseServerList method of the Win32\_TerminalServiceSetting class</span></span>

<span data-ttu-id="e5a5f-107">Удаляет указанный сервер лицензирования из списка указанных серверов лицензирования.</span><span class="sxs-lookup"><span data-stu-id="e5a5f-107">Removes the given license server from the list of specified license servers.</span></span>

## <a name="syntax"></a><span data-ttu-id="e5a5f-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e5a5f-108">Syntax</span></span>


```mof
uint32 RemoveLSFromSpecifiedLicenseServerList(
  [in] string LicenseServerName
);
```



## <a name="parameters"></a><span data-ttu-id="e5a5f-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="e5a5f-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e5a5f-110">*Лиценсесервернаме* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="e5a5f-110">*LicenseServerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e5a5f-111">Имя удаляемого сервера лицензирования.</span><span class="sxs-lookup"><span data-stu-id="e5a5f-111">The name of the license server to remove.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e5a5f-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="e5a5f-112">Return value</span></span>

<span data-ttu-id="e5a5f-113">Возвращает значение 0 при успешном выполнении, в противном случае возвращает код ошибки WMI.</span><span class="sxs-lookup"><span data-stu-id="e5a5f-113">Returns 0 on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="e5a5f-114">Список этих значений см. в разделе [службы удаленных рабочих столов коды ошибок поставщика WMI](terminal-services-wmi-provider-error-codes.md) .</span><span class="sxs-lookup"><span data-stu-id="e5a5f-114">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span>

## <a name="requirements"></a><span data-ttu-id="e5a5f-115">Требования</span><span class="sxs-lookup"><span data-stu-id="e5a5f-115">Requirements</span></span>



| <span data-ttu-id="e5a5f-116">Требование</span><span class="sxs-lookup"><span data-stu-id="e5a5f-116">Requirement</span></span> | <span data-ttu-id="e5a5f-117">Значение</span><span class="sxs-lookup"><span data-stu-id="e5a5f-117">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e5a5f-118">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="e5a5f-118">Minimum supported client</span></span><br/> | <span data-ttu-id="e5a5f-119">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="e5a5f-119">None supported</span></span><br/>                                                               |
| <span data-ttu-id="e5a5f-120">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="e5a5f-120">Minimum supported server</span></span><br/> | <span data-ttu-id="e5a5f-121">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="e5a5f-121">Windows Server 2008 R2</span></span><br/>                                                       |
| <span data-ttu-id="e5a5f-122">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="e5a5f-122">Namespace</span></span><br/>                | <span data-ttu-id="e5a5f-123">Корневой \\ CIMv2 \\ терминалсервицес</span><span class="sxs-lookup"><span data-stu-id="e5a5f-123">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="e5a5f-124">MOF</span><span class="sxs-lookup"><span data-stu-id="e5a5f-124">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e5a5f-125"><dt>Тскфгвми. mof</dt></span><span class="sxs-lookup"><span data-stu-id="e5a5f-125"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="e5a5f-126">DLL</span><span class="sxs-lookup"><span data-stu-id="e5a5f-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e5a5f-127"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e5a5f-127"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e5a5f-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e5a5f-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e5a5f-129">**\_Терминалсервицесеттинг Win32**</span><span class="sxs-lookup"><span data-stu-id="e5a5f-129">**Win32\_TerminalServiceSetting**</span></span>](win32-terminalservicesetting.md)
</dt> <dt>

[<span data-ttu-id="e5a5f-130">**аддлстоспеЦифиедлиценсесерверлист**</span><span class="sxs-lookup"><span data-stu-id="e5a5f-130">**AddLSToSpecifiedLicenseServerList**</span></span>](addlstospecifiedlicenseserverlist-win32-terminalservicesetting.md)
</dt> <dt>

[<span data-ttu-id="e5a5f-131">**емптиспеЦифиедлиценсесерверлист**</span><span class="sxs-lookup"><span data-stu-id="e5a5f-131">**EmptySpecifiedLicenseServerList**</span></span>](emptyspecifiedlicenseserverlist-win32-terminalservicesetting.md)
</dt> <dt>

[<span data-ttu-id="e5a5f-132">**жетспеЦифиедлиценсесерверлист**</span><span class="sxs-lookup"><span data-stu-id="e5a5f-132">**GetSpecifiedLicenseServerList**</span></span>](getspecifiedlicenseserverlist-win32-terminalservicesetting.md)
</dt> <dt>

[<span data-ttu-id="e5a5f-133">**сетспеЦифиедлиценсесерверлист**</span><span class="sxs-lookup"><span data-stu-id="e5a5f-133">**SetSpecifiedLicenseServerList**</span></span>](setspecifiedlicenseserverlist-win32-terminalservicesetting.md)
</dt> </dl>

 

 





