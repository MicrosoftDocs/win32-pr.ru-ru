---
description: Представляет адрес в основной таблице файлов (MFT). Адрес помечается с помощью циклического повторно используемого порядкового номера, который задается в момент, когда ссылка на сегмент MFT является допустимой.
ms.assetid: 59d83b95-83fb-4630-8ce4-f58441c748ab
title: Структура MFT_SEGMENT_REFERENCE
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MFT_SEGMENT_REFERENCE
api_type:
- NA
api_location: ''
ms.openlocfilehash: beabe7620dadd01b25b3556715b33e2f10c2c230
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104140747"
---
# <a name="mft_segment_reference-structure"></a>\_ \_ Структура ссылки на сегмент MFT

\[Эта структура допустима только для томов NTFS версии 3; Он может быть изменен в будущих версиях.\]

Представляет адрес в основной таблице файлов (MFT). Адрес помечается с помощью циклического повторно используемого порядкового номера, который задается в момент, когда ссылка на сегмент MFT является допустимой.

## <a name="syntax"></a>Синтаксис


```C++
typedef struct _MFT_SEGMENT_REFERENCE {
  ULONG  SegmentNumberLowPart;
  USHORT SegmentNumberHighPart;
  USHORT SequenceNumber;
} MFT_SEGMENT_REFERENCE, *PMFT_SEGMENT_REFERENCE;
```



## <a name="members"></a>Члены

<dl> <dt>

**сегментнумберловпарт**
</dt> <dd>

Нижняя часть номера сегмента.

</dd> <dt>

**сегментнумберхигхпарт**
</dt> <dd>

Старшая часть номера сегмента.

</dd> <dt>

**SequenceNumber**
</dt> <dd>

Ненулевой порядковый номер. Значение 0 зарезервировано.

</dd> </dl>

## <a name="remarks"></a>Комментарии

Обратите внимание, что для этой структуры нет связанного файла заголовка.

Это определение структуры допустимо только для основной версии 3 и дополнительной версии 0 или 1, как сообщается [**фсктл \_ Получение \_ \_ \_ данных тома NTFS**](/windows/win32/api/winioctl/ni-winioctl-fsctl_get_ntfs_volume_data).

Тип **данных \_ ссылки на файл** определяется следующим образом.

``` syntax
typedef MFT_SEGMENT_REFERENCE FILE_REFERENCE, *PFILE_REFERENCE;
```

## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Основная таблица файлов](master-file-table.md)
</dt> </dl>

 

 
