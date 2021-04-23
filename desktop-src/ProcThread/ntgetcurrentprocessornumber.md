---
description: Возвращает номер процессора, на котором выполнялся текущий поток во время вызова этой функции.
ms.assetid: f0141550-58e2-421a-934d-9a6c488d2b81
title: Функция Нтжеткуррентпроцессорнумбер
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtGetCurrentProcessorNumber
api_type:
- DllExport
api_location:
- Ntdll.dll
ms.openlocfilehash: 96862836d3f9c16034ce1c2e751aebea2884d114
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679817"
---
# <a name="ntgetcurrentprocessornumber-function"></a><span data-ttu-id="53236-103">Функция Нтжеткуррентпроцессорнумбер</span><span class="sxs-lookup"><span data-stu-id="53236-103">NtGetCurrentProcessorNumber function</span></span>

<span data-ttu-id="53236-104">\[**Нтжеткуррентпроцессорнумбер** может быть изменен или недоступен в будущих версиях Windows.</span><span class="sxs-lookup"><span data-stu-id="53236-104">\[**NtGetCurrentProcessorNumber** may be altered or unavailable in future versions of Windows.</span></span> <span data-ttu-id="53236-105">Вместо этого приложения должны использовать функцию [**жеткуррентпроцессорнумбер**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getcurrentprocessornumber) .\]</span><span class="sxs-lookup"><span data-stu-id="53236-105">Applications should use the [**GetCurrentProcessorNumber**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getcurrentprocessornumber) function instead.\]</span></span>

<span data-ttu-id="53236-106">Возвращает номер процессора, на котором выполнялся текущий поток во время вызова этой функции.</span><span class="sxs-lookup"><span data-stu-id="53236-106">Retrieves the number of the processor the current thread was running on during the call to this function.</span></span>

## <a name="syntax"></a><span data-ttu-id="53236-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="53236-107">Syntax</span></span>


```C++
ULONG WINAPI NtGetCurrentProcessorNumber(void);
```



## <a name="parameters"></a><span data-ttu-id="53236-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="53236-108">Parameters</span></span>

<span data-ttu-id="53236-109">У этой функции нет параметров.</span><span class="sxs-lookup"><span data-stu-id="53236-109">This function has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="53236-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="53236-110">Return value</span></span>

<span data-ttu-id="53236-111">Функция возвращает текущий номер процессора.</span><span class="sxs-lookup"><span data-stu-id="53236-111">The function returns the current processor number.</span></span>

## <a name="remarks"></a><span data-ttu-id="53236-112">Комментарии</span><span class="sxs-lookup"><span data-stu-id="53236-112">Remarks</span></span>

<span data-ttu-id="53236-113">Эта функция используется для предоставления сведений для оценки производительности процесса.</span><span class="sxs-lookup"><span data-stu-id="53236-113">This function is used to provide information for estimating process performance.</span></span>

<span data-ttu-id="53236-114">Эта функция не имеет связанной библиотеки импорта.</span><span class="sxs-lookup"><span data-stu-id="53236-114">This function has no associated import library.</span></span> <span data-ttu-id="53236-115">Для динамической привязки к Ntdll.dll необходимо использовать функции [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) и [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="53236-115">You must use the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions to dynamically link to Ntdll.dll.</span></span>

## <a name="requirements"></a><span data-ttu-id="53236-116">Требования</span><span class="sxs-lookup"><span data-stu-id="53236-116">Requirements</span></span>



| <span data-ttu-id="53236-117">Требование</span><span class="sxs-lookup"><span data-stu-id="53236-117">Requirement</span></span> | <span data-ttu-id="53236-118">Значение</span><span class="sxs-lookup"><span data-stu-id="53236-118">Value</span></span> |
|----------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="53236-119">DLL</span><span class="sxs-lookup"><span data-stu-id="53236-119">DLL</span></span><br/> | <dl> <span data-ttu-id="53236-120"><dt>Ntdll.dll</dt></span><span class="sxs-lookup"><span data-stu-id="53236-120"><dt>Ntdll.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="53236-121">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="53236-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="53236-122">Несколько процессоров</span><span class="sxs-lookup"><span data-stu-id="53236-122">Multiple Processors</span></span>](multiple-processors.md)
</dt> <dt>

[<span data-ttu-id="53236-123">Функции процессов и потоков</span><span class="sxs-lookup"><span data-stu-id="53236-123">Process and Thread Functions</span></span>](process-and-thread-functions.md)
</dt> <dt>

[<span data-ttu-id="53236-124">Процессы</span><span class="sxs-lookup"><span data-stu-id="53236-124">Processes</span></span>](child-processes.md)
</dt> </dl>

 

 
