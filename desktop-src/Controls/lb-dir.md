---
title: Сообщение LB_DIR (Winuser. h)
description: Добавляет имена в список, отображаемый списком. В сообщении добавляются имена каталогов и файлов, соответствующие заданной строке и набору атрибутов файлов. Команда балансировки нагрузки \_ также может добавлять в список буквы подключенных дисков.
ms.assetid: 5ec134e9-fe42-4cc0-bdea-fa5e66c218f6
keywords:
- Элементы управления Windows для LB_DIR сообщений
topic_type:
- apiref
api_name:
- LB_DIR
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 80abddbce13adec2e66824057fc5e873def306ad
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104137446"
---
# <a name="lb_dir-message"></a><span data-ttu-id="0b695-106">\_Сообщение с каталогом балансировки</span><span class="sxs-lookup"><span data-stu-id="0b695-106">LB\_DIR message</span></span>

<span data-ttu-id="0b695-107">Добавляет имена в список, отображаемый списком.</span><span class="sxs-lookup"><span data-stu-id="0b695-107">Adds names to the list displayed by a list box.</span></span> <span data-ttu-id="0b695-108">В сообщении добавляются имена каталогов и файлов, соответствующие заданной строке и набору атрибутов файлов.</span><span class="sxs-lookup"><span data-stu-id="0b695-108">The message adds the names of directories and files that match a specified string and set of file attributes.</span></span> <span data-ttu-id="0b695-109">**Фунтов \_ DIR** также может добавлять в список буквы подключенных дисков.</span><span class="sxs-lookup"><span data-stu-id="0b695-109">**LB\_DIR** can also add mapped drive letters to the list box.</span></span>

## <a name="parameters"></a><span data-ttu-id="0b695-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="0b695-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0b695-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="0b695-111">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="0b695-112">Атрибуты файлов или каталогов, добавляемых в список.</span><span class="sxs-lookup"><span data-stu-id="0b695-112">The attributes of the files or directories to be added to the list box.</span></span> <span data-ttu-id="0b695-113">Этот параметр может принимать одно или несколько следующих значений.</span><span class="sxs-lookup"><span data-stu-id="0b695-113">This parameter can be one or more of the following values.</span></span>



