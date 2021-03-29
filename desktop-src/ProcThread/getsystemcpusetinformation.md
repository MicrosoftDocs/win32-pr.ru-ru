---
description: Позволяет приложению запрашивать доступные наборы ЦП в системе и их текущее состояние.
ms.assetid: 168B00AB-1B11-44A0-B548-903CA3F4BBDE
title: Функция Жетсистемкпусетинформатион (Процесссреадапи. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetSystemCpuSetInformation
api_type:
- DllExport
api_location:
- Kernel32.dll
- API-MS-Win-Core-ProcessThreads-L1-1-3.dll
- KernelBase.dll
ms.openlocfilehash: d8ce490e3377e45a81b24523504d06941755de49
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104264496"
---
# <a name="getsystemcpusetinformation-function"></a><span data-ttu-id="e70ca-103">Функция Жетсистемкпусетинформатион</span><span class="sxs-lookup"><span data-stu-id="e70ca-103">GetSystemCpuSetInformation function</span></span>

<span data-ttu-id="e70ca-104">Позволяет приложению запрашивать доступные наборы ЦП в системе и их текущее состояние.</span><span class="sxs-lookup"><span data-stu-id="e70ca-104">Allows an application to query the available CPU Sets on the system, and their current state.</span></span>

## <a name="syntax"></a><span data-ttu-id="e70ca-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e70ca-105">Syntax</span></span>


```C++
BOOL WINAPI GetSystemCpuSetInformation(
  _Out_opt_  PSYSTEM_CPU_SET_INFORMATION  Information,
  _In_       ULONG                        BufferLength,
  _Out_      PULONG                       ReturnedLength,
  _In_opt_   HANDLE                       Process,
  _Reserved_ ULONG                        Flags
);
```



## <a name="parameters"></a><span data-ttu-id="e70ca-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="e70ca-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e70ca-107">*Сведения о* \[ out, необязательно\]</span><span class="sxs-lookup"><span data-stu-id="e70ca-107">*Information* \[out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="e70ca-108">Указатель на [**\_ \_ \_ информационную структуру набора ЦП системы**](/windows/desktop/api/winnt/ns-winnt-system_cpu_set_information) , которая получает данные о наборе ЦП.</span><span class="sxs-lookup"><span data-stu-id="e70ca-108">A pointer to a [**SYSTEM\_CPU\_SET\_INFORMATION**](/windows/desktop/api/winnt/ns-winnt-system_cpu_set_information) structure that receives the CPU Set data.</span></span> <span data-ttu-id="e70ca-109">Передайте значение NULL с длиной буфера 0, чтобы определить требуемый размер буфера.</span><span class="sxs-lookup"><span data-stu-id="e70ca-109">Pass NULL with a buffer length of 0 to determine the required buffer size.</span></span>

</dd> <dt>

<span data-ttu-id="e70ca-110">*BufferLength* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="e70ca-110">*BufferLength* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e70ca-111">Длина выходного буфера (в байтах), переданного в качестве информационного аргумента.</span><span class="sxs-lookup"><span data-stu-id="e70ca-111">The length, in bytes, of the output buffer passed as the Information argument.</span></span>

</dd> <dt>

<span data-ttu-id="e70ca-112">*Ретурнедленгс* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="e70ca-112">*ReturnedLength* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e70ca-113">Длина в байтах допустимых данных в выходном буфере, если буфер достаточно большой, или требуемый размер выходного буфера.</span><span class="sxs-lookup"><span data-stu-id="e70ca-113">The length, in bytes, of the valid data in the output buffer if the buffer is large enough, or the required size of the output buffer.</span></span> <span data-ttu-id="e70ca-114">Если наборы ЦП не существуют, это значение будет равно 0.</span><span class="sxs-lookup"><span data-stu-id="e70ca-114">If no CPU Sets exist, this value will be 0.</span></span>

</dd> <dt>

<span data-ttu-id="e70ca-115">*Обработка* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="e70ca-115">*Process* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="e70ca-116">Необязательный обработчик для процесса.</span><span class="sxs-lookup"><span data-stu-id="e70ca-116">An optional handle to a process.</span></span> <span data-ttu-id="e70ca-117">Этот процесс используется для определения значения флага **аллокатедтотаржетпроцесс** в \_ \_ структуре сведений о наборе ЦП системы \_ .</span><span class="sxs-lookup"><span data-stu-id="e70ca-117">This process is used to determine the value of the **AllocatedToTargetProcess** flag in the SYSTEM\_CPU\_SET\_INFORMATION structure.</span></span> <span data-ttu-id="e70ca-118">Если набор ЦП выделен для указанного процесса, устанавливается флаг.</span><span class="sxs-lookup"><span data-stu-id="e70ca-118">If a CPU Set is allocated to the specified process, the flag is set.</span></span> <span data-ttu-id="e70ca-119">В противном случае он очищается.</span><span class="sxs-lookup"><span data-stu-id="e70ca-119">Otherwise, it is clear.</span></span> <span data-ttu-id="e70ca-120">Этот обработчик должен иметь право на \_ \_ доступ к ограниченным данным Process \_ .</span><span class="sxs-lookup"><span data-stu-id="e70ca-120">This handle must have the PROCESS\_QUERY\_LIMITED\_INFORMATION access right.</span></span> <span data-ttu-id="e70ca-121">Значение, возвращаемое функцией [**жеткуррентпроцесс**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getcurrentprocess) , также может быть указано здесь.</span><span class="sxs-lookup"><span data-stu-id="e70ca-121">The value returned by [**GetCurrentProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getcurrentprocess) may also be specified here.</span></span>

</dd> <dt>

<span data-ttu-id="e70ca-122">*Флаги*</span><span class="sxs-lookup"><span data-stu-id="e70ca-122">*Flags*</span></span> 
</dt> <dd>

<span data-ttu-id="e70ca-123">Зарезервировано, должно быть равно 0.</span><span class="sxs-lookup"><span data-stu-id="e70ca-123">Reserved, must be 0.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e70ca-124">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="e70ca-124">Return value</span></span>

<span data-ttu-id="e70ca-125">Если API завершается, возвращается значение TRUE.</span><span class="sxs-lookup"><span data-stu-id="e70ca-125">If the API succeeds it returns TRUE.</span></span> <span data-ttu-id="e70ca-126">В случае неудачи причина ошибки доступна через **GetLastError**.</span><span class="sxs-lookup"><span data-stu-id="e70ca-126">If it fails, the error reason is available through **GetLastError**.</span></span> <span data-ttu-id="e70ca-127">Если информационный буфер имел неопределенное значение или недостаточно большой, возвращается ошибка с кодом \_ недостаточный \_ Размер буфера.</span><span class="sxs-lookup"><span data-stu-id="e70ca-127">If the Information buffer was NULL or not large enough, the error code ERROR\_INSUFFICIENT\_BUFFER is returned.</span></span> <span data-ttu-id="e70ca-128">Этот API не может быть выполнен, если переданы допустимые параметры и буфер, достаточно большой для хранения всех возвращаемых данных.</span><span class="sxs-lookup"><span data-stu-id="e70ca-128">This API cannot fail when passed valid parameters and a buffer that is large enough to hold all of the return data.</span></span>

## <a name="requirements"></a><span data-ttu-id="e70ca-129">Требования</span><span class="sxs-lookup"><span data-stu-id="e70ca-129">Requirements</span></span>



| <span data-ttu-id="e70ca-130">Требование</span><span class="sxs-lookup"><span data-stu-id="e70ca-130">Requirement</span></span> | <span data-ttu-id="e70ca-131">Значение</span><span class="sxs-lookup"><span data-stu-id="e70ca-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="e70ca-132">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="e70ca-132">Minimum supported client</span></span><br/> | <span data-ttu-id="e70ca-133">\[Приложения UWP для классических приложений Windows 10 \|\]</span><span class="sxs-lookup"><span data-stu-id="e70ca-133">Windows 10 \[desktop apps \| UWP apps\]</span></span><br/>                                            |
| <span data-ttu-id="e70ca-134">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="e70ca-134">Minimum supported server</span></span><br/> | <span data-ttu-id="e70ca-135">\[Приложения UWP для классических приложений Windows Server 2016 \|\]</span><span class="sxs-lookup"><span data-stu-id="e70ca-135">Windows Server 2016 \[desktop apps \| UWP apps\]</span></span><br/>                                   |
| <span data-ttu-id="e70ca-136">Header</span><span class="sxs-lookup"><span data-stu-id="e70ca-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="e70ca-137"><dt>Процесссреадсапи. h</dt></span><span class="sxs-lookup"><span data-stu-id="e70ca-137"><dt>Processthreadsapi.h</dt></span></span> </dl> |
| <span data-ttu-id="e70ca-138">Библиотека</span><span class="sxs-lookup"><span data-stu-id="e70ca-138">Library</span></span><br/>                  | <dl> <span data-ttu-id="e70ca-139"><dt>Windows. h</dt></span><span class="sxs-lookup"><span data-stu-id="e70ca-139"><dt>Windows.h</dt></span></span> </dl>          |
| <span data-ttu-id="e70ca-140">DLL</span><span class="sxs-lookup"><span data-stu-id="e70ca-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e70ca-141"><dt>Kernel32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e70ca-141"><dt>Kernel32.dll</dt></span></span> </dl>       |



 

