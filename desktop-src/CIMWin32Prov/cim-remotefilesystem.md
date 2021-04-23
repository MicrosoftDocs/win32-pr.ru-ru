---
description: Класс CIM \_ ремотефилесистем представляет собой удаленную файловую систему, доступ к которой осуществляется посредством сетевой службы. В этом случае хранилище файлов размещается на компьютере, который выступает в качестве файлового сервера.
ms.assetid: 932970a8-0ab3-45d8-912d-c4ba7cf433b5
ms.tgt_platform: multiple
title: Класс CIM_RemoteFileSystem
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_RemoteFileSystem
- CIM_RemoteFileSystem.AvailableSpace
- CIM_RemoteFileSystem.BlockSize
- CIM_RemoteFileSystem.Caption
- CIM_RemoteFileSystem.CasePreserved
- CIM_RemoteFileSystem.CaseSensitive
- CIM_RemoteFileSystem.CodeSet
- CIM_RemoteFileSystem.CompressionMethod
- CIM_RemoteFileSystem.CreationClassName
- CIM_RemoteFileSystem.CSCreationClassName
- CIM_RemoteFileSystem.CSName
- CIM_RemoteFileSystem.Description
- CIM_RemoteFileSystem.EncryptionMethod
- CIM_RemoteFileSystem.FileSystemSize
- CIM_RemoteFileSystem.InstallDate
- CIM_RemoteFileSystem.MaxFileNameLength
- CIM_RemoteFileSystem.Name
- CIM_RemoteFileSystem.ReadOnly
- CIM_RemoteFileSystem.Root
- CIM_RemoteFileSystem.Status
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 7c29e0212ba55b37abd734fb149d118ccc693908
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104141075"
---
# <a name="cim_remotefilesystem-class"></a><span data-ttu-id="dfa61-104">\_Класс CIM ремотефилесистем</span><span class="sxs-lookup"><span data-stu-id="dfa61-104">CIM\_RemoteFileSystem class</span></span>

<span data-ttu-id="dfa61-105">Класс **CIM \_ ремотефилесистем** представляет собой удаленную файловую систему, доступ к которой осуществляется посредством сетевой службы.</span><span class="sxs-lookup"><span data-stu-id="dfa61-105">The **CIM\_RemoteFileSystem** class represents a remote file system that is accessed by way of a network-related service.</span></span> <span data-ttu-id="dfa61-106">В этом случае хранилище файлов размещается на компьютере, который выступает в качестве файлового сервера.</span><span class="sxs-lookup"><span data-stu-id="dfa61-106">In this case, the file store is hosted by a computer, which acts as a file server.</span></span> <span data-ttu-id="dfa61-107">Например, хранилище файлов для файловой системы NFS обычно не находится на локальном компьютере, управляемом компьютером, и не предоставляется напрямую через драйвер устройства.</span><span class="sxs-lookup"><span data-stu-id="dfa61-107">For example, the file store for an NFS file system is typically not on a computer system's locally controlled media, nor is it directly accessed through a device driver.</span></span> <span data-ttu-id="dfa61-108">Подклассы **CIM \_ ремотефилесистем** содержат сведения о конфигурации на стороне клиента, связанные с доступом к файловой системе.</span><span class="sxs-lookup"><span data-stu-id="dfa61-108">Subclasses of **CIM\_RemoteFileSystem** contain client-side configuration information related to the access of the file system.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="dfa61-109">Классы CIM (модель CIM) в DMTF (распределенная задача управления) являются родительскими классами, на которых строятся классы WMI.</span><span class="sxs-lookup"><span data-stu-id="dfa61-109">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="dfa61-110">В настоящее время WMI поддерживает только [схемы версии CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="dfa61-110">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="dfa61-111">Следующий синтаксис упрощен из кода MOF-файл (MOF) и включает все его унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="dfa61-111">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="dfa61-112">Свойства перечислены в алфавитном порядке, а не в MOF.</span><span class="sxs-lookup"><span data-stu-id="dfa61-112">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="dfa61-113">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="dfa61-113">Syntax</span></span>

