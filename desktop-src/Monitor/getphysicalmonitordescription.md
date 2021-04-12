---
title: Функция Жетфисикалмонитордескриптион
description: Возвращает описание физического монитора.
ms.assetid: 81789eaf-7831-4833-87e1-7f318f831c96
keywords:
- Настройка монитора функции Жетфисикалмонитордескриптион
topic_type:
- apiref
api_name:
- GetPhysicalMonitorDescription
api_location:
- gdi32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 259ced1185e229fccd426adfbf94fa47af22b170
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104135834"
---
# <a name="getphysicalmonitordescription-function"></a><span data-ttu-id="09f9c-104">Функция Жетфисикалмонитордескриптион</span><span class="sxs-lookup"><span data-stu-id="09f9c-104">GetPhysicalMonitorDescription function</span></span>

> [!IMPORTANT]
> <span data-ttu-id="09f9c-105">Эта функция используется API конфигурации монитора для доступа к функциональным возможностям драйвера экрана.</span><span class="sxs-lookup"><span data-stu-id="09f9c-105">This function is used by the monitor configuration API to access functionality in the display driver.</span></span> <span data-ttu-id="09f9c-106">Приложения не должны вызывать эту функцию.</span><span class="sxs-lookup"><span data-stu-id="09f9c-106">Applications should not call this function.</span></span>

 

<span data-ttu-id="09f9c-107">Возвращает описание физического монитора.</span><span class="sxs-lookup"><span data-stu-id="09f9c-107">Gets a description of a physical monitor.</span></span>

## <a name="syntax"></a><span data-ttu-id="09f9c-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="09f9c-108">Syntax</span></span>


```C++
NTSTATUS WINAPI GetPhysicalMonitorDescription(
  _In_  HANDLE hMonitor,
  _In_  DWORD  dwPhysicalMonitorDescriptionSizeInChars,
  _Out_ LPWSTR szPhysicalMonitorDescription
);
```



## <a name="parameters"></a><span data-ttu-id="09f9c-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="09f9c-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="09f9c-110">*хмонитор* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="09f9c-110">*hMonitor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="09f9c-111">Маркер физического монитора.</span><span class="sxs-lookup"><span data-stu-id="09f9c-111">A handle to a physical monitor.</span></span>

</dd> <dt>

<span data-ttu-id="09f9c-112">*двфисикалмонитордескриптионсизеинчарс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="09f9c-112">*dwPhysicalMonitorDescriptionSizeInChars* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="09f9c-113">Число символов в массиве *сзфисикалмонитордескриптион* .</span><span class="sxs-lookup"><span data-stu-id="09f9c-113">The number of characters in the *szPhysicalMonitorDescription* array.</span></span>

</dd> <dt>

<span data-ttu-id="09f9c-114">*сзфисикалмонитордескриптион* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="09f9c-114">*szPhysicalMonitorDescription* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="09f9c-115">Указатель на массив, который получает описание.</span><span class="sxs-lookup"><span data-stu-id="09f9c-115">A pointer to an array that receives the description.</span></span> <span data-ttu-id="09f9c-116">Число элементов в массиве должно быть не меньше, чем **\_ \_ \_ размер описания физического монитора**.</span><span class="sxs-lookup"><span data-stu-id="09f9c-116">The number of elements in the array should be at least **PHYSICAL\_MONITOR\_DESCRIPTION\_SIZE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="09f9c-117">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="09f9c-117">Return value</span></span>

<span data-ttu-id="09f9c-118">Если метод завершается успешно, возвращается **состояние \_ Success**.</span><span class="sxs-lookup"><span data-stu-id="09f9c-118">If the method succeeds, it returns **STATUS\_SUCCESS**.</span></span> <span data-ttu-id="09f9c-119">В противном случае возвращается код ошибки **NTSTATUS** .</span><span class="sxs-lookup"><span data-stu-id="09f9c-119">Otherwise, it returns an **NTSTATUS** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="09f9c-120">Комментарии</span><span class="sxs-lookup"><span data-stu-id="09f9c-120">Remarks</span></span>

<span data-ttu-id="09f9c-121">Вместо использования этой функции приложения должны вызывать одну из следующих функций:</span><span class="sxs-lookup"><span data-stu-id="09f9c-121">Instead of using this function, applications should call one of the following functions:</span></span>

-   [<span data-ttu-id="09f9c-122">**жетфисикалмониторсфромхмонитор**</span><span class="sxs-lookup"><span data-stu-id="09f9c-122">**GetPhysicalMonitorsFromHMONITOR**</span></span>](/windows/desktop/api/PhysicalMonitorEnumerationAPI/nf-physicalmonitorenumerationapi-getphysicalmonitorsfromhmonitor)
-   [<span data-ttu-id="09f9c-123">**GetPhysicalMonitorsFromIDirect3DDevice9**</span><span class="sxs-lookup"><span data-stu-id="09f9c-123">**GetPhysicalMonitorsFromIDirect3DDevice9**</span></span>](/windows/desktop/api/PhysicalMonitorEnumerationAPI/nf-physicalmonitorenumerationapi-getphysicalmonitorsfromidirect3ddevice9)

<span data-ttu-id="09f9c-124">Эта функция не имеет связанной библиотеки импорта.</span><span class="sxs-lookup"><span data-stu-id="09f9c-124">This function has no associated import library.</span></span> <span data-ttu-id="09f9c-125">Для вызова этой функции необходимо использовать функции [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) и [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) для динамической привязки к Gdi32.dll.</span><span class="sxs-lookup"><span data-stu-id="09f9c-125">To call this function, you must use the [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) functions to dynamically link to Gdi32.dll.</span></span>

## <a name="requirements"></a><span data-ttu-id="09f9c-126">Требования</span><span class="sxs-lookup"><span data-stu-id="09f9c-126">Requirements</span></span>



| <span data-ttu-id="09f9c-127">Требование</span><span class="sxs-lookup"><span data-stu-id="09f9c-127">Requirement</span></span> | <span data-ttu-id="09f9c-128">Значение</span><span class="sxs-lookup"><span data-stu-id="09f9c-128">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="09f9c-129">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="09f9c-129">Minimum supported client</span></span><br/> | <span data-ttu-id="09f9c-130">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="09f9c-130">Windows Vista \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="09f9c-131">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="09f9c-131">Minimum supported server</span></span><br/> | <span data-ttu-id="09f9c-132">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="09f9c-132">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="09f9c-133">DLL</span><span class="sxs-lookup"><span data-stu-id="09f9c-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="09f9c-134"><dt>Gdi32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="09f9c-134"><dt>Gdi32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="09f9c-135">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="09f9c-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="09f9c-136">Мониторинг функций конфигурации</span><span class="sxs-lookup"><span data-stu-id="09f9c-136">Monitor Configuration Functions</span></span>](monitor-configuration-functions.md)
</dt> </dl>

 

