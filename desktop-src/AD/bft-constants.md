---
title: Константы БФТ (Нтдсбкли. h)
description: Константы БФТ используются в качестве битовых флагов для обнаружения различных типов файлов в резервной копии служб домен Active Directory Services.
ms.assetid: 3658a657-d9e3-4fbf-9120-4b0205b81a36
ms.tgt_platform: multiple
topic_type:
- apiref
api_name:
- BFT_LOG_DIRECTORY
- BFT_DATABASE_DIRECTORY
- BFT_DIRECTORY
- BFT_LOG
- BFT_LOG_DIR
- BFT_CHECKPOINT_DIR
- BFT_NTDS_DATABASE
- BFT_PATCH_FILE
- BFT_UNKNOWN
api_location:
- Ntdsbcli.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9607b5e61e5689d8895b39a11aa7e813fc7fcbe6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988499"
---
# <a name="bft-constants"></a>Константы БФТ

Константы БФТ используются в качестве битовых флагов для обнаружения различных типов файлов в резервной копии служб домен Active Directory Services.

<dl> <dt>

<span id="BFT_LOG_DIRECTORY"></span><span id="bft_log_directory"></span>**\_Каталог журналов \_ БФТ**
</dt> <dd> <dl> <dt>

0x20
</dt> <dt>



Файл принадлежит каталогу журнала.


</dt> </dl> </dd> <dt>

<span id="BFT_DATABASE_DIRECTORY"></span><span id="bft_database_directory"></span>**\_Каталог базы данных БФТ \_**
</dt> <dd> <dl> <dt>

0x40
</dt> <dt>



Файл принадлежит каталогу базы данных.


</dt> </dl> </dd> <dt>

<span id="BFT_DIRECTORY"></span><span id="bft_directory"></span>**\_Каталог БФТ**
</dt> <dd> <dl> <dt>

0x80
</dt> <dt>



Указанный путь является каталогом, а не именем файла.


</dt> </dl> </dd> <dt>

<span id="BFT_LOG"></span><span id="bft_log"></span>**\_Журнал БФТ**
</dt> <dd> <dl> <dt>

0x21
</dt> <dt>



Указывает файл журнала, который принадлежит каталогу журнала.


</dt> </dl> </dd> <dt>

<span id="BFT_LOG_DIR"></span><span id="bft_log_dir"></span>**БФТ \_ log \_ dir**
</dt> <dd> <dl> <dt>

0x22
</dt> <dt>



Файл — это путь к каталогу журнала.


</dt> </dl> </dd> <dt>

<span id="BFT_CHECKPOINT_DIR"></span><span id="bft_checkpoint_dir"></span>**\_dir Checkpoint \_ БФТ**
</dt> <dd> <dl> <dt>

0x23
</dt> <dt>



Файл — это путь к каталогу контрольных точек.


</dt> </dl> </dd> <dt>

<span id="BFT_NTDS_DATABASE"></span><span id="bft_ntds_database"></span>**\_ \_ база данных NTDS БФТ**
</dt> <dd> <dl> <dt>

0x44
</dt> <dt>



Этот файл является базой данных службы каталогов, которая принадлежит каталогу базы данных.


</dt> </dl> </dd> <dt>

<span id="BFT_PATCH_FILE"></span><span id="bft_patch_file"></span>**\_файл исправления \_ БФТ**
</dt> <dd> <dl> <dt>

0x25
</dt> <dt>



Файл является файлом исправления, который принадлежит каталогу журнала.


</dt> </dl> </dd> <dt>

<span id="BFT_UNKNOWN"></span><span id="bft_unknown"></span>**БФТ \_ неизвестный**
</dt> <dd> <dl> <dt>

0x0F
</dt> <dt>



Не удается распознать файл. Файл не совпадает с известными именами файлов и типами файлов.


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows Vista<br/>                                                              |
| Минимальная версия сервера<br/> | Windows Server 2008<br/>                                                        |
| Header<br/>                   | <dl> <dt>Нтдсбкли. h</dt> </dl> |



 

 





