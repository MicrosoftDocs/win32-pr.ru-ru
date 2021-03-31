---
title: Метод Жеткуррентвммплугин класса Win32_SessionDirectoryVMMPlugin
description: Возвращает подключаемый модуль наивысшего приоритета, который включен.
ms.assetid: 7712573f-2252-4a3c-820c-b679be5dfd46
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода Жеткуррентвммплугин
- Службы удаленных рабочих столов метода Жеткуррентвммплугин, класс Win32_SessionDirectoryVMMPlugin
- Класс Win32_SessionDirectoryVMMPlugin службы удаленных рабочих столов, метод Жеткуррентвммплугин
topic_type:
- apiref
api_name:
- Win32_SessionDirectoryVMMPlugin.GetCurrentVMMPlugin
api_location:
- TssdWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7162322f4e5e3939309d64e27c93cf8d20da540c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103892666"
---
# <a name="getcurrentvmmplugin-method-of-the-win32_sessiondirectoryvmmplugin-class"></a><span data-ttu-id="c96a9-106">Метод Жеткуррентвммплугин \_ класса Win32 сессиондиректоривммплугин</span><span class="sxs-lookup"><span data-stu-id="c96a9-106">GetCurrentVMMPlugin method of the Win32\_SessionDirectoryVMMPlugin class</span></span>

<span data-ttu-id="c96a9-107">Возвращает подключаемый модуль наивысшего приоритета, который включен.</span><span class="sxs-lookup"><span data-stu-id="c96a9-107">Gets the highest priority plug-in that is enabled.</span></span>

## <a name="syntax"></a><span data-ttu-id="c96a9-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c96a9-108">Syntax</span></span>


```mof
uint32 GetCurrentVMMPlugin(
  [out] string  sName,
  [out] string  sProvider,
  [out] string  sServiceLocation,
  [out] string  sClassID,
  [out] sint32  Priority,
  [out] boolean Enabled
);
```



## <a name="parameters"></a><span data-ttu-id="c96a9-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="c96a9-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c96a9-110">*sName* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="c96a9-110">*sName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c96a9-111">Имя подключаемого модуля.</span><span class="sxs-lookup"><span data-stu-id="c96a9-111">The name of the plug-in.</span></span>

</dd> <dt>

<span data-ttu-id="c96a9-112">*спровидер* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="c96a9-112">*sProvider* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c96a9-113">Имя поставщика подключаемого модуля.</span><span class="sxs-lookup"><span data-stu-id="c96a9-113">The name of the plug-in provider.</span></span>

</dd> <dt>

<span data-ttu-id="c96a9-114">*ссервицелокатион* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="c96a9-114">*sServiceLocation* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c96a9-115">Расположение службы, с которой должен связаться подключаемый модуль.</span><span class="sxs-lookup"><span data-stu-id="c96a9-115">The service location that the plug-in should contact.</span></span>

</dd> <dt>

<span data-ttu-id="c96a9-116">*склассид* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="c96a9-116">*sClassID* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c96a9-117">Идентификатор класса подключаемого модуля.</span><span class="sxs-lookup"><span data-stu-id="c96a9-117">The class identifier of the plug-in.</span></span>

</dd> <dt>

<span data-ttu-id="c96a9-118">*Приоритет* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="c96a9-118">*Priority* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c96a9-119">Приоритет подключаемого модуля.</span><span class="sxs-lookup"><span data-stu-id="c96a9-119">The priority of the plug-in.</span></span> <span data-ttu-id="c96a9-120">Чем выше значение, тем выше приоритет подключаемого модуля.</span><span class="sxs-lookup"><span data-stu-id="c96a9-120">The higher the value, the higher the priority of the plug-in.</span></span>

</dd> <dt>

<span data-ttu-id="c96a9-121">*Включено* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="c96a9-121">*Enabled* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c96a9-122">Указывает, включен ли или отключен подключаемый модуль.</span><span class="sxs-lookup"><span data-stu-id="c96a9-122">Indicates whether the plug-in is enabled or disabled.</span></span> <span data-ttu-id="c96a9-123">**Значение true** , если подключаемый модуль включен или **false** в противном случае.</span><span class="sxs-lookup"><span data-stu-id="c96a9-123">**True** if the plug-in is enabled or **false** otherwise.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c96a9-124">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="c96a9-124">Return value</span></span>

<span data-ttu-id="c96a9-125">Возвращает значение 0 при успешном выполнении, в противном случае возвращает код ошибки WMI.</span><span class="sxs-lookup"><span data-stu-id="c96a9-125">Returns 0 on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="c96a9-126">Список этих значений см. в разделе [службы удаленных рабочих столов коды ошибок поставщика WMI](terminal-services-wmi-provider-error-codes.md) .</span><span class="sxs-lookup"><span data-stu-id="c96a9-126">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span>

## <a name="requirements"></a><span data-ttu-id="c96a9-127">Требования</span><span class="sxs-lookup"><span data-stu-id="c96a9-127">Requirements</span></span>



| <span data-ttu-id="c96a9-128">Требование</span><span class="sxs-lookup"><span data-stu-id="c96a9-128">Requirement</span></span> | <span data-ttu-id="c96a9-129">Значение</span><span class="sxs-lookup"><span data-stu-id="c96a9-129">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="c96a9-130">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="c96a9-130">Minimum supported client</span></span><br/> | <span data-ttu-id="c96a9-131">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="c96a9-131">None supported</span></span><br/>                                                              |
| <span data-ttu-id="c96a9-132">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="c96a9-132">Minimum supported server</span></span><br/> | <span data-ttu-id="c96a9-133">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="c96a9-133">Windows Server 2008 R2</span></span><br/>                                                      |
| <span data-ttu-id="c96a9-134">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="c96a9-134">Namespace</span></span><br/>                | <span data-ttu-id="c96a9-135">Корневой \\ CIMv2 \\ терминалсервицес</span><span class="sxs-lookup"><span data-stu-id="c96a9-135">Root\\CIMv2\\TerminalServices</span></span><br/>                                               |
| <span data-ttu-id="c96a9-136">MOF</span><span class="sxs-lookup"><span data-stu-id="c96a9-136">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c96a9-137"><dt>Тссдвми. mof</dt></span><span class="sxs-lookup"><span data-stu-id="c96a9-137"><dt>TssdWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="c96a9-138">DLL</span><span class="sxs-lookup"><span data-stu-id="c96a9-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c96a9-139"><dt>TssdWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c96a9-139"><dt>TssdWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c96a9-140">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c96a9-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c96a9-141">**\_Сессиондиректоривммплугин Win32**</span><span class="sxs-lookup"><span data-stu-id="c96a9-141">**Win32\_SessionDirectoryVMMPlugin**</span></span>](win32-sessiondirectoryvmmplugin.md)
</dt> </dl>

 

 





