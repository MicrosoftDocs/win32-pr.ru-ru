---
description: '\_Класс системы CIM выполняет статистическую обработку перечислимого набора управляемых системных элементов.'
ms.assetid: cbfa60d4-36ae-4e0c-a57f-aabf219851d0
ms.tgt_platform: multiple
title: Класс CIM_System (поставщики WMI CIMWin32)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_System
- CIM_System.Caption
- CIM_System.Description
- CIM_System.InstallDate
- CIM_System.Status
- CIM_System.CreationClassName
- CIM_System.Name
- CIM_System.NameFormat
- CIM_System.PrimaryOwnerContact
- CIM_System.PrimaryOwnerName
- CIM_System.Roles
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: ef04e472e11c848aadb63c98b3dee2ea645a3ce7
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103990630"
---
# <a name="cim_system-class-cimwin32-wmi-providers"></a><span data-ttu-id="88225-103">Класс CIM_System (поставщики WMI CIMWin32)</span><span class="sxs-lookup"><span data-stu-id="88225-103">CIM_System class (CIMWin32 WMI Providers)</span></span>

<span data-ttu-id="88225-104">Класс **\_ системы CIM** выполняет статистическую обработку перечислимого набора управляемых системных элементов.</span><span class="sxs-lookup"><span data-stu-id="88225-104">The **CIM\_System** class aggregates an enumerable set of managed system elements.</span></span> <span data-ttu-id="88225-105">Статистическая обработка работает как единое функциональное целое.</span><span class="sxs-lookup"><span data-stu-id="88225-105">The aggregation operates as a functional whole.</span></span> <span data-ttu-id="88225-106">В любом конкретном подклассе системы имеется четко определенный список управляемых классов системных элементов, экземпляры которых должны быть агрегированы.</span><span class="sxs-lookup"><span data-stu-id="88225-106">Within any particular subclass of the system, there is a well-defined list of managed system element classes whose instances must be aggregated.</span></span>

