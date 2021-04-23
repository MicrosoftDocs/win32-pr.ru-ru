---
description: Извлекает указанные сведения о системе.
ms.assetid: c91b9a35-ca2b-4d81-973d-fe709144df90
title: Функция Звкуерисистеминформатион
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ZwQuerySystemInformation
api_type:
- DllExport
api_location:
- Ntdll.dll
- ntoskrnl.exe
ms.openlocfilehash: 2e516b12e5109470c1ddb86ea6a665ca29f138b2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105668695"
---
# <a name="zwquerysysteminformation-function"></a><span data-ttu-id="f18a0-103">Функция Звкуерисистеминформатион</span><span class="sxs-lookup"><span data-stu-id="f18a0-103">ZwQuerySystemInformation function</span></span>

<span data-ttu-id="f18a0-104">\[**Звкуерисистеминформатион** больше не доступен для использования в Windows 8.</span><span class="sxs-lookup"><span data-stu-id="f18a0-104">\[**ZwQuerySystemInformation** is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="f18a0-105">Вместо этого используйте альтернативные функции, перечисленные в этом разделе.\]</span><span class="sxs-lookup"><span data-stu-id="f18a0-105">Instead, use the alternate functions listed in this topic.\]</span></span>

<span data-ttu-id="f18a0-106">Извлекает указанные сведения о системе.</span><span class="sxs-lookup"><span data-stu-id="f18a0-106">Retrieves the specified system information.</span></span>

## <a name="syntax"></a><span data-ttu-id="f18a0-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f18a0-107">Syntax</span></span>


```C++
NTSTATUS WINAPI ZwQuerySystemInformation(
  _In_      SYSTEM_INFORMATION_CLASS SystemInformationClass,
  _Inout_   PVOID                    SystemInformation,
  _In_      ULONG                    SystemInformationLength,
  _Out_opt_ PULONG                   ReturnLength
);
```



## <a name="parameters"></a><span data-ttu-id="f18a0-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="f18a0-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f18a0-109">*Системинформатионкласс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="f18a0-109">*SystemInformationClass* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f18a0-110">Тип системных сведений для извлечения.</span><span class="sxs-lookup"><span data-stu-id="f18a0-110">The type of system information to be retrieved.</span></span> <span data-ttu-id="f18a0-111">Этот параметр может принимать одно из следующих значений из типа перечисления **\_ \_ класс системных сведений** .</span><span class="sxs-lookup"><span data-stu-id="f18a0-111">This parameter can be one of the following values from the **SYSTEM\_INFORMATION\_CLASS** enumeration type.</span></span>

<dt>

<span id="SystemBasicInformation"></span><span id="systembasicinformation"></span><span id="SYSTEMBASICINFORMATION"></span>

<span data-ttu-id="f18a0-112"><span id="SystemBasicInformation"></span><span id="systembasicinformation"></span><span id="SYSTEMBASICINFORMATION"></span>**систембасиЦинформатион**</span><span class="sxs-lookup"><span data-stu-id="f18a0-112"><span id="SystemBasicInformation"></span><span id="systembasicinformation"></span><span id="SYSTEMBASICINFORMATION"></span>**SystemBasicInformation**</span></span>


</dt> <dd>

<span data-ttu-id="f18a0-113">Количество процессоров в системе в **\_ базовой \_ информационной структуре системы** .</span><span class="sxs-lookup"><span data-stu-id="f18a0-113">The number of processors in the system in a **SYSTEM\_BASIC\_INFORMATION** structure.</span></span> <span data-ttu-id="f18a0-114">Вместо этого используйте функцию [**жетсистеминфо**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getsysteminfo) .</span><span class="sxs-lookup"><span data-stu-id="f18a0-114">Use the [**GetSystemInfo**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getsysteminfo) function instead.</span></span>

</dd> <dt>

<span id="SystemPerformanceInformation"></span><span id="systemperformanceinformation"></span><span id="SYSTEMPERFORMANCEINFORMATION"></span>

<span data-ttu-id="f18a0-115"><span id="SystemPerformanceInformation"></span><span id="systemperformanceinformation"></span><span id="SYSTEMPERFORMANCEINFORMATION"></span>**системперформанцеинформатион**</span><span class="sxs-lookup"><span data-stu-id="f18a0-115"><span id="SystemPerformanceInformation"></span><span id="systemperformanceinformation"></span><span id="SYSTEMPERFORMANCEINFORMATION"></span>**SystemPerformanceInformation**</span></span>


</dt> <dd>

<span data-ttu-id="f18a0-116">Структура **\_ \_ сведений о производительности** непрозрачной системы, которую можно использовать для создания непредсказуемого начального значения генератора случайных чисел.</span><span class="sxs-lookup"><span data-stu-id="f18a0-116">An opaque **SYSTEM\_PERFORMANCE\_INFORMATION** structure that can be used to generate an unpredictable seed for a random number generator.</span></span> <span data-ttu-id="f18a0-117">Вместо этого используйте функцию [**CryptGenRandom**](/windows/desktop/api/wincrypt/nf-wincrypt-cryptgenrandom) .</span><span class="sxs-lookup"><span data-stu-id="f18a0-117">Use the [**CryptGenRandom**](/windows/desktop/api/wincrypt/nf-wincrypt-cryptgenrandom) function instead.</span></span>

</dd> <dt>

<span id="SystemTimeOfDayInformation"></span><span id="systemtimeofdayinformation"></span><span id="SYSTEMTIMEOFDAYINFORMATION"></span>

<span data-ttu-id="f18a0-118"><span id="SystemTimeOfDayInformation"></span><span id="systemtimeofdayinformation"></span><span id="SYSTEMTIMEOFDAYINFORMATION"></span>**системтимеофдайинформатион**</span><span class="sxs-lookup"><span data-stu-id="f18a0-118"><span id="SystemTimeOfDayInformation"></span><span id="systemtimeofdayinformation"></span><span id="SYSTEMTIMEOFDAYINFORMATION"></span>**SystemTimeOfDayInformation**</span></span>


