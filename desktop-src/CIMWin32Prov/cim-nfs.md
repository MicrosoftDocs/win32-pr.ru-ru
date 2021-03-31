---
description: '\_Класс NFS CIM представляет удаленную файловую систему, подключенную с помощью протокола NFS, из компьютерной системы.'
ms.assetid: 24eba28f-fbd5-4aa3-a7c7-a611269d55ac
ms.tgt_platform: multiple
title: Класс CIM_NFS
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_NFS
- CIM_NFS.AttributeCaching
- CIM_NFS.AttributeCachingForDirectoriesMax
- CIM_NFS.AttributeCachingForDirectoriesMin
- CIM_NFS.AttributeCachingForRegularFilesMax
- CIM_NFS.AttributeCachingForRegularFilesMin
- CIM_NFS.AvailableSpace
- CIM_NFS.BlockSize
- CIM_NFS.Caption
- CIM_NFS.CasePreserved
- CIM_NFS.CaseSensitive
- CIM_NFS.CodeSet
- CIM_NFS.CompressionMethod
- CIM_NFS.CreationClassName
- CIM_NFS.CSCreationClassName
- CIM_NFS.CSName
- CIM_NFS.Description
- CIM_NFS.EncryptionMethod
- CIM_NFS.FileSystemSize
- CIM_NFS.ForegroundMount
- CIM_NFS.HardMount
- CIM_NFS.InstallDate
- CIM_NFS.Interrupt
- CIM_NFS.MaxFileNameLength
- CIM_NFS.MountFailureRetries
- CIM_NFS.Name
- CIM_NFS.ReadBufferSize
- CIM_NFS.ReadOnly
- CIM_NFS.RetransmissionAttempts
- CIM_NFS.RetransmissionTimeout
- CIM_NFS.Root
- CIM_NFS.ServerCommunicationPort
- CIM_NFS.Status
- CIM_NFS.WriteBufferSize
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: f0dcfb44fdcd035ca47cbe3056da2a081ef2ae07
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103807589"
---
# <a name="cim_nfs-class"></a><span data-ttu-id="73c11-103">CIM, \_ класс NFS</span><span class="sxs-lookup"><span data-stu-id="73c11-103">CIM\_NFS class</span></span>

<span data-ttu-id="73c11-104">Класс **\_ NFS CIM** представляет удаленную файловую систему, подключенную с помощью протокола NFS, из компьютерной системы.</span><span class="sxs-lookup"><span data-stu-id="73c11-104">The **CIM\_NFS** class represents a remote file system that is mounted, using the network file system (NFS) protocol, from a computer system.</span></span> <span data-ttu-id="73c11-105">Свойства объекта NFS соответствуют рабочим аспектам подключения и представляют конфигурацию на стороне клиента для доступа NFS.</span><span class="sxs-lookup"><span data-stu-id="73c11-105">The properties of the NFS object correspond to the operational aspects of the mount and represent the client-side configuration for NFS access.</span></span> <span data-ttu-id="73c11-106">Необходимо задать тип файловой системы, чтобы указать тип файловой системы, отображаемой клиенту.</span><span class="sxs-lookup"><span data-stu-id="73c11-106">The file system type should be set to indicate the type of file system as it appears to the client.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="73c11-107">Классы CIM (модель CIM) в DMTF (распределенная задача управления) являются родительскими классами, на которых строятся классы WMI.</span><span class="sxs-lookup"><span data-stu-id="73c11-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="73c11-108">В настоящее время WMI поддерживает только [схемы версии CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="73c11-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="73c11-109">Приведенный ниже синтаксис является упрощенной версией кода MOF и включает все унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="73c11-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="73c11-110">Свойства перечислены в алфавитном порядке, а не в MOF.</span><span class="sxs-lookup"><span data-stu-id="73c11-110">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="73c11-111">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="73c11-111">Syntax</span></span>

``` syntax
[Abstract, UUID("{75BCF4FB-DB46-11D2-B4C8-80080C7B6371}"), AMENDMENT]
class CIM_NFS : CIM_RemoteFileSystem
{
  boolean  AttributeCaching;
  uint16   AttributeCachingForDirectoriesMax;
  uint16   AttributeCachingForDirectoriesMin;
  uint16   AttributeCachingForRegularFilesMax;
  uint16   AttributeCachingForRegularFilesMin;
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
  boolean  ForegroundMount;
  boolean  HardMount;
  datetime InstallDate;
  boolean  Interrupt;
  uint32   MaxFileNameLength;
  uint16   MountFailureRetries;
  string   Name;
  uint64   ReadBufferSize;
  boolean  ReadOnly;
  uint16   RetransmissionAttempts;
  uint32   RetransmissionTimeout;
  string   Root;
  uint32   ServerCommunicationPort;
  string   Status;
  uint64   WriteBufferSize;
};
```

## <a name="members"></a><span data-ttu-id="73c11-112">Члены</span><span class="sxs-lookup"><span data-stu-id="73c11-112">Members</span></span>

<span data-ttu-id="73c11-113">Класс **\_ NFS CIM** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="73c11-113">The **CIM\_NFS** class has these types of members:</span></span>