| <span data-ttu-id="0b695-114">Значение</span><span class="sxs-lookup"><span data-stu-id="0b695-114">Value</span></span>                                                                                                                                                         | <span data-ttu-id="0b695-115">Значение</span><span class="sxs-lookup"><span data-stu-id="0b695-115">Meaning</span></span>                                                                                                                                        |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="DDL_ARCHIVE"></span><span id="ddl_archive"></span><dl> <span data-ttu-id="0b695-116"><dt>**\_Архив DDL**</dt></span><span class="sxs-lookup"><span data-stu-id="0b695-116"><dt>**DDL\_ARCHIVE**</dt></span></span> </dl>       | <span data-ttu-id="0b695-117">Включает архивные файлы.</span><span class="sxs-lookup"><span data-stu-id="0b695-117">Includes archived files.</span></span><br/>                                                                                                            |
| <span id="DDL_DIRECTORY"></span><span id="ddl_directory"></span><dl> <span data-ttu-id="0b695-118"><dt>**\_Каталог DDL**</dt></span><span class="sxs-lookup"><span data-stu-id="0b695-118"><dt>**DDL\_DIRECTORY**</dt></span></span> </dl> | <span data-ttu-id="0b695-119">Включает подкаталоги.</span><span class="sxs-lookup"><span data-stu-id="0b695-119">Includes subdirectories.</span></span> <span data-ttu-id="0b695-120">Имена вложенных подкаталогов заключаются в квадратные скобки ( \[ \] ).</span><span class="sxs-lookup"><span data-stu-id="0b695-120">Subdirectory names are enclosed in square brackets (\[ \]).</span></span><br/>                                                |
| <span id="DDL_DRIVES"></span><span id="ddl_drives"></span><dl> <span data-ttu-id="0b695-121"><dt>**\_диски DDL**</dt></span><span class="sxs-lookup"><span data-stu-id="0b695-121"><dt>**DDL\_DRIVES**</dt></span></span> </dl>          | <span data-ttu-id="0b695-122">Все сопоставленные диски добавляются в список.</span><span class="sxs-lookup"><span data-stu-id="0b695-122">All mapped drives are added to the list.</span></span> <span data-ttu-id="0b695-123">Диски перечислены в формате \[ - *x* - \] , где *x* — буква диска.</span><span class="sxs-lookup"><span data-stu-id="0b695-123">Drives are listed in the form \[-*x*-\], where *x* is the drive letter.</span></span><br/>                    |
| <span id="DDL_EXCLUSIVE"></span><span id="ddl_exclusive"></span><dl> <span data-ttu-id="0b695-124"><dt>**\_эксклюзивный DDL**</dt></span><span class="sxs-lookup"><span data-stu-id="0b695-124"><dt>**DDL\_EXCLUSIVE**</dt></span></span> </dl> | <span data-ttu-id="0b695-125">Включает только файлы с указанными атрибутами.</span><span class="sxs-lookup"><span data-stu-id="0b695-125">Includes only files with the specified attributes.</span></span> <span data-ttu-id="0b695-126">По умолчанию файлы для чтения и записи перечисляются, даже если \_ не указано значение DDL ReadWrite.</span><span class="sxs-lookup"><span data-stu-id="0b695-126">By default, read/write files are listed even if DDL\_READWRITE is not specified.</span></span><br/> |
| <span id="DDL_HIDDEN"></span><span id="ddl_hidden"></span><dl> <span data-ttu-id="0b695-127"><dt>**\_скрытый DDL**</dt></span><span class="sxs-lookup"><span data-stu-id="0b695-127"><dt>**DDL\_HIDDEN**</dt></span></span> </dl>          | <span data-ttu-id="0b695-128">Включает скрытые файлы.</span><span class="sxs-lookup"><span data-stu-id="0b695-128">Includes hidden files.</span></span><br/>                                                                                                              |
| <span id="DDL_READONLY"></span><span id="ddl_readonly"></span><dl> <span data-ttu-id="0b695-129"><dt>**DDL \_ ReadOnly**</dt></span><span class="sxs-lookup"><span data-stu-id="0b695-129"><dt>**DDL\_READONLY**</dt></span></span> </dl>    | <span data-ttu-id="0b695-130">Включает файлы только для чтения.</span><span class="sxs-lookup"><span data-stu-id="0b695-130">Includes read-only files.</span></span><br/>                                                                                                           |
| <span id="DDL_READWRITE"></span><span id="ddl_readwrite"></span><dl> <span data-ttu-id="0b695-131"><dt>**DDL \_ ReadWrite**</dt></span><span class="sxs-lookup"><span data-stu-id="0b695-131"><dt>**DDL\_READWRITE**</dt></span></span> </dl> | <span data-ttu-id="0b695-132">Включает файлы для чтения и записи без дополнительных атрибутов.</span><span class="sxs-lookup"><span data-stu-id="0b695-132">Includes read/write files with no additional attributes.</span></span> <span data-ttu-id="0b695-133">Это параметр по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="0b695-133">This is the default setting.</span></span><br/>                                               |
| <span id="DDL_SYSTEM"></span><span id="ddl_system"></span><dl> <span data-ttu-id="0b695-134"><dt>**\_система DDL**</dt></span><span class="sxs-lookup"><span data-stu-id="0b695-134"><dt>**DDL\_SYSTEM**</dt></span></span> </dl>          | <span data-ttu-id="0b695-135">Включает системные файлы.</span><span class="sxs-lookup"><span data-stu-id="0b695-135">Includes system files.</span></span><br/>                                                                                                              |



 

</dd> <dt>