</dt> <dd>

<span data-ttu-id="f18a0-119">Структура **\_ \_ сведений о** непрозрачной системе, которую можно использовать для создания непредсказуемого начального значения для генератора случайных чисел.</span><span class="sxs-lookup"><span data-stu-id="f18a0-119">An opaque **SYSTEM\_TIMEOFDAY\_INFORMATION** structure that can be used to generate an unpredictable seed for a random number generator.</span></span> <span data-ttu-id="f18a0-120">Вместо этого используйте функцию [**CryptGenRandom**](/windows/desktop/api/wincrypt/nf-wincrypt-cryptgenrandom) .</span><span class="sxs-lookup"><span data-stu-id="f18a0-120">Use the [**CryptGenRandom**](/windows/desktop/api/wincrypt/nf-wincrypt-cryptgenrandom) function instead.</span></span>

</dd> <dt>

<span id="SystemProcessInformation"></span><span id="systemprocessinformation"></span><span id="SYSTEMPROCESSINFORMATION"></span>

<span data-ttu-id="f18a0-121"><span id="SystemProcessInformation"></span><span id="systemprocessinformation"></span><span id="SYSTEMPROCESSINFORMATION"></span>**системпроцессинформатион**</span><span class="sxs-lookup"><span data-stu-id="f18a0-121"><span id="SystemProcessInformation"></span><span id="systemprocessinformation"></span><span id="SYSTEMPROCESSINFORMATION"></span>**SystemProcessInformation**</span></span>


</dt> <dd>

<span data-ttu-id="f18a0-122">Массив структур **\_ \_ сведений о системных процессах** , по одному для каждого процесса, выполняемого в системе.</span><span class="sxs-lookup"><span data-stu-id="f18a0-122">An array of **SYSTEM\_PROCESS\_INFORMATION** structures, one for each process running in the system.</span></span>

<span data-ttu-id="f18a0-123">Эти структуры содержат сведения об использовании ресурсов каждым процессом, включая количество дескрипторов, используемых процессом, пиковое использование файлов страниц и количество страниц памяти, выделенных процессом.</span><span class="sxs-lookup"><span data-stu-id="f18a0-123">These structures contain information about the resource usage of each process, including the number of handles used by the process, the peak page-file usage, and the number of memory pages that the process has allocated.</span></span>

</dd> <dt>

<span id="SystemProcessorPerformanceInformation"></span><span id="systemprocessorperformanceinformation"></span><span id="SYSTEMPROCESSORPERFORMANCEINFORMATION"></span>

<span data-ttu-id="f18a0-124"><span id="SystemProcessorPerformanceInformation"></span><span id="systemprocessorperformanceinformation"></span><span id="SYSTEMPROCESSORPERFORMANCEINFORMATION"></span>**системпроцессорперформанцеинформатион**</span><span class="sxs-lookup"><span data-stu-id="f18a0-124"><span id="SystemProcessorPerformanceInformation"></span><span id="systemprocessorperformanceinformation"></span><span id="SYSTEMPROCESSORPERFORMANCEINFORMATION"></span>**SystemProcessorPerformanceInformation**</span></span>


</dt> <dd>

<span data-ttu-id="f18a0-125">Массив структур **\_ \_ \_ сведений о производительности системного процессора** , по одному для каждого процессора, установленного в системе.</span><span class="sxs-lookup"><span data-stu-id="f18a0-125">An array of **SYSTEM\_PROCESSOR\_PERFORMANCE\_INFORMATION** structures, one for each processor installed in the system.</span></span>

</dd> <dt>

<span id="SystemInterruptInformation"></span><span id="systeminterruptinformation"></span><span id="SYSTEMINTERRUPTINFORMATION"></span>

<span data-ttu-id="f18a0-126"><span id="SystemInterruptInformation"></span><span id="systeminterruptinformation"></span><span id="SYSTEMINTERRUPTINFORMATION"></span>**системинтерруптинформатион**</span><span class="sxs-lookup"><span data-stu-id="f18a0-126"><span id="SystemInterruptInformation"></span><span id="systeminterruptinformation"></span><span id="SYSTEMINTERRUPTINFORMATION"></span>**SystemInterruptInformation**</span></span>


</dt> <dd>

<span data-ttu-id="f18a0-127">Структура **\_ \_ информации о непрозрачном системном прерывании** , которую можно использовать для создания непредсказуемого начального значения генератора случайных чисел.</span><span class="sxs-lookup"><span data-stu-id="f18a0-127">An opaque **SYSTEM\_INTERRUPT\_INFORMATION** structure that can be used to generate an unpredictable seed for a random number generator.</span></span> <span data-ttu-id="f18a0-128">Вместо этого используйте функцию [**CryptGenRandom**](/windows/desktop/api/wincrypt/nf-wincrypt-cryptgenrandom) .</span><span class="sxs-lookup"><span data-stu-id="f18a0-128">Use the [**CryptGenRandom**](/windows/desktop/api/wincrypt/nf-wincrypt-cryptgenrandom) function instead.</span></span>

</dd> <dt>

<span id="SystemExceptionInformation"></span><span id="systemexceptioninformation"></span><span id="SYSTEMEXCEPTIONINFORMATION"></span>

<span data-ttu-id="f18a0-129"><span id="SystemExceptionInformation"></span><span id="systemexceptioninformation"></span><span id="SYSTEMEXCEPTIONINFORMATION"></span>**системексцептионинформатион**</span><span class="sxs-lookup"><span data-stu-id="f18a0-129"><span id="SystemExceptionInformation"></span><span id="systemexceptioninformation"></span><span id="SYSTEMEXCEPTIONINFORMATION"></span>**SystemExceptionInformation**</span></span>


</dt> <dd>

