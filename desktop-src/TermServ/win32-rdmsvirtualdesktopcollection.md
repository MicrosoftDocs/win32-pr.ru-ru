---
title: Класс Win32_RDMSVirtualDesktopCollection
description: Создает коллекцию виртуальных рабочих столов и управляет ею.
ms.assetid: fe0a484e-f9e3-4b99-8e69-da8f337ae957
ms.tgt_platform: multiple
keywords:
- Класс Win32_RDMSVirtualDesktopCollection службы удаленных рабочих столов
- Службы удаленных рабочих столов класса Win32_RDMSVirtualDesktopCollection, описание
topic_type:
- apiref
api_name:
- Win32_RDMSVirtualDesktopCollection
- Win32_RDMSVirtualDesktopCollection.Alias
- Win32_RDMSVirtualDesktopCollection.Type
- Win32_RDMSVirtualDesktopCollection.IsManaged
- Win32_RDMSVirtualDesktopCollection.Name
- Win32_RDMSVirtualDesktopCollection.CollectionDescription
- Win32_RDMSVirtualDesktopCollection.SecurityDescriptor
- Win32_RDMSVirtualDesktopCollection.VmFarmSettings
- Win32_RDMSVirtualDesktopCollection.UserVHDSetting
- Win32_RDMSVirtualDesktopCollection.IconContents
- Win32_RDMSVirtualDesktopCollection.ShowInPortal
- Win32_RDMSVirtualDesktopCollection.IsHA
- Win32_RDMSVirtualDesktopCollection.IsUserAdmin
- Win32_RDMSVirtualDesktopCollection.RollbackEnabled
api_location:
- RDMS.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5a6da0c13b6ab223afc7afe6e92039a5388c6204
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105672613"
---
# <a name="win32_rdmsvirtualdesktopcollection-class"></a><span data-ttu-id="3a75c-105">\_Класс Win32 рдмсвиртуалдесктопколлектион</span><span class="sxs-lookup"><span data-stu-id="3a75c-105">Win32\_RDMSVirtualDesktopCollection class</span></span>

<span data-ttu-id="3a75c-106">Создает коллекцию виртуальных рабочих столов и управляет ею.</span><span class="sxs-lookup"><span data-stu-id="3a75c-106">Creates and manages a virtual desktop collection.</span></span>

<span data-ttu-id="3a75c-107">Следующий пример синтаксиса — упрощенный MOF-код, который включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="3a75c-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="3a75c-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="3a75c-108">Syntax</span></span>

``` syntax
[dynamic, provider("Win32_RDManagement_Prov"), AMENDMENT]
class Win32_RDMSVirtualDesktopCollection
{
  string  Alias;
  uint32  Type;
  boolean IsManaged;
  string  Name;
  string  CollectionDescription;
  string  SecurityDescriptor;
  string  VmFarmSettings;
  string  UserVHDSetting;
  uint8   IconContents[];
  boolean ShowInPortal;
  boolean IsHA;
  boolean IsUserAdmin;
  boolean RollbackEnabled;
};
```

## <a name="members"></a><span data-ttu-id="3a75c-109">Члены</span><span class="sxs-lookup"><span data-stu-id="3a75c-109">Members</span></span>

<span data-ttu-id="3a75c-110">Класс **Win32 \_ рдмсвиртуалдесктопколлектион** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="3a75c-110">The **Win32\_RDMSVirtualDesktopCollection** class has these types of members:</span></span>

