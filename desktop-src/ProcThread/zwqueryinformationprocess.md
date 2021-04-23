---
description: Извлекает сведения об указанном процессе.
ms.assetid: c36c023f-7f9a-4ba5-a41f-f2f755a24eb6
title: Функция Звкуеринформатионпроцесс
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ZwQueryInformationProcess
api_type:
- DllExport
api_location:
- Ntdll.dll
- ntoskrnl.exe
ms.openlocfilehash: 30207c8d3d54c54f77194b542e10e9fee94e055a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105673726"
---
# <a name="zwqueryinformationprocess-function"></a><span data-ttu-id="08c32-103">Функция Звкуеринформатионпроцесс</span><span class="sxs-lookup"><span data-stu-id="08c32-103">ZwQueryInformationProcess function</span></span>

<span data-ttu-id="08c32-104">\[**Звкуеринформатионпроцесс** может быть изменен или недоступен в будущих версиях Windows.</span><span class="sxs-lookup"><span data-stu-id="08c32-104">\[**ZwQueryInformationProcess** may be altered or unavailable in future versions of Windows.</span></span> <span data-ttu-id="08c32-105">Приложения должны использовать альтернативные функции, перечисленные в этом разделе.\]</span><span class="sxs-lookup"><span data-stu-id="08c32-105">Applications should use the alternate functions listed in this topic.\]</span></span>

<span data-ttu-id="08c32-106">Извлекает сведения об указанном процессе.</span><span class="sxs-lookup"><span data-stu-id="08c32-106">Retrieves information about the specified process.</span></span>

## <a name="syntax"></a><span data-ttu-id="08c32-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="08c32-107">Syntax</span></span>


```C++
NTSTATUS WINAPI ZwQueryInformationProcess(
  _In_      HANDLE           ProcessHandle,
  _In_      PROCESSINFOCLASS ProcessInformationClass,
  _Out_     PVOID            ProcessInformation,
  _In_      ULONG            ProcessInformationLength,
  _Out_opt_ PULONG           ReturnLength
);
```



## <a name="parameters"></a><span data-ttu-id="08c32-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="08c32-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="08c32-109">*Процесшандле* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="08c32-109">*ProcessHandle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="08c32-110">Описатель процесса, для которого извлекаются сведения.</span><span class="sxs-lookup"><span data-stu-id="08c32-110">A handle to the process for which information is to be retrieved.</span></span>

</dd> <dt>

