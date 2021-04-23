---
description: Содержит подробные сведения о подключенном вручную образе хранилища.
ms.assetid: 40b94c5f-c277-40c8-a55d-ebc64cb231ca
title: Класс Msvm_MountedStorageImage
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_MountedStorageImage
- Msvm_MountedStorageImage.InstanceID
- Msvm_MountedStorageImage.Caption
- Msvm_MountedStorageImage.Description
- Msvm_MountedStorageImage.ElementName
- Msvm_MountedStorageImage.InstallDate
- Msvm_MountedStorageImage.Name
- Msvm_MountedStorageImage.OperationalStatus
- Msvm_MountedStorageImage.StatusDescriptions
- Msvm_MountedStorageImage.Status
- Msvm_MountedStorageImage.HealthState
- Msvm_MountedStorageImage.CommunicationStatus
- Msvm_MountedStorageImage.DetailedStatus
- Msvm_MountedStorageImage.OperatingStatus
- Msvm_MountedStorageImage.PrimaryStatus
- Msvm_MountedStorageImage.Type
- Msvm_MountedStorageImage.Access
- Msvm_MountedStorageImage.PortNumber
- Msvm_MountedStorageImage.PathId
- Msvm_MountedStorageImage.TargetId
- Msvm_MountedStorageImage.Lun
- Msvm_MountedStorageImage.PnpDevicePath
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 1b6f00b137fc73bcf8f79d39e6f7bfb5a6d7c944
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103817889"
---
# <a name="msvm_mountedstorageimage-class"></a><span data-ttu-id="54266-103">\_Класс мсвм маунтедсторажеимаже</span><span class="sxs-lookup"><span data-stu-id="54266-103">Msvm\_MountedStorageImage class</span></span>

<span data-ttu-id="54266-104">Содержит подробные сведения о подключенном вручную образе хранилища.</span><span class="sxs-lookup"><span data-stu-id="54266-104">Provides detailed information about a manually mounted storage image.</span></span>

