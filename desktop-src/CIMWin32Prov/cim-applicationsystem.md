---
description: Класс CIM \_ аппликатионсистем представляет приложение или программную систему, поддерживающую определенную бизнес-функцию, которая может управляться как независимая единица.
ms.assetid: 42471863-ff6c-4464-8b0a-7dad2fd11934
ms.tgt_platform: multiple
title: Класс CIM_ApplicationSystem
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ApplicationSystem
- CIM_ApplicationSystem.Caption
- CIM_ApplicationSystem.Description
- CIM_ApplicationSystem.InstallDate
- CIM_ApplicationSystem.Status
- CIM_ApplicationSystem.CreationClassName
- CIM_ApplicationSystem.Name
- CIM_ApplicationSystem.NameFormat
- CIM_ApplicationSystem.PrimaryOwnerContact
- CIM_ApplicationSystem.PrimaryOwnerName
- CIM_ApplicationSystem.Roles
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: a69c05b11c5f3c623824783ed13f42c0a3eab801
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105655971"
---
# <a name="cim_applicationsystem-class"></a><span data-ttu-id="2b0a8-103">\_Класс CIM аппликатионсистем</span><span class="sxs-lookup"><span data-stu-id="2b0a8-103">CIM\_ApplicationSystem class</span></span>

<span data-ttu-id="2b0a8-104">Класс **CIM \_ аппликатионсистем** представляет приложение или программную систему, поддерживающую определенную бизнес-функцию, которая может управляться как независимая единица.</span><span class="sxs-lookup"><span data-stu-id="2b0a8-104">The **CIM\_ApplicationSystem** class represents an application or software system that supports a particular business function that can be managed as an independent unit.</span></span> <span data-ttu-id="2b0a8-105">Такая система может быть разложена на функциональные компоненты с помощью класса [**CIM \_ софтварефеатуре**](cim-softwarefeature.md) .</span><span class="sxs-lookup"><span data-stu-id="2b0a8-105">Such a system can be decomposed into its functional components using the [**CIM\_SoftwareFeature**](cim-softwarefeature.md) class.</span></span> <span data-ttu-id="2b0a8-106">Функции программного обеспечения для конкретного приложения или программной системы находятся с помощью ассоциации [**CIM \_ аппликатионсистемсофтварефеатуре**](cim-applicationsystemsoftwarefeature.md) .</span><span class="sxs-lookup"><span data-stu-id="2b0a8-106">The software features for a particular application or software system are located using the [**CIM\_ApplicationSystemSoftwareFeature**](cim-applicationsystemsoftwarefeature.md) association.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="2b0a8-107">Классы CIM (модель CIM) в DMTF (распределенная задача управления) являются родительскими классами, на которых строятся классы WMI.</span><span class="sxs-lookup"><span data-stu-id="2b0a8-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="2b0a8-108">В настоящее время WMI поддерживает только [схемы версии CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="2b0a8-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="2b0a8-109">Приведенный ниже синтаксис является упрощенной версией кода MOF и включает все унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="2b0a8-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="2b0a8-110">Свойства перечислены в алфавитном порядке, а не в MOF.</span><span class="sxs-lookup"><span data-stu-id="2b0a8-110">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="2b0a8-111">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="2b0a8-111">Syntax</span></span>

``` syntax
[Abstract, UUID("{120BB700-DB2B-11d2-85FC-0000F8102E5F}"), AMENDMENT]
class CIM_ApplicationSystem : CIM_System
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Status;
  string   CreationClassName;
  string   Name;
  string   NameFormat;
  string   PrimaryOwnerContact;
  string   PrimaryOwnerName;
  string   Roles[];
};
```

## <a name="members"></a><span data-ttu-id="2b0a8-112">Члены</span><span class="sxs-lookup"><span data-stu-id="2b0a8-112">Members</span></span>

<span data-ttu-id="2b0a8-113">Класс **CIM \_ аппликатионсистем** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="2b0a8-113">The **CIM\_ApplicationSystem** class has these types of members:</span></span>