<span data-ttu-id="08c32-111">*Процессинформатионкласс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="08c32-111">*ProcessInformationClass* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="08c32-112">Тип извлекаемых сведений о процессе.</span><span class="sxs-lookup"><span data-stu-id="08c32-112">The type of process information to be retrieved.</span></span> <span data-ttu-id="08c32-113">Этот параметр может принимать одно из следующих значений перечисления **процессинфокласс** .</span><span class="sxs-lookup"><span data-stu-id="08c32-113">This parameter can be one of the following values from the **PROCESSINFOCLASS** enumeration.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="08c32-114">Значение</span><span class="sxs-lookup"><span data-stu-id="08c32-114">Value</span></span></th>
<th><span data-ttu-id="08c32-115">Значение</span><span class="sxs-lookup"><span data-stu-id="08c32-115">Meaning</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span id="ProcessBasicInformation"></span><span id="processbasicinformation"></span><span id="PROCESSBASICINFORMATION"></span><dl> <span data-ttu-id="08c32-116"><dt><strong>ПроцессбасиЦинформатион</strong></dt> <dt>0</dt> </span><span class="sxs-lookup"><span data-stu-id="08c32-116"><dt><strong>ProcessBasicInformation</strong></dt> <dt>0</dt> </span></span></dl></td>
<td><span data-ttu-id="08c32-117">Получает указатель на структуру ПЕБ, которую можно использовать, чтобы определить, выполняется ли отладка указанного процесса, и уникальное значение, используемое системой для определения указанного процесса.</span><span class="sxs-lookup"><span data-stu-id="08c32-117">Retrieves a pointer to a PEB structure that can be used to determine whether the specified process is being debugged, and a unique value used by the system to identify the specified process.</span></span> <br/> <span data-ttu-id="08c32-118">Для получения этих сведений лучше использовать функции <a href="/windows/desktop/api/debugapi/nf-debugapi-checkremotedebuggerpresent"><strong>чеккремотедебугжерпресент</strong></a> и <a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-getprocessid"><strong>GetProcessId</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="08c32-118">It is best to use the <a href="/windows/desktop/api/debugapi/nf-debugapi-checkremotedebuggerpresent"><strong>CheckRemoteDebuggerPresent</strong></a> and <a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-getprocessid"><strong>GetProcessId</strong></a> functions to obtain this information.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ProcessDebugPort"></span><span id="processdebugport"></span><span id="PROCESSDEBUGPORT"></span><dl> <span data-ttu-id="08c32-119"><dt><strong>Процессдебугпорт</strong></dt> <dt>7</dt> </span><span class="sxs-lookup"><span data-stu-id="08c32-119"><dt><strong>ProcessDebugPort</strong></dt> <dt>7</dt> </span></span></dl></td>
<td><span data-ttu-id="08c32-120">Извлекает <strong>DWORD_PTR</strong> значение, которое является номером порта отладчика для процесса.</span><span class="sxs-lookup"><span data-stu-id="08c32-120">Retrieves a <strong>DWORD_PTR</strong> value that is the port number of the debugger for the process.</span></span> <span data-ttu-id="08c32-121">Ненулевое значение указывает, что процесс выполняется под управлением отладчика Ring 3.</span><span class="sxs-lookup"><span data-stu-id="08c32-121">A nonzero value indicates that the process is being run under the control of a ring 3 debugger.</span></span><br/> <span data-ttu-id="08c32-122">Лучше использовать функцию <a href="/windows/desktop/api/debugapi/nf-debugapi-checkremotedebuggerpresent"><strong>чеккремотедебугжерпресент</strong></a> или <a href="/windows/desktop/api/debugapi/nf-debugapi-isdebuggerpresent"><strong>исдебугжерпресент</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="08c32-122">It is best to use the <a href="/windows/desktop/api/debugapi/nf-debugapi-checkremotedebuggerpresent"><strong>CheckRemoteDebuggerPresent</strong></a> or <a href="/windows/desktop/api/debugapi/nf-debugapi-isdebuggerpresent"><strong>IsDebuggerPresent</strong></a> function.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ProcessWow64Information"></span><span id="processwow64information"></span><span id="PROCESSWOW64INFORMATION"></span><dl> <span data-ttu-id="08c32-123"><dt><strong>ProcessWow64Information</strong></dt> <dt>26</dt> </span><span class="sxs-lookup"><span data-stu-id="08c32-123"><dt><strong>ProcessWow64Information</strong></dt> <dt>26</dt> </span></span></dl></td>
<td><span data-ttu-id="08c32-124">Определяет, выполняется ли процесс в среде WOW64 (WOW64 — эмулятор x86, позволяющий приложениям на основе Win32 работать в 64-разрядной версии Windows).</span><span class="sxs-lookup"><span data-stu-id="08c32-124">Determines whether the process is running in the WOW64 environment (WOW64 is the x86 emulator that allows Win32-based applications to run on 64-bit Windows).</span></span><br/> <span data-ttu-id="08c32-125">Для получения этих сведений лучше использовать функцию <a href="/windows/desktop/api/wow64apiset/nf-wow64apiset-iswow64process"><strong>IsWow64Process</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="08c32-125">It is best to use the <a href="/windows/desktop/api/wow64apiset/nf-wow64apiset-iswow64process"><strong>IsWow64Process</strong></a> function to obtain this information.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ProcessImageFileName"></span><span id="processimagefilename"></span><span id="PROCESSIMAGEFILENAME"></span><dl> <span data-ttu-id="08c32-126"><dt><strong>Процессимажефиленаме</strong></dt> <dt>27</dt> </span><span class="sxs-lookup"><span data-stu-id="08c32-126"><dt><strong>ProcessImageFileName</strong></dt> <dt>27</dt> </span></span></dl></td>
<td><span data-ttu-id="08c32-127">Извлекает значение <strong>UNICODE_STRING</strong> , содержащее имя файла изображения для процесса.</span><span class="sxs-lookup"><span data-stu-id="08c32-127">Retrieves a <strong>UNICODE_STRING</strong> value containing the name of the image file for the process.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ProcessBreakOnTermination"></span><span id="processbreakontermination"></span><span id="PROCESSBREAKONTERMINATION"></span><dl> <span data-ttu-id="08c32-128"><dt><strong>Процессбреаконтерминатион</strong></dt> <dt>29</dt> </span><span class="sxs-lookup"><span data-stu-id="08c32-128"><dt><strong>ProcessBreakOnTermination</strong></dt> <dt>29</dt> </span></span></dl></td>
<td><span data-ttu-id="08c32-129">Извлекает значение типа <strong>ulong</strong> , указывающее, считается ли процесс критическим.</span><span class="sxs-lookup"><span data-stu-id="08c32-129">Retrieves a <strong>ULONG</strong> value indicating whether the process is considered critical.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="08c32-130">Это значение можно использовать в Windows XP с пакетом обновления 3 (SP3).</span><span class="sxs-lookup"><span data-stu-id="08c32-130">This value can be used starting in Windows XP with SP3.</span></span> <span data-ttu-id="08c32-131">Начиная с Windows 8.1 вместо него следует использовать <a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-isprocesscritical"><strong>испроцесскритикал</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="08c32-131">Starting in Windows 8.1, <a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-isprocesscritical"><strong>IsProcessCritical</strong></a> should be used instead.</span></span>
</blockquote>
<br/></td>
</tr><tr class="even">
<td><span id="ProcessProtectionInformation"></span><span id="processprotectioninformation"></span><span id="PROCESSPROTECTIONINFORMATION"></span><dl> <span data-ttu-id="08c32-132"><dt><strong>Процесспротектионинформатион</strong></dt> <dt>61</dt> </span><span class="sxs-lookup"><span data-stu-id="08c32-132"><dt><strong>ProcessProtectionInformation</strong></dt> <dt>61</dt> </span></span></dl></td>
<td><span data-ttu-id="08c32-133">Извлекает значение БАЙТа, указывающее тип защищенного процесса и подписанного процесса.</span><span class="sxs-lookup"><span data-stu-id="08c32-133">Retrieves a BYTE value indicating the type of protected process and the protected process signer.</span></span><br/></td>
</tr>
</tbody>
</table>



 

