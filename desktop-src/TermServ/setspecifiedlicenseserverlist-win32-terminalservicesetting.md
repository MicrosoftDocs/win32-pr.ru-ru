---
title: Метод СетспеЦифиедлиценсесерверлист класса Win32_TerminalServiceSetting
description: Обновляет список указанных серверов лицензирования, заменяя все существующие указанные серверы лицензирования.
ms.assetid: afd7ca11-9db5-4cf3-9706-3c6984789ecd
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода СетспеЦифиедлиценсесерверлист
- Службы удаленных рабочих столов метода СетспеЦифиедлиценсесерверлист, класс Win32_TerminalServiceSetting
- Класс Win32_TerminalServiceSetting службы удаленных рабочих столов, метод СетспеЦифиедлиценсесерверлист
topic_type:
- apiref
api_name:
- Win32_TerminalServiceSetting.SetSpecifiedLicenseServerList
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d10fde34e490f26c287e63dcddae3c62761670bc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105681962"
---
# <a name="setspecifiedlicenseserverlist-method-of-the-win32_terminalservicesetting-class"></a><span data-ttu-id="fbb43-106">Метод СетспеЦифиедлиценсесерверлист \_ класса Win32 терминалсервицесеттинг</span><span class="sxs-lookup"><span data-stu-id="fbb43-106">SetSpecifiedLicenseServerList method of the Win32\_TerminalServiceSetting class</span></span>

<span data-ttu-id="fbb43-107">Обновляет список указанных серверов лицензирования, заменяя все существующие указанные серверы лицензирования.</span><span class="sxs-lookup"><span data-stu-id="fbb43-107">Updates the list of specified license servers, replacing any existing specified license servers.</span></span>

## <a name="syntax"></a><span data-ttu-id="fbb43-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="fbb43-108">Syntax</span></span>


```mof
uint32 SetSpecifiedLicenseServerList(
  [in] string SpecifiedLSList[]
);
```



## <a name="parameters"></a><span data-ttu-id="fbb43-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="fbb43-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fbb43-110">*СпеЦифиедлслист* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="fbb43-110">*SpecifiedLSList* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fbb43-111">Массив строк, содержащий новый список указанных серверов лицензирования.</span><span class="sxs-lookup"><span data-stu-id="fbb43-111">A string array that contains the new list of specified license servers.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fbb43-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="fbb43-112">Return value</span></span>

<span data-ttu-id="fbb43-113">Возвращает значение 0 при успешном выполнении, в противном случае возвращает код ошибки WMI.</span><span class="sxs-lookup"><span data-stu-id="fbb43-113">Returns 0 on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="fbb43-114">Список этих значений см. в разделе [службы удаленных рабочих столов коды ошибок поставщика WMI](terminal-services-wmi-provider-error-codes.md) .</span><span class="sxs-lookup"><span data-stu-id="fbb43-114">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span>

## <a name="requirements"></a><span data-ttu-id="fbb43-115">Требования</span><span class="sxs-lookup"><span data-stu-id="fbb43-115">Requirements</span></span>



| <span data-ttu-id="fbb43-116">Требование</span><span class="sxs-lookup"><span data-stu-id="fbb43-116">Requirement</span></span> | <span data-ttu-id="fbb43-117">Значение</span><span class="sxs-lookup"><span data-stu-id="fbb43-117">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="fbb43-118">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="fbb43-118">Minimum supported client</span></span><br/> | <span data-ttu-id="fbb43-119">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="fbb43-119">None supported</span></span><br/>                                                               |
| <span data-ttu-id="fbb43-120">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="fbb43-120">Minimum supported server</span></span><br/> | <span data-ttu-id="fbb43-121">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="fbb43-121">Windows Server 2008 R2</span></span><br/>                                                       |
| <span data-ttu-id="fbb43-122">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="fbb43-122">Namespace</span></span><br/>                | <span data-ttu-id="fbb43-123">Корневой \\ CIMv2 \\ терминалсервицес</span><span class="sxs-lookup"><span data-stu-id="fbb43-123">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="fbb43-124">MOF</span><span class="sxs-lookup"><span data-stu-id="fbb43-124">MOF</span></span><br/>                      | <dl> <span data-ttu-id="fbb43-125"><dt>Тскфгвми. mof</dt></span><span class="sxs-lookup"><span data-stu-id="fbb43-125"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="fbb43-126">DLL</span><span class="sxs-lookup"><span data-stu-id="fbb43-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fbb43-127"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fbb43-127"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fbb43-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="fbb43-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fbb43-129">**\_Терминалсервицесеттинг Win32**</span><span class="sxs-lookup"><span data-stu-id="fbb43-129">**Win32\_TerminalServiceSetting**</span></span>](win32-terminalservicesetting.md)
</dt> <dt>

[<span data-ttu-id="fbb43-130">**аддлстоспеЦифиедлиценсесерверлист**</span><span class="sxs-lookup"><span data-stu-id="fbb43-130">**AddLSToSpecifiedLicenseServerList**</span></span>](addlstospecifiedlicenseserverlist-win32-terminalservicesetting.md)
</dt> <dt>

[<span data-ttu-id="fbb43-131">**жетспеЦифиедлиценсесерверлист**</span><span class="sxs-lookup"><span data-stu-id="fbb43-131">**GetSpecifiedLicenseServerList**</span></span>](getspecifiedlicenseserverlist-win32-terminalservicesetting.md)
</dt> <dt>

[<span data-ttu-id="fbb43-132">**емптиспеЦифиедлиценсесерверлист**</span><span class="sxs-lookup"><span data-stu-id="fbb43-132">**EmptySpecifiedLicenseServerList**</span></span>](emptyspecifiedlicenseserverlist-win32-terminalservicesetting.md)
</dt> <dt>

[<span data-ttu-id="fbb43-133">**ремовелсфромспеЦифиедлиценсесерверлист**</span><span class="sxs-lookup"><span data-stu-id="fbb43-133">**RemoveLSFromSpecifiedLicenseServerList**</span></span>](removelsfromspecifiedlicenseserverlist-win32-terminalservicesetting.md)
</dt> </dl>

 

 





