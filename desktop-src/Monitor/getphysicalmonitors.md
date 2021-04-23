---
title: Функция Жетфисикалмониторс
description: Возвращает физические мониторы, связанные с устройством вывода.
ms.assetid: 8bbbad0a-2e45-439c-9312-f922a920c7fd
keywords:
- Настройка монитора функции Жетфисикалмониторс
topic_type:
- apiref
api_name:
- GetPhysicalMonitors
api_location:
- gdi32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d95ccb801dbf06e096534754bd0adffbe36b5084
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105661895"
---
# <a name="getphysicalmonitors-function"></a><span data-ttu-id="17b7c-104">Функция Жетфисикалмониторс</span><span class="sxs-lookup"><span data-stu-id="17b7c-104">GetPhysicalMonitors function</span></span>

> [!IMPORTANT]
> <span data-ttu-id="17b7c-105">Эта функция используется API конфигурации монитора для доступа к функциональным возможностям драйвера экрана.</span><span class="sxs-lookup"><span data-stu-id="17b7c-105">This function is used by the monitor configuration API to access functionality in the display driver.</span></span> <span data-ttu-id="17b7c-106">Приложения не должны вызывать эту функцию.</span><span class="sxs-lookup"><span data-stu-id="17b7c-106">Applications should not call this function.</span></span>

 

<span data-ttu-id="17b7c-107">Возвращает физические мониторы, связанные с устройством вывода.</span><span class="sxs-lookup"><span data-stu-id="17b7c-107">Gets the physical monitors associated with a display device.</span></span>

## <a name="syntax"></a><span data-ttu-id="17b7c-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="17b7c-108">Syntax</span></span>


```C++
NTSTATUS WINAPI GetPhysicalMonitors(
  _In_  UNICODE_STRING *pstrDeviceName,
  _In_  DWORD          dwPhysicalMonitorArraySize,
  _Out_ DWORD          *pdwNumPhysicalMonitorHandlesInArray,
  _Out_ HANDLE         *phPhysicalMonitorArray
);
```



## <a name="parameters"></a><span data-ttu-id="17b7c-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="17b7c-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="17b7c-110">*пстрдевиценаме* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="17b7c-110">*pstrDeviceName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="17b7c-111">Указатель на [**\_ строковую структуру Юникода**](/windows/desktop/api/subauth/ns-subauth-unicode_string) , содержащую имя устройства вывода, которое возвращается функцией [**жетмониторинфо**](/windows/desktop/api/winuser/nf-winuser-getmonitorinfoa) .</span><span class="sxs-lookup"><span data-stu-id="17b7c-111">A pointer to a [**UNICODE\_STRING**](/windows/desktop/api/subauth/ns-subauth-unicode_string) structure that contains the name of the display device, as returned by the [**GetMonitorInfo**](/windows/desktop/api/winuser/nf-winuser-getmonitorinfoa) function.</span></span>

</dd> <dt>

<span data-ttu-id="17b7c-112">*двфисикалмонитораррайсизе* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="17b7c-112">*dwPhysicalMonitorArraySize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="17b7c-113">Число элементов в массиве *пдвнумфисикалмониторхандлесинаррай* .</span><span class="sxs-lookup"><span data-stu-id="17b7c-113">The number of elements in the *pdwNumPhysicalMonitorHandlesInArray* array.</span></span> <span data-ttu-id="17b7c-114">Чтобы получить требуемый размер массива, вызовите [**жетнумбероффисикалмониторс**](getnumberofphysicalmonitors.md).</span><span class="sxs-lookup"><span data-stu-id="17b7c-114">To get the required size of the array, call [**GetNumberOfPhysicalMonitors**](getnumberofphysicalmonitors.md).</span></span>

</dd> <dt>

<span data-ttu-id="17b7c-115">*пдвнумфисикалмониторхандлесинаррай* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="17b7c-115">*pdwNumPhysicalMonitorHandlesInArray* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="17b7c-116">Получает число элементов, которые функция копирует в массив *ффисикалмонитораррай* .</span><span class="sxs-lookup"><span data-stu-id="17b7c-116">Receives the number of items that the function copies to the *phPhysicalMonitorArray* array.</span></span>

</dd> <dt>

