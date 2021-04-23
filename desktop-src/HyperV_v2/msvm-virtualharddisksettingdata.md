---
description: Предоставляет данные настройки для виртуального жесткого диска.
ms.assetid: 492a0b81-86b2-4d7d-a118-6ec14e3971ed
title: Класс Msvm_VirtualHardDiskSettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualHardDiskSettingData
- Msvm_VirtualHardDiskSettingData.InstanceID
- Msvm_VirtualHardDiskSettingData.Caption
- Msvm_VirtualHardDiskSettingData.Description
- Msvm_VirtualHardDiskSettingData.ElementName
- Msvm_VirtualHardDiskSettingData.Type
- Msvm_VirtualHardDiskSettingData.Format
- Msvm_VirtualHardDiskSettingData.Path
- Msvm_VirtualHardDiskSettingData.ParentPath
- Msvm_VirtualHardDiskSettingData.ParentTimestamp
- Msvm_VirtualHardDiskSettingData.ParentIdentifier
- Msvm_VirtualHardDiskSettingData.MaxInternalSize
- Msvm_VirtualHardDiskSettingData.BlockSize
- Msvm_VirtualHardDiskSettingData.LogicalSectorSize
- Msvm_VirtualHardDiskSettingData.PhysicalSectorSize
- Msvm_VirtualHardDiskSettingData.VirtualDiskId
- Msvm_VirtualHardDiskSettingData.DataAlignment
- Msvm_VirtualHardDiskSettingData.PmemAddressAbstractionType
- Msvm_VirtualHardDiskSettingData.IsPmemCompatible
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 6e13efbb068d15ca4051995e7d9f317eb2ccacab
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104143891"
---
# <a name="msvm_virtualharddisksettingdata-class"></a><span data-ttu-id="d669c-103">\_Класс мсвм виртуалхарддисксеттингдата</span><span class="sxs-lookup"><span data-stu-id="d669c-103">Msvm\_VirtualHardDiskSettingData class</span></span>

<span data-ttu-id="d669c-104">Предоставляет данные настройки для виртуального жесткого диска.</span><span class="sxs-lookup"><span data-stu-id="d669c-104">Provides setting data for a virtual hard disk.</span></span>

<span data-ttu-id="d669c-105">Следующий синтаксис является упрощенным MOF-файлным (MOF) кодом и включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="d669c-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="d669c-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d669c-106">Syntax</span></span>

``` syntax
[AMENDMENT]
class Msvm_VirtualHardDiskSettingData : CIM_SettingData
{
  string   InstanceID;
  string   Caption = "Virtual Hard Disk Setting Data";
  string   Description = "Setting Data for a Virtual Hard Disk";
  string   ElementName;
  uint16   Type;
  uint16   Format;
  string   Path;
  string   ParentPath;
  DATETIME ParentTimestamp;
  string   ParentIdentifier;
  uint64   MaxInternalSize;
  uint32   BlockSize;
  uint32   LogicalSectorSize;
  uint32   PhysicalSectorSize;
  string   VirtualDiskId;
  uint64   DataAlignment;
  uint16   PmemAddressAbstractionType;
  boolean  IsPmemCompatible;
};
```

## <a name="members"></a><span data-ttu-id="d669c-107">Члены</span><span class="sxs-lookup"><span data-stu-id="d669c-107">Members</span></span>

<span data-ttu-id="d669c-108">Класс **мсвм \_ виртуалхарддисксеттингдата** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="d669c-108">The **Msvm\_VirtualHardDiskSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="d669c-109">Свойства</span><span class="sxs-lookup"><span data-stu-id="d669c-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="d669c-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="d669c-110">Properties</span></span>