-   [<span data-ttu-id="73c11-114">Свойства</span><span class="sxs-lookup"><span data-stu-id="73c11-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="73c11-115">Свойства</span><span class="sxs-lookup"><span data-stu-id="73c11-115">Properties</span></span>

<span data-ttu-id="73c11-116">Класс **CIM \_ NFS** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="73c11-116">The **CIM\_NFS** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="73c11-117">**аттрибутекачинг**</span><span class="sxs-lookup"><span data-stu-id="73c11-117">**AttributeCaching**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="73c11-118">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="73c11-118">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="73c11-119">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="73c11-119">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="73c11-120">Если **значение — true**, кэширование атрибутов управления включено.</span><span class="sxs-lookup"><span data-stu-id="73c11-120">If **TRUE**, control attribute caching is enabled.</span></span> <span data-ttu-id="73c11-121">Если задано **значение false**, кэширование атрибутов элемента управления отключено.</span><span class="sxs-lookup"><span data-stu-id="73c11-121">If **FALSE**, control attribute caching is disabled.</span></span>

</dd> <dt>

<span data-ttu-id="73c11-122">**аттрибутекачингфордиректориесмакс**</span><span class="sxs-lookup"><span data-stu-id="73c11-122">**AttributeCachingForDirectoriesMax**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="73c11-123">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="73c11-123">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="73c11-124">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="73c11-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="73c11-125">Квалификаторы: [**единицы**](/windows/desktop/WmiSdk/standard-qualifiers) ("секунды")</span><span class="sxs-lookup"><span data-stu-id="73c11-125">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("seconds")</span></span>
</dt> </dl>

<span data-ttu-id="73c11-126">Максимальное количество секунд, в течение которых кэшированные атрибуты удерживаются после обновления каталога.</span><span class="sxs-lookup"><span data-stu-id="73c11-126">Maximum number of seconds that cached attributes are held after directory update.</span></span>

</dd> <dt>

<span data-ttu-id="73c11-127">**аттрибутекачингфордиректориесмин**</span><span class="sxs-lookup"><span data-stu-id="73c11-127">**AttributeCachingForDirectoriesMin**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="73c11-128">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="73c11-128">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="73c11-129">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="73c11-129">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="73c11-130">Квалификаторы: [**единицы**](/windows/desktop/WmiSdk/standard-qualifiers) ("секунды")</span><span class="sxs-lookup"><span data-stu-id="73c11-130">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("seconds")</span></span>
</dt> </dl>

<span data-ttu-id="73c11-131">Минимальное количество секунд, в течение которых кэшированные атрибуты удерживаются после обновления каталога.</span><span class="sxs-lookup"><span data-stu-id="73c11-131">Minimum number of seconds that cached attributes are held after directory update.</span></span>

</dd> <dt>

<span data-ttu-id="73c11-132">**аттрибутекачингфоррегуларфилесмакс**</span><span class="sxs-lookup"><span data-stu-id="73c11-132">**AttributeCachingForRegularFilesMax**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="73c11-133">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="73c11-133">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="73c11-134">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="73c11-134">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="73c11-135">Квалификаторы: [**единицы**](/windows/desktop/WmiSdk/standard-qualifiers) ("секунды")</span><span class="sxs-lookup"><span data-stu-id="73c11-135">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("seconds")</span></span>
</dt> </dl>

<span data-ttu-id="73c11-136">Максимальное количество секунд, в течение которых кэшированные атрибуты удерживаются после изменения файла.</span><span class="sxs-lookup"><span data-stu-id="73c11-136">Maximum number of seconds that cached attributes are held after file modification.</span></span>

</dd> <dt>

<span data-ttu-id="73c11-137">**аттрибутекачингфоррегуларфилесмин**</span><span class="sxs-lookup"><span data-stu-id="73c11-137">**AttributeCachingForRegularFilesMin**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="73c11-138">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="73c11-138">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="73c11-139">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="73c11-139">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="73c11-140">Квалификаторы: [**единицы**](/windows/desktop/WmiSdk/standard-qualifiers) ("секунды")</span><span class="sxs-lookup"><span data-stu-id="73c11-140">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("seconds")</span></span>
</dt> </dl>

<span data-ttu-id="73c11-141">Минимальное количество секунд, в течение которых кэшированные атрибуты удерживаются после изменения файла.</span><span class="sxs-lookup"><span data-stu-id="73c11-141">Minimum number of seconds that cached attributes are held after file modification.</span></span>

</dd> <dt>

<span data-ttu-id="73c11-142">**аваилаблеспаце**</span><span class="sxs-lookup"><span data-stu-id="73c11-142">**AvailableSpace**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="73c11-143">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="73c11-143">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="73c11-144">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="73c11-144">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="73c11-145">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. \|Раздел DMTF \| 002,4 "), [**единицы**](/windows/desktop/WmiSdk/standard-qualifiers) (" байт ")</span><span class="sxs-lookup"><span data-stu-id="73c11-145">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Partition\|002.4"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="73c11-146">Общий объем свободного пространства в байтах для файловой системы.</span><span class="sxs-lookup"><span data-stu-id="73c11-146">Total amount of free space, in bytes, for the file system.</span></span> <span data-ttu-id="73c11-147">Если значение неизвестно, введите 0.</span><span class="sxs-lookup"><span data-stu-id="73c11-147">If unknown, enter 0.</span></span>

<span data-ttu-id="73c11-148">Это свойство наследуется [**от \_ файловой системы CIM**](cim-filesystem.md).</span><span class="sxs-lookup"><span data-stu-id="73c11-148">This property is inherited from [**CIM\_FileSystem**](cim-filesystem.md).</span></span>

<span data-ttu-id="73c11-149">Дополнительные сведения об использовании значений **UInt64** в скриптах см. [в разделе Создание сценариев в WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="73c11-149">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="73c11-150">**BlockSize**</span><span class="sxs-lookup"><span data-stu-id="73c11-150">**BlockSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="73c11-151">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="73c11-151">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="73c11-152">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="73c11-152">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="73c11-153">Квалификаторы: [**единицы**](/windows/desktop/WmiSdk/standard-qualifiers) ("байт")</span><span class="sxs-lookup"><span data-stu-id="73c11-153">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="73c11-154">Файловые системы могут считывать или записывать данные в блоках, которые определены независимо от базовых экстентов хранения.</span><span class="sxs-lookup"><span data-stu-id="73c11-154">File systems can read or write data in blocks that are defined independently of the underlying storage extents.</span></span> <span data-ttu-id="73c11-155">Это свойство захватывает размер блока файловой системы для хранения и извлечения данных.</span><span class="sxs-lookup"><span data-stu-id="73c11-155">This property captures the file system's block size for data storage and retrieval.</span></span>

<span data-ttu-id="73c11-156">Это свойство наследуется [**от \_ файловой системы CIM**](cim-filesystem.md).</span><span class="sxs-lookup"><span data-stu-id="73c11-156">This property is inherited from [**CIM\_FileSystem**](cim-filesystem.md).</span></span>

<span data-ttu-id="73c11-157">Дополнительные сведения об использовании значений **UInt64** в скриптах см. [в разделе Создание сценариев в WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="73c11-157">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="73c11-158">**Заголовок**</span><span class="sxs-lookup"><span data-stu-id="73c11-158">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="73c11-159">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="73c11-159">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="73c11-160">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="73c11-160">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="73c11-161">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="73c11-161">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="73c11-162">Краткое текстовое описание объекта.</span><span class="sxs-lookup"><span data-stu-id="73c11-162">Short textual description of the object.</span></span>

<span data-ttu-id="73c11-163">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="73c11-163">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="73c11-164">**касепресервед**</span><span class="sxs-lookup"><span data-stu-id="73c11-164">**CasePreserved**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="73c11-165">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="73c11-165">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="73c11-166">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="73c11-166">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="73c11-167">Если **значение равно true**, регистр имен файлов сохраняется.</span><span class="sxs-lookup"><span data-stu-id="73c11-167">If **TRUE**, the case of file names are preserved.</span></span>

<span data-ttu-id="73c11-168">Это свойство наследуется [**от \_ файловой системы CIM**](cim-filesystem.md).</span><span class="sxs-lookup"><span data-stu-id="73c11-168">This property is inherited from [**CIM\_FileSystem**](cim-filesystem.md).</span></span>

</dd> <dt>

<span data-ttu-id="73c11-169">**CaseSensitive**</span><span class="sxs-lookup"><span data-stu-id="73c11-169">**CaseSensitive**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="73c11-170">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="73c11-170">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="73c11-171">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="73c11-171">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="73c11-172">**Значение true** показывает, что имена файлов с учетом регистра поддерживаются.</span><span class="sxs-lookup"><span data-stu-id="73c11-172">If **TRUE**, case-sensitive file names are supported.</span></span>

<span data-ttu-id="73c11-173">Это свойство наследуется [**от \_ файловой системы CIM**](cim-filesystem.md).</span><span class="sxs-lookup"><span data-stu-id="73c11-173">This property is inherited from [**CIM\_FileSystem**](cim-filesystem.md).</span></span>

</dd> <dt>

<span data-ttu-id="73c11-174">**Исходный код**</span><span class="sxs-lookup"><span data-stu-id="73c11-174">**CodeSet**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="73c11-175">Тип данных: **UInt16** , массив</span><span class="sxs-lookup"><span data-stu-id="73c11-175">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="73c11-176">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="73c11-176">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="73c11-177">Наборы символов или кодировка, поддерживаемые файловой системой.</span><span class="sxs-lookup"><span data-stu-id="73c11-177">Character sets or encoding supported by the file system.</span></span>

<span data-ttu-id="73c11-178">Это свойство наследуется [**от \_ файловой системы CIM**](cim-filesystem.md).</span><span class="sxs-lookup"><span data-stu-id="73c11-178">This property is inherited from [**CIM\_FileSystem**](cim-filesystem.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="73c11-179">**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="73c11-179">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="73c11-180">**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="73c11-180">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="ASCII"></span><span id="ascii"></span>

<span data-ttu-id="73c11-181">**ASCII** (2)</span><span class="sxs-lookup"><span data-stu-id="73c11-181">**ASCII** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Unicode"></span><span id="unicode"></span><span id="UNICODE"></span>

<span data-ttu-id="73c11-182">**Юникод** (3)</span><span class="sxs-lookup"><span data-stu-id="73c11-182">**Unicode** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="ISO2022"></span><span id="iso2022"></span>

<span data-ttu-id="73c11-183">**ISO2022** (4)</span><span class="sxs-lookup"><span data-stu-id="73c11-183">**ISO2022** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="ISO8859"></span><span id="iso8859"></span>

<span data-ttu-id="73c11-184">**ISO8859** (5)</span><span class="sxs-lookup"><span data-stu-id="73c11-184">**ISO8859** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Extended_UNIX_Code"></span><span id="extended_unix_code"></span><span id="EXTENDED_UNIX_CODE"></span>

<span data-ttu-id="73c11-185">**Расширенный код UNIX** (6)</span><span class="sxs-lookup"><span data-stu-id="73c11-185">**Extended UNIX Code** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="UTF-8"></span><span id="utf-8"></span>

<span data-ttu-id="73c11-186">**UTF-8** (7)</span><span class="sxs-lookup"><span data-stu-id="73c11-186">**UTF-8** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="UCS-2"></span><span id="ucs-2"></span>

<span data-ttu-id="73c11-187">**UCS-2** (8)</span><span class="sxs-lookup"><span data-stu-id="73c11-187">**UCS-2** (8)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="73c11-188">**компрессионмесод**</span><span class="sxs-lookup"><span data-stu-id="73c11-188">**CompressionMethod**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="73c11-189">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="73c11-189">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="73c11-190">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="73c11-190">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="73c11-191">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. DMTF \| \| -раздел 002,7 ")</span><span class="sxs-lookup"><span data-stu-id="73c11-191">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Partition\|002.7")</span></span>
</dt> </dl>

<span data-ttu-id="73c11-192">Произвольная строка, указывающая алгоритм или инструмент, используемый для сжатия логического файла.</span><span class="sxs-lookup"><span data-stu-id="73c11-192">Free-form string that indicates the algorithm or tool used to compress the logical file.</span></span> <span data-ttu-id="73c11-193">Если схема сжатия неизвестна или не описана, используйте "Unknown".</span><span class="sxs-lookup"><span data-stu-id="73c11-193">If the compression scheme is unknown or not described, use "Unknown".</span></span> <span data-ttu-id="73c11-194">Если логический файл сжат, но схема сжатия неизвестна или не описана, используйте "сжатый".</span><span class="sxs-lookup"><span data-stu-id="73c11-194">If the logical file is compressed, but the compression scheme is unknown or not described, use "Compressed".</span></span> <span data-ttu-id="73c11-195">Если логический файл не сжат, используйте параметр NOT сжатый.</span><span class="sxs-lookup"><span data-stu-id="73c11-195">If the logical file is not compressed, use "Not Compressed".</span></span>

<span data-ttu-id="73c11-196">Это свойство наследуется [**от \_ файловой системы CIM**](cim-filesystem.md).</span><span class="sxs-lookup"><span data-stu-id="73c11-196">This property is inherited from [**CIM\_FileSystem**](cim-filesystem.md).</span></span>

</dd> <dt>

<span data-ttu-id="73c11-197">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="73c11-197">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="73c11-198">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="73c11-198">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="73c11-199">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="73c11-199">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="73c11-200">Квалификаторы: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="73c11-200">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="73c11-201">Имя класса или подкласса, используемого при создании экземпляра.</span><span class="sxs-lookup"><span data-stu-id="73c11-201">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="73c11-202">При использовании с другими ключевыми свойствами класса это свойство позволяет однозначно идентифицировать все экземпляры класса и его подклассов.</span><span class="sxs-lookup"><span data-stu-id="73c11-202">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="73c11-203">Это свойство наследуется [**от \_ файловой системы CIM**](cim-filesystem.md).</span><span class="sxs-lookup"><span data-stu-id="73c11-203">This property is inherited from [**CIM\_FileSystem**](cim-filesystem.md).</span></span>

</dd> <dt>

<span data-ttu-id="73c11-204">**кскреатионкласснаме**</span><span class="sxs-lookup"><span data-stu-id="73c11-204">**CSCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="73c11-205">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="73c11-205">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="73c11-206">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="73c11-206">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="73c11-207">Квалификаторы: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**распространяются**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ ComputerSystem**](cim-computersystem.md).**CreationClassName**")</span><span class="sxs-lookup"><span data-stu-id="73c11-207">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_ComputerSystem**](cim-computersystem.md).**CreationClassName**")</span></span>
</dt> </dl>

<span data-ttu-id="73c11-208">Определение области имени класса создания системы компьютера.</span><span class="sxs-lookup"><span data-stu-id="73c11-208">Scoping computer system's creation class name.</span></span>

<span data-ttu-id="73c11-209">Это свойство наследуется [**от \_ файловой системы CIM**](cim-filesystem.md).</span><span class="sxs-lookup"><span data-stu-id="73c11-209">This property is inherited from [**CIM\_FileSystem**](cim-filesystem.md).</span></span>

</dd> <dt>

<span data-ttu-id="73c11-210">**CSName**</span><span class="sxs-lookup"><span data-stu-id="73c11-210">**CSName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="73c11-211">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="73c11-211">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="73c11-212">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="73c11-212">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="73c11-213">Квалификаторы: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**распространяются**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ ComputerSystem**](cim-computersystem.md).**Name**")</span><span class="sxs-lookup"><span data-stu-id="73c11-213">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_ComputerSystem**](cim-computersystem.md).**Name**")</span></span>
</dt> </dl>