-   [<span data-ttu-id="3a75c-111">Методы</span><span class="sxs-lookup"><span data-stu-id="3a75c-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="3a75c-112">Свойства</span><span class="sxs-lookup"><span data-stu-id="3a75c-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="3a75c-113">Методы</span><span class="sxs-lookup"><span data-stu-id="3a75c-113">Methods</span></span>

<span data-ttu-id="3a75c-114">Класс **Win32 \_ рдмсвиртуалдесктопколлектион** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="3a75c-114">The **Win32\_RDMSVirtualDesktopCollection** class has these methods.</span></span>



| <span data-ttu-id="3a75c-115">Метод</span><span class="sxs-lookup"><span data-stu-id="3a75c-115">Method</span></span>                                                                                            | <span data-ttu-id="3a75c-116">Описание</span><span class="sxs-lookup"><span data-stu-id="3a75c-116">Description</span></span>                                                                                                                                     |
|:--------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="3a75c-117">**аддвиртуалдесктоп**</span><span class="sxs-lookup"><span data-stu-id="3a75c-117">**AddVirtualDesktop**</span></span>](addvirtualdesktop-win32-rdmsvirtualdesktopcollection.md)                 | <span data-ttu-id="3a75c-118">Добавляет виртуальный рабочий стол в коллекцию виртуальных рабочих столов.</span><span class="sxs-lookup"><span data-stu-id="3a75c-118">Adds a virtual desktop to a virtual desktop collection.</span></span><br/>                                                                              |
| [<span data-ttu-id="3a75c-119">**канцелпатч**</span><span class="sxs-lookup"><span data-stu-id="3a75c-119">**CancelPatch**</span></span>](cancelpatch-win32-rdmsvirtualdesktopcollection.md)                             | <span data-ttu-id="3a75c-120">Отменяет задание подготовки обновлений программного обеспечения для виртуальных машин в коллекции виртуальных рабочих столов.</span><span class="sxs-lookup"><span data-stu-id="3a75c-120">Cancels a software update provisioning job for the virtual machines in a virtual desktop collection.</span></span><br/>                                 |
| [<span data-ttu-id="3a75c-121">**GetInt32Property**</span><span class="sxs-lookup"><span data-stu-id="3a75c-121">**GetInt32Property**</span></span>](getint32property-win32-rdmsvirtualdesktopcollection.md)                   | <span data-ttu-id="3a75c-122">Извлекает значение целочисленного свойства из коллекции виртуальных рабочих столов.</span><span class="sxs-lookup"><span data-stu-id="3a75c-122">Retrieves an integer property value from a virtual desktop collection.</span></span><br/>                                                               |
| [<span data-ttu-id="3a75c-123">**жетпатчпропертиес**</span><span class="sxs-lookup"><span data-stu-id="3a75c-123">**GetPatchProperties**</span></span>](getpatchproperties-win32-rdmsvirtualdesktopcollection.md)               | <span data-ttu-id="3a75c-124">Извлекает свойства задания подготовки обновлений программного обеспечения для виртуальных машин в коллекции виртуальных рабочих столов.</span><span class="sxs-lookup"><span data-stu-id="3a75c-124">Retrieves the properties of a software update provisioning job for the virtual machines in a virtual desktop collection.</span></span><br/>             |
| [<span data-ttu-id="3a75c-125">**жетстрингпроперти**</span><span class="sxs-lookup"><span data-stu-id="3a75c-125">**GetStringProperty**</span></span>](getstringproperty-win32-rdmsvirtualdesktopcollection.md)                 | <span data-ttu-id="3a75c-126">Извлекает значение свойства строки из коллекции виртуальных рабочих столов.</span><span class="sxs-lookup"><span data-stu-id="3a75c-126">Retrieves a string property value from a virtual desktop collection.</span></span><br/>                                                                 |
| [<span data-ttu-id="3a75c-127">**провисионинженумератежобс**</span><span class="sxs-lookup"><span data-stu-id="3a75c-127">**ProvisioningEnumerateJobs**</span></span>](provisioningenumeratejobs-win32-rdmsvirtualdesktopcollection.md) | <span data-ttu-id="3a75c-128">Перечисляет задания подготовки виртуальных рабочих столов для этой службы.</span><span class="sxs-lookup"><span data-stu-id="3a75c-128">Enumerates virtual desktop provisioning jobs for this service.</span></span><br/>                                                                       |
| [<span data-ttu-id="3a75c-129">**провисионингжобканцел**</span><span class="sxs-lookup"><span data-stu-id="3a75c-129">**ProvisioningJobCancel**</span></span>](provisioningjobcancel-win32-rdmsvirtualdesktopcollection.md)         | <span data-ttu-id="3a75c-130">Отмена задания подготовки виртуальных рабочих столов.</span><span class="sxs-lookup"><span data-stu-id="3a75c-130">Cancels a virtual desktop provisioning job.</span></span><br/>                                                                                          |
| [<span data-ttu-id="3a75c-131">**провисионингжобексекуте**</span><span class="sxs-lookup"><span data-stu-id="3a75c-131">**ProvisioningJobExecute**</span></span>](provisioningjobexecute-win32-rdmsvirtualdesktopcollection.md)       | <span data-ttu-id="3a75c-132">Запускает задание подготовки виртуальных рабочих столов.</span><span class="sxs-lookup"><span data-stu-id="3a75c-132">Runs a virtual desktop provisioning job.</span></span><br/>                                                                                             |
| [<span data-ttu-id="3a75c-133">**провисионингжобжетрепорт**</span><span class="sxs-lookup"><span data-stu-id="3a75c-133">**ProvisioningJobGetReport**</span></span>](provisioningjobgetreport-win32-rdmsvirtualdesktopcollection.md)   | <span data-ttu-id="3a75c-134">Возвращает отчет о состоянии задания подготовки виртуальных рабочих столов.</span><span class="sxs-lookup"><span data-stu-id="3a75c-134">Gets a report about the status of a virtual desktop provisioning job.</span></span><br/>                                                                |
| [<span data-ttu-id="3a75c-135">**провисионингпрепжоб**</span><span class="sxs-lookup"><span data-stu-id="3a75c-135">**ProvisioningPrepJob**</span></span>](win32-rdmsvirtualdesktopcollection-provisioningprepjob.md)             | <span data-ttu-id="3a75c-136">Создает задание подготовки виртуальных рабочих столов.</span><span class="sxs-lookup"><span data-stu-id="3a75c-136">Creates a virtual desktop provisioning job.</span></span><br/>                                                                                          |
| [<span data-ttu-id="3a75c-137">**ремовевиртуалдесктоп**</span><span class="sxs-lookup"><span data-stu-id="3a75c-137">**RemoveVirtualDesktop**</span></span>](removevirtualdesktop-win32-rdmsvirtualdesktopcollection.md)           | <span data-ttu-id="3a75c-138">Удаляет виртуальный рабочий стол из коллекции виртуальных рабочих столов.</span><span class="sxs-lookup"><span data-stu-id="3a75c-138">Removes a virtual desktop from a virtual desktop collection.</span></span><br/>                                                                         |
| [<span data-ttu-id="3a75c-139">**счедулепатч**</span><span class="sxs-lookup"><span data-stu-id="3a75c-139">**SchedulePatch**</span></span>](schedulepatch-win32-rdmsvirtualdesktopcollection.md)                         | <span data-ttu-id="3a75c-140">Планирует задание подготовки обновлений программного обеспечения, устанавливающее обновления программного обеспечения на виртуальных машинах в коллекции виртуальных рабочих столов.</span><span class="sxs-lookup"><span data-stu-id="3a75c-140">Schedules a software update provisioning job that installs software updates on the virtual machines in a virtual desktop collection.</span></span><br/> |
| [<span data-ttu-id="3a75c-141">**SetInt32Property**</span><span class="sxs-lookup"><span data-stu-id="3a75c-141">**SetInt32Property**</span></span>](setint32property-win32-rdmsvirtualdesktopcollection.md)                   | <span data-ttu-id="3a75c-142">Обновляет значение целочисленного свойства коллекции виртуальных рабочих столов.</span><span class="sxs-lookup"><span data-stu-id="3a75c-142">Updates an integer property value of a virtual desktop collection.</span></span><br/>                                                                   |
| [<span data-ttu-id="3a75c-143">**сетстрингпроперти**</span><span class="sxs-lookup"><span data-stu-id="3a75c-143">**SetStringProperty**</span></span>](setstringproperty-win32-rdmsvirtualdesktopcollection.md)                 | <span data-ttu-id="3a75c-144">Обновляет значение свойства строки коллекции виртуальных рабочих столов.</span><span class="sxs-lookup"><span data-stu-id="3a75c-144">Updates a string property value of a virtual desktop collection.</span></span><br/>                                                                     |



 

