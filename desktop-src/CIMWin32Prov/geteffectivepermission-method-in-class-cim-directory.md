---
description: Определяет, имеет ли вызывающий объект агрегированные разрешения для \_ объекта каталога CIM, а также общую папку, в которой находится файл или каталог, как указано в аргументе разрешения. Этот метод наследуется от CIM \_ LogicalFile.
ms.assetid: b3dc1e3c-5c99-46ba-93c4-15fbf18e98e8
ms.tgt_platform: multiple
title: Метод Жетеффективепермиссион класса CIM_Directory (Аклуи. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Directory.GetEffectivePermission
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 436a30517b7f3306ef8be2426385fe385947296e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103895718"
---
# <a name="geteffectivepermission-method-of-the-cim_directory-class"></a><span data-ttu-id="03f1d-104">Метод Жетеффективепермиссион \_ класса каталога CIM</span><span class="sxs-lookup"><span data-stu-id="03f1d-104">GetEffectivePermission method of the CIM\_Directory class</span></span>

<span data-ttu-id="03f1d-105">Метод **жетеффективепермиссион** определяет, имеет ли вызывающий объект агрегированные разрешения для объекта [**\_ каталога CIM**](cim-directory.md) , а также общую папку, в которой находится файл или каталог, как указано в аргументе **разрешения** .</span><span class="sxs-lookup"><span data-stu-id="03f1d-105">The **GetEffectivePermission** method determines whether the caller has the aggregated permissions on the [**CIM\_Directory**](cim-directory.md) object, and the share on which the file or directory resides, as specified by the **Permission** argument.</span></span> <span data-ttu-id="03f1d-106">Этот метод наследуется от [**CIM \_ LogicalFile**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="03f1d-106">This method is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="03f1d-107">Классы CIM (модель CIM) в DMTF (распределенная задача управления) являются родительскими классами, на которых строятся классы WMI.</span><span class="sxs-lookup"><span data-stu-id="03f1d-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="03f1d-108">В настоящее время WMI поддерживает только [схемы версии CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="03f1d-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="03f1d-109">В этом разделе используется синтаксис MOF-файл (MOF).</span><span class="sxs-lookup"><span data-stu-id="03f1d-109">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="03f1d-110">Дополнительные сведения об использовании этого метода см. [в разделе вызов метода](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="03f1d-110">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="03f1d-111">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="03f1d-111">Syntax</span></span>


```mof
boolean GetEffectivePermission(
  [in] uint32 Permissions
);
```



## <a name="parameters"></a><span data-ttu-id="03f1d-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="03f1d-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="03f1d-113">*Разрешения* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="03f1d-113">*Permissions* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="03f1d-114">Список разрешений, о которых может запросить пользователь.</span><span class="sxs-lookup"><span data-stu-id="03f1d-114">List of permissions that the user can inquire about.</span></span>

<dt>

<span id="FILE_READ_DATA__file__FILE_LIST_DIRECTORY__directory_"></span><span id="file_read_data__file__file_list_directory__directory_"></span><span id="FILE_READ_DATA__FILE__FILE_LIST_DIRECTORY__DIRECTORY_"></span>

<span data-ttu-id="03f1d-115"><span id="FILE_READ_DATA__file__FILE_LIST_DIRECTORY__directory_"></span><span id="file_read_data__file__file_list_directory__directory_"></span><span id="FILE_READ_DATA__FILE__FILE_LIST_DIRECTORY__DIRECTORY_"></span>**Файл \_ ЧТЕНИЕ \_ данных (файл) \_ каталог списка файлов \_ (каталог)** (1 (0x1))</span><span class="sxs-lookup"><span data-stu-id="03f1d-115"><span id="FILE_READ_DATA__file__FILE_LIST_DIRECTORY__directory_"></span><span id="file_read_data__file__file_list_directory__directory_"></span><span id="FILE_READ_DATA__FILE__FILE_LIST_DIRECTORY__DIRECTORY_"></span>**FILE\_READ\_DATA (file) FILE\_LIST\_DIRECTORY (directory)** (1 (0x1))</span></span>


</dt> <dd>

<span data-ttu-id="03f1d-116">Предоставляет право на чтение данных из файла.</span><span class="sxs-lookup"><span data-stu-id="03f1d-116">Grants the right to read data from the file.</span></span> <span data-ttu-id="03f1d-117">Для каталога это значение предоставляет право на перечисление содержимого каталога.</span><span class="sxs-lookup"><span data-stu-id="03f1d-117">For a directory, this value grants the right to list the contents of the directory.</span></span>

</dd> <dt>

<span id="FILE_WRITE_DATA__file__FILE_ADD_FILE__directory_"></span><span id="file_write_data__file__file_add_file__directory_"></span><span id="FILE_WRITE_DATA__FILE__FILE_ADD_FILE__DIRECTORY_"></span>

<span data-ttu-id="03f1d-118"><span id="FILE_WRITE_DATA__file__FILE_ADD_FILE__directory_"></span><span id="file_write_data__file__file_add_file__directory_"></span><span id="FILE_WRITE_DATA__FILE__FILE_ADD_FILE__DIRECTORY_"></span>**Файл \_ ЗАПИСЬ \_ данных (файл) файл \_ Добавить \_ файл (каталог)** (2 (0x2))</span><span class="sxs-lookup"><span data-stu-id="03f1d-118"><span id="FILE_WRITE_DATA__file__FILE_ADD_FILE__directory_"></span><span id="file_write_data__file__file_add_file__directory_"></span><span id="FILE_WRITE_DATA__FILE__FILE_ADD_FILE__DIRECTORY_"></span>**FILE\_WRITE\_DATA (file) FILE\_ADD\_FILE (directory)** (2 (0x2))</span></span>


</dt> <dd>

<span data-ttu-id="03f1d-119">Предоставляет право на запись данных в файл.</span><span class="sxs-lookup"><span data-stu-id="03f1d-119">Grants the right to write data to the file.</span></span> <span data-ttu-id="03f1d-120">Для каталога это значение предоставляет право на создание файла в каталоге.</span><span class="sxs-lookup"><span data-stu-id="03f1d-120">For a directory, this value grants the right to create a file in the directory.</span></span>

</dd> <dt>

<span id="FILE_APPEND_DATA__file__FILE_ADD_SUBDIRECTORY__directory_"></span><span id="file_append_data__file__file_add_subdirectory__directory_"></span><span id="FILE_APPEND_DATA__FILE__FILE_ADD_SUBDIRECTORY__DIRECTORY_"></span>

<span data-ttu-id="03f1d-121"><span id="FILE_APPEND_DATA__file__FILE_ADD_SUBDIRECTORY__directory_"></span><span id="file_append_data__file__file_add_subdirectory__directory_"></span><span id="FILE_APPEND_DATA__FILE__FILE_ADD_SUBDIRECTORY__DIRECTORY_"></span>**Файл \_ Добавление \_ данных (файл) файл \_ Добавить \_ подкаталог (каталог)** (4 (0x4))</span><span class="sxs-lookup"><span data-stu-id="03f1d-121"><span id="FILE_APPEND_DATA__file__FILE_ADD_SUBDIRECTORY__directory_"></span><span id="file_append_data__file__file_add_subdirectory__directory_"></span><span id="FILE_APPEND_DATA__FILE__FILE_ADD_SUBDIRECTORY__DIRECTORY_"></span>**FILE\_APPEND\_DATA (file) FILE\_ADD\_SUBDIRECTORY (directory)** (4 (0x4))</span></span>


</dt> <dd>

<span data-ttu-id="03f1d-122">Предоставляет право добавлять данные в файл.</span><span class="sxs-lookup"><span data-stu-id="03f1d-122">Grants the right to append data to the file.</span></span> <span data-ttu-id="03f1d-123">Для каталога это значение предоставляет право на создание подкаталога.</span><span class="sxs-lookup"><span data-stu-id="03f1d-123">For a directory, this value grants the right to create a subdirectory.</span></span>

</dd> <dt>

<span id="FILE_READ_EA"></span><span id="file_read_ea"></span>

<span data-ttu-id="03f1d-124"><span id="FILE_READ_EA"></span><span id="file_read_ea"></span>**Файл \_ ЧТЕНИЕ \_ EA** (8 (0x8))</span><span class="sxs-lookup"><span data-stu-id="03f1d-124"><span id="FILE_READ_EA"></span><span id="file_read_ea"></span>**FILE\_READ\_EA** (8 (0x8))</span></span>


</dt> <dd>

<span data-ttu-id="03f1d-125">Предоставляет право на чтение расширенных атрибутов.</span><span class="sxs-lookup"><span data-stu-id="03f1d-125">Grants the right to read extended attributes.</span></span>

</dd> <dt>

<span id="FILE_WRITE_EA"></span><span id="file_write_ea"></span>

<span data-ttu-id="03f1d-126"><span id="FILE_WRITE_EA"></span><span id="file_write_ea"></span>**Файл \_ НАПИСАНие \_ соглашения EA** (16 (0x10))</span><span class="sxs-lookup"><span data-stu-id="03f1d-126"><span id="FILE_WRITE_EA"></span><span id="file_write_ea"></span>**FILE\_WRITE\_EA** (16 (0x10))</span></span>


</dt> <dd>

<span data-ttu-id="03f1d-127">Предоставляет право на запись расширенных атрибутов.</span><span class="sxs-lookup"><span data-stu-id="03f1d-127">Grants the right to write extended attributes.</span></span>

</dd> <dt>

<span id="FILE_EXECUTE__file__FILE_TRAVERSE__directory_"></span><span id="file_execute__file__file_traverse__directory_"></span><span id="FILE_EXECUTE__FILE__FILE_TRAVERSE__DIRECTORY_"></span>

<span data-ttu-id="03f1d-128"><span id="FILE_EXECUTE__file__FILE_TRAVERSE__directory_"></span><span id="file_execute__file__file_traverse__directory_"></span><span id="FILE_EXECUTE__FILE__FILE_TRAVERSE__DIRECTORY_"></span>**Файл \_ ВЫПОЛНИТЬ (файл) \_ обход файла (каталог)** (32 (0x20))</span><span class="sxs-lookup"><span data-stu-id="03f1d-128"><span id="FILE_EXECUTE__file__FILE_TRAVERSE__directory_"></span><span id="file_execute__file__file_traverse__directory_"></span><span id="FILE_EXECUTE__FILE__FILE_TRAVERSE__DIRECTORY_"></span>**FILE\_EXECUTE (file) FILE\_TRAVERSE (directory)** (32 (0x20))</span></span>


</dt> <dd>

<span data-ttu-id="03f1d-129">Предоставляет право на выполнение файла.</span><span class="sxs-lookup"><span data-stu-id="03f1d-129">Grants the right to execute a file.</span></span> <span data-ttu-id="03f1d-130">Для каталога можно просмотреть каталог.</span><span class="sxs-lookup"><span data-stu-id="03f1d-130">For a directory, the directory can be traversed.</span></span>

</dd> <dt>

<span id="FILE_DELETE_CHILD__directory_"></span><span id="file_delete_child__directory_"></span><span id="FILE_DELETE_CHILD__DIRECTORY_"></span>

<span data-ttu-id="03f1d-131"><span id="FILE_DELETE_CHILD__directory_"></span><span id="file_delete_child__directory_"></span><span id="FILE_DELETE_CHILD__DIRECTORY_"></span>**Файл \_ Удаление \_ дочернего (каталога)** (64 (0x40))</span><span class="sxs-lookup"><span data-stu-id="03f1d-131"><span id="FILE_DELETE_CHILD__directory_"></span><span id="file_delete_child__directory_"></span><span id="FILE_DELETE_CHILD__DIRECTORY_"></span>**FILE\_DELETE\_CHILD (directory)** (64 (0x40))</span></span>


</dt> <dd>

<span data-ttu-id="03f1d-132">Предоставляет право на удаление каталога и всех содержащихся в нем файлов, даже если файлы доступны только для чтения.</span><span class="sxs-lookup"><span data-stu-id="03f1d-132">Grants the right to delete a directory and all the files it contains, even if the files are read-only.</span></span>

</dd> <dt>

<span id="FILE_READ_ATTRIBUTES"></span><span id="file_read_attributes"></span>

<span data-ttu-id="03f1d-133"><span id="FILE_READ_ATTRIBUTES"></span><span id="file_read_attributes"></span>**Файл \_ ЧТЕНИЕ \_ атрибутов** (128 (0x80))</span><span class="sxs-lookup"><span data-stu-id="03f1d-133"><span id="FILE_READ_ATTRIBUTES"></span><span id="file_read_attributes"></span>**FILE\_READ\_ATTRIBUTES** (128 (0x80))</span></span>


</dt> <dd>

<span data-ttu-id="03f1d-134">Предоставляет право на чтение атрибутов файлов.</span><span class="sxs-lookup"><span data-stu-id="03f1d-134">Grants the right to read file attributes.</span></span>

</dd> <dt>

<span id="FILE_WRITE_ATTRIBUTES"></span><span id="file_write_attributes"></span>

<span data-ttu-id="03f1d-135"><span id="FILE_WRITE_ATTRIBUTES"></span><span id="file_write_attributes"></span>**Файл \_ ЗАПИСЬ \_ атрибутов** (256 (0x100))</span><span class="sxs-lookup"><span data-stu-id="03f1d-135"><span id="FILE_WRITE_ATTRIBUTES"></span><span id="file_write_attributes"></span>**FILE\_WRITE\_ATTRIBUTES** (256 (0x100))</span></span>


</dt> <dd>

<span data-ttu-id="03f1d-136">Предоставляет право на изменение атрибутов файлов.</span><span class="sxs-lookup"><span data-stu-id="03f1d-136">Grants the right to change file attributes.</span></span>

</dd> <dt>

<span id="DELETE"></span><span id="delete"></span>

<span data-ttu-id="03f1d-137"><span id="DELETE"></span><span id="delete"></span>**Delete** (65536 (0x10000))</span><span class="sxs-lookup"><span data-stu-id="03f1d-137"><span id="DELETE"></span><span id="delete"></span>**DELETE** (65536 (0x10000))</span></span>


</dt> <dd>

<span data-ttu-id="03f1d-138">Предоставляет доступ на удаление.</span><span class="sxs-lookup"><span data-stu-id="03f1d-138">Grants delete access.</span></span>

</dd> <dt>

<span id="READ_CONTROL"></span><span id="read_control"></span>

<span data-ttu-id="03f1d-139"><span id="READ_CONTROL"></span><span id="read_control"></span>**Чтение \_ Элемент управления** (131072 (0x20000))</span><span class="sxs-lookup"><span data-stu-id="03f1d-139"><span id="READ_CONTROL"></span><span id="read_control"></span>**READ\_CONTROL** (131072 (0x20000))</span></span>


</dt> <dd>

<span data-ttu-id="03f1d-140">Предоставляет доступ на чтение дескриптора безопасности и владельца.</span><span class="sxs-lookup"><span data-stu-id="03f1d-140">Grants read access to the security descriptor and owner.</span></span>

</dd> <dt>

<span id="WRITE_DAC"></span><span id="write_dac"></span>

<span data-ttu-id="03f1d-141"><span id="WRITE_DAC"></span><span id="write_dac"></span>**Запись \_ DAC** (262144 (0x40000))</span><span class="sxs-lookup"><span data-stu-id="03f1d-141"><span id="WRITE_DAC"></span><span id="write_dac"></span>**WRITE\_DAC** (262144 (0x40000))</span></span>


</dt> <dd>

<span data-ttu-id="03f1d-142">Предоставляет доступ на запись к избирательному списку управления доступом.</span><span class="sxs-lookup"><span data-stu-id="03f1d-142">Grants write access to the discretionary ACL.</span></span>

</dd> <dt>

<span id="WRITE_OWNER"></span><span id="write_owner"></span>

<span data-ttu-id="03f1d-143"><span id="WRITE_OWNER"></span><span id="write_owner"></span>**Запись \_ Владелец** (524288 (0x80000))</span><span class="sxs-lookup"><span data-stu-id="03f1d-143"><span id="WRITE_OWNER"></span><span id="write_owner"></span>**WRITE\_OWNER** (524288 (0x80000))</span></span>


</dt> <dd>

<span data-ttu-id="03f1d-144">Назначает владельца записи.</span><span class="sxs-lookup"><span data-stu-id="03f1d-144">Assigns the write owner.</span></span>

</dd> <dt>

<span id="SYNCHRONIZE"></span><span id="synchronize"></span>

<span data-ttu-id="03f1d-145"><span id="SYNCHRONIZE"></span><span id="synchronize"></span>**SYNCHRONIZE** (1048576 (0x100000))</span><span class="sxs-lookup"><span data-stu-id="03f1d-145"><span id="SYNCHRONIZE"></span><span id="synchronize"></span>**SYNCHRONIZE** (1048576 (0x100000))</span></span>


</dt> <dd>

<span data-ttu-id="03f1d-146">Синхронизирует доступ и позволяет процессу ожидать, пока объект перейдет в сигнальное состояние.</span><span class="sxs-lookup"><span data-stu-id="03f1d-146">Synchronizes access and allows a process to wait for an object to enter the signaled state.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="03f1d-147">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="03f1d-147">Return value</span></span>

<span data-ttu-id="03f1d-148">Возвращает **значение true** , если вызов имеет необходимое разрешение; в противном случае возвращается **значение false**.</span><span class="sxs-lookup"><span data-stu-id="03f1d-148">Returns **True** if the call has the necessary permission; otherwise, it returns **false**.</span></span>

## <a name="remarks"></a><span data-ttu-id="03f1d-149">Комментарии</span><span class="sxs-lookup"><span data-stu-id="03f1d-149">Remarks</span></span>

<span data-ttu-id="03f1d-150">В настоящее время этот метод не реализован инструментарием WMI.</span><span class="sxs-lookup"><span data-stu-id="03f1d-150">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="03f1d-151">Чтобы использовать этот метод, его необходимо реализовать в собственном поставщике.</span><span class="sxs-lookup"><span data-stu-id="03f1d-151">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="03f1d-152">Эта документация является производной от описаний класса CIM, опубликованных в формате DMTF.</span><span class="sxs-lookup"><span data-stu-id="03f1d-152">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="03f1d-153">Корпорация Майкрософт могла внести изменения в Исправление незначительных ошибок, соответствовать стандартам документации пакета Microsoft SDK или предоставить дополнительные сведения.</span><span class="sxs-lookup"><span data-stu-id="03f1d-153">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="03f1d-154">Требования</span><span class="sxs-lookup"><span data-stu-id="03f1d-154">Requirements</span></span>



| <span data-ttu-id="03f1d-155">Требование</span><span class="sxs-lookup"><span data-stu-id="03f1d-155">Requirement</span></span> | <span data-ttu-id="03f1d-156">Значение</span><span class="sxs-lookup"><span data-stu-id="03f1d-156">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="03f1d-157">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="03f1d-157">Minimum supported client</span></span><br/> | <span data-ttu-id="03f1d-158">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="03f1d-158">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="03f1d-159">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="03f1d-159">Minimum supported server</span></span><br/> | <span data-ttu-id="03f1d-160">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="03f1d-160">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="03f1d-161">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="03f1d-161">Namespace</span></span><br/>                | <span data-ttu-id="03f1d-162">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="03f1d-162">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="03f1d-163">Header</span><span class="sxs-lookup"><span data-stu-id="03f1d-163">Header</span></span><br/>                   | <dl> <span data-ttu-id="03f1d-164"><dt>Аклуи. h</dt></span><span class="sxs-lookup"><span data-stu-id="03f1d-164"><dt>Aclui.h</dt></span></span> </dl>      |
| <span data-ttu-id="03f1d-165">MOF</span><span class="sxs-lookup"><span data-stu-id="03f1d-165">MOF</span></span><br/>                      | <dl> <span data-ttu-id="03f1d-166"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="03f1d-166"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="03f1d-167">DLL</span><span class="sxs-lookup"><span data-stu-id="03f1d-167">DLL</span></span><br/>                      | <dl> <span data-ttu-id="03f1d-168"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="03f1d-168"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="03f1d-169">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="03f1d-169">See also</span></span>

<dl> <dt>

[<span data-ttu-id="03f1d-170">**\_Каталог CIM**</span><span class="sxs-lookup"><span data-stu-id="03f1d-170">**CIM\_Directory**</span></span>](geteffectivepermission-method-in-class-cim-directory.md)
</dt> <dt>

[<span data-ttu-id="03f1d-171">**\_Каталог CIM**</span><span class="sxs-lookup"><span data-stu-id="03f1d-171">**CIM\_Directory**</span></span>](cim-directory.md)
</dt> </dl>

 

