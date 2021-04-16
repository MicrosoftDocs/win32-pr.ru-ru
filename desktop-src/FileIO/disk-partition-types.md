---
description: Допустимые типы разделов, используемые драйверами дисков.
ms.assetid: b2e15b93-a02b-4d6f-b242-b5ec9a30c97b
title: Типы разделов диска (Виниоктл. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4109d4386d4892ca695fe8876b61501110cef455
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105664279"
---
# <a name="disk-partition-types"></a>Типы разделов диска

В следующей таблице указаны допустимые типы разделов, используемые драйверами дисков.



| Константа/значение                                                                                                                                                                                                                                      | Описание                                                                                                                                                |
|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="PARTITION_ENTRY_UNUSED"></span><span id="partition_entry_unused"></span><dl> <dt>**Раздел \_ \_Неиспользуемая запись**</dt> <dt>0x00</dt> </dl> | Неиспользуемая Секция записи.<br/>                                                                                                                      |
| <span id="PARTITION_EXTENDED"></span><span id="partition_extended"></span><dl> <dt>**Раздел \_ Расширенные**</dt> <dt>0x05</dt> </dl>              | Дополнительный раздел.<br/>                                                                                                                          |
| <span id="PARTITION_FAT_12"></span><span id="partition_fat_12"></span><dl> <dt>**Раздел \_ FAT \_ 12**</dt> <dt>0x01</dt> </dl>                   | Раздел FAT12 файловой системы.<br/>                                                                                                                  |
| <span id="PARTITION_FAT_16"></span><span id="partition_fat_16"></span><dl> <dt>**Раздел \_ 0x04 FAT \_ 16**</dt> <dt></dt> </dl>                   | Раздел файловой системы FAT16.<br/>                                                                                                                  |
| <span id="PARTITION_FAT32"></span><span id="partition_fat32"></span><dl> <dt>**Раздел \_**</dt> <dt>0x0B</dt> FAT32 </dl>                       | Раздел файловой системы FAT32.<br/>                                                                                                                  |
| <span id="PARTITION_IFS"></span><span id="partition_ifs"></span><dl> <dt>**Раздел \_**</dt> <dt>0x07</dt> IFS </dl>                             | Раздел IFS.<br/>                                                                                                                               |
| <span id="PARTITION_LDM"></span><span id="partition_ldm"></span><dl> <dt>**Раздел \_**</dt> <dt>0x42</dt> LDM </dl>                             | Раздел диспетчера логических дисков (LDM).<br/>                                                                                                         |
| <span id="PARTITION_NTFT"></span><span id="partition_ntft"></span><dl> <dt>**Раздел \_ НТФТ**</dt> <dt>0x80</dt> </dl>                          | Секция НТФТ.<br/>                                                                                                                              |
| <span id="VALID_NTFT"></span><span id="valid_ntft"></span><dl> <dt>**Допустимое \_ НТФТ**</dt> <dt>0xC0</dt> </dl>                                      | Допустимая Секция НТФТ.<br/> Старший бит кода типа секции указывает на то, что Секция является частью зеркального или чередующегося массива НТФТ.<br/> |



## <a name="remarks"></a>Комментарии

Существует несколько макросов, которые могут помочь при обнаружении типа раздела: **исконтаинерпартитион**, **исфтпартитион** и **исрекогнизедпартитион**. Дополнительные сведения см. в разделе Виниоктл. h.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows XP\]<br/>                                                               |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2003\]<br/>                                                      |
| Header<br/>                   | <dl> <dt>Виниоктл. h (включение Windows. h)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**\_сведения о разделах, \_ например**](/windows/desktop/api/WinIoCtl/ns-winioctl-partition_information_ex)
</dt> <dt>

[**\_ \_ Основная загрузочная запись о разделах**](/windows/desktop/api/WinIoCtl/ns-winioctl-partition_information_mbr)
</dt> <dt>

[**Задание \_ \_ сведений о секции**](/windows/desktop/api/WinIoCtl/ns-winioctl-set_partition_information)
</dt> </dl>

 

 