### <a name="properties"></a><span data-ttu-id="3a75c-145">Свойства</span><span class="sxs-lookup"><span data-stu-id="3a75c-145">Properties</span></span>

<span data-ttu-id="3a75c-146">Класс **Win32 \_ рдмсвиртуалдесктопколлектион** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="3a75c-146">The **Win32\_RDMSVirtualDesktopCollection** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="3a75c-147">**Псевдоним**</span><span class="sxs-lookup"><span data-stu-id="3a75c-147">**Alias**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a75c-148">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="3a75c-148">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3a75c-149">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="3a75c-149">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="3a75c-150">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="3a75c-150">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="3a75c-151">Возвращает или задает псевдоним коллекции.</span><span class="sxs-lookup"><span data-stu-id="3a75c-151">Gets or sets the alias of the collection</span></span>

</dd> <dt>

<span data-ttu-id="3a75c-152">**коллектиондескриптион**</span><span class="sxs-lookup"><span data-stu-id="3a75c-152">**CollectionDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a75c-153">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="3a75c-153">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3a75c-154">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="3a75c-154">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="3a75c-155">Квалификаторы: [ **необязательно**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="3a75c-155">Qualifiers: [**optional**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="3a75c-156">Возвращает или задает описание коллекции.</span><span class="sxs-lookup"><span data-stu-id="3a75c-156">Gets or sets the description of the collection</span></span>

</dd> <dt>

<span data-ttu-id="3a75c-157">**иконконтентс**</span><span class="sxs-lookup"><span data-stu-id="3a75c-157">**IconContents**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a75c-158">Тип данных: массив **Uint8**</span><span class="sxs-lookup"><span data-stu-id="3a75c-158">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="3a75c-159">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="3a75c-159">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="3a75c-160">Квалификаторы: [ **необязательно**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="3a75c-160">Qualifiers: [**optional**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="3a75c-161">Возвращает или задает массив значений, указывающих значки для коллекции.</span><span class="sxs-lookup"><span data-stu-id="3a75c-161">Gets or sets an array of values that specify icons for the collection.</span></span>

</dd> <dt>

<span data-ttu-id="3a75c-162">**иша**</span><span class="sxs-lookup"><span data-stu-id="3a75c-162">**IsHA**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a75c-163">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="3a75c-163">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="3a75c-164">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="3a75c-164">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="3a75c-165">Возвращает или задает значения, указывающие, содержит ли коллекция виртуальные машины высокой доступности.</span><span class="sxs-lookup"><span data-stu-id="3a75c-165">Gets or sets a values that indicates whether the collection contains highly available VMs.</span></span> <span data-ttu-id="3a75c-166">**Значение true** , если коллекция содержит виртуальные машины высокой доступности; в противном случае — **значение false**.</span><span class="sxs-lookup"><span data-stu-id="3a75c-166">**TRUE** if the collection contains highly available VMs; otherwise, **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="3a75c-167">**IsManaged**</span><span class="sxs-lookup"><span data-stu-id="3a75c-167">**IsManaged**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a75c-168">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="3a75c-168">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="3a75c-169">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="3a75c-169">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="3a75c-170">Возвращает или задает значение, указывающее, является ли коллекция управляемой.</span><span class="sxs-lookup"><span data-stu-id="3a75c-170">Gets or sets a value that indicates whether the collection is managed.</span></span> <span data-ttu-id="3a75c-171">**Значение true** , если коллекция является управляемой; в противном случае — **значение false**.</span><span class="sxs-lookup"><span data-stu-id="3a75c-171">**TRUE** if the collection is managed; otherwise, **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="3a75c-172">**исусерадмин**</span><span class="sxs-lookup"><span data-stu-id="3a75c-172">**IsUserAdmin**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a75c-173">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="3a75c-173">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="3a75c-174">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="3a75c-174">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="3a75c-175">Возвращает или задает значения, указывающие, является ли пользователь администратором виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="3a75c-175">Gets or sets a values that indicates whether a user is an administrator on a VM.</span></span> <span data-ttu-id="3a75c-176">**Значение true** , если пользователь является администратором на виртуальной машине; в противном случае — **значение false**.</span><span class="sxs-lookup"><span data-stu-id="3a75c-176">**TRUE** if the user is an administrator on a VM; otherwise, **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="3a75c-177">**Name**</span><span class="sxs-lookup"><span data-stu-id="3a75c-177">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a75c-178">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="3a75c-178">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3a75c-179">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="3a75c-179">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="3a75c-180">Возвращает или задает имя коллекции.</span><span class="sxs-lookup"><span data-stu-id="3a75c-180">Gets or sets the name of the collection.</span></span>

</dd> <dt>

<span data-ttu-id="3a75c-181">**роллбаккенаблед**</span><span class="sxs-lookup"><span data-stu-id="3a75c-181">**RollbackEnabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a75c-182">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="3a75c-182">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="3a75c-183">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="3a75c-183">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="3a75c-184">Возвращает или задает значения, указывающие, была ли виртуальная машина восстановлена с помощью моментального снимка виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="3a75c-184">Gets or sets a values that indicates whether a VM was rolled with a VM snapshot.</span></span> <span data-ttu-id="3a75c-185">**Значение true** , если виртуальная машина была восстановлена с помощью моментального СНИМКА виртуальной машины. в противном случае — **значение false**.</span><span class="sxs-lookup"><span data-stu-id="3a75c-185">**TRUE** if the VM was rolled with a VM snapshot; otherwise, **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="3a75c-186">**SecurityDescriptor**</span><span class="sxs-lookup"><span data-stu-id="3a75c-186">**SecurityDescriptor**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a75c-187">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="3a75c-187">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3a75c-188">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="3a75c-188">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="3a75c-189">Квалификаторы: [ **необязательно**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="3a75c-189">Qualifiers: [**optional**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="3a75c-190">Возвращает или задает дескриптор безопасности в формате SSDL, который управляет доступом к коллекции.</span><span class="sxs-lookup"><span data-stu-id="3a75c-190">Gets or sets an SSDL formated security descriptor that controls access to the collection.</span></span>

</dd> <dt>

<span data-ttu-id="3a75c-191">**шовинпортал**</span><span class="sxs-lookup"><span data-stu-id="3a75c-191">**ShowInPortal**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a75c-192">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="3a75c-192">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="3a75c-193">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="3a75c-193">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="3a75c-194">Возвращает или задает значения, указывающие, отображается ли коллекция в Веб-доступ служб терминалов (TS Веб-доступ).</span><span class="sxs-lookup"><span data-stu-id="3a75c-194">Gets or sets a values that indicates whether the collection is displayed in Terminal Services Web Access (TS Web Access).</span></span> <span data-ttu-id="3a75c-195">**Значение true** , чтобы отобразить коллекцию в службах терминалов веб-доступ; в противном случае — **значение false**.</span><span class="sxs-lookup"><span data-stu-id="3a75c-195">**TRUE** to display the collection in TS Web Access; otherwise, **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="3a75c-196">**Тип**</span><span class="sxs-lookup"><span data-stu-id="3a75c-196">**Type**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a75c-197">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="3a75c-197">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="3a75c-198">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="3a75c-198">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="3a75c-199">Возвращает или задает значение, указывающее тип сеансов виртуальных машин, размещенных в коллекции.</span><span class="sxs-lookup"><span data-stu-id="3a75c-199">Gets or sets a value that indicates the type of virtual machine sessions hosted by the collection.</span></span>

<span data-ttu-id="3a75c-200">Это свойство содержит одно из следующих значений:</span><span class="sxs-lookup"><span data-stu-id="3a75c-200">This property contains one of the following values:</span></span>

<dt>

<span id="TempVM"></span><span id="tempvm"></span><span id="TEMPVM"></span>

<span data-ttu-id="3a75c-201"><span id="TempVM"></span><span id="tempvm"></span><span id="TEMPVM"></span>**Темпвм** (1)</span><span class="sxs-lookup"><span data-stu-id="3a75c-201"><span id="TempVM"></span><span id="tempvm"></span><span id="TEMPVM"></span>**TempVM** (1)</span></span>


</dt> <dd>

<span data-ttu-id="3a75c-202">Временные виртуальные машины.</span><span class="sxs-lookup"><span data-stu-id="3a75c-202">Temporary virtual machines.</span></span>

</dd> <dt>

<span id="ManualPersonalVM"></span><span id="manualpersonalvm"></span><span id="MANUALPERSONALVM"></span>

<span data-ttu-id="3a75c-203"><span id="ManualPersonalVM"></span><span id="manualpersonalvm"></span><span id="MANUALPERSONALVM"></span>**Мануалперсоналвм** (2)</span><span class="sxs-lookup"><span data-stu-id="3a75c-203"><span id="ManualPersonalVM"></span><span id="manualpersonalvm"></span><span id="MANUALPERSONALVM"></span>**ManualPersonalVM** (2)</span></span>


</dt> <dd>

<span data-ttu-id="3a75c-204">Виртуальные машины, созданные вручную.</span><span class="sxs-lookup"><span data-stu-id="3a75c-204">Manually created virtual machines.</span></span>

</dd> <dt>

<span id="AutoPersonalVM"></span><span id="autopersonalvm"></span><span id="AUTOPERSONALVM"></span>

<span data-ttu-id="3a75c-205"><span id="AutoPersonalVM"></span><span id="autopersonalvm"></span><span id="AUTOPERSONALVM"></span>**Аутоперсоналвм** (3)</span><span class="sxs-lookup"><span data-stu-id="3a75c-205"><span id="AutoPersonalVM"></span><span id="autopersonalvm"></span><span id="AUTOPERSONALVM"></span>**AutoPersonalVM** (3)</span></span>


</dt> <dd>

<span data-ttu-id="3a75c-206">Автоматически создаваемые виртуальные машины.</span><span class="sxs-lookup"><span data-stu-id="3a75c-206">Auto-generated virtual machines.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="3a75c-207">**усервхдсеттинг**</span><span class="sxs-lookup"><span data-stu-id="3a75c-207">**UserVHDSetting**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a75c-208">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="3a75c-208">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3a75c-209">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="3a75c-209">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="3a75c-210">Квалификаторы: [ **необязательно**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="3a75c-210">Qualifiers: [**optional**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="3a75c-211">Возвращает или задает параметр виртуального жесткого диска данных пользователя для коллекции.</span><span class="sxs-lookup"><span data-stu-id="3a75c-211">Gets or sets the user data VHD setting for the collection.</span></span>

</dd> <dt>

<span data-ttu-id="3a75c-212">**вмфармсеттингс**</span><span class="sxs-lookup"><span data-stu-id="3a75c-212">**VmFarmSettings**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a75c-213">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="3a75c-213">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3a75c-214">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="3a75c-214">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="3a75c-215">Квалификаторы: [ **необязательно**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="3a75c-215">Qualifiers: [**optional**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="3a75c-216">Возвращает или задает параметры рабочего стола для виртуальных машин в коллекции.</span><span class="sxs-lookup"><span data-stu-id="3a75c-216">Gets or sets he desktop settings for the virtual machines in the collection.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="3a75c-217">Требования</span><span class="sxs-lookup"><span data-stu-id="3a75c-217">Requirements</span></span>



| <span data-ttu-id="3a75c-218">Требование</span><span class="sxs-lookup"><span data-stu-id="3a75c-218">Requirement</span></span> | <span data-ttu-id="3a75c-219">Значение</span><span class="sxs-lookup"><span data-stu-id="3a75c-219">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="3a75c-220">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="3a75c-220">Minimum supported client</span></span><br/> | <span data-ttu-id="3a75c-221">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="3a75c-221">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="3a75c-222">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="3a75c-222">Minimum supported server</span></span><br/> | <span data-ttu-id="3a75c-223">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="3a75c-223">Windows Server 2012</span></span><br/>                                                              |
| <span data-ttu-id="3a75c-224">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="3a75c-224">Namespace</span></span><br/>                | <span data-ttu-id="3a75c-225">Корневой \\ \\ rdms CIMV2</span><span class="sxs-lookup"><span data-stu-id="3a75c-225">Root\\cimv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="3a75c-226">MOF</span><span class="sxs-lookup"><span data-stu-id="3a75c-226">MOF</span></span><br/>                      | <dl> <span data-ttu-id="3a75c-227"><dt>Рдманажемент. mof</dt></span><span class="sxs-lookup"><span data-stu-id="3a75c-227"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="3a75c-228">DLL</span><span class="sxs-lookup"><span data-stu-id="3a75c-228">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3a75c-229"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3a75c-229"><dt>RDMS.dll</dt></span></span> </dl>         |



## <a name="see-also"></a><span data-ttu-id="3a75c-230">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="3a75c-230">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3a75c-231">Поставщик служб удаленный рабочий стол Management Services</span><span class="sxs-lookup"><span data-stu-id="3a75c-231">Remote Desktop Management Services Provider</span></span>](rdms-api-reference.md)
</dt> </dl>

 