</dd> <dt>

<span data-ttu-id="08c32-134">*Процессинформатион* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="08c32-134">*ProcessInformation* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="08c32-135">Указатель на буфер, предоставленный вызывающим приложением, в который функция записывает запрошенные сведения.</span><span class="sxs-lookup"><span data-stu-id="08c32-135">A pointer to a buffer supplied by the calling application into which the function writes the requested information.</span></span> <span data-ttu-id="08c32-136">Размер записываемой информации зависит от значения параметра *процессинформатионкласс* :</span><span class="sxs-lookup"><span data-stu-id="08c32-136">The size of the information written varies depending on the value of the *ProcessInformationClass* parameter:</span></span>

<dl> <dt>

<span data-ttu-id="08c32-137"><span id="PROCESS_BASIC_INFORMATION"></span><span id="process_basic_information"></span>\_основные \_ сведения об обработке</span><span class="sxs-lookup"><span data-stu-id="08c32-137"><span id="PROCESS_BASIC_INFORMATION"></span><span id="process_basic_information"></span>PROCESS\_BASIC\_INFORMATION</span></span>
</dt> <dd>

<span data-ttu-id="08c32-138">Если параметр *процессинформатионкласс* имеет значение **процессбасиЦинформатион**, буфер, на который указывает параметр *процессинформатион* , должен быть достаточно большим, чтобы вместить одну **\_ базовую структуру \_ сведений** , имеющую следующий макет:</span><span class="sxs-lookup"><span data-stu-id="08c32-138">When the *ProcessInformationClass* parameter is **ProcessBasicInformation**, the buffer pointed to by the *ProcessInformation* parameter should be large enough to hold a single **PROCESS\_BASIC\_INFORMATION** structure having the following layout:</span></span>

``` syntax
typedef struct _PROCESS_BASIC_INFORMATION {
    PVOID Reserved1;
    PPEB PebBaseAddress;
    PVOID Reserved2[2];
    ULONG_PTR UniqueProcessId;
    PVOID Reserved3;
} PROCESS_BASIC_INFORMATION;
```

<span data-ttu-id="08c32-139">Элемент **уникуепроцессид** указывает на уникальный идентификатор системы для этого процесса.</span><span class="sxs-lookup"><span data-stu-id="08c32-139">The **UniqueProcessId** member points to the system's unique identifier for this process.</span></span> <span data-ttu-id="08c32-140">Для получения этих сведений лучше использовать функцию [**GetProcessId**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getprocessid) .</span><span class="sxs-lookup"><span data-stu-id="08c32-140">It is best to use the [**GetProcessId**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getprocessid) function to retrieve this information.</span></span>