<span data-ttu-id="d669c-111">Класс **мсвм \_ виртуалхарддисксеттингдата** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="d669c-111">The **Msvm\_VirtualHardDiskSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="d669c-112">**BlockSize**</span><span class="sxs-lookup"><span data-stu-id="d669c-112">**BlockSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d669c-113">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="d669c-113">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="d669c-114">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="d669c-114">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="d669c-115">Размер блока, используемого виртуальным жестким диском в байтах.</span><span class="sxs-lookup"><span data-stu-id="d669c-115">The block size used by the virtual hard disk, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="d669c-116">**Заголовок**</span><span class="sxs-lookup"><span data-stu-id="d669c-116">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d669c-117">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="d669c-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d669c-118">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d669c-118">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d669c-119">Краткое описание объекта.</span><span class="sxs-lookup"><span data-stu-id="d669c-119">A short description of the object.</span></span> <span data-ttu-id="d669c-120">Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)и всегда имеет значение "данные параметров виртуального жесткого диска".</span><span class="sxs-lookup"><span data-stu-id="d669c-120">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Virtual Hard Disk Setting Data".</span></span>

</dd> <dt>

<span data-ttu-id="d669c-121">**Выравнивание по**</span><span class="sxs-lookup"><span data-stu-id="d669c-121">**DataAlignment**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d669c-122">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="d669c-122">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="d669c-123">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="d669c-123">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="d669c-124">Задает требуемое выравнивание в байтах для полезных данных виртуального диска.</span><span class="sxs-lookup"><span data-stu-id="d669c-124">Specifies the desired alignment, in bytes, for the data payload of the virtual disk</span></span>

> [!Note]  
> <span data-ttu-id="d669c-125">Добавлено в Windows 10 версии 1709.</span><span class="sxs-lookup"><span data-stu-id="d669c-125">Added in Windows 10, version 1709.</span></span>

 

</dd> <dt>

<span data-ttu-id="d669c-126">**Описание**</span><span class="sxs-lookup"><span data-stu-id="d669c-126">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d669c-127">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="d669c-127">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d669c-128">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d669c-128">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d669c-129">Описание объекта.</span><span class="sxs-lookup"><span data-stu-id="d669c-129">A description of the object.</span></span> <span data-ttu-id="d669c-130">Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)и всегда имеет значение "Настройка данных для виртуального жесткого диска".</span><span class="sxs-lookup"><span data-stu-id="d669c-130">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Setting Data for a Virtual Hard Disk".</span></span>

</dd> <dt>

<span data-ttu-id="d669c-131">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="d669c-131">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d669c-132">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="d669c-132">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d669c-133">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d669c-133">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d669c-134">Отображаемое имя объекта.</span><span class="sxs-lookup"><span data-stu-id="d669c-134">A display name for the object.</span></span> <span data-ttu-id="d669c-135">Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="d669c-135">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="d669c-136">**Формат**</span><span class="sxs-lookup"><span data-stu-id="d669c-136">**Format**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d669c-137">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d669c-137">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d669c-138">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="d669c-138">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="d669c-139">Формат виртуального жесткого диска.</span><span class="sxs-lookup"><span data-stu-id="d669c-139">The format for the virtual hard disk.</span></span> <span data-ttu-id="d669c-140">Это может быть одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="d669c-140">This will be one of the following values.</span></span>

<dt>

<span id="VHD"></span><span id="vhd"></span>

<span data-ttu-id="d669c-141"><span id="VHD"></span><span id="vhd"></span>**Виртуальный жесткий диск** (2)</span><span class="sxs-lookup"><span data-stu-id="d669c-141"><span id="VHD"></span><span id="vhd"></span>**VHD** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="VHDX"></span><span id="vhdx"></span>

<span data-ttu-id="d669c-142"><span id="VHDX"></span><span id="vhdx"></span>**VHDX** (3)</span><span class="sxs-lookup"><span data-stu-id="d669c-142"><span id="VHDX"></span><span id="vhdx"></span>**VHDX** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="VHDSet"></span><span id="vhdset"></span><span id="VHDSET"></span>