<span data-ttu-id="88225-107">**\_ Системный объект CIM** и его производные являются объектами верхнего уровня CIM.</span><span class="sxs-lookup"><span data-stu-id="88225-107">The **CIM\_System** object and its derivatives are top-level objects of CIM.</span></span> <span data-ttu-id="88225-108">Они предоставляют область для множества компонентов и должны иметь уникальные системные ключи.</span><span class="sxs-lookup"><span data-stu-id="88225-108">They provide the scope for numerous components and are required to have unique system keys.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="88225-109">Классы CIM (модель CIM) в DMTF (распределенная задача управления) являются родительскими классами, на которых строятся классы WMI.</span><span class="sxs-lookup"><span data-stu-id="88225-109">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="88225-110">В настоящее время WMI поддерживает только [схемы версии CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="88225-110">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="88225-111">Следующий синтаксис упрощен из кода MOF-файл (MOF) и включает все его унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="88225-111">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="88225-112">Свойства перечислены в алфавитном порядке, а не в MOF.</span><span class="sxs-lookup"><span data-stu-id="88225-112">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="88225-113">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="88225-113">Syntax</span></span>

``` syntax
[Abstract, UUID("{8502C524-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class CIM_System : CIM_LogicalElement
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

## <a name="members"></a><span data-ttu-id="88225-114">Члены</span><span class="sxs-lookup"><span data-stu-id="88225-114">Members</span></span>

<span data-ttu-id="88225-115">Класс **\_ системы CIM** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="88225-115">The **CIM\_System** class has these types of members:</span></span>

-   [<span data-ttu-id="88225-116">Свойства</span><span class="sxs-lookup"><span data-stu-id="88225-116">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="88225-117">Свойства</span><span class="sxs-lookup"><span data-stu-id="88225-117">Properties</span></span>

<span data-ttu-id="88225-118">Класс **\_ системы CIM** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="88225-118">The **CIM\_System** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="88225-119">**Заголовок**</span><span class="sxs-lookup"><span data-stu-id="88225-119">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="88225-120">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="88225-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="88225-121">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="88225-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="88225-122">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="88225-122">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="88225-123">Краткое текстовое описание объекта.</span><span class="sxs-lookup"><span data-stu-id="88225-123">A short textual description of the object.</span></span>

<span data-ttu-id="88225-124">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="88225-124">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="88225-125">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="88225-125">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="88225-126">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="88225-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="88225-127">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="88225-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="88225-128">Квалификаторы: [ **\_ ключ CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="88225-128">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="88225-129">Имя класса или подкласса, используемого при создании экземпляра.</span><span class="sxs-lookup"><span data-stu-id="88225-129">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="88225-130">При использовании с другими ключевыми свойствами класса это свойство позволяет однозначно идентифицировать все экземпляры класса и его подклассов.</span><span class="sxs-lookup"><span data-stu-id="88225-130">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

</dd> <dt>

<span data-ttu-id="88225-131">**Описание**</span><span class="sxs-lookup"><span data-stu-id="88225-131">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="88225-132">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="88225-132">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="88225-133">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="88225-133">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="88225-134">Квалификаторы: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Описание")</span><span class="sxs-lookup"><span data-stu-id="88225-134">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="88225-135">Текстовое описание объекта.</span><span class="sxs-lookup"><span data-stu-id="88225-135">A textual description of the object.</span></span>

<span data-ttu-id="88225-136">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="88225-136">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="88225-137">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="88225-137">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="88225-138">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="88225-138">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="88225-139">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="88225-139">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="88225-140">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" Дата установки ")</span><span class="sxs-lookup"><span data-stu-id="88225-140">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="88225-141">Указывает, когда был установлен объект.</span><span class="sxs-lookup"><span data-stu-id="88225-141">Indicates when the object was installed.</span></span> <span data-ttu-id="88225-142">Отсутствие значения не означает, что объект не установлен.</span><span class="sxs-lookup"><span data-stu-id="88225-142">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="88225-143">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="88225-143">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="88225-144">**Name**</span><span class="sxs-lookup"><span data-stu-id="88225-144">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="88225-145">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="88225-145">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="88225-146">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="88225-146">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="88225-147">Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("имя"), [**ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="88225-147">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name"), [**Key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="88225-148">Определяет метку, по которой известен объект.</span><span class="sxs-lookup"><span data-stu-id="88225-148">Defines the label by which the object is known.</span></span>

</dd> <dt>

<span data-ttu-id="88225-149">**намеформат**</span><span class="sxs-lookup"><span data-stu-id="88225-149">**NameFormat**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="88225-150">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="88225-150">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="88225-151">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="88225-151">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="88225-152">Определяет, как было создано системное имя с помощью эвристики подклассов.</span><span class="sxs-lookup"><span data-stu-id="88225-152">Identifies how the system name was generated, using the subclass heuristic.</span></span>

</dd> <dt>

<span data-ttu-id="88225-153">**примарйовнерконтакт**</span><span class="sxs-lookup"><span data-stu-id="88225-153">**PrimaryOwnerContact**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="88225-154">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="88225-154">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="88225-155">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="88225-155">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="88225-156">Способ достижения основного владельца системы (например, номер телефона или адрес электронной почты).</span><span class="sxs-lookup"><span data-stu-id="88225-156">How the primary system owner can be reached (for example, phone number or email address).</span></span>

</dd> <dt>

<span data-ttu-id="88225-157">**примарйовнернаме**</span><span class="sxs-lookup"><span data-stu-id="88225-157">**PrimaryOwnerName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="88225-158">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="88225-158">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="88225-159">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="88225-159">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="88225-160">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="88225-160">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="88225-161">Имя основного владельца системы.</span><span class="sxs-lookup"><span data-stu-id="88225-161">Name of the primary system owner.</span></span>

</dd> <dt>

<span data-ttu-id="88225-162">**Роли**</span><span class="sxs-lookup"><span data-stu-id="88225-162">**Roles**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="88225-163">Тип данных: массив **строк**</span><span class="sxs-lookup"><span data-stu-id="88225-163">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="88225-164">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="88225-164">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="88225-165">Роли, которые система играет в среде информационных технологий.</span><span class="sxs-lookup"><span data-stu-id="88225-165">Roles the system plays in the information technology environment.</span></span> <span data-ttu-id="88225-166">Подклассы системы могут переопределять это свойство для определения явных значений ролей.</span><span class="sxs-lookup"><span data-stu-id="88225-166">Subclasses of the system can override this property to define explicit role values.</span></span> <span data-ttu-id="88225-167">Кроме того, Рабочая группа может описывать эвристику, соглашения и правила для указания ролей.</span><span class="sxs-lookup"><span data-stu-id="88225-167">Alternately, a working group can describe the heuristics, conventions, and guidelines for specifying roles.</span></span> <span data-ttu-id="88225-168">Например, для экземпляра сетевой системы это свойство может содержать строку "Switch" или "Bridge".</span><span class="sxs-lookup"><span data-stu-id="88225-168">For example, for an instance of a networking system, this property might contain the string "Switch" or "Bridge".</span></span>

</dd> <dt>

<span data-ttu-id="88225-169">**Состояние**</span><span class="sxs-lookup"><span data-stu-id="88225-169">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="88225-170">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="88225-170">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="88225-171">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="88225-171">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="88225-172">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("состояние")</span><span class="sxs-lookup"><span data-stu-id="88225-172">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="88225-173">Строка, указывающая текущее состояние объекта.</span><span class="sxs-lookup"><span data-stu-id="88225-173">String that indicates the current status of the object.</span></span> <span data-ttu-id="88225-174">Можно определить операционное и нерабочее состояние.</span><span class="sxs-lookup"><span data-stu-id="88225-174">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="88225-175">Оперативное состояние может включать "ОК", "деградация" и "пред Fail".</span><span class="sxs-lookup"><span data-stu-id="88225-175">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="88225-176">"Пред-Fail" указывает, что элемент работает правильно, но прогнозирует сбой (например, жесткий диск с поддержкой SMART).</span><span class="sxs-lookup"><span data-stu-id="88225-176">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="88225-177">Нерабочее состояние может включать "Error", "starting", "остановка" и "обслуживание".</span><span class="sxs-lookup"><span data-stu-id="88225-177">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="88225-178">"Служба" может применяться при зеркальном отображении дисков, перезагрузке списка разрешений пользователя или выполнении других административных задач.</span><span class="sxs-lookup"><span data-stu-id="88225-178">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="88225-179">Не вся такая работа находится в оперативном режиме, но управляемый элемент не является ни "ОК", ни в одном из других состояний.</span><span class="sxs-lookup"><span data-stu-id="88225-179">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="88225-180">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="88225-180">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="88225-181">В эти значения входят:</span><span class="sxs-lookup"><span data-stu-id="88225-181">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="88225-182">**ОК** ("ОК")</span><span class="sxs-lookup"><span data-stu-id="88225-182">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="88225-183">**Ошибка** ("ошибка")</span><span class="sxs-lookup"><span data-stu-id="88225-183">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="88225-184">**Пониженная работоспособность** (пониженная работоспособность)</span><span class="sxs-lookup"><span data-stu-id="88225-184">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="88225-185">**Неизвестно** ("неизвестно")</span><span class="sxs-lookup"><span data-stu-id="88225-185">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="88225-186">**Пред-ошибка** ("пред Fail")</span><span class="sxs-lookup"><span data-stu-id="88225-186">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="88225-187">**Запуск** ("Запуск")</span><span class="sxs-lookup"><span data-stu-id="88225-187">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="88225-188">**Остановка** ("остановка")</span><span class="sxs-lookup"><span data-stu-id="88225-188">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="88225-189">**Служба** ("служба")</span><span class="sxs-lookup"><span data-stu-id="88225-189">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="88225-190">**Пренапряжению** ("напряжению")</span><span class="sxs-lookup"><span data-stu-id="88225-190">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="88225-191">**Невосстановление** ("невосстановление")</span><span class="sxs-lookup"><span data-stu-id="88225-191">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="88225-192">**Нет контакта** ("нет контакта")</span><span class="sxs-lookup"><span data-stu-id="88225-192">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="88225-193">**Потеря** связи ("потеря связи")</span><span class="sxs-lookup"><span data-stu-id="88225-193">**Lost Comm** ("Lost Comm")</span></span>


<span data-ttu-id="88225-194"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="88225-194"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="remarks"></a><span data-ttu-id="88225-195">Комментарии</span><span class="sxs-lookup"><span data-stu-id="88225-195">Remarks</span></span>

<span data-ttu-id="88225-196">Класс **\_ системы CIM** является производным от [**CIM \_ логикалелемент**](cim-logicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="88225-196">The **CIM\_System** class is derived from [**CIM\_LogicalElement**](cim-logicalelement.md).</span></span>

<span data-ttu-id="88225-197">Инструментарий WMI не реализует этот класс.</span><span class="sxs-lookup"><span data-stu-id="88225-197">WMI does not implement this class.</span></span> <span data-ttu-id="88225-198">Классы WMI, производные **от \_ системы CIM**, см. в разделе [Классы Win32](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="88225-198">For WMI classes derived from **CIM\_System**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="88225-199">Эта документация является производной от описаний класса CIM, опубликованных в формате DMTF.</span><span class="sxs-lookup"><span data-stu-id="88225-199">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="88225-200">Корпорация Майкрософт могла внести изменения в Исправление незначительных ошибок, соответствовать стандартам документации пакета Microsoft SDK или предоставить дополнительные сведения.</span><span class="sxs-lookup"><span data-stu-id="88225-200">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="88225-201">Требования</span><span class="sxs-lookup"><span data-stu-id="88225-201">Requirements</span></span>



| <span data-ttu-id="88225-202">Требование</span><span class="sxs-lookup"><span data-stu-id="88225-202">Requirement</span></span> | <span data-ttu-id="88225-203">Значение</span><span class="sxs-lookup"><span data-stu-id="88225-203">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="88225-204">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="88225-204">Minimum supported client</span></span><br/> | <span data-ttu-id="88225-205">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="88225-205">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="88225-206">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="88225-206">Minimum supported server</span></span><br/> | <span data-ttu-id="88225-207">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="88225-207">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="88225-208">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="88225-208">Namespace</span></span><br/>                | <span data-ttu-id="88225-209">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="88225-209">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="88225-210">MOF</span><span class="sxs-lookup"><span data-stu-id="88225-210">MOF</span></span><br/>                      | <dl> <span data-ttu-id="88225-211"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="88225-211"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="88225-212">DLL</span><span class="sxs-lookup"><span data-stu-id="88225-212">DLL</span></span><br/>                      | <dl> <span data-ttu-id="88225-213"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="88225-213"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="88225-214">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="88225-214">See also</span></span>

<dl> <dt>

[<span data-ttu-id="88225-215">**\_ЛОГИКАЛЕЛЕМЕНТ CIM**</span><span class="sxs-lookup"><span data-stu-id="88225-215">**CIM\_LogicalElement**</span></span>](cim-logicalelement.md)
</dt> </dl>

 

