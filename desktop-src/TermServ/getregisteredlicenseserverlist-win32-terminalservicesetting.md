---
title: Метод Жетрегистередлиценсесерверлист класса Win32_TerminalServiceSetting
description: Возвращает список зарегистрированных серверов лицензирования.
ms.assetid: 32e06b4b-652f-4977-be1f-6d52983d2605
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода Жетрегистередлиценсесерверлист
- Службы удаленных рабочих столов метода Жетрегистередлиценсесерверлист, класс Win32_TerminalServiceSetting
- Класс Win32_TerminalServiceSetting службы удаленных рабочих столов, метод Жетрегистередлиценсесерверлист
topic_type:
- apiref
api_name:
- Win32_TerminalServiceSetting.GetRegisteredLicenseServerList
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5336910956a0d281fbfc8fbc65e1d3b8d5018cb2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105682084"
---
# <a name="getregisteredlicenseserverlist-method-of-the-win32_terminalservicesetting-class"></a><span data-ttu-id="c72f5-106">Метод Жетрегистередлиценсесерверлист \_ класса Win32 терминалсервицесеттинг</span><span class="sxs-lookup"><span data-stu-id="c72f5-106">GetRegisteredLicenseServerList method of the Win32\_TerminalServiceSetting class</span></span>

<span data-ttu-id="c72f5-107">Возвращает список зарегистрированных серверов лицензирования.</span><span class="sxs-lookup"><span data-stu-id="c72f5-107">Gets the list of registered license servers.</span></span>

## <a name="syntax"></a><span data-ttu-id="c72f5-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c72f5-108">Syntax</span></span>


```mof
uint32 GetRegisteredLicenseServerList(
  [out] string RegisteredLSList[]
);
```



## <a name="parameters"></a><span data-ttu-id="c72f5-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="c72f5-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c72f5-110">*Регистередлслист* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="c72f5-110">*RegisteredLSList* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c72f5-111">Массив строк, который получает список зарегистрированных серверов лицензирования.</span><span class="sxs-lookup"><span data-stu-id="c72f5-111">A string array that receives the list of registered license servers.</span></span> <span data-ttu-id="c72f5-112">Если нет зарегистрированных серверов лицензирования, этот массив будет пустым.</span><span class="sxs-lookup"><span data-stu-id="c72f5-112">If there are no registered license servers, this array will be empty.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c72f5-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="c72f5-113">Return value</span></span>

<span data-ttu-id="c72f5-114">Возвращает значение 0 при успешном выполнении, в противном случае возвращает код ошибки WMI.</span><span class="sxs-lookup"><span data-stu-id="c72f5-114">Returns 0 on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="c72f5-115">Список этих значений см. в разделе [службы удаленных рабочих столов коды ошибок поставщика WMI](terminal-services-wmi-provider-error-codes.md) .</span><span class="sxs-lookup"><span data-stu-id="c72f5-115">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span>

## <a name="requirements"></a><span data-ttu-id="c72f5-116">Требования</span><span class="sxs-lookup"><span data-stu-id="c72f5-116">Requirements</span></span>



| <span data-ttu-id="c72f5-117">Требование</span><span class="sxs-lookup"><span data-stu-id="c72f5-117">Requirement</span></span> | <span data-ttu-id="c72f5-118">Значение</span><span class="sxs-lookup"><span data-stu-id="c72f5-118">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c72f5-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="c72f5-119">Minimum supported client</span></span><br/> | <span data-ttu-id="c72f5-120">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="c72f5-120">None supported</span></span><br/>                                                               |
| <span data-ttu-id="c72f5-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="c72f5-121">Minimum supported server</span></span><br/> | <span data-ttu-id="c72f5-122">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="c72f5-122">Windows Server 2008 R2</span></span><br/>                                                       |
| <span data-ttu-id="c72f5-123">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="c72f5-123">Namespace</span></span><br/>                | <span data-ttu-id="c72f5-124">Корневой \\ CIMv2 \\ терминалсервицес</span><span class="sxs-lookup"><span data-stu-id="c72f5-124">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="c72f5-125">MOF</span><span class="sxs-lookup"><span data-stu-id="c72f5-125">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c72f5-126"><dt>Тскфгвми. mof</dt></span><span class="sxs-lookup"><span data-stu-id="c72f5-126"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="c72f5-127">DLL</span><span class="sxs-lookup"><span data-stu-id="c72f5-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c72f5-128"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c72f5-128"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c72f5-129">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c72f5-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c72f5-130">**\_Терминалсервицесеттинг Win32**</span><span class="sxs-lookup"><span data-stu-id="c72f5-130">**Win32\_TerminalServiceSetting**</span></span>](win32-terminalservicesetting.md)
</dt> </dl>

 

 





