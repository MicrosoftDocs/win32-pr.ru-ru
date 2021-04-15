---
title: Метод Сетсервицелокатион класса Win32_SessionDirectoryVMMPlugin
description: Задает расположение службы для подключаемого модуля.
ms.assetid: e886a40b-9ea9-4159-a2ea-776160559410
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода Сетсервицелокатион
- Службы удаленных рабочих столов метода Сетсервицелокатион, класс Win32_SessionDirectoryVMMPlugin
- Класс Win32_SessionDirectoryVMMPlugin службы удаленных рабочих столов, метод Сетсервицелокатион
topic_type:
- apiref
api_name:
- Win32_SessionDirectoryVMMPlugin.SetServiceLocation
api_location:
- TssdWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 64c16a6bbe802052f53d28d4cd8cc2b9ab559b61
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104534550"
---
# <a name="setservicelocation-method-of-the-win32_sessiondirectoryvmmplugin-class"></a><span data-ttu-id="b4ae9-106">Метод Сетсервицелокатион \_ класса Win32 сессиондиректоривммплугин</span><span class="sxs-lookup"><span data-stu-id="b4ae9-106">SetServiceLocation method of the Win32\_SessionDirectoryVMMPlugin class</span></span>

<span data-ttu-id="b4ae9-107">Задает расположение службы для подключаемого модуля.</span><span class="sxs-lookup"><span data-stu-id="b4ae9-107">Sets the service location for the plug-in.</span></span>

## <a name="syntax"></a><span data-ttu-id="b4ae9-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b4ae9-108">Syntax</span></span>


```mof
uint32 SetServiceLocation(
  [in] string sServiceLocation
);
```



## <a name="parameters"></a><span data-ttu-id="b4ae9-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="b4ae9-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b4ae9-110">*ссервицелокатион* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="b4ae9-110">*sServiceLocation* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b4ae9-111">Расположение службы, с которой должен связаться подключаемый модуль.</span><span class="sxs-lookup"><span data-stu-id="b4ae9-111">The service location that the plug-in should contact.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b4ae9-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="b4ae9-112">Return value</span></span>

<span data-ttu-id="b4ae9-113">Возвращает значение 0 при успешном выполнении, в противном случае возвращает код ошибки WMI.</span><span class="sxs-lookup"><span data-stu-id="b4ae9-113">Returns 0 on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="b4ae9-114">Список этих значений см. в разделе [службы удаленных рабочих столов коды ошибок поставщика WMI](terminal-services-wmi-provider-error-codes.md) .</span><span class="sxs-lookup"><span data-stu-id="b4ae9-114">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span>

## <a name="requirements"></a><span data-ttu-id="b4ae9-115">Требования</span><span class="sxs-lookup"><span data-stu-id="b4ae9-115">Requirements</span></span>



| <span data-ttu-id="b4ae9-116">Требование</span><span class="sxs-lookup"><span data-stu-id="b4ae9-116">Requirement</span></span> | <span data-ttu-id="b4ae9-117">Значение</span><span class="sxs-lookup"><span data-stu-id="b4ae9-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="b4ae9-118">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="b4ae9-118">Minimum supported client</span></span><br/> | <span data-ttu-id="b4ae9-119">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="b4ae9-119">None supported</span></span><br/>                                                              |
| <span data-ttu-id="b4ae9-120">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="b4ae9-120">Minimum supported server</span></span><br/> | <span data-ttu-id="b4ae9-121">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="b4ae9-121">Windows Server 2008 R2</span></span><br/>                                                      |
| <span data-ttu-id="b4ae9-122">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="b4ae9-122">Namespace</span></span><br/>                | <span data-ttu-id="b4ae9-123">Корневой \\ CIMv2 \\ терминалсервицес</span><span class="sxs-lookup"><span data-stu-id="b4ae9-123">Root\\CIMv2\\TerminalServices</span></span><br/>                                               |
| <span data-ttu-id="b4ae9-124">MOF</span><span class="sxs-lookup"><span data-stu-id="b4ae9-124">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b4ae9-125"><dt>Тссдвми. mof</dt></span><span class="sxs-lookup"><span data-stu-id="b4ae9-125"><dt>TssdWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="b4ae9-126">DLL</span><span class="sxs-lookup"><span data-stu-id="b4ae9-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b4ae9-127"><dt>TssdWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b4ae9-127"><dt>TssdWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b4ae9-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b4ae9-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b4ae9-129">**\_Сессиондиректоривммплугин Win32**</span><span class="sxs-lookup"><span data-stu-id="b4ae9-129">**Win32\_SessionDirectoryVMMPlugin**</span></span>](win32-sessiondirectoryvmmplugin.md)
</dt> </dl>

 

 