``` syntax
[Abstract, UUID("{75BCF4F9-DB46-11D2-B4C8-80080C7B6371}"), AMENDMENT]
class CIM_RemoteFileSystem : CIM_FileSystem
{
  uint64   AvailableSpace;
  uint64   BlockSize;
  string   Caption;
  boolean  CasePreserved;
  boolean  CaseSensitive;
  uint16   CodeSet[];
  string   CompressionMethod;
  string   CreationClassName;
  string   CSCreationClassName;
  string   CSName;
  string   Description;
  string   EncryptionMethod;
  uint64   FileSystemSize;
  datetime InstallDate;
  uint32   MaxFileNameLength;
  string   Name;
  boolean  ReadOnly;
  string   Root;
  string   Status;
};
```

## <a name="members"></a><span data-ttu-id="dfa61-114">Члены</span><span class="sxs-lookup"><span data-stu-id="dfa61-114">Members</span></span>

<span data-ttu-id="dfa61-115">Класс **CIM \_ ремотефилесистем** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="dfa61-115">The **CIM\_RemoteFileSystem** class has these types of members:</span></span>

-   [<span data-ttu-id="dfa61-116">Свойства</span><span class="sxs-lookup"><span data-stu-id="dfa61-116">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="dfa61-117">Свойства</span><span class="sxs-lookup"><span data-stu-id="dfa61-117">Properties</span></span>

<span data-ttu-id="dfa61-118">Класс **CIM \_ ремотефилесистем** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="dfa61-118">The **CIM\_RemoteFileSystem** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="dfa61-119">**аваилаблеспаце**</span><span class="sxs-lookup"><span data-stu-id="dfa61-119">**AvailableSpace**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dfa61-120">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="dfa61-120">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="dfa61-121">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="dfa61-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dfa61-122">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. \|Раздел DMTF \| 002,4 "), [**единицы**](/windows/desktop/WmiSdk/standard-qualifiers) (" байт ")</span><span class="sxs-lookup"><span data-stu-id="dfa61-122">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Partition\|002.4"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="dfa61-123">Объем свободного места в байтах для файловой системы.</span><span class="sxs-lookup"><span data-stu-id="dfa61-123">Amount of free space for the file system, in bytes.</span></span> <span data-ttu-id="dfa61-124">Если значение неизвестно, введите 0.</span><span class="sxs-lookup"><span data-stu-id="dfa61-124">If unknown, enter 0.</span></span>

<span data-ttu-id="dfa61-125">Это свойство наследуется [**от \_ файловой системы CIM**](cim-filesystem.md).</span><span class="sxs-lookup"><span data-stu-id="dfa61-125">This property is inherited from [**CIM\_FileSystem**](cim-filesystem.md).</span></span>

