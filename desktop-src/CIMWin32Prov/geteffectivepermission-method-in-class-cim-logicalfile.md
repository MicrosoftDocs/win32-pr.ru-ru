---
description: Определяет, имеет ли вызывающий объект агрегированные разрешения для \_ объекта LOGICALFILE CIM и общую папку, в которой находится файл или каталог, как указано в аргументе Permissions.
ms.assetid: 7b6845df-2427-44a8-bd91-9a4ba65caa51
ms.tgt_platform: multiple
title: Метод Жетеффективепермиссион класса CIM_LogicalFile (Аклуи. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_LogicalFile.GetEffectivePermission
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 8cc578436c5d116e202911d2bb68edf7369564a9
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104141318"
---
# <a name="geteffectivepermission-method-of-the-cim_logicalfile-class"></a><span data-ttu-id="4a233-103">Метод Жетеффективепермиссион \_ класса CIM LogicalFile</span><span class="sxs-lookup"><span data-stu-id="4a233-103">GetEffectivePermission method of the CIM\_LogicalFile class</span></span>

<span data-ttu-id="4a233-104">Метод **жетеффективепермиссион** определяет, есть ли у вызывающего объекта агрегированные разрешения на объект [**CIM \_ LogicalFile**](cim-logicalfile.md) , а также общую папку, в которой находится файл или каталог, как указано в аргументе *Permissions* .</span><span class="sxs-lookup"><span data-stu-id="4a233-104">The **GetEffectivePermission** method determines whether the caller has the aggregated permissions on the [**CIM\_LogicalFile**](cim-logicalfile.md) object, and the share on which the file or directory resides, as specified by the *Permissions* argument.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="4a233-105">Классы CIM (модель CIM) в DMTF (распределенная задача управления) являются родительскими классами, на которых строятся классы WMI.</span><span class="sxs-lookup"><span data-stu-id="4a233-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="4a233-106">В настоящее время WMI поддерживает только [схемы версии CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="4a233-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="4a233-107">В этом разделе используется синтаксис MOF-файл (MOF).</span><span class="sxs-lookup"><span data-stu-id="4a233-107">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="4a233-108">Дополнительные сведения об использовании этого метода см. [в разделе вызов метода](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="4a233-108">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="4a233-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="4a233-109">Syntax</span></span>


```mof
boolean GetEffectivePermission(
  [in] uint32 Permissions
);
```



## <a name="parameters"></a><span data-ttu-id="4a233-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="4a233-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4a233-111">*Разрешения* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="4a233-111">*Permissions* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4a233-112">Список разрешений, о которых может запросить пользователь.</span><span class="sxs-lookup"><span data-stu-id="4a233-112">List of permissions that the user can inquire about.</span></span>

<dt>

<span id="FILE_READ_DATA__file__or_FILE_LIST_DIRECTORY__directory_"></span><span id="file_read_data__file__or_file_list_directory__directory_"></span><span id="FILE_READ_DATA__FILE__OR_FILE_LIST_DIRECTORY__DIRECTORY_"></span>

<span data-ttu-id="4a233-113"><span id="FILE_READ_DATA__file__or_FILE_LIST_DIRECTORY__directory_"></span><span id="file_read_data__file__or_file_list_directory__directory_"></span><span id="FILE_READ_DATA__FILE__OR_FILE_LIST_DIRECTORY__DIRECTORY_"></span>**Файл \_ ЧТЕНИЕ \_ данных (файла) или \_ каталога со списком файлов \_ (каталог)** (1)</span><span class="sxs-lookup"><span data-stu-id="4a233-113"><span id="FILE_READ_DATA__file__or_FILE_LIST_DIRECTORY__directory_"></span><span id="file_read_data__file__or_file_list_directory__directory_"></span><span id="FILE_READ_DATA__FILE__OR_FILE_LIST_DIRECTORY__DIRECTORY_"></span>**FILE\_READ\_DATA (file) or FILE\_LIST\_DIRECTORY (directory)** (1)</span></span>


</dt> <dd>

<span data-ttu-id="4a233-114">Предоставляет право на чтение данных из файла.</span><span class="sxs-lookup"><span data-stu-id="4a233-114">Grants the right to read data from the file.</span></span> <span data-ttu-id="4a233-115">Для каталога это значение предоставляет право на перечисление содержимого каталога.</span><span class="sxs-lookup"><span data-stu-id="4a233-115">For a directory, this value grants the right to list the contents of the directory.</span></span>

</dd> <dt>

<span id="FILE_WRITE_DATA__file__or_FILE_ADD_FILE__directory_"></span><span id="file_write_data__file__or_file_add_file__directory_"></span><span id="FILE_WRITE_DATA__FILE__OR_FILE_ADD_FILE__DIRECTORY_"></span>

<span data-ttu-id="4a233-116"><span id="FILE_WRITE_DATA__file__or_FILE_ADD_FILE__directory_"></span><span id="file_write_data__file__or_file_add_file__directory_"></span><span id="FILE_WRITE_DATA__FILE__OR_FILE_ADD_FILE__DIRECTORY_"></span>**Файл \_ ЗАПИСЬ \_ данных (файл) или \_ Добавление \_ файла (каталог)** (2)</span><span class="sxs-lookup"><span data-stu-id="4a233-116"><span id="FILE_WRITE_DATA__file__or_FILE_ADD_FILE__directory_"></span><span id="file_write_data__file__or_file_add_file__directory_"></span><span id="FILE_WRITE_DATA__FILE__OR_FILE_ADD_FILE__DIRECTORY_"></span>**FILE\_WRITE\_DATA (file) or FILE\_ADD\_FILE (directory)** (2)</span></span>


</dt> <dd>

<span data-ttu-id="4a233-117">Предоставляет право на запись данных в файл.</span><span class="sxs-lookup"><span data-stu-id="4a233-117">Grants the right to write data to the file.</span></span> <span data-ttu-id="4a233-118">Для каталога это значение предоставляет право на создание файла в каталоге.</span><span class="sxs-lookup"><span data-stu-id="4a233-118">For a directory, this value grants the right to create a file in the directory.</span></span>

</dd> <dt>

<span id="FILE_APPEND_DATA__file__or_FILE_ADD_SUBDIRECTORY__directory_"></span><span id="file_append_data__file__or_file_add_subdirectory__directory_"></span><span id="FILE_APPEND_DATA__FILE__OR_FILE_ADD_SUBDIRECTORY__DIRECTORY_"></span>

<span data-ttu-id="4a233-119"><span id="FILE_APPEND_DATA__file__or_FILE_ADD_SUBDIRECTORY__directory_"></span><span id="file_append_data__file__or_file_add_subdirectory__directory_"></span><span id="FILE_APPEND_DATA__FILE__OR_FILE_ADD_SUBDIRECTORY__DIRECTORY_"></span>**Файл \_ Добавление \_ данных (файла) или файла \_ Добавить \_ подкаталог (каталог)** (4)</span><span class="sxs-lookup"><span data-stu-id="4a233-119"><span id="FILE_APPEND_DATA__file__or_FILE_ADD_SUBDIRECTORY__directory_"></span><span id="file_append_data__file__or_file_add_subdirectory__directory_"></span><span id="FILE_APPEND_DATA__FILE__OR_FILE_ADD_SUBDIRECTORY__DIRECTORY_"></span>**FILE\_APPEND\_DATA (file) or FILE\_ADD\_SUBDIRECTORY (directory)** (4)</span></span>


</dt> <dd>

<span data-ttu-id="4a233-120">Предоставляет право добавлять данные в файл.</span><span class="sxs-lookup"><span data-stu-id="4a233-120">Grants the right to append data to the file.</span></span> <span data-ttu-id="4a233-121">Для каталога это значение предоставляет право на создание подкаталога.</span><span class="sxs-lookup"><span data-stu-id="4a233-121">For a directory, this value grants the right to create a subdirectory.</span></span>

</dd> <dt>

<span id="FILE_READ_EA"></span><span id="file_read_ea"></span>

<span data-ttu-id="4a233-122"><span id="FILE_READ_EA"></span><span id="file_read_ea"></span>**Файл \_ ЧТЕНИЕ \_ EA** (8)</span><span class="sxs-lookup"><span data-stu-id="4a233-122"><span id="FILE_READ_EA"></span><span id="file_read_ea"></span>**FILE\_READ\_EA** (8)</span></span>


</dt> <dd>

<span data-ttu-id="4a233-123">Предоставляет право на чтение расширенных атрибутов.</span><span class="sxs-lookup"><span data-stu-id="4a233-123">Grants the right to read extended attributes.</span></span>

</dd> <dt>

<span id="FILE_WRITE_EA"></span><span id="file_write_ea"></span>

<span data-ttu-id="4a233-124"><span id="FILE_WRITE_EA"></span><span id="file_write_ea"></span>**Файл \_ НАПИСАНие \_ соглашения EA** (16)</span><span class="sxs-lookup"><span data-stu-id="4a233-124"><span id="FILE_WRITE_EA"></span><span id="file_write_ea"></span>**FILE\_WRITE\_EA** (16)</span></span>


</dt> <dd>

<span data-ttu-id="4a233-125">Предоставляет право на запись расширенных атрибутов.</span><span class="sxs-lookup"><span data-stu-id="4a233-125">Grants the right to write extended attributes.</span></span>

</dd> <dt>

<span id="FILE_EXECUTE__file__or_FILE_TRAVERSE__directory_"></span><span id="file_execute__file__or_file_traverse__directory_"></span><span id="FILE_EXECUTE__FILE__OR_FILE_TRAVERSE__DIRECTORY_"></span>

<span data-ttu-id="4a233-126"><span id="FILE_EXECUTE__file__or_FILE_TRAVERSE__directory_"></span><span id="file_execute__file__or_file_traverse__directory_"></span><span id="FILE_EXECUTE__FILE__OR_FILE_TRAVERSE__DIRECTORY_"></span>**Файл \_ ВЫПОЛНЕНИЕ (файл) или \_ обход файла (каталог)** (32)</span><span class="sxs-lookup"><span data-stu-id="4a233-126"><span id="FILE_EXECUTE__file__or_FILE_TRAVERSE__directory_"></span><span id="file_execute__file__or_file_traverse__directory_"></span><span id="FILE_EXECUTE__FILE__OR_FILE_TRAVERSE__DIRECTORY_"></span>**FILE\_EXECUTE (file) or FILE\_TRAVERSE (directory)** (32)</span></span>


</dt> <dd>

<span data-ttu-id="4a233-127">Предоставляет право на выполнение файла.</span><span class="sxs-lookup"><span data-stu-id="4a233-127">Grants the right to execute a file.</span></span> <span data-ttu-id="4a233-128">Для каталога можно просмотреть каталог.</span><span class="sxs-lookup"><span data-stu-id="4a233-128">For a directory, the directory can be traversed.</span></span>

</dd> <dt>

<span id="FILE_DELETE_CHILD__directory_"></span><span id="file_delete_child__directory_"></span><span id="FILE_DELETE_CHILD__DIRECTORY_"></span>

<span data-ttu-id="4a233-129"><span id="FILE_DELETE_CHILD__directory_"></span><span id="file_delete_child__directory_"></span><span id="FILE_DELETE_CHILD__DIRECTORY_"></span>**Файл \_ Удаление \_ дочернего (каталога)** (64)</span><span class="sxs-lookup"><span data-stu-id="4a233-129"><span id="FILE_DELETE_CHILD__directory_"></span><span id="file_delete_child__directory_"></span><span id="FILE_DELETE_CHILD__DIRECTORY_"></span>**FILE\_DELETE\_CHILD (directory)** (64)</span></span>


</dt> <dd>

<span data-ttu-id="4a233-130">Предоставляет право на удаление каталога и всех содержащихся в нем файлов, даже если файлы доступны только для чтения.</span><span class="sxs-lookup"><span data-stu-id="4a233-130">Grants the right to delete a directory and all the files it contains, even if the files are read-only.</span></span>

</dd> <dt>

<span id="FILE_READ_ATTRIBUTES"></span><span id="file_read_attributes"></span>

<span data-ttu-id="4a233-131"><span id="FILE_READ_ATTRIBUTES"></span><span id="file_read_attributes"></span>**Файл \_ ЧТЕНИЕ \_ атрибутов** (128)</span><span class="sxs-lookup"><span data-stu-id="4a233-131"><span id="FILE_READ_ATTRIBUTES"></span><span id="file_read_attributes"></span>**FILE\_READ\_ATTRIBUTES** (128)</span></span>


</dt> <dd>

<span data-ttu-id="4a233-132">Предоставляет право на чтение атрибутов файлов.</span><span class="sxs-lookup"><span data-stu-id="4a233-132">Grants the right to read file attributes.</span></span>

</dd> <dt>

<span id="FILE_WRITE_ATTRIBUTES"></span><span id="file_write_attributes"></span>

<span data-ttu-id="4a233-133"><span id="FILE_WRITE_ATTRIBUTES"></span><span id="file_write_attributes"></span>**Файл \_ ЗАПИСЬ \_ атрибутов** (256)</span><span class="sxs-lookup"><span data-stu-id="4a233-133"><span id="FILE_WRITE_ATTRIBUTES"></span><span id="file_write_attributes"></span>**FILE\_WRITE\_ATTRIBUTES** (256)</span></span>


</dt> <dd>

<span data-ttu-id="4a233-134">Предоставляет право на изменение атрибутов файлов.</span><span class="sxs-lookup"><span data-stu-id="4a233-134">Grants the right to change file attributes.</span></span>

</dd> <dt>

<span id="DELETE"></span><span id="delete"></span>

<span data-ttu-id="4a233-135"><span id="DELETE"></span><span id="delete"></span>**Delete** (65536)</span><span class="sxs-lookup"><span data-stu-id="4a233-135"><span id="DELETE"></span><span id="delete"></span>**DELETE** (65536)</span></span>


</dt> <dd>

<span data-ttu-id="4a233-136">Предоставляет доступ на удаление.</span><span class="sxs-lookup"><span data-stu-id="4a233-136">Grants delete access.</span></span>

</dd> <dt>

<span id="READ_CONTROL"></span><span id="read_control"></span>

<span data-ttu-id="4a233-137"><span id="READ_CONTROL"></span><span id="read_control"></span>**Чтение \_ Элемент управления** (131072)</span><span class="sxs-lookup"><span data-stu-id="4a233-137"><span id="READ_CONTROL"></span><span id="read_control"></span>**READ\_CONTROL** (131072)</span></span>


</dt> <dd>

<span data-ttu-id="4a233-138">Предоставляет доступ на чтение дескриптора безопасности и владельца.</span><span class="sxs-lookup"><span data-stu-id="4a233-138">Grants read access to the security descriptor and owner.</span></span>

</dd> <dt>

<span id="WRITE_DAC"></span><span id="write_dac"></span>

<span data-ttu-id="4a233-139"><span id="WRITE_DAC"></span><span id="write_dac"></span>**Запись \_ DAC** (262144)</span><span class="sxs-lookup"><span data-stu-id="4a233-139"><span id="WRITE_DAC"></span><span id="write_dac"></span>**WRITE\_DAC** (262144)</span></span>


</dt> <dd>

<span data-ttu-id="4a233-140">Предоставляет доступ на запись к избирательному списку управления доступом.</span><span class="sxs-lookup"><span data-stu-id="4a233-140">Grants write access to the discretionary ACL.</span></span>

</dd> <dt>

<span id="WRITE_OWNER"></span><span id="write_owner"></span>

<span data-ttu-id="4a233-141"><span id="WRITE_OWNER"></span><span id="write_owner"></span>**Запись \_ Владелец** (524288)</span><span class="sxs-lookup"><span data-stu-id="4a233-141"><span id="WRITE_OWNER"></span><span id="write_owner"></span>**WRITE\_OWNER** (524288)</span></span>


</dt> <dd>

<span data-ttu-id="4a233-142">Назначает владельца записи.</span><span class="sxs-lookup"><span data-stu-id="4a233-142">Assigns the write owner.</span></span>

</dd> <dt>

<span id="SYNCHRONIZE"></span><span id="synchronize"></span>

<span data-ttu-id="4a233-143"><span id="SYNCHRONIZE"></span><span id="synchronize"></span>**Синхронизация** (1048576)</span><span class="sxs-lookup"><span data-stu-id="4a233-143"><span id="SYNCHRONIZE"></span><span id="synchronize"></span>**SYNCHRONIZE** (1048576)</span></span>


</dt> <dd>

<span data-ttu-id="4a233-144">Синхронизирует доступ и позволяет процессу ожидать, пока объект перейдет в сигнальное состояние.</span><span class="sxs-lookup"><span data-stu-id="4a233-144">Synchronizes access and allows a process to wait for an object to enter the signaled state.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4a233-145">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="4a233-145">Return value</span></span>

<span data-ttu-id="4a233-146">Возвращает **значение true** , если вызов имеет необходимое разрешение; в противном случае возвращается **значение false**.</span><span class="sxs-lookup"><span data-stu-id="4a233-146">Returns **True** if the call has the necessary permission; otherwise, it returns **false**.</span></span>

## <a name="remarks"></a><span data-ttu-id="4a233-147">Комментарии</span><span class="sxs-lookup"><span data-stu-id="4a233-147">Remarks</span></span>

<span data-ttu-id="4a233-148">В настоящее время этот метод не реализован инструментарием WMI.</span><span class="sxs-lookup"><span data-stu-id="4a233-148">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="4a233-149">Чтобы использовать этот метод, его необходимо реализовать в собственном поставщике.</span><span class="sxs-lookup"><span data-stu-id="4a233-149">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="4a233-150">Эта документация является производной от описаний класса CIM, опубликованных в формате DMTF.</span><span class="sxs-lookup"><span data-stu-id="4a233-150">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="4a233-151">Корпорация Майкрософт могла внести изменения в Исправление незначительных ошибок, соответствовать стандартам документации пакета Microsoft SDK или предоставить дополнительные сведения.</span><span class="sxs-lookup"><span data-stu-id="4a233-151">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="4a233-152">Требования</span><span class="sxs-lookup"><span data-stu-id="4a233-152">Requirements</span></span>



| <span data-ttu-id="4a233-153">Требование</span><span class="sxs-lookup"><span data-stu-id="4a233-153">Requirement</span></span> | <span data-ttu-id="4a233-154">Значение</span><span class="sxs-lookup"><span data-stu-id="4a233-154">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4a233-155">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="4a233-155">Minimum supported client</span></span><br/> | <span data-ttu-id="4a233-156">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="4a233-156">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="4a233-157">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="4a233-157">Minimum supported server</span></span><br/> | <span data-ttu-id="4a233-158">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="4a233-158">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="4a233-159">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="4a233-159">Namespace</span></span><br/>                | <span data-ttu-id="4a233-160">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="4a233-160">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="4a233-161">Header</span><span class="sxs-lookup"><span data-stu-id="4a233-161">Header</span></span><br/>                   | <dl> <span data-ttu-id="4a233-162"><dt>Аклуи. h</dt></span><span class="sxs-lookup"><span data-stu-id="4a233-162"><dt>Aclui.h</dt></span></span> </dl>      |
| <span data-ttu-id="4a233-163">MOF</span><span class="sxs-lookup"><span data-stu-id="4a233-163">MOF</span></span><br/>                      | <dl> <span data-ttu-id="4a233-164"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="4a233-164"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="4a233-165">DLL</span><span class="sxs-lookup"><span data-stu-id="4a233-165">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4a233-166"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4a233-166"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4a233-167">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="4a233-167">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4a233-168">**\_LOGICALFILE CIM**</span><span class="sxs-lookup"><span data-stu-id="4a233-168">**CIM\_LogicalFile**</span></span>](geteffectivepermission-method-in-class-cim-logicalfile.md)
</dt> <dt>

[<span data-ttu-id="4a233-169">**\_LOGICALFILE CIM**</span><span class="sxs-lookup"><span data-stu-id="4a233-169">**CIM\_LogicalFile**</span></span>](cim-logicalfile.md)
</dt> </dl>

 

