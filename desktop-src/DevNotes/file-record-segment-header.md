---
description: Представляет сегмент записи файла. Это заголовок для каждого сегмента записи файла в главной таблице файлов (MFT).
ms.assetid: 4548ad49-1924-4888-8966-c45f8e453c6f
title: Структура FILE_RECORD_SEGMENT_HEADER
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FILE_RECORD_SEGMENT_HEADER
api_type:
- NA
api_location: ''
ms.openlocfilehash: 0c9d7a3653ad965141e691546866f599d8615f5f12feb92fa25c861d7c429b74
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119260604"
---
# <a name="file_record_segment_header-structure"></a>\_ \_ Структура заголовка сегмента записи файла \_

\[Эта структура допустима только для томов NTFS версии 3; Он может быть изменен в будущих версиях.\]

Представляет сегмент записи файла. Это заголовок для каждого сегмента записи файла в главной таблице файлов (MFT).

## <a name="syntax"></a>Синтаксис


```C++
typedef struct _FILE_RECORD_SEGMENT_HEADER {
  MULTI_SECTOR_HEADER   MultiSectorHeader;
  ULONGLONG             Reserved1;
  USHORT                SequenceNumber;
  USHORT                Reserved2;
  USHORT                FirstAttributeOffset;
  USHORT                Flags;
  ULONG                 Reserved3[2];
  FILE_REFERENCE        BaseFileRecordSegment;
  USHORT                Reserved4;
  UPDATE_SEQUENCE_ARRAY UpdateSequenceArray;
} FILE_RECORD_SEGMENT_HEADER, *PFILE_RECORD_SEGMENT_HEADER;
```



## <a name="members"></a>Члены

<dl> <dt>

**мултисекторхеадер**
</dt> <dd>

Заголовок в многосекционе, определенный диспетчером кэша. Структура [**\_ \_ заголовка с несколькими секторами**](multi-sector-header.md) всегда содержит подпись "File" и описание расположения и размера массива последовательностей обновления.

</dd> <dt>

**Reserved1**
</dt> <dd>

Зарезервировано.

</dd> <dt>

**SequenceNumber**
</dt> <dd>

Порядковый номер. Это значение увеличивается каждый раз при освобождении сегмента записи файла; значение 0, если сегмент не используется. Поле **SequenceNumber** в ссылке на файл должно соответствовать содержимому этого поля; Если они не совпадают, ссылка на файл неверна и, вероятно, устарела.

</dd> <dt>

**Зарезервировано 2**
</dt> <dd>

Зарезервировано.

</dd> <dt>

**фирстаттрибутеоффсет**
</dt> <dd>

Смещение первой записи атрибута в байтах.

</dd> <dt>

**Флаги**
</dt> <dd>

Флаги файла.

<dl> <dt>

<span id="FILE_RECORD_SEGMENT_IN_USE"></span><span id="file_record_segment_in_use"></span>**Файл \_ \_ \_ \_ Используемый сегмент записи** (0x0001)
</dt> <dt>

<span id="FILE_FILE_NAME_INDEX_PRESENT"></span><span id="file_file_name_index_present"></span>**Файл \_ \_ \_ \_ Имеется индекс имени файла** (0x0002)
</dt> </dl> </dd> <dt>

**Reserved3**
</dt> <dd>

Зарезервировано.

</dd> <dt>

**басефилерекордсегмент**
</dt> <dd>

Ссылка на файл основного сегмента записи файла для этого файла. Если это базовая запись файла, значение равно 0. См [**. \_ \_ Справочник по сегментам MFT**](mft-segment-reference.md).

</dd> <dt>

**Reserved4**
</dt> <dd>

Зарезервировано.

</dd> <dt>

**упдатесекуенцеаррай**
</dt> <dd>

Массив последовательностей обновления для защиты многосекционных передач сегмента записи файла.

</dd> </dl>

## <a name="remarks"></a>Remarks

Обратите внимание, что для этой структуры нет связанного файла заголовка.

Это определение структуры допустимо только для основной версии 3 и дополнительной версии 0 или 1, как сообщается [**фсктл \_ Получение \_ \_ \_ данных тома NTFS**](/windows/win32/api/winioctl/ni-winioctl-fsctl_get_ntfs_volume_data).

## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Основная таблица файлов](master-file-table.md)
</dt> </dl>

 

 
