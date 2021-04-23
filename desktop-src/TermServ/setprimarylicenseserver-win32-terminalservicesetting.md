---
title: Метод Сетпримарилиценсесервер класса Win32_TerminalServiceSetting
description: Задает указанный сервер лицензирования в качестве первой записи в списке указанных серверов лицензирования.
ms.assetid: 8921e861-3b9a-49c5-a691-ded7be18ca0a
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода Сетпримарилиценсесервер
- Службы удаленных рабочих столов метода Сетпримарилиценсесервер, класс Win32_TerminalServiceSetting
- Класс Win32_TerminalServiceSetting службы удаленных рабочих столов, метод Сетпримарилиценсесервер
topic_type:
- apiref
api_name:
- Win32_TerminalServiceSetting.SetPrimaryLicenseServer
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 61d73212230d1ca69e0a0809c48b8f2985920045
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103891605"
---
# <a name="setprimarylicenseserver-method-of-the-win32_terminalservicesetting-class"></a><span data-ttu-id="e28f5-106">Метод Сетпримарилиценсесервер \_ класса Win32 терминалсервицесеттинг</span><span class="sxs-lookup"><span data-stu-id="e28f5-106">SetPrimaryLicenseServer method of the Win32\_TerminalServiceSetting class</span></span>

<span data-ttu-id="e28f5-107">Задает указанный сервер лицензирования в качестве первой записи в списке указанных серверов лицензирования.</span><span class="sxs-lookup"><span data-stu-id="e28f5-107">Sets the given license server as the first entry in the list of specified license servers.</span></span>

## <a name="syntax"></a><span data-ttu-id="e28f5-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e28f5-108">Syntax</span></span>


```mof
uint32 SetPrimaryLicenseServer(
  [in] string LicenseServerName
);
```



## <a name="parameters"></a><span data-ttu-id="e28f5-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="e28f5-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e28f5-110">*Лиценсесервернаме* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="e28f5-110">*LicenseServerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e28f5-111">Имя сервера лицензирования.</span><span class="sxs-lookup"><span data-stu-id="e28f5-111">The name of the license server.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e28f5-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="e28f5-112">Return value</span></span>

<span data-ttu-id="e28f5-113">Возвращает значение 0 при успешном выполнении, в противном случае возвращает код ошибки WMI.</span><span class="sxs-lookup"><span data-stu-id="e28f5-113">Returns 0 on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="e28f5-114">Список этих значений см. в разделе [службы удаленных рабочих столов коды ошибок поставщика WMI](terminal-services-wmi-provider-error-codes.md) .</span><span class="sxs-lookup"><span data-stu-id="e28f5-114">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span>

## <a name="requirements"></a><span data-ttu-id="e28f5-115">Требования</span><span class="sxs-lookup"><span data-stu-id="e28f5-115">Requirements</span></span>



| <span data-ttu-id="e28f5-116">Требование</span><span class="sxs-lookup"><span data-stu-id="e28f5-116">Requirement</span></span> | <span data-ttu-id="e28f5-117">Значение</span><span class="sxs-lookup"><span data-stu-id="e28f5-117">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e28f5-118">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="e28f5-118">Minimum supported client</span></span><br/> | <span data-ttu-id="e28f5-119">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="e28f5-119">None supported</span></span><br/>                                                               |
| <span data-ttu-id="e28f5-120">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="e28f5-120">Minimum supported server</span></span><br/> | <span data-ttu-id="e28f5-121">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="e28f5-121">Windows Server 2008 R2</span></span><br/>                                                       |
| <span data-ttu-id="e28f5-122">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="e28f5-122">Namespace</span></span><br/>                | <span data-ttu-id="e28f5-123">Корневой \\ CIMv2 \\ терминалсервицес</span><span class="sxs-lookup"><span data-stu-id="e28f5-123">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="e28f5-124">MOF</span><span class="sxs-lookup"><span data-stu-id="e28f5-124">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e28f5-125"><dt>Тскфгвми. mof</dt></span><span class="sxs-lookup"><span data-stu-id="e28f5-125"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="e28f5-126">DLL</span><span class="sxs-lookup"><span data-stu-id="e28f5-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e28f5-127"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e28f5-127"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e28f5-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e28f5-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e28f5-129">**\_Терминалсервицесеттинг Win32**</span><span class="sxs-lookup"><span data-stu-id="e28f5-129">**Win32\_TerminalServiceSetting**</span></span>](win32-terminalservicesetting.md)
</dt> </dl>

 

 