<span data-ttu-id="f18a0-130">Структура **\_ \_ сведений о непрозрачных системных исключениях** , которую можно использовать для создания непредсказуемого начального значения генератора случайных чисел.</span><span class="sxs-lookup"><span data-stu-id="f18a0-130">An opaque **SYSTEM\_EXCEPTION\_INFORMATION** structure that can be used to generate an unpredictable seed for a random number generator.</span></span> <span data-ttu-id="f18a0-131">Вместо этого используйте функцию [**CryptGenRandom**](/windows/desktop/api/wincrypt/nf-wincrypt-cryptgenrandom) .</span><span class="sxs-lookup"><span data-stu-id="f18a0-131">Use the [**CryptGenRandom**](/windows/desktop/api/wincrypt/nf-wincrypt-cryptgenrandom) function instead.</span></span>

</dd> <dt>

<span id="SystemRegistryQuotaInformation"></span><span id="systemregistryquotainformation"></span><span id="SYSTEMREGISTRYQUOTAINFORMATION"></span>

<span data-ttu-id="f18a0-132"><span id="SystemRegistryQuotaInformation"></span><span id="systemregistryquotainformation"></span><span id="SYSTEMREGISTRYQUOTAINFORMATION"></span>**системрегистрикуотаинформатион**</span><span class="sxs-lookup"><span data-stu-id="f18a0-132"><span id="SystemRegistryQuotaInformation"></span><span id="systemregistryquotainformation"></span><span id="SYSTEMREGISTRYQUOTAINFORMATION"></span>**SystemRegistryQuotaInformation**</span></span>


</dt> <dd>

<span data-ttu-id="f18a0-133">Структура **\_ \_ \_ сведений о квотах системного реестра** .</span><span class="sxs-lookup"><span data-stu-id="f18a0-133">A **SYSTEM\_REGISTRY\_QUOTA\_INFORMATION** structure.</span></span>

</dd> <dt>

<span id="SystemLookasideInformation"></span><span id="systemlookasideinformation"></span><span id="SYSTEMLOOKASIDEINFORMATION"></span>

<span data-ttu-id="f18a0-134"><span id="SystemLookasideInformation"></span><span id="systemlookasideinformation"></span><span id="SYSTEMLOOKASIDEINFORMATION"></span>**системлукасидеинформатион**</span><span class="sxs-lookup"><span data-stu-id="f18a0-134"><span id="SystemLookasideInformation"></span><span id="systemlookasideinformation"></span><span id="SYSTEMLOOKASIDEINFORMATION"></span>**SystemLookasideInformation**</span></span>


</dt> <dd>

<span data-ttu-id="f18a0-135">Структура информации непрозрачного **\_ \_ резерва системы** , которую можно использовать для создания непредсказуемого начального значения генератора случайных чисел.</span><span class="sxs-lookup"><span data-stu-id="f18a0-135">An opaque **SYSTEM\_LOOKASIDE\_INFORMATION** structure that can be used to generate an unpredictable seed for a random number generator.</span></span> <span data-ttu-id="f18a0-136">Вместо этого используйте функцию [**CryptGenRandom**](/windows/desktop/api/wincrypt/nf-wincrypt-cryptgenrandom) .</span><span class="sxs-lookup"><span data-stu-id="f18a0-136">Use the [**CryptGenRandom**](/windows/desktop/api/wincrypt/nf-wincrypt-cryptgenrandom) function instead.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="f18a0-137">*SystemInformation* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="f18a0-137">*SystemInformation* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="f18a0-138">Указатель на буфер, который получает запрошенную информацию.</span><span class="sxs-lookup"><span data-stu-id="f18a0-138">A pointer to a buffer that receives the requested information.</span></span> <span data-ttu-id="f18a0-139">Размер и структура этих сведений зависят от значения параметра *системинформатионкласс* , как показано в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="f18a0-139">The size and structure of this information varies depending on the value of the *SystemInformationClass* parameter, as indicated in the following table.</span></span>

<dt>

<span id="SYSTEM_BASIC_INFORMATION"></span><span id="system_basic_information"></span>

<span data-ttu-id="f18a0-140"><span id="SYSTEM_BASIC_INFORMATION"></span><span id="system_basic_information"></span>**\_основные \_ сведения о системе**</span><span class="sxs-lookup"><span data-stu-id="f18a0-140"><span id="SYSTEM_BASIC_INFORMATION"></span><span id="system_basic_information"></span>**SYSTEM\_BASIC\_INFORMATION**</span></span>


</dt> <dd>

<span data-ttu-id="f18a0-141">Если параметр *системинформатионкласс* имеет значение **систембасиЦинформатион**, буфер, на который указывает параметр *SystemInformation* , должен быть достаточно большим, чтобы вместить одну **системную \_ базовую структуру \_ информации** со следующим макетом:</span><span class="sxs-lookup"><span data-stu-id="f18a0-141">When the *SystemInformationClass* parameter is **SystemBasicInformation**, the buffer pointed to by the *SystemInformation* parameter should be large enough to hold a single **SYSTEM\_BASIC\_INFORMATION** structure having the following layout:</span></span>

``` syntax
typedef struct _SYSTEM_BASIC_INFORMATION {
    BYTE Reserved1[24];
    PVOID Reserved2[4];
    CCHAR NumberOfProcessors;
} SYSTEM_BASIC_INFORMATION;
```

<span data-ttu-id="f18a0-142">Член **NumberOfProcessors** содержит количество процессоров, имеющихся в системе.</span><span class="sxs-lookup"><span data-stu-id="f18a0-142">The **NumberOfProcessors** member contains the number of processors present in the system.</span></span> <span data-ttu-id="f18a0-143">Вместо этого используйте [**жетсистеминфо**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getsysteminfo) для получения этих сведений.</span><span class="sxs-lookup"><span data-stu-id="f18a0-143">Use [**GetSystemInfo**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getsysteminfo) instead to retrieve this information.</span></span>

<span data-ttu-id="f18a0-144">Другие члены структуры зарезервированы для внутреннего использования операционной системой.</span><span class="sxs-lookup"><span data-stu-id="f18a0-144">The other members of the structure are reserved for internal use by the operating system.</span></span>

</dd> <dt>

<span id="SYSTEM_PERFORMANCE_INFORMATION"></span><span id="system_performance_information"></span>