<span data-ttu-id="08c32-141">Элемент **пеббасеаддресс** указывает на структуру [**пеб**](/windows/desktop/api/Winternl/ns-winternl-peb) .</span><span class="sxs-lookup"><span data-stu-id="08c32-141">The **PebBaseAddress** member points to a [**PEB**](/windows/desktop/api/Winternl/ns-winternl-peb) structure.</span></span>

<span data-ttu-id="08c32-142">Другие члены этой структуры зарезервированы для внутреннего использования операционной системой.</span><span class="sxs-lookup"><span data-stu-id="08c32-142">The other members of this structure are reserved for internal use by the operating system.</span></span>

</dd> <dt>

<span data-ttu-id="08c32-143"><span id="ULONG_PTR"></span><span id="ulong_ptr"></span>ULONG- \_ ptr</span><span class="sxs-lookup"><span data-stu-id="08c32-143"><span id="ULONG_PTR"></span><span id="ulong_ptr"></span>ULONG\_PTR</span></span>
</dt> <dd>

<span data-ttu-id="08c32-144">Если параметр *процессинформатионкласс* имеет значение **ProcessWow64Information**, буфер, на который указывает параметр *процессинформатион* , должен быть достаточно большим для хранения записи **\_ типа ulong**.</span><span class="sxs-lookup"><span data-stu-id="08c32-144">When the *ProcessInformationClass* parameter is **ProcessWow64Information**, the buffer pointed to by the *ProcessInformation* parameter should be large enough to hold a **ULONG\_PTR**.</span></span> <span data-ttu-id="08c32-145">Если это значение не равно нулю, процесс выполняется в среде WOW64; в противном случае, если значение равно нулю, процесс не выполняется в среде WOW64.</span><span class="sxs-lookup"><span data-stu-id="08c32-145">If this value is nonzero, the process is running in a WOW64 environment; otherwise, if the value is equal to zero, the process is not running in a WOW64 environment.</span></span>

<span data-ttu-id="08c32-146">Лучше использовать функцию [**IsWow64Process**](/windows/win32/api/wow64apiset/nf-wow64apiset-iswow64process) , чтобы определить, выполняется ли процесс в среде WOW64.</span><span class="sxs-lookup"><span data-stu-id="08c32-146">It is best to use the [**IsWow64Process**](/windows/win32/api/wow64apiset/nf-wow64apiset-iswow64process) function to determine whether a process is running in the WOW64 environment.</span></span>

</dd> <dt>

<span data-ttu-id="08c32-147"><span id="UNICODE_STRING"></span><span id="unicode_string"></span>строка в Юникоде \_</span><span class="sxs-lookup"><span data-stu-id="08c32-147"><span id="UNICODE_STRING"></span><span id="unicode_string"></span>UNICODE\_STRING</span></span>
</dt> <dd>

<span data-ttu-id="08c32-148">Если параметр *процессинформатионкласс* имеет значение **процессимажефиленаме**, буфер, на который указывает параметр *процессинформатион* , должен быть достаточно большим, чтобы вместить **\_ строковую** структуру в Юникоде, а также саму строку.</span><span class="sxs-lookup"><span data-stu-id="08c32-148">When the *ProcessInformationClass* parameter is **ProcessImageFileName**, the buffer pointed to by the *ProcessInformation* parameter should be large enough to hold a **UNICODE\_STRING** structure as well as the string itself.</span></span> <span data-ttu-id="08c32-149">Строка, хранящаяся в элементе **buffer** , является именем файла изображения.</span><span class="sxs-lookup"><span data-stu-id="08c32-149">The string stored in the **Buffer** member is the name of the image file.</span></span>

<span data-ttu-id="08c32-150">Если буфер слишком мал, функция завершается с ошибкой \_ \_ несоответствия длины сведений о состоянии \_ и параметру *ретурнленгс* присваивается требуемый размер буфера.</span><span class="sxs-lookup"><span data-stu-id="08c32-150">If the buffer is too small, the function fails with the STATUS\_INFO\_LENGTH\_MISMATCH error code and the *ReturnLength* parameter is set to the required buffer size.</span></span>

</dd> <dt>

<span data-ttu-id="08c32-151"><span id="PS_PROTECTION"></span><span id="ps_protection"></span>PS_PROTECTION</span><span class="sxs-lookup"><span data-stu-id="08c32-151"><span id="PS_PROTECTION"></span><span id="ps_protection"></span>PS_PROTECTION</span></span>
</dt> <dd>

