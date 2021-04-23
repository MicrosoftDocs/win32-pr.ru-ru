---
description: Представляет активное сетевое подключение в среде на основе Windows.
ms.assetid: e16e5f13-ea28-4d75-9978-4ff2ef5e5506
ms.tgt_platform: multiple
title: Класс Win32_NetworkConnection
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_NetworkConnection
- Win32_NetworkConnection.Caption
- Win32_NetworkConnection.Description
- Win32_NetworkConnection.InstallDate
- Win32_NetworkConnection.Status
- Win32_NetworkConnection.AccessMask
- Win32_NetworkConnection.Comment
- Win32_NetworkConnection.ConnectionState
- Win32_NetworkConnection.ConnectionType
- Win32_NetworkConnection.DisplayType
- Win32_NetworkConnection.LocalName
- Win32_NetworkConnection.Name
- Win32_NetworkConnection.Persistent
- Win32_NetworkConnection.ProviderName
- Win32_NetworkConnection.RemoteName
- Win32_NetworkConnection.RemotePath
- Win32_NetworkConnection.ResourceType
- Win32_NetworkConnection.UserName
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 96d91008ff8ad2f947e6c9957d16c4f007d15e47
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103807834"
---
# <a name="win32_networkconnection-class"></a><span data-ttu-id="626ae-103">\_Класс Win32 NetworkConnection</span><span class="sxs-lookup"><span data-stu-id="626ae-103">Win32\_NetworkConnection class</span></span>

<span data-ttu-id="626ae-104">[Класс WMI](../wmisdk/retrieving-a-class.md) **\_ NetworkConnection для Win32** представляет активное сетевое подключение в среде на основе Windows.</span><span class="sxs-lookup"><span data-stu-id="626ae-104">The **Win32\_NetworkConnection** [WMI class](../wmisdk/retrieving-a-class.md)represents an active network connection in a Windows-based environment.</span></span>