<span data-ttu-id="dfa61-126">Дополнительные сведения об использовании значений **UInt64** в скриптах см. [в разделе Создание сценариев в WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="dfa61-126">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="dfa61-127">**BlockSize**</span><span class="sxs-lookup"><span data-stu-id="dfa61-127">**BlockSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dfa61-128">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="dfa61-128">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="dfa61-129">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="dfa61-129">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dfa61-130">Квалификаторы: [**единицы**](/windows/desktop/WmiSdk/standard-qualifiers) ("байт")</span><span class="sxs-lookup"><span data-stu-id="dfa61-130">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="dfa61-131">Размер (в байтах) блоков, образующих экстент хранения.</span><span class="sxs-lookup"><span data-stu-id="dfa61-131">Size, in bytes, of the blocks that form the storage extent.</span></span> <span data-ttu-id="dfa61-132">Если значение неизвестно или если концепция блока является недопустимой (например, для агрегатных экстентов, памяти или логических дисков), введите 1 (один).</span><span class="sxs-lookup"><span data-stu-id="dfa61-132">If unknown, or if a block concept is not valid, (for example, for aggregate extents, memory, or logical disks), enter a 1 (one).</span></span>

<span data-ttu-id="dfa61-133">Это свойство наследуется [**от \_ файловой системы CIM**](cim-filesystem.md).</span><span class="sxs-lookup"><span data-stu-id="dfa61-133">This property is inherited from [**CIM\_FileSystem**](cim-filesystem.md).</span></span>

<span data-ttu-id="dfa61-134">Дополнительные сведения об использовании значений **UInt64** в скриптах см. [в разделе Создание сценариев в WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="dfa61-134">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="dfa61-135">**Заголовок**</span><span class="sxs-lookup"><span data-stu-id="dfa61-135">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dfa61-136">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="dfa61-136">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dfa61-137">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="dfa61-137">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dfa61-138">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="dfa61-138">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="dfa61-139">Текстовое описание объекта.</span><span class="sxs-lookup"><span data-stu-id="dfa61-139">Textual description of the object.</span></span>

<span data-ttu-id="dfa61-140">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="dfa61-140">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="dfa61-141">**касепресервед**</span><span class="sxs-lookup"><span data-stu-id="dfa61-141">**CasePreserved**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dfa61-142">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="dfa61-142">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="dfa61-143">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="dfa61-143">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dfa61-144">Если **значение равно true**, регистр имен файлов сохраняется.</span><span class="sxs-lookup"><span data-stu-id="dfa61-144">If **TRUE**, the case of file names are preserved.</span></span>

<span data-ttu-id="dfa61-145">Это свойство наследуется [**от \_ файловой системы CIM**](cim-filesystem.md).</span><span class="sxs-lookup"><span data-stu-id="dfa61-145">This property is inherited from [**CIM\_FileSystem**](cim-filesystem.md).</span></span>

</dd> <dt>

<span data-ttu-id="dfa61-146">**CaseSensitive**</span><span class="sxs-lookup"><span data-stu-id="dfa61-146">**CaseSensitive**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dfa61-147">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="dfa61-147">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="dfa61-148">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="dfa61-148">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dfa61-149">**Значение true** показывает, что имена файлов с учетом регистра поддерживаются.</span><span class="sxs-lookup"><span data-stu-id="dfa61-149">If **TRUE**, case-sensitive file names are supported.</span></span>

<span data-ttu-id="dfa61-150">Это свойство наследуется [**от \_ файловой системы CIM**](cim-filesystem.md).</span><span class="sxs-lookup"><span data-stu-id="dfa61-150">This property is inherited from [**CIM\_FileSystem**](cim-filesystem.md).</span></span>

</dd> <dt>

<span data-ttu-id="dfa61-151">**Исходный код**</span><span class="sxs-lookup"><span data-stu-id="dfa61-151">**CodeSet**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dfa61-152">Тип данных: **UInt16** , массив</span><span class="sxs-lookup"><span data-stu-id="dfa61-152">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="dfa61-153">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="dfa61-153">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dfa61-154">Наборы символов или кодировка, поддерживаемые файловой системой.</span><span class="sxs-lookup"><span data-stu-id="dfa61-154">Character sets or encoding supported by the file system.</span></span> <span data-ttu-id="dfa61-155">Это свойство наследуется [**от \_ файловой системы CIM**](cim-filesystem.md).</span><span class="sxs-lookup"><span data-stu-id="dfa61-155">This property is inherited from [**CIM\_FileSystem**](cim-filesystem.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="dfa61-156">**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="dfa61-156">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="dfa61-157">**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="dfa61-157">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="ASCII"></span><span id="ascii"></span>

<span data-ttu-id="dfa61-158">**ASCII** (2)</span><span class="sxs-lookup"><span data-stu-id="dfa61-158">**ASCII** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Unicode"></span><span id="unicode"></span><span id="UNICODE"></span>

<span data-ttu-id="dfa61-159">**Юникод** (3)</span><span class="sxs-lookup"><span data-stu-id="dfa61-159">**Unicode** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="ISO2022"></span><span id="iso2022"></span>

<span data-ttu-id="dfa61-160">**ISO2022** (4)</span><span class="sxs-lookup"><span data-stu-id="dfa61-160">**ISO2022** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="ISO8859"></span><span id="iso8859"></span>

<span data-ttu-id="dfa61-161">**ISO8859** (5)</span><span class="sxs-lookup"><span data-stu-id="dfa61-161">**ISO8859** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Extended_UNIX_Code"></span><span id="extended_unix_code"></span><span id="EXTENDED_UNIX_CODE"></span>

<span data-ttu-id="dfa61-162">**Расширенный код UNIX** (6)</span><span class="sxs-lookup"><span data-stu-id="dfa61-162">**Extended UNIX Code** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="UTF-8"></span><span id="utf-8"></span>

<span data-ttu-id="dfa61-163">**UTF-8** (7)</span><span class="sxs-lookup"><span data-stu-id="dfa61-163">**UTF-8** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="UCS-2"></span><span id="ucs-2"></span>

<span data-ttu-id="dfa61-164">**UCS-2** (8)</span><span class="sxs-lookup"><span data-stu-id="dfa61-164">**UCS-2** (8)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="dfa61-165">**компрессионмесод**</span><span class="sxs-lookup"><span data-stu-id="dfa61-165">**CompressionMethod**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dfa61-166">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="dfa61-166">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dfa61-167">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="dfa61-167">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dfa61-168">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. DMTF \| \| -раздел 002,7 ")</span><span class="sxs-lookup"><span data-stu-id="dfa61-168">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Partition\|002.7")</span></span>
</dt> </dl>

<span data-ttu-id="dfa61-169">Произвольная строка, указывающая алгоритм или инструмент, используемый для сжатия логического файла.</span><span class="sxs-lookup"><span data-stu-id="dfa61-169">Free-form string that indicates the algorithm or tool used to compress the logical file.</span></span> <span data-ttu-id="dfa61-170">Если схема сжатия неизвестна или не описана, используйте "Unknown".</span><span class="sxs-lookup"><span data-stu-id="dfa61-170">If the compression scheme is unknown or not described, use "Unknown".</span></span> <span data-ttu-id="dfa61-171">Если логический файл сжат, но схема сжатия неизвестна или не описана, используйте "сжатый".</span><span class="sxs-lookup"><span data-stu-id="dfa61-171">If the logical file is compressed, but the compression scheme is unknown or not described, use "Compressed".</span></span> <span data-ttu-id="dfa61-172">Если логический файл не сжат, используйте параметр NOT сжатый.</span><span class="sxs-lookup"><span data-stu-id="dfa61-172">If the logical file is not compressed, use "Not Compressed".</span></span>

<span data-ttu-id="dfa61-173">Это свойство наследуется [**от \_ файловой системы CIM**](cim-filesystem.md).</span><span class="sxs-lookup"><span data-stu-id="dfa61-173">This property is inherited from [**CIM\_FileSystem**](cim-filesystem.md).</span></span>

</dd> <dt>

<span data-ttu-id="dfa61-174">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="dfa61-174">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dfa61-175">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="dfa61-175">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dfa61-176">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="dfa61-176">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dfa61-177">Квалификаторы: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="dfa61-177">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="dfa61-178">Имя класса или подкласса, используемого при создании экземпляра.</span><span class="sxs-lookup"><span data-stu-id="dfa61-178">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="dfa61-179">При использовании с другими ключевыми свойствами класса это свойство позволяет однозначно идентифицировать все экземпляры класса и его подклассов.</span><span class="sxs-lookup"><span data-stu-id="dfa61-179">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="dfa61-180">Это свойство наследуется [**от \_ файловой системы CIM**](cim-filesystem.md).</span><span class="sxs-lookup"><span data-stu-id="dfa61-180">This property is inherited from [**CIM\_FileSystem**](cim-filesystem.md).</span></span>

</dd> <dt>

<span data-ttu-id="dfa61-181">**кскреатионкласснаме**</span><span class="sxs-lookup"><span data-stu-id="dfa61-181">**CSCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dfa61-182">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="dfa61-182">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dfa61-183">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="dfa61-183">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dfa61-184">Квалификаторы: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**распространяются**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ ComputerSystem**](cim-computersystem.md).**CreationClassName**")</span><span class="sxs-lookup"><span data-stu-id="dfa61-184">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_ComputerSystem**](cim-computersystem.md).**CreationClassName**")</span></span>
</dt> </dl>

