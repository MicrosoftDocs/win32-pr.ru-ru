---
description: Windows 8 и Windows Server 2012 представляют собой возможность программного обеспечения, выполняемого на виртуальной машине, чтобы обнаружить, что событие сдвига времени могло произойти.
ms.assetid: 0793E46B-8464-425E-8C5B-77C14DA90004
title: Идентификатор создания виртуальной машины
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7df6ecbb600dbc7ae2efe14d36cb17cc75816444
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105684259"
---
# <a name="virtual-machine-generation-identifier"></a><span data-ttu-id="15f33-103">Идентификатор создания виртуальной машины</span><span class="sxs-lookup"><span data-stu-id="15f33-103">Virtual machine generation identifier</span></span>

<span data-ttu-id="15f33-104">Windows 8 и Windows Server 2012 представляют собой возможность программного обеспечения, выполняемого на виртуальной машине, чтобы обнаружить, что событие сдвига времени могло произойти.</span><span class="sxs-lookup"><span data-stu-id="15f33-104">Windows 8 and Windows Server 2012 introduce the ability for software that is running on a virtual machine to detect that a time shift event may have occurred.</span></span> <span data-ttu-id="15f33-105">События сдвига времени могут возникать в результате применения моментального снимка виртуальной машины или восстановления резервной копии виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="15f33-105">Time shift events can occur as a result of an application of a virtual machine snapshot or the restoration of a virtual machine backup.</span></span> <span data-ttu-id="15f33-106">Дополнительные сведения об этих функциях см. в [техническом документе с идентификатором создания виртуальной машины](https://download.microsoft.com/download/3/1/C/31CFC307-98CA-4CA5-914C-D9772691E214/VirtualMachineGenerationID.docx).</span><span class="sxs-lookup"><span data-stu-id="15f33-106">For more information about this functionality, see the [Virtual Machine Generation ID white paper](https://download.microsoft.com/download/3/1/C/31CFC307-98CA-4CA5-914C-D9772691E214/VirtualMachineGenerationID.docx).</span></span>

## <a name="prerequisites"></a><span data-ttu-id="15f33-107">Предварительные условия</span><span class="sxs-lookup"><span data-stu-id="15f33-107">Prerequisites</span></span>

<span data-ttu-id="15f33-108">Чтобы использовать идентификатор создания виртуальной машины из виртуальной машины, виртуальная машина должна соответствовать следующим требованиям.</span><span class="sxs-lookup"><span data-stu-id="15f33-108">To use the virtual machine generation identifier from inside a virtual machine your virtual machine must conform to the following.</span></span>

-   <span data-ttu-id="15f33-109">Виртуальная машина должна работать в низкоуровневой оболочке, которая реализует поддержку идентификаторов создания виртуальных машин.</span><span class="sxs-lookup"><span data-stu-id="15f33-109">The virtual machine must be running on a hypervisor that implements support for virtual machine generation identifiers.</span></span> <span data-ttu-id="15f33-110">В настоящее время это следующие данные:</span><span class="sxs-lookup"><span data-stu-id="15f33-110">Currently, these are the following:</span></span>
    -   <span data-ttu-id="15f33-111">Windows 8</span><span class="sxs-lookup"><span data-stu-id="15f33-111">Windows 8</span></span>
    -   <span data-ttu-id="15f33-112">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="15f33-112">Windows Server 2012</span></span>
    -   <span data-ttu-id="15f33-113">Microsoft Hyper-V Server 2012</span><span class="sxs-lookup"><span data-stu-id="15f33-113">Microsoft Hyper-V Server 2012</span></span>
-   <span data-ttu-id="15f33-114">Виртуальная машина должна работать под управлением гостевой операционной системы, которая поддерживает идентификатор создания виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="15f33-114">The virtual machine must be running a guest operating system that has support for the virtual machine generation identifier.</span></span> <span data-ttu-id="15f33-115">В настоящее время это следующие данные.</span><span class="sxs-lookup"><span data-stu-id="15f33-115">Currently, these are the following.</span></span>

    <span data-ttu-id="15f33-116">Следующие операционные системы имеют встроенную поддержку идентификатора создания виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="15f33-116">The following operating systems have native support for the virtual machine generation identifier.</span></span>

    -   <span data-ttu-id="15f33-117">Windows 8</span><span class="sxs-lookup"><span data-stu-id="15f33-117">Windows 8</span></span>
    -   <span data-ttu-id="15f33-118">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="15f33-118">Windows Server 2012</span></span>
    -   

    <span data-ttu-id="15f33-119">В качестве операционной системы на виртуальной машине можно использовать следующую операционную систему, если установлены службы интеграции Hyper-V из Windows 8 или Windows Server 2012.</span><span class="sxs-lookup"><span data-stu-id="15f33-119">The following operating can be used as the guest operating system if the Hyper-V integration services from Windows 8 or Windows Server 2012 are installed.</span></span>

    -   <span data-ttu-id="15f33-120">Windows Server 2008 R2 с пакетом обновления 1 (SP1)</span><span class="sxs-lookup"><span data-stu-id="15f33-120">Windows Server 2008 R2 with Service Pack 1 (SP1)</span></span>
    -   <span data-ttu-id="15f33-121">Windows 7 с пакетом обновления 1 (SP1)</span><span class="sxs-lookup"><span data-stu-id="15f33-121">Windows 7 with Service Pack 1 (SP1)</span></span>
    -   <span data-ttu-id="15f33-122">Windows Server 2008 с пакетом обновления 2 (SP2)</span><span class="sxs-lookup"><span data-stu-id="15f33-122">Windows Server 2008 with Service Pack 2 (SP2)</span></span>
    -   <span data-ttu-id="15f33-123">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="15f33-123">Windows Server 2003 R2</span></span>
    -   <span data-ttu-id="15f33-124">Windows Server 2003 с пакетом обновления 2 (SP2)</span><span class="sxs-lookup"><span data-stu-id="15f33-124">Windows Server 2003 with Service Pack 2 (SP2)</span></span>
    -   <span data-ttu-id="15f33-125">Windows Vista с пакетом обновления 2 (SP2)</span><span class="sxs-lookup"><span data-stu-id="15f33-125">Windows Vista with Service Pack 2 (SP2)</span></span>
    -   <span data-ttu-id="15f33-126">Windows XP с пакетом обновления 3 (SP3)</span><span class="sxs-lookup"><span data-stu-id="15f33-126">Windows XP with Service Pack 3 (SP3)</span></span>

## <a name="obtaining-the-virtual-machine-generation-identifier"></a><span data-ttu-id="15f33-127">Получение идентификатора создания виртуальной машины</span><span class="sxs-lookup"><span data-stu-id="15f33-127">Obtaining the virtual machine generation identifier</span></span>

<span data-ttu-id="15f33-128">Чтобы получить идентификатор создания виртуальной машины программным способом, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="15f33-128">To programmatically obtain the virtual machine generation identifier, perform the following steps.</span></span>

> [!Note]  
> <span data-ttu-id="15f33-129">Для правильной работы необходимо выполнить следующие функции с правами администратора или системы.</span><span class="sxs-lookup"><span data-stu-id="15f33-129">The following must be run with administrator or system privileges to function correctly.</span></span>

 

1.  <span data-ttu-id="15f33-130">Включить заголовочный файл "вмженератионкаунтер. h" в приложение.</span><span class="sxs-lookup"><span data-stu-id="15f33-130">Include header file "vmgenerationcounter.h" in your app.</span></span> <span data-ttu-id="15f33-131">Файл заголовка содержит следующие определения:</span><span class="sxs-lookup"><span data-stu-id="15f33-131">The header file contains these definitions:</span></span>
    ```C++
    DEFINE_GUID(
        GUID_DEVINTERFACE_VM_GENCOUNTER,
        0x3ff2c92b, 
        0x6598, 
        0x4e60, 
        0x8e, 
        0x1c, 
        0x0c, 
        0xcf, 
        0x49, 
        0x27, 
        0xe3, 
        0x19);

    #define VM_GENCOUNTER_SYMBOLIC_LINK_NAME L"VmGenerationCounter"

    #define IOCTL_VMGENCOUNTER_READ CTL_CODE( \
        FILE_DEVICE_ACPI, \
        0x1, METHOD_BUFFERED, \
        FILE_READ_ACCESS | FILE_WRITE_ACCESS)

    typedef struct _VM_GENCOUNTER
    {
        ULONGLONG GenerationCount;
        ULONGLONG GenerationCountHigh;
    } VM_GENCOUNTER, *PVM_GENCOUNTER;
    ```

    

2.  <span data-ttu-id="15f33-132">Откройте маркер для \\ \\ . \\ Вмженератионкаунтер "устройство с помощью функции [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) .</span><span class="sxs-lookup"><span data-stu-id="15f33-132">Open a handle to the "\\\\.\\VmGenerationCounter" device using the [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) function.</span></span> <span data-ttu-id="15f33-133">Кроме того, можно использовать диспетчер PnP для использования GUID интерфейса устройства **\_ девинтерфаце \_ VM \_ женкаунтер** ({3ff2c92b-6598-4e60-8e1c-0ccf4927e319}).</span><span class="sxs-lookup"><span data-stu-id="15f33-133">Alternatively, you can use the PnP manager to consume the device interface **GUID\_DEVINTERFACE\_VM\_GENCOUNTER** ({3ff2c92b-6598-4e60-8e1c-0ccf4927e319}).</span></span> <span data-ttu-id="15f33-134">Эти объекты не будут представлены, если приложение не выполняется на виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="15f33-134">These objects will not be present if the app is not running in a virtual machine.</span></span>
3.  <span data-ttu-id="15f33-135">Отправьте запрос [**ioctl \_ вмженкаунтер \_ Read**](/windows/desktop/api/Vmgenerationcounter/ni-vmgenerationcounter-ioctl_vmgencounter_read) IOCTL на драйвер для получения идентификатора поколения.</span><span class="sxs-lookup"><span data-stu-id="15f33-135">Send the [**IOCTL\_VMGENCOUNTER\_READ**](/windows/desktop/api/Vmgenerationcounter/ni-vmgenerationcounter-ioctl_vmgencounter_read) IOCTL to the driver to retrieve the generation identifier.</span></span>

    <span data-ttu-id="15f33-136">Запрос [**ioctl \_ вмженкаунтер \_ Read**](/windows/desktop/api/Vmgenerationcounter/ni-vmgenerationcounter-ioctl_vmgencounter_read) ioctl работает в одном из двух режимов: *опросов* и *управляемых событиями*.</span><span class="sxs-lookup"><span data-stu-id="15f33-136">The [**IOCTL\_VMGENCOUNTER\_READ**](/windows/desktop/api/Vmgenerationcounter/ni-vmgenerationcounter-ioctl_vmgencounter_read) IOCTL operates in one of two modes, *polling*, and *event driven*.</span></span>

    <span data-ttu-id="15f33-137">Чтобы выдать запрос IOCTL в режиме опроса, необходимо отправить IOCTL с входным буфером нулевой длины.</span><span class="sxs-lookup"><span data-stu-id="15f33-137">To issue the IOCTL in polling mode, you submit the IOCTL with an input buffer of zero length.</span></span> <span data-ttu-id="15f33-138">В ответ на это драйвер получает текущий идентификатор поколения, записывает его в выходной буфер и завершает запрос IOCTL.</span><span class="sxs-lookup"><span data-stu-id="15f33-138">In response to this, the driver retrieves the current generation identifier, writes it to the output buffer, and completes the IOCTL.</span></span>

    <span data-ttu-id="15f33-139">Чтобы выдать запрос IOCTL в режиме, управляемом событиями, отправьте запрос IOCTL с входным буфером, содержащим существующий идентификатор поколения.</span><span class="sxs-lookup"><span data-stu-id="15f33-139">To issue the IOCTL in event driven mode, submit the IOCTL with an input buffer that contains an existing generation identifier.</span></span> <span data-ttu-id="15f33-140">В ответ на это драйвер ожидает, пока идентификатор текущего поколения не будет отличаться от переданного идентификатора поколения.</span><span class="sxs-lookup"><span data-stu-id="15f33-140">In response to this, the driver waits until the current generation identifier becomes different from the generation identifier that was passed in.</span></span> <span data-ttu-id="15f33-141">При изменении идентификатора поколения драйвер записывает текущий идентификатор поколения в выходной буфер и завершает запрос IOCTL.</span><span class="sxs-lookup"><span data-stu-id="15f33-141">When the generation identifier changes, the driver writes the current generation identifier to the output buffer and completes the IOCTL.</span></span>

    <span data-ttu-id="15f33-142">В обоих режимах формат и длина выходного буфера определяются структурой [**\_ Женкаунтер виртуальной машины**](/windows/desktop/api/Vmgenerationcounter/ns-vmgenerationcounter-vm_gencounter) .</span><span class="sxs-lookup"><span data-stu-id="15f33-142">In both modes, the format and length of the output buffer is dictated by the [**VM\_GENCOUNTER**](/windows/desktop/api/Vmgenerationcounter/ns-vmgenerationcounter-vm_gencounter) structure.</span></span>

    <span data-ttu-id="15f33-143">Режим опроса поддерживается во всех указанных выше операционных системах на виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="15f33-143">Polling mode is supported on all of the guest operating systems listed above.</span></span> <span data-ttu-id="15f33-144">Режим обработки событий поддерживается только в Windows Vista с пакетом обновления 2 (SP2), Windows Server 2008 с пакетом обновления 2 (SP2) и более поздних операционных системах.</span><span class="sxs-lookup"><span data-stu-id="15f33-144">Event driven mode is supported only on Windows Vista with SP2, Windows Server 2008 with SP2, and later operating systems.</span></span> <span data-ttu-id="15f33-145">В более ранних операционных системах запрос IOCTL завершится ошибкой с кодом **ошибки \_ не \_ поддерживается** при выдаче в режиме, управляемом событиями.</span><span class="sxs-lookup"><span data-stu-id="15f33-145">On earlier operating systems, the IOCTL will fail with the error code **ERROR\_NOT\_SUPPORTED** when issued in event driven mode.</span></span>

    <span data-ttu-id="15f33-146">Идентификатор поколения может изменяться между моментом, когда он извлекается драйвером, и временем завершения IOCTL.</span><span class="sxs-lookup"><span data-stu-id="15f33-146">It is possible for the generation identifier to change between the time that it is retrieved by the driver and the time the IOCTL is completed.</span></span> <span data-ttu-id="15f33-147">Это может привести к тому, что клиентское приложение получит устаревшие данные.</span><span class="sxs-lookup"><span data-stu-id="15f33-147">This can result in the client app receiving stale data.</span></span> <span data-ttu-id="15f33-148">Чтобы избежать этого, клиентское приложение может использовать режим, управляемый событиями, чтобы убедиться, что он в конечном итоге получит сведения об обновлениях идентификатора поколения.</span><span class="sxs-lookup"><span data-stu-id="15f33-148">To avoid this, the client app can use event driven mode to ensure that it will eventually learn about any updates to the generation identifier.</span></span> <span data-ttu-id="15f33-149">Используя текущий идентификатор клиентского приложения в качестве входных данных, в режиме, управляемом событиями, можно избежать потенциальных состояний гонки, которые приведут к тому, что вызывающий объект не будет получать уведомления.</span><span class="sxs-lookup"><span data-stu-id="15f33-149">By taking the client app's current identifier as input, event driven mode avoids potential race conditions that would cause the caller to miss notifications.</span></span>

<span data-ttu-id="15f33-150">В следующем примере кода показано, как выполнить указанные выше действия для получения идентификатора создания виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="15f33-150">The following code example shows how to perform the above actions to obtain the virtual machine generation identifier.</span></span>

> [!Note]  
> <span data-ttu-id="15f33-151">Для правильной работы необходимо запустить следующий код с правами администратора или системы.</span><span class="sxs-lookup"><span data-stu-id="15f33-151">The following code must be run with administrator or system privileges to function correctly.</span></span>

 


```C++
HRESULT GetVmCounter(bool fWaitForChange)
{
    BOOL success = FALSE;
    DWORD error = ERROR_SUCCESS;
    VM_GENCOUNTER vmCounterOutput = {0};
    DWORD size = 0;
    HANDLE handle = INVALID_HANDLE_VALUE;
    HRESULT hr = S_OK;

    handle = CreateFile(
        L"\\\\.\\" VM_GENCOUNTER_SYMBOLIC_LINK_NAME,
        GENERIC_READ | GENERIC_WRITE,
        FILE_SHARE_READ | FILE_SHARE_WRITE,
        NULL,
        OPEN_EXISTING,
        0,
        NULL);

    if (handle == INVALID_HANDLE_VALUE)
    {
        error = GetLastError();

        wprintf(
            L"Unable to open device %s. Error code = %d.", 
            VM_GENCOUNTER_SYMBOLIC_LINK_NAME, 
            error);

        hr = HRESULT_FROM_WIN32(error);

        goto Cleanup;
    }

    /*
    Call into the driver. 

    Because the 4th parameter to DeviceIoControl (nInBufferSize) is zero, this 
    is a polling request rather than an event-driven request.
    */
    success = DeviceIoControl(
        handle,
        IOCTL_VMGENCOUNTER_READ,
        NULL,
        0,
        &vmCounterOutput,
        sizeof(vmCounterOutput),
        &size,
        NULL);

    if (!success)
    {
        error = GetLastError();

        wprintf(L"Call IOCTL_VMGENCOUNTER_READ failed with %d.", error);

        hr = HRESULT_FROM_WIN32(error);

        goto Cleanup;
    }

    wprintf(
        L"VmCounterValue: %I64x:%I64x",
        vmCounterOutput.GenerationCount,
        vmCounterOutput.GenerationCountHigh);

    if (fWaitForChange)
    {
        /*
        Call into the driver again in event-driven mode. DeviceIoControl won't 
        return until the generation identifier has changed.
        */
        success = DeviceIoControl(
            handle,
            IOCTL_VMGENCOUNTER_READ,
            &vmCounterOutput,
            sizeof(vmCounterOutput),
            &vmCounterOutput,
            sizeof(vmCounterOutput),
            &size,
            NULL);

        if (!success)
        {
            error = GetLastError();

            wprintf(L"Call IOCTL_VMGENCOUNTER_READ failed with %d.", error);

            hr = HRESULT_FROM_WIN32(error);

            goto Cleanup;
        }

        wprintf(
            L"VmCounterValue changed to: %I64x:%I64x",
            vmCounterOutput.GenerationCount,
            vmCounterOutput.GenerationCountHigh);
    }

Cleanup:

    if (handle != INVALID_HANDLE_VALUE)
    {
        CloseHandle(handle);
    }

    return hr;
};
```



## <a name="determining-if-a-time-shift-event-has-occurred"></a><span data-ttu-id="15f33-152">Определение, произошло ли событие сдвига времени</span><span class="sxs-lookup"><span data-stu-id="15f33-152">Determining if a time shift event has occurred</span></span>

<span data-ttu-id="15f33-153">После получения идентификатора создания виртуальной машины его необходимо сохранить для дальнейшего использования.</span><span class="sxs-lookup"><span data-stu-id="15f33-153">After you have obtained the virtual machine generation identifier, you should store it for future use.</span></span> <span data-ttu-id="15f33-154">Прежде чем приложение выполняет зависящую от времени операцию, например фиксацию в базе данных, необходимо повторно получить идентификатор поколения и сравнить его с сохраненным значением.</span><span class="sxs-lookup"><span data-stu-id="15f33-154">Before your app performs a time-sensitive operation, such as committing to a database, you should re-obtain the generation identifier and compare it to the stored value.</span></span> <span data-ttu-id="15f33-155">Если идентификатор изменился, это означает, что произошло событие сдвига времени, и приложение должно работать правильно.</span><span class="sxs-lookup"><span data-stu-id="15f33-155">If the identifier has changed, that means that a time shift event has occurred, and your app must act appropriately.</span></span>

 

 
