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
# <a name="zwquerysysteminformation-function"></a>Функция Звкуерисистеминформатион

\[**Звкуерисистеминформатион** больше не доступен для использования в Windows 8. Вместо этого используйте альтернативные функции, перечисленные в этом разделе.\]

Извлекает указанные сведения о системе.

## <a name="syntax"></a>Синтаксис


```C++
NTSTATUS WINAPI ZwQuerySystemInformation(
  _In_      SYSTEM_INFORMATION_CLASS SystemInformationClass,
  _Inout_   PVOID                    SystemInformation,
  _In_      ULONG                    SystemInformationLength,
  _Out_opt_ PULONG                   ReturnLength
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Системинформатионкласс* \[ окне\]
</dt> <dd>

Тип системных сведений для извлечения. Этот параметр может принимать одно из следующих значений из типа перечисления **\_ \_ класс системных сведений** .

<dt>

<span id="SystemBasicInformation"></span><span id="systembasicinformation"></span><span id="SYSTEMBASICINFORMATION"></span>

<span id="SystemBasicInformation"></span><span id="systembasicinformation"></span><span id="SYSTEMBASICINFORMATION"></span>**систембасиЦинформатион**


</dt> <dd>

Количество процессоров в системе в **\_ базовой \_ информационной структуре системы** . Вместо этого используйте функцию [**жетсистеминфо**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getsysteminfo) .

</dd> <dt>

<span id="SystemPerformanceInformation"></span><span id="systemperformanceinformation"></span><span id="SYSTEMPERFORMANCEINFORMATION"></span>

<span id="SystemPerformanceInformation"></span><span id="systemperformanceinformation"></span><span id="SYSTEMPERFORMANCEINFORMATION"></span>**системперформанцеинформатион**


</dt> <dd>

Структура **\_ \_ сведений о производительности** непрозрачной системы, которую можно использовать для создания непредсказуемого начального значения генератора случайных чисел. Вместо этого используйте функцию [**CryptGenRandom**](/windows/desktop/api/wincrypt/nf-wincrypt-cryptgenrandom) .

</dd> <dt>

<span id="SystemTimeOfDayInformation"></span><span id="systemtimeofdayinformation"></span><span id="SYSTEMTIMEOFDAYINFORMATION"></span>

<span id="SystemTimeOfDayInformation"></span><span id="systemtimeofdayinformation"></span><span id="SYSTEMTIMEOFDAYINFORMATION"></span>**системтимеофдайинформатион**


</dt> <dd>

Структура **\_ \_ сведений о** непрозрачной системе, которую можно использовать для создания непредсказуемого начального значения для генератора случайных чисел. Вместо этого используйте функцию [**CryptGenRandom**](/windows/desktop/api/wincrypt/nf-wincrypt-cryptgenrandom) .

</dd> <dt>

<span id="SystemProcessInformation"></span><span id="systemprocessinformation"></span><span id="SYSTEMPROCESSINFORMATION"></span>

<span id="SystemProcessInformation"></span><span id="systemprocessinformation"></span><span id="SYSTEMPROCESSINFORMATION"></span>**системпроцессинформатион**


</dt> <dd>

Массив структур **\_ \_ сведений о системных процессах** , по одному для каждого процесса, выполняемого в системе.

Эти структуры содержат сведения об использовании ресурсов каждым процессом, включая количество дескрипторов, используемых процессом, пиковое использование файлов страниц и количество страниц памяти, выделенных процессом.

</dd> <dt>

<span id="SystemProcessorPerformanceInformation"></span><span id="systemprocessorperformanceinformation"></span><span id="SYSTEMPROCESSORPERFORMANCEINFORMATION"></span>

<span id="SystemProcessorPerformanceInformation"></span><span id="systemprocessorperformanceinformation"></span><span id="SYSTEMPROCESSORPERFORMANCEINFORMATION"></span>**системпроцессорперформанцеинформатион**


</dt> <dd>

Массив структур **\_ \_ \_ сведений о производительности системного процессора** , по одному для каждого процессора, установленного в системе.

</dd> <dt>

<span id="SystemInterruptInformation"></span><span id="systeminterruptinformation"></span><span id="SYSTEMINTERRUPTINFORMATION"></span>

<span id="SystemInterruptInformation"></span><span id="systeminterruptinformation"></span><span id="SYSTEMINTERRUPTINFORMATION"></span>**системинтерруптинформатион**


</dt> <dd>

Структура **\_ \_ информации о непрозрачном системном прерывании** , которую можно использовать для создания непредсказуемого начального значения генератора случайных чисел. Вместо этого используйте функцию [**CryptGenRandom**](/windows/desktop/api/wincrypt/nf-wincrypt-cryptgenrandom) .

</dd> <dt>

<span id="SystemExceptionInformation"></span><span id="systemexceptioninformation"></span><span id="SYSTEMEXCEPTIONINFORMATION"></span>

<span id="SystemExceptionInformation"></span><span id="systemexceptioninformation"></span><span id="SYSTEMEXCEPTIONINFORMATION"></span>**системексцептионинформатион**


</dt> <dd>

Структура **\_ \_ сведений о непрозрачных системных исключениях** , которую можно использовать для создания непредсказуемого начального значения генератора случайных чисел. Вместо этого используйте функцию [**CryptGenRandom**](/windows/desktop/api/wincrypt/nf-wincrypt-cryptgenrandom) .

</dd> <dt>

<span id="SystemRegistryQuotaInformation"></span><span id="systemregistryquotainformation"></span><span id="SYSTEMREGISTRYQUOTAINFORMATION"></span>

<span id="SystemRegistryQuotaInformation"></span><span id="systemregistryquotainformation"></span><span id="SYSTEMREGISTRYQUOTAINFORMATION"></span>**системрегистрикуотаинформатион**


</dt> <dd>

Структура **\_ \_ \_ сведений о квотах системного реестра** .

</dd> <dt>

<span id="SystemLookasideInformation"></span><span id="systemlookasideinformation"></span><span id="SYSTEMLOOKASIDEINFORMATION"></span>

<span id="SystemLookasideInformation"></span><span id="systemlookasideinformation"></span><span id="SYSTEMLOOKASIDEINFORMATION"></span>**системлукасидеинформатион**


</dt> <dd>

Структура информации непрозрачного **\_ \_ резерва системы** , которую можно использовать для создания непредсказуемого начального значения генератора случайных чисел. Вместо этого используйте функцию [**CryptGenRandom**](/windows/desktop/api/wincrypt/nf-wincrypt-cryptgenrandom) .

</dd> </dl> </dd> <dt>

*SystemInformation* \[ в, out\]
</dt> <dd>

Указатель на буфер, который получает запрошенную информацию. Размер и структура этих сведений зависят от значения параметра *системинформатионкласс* , как показано в следующей таблице.

<dt>

<span id="SYSTEM_BASIC_INFORMATION"></span><span id="system_basic_information"></span>

<span id="SYSTEM_BASIC_INFORMATION"></span><span id="system_basic_information"></span>**\_основные \_ сведения о системе**


</dt> <dd>

Если параметр *системинформатионкласс* имеет значение **систембасиЦинформатион**, буфер, на который указывает параметр *SystemInformation* , должен быть достаточно большим, чтобы вместить одну **системную \_ базовую структуру \_ информации** со следующим макетом:

``` syntax
typedef struct _SYSTEM_BASIC_INFORMATION {
    BYTE Reserved1[24];
    PVOID Reserved2[4];
    CCHAR NumberOfProcessors;
} SYSTEM_BASIC_INFORMATION;
```

Член **NumberOfProcessors** содержит количество процессоров, имеющихся в системе. Вместо этого используйте [**жетсистеминфо**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getsysteminfo) для получения этих сведений.

Другие члены структуры зарезервированы для внутреннего использования операционной системой.

</dd> <dt>

<span id="SYSTEM_PERFORMANCE_INFORMATION"></span><span id="system_performance_information"></span>

<span id="SYSTEM_PERFORMANCE_INFORMATION"></span><span id="system_performance_information"></span>**\_ \_ сведения о производительности системы**


</dt> <dd>

Если параметр *системинформатионкласс* имеет значение **системперформанцеинформатион**, буфер, на который указывает параметр *SystemInformation* , должен быть достаточно большим, чтобы вместить непрозрачную структуру **\_ \_ сведений о производительности системы** для использования при формировании непредсказуемого начального значения генератора случайных чисел. Для этой цели структура имеет следующий макет:

``` syntax
typedef struct _SYSTEM_PERFORMANCE_INFORMATION {
    BYTE Reserved1[312];
} SYSTEM_PERFORMANCE_INFORMATION;
```

Отдельные члены структуры зарезервированы для внутреннего использования операционной системой.

Вместо этого используйте функцию [**CryptGenRandom**](/windows/desktop/api/wincrypt/nf-wincrypt-cryptgenrandom) , чтобы создать криптографически случайные данные.

</dd> <dt>

<span id="SYSTEM_TIMEOFDAY_INFORMATION"></span><span id="system_timeofday_information"></span>

<span id="SYSTEM_TIMEOFDAY_INFORMATION"></span><span id="system_timeofday_information"></span>**\_ \_ сведения о TIMEOFDAY системы**


</dt> <dd>

Если параметр *системинформатионкласс* имеет значение **системтимеофдайинформатион**, буфер, на который указывает параметр *SystemInformation* , должен быть достаточно большим, чтобы вместить непрозрачную структуру **\_ \_ сведений о TIMEOFDAY системы** для использования при формировании непредсказуемого начального значения для генератора случайных чисел. Для этой цели структура имеет следующий макет:

``` syntax
typedef struct _SYSTEM_TIMEOFDAY_INFORMATION {
    BYTE Reserved1[48];
} SYSTEM_TIMEOFDAY_INFORMATION;
```

Отдельные члены структуры зарезервированы для внутреннего использования операционной системой.

Вместо этого используйте функцию [**CryptGenRandom**](/windows/desktop/api/wincrypt/nf-wincrypt-cryptgenrandom) , чтобы создать криптографически случайные данные.

</dd> <dt>

<span id="SYSTEM_PROCESS_INFORMATION"></span><span id="system_process_information"></span>

<span id="SYSTEM_PROCESS_INFORMATION"></span><span id="system_process_information"></span>**\_сведения о системных процессах \_**


</dt> <dd>

Если параметр *системинформатионкласс* имеет значение **системпроцессинформатион**, буфер, на который указывает параметр *SystemInformation* , должен быть достаточно большим, чтобы вместить массив, содержащий столько структур **\_ \_ сведений о системных процессах** , сколько запущенных в системе процессов. Каждая структура имеет следующий макет:

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

Элемент **NumberOfThreads** содержит общее число выполняющихся в данный момент потоков в процессе.

Элемент **HandleCount** содержит общее количество дескрипторов, используемых рассматриваемым процессом; Используйте [**жетпроцесшандлекаунт**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-getprocesshandlecount) для получения этих сведений.

Элемент **пеакпажефилеусаже** содержит максимальное число байтов хранилища файлов страниц, используемое процессом, а член **приватепажекаунт** содержит количество страниц памяти, выделенных для использования этим процессом.

Эти сведения также можно получить с помощью функции [**жетпроцессмеморинфо**](/windows/desktop/api/psapi/nf-psapi-getprocessmemoryinfo) или класса [**\_ процесса Win32**](/windows/desktop/CIMWin32Prov/win32-process) .

Другие члены структуры зарезервированы для внутреннего использования операционной системой.

</dd> <dt>

<span id="SYSTEM_PROCESSOR_PERFORMANCE_INFORMATION"></span><span id="system_processor_performance_information"></span>

<span id="SYSTEM_PROCESSOR_PERFORMANCE_INFORMATION"></span><span id="system_processor_performance_information"></span>**\_ \_ сведения о производительности процессора системы \_**


</dt> <dd>

Если параметр *системинформатионкласс* имеет значение **системпроцессорперформанцеинформатион**, буфер, на который указывает параметр *SystemInformation* , должен быть достаточно большим, чтобы вместить массив, содержащий столько структур **\_ \_ сведений о системных процессах** , сколько процессоров (ЦП) установлено в системе. Каждая структура имеет следующий макет:

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

Элемент **идлетиме** содержит период бездействия системы в 1/100ths в наносекундных.

Элемент **кернелтиме** содержит количество времени, которое система потратила на выполнение в режиме ядра (включая все потоки во всех процессах, на всех процессорах), в 1/100ths в наносекундных.

Элемент **усертиме** содержит количество времени, которое система потратила на выполнение в пользовательском режиме (включая все потоки во всех процессах, на всех процессорах), в 1/100ths в наносекундных.

Вместо этого используйте [**жетсистемтимес**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getsystemtimes) для получения этих сведений.

</dd> <dt>

<span id="SYSTEM_INTERRUPT_INFORMATION"></span><span id="system_interrupt_information"></span>

<span id="SYSTEM_INTERRUPT_INFORMATION"></span><span id="system_interrupt_information"></span>**\_сведения о прерывании системы \_**


</dt> <dd>

Если параметр *системинформатионкласс* имеет значение **системинтерруптинформатион**, буфер, на который указывает параметр *SystemInformation* , должен быть достаточно большим, чтобы вместить массив, содержащий множество структур непрозрачных **системных \_ прерываний \_** , так как в системе установлены процессоры (ЦП). Каждая структура или массив в целом может использоваться для создания непредсказуемого начального значения генератора случайных чисел. Для этой цели структура имеет следующий макет:

``` syntax
typedef struct _SYSTEM_INTERRUPT_INFORMATION {
    BYTE Reserved1[24];
} SYSTEM_INTERRUPT_INFORMATION;
```

Отдельные члены структуры зарезервированы для внутреннего использования операционной системой.

Вместо этого используйте функцию [**CryptGenRandom**](/windows/desktop/api/wincrypt/nf-wincrypt-cryptgenrandom) , чтобы создать криптографически случайные данные.

</dd> <dt>

<span id="SYSTEM_EXCEPTION_INFORMATION"></span><span id="system_exception_information"></span>

<span id="SYSTEM_EXCEPTION_INFORMATION"></span><span id="system_exception_information"></span>**\_сведения об системном исключении \_**


</dt> <dd>

Если параметр *системинформатионкласс* имеет значение **системексцептионинформатион**, буфер, на который указывает параметр *SystemInformation* , должен быть достаточно большим, чтобы вместить непрозрачную структуру **\_ \_ информации об исключениях системы** для использования при формировании непредсказуемого начального значения генератора случайных чисел. Для этой цели структура имеет следующий макет:

``` syntax
typedef struct _SYSTEM_EXCEPTION_INFORMATION {
    BYTE Reserved1[16];
} SYSTEM_EXCEPTION_INFORMATION;
```

Отдельные члены структуры зарезервированы для внутреннего использования операционной системой.

Вместо этого используйте функцию [**CryptGenRandom**](/windows/desktop/api/wincrypt/nf-wincrypt-cryptgenrandom) , чтобы создать криптографически случайные данные.

</dd> <dt>

<span id="SYSTEM_REGISTRY_QUOTA_INFORMATION"></span><span id="system_registry_quota_information"></span>

<span id="SYSTEM_REGISTRY_QUOTA_INFORMATION"></span><span id="system_registry_quota_information"></span>**\_ \_ сведения о квотах системного реестра \_**


</dt> <dd>

Если параметр *системинформатионкласс* имеет значение **системрегистрикуотаинформатион**, буфер, на который указывает параметр *SystemInformation* , должен быть достаточно большим, чтобы вместить одну **структуру \_ \_ \_ сведений о квотах системного реестра** со следующим макетом:

``` syntax
typedef struct _SYSTEM_REGISTRY_QUOTA_INFORMATION {
    ULONG RegistryQuotaAllowed;
    ULONG RegistryQuotaUsed;
    PVOID Reserved1;
} SYSTEM_REGISTRY_QUOTA_INFORMATION;
```

Элемент **регистрикуотаалловед** содержит максимальный размер (в байтах), который может достичь реестр в системе.

Элемент **регистрикуотаусед** содержит текущий размер реестра в байтах.

Вместо этого используйте [**жетсистемрегистрикуота**](/windows/desktop/api/Winbase/nf-winbase-getsystemregistryquota) для получения этих сведений.

Другой член структуры зарезервирован для внутреннего использования операционной системой.

</dd> <dt>

<span id="SYSTEM_LOOKASIDE_INFORMATION"></span><span id="system_lookaside_information"></span>

<span id="SYSTEM_LOOKASIDE_INFORMATION"></span><span id="system_lookaside_information"></span>**\_сведения о резерве системы \_**


</dt> <dd>

Если параметр *системинформатионкласс* имеет значение **системлукасидеинформатион**, буфер, на который указывает параметр *SystemInformation* , должен быть достаточно большим, чтобы вместить непрозрачную структуру **\_ \_ информации о резерве системы** для использования при формировании непредсказуемого начального значения генератора случайных чисел. Для этой цели структура имеет следующий макет:

``` syntax
typedef struct _SYSTEM_LOOKASIDE_INFORMATION {
    BYTE Reserved1[32];
} SYSTEM_LOOKASIDE_INFORMATION;
```

Отдельные члены структуры зарезервированы для внутреннего использования операционной системой.

Вместо этого используйте функцию [**CryptGenRandom**](/windows/desktop/api/wincrypt/nf-wincrypt-cryptgenrandom) , чтобы создать криптографически случайные данные.

</dd> </dl> </dd> <dt>

*Системинформатионленгс* \[ окне\]
</dt> <dd>

Размер буфера, на который указывает параметр *SystemInformation* в байтах.

</dd> <dt>

*Ретурнленгс* \[ out, необязательно\]
</dt> <dd>

Необязательный указатель на расположение, в котором функция записывает фактический размер запрашиваемой информации. Если этот размер меньше или равен значению параметра *системинформатионленгс* , функция копирует данные в буфер *SystemInformation* . в противном случае он возвращает код ошибки NTSTATUS и возвращает в *ретурнленгс* размер буфера, необходимого для получения запрошенной информации.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает сообщение об успешном завершении NTSTATUS или код ошибки.

Формы и коды ошибок NTSTATUS перечислены в файле заголовка NTSTATUS. h, доступном в наборе DDK, и описаны в документации по DDK.

## <a name="remarks"></a>Комментарии

Функция **звкуерисистеминформатион** и возвращаемые ею структуры являются внутренними по отношению к операционной системе и могут изменяться от одного выпуска Windows к другому. Чтобы обеспечить совместимость приложения, лучше использовать альтернативные ранее упомянутые функции.

Если вы используете **звкуерисистеминформатион**, то получите доступ к функции через [динамическую компоновку во время выполнения](/windows/desktop/Dlls/using-run-time-dynamic-linking). Это дает коду возможность корректно реагировать, если функция была изменена или удалена из операционной системы. Однако изменения сигнатуры могут быть недоступны для обнаружения.

Эта функция не имеет связанной библиотеки импорта. Для динамической привязки к Ntdll.dll необходимо использовать функции [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) и [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) .

## <a name="requirements"></a>Требования



| Требование | Значение |
|----------------|--------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Ntdll.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**жетсистеминфо**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getsysteminfo)
</dt> <dt>

[**жетпроцесшандлекаунт**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-getprocesshandlecount)
</dt> <dt>

[**жетпроцессмеморинфо**](/windows/desktop/api/psapi/nf-psapi-getprocessmemoryinfo)
</dt> <dt>

[**жетсистемтимес**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getsystemtimes)
</dt> <dt>

[**жетсистемрегистрикуота**](/windows/desktop/api/Winbase/nf-winbase-getsystemregistryquota)
</dt> </dl>

 