<span data-ttu-id="dfa61-185">Определение области имени класса создания системы компьютера.</span><span class="sxs-lookup"><span data-stu-id="dfa61-185">Scoping computer system's creation class name.</span></span>

<span data-ttu-id="dfa61-186">Это свойство наследуется [**от \_ файловой системы CIM**](cim-filesystem.md).</span><span class="sxs-lookup"><span data-stu-id="dfa61-186">This property is inherited from [**CIM\_FileSystem**](cim-filesystem.md).</span></span>

</dd> <dt>

<span data-ttu-id="dfa61-187">**CSName**</span><span class="sxs-lookup"><span data-stu-id="dfa61-187">**CSName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dfa61-188">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="dfa61-188">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dfa61-189">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="dfa61-189">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dfa61-190">Квалификаторы: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**распространяются**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ ComputerSystem**](cim-computersystem.md).**Name**")</span><span class="sxs-lookup"><span data-stu-id="dfa61-190">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_ComputerSystem**](cim-computersystem.md).**Name**")</span></span>
</dt> </dl>

<span data-ttu-id="dfa61-191">Определение области имени системы компьютера.</span><span class="sxs-lookup"><span data-stu-id="dfa61-191">Scoping computer system's name.</span></span>

<span data-ttu-id="dfa61-192">Это свойство наследуется [**от \_ файловой системы CIM**](cim-filesystem.md).</span><span class="sxs-lookup"><span data-stu-id="dfa61-192">This property is inherited from [**CIM\_FileSystem**](cim-filesystem.md).</span></span>

