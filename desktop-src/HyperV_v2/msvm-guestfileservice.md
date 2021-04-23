---
description: Мсвм \_ гуестфилесервице содержит метод, который можно использовать для копирования файла на виртуальную машину с узла Hyper-V.
ms.assetid: 3599d5a8-415f-48f8-b887-00a93b7abb83
title: Класс Msvm_GuestFileService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_GuestFileService
- Msvm_GuestFileService.StartService
- Msvm_GuestFileService.StopService
- Msvm_GuestFileService.Caption
- Msvm_GuestFileService.CreationClassName
- Msvm_GuestFileService.Description
- Msvm_GuestFileService.InstallDate
- Msvm_GuestFileService.Name
- Msvm_GuestFileService.Started
- Msvm_GuestFileService.StartMode
- Msvm_GuestFileService.Status
- Msvm_GuestFileService.SystemCreationClassName
- Msvm_GuestFileService.SystemName
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 0ee0f235d7549428ecf02e9c758c83bcea33efe3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105662242"
---
# <a name="msvm_guestfileservice-class"></a><span data-ttu-id="c8996-103">\_Класс мсвм гуестфилесервице</span><span class="sxs-lookup"><span data-stu-id="c8996-103">Msvm\_GuestFileService class</span></span>

<span data-ttu-id="c8996-104">**Мсвм \_ Гуестфилесервице** содержит метод, который можно использовать для копирования файла на виртуальную машину с узла Hyper-V.</span><span class="sxs-lookup"><span data-stu-id="c8996-104">**Msvm\_GuestFileService** contains a method that can be used to copy a file to a virtual machine from the Hyper-V host.</span></span> <span data-ttu-id="c8996-105">Этот класс является производным от [**мсвм \_ гуестсервице**](msvm-guestservice.md).</span><span class="sxs-lookup"><span data-stu-id="c8996-105">This class derives from [**Msvm\_GuestService**](msvm-guestservice.md).</span></span>

