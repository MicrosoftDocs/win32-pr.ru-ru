---
title: Функция ДдкЦижеткапабилитиесстринг
description: Возвращает строку, описывающую возможности монитора.
ms.assetid: 54041126-b710-4448-a9f0-9b644d6b8186
keywords:
- Настройка монитора функции ДдкЦижеткапабилитиесстринг
topic_type:
- apiref
api_name:
- DDCCIGetCapabilitiesString
api_location:
- gdi32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c9a49a6d7672ee505b4095afd3c6603c719679f5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105661897"
---
# <a name="ddccigetcapabilitiesstring-function"></a><span data-ttu-id="469ab-104">Функция ДдкЦижеткапабилитиесстринг</span><span class="sxs-lookup"><span data-stu-id="469ab-104">DDCCIGetCapabilitiesString function</span></span>

> [!IMPORTANT]
> <span data-ttu-id="469ab-105">Эта функция используется API конфигурации монитора для доступа к функциональным возможностям драйвера экрана.</span><span class="sxs-lookup"><span data-stu-id="469ab-105">This function is used by the monitor configuration API to access functionality in the display driver.</span></span> <span data-ttu-id="469ab-106">Приложения не должны вызывать эту функцию.</span><span class="sxs-lookup"><span data-stu-id="469ab-106">Applications should not call this function.</span></span>

 

<span data-ttu-id="469ab-107">Возвращает строку, описывающую возможности монитора.</span><span class="sxs-lookup"><span data-stu-id="469ab-107">Gets a string that describes the capabilities of a monitor.</span></span>

## <a name="syntax"></a><span data-ttu-id="469ab-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="469ab-108">Syntax</span></span>


```C++
NTSTATUS WINAPI DDCCIGetCapabilitiesString(
  _In_  HANDLE hMonitor,
  _Out_ LPSTR  pszString,
  _In_  DWORD  dwLength
);
```



## <a name="parameters"></a><span data-ttu-id="469ab-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="469ab-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="469ab-110">*хмонитор* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="469ab-110">*hMonitor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="469ab-111">Маркер физического монитора.</span><span class="sxs-lookup"><span data-stu-id="469ab-111">A handle to a physical monitor.</span></span>

</dd> <dt>

<span data-ttu-id="469ab-112">*псзстринг* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="469ab-112">*pszString* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="469ab-113">Указатель на буфер, который получает строку возможностей.</span><span class="sxs-lookup"><span data-stu-id="469ab-113">A pointer to a buffer that receives the capabilities string.</span></span> <span data-ttu-id="469ab-114">Чтобы получить длину строки возможностей, вызовите [**ддкЦижеткапабилитиесстрингленгс**](ddccigetcapabilitiesstringlength.md).</span><span class="sxs-lookup"><span data-stu-id="469ab-114">To get the length of the capabilities string, call [**DDCCIGetCapabilitiesStringLength**](ddccigetcapabilitiesstringlength.md).</span></span>

</dd> <dt>

<span data-ttu-id="469ab-115">*двленгс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="469ab-115">*dwLength* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="469ab-116">Размер буфера *псзстринг* в символах, включая завершающий символ null.</span><span class="sxs-lookup"><span data-stu-id="469ab-116">The size of the *pszString* buffer, in characters, including the terminating null character.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="469ab-117">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="469ab-117">Return value</span></span>

<span data-ttu-id="469ab-118">Если метод завершается успешно, возвращается **состояние \_ Success**.</span><span class="sxs-lookup"><span data-stu-id="469ab-118">If the method succeeds, it returns **STATUS\_SUCCESS**.</span></span> <span data-ttu-id="469ab-119">В противном случае возвращается код ошибки **NTSTATUS** .</span><span class="sxs-lookup"><span data-stu-id="469ab-119">Otherwise, it returns an **NTSTATUS** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="469ab-120">Комментарии</span><span class="sxs-lookup"><span data-stu-id="469ab-120">Remarks</span></span>

<span data-ttu-id="469ab-121">Приложения должны вызывать [**капабилитиесрекуестандкапабилитиесрепли**](/windows/desktop/api/LowLevelMonitorConfigurationAPI/nf-lowlevelmonitorconfigurationapi-capabilitiesrequestandcapabilitiesreply) вместо вызова этой функции.</span><span class="sxs-lookup"><span data-stu-id="469ab-121">Applications should call [**CapabilitiesRequestAndCapabilitiesReply**](/windows/desktop/api/LowLevelMonitorConfigurationAPI/nf-lowlevelmonitorconfigurationapi-capabilitiesrequestandcapabilitiesreply) instead of calling this function.</span></span>

<span data-ttu-id="469ab-122">Эта функция не имеет связанной библиотеки импорта.</span><span class="sxs-lookup"><span data-stu-id="469ab-122">This function has no associated import library.</span></span> <span data-ttu-id="469ab-123">Для вызова этой функции необходимо использовать функции [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) и [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) для динамической привязки к Gdi32.dll.</span><span class="sxs-lookup"><span data-stu-id="469ab-123">To call this function, you must use the [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) functions to dynamically link to Gdi32.dll.</span></span>

## <a name="requirements"></a><span data-ttu-id="469ab-124">Требования</span><span class="sxs-lookup"><span data-stu-id="469ab-124">Requirements</span></span>



| <span data-ttu-id="469ab-125">Требование</span><span class="sxs-lookup"><span data-stu-id="469ab-125">Requirement</span></span> | <span data-ttu-id="469ab-126">Значение</span><span class="sxs-lookup"><span data-stu-id="469ab-126">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="469ab-127">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="469ab-127">Minimum supported client</span></span><br/> | <span data-ttu-id="469ab-128">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="469ab-128">Windows Vista \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="469ab-129">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="469ab-129">Minimum supported server</span></span><br/> | <span data-ttu-id="469ab-130">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="469ab-130">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="469ab-131">DLL</span><span class="sxs-lookup"><span data-stu-id="469ab-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="469ab-132"><dt>Gdi32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="469ab-132"><dt>Gdi32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="469ab-133">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="469ab-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="469ab-134">Мониторинг функций конфигурации</span><span class="sxs-lookup"><span data-stu-id="469ab-134">Monitor Configuration Functions</span></span>](monitor-configuration-functions.md)
</dt> </dl>

 