</dd> <dt>

<span data-ttu-id="dfa61-193">**Описание**</span><span class="sxs-lookup"><span data-stu-id="dfa61-193">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dfa61-194">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="dfa61-194">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dfa61-195">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="dfa61-195">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dfa61-196">Квалификаторы: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Описание")</span><span class="sxs-lookup"><span data-stu-id="dfa61-196">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="dfa61-197">Текстовое описание объекта.</span><span class="sxs-lookup"><span data-stu-id="dfa61-197">Textual description of the object.</span></span>

<span data-ttu-id="dfa61-198">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="dfa61-198">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="dfa61-199">**EncryptionMethod**</span><span class="sxs-lookup"><span data-stu-id="dfa61-199">**EncryptionMethod**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dfa61-200">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="dfa61-200">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dfa61-201">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="dfa61-201">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dfa61-202">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. DMTF \| \| -раздел 002,8 ")</span><span class="sxs-lookup"><span data-stu-id="dfa61-202">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Partition\|002.8")</span></span>
</dt> </dl>

<span data-ttu-id="dfa61-203">Произвольная строка, идентифицирующая алгоритм или средство, используемые для шифрования логического файла.</span><span class="sxs-lookup"><span data-stu-id="dfa61-203">Free-form string that identifies the algorithm or tool used to encrypt a logical file.</span></span> <span data-ttu-id="dfa61-204">Если схема шифрования не индулжед (например, из соображений безопасности), используйте "Unknown".</span><span class="sxs-lookup"><span data-stu-id="dfa61-204">If the encryption scheme is not indulged (for security reasons, for example), use "Unknown".</span></span> <span data-ttu-id="dfa61-205">Если файл зашифрован, но либо его схема шифрования неизвестна, либо не раскрывается, используйте "encrypted".</span><span class="sxs-lookup"><span data-stu-id="dfa61-205">If the file is encrypted, but either its encryption scheme is unknown or not disclosed, use "Encrypted".</span></span> <span data-ttu-id="dfa61-206">Если логический файл не зашифрован, используйте параметр NOT encrypted.</span><span class="sxs-lookup"><span data-stu-id="dfa61-206">If the logical file is not encrypted, use "Not Encrypted".</span></span> <span data-ttu-id="dfa61-207">Это свойство наследуется [**от \_ файловой системы CIM**](cim-filesystem.md).</span><span class="sxs-lookup"><span data-stu-id="dfa61-207">This property is inherited from [**CIM\_FileSystem**](cim-filesystem.md).</span></span>