<span data-ttu-id="54266-105">Следующий синтаксис является упрощенным MOF-файлным (MOF) кодом и включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="54266-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="54266-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="54266-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_MountedStorageImage : CIM_LogicalElement
{
  string   InstanceID;
  string   Caption = "Mounted Storage Image";
  string   Description = "Information about a mounted storage image.";
  string   ElementName = "Mounted Storage Image";
  datetime InstallDate;
  string   Name;
  uint16   OperationalStatus[];
  string   StatusDescriptions[] = { "OK" };
  string   Status = "OK";
  uint16   HealthState = 5;
  uint16   CommunicationStatus;
  uint16   DetailedStatus;
  uint16   OperatingStatus;
  uint16   PrimaryStatus;
  uint16   Type;
  uint16   Access;
  UINT8    PortNumber;
  UINT8    PathId;
  UINT8    TargetId;
  UINT8    Lun;
  string   PnpDevicePath;
};
```

## <a name="members"></a><span data-ttu-id="54266-107">Члены</span><span class="sxs-lookup"><span data-stu-id="54266-107">Members</span></span>

<span data-ttu-id="54266-108">Класс **мсвм \_ маунтедсторажеимаже** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="54266-108">The **Msvm\_MountedStorageImage** class has these types of members:</span></span>

-   [<span data-ttu-id="54266-109">Методы</span><span class="sxs-lookup"><span data-stu-id="54266-109">Methods</span></span>](#methods)
-   [<span data-ttu-id="54266-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="54266-110">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="54266-111">Методы</span><span class="sxs-lookup"><span data-stu-id="54266-111">Methods</span></span>

<span data-ttu-id="54266-112">Класс **мсвм \_ маунтедсторажеимаже** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="54266-112">The **Msvm\_MountedStorageImage** class has these methods.</span></span>



| <span data-ttu-id="54266-113">Метод</span><span class="sxs-lookup"><span data-stu-id="54266-113">Method</span></span>                                                                          | <span data-ttu-id="54266-114">Описание</span><span class="sxs-lookup"><span data-stu-id="54266-114">Description</span></span>                                    |
|:--------------------------------------------------------------------------------|:-----------------------------------------------|
| [<span data-ttu-id="54266-115">**детачвиртуалхарддиск**</span><span class="sxs-lookup"><span data-stu-id="54266-115">**DetachVirtualHardDisk**</span></span>](detachvirtualharddisk-msvm-mountedstorageimage.md) | <span data-ttu-id="54266-116">Отсоединяет образ подключенного хранилища.</span><span class="sxs-lookup"><span data-stu-id="54266-116">Detaches the mounted storage image.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="54266-117">Свойства</span><span class="sxs-lookup"><span data-stu-id="54266-117">Properties</span></span>

<span data-ttu-id="54266-118">Класс **мсвм \_ маунтедсторажеимаже** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="54266-118">The **Msvm\_MountedStorageImage** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="54266-119">**Доступ**</span><span class="sxs-lookup"><span data-stu-id="54266-119">**Access**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="54266-120">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="54266-120">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="54266-121">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="54266-121">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="54266-122">Доступ, под которым подключен образ хранилища.</span><span class="sxs-lookup"><span data-stu-id="54266-122">The access under which the storage image is mounted.</span></span>

<dt>

<span id="Read-only"></span><span id="read-only"></span><span id="READ-ONLY"></span>

<span data-ttu-id="54266-123">**Только для чтения** (1)</span><span class="sxs-lookup"><span data-stu-id="54266-123">**Read-only** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Read_Write"></span><span id="read_write"></span><span id="READ_WRITE"></span>

<span data-ttu-id="54266-124">**Чтение и запись** (2)</span><span class="sxs-lookup"><span data-stu-id="54266-124">**Read/Write** (2)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="54266-125">**Заголовок**</span><span class="sxs-lookup"><span data-stu-id="54266-125">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="54266-126">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="54266-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="54266-127">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="54266-127">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="54266-128">Краткое описание объекта.</span><span class="sxs-lookup"><span data-stu-id="54266-128">A short description of the object.</span></span> <span data-ttu-id="54266-129">Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)и всегда содержит "образ подключенного хранилища".</span><span class="sxs-lookup"><span data-stu-id="54266-129">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it always contains "Mounted Storage Image".</span></span>

</dd> <dt>

<span data-ttu-id="54266-130">**коммуникатионстатус**</span><span class="sxs-lookup"><span data-stu-id="54266-130">**CommunicationStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="54266-131">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="54266-131">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="54266-132">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="54266-132">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="54266-133">Указывает способность инструментирования взаимодействовать с базовым управляемым элементом.</span><span class="sxs-lookup"><span data-stu-id="54266-133">Indicates the ability of the instrumentation to communicate with the underlying managed element.</span></span> <span data-ttu-id="54266-134">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)и всегда имеет значение **null**.</span><span class="sxs-lookup"><span data-stu-id="54266-134">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="54266-135">**Описание**</span><span class="sxs-lookup"><span data-stu-id="54266-135">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="54266-136">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="54266-136">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="54266-137">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="54266-137">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="54266-138">Описание объекта.</span><span class="sxs-lookup"><span data-stu-id="54266-138">A description of the object.</span></span> <span data-ttu-id="54266-139">Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)и всегда содержит "сведения о подключенном образе хранилища".</span><span class="sxs-lookup"><span data-stu-id="54266-139">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it always contains "Information about a mounted storage image.".</span></span>

</dd> <dt>

<span data-ttu-id="54266-140">**DetailedStatus**</span><span class="sxs-lookup"><span data-stu-id="54266-140">**DetailedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="54266-141">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="54266-141">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="54266-142">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="54266-142">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="54266-143">Дополняет свойство **примаристатус** дополнительными сведениями о состоянии.</span><span class="sxs-lookup"><span data-stu-id="54266-143">Compliments the **PrimaryStatus** property with additional status detail.</span></span> <span data-ttu-id="54266-144">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)и всегда имеет значение **null**.</span><span class="sxs-lookup"><span data-stu-id="54266-144">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="54266-145">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="54266-145">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="54266-146">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="54266-146">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="54266-147">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="54266-147">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="54266-148">Отображаемое имя объекта.</span><span class="sxs-lookup"><span data-stu-id="54266-148">A display name for the object.</span></span> <span data-ttu-id="54266-149">Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)и всегда содержит "образ подключенного хранилища".</span><span class="sxs-lookup"><span data-stu-id="54266-149">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it always contains "Mounted Storage Image".</span></span>

</dd> <dt>

<span data-ttu-id="54266-150">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="54266-150">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="54266-151">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="54266-151">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="54266-152">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="54266-152">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="54266-153">Текущая работоспособность элемента.</span><span class="sxs-lookup"><span data-stu-id="54266-153">The current health of the element.</span></span> <span data-ttu-id="54266-154">Этот атрибут выражает работоспособность этого элемента, но не обязательно для его подкомпонентов.</span><span class="sxs-lookup"><span data-stu-id="54266-154">This attribute expresses the health of this element but not necessarily that of its subcomponents.</span></span> <span data-ttu-id="54266-155">Возможные значения: от 0 до 30, где 5 означает, что элемент полностью работоспособен, а 30 означает, что элемент полностью нефункциональный.</span><span class="sxs-lookup"><span data-stu-id="54266-155">The possible values are 0 to 30, where 5 means the element is entirely healthy and 30 means the element is completely nonfunctional.</span></span> <span data-ttu-id="54266-156">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)и всегда имеет значение 5.</span><span class="sxs-lookup"><span data-stu-id="54266-156">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and it is always set to 5.</span></span>

</dd> <dt>

<span data-ttu-id="54266-157">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="54266-157">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="54266-158">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="54266-158">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="54266-159">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="54266-159">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="54266-160">Дата и время создания конфигурации виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="54266-160">The date and time the virtual machine configuration was created.</span></span> <span data-ttu-id="54266-161">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="54266-161">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="54266-162">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="54266-162">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="54266-163">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="54266-163">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="54266-164">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="54266-164">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="54266-165">Квалификаторы: **ключ**</span><span class="sxs-lookup"><span data-stu-id="54266-165">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="54266-166">Уникально идентифицирует экземпляр этого класса.</span><span class="sxs-lookup"><span data-stu-id="54266-166">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="54266-167">Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)и всегда имеет **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="54266-167">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="54266-168">**Номеров**</span><span class="sxs-lookup"><span data-stu-id="54266-168">**Lun**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="54266-169">Тип данных: **UINT8**</span><span class="sxs-lookup"><span data-stu-id="54266-169">Data type: **UINT8**</span></span>
</dt> <dt>

<span data-ttu-id="54266-170">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="54266-170">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="54266-171">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="54266-171">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="54266-172">ИДЕНТИФИКАТОР LUN SCSI Address.</span><span class="sxs-lookup"><span data-stu-id="54266-172">The SCSI address LUN ID.</span></span>

</dd> <dt>

<span data-ttu-id="54266-173">**Name**</span><span class="sxs-lookup"><span data-stu-id="54266-173">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="54266-174">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="54266-174">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="54266-175">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="54266-175">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="54266-176">Путь к подключенному виртуальному жесткому диску.</span><span class="sxs-lookup"><span data-stu-id="54266-176">The path to the VHD that is mounted.</span></span> <span data-ttu-id="54266-177">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="54266-177">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="54266-178">**оператингстатус**</span><span class="sxs-lookup"><span data-stu-id="54266-178">**OperatingStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="54266-179">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="54266-179">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="54266-180">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="54266-180">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="54266-181">Предоставляет сведения о текущем состоянии для рабочего условия элемента и может использоваться для предоставления более подробных сведений относительно значения свойства **EnabledState** .</span><span class="sxs-lookup"><span data-stu-id="54266-181">Provides current status information for the operational condition of the element and can be used for providing more detail with respect to the value of the **EnabledState** property.</span></span> <span data-ttu-id="54266-182">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)и всегда имеет значение **null**.</span><span class="sxs-lookup"><span data-stu-id="54266-182">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="54266-183">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="54266-183">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="54266-184">Тип данных: **UInt16** , массив</span><span class="sxs-lookup"><span data-stu-id="54266-184">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="54266-185">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="54266-185">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="54266-186">Текущее состояние объекта.</span><span class="sxs-lookup"><span data-stu-id="54266-186">The current status of the object.</span></span> <span data-ttu-id="54266-187">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), и каждый элемент массива всегда имеет значение **null**.</span><span class="sxs-lookup"><span data-stu-id="54266-187">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and each array element is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="54266-188">**пасид**</span><span class="sxs-lookup"><span data-stu-id="54266-188">**PathId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="54266-189">Тип данных: **UINT8**</span><span class="sxs-lookup"><span data-stu-id="54266-189">Data type: **UINT8**</span></span>
</dt> <dt>

<span data-ttu-id="54266-190">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="54266-190">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="54266-191">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="54266-191">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="54266-192">ИДЕНТИФИКАТОР пути к адресу SCSI.</span><span class="sxs-lookup"><span data-stu-id="54266-192">The SCSI address path ID.</span></span>

</dd> <dt>

<span data-ttu-id="54266-193">**пнпдевицепас**</span><span class="sxs-lookup"><span data-stu-id="54266-193">**PnpDevicePath**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="54266-194">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="54266-194">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="54266-195">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="54266-195">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="54266-196">Путь к устройству PNP.</span><span class="sxs-lookup"><span data-stu-id="54266-196">The PNP device path.</span></span>

<span data-ttu-id="54266-197">**Windows 8.1:** Это значение не поддерживается до Windows 8.1 и Windows Server 2012 R2.</span><span class="sxs-lookup"><span data-stu-id="54266-197">**Windows 8.1:** This value is not supported until Windows 8.1 and Windows Server 2012 R2.</span></span>

</dd> <dt>

<span data-ttu-id="54266-198">**PortNumber**</span><span class="sxs-lookup"><span data-stu-id="54266-198">**PortNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="54266-199">Тип данных: **UINT8**</span><span class="sxs-lookup"><span data-stu-id="54266-199">Data type: **UINT8**</span></span>
</dt> <dt>

<span data-ttu-id="54266-200">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="54266-200">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="54266-201">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="54266-201">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="54266-202">Номер порта для адреса SCSI.</span><span class="sxs-lookup"><span data-stu-id="54266-202">The SCSI address port number.</span></span>

</dd> <dt>

<span data-ttu-id="54266-203">**примаристатус**</span><span class="sxs-lookup"><span data-stu-id="54266-203">**PrimaryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="54266-204">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="54266-204">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="54266-205">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="54266-205">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="54266-206">Предоставляет сведения о состоянии высокого уровня.</span><span class="sxs-lookup"><span data-stu-id="54266-206">Provides high level status information.</span></span> <span data-ttu-id="54266-207">Это свойство следует использовать вместе со свойством **детаиледстатус** , чтобы обеспечить высокий уровень и подробные сведения о состоянии работоспособности элемента и его подкомпонентов.</span><span class="sxs-lookup"><span data-stu-id="54266-207">This property should be used in conjunction with the **DetailedStatus** property to provide high level and detailed health status of the element and its subcomponents.</span></span> <span data-ttu-id="54266-208">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)и всегда имеет значение **null**.</span><span class="sxs-lookup"><span data-stu-id="54266-208">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="54266-209">**Состояние**</span><span class="sxs-lookup"><span data-stu-id="54266-209">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="54266-210">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="54266-210">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="54266-211">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="54266-211">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="54266-212">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)и всегда имеет значение "ОК".</span><span class="sxs-lookup"><span data-stu-id="54266-212">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and it is always set to "OK".</span></span>

</dd> <dt>

<span data-ttu-id="54266-213">**статусдескриптионс**</span><span class="sxs-lookup"><span data-stu-id="54266-213">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="54266-214">Тип данных: массив **строк**</span><span class="sxs-lookup"><span data-stu-id="54266-214">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="54266-215">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="54266-215">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="54266-216">Строки, описывающие различные значения массива **OperationalStatus** .</span><span class="sxs-lookup"><span data-stu-id="54266-216">Strings that describe the various **OperationalStatus** array values.</span></span> <span data-ttu-id="54266-217">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), и каждый элемент массива всегда имеет значение "ОК".</span><span class="sxs-lookup"><span data-stu-id="54266-217">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and each array element is always set to "OK".</span></span>

</dd> <dt>

<span data-ttu-id="54266-218">**TargetId**</span><span class="sxs-lookup"><span data-stu-id="54266-218">**TargetId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="54266-219">Тип данных: **UINT8**</span><span class="sxs-lookup"><span data-stu-id="54266-219">Data type: **UINT8**</span></span>
</dt> <dt>

<span data-ttu-id="54266-220">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="54266-220">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="54266-221">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="54266-221">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="54266-222">Идентификатор целевого объекта SCSI Address.</span><span class="sxs-lookup"><span data-stu-id="54266-222">The SCSI address target ID.</span></span>

</dd> <dt>

<span data-ttu-id="54266-223">**Тип**</span><span class="sxs-lookup"><span data-stu-id="54266-223">**Type**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="54266-224">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="54266-224">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="54266-225">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="54266-225">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="54266-226">Тип подключенного образа хранилища.</span><span class="sxs-lookup"><span data-stu-id="54266-226">The type of storage image mounted.</span></span>

<dt>

<span id="Virtual_Hard_Disk"></span><span id="virtual_hard_disk"></span><span id="VIRTUAL_HARD_DISK"></span>

<span data-ttu-id="54266-227">**Виртуальный жесткий диск** (0)</span><span class="sxs-lookup"><span data-stu-id="54266-227">**Virtual Hard Disk** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="ISO_Image"></span><span id="iso_image"></span><span id="ISO_IMAGE"></span>

<span data-ttu-id="54266-228">**ISO-образ** (1)</span><span class="sxs-lookup"><span data-stu-id="54266-228">**ISO Image** (1)</span></span>


<span data-ttu-id="54266-229"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="54266-229"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="remarks"></a><span data-ttu-id="54266-230">Комментарии</span><span class="sxs-lookup"><span data-stu-id="54266-230">Remarks</span></span>

<span data-ttu-id="54266-231">Доступ к классу **\_ маунтедсторажеимаже мсвм** может быть ограничен фильтром контроля учетных записей.</span><span class="sxs-lookup"><span data-stu-id="54266-231">Access to the **Msvm\_MountedStorageImage** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="54266-232">Дополнительные сведения см. в разделе [Управление учетными записями пользователей и инструментарий WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="54266-232">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="54266-233">Требования</span><span class="sxs-lookup"><span data-stu-id="54266-233">Requirements</span></span>



| <span data-ttu-id="54266-234">Требование</span><span class="sxs-lookup"><span data-stu-id="54266-234">Requirement</span></span> | <span data-ttu-id="54266-235">Значение</span><span class="sxs-lookup"><span data-stu-id="54266-235">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="54266-236">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="54266-236">Minimum supported client</span></span><br/> | <span data-ttu-id="54266-237">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="54266-237">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="54266-238">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="54266-238">Minimum supported server</span></span><br/> | <span data-ttu-id="54266-239">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="54266-239">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="54266-240">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="54266-240">Namespace</span></span><br/>                | <span data-ttu-id="54266-241">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="54266-241">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="54266-242">MOF</span><span class="sxs-lookup"><span data-stu-id="54266-242">MOF</span></span><br/>                      | <dl> <span data-ttu-id="54266-243"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="54266-243"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="54266-244">DLL</span><span class="sxs-lookup"><span data-stu-id="54266-244">DLL</span></span><br/>                      | <dl> <span data-ttu-id="54266-245"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="54266-245"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="54266-246">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="54266-246">See also</span></span>

<dl> <dt>

[<span data-ttu-id="54266-247">**\_ЛОГИКАЛЕЛЕМЕНТ CIM**</span><span class="sxs-lookup"><span data-stu-id="54266-247">**CIM\_LogicalElement**</span></span>](cim-logicalelement.md)
</dt> <dt>

[<span data-ttu-id="54266-248">**\_ЛОГИКАЛЕЛЕМЕНТ CIM**</span><span class="sxs-lookup"><span data-stu-id="54266-248">**CIM\_LogicalElement**</span></span>](/windows/desktop/CIMWin32Prov/cim-logicalelement)
</dt> <dt>

[<span data-ttu-id="54266-249">Классы хранения</span><span class="sxs-lookup"><span data-stu-id="54266-249">Storage Classes</span></span>](storage-classes.md)
</dt> </dl>

 

