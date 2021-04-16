---
description: В Windows 10 появилась новая функция безопасности с именем виртуальный безопасный режим (VSM).
ms.assetid: 58374CC4-593F-4B91-A5E4-85E29C44F8B4
title: Процессы с изолированным пользовательским режимом (ИУМ)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 81a176421174a58abe4ab595bb37ab75434edade
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104558348"
---
# <a name="isolated-user-mode-ium-processes"></a><span data-ttu-id="87f24-103">Процессы с изолированным пользовательским режимом (ИУМ)</span><span class="sxs-lookup"><span data-stu-id="87f24-103">Isolated User Mode (IUM) Processes</span></span>

<span data-ttu-id="87f24-104">В Windows 10 появилась новая функция безопасности с именем виртуальный безопасный режим (VSM).</span><span class="sxs-lookup"><span data-stu-id="87f24-104">Windows 10 introduced a new security feature named Virtual Secure Mode (VSM).</span></span> <span data-ttu-id="87f24-105">VSM использует гипервизор Hyper-V и преобразование адресов второго уровня (SLAT) для создания набора режимов, именуемых виртуальными уровнями доверия (Втлс).</span><span class="sxs-lookup"><span data-stu-id="87f24-105">VSM leverages the Hyper-V Hypervisor and Second Level Address Translation (SLAT) to create a set of modes called Virtual Trust Levels (VTLs).</span></span> <span data-ttu-id="87f24-106">Эта новая архитектура программного обеспечения создает границу безопасности, чтобы предотвратить доступ процессов, выполняющихся в одном VTL, к памяти другого VTL.</span><span class="sxs-lookup"><span data-stu-id="87f24-106">This new software architecture creates a security boundary to prevent processes running in one VTL from accessing the memory of another VTL.</span></span> <span data-ttu-id="87f24-107">Преимуществом этой изоляции является дополнительное устранение уязвимостей ядра при защите ресурсов, таких как хэши паролей и ключи Kerberos.</span><span class="sxs-lookup"><span data-stu-id="87f24-107">The benefit of this isolation includes additional mitigation from kernel exploits while protecting assets such as password hashes and Kerberos keys.</span></span>

<span data-ttu-id="87f24-108">На схеме 1 показана традиционная модель режима ядра и кода пользовательского режима, выполняемых в кольцевых и кольцевых ПРОЦЕССОРах 0 и 3 соответственно.</span><span class="sxs-lookup"><span data-stu-id="87f24-108">Diagram 1 depicts the traditional model of Kernel mode and User mode code running in CPU ring 0 and ring 3, respectively.</span></span> <span data-ttu-id="87f24-109">В этой новой модели код, выполняемый в традиционной модели, выполняется в VTL0 и не может получить доступ к более высоким привилегированным VTL1, где выполняется код в безопасном ядре и изолированном пользовательском режиме (ИУМ).</span><span class="sxs-lookup"><span data-stu-id="87f24-109">In this new model, the code running in the traditional model executes in VTL0 and it cannot access the higher privileged VTL1, where the Secure Kernel and Isolated User Mode (IUM) execute code.</span></span> <span data-ttu-id="87f24-110">Втлс представляют собой иерархические значения, что любой код, выполняемый в VTL1, является более привилегированным, чем код, выполняющийся в VTL0.</span><span class="sxs-lookup"><span data-stu-id="87f24-110">The VTLs are hierarchal meaning any code running in VTL1 is more privileged than code running in VTL0.</span></span>

