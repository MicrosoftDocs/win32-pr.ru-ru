---
title: Структура WINBIO_STORAGE_SCHEMA (Винбио \_ types. h)
description: Описание возможностей адаптера биометрического хранилища.
ms.assetid: e4924803-5a1b-4e0a-b2cb-01d018d27ba1
keywords:
- API структуры WINBIO_STORAGE_SCHEMA биометрическая платформа Windows
- PWINBIO_STORAGE_SCHEMA API биометрическая платформа Windows указателя структуры
topic_type:
- apiref
api_name:
- WINBIO_STORAGE_SCHEMA
api_location:
- Winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 28db23d55a7b3e43caaae5a88ca4bbf32fdf1178
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105661983"
---
# <a name="winbio_storage_schema-structure"></a><span data-ttu-id="b42d4-105">\_ \_ Структура схемы хранилища винбио</span><span class="sxs-lookup"><span data-stu-id="b42d4-105">WINBIO\_STORAGE\_SCHEMA structure</span></span>

<span data-ttu-id="b42d4-106">Структура **\_ \_ схемы хранилища винбио** описывает возможности использования адаптера биометрического хранилища.</span><span class="sxs-lookup"><span data-stu-id="b42d4-106">The **WINBIO\_STORAGE\_SCHEMA** structure describes the capabilities of a biometric storage adapter.</span></span> <span data-ttu-id="b42d4-107">Эта структура используется функцией [**винбиоенумдатабасес**](/windows/desktop/api/Winbio/nf-winbio-winbioenumdatabases) .</span><span class="sxs-lookup"><span data-stu-id="b42d4-107">This structure is used by the [**WinBioEnumDatabases**](/windows/desktop/api/Winbio/nf-winbio-winbioenumdatabases) function.</span></span>

## <a name="syntax"></a><span data-ttu-id="b42d4-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b42d4-108">Syntax</span></span>


```C++
typedef struct _WINBIO_STORAGE_SCHEMA {
  WINBIO_BIOMETRIC_TYPE BiometricFactor;
  WINBIO_UUID           DatabaseId;
  WINBIO_UUID           DataFormat;
  ULONG                 Attributes;
  WINBIO_STRING         FilePath;
  WINBIO_STRING         ConnectionString;
} WINBIO_STORAGE_SCHEMA, *PWINBIO_STORAGE_SCHEMA;
```



## <a name="members"></a><span data-ttu-id="b42d4-109">Члены</span><span class="sxs-lookup"><span data-stu-id="b42d4-109">Members</span></span>

<dl> <dt>

<span data-ttu-id="b42d4-110">**биометрикфактор**</span><span class="sxs-lookup"><span data-stu-id="b42d4-110">**BiometricFactor**</span></span>
</dt> <dd>

<span data-ttu-id="b42d4-111">Тип биометрического измерения, сохраненный в базе данных.</span><span class="sxs-lookup"><span data-stu-id="b42d4-111">The type of biometric measurement saved in the database.</span></span>

</dd> <dt>

<span data-ttu-id="b42d4-112">**DatabaseId**</span><span class="sxs-lookup"><span data-stu-id="b42d4-112">**DatabaseId**</span></span>
</dt> <dd>

<span data-ttu-id="b42d4-113">Идентификатор GUID, идентифицирующий базу данных.</span><span class="sxs-lookup"><span data-stu-id="b42d4-113">A GUID that identifies the database.</span></span>

</dd> <dt>

<span data-ttu-id="b42d4-114">**DataFormat**</span><span class="sxs-lookup"><span data-stu-id="b42d4-114">**DataFormat**</span></span>
</dt> <dd>

<span data-ttu-id="b42d4-115">Идентификатор GUID, определяющий формат шаблонов в базе данных.</span><span class="sxs-lookup"><span data-stu-id="b42d4-115">A GUID that identifies the format of the templates in the database.</span></span>

</dd> <dt>

<span data-ttu-id="b42d4-116">**Атрибуты**</span><span class="sxs-lookup"><span data-stu-id="b42d4-116">**Attributes**</span></span>
</dt> <dd>

<span data-ttu-id="b42d4-117">Сведения о характеристиках базы данных.</span><span class="sxs-lookup"><span data-stu-id="b42d4-117">Information about the characteristics of the database.</span></span> <span data-ttu-id="b42d4-118">Это может быть побитовое **или** для следующих констант.</span><span class="sxs-lookup"><span data-stu-id="b42d4-118">This can be a bitwise **OR** of the following constants.</span></span>