<span data-ttu-id="73c11-214">Определение области имени системы компьютера.</span><span class="sxs-lookup"><span data-stu-id="73c11-214">Scoping computer system's name.</span></span>

<span data-ttu-id="73c11-215">Это свойство наследуется [**от \_ файловой системы CIM**](cim-filesystem.md).</span><span class="sxs-lookup"><span data-stu-id="73c11-215">This property is inherited from [**CIM\_FileSystem**](cim-filesystem.md).</span></span>

</dd> <dt>

<span data-ttu-id="73c11-216">**Описание**</span><span class="sxs-lookup"><span data-stu-id="73c11-216">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="73c11-217">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="73c11-217">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="73c11-218">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="73c11-218">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="73c11-219">Квалификаторы: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Описание")</span><span class="sxs-lookup"><span data-stu-id="73c11-219">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="73c11-220">Текстовое описание объекта.</span><span class="sxs-lookup"><span data-stu-id="73c11-220">Textual description of the object.</span></span>

<span data-ttu-id="73c11-221">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="73c11-221">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="73c11-222">**EncryptionMethod**</span><span class="sxs-lookup"><span data-stu-id="73c11-222">**EncryptionMethod**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="73c11-223">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="73c11-223">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="73c11-224">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="73c11-224">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="73c11-225">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. DMTF \| \| -раздел 002,8 ")</span><span class="sxs-lookup"><span data-stu-id="73c11-225">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Partition\|002.8")</span></span>
</dt> </dl>