</dd> <dt>

<span data-ttu-id="dfa61-208">**филесистемсизе**</span><span class="sxs-lookup"><span data-stu-id="dfa61-208">**FileSystemSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dfa61-209">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="dfa61-209">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="dfa61-210">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="dfa61-210">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dfa61-211">Квалификаторы: [**единицы**](/windows/desktop/WmiSdk/standard-qualifiers) ("байт")</span><span class="sxs-lookup"><span data-stu-id="dfa61-211">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="dfa61-212">Общий размер файловой системы в байтах.</span><span class="sxs-lookup"><span data-stu-id="dfa61-212">Total size of the file system, in bytes.</span></span> <span data-ttu-id="dfa61-213">Если значение неизвестно, введите 0.</span><span class="sxs-lookup"><span data-stu-id="dfa61-213">If unknown, enter 0.</span></span>

<span data-ttu-id="dfa61-214">Это свойство наследуется [**от \_ файловой системы CIM**](cim-filesystem.md).</span><span class="sxs-lookup"><span data-stu-id="dfa61-214">This property is inherited from [**CIM\_FileSystem**](cim-filesystem.md).</span></span>

<span data-ttu-id="dfa61-215">Дополнительные сведения об использовании значений **UInt64** в скриптах см. [в разделе Создание сценариев в WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="dfa61-215">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="dfa61-216">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="dfa61-216">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dfa61-217">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="dfa61-217">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="dfa61-218">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="dfa61-218">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dfa61-219">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" Дата установки ")</span><span class="sxs-lookup"><span data-stu-id="dfa61-219">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="dfa61-220">Дата и время установки объекта.</span><span class="sxs-lookup"><span data-stu-id="dfa61-220">Date and time the object was installed.</span></span> <span data-ttu-id="dfa61-221">Для этого свойства не требуется значение, указывающее, что объект установлен.</span><span class="sxs-lookup"><span data-stu-id="dfa61-221">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="dfa61-222">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="dfa61-222">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="dfa61-223">**максфиленамеленгс**</span><span class="sxs-lookup"><span data-stu-id="dfa61-223">**MaxFileNameLength**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dfa61-224">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="dfa61-224">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="dfa61-225">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="dfa61-225">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dfa61-226">Максимальная длина имени файла в файловой системе.</span><span class="sxs-lookup"><span data-stu-id="dfa61-226">Maximum length of a file name within the file system.</span></span> <span data-ttu-id="dfa61-227">Значение 0 указывает, что длина имени файла не ограничена.</span><span class="sxs-lookup"><span data-stu-id="dfa61-227">A value of 0 indicates that file name length is unlimited.</span></span>

<span data-ttu-id="dfa61-228">Это свойство наследуется [**от \_ файловой системы CIM**](cim-filesystem.md).</span><span class="sxs-lookup"><span data-stu-id="dfa61-228">This property is inherited from [**CIM\_FileSystem**](cim-filesystem.md).</span></span>

</dd> <dt>

