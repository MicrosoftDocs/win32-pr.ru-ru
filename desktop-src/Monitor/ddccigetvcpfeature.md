---
title: Функция ДдкЦижетвкпфеатуре
description: Возвращает текущее значение, максимальное значение и тип кода для монитора в виртуальной панели управления.
ms.assetid: 7749d45c-a0d5-44ee-8f91-811677cbf59f
keywords:
- Настройка монитора функции ДдкЦижетвкпфеатуре
topic_type:
- apiref
api_name:
- DDCCIGetVCPFeature
api_location:
- gdi32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5758bbd1c86b9f228b64063fdd05c04cb05bedcb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988627"
---
# <a name="ddccigetvcpfeature-function"></a><span data-ttu-id="cb5fc-104">Функция ДдкЦижетвкпфеатуре</span><span class="sxs-lookup"><span data-stu-id="cb5fc-104">DDCCIGetVCPFeature function</span></span>

> [!IMPORTANT]
> <span data-ttu-id="cb5fc-105">Эта функция используется API конфигурации монитора для доступа к функциональным возможностям драйвера экрана.</span><span class="sxs-lookup"><span data-stu-id="cb5fc-105">This function is used by the monitor configuration API to access functionality in the display driver.</span></span> <span data-ttu-id="cb5fc-106">Приложения не должны вызывать эту функцию.</span><span class="sxs-lookup"><span data-stu-id="cb5fc-106">Applications should not call this function.</span></span>

 

<span data-ttu-id="cb5fc-107">Возвращает текущее значение, максимальное значение и тип кода для монитора в виртуальной панели управления.</span><span class="sxs-lookup"><span data-stu-id="cb5fc-107">Gets the current value, maximum value, and code type of a Virtual Control Panel (VCP) code for a monitor.</span></span>

## <a name="syntax"></a><span data-ttu-id="cb5fc-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="cb5fc-108">Syntax</span></span>


```C++
NTSTATUS WINAPI DDCCIGetVCPFeature(
  _In_      HANDLE             hMonitor,
  _In_      DWORD              dwVCPCode,
  _Out_opt_ LPMC_VCP_CODE_TYPE pvct,
  _Out_     DWORD              *pdwCurrentValue,
  _Out_opt_ DWORD              *pdwMaximumValue
);
```



## <a name="parameters"></a><span data-ttu-id="cb5fc-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="cb5fc-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cb5fc-110">*хмонитор* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="cb5fc-110">*hMonitor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cb5fc-111">Маркер физического монитора.</span><span class="sxs-lookup"><span data-stu-id="cb5fc-111">A handle to a physical monitor.</span></span>

</dd> <dt>

<span data-ttu-id="cb5fc-112">*дввкпкоде* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="cb5fc-112">*dwVCPCode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cb5fc-113">Код, который необходимо запросить.</span><span class="sxs-lookup"><span data-stu-id="cb5fc-113">The VCP code to query.</span></span>

</dd> <dt>