<span data-ttu-id="17b7c-117">*ффисикалмонитораррай* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="17b7c-117">*phPhysicalMonitorArray* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="17b7c-118">Массив, который получает дескрипторы физических мониторов.</span><span class="sxs-lookup"><span data-stu-id="17b7c-118">An array that receives handles to the physical monitors.</span></span> <span data-ttu-id="17b7c-119">Каждый обработчик должен быть освобожден путем вызова [**дестройфисикалмонитор**](/windows/desktop/api/PhysicalMonitorEnumerationAPI/nf-physicalmonitorenumerationapi-destroyphysicalmonitor).</span><span class="sxs-lookup"><span data-stu-id="17b7c-119">Each handle must be released by calling [**DestroyPhysicalMonitor**](/windows/desktop/api/PhysicalMonitorEnumerationAPI/nf-physicalmonitorenumerationapi-destroyphysicalmonitor).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="17b7c-120">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="17b7c-120">Return value</span></span>

<span data-ttu-id="17b7c-121">Если метод завершается успешно, возвращается **состояние \_ Success**.</span><span class="sxs-lookup"><span data-stu-id="17b7c-121">If the method succeeds, it returns **STATUS\_SUCCESS**.</span></span> <span data-ttu-id="17b7c-122">В противном случае возвращается код ошибки **NTSTATUS** .</span><span class="sxs-lookup"><span data-stu-id="17b7c-122">Otherwise, it returns an **NTSTATUS** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="17b7c-123">Комментарии</span><span class="sxs-lookup"><span data-stu-id="17b7c-123">Remarks</span></span>

<span data-ttu-id="17b7c-124">Вместо использования этой функции приложения должны вызывать одну из следующих функций:</span><span class="sxs-lookup"><span data-stu-id="17b7c-124">Instead of using this function, applications should call one of the following functions:</span></span>

-   [<span data-ttu-id="17b7c-125">**жетфисикалмониторсфромхмонитор**</span><span class="sxs-lookup"><span data-stu-id="17b7c-125">**GetPhysicalMonitorsFromHMONITOR**</span></span>](/windows/desktop/api/PhysicalMonitorEnumerationAPI/nf-physicalmonitorenumerationapi-getphysicalmonitorsfromhmonitor)
-   [<span data-ttu-id="17b7c-126">**GetPhysicalMonitorsFromIDirect3DDevice9**</span><span class="sxs-lookup"><span data-stu-id="17b7c-126">**GetPhysicalMonitorsFromIDirect3DDevice9**</span></span>](/windows/desktop/api/PhysicalMonitorEnumerationAPI/nf-physicalmonitorenumerationapi-getphysicalmonitorsfromidirect3ddevice9)

<span data-ttu-id="17b7c-127">Эта функция не имеет связанной библиотеки импорта.</span><span class="sxs-lookup"><span data-stu-id="17b7c-127">This function has no associated import library.</span></span> <span data-ttu-id="17b7c-128">Для вызова этой функции необходимо использовать функции [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) и [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) для динамической привязки к Gdi32.dll.</span><span class="sxs-lookup"><span data-stu-id="17b7c-128">To call this function, you must use the [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) functions to dynamically link to Gdi32.dll.</span></span>

## <a name="requirements"></a><span data-ttu-id="17b7c-129">Требования</span><span class="sxs-lookup"><span data-stu-id="17b7c-129">Requirements</span></span>



| <span data-ttu-id="17b7c-130">Требование</span><span class="sxs-lookup"><span data-stu-id="17b7c-130">Requirement</span></span> | <span data-ttu-id="17b7c-131">Значение</span><span class="sxs-lookup"><span data-stu-id="17b7c-131">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="17b7c-132">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="17b7c-132">Minimum supported client</span></span><br/> | <span data-ttu-id="17b7c-133">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="17b7c-133">Windows Vista \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="17b7c-134">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="17b7c-134">Minimum supported server</span></span><br/> | <span data-ttu-id="17b7c-135">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="17b7c-135">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="17b7c-136">DLL</span><span class="sxs-lookup"><span data-stu-id="17b7c-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="17b7c-137"><dt>Gdi32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="17b7c-137"><dt>Gdi32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="17b7c-138">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="17b7c-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="17b7c-139">Мониторинг функций конфигурации</span><span class="sxs-lookup"><span data-stu-id="17b7c-139">Monitor Configuration Functions</span></span>](monitor-configuration-functions.md)
</dt> </dl>

 