<span data-ttu-id="dfa61-229">**Name**</span><span class="sxs-lookup"><span data-stu-id="dfa61-229">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dfa61-230">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="dfa61-230">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dfa61-231">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="dfa61-231">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dfa61-232">Квалификаторы: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("имя")</span><span class="sxs-lookup"><span data-stu-id="dfa61-232">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="dfa61-233">Метка, по которой известен объект.</span><span class="sxs-lookup"><span data-stu-id="dfa61-233">Label by which the object is known.</span></span> <span data-ttu-id="dfa61-234">При создании подклассов это свойство может быть переопределено как свойство ключа.</span><span class="sxs-lookup"><span data-stu-id="dfa61-234">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="dfa61-235">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="dfa61-235">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="dfa61-236">**ReadOnly**</span><span class="sxs-lookup"><span data-stu-id="dfa61-236">**ReadOnly**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dfa61-237">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="dfa61-237">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="dfa61-238">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="dfa61-238">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dfa61-239">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB. \|Основной узел IETF-Resources-MIB. хрфсакцесс ")</span><span class="sxs-lookup"><span data-stu-id="dfa61-239">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB.IETF\|HOST-RESOURCES-MIB.hrFSAccess")</span></span>
</dt> </dl>

<span data-ttu-id="dfa61-240">Если **значение — true**, файловая система предназначена только для чтения.</span><span class="sxs-lookup"><span data-stu-id="dfa61-240">If **TRUE**, the file system is designated as read-only.</span></span>

<span data-ttu-id="dfa61-241">Это свойство наследуется [**от \_ файловой системы CIM**](cim-filesystem.md).</span><span class="sxs-lookup"><span data-stu-id="dfa61-241">This property is inherited from [**CIM\_FileSystem**](cim-filesystem.md).</span></span>

</dd> <dt>

<span data-ttu-id="dfa61-242">**Корневой**</span><span class="sxs-lookup"><span data-stu-id="dfa61-242">**Root**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dfa61-243">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="dfa61-243">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dfa61-244">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="dfa61-244">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dfa61-245">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB. \|Основной узел IETF-Resources-MIB. хрфсмаунтпоинт ")</span><span class="sxs-lookup"><span data-stu-id="dfa61-245">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB.IETF\|HOST-RESOURCES-MIB.hrFSMountPoint")</span></span>
</dt> </dl>

<span data-ttu-id="dfa61-246">Имя пути или другие сведения, определяющие корень файловой системы.</span><span class="sxs-lookup"><span data-stu-id="dfa61-246">Path name or other information that defines the root of the file system.</span></span>

<span data-ttu-id="dfa61-247">Это свойство наследуется [**от \_ файловой системы CIM**](cim-filesystem.md).</span><span class="sxs-lookup"><span data-stu-id="dfa61-247">This property is inherited from [**CIM\_FileSystem**](cim-filesystem.md).</span></span>

</dd> <dt>

<span data-ttu-id="dfa61-248">**Состояние**</span><span class="sxs-lookup"><span data-stu-id="dfa61-248">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dfa61-249">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="dfa61-249">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dfa61-250">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="dfa61-250">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dfa61-251">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("состояние")</span><span class="sxs-lookup"><span data-stu-id="dfa61-251">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="dfa61-252">Текущее состояние объекта.</span><span class="sxs-lookup"><span data-stu-id="dfa61-252">Current status of the object.</span></span>

