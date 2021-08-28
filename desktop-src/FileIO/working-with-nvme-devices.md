---
description: узнайте, как работать с высокоскоростными устройствами NVMe из приложения Windows.
ms.assetid: 037AF841-C2C9-4551-9CCB-F2A2F199083A
title: Работа с дисками NVMe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 22a749764aa0874aef618558199ca418582d0d36
ms.sourcegitcommit: 0dec0044816af3f2b2e6403659e1cf11138c90cd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/13/2021
ms.locfileid: "121812867"
---
# <a name="working-with-nvme-drives"></a>Работа с дисками NVMe

**Применимо к:**

-   Windows 10
-   Windows Server 2016

узнайте, как работать с высокоскоростными устройствами NVMe из приложения Windows. доступ к устройству включается с помощью **StorNVMe.sys**, встроенный драйвер впервые появился в Windows Server 2012 R2 и Windows 8.1. он также доступен для Windows 7 устройств с помощью горячего исправления KB. в Windows 10 появились несколько новых функций, включая сквозной механизм для специфичных для поставщика команд NVMe и обновлений существующих ioctl.

В этом разделе приводятся общие сведения об интерфейсах API общего использования, которые можно использовать для доступа к дискам NVMe в Windows 10. Он также описывает:

-   Отправка команды NVMe, относящейся к поставщику, с [передаваемым](#pass-through-mechanism)
-   [Отправка команды "найти", "получить компоненты" или "получение страниц журнала](#protocol-specific-queries) " на диск NVMe
-   [Получение сведений о температуре](#temperature-queries) с диска NVMe
-   Как выполнить изменение параметров поведения, например [задать пороговые значения температуры](#behavior-changing-commands)

## <a name="apis-for-working-with-nvme-drives"></a>Интерфейсы API для работы с дисками NVMe

Для доступа к дискам NVMe в Windows 10 можно использовать следующие интерфейсы API общего пользования. Эти API-интерфейсы можно найти в **виниоктл. h** для приложений пользовательского режима и **нтддстор. h** для драйверов режима ядра. Дополнительные сведения о файлах заголовков см. в разделе [заголовочные файлы](#header-files).

-   Запрос [**ioctl \_ \_ \_ Команда протокола хранилища**](/windows/desktop/api/winioctl/ni-winioctl-ioctl_storage_protocol_command) . Используйте этот запрос IOCTL в **структуре \_ \_ команд протокола хранилища** для выпусков команд NVMe. Этот запрос IOCTL обеспечивает сквозную передачу NVMe и поддерживает журнал командных эффектов в NVMe. Его можно использовать с командами, зависящими от поставщика. Дополнительные сведения см. в разделе [сквозной механизм](#pass-through-mechanism).

-   [**Хранилище \_ \_Команда протокола**](/windows/desktop/api/winioctl/ns-winioctl-storage_protocol_command) : Эта структура входного буфера включает поле **ReturnStatus** , которое можно использовать для передачи следующих значений состояния.
    -   **\_ \_ ожидается состояние протокола \_ хранилища**
    -   **\_состояние протокола хранилища — \_ \_ успешно**
    -   **\_ \_ Ошибка состояния протокола \_ хранилища**
    -   **\_ \_ \_ Недопустимый \_ запрос состояния протокола хранилища**
    -   **\_состояние протокола \_ хранилища \_ нет \_ устройства**
    -   **\_состояние протокола \_ хранилища \_ занято**
    -   **\_ \_ \_ переполнение данных о состоянии протокола \_ хранилища**
    -   **\_состояние протокола хранилища — \_ \_ недостаточно \_ ресурсов**
    -   **\_состояние протокола \_ хранилища \_ не \_ поддерживается**
-   Запрос [**ioctl \_ \_ \_ Свойство "запрос хранилища**](/windows/desktop/api/WinIoCtl/ni-winioctl-ioctl_storage_query_property) ". Используйте этот запрос IOCTL со структурой **\_ \_ запроса свойства хранилища** для получения сведений об устройстве. Дополнительные сведения см. в разделе [запросы, зависящие от протокола](#protocol-specific-queries) , и [запросы на температуру](#temperature-queries).

-   [**Хранилище \_ \_Запрос свойства**](/windows/desktop/api/WinIoCtl/ns-winioctl-storage_property_query) . Эта структура включает в себя поля **PropertyId** и **аддитионалпараметерс** для указания данных для запроса. В **PropertyId** с помощью перечисления **\_ \_ идентификаторов свойств хранилища** укажите тип данных. Используйте поле **аддитионалпараметерс** для указания дополнительных сведений в зависимости от типа данных. Для данных, относящихся к протоколу, используйте структуру **данных, \_ \_ относящуюся \_ к протоколу хранилища** , в поле **аддитионалпараметерс** . Для данных температуры используйте структуру **\_ \_ сведений о температуре хранилища** в поле **аддитионалпараметерс** .
-   [**Хранилище \_ \_Идентификатор свойства**](/windows/win32/api/winioctl/ne-winioctl-storage_property_id) . Это перечисление включает новые значения, которые позволяют **\_ \_ \_ свойству запроса на хранение через ioctl** получать сведения об особенностях протокола и температуры.

    -   **СторажеадаптерпротоколспеЦификпроперти**: Если ProtocolType = Протоколтипенвме и DataType = нвмедататипелогпаже, вызывающие объекты должны запрашивать 512 байтовых фрагментов данных.
    -   **сторажедевицепротоколспеЦификпроперти**

    Используйте один из этих идентификаторов свойств для конкретного протокола в сочетании **с \_ \_ \_ данными протокола хранилища** для получения данных, относящихся к протоколу, в структуре [**\_ \_ \_ дескриптора данных протокола хранилища**](/windows/desktop/api/WinIoCtl/ns-winioctl-storage_protocol_data_descriptor) .

    -   **сторажеадаптертемпературепроперти**
    -   **сторажедевицетемпературепроперти**

    Используйте один из этих идентификаторов свойств температуры для получения данных температуры в [**структуре \_ \_ \_ дескриптора данных температуры хранилища**](/windows/desktop/api/WinIoctl/ns-winioctl-storage_temperature_data_descriptor) .

-   [**Хранилище \_ \_ \_ Данные, относящиеся к протоколу**](/windows/desktop/api/WinIoCtl/ns-winioctl-storage_protocol_specific_data) : получение данных, относящихся к NVMe, если эта структура используется для поля **аддитионалпараметерс** **\_ \_ запроса свойства хранилища** и указано значение перечисления [**\_ \_ \_ \_ типа данных NVMe протокола хранилища**](/windows/desktop/api/WinIoCtl/ne-winioctl-storage_protocol_nvme_data_type) . Используйте одно из следующих значений **\_ \_ \_ \_ типа данных NVME протокола хранилища** в поле **DataType** структуры **\_ \_ \_ данных, характерной для протокола хранилища** :

    -   Используйте **нвмедататипеидентифи** , чтобы найти данные контроллера или указать данные пространства имен.
    -   Используйте **нвмедататипелогпаже** для получения страниц журнала (в том числе интеллектуальных и данных о работоспособности).
    -   Используйте **нвмедататипефеатуре** для получения компонентов диска NVMe.

-   [**Хранилище \_ \_Сведения о температуре**](/windows/desktop/api/WinIoctl/ns-winioctl-storage_temperature_info) . Эта структура используется для хранения данных о температуре. Он используется в **\_ \_ \_ дескрипторе данных темературе хранилища** для возврата результатов запроса температуры.

-   Запрос [**ioctl \_ \_ \_ \_ Порог температуры для набора хранения**](/windows/desktop/api/WinIoctl/ni-winioctl-ioctl_storage_set_temperature_threshold) : Используйте этот запрос IOCTL **с \_ \_ пороговой структурой температуры хранилища** , чтобы задать пороговые значения температуры. Дополнительные сведения см. в разделе [поведение при изменении команд](#behavior-changing-commands).

-   [**Хранилище \_ \_Пороговое значение температуры**](/windows/desktop/api/WinIoctl/ns-winioctl-storage_temperature_threshold) . Эта структура используется в качестве входного буфера для указания порога температуры. Поле "превышение **порогового** значения" (логическое значение) указывает, является ли поле **порогового** значения пороговое значение или нет (в противном случае это будет ниже порогового значения).

## <a name="pass-through-mechanism"></a>Сквозной механизм

Команды, которые не определены в спецификации NVMe, наиболее сложны для обработки. узел не имеет сведений о влиянии команд на целевое устройство, предоставленной инфраструктуре (пространствах имен/размеров блоков) и его поведении.

для более эффективного выполнения таких команд, связанных с конкретными устройствами, через стек хранилища Windows, новый механизм сквозного перебора позволяет передавать команды для конкретного поставщика. Этот транзитный канал также поможет в разработке средств управления и тестирования. Однако этот механизм передачи данных требует использования журнала командных эффектов. Более того, для StoreNVMe.sys требуются все команды, а не только транзитные команды, которые должны быть описаны в журнале командных эффектов.

> [!IMPORTANT]
> StorNVMe.sys и Storport.sys будут блокировать любую команду на устройство, если оно не описано в журнале командных эффектов.

 

### <a name="supporting-the-command-effects-log"></a>Поддержка журнала командных эффектов

Журнал командных эффектов (как описано в разделе Supported and Effects, Section 5.10.1.5 of [NVMe 1,2](https://nvmexpress.org/specifications)) позволяет описать влияние команд, относящихся к поставщику, вместе с командами, определяемыми спецификацией. Это упрощает проверку поддержки команд, а также оптимизацию поведения команд и, следовательно, должна быть реализована для всего набора команд, поддерживаемых устройством. Следующие условия описывают результат отправки команды на основе записи журнала командных эффектов.

Для любой команды, описанной в журнале командных эффектов...

**Время**:

-   Для поддерживаемой команды (КСУПП) задано значение "1", что означает, что команда поддерживается контроллером (бит 01).

    > [!Note]  
    > Если для КСУПП задано значение "0" (что означает, что команда не поддерживается), команда будет заблокирована

     

**Если** заданы следующие значения:

-   Для изменения возможностей контроллера (CCC) задано значение "1", что означает, что команда может изменить возможности контроллера (бит 04)

-   Для изменения описи пространства имен (NIC) задано значение "1", что означает, что команда может изменить число или возможности для нескольких пространств имен (бит 03)

-   Для изменения возможностей пространства имен (RIPE) задано значение "1", что означает, что команда может изменить возможности одного пространства имен (бит 02)

-   Для отправки команды и выполнения (CSE) задано значение 001В или 010B, что означает, что команда может быть отправлена при отсутствии других невыполненных команд для одного и того же или любого пространства имен, а другая команда не должна быть отправлена в то же или какое-либо пространство имен, пока эта команда не будет завершена (BITS 18:16).

**Затем** команда будет отправлена в качестве единственной команды, ожидающей адаптеру.

**Else If**:

-   Для отправки команды и выполнения (CSE) задано значение 001В, что означает, что команда может быть отправлена при отсутствии других необработанных команд в том же пространстве имен, а другая команда не должна быть отправлена в то же пространство имен, пока эта команда не будет завершена (BITS 18:16).

**Затем** команда будет отправлена как единственная команда, недоступная для объекта логического номера устройства (LUN).

**В противном случае** команда отправляется с другими командами, выполненными без запрета. Например, если на устройство отправляется команда, зависящая от поставщика, для получения статистических сведений, не определенных спецификацией, не должно быть риска изменять поведение устройства или возможность выполнения команд ввода-вывода. Такие запросы могут обслуживаться параллельно с вводом-выводом, а пауза-возобновление не потребуется.

### <a name="using-ioctl_storage_protocol_command-to-send-commands"></a>Использование \_ \_ команды протокола хранилища ioctl \_ для отправки команд

Для передачи данных можно использовать [**\_ \_ \_ команду протокола хранилища ioctl**](/windows/desktop/api/winioctl/ni-winioctl-ioctl_storage_protocol_command), представленную в Windows 10. Этот запрос IOCTL был разработан так, чтобы иметь такое же поведение, как и существующие сквозные IOCTL SCSI и ATA, для отправки внедренной команды на целевое устройство. С помощью этого IOCTL можно отправлять данные на устройство хранения, включая диск NVMe.

Например, в NVMe запрос IOCTL разрешит отправку следующих кодов команд.

-   Команды администрирования для конкретного поставщика (C0h – ФФХ)
-   Специфические для поставщика команды NVMe (80h – ФФХ)

Как и в случае со всеми другими IOCTL, используйте [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) для отправки сквозного IOCTL. Запрос IOCTL заполняется с помощью структуры входного буфера [**\_ \_ команды протокола хранилища**](/windows/desktop/api/winioctl/ns-winioctl-storage_protocol_command) , обнаруженной в **нтддстор. h**. Заполните поле **команда** командой, зависящей от поставщика.


```C++
typedef struct _STORAGE_PROTOCOL_COMMAND {

    ULONG   Version;                        // STORAGE_PROTOCOL_STRUCTURE_VERSION
    ULONG   Length;                         // sizeof(STORAGE_PROTOCOL_COMMAND)

    STORAGE_PROTOCOL_TYPE  ProtocolType;
    ULONG   Flags;                          // Flags for the request

    ULONG   ReturnStatus;                   // return value
    ULONG   ErrorCode;                      // return value, optional

    ULONG   CommandLength;                  // non-zero value should be set by caller
    ULONG   ErrorInfoLength;                // optional, can be zero
    ULONG   DataToDeviceTransferLength;     // optional, can be zero. Used by WRITE type of request.
    ULONG   DataFromDeviceTransferLength;   // optional, can be zero. Used by READ type of request.

    ULONG   TimeOutValue;                   // in unit of seconds

    ULONG   ErrorInfoOffset;                // offsets need to be pointer aligned
    ULONG   DataToDeviceBufferOffset;       // offsets need to be pointer aligned
    ULONG   DataFromDeviceBufferOffset;     // offsets need to be pointer aligned

    ULONG   CommandSpecific;                // optional information passed along with Command.
    ULONG   Reserved0;

    ULONG   FixedProtocolReturnData;        // return data, optional. Some protocol, such as NVMe, may return a small amount data (DWORD0 from completion queue entry) without the need of separate device data transfer.
    ULONG   Reserved1[3];

    _Field_size_bytes_full_(CommandLength) UCHAR Command[ANYSIZE_ARRAY];

} STORAGE_PROTOCOL_COMMAND, *PSTORAGE_PROTOCOL_COMMAND;
```



Указанная выше команда для конкретного поставщика должна быть заполнена в выделенном поле выше. Обратите внимание, что журнал командных эффектов должен быть реализован для транзитных команд. В частности, эти команды необходимо сообщить как поддерживаемые в журнале командных эффектов (Дополнительные сведения см. в предыдущем разделе). Кроме того, обратите внимание, что поля репликации паролей являются специфическими для драйвера, поэтому приложения, отправляющие команды, могут оставить их как 0

Наконец, этот транзитный запрос IOCTL предназначен для отправки команд, относящихся к поставщику. Чтобы отправить другим администраторам или не относящимся к поставщику команды NVMe, такие как Identify, не следует использовать этот сквозной запрос IOCTL. Например, **\_ \_ \_ свойство запроса хранилища ioctl** должно использоваться для поиска и получения страниц журнала. Дополнительные сведения см. в следующем разделе запросы, [относящиеся к протоколу](/windows).

### <a name="dont-update-firmware-through-the-pass-through-mechanism"></a>Не обновляйте встроенное по через сквозной механизм

Команды загрузки и активации встроенного по не должны отправляться с помощью сквозной передачи. Запрос **ioctl \_ \_ \_ Команда протокола хранилища** должна использоваться только для специфичных для поставщика команд.

вместо этого используйте следующие общие протоколы IOCTL службы хранилища (появившиеся в Windows 10), чтобы избежать непосредственного использования \_ версии минипорта встроенного по на основе SCSI. служба хранилища drivers преобразует ioctl в команду scsi или \_ версию минипорта scsi для IOCTL на минипорт.

эти запросы ioctl рекомендуются для разработки средств обновления встроенного по в Windows 10 и Windows Server 2016.

-   [**\_ \_ \_ Получение сведений о встроенном по для хранилища ioctl \_**](/windows/desktop/api/WinIoctl/ni-winioctl-ioctl_storage_firmware_get_info)
-   [**\_ \_ скачивание встроенного по для хранилища ioctl \_**](/windows/desktop/api/WinIoctl/ni-winioctl-ioctl_storage_firmware_download)
-   [**\_ \_ Активация встроенного по службы хранилища ioctl \_**](/windows/desktop/api/WinIoctl/ni-winioctl-ioctl_storage_firmware_activate)

для быстрого получения сведений о хранилище и обновления встроенного по Windows также поддерживает командлеты PowerShell.

-   `Get-StorageFirmwareInfo`
-   `Update-StorageFirmware `

> [!Note]  
> для обновления встроенного по в NVMe в Windows 8.1 используйте \_ \_ \_ подпрограмму IOCTL SCSI минипорта. этот запрос IOCTL не был перенесен в Windows 7. Дополнительные сведения см. [в разделе Обновление встроенного по для устройства NVMe в Windows 8.1](/windows-hardware/drivers/storage/upgrading-firmware-for-an-nvme-device).

 

### <a name="returning-errors-through-the-pass-through-mechanism"></a>Возвращение ошибок через сквозной механизм

При отправке команды или запроса на мини-порт или устройство, как и в случае передачи команд и запросов между SCSI и ATA, функция IOCTL возвращает значение, если он был успешным. В структуре [**\_ \_ команды протокола хранилища**](/windows/desktop/api/winioctl/ns-winioctl-storage_protocol_command) ioctl возвращает состояние через поле **ReturnStatus** .

### <a name="example-sending-a-vendor-specific-command"></a>Пример. Отправка команды, относящейся к поставщику

В этом примере произвольная команда, зависящая от поставщика (0xFF), отправляется через транзитный диск в устройство NVMe. Следующий код выделяет буфер, инициализирует запрос, а затем отправляет команду на устройство через DeviceIoControl.


```C++
    ZeroMemory(buffer, bufferLength);  
    protocolCommand = (PSTORAGE_PROTOCOL_COMMAND)buffer;  

    protocolCommand->Version = STORAGE_PROTOCOL_STRUCTURE_VERSION;  
    protocolCommand->Length = sizeof(STORAGE_PROTOCOL_COMMAND);  
    protocolCommand->ProtocolType = ProtocolTypeNvme;  
    protocolCommand->Flags = STORAGE_PROTOCOL_COMMAND_FLAG_ADAPTER_REQUEST;  
    protocolCommand->CommandLength = STORAGE_PROTOCOL_COMMAND_LENGTH_NVME;  
    protocolCommand->ErrorInfoLength = sizeof(NVME_ERROR_INFO_LOG);  
    protocolCommand->DataFromDeviceTransferLength = 4096;  
    protocolCommand->TimeOutValue = 10;  
    protocolCommand->ErrorInfoOffset = FIELD_OFFSET(STORAGE_PROTOCOL_COMMAND, Command) + STORAGE_PROTOCOL_COMMAND_LENGTH_NVME;  
    protocolCommand->DataFromDeviceBufferOffset = protocolCommand->ErrorInfoOffset + protocolCommand->ErrorInfoLength;  
    protocolCommand->CommandSpecific = STORAGE_PROTOCOL_SPECIFIC_NVME_ADMIN_COMMAND;  

    command = (PNVME_COMMAND)protocolCommand->Command;  

    command->CDW0.OPC = 0xFF;  
    command->u.GENERAL.CDW10 = 0xto_fill_in;  
    command->u.GENERAL.CDW12 = 0xto_fill_in;  
    command->u.GENERAL.CDW13 = 0xto_fill_in;  

    //  
    // Send request down.  
    //  

    result = DeviceIoControl(DeviceList[DeviceIndex].Handle,  
                             IOCTL_STORAGE_PROTOCOL_COMMAND,  
                             buffer,  
                             bufferLength,  
                             buffer,  
                             bufferLength,  
                             &returnedLength,  
                             NULL 
                             );  
```



В этом примере мы предполагаем, что `protocolCommand->ReturnStatus == STORAGE_PROTOCOL_STATUS_SUCCESS` команда была успешной на устройстве.

## <a name="protocol-specific-queries"></a>Запросы для конкретного протокола

Windows 8.1 представил [**\_ \_ \_ свойство запроса хранилища IOCTL**](/windows/desktop/api/WinIoCtl/ni-winioctl-ioctl_storage_query_property) для получения данных. в Windows 10 функция IOCTL была улучшена для поддержки часто запрашиваемых функций NVMe, таких как **получение страниц журнала**, **получение функций** и **обнаружение**. Это позволяет получить сведения о конкретном NVMe для мониторинга и инвентаризации.

здесь показан входной буфер для запроса IOCTL [**, \_ свойства \_ хранилища**](/windows/desktop/api/WinIoCtl/ns-winioctl-storage_property_query) (от Windows 10).


```C++
typedef struct _STORAGE_PROPERTY_QUERY {
    STORAGE_PROPERTY_ID PropertyId;
    STORAGE_QUERY_TYPE QueryType;
    UCHAR  AdditionalParameters[1];
} STORAGE_PROPERTY_QUERY, *PSTORAGE_PROPERTY_QUERY;
```



При использовании [**\_ \_ \_ Свойства запроса хранилища ioctl**](/windows/desktop/api/WinIoCtl/ni-winioctl-ioctl_storage_query_property) для получения сведений о конкретном протоколе NVMe [**в \_ \_ \_ дескрипторе данных протокола хранилища**](/windows/desktop/api/WinIoCtl/ns-winioctl-storage_protocol_data_descriptor)настройте [**структуру \_ \_ запроса свойства хранилища**](/windows/desktop/api/WinIoCtl/ns-winioctl-storage_property_query) следующим образом:

-   Выделите буфер, который может содержать как [**\_ \_ запрос свойства хранилища**](/windows/desktop/api/WinIoCtl/ns-winioctl-storage_property_query) , так и структуру [**\_ \_ \_ данных, специфичную для протокола хранилища**](/windows/desktop/api/WinIoCtl/ns-winioctl-storage_protocol_specific_data) .

-   Задайте для поля **PropertyID** значение **сторажеадаптерпротоколспеЦификпроперти** или **сторажедевицепротоколспеЦификпроперти** для запроса контроллера или устройства/пространства имен соответственно.

-   Задайте для поля **QueryType** значение **пропертистандардкуери**.

-   Заполните структуру [**\_ данных, \_ относящуюся \_ к протоколу хранилища**](/windows/desktop/api/WinIoCtl/ns-winioctl-storage_protocol_specific_data) , с нужными значениями. В начале **\_ \_ \_ данных протокола хранилища** задается поле **аддитионалпараметерс** [**\_ \_ запроса свойства хранилища**](/windows/desktop/api/WinIoCtl/ns-winioctl-storage_property_query).

здесь показана структура [**\_ \_ \_ данных, специфичная для протокола хранилища**](/windows/desktop/api/WinIoCtl/ns-winioctl-storage_protocol_specific_data) (от Windows 10).


```C++
typedef struct _STORAGE_PROTOCOL_SPECIFIC_DATA {

    STORAGE_PROTOCOL_TYPE ProtocolType;
    ULONG   DataType;                 

    ULONG   ProtocolDataRequestValue;
    ULONG   ProtocolDataRequestSubValue;

    ULONG   ProtocolDataOffset;         
    ULONG   ProtocolDataLength;

    ULONG   FixedProtocolReturnData;   
    ULONG   Reserved[3];

} STORAGE_PROTOCOL_SPECIFIC_DATA, *PSTORAGE_PROTOCOL_SPECIFIC_DATA;
```



Чтобы указать тип сведений, относящихся к протоколу NVMe, настройте структуру [**\_ \_ \_ данных, специфичную для протокола хранилища**](/windows/desktop/api/WinIoCtl/ns-winioctl-storage_protocol_specific_data) , следующим образом.

-   Задайте для поля **ProtocolType** значение **протоколтипенвме**.

-   Задайте для поля **DataType** значение перечисления, определенное [**\_ \_ \_ \_ типом данных NVME протоколом хранилища**](/windows/desktop/api/WinIoCtl/ne-winioctl-storage_protocol_nvme_data_type):

    -   Используйте **нвмедататипеидентифи** , чтобы найти данные контроллера или указать данные пространства имен.
    -   Используйте **нвмедататипелогпаже** для получения страниц журнала (в том числе интеллектуальных и данных о работоспособности).
    -   Используйте **нвмедататипефеатуре** для получения компонентов диска NVMe.

Если в качестве **ProtocolType** используется **протоколтипенвме** , запросы сведений, относящихся к протоколу, можно получить параллельно с другими операциями ввода-вывода на диске NVMe.

> [!IMPORTANT]
> Для [**IOCTL_STORAGE_QUERY_PROPERTY**](/windows/win32/api/winioctl/ni-winioctl-ioctl_storage_query_property) , в которой используется **STORAGE_PROPERTY_ID** [**сторажеадаптерпротоколспеЦификпроперти**](/windows/win32/api/winioctl/ne-winioctl-storage_property_id), для которой [**STORAGE_PROTOCOL_SPECIFIC_DATA**](/windows/win32/api/winioctl/ns-winioctl-storage_protocol_specific_data) или [**STORAGE_PROTOCOL_SPECIFIC_DATA_EXT**](/windows-hardware/drivers/ddi/ntddstor/ns-ntddstor-storage_protocol_specific_data_ext) структура имеет значение `ProtocolType=ProtocolTypeNvme` и `DataType=NVMeDataTypeLogPage` , установите для элемента протоколдаталенгс той же структуры минимальное значение 512 (байт).


В следующих примерах демонстрируются запросы, зависящие от протокола NVMe.

### <a name="example-nvme-identify-query"></a>Пример: NVMe Identify, запрос

В этом примере запрос **Identify** отправляется на диск NVMe. Следующий код инициализирует структуру данных запроса, а затем отправляет команду на устройство через DeviceIoControl.


```C++
    BOOL    result;
    PVOID   buffer = NULL;
    ULONG   bufferLength = 0;
    ULONG   returnedLength = 0;

    PSTORAGE_PROPERTY_QUERY query = NULL;
    PSTORAGE_PROTOCOL_SPECIFIC_DATA protocolData = NULL;
    PSTORAGE_PROTOCOL_DATA_DESCRIPTOR protocolDataDescr = NULL;

    //
    // Allocate buffer for use.
    //
    bufferLength = FIELD_OFFSET(STORAGE_PROPERTY_QUERY, AdditionalParameters) + sizeof(STORAGE_PROTOCOL_SPECIFIC_DATA) + NVME_MAX_LOG_SIZE;
    buffer = malloc(bufferLength);

    if (buffer == NULL) {
        _tprintf(_T("DeviceNVMeQueryProtocolDataTest: allocate buffer failed, exit.\n"));
        goto exit;
    }

    //
    // Initialize query data structure to get Identify Controller Data.
    //
    ZeroMemory(buffer, bufferLength);

    query = (PSTORAGE_PROPERTY_QUERY)buffer;
    protocolDataDescr = (PSTORAGE_PROTOCOL_DATA_DESCRIPTOR)buffer;
    protocolData = (PSTORAGE_PROTOCOL_SPECIFIC_DATA)query->AdditionalParameters;

    query->PropertyId = StorageAdapterProtocolSpecificProperty;
    query->QueryType = PropertyStandardQuery;

    protocolData->ProtocolType = ProtocolTypeNvme;
    protocolData->DataType = NVMeDataTypeIdentify;
    protocolData->ProtocolDataRequestValue = NVME_IDENTIFY_CNS_CONTROLLER;
    protocolData->ProtocolDataRequestSubValue = 0;
    protocolData->ProtocolDataOffset = sizeof(STORAGE_PROTOCOL_SPECIFIC_DATA);
    protocolData->ProtocolDataLength = NVME_MAX_LOG_SIZE;

    //
    // Send request down.
    //
    result = DeviceIoControl(DeviceList[Index].Handle,
                             IOCTL_STORAGE_QUERY_PROPERTY,
                             buffer,
                             bufferLength,
                             buffer,
                             bufferLength,
                             &returnedLength,
                             NULL
                             );

    ZeroMemory(buffer, bufferLength);
    query = (PSTORAGE_PROPERTY_QUERY)buffer;  
    protocolDataDescr = (PSTORAGE_PROTOCOL_DATA_DESCRIPTOR)buffer;  
    protocolData = (PSTORAGE_PROTOCOL_SPECIFIC_DATA)query->AdditionalParameters;  

    query->PropertyId = StorageDeviceProtocolSpecificProperty;  
    query->QueryType = PropertyStandardQuery;  

    protocolData->ProtocolType = ProtocolTypeNvme;  
    protocolData->DataType = NVMeDataTypeLogPage;  
    protocolData->ProtocolDataRequestValue = NVME_LOG_PAGE_HEALTH_INFO;  
    protocolData->ProtocolDataRequestSubValue = 0;  
    protocolData->ProtocolDataOffset = sizeof(STORAGE_PROTOCOL_SPECIFIC_DATA);  
    protocolData->ProtocolDataLength = sizeof(NVME_HEALTH_INFO_LOG);  

    //  
    // Send request down.  
    //  
    result = DeviceIoControl(DeviceList[Index].Handle,  
                             IOCTL_STORAGE_QUERY_PROPERTY,  
                             buffer,  
                             bufferLength,  
                             buffer, 
                             bufferLength,  
                             &returnedLength,  
                             NULL  
                             );  

    //
    // Validate the returned data.
    //
    if ((protocolDataDescr->Version != sizeof(STORAGE_PROTOCOL_DATA_DESCRIPTOR)) ||
        (protocolDataDescr->Size != sizeof(STORAGE_PROTOCOL_DATA_DESCRIPTOR))) {
        _tprintf(_T("DeviceNVMeQueryProtocolDataTest: Get Identify Controller Data - data descriptor header not valid.\n"));
        return;
    }

    protocolData = &protocolDataDescr->ProtocolSpecificData;

    if ((protocolData->ProtocolDataOffset < sizeof(STORAGE_PROTOCOL_SPECIFIC_DATA)) ||
        (protocolData->ProtocolDataLength < NVME_MAX_LOG_SIZE)) {
        _tprintf(_T("DeviceNVMeQueryProtocolDataTest: Get Identify Controller Data - ProtocolData Offset/Length not valid.\n"));
        goto exit;
    }

    //
    // Identify Controller Data 
    //
    {
        PNVME_IDENTIFY_CONTROLLER_DATA identifyControllerData = (PNVME_IDENTIFY_CONTROLLER_DATA)((PCHAR)protocolData + protocolData->ProtocolDataOffset);

        if ((identifyControllerData->VID == 0) ||
            (identifyControllerData->NN == 0)) {
            _tprintf(_T("DeviceNVMeQueryProtocolDataTest: Identify Controller Data not valid.\n"));
            goto exit;
        } else {
            _tprintf(_T("DeviceNVMeQueryProtocolDataTest: ***Identify Controller Data succeeded***.\n"));
        }
    }

  
```

> [!IMPORTANT]
> Для [**IOCTL_STORAGE_QUERY_PROPERTY**](/windows/win32/api/winioctl/ni-winioctl-ioctl_storage_query_property) , в которой используется **STORAGE_PROPERTY_ID** [**сторажеадаптерпротоколспеЦификпроперти**](/windows/win32/api/winioctl/ne-winioctl-storage_property_id), для которой [**STORAGE_PROTOCOL_SPECIFIC_DATA**](/windows/win32/api/winioctl/ns-winioctl-storage_protocol_specific_data) или [**STORAGE_PROTOCOL_SPECIFIC_DATA_EXT**](/windows-hardware/drivers/ddi/ntddstor/ns-ntddstor-storage_protocol_specific_data_ext) структура имеет значение `ProtocolType=ProtocolTypeNvme` и `DataType=NVMeDataTypeLogPage` , установите для элемента протоколдаталенгс той же структуры минимальное значение 512 (байт).


Обратите внимание, что вызывающему объекту необходимо выделить один буфер, содержащий \_ запрос свойства хранилища \_ , и \_ размер \_ данных, характерных для протокола хранилища \_ . В этом примере для ввода и вывода запроса свойства используется один и тот же буфер. Вот почему выделенный буфер имеет размер " \_ смещение поля ( \_ запрос свойства хранилища \_ , аддитионалпараметерс) + sizeof ( \_ данные протокола хранилища \_ \_ ) + \_ \_ " максимальный размер журнала NVME \_ ". Несмотря на то, что отдельные буферы можно выделить для ввода и вывода, мы рекомендуем использовать один буфер для запроса связанных данных NVMe.

### <a name="example-nvme-get-log-pages-query"></a>Пример: запрос на получение страниц журнала NVMe

В этом примере, основанном на предыдущем, запрос на **получение страниц журнала** отправляется на диск NVMe. Следующий код подготавливает структуру данных запроса, а затем отправляет команду на устройство через DeviceIoControl.


```C++
    ZeroMemory(buffer, bufferLength);  

    query = (PSTORAGE_PROPERTY_QUERY)buffer;  
    protocolDataDescr = (PSTORAGE_PROTOCOL_DATA_DESCRIPTOR)buffer;  
    protocolData = (PSTORAGE_PROTOCOL_SPECIFIC_DATA)query->AdditionalParameters;  

    query->PropertyId = StorageDeviceProtocolSpecificProperty;  
    query->QueryType = PropertyStandardQuery;  

    protocolData->ProtocolType = ProtocolTypeNvme;  
    protocolData->DataType = NVMeDataTypeLogPage;  
    protocolData->ProtocolDataRequestValue = NVME_LOG_PAGE_HEALTH_INFO;  
    protocolData->ProtocolDataRequestSubValue = 0;  // This will be passed as the lower 32 bit of log page offset if controller supports extended data for the Get Log Page.
    protocolData->ProtocolDataRequestSubValue2 = 0; // This will be passed as the higher 32 bit of log page offset if controller supports extended data for the Get Log Page.
    protocolData->ProtocolDataRequestSubValue3 = 0; // This will be passed as Log Specific Identifier in CDW11.
    protocolData->ProtocolDataRequestSubValue4 = 0; // This will map to STORAGE_PROTOCOL_DATA_SUBVALUE_GET_LOG_PAGE definition, then user can pass Retain Asynchronous Event, Log Specific Field.

    protocolData->ProtocolDataOffset = sizeof(STORAGE_PROTOCOL_SPECIFIC_DATA);  
    protocolData->ProtocolDataLength = sizeof(NVME_HEALTH_INFO_LOG);  

    //  
    // Send request down.  
    //  
    result = DeviceIoControl(DeviceList[Index].Handle,  
                             IOCTL_STORAGE_QUERY_PROPERTY,  
                             buffer,  
                             bufferLength,  
                             buffer, 
                             bufferLength,  
                             &returnedLength,  
                             NULL  
                             );  

    if (!result || (returnedLength == 0)) {
        _tprintf(_T("DeviceNVMeQueryProtocolDataTest: SMART/Health Information Log failed. Error Code %d.\n"), GetLastError());
        goto exit;
    }

    //
    // Validate the returned data.
    //
    if ((protocolDataDescr->Version != sizeof(STORAGE_PROTOCOL_DATA_DESCRIPTOR)) ||
        (protocolDataDescr->Size != sizeof(STORAGE_PROTOCOL_DATA_DESCRIPTOR))) {
        _tprintf(_T("DeviceNVMeQueryProtocolDataTest: SMART/Health Information Log - data descriptor header not valid.\n"));
        return;
    }

    protocolData = &protocolDataDescr->ProtocolSpecificData;

    if ((protocolData->ProtocolDataOffset < sizeof(STORAGE_PROTOCOL_SPECIFIC_DATA)) ||
        (protocolData->ProtocolDataLength < sizeof(NVME_HEALTH_INFO_LOG))) {
        _tprintf(_T("DeviceNVMeQueryProtocolDataTest: SMART/Health Information Log - ProtocolData Offset/Length not valid.\n"));
        goto exit;
    }

    //
    // SMART/Health Information Log Data 
    //
    {
        PNVME_HEALTH_INFO_LOG smartInfo = (PNVME_HEALTH_INFO_LOG)((PCHAR)protocolData + protocolData->ProtocolDataOffset);

        _tprintf(_T("DeviceNVMeQueryProtocolDataTest: SMART/Health Information Log Data - Temperature %d.\n"), ((ULONG)smartInfo->Temperature[1] << 8 | smartInfo->Temperature[0]) - 273);

        _tprintf(_T("DeviceNVMeQueryProtocolDataTest: ***SMART/Health Information Log succeeded***.\n"));
    }

```



### <a name="example-nvme-get-features-query"></a>Пример: запрос на получение функций NVMe

В этом примере, основанном на предыдущем, запрос **Get Features** отправляется на диск NVMe. Следующий код подготавливает структуру данных запроса, а затем отправляет команду на устройство через DeviceIoControl.


```C++
    //  
    // Initialize query data structure to Volatile Cache feature.  
    //  

    ZeroMemory(buffer, bufferLength);  


    query = (PSTORAGE_PROPERTY_QUERY)buffer;  
    protocolDataDescr = (PSTORAGE_PROTOCOL_DATA_DESCRIPTOR)buffer;  
    protocolData = (PSTORAGE_PROTOCOL_SPECIFIC_DATA)query->AdditionalParameters;  

    query->PropertyId = StorageDeviceProtocolSpecificProperty;  
    query->QueryType = PropertyStandardQuery;  

    protocolData->ProtocolType = ProtocolTypeNvme;  
    protocolData->DataType = NVMeDataTypeFeature;  
    protocolData->ProtocolDataRequestValue = NVME_FEATURE_VOLATILE_WRITE_CACHE;  
    protocolData->ProtocolDataRequestSubValue = 0;  
    protocolData->ProtocolDataOffset = 0;  
    protocolData->ProtocolDataLength = 0;  

    //  
    // Send request down.  
    //  

    result = DeviceIoControl(DeviceList[Index].Handle,  
                             IOCTL_STORAGE_QUERY_PROPERTY,  
                             buffer,  
                             bufferLength,  
                             buffer,  
                             bufferLength,  
                             &returnedLength,  
                             NULL  
                             );  

    if (!result || (returnedLength == 0)) {  
        _tprintf(_T("DeviceNVMeQueryProtocolDataTest: Get Feature - Volatile Cache failed. Error Code %d.\n"), GetLastError());  
        goto exit;  
    }  

    //  
    // Validate the returned data.  
    //  

    if ((protocolDataDescr->Version != sizeof(STORAGE_PROTOCOL_DATA_DESCRIPTOR)) ||  
        (protocolDataDescr->Size != sizeof(STORAGE_PROTOCOL_DATA_DESCRIPTOR))) {  
        _tprintf(_T("DeviceNVMeQueryProtocolDataTest: Get Feature - Volatile Cache  - data descriptor header not valid.\n"));  
        return;                                           
    }  

    //
    // Volatile Cache 
    //
    {
        _tprintf(_T("DeviceNVMeQueryProtocolDataTest: Get Feature - Volatile Cache - %x.\n"), protocolDataDescr->ProtocolSpecificData.FixedProtocolReturnData);

        _tprintf(_T("DeviceNVMeQueryProtocolDataTest: ***Get Feature - Volatile Cache succeeded***.\n"));
    }
```
## <a name="protocol-specific-set"></a>Набор, зависящий от протокола

начиная с Windows 10 19H1, IOCTL_STORAGE_SET_PROPERTY был усовершенствован для поддержки функций набора NVMe.

Входной буфер для IOCTL_STORAGE_SET_PROPERTY показан ниже:

```C++
typedef struct _STORAGE_PROPERTY_SET {

    //
    // ID of the property being retrieved
    //

    STORAGE_PROPERTY_ID PropertyId;

    //
    // Flags indicating the type of set property being performed
    //

    STORAGE_SET_TYPE SetType;

    //
    // Space for additional parameters if necessary
    //

    UCHAR AdditionalParameters[1];

} STORAGE_PROPERTY_SET, *PSTORAGE_PROPERTY_SET;
```

При использовании IOCTL_STORAGE_SET_PROPERTY для установки функции NVMe Настройте структуру STORAGE_PROPERTY_SET следующим образом:

-   Выделите буфер, который может содержать как STORAGE_PROPERTY_SET, так и STORAGE_PROTOCOL_SPECIFIC_DATA_EXT структуру.
-   Задайте для поля PropertyID значение СторажеадаптерпротоколспеЦификпроперти или СторажедевицепротоколспеЦификпроперти для запроса контроллера или устройства/пространства имен соответственно.
-   Заполните структуру STORAGE_PROTOCOL_SPECIFIC_DATA_EXT нужными значениями. Началом STORAGE_PROTOCOL_SPECIFIC_DATA_EXT является поле Аддитионалпараметерс STORAGE_PROPERTY_SET.

Структура STORAGE_PROTOCOL_SPECIFIC_DATA_EXT показана здесь.

```C++
typedef struct _STORAGE_PROTOCOL_SPECIFIC_DATA_EXT {

    STORAGE_PROTOCOL_TYPE ProtocolType;
    ULONG   DataType;                   // The value will be protocol specific, as defined in STORAGE_PROTOCOL_NVME_DATA_TYPE or STORAGE_PROTOCOL_ATA_DATA_TYPE.

    ULONG   ProtocolDataValue;
    ULONG   ProtocolDataSubValue;      // Data sub request value

    ULONG   ProtocolDataOffset;         // The offset of data buffer is from beginning of this data structure.
    ULONG   ProtocolDataLength;

    ULONG   FixedProtocolReturnData;
    ULONG   ProtocolDataSubValue2;     // First additional data sub request value

    ULONG   ProtocolDataSubValue3;     // Second additional data sub request value
    ULONG   ProtocolDataSubValue4;     // Third additional data sub request value

    ULONG   ProtocolDataSubValue5;     // Fourth additional data sub request value
    ULONG   Reserved[5];
} STORAGE_PROTOCOL_SPECIFIC_DATA_EXT, *PSTORAGE_PROTOCOL_SPECIFIC_DATA_EXT;
```

Чтобы указать тип устанавливаемой функции NVMe, настройте структуру STORAGE_PROTOCOL_SPECIFIC_DATA_EXT следующим образом:
-   Задайте для поля ProtocolType значение Протоколтипенвме.
-   Задайте в поле DataType значение перечисления Нвмедататипефеатуре, определенное STORAGE_PROTOCOL_NVME_DATA_TYPE.

В следующих примерах демонстрируется набор функций NVMe.

### <a name="example-nvme-set-features"></a>Пример: параметры SET NVMe

В этом примере запрос Set Features отправляется на диск NVMe. Следующий код подготавливает структуру данных SET, а затем отправляет команду на устройство через DeviceIoControl.

```C++
            PSTORAGE_PROPERTY_SET                   setProperty = NULL;
            PSTORAGE_PROTOCOL_SPECIFIC_DATA_EXT     protocolData = NULL;
            PSTORAGE_PROTOCOL_DATA_DESCRIPTOR_EXT   protocolDataDescr = NULL;

            //
            // Allocate buffer for use.
            //
            bufferLength = FIELD_OFFSET(STORAGE_PROPERTY_SET, AdditionalParameters) + sizeof(STORAGE_PROTOCOL_SPECIFIC_DATA_EXT);
            bufferLength += NVME_MAX_LOG_SIZE;

            buffer = new UCHAR[bufferLength];

            //
            // Initialize query data structure to get the desired log page.
            //
            ZeroMemory(buffer, bufferLength);

            setProperty = (PSTORAGE_PROPERTY_SET)buffer;

            setProperty->PropertyId = StorageAdapterProtocolSpecificProperty;
            setProperty->SetType = PropertyStandardSet;

            protocolData = (PSTORAGE_PROTOCOL_SPECIFIC_DATA_EXT)setProperty->AdditionalParameters;

            protocolData->ProtocolType = ProtocolTypeNvme;
            protocolData->DataType = NVMeDataTypeFeature;
            protocolData->ProtocolDataValue = NVME_FEATURE_HOST_CONTROLLED_THERMAL_MANAGEMENT;

            protocolData->ProtocolDataSubValue = 0; // This will pass to CDW11.
            protocolData->ProtocolDataSubValue2 = 0; // This will pass to CDW12.
            protocolData->ProtocolDataSubValue3 = 0; // This will pass to CDW13.
            protocolData->ProtocolDataSubValue4 = 0; // This will pass to CDW14.
            protocolData->ProtocolDataSubValue5 = 0; // This will pass to CDW15.

            protocolData->ProtocolDataOffset = 0;
            protocolData->ProtocolDataLength = 0;

            //
            // Send request down.
            //
            result = DeviceIoControl(m_deviceHandle,
                                     IOCTL_STORAGE_SET_PROPERTY,
                                     buffer,
                                     bufferLength,
                                     buffer,
                                     bufferLength,
                                     &returnedLength,
                                     NULL
            );
```

## <a name="temperature-queries"></a>Запросы температуры

в Windows 10 [**\_ \_ \_ свойство запроса хранилища IOCTL**](/windows/desktop/api/WinIoCtl/ni-winioctl-ioctl_storage_query_property) также можно использовать для запроса данных о температуре с устройств NVMe.

Чтобы получить сведения о температуре с диска NVMe в [**\_ \_ \_ дескрипторе данных температуры хранилища**](/windows/desktop/api/WinIoctl/ns-winioctl-storage_temperature_data_descriptor), настройте структуру [**\_ \_ запроса свойства хранилища**](/windows/desktop/api/WinIoCtl/ns-winioctl-storage_property_query) следующим образом:

-   Выделение буфера, который может содержать структуру [**\_ \_ запроса свойства хранилища**](/windows/desktop/api/WinIoCtl/ns-winioctl-storage_property_query) .

-   Задайте для поля **PropertyID** значение **сторажеадаптертемпературепроперти** или **сторажедевицетемпературепроперти** для запроса контроллера или устройства/пространства имен соответственно.

-   Задайте для поля **QueryType** значение **пропертистандардкуери**.

здесь показана структура [**\_ \_ сведений о температуре хранилища**](/windows/desktop/api/WinIoctl/ns-winioctl-storage_temperature_info) (от Windows 10).


```C++
typedef struct _STORAGE_TEMPERATURE_INFO {

    USHORT  Index;                      // Starts from 0. Index 0 may indicate a composite value.
    SHORT   Temperature;                // Signed value; in Celsius.
    SHORT   OverThreshold;              // Signed value; in Celsius.
    SHORT   UnderThreshold;             // Signed value; in Celsius.

    BOOLEAN OverThresholdChangable;     // Can the threshold value being changed by using IOCTL_STORAGE_SET_TEMPERATURE_THRESHOLD.
    BOOLEAN UnderThresholdChangable;    // Can the threshold value being changed by using IOCTL_STORAGE_SET_TEMPERATURE_THRESHOLD.
    BOOLEAN EventGenerated;             // Indicates that notification will be generated when temperature cross threshold.
    UCHAR   Reserved0;
    ULONG   Reserved1;

} STORAGE_TEMPERATURE_INFO, *PSTORAGE_TEMPERATURE_INFO;
```



## <a name="behavior-changing-commands"></a>Изменение поведения команд

Команды, которые управляют атрибутами устройства или потенциально влияют на поведение устройства, сложнее для работы с операционной системой. Если при обработке операций ввода-вывода атрибуты устройств изменяются во время выполнения, в случае неправильной обработки могут возникнуть проблемы с синхронизацией или целостностью данных.

Команда NVMe **Set-Features** — хороший пример команды изменения поведения. Он позволяет изменять механизм арбитража и устанавливать пороговые значения температуры. чтобы гарантировать, что при отправке команд set, влияющих на работу, Windows будет приостанавливать все операции ввода-вывода на устройстве NVMe, очищать очереди и буферы очистки. После успешного выполнения команды Set операции ввода-вывода возобновляются (если это возможно). Если операция ввода-вывода не может быть возобновлена, может потребоваться сброс устройства.

### <a name="setting-temperature-thresholds"></a>Установка пороговых значений температуры

Windows 10 введено [**\_ \_ \_ \_ пороговое значение температуры для набора параметров хранения ioctl**](/windows/desktop/api/WinIoctl/ni-winioctl-ioctl_storage_set_temperature_threshold), ioctl для получения и установки порогов температуры. Его также можно использовать для получения текущей температуры устройства. Буфер ввода-вывода для этого IOCTL является структурой [**\_ \_ сведений о температуре хранилища**](/windows/desktop/api/WinIoctl/ns-winioctl-storage_temperature_info) из предыдущего раздела кода.

### <a name="example-setting-over-threshold-temperature"></a>Пример. Настройка температуры с чрезмерным пороговым значением

В этом примере задается пороговое значение температуры диска NVMe. Следующий код подготавливает команду, а затем отправляет ее на устройство через DeviceIoControl.


```C++
    BOOL    result;  
    ULONG   returnedLength = 0;  
    
    STORAGE_TEMPERATURE_THRESHOLD setThreshold = {0};  

    setThreshold.Version = sizeof(STORAGE_TEMPERATURE_THRESHOLD); 
    setThreshold.Size = sizeof(STORAGE_TEMPERATURE_THRESHOLD);  
    setThreshold.Flags = STORAGE_TEMPERATURE_THRESHOLD_FLAG_ADAPTER_REQUEST;  
    setThreshold.Index = SensorIndex;  
    setThreshold.Threshold = Threshold;  
    setThreshold.OverThreshold = UpdateOverThreshold; 

    //  
    // Send request down.  
    //  

    result = DeviceIoControl(DeviceList[DeviceIndex].Handle,  
                             IOCTL_STORAGE_SET_TEMPERATURE_THRESHOLD,  
                             &setThreshold,  
                             sizeof(STORAGE_TEMPERATURE_THRESHOLD),  
                             NULL,  
                             0,  
                             &returnedLength,  
                             NULL  
                             ); 

```



### <a name="setting-vendor-specific-features"></a>Настройка функций для конкретного поставщика

Без журнала командных эффектов драйвер не знает о последствиях выполнения команды. Именно поэтому требуется журнал командных эффектов. Она помогает операционной системе определить, является ли команда высокой, и может ли она параллельно отправляться с другими командами на диск.

Журнал командных эффектов еще не является достаточно детализированным, чтобы охватывать команды **набора функций** , зависящие от поставщика. По этой причине невозможно отправить команды **набора функций** , зависящие от поставщика. Однако можно использовать сквозной механизм, рассмотренный ранее, для отправки команд, относящихся к поставщику. Дополнительные сведения см. в разделе [сквозной механизм](#pass-through-mechanism).

## <a name="header-files"></a>Файлы заголовков

Следующие файлы относятся к разработке NVMe. эти файлы входят в состав [пакета средств разработки программного обеспечения (SDK) для Microsoft Windows](https://developer.microsoft.com/windows/downloads).



| Файл заголовка    | Описание                                                                             |
|----------------|-----------------------------------------------------------------------------------------|
| **нтддстор. h** | Определяет константы и типы для доступа к драйверам класса хранилища из режима ядра.   |
| **nvme. h**     | Для других структур данных, связанных с NVMe.                                                 |
| **виниоктл. h** | Для общих определений Win32 IOCTL, включая API хранилища для приложений пользовательского режима. |



 

 

 