<span data-ttu-id="f18a0-145"><span id="SYSTEM_PERFORMANCE_INFORMATION"></span><span id="system_performance_information"></span>**\_ \_ сведения о производительности системы**</span><span class="sxs-lookup"><span data-stu-id="f18a0-145"><span id="SYSTEM_PERFORMANCE_INFORMATION"></span><span id="system_performance_information"></span>**SYSTEM\_PERFORMANCE\_INFORMATION**</span></span>


</dt> <dd>

<span data-ttu-id="f18a0-146">Если параметр *системинформатионкласс* имеет значение **системперформанцеинформатион**, буфер, на который указывает параметр *SystemInformation* , должен быть достаточно большим, чтобы вместить непрозрачную структуру **\_ \_ сведений о производительности системы** для использования при формировании непредсказуемого начального значения генератора случайных чисел.</span><span class="sxs-lookup"><span data-stu-id="f18a0-146">When the *SystemInformationClass* parameter is **SystemPerformanceInformation**, the buffer pointed to by the *SystemInformation* parameter should be large enough to hold an opaque **SYSTEM\_PERFORMANCE\_INFORMATION** structure for use in generating an unpredictable seed for a random number generator.</span></span> <span data-ttu-id="f18a0-147">Для этой цели структура имеет следующий макет:</span><span class="sxs-lookup"><span data-stu-id="f18a0-147">For this purpose, the structure has the following layout:</span></span>

``` syntax
typedef struct _SYSTEM_PERFORMANCE_INFORMATION {
    BYTE Reserved1[312];
} SYSTEM_PERFORMANCE_INFORMATION;
```

<span data-ttu-id="f18a0-148">Отдельные члены структуры зарезервированы для внутреннего использования операционной системой.</span><span class="sxs-lookup"><span data-stu-id="f18a0-148">Individual members of the structure are reserved for internal use by the operating system.</span></span>

<span data-ttu-id="f18a0-149">Вместо этого используйте функцию [**CryptGenRandom**](/windows/desktop/api/wincrypt/nf-wincrypt-cryptgenrandom) , чтобы создать криптографически случайные данные.</span><span class="sxs-lookup"><span data-stu-id="f18a0-149">Use the [**CryptGenRandom**](/windows/desktop/api/wincrypt/nf-wincrypt-cryptgenrandom) function instead to generate cryptographically random data.</span></span>

</dd> <dt>

<span id="SYSTEM_TIMEOFDAY_INFORMATION"></span><span id="system_timeofday_information"></span>

<span data-ttu-id="f18a0-150"><span id="SYSTEM_TIMEOFDAY_INFORMATION"></span><span id="system_timeofday_information"></span>**\_ \_ сведения о TIMEOFDAY системы**</span><span class="sxs-lookup"><span data-stu-id="f18a0-150"><span id="SYSTEM_TIMEOFDAY_INFORMATION"></span><span id="system_timeofday_information"></span>**SYSTEM\_TIMEOFDAY\_INFORMATION**</span></span>


</dt> <dd>

<span data-ttu-id="f18a0-151">Если параметр *системинформатионкласс* имеет значение **системтимеофдайинформатион**, буфер, на который указывает параметр *SystemInformation* , должен быть достаточно большим, чтобы вместить непрозрачную структуру **\_ \_ сведений о TIMEOFDAY системы** для использования при формировании непредсказуемого начального значения для генератора случайных чисел.</span><span class="sxs-lookup"><span data-stu-id="f18a0-151">When the *SystemInformationClass* parameter is **SystemTimeOfDayInformation**, the buffer pointed to by the *SystemInformation* parameter should be large enough to hold an opaque **SYSTEM\_TIMEOFDAY\_INFORMATION** structure for use in generating an unpredictable seed for a random number generator.</span></span> <span data-ttu-id="f18a0-152">Для этой цели структура имеет следующий макет:</span><span class="sxs-lookup"><span data-stu-id="f18a0-152">For this purpose, the structure has the following layout:</span></span>

``` syntax
typedef struct _SYSTEM_TIMEOFDAY_INFORMATION {
    BYTE Reserved1[48];
} SYSTEM_TIMEOFDAY_INFORMATION;
```

<span data-ttu-id="f18a0-153">Отдельные члены структуры зарезервированы для внутреннего использования операционной системой.</span><span class="sxs-lookup"><span data-stu-id="f18a0-153">Individual members of the structure are reserved for internal use by the operating system.</span></span>

<span data-ttu-id="f18a0-154">Вместо этого используйте функцию [**CryptGenRandom**](/windows/desktop/api/wincrypt/nf-wincrypt-cryptgenrandom) , чтобы создать криптографически случайные данные.</span><span class="sxs-lookup"><span data-stu-id="f18a0-154">Use the [**CryptGenRandom**](/windows/desktop/api/wincrypt/nf-wincrypt-cryptgenrandom) function instead to generate cryptographically random data.</span></span>

</dd> <dt>

<span id="SYSTEM_PROCESS_INFORMATION"></span><span id="system_process_information"></span>

<span data-ttu-id="f18a0-155"><span id="SYSTEM_PROCESS_INFORMATION"></span><span id="system_process_information"></span>**\_сведения о системных процессах \_**</span><span class="sxs-lookup"><span data-stu-id="f18a0-155"><span id="SYSTEM_PROCESS_INFORMATION"></span><span id="system_process_information"></span>**SYSTEM\_PROCESS\_INFORMATION**</span></span>


</dt> <dd>

<span data-ttu-id="f18a0-156">Если параметр *системинформатионкласс* имеет значение **системпроцессинформатион**, буфер, на который указывает параметр *SystemInformation* , должен быть достаточно большим, чтобы вместить массив, содержащий столько структур **\_ \_ сведений о системных процессах** , сколько запущенных в системе процессов.</span><span class="sxs-lookup"><span data-stu-id="f18a0-156">When the *SystemInformationClass* parameter is **SystemProcessInformation**, the buffer pointed to by the *SystemInformation* parameter should be large enough to hold an array that contains as many **SYSTEM\_PROCESS\_INFORMATION** structures as there are processes running in the system.</span></span> <span data-ttu-id="f18a0-157">Каждая структура имеет следующий макет:</span><span class="sxs-lookup"><span data-stu-id="f18a0-157">Each structure has the following layout:</span></span>