<span data-ttu-id="dfa61-253">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="dfa61-253">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="dfa61-254">В эти значения входят:</span><span class="sxs-lookup"><span data-stu-id="dfa61-254">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="dfa61-255">**ОК** ("ОК")</span><span class="sxs-lookup"><span data-stu-id="dfa61-255">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="dfa61-256">**Ошибка** ("ошибка")</span><span class="sxs-lookup"><span data-stu-id="dfa61-256">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="dfa61-257">**Пониженная работоспособность** (пониженная работоспособность)</span><span class="sxs-lookup"><span data-stu-id="dfa61-257">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="dfa61-258">**Неизвестно** ("неизвестно")</span><span class="sxs-lookup"><span data-stu-id="dfa61-258">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="dfa61-259">**Пред-ошибка** ("пред Fail")</span><span class="sxs-lookup"><span data-stu-id="dfa61-259">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="dfa61-260">**Запуск** ("Запуск")</span><span class="sxs-lookup"><span data-stu-id="dfa61-260">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="dfa61-261">**Остановка** ("остановка")</span><span class="sxs-lookup"><span data-stu-id="dfa61-261">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="dfa61-262">**Служба** ("служба")</span><span class="sxs-lookup"><span data-stu-id="dfa61-262">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="dfa61-263">**Пренапряжению** ("напряжению")</span><span class="sxs-lookup"><span data-stu-id="dfa61-263">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="dfa61-264">**Невосстановление** ("невосстановление")</span><span class="sxs-lookup"><span data-stu-id="dfa61-264">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="dfa61-265">**Нет контакта** ("нет контакта")</span><span class="sxs-lookup"><span data-stu-id="dfa61-265">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="dfa61-266">**Потеря** связи ("потеря связи")</span><span class="sxs-lookup"><span data-stu-id="dfa61-266">**Lost Comm** ("Lost Comm")</span></span>


<span data-ttu-id="dfa61-267"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="dfa61-267"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="remarks"></a><span data-ttu-id="dfa61-268">Комментарии</span><span class="sxs-lookup"><span data-stu-id="dfa61-268">Remarks</span></span>

<span data-ttu-id="dfa61-269">Класс **CIM \_ ремотефилесистем** является производным от [**\_ файловой системы CIM**](cim-filesystem.md).</span><span class="sxs-lookup"><span data-stu-id="dfa61-269">The **CIM\_RemoteFileSystem** class is derived from [**CIM\_FileSystem**](cim-filesystem.md).</span></span>

<span data-ttu-id="dfa61-270">Инструментарий WMI не реализует этот класс.</span><span class="sxs-lookup"><span data-stu-id="dfa61-270">WMI does not implement this class.</span></span>

<span data-ttu-id="dfa61-271">Эта документация является производной от описаний класса CIM, опубликованных в формате DMTF.</span><span class="sxs-lookup"><span data-stu-id="dfa61-271">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="dfa61-272">Корпорация Майкрософт могла внести изменения в Исправление незначительных ошибок, соответствовать стандартам документации пакета Microsoft SDK или предоставить дополнительные сведения.</span><span class="sxs-lookup"><span data-stu-id="dfa61-272">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="dfa61-273">Требования</span><span class="sxs-lookup"><span data-stu-id="dfa61-273">Requirements</span></span>



| <span data-ttu-id="dfa61-274">Требование</span><span class="sxs-lookup"><span data-stu-id="dfa61-274">Requirement</span></span> | <span data-ttu-id="dfa61-275">Значение</span><span class="sxs-lookup"><span data-stu-id="dfa61-275">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="dfa61-276">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="dfa61-276">Minimum supported client</span></span><br/> | <span data-ttu-id="dfa61-277">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="dfa61-277">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="dfa61-278">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="dfa61-278">Minimum supported server</span></span><br/> | <span data-ttu-id="dfa61-279">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="dfa61-279">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="dfa61-280">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="dfa61-280">Namespace</span></span><br/>                | <span data-ttu-id="dfa61-281">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="dfa61-281">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="dfa61-282">MOF</span><span class="sxs-lookup"><span data-stu-id="dfa61-282">MOF</span></span><br/>                      | <dl> <span data-ttu-id="dfa61-283"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="dfa61-283"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="dfa61-284">DLL</span><span class="sxs-lookup"><span data-stu-id="dfa61-284">DLL</span></span><br/>                      | <dl> <span data-ttu-id="dfa61-285"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="dfa61-285"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dfa61-286">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="dfa61-286">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dfa61-287">**\_Файловая система CIM**</span><span class="sxs-lookup"><span data-stu-id="dfa61-287">**CIM\_FileSystem**</span></span>](cim-filesystem.md)
</dt> </dl>

 

