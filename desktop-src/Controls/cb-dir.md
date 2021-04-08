---
title: Сообщение CB_DIR (Winuser. h)
description: Добавляет имена в список, отображаемый полем со списком. В сообщении добавляются имена каталогов и файлов, соответствующие заданной строке и набору атрибутов файлов. \_Каталог CB также может добавлять в список буквы подключенных дисков.
ms.assetid: 6082d12c-0af4-4a99-98c0-6a98d171f4d8
keywords:
- Элементы управления Windows для CB_DIR сообщений
topic_type:
- apiref
api_name:
- CB_DIR
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 98cbea5bb88614d5606dd3d5cb165be59f632556
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103891929"
---
# <a name="cb_dir-message"></a><span data-ttu-id="3d74e-106">\_Сообщение в каталоге CB</span><span class="sxs-lookup"><span data-stu-id="3d74e-106">CB\_DIR message</span></span>

<span data-ttu-id="3d74e-107">Добавляет имена в список, отображаемый полем со списком.</span><span class="sxs-lookup"><span data-stu-id="3d74e-107">Adds names to the list displayed by the combo box.</span></span> <span data-ttu-id="3d74e-108">В сообщении добавляются имена каталогов и файлов, соответствующие заданной строке и набору атрибутов файлов.</span><span class="sxs-lookup"><span data-stu-id="3d74e-108">The message adds the names of directories and files that match a specified string and set of file attributes.</span></span> <span data-ttu-id="3d74e-109">**CB \_ DIR** также может добавлять в список буквы подключенных дисков.</span><span class="sxs-lookup"><span data-stu-id="3d74e-109">**CB\_DIR** can also add mapped drive letters to the list.</span></span>

## <a name="parameters"></a><span data-ttu-id="3d74e-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="3d74e-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3d74e-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="3d74e-111">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="3d74e-112">Атрибуты файлов или каталогов, добавляемых в поле со списком.</span><span class="sxs-lookup"><span data-stu-id="3d74e-112">The attributes of the files or directories to be added to the combo box.</span></span> <span data-ttu-id="3d74e-113">Этот параметр может принимать одно или несколько следующих значений.</span><span class="sxs-lookup"><span data-stu-id="3d74e-113">This parameter can be one or more of the following values.</span></span>



