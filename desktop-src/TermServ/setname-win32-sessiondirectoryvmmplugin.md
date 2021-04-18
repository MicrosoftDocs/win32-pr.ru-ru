---
title: Метод SetName класса Win32_SessionDirectoryVMMPlugin
description: Задает имя подключаемого модуля.
ms.assetid: 8af4abca-f147-4027-91fb-4d669b58caa4
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода SetName
- Службы удаленных рабочих столов метода SetName, класс Win32_SessionDirectoryVMMPlugin
- Класс Win32_SessionDirectoryVMMPlugin службы удаленных рабочих столов, метод SetName
topic_type:
- apiref
api_name:
- Win32_SessionDirectoryVMMPlugin.SetName
api_location:
- TssdWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2dc9902e8d5931f0800dc6c62d36815f4f78db73
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104340665"
---
# <a name="setname-method-of-the-win32_sessiondirectoryvmmplugin-class"></a><span data-ttu-id="cd7dc-106">Метод SetName \_ класса Win32 сессиондиректоривммплугин</span><span class="sxs-lookup"><span data-stu-id="cd7dc-106">SetName method of the Win32\_SessionDirectoryVMMPlugin class</span></span>

<span data-ttu-id="cd7dc-107">Задает имя подключаемого модуля.</span><span class="sxs-lookup"><span data-stu-id="cd7dc-107">Sets the name of the plug-in.</span></span>

## <a name="syntax"></a><span data-ttu-id="cd7dc-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="cd7dc-108">Syntax</span></span>


```mof
uint32 SetName(
  [in] string sName
);
```



## <a name="parameters"></a><span data-ttu-id="cd7dc-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="cd7dc-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cd7dc-110">*sName* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="cd7dc-110">*sName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cd7dc-111">Имя подключаемого модуля.</span><span class="sxs-lookup"><span data-stu-id="cd7dc-111">The name of the plug-in.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cd7dc-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="cd7dc-112">Return value</span></span>

<span data-ttu-id="cd7dc-113">Возвращает значение 0 при успешном выполнении, в противном случае возвращает код ошибки WMI.</span><span class="sxs-lookup"><span data-stu-id="cd7dc-113">Returns 0 on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="cd7dc-114">Список этих значений см. в разделе [службы удаленных рабочих столов коды ошибок поставщика WMI](terminal-services-wmi-provider-error-codes.md) .</span><span class="sxs-lookup"><span data-stu-id="cd7dc-114">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span>

## <a name="requirements"></a><span data-ttu-id="cd7dc-115">Требования</span><span class="sxs-lookup"><span data-stu-id="cd7dc-115">Requirements</span></span>



| <span data-ttu-id="cd7dc-116">Требование</span><span class="sxs-lookup"><span data-stu-id="cd7dc-116">Requirement</span></span> | <span data-ttu-id="cd7dc-117">Значение</span><span class="sxs-lookup"><span data-stu-id="cd7dc-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="cd7dc-118">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="cd7dc-118">Minimum supported client</span></span><br/> | <span data-ttu-id="cd7dc-119">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="cd7dc-119">None supported</span></span><br/>                                                              |
| <span data-ttu-id="cd7dc-120">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="cd7dc-120">Minimum supported server</span></span><br/> | <span data-ttu-id="cd7dc-121">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="cd7dc-121">Windows Server 2008 R2</span></span><br/>                                                      |
| <span data-ttu-id="cd7dc-122">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="cd7dc-122">Namespace</span></span><br/>                | <span data-ttu-id="cd7dc-123">Корневой \\ CIMv2 \\ терминалсервицес</span><span class="sxs-lookup"><span data-stu-id="cd7dc-123">Root\\CIMv2\\TerminalServices</span></span><br/>                                               |
| <span data-ttu-id="cd7dc-124">MOF</span><span class="sxs-lookup"><span data-stu-id="cd7dc-124">MOF</span></span><br/>                      | <dl> <span data-ttu-id="cd7dc-125"><dt>Тссдвми. mof</dt></span><span class="sxs-lookup"><span data-stu-id="cd7dc-125"><dt>TssdWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="cd7dc-126">DLL</span><span class="sxs-lookup"><span data-stu-id="cd7dc-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cd7dc-127"><dt>TssdWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cd7dc-127"><dt>TssdWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cd7dc-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="cd7dc-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cd7dc-129">**\_Сессиондиректоривммплугин Win32**</span><span class="sxs-lookup"><span data-stu-id="cd7dc-129">**Win32\_SessionDirectoryVMMPlugin**</span></span>](win32-sessiondirectoryvmmplugin.md)
</dt> </dl>

 

 





