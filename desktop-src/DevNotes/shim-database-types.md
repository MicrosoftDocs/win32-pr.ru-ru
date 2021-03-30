---
description: Представляет типы для основных и пользовательских баз данных оболочек совместимости.
ms.assetid: e893963a-6130-4f65-b925-6f3d292fc86d
title: Типы баз данных оболочек совместимости
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 789265ea945ce068d2b0b74e3358582d5e4ccd78
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103806905"
---
# <a name="shim-database-types"></a>Типы баз данных оболочек совместимости

Представляет типы для основных и пользовательских баз данных оболочек совместимости.



| Константа/значение                                                                                                                                                                                                                                                | Описание                                                                                   |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------|
| <span id="SDB_DATABASE_MAIN"></span><span id="sdb_database_main"></span><dl> <dt>**SDB \_ \_Основной 0X80000000 базы данных**</dt> <dt></dt> </dl>                    | Основная база данных. Если этот флаг отсутствует, база данных является пользовательской базой данных.<br/> |
| <span id="SDB_DATABASE_SHIM"></span><span id="sdb_database_shim"></span><dl> <dt>**SDB \_ \_Оболочка совместимости базы данных**</dt> <dt>0x00010000</dt> </dl>                    | База данных содержит записи приложений, которые будут оболочкой совместимости.<br/>                           |
| <span id="SDB_DATABASE_MSI"></span><span id="sdb_database_msi"></span><dl> <dt>**SDB \_ 0x00020000 \_ MSI базы данных**</dt> <dt></dt> </dl>                       | База данных содержит записи MSI.<br/>                                                 |
| <span id="SDB_DATABASE_DRIVERS"></span><span id="sdb_database_drivers"></span><dl> <dt>**SDB \_ \_Драйверы базы данных**</dt> <dt>0x00040000</dt> </dl>           | База данных содержит записи блока драйвера.<br/>                                        |
| <span id="SDB_DATABASE_DETAILS"></span><span id="sdb_database_details"></span><dl> <dt>**SDB \_ \_Сведения о базе данных**</dt> <dt>0x00080000</dt> </dl>           | База данных содержит сведения о AppHelp.<br/>                                             |
| <span id="SDB_DATABASE_SP_DETAILS"></span><span id="sdb_database_sp_details"></span><dl> <dt>**SDB \_ \_ \_ Сведения о SP для базы данных**</dt> <dt>0x00100000</dt> </dl> | База данных содержит сведения о AppHelp SP.<br/>                                          |
| <span id="SDB_DATABASE_RESOURCE"></span><span id="sdb_database_resource"></span><dl> <dt>**SDB \_ 0x00200000 \_ ресурсов базы данных**</dt> <dt></dt> </dl>        | Библиотека ресурсов содержит сведения о AppHelp.<br/>                                         |
| <span id="SDB_DATABASE_TYPE_MASK"></span><span id="sdb_database_type_mask"></span><dl> <dt>**SDB \_ 0xF02F0000 \_ типа \_ маски базы данных**</dt> <dt></dt> </dl>    | Маска, используемая для извлечения сведений о основной базе данных.<br/>                                  |
| <span id="SDB_DATABASE_MAIN_SHIM"></span><span id="sdb_database_main_shim"></span><dl> <dt>**\_ \_ основная оболочка совместимости sdbй базы данных \_**</dt> </dl>                                                                    | база данных с \_ \_ оболочкой совместимости SDB базы данных файл \| \_ \_ MSI \| \_ \_ SDB Database<br/>                   |
| <span id="SDB_DATABASE_MAIN_MSI"></span><span id="sdb_database_main_msi"></span><dl> <dt>**\_ \_ основной MSI базы данных sdb \_**</dt> </dl>                                                                       | \_основная база \_ \| данных MSI \_ SDB \_ база данных<br/>                                          |
| <span id="SDB_DATABASE_MAIN_DRIVERS"></span><span id="sdb_database_main_drivers"></span><dl> <dt>**\_ \_ основные драйверы SDB базы данных \_**</dt> </dl>                                                           | \_драйвер базы данных sdb, \_ \| \_ основная база данных \_<br/>                                      |
| <span id="SDB_DATABASE_MAIN_DETAILS"></span><span id="sdb_database_main_details"></span><dl> <dt>**\_ \_ основные \_ сведения о базе данных sdb**</dt> </dl>                                                           | \_сведения о базе данных sdb база \_ \| \_ данных sdb \_<br/>                                      |
| <span id="SDB_DATABASE_MAIN_SP_DETAILS"></span><span id="sdb_database_main_sp_details"></span><dl> <dt>**\_ \_ основные \_ \_ сведения о SP базы данных sdb**</dt> </dl>                                                 | \_ \_ \_ подробные сведения о пакете \| обновления \_ для базы данных sdb \_<br/>                                  |
| <span id="SDB_DATABASE_MAIN_RESOURCE"></span><span id="sdb_database_main_resource"></span><dl> <dt>**\_ \_ основной ресурс базы данных sdb \_**</dt> </dl>                                                        | база данных sdb Resource БД, \_ \_ \| \_ \_ Главная<br/>                                     |



## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>       |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2008\]<br/> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**сдбопендатабасе**](sdbopendatabase.md)
</dt> </dl>

 

 




