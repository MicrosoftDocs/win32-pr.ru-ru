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
# <a name="virtual-machine-generation-identifier"></a>Идентификатор создания виртуальной машины

Windows 8 и Windows Server 2012 представляют собой возможность программного обеспечения, выполняемого на виртуальной машине, чтобы обнаружить, что событие сдвига времени могло произойти. События сдвига времени могут возникать в результате применения моментального снимка виртуальной машины или восстановления резервной копии виртуальной машины. Дополнительные сведения об этих функциях см. в [техническом документе с идентификатором создания виртуальной машины](https://download.microsoft.com/download/3/1/C/31CFC307-98CA-4CA5-914C-D9772691E214/VirtualMachineGenerationID.docx).

## <a name="prerequisites"></a>Предварительные условия

Чтобы использовать идентификатор создания виртуальной машины из виртуальной машины, виртуальная машина должна соответствовать следующим требованиям.

-   Виртуальная машина должна работать в низкоуровневой оболочке, которая реализует поддержку идентификаторов создания виртуальных машин. В настоящее время это следующие данные:
    -   Windows 8
    -   Windows Server 2012
    -   Microsoft Hyper-V Server 2012
-   Виртуальная машина должна работать под управлением гостевой операционной системы, которая поддерживает идентификатор создания виртуальной машины. В настоящее время это следующие данные.

    Следующие операционные системы имеют встроенную поддержку идентификатора создания виртуальной машины.

    -   Windows 8
    -   Windows Server 2012
    -   

    В качестве операционной системы на виртуальной машине можно использовать следующую операционную систему, если установлены службы интеграции Hyper-V из Windows 8 или Windows Server 2012.

    -   Windows Server 2008 R2 с пакетом обновления 1 (SP1)
    -   Windows 7 с пакетом обновления 1 (SP1)
    -   Windows Server 2008 с пакетом обновления 2 (SP2)
    -   Windows Server 2003 R2
    -   Windows Server 2003 с пакетом обновления 2 (SP2)
    -   Windows Vista с пакетом обновления 2 (SP2)
    -   Windows XP с пакетом обновления 3 (SP3)

## <a name="obtaining-the-virtual-machine-generation-identifier"></a>Получение идентификатора создания виртуальной машины

Чтобы получить идентификатор создания виртуальной машины программным способом, выполните следующие действия.

> [!Note]  
> Для правильной работы необходимо выполнить следующие функции с правами администратора или системы.

 

1.  Включить заголовочный файл "вмженератионкаунтер. h" в приложение. Файл заголовка содержит следующие определения:
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

    

2.  Откройте маркер для \\ \\ . \\ Вмженератионкаунтер "устройство с помощью функции [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) . Кроме того, можно использовать диспетчер PnP для использования GUID интерфейса устройства **\_ девинтерфаце \_ VM \_ женкаунтер** ({3ff2c92b-6598-4e60-8e1c-0ccf4927e319}). Эти объекты не будут представлены, если приложение не выполняется на виртуальной машине.
3.  Отправьте запрос [**ioctl \_ вмженкаунтер \_ Read**](/windows/desktop/api/Vmgenerationcounter/ni-vmgenerationcounter-ioctl_vmgencounter_read) IOCTL на драйвер для получения идентификатора поколения.

    Запрос [**ioctl \_ вмженкаунтер \_ Read**](/windows/desktop/api/Vmgenerationcounter/ni-vmgenerationcounter-ioctl_vmgencounter_read) ioctl работает в одном из двух режимов: *опросов* и *управляемых событиями*.

    Чтобы выдать запрос IOCTL в режиме опроса, необходимо отправить IOCTL с входным буфером нулевой длины. В ответ на это драйвер получает текущий идентификатор поколения, записывает его в выходной буфер и завершает запрос IOCTL.

    Чтобы выдать запрос IOCTL в режиме, управляемом событиями, отправьте запрос IOCTL с входным буфером, содержащим существующий идентификатор поколения. В ответ на это драйвер ожидает, пока идентификатор текущего поколения не будет отличаться от переданного идентификатора поколения. При изменении идентификатора поколения драйвер записывает текущий идентификатор поколения в выходной буфер и завершает запрос IOCTL.

    В обоих режимах формат и длина выходного буфера определяются структурой [**\_ Женкаунтер виртуальной машины**](/windows/desktop/api/Vmgenerationcounter/ns-vmgenerationcounter-vm_gencounter) .

    Режим опроса поддерживается во всех указанных выше операционных системах на виртуальной машине. Режим обработки событий поддерживается только в Windows Vista с пакетом обновления 2 (SP2), Windows Server 2008 с пакетом обновления 2 (SP2) и более поздних операционных системах. В более ранних операционных системах запрос IOCTL завершится ошибкой с кодом **ошибки \_ не \_ поддерживается** при выдаче в режиме, управляемом событиями.

    Идентификатор поколения может изменяться между моментом, когда он извлекается драйвером, и временем завершения IOCTL. Это может привести к тому, что клиентское приложение получит устаревшие данные. Чтобы избежать этого, клиентское приложение может использовать режим, управляемый событиями, чтобы убедиться, что он в конечном итоге получит сведения об обновлениях идентификатора поколения. Используя текущий идентификатор клиентского приложения в качестве входных данных, в режиме, управляемом событиями, можно избежать потенциальных состояний гонки, которые приведут к тому, что вызывающий объект не будет получать уведомления.

В следующем примере кода показано, как выполнить указанные выше действия для получения идентификатора создания виртуальной машины.

> [!Note]  
> Для правильной работы необходимо запустить следующий код с правами администратора или системы.

 


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



## <a name="determining-if-a-time-shift-event-has-occurred"></a>Определение, произошло ли событие сдвига времени

После получения идентификатора создания виртуальной машины его необходимо сохранить для дальнейшего использования. Прежде чем приложение выполняет зависящую от времени операцию, например фиксацию в базе данных, необходимо повторно получить идентификатор поколения и сравнить его с сохраненным значением. Если идентификатор изменился, это означает, что произошло событие сдвига времени, и приложение должно работать правильно.

 

 
