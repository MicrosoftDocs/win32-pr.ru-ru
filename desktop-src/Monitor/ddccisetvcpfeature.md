---
title: Функция ДдкЦисетвкпфеатуре
description: Задает значение кода для монитора в виртуальной панели управления.
ms.assetid: 1069588b-5f8a-49da-b857-6f0a0c737a11
keywords:
- Настройка монитора функции ДдкЦисетвкпфеатуре
topic_type:
- apiref
api_name:
- DDCCISetVCPFeature
api_location:
- gdi32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a72da2b2540c73e023a753a3fdb28507f8cbb40d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104135835"
---
# <a name="ddccisetvcpfeature-function"></a><span data-ttu-id="9d55f-104">Функция ДдкЦисетвкпфеатуре</span><span class="sxs-lookup"><span data-stu-id="9d55f-104">DDCCISetVCPFeature function</span></span>

> [!IMPORTANT]
> <span data-ttu-id="9d55f-105">Эта функция используется API конфигурации монитора для доступа к функциональным возможностям драйвера экрана.</span><span class="sxs-lookup"><span data-stu-id="9d55f-105">This function is used by the monitor configuration API to access functionality in the display driver.</span></span> <span data-ttu-id="9d55f-106">Приложения не должны вызывать эту функцию.</span><span class="sxs-lookup"><span data-stu-id="9d55f-106">Applications should not call this function.</span></span>

 

<span data-ttu-id="9d55f-107">Задает значение кода для монитора в виртуальной панели управления.</span><span class="sxs-lookup"><span data-stu-id="9d55f-107">Sets the value of a Virtual Control Panel (VCP) code for a monitor.</span></span>

## <a name="syntax"></a><span data-ttu-id="9d55f-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="9d55f-108">Syntax</span></span>


```C++
NTSTATUS WINAPI DDCCISetVCPFeature(
  _In_ HANDLE hMonitor,
  _In_ DWORD  dwVCPCode,
  _In_ DWORD  dwNewValue
);
```



## <a name="parameters"></a><span data-ttu-id="9d55f-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="9d55f-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9d55f-110">*хмонитор* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="9d55f-110">*hMonitor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9d55f-111">Маркер физического монитора.</span><span class="sxs-lookup"><span data-stu-id="9d55f-111">A handle to a physical monitor.</span></span>

</dd> <dt>

<span data-ttu-id="9d55f-112">*дввкпкоде* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="9d55f-112">*dwVCPCode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9d55f-113">Заданный код.</span><span class="sxs-lookup"><span data-stu-id="9d55f-113">The VCP code to set.</span></span>

</dd> <dt>

<span data-ttu-id="9d55f-114">*двневвалуе* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="9d55f-114">*dwNewValue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9d55f-115">Значение кода "код версии".</span><span class="sxs-lookup"><span data-stu-id="9d55f-115">The value of the VCP code.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9d55f-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="9d55f-116">Return value</span></span>

<span data-ttu-id="9d55f-117">Если метод завершается успешно, возвращается **состояние \_ Success**.</span><span class="sxs-lookup"><span data-stu-id="9d55f-117">If the method succeeds, it returns **STATUS\_SUCCESS**.</span></span> <span data-ttu-id="9d55f-118">В противном случае возвращается код ошибки **NTSTATUS** .</span><span class="sxs-lookup"><span data-stu-id="9d55f-118">Otherwise, it returns an **NTSTATUS** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="9d55f-119">Комментарии</span><span class="sxs-lookup"><span data-stu-id="9d55f-119">Remarks</span></span>

<span data-ttu-id="9d55f-120">Приложения должны вызывать [**сетвкпфеатуре**](/windows/desktop/api/LowLevelMonitorConfigurationAPI/nf-lowlevelmonitorconfigurationapi-setvcpfeature) вместо вызова этой функции.</span><span class="sxs-lookup"><span data-stu-id="9d55f-120">Applications should call [**SetVCPFeature**](/windows/desktop/api/LowLevelMonitorConfigurationAPI/nf-lowlevelmonitorconfigurationapi-setvcpfeature) instead of calling this function.</span></span>

<span data-ttu-id="9d55f-121">Эта функция не имеет связанной библиотеки импорта.</span><span class="sxs-lookup"><span data-stu-id="9d55f-121">This function has no associated import library.</span></span> <span data-ttu-id="9d55f-122">Для вызова этой функции необходимо использовать функции [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) и [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) для динамической привязки к Gdi32.dll.</span><span class="sxs-lookup"><span data-stu-id="9d55f-122">To call this function, you must use the [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) functions to dynamically link to Gdi32.dll.</span></span>

## <a name="requirements"></a><span data-ttu-id="9d55f-123">Требования</span><span class="sxs-lookup"><span data-stu-id="9d55f-123">Requirements</span></span>



| <span data-ttu-id="9d55f-124">Требование</span><span class="sxs-lookup"><span data-stu-id="9d55f-124">Requirement</span></span> | <span data-ttu-id="9d55f-125">Значение</span><span class="sxs-lookup"><span data-stu-id="9d55f-125">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="9d55f-126">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="9d55f-126">Minimum supported client</span></span><br/> | <span data-ttu-id="9d55f-127">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="9d55f-127">Windows Vista \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="9d55f-128">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="9d55f-128">Minimum supported server</span></span><br/> | <span data-ttu-id="9d55f-129">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="9d55f-129">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="9d55f-130">DLL</span><span class="sxs-lookup"><span data-stu-id="9d55f-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9d55f-131"><dt>Gdi32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9d55f-131"><dt>Gdi32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9d55f-132">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="9d55f-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9d55f-133">Мониторинг функций конфигурации</span><span class="sxs-lookup"><span data-stu-id="9d55f-133">Monitor Configuration Functions</span></span>](monitor-configuration-functions.md)
</dt> </dl>

 

