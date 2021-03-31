---
description: Мсвм \_ гуестсервице — это абстрактный базовый класс для служб в гостевой системе, к которому можно получить доступ с узла.
ms.assetid: F9E6FFE6-B8C5-4F06-BF22-A4BDB20F813A
title: Класс Msvm_GuestService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_GuestService
- Msvm_GuestService.Caption
- Msvm_GuestService.CreationClassName
- Msvm_GuestService.Description
- Msvm_GuestService.InstallDate
- Msvm_GuestService.Name
- Msvm_GuestService.Started
- Msvm_GuestService.StartMode
- Msvm_GuestService.Status
- Msvm_GuestService.SystemCreationClassName
- Msvm_GuestService.SystemName
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 99d1936a2678fc2d8357974f9c11a250a1d9bce8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104423698"
---
# <a name="msvm_guestservice-class"></a><span data-ttu-id="9bd08-103">\_Класс мсвм гуестсервице</span><span class="sxs-lookup"><span data-stu-id="9bd08-103">Msvm\_GuestService class</span></span>

<span data-ttu-id="9bd08-104">**Мсвм \_ Гуестсервице** — это абстрактный базовый класс для служб в гостевой системе, к которому можно получить доступ с узла.</span><span class="sxs-lookup"><span data-stu-id="9bd08-104">**Msvm\_GuestService** is the abstract base class for services in the guest that can be accessed from the host.</span></span> <span data-ttu-id="9bd08-105">Этот класс является производным от [**класса \_ службы CIM**](/windows/desktop/CIMWin32Prov/cim-service) .</span><span class="sxs-lookup"><span data-stu-id="9bd08-105">This class derives from the [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service) class.</span></span>

<span data-ttu-id="9bd08-106">Следующий синтаксис упрощен из MOF-кода и включает все унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="9bd08-106">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="9bd08-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="9bd08-107">Syntax</span></span>