<span data-ttu-id="d669c-143"><span id="VHDSet"></span><span id="vhdset"></span><span id="VHDSET"></span>**Вхдсет** (4)</span><span class="sxs-lookup"><span data-stu-id="d669c-143"><span id="VHDSet"></span><span id="vhdset"></span><span id="VHDSET"></span>**VHDSet** (4)</span></span>


</dt> <dd>

> [!Note]  
> <span data-ttu-id="d669c-144">Добавлено в Windows 10 и Windows Server 2016.</span><span class="sxs-lookup"><span data-stu-id="d669c-144">Added in Windows 10 and Windows Server 2016.</span></span>

 

</dd> </dl>

</dd> <dt>

<span data-ttu-id="d669c-145">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="d669c-145">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d669c-146">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="d669c-146">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d669c-147">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d669c-147">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d669c-148">Квалификаторы: **ключ**</span><span class="sxs-lookup"><span data-stu-id="d669c-148">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="d669c-149">Уникально идентифицирует экземпляр этого класса.</span><span class="sxs-lookup"><span data-stu-id="d669c-149">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="d669c-150">Это свойство наследуется [**от \_ SettingData в CIM**](/previous-versions//cc136911(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="d669c-150">This property is inherited from [**CIM\_SettingData**](/previous-versions//cc136911(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="d669c-151">**испмемкомпатибле**</span><span class="sxs-lookup"><span data-stu-id="d669c-151">**IsPmemCompatible**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d669c-152">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="d669c-152">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="d669c-153">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="d669c-153">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="d669c-154">Указывает, можно ли использовать виртуальный диск в качестве резервного хранилища для устройства с энергонезависимой памятью.</span><span class="sxs-lookup"><span data-stu-id="d669c-154">Specifies whether the virtual disk can be used as the backing store for a persistent memory device.</span></span>

> [!Note]  
> <span data-ttu-id="d669c-155">Добавлено в Windows 10 версии 1709.</span><span class="sxs-lookup"><span data-stu-id="d669c-155">Added in Windows 10, version 1709.</span></span>

 

</dd> <dt>

<span data-ttu-id="d669c-156">**логикалсекторсизе**</span><span class="sxs-lookup"><span data-stu-id="d669c-156">**LogicalSectorSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d669c-157">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="d669c-157">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="d669c-158">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="d669c-158">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="d669c-159">Размер логического сектора, используемого виртуальным жестким диском в байтах.</span><span class="sxs-lookup"><span data-stu-id="d669c-159">The logical sector size used by the virtual hard disk, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="d669c-160">**MaxInternalSize**</span><span class="sxs-lookup"><span data-stu-id="d669c-160">**MaxInternalSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d669c-161">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="d669c-161">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="d669c-162">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="d669c-162">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="d669c-163">Максимальный размер виртуального жесткого диска, отображаемый виртуальной машиной в байтах.</span><span class="sxs-lookup"><span data-stu-id="d669c-163">The maximum size of the virtual hard disk as viewable by the virtual machine, in bytes.</span></span> <span data-ttu-id="d669c-164">Этот размер будет округляться до следующего большего числа, кратного размеру сектора.</span><span class="sxs-lookup"><span data-stu-id="d669c-164">This size will be rounded up to the next largest multiple of the sector size.</span></span>

</dd> <dt>

<span data-ttu-id="d669c-165">**парентидентифиер**</span><span class="sxs-lookup"><span data-stu-id="d669c-165">**ParentIdentifier**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d669c-166">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="d669c-166">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d669c-167">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d669c-167">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d669c-168">Идентификатор GUID, используемый для уникальной идентификации родителя виртуального жесткого диска.</span><span class="sxs-lookup"><span data-stu-id="d669c-168">The GUID used to uniquely identify the parent of the virtual hard disk.</span></span> <span data-ttu-id="d669c-169">Если виртуальный жесткий диск не имеет родителя, это поле будет пустым.</span><span class="sxs-lookup"><span data-stu-id="d669c-169">If the virtual hard disk does not have a parent, then this field is empty.</span></span>

> [!Note]  
> <span data-ttu-id="d669c-170">Добавлено в Windows 10 и Windows Server 2016.</span><span class="sxs-lookup"><span data-stu-id="d669c-170">Added in Windows 10 and Windows Server 2016.</span></span>

 

</dd> <dt>

<span data-ttu-id="d669c-171">**ParentPath**</span><span class="sxs-lookup"><span data-stu-id="d669c-171">**ParentPath**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d669c-172">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="d669c-172">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d669c-173">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="d669c-173">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="d669c-174">Родительский элемент виртуального жесткого диска.</span><span class="sxs-lookup"><span data-stu-id="d669c-174">The parent of the virtual hard disk.</span></span> <span data-ttu-id="d669c-175">Если виртуальный жесткий диск не имеет родителя, это свойство будет пустым.</span><span class="sxs-lookup"><span data-stu-id="d669c-175">If the virtual hard disk does not have a parent, then this property is empty.</span></span>

</dd> <dt>

<span data-ttu-id="d669c-176">**паренттиместамп**</span><span class="sxs-lookup"><span data-stu-id="d669c-176">**ParentTimestamp**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d669c-177">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="d669c-177">Data type: **DATETIME**</span></span>
</dt> <dt>

<span data-ttu-id="d669c-178">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d669c-178">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d669c-179">Метка времени родителя виртуального жесткого диска.</span><span class="sxs-lookup"><span data-stu-id="d669c-179">The timestamp of the parent of the virtual hard disk.</span></span> <span data-ttu-id="d669c-180">Если виртуальный жесткий диск не имеет родителя, это поле будет пустым.</span><span class="sxs-lookup"><span data-stu-id="d669c-180">If the virtual hard disk does not have a parent, then this field is empty.</span></span>

> [!Note]  
> <span data-ttu-id="d669c-181">Добавлено в Windows 10 и Windows Server 2016.</span><span class="sxs-lookup"><span data-stu-id="d669c-181">Added in Windows 10 and Windows Server 2016.</span></span>

 

</dd> <dt>

<span data-ttu-id="d669c-182">**Путь**</span><span class="sxs-lookup"><span data-stu-id="d669c-182">**Path**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d669c-183">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="d669c-183">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d669c-184">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="d669c-184">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="d669c-185">Полный путь к виртуальному жесткому диску.</span><span class="sxs-lookup"><span data-stu-id="d669c-185">The fully qualified path of the virtual hard disk.</span></span>

</dd> <dt>

<span data-ttu-id="d669c-186">**фисикалсекторсизе**</span><span class="sxs-lookup"><span data-stu-id="d669c-186">**PhysicalSectorSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d669c-187">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="d669c-187">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="d669c-188">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="d669c-188">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="d669c-189">Размер физического сектора, используемый виртуальным жестким диском в байтах.</span><span class="sxs-lookup"><span data-stu-id="d669c-189">The physical sector size used by the virtual hard disk, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="d669c-190">**пмемаддрессабстрактионтипе**</span><span class="sxs-lookup"><span data-stu-id="d669c-190">**PmemAddressAbstractionType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d669c-191">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d669c-191">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d669c-192">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="d669c-192">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="d669c-193">Метод абстракции постоянных адресов памяти для использования с этим виртуальным диском.</span><span class="sxs-lookup"><span data-stu-id="d669c-193">The persistent memory address abstraction method to be used with this virtual disk.</span></span>

> [!Note]  
> <span data-ttu-id="d669c-194">Добавлено в Windows 10 версии 1709.</span><span class="sxs-lookup"><span data-stu-id="d669c-194">Added in Windows 10, version 1709.</span></span>

 

<dt>

<span id="None"></span><span id="none"></span><span id="NONE"></span>

<span data-ttu-id="d669c-195">**Нет** (0)</span><span class="sxs-lookup"><span data-stu-id="d669c-195">**None** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="BTT"></span><span id="btt"></span>

<span data-ttu-id="d669c-196">**БТТ** (1)</span><span class="sxs-lookup"><span data-stu-id="d669c-196">**BTT** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="d669c-197">**Неизвестно** (65535)</span><span class="sxs-lookup"><span data-stu-id="d669c-197">**Unknown** (65535)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="d669c-198">**Тип**</span><span class="sxs-lookup"><span data-stu-id="d669c-198">**Type**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d669c-199">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d669c-199">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d669c-200">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="d669c-200">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="d669c-201">Тип виртуального жесткого диска.</span><span class="sxs-lookup"><span data-stu-id="d669c-201">The type of virtual hard disk.</span></span> <span data-ttu-id="d669c-202">Это может быть одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="d669c-202">This will be one of the following values.</span></span>

<dt>

<span id="Fixed"></span><span id="fixed"></span><span id="FIXED"></span>

<span data-ttu-id="d669c-203">**Исправлено** (2)</span><span class="sxs-lookup"><span data-stu-id="d669c-203">**Fixed** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Dynamic"></span><span id="dynamic"></span><span id="DYNAMIC"></span>

<span data-ttu-id="d669c-204">**Dynamic** (3)</span><span class="sxs-lookup"><span data-stu-id="d669c-204">**Dynamic** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Differencing"></span><span id="differencing"></span><span id="DIFFERENCING"></span>

<span data-ttu-id="d669c-205">**Разностное** (4)</span><span class="sxs-lookup"><span data-stu-id="d669c-205">**Differencing** (4)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="d669c-206">**VirtualDiskId**</span><span class="sxs-lookup"><span data-stu-id="d669c-206">**VirtualDiskId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d669c-207">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="d669c-207">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d669c-208">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="d669c-208">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="d669c-209">Идентификатор GUID, используемый для уникальной идентификации виртуального диска.</span><span class="sxs-lookup"><span data-stu-id="d669c-209">The GUID that is used to uniquely identify the virtual disk.</span></span>

<span data-ttu-id="d669c-210">Если метод [**мсвм \_ ). жетвиртуалхарддисксеттингдата**](getvirtualharddisksettingdata-msvm-imagemanagementservice.md) возвращает экземпляр **мсвм \_ виртуалхарддисксеттингдата**, клиент может использовать это свойство для получения уникального идентификатора диска VHD.</span><span class="sxs-lookup"><span data-stu-id="d669c-210">When the [**Msvm\_ImageManagementService.GetVirtualHardDiskSettingData**](getvirtualharddisksettingdata-msvm-imagemanagementservice.md) method returns an instance of **Msvm\_VirtualHardDiskSettingData**, the client can use this property to get the unique disk ID of the VHD.</span></span>