``` syntax
typedef struct _SYSTEM_PROCESS_INFORMATION {
    ULONG NextEntryOffset;
    ULONG NumberOfThreads;
    BYTE Reserved1[48];
    PVOID Reserved2[3];
    HANDLE UniqueProcessId;
    PVOID Reserved3;
    ULONG HandleCount;
    BYTE Reserved4[4];
    PVOID Reserved5[11];
    SIZE_T PeakPagefileUsage;
    SIZE_T PrivatePageCount;
    LARGE_INTEGER Reserved6[6];
} SYSTEM_PROCESS_INFORMATION;
```

<span data-ttu-id="f18a0-158">Элемент **NumberOfThreads** содержит общее число выполняющихся в данный момент потоков в процессе.</span><span class="sxs-lookup"><span data-stu-id="f18a0-158">The **NumberOfThreads** member contains the total number of currently running threads in the process.</span></span>

<span data-ttu-id="f18a0-159">Элемент **HandleCount** содержит общее количество дескрипторов, используемых рассматриваемым процессом; Используйте [**жетпроцесшандлекаунт**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-getprocesshandlecount) для получения этих сведений.</span><span class="sxs-lookup"><span data-stu-id="f18a0-159">The **HandleCount** member contains the total number of handles being used by the process in question; use [**GetProcessHandleCount**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-getprocesshandlecount) to retrieve this information instead.</span></span>

<span data-ttu-id="f18a0-160">Элемент **пеакпажефилеусаже** содержит максимальное число байтов хранилища файлов страниц, используемое процессом, а член **приватепажекаунт** содержит количество страниц памяти, выделенных для использования этим процессом.</span><span class="sxs-lookup"><span data-stu-id="f18a0-160">The **PeakPagefileUsage** member contains the maximum number of bytes of page-file storage used by the process, and the **PrivatePageCount** member contains the number of memory pages allocated for the use of this process.</span></span>

<span data-ttu-id="f18a0-161">Эти сведения также можно получить с помощью функции [**жетпроцессмеморинфо**](/windows/desktop/api/psapi/nf-psapi-getprocessmemoryinfo) или класса [**\_ процесса Win32**](/windows/desktop/CIMWin32Prov/win32-process) .</span><span class="sxs-lookup"><span data-stu-id="f18a0-161">You can also retrieve this information using either the [**GetProcessMemoryInfo**](/windows/desktop/api/psapi/nf-psapi-getprocessmemoryinfo) function or the [**Win32\_Process**](/windows/desktop/CIMWin32Prov/win32-process) class.</span></span>

<span data-ttu-id="f18a0-162">Другие члены структуры зарезервированы для внутреннего использования операционной системой.</span><span class="sxs-lookup"><span data-stu-id="f18a0-162">The other members of the structure are reserved for internal use by the operating system.</span></span>

</dd> <dt>

<span id="SYSTEM_PROCESSOR_PERFORMANCE_INFORMATION"></span><span id="system_processor_performance_information"></span>

<span data-ttu-id="f18a0-163"><span id="SYSTEM_PROCESSOR_PERFORMANCE_INFORMATION"></span><span id="system_processor_performance_information"></span>**\_ \_ сведения о производительности процессора системы \_**</span><span class="sxs-lookup"><span data-stu-id="f18a0-163"><span id="SYSTEM_PROCESSOR_PERFORMANCE_INFORMATION"></span><span id="system_processor_performance_information"></span>**SYSTEM\_PROCESSOR\_PERFORMANCE\_INFORMATION**</span></span>


</dt> <dd>

<span data-ttu-id="f18a0-164">Если параметр *системинформатионкласс* имеет значение **системпроцессорперформанцеинформатион**, буфер, на который указывает параметр *SystemInformation* , должен быть достаточно большим, чтобы вместить массив, содержащий столько структур **\_ \_ сведений о системных процессах** , сколько процессоров (ЦП) установлено в системе.</span><span class="sxs-lookup"><span data-stu-id="f18a0-164">When the *SystemInformationClass* parameter is **SystemProcessorPerformanceInformation**, the buffer pointed to by the *SystemInformation* parameter should be large enough to hold an array that contains as many **SYSTEM\_PROCESS\_INFORMATION** structures as there are processors (CPUs) installed in the system.</span></span> <span data-ttu-id="f18a0-165">Каждая структура имеет следующий макет:</span><span class="sxs-lookup"><span data-stu-id="f18a0-165">Each structure has the following layout:</span></span>

``` syntax
typedef struct
_SYSTEM_PROCESSOR_PERFORMANCE_INFORMATION {
    LARGE_INTEGER IdleTime;
    LARGE_INTEGER KernelTime;
    LARGE_INTEGER UserTime;
    LARGE_INTEGER Reserved1[2];
    ULONG Reserved2;
} SYSTEM_PROCESSOR_PERFORMANCE_INFORMATION;
```

<span data-ttu-id="f18a0-166">Элемент **идлетиме** содержит период бездействия системы в 1/100ths в наносекундных.</span><span class="sxs-lookup"><span data-stu-id="f18a0-166">The **IdleTime** member contains the amount of time that the system has been idle, in 1/100ths of a nanosecond.</span></span>

<span data-ttu-id="f18a0-167">Элемент **кернелтиме** содержит количество времени, которое система потратила на выполнение в режиме ядра (включая все потоки во всех процессах, на всех процессорах), в 1/100ths в наносекундных.</span><span class="sxs-lookup"><span data-stu-id="f18a0-167">The **KernelTime** member contains the amount of time that the system has spent executing in Kernel mode (including all threads in all processes, on all processors), in 1/100ths of a nanosecond.</span></span>

