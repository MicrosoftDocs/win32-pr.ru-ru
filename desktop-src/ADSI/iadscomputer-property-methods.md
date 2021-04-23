---
title: Методы свойств Иадскомпутер (iAds. h)
description: Методы интерфейса Иадскомпутер считывают и записывают свойства, описанные в этом разделе. Дополнительные сведения см. в разделе методы свойств интерфейса.
ms.assetid: c990b6bb-6256-4216-9435-c85c67db4d13
ms.tgt_platform: multiple
keywords:
- Методы свойств Иадскомпутер ADSI
topic_type:
- apiref
api_name:
- IADsComputer Property Methods
- IADsComputer.ComputerID
- IADsComputer.get_ComputerID
- IADsComputer.Department
- IADsComputer.get_Department
- IADsComputer.put_Department
- IADsComputer.Description
- IADsComputer.get_Description
- IADsComputer.put_Description
- IADsComputer.Division
- IADsComputer.get_Division
- IADsComputer.put_Division
- IADsComputer.Location
- IADsComputer.get_Location
- IADsComputer.put_Location
- IADsComputer.MemorySize
- IADsComputer.get_MemorySize
- IADsComputer.put_MemorySize
- IADsComputer.Model
- IADsComputer.get_Model
- IADsComputer.put_Model
- IADsComputer.NetAddresses
- IADsComputer.get_NetAddresses
- IADsComputer.put_NetAddresses
- IADsComputer.OperatingSystem
- IADsComputer.get_OperatingSystem
- IADsComputer.put_OperatingSystem
- IADsComputer.OperatingSystemVersion
- IADsComputer.get_OperatingSystemVersion
- IADsComputer.put_OperatingSystemVersion
- IADsComputer.Owner
- IADsComputer.get_Owner
- IADsComputer.put_Owner
- IADsComputer.PrimaryUser
- IADsComputer.get_PrimaryUser
- IADsComputer.put_PrimaryUser
- IADsComputer.Processor
- IADsComputer.get_Processor
- IADsComputer.put_Processor
- IADsComputer.ProcessorCount
- IADsComputer.get_ProcessorCount
- IADsComputer.put_ProcessorCount
- IADsComputer.Role
- IADsComputer.get_Role
- IADsComputer.put_Role
- IADsComputer.Site
- IADsComputer.get_Site
- IADsComputer.StorageCapacity
- IADsComputer.get_StorageCapacity
- IADsComputer.put_StorageCapacity
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9f2f3c455e2e43436627b62d142781bb6a605bef
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103892369"
---
# <a name="iadscomputer-property-methods"></a><span data-ttu-id="35757-105">Методы свойств Иадскомпутер</span><span class="sxs-lookup"><span data-stu-id="35757-105">IADsComputer Property Methods</span></span>

<span data-ttu-id="35757-106">Методы интерфейса [**иадскомпутер**](/windows/desktop/api/Iads/nn-iads-iadscomputer) считывают и записывают свойства, описанные в этом разделе.</span><span class="sxs-lookup"><span data-stu-id="35757-106">The [**IADsComputer**](/windows/desktop/api/Iads/nn-iads-iadscomputer) interface methods read and write the properties described in this topic.</span></span> <span data-ttu-id="35757-107">Дополнительные сведения см. в разделе [методы свойств интерфейса](interface-property-methods.md).</span><span class="sxs-lookup"><span data-stu-id="35757-107">For more information, see [Interface Property Methods](interface-property-methods.md).</span></span>

## <a name="properties"></a><span data-ttu-id="35757-108">Свойства</span><span class="sxs-lookup"><span data-stu-id="35757-108">Properties</span></span>

<dl> <dt>

<span data-ttu-id="35757-109">**компутерид**</span><span class="sxs-lookup"><span data-stu-id="35757-109">**ComputerID**</span></span>
<span data-ttu-id="35757-110"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="35757-110"></dt> <dd> <dl></span></span>

<span data-ttu-id="35757-111">Глобальный уникальный идентификатор, назначенный каждому компьютеру.</span><span class="sxs-lookup"><span data-stu-id="35757-111">The globally unique identifier assigned to each computer.</span></span>

<dt>

