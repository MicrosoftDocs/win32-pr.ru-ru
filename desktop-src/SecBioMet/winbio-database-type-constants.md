---
title: Константы WINBIO_DATABASE_TYPE (Винбио \_ types. h)
description: Флаги, которые могут использоваться для элемента Attributes \_ \_ структуры схемы хранилища винбио.
ms.assetid: 07e7e91c-3ca6-41cd-a2c7-ac43bb5156a6
topic_type:
- apiref
api_name:
- WINBIO_DATABASE_TYPE_MASK
- WINBIO_DATABASE_TYPE_FILE
- WINBIO_DATABASE_TYPE_DBMS
- WINBIO_DATABASE_TYPE_ONCHIP
- WINBIO_DATABASE_TYPE_SMARTCARD
- WINBIO_DATABASE_FLAG_MASK
- WINBIO_DATABASE_FLAG_REMOVABLE
- WINBIO_DATABASE_FLAG_REMOTE
api_location:
- Winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: acd67f49c5fa689fb4418789aae7c4d6c9a305a8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103802296"
---
# <a name="winbio_database_type-constants"></a>\_ \_ Константы типа базы данных винбио

Следующие флаги можно использовать для элемента **Attributes** структуры [**\_ \_ схемы хранилища винбио**](winbio-storage-schema.md) .



| Константа/значение                                                                                                                                                                                                                                                                     | Описание                                                                                                                  |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------|
| <span id="WINBIO_DATABASE_TYPE_MASK"></span><span id="winbio_database_type_mask"></span><dl> <dt>**Винбио \_ 0x0000FFFF \_ типа \_ маски базы данных**</dt> <dt></dt> </dl>                | Представляет маску для всех \_ \_ битов типа.<br/>                                                                   |
| <span id="WINBIO_DATABASE_TYPE_FILE"></span><span id="winbio_database_type_file"></span><dl> <dt>**Винбио \_ \_ \_ Файл типа базы данных**</dt> <dt>0x00000001</dt> </dl>                | База данных содержится в файле.<br/>                                                                              |
| <span id="WINBIO_DATABASE_TYPE_DBMS"></span><span id="winbio_database_type_dbms"></span><dl> <dt>**Винбио \_ Тип базы данных \_ \_ СУБД**</dt> <dt>0x00000002</dt> </dl>                | База данных управляется компонентом системы управления внешней базой данных (СУБД), например Microsoft SQL Server.<br/> |
| <span id="WINBIO_DATABASE_TYPE_ONCHIP"></span><span id="winbio_database_type_onchip"></span><dl> <dt>**Винбио \_ \_Тип базы \_ данных**</dt> <dt>onchip</dt> </dl>          | База данных находится на биометрических датчиках.<br/>                                                                     |
| <span id="WINBIO_DATABASE_TYPE_SMARTCARD"></span><span id="winbio_database_type_smartcard"></span><dl> <dt>**Винбио \_ \_Смарт- \_ карта типа базы данных**</dt> <dt>0x00000004</dt> </dl> | База данных находится на смарт-карте.<br/>                                                                             |
| <span id="WINBIO_DATABASE_FLAG_MASK"></span><span id="winbio_database_flag_mask"></span><dl> <dt>**Винбио \_ 0xFFFF0000 \_ \_ маска флага базы данных**</dt> <dt></dt> </dl>                | Представляет маску для всех \_ битов флагов \_ .<br/>                                                                   |
| <span id="WINBIO_DATABASE_FLAG_REMOVABLE"></span><span id="winbio_database_flag_removable"></span><dl> <dt>**Винбио \_ Флаг базы данных \_ \_ съемный**</dt> <dt>0x00010000</dt> </dl> | Носитель, содержащий базу данных, можно физически удалить с компьютера.<br/>                           |
| <span id="WINBIO_DATABASE_FLAG_REMOTE"></span><span id="winbio_database_flag_remote"></span><dl> <dt>**Винбио \_ Флаг базы данных \_ \_ Remote**</dt> <dt>0x00020000</dt> </dl>          | База данных находится на удаленном компьютере.<br/>                                                                        |



## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | \[Только классические приложения Windows 7\]<br/>                                                                    |
| Минимальная версия сервера<br/> | Только классические приложения Windows Server 2008 R2 \[\]<br/>                                                       |
| Header<br/>                   | <dl> <dt>Винбио \_ types. h (include винбио. h)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Константы клиентского приложения](client-application-constants.md)
</dt> </dl>

 

 