<span data-ttu-id="87f24-111">Изоляция VTL создается гипервизором Hyper-V, который назначает память во время загрузки с помощью преобразования адресов второго уровня (SLAT).</span><span class="sxs-lookup"><span data-stu-id="87f24-111">The VTL isolation is created by the Hyper-V Hypervisor which assigns memory at boot time using Second Level Address Translation (SLAT).</span></span> <span data-ttu-id="87f24-112">Он будет продолжать динамически по мере выполнения системы, защищая память, которую защищенный ядро указывает на необходимость защиты от VTL0, так как она будет использоваться для хранения секретов.</span><span class="sxs-lookup"><span data-stu-id="87f24-112">It continues this dynamically as the system runs, protecting memory the Secure Kernel specifies needing protection from VTL0 because it will be used to contain secrets.</span></span> <span data-ttu-id="87f24-113">Так как отдельные блоки памяти выделяются для двух Втлс, для VTL1 создается среда безопасной среды выполнения путем назначения эксклюзивных блоков памяти VTL1 и VTL0 с соответствующими разрешениями на доступ.</span><span class="sxs-lookup"><span data-stu-id="87f24-113">As separate blocks of memory are allocated for the two VTLs, a secure runtime environment is created for VTL1 by assigning exclusive memory blocks to VTL1 and VTL0 with the appropriate access permissions.</span></span>

<span data-ttu-id="87f24-114">**Схема 1 — Архитектура ИУМ**</span><span class="sxs-lookup"><span data-stu-id="87f24-114">**Diagram 1 - IUM Architecture**</span></span>

![Схема 1 — Архитектура ИУМ](images/uim-architecture.png)

## <a name="trustlets"></a><span data-ttu-id="87f24-116">трустлетс</span><span class="sxs-lookup"><span data-stu-id="87f24-116">Trustlets</span></span>

<span data-ttu-id="87f24-117">Трустлетс (также называемые надежными процессами, безопасными процессами или процессами ИУМ) — это программы, выполняемые как ИУМ процессы в VSM.</span><span class="sxs-lookup"><span data-stu-id="87f24-117">Trustlets (also known as trusted processes, secure processes, or IUM processes) are programs running as IUM processes in VSM.</span></span> <span data-ttu-id="87f24-118">Они завершают системные вызовы путем их маршалинга в ядро Windows, работающее в VTL0 Ring 0.</span><span class="sxs-lookup"><span data-stu-id="87f24-118">They complete system calls by marshalling them over to the Windows kernel running in VTL0 ring 0.</span></span> <span data-ttu-id="87f24-119">VSM создает малую среду выполнения, которая включает в себя небольшой безопасный ядро, выполняющееся в VTL1 (изолированном от ядра и драйверов, запущенных в VTL0).</span><span class="sxs-lookup"><span data-stu-id="87f24-119">VSM creates a small execution environment that includes the small Secure Kernel executing in VTL1 (isolated from the kernel and drivers running in VTL0).</span></span> <span data-ttu-id="87f24-120">Очевидное преимущество безопасности заключается в изоляции страниц пользовательского режима трустлет в VTL1 от драйверов, выполняющихся в ядре VTL0.</span><span class="sxs-lookup"><span data-stu-id="87f24-120">The clear security benefit is isolation of trustlet user mode pages in VTL1 from drivers running in the VTL0 kernel.</span></span> <span data-ttu-id="87f24-121">Даже если режим ядра VTL0 скомпрометирован вредоносными программами, он не будет иметь доступа к страницам процесса ИУМ.</span><span class="sxs-lookup"><span data-stu-id="87f24-121">Even if kernel mode of VTL0 is compromised by malware, it will not have access to the IUM process pages.</span></span>

<span data-ttu-id="87f24-122">При включенном протоколе VSM среда локального центра безопасности (LSASS) работает как трустлет.</span><span class="sxs-lookup"><span data-stu-id="87f24-122">With VSM enabled, the Local Security Authority (LSASS) environment runs as a trustlet.</span></span> <span data-ttu-id="87f24-123">LSASS управляет локальной системной политикой, проверкой подлинности пользователей и аудитом при обработке конфиденциальных данных безопасности, таких как хэши паролей и ключи Kerberos.</span><span class="sxs-lookup"><span data-stu-id="87f24-123">LSASS manages the local system policy, user authentication, and auditing while handling sensitive security data such as password hashes and Kerberos keys.</span></span> <span data-ttu-id="87f24-124">Чтобы использовать преимущества безопасности VSM, трустлет с именем LSAISO.exe (изолированный LSA) работает в VTL1 и взаимодействует с LSASS.exe, запущенным в VTL0 через канал RPC.</span><span class="sxs-lookup"><span data-stu-id="87f24-124">To leverage the security benefits of VSM, a trustlet named LSAISO.exe (LSA Isolated) runs in VTL1 and communicates with LSASS.exe running in VTL0 through an RPC channel.</span></span> <span data-ttu-id="87f24-125">Секреты ЛСАИСО шифруются перед отправкой в LSASS в нормальном режиме, а страницы ЛСАИСО защищены от вредоносного кода, запущенного в VTL0.</span><span class="sxs-lookup"><span data-stu-id="87f24-125">The LSAISO secrets are encrypted before sending them over to LSASS running in VSM Normal Mode and the pages of LSAISO are protected from malicious code running in VTL0.</span></span>

