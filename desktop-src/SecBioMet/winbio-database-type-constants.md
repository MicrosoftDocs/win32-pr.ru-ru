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
# <a name="winbio_database_type-constants"></a><span data-ttu-id="c1864-103">\_ \_ Константы типа базы данных винбио</span><span class="sxs-lookup"><span data-stu-id="c1864-103">WINBIO\_DATABASE\_TYPE Constants</span></span>

<span data-ttu-id="c1864-104">Следующие флаги можно использовать для элемента **Attributes** структуры [**\_ \_ схемы хранилища винбио**](winbio-storage-schema.md) .</span><span class="sxs-lookup"><span data-stu-id="c1864-104">The following flags can be used for the **Attributes** member of the [**WINBIO\_STORAGE\_SCHEMA**](winbio-storage-schema.md) structure.</span></span>



| <span data-ttu-id="c1864-105">Константа/значение</span><span class="sxs-lookup"><span data-stu-id="c1864-105">Constant/value</span></span>                                                                                                                                                                                                                                                                     | <span data-ttu-id="c1864-106">Описание</span><span class="sxs-lookup"><span data-stu-id="c1864-106">Description</span></span>                                                                                                                  |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------|
| <span id="WINBIO_DATABASE_TYPE_MASK"></span><span id="winbio_database_type_mask"></span><dl> <span data-ttu-id="c1864-107"><dt>**Винбио \_ 0x0000FFFF \_ типа \_ маски базы данных**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="c1864-107"><dt>**WINBIO\_DATABASE\_TYPE\_MASK**</dt> <dt>0x0000FFFF</dt></span></span> </dl>                | <span data-ttu-id="c1864-108">Представляет маску для всех \_ \_ битов типа.</span><span class="sxs-lookup"><span data-stu-id="c1864-108">Represents a mask for all of the \_TYPE\_ bits.</span></span><br/>                                                                   |
| <span id="WINBIO_DATABASE_TYPE_FILE"></span><span id="winbio_database_type_file"></span><dl> <span data-ttu-id="c1864-109"><dt>**Винбио \_ \_ \_ Файл типа базы данных**</dt> <dt>0x00000001</dt></span><span class="sxs-lookup"><span data-stu-id="c1864-109"><dt>**WINBIO\_DATABASE\_TYPE\_FILE**</dt> <dt>0x00000001</dt></span></span> </dl>                | <span data-ttu-id="c1864-110">База данных содержится в файле.</span><span class="sxs-lookup"><span data-stu-id="c1864-110">The database is contained in a file.</span></span><br/>                                                                              |
| <span id="WINBIO_DATABASE_TYPE_DBMS"></span><span id="winbio_database_type_dbms"></span><dl> <span data-ttu-id="c1864-111"><dt>**Винбио \_ Тип базы данных \_ \_ СУБД**</dt> <dt>0x00000002</dt></span><span class="sxs-lookup"><span data-stu-id="c1864-111"><dt>**WINBIO\_DATABASE\_TYPE\_DBMS**</dt> <dt>0x00000002</dt></span></span> </dl>                | <span data-ttu-id="c1864-112">База данных управляется компонентом системы управления внешней базой данных (СУБД), например Microsoft SQL Server.</span><span class="sxs-lookup"><span data-stu-id="c1864-112">The database is managed by an external database management system (DBMS) component, such as Microsoft SQL Server.</span></span><br/> |
| <span id="WINBIO_DATABASE_TYPE_ONCHIP"></span><span id="winbio_database_type_onchip"></span><dl> <span data-ttu-id="c1864-113"><dt>**Винбио \_ \_Тип базы \_ данных**</dt> <dt>onchip</dt></span><span class="sxs-lookup"><span data-stu-id="c1864-113"><dt>**WINBIO\_DATABASE\_TYPE\_ONCHIP**</dt> <dt>0x00000003</dt></span></span> </dl>          | <span data-ttu-id="c1864-114">База данных находится на биометрических датчиках.</span><span class="sxs-lookup"><span data-stu-id="c1864-114">The database resides on the biometric sensor.</span></span><br/>                                                                     |
| <span id="WINBIO_DATABASE_TYPE_SMARTCARD"></span><span id="winbio_database_type_smartcard"></span><dl> <span data-ttu-id="c1864-115"><dt>**Винбио \_ \_Смарт- \_ карта типа базы данных**</dt> <dt>0x00000004</dt></span><span class="sxs-lookup"><span data-stu-id="c1864-115"><dt>**WINBIO\_DATABASE\_TYPE\_SMARTCARD**</dt> <dt>0x00000004</dt></span></span> </dl> | <span data-ttu-id="c1864-116">База данных находится на смарт-карте.</span><span class="sxs-lookup"><span data-stu-id="c1864-116">The database resides on a smart card.</span></span><br/>                                                                             |
| <span id="WINBIO_DATABASE_FLAG_MASK"></span><span id="winbio_database_flag_mask"></span><dl> <span data-ttu-id="c1864-117"><dt>**Винбио \_ 0xFFFF0000 \_ \_ маска флага базы данных**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="c1864-117"><dt>**WINBIO\_DATABASE\_FLAG\_MASK**</dt> <dt>0xFFFF0000</dt></span></span> </dl>                | <span data-ttu-id="c1864-118">Представляет маску для всех \_ битов флагов \_ .</span><span class="sxs-lookup"><span data-stu-id="c1864-118">Represents a mask for all of the \_FLAG\_ bits.</span></span><br/>                                                                   |
| <span id="WINBIO_DATABASE_FLAG_REMOVABLE"></span><span id="winbio_database_flag_removable"></span><dl> <span data-ttu-id="c1864-119"><dt>**Винбио \_ Флаг базы данных \_ \_ съемный**</dt> <dt>0x00010000</dt></span><span class="sxs-lookup"><span data-stu-id="c1864-119"><dt>**WINBIO\_DATABASE\_FLAG\_REMOVABLE**</dt> <dt>0x00010000</dt></span></span> </dl> | <span data-ttu-id="c1864-120">Носитель, содержащий базу данных, можно физически удалить с компьютера.</span><span class="sxs-lookup"><span data-stu-id="c1864-120">The storage medium containing the database can be physically removed from the computer.</span></span><br/>                           |
| <span id="WINBIO_DATABASE_FLAG_REMOTE"></span><span id="winbio_database_flag_remote"></span><dl> <span data-ttu-id="c1864-121"><dt>**Винбио \_ Флаг базы данных \_ \_ Remote**</dt> <dt>0x00020000</dt></span><span class="sxs-lookup"><span data-stu-id="c1864-121"><dt>**WINBIO\_DATABASE\_FLAG\_REMOTE**</dt> <dt>0x00020000</dt></span></span> </dl>          | <span data-ttu-id="c1864-122">База данных находится на удаленном компьютере.</span><span class="sxs-lookup"><span data-stu-id="c1864-122">The database resides on a remote computer.</span></span><br/>                                                                        |