<span data-ttu-id="35757-112">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="35757-112">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="35757-113">Тип данных скрипта: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="35757-113">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_ComputerID(
  [out] BSTR* pbstrComputerID
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="35757-114">**Отдел**</span><span class="sxs-lookup"><span data-stu-id="35757-114">**Department**</span></span>
<span data-ttu-id="35757-115"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="35757-115"></dt> <dd> <dl></span></span>

<span data-ttu-id="35757-116">Подразделение, например отдел, к которому принадлежит этот компьютер.</span><span class="sxs-lookup"><span data-stu-id="35757-116">The organizational unit (OU), such as department, that this computer belongs to.</span></span>

<dt>

<span data-ttu-id="35757-117">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="35757-117">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="35757-118">Тип данных скрипта: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="35757-118">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Department(
  [out] BSTR* pbstrDepartment
);
HRESULT put_Department(
  [in] BSTR bstrDepartment
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="35757-119">**Описание**</span><span class="sxs-lookup"><span data-stu-id="35757-119">**Description**</span></span>
<span data-ttu-id="35757-120"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="35757-120"></dt> <dd> <dl></span></span>

<span data-ttu-id="35757-121">Описание этого компьютера.</span><span class="sxs-lookup"><span data-stu-id="35757-121">The description of this computer.</span></span>

<dt>

<span data-ttu-id="35757-122">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="35757-122">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="35757-123">Тип данных скрипта: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="35757-123">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Description(
  [out] BSTR* pbstrDescription
);
HRESULT put_Description(
  [in] BSTR bstrDescription
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="35757-124">**Отдел**</span><span class="sxs-lookup"><span data-stu-id="35757-124">**Division**</span></span>
<span data-ttu-id="35757-125"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="35757-125"></dt> <dd> <dl></span></span>

<span data-ttu-id="35757-126">Подразделение в пределах организации, к которому принадлежит этот компьютер.</span><span class="sxs-lookup"><span data-stu-id="35757-126">The division, within an organization, that this computer belongs to.</span></span>

<dt>

<span data-ttu-id="35757-127">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="35757-127">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="35757-128">Тип данных скрипта: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="35757-128">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Division(
  [out] BSTR* pbstrDivision
);
HRESULT put_Division(
  [in] BSTR bstrDivision
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="35757-129">**Расположение**</span><span class="sxs-lookup"><span data-stu-id="35757-129">**Location**</span></span>
<span data-ttu-id="35757-130"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="35757-130"></dt> <dd> <dl></span></span>

<span data-ttu-id="35757-131">Назначенное физическое расположение компьютера.</span><span class="sxs-lookup"><span data-stu-id="35757-131">The assigned physical location of this computer.</span></span>

<dt>

<span data-ttu-id="35757-132">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="35757-132">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="35757-133">Тип данных скрипта: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="35757-133">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Location(
  [out] BSTR* pbstrLocation
);
HRESULT put_Location(
  [in] BSTR bstrLocation
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="35757-134">**MemorySize**</span><span class="sxs-lookup"><span data-stu-id="35757-134">**MemorySize**</span></span>
<span data-ttu-id="35757-135"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="35757-135"></dt> <dd> <dl></span></span>

<span data-ttu-id="35757-136">Размер (в мегабайтах) памяти произвольного доступа для этого компьютера.</span><span class="sxs-lookup"><span data-stu-id="35757-136">The size, in megabytes, of random access memory for this computer.</span></span>

<dt>

<span data-ttu-id="35757-137">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="35757-137">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="35757-138">Тип данных скрипта: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="35757-138">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_MemorySize(
  [out] BSTR* pbstrMemorySize
);
HRESULT put_MemorySize(
  [in] BSTR bstrMemorySize
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="35757-139">**Модель**</span><span class="sxs-lookup"><span data-stu-id="35757-139">**Model**</span></span>
<span data-ttu-id="35757-140"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="35757-140"></dt> <dd> <dl></span></span>

<span data-ttu-id="35757-141">Марка и модель этого компьютера.</span><span class="sxs-lookup"><span data-stu-id="35757-141">The make and model of this computer.</span></span>

<dt>

<span data-ttu-id="35757-142">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="35757-142">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="35757-143">Тип данных скрипта: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="35757-143">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Model(
  [out] BSTR* pbstrModel
);
HRESULT put_Model(
  [in] BSTR bstrModel
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="35757-144">**нетаддрессес**</span><span class="sxs-lookup"><span data-stu-id="35757-144">**NetAddresses**</span></span>
<span data-ttu-id="35757-145"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="35757-145"></dt> <dd> <dl></span></span>

<span data-ttu-id="35757-146">Массив полей Нетаддресс, представляющих адреса, по которым может быть достигнут данный компьютер.</span><span class="sxs-lookup"><span data-stu-id="35757-146">An array of NetAddress fields that represent the addresses by which this computer can be reached.</span></span> <span data-ttu-id="35757-147">Нетаддресс — это определяемая поставщиком **BSTR** , состоящая из двух подстрок, разделенных двоеточием (:).</span><span class="sxs-lookup"><span data-stu-id="35757-147">NetAddress is a provider-specific **BSTR** composed of two substrings separated by a colon (:).</span></span> <span data-ttu-id="35757-148">Левая подстрока указывает тип адреса, а правая подстрока — строковое представление адреса этого типа.</span><span class="sxs-lookup"><span data-stu-id="35757-148">The left substring indicates the address type, and the right substring is a string representation of an address of that type.</span></span> <span data-ttu-id="35757-149">Например, TCP/IP-адреса имеют вид: IP: 100.201.301.45.</span><span class="sxs-lookup"><span data-stu-id="35757-149">For example, TCP/IP addresses are of the form: IP:100.201.301.45.</span></span> <span data-ttu-id="35757-150">IPX-адреса типов имеют вид: IPX: 10.123456.80.</span><span class="sxs-lookup"><span data-stu-id="35757-150">IPX type addresses are of the form: IPX:10.123456.80.</span></span>

<dt>

<span data-ttu-id="35757-151">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="35757-151">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="35757-152">Тип данных скрипта: **Variant**</span><span class="sxs-lookup"><span data-stu-id="35757-152">Scripting data type: **VARIANT**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_NetAddresses(
  [out] VARIANT* pvNetAddresses
);
HRESULT put_NetAddresses(
  [in] VARIANT vNetAddresses
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="35757-153">**OperatingSystem**</span><span class="sxs-lookup"><span data-stu-id="35757-153">**OperatingSystem**</span></span>
<span data-ttu-id="35757-154"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="35757-154"></dt> <dd> <dl></span></span>

<span data-ttu-id="35757-155">Операционная система, используемая на этом компьютере.</span><span class="sxs-lookup"><span data-stu-id="35757-155">The operating system used on this computer.</span></span>

<dt>

<span data-ttu-id="35757-156">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="35757-156">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="35757-157">Тип данных скрипта: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="35757-157">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_OperatingSystem(
  [out] BSTR* pbstrOperatingSystem
);
HRESULT put_OperatingSystem(
  [in] BSTR bstrOperatingSystem
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="35757-158">**оператингсистемверсион**</span><span class="sxs-lookup"><span data-stu-id="35757-158">**OperatingSystemVersion**</span></span>
<span data-ttu-id="35757-159"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="35757-159"></dt> <dd> <dl></span></span>

<span data-ttu-id="35757-160">Версия операционной системы, используемой на этом компьютере.</span><span class="sxs-lookup"><span data-stu-id="35757-160">The version of the operating system used on this computer.</span></span>

<dt>

<span data-ttu-id="35757-161">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="35757-161">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="35757-162">Тип данных скрипта: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="35757-162">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_OperatingSystemVersion(
  [out] BSTR* pbstrOperatingSystemVersion
);
HRESULT put_OperatingSystemVersion(
  [in] BSTR bstrOperatingSystemVersion
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="35757-163">**Владелец**</span><span class="sxs-lookup"><span data-stu-id="35757-163">**Owner**</span></span>
<span data-ttu-id="35757-164"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="35757-164"></dt> <dd> <dl></span></span>

<span data-ttu-id="35757-165">Пользователь, которому назначен этот компьютер.</span><span class="sxs-lookup"><span data-stu-id="35757-165">The person to whom this computer is assigned.</span></span> <span data-ttu-id="35757-166">У этого лица также должна быть лицензия для запуска установленного программного обеспечения.</span><span class="sxs-lookup"><span data-stu-id="35757-166">This person should also have a license to run the installed software.</span></span>

<dt>

<span data-ttu-id="35757-167">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="35757-167">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="35757-168">Тип данных скрипта: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="35757-168">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Owner(
  [out] BSTR* pbstrOwner
);
HRESULT put_Owner(
  [in] BSTR bstrOwner
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="35757-169">**PrimaryUser**</span><span class="sxs-lookup"><span data-stu-id="35757-169">**PrimaryUser**</span></span>
<span data-ttu-id="35757-170"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="35757-170"></dt> <dd> <dl></span></span>

<span data-ttu-id="35757-171">Имя контактного лица, например администратора, для данного компьютера.</span><span class="sxs-lookup"><span data-stu-id="35757-171">The name of the contact person, such as an administrator, for this computer.</span></span>

<dt>

<span data-ttu-id="35757-172">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="35757-172">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="35757-173">Тип данных скрипта: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="35757-173">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_PrimaryUser(
  [out] BSTR* pbstrPrimaryUser
);
HRESULT put_PrimaryUser(
  [in] BSTR bstrPrimaryUser
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="35757-174">**Процессор**</span><span class="sxs-lookup"><span data-stu-id="35757-174">**Processor**</span></span>
<span data-ttu-id="35757-175"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="35757-175"></dt> <dd> <dl></span></span>

<span data-ttu-id="35757-176">Тип процессора.</span><span class="sxs-lookup"><span data-stu-id="35757-176">The processor type.</span></span>

<dt>

<span data-ttu-id="35757-177">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="35757-177">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="35757-178">Тип данных скрипта: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="35757-178">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Processor(
  [out] BSTR* pbstrProcessor
);
HRESULT put_Processor(
  [in] BSTR bstrProcessor
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="35757-179">**ProcessorCount**</span><span class="sxs-lookup"><span data-stu-id="35757-179">**ProcessorCount**</span></span>
<span data-ttu-id="35757-180"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="35757-180"></dt> <dd> <dl></span></span>

<span data-ttu-id="35757-181">Число установленных процессоров.</span><span class="sxs-lookup"><span data-stu-id="35757-181">The number of installed processors.</span></span>

<dt>

<span data-ttu-id="35757-182">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="35757-182">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="35757-183">Тип данных скрипта: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="35757-183">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_ProcessorCount(
  [out] BSTR* pbstrProcessorCount
);
HRESULT put_ProcessorCount(
  [in] BSTR bstrProcessorCount
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="35757-184">**Роль**</span><span class="sxs-lookup"><span data-stu-id="35757-184">**Role**</span></span>
<span data-ttu-id="35757-185"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="35757-185"></dt> <dd> <dl></span></span>

<span data-ttu-id="35757-186">Роль этого компьютера, например рабочая станция, сервер или контроллер домена.</span><span class="sxs-lookup"><span data-stu-id="35757-186">The role of this computer, for example, workstation, server, or domain controller.</span></span>

<dt>

<span data-ttu-id="35757-187">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="35757-187">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="35757-188">Тип данных скрипта: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="35757-188">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Role(
  [out] BSTR* pbstrRole
);
HRESULT put_Role(
  [in] BSTR bstrRole
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="35757-189">**Сайт**</span><span class="sxs-lookup"><span data-stu-id="35757-189">**Site**</span></span>
<span data-ttu-id="35757-190"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="35757-190"></dt> <dd> <dl></span></span>

<span data-ttu-id="35757-191">Глобальный уникальный идентификатор, определяющий сайт, в котором был установлен этот компьютер.</span><span class="sxs-lookup"><span data-stu-id="35757-191">The globally unique identifier that identifies the site that this computer was installed in.</span></span> <span data-ttu-id="35757-192">Сайт — это физическая область хорошего подключения в сети.</span><span class="sxs-lookup"><span data-stu-id="35757-192">A site is a physical region of good connectivity in a network.</span></span>

<dt>

<span data-ttu-id="35757-193">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="35757-193">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="35757-194">Тип данных скрипта: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="35757-194">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Site(
  [out] BSTR* pbstrSite
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="35757-195">**сторажекапаЦити**</span><span class="sxs-lookup"><span data-stu-id="35757-195">**StorageCapacity**</span></span>
<span data-ttu-id="35757-196"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="35757-196"></dt> <dd> <dl></span></span>

<span data-ttu-id="35757-197">Размер диска (в мегабайтах).</span><span class="sxs-lookup"><span data-stu-id="35757-197">The size, in megabytes, of the disk.</span></span>

<dt>

<span data-ttu-id="35757-198">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="35757-198">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="35757-199">Тип данных скрипта: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="35757-199">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_StorageCapacity(
  [out] BSTR* pbstrStorageCapacity
);
HRESULT put_StorageCapacity(
  [in] BSTR bstrStorageCapacity
);
```


</dt> </dl> </dd> </dl>

 

## <a name="remarks"></a><span data-ttu-id="35757-200">Комментарии</span><span class="sxs-lookup"><span data-stu-id="35757-200">Remarks</span></span>

<span data-ttu-id="35757-201">Различные поставщики могут предоставлять различные свойства объекта Computer.</span><span class="sxs-lookup"><span data-stu-id="35757-201">Different providers may choose to expose different properties of a computer object.</span></span> <span data-ttu-id="35757-202">Дополнительные сведения см. в разделе [поставщики систем ADSI](adsi-system-providers.md).</span><span class="sxs-lookup"><span data-stu-id="35757-202">For more information, see [ADSI System Providers](adsi-system-providers.md).</span></span>

<span data-ttu-id="35757-203">Чтобы узнать, какие свойства поддерживаются, можно проверить обязательные и необязательные свойства с помощью класса схемы.</span><span class="sxs-lookup"><span data-stu-id="35757-203">You can discover what properties are supported by inspecting the mandatory and optional properties through its schema class.</span></span> <span data-ttu-id="35757-204">Дополнительные сведения см. в описании интерфейса [**иадскласс**](/windows/desktop/api/Iads/nn-iads-iadsclass) .</span><span class="sxs-lookup"><span data-stu-id="35757-204">For more information, see the [**IADsClass**](/windows/desktop/api/Iads/nn-iads-iadsclass) interface.</span></span>

<span data-ttu-id="35757-205">Чтобы проверить состояние компьютера или выполнить операцию завершения работы по сети, необходимо использовать интерфейс [**иадскомпутероператионс**](/windows/desktop/api/Iads/nn-iads-iadscomputeroperations) .</span><span class="sxs-lookup"><span data-stu-id="35757-205">To examine the status of a computer or to perform the shutdown operation across the network, you must use the [**IADsComputerOperations**](/windows/desktop/api/Iads/nn-iads-iadscomputeroperations) interface.</span></span>

## <a name="examples"></a><span data-ttu-id="35757-206">Примеры</span><span class="sxs-lookup"><span data-stu-id="35757-206">Examples</span></span>

<span data-ttu-id="35757-207">В следующем примере кода Visual Basic изучаются свойства компьютера, поддерживаемые поставщиком ADSI WinNT.</span><span class="sxs-lookup"><span data-stu-id="35757-207">The following Visual Basic code example examines computer properties supported by the ADSI WinNT provider.</span></span>


```VB
Dim obj As IADs
On Error Resume Next

Set obj = GetObject("WinNT://myMachine,computer")
If (obj.Class = "Computer") Then
    MsgBox "Computer owner: " & obj.owner
    MsgBox "Computer division: " & obj.Division
    MsgBox "Computer operatingSystem: " & obj.OperatingSystem
    MsgBox "Computer operating System Version: " & obj.OperatingSystemVersion
    MsgBox "Computer processor: " & obj.Processor
    MsgBox "Computer processor Count: " & obj.ProcessorCount
End If
```



<span data-ttu-id="35757-208">В следующем примере кода C++ изучаются свойства компьютера, поддерживаемые поставщиком ADSI WinNT.</span><span class="sxs-lookup"><span data-stu-id="35757-208">The following C++ code example examines computer properties supported by the ADSI WinNT provider.</span></span>


```C++
IADsComputer *pComp = NULL;
LPWSTR adspath = L"WinNT://jeffsmith1,computer";
HRESULT hr = S_OK;
BSTR bstr = NULL;

hr = ADsGetObject(adspath,IID_IADsComputer,(void**)&pComp);
if(FAILED(hr)) {goto Cleanup;}

hr = pComp->get_Owner(&bstr);
if(FAILED(hr)) {goto Cleanup;}

printf("Computer owner: %S\n",bstr);
SysFreeString(bstr);

hr = pComp->get_OperatingSystem(&bstr);
if(FAILED(hr)) {goto Cleanup;}
printf("Operating System: %S\n",bstr);
SysFreeString(bstr);

Cleanup:
    if(pComp) pComp->Release();
    if(bstr) SysFreeString(bstr);
    return hr;
```



## <a name="requirements"></a><span data-ttu-id="35757-209">Требования</span><span class="sxs-lookup"><span data-stu-id="35757-209">Requirements</span></span>



| <span data-ttu-id="35757-210">Требование</span><span class="sxs-lookup"><span data-stu-id="35757-210">Requirement</span></span> | <span data-ttu-id="35757-211">Значение</span><span class="sxs-lookup"><span data-stu-id="35757-211">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="35757-212">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="35757-212">Minimum supported client</span></span><br/> | <span data-ttu-id="35757-213">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="35757-213">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="35757-214">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="35757-214">Minimum supported server</span></span><br/> | <span data-ttu-id="35757-215">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="35757-215">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="35757-216">Header</span><span class="sxs-lookup"><span data-stu-id="35757-216">Header</span></span><br/>                   | <dl> <span data-ttu-id="35757-217"><dt>IAds. h</dt></span><span class="sxs-lookup"><span data-stu-id="35757-217"><dt>Iads.h</dt></span></span> </dl>       |
| <span data-ttu-id="35757-218">DLL</span><span class="sxs-lookup"><span data-stu-id="35757-218">DLL</span></span><br/>                      | <dl> <span data-ttu-id="35757-219"><dt>Activeds.dll</dt></span><span class="sxs-lookup"><span data-stu-id="35757-219"><dt>Activeds.dll</dt></span></span> </dl> |
| <span data-ttu-id="35757-220">IID</span><span class="sxs-lookup"><span data-stu-id="35757-220">IID</span></span><br/>                      | <span data-ttu-id="35757-221">IID \_ иадскомпутер определен как EFE3CC70-1D9F-11CF-B1F3-02608C9E7553</span><span class="sxs-lookup"><span data-stu-id="35757-221">IID\_IADsComputer is defined as EFE3CC70-1D9F-11CF-B1F3-02608C9E7553</span></span><br/>         |



## <a name="see-also"></a><span data-ttu-id="35757-222">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="35757-222">See also</span></span>

<dl> <dt>

[<span data-ttu-id="35757-223">**иадскомпутер**</span><span class="sxs-lookup"><span data-stu-id="35757-223">**IADsComputer**</span></span>](/windows/desktop/api/Iads/nn-iads-iadscomputer)
</dt> <dt>

[<span data-ttu-id="35757-224">Поставщики систем ADSI</span><span class="sxs-lookup"><span data-stu-id="35757-224">ADSI System Providers</span></span>](adsi-system-providers.md)
</dt> <dt>

[<span data-ttu-id="35757-225">**иадскласс**</span><span class="sxs-lookup"><span data-stu-id="35757-225">**IADsClass**</span></span>](/windows/desktop/api/Iads/nn-iads-iadsclass)
</dt> <dt>

[<span data-ttu-id="35757-226">**иадскомпутероператионс**</span><span class="sxs-lookup"><span data-stu-id="35757-226">**IADsComputerOperations**</span></span>](/windows/desktop/api/Iads/nn-iads-iadscomputeroperations)
</dt> <dt>

[<span data-ttu-id="35757-227">Методы свойств интерфейса</span><span class="sxs-lookup"><span data-stu-id="35757-227">Interface Property Methods</span></span>](interface-property-methods.md)
</dt> </dl>

 

 