``` syntax
[Abstract, AMENDMENT]
class Msvm_GuestService : CIM_Service
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

## <a name="members"></a><span data-ttu-id="9bd08-108">Члены</span><span class="sxs-lookup"><span data-stu-id="9bd08-108">Members</span></span>

<span data-ttu-id="9bd08-109">Класс **мсвм \_ гуестсервице** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="9bd08-109">The **Msvm\_GuestService** class has these types of members:</span></span>

-   [<span data-ttu-id="9bd08-110">Методы</span><span class="sxs-lookup"><span data-stu-id="9bd08-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="9bd08-111">Свойства</span><span class="sxs-lookup"><span data-stu-id="9bd08-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="9bd08-112">Методы</span><span class="sxs-lookup"><span data-stu-id="9bd08-112">Methods</span></span>

<span data-ttu-id="9bd08-113">Класс **мсвм \_ гуестсервице** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="9bd08-113">The **Msvm\_GuestService** class has these methods.</span></span>



| <span data-ttu-id="9bd08-114">Метод</span><span class="sxs-lookup"><span data-stu-id="9bd08-114">Method</span></span>                                                             | <span data-ttu-id="9bd08-115">Описание</span><span class="sxs-lookup"><span data-stu-id="9bd08-115">Description</span></span>                                                                                |
|:-------------------------------------------------------------------|:-------------------------------------------------------------------------------------------|
| [<span data-ttu-id="9bd08-116">**Равен**</span><span class="sxs-lookup"><span data-stu-id="9bd08-116">**RequestStateChange**</span></span>](requeststatechange-msvm-guestservice.md) | <span data-ttu-id="9bd08-117">Запрашивает изменение состояния гостевой службы на указанное значение.</span><span class="sxs-lookup"><span data-stu-id="9bd08-117">Requests that the state of the guest service be changed to the specified value.</span></span><br/> |
| [<span data-ttu-id="9bd08-118">**StartService**</span><span class="sxs-lookup"><span data-stu-id="9bd08-118">**StartService**</span></span>](startservice-msvm-guestservice.md)             | <span data-ttu-id="9bd08-119">Перевод гостевой службы в состояние запуска.</span><span class="sxs-lookup"><span data-stu-id="9bd08-119">Puts the guest service in a started state.</span></span> <br/>                                     |
| [<span data-ttu-id="9bd08-120">**StopService**</span><span class="sxs-lookup"><span data-stu-id="9bd08-120">**StopService**</span></span>](stopservice-msvm-guestservice.md)               | <span data-ttu-id="9bd08-121">Останавливает гостевую службу.</span><span class="sxs-lookup"><span data-stu-id="9bd08-121">Stops the guest service.</span></span> <br/>                                                       |



 

### <a name="properties"></a><span data-ttu-id="9bd08-122">Свойства</span><span class="sxs-lookup"><span data-stu-id="9bd08-122">Properties</span></span>

<span data-ttu-id="9bd08-123">Класс **мсвм \_ гуестсервице** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="9bd08-123">The **Msvm\_GuestService** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="9bd08-124">**Заголовок**</span><span class="sxs-lookup"><span data-stu-id="9bd08-124">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9bd08-125">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="9bd08-125">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9bd08-126">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9bd08-126">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9bd08-127">Краткое текстовое описание объекта.</span><span class="sxs-lookup"><span data-stu-id="9bd08-127">Short textual description of the object.</span></span> <span data-ttu-id="9bd08-128">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="9bd08-128">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="9bd08-129">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="9bd08-129">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9bd08-130">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="9bd08-130">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9bd08-131">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9bd08-131">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9bd08-132">Имя класса или подкласса, используемого при создании экземпляра.</span><span class="sxs-lookup"><span data-stu-id="9bd08-132">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="9bd08-133">При использовании с другими ключевыми свойствами класса это свойство позволяет однозначно идентифицировать все экземпляры класса и его подклассов.</span><span class="sxs-lookup"><span data-stu-id="9bd08-133">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

</dd> <dt>

<span data-ttu-id="9bd08-134">**Описание**</span><span class="sxs-lookup"><span data-stu-id="9bd08-134">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9bd08-135">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="9bd08-135">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9bd08-136">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9bd08-136">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9bd08-137">Текстовое описание объекта.</span><span class="sxs-lookup"><span data-stu-id="9bd08-137">Textual description of the object.</span></span> <span data-ttu-id="9bd08-138">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="9bd08-138">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="9bd08-139">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="9bd08-139">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9bd08-140">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="9bd08-140">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="9bd08-141">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9bd08-141">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9bd08-142">Дата и время установки объекта.</span><span class="sxs-lookup"><span data-stu-id="9bd08-142">Date and time the object was installed.</span></span> <span data-ttu-id="9bd08-143">Для этого свойства не требуется значение, указывающее, что объект установлен.</span><span class="sxs-lookup"><span data-stu-id="9bd08-143">This property does not need a value to indicate that the object is installed.</span></span> <span data-ttu-id="9bd08-144">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="9bd08-144">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="9bd08-145">**Name**</span><span class="sxs-lookup"><span data-stu-id="9bd08-145">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9bd08-146">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="9bd08-146">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9bd08-147">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9bd08-147">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9bd08-148">Уникальный идентификатор службы, который также содержит сведения об управляемых функциях.</span><span class="sxs-lookup"><span data-stu-id="9bd08-148">Unique identifier for the service that also provides an indication of the functionality that is managed.</span></span> <span data-ttu-id="9bd08-149">Дополнительные сведения о функциональных возможностях см. в описании свойства объекта **Description** .</span><span class="sxs-lookup"><span data-stu-id="9bd08-149">For more information about the functionality, see the object's **Description** property.</span></span> <span data-ttu-id="9bd08-150">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="9bd08-150">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="9bd08-151">**Запуск**</span><span class="sxs-lookup"><span data-stu-id="9bd08-151">**Started**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9bd08-152">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="9bd08-152">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="9bd08-153">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9bd08-153">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9bd08-154">Если **значение равно true**, служба запущена.</span><span class="sxs-lookup"><span data-stu-id="9bd08-154">If **TRUE**, the service has started.</span></span>

</dd> <dt>

<span data-ttu-id="9bd08-155">**StartMode**</span><span class="sxs-lookup"><span data-stu-id="9bd08-155">**StartMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9bd08-156">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="9bd08-156">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9bd08-157">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9bd08-157">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9bd08-158">Указывает, запускается ли служба автоматически (например, операционная система) или только после запроса.</span><span class="sxs-lookup"><span data-stu-id="9bd08-158">Indicates whether the service is automatically started (for example, by an operating system) or only started upon request.</span></span>

<span data-ttu-id="9bd08-159">В эти значения входят:</span><span class="sxs-lookup"><span data-stu-id="9bd08-159">Values include the following:</span></span>

<dl><span id="Automatic"></span><span id="automatic"></span><span id="AUTOMATIC"></span><dt>

<span data-ttu-id="9bd08-160">**Автоматическое**</span><span class="sxs-lookup"><span data-stu-id="9bd08-160">**"Automatic"**</span></span>
</dt><span id="Manual"></span><span id="manual"></span><span id="MANUAL"></span><dt>

<span data-ttu-id="9bd08-161">**Документации**</span><span class="sxs-lookup"><span data-stu-id="9bd08-161">**"Manual"**</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="9bd08-162">**Состояние**</span><span class="sxs-lookup"><span data-stu-id="9bd08-162">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9bd08-163">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="9bd08-163">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9bd08-164">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9bd08-164">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9bd08-165">Текущее состояние объекта.</span><span class="sxs-lookup"><span data-stu-id="9bd08-165">Current status of the object.</span></span> <span data-ttu-id="9bd08-166">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="9bd08-166">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<span data-ttu-id="9bd08-167">В эти значения входят:</span><span class="sxs-lookup"><span data-stu-id="9bd08-167">Values include the following:</span></span>

<dl><span id="OK"></span><span id="ok"></span><dt>

<span data-ttu-id="9bd08-168">**'**</span><span class="sxs-lookup"><span data-stu-id="9bd08-168">**"OK"**</span></span>
</dt><span id="Error"></span><span id="error"></span><span id="ERROR"></span><dt>

<span data-ttu-id="9bd08-169">**План**</span><span class="sxs-lookup"><span data-stu-id="9bd08-169">**"Error"**</span></span>
</dt><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span><dt>

<span data-ttu-id="9bd08-170">**Пониженной функциональности**</span><span class="sxs-lookup"><span data-stu-id="9bd08-170">**"Degraded"**</span></span>
</dt><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span><dt>

<span data-ttu-id="9bd08-171">**Неизвестный**</span><span class="sxs-lookup"><span data-stu-id="9bd08-171">**"Unknown"**</span></span>
</dt><span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span><dt>

<span data-ttu-id="9bd08-172">**"Пред Fail"**</span><span class="sxs-lookup"><span data-stu-id="9bd08-172">**"Pred Fail"**</span></span>
</dt><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span><dt>

<span data-ttu-id="9bd08-173">**Start**</span><span class="sxs-lookup"><span data-stu-id="9bd08-173">**"Starting"**</span></span>
</dt><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span><dt>

<span data-ttu-id="9bd08-174">**Идет**</span><span class="sxs-lookup"><span data-stu-id="9bd08-174">**"Stopping"**</span></span>
</dt><span id="Service"></span><span id="service"></span><span id="SERVICE"></span><dt>

<span data-ttu-id="9bd08-175">**Служеб**</span><span class="sxs-lookup"><span data-stu-id="9bd08-175">**"Service"**</span></span>
</dt><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span><dt>

<span data-ttu-id="9bd08-176">**Груз**</span><span class="sxs-lookup"><span data-stu-id="9bd08-176">**"Stressed"**</span></span>
</dt><span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span><dt>

<span data-ttu-id="9bd08-177">**"Recover"**</span><span class="sxs-lookup"><span data-stu-id="9bd08-177">**"NonRecover"**</span></span>
</dt><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span><dt>

<span data-ttu-id="9bd08-178">**"Нет контакта"**</span><span class="sxs-lookup"><span data-stu-id="9bd08-178">**"No Contact"**</span></span>
</dt><span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span><dt>

<span data-ttu-id="9bd08-179">**"Потеря связи"**</span><span class="sxs-lookup"><span data-stu-id="9bd08-179">**"Lost Comm"**</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="9bd08-180">**системкреатионкласснаме**</span><span class="sxs-lookup"><span data-stu-id="9bd08-180">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9bd08-181">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="9bd08-181">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9bd08-182">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9bd08-182">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9bd08-183">Имя класса создания системы области.</span><span class="sxs-lookup"><span data-stu-id="9bd08-183">Scoping system's creation class name.</span></span>

</dd> <dt>

<span data-ttu-id="9bd08-184">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="9bd08-184">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9bd08-185">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="9bd08-185">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9bd08-186">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9bd08-186">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9bd08-187">Имя системы, в которой размещена служба.</span><span class="sxs-lookup"><span data-stu-id="9bd08-187">Name of the system that hosts the service.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="9bd08-188">Требования</span><span class="sxs-lookup"><span data-stu-id="9bd08-188">Requirements</span></span>



| <span data-ttu-id="9bd08-189">Требование</span><span class="sxs-lookup"><span data-stu-id="9bd08-189">Requirement</span></span> | <span data-ttu-id="9bd08-190">Значение</span><span class="sxs-lookup"><span data-stu-id="9bd08-190">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9bd08-191">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="9bd08-191">Minimum supported client</span></span><br/> | <span data-ttu-id="9bd08-192">\[Только Windows 8.1 Классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="9bd08-192">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="9bd08-193">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="9bd08-193">Minimum supported server</span></span><br/> | <span data-ttu-id="9bd08-194">Только классические приложения Windows Server 2012 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="9bd08-194">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="9bd08-195">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="9bd08-195">Namespace</span></span><br/>                | <span data-ttu-id="9bd08-196">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="9bd08-196">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="9bd08-197">MOF</span><span class="sxs-lookup"><span data-stu-id="9bd08-197">MOF</span></span><br/>                      | <dl> <span data-ttu-id="9bd08-198"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="9bd08-198"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="9bd08-199">DLL</span><span class="sxs-lookup"><span data-stu-id="9bd08-199">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9bd08-200"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="9bd08-200"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="9bd08-201">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="9bd08-201">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9bd08-202">**\_Служба CIM**</span><span class="sxs-lookup"><span data-stu-id="9bd08-202">**CIM\_Service**</span></span>](cim-service.md)
</dt> <dt>

[<span data-ttu-id="9bd08-203">**\_Служба CIM**</span><span class="sxs-lookup"><span data-stu-id="9bd08-203">**CIM\_Service**</span></span>](/windows/desktop/CIMWin32Prov/cim-service)
</dt> </dl>

 