<span data-ttu-id="f18a0-168">Элемент **усертиме** содержит количество времени, которое система потратила на выполнение в пользовательском режиме (включая все потоки во всех процессах, на всех процессорах), в 1/100ths в наносекундных.</span><span class="sxs-lookup"><span data-stu-id="f18a0-168">The **UserTime** member contains the amount of time that the system has spent executing in User mode (including all threads in all processes, on all processors), in 1/100ths of a nanosecond.</span></span>

<span data-ttu-id="f18a0-169">Вместо этого используйте [**жетсистемтимес**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getsystemtimes) для получения этих сведений.</span><span class="sxs-lookup"><span data-stu-id="f18a0-169">Use [**GetSystemTimes**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getsystemtimes) instead to retrieve this information.</span></span>

</dd> <dt>

<span id="SYSTEM_INTERRUPT_INFORMATION"></span><span id="system_interrupt_information"></span>

<span data-ttu-id="f18a0-170"><span id="SYSTEM_INTERRUPT_INFORMATION"></span><span id="system_interrupt_information"></span>**\_сведения о прерывании системы \_**</span><span class="sxs-lookup"><span data-stu-id="f18a0-170"><span id="SYSTEM_INTERRUPT_INFORMATION"></span><span id="system_interrupt_information"></span>**SYSTEM\_INTERRUPT\_INFORMATION**</span></span>


</dt> <dd>

<span data-ttu-id="f18a0-171">Если параметр *системинформатионкласс* имеет значение **системинтерруптинформатион**, буфер, на который указывает параметр *SystemInformation* , должен быть достаточно большим, чтобы вместить массив, содержащий множество структур непрозрачных **системных \_ прерываний \_** , так как в системе установлены процессоры (ЦП).</span><span class="sxs-lookup"><span data-stu-id="f18a0-171">When the *SystemInformationClass* parameter is **SystemInterruptInformation**, the buffer pointed to by the *SystemInformation* parameter should be large enough to hold an array that contains as many opaque **SYSTEM\_INTERRUPT\_INFORMATION** structures as there are processors (CPUs) installed on the system.</span></span> <span data-ttu-id="f18a0-172">Каждая структура или массив в целом может использоваться для создания непредсказуемого начального значения генератора случайных чисел.</span><span class="sxs-lookup"><span data-stu-id="f18a0-172">Each structure, or the array as a whole, can be used to generate an unpredictable seed for a random number generator.</span></span> <span data-ttu-id="f18a0-173">Для этой цели структура имеет следующий макет:</span><span class="sxs-lookup"><span data-stu-id="f18a0-173">For this purpose, the structure has the following layout:</span></span>

``` syntax
typedef struct _SYSTEM_INTERRUPT_INFORMATION {
    BYTE Reserved1[24];
} SYSTEM_INTERRUPT_INFORMATION;
```

<span data-ttu-id="f18a0-174">Отдельные члены структуры зарезервированы для внутреннего использования операционной системой.</span><span class="sxs-lookup"><span data-stu-id="f18a0-174">Individual members of the structure are reserved for internal use by the operating system.</span></span>

<span data-ttu-id="f18a0-175">Вместо этого используйте функцию [**CryptGenRandom**](/windows/desktop/api/wincrypt/nf-wincrypt-cryptgenrandom) , чтобы создать криптографически случайные данные.</span><span class="sxs-lookup"><span data-stu-id="f18a0-175">Use the [**CryptGenRandom**](/windows/desktop/api/wincrypt/nf-wincrypt-cryptgenrandom) function instead to generate cryptographically random data.</span></span>

</dd> <dt>

<span id="SYSTEM_EXCEPTION_INFORMATION"></span><span id="system_exception_information"></span>

<span data-ttu-id="f18a0-176"><span id="SYSTEM_EXCEPTION_INFORMATION"></span><span id="system_exception_information"></span>**\_сведения об системном исключении \_**</span><span class="sxs-lookup"><span data-stu-id="f18a0-176"><span id="SYSTEM_EXCEPTION_INFORMATION"></span><span id="system_exception_information"></span>**SYSTEM\_EXCEPTION\_INFORMATION**</span></span>


</dt> <dd>

<span data-ttu-id="f18a0-177">Если параметр *системинформатионкласс* имеет значение **системексцептионинформатион**, буфер, на который указывает параметр *SystemInformation* , должен быть достаточно большим, чтобы вместить непрозрачную структуру **\_ \_ информации об исключениях системы** для использования при формировании непредсказуемого начального значения генератора случайных чисел.</span><span class="sxs-lookup"><span data-stu-id="f18a0-177">When the *SystemInformationClass* parameter is **SystemExceptionInformation**, the buffer pointed to by the *SystemInformation* parameter should be large enough to hold an opaque **SYSTEM\_EXCEPTION\_INFORMATION** structure for use in generating an unpredictable seed for a random number generator.</span></span> <span data-ttu-id="f18a0-178">Для этой цели структура имеет следующий макет:</span><span class="sxs-lookup"><span data-stu-id="f18a0-178">For this purpose, the structure has the following layout:</span></span>

``` syntax
typedef struct _SYSTEM_EXCEPTION_INFORMATION {
    BYTE Reserved1[16];
} SYSTEM_EXCEPTION_INFORMATION;
```

<span data-ttu-id="f18a0-179">Отдельные члены структуры зарезервированы для внутреннего использования операционной системой.</span><span class="sxs-lookup"><span data-stu-id="f18a0-179">Individual members of the structure are reserved for internal use by the operating system.</span></span>

<span data-ttu-id="f18a0-180">Вместо этого используйте функцию [**CryptGenRandom**](/windows/desktop/api/wincrypt/nf-wincrypt-cryptgenrandom) , чтобы создать криптографически случайные данные.</span><span class="sxs-lookup"><span data-stu-id="f18a0-180">Use the [**CryptGenRandom**](/windows/desktop/api/wincrypt/nf-wincrypt-cryptgenrandom) function instead to generate cryptographically random data.</span></span>

