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
# <a name="record_header-structure"></a><span data-ttu-id="e9fcf-105">\_Структура заголовка записи</span><span class="sxs-lookup"><span data-stu-id="e9fcf-105">RECORD\_HEADER structure</span></span>

<span data-ttu-id="e9fcf-106">\[Эти сведения относятся только к Windows XP с пакетом обновления 2 (SP2).\]</span><span class="sxs-lookup"><span data-stu-id="e9fcf-106">\[This information applies only to Windows XP with Service Pack 2 (SP2).\]</span></span>

<span data-ttu-id="e9fcf-107">Заголовок записи, используемый структурами [**записей \_ журнала \_ изменений**](change-log-entry.md) и [**\_ журнала изменений \_**](change-log-header.md) .</span><span class="sxs-lookup"><span data-stu-id="e9fcf-107">The record header used by the [**CHANGE\_LOG\_ENTRY**](change-log-entry.md) and [**CHANGE\_LOG\_HEADER**](change-log-header.md) structures.</span></span>

## <a name="syntax"></a><span data-ttu-id="e9fcf-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e9fcf-108">Syntax</span></span>


```C++
typedef struct _RECORD_HEADER {
  DWORD dwRecordSize;
  DWORD dwRecordType;
} RECORD_HEADER, *PRECORD_HEADER;
```



## <a name="members"></a><span data-ttu-id="e9fcf-109">Члены</span><span class="sxs-lookup"><span data-stu-id="e9fcf-109">Members</span></span>

<dl> <dt>

<span data-ttu-id="e9fcf-110">**дврекордсизе**</span><span class="sxs-lookup"><span data-stu-id="e9fcf-110">**dwRecordSize**</span></span>
</dt> <dd>

<span data-ttu-id="e9fcf-111">Общий размер записи, включая заголовок в байтах.</span><span class="sxs-lookup"><span data-stu-id="e9fcf-111">The total size of the record, including the header, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="e9fcf-112">**дврекордтипе**</span><span class="sxs-lookup"><span data-stu-id="e9fcf-112">**dwRecordType**</span></span>
</dt> <dd>

<span data-ttu-id="e9fcf-113">Тип записи.</span><span class="sxs-lookup"><span data-stu-id="e9fcf-113">The record type.</span></span> <span data-ttu-id="e9fcf-114">Этот элемент может иметь одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="e9fcf-114">This member may be one of the following values.</span></span>