<span data-ttu-id="73c11-226">Произвольная строка, идентифицирующая алгоритм или средство, используемые для шифрования логического файла.</span><span class="sxs-lookup"><span data-stu-id="73c11-226">Free-form string that identifies the algorithm or tool used to encrypt a logical file.</span></span> <span data-ttu-id="73c11-227">Если схема шифрования не индулжед (например, из соображений безопасности), используйте "Unknown".</span><span class="sxs-lookup"><span data-stu-id="73c11-227">If the encryption scheme is not indulged (for security reasons, for example), use "Unknown".</span></span> <span data-ttu-id="73c11-228">Если файл зашифрован, но либо его схема шифрования неизвестна, либо не раскрывается, используйте "encrypted".</span><span class="sxs-lookup"><span data-stu-id="73c11-228">If the file is encrypted, but either its encryption scheme is unknown or not disclosed, use "Encrypted".</span></span> <span data-ttu-id="73c11-229">Если логический файл не зашифрован, используйте параметр NOT encrypted.</span><span class="sxs-lookup"><span data-stu-id="73c11-229">If the logical file is not encrypted, use "Not Encrypted".</span></span> <span data-ttu-id="73c11-230">Это свойство наследуется [**от \_ файловой системы CIM**](cim-filesystem.md).</span><span class="sxs-lookup"><span data-stu-id="73c11-230">This property is inherited from [**CIM\_FileSystem**](cim-filesystem.md).</span></span>