| <span data-ttu-id="3d74e-114">Значение</span><span class="sxs-lookup"><span data-stu-id="3d74e-114">Value</span></span>                                                                                                                                                         | <span data-ttu-id="3d74e-115">Значение</span><span class="sxs-lookup"><span data-stu-id="3d74e-115">Meaning</span></span>                                                                                                                                        |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="DDL_ARCHIVE"></span><span id="ddl_archive"></span><dl> <span data-ttu-id="3d74e-116"><dt>**\_Архив DDL**</dt></span><span class="sxs-lookup"><span data-stu-id="3d74e-116"><dt>**DDL\_ARCHIVE**</dt></span></span> </dl>       | <span data-ttu-id="3d74e-117">Включает архивные файлы.</span><span class="sxs-lookup"><span data-stu-id="3d74e-117">Includes archived files.</span></span><br/>                                                                                                            |
| <span id="DDL_DIRECTORY"></span><span id="ddl_directory"></span><dl> <span data-ttu-id="3d74e-118"><dt>**\_Каталог DDL**</dt></span><span class="sxs-lookup"><span data-stu-id="3d74e-118"><dt>**DDL\_DIRECTORY**</dt></span></span> </dl> | <span data-ttu-id="3d74e-119">Включает подкаталоги, заключенные в квадратные скобки ( \[ \] ).</span><span class="sxs-lookup"><span data-stu-id="3d74e-119">Includes subdirectories, which are enclosed in square brackets (\[ \]).</span></span><br/>                                                             |
| <span id="DDL_DRIVES"></span><span id="ddl_drives"></span><dl> <span data-ttu-id="3d74e-120"><dt>**\_диски DDL**</dt></span><span class="sxs-lookup"><span data-stu-id="3d74e-120"><dt>**DDL\_DRIVES**</dt></span></span> </dl>          | <span data-ttu-id="3d74e-121">Все сопоставленные диски добавляются в список.</span><span class="sxs-lookup"><span data-stu-id="3d74e-121">All mapped drives are added to the list.</span></span> <span data-ttu-id="3d74e-122">Диски перечислены в формате \[ - *x* - \] , где *x* — буква диска.</span><span class="sxs-lookup"><span data-stu-id="3d74e-122">Drives are listed in the form \[-*x*-\], where *x* is the drive letter.</span></span><br/>                    |
| <span id="DDL_EXCLUSIVE"></span><span id="ddl_exclusive"></span><dl> <span data-ttu-id="3d74e-123"><dt>**\_эксклюзивный DDL**</dt></span><span class="sxs-lookup"><span data-stu-id="3d74e-123"><dt>**DDL\_EXCLUSIVE**</dt></span></span> </dl> | <span data-ttu-id="3d74e-124">Включает только файлы с указанными атрибутами.</span><span class="sxs-lookup"><span data-stu-id="3d74e-124">Includes only files with the specified attributes.</span></span> <span data-ttu-id="3d74e-125">По умолчанию файлы для чтения и записи перечисляются, даже если \_ не указано значение DDL ReadWrite.</span><span class="sxs-lookup"><span data-stu-id="3d74e-125">By default, read/write files are listed even if DDL\_READWRITE is not specified.</span></span><br/> |
| <span id="DDL_HIDDEN"></span><span id="ddl_hidden"></span><dl> <span data-ttu-id="3d74e-126"><dt>**\_скрытый DDL**</dt></span><span class="sxs-lookup"><span data-stu-id="3d74e-126"><dt>**DDL\_HIDDEN**</dt></span></span> </dl>          | <span data-ttu-id="3d74e-127">Включает скрытые файлы.</span><span class="sxs-lookup"><span data-stu-id="3d74e-127">Includes hidden files.</span></span><br/>                                                                                                              |
| <span id="DDL_READONLY"></span><span id="ddl_readonly"></span><dl> <span data-ttu-id="3d74e-128"><dt>**DDL \_ ReadOnly**</dt></span><span class="sxs-lookup"><span data-stu-id="3d74e-128"><dt>**DDL\_READONLY**</dt></span></span> </dl>    | <span data-ttu-id="3d74e-129">Включает файлы только для чтения.</span><span class="sxs-lookup"><span data-stu-id="3d74e-129">Includes read-only files.</span></span><br/>                                                                                                           |
| <span id="DDL_READWRITE"></span><span id="ddl_readwrite"></span><dl> <span data-ttu-id="3d74e-130"><dt>**DDL \_ ReadWrite**</dt></span><span class="sxs-lookup"><span data-stu-id="3d74e-130"><dt>**DDL\_READWRITE**</dt></span></span> </dl> | <span data-ttu-id="3d74e-131">Включает файлы для чтения и записи без дополнительных атрибутов.</span><span class="sxs-lookup"><span data-stu-id="3d74e-131">Includes read/write files with no additional attributes.</span></span> <span data-ttu-id="3d74e-132">Это значение по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="3d74e-132">This is the default.</span></span><br/>                                                       |
| <span id="DDL_SYSTEM"></span><span id="ddl_system"></span><dl> <span data-ttu-id="3d74e-133"><dt>**\_система DDL**</dt></span><span class="sxs-lookup"><span data-stu-id="3d74e-133"><dt>**DDL\_SYSTEM**</dt></span></span> </dl>          | <span data-ttu-id="3d74e-134">Включает системные файлы.</span><span class="sxs-lookup"><span data-stu-id="3d74e-134">Includes system files.</span></span><br/>                                                                                                              |



 

</dd> <dt>

<span data-ttu-id="3d74e-135">*lParam*</span><span class="sxs-lookup"><span data-stu-id="3d74e-135">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="3d74e-136">Указатель **LPCTSTR** на строку, завершающуюся нулем, которая указывает абсолютный путь, относительный путь или имя файла.</span><span class="sxs-lookup"><span data-stu-id="3d74e-136">An **LPCTSTR** pointer to a null-terminated string that specifies an absolute path, relative path, or file name.</span></span> <span data-ttu-id="3d74e-137">Абсолютный путь может начинаться с буквы диска (например, d: \) или UNC-имени (например, \\ \\ *MachineName* \\ *ShareName*).</span><span class="sxs-lookup"><span data-stu-id="3d74e-137">An absolute path can begin with a drive letter (for example, d:\) or a UNC name (for example, \\\\*machinename*\\*sharename*).</span></span> <span data-ttu-id="3d74e-138">Если строка указывает имя файла или каталог с атрибутами, заданными параметром *wParam* , то имя файла или каталога добавляется в список.</span><span class="sxs-lookup"><span data-stu-id="3d74e-138">If the string specifies a file name or directory that has the attributes specified by the *wParam* parameter, the file name or directory is added to the list.</span></span> <span data-ttu-id="3d74e-139">Если имя файла или каталога содержит подстановочные знаки (?</span><span class="sxs-lookup"><span data-stu-id="3d74e-139">If the file name or directory name contains wildcard characters (?</span></span> <span data-ttu-id="3d74e-140">или \* ), все файлы или каталоги, которые соответствуют выражению-шаблону и имеют атрибуты, заданные параметром *wParam* , добавляются в список, отображаемый в поле со списком.</span><span class="sxs-lookup"><span data-stu-id="3d74e-140">or \*), all files or directories that match the wildcard expression and have the attributes specified by the *wParam* parameter are added to the list displayed in the combo box.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3d74e-141">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="3d74e-141">Return value</span></span>