-   [<span data-ttu-id="2b0a8-114">Свойства</span><span class="sxs-lookup"><span data-stu-id="2b0a8-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="2b0a8-115">Свойства</span><span class="sxs-lookup"><span data-stu-id="2b0a8-115">Properties</span></span>

<span data-ttu-id="2b0a8-116">Класс **CIM \_ аппликатионсистем** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="2b0a8-116">The **CIM\_ApplicationSystem** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="2b0a8-117">**Заголовок**</span><span class="sxs-lookup"><span data-stu-id="2b0a8-117">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2b0a8-118">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="2b0a8-118">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2b0a8-119">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="2b0a8-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2b0a8-120">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="2b0a8-120">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="2b0a8-121">Краткое текстовое описание объекта.</span><span class="sxs-lookup"><span data-stu-id="2b0a8-121">A short textual description of the object.</span></span>

<span data-ttu-id="2b0a8-122">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="2b0a8-122">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="2b0a8-123">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="2b0a8-123">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2b0a8-124">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="2b0a8-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2b0a8-125">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="2b0a8-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2b0a8-126">Квалификаторы: [ **\_ ключ CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="2b0a8-126">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="2b0a8-127">Имя класса или подкласса, используемого при создании экземпляра.</span><span class="sxs-lookup"><span data-stu-id="2b0a8-127">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="2b0a8-128">При использовании с другими ключевыми свойствами класса это свойство позволяет однозначно идентифицировать все экземпляры класса и его подклассов.</span><span class="sxs-lookup"><span data-stu-id="2b0a8-128">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="2b0a8-129">Это свойство наследуется [**от \_ системы CIM**](cim-system.md).</span><span class="sxs-lookup"><span data-stu-id="2b0a8-129">This property is inherited from [**CIM\_System**](cim-system.md).</span></span>

</dd> <dt>

<span data-ttu-id="2b0a8-130">**Описание**</span><span class="sxs-lookup"><span data-stu-id="2b0a8-130">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2b0a8-131">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="2b0a8-131">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2b0a8-132">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="2b0a8-132">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2b0a8-133">Квалификаторы: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Описание")</span><span class="sxs-lookup"><span data-stu-id="2b0a8-133">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="2b0a8-134">Текстовое описание объекта.</span><span class="sxs-lookup"><span data-stu-id="2b0a8-134">A textual description of the object.</span></span>

<span data-ttu-id="2b0a8-135">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="2b0a8-135">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="2b0a8-136">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="2b0a8-136">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2b0a8-137">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="2b0a8-137">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="2b0a8-138">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="2b0a8-138">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2b0a8-139">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" Дата установки ")</span><span class="sxs-lookup"><span data-stu-id="2b0a8-139">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="2b0a8-140">Указывает, когда был установлен объект.</span><span class="sxs-lookup"><span data-stu-id="2b0a8-140">Indicates when the object was installed.</span></span> <span data-ttu-id="2b0a8-141">Отсутствие значения не означает, что объект не установлен.</span><span class="sxs-lookup"><span data-stu-id="2b0a8-141">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="2b0a8-142">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="2b0a8-142">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="2b0a8-143">**Name**</span><span class="sxs-lookup"><span data-stu-id="2b0a8-143">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2b0a8-144">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="2b0a8-144">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2b0a8-145">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="2b0a8-145">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2b0a8-146">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="2b0a8-146">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="2b0a8-147">Определяет метку, по которой известен объект.</span><span class="sxs-lookup"><span data-stu-id="2b0a8-147">Defines the label by which the object is known.</span></span>

<span data-ttu-id="2b0a8-148">Это свойство наследуется [**от \_ системы CIM**](cim-system.md).</span><span class="sxs-lookup"><span data-stu-id="2b0a8-148">This property is inherited from [**CIM\_System**](cim-system.md).</span></span>

</dd> <dt>

<span data-ttu-id="2b0a8-149">**намеформат**</span><span class="sxs-lookup"><span data-stu-id="2b0a8-149">**NameFormat**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2b0a8-150">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="2b0a8-150">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2b0a8-151">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="2b0a8-151">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2b0a8-152">Определяет, как было создано системное имя с помощью эвристики подклассов.</span><span class="sxs-lookup"><span data-stu-id="2b0a8-152">Identifies how the system name was generated, using the subclass heuristic.</span></span>

<span data-ttu-id="2b0a8-153">Это свойство наследуется [**от \_ системы CIM**](cim-system.md).</span><span class="sxs-lookup"><span data-stu-id="2b0a8-153">This property is inherited from [**CIM\_System**](cim-system.md).</span></span>

</dd> <dt>

<span data-ttu-id="2b0a8-154">**примарйовнерконтакт**</span><span class="sxs-lookup"><span data-stu-id="2b0a8-154">**PrimaryOwnerContact**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2b0a8-155">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="2b0a8-155">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2b0a8-156">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="2b0a8-156">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2b0a8-157">Способ достижения основного владельца системы (например, номер телефона или адрес электронной почты).</span><span class="sxs-lookup"><span data-stu-id="2b0a8-157">How the primary system owner can be reached (for example, phone number or email address).</span></span>