</dd> <dt>

<span data-ttu-id="73c11-231">**филесистемсизе**</span><span class="sxs-lookup"><span data-stu-id="73c11-231">**FileSystemSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="73c11-232">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="73c11-232">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="73c11-233">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="73c11-233">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="73c11-234">Квалификаторы: [**единицы**](/windows/desktop/WmiSdk/standard-qualifiers) ("байт")</span><span class="sxs-lookup"><span data-stu-id="73c11-234">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="73c11-235">Общий размер файловой системы в байтах.</span><span class="sxs-lookup"><span data-stu-id="73c11-235">Total size of the file system, in bytes.</span></span> <span data-ttu-id="73c11-236">Если значение неизвестно, введите 0 (ноль).</span><span class="sxs-lookup"><span data-stu-id="73c11-236">If unknown, enter 0 (zero).</span></span>

<span data-ttu-id="73c11-237">Это свойство наследуется [**от \_ файловой системы CIM**](cim-filesystem.md).</span><span class="sxs-lookup"><span data-stu-id="73c11-237">This property is inherited from [**CIM\_FileSystem**](cim-filesystem.md).</span></span>

<span data-ttu-id="73c11-238">Дополнительные сведения об использовании значений **UInt64** в скриптах см. [в разделе Создание сценариев в WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="73c11-238">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="73c11-239">**фореграундмаунт**</span><span class="sxs-lookup"><span data-stu-id="73c11-239">**ForegroundMount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="73c11-240">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="73c11-240">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="73c11-241">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="73c11-241">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="73c11-242">Если **значение равно true**, повторные попытки выполняются на переднем плане.</span><span class="sxs-lookup"><span data-stu-id="73c11-242">If **TRUE**, retries are performed in the foreground.</span></span> <span data-ttu-id="73c11-243">Если **значение равно false** и первая попытка подключения завершается неудачно, повторные попытки выполняются в фоновом режиме.</span><span class="sxs-lookup"><span data-stu-id="73c11-243">If **FALSE**, and the first mount attempt fails, retries are performed in the background.</span></span>

</dd> <dt>

<span data-ttu-id="73c11-244">**хардмаунт**</span><span class="sxs-lookup"><span data-stu-id="73c11-244">**HardMount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="73c11-245">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="73c11-245">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="73c11-246">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="73c11-246">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="73c11-247">Если **значение равно true**, то после подключения файловой системы запросы NFS повторяются до тех пор, пока система размещения не ответит.</span><span class="sxs-lookup"><span data-stu-id="73c11-247">If **TRUE**, after the file system is mounted, NFS requests are retried until the hosting system responds.</span></span> <span data-ttu-id="73c11-248">Если **значение равно false**, то после подключения файловой системы возвращается сообщение об ошибке, если система размещения не отвечает.</span><span class="sxs-lookup"><span data-stu-id="73c11-248">If **FALSE**, after the file system is mounted, an error is returned if the hosting system does not respond.</span></span>

</dd> <dt>

<span data-ttu-id="73c11-249">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="73c11-249">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="73c11-250">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="73c11-250">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="73c11-251">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="73c11-251">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="73c11-252">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" Дата установки ")</span><span class="sxs-lookup"><span data-stu-id="73c11-252">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="73c11-253">Дата и время установки объекта.</span><span class="sxs-lookup"><span data-stu-id="73c11-253">Date and time the object was installed.</span></span> <span data-ttu-id="73c11-254">Для этого свойства не требуется значение, указывающее, что объект установлен.</span><span class="sxs-lookup"><span data-stu-id="73c11-254">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="73c11-255">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="73c11-255">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="73c11-256">**Прервать**</span><span class="sxs-lookup"><span data-stu-id="73c11-256">**Interrupt**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="73c11-257">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="73c11-257">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="73c11-258">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="73c11-258">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="73c11-259">**Значение true** показывает, что прерывания разрешены для жестких подключений.</span><span class="sxs-lookup"><span data-stu-id="73c11-259">If **TRUE**, interrupts are permitted for hard mounts.</span></span> <span data-ttu-id="73c11-260">Если **значение равно false**, прерывания не учитываются для жестких подключений.</span><span class="sxs-lookup"><span data-stu-id="73c11-260">If **FALSE**, interrupts are ignored for hard mounts.</span></span>