<span data-ttu-id="d669c-211">При обнаружении конфликтов или в противном случае клиент может задать значение **виртуалдискид** для нового идентификатора GUID и передать этот экземпляр **мсвм \_ виртуалхарддисксеттингдата** в метод [**мсвм \_ ). сетвиртуалхарддисксеттингдата**](setvirtualharddisksettingdata-msvm-imagemanagementservice.md) , чтобы изменить идентификатор диска VHD.</span><span class="sxs-lookup"><span data-stu-id="d669c-211">On conflict detection or otherwise, a client can set the **VirtualDiskId** value to a new GUID and pass this **Msvm\_VirtualHardDiskSettingData** instance to the [**Msvm\_ImageManagementService.SetVirtualHardDiskSettingData**](setvirtualharddisksettingdata-msvm-imagemanagementservice.md) method to change the disk ID of the VHD.</span></span> <span data-ttu-id="d669c-212">Если виртуальный жесткий диск не является VHD-файлами или подключен к нему, операция завершается ошибкой.</span><span class="sxs-lookup"><span data-stu-id="d669c-212">If the VHD is not a VHDX VHD, or if the VHD is attached, the operation fails.</span></span> <span data-ttu-id="d669c-213">Операция также завершается ошибкой, если переданное значение имеет неправильный формат, то есть не GUID или все 0.</span><span class="sxs-lookup"><span data-stu-id="d669c-213">The operation also fails if the passed value is malformed, that is, not a GUID or has all 0s.</span></span> <span data-ttu-id="d669c-214">Операция автоматически завершается успешно, если переданное значение совпадает с ИДЕНТИФИКАТОРом текущего диска.</span><span class="sxs-lookup"><span data-stu-id="d669c-214">The operation silently succeeds if the passed value is the same as the current disk ID.</span></span>

