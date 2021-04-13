---
title: Метод ЕмптиспеЦифиедлиценсесерверлист класса Win32_TerminalServiceSetting
description: Удаляет все серверы лицензий из списка указанных серверов лицензирования.
ms.assetid: de1633ca-3f0b-4540-8b45-44303a4e72fe
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода ЕмптиспеЦифиедлиценсесерверлист
- Службы удаленных рабочих столов метода ЕмптиспеЦифиедлиценсесерверлист, класс Win32_TerminalServiceSetting
- Класс Win32_TerminalServiceSetting службы удаленных рабочих столов, метод ЕмптиспеЦифиедлиценсесерверлист
topic_type:
- apiref
api_name:
- Win32_TerminalServiceSetting.EmptySpecifiedLicenseServerList
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1392c05618860f742a13140167e423b312e49b0a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104493212"
---
# <a name="emptyspecifiedlicenseserverlist-method-of-the-win32_terminalservicesetting-class"></a><span data-ttu-id="a6a0f-106">Метод ЕмптиспеЦифиедлиценсесерверлист \_ класса Win32 терминалсервицесеттинг</span><span class="sxs-lookup"><span data-stu-id="a6a0f-106">EmptySpecifiedLicenseServerList method of the Win32\_TerminalServiceSetting class</span></span>

<span data-ttu-id="a6a0f-107">Удаляет все серверы лицензий из списка указанных серверов лицензирования.</span><span class="sxs-lookup"><span data-stu-id="a6a0f-107">Removes all license servers from the list of specified license servers.</span></span>

## <a name="syntax"></a><span data-ttu-id="a6a0f-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a6a0f-108">Syntax</span></span>


```mof
uint32 EmptySpecifiedLicenseServerList();
```



## <a name="parameters"></a><span data-ttu-id="a6a0f-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="a6a0f-109">Parameters</span></span>

<span data-ttu-id="a6a0f-110">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="a6a0f-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="a6a0f-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="a6a0f-111">Return value</span></span>

<span data-ttu-id="a6a0f-112">Возвращает значение 0 при успешном выполнении, в противном случае возвращает код ошибки WMI.</span><span class="sxs-lookup"><span data-stu-id="a6a0f-112">Returns 0 on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="a6a0f-113">Список этих значений см. в разделе [службы удаленных рабочих столов коды ошибок поставщика WMI](terminal-services-wmi-provider-error-codes.md) .</span><span class="sxs-lookup"><span data-stu-id="a6a0f-113">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span>

## <a name="requirements"></a><span data-ttu-id="a6a0f-114">Требования</span><span class="sxs-lookup"><span data-stu-id="a6a0f-114">Requirements</span></span>



| <span data-ttu-id="a6a0f-115">Требование</span><span class="sxs-lookup"><span data-stu-id="a6a0f-115">Requirement</span></span> | <span data-ttu-id="a6a0f-116">Значение</span><span class="sxs-lookup"><span data-stu-id="a6a0f-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a6a0f-117">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="a6a0f-117">Minimum supported client</span></span><br/> | <span data-ttu-id="a6a0f-118">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="a6a0f-118">None supported</span></span><br/>                                                               |
| <span data-ttu-id="a6a0f-119">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="a6a0f-119">Minimum supported server</span></span><br/> | <span data-ttu-id="a6a0f-120">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="a6a0f-120">Windows Server 2008 R2</span></span><br/>                                                       |
| <span data-ttu-id="a6a0f-121">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="a6a0f-121">Namespace</span></span><br/>                | <span data-ttu-id="a6a0f-122">Корневой \\ CIMv2 \\ терминалсервицес</span><span class="sxs-lookup"><span data-stu-id="a6a0f-122">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="a6a0f-123">MOF</span><span class="sxs-lookup"><span data-stu-id="a6a0f-123">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a6a0f-124"><dt>Тскфгвми. mof</dt></span><span class="sxs-lookup"><span data-stu-id="a6a0f-124"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="a6a0f-125">DLL</span><span class="sxs-lookup"><span data-stu-id="a6a0f-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a6a0f-126"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a6a0f-126"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a6a0f-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a6a0f-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a6a0f-128">**\_Терминалсервицесеттинг Win32**</span><span class="sxs-lookup"><span data-stu-id="a6a0f-128">**Win32\_TerminalServiceSetting**</span></span>](win32-terminalservicesetting.md)
</dt> <dt>

[<span data-ttu-id="a6a0f-129">**аддлстоспеЦифиедлиценсесерверлист**</span><span class="sxs-lookup"><span data-stu-id="a6a0f-129">**AddLSToSpecifiedLicenseServerList**</span></span>](addlstospecifiedlicenseserverlist-win32-terminalservicesetting.md)
</dt> <dt>

[<span data-ttu-id="a6a0f-130">**жетспеЦифиедлиценсесерверлист**</span><span class="sxs-lookup"><span data-stu-id="a6a0f-130">**GetSpecifiedLicenseServerList**</span></span>](getspecifiedlicenseserverlist-win32-terminalservicesetting.md)
</dt> <dt>

[<span data-ttu-id="a6a0f-131">**ремовелсфромспеЦифиедлиценсесерверлист**</span><span class="sxs-lookup"><span data-stu-id="a6a0f-131">**RemoveLSFromSpecifiedLicenseServerList**</span></span>](removelsfromspecifiedlicenseserverlist-win32-terminalservicesetting.md)
</dt> <dt>

[<span data-ttu-id="a6a0f-132">**сетспеЦифиедлиценсесерверлист**</span><span class="sxs-lookup"><span data-stu-id="a6a0f-132">**SetSpecifiedLicenseServerList**</span></span>](setspecifiedlicenseserverlist-win32-terminalservicesetting.md)
</dt> </dl>

 

 