</dd> <dt>

<span data-ttu-id="73c11-261">**максфиленамеленгс**</span><span class="sxs-lookup"><span data-stu-id="73c11-261">**MaxFileNameLength**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="73c11-262">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="73c11-262">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="73c11-263">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="73c11-263">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="73c11-264">Максимальная длина имени файла в файловой системе.</span><span class="sxs-lookup"><span data-stu-id="73c11-264">Maximum length of a file name within the file system.</span></span> <span data-ttu-id="73c11-265">Значение 0 (ноль) указывает на отсутствие ограничения на длину имени файла.</span><span class="sxs-lookup"><span data-stu-id="73c11-265">A value of 0 (zero)indicates that there is no limit for file name length.</span></span>

<span data-ttu-id="73c11-266">Это свойство наследуется [**от \_ файловой системы CIM**](cim-filesystem.md).</span><span class="sxs-lookup"><span data-stu-id="73c11-266">This property is inherited from [**CIM\_FileSystem**](cim-filesystem.md).</span></span>

</dd> <dt>

<span data-ttu-id="73c11-267">**маунтфаилуреретриес**</span><span class="sxs-lookup"><span data-stu-id="73c11-267">**MountFailureRetries**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="73c11-268">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="73c11-268">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="73c11-269">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="73c11-269">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="73c11-270">Максимально допустимое число повторных попыток подключения.</span><span class="sxs-lookup"><span data-stu-id="73c11-270">Maximum number of mount failure retries that are allowed.</span></span>

</dd> <dt>

<span data-ttu-id="73c11-271">**Name**</span><span class="sxs-lookup"><span data-stu-id="73c11-271">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="73c11-272">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="73c11-272">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="73c11-273">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="73c11-273">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="73c11-274">Квалификаторы: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("имя")</span><span class="sxs-lookup"><span data-stu-id="73c11-274">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="73c11-275">Метка, по которой известен объект.</span><span class="sxs-lookup"><span data-stu-id="73c11-275">Label by which the object is known.</span></span> <span data-ttu-id="73c11-276">При создании подклассов это свойство может быть переопределено как свойство ключа.</span><span class="sxs-lookup"><span data-stu-id="73c11-276">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="73c11-277">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="73c11-277">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="73c11-278">**реадбуфферсизе**</span><span class="sxs-lookup"><span data-stu-id="73c11-278">**ReadBufferSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="73c11-279">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="73c11-279">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="73c11-280">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="73c11-280">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="73c11-281">Квалификаторы: [**единицы**](/windows/desktop/WmiSdk/standard-qualifiers) ("байт")</span><span class="sxs-lookup"><span data-stu-id="73c11-281">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="73c11-282">Размер буфера чтения, в байтах.</span><span class="sxs-lookup"><span data-stu-id="73c11-282">Read buffer size, in bytes.</span></span>

