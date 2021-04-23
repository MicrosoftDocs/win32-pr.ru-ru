---
description: Возвращает текущее значение счетчика производительности и, при необходимости, частоту счетчика производительности.
ms.assetid: ab8973b7-a358-4e50-85e8-9dbff4e67010
title: Функция Нткуериперформанцекаунтер
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtQueryPerformanceCounter
api_type:
- DllExport
api_location:
- Ntdll.dll
ms.openlocfilehash: 5bf0aad74f6992212fb3b2238b3030c68cda2fc6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105665365"
---
# <a name="ntqueryperformancecounter-function"></a><span data-ttu-id="16f93-103">Функция Нткуериперформанцекаунтер</span><span class="sxs-lookup"><span data-stu-id="16f93-103">NtQueryPerformanceCounter function</span></span>

<span data-ttu-id="16f93-104">\[Эта функция не поддерживается и не должна использоваться.</span><span class="sxs-lookup"><span data-stu-id="16f93-104">\[This function is not supported and should not be used.</span></span> <span data-ttu-id="16f93-105">Вместо этого используйте функции **QueryPerformanceCounter** и **куериперформанцефрекуенци** .\]</span><span class="sxs-lookup"><span data-stu-id="16f93-105">Use the **QueryPerformanceCounter** and **QueryPerformanceFrequency** functions instead.\]</span></span>

<span data-ttu-id="16f93-106">Возвращает текущее значение счетчика производительности и, при необходимости, частоту счетчика производительности.</span><span class="sxs-lookup"><span data-stu-id="16f93-106">Returns the current value of a performance counter and, optionally, the frequency of the performance counter.</span></span>

## <a name="syntax"></a><span data-ttu-id="16f93-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="16f93-107">Syntax</span></span>


```C++
NTSTATUS NtQueryPerformanceCounter(
  _Out_     PLARGE_INTEGER PerformanceCounter,
  _Out_opt_ PLARGE_INTEGER PerformanceFrequency
);
```



## <a name="parameters"></a><span data-ttu-id="16f93-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="16f93-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="16f93-109">*PerformanceCounter* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="16f93-109">*PerformanceCounter* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="16f93-110">Адрес переменной, получающей текущее значение счетчика производительности.</span><span class="sxs-lookup"><span data-stu-id="16f93-110">The address of a variable to receive the current performance counter value.</span></span>

</dd> <dt>

<span data-ttu-id="16f93-111">*PerformanceFrequency* \[ out, необязательно\]</span><span class="sxs-lookup"><span data-stu-id="16f93-111">*PerformanceFrequency* \[out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="16f93-112">Адрес переменной для получения частоты счетчика производительности.</span><span class="sxs-lookup"><span data-stu-id="16f93-112">The address of a variable to receive the performance counter frequency.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="16f93-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="16f93-113">Return value</span></span>

<span data-ttu-id="16f93-114">Если функция выполнена успешно, она возвращает код **NTSTATUS** **\_ Success**, в противном случае возвращается код ошибки, например **\_ \_ нарушение прав доступа к состоянию**.</span><span class="sxs-lookup"><span data-stu-id="16f93-114">If the function succeeds, it returns the **NTSTATUS** code **STATUS\_SUCCESS**; otherwise, it returns an error code such as **STATUS\_ACCESS\_VIOLATION**.</span></span>

## <a name="remarks"></a><span data-ttu-id="16f93-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="16f93-115">Remarks</span></span>

<span data-ttu-id="16f93-116">Нет файла заголовка, доступного для **нткуериперформанцекаунтер**.</span><span class="sxs-lookup"><span data-stu-id="16f93-116">No header file is available for **NtQueryPerformanceCounter**.</span></span> <span data-ttu-id="16f93-117">Следует использовать альтернативные функции, указанные выше, хотя функции [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) и [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) можно использовать для динамической привязки к Ntdll.dll.</span><span class="sxs-lookup"><span data-stu-id="16f93-117">You should use the alternative functions named above, although you can also use the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions to dynamically link to Ntdll.dll.</span></span>

<span data-ttu-id="16f93-118">Частота производительности — это частота счетчика производительности в герцах, особенно в количестве в секунду.</span><span class="sxs-lookup"><span data-stu-id="16f93-118">Performance frequency is the frequency of the performance counter in hertz, specifically in counts per second.</span></span> <span data-ttu-id="16f93-119">Это значение зависит от реализации.</span><span class="sxs-lookup"><span data-stu-id="16f93-119">This value is implementation dependent.</span></span> <span data-ttu-id="16f93-120">Если в реализации отсутствует оборудование для поддержки времени производительности, возвращается значение 0.</span><span class="sxs-lookup"><span data-stu-id="16f93-120">If the implementation does not have hardware to support performance timing, the value returned is 0.</span></span>

## <a name="requirements"></a><span data-ttu-id="16f93-121">Требования</span><span class="sxs-lookup"><span data-stu-id="16f93-121">Requirements</span></span>



| <span data-ttu-id="16f93-122">Требование</span><span class="sxs-lookup"><span data-stu-id="16f93-122">Requirement</span></span> | <span data-ttu-id="16f93-123">Значение</span><span class="sxs-lookup"><span data-stu-id="16f93-123">Value</span></span> |
|----------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="16f93-124">DLL</span><span class="sxs-lookup"><span data-stu-id="16f93-124">DLL</span></span><br/> | <dl> <span data-ttu-id="16f93-125"><dt>Ntdll.dll</dt></span><span class="sxs-lookup"><span data-stu-id="16f93-125"><dt>Ntdll.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="16f93-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="16f93-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="16f93-127">**QueryPerformanceCounter**</span><span class="sxs-lookup"><span data-stu-id="16f93-127">**QueryPerformanceCounter**</span></span>](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter)
</dt> <dt>

[<span data-ttu-id="16f93-128">**куериперформанцефрекуенци**</span><span class="sxs-lookup"><span data-stu-id="16f93-128">**QueryPerformanceFrequency**</span></span>](/windows/win32/api/profileapi/nf-profileapi-queryperformancefrequency)
</dt> </dl>

 

 
