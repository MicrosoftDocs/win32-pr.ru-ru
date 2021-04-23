---
title: Функция Жетнумбероффисикалмониторс
description: Возвращает число мониторов фикал, связанных с устройством вывода.
ms.assetid: 498404e7-867d-4971-bea1-16e9f8fd9838
keywords:
- Настройка монитора функции Жетнумбероффисикалмониторс
topic_type:
- apiref
api_name:
- GetNumberOfPhysicalMonitors
api_location:
- gdi32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 09bec6abf296d807f80ab77cdc7ad8b4062fea9b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103891877"
---
# <a name="getnumberofphysicalmonitors-function"></a><span data-ttu-id="f1a79-104">Функция Жетнумбероффисикалмониторс</span><span class="sxs-lookup"><span data-stu-id="f1a79-104">GetNumberOfPhysicalMonitors function</span></span>

> [!IMPORTANT]
> <span data-ttu-id="f1a79-105">Эта функция используется API конфигурации монитора для доступа к функциональным возможностям драйвера экрана.</span><span class="sxs-lookup"><span data-stu-id="f1a79-105">This function is used by the monitor configuration API to access functionality in the display driver.</span></span> <span data-ttu-id="f1a79-106">Приложения не должны вызывать эту функцию.</span><span class="sxs-lookup"><span data-stu-id="f1a79-106">Applications should not call this function.</span></span>

 

<span data-ttu-id="f1a79-107">Возвращает число мониторов фикал, связанных с устройством вывода.</span><span class="sxs-lookup"><span data-stu-id="f1a79-107">Gets the number of phyical monitors associated with a display device.</span></span>

## <a name="syntax"></a><span data-ttu-id="f1a79-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f1a79-108">Syntax</span></span>


```C++
NTSTATUS WINAPI GetNumberOfPhysicalMonitors(
  _In_  UNICODE_STRING *pstrDeviceName,
  _Out_ LPDWORD        pdwNumberOfPhysicalMonitors
);
```



## <a name="parameters"></a><span data-ttu-id="f1a79-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="f1a79-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f1a79-110">*пстрдевиценаме* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="f1a79-110">*pstrDeviceName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f1a79-111">Указатель на [**\_ строковую структуру Юникода**](/windows/desktop/api/subauth/ns-subauth-unicode_string) , содержащую имя устройства вывода, которое возвращается функцией [**жетмониторинфо**](/windows/desktop/api/winuser/nf-winuser-getmonitorinfoa) .</span><span class="sxs-lookup"><span data-stu-id="f1a79-111">A pointer to a [**UNICODE\_STRING**](/windows/desktop/api/subauth/ns-subauth-unicode_string) structure that contains the name of the display device, as returned by the [**GetMonitorInfo**](/windows/desktop/api/winuser/nf-winuser-getmonitorinfoa) function.</span></span>

</dd> <dt>

<span data-ttu-id="f1a79-112">*пдвнумбероффисикалмониторс* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="f1a79-112">*pdwNumberOfPhysicalMonitors* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f1a79-113">Получает число физических мониторов.</span><span class="sxs-lookup"><span data-stu-id="f1a79-113">Receives the number of physical monitors.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f1a79-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="f1a79-114">Return value</span></span>

<span data-ttu-id="f1a79-115">Если метод завершается успешно, возвращается **состояние \_ Success**.</span><span class="sxs-lookup"><span data-stu-id="f1a79-115">If the method succeeds, it returns **STATUS\_SUCCESS**.</span></span> <span data-ttu-id="f1a79-116">В противном случае возвращается код ошибки **NTSTATUS** .</span><span class="sxs-lookup"><span data-stu-id="f1a79-116">Otherwise, it returns an **NTSTATUS** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="f1a79-117">Комментарии</span><span class="sxs-lookup"><span data-stu-id="f1a79-117">Remarks</span></span>

<span data-ttu-id="f1a79-118">Вместо использования этой функции приложения должны вызывать одну из следующих функций:</span><span class="sxs-lookup"><span data-stu-id="f1a79-118">Instead of using this function, applications should call one of the following functions:</span></span>

-   [<span data-ttu-id="f1a79-119">**жетнумбероффисикалмониторсфромхмонитор**</span><span class="sxs-lookup"><span data-stu-id="f1a79-119">**GetNumberOfPhysicalMonitorsFromHMONITOR**</span></span>](/windows/desktop/api/PhysicalMonitorEnumerationAPI/nf-physicalmonitorenumerationapi-getnumberofphysicalmonitorsfromhmonitor)
-   [<span data-ttu-id="f1a79-120">**GetNumberOfPhysicalMonitorsFromIDirect3DDevice9**</span><span class="sxs-lookup"><span data-stu-id="f1a79-120">**GetNumberOfPhysicalMonitorsFromIDirect3DDevice9**</span></span>](/windows/desktop/api/PhysicalMonitorEnumerationAPI/nf-physicalmonitorenumerationapi-getnumberofphysicalmonitorsfromidirect3ddevice9)

<span data-ttu-id="f1a79-121">Эта функция не имеет связанной библиотеки импорта.</span><span class="sxs-lookup"><span data-stu-id="f1a79-121">This function has no associated import library.</span></span> <span data-ttu-id="f1a79-122">Для вызова этой функции необходимо использовать функции [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) и [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) для динамической привязки к Gdi32.dll.</span><span class="sxs-lookup"><span data-stu-id="f1a79-122">To call this function, you must use the [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) functions to dynamically link to Gdi32.dll.</span></span>

## <a name="requirements"></a><span data-ttu-id="f1a79-123">Требования</span><span class="sxs-lookup"><span data-stu-id="f1a79-123">Requirements</span></span>



| <span data-ttu-id="f1a79-124">Требование</span><span class="sxs-lookup"><span data-stu-id="f1a79-124">Requirement</span></span> | <span data-ttu-id="f1a79-125">Значение</span><span class="sxs-lookup"><span data-stu-id="f1a79-125">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="f1a79-126">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="f1a79-126">Minimum supported client</span></span><br/> | <span data-ttu-id="f1a79-127">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="f1a79-127">Windows Vista \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="f1a79-128">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="f1a79-128">Minimum supported server</span></span><br/> | <span data-ttu-id="f1a79-129">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="f1a79-129">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="f1a79-130">DLL</span><span class="sxs-lookup"><span data-stu-id="f1a79-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f1a79-131"><dt>Gdi32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f1a79-131"><dt>Gdi32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f1a79-132">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f1a79-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f1a79-133">Мониторинг функций конфигурации</span><span class="sxs-lookup"><span data-stu-id="f1a79-133">Monitor Configuration Functions</span></span>](monitor-configuration-functions.md)
</dt> </dl>

 