<span data-ttu-id="c8996-106">Следующий синтаксис упрощен из MOF-кода и включает все унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="c8996-106">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="c8996-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c8996-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_GuestFileService : Msvm_GuestService
{
  string   Caption;
  string   CreationClassName;
  string   Description;
  datetime InstallDate;
  string   Name;
  boolean  Started;
  string   StartMode;
  string   Status;
  string   SystemCreationClassName;
  string   SystemName;
};
```

## <a name="members"></a><span data-ttu-id="c8996-108">Члены</span><span class="sxs-lookup"><span data-stu-id="c8996-108">Members</span></span>

<span data-ttu-id="c8996-109">Класс **мсвм \_ гуестфилесервице** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="c8996-109">The **Msvm\_GuestFileService** class has these types of members:</span></span>

-   [<span data-ttu-id="c8996-110">Методы</span><span class="sxs-lookup"><span data-stu-id="c8996-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="c8996-111">Свойства</span><span class="sxs-lookup"><span data-stu-id="c8996-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="c8996-112">Методы</span><span class="sxs-lookup"><span data-stu-id="c8996-112">Methods</span></span>

<span data-ttu-id="c8996-113">Класс **мсвм \_ гуестфилесервице** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="c8996-113">The **Msvm\_GuestFileService** class has these methods.</span></span>



| <span data-ttu-id="c8996-114">Метод</span><span class="sxs-lookup"><span data-stu-id="c8996-114">Method</span></span>                                                             | <span data-ttu-id="c8996-115">Описание</span><span class="sxs-lookup"><span data-stu-id="c8996-115">Description</span></span>                                                                                                                                                                  |
|:-------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="c8996-116">**копифилестогуест**</span><span class="sxs-lookup"><span data-stu-id="c8996-116">**CopyFilesToGuest**</span></span>](copyfilestoguest-msvm-guestfileservice.md) | <span data-ttu-id="c8996-117">Копирует файлы с узла Hyper-V на виртуальную машину.</span><span class="sxs-lookup"><span data-stu-id="c8996-117">Copies files from the Hyper-V host to the virtual machine.</span></span><br/> <span data-ttu-id="c8996-118">**Windows 8.1:** Этот метод не поддерживается до Windows 8.1 и Windows Server 2012 R2.</span><span class="sxs-lookup"><span data-stu-id="c8996-118">**Windows 8.1:** This method is not supported until Windows 8.1 and Windows Server 2012 R2.</span></span><br/> |
| <span data-ttu-id="c8996-119">**StartService**</span><span class="sxs-lookup"><span data-stu-id="c8996-119">**StartService**</span></span>                                                   | <span data-ttu-id="c8996-120">Этот метод не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="c8996-120">This method is not supported.</span></span><br/>                                                                                                                                     |
| <span data-ttu-id="c8996-121">**StopService**</span><span class="sxs-lookup"><span data-stu-id="c8996-121">**StopService**</span></span>                                                    | <span data-ttu-id="c8996-122">Этот метод не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="c8996-122">This method is not supported.</span></span><br/>                                                                                                                                     |



 

### <a name="properties"></a><span data-ttu-id="c8996-123">Свойства</span><span class="sxs-lookup"><span data-stu-id="c8996-123">Properties</span></span>

<span data-ttu-id="c8996-124">Класс **мсвм \_ гуестфилесервице** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="c8996-124">The **Msvm\_GuestFileService** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="c8996-125">**Заголовок**</span><span class="sxs-lookup"><span data-stu-id="c8996-125">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c8996-126">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="c8996-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c8996-127">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c8996-127">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c8996-128">Краткое текстовое описание объекта.</span><span class="sxs-lookup"><span data-stu-id="c8996-128">Short textual description of the object.</span></span> <span data-ttu-id="c8996-129">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="c8996-129">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="c8996-130">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="c8996-130">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c8996-131">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="c8996-131">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c8996-132">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c8996-132">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c8996-133">Имя класса или подкласса, используемого при создании экземпляра.</span><span class="sxs-lookup"><span data-stu-id="c8996-133">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="c8996-134">При использовании с другими ключевыми свойствами класса это свойство позволяет однозначно идентифицировать все экземпляры класса и его подклассов.</span><span class="sxs-lookup"><span data-stu-id="c8996-134">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

</dd> <dt>

<span data-ttu-id="c8996-135">**Описание**</span><span class="sxs-lookup"><span data-stu-id="c8996-135">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c8996-136">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="c8996-136">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c8996-137">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c8996-137">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c8996-138">Текстовое описание объекта.</span><span class="sxs-lookup"><span data-stu-id="c8996-138">Textual description of the object.</span></span> <span data-ttu-id="c8996-139">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="c8996-139">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="c8996-140">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="c8996-140">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c8996-141">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="c8996-141">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="c8996-142">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c8996-142">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c8996-143">Дата и время установки объекта.</span><span class="sxs-lookup"><span data-stu-id="c8996-143">Date and time the object was installed.</span></span> <span data-ttu-id="c8996-144">Для этого свойства не требуется значение, указывающее, что объект установлен.</span><span class="sxs-lookup"><span data-stu-id="c8996-144">This property does not need a value to indicate that the object is installed.</span></span> <span data-ttu-id="c8996-145">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="c8996-145">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="c8996-146">**Name**</span><span class="sxs-lookup"><span data-stu-id="c8996-146">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c8996-147">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="c8996-147">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c8996-148">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c8996-148">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c8996-149">Уникальный идентификатор службы, который также содержит сведения об управляемых функциях.</span><span class="sxs-lookup"><span data-stu-id="c8996-149">Unique identifier for the service that also provides an indication of the functionality that is managed.</span></span> <span data-ttu-id="c8996-150">Дополнительные сведения о функциональных возможностях см. в описании свойства объекта **Description** .</span><span class="sxs-lookup"><span data-stu-id="c8996-150">For more information about the functionality, see the object's **Description** property.</span></span> <span data-ttu-id="c8996-151">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="c8996-151">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="c8996-152">**Запуск**</span><span class="sxs-lookup"><span data-stu-id="c8996-152">**Started**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c8996-153">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="c8996-153">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="c8996-154">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c8996-154">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c8996-155">Если **значение равно true**, служба запущена.</span><span class="sxs-lookup"><span data-stu-id="c8996-155">If **TRUE**, the service has started.</span></span>

</dd> <dt>

<span data-ttu-id="c8996-156">**StartMode**</span><span class="sxs-lookup"><span data-stu-id="c8996-156">**StartMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c8996-157">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="c8996-157">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c8996-158">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c8996-158">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c8996-159">Указывает, запускается ли служба автоматически (например, операционная система) или только после запроса.</span><span class="sxs-lookup"><span data-stu-id="c8996-159">Indicates whether the service is automatically started (for example, by an operating system) or only started upon request.</span></span>

<span data-ttu-id="c8996-160">В эти значения входят:</span><span class="sxs-lookup"><span data-stu-id="c8996-160">Values include the following:</span></span>

<dl><span id="Automatic"></span><span id="automatic"></span><span id="AUTOMATIC"></span><dt>

<span data-ttu-id="c8996-161">**Автоматическое**</span><span class="sxs-lookup"><span data-stu-id="c8996-161">**"Automatic"**</span></span>
</dt><span id="Manual"></span><span id="manual"></span><span id="MANUAL"></span><dt>

<span data-ttu-id="c8996-162">**Документации**</span><span class="sxs-lookup"><span data-stu-id="c8996-162">**"Manual"**</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="c8996-163">**Состояние**</span><span class="sxs-lookup"><span data-stu-id="c8996-163">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c8996-164">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="c8996-164">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c8996-165">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c8996-165">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c8996-166">Текущее состояние объекта.</span><span class="sxs-lookup"><span data-stu-id="c8996-166">Current status of the object.</span></span> <span data-ttu-id="c8996-167">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="c8996-167">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<span data-ttu-id="c8996-168">В эти значения входят:</span><span class="sxs-lookup"><span data-stu-id="c8996-168">Values include the following:</span></span>

<dl><span id="OK"></span><span id="ok"></span><dt>

<span data-ttu-id="c8996-169">**'**</span><span class="sxs-lookup"><span data-stu-id="c8996-169">**"OK"**</span></span>
</dt><span id="Error"></span><span id="error"></span><span id="ERROR"></span><dt>

<span data-ttu-id="c8996-170">**План**</span><span class="sxs-lookup"><span data-stu-id="c8996-170">**"Error"**</span></span>
</dt><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span><dt>

<span data-ttu-id="c8996-171">**Пониженной функциональности**</span><span class="sxs-lookup"><span data-stu-id="c8996-171">**"Degraded"**</span></span>
</dt><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span><dt>

<span data-ttu-id="c8996-172">**Неизвестный**</span><span class="sxs-lookup"><span data-stu-id="c8996-172">**"Unknown"**</span></span>
</dt><span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span><dt>

<span data-ttu-id="c8996-173">**"Пред Fail"**</span><span class="sxs-lookup"><span data-stu-id="c8996-173">**"Pred Fail"**</span></span>
</dt><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span><dt>

<span data-ttu-id="c8996-174">**Start**</span><span class="sxs-lookup"><span data-stu-id="c8996-174">**"Starting"**</span></span>
</dt><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span><dt>

<span data-ttu-id="c8996-175">**Идет**</span><span class="sxs-lookup"><span data-stu-id="c8996-175">**"Stopping"**</span></span>
</dt><span id="Service"></span><span id="service"></span><span id="SERVICE"></span><dt>

<span data-ttu-id="c8996-176">**Служеб**</span><span class="sxs-lookup"><span data-stu-id="c8996-176">**"Service"**</span></span>
</dt><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span><dt>

<span data-ttu-id="c8996-177">**Груз**</span><span class="sxs-lookup"><span data-stu-id="c8996-177">**"Stressed"**</span></span>
</dt><span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span><dt>

<span data-ttu-id="c8996-178">**"Recover"**</span><span class="sxs-lookup"><span data-stu-id="c8996-178">**"NonRecover"**</span></span>
</dt><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span><dt>

<span data-ttu-id="c8996-179">**"Нет контакта"**</span><span class="sxs-lookup"><span data-stu-id="c8996-179">**"No Contact"**</span></span>
</dt><span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span><dt>

<span data-ttu-id="c8996-180">**"Потеря связи"**</span><span class="sxs-lookup"><span data-stu-id="c8996-180">**"Lost Comm"**</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="c8996-181">**системкреатионкласснаме**</span><span class="sxs-lookup"><span data-stu-id="c8996-181">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c8996-182">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="c8996-182">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c8996-183">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c8996-183">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c8996-184">Имя класса создания системы области.</span><span class="sxs-lookup"><span data-stu-id="c8996-184">Scoping system's creation class name.</span></span>

</dd> <dt>

<span data-ttu-id="c8996-185">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="c8996-185">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c8996-186">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="c8996-186">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c8996-187">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c8996-187">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c8996-188">Имя системы, в которой размещена служба.</span><span class="sxs-lookup"><span data-stu-id="c8996-188">Name of the system that hosts the service.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="c8996-189">Требования</span><span class="sxs-lookup"><span data-stu-id="c8996-189">Requirements</span></span>



| <span data-ttu-id="c8996-190">Требование</span><span class="sxs-lookup"><span data-stu-id="c8996-190">Requirement</span></span> | <span data-ttu-id="c8996-191">Значение</span><span class="sxs-lookup"><span data-stu-id="c8996-191">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c8996-192">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="c8996-192">Minimum supported client</span></span><br/> | <span data-ttu-id="c8996-193">\[Только Windows 8.1 Классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="c8996-193">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="c8996-194">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="c8996-194">Minimum supported server</span></span><br/> | <span data-ttu-id="c8996-195">Только классические приложения Windows Server 2012 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="c8996-195">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="c8996-196">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="c8996-196">Namespace</span></span><br/>                | <span data-ttu-id="c8996-197">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="c8996-197">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="c8996-198">MOF</span><span class="sxs-lookup"><span data-stu-id="c8996-198">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c8996-199"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="c8996-199"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="c8996-200">DLL</span><span class="sxs-lookup"><span data-stu-id="c8996-200">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c8996-201"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="c8996-201"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="c8996-202">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c8996-202">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c8996-203">**Мсвм \_ гуестсервице**</span><span class="sxs-lookup"><span data-stu-id="c8996-203">**Msvm\_GuestService**</span></span>](msvm-guestservice.md)
</dt> </dl>

 