</dd> <dt>

<span id="SYSTEM_REGISTRY_QUOTA_INFORMATION"></span><span id="system_registry_quota_information"></span>

<span data-ttu-id="f18a0-181"><span id="SYSTEM_REGISTRY_QUOTA_INFORMATION"></span><span id="system_registry_quota_information"></span>**\_ \_ сведения о квотах системного реестра \_**</span><span class="sxs-lookup"><span data-stu-id="f18a0-181"><span id="SYSTEM_REGISTRY_QUOTA_INFORMATION"></span><span id="system_registry_quota_information"></span>**SYSTEM\_REGISTRY\_QUOTA\_INFORMATION**</span></span>


</dt> <dd>

<span data-ttu-id="f18a0-182">Если параметр *системинформатионкласс* имеет значение **системрегистрикуотаинформатион**, буфер, на который указывает параметр *SystemInformation* , должен быть достаточно большим, чтобы вместить одну **структуру \_ \_ \_ сведений о квотах системного реестра** со следующим макетом:</span><span class="sxs-lookup"><span data-stu-id="f18a0-182">When the *SystemInformationClass* parameter is **SystemRegistryQuotaInformation**, the buffer pointed to by the *SystemInformation* parameter should be large enough to hold a single **SYSTEM\_REGISTRY\_QUOTA\_INFORMATION** structure having the following layout:</span></span>

``` syntax
typedef struct _SYSTEM_REGISTRY_QUOTA_INFORMATION {
    ULONG RegistryQuotaAllowed;
    ULONG RegistryQuotaUsed;
    PVOID Reserved1;
} SYSTEM_REGISTRY_QUOTA_INFORMATION;
```

<span data-ttu-id="f18a0-183">Элемент **регистрикуотаалловед** содержит максимальный размер (в байтах), который может достичь реестр в системе.</span><span class="sxs-lookup"><span data-stu-id="f18a0-183">The **RegistryQuotaAllowed** member contains the maximum size, in bytes, that the Registry can attain on this system.</span></span>

<span data-ttu-id="f18a0-184">Элемент **регистрикуотаусед** содержит текущий размер реестра в байтах.</span><span class="sxs-lookup"><span data-stu-id="f18a0-184">The **RegistryQuotaUsed** member contains the current size of the Registry, in bytes.</span></span>

<span data-ttu-id="f18a0-185">Вместо этого используйте [**жетсистемрегистрикуота**](/windows/desktop/api/Winbase/nf-winbase-getsystemregistryquota) для получения этих сведений.</span><span class="sxs-lookup"><span data-stu-id="f18a0-185">Use [**GetSystemRegistryQuota**](/windows/desktop/api/Winbase/nf-winbase-getsystemregistryquota) instead to retrieve this information.</span></span>

<span data-ttu-id="f18a0-186">Другой член структуры зарезервирован для внутреннего использования операционной системой.</span><span class="sxs-lookup"><span data-stu-id="f18a0-186">The other member of the structure is reserved for internal use by the operating system.</span></span>

</dd> <dt>

<span id="SYSTEM_LOOKASIDE_INFORMATION"></span><span id="system_lookaside_information"></span>

<span data-ttu-id="f18a0-187"><span id="SYSTEM_LOOKASIDE_INFORMATION"></span><span id="system_lookaside_information"></span>**\_сведения о резерве системы \_**</span><span class="sxs-lookup"><span data-stu-id="f18a0-187"><span id="SYSTEM_LOOKASIDE_INFORMATION"></span><span id="system_lookaside_information"></span>**SYSTEM\_LOOKASIDE\_INFORMATION**</span></span>


</dt> <dd>

<span data-ttu-id="f18a0-188">Если параметр *системинформатионкласс* имеет значение **системлукасидеинформатион**, буфер, на который указывает параметр *SystemInformation* , должен быть достаточно большим, чтобы вместить непрозрачную структуру **\_ \_ информации о резерве системы** для использования при формировании непредсказуемого начального значения генератора случайных чисел.</span><span class="sxs-lookup"><span data-stu-id="f18a0-188">When the *SystemInformationClass* parameter is **SystemLookasideInformation**, the buffer pointed to by the *SystemInformation* parameter should be large enough to hold an opaque **SYSTEM\_LOOKASIDE\_INFORMATION** structure for use in generating an unpredictable seed for a random number generator.</span></span> <span data-ttu-id="f18a0-189">Для этой цели структура имеет следующий макет:</span><span class="sxs-lookup"><span data-stu-id="f18a0-189">For this purpose, the structure has the following layout:</span></span>

``` syntax
typedef struct _SYSTEM_LOOKASIDE_INFORMATION {
    BYTE Reserved1[32];
} SYSTEM_LOOKASIDE_INFORMATION;
```

<span data-ttu-id="f18a0-190">Отдельные члены структуры зарезервированы для внутреннего использования операционной системой.</span><span class="sxs-lookup"><span data-stu-id="f18a0-190">Individual members of the structure are reserved for internal use by the operating system.</span></span>

<span data-ttu-id="f18a0-191">Вместо этого используйте функцию [**CryptGenRandom**](/windows/desktop/api/wincrypt/nf-wincrypt-cryptgenrandom) , чтобы создать криптографически случайные данные.</span><span class="sxs-lookup"><span data-stu-id="f18a0-191">Use the [**CryptGenRandom**](/windows/desktop/api/wincrypt/nf-wincrypt-cryptgenrandom) function instead to generate cryptographically random data.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="f18a0-192">*Системинформатионленгс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="f18a0-192">*SystemInformationLength* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f18a0-193">Размер буфера, на который указывает параметр *SystemInformation* в байтах.</span><span class="sxs-lookup"><span data-stu-id="f18a0-193">The size of the buffer pointed to by the *SystemInformation* parameter, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="f18a0-194">*Ретурнленгс* \[ out, необязательно\]</span><span class="sxs-lookup"><span data-stu-id="f18a0-194">*ReturnLength* \[out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="f18a0-195">Необязательный указатель на расположение, в котором функция записывает фактический размер запрашиваемой информации.</span><span class="sxs-lookup"><span data-stu-id="f18a0-195">An optional pointer to a location where the function writes the actual size of the information requested.</span></span> <span data-ttu-id="f18a0-196">Если этот размер меньше или равен значению параметра *системинформатионленгс* , функция копирует данные в буфер *SystemInformation* . в противном случае он возвращает код ошибки NTSTATUS и возвращает в *ретурнленгс* размер буфера, необходимого для получения запрошенной информации.</span><span class="sxs-lookup"><span data-stu-id="f18a0-196">If that size is less than or equal to the *SystemInformationLength* parameter, the function copies the information into the *SystemInformation* buffer; otherwise, it returns an NTSTATUS error code and returns in *ReturnLength* the size of buffer required to receive the requested information.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f18a0-197">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="f18a0-197">Return value</span></span>

