---
description: Метод Опендатабасе объекта Installer открывает существующую базу данных или создает новую, возвращая объект базы данных. Он выдает ошибку, если не удается успешно создать и открыть объект базы данных.
ms.assetid: a77b3954-db27-41a0-8f8b-2654766bde6a
title: Метод Installer. Опендатабасе
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.OpenDatabase
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 897e683fd56ce3e7496dd945ee068a9e6f0c0f77
ms.sourcegitcommit: 91110c16e4713ed82d7fb80562d3ddf40b5d76b2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/14/2021
ms.locfileid: "107492273"
---
# <a name="installeropendatabase-method"></a><span data-ttu-id="05c7d-104">Метод Installer. Опендатабасе</span><span class="sxs-lookup"><span data-stu-id="05c7d-104">Installer.OpenDatabase method</span></span>

<span data-ttu-id="05c7d-105">Метод **опендатабасе** объекта [**Installer**](installer-object.md) открывает существующую базу данных или создает новую, возвращая объект [**базы данных**](database-object.md) .</span><span class="sxs-lookup"><span data-stu-id="05c7d-105">The **OpenDatabase** method of the [**Installer**](installer-object.md) object opens an existing database or creates a new one, returning a [**Database**](database-object.md) object.</span></span> <span data-ttu-id="05c7d-106">Он выдает ошибку, если не удается успешно создать и открыть объект **базы данных** .</span><span class="sxs-lookup"><span data-stu-id="05c7d-106">It generates an error if the **Database** object cannot be successfully created and opened.</span></span>

## <a name="syntax"></a><span data-ttu-id="05c7d-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="05c7d-107">Syntax</span></span>


```JScript
Installer.OpenDatabase(
  name,
  openMode
)
```



## <a name="parameters"></a><span data-ttu-id="05c7d-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="05c7d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="05c7d-109">*name*</span><span class="sxs-lookup"><span data-stu-id="05c7d-109">*name*</span></span> 
</dt> <dd>

<span data-ttu-id="05c7d-110">Обязательная строка, содержащая имя пути к базе данных.</span><span class="sxs-lookup"><span data-stu-id="05c7d-110">Required string that contains the path name of the database.</span></span> <span data-ttu-id="05c7d-111">Если указана пустая строка, создается временная база данных, которая не сохраняется.</span><span class="sxs-lookup"><span data-stu-id="05c7d-111">If an empty string is supplied, a temporary database is created that is not persisted.</span></span>

</dd> <dt>

<span data-ttu-id="05c7d-112">*openMode*</span><span class="sxs-lookup"><span data-stu-id="05c7d-112">*openMode*</span></span> 
</dt> <dd>

<span data-ttu-id="05c7d-113">Параметр из следующего списка или строка, содержащая имя нового файла выходной базы данных, в который необходимо выполнить запись после фиксации.</span><span class="sxs-lookup"><span data-stu-id="05c7d-113">A parameter from the following list or a string that contains the path name of the new output database file that is to be written to upon commit.</span></span>



