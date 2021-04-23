---
title: Функция ДдкЦижеттимингрепорт
description: Возвращает частоту синхронизации по горизонтали и вертикали монитора.
ms.assetid: d490cb89-082a-42a1-ac0a-335c929cd5d7
keywords:
- Настройка монитора функции ДдкЦижеттимингрепорт
topic_type:
- apiref
api_name:
- DDCCIGetTimingReport
api_location:
- gdi32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1b87cb4269c2cdff2303bbe763905cb572acfbb7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988628"
---
# <a name="ddccigettimingreport-function"></a><span data-ttu-id="e5e4b-104">Функция ДдкЦижеттимингрепорт</span><span class="sxs-lookup"><span data-stu-id="e5e4b-104">DDCCIGetTimingReport function</span></span>

> [!IMPORTANT]
> <span data-ttu-id="e5e4b-105">Эта функция используется API конфигурации монитора для доступа к функциональным возможностям драйвера экрана.</span><span class="sxs-lookup"><span data-stu-id="e5e4b-105">This function is used by the monitor configuration API to access functionality in the display driver.</span></span> <span data-ttu-id="e5e4b-106">Приложения не должны вызывать эту функцию.</span><span class="sxs-lookup"><span data-stu-id="e5e4b-106">Applications should not call this function.</span></span>

 

<span data-ttu-id="e5e4b-107">Возвращает частоту синхронизации по горизонтали и вертикали монитора.</span><span class="sxs-lookup"><span data-stu-id="e5e4b-107">Gets the horizontal and vertical synchronization frequencies of a monitor.</span></span>

## <a name="syntax"></a><span data-ttu-id="e5e4b-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e5e4b-108">Syntax</span></span>


```C++
NTSTATUS WINAPI DDCCIGetTimingReport(
  _In_  HANDLE             hMonitor,
  _Out_ LPMC_TIMING_REPORT pmtr
);
```



## <a name="parameters"></a><span data-ttu-id="e5e4b-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="e5e4b-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e5e4b-110">*хмонитор* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="e5e4b-110">*hMonitor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e5e4b-111">Маркер физического монитора.</span><span class="sxs-lookup"><span data-stu-id="e5e4b-111">A handle to a physical monitor.</span></span>

</dd> <dt>

<span data-ttu-id="e5e4b-112">*ПМТР* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="e5e4b-112">*pmtr* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e5e4b-113">Указатель на структуру [**\_ \_ отчета о времени MC**](/windows/desktop/api/LowLevelMonitorConfigurationAPI/ns-lowlevelmonitorconfigurationapi-mc_timing_report) , которая получает сведения о времени.</span><span class="sxs-lookup"><span data-stu-id="e5e4b-113">A pointer to an [**MC\_TIMING\_REPORT**](/windows/desktop/api/LowLevelMonitorConfigurationAPI/ns-lowlevelmonitorconfigurationapi-mc_timing_report) structure that receives the timing information.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e5e4b-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="e5e4b-114">Return value</span></span>

<span data-ttu-id="e5e4b-115">Если метод завершается успешно, возвращается **состояние \_ Success**.</span><span class="sxs-lookup"><span data-stu-id="e5e4b-115">If the method succeeds, it returns **STATUS\_SUCCESS**.</span></span> <span data-ttu-id="e5e4b-116">В противном случае возвращается код ошибки **NTSTATUS** .</span><span class="sxs-lookup"><span data-stu-id="e5e4b-116">Otherwise, it returns an **NTSTATUS** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="e5e4b-117">Комментарии</span><span class="sxs-lookup"><span data-stu-id="e5e4b-117">Remarks</span></span>

<span data-ttu-id="e5e4b-118">Приложения должны вызывать [**жеттимингрепорт**](/windows/desktop/api/LowLevelMonitorConfigurationAPI/nf-lowlevelmonitorconfigurationapi-gettimingreport) вместо вызова этой функции.</span><span class="sxs-lookup"><span data-stu-id="e5e4b-118">Applications should call [**GetTimingReport**](/windows/desktop/api/LowLevelMonitorConfigurationAPI/nf-lowlevelmonitorconfigurationapi-gettimingreport) instead of calling this function.</span></span>

<span data-ttu-id="e5e4b-119">Эта функция не имеет связанной библиотеки импорта.</span><span class="sxs-lookup"><span data-stu-id="e5e4b-119">This function has no associated import library.</span></span> <span data-ttu-id="e5e4b-120">Для вызова этой функции необходимо использовать функции [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) и [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) для динамической привязки к Gdi32.dll.</span><span class="sxs-lookup"><span data-stu-id="e5e4b-120">To call this function, you must use the [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) functions to dynamically link to Gdi32.dll.</span></span>

## <a name="requirements"></a><span data-ttu-id="e5e4b-121">Требования</span><span class="sxs-lookup"><span data-stu-id="e5e4b-121">Requirements</span></span>



| <span data-ttu-id="e5e4b-122">Требование</span><span class="sxs-lookup"><span data-stu-id="e5e4b-122">Requirement</span></span> | <span data-ttu-id="e5e4b-123">Значение</span><span class="sxs-lookup"><span data-stu-id="e5e4b-123">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="e5e4b-124">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="e5e4b-124">Minimum supported client</span></span><br/> | <span data-ttu-id="e5e4b-125">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="e5e4b-125">Windows Vista \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="e5e4b-126">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="e5e4b-126">Minimum supported server</span></span><br/> | <span data-ttu-id="e5e4b-127">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="e5e4b-127">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="e5e4b-128">DLL</span><span class="sxs-lookup"><span data-stu-id="e5e4b-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e5e4b-129"><dt>Gdi32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e5e4b-129"><dt>Gdi32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e5e4b-130">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e5e4b-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e5e4b-131">Мониторинг функций конфигурации</span><span class="sxs-lookup"><span data-stu-id="e5e4b-131">Monitor Configuration Functions</span></span>](monitor-configuration-functions.md)
</dt> </dl>

 

