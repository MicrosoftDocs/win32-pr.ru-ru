---
description: Открывает базу данных оболочек совместимости.
ms.assetid: ece1bd39-20a1-42e6-8e2b-1d38f7223d42
title: Функция Сдбинитдатабасе
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbInitDatabase
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: 7a3c63fa712aec988dbf13c4fb7f9fddbf159fdd
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104495924"
---
# <a name="sdbinitdatabase-function"></a><span data-ttu-id="65e7d-103">Функция Сдбинитдатабасе</span><span class="sxs-lookup"><span data-stu-id="65e7d-103">SdbInitDatabase function</span></span>

<span data-ttu-id="65e7d-104">Открывает базу данных оболочек совместимости.</span><span class="sxs-lookup"><span data-stu-id="65e7d-104">Opens the shim database.</span></span>

## <a name="syntax"></a><span data-ttu-id="65e7d-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="65e7d-105">Syntax</span></span>


```C++
HSDB WINAPI SdbInitDatabase(
  _In_ DWORD   dwFlags,
  _In_ LPCTSTR pszDatabasePath
);
```



## <a name="parameters"></a><span data-ttu-id="65e7d-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="65e7d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="65e7d-107">*dwFlags* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="65e7d-107">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="65e7d-108">Этот параметр задает формат пути в параметре *псздатабасепас* .</span><span class="sxs-lookup"><span data-stu-id="65e7d-108">This parameter specifies the format of the path in the *pszDatabasePath* parameter.</span></span> <span data-ttu-id="65e7d-109">Может быть одним из указанных далее.</span><span class="sxs-lookup"><span data-stu-id="65e7d-109">It can be one of the following values.</span></span>



| <span data-ttu-id="65e7d-110">Значение</span><span class="sxs-lookup"><span data-stu-id="65e7d-110">Value</span></span>                                                                                                                                                                                                                                                      | <span data-ttu-id="65e7d-111">Значение</span><span class="sxs-lookup"><span data-stu-id="65e7d-111">Meaning</span></span>                                                                                                |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| <span id="HID_DOS_PATHS"></span><span id="hid_dos_paths"></span><dl> <span data-ttu-id="65e7d-112"><dt>**HID \_ \_Пути к DOS**</dt> <dt>0x00000001</dt></span><span class="sxs-lookup"><span data-stu-id="65e7d-112"><dt>**HID\_DOS\_PATHS**</dt> <dt>0x00000001</dt></span></span> </dl>                             | <span data-ttu-id="65e7d-113">Путь в стиле MS-DOS.</span><span class="sxs-lookup"><span data-stu-id="65e7d-113">An MS-DOS style path.</span></span><br/>                                                                       |
| <span id="HID_DATABASE_FULLPATH"></span><span id="hid_database_fullpath"></span><dl> <span data-ttu-id="65e7d-114"><dt>**HID \_ \_FullPath, база данных**</dt> , <dt>0x00000002</dt></span><span class="sxs-lookup"><span data-stu-id="65e7d-114"><dt>**HID\_DATABASE\_FULLPATH**</dt> <dt>0x00000002</dt></span></span> </dl>     | <span data-ttu-id="65e7d-115">Полный путь.</span><span class="sxs-lookup"><span data-stu-id="65e7d-115">A full path.</span></span><br/>                                                                                |
| <span id="HID_NO_DATABASE"></span><span id="hid_no_database"></span><dl> <span data-ttu-id="65e7d-116"><dt>**HID \_ БЕЗ \_ базы данных**</dt> <dt>0x00000004</dt></span><span class="sxs-lookup"><span data-stu-id="65e7d-116"><dt>**HID\_NO\_DATABASE**</dt> <dt>0x00000004</dt></span></span> </dl>                       | <span data-ttu-id="65e7d-117">Параметр *псздатабасепас* игнорируется, и база данных не открывается.</span><span class="sxs-lookup"><span data-stu-id="65e7d-117">The *pszDatabasePath* parameter is ignored and no database is opened.</span></span><br/>                       |
| <span id="HID_DATABASE_TYPE_MASK"></span><span id="hid_database_type_mask"></span><dl> <span data-ttu-id="65e7d-118"><dt>**HID \_ 0xF00F0000 \_ типа \_ маски базы данных**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="65e7d-118"><dt>**HID\_DATABASE\_TYPE\_MASK**</dt> <dt>0xF00F0000</dt></span></span> </dl> | <span data-ttu-id="65e7d-119">Этот параметр указывает предопределенную базу данных.</span><span class="sxs-lookup"><span data-stu-id="65e7d-119">This parameter specifies a predefined database.</span></span> <span data-ttu-id="65e7d-120">Параметр *псздатабасепас* игнорируется.</span><span class="sxs-lookup"><span data-stu-id="65e7d-120">The *pszDatabasePath* parameter is ignored.</span></span><br/> |



 

<span data-ttu-id="65e7d-121">Если *dwFlags* содержит **\_ \_ \_ маску типа данных HID**, этот параметр также может включать одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="65e7d-121">If *dwFlags* contains **HID\_DATA\_TYPE\_MASK**, this parameter can also include one of the following values.</span></span>



