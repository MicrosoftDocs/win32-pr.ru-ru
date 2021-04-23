---
description: Определяет, имеет ли пользователь все необходимые разрешения, указанные в параметре разрешений, определенном для объекта файла подкачки Win32 \_ , каталога и общего ресурса, в котором находится файл подкачки, если файл или каталог находятся в общей папке.
ms.assetid: 1c417ac2-6968-4faf-b596-8df9308f8647
ms.tgt_platform: multiple
title: Метод Жетеффективепермиссион класса Win32_PageFile (Аклуи. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_PageFile.GetEffectivePermission
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: c3b9985d18e93f3a3dbcc8f65484bf3fd72284fd
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103990495"
---
# <a name="geteffectivepermission-method-of-the-win32_pagefile-class"></a><span data-ttu-id="5af43-103">Метод Жетеффективепермиссион \_ класса файла подкачки Win32</span><span class="sxs-lookup"><span data-stu-id="5af43-103">GetEffectivePermission method of the Win32\_PageFile class</span></span>

<span data-ttu-id="5af43-104">Метод [](geteffectivepermission-method-in-class-win32-shortcutfile.md) [класса WMI](/windows/desktop/WmiSdk/retrieving-a-class) жетеффективепермиссион определяет, имеет ли пользователь все необходимые разрешения, указанные в параметре *Permissions* , определенного для объекта файла [**\_ подкачки Win32**](win32-pagefile.md) , каталога и общего ресурса, в котором находится файл подкачки, если файл или каталог находятся в общей папке.</span><span class="sxs-lookup"><span data-stu-id="5af43-104">The [**GetEffectivePermission**](geteffectivepermission-method-in-class-win32-shortcutfile.md) [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method determines whether the user has all of the required permissions specified in the *Permissions* parameter identified for the [**Win32\_PageFile**](win32-pagefile.md) object, directory, and share where the paging file is located, if the file or directory are on a share.</span></span>

<span data-ttu-id="5af43-105">В этом разделе используется синтаксис MOF-файл (MOF).</span><span class="sxs-lookup"><span data-stu-id="5af43-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="5af43-106">Дополнительные сведения об использовании этого метода см. [в разделе вызов метода](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="5af43-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="5af43-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="5af43-107">Syntax</span></span>


```mof
boolean GetEffectivePermission(
  [in] uint32 Permissions
);
```



## <a name="parameters"></a><span data-ttu-id="5af43-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="5af43-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5af43-109">*Разрешения* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="5af43-109">*Permissions* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5af43-110">Битовая карта разрешений, о которых может запросить вызывающий объект.</span><span class="sxs-lookup"><span data-stu-id="5af43-110">Bitmap of permissions that the caller can inquire about.</span></span>

<dt>

<span id="FILE_READ_DATA__file__FILE_LIST_DIRECTORY__directory_"></span><span id="file_read_data__file__file_list_directory__directory_"></span><span id="FILE_READ_DATA__FILE__FILE_LIST_DIRECTORY__DIRECTORY_"></span>

<span data-ttu-id="5af43-111"><span id="FILE_READ_DATA__file__FILE_LIST_DIRECTORY__directory_"></span><span id="file_read_data__file__file_list_directory__directory_"></span><span id="FILE_READ_DATA__FILE__FILE_LIST_DIRECTORY__DIRECTORY_"></span>**Файл \_ ЧТЕНИЕ \_ данных (файл) \_ каталог списка файлов \_ (каталог)** (1 (0x1))</span><span class="sxs-lookup"><span data-stu-id="5af43-111"><span id="FILE_READ_DATA__file__FILE_LIST_DIRECTORY__directory_"></span><span id="file_read_data__file__file_list_directory__directory_"></span><span id="FILE_READ_DATA__FILE__FILE_LIST_DIRECTORY__DIRECTORY_"></span>**FILE\_READ\_DATA (file) FILE\_LIST\_DIRECTORY (directory)** (1 (0x1))</span></span>


</dt> <dd>

<span data-ttu-id="5af43-112">Предоставляет право на чтение данных из файла.</span><span class="sxs-lookup"><span data-stu-id="5af43-112">Grants the right to read data from the file.</span></span> <span data-ttu-id="5af43-113">Для каталога это значение предоставляет право на перечисление содержимого каталога.</span><span class="sxs-lookup"><span data-stu-id="5af43-113">For a directory, this value grants the right to list the contents of the directory.</span></span>

</dd> <dt>

<span id="FILE_WRITE_DATA__file__FILE_ADD_FILE__directory_"></span><span id="file_write_data__file__file_add_file__directory_"></span><span id="FILE_WRITE_DATA__FILE__FILE_ADD_FILE__DIRECTORY_"></span>

<span data-ttu-id="5af43-114"><span id="FILE_WRITE_DATA__file__FILE_ADD_FILE__directory_"></span><span id="file_write_data__file__file_add_file__directory_"></span><span id="FILE_WRITE_DATA__FILE__FILE_ADD_FILE__DIRECTORY_"></span>**Файл \_ ЗАПИСЬ \_ данных (файл) файл \_ Добавить \_ файл (каталог)** (2 (0x2))</span><span class="sxs-lookup"><span data-stu-id="5af43-114"><span id="FILE_WRITE_DATA__file__FILE_ADD_FILE__directory_"></span><span id="file_write_data__file__file_add_file__directory_"></span><span id="FILE_WRITE_DATA__FILE__FILE_ADD_FILE__DIRECTORY_"></span>**FILE\_WRITE\_DATA (file) FILE\_ADD\_FILE (directory)** (2 (0x2))</span></span>


</dt> <dd>

<span data-ttu-id="5af43-115">Предоставляет право на запись данных в файл.</span><span class="sxs-lookup"><span data-stu-id="5af43-115">Grants the right to write data to the file.</span></span> <span data-ttu-id="5af43-116">Для каталога это значение предоставляет право на создание файла в каталоге.</span><span class="sxs-lookup"><span data-stu-id="5af43-116">For a directory, this value grants the right to create a file in the directory.</span></span>

</dd> <dt>

<span id="FILE_APPEND_DATA__file__FILE_ADD_SUBDIRECTORY__directory_"></span><span id="file_append_data__file__file_add_subdirectory__directory_"></span><span id="FILE_APPEND_DATA__FILE__FILE_ADD_SUBDIRECTORY__DIRECTORY_"></span>

<span data-ttu-id="5af43-117"><span id="FILE_APPEND_DATA__file__FILE_ADD_SUBDIRECTORY__directory_"></span><span id="file_append_data__file__file_add_subdirectory__directory_"></span><span id="FILE_APPEND_DATA__FILE__FILE_ADD_SUBDIRECTORY__DIRECTORY_"></span>**Файл \_ Добавление \_ данных (файл) файл \_ Добавить \_ подкаталог (каталог)** (4 (0x4))</span><span class="sxs-lookup"><span data-stu-id="5af43-117"><span id="FILE_APPEND_DATA__file__FILE_ADD_SUBDIRECTORY__directory_"></span><span id="file_append_data__file__file_add_subdirectory__directory_"></span><span id="FILE_APPEND_DATA__FILE__FILE_ADD_SUBDIRECTORY__DIRECTORY_"></span>**FILE\_APPEND\_DATA (file) FILE\_ADD\_SUBDIRECTORY (directory)** (4 (0x4))</span></span>


</dt> <dd>

<span data-ttu-id="5af43-118">Предоставляет право добавлять данные в файл.</span><span class="sxs-lookup"><span data-stu-id="5af43-118">Grants the right to append data to the file.</span></span> <span data-ttu-id="5af43-119">Для каталога это значение предоставляет право на создание подкаталога.</span><span class="sxs-lookup"><span data-stu-id="5af43-119">For a directory, this value grants the right to create a subdirectory.</span></span>

</dd> <dt>

<span id="FILE_READ_EA"></span><span id="file_read_ea"></span>

<span data-ttu-id="5af43-120"><span id="FILE_READ_EA"></span><span id="file_read_ea"></span>**Файл \_ ЧТЕНИЕ \_ EA** (8 (0x8))</span><span class="sxs-lookup"><span data-stu-id="5af43-120"><span id="FILE_READ_EA"></span><span id="file_read_ea"></span>**FILE\_READ\_EA** (8 (0x8))</span></span>


</dt> <dd>

<span data-ttu-id="5af43-121">Предоставляет право на чтение расширенных атрибутов.</span><span class="sxs-lookup"><span data-stu-id="5af43-121">Grants the right to read extended attributes.</span></span>

</dd> <dt>

<span id="FILE_WRITE_EA"></span><span id="file_write_ea"></span>

<span data-ttu-id="5af43-122"><span id="FILE_WRITE_EA"></span><span id="file_write_ea"></span>**Файл \_ НАПИСАНие \_ соглашения EA** (16 (0x10))</span><span class="sxs-lookup"><span data-stu-id="5af43-122"><span id="FILE_WRITE_EA"></span><span id="file_write_ea"></span>**FILE\_WRITE\_EA** (16 (0x10))</span></span>


</dt> <dd>

<span data-ttu-id="5af43-123">Предоставляет право на запись расширенных атрибутов.</span><span class="sxs-lookup"><span data-stu-id="5af43-123">Grants the right to write extended attributes.</span></span>

</dd> <dt>

<span id="FILE_EXECUTE__file__FILE_TRAVERSE_directory_"></span><span id="file_execute__file__file_traverse_directory_"></span><span id="FILE_EXECUTE__FILE__FILE_TRAVERSE_DIRECTORY_"></span>

<span data-ttu-id="5af43-124"><span id="FILE_EXECUTE__file__FILE_TRAVERSE_directory_"></span><span id="file_execute__file__file_traverse_directory_"></span><span id="FILE_EXECUTE__FILE__FILE_TRAVERSE_DIRECTORY_"></span>**Файл \_ ВЫПОЛНИТЬ (файл) \_ обход файла (каталог)** (32 (0x20))</span><span class="sxs-lookup"><span data-stu-id="5af43-124"><span id="FILE_EXECUTE__file__FILE_TRAVERSE_directory_"></span><span id="file_execute__file__file_traverse_directory_"></span><span id="FILE_EXECUTE__FILE__FILE_TRAVERSE_DIRECTORY_"></span>**FILE\_EXECUTE (file) FILE\_TRAVERSE (directory)** (32 (0x20))</span></span>


</dt> <dd>

<span data-ttu-id="5af43-125">Предоставляет право на выполнение файла.</span><span class="sxs-lookup"><span data-stu-id="5af43-125">Grants the right to execute a file.</span></span> <span data-ttu-id="5af43-126">Для каталога можно просмотреть каталог.</span><span class="sxs-lookup"><span data-stu-id="5af43-126">For a directory, the directory can be traversed.</span></span>

</dd> <dt>

<span id="FILE_DELETE_CHILD__directory_"></span><span id="file_delete_child__directory_"></span><span id="FILE_DELETE_CHILD__DIRECTORY_"></span>

<span data-ttu-id="5af43-127"><span id="FILE_DELETE_CHILD__directory_"></span><span id="file_delete_child__directory_"></span><span id="FILE_DELETE_CHILD__DIRECTORY_"></span>**Файл \_ Удаление \_ дочернего (каталога)** (64 (0x40))</span><span class="sxs-lookup"><span data-stu-id="5af43-127"><span id="FILE_DELETE_CHILD__directory_"></span><span id="file_delete_child__directory_"></span><span id="FILE_DELETE_CHILD__DIRECTORY_"></span>**FILE\_DELETE\_CHILD (directory)** (64 (0x40))</span></span>


</dt> <dd>

<span data-ttu-id="5af43-128">Предоставляет право на удаление каталога и всех содержащихся в нем файлов, даже если файлы доступны только для чтения.</span><span class="sxs-lookup"><span data-stu-id="5af43-128">Grants the right to delete a directory and all of the files it contains, even if the files are read-only.</span></span>

</dd> <dt>

<span id="FILE_READ_ATTRIBUTES"></span><span id="file_read_attributes"></span>

<span data-ttu-id="5af43-129"><span id="FILE_READ_ATTRIBUTES"></span><span id="file_read_attributes"></span>**Файл \_ ЧТЕНИЕ \_ атрибутов** (128 (0x80))</span><span class="sxs-lookup"><span data-stu-id="5af43-129"><span id="FILE_READ_ATTRIBUTES"></span><span id="file_read_attributes"></span>**FILE\_READ\_ATTRIBUTES** (128 (0x80))</span></span>


</dt> <dd>

<span data-ttu-id="5af43-130">Предоставляет право на чтение атрибутов файлов.</span><span class="sxs-lookup"><span data-stu-id="5af43-130">Grants the right to read file attributes.</span></span>

</dd> <dt>

<span id="FILE_WRITE_ATTRIBUTES"></span><span id="file_write_attributes"></span>

<span data-ttu-id="5af43-131"><span id="FILE_WRITE_ATTRIBUTES"></span><span id="file_write_attributes"></span>**Файл \_ ЗАПИСЬ \_ атрибутов** (256 (0x100))</span><span class="sxs-lookup"><span data-stu-id="5af43-131"><span id="FILE_WRITE_ATTRIBUTES"></span><span id="file_write_attributes"></span>**FILE\_WRITE\_ATTRIBUTES** (256 (0x100))</span></span>


</dt> <dd>

<span data-ttu-id="5af43-132">Предоставляет право на изменение атрибутов файлов.</span><span class="sxs-lookup"><span data-stu-id="5af43-132">Grants the right to change file attributes.</span></span>

</dd> <dt>

<span id="DELETE"></span><span id="delete"></span>

<span data-ttu-id="5af43-133"><span id="DELETE"></span><span id="delete"></span>**Delete** (65536 (0x10000))</span><span class="sxs-lookup"><span data-stu-id="5af43-133"><span id="DELETE"></span><span id="delete"></span>**DELETE** (65536 (0x10000))</span></span>


</dt> <dd>

<span data-ttu-id="5af43-134">Предоставляет доступ на удаление.</span><span class="sxs-lookup"><span data-stu-id="5af43-134">Grants delete access.</span></span>

</dd> <dt>

<span id="READ_CONTROL"></span><span id="read_control"></span>

<span data-ttu-id="5af43-135"><span id="READ_CONTROL"></span><span id="read_control"></span>**Чтение \_ Элемент управления** (131072 (0x20000))</span><span class="sxs-lookup"><span data-stu-id="5af43-135"><span id="READ_CONTROL"></span><span id="read_control"></span>**READ\_CONTROL** (131072 (0x20000))</span></span>


</dt> <dd>

<span data-ttu-id="5af43-136">Предоставляет доступ на чтение дескриптора безопасности и владельца.</span><span class="sxs-lookup"><span data-stu-id="5af43-136">Grants read access to the security descriptor and owner.</span></span>

</dd> <dt>

<span id="WRITE_DAC"></span><span id="write_dac"></span>

<span data-ttu-id="5af43-137"><span id="WRITE_DAC"></span><span id="write_dac"></span>**Запись \_ DAC** (262144 (0x40000))</span><span class="sxs-lookup"><span data-stu-id="5af43-137"><span id="WRITE_DAC"></span><span id="write_dac"></span>**WRITE\_DAC** (262144 (0x40000))</span></span>


</dt> <dd>

<span data-ttu-id="5af43-138">Предоставляет доступ на запись к списку управления доступом на уровне пользователей (DACL).</span><span class="sxs-lookup"><span data-stu-id="5af43-138">Grants write access to the discretionary access control list (DACL).</span></span>

</dd> <dt>

<span id="WRITE_OWNER"></span><span id="write_owner"></span>

<span data-ttu-id="5af43-139"><span id="WRITE_OWNER"></span><span id="write_owner"></span>**Запись \_ Владелец** (524288 (0x80000))</span><span class="sxs-lookup"><span data-stu-id="5af43-139"><span id="WRITE_OWNER"></span><span id="write_owner"></span>**WRITE\_OWNER** (524288 (0x80000))</span></span>


</dt> <dd>

<span data-ttu-id="5af43-140">Назначает владельца записи.</span><span class="sxs-lookup"><span data-stu-id="5af43-140">Assigns the write owner.</span></span>

</dd> <dt>

<span id="SYNCHRONIZE"></span><span id="synchronize"></span>

<span data-ttu-id="5af43-141"><span id="SYNCHRONIZE"></span><span id="synchronize"></span>**SYNCHRONIZE** (1048576 (0x100000))</span><span class="sxs-lookup"><span data-stu-id="5af43-141"><span id="SYNCHRONIZE"></span><span id="synchronize"></span>**SYNCHRONIZE** (1048576 (0x100000))</span></span>


</dt> <dd>

<span data-ttu-id="5af43-142">Синхронизирует доступ и позволяет процессу ожидать, пока объект перейдет в сигнальное состояние.</span><span class="sxs-lookup"><span data-stu-id="5af43-142">Synchronizes access and allows a process to wait for an object to enter the signaled state.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5af43-143">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="5af43-143">Return value</span></span>

<span data-ttu-id="5af43-144">Возвращает **значение true** , если вызывающий объект имеет указанные разрешения, и **значение false** , если вызывающий объект не имеет указанных разрешений.</span><span class="sxs-lookup"><span data-stu-id="5af43-144">Returns **True** if the caller has the specified permissions, and **false** if the caller does not have the specified permissions.</span></span>

## <a name="requirements"></a><span data-ttu-id="5af43-145">Требования</span><span class="sxs-lookup"><span data-stu-id="5af43-145">Requirements</span></span>



| <span data-ttu-id="5af43-146">Требование</span><span class="sxs-lookup"><span data-stu-id="5af43-146">Requirement</span></span> | <span data-ttu-id="5af43-147">Значение</span><span class="sxs-lookup"><span data-stu-id="5af43-147">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5af43-148">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="5af43-148">Minimum supported client</span></span><br/> | <span data-ttu-id="5af43-149">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="5af43-149">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="5af43-150">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="5af43-150">Minimum supported server</span></span><br/> | <span data-ttu-id="5af43-151">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="5af43-151">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="5af43-152">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="5af43-152">Namespace</span></span><br/>                | <span data-ttu-id="5af43-153">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="5af43-153">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="5af43-154">Header</span><span class="sxs-lookup"><span data-stu-id="5af43-154">Header</span></span><br/>                   | <dl> <span data-ttu-id="5af43-155"><dt>Аклуи. h</dt></span><span class="sxs-lookup"><span data-stu-id="5af43-155"><dt>Aclui.h</dt></span></span> </dl>      |
| <span data-ttu-id="5af43-156">MOF</span><span class="sxs-lookup"><span data-stu-id="5af43-156">MOF</span></span><br/>                      | <dl> <span data-ttu-id="5af43-157"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="5af43-157"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="5af43-158">DLL</span><span class="sxs-lookup"><span data-stu-id="5af43-158">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5af43-159"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5af43-159"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5af43-160">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="5af43-160">See also</span></span>

<dl> <dt>

<span data-ttu-id="5af43-161">[Классы операционной системы](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="5af43-161">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="5af43-162">**\_Файл подкачки Win32**</span><span class="sxs-lookup"><span data-stu-id="5af43-162">**Win32\_PageFile**</span></span>](win32-pagefile.md)
</dt> </dl>

 

