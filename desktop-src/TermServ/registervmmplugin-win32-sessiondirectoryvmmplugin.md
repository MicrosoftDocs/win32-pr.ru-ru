---
title: Метод Регистервммплугин класса Win32_SessionDirectoryVMMPlugin
description: Регистрирует новый подключаемый модуль VMM.
ms.assetid: 8fa6109e-6320-4ad1-b313-f100d8383f85
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода Регистервммплугин
- Службы удаленных рабочих столов метода Регистервммплугин, класс Win32_SessionDirectoryVMMPlugin
- Класс Win32_SessionDirectoryVMMPlugin службы удаленных рабочих столов, метод Регистервммплугин
topic_type:
- apiref
api_name:
- Win32_SessionDirectoryVMMPlugin.RegisterVMMPlugin
api_location:
- TssdWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 381be34f9398147b323fa99093479da48adfd480
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104415153"
---
# <a name="registervmmplugin-method-of-the-win32_sessiondirectoryvmmplugin-class"></a><span data-ttu-id="49ab4-106">Метод Регистервммплугин \_ класса Win32 сессиондиректоривммплугин</span><span class="sxs-lookup"><span data-stu-id="49ab4-106">RegisterVMMPlugin method of the Win32\_SessionDirectoryVMMPlugin class</span></span>

<span data-ttu-id="49ab4-107">Регистрирует новый подключаемый модуль VMM.</span><span class="sxs-lookup"><span data-stu-id="49ab4-107">Registers a new VMM plug-in.</span></span>

## <a name="syntax"></a><span data-ttu-id="49ab4-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="49ab4-108">Syntax</span></span>


```mof
uint32 RegisterVMMPlugin(
  [in] string  sName,
  [in] string  sProvider,
  [in] string  sServiceLocation,
  [in] string  sClassID,
  [in] sint32  Priority = ,
  [in] boolean Enabled = 
);
```



## <a name="parameters"></a><span data-ttu-id="49ab4-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="49ab4-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="49ab4-110">*sName* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="49ab4-110">*sName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="49ab4-111">Имя подключаемого модуля.</span><span class="sxs-lookup"><span data-stu-id="49ab4-111">The name of the plug-in.</span></span>

</dd> <dt>

<span data-ttu-id="49ab4-112">*спровидер* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="49ab4-112">*sProvider* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="49ab4-113">Имя поставщика подключаемого модуля.</span><span class="sxs-lookup"><span data-stu-id="49ab4-113">The name of the plug-in provider.</span></span>

</dd> <dt>

<span data-ttu-id="49ab4-114">*ссервицелокатион* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="49ab4-114">*sServiceLocation* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="49ab4-115">Расположение службы, с которой должен связаться подключаемый модуль.</span><span class="sxs-lookup"><span data-stu-id="49ab4-115">The service location that the plug-in should contact.</span></span>

</dd> <dt>

<span data-ttu-id="49ab4-116">*склассид* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="49ab4-116">*sClassID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="49ab4-117">Идентификатор класса подключаемого модуля.</span><span class="sxs-lookup"><span data-stu-id="49ab4-117">The class identifier of the plug-in.</span></span>

</dd> <dt>

<span data-ttu-id="49ab4-118">*Приоритет* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="49ab4-118">*Priority* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="49ab4-119">Приоритет подключаемого модуля.</span><span class="sxs-lookup"><span data-stu-id="49ab4-119">The priority of the plug-in.</span></span> <span data-ttu-id="49ab4-120">Чем выше значение, тем выше приоритет подключаемого модуля.</span><span class="sxs-lookup"><span data-stu-id="49ab4-120">The higher the value, the higher the priority of the plug-in.</span></span>

</dd> <dt>

<span data-ttu-id="49ab4-121">*Включено* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="49ab4-121">*Enabled* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="49ab4-122">Указывает, включен ли или отключен подключаемый модуль.</span><span class="sxs-lookup"><span data-stu-id="49ab4-122">Indicates whether the plug-in is enabled or disabled.</span></span> <span data-ttu-id="49ab4-123">**Значение true** , если подключаемый модуль включен или **false** в противном случае.</span><span class="sxs-lookup"><span data-stu-id="49ab4-123">**True** if the plug-in is enabled or **false** otherwise.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="49ab4-124">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="49ab4-124">Return value</span></span>

<span data-ttu-id="49ab4-125">Возвращает значение 0 при успешном выполнении, в противном случае возвращает код ошибки WMI.</span><span class="sxs-lookup"><span data-stu-id="49ab4-125">Returns 0 on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="49ab4-126">Список этих значений см. в разделе [службы удаленных рабочих столов коды ошибок поставщика WMI](terminal-services-wmi-provider-error-codes.md) .</span><span class="sxs-lookup"><span data-stu-id="49ab4-126">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span>

## <a name="requirements"></a><span data-ttu-id="49ab4-127">Требования</span><span class="sxs-lookup"><span data-stu-id="49ab4-127">Requirements</span></span>



| <span data-ttu-id="49ab4-128">Требование</span><span class="sxs-lookup"><span data-stu-id="49ab4-128">Requirement</span></span> | <span data-ttu-id="49ab4-129">Значение</span><span class="sxs-lookup"><span data-stu-id="49ab4-129">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="49ab4-130">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="49ab4-130">Minimum supported client</span></span><br/> | <span data-ttu-id="49ab4-131">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="49ab4-131">None supported</span></span><br/>                                                              |
| <span data-ttu-id="49ab4-132">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="49ab4-132">Minimum supported server</span></span><br/> | <span data-ttu-id="49ab4-133">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="49ab4-133">Windows Server 2008 R2</span></span><br/>                                                      |
| <span data-ttu-id="49ab4-134">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="49ab4-134">Namespace</span></span><br/>                | <span data-ttu-id="49ab4-135">Корневой \\ CIMv2 \\ терминалсервицес</span><span class="sxs-lookup"><span data-stu-id="49ab4-135">Root\\CIMv2\\TerminalServices</span></span><br/>                                               |
| <span data-ttu-id="49ab4-136">MOF</span><span class="sxs-lookup"><span data-stu-id="49ab4-136">MOF</span></span><br/>                      | <dl> <span data-ttu-id="49ab4-137"><dt>Тссдвми. mof</dt></span><span class="sxs-lookup"><span data-stu-id="49ab4-137"><dt>TssdWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="49ab4-138">DLL</span><span class="sxs-lookup"><span data-stu-id="49ab4-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="49ab4-139"><dt>TssdWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="49ab4-139"><dt>TssdWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="49ab4-140">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="49ab4-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="49ab4-141">**\_Сессиондиректоривммплугин Win32**</span><span class="sxs-lookup"><span data-stu-id="49ab4-141">**Win32\_SessionDirectoryVMMPlugin**</span></span>](win32-sessiondirectoryvmmplugin.md)
</dt> </dl>

 

 