<span data-ttu-id="73c11-283">Дополнительные сведения об использовании значений **UInt64** в скриптах см. [в разделе Создание сценариев в WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="73c11-283">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="73c11-284">**ReadOnly**</span><span class="sxs-lookup"><span data-stu-id="73c11-284">**ReadOnly**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="73c11-285">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="73c11-285">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="73c11-286">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="73c11-286">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="73c11-287">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB. \|Основной узел IETF-Resources-MIB. хрфсакцесс ")</span><span class="sxs-lookup"><span data-stu-id="73c11-287">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB.IETF\|HOST-RESOURCES-MIB.hrFSAccess")</span></span>
</dt> </dl>

<span data-ttu-id="73c11-288">Если **значение — true**, файловая система предназначена только для чтения.</span><span class="sxs-lookup"><span data-stu-id="73c11-288">If **TRUE**, the file system is designated as read-only.</span></span>

<span data-ttu-id="73c11-289">Это свойство наследуется [**от \_ файловой системы CIM**](cim-filesystem.md).</span><span class="sxs-lookup"><span data-stu-id="73c11-289">This property is inherited from [**CIM\_FileSystem**](cim-filesystem.md).</span></span>

</dd> <dt>

<span data-ttu-id="73c11-290">**ретрансмиссионаттемптс**</span><span class="sxs-lookup"><span data-stu-id="73c11-290">**RetransmissionAttempts**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="73c11-291">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="73c11-291">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="73c11-292">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="73c11-292">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="73c11-293">Максимально допустимое количество повторных передач NFS.</span><span class="sxs-lookup"><span data-stu-id="73c11-293">Maximum number of NFS retransmissions allowed.</span></span>

</dd> <dt>

<span data-ttu-id="73c11-294">**ретрансмиссионтимеаут**</span><span class="sxs-lookup"><span data-stu-id="73c11-294">**RetransmissionTimeout**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="73c11-295">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="73c11-295">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="73c11-296">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="73c11-296">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="73c11-297">Квалификаторы: [**единицы**](/windows/desktop/WmiSdk/standard-qualifiers) ("десятые доли секунды")</span><span class="sxs-lookup"><span data-stu-id="73c11-297">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("tenths of seconds")</span></span>
</dt> </dl>

<span data-ttu-id="73c11-298">Время ожидания NFS (в десятых долях секунды).</span><span class="sxs-lookup"><span data-stu-id="73c11-298">NFS time-out, in tenths of a second.</span></span>

</dd> <dt>

<span data-ttu-id="73c11-299">**Корневой**</span><span class="sxs-lookup"><span data-stu-id="73c11-299">**Root**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="73c11-300">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="73c11-300">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="73c11-301">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="73c11-301">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="73c11-302">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB. \|Основной узел IETF-Resources-MIB. хрфсмаунтпоинт ")</span><span class="sxs-lookup"><span data-stu-id="73c11-302">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB.IETF\|HOST-RESOURCES-MIB.hrFSMountPoint")</span></span>
</dt> </dl>

<span data-ttu-id="73c11-303">Имя пути или другие сведения, определяющие корень файловой системы.</span><span class="sxs-lookup"><span data-stu-id="73c11-303">Path name or other information that defines the root of the file system.</span></span>

<span data-ttu-id="73c11-304">Это свойство наследуется [**от \_ файловой системы CIM**](cim-filesystem.md).</span><span class="sxs-lookup"><span data-stu-id="73c11-304">This property is inherited from [**CIM\_FileSystem**](cim-filesystem.md).</span></span>

</dd> <dt>

<span data-ttu-id="73c11-305">**серверкоммуникатионпорт**</span><span class="sxs-lookup"><span data-stu-id="73c11-305">**ServerCommunicationPort**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="73c11-306">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="73c11-306">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="73c11-307">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="73c11-307">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="73c11-308">Номер порта UDP системы удаленного компьютера.</span><span class="sxs-lookup"><span data-stu-id="73c11-308">Remote computer system's UDP port number.</span></span>

</dd> <dt>

<span data-ttu-id="73c11-309">**Состояние**</span><span class="sxs-lookup"><span data-stu-id="73c11-309">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="73c11-310">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="73c11-310">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="73c11-311">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="73c11-311">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="73c11-312">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("состояние")</span><span class="sxs-lookup"><span data-stu-id="73c11-312">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="73c11-313">Текущее состояние объекта.</span><span class="sxs-lookup"><span data-stu-id="73c11-313">Current status of the object.</span></span>