<span data-ttu-id="3d74e-142">Если сообщение прошло удачно, возвращаемое значение представляет собой отсчитываемый от нуля индекс последнего имени, добавленного в список.</span><span class="sxs-lookup"><span data-stu-id="3d74e-142">If the message succeeds, the return value is the zero-based index of the last name added to the list.</span></span>

<span data-ttu-id="3d74e-143">Если возникает ошибка, возвращается значение CB \_ Err.</span><span class="sxs-lookup"><span data-stu-id="3d74e-143">If an error occurs, the return value is CB\_ERR.</span></span> <span data-ttu-id="3d74e-144">Если недостаточно места для хранения новых строк, возвращается значение CB \_ еррспаце.</span><span class="sxs-lookup"><span data-stu-id="3d74e-144">If there is insufficient space to store the new strings, the return value is CB\_ERRSPACE.</span></span>

## <a name="remarks"></a><span data-ttu-id="3d74e-145">Комментарии</span><span class="sxs-lookup"><span data-stu-id="3d74e-145">Remarks</span></span>

<span data-ttu-id="3d74e-146">Если параметр *wParam* включает \_ флаг DDL-каталога и *lParam* указывает все подкаталоги каталога первого уровня, например C: \\ temp \\ \* , список всегда будет содержать запись ".." для корневого каталога.</span><span class="sxs-lookup"><span data-stu-id="3d74e-146">If *wParam* includes the DDL\_DIRECTORY flag and *lParam* specifies all the subdirectories of a first-level directory, such as C:\\TEMP\\\*, the list box will always include a ".." entry for the root directory.</span></span> <span data-ttu-id="3d74e-147">Это справедливо даже в том случае, если корневой каталог имеет скрытые или системные атрибуты и \_ \_ не указаны системные флаги DDL Hidden и DDL.</span><span class="sxs-lookup"><span data-stu-id="3d74e-147">This is true even if the root directory has hidden or system attributes and the DDL\_HIDDEN and DDL\_SYSTEM flags are not specified.</span></span> <span data-ttu-id="3d74e-148">Корневой каталог тома NTFS содержит скрытые и системные атрибуты.</span><span class="sxs-lookup"><span data-stu-id="3d74e-148">The root directory of an NTFS volume has hidden and system attributes.</span></span>

<span data-ttu-id="3d74e-149">В списке отображаются длинные имена файлов, если они есть.</span><span class="sxs-lookup"><span data-stu-id="3d74e-149">The list displays long file names, if any.</span></span>

## <a name="requirements"></a><span data-ttu-id="3d74e-150">Требования</span><span class="sxs-lookup"><span data-stu-id="3d74e-150">Requirements</span></span>



| <span data-ttu-id="3d74e-151">Требование</span><span class="sxs-lookup"><span data-stu-id="3d74e-151">Requirement</span></span> | <span data-ttu-id="3d74e-152">Значение</span><span class="sxs-lookup"><span data-stu-id="3d74e-152">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3d74e-153">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="3d74e-153">Minimum supported client</span></span><br/> | <span data-ttu-id="3d74e-154">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="3d74e-154">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="3d74e-155">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="3d74e-155">Minimum supported server</span></span><br/> | <span data-ttu-id="3d74e-156">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="3d74e-156">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="3d74e-157">Header</span><span class="sxs-lookup"><span data-stu-id="3d74e-157">Header</span></span><br/>                   | <dl> <span data-ttu-id="3d74e-158"><dt>Winuser. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="3d74e-158"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3d74e-159">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="3d74e-159">See also</span></span>

<dl> <dt>

<span data-ttu-id="3d74e-160">**Ссылки**</span><span class="sxs-lookup"><span data-stu-id="3d74e-160">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="3d74e-161">**\_ADDSTRING CB**</span><span class="sxs-lookup"><span data-stu-id="3d74e-161">**CB\_ADDSTRING**</span></span>](cb-addstring.md)
</dt> <dt>

[<span data-ttu-id="3d74e-162">**\_ИНСЕРТСТРИНГ CB**</span><span class="sxs-lookup"><span data-stu-id="3d74e-162">**CB\_INSERTSTRING**</span></span>](cb-insertstring.md)
</dt> <dt>

[<span data-ttu-id="3d74e-163">**длгдирлисткомбобокс**</span><span class="sxs-lookup"><span data-stu-id="3d74e-163">**DlgDirListComboBox**</span></span>](/windows/desktop/api/Winuser/nf-winuser-dlgdirlistcomboboxa)
</dt> </dl>

 

 