<span data-ttu-id="d669c-215">Ошибки, создаваемые функцией [**сетвиртуалдискинформатион**](/windows/win32/api/virtdisk/nf-virtdisk-setvirtualdiskinformation) , передаются через это свойство.</span><span class="sxs-lookup"><span data-stu-id="d669c-215">Errors generated by the [**SetVirtualDiskInformation**](/windows/win32/api/virtdisk/nf-virtdisk-setvirtualdiskinformation) function are bubbled up through this property.</span></span> <span data-ttu-id="d669c-216">Клиент также может использовать тот же механизм для предоставления значения **виртуалдискид** при создании виртуального жесткого диска с помощью метода [**Мсвм \_ ). креатевиртуалхарддиск**](createvirtualharddisk-msvm-imagemanagementservice.md) в том же пространстве имен.</span><span class="sxs-lookup"><span data-stu-id="d669c-216">A client can also use the same mechanism to provide the **VirtualDiskId** value at VHD creation via the [**Msvm\_ImageManagementService.CreateVirtualHardDisk**](createvirtualharddisk-msvm-imagemanagementservice.md) method in the same namespace.</span></span> <span data-ttu-id="d669c-217">Это можно использовать для создания виртуальных жестких дисков VHD1 или VHD2.</span><span class="sxs-lookup"><span data-stu-id="d669c-217">This can be used to create VHD1 or VHD2 VHDs.</span></span>