<span data-ttu-id="f18a0-198">Возвращает сообщение об успешном завершении NTSTATUS или код ошибки.</span><span class="sxs-lookup"><span data-stu-id="f18a0-198">Returns an NTSTATUS success or error code.</span></span>

<span data-ttu-id="f18a0-199">Формы и коды ошибок NTSTATUS перечислены в файле заголовка NTSTATUS. h, доступном в наборе DDK, и описаны в документации по DDK.</span><span class="sxs-lookup"><span data-stu-id="f18a0-199">The forms and significance of NTSTATUS error codes are listed in the Ntstatus.h header file available in the DDK, and are described in the DDK documentation.</span></span>

## <a name="remarks"></a><span data-ttu-id="f18a0-200">Комментарии</span><span class="sxs-lookup"><span data-stu-id="f18a0-200">Remarks</span></span>

<span data-ttu-id="f18a0-201">Функция **звкуерисистеминформатион** и возвращаемые ею структуры являются внутренними по отношению к операционной системе и могут изменяться от одного выпуска Windows к другому.</span><span class="sxs-lookup"><span data-stu-id="f18a0-201">The **ZwQuerySystemInformation** function and the structures that it returns are internal to the operating system and subject to change from one release of Windows to another.</span></span> <span data-ttu-id="f18a0-202">Чтобы обеспечить совместимость приложения, лучше использовать альтернативные ранее упомянутые функции.</span><span class="sxs-lookup"><span data-stu-id="f18a0-202">To maintain the compatibility of your application, it is better to use the alternate functions previously mentioned instead.</span></span>

<span data-ttu-id="f18a0-203">Если вы используете **звкуерисистеминформатион**, то получите доступ к функции через [динамическую компоновку во время выполнения](/windows/desktop/Dlls/using-run-time-dynamic-linking).</span><span class="sxs-lookup"><span data-stu-id="f18a0-203">If you do use **ZwQuerySystemInformation**, access the function through [run-time dynamic linking](/windows/desktop/Dlls/using-run-time-dynamic-linking).</span></span> <span data-ttu-id="f18a0-204">Это дает коду возможность корректно реагировать, если функция была изменена или удалена из операционной системы.</span><span class="sxs-lookup"><span data-stu-id="f18a0-204">This gives your code an opportunity to respond gracefully if the function has been changed or removed from the operating system.</span></span> <span data-ttu-id="f18a0-205">Однако изменения сигнатуры могут быть недоступны для обнаружения.</span><span class="sxs-lookup"><span data-stu-id="f18a0-205">Signature changes, however, may not be detectable.</span></span>

<span data-ttu-id="f18a0-206">Эта функция не имеет связанной библиотеки импорта.</span><span class="sxs-lookup"><span data-stu-id="f18a0-206">This function has no associated import library.</span></span> <span data-ttu-id="f18a0-207">Для динамической привязки к Ntdll.dll необходимо использовать функции [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) и [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="f18a0-207">You must use the [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) functions to dynamically link to Ntdll.dll.</span></span>

## <a name="requirements"></a><span data-ttu-id="f18a0-208">Требования</span><span class="sxs-lookup"><span data-stu-id="f18a0-208">Requirements</span></span>



| <span data-ttu-id="f18a0-209">Требование</span><span class="sxs-lookup"><span data-stu-id="f18a0-209">Requirement</span></span> | <span data-ttu-id="f18a0-210">Значение</span><span class="sxs-lookup"><span data-stu-id="f18a0-210">Value</span></span> |
|----------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="f18a0-211">DLL</span><span class="sxs-lookup"><span data-stu-id="f18a0-211">DLL</span></span><br/> | <dl> <span data-ttu-id="f18a0-212"><dt>Ntdll.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f18a0-212"><dt>Ntdll.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f18a0-213">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f18a0-213">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f18a0-214">**жетсистеминфо**</span><span class="sxs-lookup"><span data-stu-id="f18a0-214">**GetSystemInfo**</span></span>](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getsysteminfo)
</dt> <dt>

[<span data-ttu-id="f18a0-215">**жетпроцесшандлекаунт**</span><span class="sxs-lookup"><span data-stu-id="f18a0-215">**GetProcessHandleCount**</span></span>](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-getprocesshandlecount)
</dt> <dt>

[<span data-ttu-id="f18a0-216">**жетпроцессмеморинфо**</span><span class="sxs-lookup"><span data-stu-id="f18a0-216">**GetProcessMemoryInfo**</span></span>](/windows/desktop/api/psapi/nf-psapi-getprocessmemoryinfo)
</dt> <dt>

[<span data-ttu-id="f18a0-217">**жетсистемтимес**</span><span class="sxs-lookup"><span data-stu-id="f18a0-217">**GetSystemTimes**</span></span>](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getsystemtimes)
</dt> <dt>

[<span data-ttu-id="f18a0-218">**жетсистемрегистрикуота**</span><span class="sxs-lookup"><span data-stu-id="f18a0-218">**GetSystemRegistryQuota**</span></span>](/windows/desktop/api/Winbase/nf-winbase-getsystemregistryquota)
</dt> </dl>

 