| <span data-ttu-id="b42d4-119">Значение</span><span class="sxs-lookup"><span data-stu-id="b42d4-119">Value</span></span>                                                                                                                                                                                                                                                                              | <span data-ttu-id="b42d4-120">Значение</span><span class="sxs-lookup"><span data-stu-id="b42d4-120">Meaning</span></span>                                                             |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------|
| <span id="WINBIO_DATABASE_FLAG_MASK"></span><span id="winbio_database_flag_mask"></span><dl> <span data-ttu-id="b42d4-121"><dt>**Винбио \_ 0xFFFF0000 \_ \_ маска флага базы данных**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="b42d4-121"><dt>**WINBIO\_DATABASE\_FLAG\_MASK**</dt> <dt>0xFFFF0000</dt></span></span> </dl>                | <span data-ttu-id="b42d4-122">Представляет маску для битов флагов.</span><span class="sxs-lookup"><span data-stu-id="b42d4-122">Represents a mask for the flag bits.</span></span><br/>                     |
| <span id="WINBIO_DATABASE_FLAG_REMOTE"></span><span id="winbio_database_flag_remote"></span><dl> <span data-ttu-id="b42d4-123"><dt>**Винбио \_ Флаг базы данных \_ \_ Remote**</dt> <dt>0x00020000</dt></span><span class="sxs-lookup"><span data-stu-id="b42d4-123"><dt>**WINBIO\_DATABASE\_FLAG\_REMOTE**</dt> <dt>0x00020000</dt></span></span> </dl>          | <span data-ttu-id="b42d4-124">База данных находится на удаленном компьютере.</span><span class="sxs-lookup"><span data-stu-id="b42d4-124">The database resides on a remote computer.</span></span><br/>               |
| <span id="WINBIO_DATABASE_FLAG_REMOVABLE"></span><span id="winbio_database_flag_removable"></span><dl> <span data-ttu-id="b42d4-125"><dt>**Винбио \_ Флаг базы данных \_ \_ съемный**</dt> <dt>0x00010000</dt></span><span class="sxs-lookup"><span data-stu-id="b42d4-125"><dt>**WINBIO\_DATABASE\_FLAG\_REMOVABLE**</dt> <dt>0x00010000</dt></span></span> </dl> | <span data-ttu-id="b42d4-126">База данных находится на съемном носителе.</span><span class="sxs-lookup"><span data-stu-id="b42d4-126">The database resides on a removable drive.</span></span><br/>               |
| <span id="WINBIO_DATABASE_TYPE_DBMS"></span><span id="winbio_database_type_dbms"></span><dl> <span data-ttu-id="b42d4-127"><dt>**Винбио \_ Тип базы данных \_ \_ СУБД**</dt> <dt>0x00000002</dt></span><span class="sxs-lookup"><span data-stu-id="b42d4-127"><dt>**WINBIO\_DATABASE\_TYPE\_DBMS**</dt> <dt>0x00000002</dt></span></span> </dl>                | <span data-ttu-id="b42d4-128">База данных управляется системой управления базами данных.</span><span class="sxs-lookup"><span data-stu-id="b42d4-128">The database is managed by a database management system.</span></span><br/> |
| <span id="WINBIO_DATABASE_TYPE_FILE"></span><span id="winbio_database_type_file"></span><dl> <span data-ttu-id="b42d4-129"><dt>**Винбио \_ \_ \_ Файл типа базы данных**</dt> <dt>0x00000001</dt></span><span class="sxs-lookup"><span data-stu-id="b42d4-129"><dt>**WINBIO\_DATABASE\_TYPE\_FILE**</dt> <dt>0x00000001</dt></span></span> </dl>                | <span data-ttu-id="b42d4-130">База данных содержится в файле.</span><span class="sxs-lookup"><span data-stu-id="b42d4-130">The database is contained in a file.</span></span><br/>                     |
| <span id="WINBIO_DATABASE_TYPE_MASK"></span><span id="winbio_database_type_mask"></span><dl> <span data-ttu-id="b42d4-131"><dt>**Винбио \_ 0x0000FFFF \_ типа \_ маски базы данных**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="b42d4-131"><dt>**WINBIO\_DATABASE\_TYPE\_MASK**</dt> <dt>0x0000FFFF</dt></span></span> </dl>                | <span data-ttu-id="b42d4-132">Представляет маску для битов типа.</span><span class="sxs-lookup"><span data-stu-id="b42d4-132">Represents a mask for the type bits.</span></span><br/>                     |
| <span id="WINBIO_DATABASE_TYPE_ONCHIP"></span><span id="winbio_database_type_onchip"></span><dl> <span data-ttu-id="b42d4-133"><dt>**Винбио \_ \_Тип базы \_ данных**</dt> <dt>onchip</dt></span><span class="sxs-lookup"><span data-stu-id="b42d4-133"><dt>**WINBIO\_DATABASE\_TYPE\_ONCHIP**</dt> <dt>0x00000003</dt></span></span> </dl>          | <span data-ttu-id="b42d4-134">База данных находится на биометрических датчиках.</span><span class="sxs-lookup"><span data-stu-id="b42d4-134">The database resides on the biometric sensor.</span></span><br/>            |
| <span id="WINBIO_DATABASE_TYPE_SMARTCARD"></span><span id="winbio_database_type_smartcard"></span><dl> <span data-ttu-id="b42d4-135"><dt>**Винбио \_ \_Смарт- \_ карта типа базы данных**</dt> <dt>0x00000004</dt></span><span class="sxs-lookup"><span data-stu-id="b42d4-135"><dt>**WINBIO\_DATABASE\_TYPE\_SMARTCARD**</dt> <dt>0x00000004</dt></span></span> </dl> | <span data-ttu-id="b42d4-136">База данных находится на смарт-карте.</span><span class="sxs-lookup"><span data-stu-id="b42d4-136">The database resides on a smart card.</span></span><br/>                    |



 

