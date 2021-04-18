---
title: Структура RECORD_HEADER
description: Заголовок записи, используемый \_ структурами записей журнала изменений \_ и \_ журнала изменений \_ .
ms.assetid: f8d2147c-ad13-4be4-94d7-ae0ca26511da
keywords:
- Восстановление системы структуры RECORD_HEADER
- Восстановление системы указателей на структуру PRECORD_HEADER
topic_type:
- apiref
api_name:
- RECORD_HEADER
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 2fd304d2f1b6a5ece08d3d3535aacd7a1abcf614
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104492183"
---
# <a name="record_header-structure"></a>\_Структура заголовка записи

\[Эти сведения относятся только к Windows XP с пакетом обновления 2 (SP2).\]

Заголовок записи, используемый структурами [**записей \_ журнала \_ изменений**](change-log-entry.md) и [**\_ журнала изменений \_**](change-log-header.md) .

## <a name="syntax"></a>Синтаксис


```C++
typedef struct _RECORD_HEADER {
  DWORD dwRecordSize;
  DWORD dwRecordType;
} RECORD_HEADER, *PRECORD_HEADER;
```



## <a name="members"></a>Члены

<dl> <dt>

**дврекордсизе**
</dt> <dd>

Общий размер записи, включая заголовок в байтах.

</dd> <dt>

**дврекордтипе**
</dt> <dd>

Тип записи. Этот элемент может иметь одно из следующих значений.



| Значение                                                                                                                                                                                                                                                                           | Значение                                                                                                                                                                                                                                                                            |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="RecordTypeLogHeader"></span><span id="recordtypelogheader"></span><span id="RECORDTYPELOGHEADER"></span><dl> <dt>**Рекордтипелогхеадер**</dt> <dt>0</dt> </dl>     | Запись является заголовком журнала изменений.<br/>                                                                                                                                                                                                                            |
| <span id="RecordTypeLogEntry"></span><span id="recordtypelogentry"></span><span id="RECORDTYPELOGENTRY"></span><dl> <dt>**Рекордтипеложентри**</dt> <dt>1</dt> </dl>         | Запись является заголовком записи журнала изменений.<br/>                                                                                                                                                                                                                        |
| <span id="RecordTypeVolumePath"></span><span id="recordtypevolumepath"></span><span id="RECORDTYPEVOLUMEPATH"></span><dl> <dt>**Рекордтипеволумепас**</dt> <dt>2</dt> </dl> | Данные — это путь тома для записи журнала изменений.<br/>                                                                                                                                                                                                                   |
| <span id="RecordTypeFirstPath"></span><span id="recordtypefirstpath"></span><span id="RECORDTYPEFIRSTPATH"></span><dl> <dt>**Рекордтипефирстпас**</dt> <dt>3</dt> </dl>     | Данные — это путь к файлу для записи журнала изменений.<br/>                                                                                                                                                                                                                     |
| <span id="RecordTypeSecondPath"></span><span id="recordtypesecondpath"></span><span id="RECORDTYPESECONDPATH"></span><dl> <dt>**Рекордтипесекондпас**</dt> <dt>4</dt> </dl> | Данные используются при переименовании записей журнала изменений. путь к расположению, где хранится переименованный файл.<br/>                                                                                                                                                                       |
| <span id="RecordTypeTempPath"></span><span id="recordtypetemppath"></span><span id="RECORDTYPETEMPPATH"></span><dl> <dt>**Рекордтипетемппас**</dt> <dt>5</dt> </dl>         | Данные представляют собой имя файла резервной копии, используемого для восстановления записи журнала изменений. Файлы резервной копии находятся в папке RP *n* . Имя файла имеет следующий формат:*XXXXXXX*. *ext*, где *XXXXXXX* — это 7-значное число, а *ext* — расширение имени файла.<br/> |
| <span id="RecordTypeAclInline"></span><span id="recordtypeaclinline"></span><span id="RECORDTYPEACLINLINE"></span><dl> <dt>**Рекордтипеаклинлине**</dt> <dt>6</dt> </dl>     | Данные представляют собой ACL. Формат данных является структурой [**\_ дескриптора безопасности**](/windows/desktop/api/winnt/ns-winnt-security_descriptor) . <br/> Это значение не может быть больше 8 192 байт. Чтобы указать значение, превышающее 8 192 байт, используйте элемент **рекордтипеаклфиле** .<br/>                |
| <span id="RecordTypeAclFile"></span><span id="recordtypeaclfile"></span><span id="RECORDTYPEACLFILE"></span><dl> <dt>**Рекордтипеаклфиле**</dt> <dt>7</dt> </dl>             | Данные представляют собой имя файла ACL, используемого для хранения списка управления доступом. Файлы ACL находятся в папке RP *n* . Имя файла имеет следующий формат: S *XXXXXXX*. ACL, где *XXXXXXX* — это 7-значное число.<br/>                                                             |
| <span id="RecordTypeDebugInfo"></span><span id="recordtypedebuginfo"></span><span id="RECORDTYPEDEBUGINFO"></span><dl> <dt>**Рекордтипедебугинфо**</dt> <dt>8</dt> </dl>     | Данные представляют собой отладочную информацию для записи журнала изменений. Формат данных представляет собой структуру **\_ \_ \_ сведений об отладке журнала SR** . Дополнительные сведения см. в подразделе "Примечания".<br/>                                                                                                                     |
| <span id="RecordTypeShortName"></span><span id="recordtypeshortname"></span><span id="RECORDTYPESHORTNAME"></span><dl> <dt>**Рекордтипешортнаме**</dt> <dt>9</dt> </dl>     | Данные — это короткое имя файла резервной копии.<br/>                                                                                                                                                                                                                          |



 

</dd> </dl>

## <a name="remarks"></a>Комментарии

Структура **\_ \_ \_ сведений об отладке журнала SR** определяется следующим образом.

``` syntax
typedef struct _SR_LOG_DEBUG_INFO {
    RECORD_HEADER Header;         // log entry header
    HANDLE ThreadId;              // thread identifier
    HANDLE ProcessId;             // process identifier
    ULARGER_INTEGER TimeStamp;    // event time stamp
    CHAR ProcesName[13];          // process name
} SR_LOG_DEBUG_INFO, *PSR_LOG_DEBUG_INFO;
```

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для настольных приложений Windows XP с пакетом обновления 2 \[\]<br/> |
| Минимальная версия сервера<br/> | Ни одна версия не поддерживается<br/>                            |
| Окончание поддержки клиента<br/>    | Windows XP с пакетом обновления 2 (SP2)<br/>                       |



 

