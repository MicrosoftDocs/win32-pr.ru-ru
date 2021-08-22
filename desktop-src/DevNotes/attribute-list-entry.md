---
description: Представляет запись в списке атрибутов.
ms.assetid: daa0c97d-2ebe-4e14-b1f8-e4be3075b13e
title: Структура ATTRIBUTE_LIST_ENTRY
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ATTRIBUTE_LIST_ENTRY
api_type:
- NA
api_location: ''
ms.openlocfilehash: 0c0154de52dbefa6d29278ca05e924db6f6c1d84b124fe21b3092e728a0d07fa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118956143"
---
# <a name="attribute_list_entry-structure"></a>\_ \_ Структура ввода списка атрибутов

\[Эта структура допустима только для томов NTFS версии 3; Он может быть изменен в будущих версиях.\]

Представляет запись в списке атрибутов.

## <a name="syntax"></a>Синтаксис


```C++
typedef struct _ATTRIBUTE_LIST_ENTRY {
  ATTRIBUTE_TYPE_CODE   AttributeTypeCode;
  USHORT                RecordLength;
  UCHAR                 AttributeNameLength;
  UCHAR                 AttributeNameOffset;
  VCN                   LowestVcn;
  MFT_SEGMENT_REFERENCE SegmentReference;
  USHORT                Reserved;
  WCHAR                 AttributeName[1];
} ATTRIBUTE_LIST_ENTRY, *PATTRIBUTE_LIST_ENTRY;
```



## <a name="members"></a>Члены

<dl> <dt>

**аттрибутетипекоде**
</dt> <dd>

Код типа атрибута.



| Значение                                                                                                                                                                                                                                           | Значение                                                                                                                                     |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="_STANDARD_INFORMATION"></span><span id="_standard_information"></span><dl> <dt>**$Standard \_ СВЕДЕНИЯ**</dt> <dt>0x10</dt> </dl> | Атрибуты файлов (например, только для чтения и архивация), метки времени (например, создание файла и Последнее изменение) и число жестких связей.<br/> |
| <span id="_ATTRIBUTE_LIST"></span><span id="_attribute_list"></span><dl> <dt>**$Attribute \_ Список**</dt> <dt>0x20</dt> </dl>                   | Список атрибутов, образующих файл, и ссылка на файл записи MFT, в которой расположен каждый атрибут.<br/>     |
| <span id="_FILE_NAME"></span><span id="_file_name"></span><dl> <dt>**$File \_ ИМЯ**</dt> <dt>0x30</dt> </dl>                                  | Имя файла в символах Юникода.<br/>                                                                                     |
| <span id="_OBJECT_ID"></span><span id="_object_id"></span><dl> <dt>**$Object \_ Идентификатор**</dt> <dt>0x40</dt> </dl>                                  | 16-байтовый идентификатор объекта, назначенный службой отслеживания ссылок.<br/>                                                              |
| <span id="_VOLUME_NAME"></span><span id="_volume_name"></span><dl> <dt>**$Volume \_ ИМЯ**</dt> <dt>0x60</dt> </dl>                            | Метка тома. Содержится в файле $Volume.<br/>                                                                                   |
| <span id="_VOLUME_INFORMATION"></span><span id="_volume_information"></span><dl> <dt>**$Volume \_ СВЕДЕНИЯ**</dt> <dt>0x70</dt> </dl>       | Сведения о томе. Содержится в файле $Volume.<br/>                                                                             |
| <span id="_DATA"></span><span id="_data"></span><dl> <dt>**$Data**</dt> <dt>0x80</dt> </dl>                                                  | Содержимое файла.<br/>                                                                                                        |
| <span id="_INDEX_ROOT"></span><span id="_index_root"></span><dl> <dt>**$Index \_ КОРНЕВой**</dt> <dt>0x90</dt> </dl>                               | Используется для реализации выделения имен файлов для больших каталогов.<br/>                                                                     |
| <span id="_INDEX_ALLOCATION"></span><span id="_index_allocation"></span><dl> <dt>**$Index \_**</dt> <dt>0x82</dt> выделения </dl>             | Используется для реализации выделения имен файлов для больших каталогов.<br/>                                                                     |
| <span id="_BITMAP"></span><span id="_bitmap"></span><dl> <dt>**$Bitmap**</dt> <dt>0xB0</dt> </dl>                                            | Индекс точечного рисунка для большого каталога.<br/>                                                                                            |
| <span id="_REPARSE_POINT"></span><span id="_reparse_point"></span><dl> <dt>**$REPARSE \_ ТОЧКА**</dt> <dt>0xC0</dt> </dl>                      | Данные точки повторного анализа.<br/>                                                                                                          |



 

</dd> <dt>

**RecordLength**
</dt> <dd>

Размер этой структуры, а также необязательный буфер имен в байтах.

</dd> <dt>

**аттрибутенамеленгс**
</dt> <dd>

Размер необязательного имени атрибута в символах. Если имя существует, это значение не равно нулю, а структура сразу после строки в Юникоде указанного числа символов.

</dd> <dt>

**аттрибутенамеоффсет**
</dt> <dd>

Зарезервировано.

</dd> <dt>

**ловествкн**
</dt> <dd>

Наименьший номер виртуального кластера (VCN) для этого атрибута. Этот элемент равен нулю, если атрибуту не требуется несколько сегментов записи файла и если эта запись не является ссылкой на сегмент, отличный от первого. В этом случае это значение является наименьшим значением VCN, описанным в упоминаемом сегменте.

</dd> <dt>

**сегментреференце**
</dt> <dd>

Сегмент основной таблицы файлов (MFT), в котором находится атрибут. См [**. \_ \_ Справочник по сегментам MFT**](mft-segment-reference.md).

</dd> <dt>

**Reserved**
</dt> <dd>

Зарезервировано.

</dd> <dt>

**AttributeName**
</dt> <dd>

Начало необязательного имени атрибута.

</dd> </dl>

## <a name="remarks"></a>Remarks

Список Attributes представляет собой упорядоченный список структур **\_ \_ элементов списка атрибутов** с куадворд по рассогласованию. Этот список сначала упорядочивается по коду типа атрибута, а затем по имени атрибута (если он есть). Ни один из двух атрибутов не может иметь одинаковый код типа, имя и наименьшее значение VCN. Таким образом, может существовать не более одного атрибута для каждого кода типа без имени.

Это определение структуры допустимо только для основной версии 3 и дополнительной версии 0 или 1, как сообщается [**фсктл \_ Получение \_ \_ \_ данных тома NTFS**](/windows/win32/api/winioctl/ni-winioctl-fsctl_get_ntfs_volume_data).

Обратите внимание, что для этой структуры нет связанного файла заголовка.

## <a name="see-also"></a>См. также

<dl> <dt>

[Основная таблица файлов](master-file-table.md)
</dt> </dl>

 

 