<span data-ttu-id="626ae-105">Следующий пример синтаксиса — упрощенный MOF-код, который включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="626ae-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="626ae-106">Свойства и методы имеют алфавитный порядок, а не порядок MOF.</span><span class="sxs-lookup"><span data-stu-id="626ae-106">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="626ae-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="626ae-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C4CD-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_NetworkConnection : CIM_LogicalElement
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Status;
  uint32   AccessMask;
  string   Comment;
  string   ConnectionState;
  string   ConnectionType;
  string   DisplayType;
  string   LocalName;
  string   Name;
  boolean  Persistent;
  string   ProviderName;
  string   RemoteName;
  string   RemotePath;
  string   ResourceType;
  string   UserName;
};
```

## <a name="members"></a><span data-ttu-id="626ae-108">Члены</span><span class="sxs-lookup"><span data-stu-id="626ae-108">Members</span></span>

<span data-ttu-id="626ae-109">Класс **Win32 \_ NetworkConnection** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="626ae-109">The **Win32\_NetworkConnection** class has these types of members:</span></span>

-   [<span data-ttu-id="626ae-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="626ae-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="626ae-111">Свойства</span><span class="sxs-lookup"><span data-stu-id="626ae-111">Properties</span></span>

<span data-ttu-id="626ae-112">Класс **Win32 \_ NetworkConnection** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="626ae-112">The **Win32\_NetworkConnection** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="626ae-113">**AccessMask**</span><span class="sxs-lookup"><span data-stu-id="626ae-113">**AccessMask**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="626ae-114">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="626ae-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="626ae-115">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="626ae-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="626ae-116">Квалификаторы: [**схема**](../wmisdk/standard-qualifiers.md) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="626ae-116">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="626ae-117">Список прав доступа к указанному файлу или каталогу, удерживаемому пользователем или группой, от имени которой возвращается экземпляр.</span><span class="sxs-lookup"><span data-stu-id="626ae-117">List of access rights to the given file or directory held by the user or group on whose behalf the instance is returned.</span></span> <span data-ttu-id="626ae-118">На томах FAT вместо него возвращается значение **полного \_ доступа** , указывающее на то, что для объекта не задана безопасность.</span><span class="sxs-lookup"><span data-stu-id="626ae-118">On FAT volumes, the **FULL\_ACCESS** value is returned instead, indicating no security has been set on the object.</span></span>

<dt>

<span id="FILE_READ_DATA__file__or_FILE_LIST_DIRECTORY__directory_"></span><span id="file_read_data__file__or_file_list_directory__directory_"></span><span id="FILE_READ_DATA__FILE__OR_FILE_LIST_DIRECTORY__DIRECTORY_"></span>

<span data-ttu-id="626ae-119"><span id="FILE_READ_DATA__file__or_FILE_LIST_DIRECTORY__directory_"></span><span id="file_read_data__file__or_file_list_directory__directory_"></span><span id="FILE_READ_DATA__FILE__OR_FILE_LIST_DIRECTORY__DIRECTORY_"></span>**Файл \_ ЧТЕНИЕ \_ данных (файла) или \_ каталога со списком файлов \_ (каталог)** (1)</span><span class="sxs-lookup"><span data-stu-id="626ae-119"><span id="FILE_READ_DATA__file__or_FILE_LIST_DIRECTORY__directory_"></span><span id="file_read_data__file__or_file_list_directory__directory_"></span><span id="FILE_READ_DATA__FILE__OR_FILE_LIST_DIRECTORY__DIRECTORY_"></span>**FILE\_READ\_DATA (file) or FILE\_LIST\_DIRECTORY (directory)** (1)</span></span>


</dt> <dd>

<span data-ttu-id="626ae-120">Предоставляет право на чтение данных из файла.</span><span class="sxs-lookup"><span data-stu-id="626ae-120">Grants the right to read data from the file.</span></span> <span data-ttu-id="626ae-121">Для каталога это значение предоставляет право на перечисление содержимого каталога.</span><span class="sxs-lookup"><span data-stu-id="626ae-121">For a directory, this value grants the right to list the contents of the directory.</span></span>

</dd> <dt>

<span id="FILE_WRITE_DATA__file__or_FILE_ADD_FILE__directory_"></span><span id="file_write_data__file__or_file_add_file__directory_"></span><span id="FILE_WRITE_DATA__FILE__OR_FILE_ADD_FILE__DIRECTORY_"></span>

<span data-ttu-id="626ae-122"><span id="FILE_WRITE_DATA__file__or_FILE_ADD_FILE__directory_"></span><span id="file_write_data__file__or_file_add_file__directory_"></span><span id="FILE_WRITE_DATA__FILE__OR_FILE_ADD_FILE__DIRECTORY_"></span>**Файл \_ ЗАПИСЬ \_ данных (файл) или \_ Добавление \_ файла (каталог)** (2)</span><span class="sxs-lookup"><span data-stu-id="626ae-122"><span id="FILE_WRITE_DATA__file__or_FILE_ADD_FILE__directory_"></span><span id="file_write_data__file__or_file_add_file__directory_"></span><span id="FILE_WRITE_DATA__FILE__OR_FILE_ADD_FILE__DIRECTORY_"></span>**FILE\_WRITE\_DATA (file) or FILE\_ADD\_FILE (directory)** (2)</span></span>


</dt> <dd>

<span data-ttu-id="626ae-123">Предоставляет право на запись данных в файл.</span><span class="sxs-lookup"><span data-stu-id="626ae-123">Grants the right to write data to the file.</span></span> <span data-ttu-id="626ae-124">Для каталога это значение предоставляет право на создание файла в каталоге.</span><span class="sxs-lookup"><span data-stu-id="626ae-124">For a directory, this value grants the right to create a file in the directory.</span></span>

</dd> <dt>

<span id="FILE_APPEND_DATA__file__or_FILE_ADD_SUBDIRECTORY"></span><span id="file_append_data__file__or_file_add_subdirectory"></span><span id="FILE_APPEND_DATA__FILE__OR_FILE_ADD_SUBDIRECTORY"></span>

<span data-ttu-id="626ae-125"><span id="FILE_APPEND_DATA__file__or_FILE_ADD_SUBDIRECTORY"></span><span id="file_append_data__file__or_file_add_subdirectory"></span><span id="FILE_APPEND_DATA__FILE__OR_FILE_ADD_SUBDIRECTORY"></span>**Файл \_ Добавление \_ данных (файла) или файла \_ Добавить \_ подкаталог** (4)</span><span class="sxs-lookup"><span data-stu-id="626ae-125"><span id="FILE_APPEND_DATA__file__or_FILE_ADD_SUBDIRECTORY"></span><span id="file_append_data__file__or_file_add_subdirectory"></span><span id="FILE_APPEND_DATA__FILE__OR_FILE_ADD_SUBDIRECTORY"></span>**FILE\_APPEND\_DATA (file) or FILE\_ADD\_SUBDIRECTORY** (4)</span></span>


</dt> <dd>

<span data-ttu-id="626ae-126">Предоставляет право добавлять данные в файл.</span><span class="sxs-lookup"><span data-stu-id="626ae-126">Grants the right to append data to the file.</span></span> <span data-ttu-id="626ae-127">Для каталога это значение предоставляет право на создание подкаталога.</span><span class="sxs-lookup"><span data-stu-id="626ae-127">For a directory, this value grants the right to create a subdirectory.</span></span>

</dd> <dt>

<span id="FILE_READ_EA"></span><span id="file_read_ea"></span>

<span data-ttu-id="626ae-128"><span id="FILE_READ_EA"></span><span id="file_read_ea"></span>**Файл \_ ЧТЕНИЕ \_ EA** (8)</span><span class="sxs-lookup"><span data-stu-id="626ae-128"><span id="FILE_READ_EA"></span><span id="file_read_ea"></span>**FILE\_READ\_EA** (8)</span></span>


</dt> <dd>

<span data-ttu-id="626ae-129">Предоставляет право на чтение расширенных атрибутов.</span><span class="sxs-lookup"><span data-stu-id="626ae-129">Grants the right to read extended attributes.</span></span>

</dd> <dt>

<span id="FILE_WRITE_EA"></span><span id="file_write_ea"></span>

<span data-ttu-id="626ae-130"><span id="FILE_WRITE_EA"></span><span id="file_write_ea"></span>**Файл \_ НАПИСАНие \_ соглашения EA** (16)</span><span class="sxs-lookup"><span data-stu-id="626ae-130"><span id="FILE_WRITE_EA"></span><span id="file_write_ea"></span>**FILE\_WRITE\_EA** (16)</span></span>


</dt> <dd>

<span data-ttu-id="626ae-131">Предоставляет право на запись расширенных атрибутов.</span><span class="sxs-lookup"><span data-stu-id="626ae-131">Grants the right to write extended attributes.</span></span>

</dd> <dt>

<span id="FILE_EXECUTE__file__or_FILE_TRAVERSE__directory_"></span><span id="file_execute__file__or_file_traverse__directory_"></span><span id="FILE_EXECUTE__FILE__OR_FILE_TRAVERSE__DIRECTORY_"></span>

<span data-ttu-id="626ae-132"><span id="FILE_EXECUTE__file__or_FILE_TRAVERSE__directory_"></span><span id="file_execute__file__or_file_traverse__directory_"></span><span id="FILE_EXECUTE__FILE__OR_FILE_TRAVERSE__DIRECTORY_"></span>**Файл \_ ВЫПОЛНЕНИЕ (файл) или \_ обход файла (каталог)** (32)</span><span class="sxs-lookup"><span data-stu-id="626ae-132"><span id="FILE_EXECUTE__file__or_FILE_TRAVERSE__directory_"></span><span id="file_execute__file__or_file_traverse__directory_"></span><span id="FILE_EXECUTE__FILE__OR_FILE_TRAVERSE__DIRECTORY_"></span>**FILE\_EXECUTE (file) or FILE\_TRAVERSE (directory)** (32)</span></span>


</dt> <dd>

<span data-ttu-id="626ae-133">Предоставляет право на выполнение файла.</span><span class="sxs-lookup"><span data-stu-id="626ae-133">Grants the right to execute a file.</span></span> <span data-ttu-id="626ae-134">Для каталога можно просмотреть каталог.</span><span class="sxs-lookup"><span data-stu-id="626ae-134">For a directory, the directory can be traversed.</span></span>

</dd> <dt>

<span id="FILE_DELETE_CHILD__directory_"></span><span id="file_delete_child__directory_"></span><span id="FILE_DELETE_CHILD__DIRECTORY_"></span>

<span data-ttu-id="626ae-135"><span id="FILE_DELETE_CHILD__directory_"></span><span id="file_delete_child__directory_"></span><span id="FILE_DELETE_CHILD__DIRECTORY_"></span>**Файл \_ Удаление \_ дочернего (каталога)** (64)</span><span class="sxs-lookup"><span data-stu-id="626ae-135"><span id="FILE_DELETE_CHILD__directory_"></span><span id="file_delete_child__directory_"></span><span id="FILE_DELETE_CHILD__DIRECTORY_"></span>**FILE\_DELETE\_CHILD (directory)** (64)</span></span>


</dt> <dd>

<span data-ttu-id="626ae-136">Предоставляет право удалять каталог и все содержащиеся в нем файлы (дочерние элементы), даже если файлы доступны только для чтения.</span><span class="sxs-lookup"><span data-stu-id="626ae-136">Grants the right to delete a directory and all of the files it contains (its children), even if the files are read-only.</span></span>

</dd> <dt>

<span id="FILE_READ_ATTRIBUTES"></span><span id="file_read_attributes"></span>

<span data-ttu-id="626ae-137"><span id="FILE_READ_ATTRIBUTES"></span><span id="file_read_attributes"></span>**Файл \_ ЧТЕНИЕ \_ атрибутов** (128)</span><span class="sxs-lookup"><span data-stu-id="626ae-137"><span id="FILE_READ_ATTRIBUTES"></span><span id="file_read_attributes"></span>**FILE\_READ\_ATTRIBUTES** (128)</span></span>


</dt> <dd>

<span data-ttu-id="626ae-138">Предоставляет право на чтение атрибутов файлов.</span><span class="sxs-lookup"><span data-stu-id="626ae-138">Grants the right to read file attributes.</span></span>

</dd> <dt>

<span id="FILE_WRITE_ATTRIBUTES"></span><span id="file_write_attributes"></span>

<span data-ttu-id="626ae-139"><span id="FILE_WRITE_ATTRIBUTES"></span><span id="file_write_attributes"></span>**Файл \_ ЗАПИСЬ \_ атрибутов** (256)</span><span class="sxs-lookup"><span data-stu-id="626ae-139"><span id="FILE_WRITE_ATTRIBUTES"></span><span id="file_write_attributes"></span>**FILE\_WRITE\_ATTRIBUTES** (256)</span></span>


</dt> <dd>

<span data-ttu-id="626ae-140">Предоставляет право на изменение атрибутов файлов.</span><span class="sxs-lookup"><span data-stu-id="626ae-140">Grants the right to change file attributes.</span></span>

</dd> <dt>

<span id="DELETE"></span><span id="delete"></span>

<span data-ttu-id="626ae-141"><span id="DELETE"></span><span id="delete"></span>**Delete** (65536)</span><span class="sxs-lookup"><span data-stu-id="626ae-141"><span id="DELETE"></span><span id="delete"></span>**DELETE** (65536)</span></span>


</dt> <dd>

<span data-ttu-id="626ae-142">Предоставляет доступ на удаление.</span><span class="sxs-lookup"><span data-stu-id="626ae-142">Grants delete access.</span></span>

</dd> <dt>

<span id="READ_CONTROL"></span><span id="read_control"></span>

<span data-ttu-id="626ae-143"><span id="READ_CONTROL"></span><span id="read_control"></span>**Чтение \_ Элемент управления** (131072)</span><span class="sxs-lookup"><span data-stu-id="626ae-143"><span id="READ_CONTROL"></span><span id="read_control"></span>**READ\_CONTROL** (131072)</span></span>


</dt> <dd>

<span data-ttu-id="626ae-144">Предоставляет доступ на чтение дескриптора безопасности и владельца.</span><span class="sxs-lookup"><span data-stu-id="626ae-144">Grants read access to the security descriptor and owner.</span></span>

</dd> <dt>

<span id="WRITE_DAC"></span><span id="write_dac"></span>

<span data-ttu-id="626ae-145"><span id="WRITE_DAC"></span><span id="write_dac"></span>**Запись \_ DAC** (262144)</span><span class="sxs-lookup"><span data-stu-id="626ae-145"><span id="WRITE_DAC"></span><span id="write_dac"></span>**WRITE\_DAC** (262144)</span></span>


</dt> <dd>

<span data-ttu-id="626ae-146">Предоставляет доступ на запись к списку управления доступом на уровне пользователей (DACL).</span><span class="sxs-lookup"><span data-stu-id="626ae-146">Grants write access to the discretionary access control list (DACL).</span></span>

</dd> <dt>

<span id="WRITE_OWNER"></span><span id="write_owner"></span>

<span data-ttu-id="626ae-147"><span id="WRITE_OWNER"></span><span id="write_owner"></span>**Запись \_ Владелец** (524288)</span><span class="sxs-lookup"><span data-stu-id="626ae-147"><span id="WRITE_OWNER"></span><span id="write_owner"></span>**WRITE\_OWNER** (524288)</span></span>


</dt> <dd>

<span data-ttu-id="626ae-148">Назначает владельца записи.</span><span class="sxs-lookup"><span data-stu-id="626ae-148">Assigns the write owner.</span></span>

</dd> <dt>

<span id="SYNCHRONIZE"></span><span id="synchronize"></span>

<span data-ttu-id="626ae-149"><span id="SYNCHRONIZE"></span><span id="synchronize"></span>**Синхронизация** (1048576)</span><span class="sxs-lookup"><span data-stu-id="626ae-149"><span id="SYNCHRONIZE"></span><span id="synchronize"></span>**SYNCHRONIZE** (1048576)</span></span>


</dt> <dd>

<span data-ttu-id="626ae-150">Синхронизирует доступ и позволяет процессу ожидать, пока объект перейдет в сигнальное состояние.</span><span class="sxs-lookup"><span data-stu-id="626ae-150">Synchronizes access and allows a process to wait for an object to enter the signaled state.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="626ae-151">**Заголовок**</span><span class="sxs-lookup"><span data-stu-id="626ae-151">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="626ae-152">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="626ae-152">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="626ae-153">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="626ae-153">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="626ae-154">Квалификаторы: [**maxlen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="626ae-154">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="626ae-155">Краткое текстовое описание объекта.</span><span class="sxs-lookup"><span data-stu-id="626ae-155">A short textual description of the object.</span></span>

<span data-ttu-id="626ae-156">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="626ae-156">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="626ae-157">**Комментарий**</span><span class="sxs-lookup"><span data-stu-id="626ae-157">**Comment**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="626ae-158">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="626ae-158">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="626ae-159">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="626ae-159">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="626ae-160">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32API \| сетевые структуры Windows \| [**нетресаурце**](/windows/win32/api/rrascfg/nn-rrascfg-ieapproviderconfig) \| *лпкоммент*")</span><span class="sxs-lookup"><span data-stu-id="626ae-160">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Windows Networking Structures\|[**NETRESOURCE**](/windows/win32/api/rrascfg/nn-rrascfg-ieapproviderconfig)\|*lpComment*")</span></span>
</dt> </dl>

<span data-ttu-id="626ae-161">Комментарий, предоставленный поставщиком сети.</span><span class="sxs-lookup"><span data-stu-id="626ae-161">Comment supplied by the network provider.</span></span>

</dd> <dt>

<span data-ttu-id="626ae-162">**ConnectionState**</span><span class="sxs-lookup"><span data-stu-id="626ae-162">**ConnectionState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="626ae-163">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="626ae-163">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="626ae-164">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="626ae-164">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="626ae-165">Квалификаторы: [**maxlen**](../wmisdk/standard-qualifiers.md) (20), [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32API \| сетевые структуры управления \| [**используют \_ сведения \_ 1**](/windows/win32/api/lmuse/ns-lmuse-use_info_1) \| **ui1 \_ Status**")</span><span class="sxs-lookup"><span data-stu-id="626ae-165">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (20), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Network Management Structures\|[**USE\_INFO\_1**](/windows/win32/api/lmuse/ns-lmuse-use_info_1)\|**ui1\_status**")</span></span>
</dt> </dl>

<span data-ttu-id="626ae-166">Текущее состояние сетевого подключения.</span><span class="sxs-lookup"><span data-stu-id="626ae-166">Current state of the network connection.</span></span>

<dt>

<span id="Connected"></span><span id="connected"></span><span id="CONNECTED"></span>

<span data-ttu-id="626ae-167">**Подключено** ("подключено")</span><span class="sxs-lookup"><span data-stu-id="626ae-167">**Connected** ("Connected")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="626ae-168">**Ошибка** ("ошибка")</span><span class="sxs-lookup"><span data-stu-id="626ae-168">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="626ae-169">**Приостановлено** ("приостановлено")</span><span class="sxs-lookup"><span data-stu-id="626ae-169">**Paused** ("Paused")</span></span>


</dt> <dd></dd> <dt>

<span id="Disconnected"></span><span id="disconnected"></span><span id="DISCONNECTED"></span>

<span data-ttu-id="626ae-170">**Отключено** ("отключено")</span><span class="sxs-lookup"><span data-stu-id="626ae-170">**Disconnected** ("Disconnected")</span></span>


</dt> <dd></dd> <dt>

<span id="Connecting"></span><span id="connecting"></span><span id="CONNECTING"></span>

<span data-ttu-id="626ae-171">**Подключение** ("подключение")</span><span class="sxs-lookup"><span data-stu-id="626ae-171">**Connecting** ("Connecting")</span></span>


</dt> <dd></dd> <dt>

<span id="Reconnecting"></span><span id="reconnecting"></span><span id="RECONNECTING"></span>

<span data-ttu-id="626ae-172">**Повторное подключение** ("повторное подключение")</span><span class="sxs-lookup"><span data-stu-id="626ae-172">**Reconnecting** ("Reconnecting")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="626ae-173">**ConnectionType**</span><span class="sxs-lookup"><span data-stu-id="626ae-173">**ConnectionType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="626ae-174">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="626ae-174">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="626ae-175">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="626ae-175">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="626ae-176">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32API \| сетевые структуры Windows \| [**нетресаурце**](/windows/win32/api/rrascfg/nn-rrascfg-ieapproviderconfig) \| **двскопе**")</span><span class="sxs-lookup"><span data-stu-id="626ae-176">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Windows Networking Structures\|[**NETRESOURCE**](/windows/win32/api/rrascfg/nn-rrascfg-ieapproviderconfig)\|**dwScope**")</span></span>
</dt> </dl>

<span data-ttu-id="626ae-177">Тип сохраняемости соединения, используемого для подключения к сети.</span><span class="sxs-lookup"><span data-stu-id="626ae-177">Persistence type of the connection used for connecting to the network.</span></span>

<dt>

<span id="Current_Connection"></span><span id="current_connection"></span><span id="CURRENT_CONNECTION"></span>

<span data-ttu-id="626ae-178">**Текущее соединение** ("текущее соединение")</span><span class="sxs-lookup"><span data-stu-id="626ae-178">**Current Connection** ("Current Connection")</span></span>


</dt> <dd></dd> <dt>

<span id="Persistent_Connection"></span><span id="persistent_connection"></span><span id="PERSISTENT_CONNECTION"></span>

<span data-ttu-id="626ae-179">**Постоянное подключение** (постоянное подключение)</span><span class="sxs-lookup"><span data-stu-id="626ae-179">**Persistent Connection** ("Persistent Connection")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="626ae-180">**Описание**</span><span class="sxs-lookup"><span data-stu-id="626ae-180">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="626ae-181">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="626ae-181">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="626ae-182">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="626ae-182">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="626ae-183">Квалификаторы: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Описание")</span><span class="sxs-lookup"><span data-stu-id="626ae-183">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="626ae-184">Текстовое описание объекта.</span><span class="sxs-lookup"><span data-stu-id="626ae-184">A textual description of the object.</span></span>

<span data-ttu-id="626ae-185">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="626ae-185">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="626ae-186">**дисплайтипе**</span><span class="sxs-lookup"><span data-stu-id="626ae-186">**DisplayType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="626ae-187">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="626ae-187">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="626ae-188">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="626ae-188">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="626ae-189">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32API \| сетевые структуры Windows \| [**нетресаурце**](/windows/win32/api/rrascfg/nn-rrascfg-ieapproviderconfig) \| **двдисплайтипе**")</span><span class="sxs-lookup"><span data-stu-id="626ae-189">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Windows Networking Structures\|[**NETRESOURCE**](/windows/win32/api/rrascfg/nn-rrascfg-ieapproviderconfig)\|**dwDisplayType**")</span></span>
</dt> </dl>

<span data-ttu-id="626ae-190">Сетевой объект должен отображаться в пользовательском интерфейсе обзора сети.</span><span class="sxs-lookup"><span data-stu-id="626ae-190">Network object should be displayed in a network browsing user interface.</span></span>

<dt>

<span id="Domain"></span><span id="domain"></span><span id="DOMAIN"></span>

<span data-ttu-id="626ae-191">**Домен** ("домен")</span><span class="sxs-lookup"><span data-stu-id="626ae-191">**Domain** ("Domain")</span></span>


</dt> <dd></dd> <dt>

<span id="Generic"></span><span id="generic"></span><span id="GENERIC"></span>

<span data-ttu-id="626ae-192">**Универсальный** ("универсальный")</span><span class="sxs-lookup"><span data-stu-id="626ae-192">**Generic** ("Generic")</span></span>


</dt> <dd></dd> <dt>

<span id="Server"></span><span id="server"></span><span id="SERVER"></span>

<span data-ttu-id="626ae-193">**Сервер** ("сервер")</span><span class="sxs-lookup"><span data-stu-id="626ae-193">**Server** ("Server")</span></span>


</dt> <dd></dd> <dt>

<span id="Share"></span><span id="share"></span><span id="SHARE"></span>

<span data-ttu-id="626ae-194">**Общий доступ** ("общий доступ")</span><span class="sxs-lookup"><span data-stu-id="626ae-194">**Share** ("Share")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="626ae-195">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="626ae-195">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="626ae-196">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="626ae-196">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="626ae-197">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="626ae-197">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="626ae-198">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) (MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](../wmisdk/standard-qualifiers.md) (" Дата установки ")</span><span class="sxs-lookup"><span data-stu-id="626ae-198">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="626ae-199">Указывает, когда был установлен объект.</span><span class="sxs-lookup"><span data-stu-id="626ae-199">Indicates when the object was installed.</span></span> <span data-ttu-id="626ae-200">Отсутствие значения не означает, что объект не установлен.</span><span class="sxs-lookup"><span data-stu-id="626ae-200">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="626ae-201">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="626ae-201">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="626ae-202">**Локально**</span><span class="sxs-lookup"><span data-stu-id="626ae-202">**LocalName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="626ae-203">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="626ae-203">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="626ae-204">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="626ae-204">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="626ae-205">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32API \| сетевые структуры Windows \| [**нетресаурце**](/windows/win32/api/rrascfg/nn-rrascfg-ieapproviderconfig) \| **лплокалнаме**")</span><span class="sxs-lookup"><span data-stu-id="626ae-205">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Windows Networking Structures\|[**NETRESOURCE**](/windows/win32/api/rrascfg/nn-rrascfg-ieapproviderconfig)\|**lpLocalName**")</span></span>
</dt> </dl>

<span data-ttu-id="626ae-206">Локальное имя подключенного сетевого устройства.</span><span class="sxs-lookup"><span data-stu-id="626ae-206">Local name of the connected network device.</span></span>

<span data-ttu-id="626ae-207">Пример: "c: \\ Public"</span><span class="sxs-lookup"><span data-stu-id="626ae-207">Example: "c:\\public"</span></span>

</dd> <dt>

<span data-ttu-id="626ae-208">**Name**</span><span class="sxs-lookup"><span data-stu-id="626ae-208">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="626ae-209">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="626ae-209">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="626ae-210">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="626ae-210">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="626ae-211">Квалификаторы: [**ключ**](../wmisdk/key-qualifier.md), [**Переопределение**](../wmisdk/standard-qualifiers.md) ("имя"), [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32API Network Structures \| \| [**нетресаурце**](/windows/win32/api/rrascfg/nn-rrascfg-ieapproviderconfig)")</span><span class="sxs-lookup"><span data-stu-id="626ae-211">Qualifiers: [**key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("Name"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Windows Networking Structures\|[**NETRESOURCE**](/windows/win32/api/rrascfg/nn-rrascfg-ieapproviderconfig)")</span></span>
</dt> </dl>

<span data-ttu-id="626ae-212">Имя текущего сетевого подключения.</span><span class="sxs-lookup"><span data-stu-id="626ae-212">Name of the current network connection.</span></span> <span data-ttu-id="626ae-213">Это сочетание значений в **ремотенаме** и **LocalName**.</span><span class="sxs-lookup"><span data-stu-id="626ae-213">It is the combination of the values in **RemoteName** and **LocalName**.</span></span>

<span data-ttu-id="626ae-214">Пример: " \\ \\ нтрелеасе (c: \\ public)"</span><span class="sxs-lookup"><span data-stu-id="626ae-214">Example: "\\\\NTRELEASE (c:\\public)"</span></span>

</dd> <dt>

<span data-ttu-id="626ae-215">**Persistent**</span><span class="sxs-lookup"><span data-stu-id="626ae-215">**Persistent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="626ae-216">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="626ae-216">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="626ae-217">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="626ae-217">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="626ae-218">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32API \| сетевые функции Windows \| [**внетенумресаурце**](/windows/win32/api/winnetwk/nf-winnetwk-wnetenumresourcea)")</span><span class="sxs-lookup"><span data-stu-id="626ae-218">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Windows Networking Functions\|[**WNetEnumResource**](/windows/win32/api/winnetwk/nf-winnetwk-wnetenumresourcea)")</span></span>
</dt> </dl>

<span data-ttu-id="626ae-219">Подключение будет автоматически подключено операционной системой при следующем входе в систему.</span><span class="sxs-lookup"><span data-stu-id="626ae-219">Connection will be reconnected automatically by the operating system on the next logon.</span></span>

</dd> <dt>

<span data-ttu-id="626ae-220">**ProviderName**</span><span class="sxs-lookup"><span data-stu-id="626ae-220">**ProviderName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="626ae-221">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="626ae-221">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="626ae-222">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="626ae-222">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="626ae-223">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32API \| сетевые структуры Windows \| [**нетресаурце**](/windows/win32/api/rrascfg/nn-rrascfg-ieapproviderconfig) \| **лппровидер**")</span><span class="sxs-lookup"><span data-stu-id="626ae-223">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Windows Networking Structures\|[**NETRESOURCE**](/windows/win32/api/rrascfg/nn-rrascfg-ieapproviderconfig)\|**lpProvider**")</span></span>
</dt> </dl>

<span data-ttu-id="626ae-224">Имя поставщика, владеющего ресурсом.</span><span class="sxs-lookup"><span data-stu-id="626ae-224">Name of the provider that owns the resource.</span></span> <span data-ttu-id="626ae-225">Это свойство может иметь **значение NULL** , если имя поставщика неизвестно.</span><span class="sxs-lookup"><span data-stu-id="626ae-225">This property can be **NULL** if the provider name is unknown.</span></span>

</dd> <dt>

<span data-ttu-id="626ae-226">**ремотенаме**</span><span class="sxs-lookup"><span data-stu-id="626ae-226">**RemoteName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="626ae-227">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="626ae-227">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="626ae-228">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="626ae-228">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="626ae-229">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32API \| сетевые структуры Windows \| [**нетресаурце**](/windows/win32/api/rrascfg/nn-rrascfg-ieapproviderconfig) \| **лпремотенаме**")</span><span class="sxs-lookup"><span data-stu-id="626ae-229">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Windows Networking Structures\|[**NETRESOURCE**](/windows/win32/api/rrascfg/nn-rrascfg-ieapproviderconfig)\|**lpRemoteName**")</span></span>
</dt> </dl>

<span data-ttu-id="626ae-230">Имя удаленного сетевого ресурса для сетевого ресурса.</span><span class="sxs-lookup"><span data-stu-id="626ae-230">Remote network resource name for a network resource.</span></span> <span data-ttu-id="626ae-231">Для текущего или постоянного подключения **ремотенаме** содержит сетевое имя, связанное с именем значения в свойстве **LocalName** .</span><span class="sxs-lookup"><span data-stu-id="626ae-231">For a current or persistent connection, **RemoteName** contains the network name associated with the name of the value in the **LocalName** property.</span></span> <span data-ttu-id="626ae-232">Имя в **ремотенаме** должно соответствовать соглашениям об именовании поставщика сетевых услуг.</span><span class="sxs-lookup"><span data-stu-id="626ae-232">The name in **RemoteName** must follow the network provider's naming conventions.</span></span>

<span data-ttu-id="626ae-233">Пример: " \\ \\ нтрелеасе"</span><span class="sxs-lookup"><span data-stu-id="626ae-233">Example: "\\\\NTRELEASE"</span></span>

</dd> <dt>

<span data-ttu-id="626ae-234">**RemotePath**</span><span class="sxs-lookup"><span data-stu-id="626ae-234">**RemotePath**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="626ae-235">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="626ae-235">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="626ae-236">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="626ae-236">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="626ae-237">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32API \| сетевые структуры Windows \| [**нетресаурце**](/windows/win32/api/rrascfg/nn-rrascfg-ieapproviderconfig) \| **лпремотенаме**")</span><span class="sxs-lookup"><span data-stu-id="626ae-237">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Windows Networking Structures\|[**NETRESOURCE**](/windows/win32/api/rrascfg/nn-rrascfg-ieapproviderconfig)\|**lpRemoteName**")</span></span>
</dt> </dl>

<span data-ttu-id="626ae-238">Полный путь к сетевому ресурсу.</span><span class="sxs-lookup"><span data-stu-id="626ae-238">Full path to the network resource.</span></span>

<span data-ttu-id="626ae-239">Пример: " \\ \\ infosrv1 \\ Public"</span><span class="sxs-lookup"><span data-stu-id="626ae-239">Example: "\\\\infosrv1\\public"</span></span>

</dd> <dt>

<span data-ttu-id="626ae-240">**ResourceType**</span><span class="sxs-lookup"><span data-stu-id="626ae-240">**ResourceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="626ae-241">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="626ae-241">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="626ae-242">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="626ae-242">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="626ae-243">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32API \| сетевые структуры Windows \| [**нетресаурце**](/windows/win32/api/rrascfg/nn-rrascfg-ieapproviderconfig) \| **двтипе**")</span><span class="sxs-lookup"><span data-stu-id="626ae-243">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Windows Networking Structures\|[**NETRESOURCE**](/windows/win32/api/rrascfg/nn-rrascfg-ieapproviderconfig)\|**dwType**")</span></span>
</dt> </dl>

<span data-ttu-id="626ae-244">Тип ресурса для перечисления или подключения.</span><span class="sxs-lookup"><span data-stu-id="626ae-244">Type of resource to enumerate or connect to.</span></span>

<dt>

<span id="Disk"></span><span id="disk"></span><span id="DISK"></span>

<span data-ttu-id="626ae-245">**Диск** ("диск")</span><span class="sxs-lookup"><span data-stu-id="626ae-245">**Disk** ("Disk")</span></span>


</dt> <dd></dd> <dt>

<span id="Print"></span><span id="print"></span><span id="PRINT"></span>

<span data-ttu-id="626ae-246">**Печать** ("Печать")</span><span class="sxs-lookup"><span data-stu-id="626ae-246">**Print** ("Print")</span></span>


</dt> <dd></dd> <dt>

<span id="Any"></span><span id="any"></span><span id="ANY"></span>

<span data-ttu-id="626ae-247">**ANY** («Any»)</span><span class="sxs-lookup"><span data-stu-id="626ae-247">**Any** ("Any")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="626ae-248">**Состояние**</span><span class="sxs-lookup"><span data-stu-id="626ae-248">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="626ae-249">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="626ae-249">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="626ae-250">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="626ae-250">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="626ae-251">Квалификаторы: [**maxlen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("состояние")</span><span class="sxs-lookup"><span data-stu-id="626ae-251">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="626ae-252">Строка, указывающая текущее состояние объекта.</span><span class="sxs-lookup"><span data-stu-id="626ae-252">String that indicates the current status of the object.</span></span> <span data-ttu-id="626ae-253">Можно определить операционное и нерабочее состояние.</span><span class="sxs-lookup"><span data-stu-id="626ae-253">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="626ae-254">Оперативное состояние может включать "ОК", "деградация" и "пред Fail".</span><span class="sxs-lookup"><span data-stu-id="626ae-254">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="626ae-255">"Пред-Fail" указывает, что элемент работает правильно, но прогнозирует сбой (например, жесткий диск с поддержкой SMART).</span><span class="sxs-lookup"><span data-stu-id="626ae-255">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="626ae-256">Нерабочее состояние может включать "Error", "starting", "остановка" и "обслуживание".</span><span class="sxs-lookup"><span data-stu-id="626ae-256">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="626ae-257">"Служба" может применяться при зеркальном отображении дисков, перезагрузке списка разрешений пользователя или выполнении других административных задач.</span><span class="sxs-lookup"><span data-stu-id="626ae-257">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="626ae-258">Не вся такая работа находится в оперативном режиме, но управляемый элемент не является ни "ОК", ни в одном из других состояний.</span><span class="sxs-lookup"><span data-stu-id="626ae-258">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="626ae-259">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="626ae-259">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="626ae-260">В эти значения входят:</span><span class="sxs-lookup"><span data-stu-id="626ae-260">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="626ae-261">**ОК** ("ОК")</span><span class="sxs-lookup"><span data-stu-id="626ae-261">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="626ae-262">**Ошибка** ("ошибка")</span><span class="sxs-lookup"><span data-stu-id="626ae-262">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="626ae-263">**Пониженная работоспособность** (пониженная работоспособность)</span><span class="sxs-lookup"><span data-stu-id="626ae-263">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="626ae-264">**Неизвестно** ("неизвестно")</span><span class="sxs-lookup"><span data-stu-id="626ae-264">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="626ae-265">**Пред-ошибка** ("пред Fail")</span><span class="sxs-lookup"><span data-stu-id="626ae-265">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="626ae-266">**Запуск** ("Запуск")</span><span class="sxs-lookup"><span data-stu-id="626ae-266">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="626ae-267">**Остановка** ("остановка")</span><span class="sxs-lookup"><span data-stu-id="626ae-267">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="626ae-268">**Служба** ("служба")</span><span class="sxs-lookup"><span data-stu-id="626ae-268">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="626ae-269">**Пренапряжению** ("напряжению")</span><span class="sxs-lookup"><span data-stu-id="626ae-269">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="626ae-270">**Невосстановление** ("невосстановление")</span><span class="sxs-lookup"><span data-stu-id="626ae-270">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="626ae-271">**Нет контакта** ("нет контакта")</span><span class="sxs-lookup"><span data-stu-id="626ae-271">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="626ae-272">**Потеря** связи ("потеря связи")</span><span class="sxs-lookup"><span data-stu-id="626ae-272">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="626ae-273">**UserName**</span><span class="sxs-lookup"><span data-stu-id="626ae-273">**UserName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="626ae-274">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="626ae-274">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="626ae-275">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="626ae-275">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="626ae-276">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32API \| сетевые функции Windows \| [**внетжетусер**](/windows/win32/api/winnetwk/nf-winnetwk-wnetgetusera)")</span><span class="sxs-lookup"><span data-stu-id="626ae-276">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Windows Networking Functions\|[**WNetGetUser**](/windows/win32/api/winnetwk/nf-winnetwk-wnetgetusera)")</span></span>
</dt> </dl>

<span data-ttu-id="626ae-277">Имя пользователя или имя пользователя по умолчанию, используемые для установки сетевого подключения.</span><span class="sxs-lookup"><span data-stu-id="626ae-277">User name or the default user name used to establish a network connection.</span></span>

<span data-ttu-id="626ae-278">Пример: "SYSTEM"</span><span class="sxs-lookup"><span data-stu-id="626ae-278">Example: "SYSTEM"</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="626ae-279">Комментарии</span><span class="sxs-lookup"><span data-stu-id="626ae-279">Remarks</span></span>

<span data-ttu-id="626ae-280">Класс **Win32 \_ NetworkConnection** является производным от [**CIM \_ логикалелемент**](cim-logicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="626ae-280">The **Win32\_NetworkConnection** class is derived from [**CIM\_LogicalElement**](cim-logicalelement.md).</span></span>

## <a name="examples"></a><span data-ttu-id="626ae-281">Примеры</span><span class="sxs-lookup"><span data-stu-id="626ae-281">Examples</span></span>

<span data-ttu-id="626ae-282">Следующий пример кода VBScript извлекает сведения о локальном сетевом подключении.</span><span class="sxs-lookup"><span data-stu-id="626ae-282">The following VBScript code sample retrieves information on the local network connection.</span></span>


```VB
On Error Resume Next
strComputer = "."
Set objWMIService = GetObject("winmgmts:\\" & strComputer & "\Root\CIMv2")
Set colItems = objWMIService.ExecQuery("Select * from Win32_NetworkConnection",,48)
For Each objItem in colItems
    Wscript.Echo "AccessMask: " & objItem.AccessMask
    Wscript.Echo "Caption: " & objItem.Caption
    Wscript.Echo "Comment: " & objItem.Comment
    Wscript.Echo "ConnectionState: " & objItem.ConnectionState
    Wscript.Echo "ConnectionType: " & objItem.ConnectionType
    Wscript.Echo "Description: " & objItem.Description
    Wscript.Echo "DisplayType: " & objItem.DisplayType
    Wscript.Echo "InstallDate: " & objItem.InstallDate
    Wscript.Echo "LocalName: " & objItem.LocalName
    Wscript.Echo "Name: " & objItem.Name
    Wscript.Echo "Persistent: " & objItem.Persistent
    Wscript.Echo "ProviderName: " & objItem.ProviderName
    Wscript.Echo "RemoteName: " & objItem.RemoteName
    Wscript.Echo "RemotePath: " & objItem.RemotePath
    Wscript.Echo "ResourceType: " & objItem.ResourceType
    Wscript.Echo "Status: " & objItem.Status
    Wscript.Echo "UserName: " & objItem.UserName