<span data-ttu-id="87f24-126">**Схема 2 — Разработка LSASS Трустлет**</span><span class="sxs-lookup"><span data-stu-id="87f24-126">**Diagram 2 – LSASS Trustlet Design**</span></span>

![<span data-ttu-id="87f24-127">Схема 2 — Разработка LSASS трустлет</span><span class="sxs-lookup"><span data-stu-id="87f24-127">diagram 2 – lsass trustlet design</span></span> ](images/lsass-trustlet-design.png)

## <a name="isolated-user-mode-ium-implications"></a><span data-ttu-id="87f24-128">Последствия изолированного режима пользователя (ИУМ)</span><span class="sxs-lookup"><span data-stu-id="87f24-128">Isolated User Mode (IUM) Implications</span></span>

<span data-ttu-id="87f24-129">Невозможно присоединиться к процессу ИУМ, препятствуя возможности отладки кода VTL1.</span><span class="sxs-lookup"><span data-stu-id="87f24-129">It is not possible to attach to an IUM process, inhibiting the ability to debug VTL1 code.</span></span> <span data-ttu-id="87f24-130">Сюда входят отладочная Отладка дампов памяти и присоединение средств отладки для отладки в режиме реального времени.</span><span class="sxs-lookup"><span data-stu-id="87f24-130">This includes post mortem debugging of memory dumps and attaching the Debugging Tools for live debugging.</span></span> <span data-ttu-id="87f24-131">Он также включает попытки привилегированных учетных записей или драйверов ядра для загрузки библиотеки DLL в процесс ИУМ, внедрения потока или доставки в пользовательском режиме.</span><span class="sxs-lookup"><span data-stu-id="87f24-131">It also includes attempts by privileged accounts or kernel drivers to load a DLL into an IUM process, to inject a thread, or deliver a user-mode APC.</span></span> <span data-ttu-id="87f24-132">Такие попытки могут привести к дестабилизации всей системы.</span><span class="sxs-lookup"><span data-stu-id="87f24-132">Such attempts may result in destabilization of the entire system.</span></span> <span data-ttu-id="87f24-133">API-интерфейсы Windows, которые приведут к нарушению безопасности Трустлет, могут завершаться сбоем непредвиденным образом.</span><span class="sxs-lookup"><span data-stu-id="87f24-133">Windows APIs that would compromise the security of a Trustlet may fail in unexpected ways.</span></span> <span data-ttu-id="87f24-134">Например, загрузка библиотеки DLL в Трустлет сделает ее доступной в VTL0, но не в VTL1.</span><span class="sxs-lookup"><span data-stu-id="87f24-134">For example, loading a DLL into a Trustlet will make it available in VTL0 but not VTL1.</span></span> <span data-ttu-id="87f24-135">Куеуеусерапк может завершиться неудачно, если целевой поток находится в Трустлет.</span><span class="sxs-lookup"><span data-stu-id="87f24-135">QueueUserApc may silently fail if the target thread is in a Trustlet.</span></span> <span data-ttu-id="87f24-136">Другие API, такие как Креатеремотесреад, Виртуалаллоцекс и Read/Вритепроцессмемори, также не будут работать должным образом при использовании в Трустлетс.</span><span class="sxs-lookup"><span data-stu-id="87f24-136">Other APIs, such as CreateRemoteThread, VirtualAllocEx, and Read/WriteProcessMemory will also not work as expected when used against Trustlets.</span></span>