| <span data-ttu-id="e9fcf-115">Значение</span><span class="sxs-lookup"><span data-stu-id="e9fcf-115">Value</span></span>                                                                                                                                                                                                                                                                           | <span data-ttu-id="e9fcf-116">Значение</span><span class="sxs-lookup"><span data-stu-id="e9fcf-116">Meaning</span></span>                                                                                                                                                                                                                                                                            |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="RecordTypeLogHeader"></span><span id="recordtypelogheader"></span><span id="RECORDTYPELOGHEADER"></span><dl> <span data-ttu-id="e9fcf-117"><dt>**Рекордтипелогхеадер**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="e9fcf-117"><dt>**RecordTypeLogHeader**</dt> <dt>0</dt></span></span> </dl>     | <span data-ttu-id="e9fcf-118">Запись является заголовком журнала изменений.</span><span class="sxs-lookup"><span data-stu-id="e9fcf-118">The record is the header for the change log.</span></span><br/>                                                                                                                                                                                                                            |
| <span id="RecordTypeLogEntry"></span><span id="recordtypelogentry"></span><span id="RECORDTYPELOGENTRY"></span><dl> <span data-ttu-id="e9fcf-119"><dt>**Рекордтипеложентри**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="e9fcf-119"><dt>**RecordTypeLogEntry**</dt> <dt>1</dt></span></span> </dl>         | <span data-ttu-id="e9fcf-120">Запись является заголовком записи журнала изменений.</span><span class="sxs-lookup"><span data-stu-id="e9fcf-120">The record is the header for a change log entry.</span></span><br/>                                                                                                                                                                                                                        |
| <span id="RecordTypeVolumePath"></span><span id="recordtypevolumepath"></span><span id="RECORDTYPEVOLUMEPATH"></span><dl> <span data-ttu-id="e9fcf-121"><dt>**Рекордтипеволумепас**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="e9fcf-121"><dt>**RecordTypeVolumePath**</dt> <dt>2</dt></span></span> </dl> | <span data-ttu-id="e9fcf-122">Данные — это путь тома для записи журнала изменений.</span><span class="sxs-lookup"><span data-stu-id="e9fcf-122">The data is the volume path for the change log entry.</span></span><br/>                                                                                                                                                                                                                   |
| <span id="RecordTypeFirstPath"></span><span id="recordtypefirstpath"></span><span id="RECORDTYPEFIRSTPATH"></span><dl> <span data-ttu-id="e9fcf-123"><dt>**Рекордтипефирстпас**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="e9fcf-123"><dt>**RecordTypeFirstPath**</dt> <dt>3</dt></span></span> </dl>     | <span data-ttu-id="e9fcf-124">Данные — это путь к файлу для записи журнала изменений.</span><span class="sxs-lookup"><span data-stu-id="e9fcf-124">The data is the file path for the change log entry.</span></span><br/>                                                                                                                                                                                                                     |
| <span id="RecordTypeSecondPath"></span><span id="recordtypesecondpath"></span><span id="RECORDTYPESECONDPATH"></span><dl> <span data-ttu-id="e9fcf-125"><dt>**Рекордтипесекондпас**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="e9fcf-125"><dt>**RecordTypeSecondPath**</dt> <dt>4</dt></span></span> </dl> | <span data-ttu-id="e9fcf-126">Данные используются при переименовании записей журнала изменений. путь к расположению, где хранится переименованный файл.</span><span class="sxs-lookup"><span data-stu-id="e9fcf-126">The data is used when renaming change log entries; this path is where the renamed file is stored.</span></span><br/>                                                                                                                                                                       |
| <span id="RecordTypeTempPath"></span><span id="recordtypetemppath"></span><span id="RECORDTYPETEMPPATH"></span><dl> <span data-ttu-id="e9fcf-127"><dt>**Рекордтипетемппас**</dt> <dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="e9fcf-127"><dt>**RecordTypeTempPath**</dt> <dt>5</dt></span></span> </dl>         | <span data-ttu-id="e9fcf-128">Данные представляют собой имя файла резервной копии, используемого для восстановления записи журнала изменений.</span><span class="sxs-lookup"><span data-stu-id="e9fcf-128">The data is the name of the backup file used to restore the change log entry.</span></span> <span data-ttu-id="e9fcf-129">Файлы резервной копии находятся в папке RP *n* .</span><span class="sxs-lookup"><span data-stu-id="e9fcf-129">The backup files are located in the RP *n* folder.</span></span> <span data-ttu-id="e9fcf-130">Имя файла имеет следующий формат:*XXXXXXX*. *ext*, где *XXXXXXX* — это 7-значное число, а *ext* — расширение имени файла.</span><span class="sxs-lookup"><span data-stu-id="e9fcf-130">The file name has the following format: A *xxxxxxx*.*ext*, where *xxxxxxx* is a seven-digit number and *ext* is the file name extension.</span></span><br/> |
| <span id="RecordTypeAclInline"></span><span id="recordtypeaclinline"></span><span id="RECORDTYPEACLINLINE"></span><dl> <span data-ttu-id="e9fcf-131"><dt>**Рекордтипеаклинлине**</dt> <dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="e9fcf-131"><dt>**RecordTypeAclInline**</dt> <dt>6</dt></span></span> </dl>     | <span data-ttu-id="e9fcf-132">Данные представляют собой ACL.</span><span class="sxs-lookup"><span data-stu-id="e9fcf-132">The data is an ACL.</span></span> <span data-ttu-id="e9fcf-133">Формат данных является структурой [**\_ дескриптора безопасности**](/windows/desktop/api/winnt/ns-winnt-security_descriptor) .</span><span class="sxs-lookup"><span data-stu-id="e9fcf-133">The data format is a [**SECURITY\_DESCRIPTOR**](/windows/desktop/api/winnt/ns-winnt-security_descriptor) structure.</span></span> <br/> <span data-ttu-id="e9fcf-134">Это значение не может быть больше 8 192 байт.</span><span class="sxs-lookup"><span data-stu-id="e9fcf-134">This value cannot be larger than 8,192 bytes.</span></span> <span data-ttu-id="e9fcf-135">Чтобы указать значение, превышающее 8 192 байт, используйте элемент **рекордтипеаклфиле** .</span><span class="sxs-lookup"><span data-stu-id="e9fcf-135">To specify a value larger than 8,192 bytes, use the **RecordTypeAclFile** member.</span></span><br/>                |
| <span id="RecordTypeAclFile"></span><span id="recordtypeaclfile"></span><span id="RECORDTYPEACLFILE"></span><dl> <span data-ttu-id="e9fcf-136"><dt>**Рекордтипеаклфиле**</dt> <dt>7</dt></span><span class="sxs-lookup"><span data-stu-id="e9fcf-136"><dt>**RecordTypeAclFile**</dt> <dt>7</dt></span></span> </dl>             | <span data-ttu-id="e9fcf-137">Данные представляют собой имя файла ACL, используемого для хранения списка управления доступом.</span><span class="sxs-lookup"><span data-stu-id="e9fcf-137">The data is the name of the ACL file used to store the ACL.</span></span> <span data-ttu-id="e9fcf-138">Файлы ACL находятся в папке RP *n* .</span><span class="sxs-lookup"><span data-stu-id="e9fcf-138">The ACL files are located in the RP *n* folder.</span></span> <span data-ttu-id="e9fcf-139">Имя файла имеет следующий формат: S *XXXXXXX*. ACL, где *XXXXXXX* — это 7-значное число.</span><span class="sxs-lookup"><span data-stu-id="e9fcf-139">The file name has the following format: S *xxxxxxx*.acl, where *xxxxxxx* is a seven-digit number.</span></span><br/>                                                             |
| <span id="RecordTypeDebugInfo"></span><span id="recordtypedebuginfo"></span><span id="RECORDTYPEDEBUGINFO"></span><dl> <span data-ttu-id="e9fcf-140"><dt>**Рекордтипедебугинфо**</dt> <dt>8</dt></span><span class="sxs-lookup"><span data-stu-id="e9fcf-140"><dt>**RecordTypeDebugInfo**</dt> <dt>8</dt></span></span> </dl>     | <span data-ttu-id="e9fcf-141">Данные представляют собой отладочную информацию для записи журнала изменений.</span><span class="sxs-lookup"><span data-stu-id="e9fcf-141">The data is debug information for the change log entry.</span></span> <span data-ttu-id="e9fcf-142">Формат данных представляет собой структуру **\_ \_ \_ сведений об отладке журнала SR** .</span><span class="sxs-lookup"><span data-stu-id="e9fcf-142">The data format is a **SR\_LOG\_DEBUG\_INFO** structure.</span></span> <span data-ttu-id="e9fcf-143">Дополнительные сведения см. в подразделе "Примечания".</span><span class="sxs-lookup"><span data-stu-id="e9fcf-143">For more information, see Remarks.</span></span><br/>                                                                                                                     |
| <span id="RecordTypeShortName"></span><span id="recordtypeshortname"></span><span id="RECORDTYPESHORTNAME"></span><dl> <span data-ttu-id="e9fcf-144"><dt>**Рекордтипешортнаме**</dt> <dt>9</dt></span><span class="sxs-lookup"><span data-stu-id="e9fcf-144"><dt>**RecordTypeShortName**</dt> <dt>9</dt></span></span> </dl>     | <span data-ttu-id="e9fcf-145">Данные — это короткое имя файла резервной копии.</span><span class="sxs-lookup"><span data-stu-id="e9fcf-145">The data is the short name of the backup file.</span></span><br/>                                                                                                                                                                                                                          |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e9fcf-146">Комментарии</span><span class="sxs-lookup"><span data-stu-id="e9fcf-146">Remarks</span></span>