<span data-ttu-id="cb5fc-114">*пвкт* \[ out, необязательно\]</span><span class="sxs-lookup"><span data-stu-id="cb5fc-114">*pvct* \[out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="cb5fc-115">Получает тип кода перечислителя в виде члена перечисления [**\_ \_ \_ типа кода MC**](/windows/desktop/api/LowLevelMonitorConfigurationAPI/ne-lowlevelmonitorconfigurationapi-mc_vcp_code_type) -версии.</span><span class="sxs-lookup"><span data-stu-id="cb5fc-115">Receives the VCP code type, as a member of the [**MC\_VCP\_CODE\_TYPE**](/windows/desktop/api/LowLevelMonitorConfigurationAPI/ne-lowlevelmonitorconfigurationapi-mc_vcp_code_type) enumeration.</span></span>

</dd> <dt>

<span data-ttu-id="cb5fc-116">*пдвкуррентвалуе* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="cb5fc-116">*pdwCurrentValue* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="cb5fc-117">Получает текущее значение кода "код версии + +".</span><span class="sxs-lookup"><span data-stu-id="cb5fc-117">Receives the current value of the VCP code.</span></span>

</dd> <dt>

<span data-ttu-id="cb5fc-118">*пдвмаксимумвалуе* \[ out, необязательно\]</span><span class="sxs-lookup"><span data-stu-id="cb5fc-118">*pdwMaximumValue* \[out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="cb5fc-119">Получает максимальное значение кода "код версии + +".</span><span class="sxs-lookup"><span data-stu-id="cb5fc-119">Receives the maximum value of the VCP code.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cb5fc-120">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="cb5fc-120">Return value</span></span>

<span data-ttu-id="cb5fc-121">Если метод завершается успешно, возвращается **состояние \_ Success**.</span><span class="sxs-lookup"><span data-stu-id="cb5fc-121">If the method succeeds, it returns **STATUS\_SUCCESS**.</span></span> <span data-ttu-id="cb5fc-122">В противном случае возвращается код ошибки **NTSTATUS** .</span><span class="sxs-lookup"><span data-stu-id="cb5fc-122">Otherwise, it returns an **NTSTATUS** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="cb5fc-123">Комментарии</span><span class="sxs-lookup"><span data-stu-id="cb5fc-123">Remarks</span></span>

<span data-ttu-id="cb5fc-124">Приложения должны вызывать [**жетвкпфеатуреандвкпфеатуререпли**](/windows/desktop/api/LowLevelMonitorConfigurationAPI/nf-lowlevelmonitorconfigurationapi-getvcpfeatureandvcpfeaturereply) вместо вызова этой функции.</span><span class="sxs-lookup"><span data-stu-id="cb5fc-124">Applications should call [**GetVCPFeatureAndVCPFeatureReply**](/windows/desktop/api/LowLevelMonitorConfigurationAPI/nf-lowlevelmonitorconfigurationapi-getvcpfeatureandvcpfeaturereply) instead of calling this function.</span></span>

<span data-ttu-id="cb5fc-125">Эта функция не имеет связанной библиотеки импорта.</span><span class="sxs-lookup"><span data-stu-id="cb5fc-125">This function has no associated import library.</span></span> <span data-ttu-id="cb5fc-126">Для вызова этой функции необходимо использовать функции [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) и [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) для динамической привязки к Gdi32.dll.</span><span class="sxs-lookup"><span data-stu-id="cb5fc-126">To call this function, you must use the [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) functions to dynamically link to Gdi32.dll.</span></span>

## <a name="requirements"></a><span data-ttu-id="cb5fc-127">Требования</span><span class="sxs-lookup"><span data-stu-id="cb5fc-127">Requirements</span></span>



| <span data-ttu-id="cb5fc-128">Требование</span><span class="sxs-lookup"><span data-stu-id="cb5fc-128">Requirement</span></span> | <span data-ttu-id="cb5fc-129">Значение</span><span class="sxs-lookup"><span data-stu-id="cb5fc-129">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="cb5fc-130">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="cb5fc-130">Minimum supported client</span></span><br/> | <span data-ttu-id="cb5fc-131">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="cb5fc-131">Windows Vista \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="cb5fc-132">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="cb5fc-132">Minimum supported server</span></span><br/> | <span data-ttu-id="cb5fc-133">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="cb5fc-133">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="cb5fc-134">DLL</span><span class="sxs-lookup"><span data-stu-id="cb5fc-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cb5fc-135"><dt>Gdi32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cb5fc-135"><dt>Gdi32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cb5fc-136">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="cb5fc-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cb5fc-137">Мониторинг функций конфигурации</span><span class="sxs-lookup"><span data-stu-id="cb5fc-137">Monitor Configuration Functions</span></span>](monitor-configuration-functions.md)
</dt> </dl>

 

