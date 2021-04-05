---
description: Представляет атрибут имени файла. Файл имеет один атрибут имени файла для каждого каталога, в котором он указан.
ms.assetid: 54458eee-b786-446c-80bd-213c13bdeb4a
title: Структура FILE_NAME
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FILE_NAME
api_type:
- NA
api_location: ''
ms.openlocfilehash: 609725c21f0c0811a4222cd9dfd662b3e25673f3
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104072345"
---
# <a name="file_name-structure"></a>\_Структура имени файла

\[Эта структура допустима только для томов NTFS версии 3; Он может быть изменен в будущих версиях.\]

Представляет атрибут имени файла. Файл имеет один атрибут имени файла для каждого каталога, в котором он указан.

## <a name="syntax"></a>Синтаксис


```C++
typedef struct _FILE_NAME {
  FILE_REFERENCE ParentDirectory;
  UCHAR          Reserved[0x38];
  UCHAR          FileNameLength;
  UCHAR          Flags;
  WCHAR          FileName[1];
} FILE_NAME, *PFILE_NAME;
```



## <a name="members"></a>Члены

<dl> <dt>

**парентдиректори**
</dt> <dd>

Ссылка на файл каталога, который индексируется по этому имени. См [**. \_ \_ Справочник по сегментам MFT**](mft-segment-reference.md).

</dd> <dt>

**Reserved**
</dt> <dd>

Зарезервировано.

</dd> <dt>

**филенамеленгс**
</dt> <dd>

Длина имени файла в символах Юникода.

</dd> <dt>

**Флаги**
</dt> <dd>

Флаги имени файла.

<dl> <dt>

<span id="FILE_NAME_NTFS"></span><span id="file_name_ntfs"></span>**Файл \_ ИМЯ \_ NTFS** (0x01)
</dt> <dt>

<span id="FILE_NAME_DOS"></span><span id="file_name_dos"></span>**Файл \_ ИМЯ \_ DOS** (0x02)
</dt> </dl> </dd> <dt>

**FileName**
</dt> <dd>

Первый символ имени файла.

</dd> </dl>

## <a name="remarks"></a>Комментарии

Обратите внимание, что для этой структуры нет связанного файла заголовка.

Это определение структуры допустимо только для основной версии 3 и дополнительной версии 0 или 1, как сообщается [**фсктл \_ Получение \_ \_ \_ данных тома NTFS**](/windows/win32/api/winioctl/ni-winioctl-fsctl_get_ntfs_volume_data).

## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Основная таблица файлов](master-file-table.md)
</dt> </dl>

 

 