<span data-ttu-id="d669c-218">**Windows 8.1:** Это значение не поддерживается до Windows 8.1 и Windows Server 2012 R2.</span><span class="sxs-lookup"><span data-stu-id="d669c-218">**Windows 8.1:** This value is not supported until Windows 8.1 and Windows Server 2012 R2.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="d669c-219">Требования</span><span class="sxs-lookup"><span data-stu-id="d669c-219">Requirements</span></span>



| <span data-ttu-id="d669c-220">Требование</span><span class="sxs-lookup"><span data-stu-id="d669c-220">Requirement</span></span> | <span data-ttu-id="d669c-221">Значение</span><span class="sxs-lookup"><span data-stu-id="d669c-221">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d669c-222">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="d669c-222">Minimum supported client</span></span><br/> | <span data-ttu-id="d669c-223">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="d669c-223">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="d669c-224">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="d669c-224">Minimum supported server</span></span><br/> | <span data-ttu-id="d669c-225">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="d669c-225">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="d669c-226">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="d669c-226">Namespace</span></span><br/>                | <span data-ttu-id="d669c-227">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="d669c-227">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="d669c-228">MOF</span><span class="sxs-lookup"><span data-stu-id="d669c-228">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d669c-229"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="d669c-229"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="d669c-230">DLL</span><span class="sxs-lookup"><span data-stu-id="d669c-230">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d669c-231"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="d669c-231"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="d669c-232">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d669c-232">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d669c-233">**\_SETTINGDATA CIM**</span><span class="sxs-lookup"><span data-stu-id="d669c-233">**CIM\_SettingData**</span></span>](cim-settingdata.md)
</dt> <dt>

[<span data-ttu-id="d669c-234">**жетвиртуалхарддисксеттингдата**</span><span class="sxs-lookup"><span data-stu-id="d669c-234">**GetVirtualHardDiskSettingData**</span></span>](getvirtualharddisksettingdata-msvm-imagemanagementservice.md)
</dt> </dl>

 