## <a name="requirements"></a><span data-ttu-id="c1864-123">Требования</span><span class="sxs-lookup"><span data-stu-id="c1864-123">Requirements</span></span>



| <span data-ttu-id="c1864-124">Требование</span><span class="sxs-lookup"><span data-stu-id="c1864-124">Requirement</span></span> | <span data-ttu-id="c1864-125">Значение</span><span class="sxs-lookup"><span data-stu-id="c1864-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c1864-126">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="c1864-126">Minimum supported client</span></span><br/> | <span data-ttu-id="c1864-127">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="c1864-127">Windows 7 \[desktop apps only\]</span></span><br/>                                                                    |
| <span data-ttu-id="c1864-128">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="c1864-128">Minimum supported server</span></span><br/> | <span data-ttu-id="c1864-129">Только классические приложения Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="c1864-129">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="c1864-130">Header</span><span class="sxs-lookup"><span data-stu-id="c1864-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="c1864-131"><dt>Винбио \_ types. h (include винбио. h)</dt></span><span class="sxs-lookup"><span data-stu-id="c1864-131"><dt>Winbio\_types.h (include Winbio.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c1864-132">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c1864-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c1864-133">Константы клиентского приложения</span><span class="sxs-lookup"><span data-stu-id="c1864-133">Client Application Constants</span></span>](client-application-constants.md)
</dt> </dl>

 

 