<span data-ttu-id="2b0a8-158">Это свойство наследуется [**от \_ системы CIM**](cim-system.md).</span><span class="sxs-lookup"><span data-stu-id="2b0a8-158">This property is inherited from [**CIM\_System**](cim-system.md).</span></span>

</dd> <dt>

<span data-ttu-id="2b0a8-159">**примарйовнернаме**</span><span class="sxs-lookup"><span data-stu-id="2b0a8-159">**PrimaryOwnerName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2b0a8-160">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="2b0a8-160">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2b0a8-161">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="2b0a8-161">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2b0a8-162">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="2b0a8-162">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="2b0a8-163">Имя основного владельца системы.</span><span class="sxs-lookup"><span data-stu-id="2b0a8-163">Name of the primary system owner.</span></span>

<span data-ttu-id="2b0a8-164">Это свойство наследуется [**от \_ системы CIM**](cim-system.md).</span><span class="sxs-lookup"><span data-stu-id="2b0a8-164">This property is inherited from [**CIM\_System**](cim-system.md).</span></span>

</dd> <dt>

<span data-ttu-id="2b0a8-165">**Роли**</span><span class="sxs-lookup"><span data-stu-id="2b0a8-165">**Roles**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2b0a8-166">Тип данных: массив **строк**</span><span class="sxs-lookup"><span data-stu-id="2b0a8-166">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="2b0a8-167">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="2b0a8-167">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="2b0a8-168">Роли, которые система играет в среде информационных технологий.</span><span class="sxs-lookup"><span data-stu-id="2b0a8-168">Roles the system plays in the information technology environment.</span></span> <span data-ttu-id="2b0a8-169">Подклассы системы могут переопределять это свойство для определения явных значений ролей.</span><span class="sxs-lookup"><span data-stu-id="2b0a8-169">Subclasses of the system can override this property to define explicit role values.</span></span> <span data-ttu-id="2b0a8-170">Кроме того, Рабочая группа может описывать эвристику, соглашения и правила для указания ролей.</span><span class="sxs-lookup"><span data-stu-id="2b0a8-170">Alternately, a working group can describe the heuristics, conventions, and guidelines for specifying roles.</span></span> <span data-ttu-id="2b0a8-171">Например, для экземпляра сетевой системы это свойство может содержать строку "Switch" или "Bridge".</span><span class="sxs-lookup"><span data-stu-id="2b0a8-171">For example, for an instance of a networking system, this property might contain the string "Switch" or "Bridge".</span></span>

<span data-ttu-id="2b0a8-172">Это свойство наследуется [**от \_ системы CIM**](cim-system.md).</span><span class="sxs-lookup"><span data-stu-id="2b0a8-172">This property is inherited from [**CIM\_System**](cim-system.md).</span></span>

</dd> <dt>

<span data-ttu-id="2b0a8-173">**Состояние**</span><span class="sxs-lookup"><span data-stu-id="2b0a8-173">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2b0a8-174">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="2b0a8-174">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2b0a8-175">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="2b0a8-175">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2b0a8-176">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("состояние")</span><span class="sxs-lookup"><span data-stu-id="2b0a8-176">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="2b0a8-177">Строка, указывающая текущее состояние объекта.</span><span class="sxs-lookup"><span data-stu-id="2b0a8-177">String that indicates the current status of the object.</span></span> <span data-ttu-id="2b0a8-178">Можно определить операционное и нерабочее состояние.</span><span class="sxs-lookup"><span data-stu-id="2b0a8-178">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="2b0a8-179">Оперативное состояние может включать "ОК", "деградация" и "пред Fail".</span><span class="sxs-lookup"><span data-stu-id="2b0a8-179">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="2b0a8-180">"Пред-Fail" указывает, что элемент работает правильно, но прогнозирует сбой (например, жесткий диск с поддержкой SMART).</span><span class="sxs-lookup"><span data-stu-id="2b0a8-180">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="2b0a8-181">Нерабочее состояние может включать "Error", "starting", "остановка" и "обслуживание".</span><span class="sxs-lookup"><span data-stu-id="2b0a8-181">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="2b0a8-182">"Служба" может применяться при зеркальном отображении дисков, перезагрузке списка разрешений пользователя или выполнении других административных задач.</span><span class="sxs-lookup"><span data-stu-id="2b0a8-182">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="2b0a8-183">Не вся такая работа находится в оперативном режиме, но управляемый элемент не является ни "ОК", ни в одном из других состояний.</span><span class="sxs-lookup"><span data-stu-id="2b0a8-183">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="2b0a8-184">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="2b0a8-184">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="2b0a8-185">В эти значения входят:</span><span class="sxs-lookup"><span data-stu-id="2b0a8-185">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="2b0a8-186">**ОК** ("ОК")</span><span class="sxs-lookup"><span data-stu-id="2b0a8-186">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="2b0a8-187">**Ошибка** ("ошибка")</span><span class="sxs-lookup"><span data-stu-id="2b0a8-187">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="2b0a8-188">**Пониженная работоспособность** (пониженная работоспособность)</span><span class="sxs-lookup"><span data-stu-id="2b0a8-188">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="2b0a8-189">**Неизвестно** ("неизвестно")</span><span class="sxs-lookup"><span data-stu-id="2b0a8-189">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="2b0a8-190">**Пред-ошибка** ("пред Fail")</span><span class="sxs-lookup"><span data-stu-id="2b0a8-190">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="2b0a8-191">**Запуск** ("Запуск")</span><span class="sxs-lookup"><span data-stu-id="2b0a8-191">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="2b0a8-192">**Остановка** ("остановка")</span><span class="sxs-lookup"><span data-stu-id="2b0a8-192">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="2b0a8-193">**Служба** ("служба")</span><span class="sxs-lookup"><span data-stu-id="2b0a8-193">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="2b0a8-194">**Пренапряжению** ("напряжению")</span><span class="sxs-lookup"><span data-stu-id="2b0a8-194">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="2b0a8-195">**Невосстановление** ("невосстановление")</span><span class="sxs-lookup"><span data-stu-id="2b0a8-195">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="2b0a8-196">**Нет контакта** ("нет контакта")</span><span class="sxs-lookup"><span data-stu-id="2b0a8-196">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="2b0a8-197">**Потеря** связи ("потеря связи")</span><span class="sxs-lookup"><span data-stu-id="2b0a8-197">**Lost Comm** ("Lost Comm")</span></span>