<span data-ttu-id="87f24-137">Используйте приведенный ниже пример кода, чтобы предотвратить вызов любых функций, которые пытаются присоединить или внедрить код в процесс ИУМ.</span><span class="sxs-lookup"><span data-stu-id="87f24-137">Use the sample code below to prevent calling any functions which attempt to attach or inject code into an IUM process.</span></span> <span data-ttu-id="87f24-138">Сюда входят драйверы ядра, которые ставят APC в очередь для выполнения кода в трустлет.</span><span class="sxs-lookup"><span data-stu-id="87f24-138">This includes kernel drivers that queue APCs for execution of code in a trustlet.</span></span>

## <a name="remarks"></a><span data-ttu-id="87f24-139">Комментарии</span><span class="sxs-lookup"><span data-stu-id="87f24-139">Remarks</span></span>

<span data-ttu-id="87f24-140">Если возвращаемое состояние Иссекурепроцесс — Success, проверьте параметр Секурепроцесс \_ out, \_ чтобы определить, является ли процесс ИУМ процессом.</span><span class="sxs-lookup"><span data-stu-id="87f24-140">If the return status of IsSecureProcess is success, examine the SecureProcess \_Out\_ parameter to determine if the process is an IUM process.</span></span> <span data-ttu-id="87f24-141">Процессы ИУМ помечаются системой как "безопасные процессы".</span><span class="sxs-lookup"><span data-stu-id="87f24-141">IUM processes are marked by the system to be “Secure Processes”.</span></span> <span data-ttu-id="87f24-142">Логический результат TRUE означает, что целевой процесс относится к типу ИУМ.</span><span class="sxs-lookup"><span data-stu-id="87f24-142">A Boolean result of TRUE means the target process is of type IUM.</span></span>


```C++
NTSTATUS
IsSecureProcess(
   _In_ HANDLE ProcessHandle,
   _Out_ BOOLEAN *SecureProcess
   )
{
   NTSTATUS status;

       // definition included in ntddk.h  
   PROCESS_EXTENDED_BASIC_INFORMATION extendedInfo = {0};
 
   PAGED_CODE(); 
  
   extendedInfo.Size = sizeof(extendedInfo);

   // Query for the process information  
   status = ZwQueryInformationProcess(
                  ProcessHandle, ProcessBasicInformation, &extendedInfo,
                  sizeof(extendedInfo), NULL);

   if (NT_SUCCESS(status)) {
      *SecureProcess = (BOOLEAN)(extendedInfo.IsSecureProcess != 0);
   }
 
          return status;
}
```



<span data-ttu-id="87f24-143">WDK для Windows 10, «Windows Driver Kit — Windows 10.0.15063.0», содержит обязательное определение \_ \_ базовой \_ информационной структуры процесса.</span><span class="sxs-lookup"><span data-stu-id="87f24-143">The WDK for Windows 10, “Windows Driver Kit - Windows 10.0.15063.0”, contains the required definition of the PROCESS\_EXTENDED\_BASIC\_INFORMATION structure.</span></span> <span data-ttu-id="87f24-144">Обновленная версия структуры определена в нтддк. h с новым полем Иссекурепроцесс.</span><span class="sxs-lookup"><span data-stu-id="87f24-144">The updated version of the structure is defined in ntddk.h with the new IsSecureProcess field.</span></span>


```C++
typedef struct _PROCESS_EXTENDED_BASIC_INFORMATION {
    SIZE_T Size;    // Ignored as input, written with structure size on output
    PROCESS_BASIC_INFORMATION BasicInfo;
    union {
        ULONG Flags;
        struct {
            ULONG IsProtectedProcess : 1;
            ULONG IsWow64Process : 1;
            ULONG IsProcessDeleting : 1;
            ULONG IsCrossSessionCreate : 1;
            ULONG IsFrozen : 1;
            ULONG IsBackground : 1;
            ULONG IsStronglyNamed : 1;
            ULONG IsSecureProcess : 1;
            ULONG IsSubsystemProcess : 1;
            ULONG SpareBits : 23;
        } DUMMYSTRUCTNAME;
    } DUMMYUNIONNAME;
} PROCESS_EXTENDED_BASIC_INFORMATION, *PPROCESS_EXTENDED_BASIC_INFORMATION;
```



 

 