<span data-ttu-id="0b695-136">*lParam*</span><span class="sxs-lookup"><span data-stu-id="0b695-136">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="0b695-137">Указатель на строку, завершающуюся нулем, которая указывает абсолютный путь, относительный путь или имя файла.</span><span class="sxs-lookup"><span data-stu-id="0b695-137">A pointer to the null-terminated string that specifies an absolute path, relative path, or filename.</span></span> <span data-ttu-id="0b695-138">Абсолютный путь может начинаться с буквы диска (например, d: \) или UNC-имени (например, \\ \\ *MachineName* \\ *ShareName*).</span><span class="sxs-lookup"><span data-stu-id="0b695-138">An absolute path can begin with a drive letter (for example, d:\) or a UNC name (for example, \\\\ *machinename*\\ *sharename*).</span></span>

<span data-ttu-id="0b695-139">Если строка указывает имя файла или каталог с атрибутами, заданными параметром *wParam* , то имя файла или каталога добавляется в список.</span><span class="sxs-lookup"><span data-stu-id="0b695-139">If the string specifies a filename or directory that has the attributes specified by the *wParam* parameter, the filename or directory is added to the list.</span></span> <span data-ttu-id="0b695-140">Если имя файла или каталога содержит подстановочные знаки (?</span><span class="sxs-lookup"><span data-stu-id="0b695-140">If the filename or directory name contains wildcard characters (?</span></span> <span data-ttu-id="0b695-141">или \* ), все файлы или каталоги, которые соответствуют выражению-шаблону и имеют атрибуты, заданные параметром *wParam* , добавляются в список.</span><span class="sxs-lookup"><span data-stu-id="0b695-141">or \*), all files or directories that match the wildcard expression and have the attributes specified by the *wParam* parameter are added to the list.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0b695-142">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="0b695-142">Return value</span></span>

<span data-ttu-id="0b695-143">Если сообщение прошло удачно, возвращаемое значение представляет собой отсчитываемый от нуля индекс последнего имени, добавленного в список.</span><span class="sxs-lookup"><span data-stu-id="0b695-143">If the message succeeds, the return value is the zero-based index of the last name added to the list.</span></span>

<span data-ttu-id="0b695-144">Если возникает ошибка, возвращается значение фунтов \_ Err.</span><span class="sxs-lookup"><span data-stu-id="0b695-144">If an error occurs, the return value is LB\_ERR.</span></span> <span data-ttu-id="0b695-145">Если недостаточно места для хранения новых строк, возвращается значение фунтов \_ еррспаце.</span><span class="sxs-lookup"><span data-stu-id="0b695-145">If there is insufficient space to store the new strings, the return value is LB\_ERRSPACE.</span></span>

## <a name="remarks"></a><span data-ttu-id="0b695-146">Комментарии</span><span class="sxs-lookup"><span data-stu-id="0b695-146">Remarks</span></span>

<span data-ttu-id="0b695-147">Сообщение [**\_ инитстораже балансировки нагрузки**](lb-initstorage.md) помогает ускорить инициализацию списков с большим количеством элементов (более 100).</span><span class="sxs-lookup"><span data-stu-id="0b695-147">The [**LB\_INITSTORAGE**](lb-initstorage.md) message helps speed up the initialization of list boxes that have a large number of items (more than 100).</span></span> <span data-ttu-id="0b695-148">Он резервирует указанный объем памяти, чтобы последующие сообщения с **\_ каталогом балансировки нагрузки** занимают кратчайшее время.</span><span class="sxs-lookup"><span data-stu-id="0b695-148">It reserves the specified amount of memory so that subsequent **LB\_DIR** messages take the shortest possible time.</span></span> <span data-ttu-id="0b695-149">Для параметров *wParam* и *lParam* можно использовать оценки.</span><span class="sxs-lookup"><span data-stu-id="0b695-149">You can use estimates for the *wParam* and *lParam* parameters.</span></span> <span data-ttu-id="0b695-150">При чрезмерной оценке выделяется дополнительный объем памяти. Если недооценивать, то для элементов, превышающих запрошенный объем, используется нормальное выделение.</span><span class="sxs-lookup"><span data-stu-id="0b695-150">If you overestimate, the extra memory is allocated; if you underestimate, the normal allocation is used for items that exceed the requested amount.</span></span>