| <span data-ttu-id="65e7d-122">Значение</span><span class="sxs-lookup"><span data-stu-id="65e7d-122">Value</span></span>                                                                                                                                                                                                                                                               | <span data-ttu-id="65e7d-123">Значение</span><span class="sxs-lookup"><span data-stu-id="65e7d-123">Meaning</span></span>                                       |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------|
| <span id="SDB_DATABASE_MAIN_SHIM"></span><span id="sdb_database_main_shim"></span><dl> <span data-ttu-id="65e7d-124"><dt>**SDB \_ \_Основная \_ оболочка СОВМЕСТИМОСТИ базы данных**</dt> <dt>0x80030000</dt></span><span class="sxs-lookup"><span data-stu-id="65e7d-124"><dt>**SDB\_DATABASE\_MAIN\_SHIM**</dt> <dt>0x80030000</dt></span></span> </dl>          | <span data-ttu-id="65e7d-125">База данных оболочки совместимости приложений.</span><span class="sxs-lookup"><span data-stu-id="65e7d-125">Application shim database.</span></span><br/>         |
| <span id="SDB_DATABASE_MAIN_MSI"></span><span id="sdb_database_main_msi"></span><dl> <span data-ttu-id="65e7d-126"><dt>**SDB \_ Основной 0x80020000 базы данных \_ \_ MSI**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="65e7d-126"><dt>**SDB\_DATABASE\_MAIN\_MSI**</dt> <dt>0x80020000</dt></span></span> </dl>             | <span data-ttu-id="65e7d-127">База данных MSI.</span><span class="sxs-lookup"><span data-stu-id="65e7d-127">MSI database.</span></span><br/>                      |
| <span id="SDB_DATABASE_MAIN_DRIVERS"></span><span id="sdb_database_main_drivers"></span><dl> <span data-ttu-id="65e7d-128"><dt>**SDB \_ \_Основные \_ драйверы базы данных**</dt> <dt>0x80040000</dt></span><span class="sxs-lookup"><span data-stu-id="65e7d-128"><dt>**SDB\_DATABASE\_MAIN\_DRIVERS**</dt> <dt>0x80040000</dt></span></span> </dl> | <span data-ttu-id="65e7d-129">База данных драйверов для блокировки.</span><span class="sxs-lookup"><span data-stu-id="65e7d-129">Database of drivers to be blocked.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="65e7d-130">*псздатабасепас* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="65e7d-130">*pszDatabasePath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="65e7d-131">Путь к базе данных.</span><span class="sxs-lookup"><span data-stu-id="65e7d-131">The path to the database.</span></span> <span data-ttu-id="65e7d-132">Этот параметр может иметь **значение NULL** , если параметр *dwFlags* указывает предопределенную базу данных.</span><span class="sxs-lookup"><span data-stu-id="65e7d-132">This parameter can be **NULL** if the *dwFlags* parameter specifies a predefined database.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="65e7d-133">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="65e7d-133">Return value</span></span>

<span data-ttu-id="65e7d-134">Функция возвращает маркер открытой базы данных.</span><span class="sxs-lookup"><span data-stu-id="65e7d-134">The function returns a handle to the opened database.</span></span>

## <a name="requirements"></a><span data-ttu-id="65e7d-135">Требования</span><span class="sxs-lookup"><span data-stu-id="65e7d-135">Requirements</span></span>



| <span data-ttu-id="65e7d-136">Требование</span><span class="sxs-lookup"><span data-stu-id="65e7d-136">Requirement</span></span> | <span data-ttu-id="65e7d-137">Значение</span><span class="sxs-lookup"><span data-stu-id="65e7d-137">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="65e7d-138">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="65e7d-138">Minimum supported client</span></span><br/> | <span data-ttu-id="65e7d-139">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="65e7d-139">Windows XP \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="65e7d-140">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="65e7d-140">Minimum supported server</span></span><br/> | <span data-ttu-id="65e7d-141">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="65e7d-141">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="65e7d-142">DLL</span><span class="sxs-lookup"><span data-stu-id="65e7d-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="65e7d-143"><dt>Apphelp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="65e7d-143"><dt>Apphelp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="65e7d-144">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="65e7d-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="65e7d-145">**сдбжетапппатчдир**</span><span class="sxs-lookup"><span data-stu-id="65e7d-145">**SdbGetAppPatchDir**</span></span>](sdbgetapppatchdir.md)
</dt> <dt>

[<span data-ttu-id="65e7d-146">**сдбжетматчинжексе**</span><span class="sxs-lookup"><span data-stu-id="65e7d-146">**SdbGetMatchingExe**</span></span>](sdbgetmatchingexe.md)
</dt> <dt>

[<span data-ttu-id="65e7d-147">**сдбрелеасематчинжексе**</span><span class="sxs-lookup"><span data-stu-id="65e7d-147">**SdbReleaseMatchingExe**</span></span>](sdbreleasematchingexe.md)
</dt> <dt>

[<span data-ttu-id="65e7d-148">**сдбтагрефтотагид**</span><span class="sxs-lookup"><span data-stu-id="65e7d-148">**SdbTagRefToTagID**</span></span>](sdbtagreftotagid.md)
</dt> </dl>

 

 