<span data-ttu-id="08c32-152">Если параметр *процессинформатионкласс* имеет значение **процесспротектионинформатион**, буфер, на который указывает параметр *процессинформатион* , должен быть достаточно большим, чтобы вместить одну структуру **PS_PROTECTION** со следующим макетом:</span><span class="sxs-lookup"><span data-stu-id="08c32-152">When the *ProcessInformationClass* parameter is **ProcessProtectionInformation**, the buffer pointed to by the *ProcessInformation* parameter should be large enough to hold a single **PS_PROTECTION** structure having the following layout:</span></span>

``` syntax
typedef struct _PS_PROTECTION {
    union {
        UCHAR Level;
        struct {
            UCHAR Type   : 3;
            UCHAR Audit  : 1;                  // Reserved
            UCHAR Signer : 4;
        };
    };
} PS_PROTECTION, *PPS_PROTECTION;
```

<span data-ttu-id="08c32-153">Первые 3 бита содержат тип защищенного процесса:</span><span class="sxs-lookup"><span data-stu-id="08c32-153">The first 3 bits contain the type of protected process:</span></span>

``` syntax
typedef enum _PS_PROTECTED_TYPE {
    PsProtectedTypeNone = 0,
    PsProtectedTypeProtectedLight = 1,
    PsProtectedTypeProtected = 2
} PS_PROTECTED_TYPE, *PPS_PROTECTED_TYPE;
```

<span data-ttu-id="08c32-154">Старшие 4 бита содержат подпись защищенного процесса:</span><span class="sxs-lookup"><span data-stu-id="08c32-154">The top 4 bits contain the protected process signer:</span></span>

``` syntax
typedef enum _PS_PROTECTED_SIGNER {
    PsProtectedSignerNone = 0,
    PsProtectedSignerAuthenticode,
    PsProtectedSignerCodeGen,
    PsProtectedSignerAntimalware,
    PsProtectedSignerLsa,
    PsProtectedSignerWindows,
    PsProtectedSignerWinTcb,
    PsProtectedSignerWinSystem,
    PsProtectedSignerApp,
    PsProtectedSignerMax
} PS_PROTECTED_SIGNER, *PPS_PROTECTED_SIGNER;
```

</dd> </dl> </dd> <dt>