</dd> <dt>

<span data-ttu-id="b42d4-137">**Равно**</span><span class="sxs-lookup"><span data-stu-id="b42d4-137">**FilePath**</span></span>
</dt> <dd>

<span data-ttu-id="b42d4-138">Путь и имя файла базы данных, если она находится на диске компьютера.</span><span class="sxs-lookup"><span data-stu-id="b42d4-138">The path and file name of the database if it resides on the computer disk.</span></span>

</dd> <dt>

<span data-ttu-id="b42d4-139">**ConnectionString**</span><span class="sxs-lookup"><span data-stu-id="b42d4-139">**ConnectionString**</span></span>
</dt> <dd>

<span data-ttu-id="b42d4-140">Строковое значение, которое может быть отправлено на сервер базы данных для обнаружения базы данных.</span><span class="sxs-lookup"><span data-stu-id="b42d4-140">A string value that can be sent to a database server to identify the database.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="b42d4-141">Требования</span><span class="sxs-lookup"><span data-stu-id="b42d4-141">Requirements</span></span>



| <span data-ttu-id="b42d4-142">Требование</span><span class="sxs-lookup"><span data-stu-id="b42d4-142">Requirement</span></span> | <span data-ttu-id="b42d4-143">Значение</span><span class="sxs-lookup"><span data-stu-id="b42d4-143">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b42d4-144">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="b42d4-144">Minimum supported client</span></span><br/> | <span data-ttu-id="b42d4-145">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="b42d4-145">Windows 7 \[desktop apps only\]</span></span><br/>                                                                    |
| <span data-ttu-id="b42d4-146">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="b42d4-146">Minimum supported server</span></span><br/> | <span data-ttu-id="b42d4-147">Только классические приложения Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="b42d4-147">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="b42d4-148">Header</span><span class="sxs-lookup"><span data-stu-id="b42d4-148">Header</span></span><br/>                   | <dl> <span data-ttu-id="b42d4-149"><dt>Винбио \_ types. h (include винбио. h)</dt></span><span class="sxs-lookup"><span data-stu-id="b42d4-149"><dt>Winbio\_types.h (include Winbio.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b42d4-150">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b42d4-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b42d4-151">Структуры клиентских приложений</span><span class="sxs-lookup"><span data-stu-id="b42d4-151">Client Application Structures</span></span>](client-application-structures.md)
</dt> <dt>

[<span data-ttu-id="b42d4-152">**винбиоенумдатабасес**</span><span class="sxs-lookup"><span data-stu-id="b42d4-152">**WinBioEnumDatabases**</span></span>](/windows/desktop/api/Winbio/nf-winbio-winbioenumdatabases)
</dt> </dl>

 

 





