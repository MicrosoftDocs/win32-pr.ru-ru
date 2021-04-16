---
title: Функция ДдкЦижеткапабилитиесстрингленгс
description: Возвращает длину строки возможностей для монитора.
ms.assetid: 8a26d17b-1535-49c7-8cfb-48feb283a3c4
keywords:
- Настройка монитора функции ДдкЦижеткапабилитиесстрингленгс
topic_type:
- apiref
api_name:
- DDCCIGetCapabilitiesStringLength
api_location:
- gdi32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 28d82e2f0667d542c8fa4c9255fde765e4cea81d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105650368"
---
# <a name="ddccigetcapabilitiesstringlength-function"></a><span data-ttu-id="0ba4e-104">Функция ДдкЦижеткапабилитиесстрингленгс</span><span class="sxs-lookup"><span data-stu-id="0ba4e-104">DDCCIGetCapabilitiesStringLength function</span></span>

> [!IMPORTANT]
> <span data-ttu-id="0ba4e-105">Эта функция используется API конфигурации монитора для доступа к функциональным возможностям драйвера экрана.</span><span class="sxs-lookup"><span data-stu-id="0ba4e-105">This function is used by the monitor configuration API to access functionality in the display driver.</span></span> <span data-ttu-id="0ba4e-106">Приложения не должны вызывать эту функцию.</span><span class="sxs-lookup"><span data-stu-id="0ba4e-106">Applications should not call this function.</span></span>

 

<span data-ttu-id="0ba4e-107">Возвращает длину строки возможностей для монитора.</span><span class="sxs-lookup"><span data-stu-id="0ba4e-107">Gets the length of a capabilities string for a monitor.</span></span>

## <a name="syntax"></a><span data-ttu-id="0ba4e-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="0ba4e-108">Syntax</span></span>


```C++
NTSTATUS WINAPI DDCCIGetCapabilitiesStringLength(
  _In_  HANDLE hMonitor,
  _Out_ DWORD  *pdwLength
);
```



## <a name="parameters"></a><span data-ttu-id="0ba4e-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="0ba4e-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0ba4e-110">*хмонитор* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="0ba4e-110">*hMonitor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0ba4e-111">Маркер физического монитора.</span><span class="sxs-lookup"><span data-stu-id="0ba4e-111">A handle to a physical monitor.</span></span>

</dd> <dt>

<span data-ttu-id="0ba4e-112">*пдвленгс* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="0ba4e-112">*pdwLength* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0ba4e-113">Получает длину строки возможностей в символах, включая завершающий символ null.</span><span class="sxs-lookup"><span data-stu-id="0ba4e-113">Receives the length of the capabilities string, in characters, including the terminating null character.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0ba4e-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="0ba4e-114">Return value</span></span>

<span data-ttu-id="0ba4e-115">Если метод завершается успешно, возвращается **состояние \_ Success**.</span><span class="sxs-lookup"><span data-stu-id="0ba4e-115">If the method succeeds, it returns **STATUS\_SUCCESS**.</span></span> <span data-ttu-id="0ba4e-116">В противном случае возвращается код ошибки **NTSTATUS** .</span><span class="sxs-lookup"><span data-stu-id="0ba4e-116">Otherwise, it returns an **NTSTATUS** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="0ba4e-117">Комментарии</span><span class="sxs-lookup"><span data-stu-id="0ba4e-117">Remarks</span></span>

<span data-ttu-id="0ba4e-118">Приложения должны вызывать [**жеткапабилитиесстрингленгс**](/windows/desktop/api/LowLevelMonitorConfigurationAPI/nf-lowlevelmonitorconfigurationapi-getcapabilitiesstringlength) вместо вызова этой функции.</span><span class="sxs-lookup"><span data-stu-id="0ba4e-118">Applications should call [**GetCapabilitiesStringLength**](/windows/desktop/api/LowLevelMonitorConfigurationAPI/nf-lowlevelmonitorconfigurationapi-getcapabilitiesstringlength) instead of calling this function.</span></span>

<span data-ttu-id="0ba4e-119">Эта функция не имеет связанной библиотеки импорта.</span><span class="sxs-lookup"><span data-stu-id="0ba4e-119">This function has no associated import library.</span></span> <span data-ttu-id="0ba4e-120">Для вызова этой функции необходимо использовать функции [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) и [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) для динамической привязки к Gdi32.dll.</span><span class="sxs-lookup"><span data-stu-id="0ba4e-120">To call this function, you must use the [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) functions to dynamically link to Gdi32.dll.</span></span>

## <a name="requirements"></a><span data-ttu-id="0ba4e-121">Требования</span><span class="sxs-lookup"><span data-stu-id="0ba4e-121">Requirements</span></span>



| <span data-ttu-id="0ba4e-122">Требование</span><span class="sxs-lookup"><span data-stu-id="0ba4e-122">Requirement</span></span> | <span data-ttu-id="0ba4e-123">Значение</span><span class="sxs-lookup"><span data-stu-id="0ba4e-123">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="0ba4e-124">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="0ba4e-124">Minimum supported client</span></span><br/> | <span data-ttu-id="0ba4e-125">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="0ba4e-125">Windows Vista \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="0ba4e-126">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="0ba4e-126">Minimum supported server</span></span><br/> | <span data-ttu-id="0ba4e-127">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="0ba4e-127">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="0ba4e-128">DLL</span><span class="sxs-lookup"><span data-stu-id="0ba4e-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0ba4e-129"><dt>Gdi32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0ba4e-129"><dt>Gdi32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0ba4e-130">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="0ba4e-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0ba4e-131">Мониторинг функций конфигурации</span><span class="sxs-lookup"><span data-stu-id="0ba4e-131">Monitor Configuration Functions</span></span>](monitor-configuration-functions.md)
</dt> </dl>

 