| <span data-ttu-id="05c7d-114">Параметр</span><span class="sxs-lookup"><span data-stu-id="05c7d-114">Parameter</span></span>                                                                                                                                                                                                                                                                                                                   | <span data-ttu-id="05c7d-115">Значение</span><span class="sxs-lookup"><span data-stu-id="05c7d-115">Meaning</span></span>                                                                                                                                                                 |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="msiOpenDatabaseModeReadOnly"></span><span id="msiopendatabasemodereadonly"></span><span id="MSIOPENDATABASEMODEREADONLY"></span><dl> <span data-ttu-id="05c7d-116"><dt>**мсиопендатабасемодереадонли**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="05c7d-116"><dt>**msiOpenDatabaseModeReadOnly**</dt> <dt>0</dt></span></span> </dl>                 | <span data-ttu-id="05c7d-117">Открывает базу данных только для чтения без постоянных изменений.</span><span class="sxs-lookup"><span data-stu-id="05c7d-117">Opens a database read-only, no persistent changes.</span></span><br/>                                                                                                           |
| <span id="msiOpenDatabaseModeTransact"></span><span id="msiopendatabasemodetransact"></span><span id="MSIOPENDATABASEMODETRANSACT"></span><dl> <span data-ttu-id="05c7d-118"><dt>**мсиопендатабасемодетрансакт**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="05c7d-118"><dt>**msiOpenDatabaseModeTransact**</dt> <dt>1</dt></span></span> </dl>                 | <span data-ttu-id="05c7d-119">Открывает базу данных для чтения и записи в режиме транзакций.</span><span class="sxs-lookup"><span data-stu-id="05c7d-119">Opens a database read/write in transaction mode.</span></span><br/>                                                                                                             |
| <span id="msiOpenDatabaseModeDirect"></span><span id="msiopendatabasemodedirect"></span><span id="MSIOPENDATABASEMODEDIRECT"></span><dl> <span data-ttu-id="05c7d-120"><dt>**мсиопендатабасемодедирект**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="05c7d-120"><dt>**msiOpenDatabaseModeDirect**</dt> <dt>2</dt></span></span> </dl>                         | <span data-ttu-id="05c7d-121">Открывает базу данных с прямым чтением и записью без транзакции.</span><span class="sxs-lookup"><span data-stu-id="05c7d-121">Opens a database direct read/write without transaction.</span></span><br/>                                                                                                      |
| <span id="msiOpenDatabaseModeCreate"></span><span id="msiopendatabasemodecreate"></span><span id="MSIOPENDATABASEMODECREATE"></span><dl> <span data-ttu-id="05c7d-122"><dt>**мсиопендатабасемодекреате**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="05c7d-122"><dt>**msiOpenDatabaseModeCreate**</dt> <dt>3</dt></span></span> </dl>                         | <span data-ttu-id="05c7d-123">Создает новую базу данных, доступную для чтения и записи в режиме Transact.</span><span class="sxs-lookup"><span data-stu-id="05c7d-123">Creates a new database, transact mode read/write.</span></span><br/>                                                                                                            |
| <span id="msiOpenDatabaseModeCreateDirect"></span><span id="msiopendatabasemodecreatedirect"></span><span id="MSIOPENDATABASEMODECREATEDIRECT"></span><dl> <span data-ttu-id="05c7d-124"><dt>**мсиопендатабасемодекреатедирект**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="05c7d-124"><dt>**msiOpenDatabaseModeCreateDirect**</dt> <dt>4</dt></span></span> </dl> | <span data-ttu-id="05c7d-125">Создает новую базу данных, прямой режим — чтение и запись.</span><span class="sxs-lookup"><span data-stu-id="05c7d-125">Creates a new database, direct mode read/write.</span></span><br/>                                                                                                              |
| <span id="msiOpenDatabaseModeListScript"></span><span id="msiopendatabasemodelistscript"></span><span id="MSIOPENDATABASEMODELISTSCRIPT"></span><dl> <span data-ttu-id="05c7d-126"><dt>**мсиопендатабасемоделистскрипт**</dt> <dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="05c7d-126"><dt>**msiOpenDatabaseModeListScript**</dt> <dt>5</dt></span></span> </dl>         | <span data-ttu-id="05c7d-127">Открывает базу данных для просмотра файлов скриптов объявления, например файлов, создаваемых методом [**креатеадвертисескрипт**](installer-createadvertisescript.md) .</span><span class="sxs-lookup"><span data-stu-id="05c7d-127">Opens a database to view advertise script files, such as the files generated by the [**CreateAdvertiseScript**](installer-createadvertisescript.md) method.</span></span><br/> |
| <span id="msiOpenDatabaseModePatchFile"></span><span id="msiopendatabasemodepatchfile"></span><span id="MSIOPENDATABASEMODEPATCHFILE"></span><dl> <span data-ttu-id="05c7d-128"><dt>**мсиопендатабасемодепатчфиле**</dt> <dt>32</dt></span><span class="sxs-lookup"><span data-stu-id="05c7d-128"><dt>**msiOpenDatabaseModePatchFile**</dt> <dt>32</dt></span></span> </dl>            | <span data-ttu-id="05c7d-129">Добавляет этот флаг для указания файла исправления.</span><span class="sxs-lookup"><span data-stu-id="05c7d-129">Adds this flag to indicate a patch file.</span></span><br/>                                                                                                                     |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="05c7d-130">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="05c7d-130">Return value</span></span>

<span data-ttu-id="05c7d-131">Объект [**базы данных**](database-object.md) , представляющий существующую или новую открытую базу данных установщика.</span><span class="sxs-lookup"><span data-stu-id="05c7d-131">A [**Database**](database-object.md) object that represents the existing or new installer database that was opened.</span></span>

## <a name="remarks"></a><span data-ttu-id="05c7d-132">Remarks</span><span class="sxs-lookup"><span data-stu-id="05c7d-132">Remarks</span></span>

