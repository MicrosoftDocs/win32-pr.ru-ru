---
description: Классы WMI, представляющие файлы или каталоги, такие как Win32 \_ кодекфиле или CIM \_ File, содержат свойство AccessMask.
ms.assetid: 9020b337-d44f-4247-b623-68a1bcf35abb
ms.tgt_platform: multiple
title: Константы прав доступа к файлам и каталогам (Winnt. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5c0ddca31034ffde79fa9d9ff902a364cf07e311
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105704155"
---
# <a name="file-and-directory-access-rights-constants"></a><span data-ttu-id="d8d6f-103">Константы прав доступа к файлам и каталогам</span><span class="sxs-lookup"><span data-stu-id="d8d6f-103">File and Directory Access Rights Constants</span></span>

<span data-ttu-id="d8d6f-104">Классы WMI, представляющие файлы или каталоги, такие как [**Win32 \_ Кодекфиле**](/windows/desktop/CIMWin32Prov/win32-codecfile) или [**CIM \_ File**](/windows/desktop/CIMWin32Prov/cim-datafile), содержат свойство **AccessMask** .</span><span class="sxs-lookup"><span data-stu-id="d8d6f-104">WMI classes that represent files or directories, such as [**Win32\_CodecFile**](/windows/desktop/CIMWin32Prov/win32-codecfile) or [**CIM\_DataFile**](/windows/desktop/CIMWin32Prov/cim-datafile), contain an **AccessMask** property.</span></span> <span data-ttu-id="d8d6f-105">Это свойство содержит битовые параметры, указывающие права доступа, которые должен иметь пользователь или группа для конкретного доступа или операций с файлом.</span><span class="sxs-lookup"><span data-stu-id="d8d6f-105">This property contains bit settings that specify the access rights a user or group must have for specific access or operations on the file.</span></span> <span data-ttu-id="d8d6f-106">Дополнительные сведения см. в статьях [безопасность и права доступа к файлам](/windows/desktop/FileIO/file-security-and-access-rights) и [изменение параметров безопасности доступа к защищаемым объектам](changing-access-security-on-securable-objects.md).</span><span class="sxs-lookup"><span data-stu-id="d8d6f-106">For more information, see [File Security and Access Rights](/windows/desktop/FileIO/file-security-and-access-rights) and [Changing Access Security on Securable Objects](changing-access-security-on-securable-objects.md).</span></span>

<span data-ttu-id="d8d6f-107">Классы файла или каталога, содержащие свойство **AccessMask** , включают:</span><span class="sxs-lookup"><span data-stu-id="d8d6f-107">The file or directory classes which contain an **AccessMask** property include:</span></span>

-   [<span data-ttu-id="d8d6f-108">**\_Файл CIM**</span><span class="sxs-lookup"><span data-stu-id="d8d6f-108">**CIM\_DataFile**</span></span>](/windows/desktop/CIMWin32Prov/cim-datafile)
-   [<span data-ttu-id="d8d6f-109">**\_Каталог CIM**</span><span class="sxs-lookup"><span data-stu-id="d8d6f-109">**CIM\_Directory**</span></span>](/windows/desktop/CIMWin32Prov/cim-directory)
-   [<span data-ttu-id="d8d6f-110">**\_LOGICALFILE CIM**</span><span class="sxs-lookup"><span data-stu-id="d8d6f-110">**CIM\_LogicalFile**</span></span>](/windows/desktop/CIMWin32Prov/cim-logicalfile)
-   [<span data-ttu-id="d8d6f-111">**\_Кодекфиле Win32**</span><span class="sxs-lookup"><span data-stu-id="d8d6f-111">**Win32\_CodecFile**</span></span>](/windows/desktop/CIMWin32Prov/win32-codecfile)
-   [<span data-ttu-id="d8d6f-112">**\_Каталог Win32**</span><span class="sxs-lookup"><span data-stu-id="d8d6f-112">**Win32\_Directory**</span></span>](/windows/desktop/CIMWin32Prov/win32-directory)
-   <span data-ttu-id="d8d6f-113">[**\_Нтевентлогфиле Win32**](/previous-versions/windows/desktop/legacy/aa394225(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="d8d6f-113">[**Win32\_NTEventLogFile**](/previous-versions/windows/desktop/legacy/aa394225(v=vs.85))</span></span>
-   [<span data-ttu-id="d8d6f-114">**\_Общий ресурс Win32**</span><span class="sxs-lookup"><span data-stu-id="d8d6f-114">**Win32\_Share**</span></span>](/windows/desktop/CIMWin32Prov/win32-share)
-   [<span data-ttu-id="d8d6f-115">**\_Шорткутфиле Win32**</span><span class="sxs-lookup"><span data-stu-id="d8d6f-115">**Win32\_ShortcutFile**</span></span>](/windows/desktop/CIMWin32Prov/win32-shortcutfile)

<span data-ttu-id="d8d6f-116">В следующем списке перечислены значения прав доступа к файлу и каталогу в свойстве **AccessMask** .</span><span class="sxs-lookup"><span data-stu-id="d8d6f-116">The following list lists the values for file and directory access rights in the **AccessMask** property.</span></span> <span data-ttu-id="d8d6f-117">Это свойство является точечным рисунком.</span><span class="sxs-lookup"><span data-stu-id="d8d6f-117">This property is a bitmap.</span></span>

<dl> <dt>

<span data-ttu-id="d8d6f-118"><span id="FILE_READ_DATA"></span><span id="file_read_data"></span>**\_Чтение \_ данных файла**</span><span class="sxs-lookup"><span data-stu-id="d8d6f-118"><span id="FILE_READ_DATA"></span><span id="file_read_data"></span>**FILE\_READ\_DATA**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8d6f-119">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="d8d6f-119">1 (0x1)</span></span>
</dt> <dt>



<span data-ttu-id="d8d6f-120">Предоставляет право на чтение данных из файла.</span><span class="sxs-lookup"><span data-stu-id="d8d6f-120">Grants the right to read data from the file.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d8d6f-121"><span id="FILE_LIST_DIRECTORY"></span><span id="file_list_directory"></span>**\_каталог списка \_ файлов**</span><span class="sxs-lookup"><span data-stu-id="d8d6f-121"><span id="FILE_LIST_DIRECTORY"></span><span id="file_list_directory"></span>**FILE\_LIST\_DIRECTORY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8d6f-122">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="d8d6f-122">1 (0x1)</span></span>
</dt> <dt>



<span data-ttu-id="d8d6f-123">Предоставляет право на чтение данных из файла.</span><span class="sxs-lookup"><span data-stu-id="d8d6f-123">Grants the right to read data from the file.</span></span> <span data-ttu-id="d8d6f-124">Для каталога это значение предоставляет право на перечисление содержимого каталога.</span><span class="sxs-lookup"><span data-stu-id="d8d6f-124">For a directory, this value grants the right to list the contents of the directory.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d8d6f-125"><span id="FILE_WRITE_DATA"></span><span id="file_write_data"></span>**\_данные записи \_ файла**</span><span class="sxs-lookup"><span data-stu-id="d8d6f-125"><span id="FILE_WRITE_DATA"></span><span id="file_write_data"></span>**FILE\_WRITE\_DATA**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8d6f-126">2 (0x2)</span><span class="sxs-lookup"><span data-stu-id="d8d6f-126">2 (0x2)</span></span>
</dt> <dt>



<span data-ttu-id="d8d6f-127">Предоставляет право на запись данных в файл.</span><span class="sxs-lookup"><span data-stu-id="d8d6f-127">Grants the right to write data to the file.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d8d6f-128"><span id="FILE_ADD_FILE"></span><span id="file_add_file"></span>**ФАЙЛ \_ Добавить \_ файл**</span><span class="sxs-lookup"><span data-stu-id="d8d6f-128"><span id="FILE_ADD_FILE"></span><span id="file_add_file"></span>**FILE\_ADD\_FILE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8d6f-129">2 (0x2)</span><span class="sxs-lookup"><span data-stu-id="d8d6f-129">2 (0x2)</span></span>
</dt> <dt>



<span data-ttu-id="d8d6f-130">Предоставляет право на запись данных в файл.</span><span class="sxs-lookup"><span data-stu-id="d8d6f-130">Grants the right to write data to the file.</span></span> <span data-ttu-id="d8d6f-131">Для каталога это значение предоставляет право на создание файла в каталоге.</span><span class="sxs-lookup"><span data-stu-id="d8d6f-131">For a directory, this value grants the right to create a file in the directory.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d8d6f-132"><span id="FILE_APPEND_DATA"></span><span id="file_append_data"></span>**\_Добавление \_ данных в файл**</span><span class="sxs-lookup"><span data-stu-id="d8d6f-132"><span id="FILE_APPEND_DATA"></span><span id="file_append_data"></span>**FILE\_APPEND\_DATA**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8d6f-133">4 (0x4)</span><span class="sxs-lookup"><span data-stu-id="d8d6f-133">4 (0x4)</span></span>
</dt> <dt>



<span data-ttu-id="d8d6f-134">Предоставляет право добавлять данные в файл.</span><span class="sxs-lookup"><span data-stu-id="d8d6f-134">Grants the right to append data to the file.</span></span> <span data-ttu-id="d8d6f-135">Для каталога это значение предоставляет право на создание подкаталога.</span><span class="sxs-lookup"><span data-stu-id="d8d6f-135">For a directory, this value grants the right to create a subdirectory.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d8d6f-136"><span id="FILE_ADD_SUBDIRECTORY"></span><span id="file_add_subdirectory"></span>**ФАЙЛ \_ Добавить \_ подкаталог**</span><span class="sxs-lookup"><span data-stu-id="d8d6f-136"><span id="FILE_ADD_SUBDIRECTORY"></span><span id="file_add_subdirectory"></span>**FILE\_ADD\_SUBDIRECTORY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8d6f-137">4 (0x4)</span><span class="sxs-lookup"><span data-stu-id="d8d6f-137">4 (0x4)</span></span>
</dt> <dt>



<span data-ttu-id="d8d6f-138">Предоставляет право добавлять данные в файл.</span><span class="sxs-lookup"><span data-stu-id="d8d6f-138">Grants the right to append data to the file.</span></span> <span data-ttu-id="d8d6f-139">Для каталога это значение предоставляет право на создание подкаталога.</span><span class="sxs-lookup"><span data-stu-id="d8d6f-139">For a directory, this value grants the right to create a subdirectory.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d8d6f-140"><span id="FILE_READ_EA"></span><span id="file_read_ea"></span>**\_чтение файла \_ EA**</span><span class="sxs-lookup"><span data-stu-id="d8d6f-140"><span id="FILE_READ_EA"></span><span id="file_read_ea"></span>**FILE\_READ\_EA**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8d6f-141">8 (0x8)</span><span class="sxs-lookup"><span data-stu-id="d8d6f-141">8 (0x8)</span></span>
</dt> <dt>



<span data-ttu-id="d8d6f-142">Предоставляет право на чтение расширенных атрибутов.</span><span class="sxs-lookup"><span data-stu-id="d8d6f-142">Grants the right to read extended attributes.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d8d6f-143"><span id="FILE_WRITE_EA"></span><span id="file_write_ea"></span>**запись в файл \_ \_ EA**</span><span class="sxs-lookup"><span data-stu-id="d8d6f-143"><span id="FILE_WRITE_EA"></span><span id="file_write_ea"></span>**FILE\_WRITE\_EA**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8d6f-144">16 (0x10)</span><span class="sxs-lookup"><span data-stu-id="d8d6f-144">16 (0x10)</span></span>
</dt> <dt>



<span data-ttu-id="d8d6f-145">Предоставляет право на запись расширенных атрибутов.</span><span class="sxs-lookup"><span data-stu-id="d8d6f-145">Grants the right to write extended attributes.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d8d6f-146"><span id="FILE_EXECUTE"></span><span id="file_execute"></span>**\_выполнение файла**</span><span class="sxs-lookup"><span data-stu-id="d8d6f-146"><span id="FILE_EXECUTE"></span><span id="file_execute"></span>**FILE\_EXECUTE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8d6f-147">32 (0x20)</span><span class="sxs-lookup"><span data-stu-id="d8d6f-147">32 (0x20)</span></span>
</dt> <dt>



<span data-ttu-id="d8d6f-148">Предоставляет право на выполнение файла.</span><span class="sxs-lookup"><span data-stu-id="d8d6f-148">Grants the right to execute a file.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d8d6f-149"><span id="FILE_TRAVERSE"></span><span id="file_traverse"></span>**\_обход файла**</span><span class="sxs-lookup"><span data-stu-id="d8d6f-149"><span id="FILE_TRAVERSE"></span><span id="file_traverse"></span>**FILE\_TRAVERSE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8d6f-150">32 (0x20)</span><span class="sxs-lookup"><span data-stu-id="d8d6f-150">32 (0x20)</span></span>
</dt> <dt>



<span data-ttu-id="d8d6f-151">Предоставляет право на выполнение файла.</span><span class="sxs-lookup"><span data-stu-id="d8d6f-151">Grants the right to execute a file.</span></span> <span data-ttu-id="d8d6f-152">Для каталога можно просмотреть каталог.</span><span class="sxs-lookup"><span data-stu-id="d8d6f-152">For a directory, the directory can be traversed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d8d6f-153"><span id="FILE_DELETE_CHILD"></span><span id="file_delete_child"></span>**\_дочерний файл удаления файла \_**</span><span class="sxs-lookup"><span data-stu-id="d8d6f-153"><span id="FILE_DELETE_CHILD"></span><span id="file_delete_child"></span>**FILE\_DELETE\_CHILD**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8d6f-154">64 (0x40)</span><span class="sxs-lookup"><span data-stu-id="d8d6f-154">64 (0x40)</span></span>
</dt> <dt>



<span data-ttu-id="d8d6f-155">Предоставляет право удалять каталог и все содержащиеся в нем файлы (дочерние элементы), даже если файлы доступны только для чтения.</span><span class="sxs-lookup"><span data-stu-id="d8d6f-155">Grants the right to delete a directory and all the files it contains (its children), even if the files are read-only.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d8d6f-156"><span id="FILE_READ_ATTRIBUTES"></span><span id="file_read_attributes"></span>**\_атрибуты чтения \_ файла**</span><span class="sxs-lookup"><span data-stu-id="d8d6f-156"><span id="FILE_READ_ATTRIBUTES"></span><span id="file_read_attributes"></span>**FILE\_READ\_ATTRIBUTES**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8d6f-157">128 (0x80)</span><span class="sxs-lookup"><span data-stu-id="d8d6f-157">128 (0x80)</span></span>
</dt> <dt>



<span data-ttu-id="d8d6f-158">Предоставляет право на чтение атрибутов файлов.</span><span class="sxs-lookup"><span data-stu-id="d8d6f-158">Grants the right to read file attributes.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d8d6f-159"><span id="FILE_WRITE_ATTRIBUTES"></span><span id="file_write_attributes"></span>**\_атрибуты записи \_ файла**</span><span class="sxs-lookup"><span data-stu-id="d8d6f-159"><span id="FILE_WRITE_ATTRIBUTES"></span><span id="file_write_attributes"></span>**FILE\_WRITE\_ATTRIBUTES**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8d6f-160">256 (0x100)</span><span class="sxs-lookup"><span data-stu-id="d8d6f-160">256 (0x100)</span></span>
</dt> <dt>



<span data-ttu-id="d8d6f-161">Предоставляет право на изменение атрибутов файлов.</span><span class="sxs-lookup"><span data-stu-id="d8d6f-161">Grants the right to change file attributes.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d8d6f-162"><span id="DELETE"></span><span id="delete"></span>**УДАЛЕН**</span><span class="sxs-lookup"><span data-stu-id="d8d6f-162"><span id="DELETE"></span><span id="delete"></span>**DELETE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8d6f-163">65536 (0x10000)</span><span class="sxs-lookup"><span data-stu-id="d8d6f-163">65536 (0x10000)</span></span>
</dt> <dt>



<span data-ttu-id="d8d6f-164">Право на удаление объекта.</span><span class="sxs-lookup"><span data-stu-id="d8d6f-164">Grants the right to delete the object.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d8d6f-165"><span id="READ_CONTROL"></span><span id="read_control"></span>**\_Контроль чтения**</span><span class="sxs-lookup"><span data-stu-id="d8d6f-165"><span id="READ_CONTROL"></span><span id="read_control"></span>**READ\_CONTROL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8d6f-166">131072 (0x20000)</span><span class="sxs-lookup"><span data-stu-id="d8d6f-166">131072 (0x20000)</span></span>
</dt> <dt>



<span data-ttu-id="d8d6f-167">Предоставляет право на чтение сведений в дескрипторе безопасности для объекта, не включая сведения из списка SACL.</span><span class="sxs-lookup"><span data-stu-id="d8d6f-167">Grants the right to read the information in the security descriptor for the object, not including the information in the SACL.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d8d6f-168"><span id="WRITE_DAC"></span><span id="write_dac"></span>**ЗАПИСЬ \_ DAC**</span><span class="sxs-lookup"><span data-stu-id="d8d6f-168"><span id="WRITE_DAC"></span><span id="write_dac"></span>**WRITE\_DAC**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8d6f-169">262144 (0x40000)</span><span class="sxs-lookup"><span data-stu-id="d8d6f-169">262144 (0x40000)</span></span>
</dt> <dt>



<span data-ttu-id="d8d6f-170">Предоставляет право на изменение списка DACL в дескрипторе безопасности объекта для объекта.</span><span class="sxs-lookup"><span data-stu-id="d8d6f-170">Grants the right to modify the DACL in the object security descriptor for the object.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d8d6f-171"><span id="WRITE_OWNER"></span><span id="write_owner"></span>**\_владелец записи**</span><span class="sxs-lookup"><span data-stu-id="d8d6f-171"><span id="WRITE_OWNER"></span><span id="write_owner"></span>**WRITE\_OWNER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8d6f-172">524288 (0x80000)</span><span class="sxs-lookup"><span data-stu-id="d8d6f-172">524288 (0x80000)</span></span>
</dt> <dt>



<span data-ttu-id="d8d6f-173">Предоставляет право на изменение владельца в дескрипторе безопасности для объекта.</span><span class="sxs-lookup"><span data-stu-id="d8d6f-173">Grants the right to change the owner in the security descriptor for the object.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d8d6f-174"><span id="SYNCHRONIZE"></span><span id="synchronize"></span>**ПОЛНИТ**</span><span class="sxs-lookup"><span data-stu-id="d8d6f-174"><span id="SYNCHRONIZE"></span><span id="synchronize"></span>**SYNCHRONIZE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8d6f-175">1048576 (0x100000)</span><span class="sxs-lookup"><span data-stu-id="d8d6f-175">1048576 (0x100000)</span></span>
</dt> <dt>



<span data-ttu-id="d8d6f-176">Предоставляет право на использование объекта для синхронизации.</span><span class="sxs-lookup"><span data-stu-id="d8d6f-176">Grants the right to use the object for synchronization.</span></span> <span data-ttu-id="d8d6f-177">Это позволяет процессу ожидать, пока объект не поступает в сигнальное состояние.</span><span class="sxs-lookup"><span data-stu-id="d8d6f-177">This enables a process to wait until the object is in signaled state.</span></span> <span data-ttu-id="d8d6f-178">Некоторые типы объектов не поддерживают это право доступа.</span><span class="sxs-lookup"><span data-stu-id="d8d6f-178">Some object types do not support this access right.</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="d8d6f-179">Требования</span><span class="sxs-lookup"><span data-stu-id="d8d6f-179">Requirements</span></span>



| <span data-ttu-id="d8d6f-180">Требование</span><span class="sxs-lookup"><span data-stu-id="d8d6f-180">Requirement</span></span> | <span data-ttu-id="d8d6f-181">Значение</span><span class="sxs-lookup"><span data-stu-id="d8d6f-181">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="d8d6f-182">Header</span><span class="sxs-lookup"><span data-stu-id="d8d6f-182">Header</span></span><br/> | <dl> <span data-ttu-id="d8d6f-183"><dt>Файл Winnt. h</dt></span><span class="sxs-lookup"><span data-stu-id="d8d6f-183"><dt>Winnt.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d8d6f-184">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d8d6f-184">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d8d6f-185">Константы безопасности WMI</span><span class="sxs-lookup"><span data-stu-id="d8d6f-185">WMI Security Constants</span></span>](wmi-security-constants.md)
</dt> <dt>

[<span data-ttu-id="d8d6f-186">Поддержание безопасности WMI</span><span class="sxs-lookup"><span data-stu-id="d8d6f-186">Maintaining WMI Security</span></span>](maintaining-wmi-security.md)
</dt> </dl>

 

