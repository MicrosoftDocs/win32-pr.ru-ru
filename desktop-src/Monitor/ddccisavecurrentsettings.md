---
title: Функция ДдкЦисавекуррентсеттингс
description: Сохраняет текущие параметры монитора в неизменяемое хранилище экрана.
ms.assetid: 293b61d4-36d8-43f4-8800-4dbac3ab11b0
keywords:
- Настройка монитора функции ДдкЦисавекуррентсеттингс
topic_type:
- apiref
api_name:
- DDCCISaveCurrentSettings
api_location:
- gdi32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2de590f63acc11ed49dfcdfab6505733da07b508
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988456"
---
# <a name="ddccisavecurrentsettings-function"></a><span data-ttu-id="840af-104">Функция ДдкЦисавекуррентсеттингс</span><span class="sxs-lookup"><span data-stu-id="840af-104">DDCCISaveCurrentSettings function</span></span>

> [!IMPORTANT]
> <span data-ttu-id="840af-105">Эта функция используется API конфигурации монитора для доступа к функциональным возможностям драйвера экрана.</span><span class="sxs-lookup"><span data-stu-id="840af-105">This function is used by the monitor configuration API to access functionality in the display driver.</span></span> <span data-ttu-id="840af-106">Приложения не должны вызывать эту функцию.</span><span class="sxs-lookup"><span data-stu-id="840af-106">Applications should not call this function.</span></span>

 

<span data-ttu-id="840af-107">Сохраняет текущие параметры монитора в неизменяемое хранилище экрана.</span><span class="sxs-lookup"><span data-stu-id="840af-107">Saves the current monitor settings to the display's nonvolatile storage.</span></span>

## <a name="syntax"></a><span data-ttu-id="840af-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="840af-108">Syntax</span></span>


```C++
NTSTATUS WINAPI DDCCISaveCurrentSettings(
   HANDLE hMonitor
);
```



## <a name="parameters"></a><span data-ttu-id="840af-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="840af-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="840af-110">*хмонитор*</span><span class="sxs-lookup"><span data-stu-id="840af-110">*hMonitor*</span></span> 
</dt> <dd>

<span data-ttu-id="840af-111">Маркер физического монитора.</span><span class="sxs-lookup"><span data-stu-id="840af-111">A handle to a physical monitor.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="840af-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="840af-112">Return value</span></span>

<span data-ttu-id="840af-113">Если метод завершается успешно, возвращается **состояние \_ Success**.</span><span class="sxs-lookup"><span data-stu-id="840af-113">If the method succeeds, it returns **STATUS\_SUCCESS**.</span></span> <span data-ttu-id="840af-114">В противном случае возвращается код ошибки **NTSTATUS** .</span><span class="sxs-lookup"><span data-stu-id="840af-114">Otherwise, it returns an **NTSTATUS** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="840af-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="840af-115">Remarks</span></span>

<span data-ttu-id="840af-116">Приложения должны вызывать [**савекуррентсеттингс**](/windows/desktop/api/LowLevelMonitorConfigurationAPI/nf-lowlevelmonitorconfigurationapi-savecurrentsettings) вместо вызова этой функции.</span><span class="sxs-lookup"><span data-stu-id="840af-116">Applications should call [**SaveCurrentSettings**](/windows/desktop/api/LowLevelMonitorConfigurationAPI/nf-lowlevelmonitorconfigurationapi-savecurrentsettings) instead of calling this function.</span></span>

<span data-ttu-id="840af-117">Эта функция не имеет связанной библиотеки импорта.</span><span class="sxs-lookup"><span data-stu-id="840af-117">This function has no associated import library.</span></span> <span data-ttu-id="840af-118">Для вызова этой функции необходимо использовать функции [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) и [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) для динамической привязки к Gdi32.dll.</span><span class="sxs-lookup"><span data-stu-id="840af-118">To call this function, you must use the [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) functions to dynamically link to Gdi32.dll.</span></span>

## <a name="requirements"></a><span data-ttu-id="840af-119">Требования</span><span class="sxs-lookup"><span data-stu-id="840af-119">Requirements</span></span>



| <span data-ttu-id="840af-120">Требование</span><span class="sxs-lookup"><span data-stu-id="840af-120">Requirement</span></span> | <span data-ttu-id="840af-121">Значение</span><span class="sxs-lookup"><span data-stu-id="840af-121">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="840af-122">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="840af-122">Minimum supported client</span></span><br/> | <span data-ttu-id="840af-123">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="840af-123">Windows Vista \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="840af-124">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="840af-124">Minimum supported server</span></span><br/> | <span data-ttu-id="840af-125">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="840af-125">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="840af-126">DLL</span><span class="sxs-lookup"><span data-stu-id="840af-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="840af-127"><dt>Gdi32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="840af-127"><dt>Gdi32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="840af-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="840af-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="840af-129">Мониторинг функций конфигурации</span><span class="sxs-lookup"><span data-stu-id="840af-129">Monitor Configuration Functions</span></span>](monitor-configuration-functions.md)
</dt> </dl>

 

