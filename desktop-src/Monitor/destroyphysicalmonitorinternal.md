---
title: Функция Дестройфисикалмониторинтернал
description: Закрывает маркер физического монитора.
ms.assetid: 86705f1b-6445-444c-8e04-66a435927af3
keywords:
- Настройка монитора функции Дестройфисикалмониторинтернал
topic_type:
- apiref
api_name:
- DestroyPhysicalMonitorInternal
api_location:
- gdi32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7b8ea52645e97bc5bec49fba053f9dbab5306bcb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103891878"
---
# <a name="destroyphysicalmonitorinternal-function"></a><span data-ttu-id="efe38-104">Функция Дестройфисикалмониторинтернал</span><span class="sxs-lookup"><span data-stu-id="efe38-104">DestroyPhysicalMonitorInternal function</span></span>

> [!IMPORTANT]
> <span data-ttu-id="efe38-105">Эта функция используется API конфигурации монитора для доступа к функциональным возможностям драйвера экрана.</span><span class="sxs-lookup"><span data-stu-id="efe38-105">This function is used by the monitor configuration API to access functionality in the display driver.</span></span> <span data-ttu-id="efe38-106">Приложения не должны вызывать эту функцию.</span><span class="sxs-lookup"><span data-stu-id="efe38-106">Applications should not call this function.</span></span>

 

<span data-ttu-id="efe38-107">Закрывает маркер физического монитора.</span><span class="sxs-lookup"><span data-stu-id="efe38-107">Closes a handle to a physical monitor.</span></span>

## <a name="syntax"></a><span data-ttu-id="efe38-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="efe38-108">Syntax</span></span>


```C++
NTSTATUS WINAPI DestroyPhysicalMonitorInternal(
  _In_ HANDLE hMonitor
);
```



## <a name="parameters"></a><span data-ttu-id="efe38-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="efe38-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="efe38-110">*хмонитор* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="efe38-110">*hMonitor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="efe38-111">Маркер физического монитора.</span><span class="sxs-lookup"><span data-stu-id="efe38-111">A handle to a physical monitor.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="efe38-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="efe38-112">Return value</span></span>

<span data-ttu-id="efe38-113">Если метод завершается успешно, возвращается **состояние \_ Success**.</span><span class="sxs-lookup"><span data-stu-id="efe38-113">If the method succeeds, it returns **STATUS\_SUCCESS**.</span></span> <span data-ttu-id="efe38-114">В противном случае возвращается код ошибки **NTSTATUS** .</span><span class="sxs-lookup"><span data-stu-id="efe38-114">Otherwise, it returns an **NTSTATUS** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="efe38-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="efe38-115">Remarks</span></span>

<span data-ttu-id="efe38-116">Приложения должны вызывать [**дестройфисикалмонитор**](/windows/desktop/api/PhysicalMonitorEnumerationAPI/nf-physicalmonitorenumerationapi-destroyphysicalmonitor) вместо вызова этой функции.</span><span class="sxs-lookup"><span data-stu-id="efe38-116">Applications should call [**DestroyPhysicalMonitor**](/windows/desktop/api/PhysicalMonitorEnumerationAPI/nf-physicalmonitorenumerationapi-destroyphysicalmonitor) instead of calling this function.</span></span>

<span data-ttu-id="efe38-117">Эта функция не имеет связанной библиотеки импорта.</span><span class="sxs-lookup"><span data-stu-id="efe38-117">This function has no associated import library.</span></span> <span data-ttu-id="efe38-118">Для вызова этой функции необходимо использовать функции [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) и [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) для динамической привязки к Gdi32.dll.</span><span class="sxs-lookup"><span data-stu-id="efe38-118">To call this function, you must use the [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) functions to dynamically link to Gdi32.dll.</span></span>

## <a name="requirements"></a><span data-ttu-id="efe38-119">Требования</span><span class="sxs-lookup"><span data-stu-id="efe38-119">Requirements</span></span>



| <span data-ttu-id="efe38-120">Требование</span><span class="sxs-lookup"><span data-stu-id="efe38-120">Requirement</span></span> | <span data-ttu-id="efe38-121">Значение</span><span class="sxs-lookup"><span data-stu-id="efe38-121">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="efe38-122">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="efe38-122">Minimum supported client</span></span><br/> | <span data-ttu-id="efe38-123">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="efe38-123">Windows Vista \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="efe38-124">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="efe38-124">Minimum supported server</span></span><br/> | <span data-ttu-id="efe38-125">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="efe38-125">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="efe38-126">DLL</span><span class="sxs-lookup"><span data-stu-id="efe38-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="efe38-127"><dt>Gdi32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="efe38-127"><dt>Gdi32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="efe38-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="efe38-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="efe38-129">Мониторинг функций конфигурации</span><span class="sxs-lookup"><span data-stu-id="efe38-129">Monitor Configuration Functions</span></span>](monitor-configuration-functions.md)
</dt> </dl>

 