Next
```



## <a name="requirements"></a><span data-ttu-id="626ae-283">Требования</span><span class="sxs-lookup"><span data-stu-id="626ae-283">Requirements</span></span>



| <span data-ttu-id="626ae-284">Требование</span><span class="sxs-lookup"><span data-stu-id="626ae-284">Requirement</span></span> | <span data-ttu-id="626ae-285">Значение</span><span class="sxs-lookup"><span data-stu-id="626ae-285">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="626ae-286">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="626ae-286">Minimum supported client</span></span><br/> | <span data-ttu-id="626ae-287">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="626ae-287">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="626ae-288">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="626ae-288">Minimum supported server</span></span><br/> | <span data-ttu-id="626ae-289">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="626ae-289">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="626ae-290">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="626ae-290">Namespace</span></span><br/>                | <span data-ttu-id="626ae-291">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="626ae-291">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="626ae-292">MOF</span><span class="sxs-lookup"><span data-stu-id="626ae-292">MOF</span></span><br/>                      | <dl> <span data-ttu-id="626ae-293"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="626ae-293"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="626ae-294">DLL</span><span class="sxs-lookup"><span data-stu-id="626ae-294">DLL</span></span><br/>                      | <dl> <span data-ttu-id="626ae-295"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="626ae-295"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="626ae-296">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="626ae-296">See also</span></span>

<dl> <dt>

[<span data-ttu-id="626ae-297">**\_ЛОГИКАЛЕЛЕМЕНТ CIM**</span><span class="sxs-lookup"><span data-stu-id="626ae-297">**CIM\_LogicalElement**</span></span>](cim-logicalelement.md)
</dt> <dt>

[<span data-ttu-id="626ae-298">Классы операционной системы</span><span class="sxs-lookup"><span data-stu-id="626ae-298">Operating System Classes</span></span>](./operating-system-classes.md)
</dt> </dl>

 

 