<span data-ttu-id="2b0a8-198"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="2b0a8-198"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="remarks"></a><span data-ttu-id="2b0a8-199">Комментарии</span><span class="sxs-lookup"><span data-stu-id="2b0a8-199">Remarks</span></span>

<span data-ttu-id="2b0a8-200">Класс **CIM \_ аппликатионсистем** является производным от [**\_ системы CIM**](cim-system.md).</span><span class="sxs-lookup"><span data-stu-id="2b0a8-200">The **CIM\_ApplicationSystem** class is derived from [**CIM\_System**](cim-system.md).</span></span>

<span data-ttu-id="2b0a8-201">Инструментарий WMI не реализует этот класс.</span><span class="sxs-lookup"><span data-stu-id="2b0a8-201">WMI does not implement this class.</span></span>

<span data-ttu-id="2b0a8-202">Эта документация является производной от описаний класса CIM, опубликованных в формате DMTF.</span><span class="sxs-lookup"><span data-stu-id="2b0a8-202">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="2b0a8-203">Корпорация Майкрософт могла внести изменения в Исправление незначительных ошибок, соответствовать стандартам документации пакета Microsoft SDK или предоставить дополнительные сведения.</span><span class="sxs-lookup"><span data-stu-id="2b0a8-203">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="2b0a8-204">Требования</span><span class="sxs-lookup"><span data-stu-id="2b0a8-204">Requirements</span></span>



| <span data-ttu-id="2b0a8-205">Требование</span><span class="sxs-lookup"><span data-stu-id="2b0a8-205">Requirement</span></span> | <span data-ttu-id="2b0a8-206">Значение</span><span class="sxs-lookup"><span data-stu-id="2b0a8-206">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="2b0a8-207">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="2b0a8-207">Minimum supported client</span></span><br/> | <span data-ttu-id="2b0a8-208">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="2b0a8-208">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="2b0a8-209">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="2b0a8-209">Minimum supported server</span></span><br/> | <span data-ttu-id="2b0a8-210">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="2b0a8-210">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="2b0a8-211">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="2b0a8-211">Namespace</span></span><br/>                | <span data-ttu-id="2b0a8-212">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="2b0a8-212">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="2b0a8-213">MOF</span><span class="sxs-lookup"><span data-stu-id="2b0a8-213">MOF</span></span><br/>                      | <dl> <span data-ttu-id="2b0a8-214"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="2b0a8-214"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="2b0a8-215">DLL</span><span class="sxs-lookup"><span data-stu-id="2b0a8-215">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2b0a8-216"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2b0a8-216"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2b0a8-217">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="2b0a8-217">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2b0a8-218">**\_Система CIM**</span><span class="sxs-lookup"><span data-stu-id="2b0a8-218">**CIM\_System**</span></span>](cim-system.md)
</dt> </dl>

 

