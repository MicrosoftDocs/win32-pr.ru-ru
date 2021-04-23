---
title: Метод SetPriority класса Win32_SessionDirectoryVMMPlugin
description: Задает приоритет подключаемого модуля.
ms.assetid: ddcf30cd-b87c-4869-80fc-ec92092e0df3
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода SetPriority
- Службы удаленных рабочих столов метода SetPriority, класс Win32_SessionDirectoryVMMPlugin
- Класс Win32_SessionDirectoryVMMPlugin службы удаленных рабочих столов, метод SetPriority
topic_type:
- apiref
api_name:
- Win32_SessionDirectoryVMMPlugin.SetPriority
api_location:
- TssdWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e5d20dbc4af332d0c658f819f8e47f5b3eb4e95b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103989338"
---
# <a name="setpriority-method-of-the-win32_sessiondirectoryvmmplugin-class"></a><span data-ttu-id="a5f51-106">Метод SetPriority \_ класса Win32 сессиондиректоривммплугин</span><span class="sxs-lookup"><span data-stu-id="a5f51-106">SetPriority method of the Win32\_SessionDirectoryVMMPlugin class</span></span>

<span data-ttu-id="a5f51-107">Задает приоритет подключаемого модуля.</span><span class="sxs-lookup"><span data-stu-id="a5f51-107">Sets the priority of the plug-in.</span></span>

## <a name="syntax"></a><span data-ttu-id="a5f51-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a5f51-108">Syntax</span></span>


```mof
uint32 SetPriority(
  [in] sint32 Priority
);
```



## <a name="parameters"></a><span data-ttu-id="a5f51-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="a5f51-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a5f51-110">*Приоритет* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="a5f51-110">*Priority* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a5f51-111">Приоритет подключаемого модуля.</span><span class="sxs-lookup"><span data-stu-id="a5f51-111">The priority of the plug-in.</span></span> <span data-ttu-id="a5f51-112">Чем выше значение, тем выше приоритет подключаемого модуля.</span><span class="sxs-lookup"><span data-stu-id="a5f51-112">The higher the value, the higher the priority of the plug-in.</span></span> <span data-ttu-id="a5f51-113">По умолчанию приоритет равен нулю.</span><span class="sxs-lookup"><span data-stu-id="a5f51-113">The priority is zero by default.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a5f51-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="a5f51-114">Return value</span></span>

<span data-ttu-id="a5f51-115">Возвращает значение 0 при успешном выполнении, в противном случае возвращает код ошибки WMI.</span><span class="sxs-lookup"><span data-stu-id="a5f51-115">Returns 0 on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="a5f51-116">Список этих значений см. в разделе [службы удаленных рабочих столов коды ошибок поставщика WMI](terminal-services-wmi-provider-error-codes.md) .</span><span class="sxs-lookup"><span data-stu-id="a5f51-116">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span>

## <a name="requirements"></a><span data-ttu-id="a5f51-117">Требования</span><span class="sxs-lookup"><span data-stu-id="a5f51-117">Requirements</span></span>



| <span data-ttu-id="a5f51-118">Требование</span><span class="sxs-lookup"><span data-stu-id="a5f51-118">Requirement</span></span> | <span data-ttu-id="a5f51-119">Значение</span><span class="sxs-lookup"><span data-stu-id="a5f51-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="a5f51-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="a5f51-120">Minimum supported client</span></span><br/> | <span data-ttu-id="a5f51-121">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="a5f51-121">None supported</span></span><br/>                                                              |
| <span data-ttu-id="a5f51-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="a5f51-122">Minimum supported server</span></span><br/> | <span data-ttu-id="a5f51-123">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="a5f51-123">Windows Server 2008 R2</span></span><br/>                                                      |
| <span data-ttu-id="a5f51-124">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="a5f51-124">Namespace</span></span><br/>                | <span data-ttu-id="a5f51-125">Корневой \\ CIMv2 \\ терминалсервицес</span><span class="sxs-lookup"><span data-stu-id="a5f51-125">Root\\CIMv2\\TerminalServices</span></span><br/>                                               |
| <span data-ttu-id="a5f51-126">MOF</span><span class="sxs-lookup"><span data-stu-id="a5f51-126">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a5f51-127"><dt>Тссдвми. mof</dt></span><span class="sxs-lookup"><span data-stu-id="a5f51-127"><dt>TssdWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="a5f51-128">DLL</span><span class="sxs-lookup"><span data-stu-id="a5f51-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a5f51-129"><dt>TssdWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a5f51-129"><dt>TssdWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a5f51-130">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a5f51-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a5f51-131">**\_Сессиондиректоривммплугин Win32**</span><span class="sxs-lookup"><span data-stu-id="a5f51-131">**Win32\_SessionDirectoryVMMPlugin**</span></span>](win32-sessiondirectoryvmmplugin.md)
</dt> </dl>

 

 