<span data-ttu-id="0b695-151">Если параметр *wParam* включает \_ флаг DDL-каталога и *lParam* указывает все подкаталоги каталога первого уровня, например C: \\ temp \\ \* , список всегда будет содержать запись ".." для корневого каталога.</span><span class="sxs-lookup"><span data-stu-id="0b695-151">If *wParam* includes the DDL\_DIRECTORY flag and *lParam* specifies all the subdirectories of a first-level directory, such as C:\\TEMP\\\*, the list box will always include a ".." entry for the root directory.</span></span> <span data-ttu-id="0b695-152">Это справедливо даже в том случае, если корневой каталог имеет скрытые или системные атрибуты и \_ \_ не указаны системные флаги DDL Hidden и DDL.</span><span class="sxs-lookup"><span data-stu-id="0b695-152">This is true even if the root directory has hidden or system attributes and the DDL\_HIDDEN and DDL\_SYSTEM flags are not specified.</span></span> <span data-ttu-id="0b695-153">Корневой каталог тома NTFS содержит скрытые и системные атрибуты.</span><span class="sxs-lookup"><span data-stu-id="0b695-153">The root directory of an NTFS volume has hidden and system attributes.</span></span>

<span data-ttu-id="0b695-154">В списке отображаются длинные имена файлов, если они есть.</span><span class="sxs-lookup"><span data-stu-id="0b695-154">The list displays long filenames, if any.</span></span>

<span data-ttu-id="0b695-155">Для приложения ANSI система преобразует текст в поле со списком в Юникод с помощью команды CP \_ ACP.</span><span class="sxs-lookup"><span data-stu-id="0b695-155">For an ANSI application, the system converts the text in a list box to Unicode using CP\_ACP.</span></span> <span data-ttu-id="0b695-156">Это может вызвать проблемы.</span><span class="sxs-lookup"><span data-stu-id="0b695-156">This can cause problems.</span></span> <span data-ttu-id="0b695-157">Например, римские символы с диакритическими знаками в списке не в Юникоде в японских окнах будут выступать из искажений.</span><span class="sxs-lookup"><span data-stu-id="0b695-157">For example, accented Roman characters in a non-Unicode list box in Japanese Windows will come out garbled.</span></span> <span data-ttu-id="0b695-158">Чтобы устранить эту проблему, либо скомпилируйте приложение как Юникод, либо используйте список, рисуемый владельцем.</span><span class="sxs-lookup"><span data-stu-id="0b695-158">To fix this, either compile the application as Unicode or use an owner-drawn list box.</span></span>

## <a name="requirements"></a><span data-ttu-id="0b695-159">Требования</span><span class="sxs-lookup"><span data-stu-id="0b695-159">Requirements</span></span>



| <span data-ttu-id="0b695-160">Требование</span><span class="sxs-lookup"><span data-stu-id="0b695-160">Requirement</span></span> | <span data-ttu-id="0b695-161">Значение</span><span class="sxs-lookup"><span data-stu-id="0b695-161">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0b695-162">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="0b695-162">Minimum supported client</span></span><br/> | <span data-ttu-id="0b695-163">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="0b695-163">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="0b695-164">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="0b695-164">Minimum supported server</span></span><br/> | <span data-ttu-id="0b695-165">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="0b695-165">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="0b695-166">Header</span><span class="sxs-lookup"><span data-stu-id="0b695-166">Header</span></span><br/>                   | <dl> <span data-ttu-id="0b695-167"><dt>Winuser. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="0b695-167"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0b695-168">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="0b695-168">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0b695-169">**длгдирлист**</span><span class="sxs-lookup"><span data-stu-id="0b695-169">**DlgDirList**</span></span>](/windows/desktop/api/Winuser/nf-winuser-dlgdirlista)
</dt> </dl>

 

 