<span data-ttu-id="e9fcf-147">Структура **\_ \_ \_ сведений об отладке журнала SR** определяется следующим образом.</span><span class="sxs-lookup"><span data-stu-id="e9fcf-147">The **SR\_LOG\_DEBUG\_INFO** structure is defined as follows.</span></span>

``` syntax
typedef struct _SR_LOG_DEBUG_INFO {
    RECORD_HEADER Header;         // log entry header
    HANDLE ThreadId;              // thread identifier
    HANDLE ProcessId;             // process identifier
    ULARGER_INTEGER TimeStamp;    // event time stamp
    CHAR ProcesName[13];          // process name
} SR_LOG_DEBUG_INFO, *PSR_LOG_DEBUG_INFO;
```

## <a name="requirements"></a><span data-ttu-id="e9fcf-148">Требования</span><span class="sxs-lookup"><span data-stu-id="e9fcf-148">Requirements</span></span>



| <span data-ttu-id="e9fcf-149">Требование</span><span class="sxs-lookup"><span data-stu-id="e9fcf-149">Requirement</span></span> | <span data-ttu-id="e9fcf-150">Значение</span><span class="sxs-lookup"><span data-stu-id="e9fcf-150">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="e9fcf-151">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="e9fcf-151">Minimum supported client</span></span><br/> | <span data-ttu-id="e9fcf-152">Только для настольных приложений Windows XP с пакетом обновления 2 \[\]</span><span class="sxs-lookup"><span data-stu-id="e9fcf-152">Windows XP with SP2 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="e9fcf-153">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="e9fcf-153">Minimum supported server</span></span><br/> | <span data-ttu-id="e9fcf-154">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="e9fcf-154">None supported</span></span><br/>                            |
| <span data-ttu-id="e9fcf-155">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="e9fcf-155">End of client support</span></span><br/>    | <span data-ttu-id="e9fcf-156">Windows XP с пакетом обновления 2 (SP2)</span><span class="sxs-lookup"><span data-stu-id="e9fcf-156">Windows XP with SP2</span></span><br/>                       |



 