<span data-ttu-id="08c32-155">*Процессинформатионленгс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="08c32-155">*ProcessInformationLength* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="08c32-156">Размер буфера, на который указывает параметр *процессинформатион* в байтах.</span><span class="sxs-lookup"><span data-stu-id="08c32-156">The size of the buffer pointed to by the *ProcessInformation* parameter, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="08c32-157">*Ретурнленгс* \[ out, необязательно\]</span><span class="sxs-lookup"><span data-stu-id="08c32-157">*ReturnLength* \[out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="08c32-158">Указатель на переменную, в которой функция возвращает размер запрашиваемой информации.</span><span class="sxs-lookup"><span data-stu-id="08c32-158">A pointer to a variable in which the function returns the size of the requested information.</span></span> <span data-ttu-id="08c32-159">Если функция выполнена успешно, это размер информации, записанной в буфер, на который указывает параметр *процессинформатион* , но если буфер слишком мал, это минимальный размер буфера, необходимого для успешного получения информации.</span><span class="sxs-lookup"><span data-stu-id="08c32-159">If the function was successful, this is the size of the information written to the buffer pointed to by the *ProcessInformation* parameter, but if the buffer was too small, this is the minimum size of buffer needed to receive the information successfully.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="08c32-160">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="08c32-160">Return value</span></span>

<span data-ttu-id="08c32-161">Возвращает сообщение об успешном завершении NTSTATUS или код ошибки.</span><span class="sxs-lookup"><span data-stu-id="08c32-161">Returns an NTSTATUS success or error code.</span></span>

<span data-ttu-id="08c32-162">Формы и коды ошибок NTSTATUS перечислены в файле заголовка NTSTATUS. h, доступном в наборе DDK. они описаны в документации по DDK в разделе Kernel-Mode архитектура драйвера/руководство по проектированию/средства программирования драйверов/регистрация ошибок.</span><span class="sxs-lookup"><span data-stu-id="08c32-162">The forms and significance of NTSTATUS error codes are listed in the Ntstatus.h header file available in the DDK, and are described in the DDK documentation under Kernel-Mode Driver Architecture / Design Guide / Driver Programming Techniques / Logging Errors.</span></span>

## <a name="remarks"></a><span data-ttu-id="08c32-163">Комментарии</span><span class="sxs-lookup"><span data-stu-id="08c32-163">Remarks</span></span>

<span data-ttu-id="08c32-164">Функция **звкуеринформатионпроцесс** и возвращаемые ею структуры являются внутренними по отношению к операционной системе и могут изменяться от одного выпуска Windows к другому.</span><span class="sxs-lookup"><span data-stu-id="08c32-164">The **ZwQueryInformationProcess** function and the structures that it returns are internal to the operating system and subject to change from one release of Windows to another.</span></span> <span data-ttu-id="08c32-165">Чтобы обеспечить совместимость приложения, лучше использовать общие функции, упомянутые в описании параметра *процессинформатионкласс* .</span><span class="sxs-lookup"><span data-stu-id="08c32-165">To maintain the compatibility of your application, it is better to use public functions mentioned in the description of the *ProcessInformationClass* parameter instead.</span></span>

<span data-ttu-id="08c32-166">Если вы используете **звкуеринформатионпроцесс**, то получите доступ к функции через [динамическую компоновку во время выполнения](../dlls/using-run-time-dynamic-linking.md).</span><span class="sxs-lookup"><span data-stu-id="08c32-166">If you do use **ZwQueryInformationProcess**, access the function through [run-time dynamic linking](../dlls/using-run-time-dynamic-linking.md).</span></span> <span data-ttu-id="08c32-167">Это дает коду возможность корректно реагировать, если функция была изменена или удалена из операционной системы.</span><span class="sxs-lookup"><span data-stu-id="08c32-167">This gives your code an opportunity to respond gracefully if the function has been changed or removed from the operating system.</span></span> <span data-ttu-id="08c32-168">Однако изменения сигнатуры могут быть недоступны для обнаружения.</span><span class="sxs-lookup"><span data-stu-id="08c32-168">Signature changes, however, may not be detectable.</span></span>

<span data-ttu-id="08c32-169">Эта функция не имеет связанной библиотеки импорта.</span><span class="sxs-lookup"><span data-stu-id="08c32-169">This function has no associated import library.</span></span> <span data-ttu-id="08c32-170">Для динамической привязки к Ntdll.dll необходимо использовать функции [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) и [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="08c32-170">You must use the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions to dynamically link to Ntdll.dll.</span></span>

## <a name="requirements"></a><span data-ttu-id="08c32-171">Требования</span><span class="sxs-lookup"><span data-stu-id="08c32-171">Requirements</span></span>



| <span data-ttu-id="08c32-172">Требование</span><span class="sxs-lookup"><span data-stu-id="08c32-172">Requirement</span></span> | <span data-ttu-id="08c32-173">Значение</span><span class="sxs-lookup"><span data-stu-id="08c32-173">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="08c32-174">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="08c32-174">Minimum supported client</span></span><br/> | <span data-ttu-id="08c32-175">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="08c32-175">Windows XP \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="08c32-176">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="08c32-176">Minimum supported server</span></span><br/> | <span data-ttu-id="08c32-177">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="08c32-177">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="08c32-178">DLL</span><span class="sxs-lookup"><span data-stu-id="08c32-178">DLL</span></span><br/>                      | <dl> <span data-ttu-id="08c32-179"><dt>Ntdll.dll</dt></span><span class="sxs-lookup"><span data-stu-id="08c32-179"><dt>Ntdll.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="08c32-180">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="08c32-180">See also</span></span>

<dl> <dt>

[<span data-ttu-id="08c32-181">**чеккремотедебугжерпресент**</span><span class="sxs-lookup"><span data-stu-id="08c32-181">**CheckRemoteDebuggerPresent**</span></span>](/windows/win32/api/debugapi/nf-debugapi-checkremotedebuggerpresent)
</dt> <dt>

[<span data-ttu-id="08c32-182">**GetProcessId**</span><span class="sxs-lookup"><span data-stu-id="08c32-182">**GetProcessId**</span></span>](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getprocessid)
</dt> <dt>

[<span data-ttu-id="08c32-183">**исдебугжерпресент**</span><span class="sxs-lookup"><span data-stu-id="08c32-183">**IsDebuggerPresent**</span></span>](/windows/win32/api/debugapi/nf-debugapi-isdebuggerpresent)
</dt> <dt>

[<span data-ttu-id="08c32-184">**IsWow64Process**</span><span class="sxs-lookup"><span data-stu-id="08c32-184">**IsWow64Process**</span></span>](/windows/win32/api/wow64apiset/nf-wow64apiset-iswow64process)
</dt> </dl>

 

 
