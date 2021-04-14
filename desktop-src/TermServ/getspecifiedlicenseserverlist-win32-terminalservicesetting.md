---
title: Метод ЖетспеЦифиедлиценсесерверлист класса Win32_TerminalServiceSetting
description: Извлекает список указанных серверов лицензирования.
ms.assetid: 800be0ce-1002-48e1-be4e-88db22590f12
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода ЖетспеЦифиедлиценсесерверлист
- Службы удаленных рабочих столов метода ЖетспеЦифиедлиценсесерверлист, класс Win32_TerminalServiceSetting
- Класс Win32_TerminalServiceSetting службы удаленных рабочих столов, метод ЖетспеЦифиедлиценсесерверлист
topic_type:
- apiref
api_name:
- Win32_TerminalServiceSetting.GetSpecifiedLicenseServerList
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1f70c50281cad7072d420082db0e6916a631e2b1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104414924"
---
# <a name="getspecifiedlicenseserverlist-method-of-the-win32_terminalservicesetting-class"></a><span data-ttu-id="f0e50-106">Метод ЖетспеЦифиедлиценсесерверлист \_ класса Win32 терминалсервицесеттинг</span><span class="sxs-lookup"><span data-stu-id="f0e50-106">GetSpecifiedLicenseServerList method of the Win32\_TerminalServiceSetting class</span></span>

<span data-ttu-id="f0e50-107">Извлекает список указанных серверов лицензирования.</span><span class="sxs-lookup"><span data-stu-id="f0e50-107">Retrieves the list of specified license servers.</span></span>

## <a name="syntax"></a><span data-ttu-id="f0e50-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f0e50-108">Syntax</span></span>


```mof
uint32 GetSpecifiedLicenseServerList(
  [out] string SpecifiedLSList[]
);
```



## <a name="parameters"></a><span data-ttu-id="f0e50-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="f0e50-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f0e50-110">*СпеЦифиедлслист* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="f0e50-110">*SpecifiedLSList* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f0e50-111">Массив строк, который получает список серверов лицензирования.</span><span class="sxs-lookup"><span data-stu-id="f0e50-111">A string array that receives the list of license servers.</span></span> <span data-ttu-id="f0e50-112">Если серверы лицензий отсутствуют, этот массив будет пустым.</span><span class="sxs-lookup"><span data-stu-id="f0e50-112">If there are no license servers, this array will be empty.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f0e50-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="f0e50-113">Return value</span></span>

<span data-ttu-id="f0e50-114">Возвращает значение 0 при успешном выполнении, в противном случае возвращает код ошибки WMI.</span><span class="sxs-lookup"><span data-stu-id="f0e50-114">Returns 0 on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="f0e50-115">Список этих значений см. в разделе [службы удаленных рабочих столов коды ошибок поставщика WMI](terminal-services-wmi-provider-error-codes.md) .</span><span class="sxs-lookup"><span data-stu-id="f0e50-115">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span>

## <a name="requirements"></a><span data-ttu-id="f0e50-116">Требования</span><span class="sxs-lookup"><span data-stu-id="f0e50-116">Requirements</span></span>



| <span data-ttu-id="f0e50-117">Требование</span><span class="sxs-lookup"><span data-stu-id="f0e50-117">Requirement</span></span> | <span data-ttu-id="f0e50-118">Значение</span><span class="sxs-lookup"><span data-stu-id="f0e50-118">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f0e50-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="f0e50-119">Minimum supported client</span></span><br/> | <span data-ttu-id="f0e50-120">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="f0e50-120">None supported</span></span><br/>                                                               |
| <span data-ttu-id="f0e50-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="f0e50-121">Minimum supported server</span></span><br/> | <span data-ttu-id="f0e50-122">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="f0e50-122">Windows Server 2008 R2</span></span><br/>                                                       |
| <span data-ttu-id="f0e50-123">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="f0e50-123">Namespace</span></span><br/>                | <span data-ttu-id="f0e50-124">Корневой \\ CIMv2 \\ терминалсервицес</span><span class="sxs-lookup"><span data-stu-id="f0e50-124">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="f0e50-125">MOF</span><span class="sxs-lookup"><span data-stu-id="f0e50-125">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f0e50-126"><dt>Тскфгвми. mof</dt></span><span class="sxs-lookup"><span data-stu-id="f0e50-126"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="f0e50-127">DLL</span><span class="sxs-lookup"><span data-stu-id="f0e50-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f0e50-128"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f0e50-128"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f0e50-129">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f0e50-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f0e50-130">**\_Терминалсервицесеттинг Win32**</span><span class="sxs-lookup"><span data-stu-id="f0e50-130">**Win32\_TerminalServiceSetting**</span></span>](win32-terminalservicesetting.md)
</dt> <dt>

[<span data-ttu-id="f0e50-131">**аддлстоспеЦифиедлиценсесерверлист**</span><span class="sxs-lookup"><span data-stu-id="f0e50-131">**AddLSToSpecifiedLicenseServerList**</span></span>](addlstospecifiedlicenseserverlist-win32-terminalservicesetting.md)
</dt> <dt>

[<span data-ttu-id="f0e50-132">**емптиспеЦифиедлиценсесерверлист**</span><span class="sxs-lookup"><span data-stu-id="f0e50-132">**EmptySpecifiedLicenseServerList**</span></span>](emptyspecifiedlicenseserverlist-win32-terminalservicesetting.md)
</dt> <dt>

[<span data-ttu-id="f0e50-133">**ремовелсфромспеЦифиедлиценсесерверлист**</span><span class="sxs-lookup"><span data-stu-id="f0e50-133">**RemoveLSFromSpecifiedLicenseServerList**</span></span>](removelsfromspecifiedlicenseserverlist-win32-terminalservicesetting.md)
</dt> <dt>

[<span data-ttu-id="f0e50-134">**сетспеЦифиедлиценсесерверлист**</span><span class="sxs-lookup"><span data-stu-id="f0e50-134">**SetSpecifiedLicenseServerList**</span></span>](setspecifiedlicenseserverlist-win32-terminalservicesetting.md)
</dt> </dl>

 

 