<span data-ttu-id="05c7d-133">При открытии базы данных в качестве выходных данных другой базы данных информационный поток выходной базы данных фактически является зеркальной базой данных, предназначенной только для чтения, и поэтому не может быть изменен.</span><span class="sxs-lookup"><span data-stu-id="05c7d-133">When a database is opened as the output of another database, the summary information stream of the output database is actually a read-only mirror of the original database and thus cannot be changed.</span></span> <span data-ttu-id="05c7d-134">Кроме того, она не сохраняется в базе данных.</span><span class="sxs-lookup"><span data-stu-id="05c7d-134">Additionally, it is not persisted with the database.</span></span> <span data-ttu-id="05c7d-135">Чтобы создать или изменить сводные данные для выходной базы данных, ее необходимо закрыть и повторно открыть.</span><span class="sxs-lookup"><span data-stu-id="05c7d-135">To create or modify the summary information for the output database it must be closed and reopened.</span></span>

<span data-ttu-id="05c7d-136">Чтобы внести и сохранить изменения в базе данных, сначала откройте базу данных в Transaction (Мсиопендатабасемодетрансакт), создайте (Мсиопендатабасемодекреате или Мсиопендатабасемодекреатедирект) или Direct (msiOpenDatabaseModeDirect) режим.</span><span class="sxs-lookup"><span data-stu-id="05c7d-136">To make and save changes to a database first open the database in transaction (msiOpenDatabaseModeTransact), create (msiOpenDatabaseModeCreate or msiOpenDatabaseModeCreateDirect), or direct (msiOpenDatabaseModeDirect) mode.</span></span> <span data-ttu-id="05c7d-137">После внесения изменений всегда вызывайте метод [**commit**](database-commit.md) перед закрытием маркера базы данных.</span><span class="sxs-lookup"><span data-stu-id="05c7d-137">After making the changes, always call the [**Commit**](database-commit.md) method before closing the database handle.</span></span> <span data-ttu-id="05c7d-138">Метод **commit** очищает все буферы.</span><span class="sxs-lookup"><span data-stu-id="05c7d-138">The **Commit** method flushes all buffers.</span></span>

<span data-ttu-id="05c7d-139">Всегда вызывайте метод [**commit**](database-commit.md) для базы данных, которая была открыта в прямом режиме (Мсиопендатабасемодедирект или мсиопендатабасемодекреатедирект) перед закрытием базы данных.</span><span class="sxs-lookup"><span data-stu-id="05c7d-139">Always call the [**Commit**](database-commit.md) method on a database that has been opened in direct mode (msiOpenDatabaseModeDirect or msiOpenDatabaseModeCreateDirect) before closing the database.</span></span> <span data-ttu-id="05c7d-140">Невозможность сделать это может повредить базу данных.</span><span class="sxs-lookup"><span data-stu-id="05c7d-140">Failure to do this may corrupt the database.</span></span>

<span data-ttu-id="05c7d-141">Поскольку метод **опендатабасе** инициирует доступ к базе данных, он не может использоваться с выполняющейся установкой.</span><span class="sxs-lookup"><span data-stu-id="05c7d-141">Because the **OpenDatabase** method initiates database access, it cannot be used with a running installation.</span></span>

<span data-ttu-id="05c7d-142">В случае сбоя метода можно получить расширенные сведения об ошибке с помощью метода [**ластерроррекорд**](installer-lasterrorrecord.md) .</span><span class="sxs-lookup"><span data-stu-id="05c7d-142">If the method fails, you can obtain extended error information by using the [**LastErrorRecord**](installer-lasterrorrecord.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="05c7d-143">Требования</span><span class="sxs-lookup"><span data-stu-id="05c7d-143">Requirements</span></span>



| <span data-ttu-id="05c7d-144">Требование</span><span class="sxs-lookup"><span data-stu-id="05c7d-144">Requirement</span></span> | <span data-ttu-id="05c7d-145">Значение</span><span class="sxs-lookup"><span data-stu-id="05c7d-145">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="05c7d-146">Версия</span><span class="sxs-lookup"><span data-stu-id="05c7d-146">Version</span></span><br/> | <span data-ttu-id="05c7d-147">Установщик Windows 5,0 в Windows Server 2012, Windows 8, Windows Server 2008 R2 или Windows 7.</span><span class="sxs-lookup"><span data-stu-id="05c7d-147">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="05c7d-148">Установщик Windows 4,0 или установщик Windows 4,5 на Windows Server 2008 или Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="05c7d-148">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="05c7d-149">установщик Windows в Windows Server 2003 или Windows XP</span><span class="sxs-lookup"><span data-stu-id="05c7d-149">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="05c7d-150">DLL</span><span class="sxs-lookup"><span data-stu-id="05c7d-150">DLL</span></span><br/>     | <dl> <span data-ttu-id="05c7d-151"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="05c7d-151"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="05c7d-152">IID</span><span class="sxs-lookup"><span data-stu-id="05c7d-152">IID</span></span><br/>     | <span data-ttu-id="05c7d-153">IID \_ иинсталлер определен как 000C1090-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="05c7d-153">IID\_IInstaller is defined as 000C1090-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                           |



 

 




