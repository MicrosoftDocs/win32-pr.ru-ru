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
# <a name="shim-database-types"></a><span data-ttu-id="51524-103">Типы баз данных оболочек совместимости</span><span class="sxs-lookup"><span data-stu-id="51524-103">Shim Database Types</span></span>

<span data-ttu-id="51524-104">Представляет типы для основных и пользовательских баз данных оболочек совместимости.</span><span class="sxs-lookup"><span data-stu-id="51524-104">Represent the types for main and custom shim databases.</span></span>



| <span data-ttu-id="51524-105">Константа/значение</span><span class="sxs-lookup"><span data-stu-id="51524-105">Constant/value</span></span>                                                                                                                                                                                                                                                | <span data-ttu-id="51524-106">Описание</span><span class="sxs-lookup"><span data-stu-id="51524-106">Description</span></span>                                                                                   |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------|
| <span id="SDB_DATABASE_MAIN"></span><span id="sdb_database_main"></span><dl> <span data-ttu-id="51524-107"><dt>**SDB \_ \_Основной 0X80000000 базы данных**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="51524-107"><dt>**SDB\_DATABASE\_MAIN**</dt> <dt>0x80000000</dt></span></span> </dl>                    | <span data-ttu-id="51524-108">Основная база данных.</span><span class="sxs-lookup"><span data-stu-id="51524-108">The main database.</span></span> <span data-ttu-id="51524-109">Если этот флаг отсутствует, база данных является пользовательской базой данных.</span><span class="sxs-lookup"><span data-stu-id="51524-109">If this flag is not present, the database is a custom database.</span></span><br/> |
| <span id="SDB_DATABASE_SHIM"></span><span id="sdb_database_shim"></span><dl> <span data-ttu-id="51524-110"><dt>**SDB \_ \_Оболочка совместимости базы данных**</dt> <dt>0x00010000</dt></span><span class="sxs-lookup"><span data-stu-id="51524-110"><dt>**SDB\_DATABASE\_SHIM**</dt> <dt>0x00010000</dt></span></span> </dl>                    | <span data-ttu-id="51524-111">База данных содержит записи приложений, которые будут оболочкой совместимости.</span><span class="sxs-lookup"><span data-stu-id="51524-111">The database contains application entries to be shimmed.</span></span><br/>                           |
| <span id="SDB_DATABASE_MSI"></span><span id="sdb_database_msi"></span><dl> <span data-ttu-id="51524-112"><dt>**SDB \_ 0x00020000 \_ MSI базы данных**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="51524-112"><dt>**SDB\_DATABASE\_MSI**</dt> <dt>0x00020000</dt></span></span> </dl>                       | <span data-ttu-id="51524-113">База данных содержит записи MSI.</span><span class="sxs-lookup"><span data-stu-id="51524-113">The database contains MSI entries.</span></span><br/>                                                 |
| <span id="SDB_DATABASE_DRIVERS"></span><span id="sdb_database_drivers"></span><dl> <span data-ttu-id="51524-114"><dt>**SDB \_ \_Драйверы базы данных**</dt> <dt>0x00040000</dt></span><span class="sxs-lookup"><span data-stu-id="51524-114"><dt>**SDB\_DATABASE\_DRIVERS**</dt> <dt>0x00040000</dt></span></span> </dl>           | <span data-ttu-id="51524-115">База данных содержит записи блока драйвера.</span><span class="sxs-lookup"><span data-stu-id="51524-115">The database contains driver block entries.</span></span><br/>                                        |
| <span id="SDB_DATABASE_DETAILS"></span><span id="sdb_database_details"></span><dl> <span data-ttu-id="51524-116"><dt>**SDB \_ \_Сведения о базе данных**</dt> <dt>0x00080000</dt></span><span class="sxs-lookup"><span data-stu-id="51524-116"><dt>**SDB\_DATABASE\_DETAILS**</dt> <dt>0x00080000</dt></span></span> </dl>           | <span data-ttu-id="51524-117">База данных содержит сведения о AppHelp.</span><span class="sxs-lookup"><span data-stu-id="51524-117">The database contains Apphelp details.</span></span><br/>                                             |
| <span id="SDB_DATABASE_SP_DETAILS"></span><span id="sdb_database_sp_details"></span><dl> <span data-ttu-id="51524-118"><dt>**SDB \_ \_ \_ Сведения о SP для базы данных**</dt> <dt>0x00100000</dt></span><span class="sxs-lookup"><span data-stu-id="51524-118"><dt>**SDB\_DATABASE\_SP\_DETAILS**</dt> <dt>0x00100000</dt></span></span> </dl> | <span data-ttu-id="51524-119">База данных содержит сведения о AppHelp SP.</span><span class="sxs-lookup"><span data-stu-id="51524-119">The database contains SP Apphelp details.</span></span><br/>                                          |
| <span id="SDB_DATABASE_RESOURCE"></span><span id="sdb_database_resource"></span><dl> <span data-ttu-id="51524-120"><dt>**SDB \_ 0x00200000 \_ ресурсов базы данных**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="51524-120"><dt>**SDB\_DATABASE\_RESOURCE**</dt> <dt>0x00200000</dt></span></span> </dl>        | <span data-ttu-id="51524-121">Библиотека ресурсов содержит сведения о AppHelp.</span><span class="sxs-lookup"><span data-stu-id="51524-121">The resource DLL contains Apphelp details.</span></span><br/>                                         |
| <span id="SDB_DATABASE_TYPE_MASK"></span><span id="sdb_database_type_mask"></span><dl> <span data-ttu-id="51524-122"><dt>**SDB \_ 0xF02F0000 \_ типа \_ маски базы данных**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="51524-122"><dt>**SDB\_DATABASE\_TYPE\_MASK**</dt> <dt>0xF02F0000</dt></span></span> </dl>    | <span data-ttu-id="51524-123">Маска, используемая для извлечения сведений о основной базе данных.</span><span class="sxs-lookup"><span data-stu-id="51524-123">A mask used to extract main database information.</span></span><br/>                                  |
| <span id="SDB_DATABASE_MAIN_SHIM"></span><span id="sdb_database_main_shim"></span><dl> <span data-ttu-id="51524-124"><dt>**\_ \_ основная оболочка совместимости sdbй базы данных \_**</dt></span><span class="sxs-lookup"><span data-stu-id="51524-124"><dt>**SDB\_DATABASE\_MAIN\_SHIM**</dt></span></span> </dl>                                                                    | <span data-ttu-id="51524-125">база данных с \_ \_ оболочкой совместимости SDB базы данных файл \| \_ \_ MSI \| \_ \_ SDB Database</span><span class="sxs-lookup"><span data-stu-id="51524-125">SDB\_DATABASE\_SHIM \| SDB\_DATABASE\_MSI \| SDB\_DATABASE\_MAIN</span></span><br/>                   |
| <span id="SDB_DATABASE_MAIN_MSI"></span><span id="sdb_database_main_msi"></span><dl> <span data-ttu-id="51524-126"><dt>**\_ \_ основной MSI базы данных sdb \_**</dt></span><span class="sxs-lookup"><span data-stu-id="51524-126"><dt>**SDB\_DATABASE\_MAIN\_MSI**</dt></span></span> </dl>                                                                       | <span data-ttu-id="51524-127">\_основная база \_ \| данных MSI \_ SDB \_ база данных</span><span class="sxs-lookup"><span data-stu-id="51524-127">SDB\_DATABASE\_MSI \| SDB\_DATABASE\_MAIN</span></span><br/>                                          |
| <span id="SDB_DATABASE_MAIN_DRIVERS"></span><span id="sdb_database_main_drivers"></span><dl> <span data-ttu-id="51524-128"><dt>**\_ \_ основные драйверы SDB базы данных \_**</dt></span><span class="sxs-lookup"><span data-stu-id="51524-128"><dt>**SDB\_DATABASE\_MAIN\_DRIVERS**</dt></span></span> </dl>                                                           | <span data-ttu-id="51524-129">\_драйвер базы данных sdb, \_ \| \_ основная база данных \_</span><span class="sxs-lookup"><span data-stu-id="51524-129">SDB\_DATABASE\_DRIVERS \| SDB\_DATABASE\_MAIN</span></span><br/>                                      |
| <span id="SDB_DATABASE_MAIN_DETAILS"></span><span id="sdb_database_main_details"></span><dl> <span data-ttu-id="51524-130"><dt>**\_ \_ основные \_ сведения о базе данных sdb**</dt></span><span class="sxs-lookup"><span data-stu-id="51524-130"><dt>**SDB\_DATABASE\_MAIN\_DETAILS**</dt></span></span> </dl>                                                           | <span data-ttu-id="51524-131">\_сведения о базе данных sdb база \_ \| \_ данных sdb \_</span><span class="sxs-lookup"><span data-stu-id="51524-131">SDB\_DATABASE\_DETAILS \| SDB\_DATABASE\_MAIN</span></span><br/>                                      |
| <span id="SDB_DATABASE_MAIN_SP_DETAILS"></span><span id="sdb_database_main_sp_details"></span><dl> <span data-ttu-id="51524-132"><dt>**\_ \_ основные \_ \_ сведения о SP базы данных sdb**</dt></span><span class="sxs-lookup"><span data-stu-id="51524-132"><dt>**SDB\_DATABASE\_MAIN\_SP\_DETAILS**</dt></span></span> </dl>                                                 | <span data-ttu-id="51524-133">\_ \_ \_ подробные сведения о пакете \| обновления \_ для базы данных sdb \_</span><span class="sxs-lookup"><span data-stu-id="51524-133">SDB\_DATABASE\_SP\_DETAILS \| SDB\_DATABASE\_MAIN</span></span><br/>                                  |
| <span id="SDB_DATABASE_MAIN_RESOURCE"></span><span id="sdb_database_main_resource"></span><dl> <span data-ttu-id="51524-134"><dt>**\_ \_ основной ресурс базы данных sdb \_**</dt></span><span class="sxs-lookup"><span data-stu-id="51524-134"><dt>**SDB\_DATABASE\_MAIN\_RESOURCE**</dt></span></span> </dl>                                                        | <span data-ttu-id="51524-135">база данных sdb Resource БД, \_ \_ \| \_ \_ Главная</span><span class="sxs-lookup"><span data-stu-id="51524-135">SDB\_DATABASE\_RESOURCE \| SDB\_DATABASE\_MAIN</span></span><br/>                                     |



## <a name="requirements"></a><span data-ttu-id="51524-136">Требования</span><span class="sxs-lookup"><span data-stu-id="51524-136">Requirements</span></span>



| <span data-ttu-id="51524-137">Требование</span><span class="sxs-lookup"><span data-stu-id="51524-137">Requirement</span></span> | <span data-ttu-id="51524-138">Значение</span><span class="sxs-lookup"><span data-stu-id="51524-138">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="51524-139">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="51524-139">Minimum supported client</span></span><br/> | <span data-ttu-id="51524-140">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="51524-140">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="51524-141">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="51524-141">Minimum supported server</span></span><br/> | <span data-ttu-id="51524-142">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="51524-142">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="51524-143">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="51524-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="51524-144">**сдбопендатабасе**</span><span class="sxs-lookup"><span data-stu-id="51524-144">**SdbOpenDatabase**</span></span>](sdbopendatabase.md)
</dt> </dl>

 

 