<span data-ttu-id="73c11-314">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="73c11-314">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="73c11-315">В эти значения входят:</span><span class="sxs-lookup"><span data-stu-id="73c11-315">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="73c11-316">**ОК** ("ОК")</span><span class="sxs-lookup"><span data-stu-id="73c11-316">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="73c11-317">**Ошибка** ("ошибка")</span><span class="sxs-lookup"><span data-stu-id="73c11-317">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="73c11-318">**Пониженная работоспособность** (пониженная работоспособность)</span><span class="sxs-lookup"><span data-stu-id="73c11-318">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="73c11-319">**Неизвестно** ("неизвестно")</span><span class="sxs-lookup"><span data-stu-id="73c11-319">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="73c11-320">**Пред-ошибка** ("пред Fail")</span><span class="sxs-lookup"><span data-stu-id="73c11-320">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="73c11-321">**Запуск** ("Запуск")</span><span class="sxs-lookup"><span data-stu-id="73c11-321">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="73c11-322">**Остановка** ("остановка")</span><span class="sxs-lookup"><span data-stu-id="73c11-322">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="73c11-323">**Служба** ("служба")</span><span class="sxs-lookup"><span data-stu-id="73c11-323">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="73c11-324">**Пренапряжению** ("напряжению")</span><span class="sxs-lookup"><span data-stu-id="73c11-324">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="73c11-325">**Невосстановление** ("невосстановление")</span><span class="sxs-lookup"><span data-stu-id="73c11-325">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="73c11-326">**Нет контакта** ("нет контакта")</span><span class="sxs-lookup"><span data-stu-id="73c11-326">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="73c11-327">**Потеря** связи ("потеря связи")</span><span class="sxs-lookup"><span data-stu-id="73c11-327">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="73c11-328">**вритебуфферсизе**</span><span class="sxs-lookup"><span data-stu-id="73c11-328">**WriteBufferSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="73c11-329">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="73c11-329">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="73c11-330">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="73c11-330">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="73c11-331">Квалификаторы: [**единицы**](/windows/desktop/WmiSdk/standard-qualifiers) ("байт")</span><span class="sxs-lookup"><span data-stu-id="73c11-331">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="73c11-332">Размер буфера записи в байтах.</span><span class="sxs-lookup"><span data-stu-id="73c11-332">Write buffer size, in bytes.</span></span>

<span data-ttu-id="73c11-333">Дополнительные сведения об использовании значений **UInt64** в скриптах см. [в разделе Создание сценариев в WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="73c11-333">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="73c11-334">Комментарии</span><span class="sxs-lookup"><span data-stu-id="73c11-334">Remarks</span></span>

<span data-ttu-id="73c11-335">Класс **\_ NFS CIM** является производным от [**CIM \_ ремотефилесистем**](cim-remotefilesystem.md).</span><span class="sxs-lookup"><span data-stu-id="73c11-335">The **CIM\_NFS** class is derived from [**CIM\_RemoteFileSystem**](cim-remotefilesystem.md).</span></span>

<span data-ttu-id="73c11-336">Инструментарий WMI не реализует этот класс.</span><span class="sxs-lookup"><span data-stu-id="73c11-336">WMI does not implement this class.</span></span>

<span data-ttu-id="73c11-337">Эта документация является производной от описаний класса CIM, опубликованных в формате DMTF.</span><span class="sxs-lookup"><span data-stu-id="73c11-337">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="73c11-338">Корпорация Майкрософт могла внести изменения в Исправление незначительных ошибок, соответствовать стандартам документации пакета Microsoft SDK или предоставить дополнительные сведения.</span><span class="sxs-lookup"><span data-stu-id="73c11-338">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="73c11-339">Требования</span><span class="sxs-lookup"><span data-stu-id="73c11-339">Requirements</span></span>



| <span data-ttu-id="73c11-340">Требование</span><span class="sxs-lookup"><span data-stu-id="73c11-340">Requirement</span></span> | <span data-ttu-id="73c11-341">Значение</span><span class="sxs-lookup"><span data-stu-id="73c11-341">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="73c11-342">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="73c11-342">Minimum supported client</span></span><br/> | <span data-ttu-id="73c11-343">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="73c11-343">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="73c11-344">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="73c11-344">Minimum supported server</span></span><br/> | <span data-ttu-id="73c11-345">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="73c11-345">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="73c11-346">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="73c11-346">Namespace</span></span><br/>                | <span data-ttu-id="73c11-347">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="73c11-347">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="73c11-348">MOF</span><span class="sxs-lookup"><span data-stu-id="73c11-348">MOF</span></span><br/>                      | <dl> <span data-ttu-id="73c11-349"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="73c11-349"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="73c11-350">DLL</span><span class="sxs-lookup"><span data-stu-id="73c11-350">DLL</span></span><br/>                      | <dl> <span data-ttu-id="73c11-351"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="73c11-351"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="73c11-352">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="73c11-352">See also</span></span>

<dl> <dt>

[<span data-ttu-id="73c11-353">**\_РЕМОТЕФИЛЕСИСТЕМ CIM**</span><span class="sxs-lookup"><span data-stu-id="73c11-353">**CIM\_RemoteFileSystem**</span></span>](cim-remotefilesystem.md)
</dt> </dl>

 

