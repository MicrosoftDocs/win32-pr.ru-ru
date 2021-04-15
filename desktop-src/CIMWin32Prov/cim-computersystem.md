---
description: '\_Класс COMPUTERSYSTEM CIM представляет специальную коллекцию \_ экземпляров CIM манажедсистемелемент.'
ms.assetid: c4fd0598-3cb3-428f-ad39-a14232ef7c17
ms.tgt_platform: multiple
title: Класс CIM_ComputerSystem (поставщики WMI CIMWin32)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ComputerSystem
- CIM_ComputerSystem.Caption
- CIM_ComputerSystem.Description
- CIM_ComputerSystem.InstallDate
- CIM_ComputerSystem.Status
- CIM_ComputerSystem.CreationClassName
- CIM_ComputerSystem.Name
- CIM_ComputerSystem.PrimaryOwnerContact
- CIM_ComputerSystem.PrimaryOwnerName
- CIM_ComputerSystem.Roles
- CIM_ComputerSystem.NameFormat
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: c4645a8d4b2440b0b102658d3eca74d825d774dc
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104496404"
---
# <a name="cim_computersystem-class-cimwin32-wmi-providers"></a><span data-ttu-id="c488b-103">Класс CIM_ComputerSystem (поставщики WMI CIMWin32)</span><span class="sxs-lookup"><span data-stu-id="c488b-103">CIM_ComputerSystem class (CIMWin32 WMI Providers)</span></span>

<span data-ttu-id="c488b-104">Класс **\_ ComputerSystem CIM** представляет специальную коллекцию экземпляров [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md) .</span><span class="sxs-lookup"><span data-stu-id="c488b-104">A **CIM\_ComputerSystem** class represents a special collection of [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md) instances.</span></span> <span data-ttu-id="c488b-105">Эта коллекция предоставляет возможности компьютера и служит в качестве точки статистической обработки для связывания одного или нескольких следующих элементов: файловой системы, операционной системы, процессора и памяти (Энергозависимое и энергонезависимое хранилище).</span><span class="sxs-lookup"><span data-stu-id="c488b-105">This collection provides computer capabilities and serves as an aggregation point to associate one or more of the following elements: file system, operating system, processor and memory (volatile and non-volatile storage).</span></span> <span data-ttu-id="c488b-106">Этот класс является производным [**от \_ системы CIM**](cim-system.md).</span><span class="sxs-lookup"><span data-stu-id="c488b-106">This class is derived from [**CIM\_System**](cim-system.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="c488b-107">Классы CIM (модель CIM) в DMTF (распределенная задача управления) являются родительскими классами, на которых строятся классы WMI.</span><span class="sxs-lookup"><span data-stu-id="c488b-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="c488b-108">В настоящее время WMI поддерживает только [схемы версии CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="c488b-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="c488b-109">Приведенный ниже синтаксис является упрощенной версией кода MOF и включает все унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="c488b-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="c488b-110">Свойства перечислены в алфавитном порядке, а не в MOF.</span><span class="sxs-lookup"><span data-stu-id="c488b-110">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="c488b-111">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c488b-111">Syntax</span></span>

``` syntax
[Abstract, UUID("{8502C525-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class CIM_ComputerSystem : CIM_System
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Status;
  string   CreationClassName;
  string   Name;
  string   PrimaryOwnerContact;
  string   PrimaryOwnerName;
  string   Roles[];
  string   NameFormat;
};
```

## <a name="members"></a><span data-ttu-id="c488b-112">Члены</span><span class="sxs-lookup"><span data-stu-id="c488b-112">Members</span></span>

<span data-ttu-id="c488b-113">Класс **CIM \_ ComputerSystem** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="c488b-113">The **CIM\_ComputerSystem** class has these types of members:</span></span>

-   [<span data-ttu-id="c488b-114">Свойства</span><span class="sxs-lookup"><span data-stu-id="c488b-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="c488b-115">Свойства</span><span class="sxs-lookup"><span data-stu-id="c488b-115">Properties</span></span>

<span data-ttu-id="c488b-116">Класс **CIM \_ ComputerSystem** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="c488b-116">The **CIM\_ComputerSystem** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="c488b-117">**Заголовок**</span><span class="sxs-lookup"><span data-stu-id="c488b-117">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c488b-118">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="c488b-118">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c488b-119">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c488b-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c488b-120">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="c488b-120">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="c488b-121">Краткое текстовое описание объекта.</span><span class="sxs-lookup"><span data-stu-id="c488b-121">A short textual description of the object.</span></span>

<span data-ttu-id="c488b-122">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="c488b-122">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="c488b-123">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="c488b-123">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c488b-124">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="c488b-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c488b-125">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c488b-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c488b-126">Квалификаторы: [ **\_ ключ CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="c488b-126">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="c488b-127">Имя класса или подкласса, используемого при создании экземпляра.</span><span class="sxs-lookup"><span data-stu-id="c488b-127">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="c488b-128">При использовании с другими ключевыми свойствами класса это свойство позволяет однозначно идентифицировать все экземпляры класса и его подклассов.</span><span class="sxs-lookup"><span data-stu-id="c488b-128">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="c488b-129">Это свойство наследуется [**от \_ системы CIM**](cim-system.md).</span><span class="sxs-lookup"><span data-stu-id="c488b-129">This property is inherited from [**CIM\_System**](cim-system.md).</span></span>

</dd> <dt>

<span data-ttu-id="c488b-130">**Описание**</span><span class="sxs-lookup"><span data-stu-id="c488b-130">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c488b-131">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="c488b-131">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c488b-132">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c488b-132">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c488b-133">Квалификаторы: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Описание")</span><span class="sxs-lookup"><span data-stu-id="c488b-133">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="c488b-134">Текстовое описание объекта.</span><span class="sxs-lookup"><span data-stu-id="c488b-134">A textual description of the object.</span></span>

<span data-ttu-id="c488b-135">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="c488b-135">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="c488b-136">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="c488b-136">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c488b-137">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="c488b-137">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="c488b-138">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c488b-138">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c488b-139">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" Дата установки ")</span><span class="sxs-lookup"><span data-stu-id="c488b-139">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="c488b-140">Указывает, когда был установлен объект.</span><span class="sxs-lookup"><span data-stu-id="c488b-140">Indicates when the object was installed.</span></span> <span data-ttu-id="c488b-141">Отсутствие значения не означает, что объект не установлен.</span><span class="sxs-lookup"><span data-stu-id="c488b-141">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="c488b-142">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="c488b-142">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="c488b-143">**Name**</span><span class="sxs-lookup"><span data-stu-id="c488b-143">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c488b-144">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="c488b-144">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c488b-145">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c488b-145">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c488b-146">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="c488b-146">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="c488b-147">Определяет метку, по которой известен объект.</span><span class="sxs-lookup"><span data-stu-id="c488b-147">Defines the label by which the object is known.</span></span>

<span data-ttu-id="c488b-148">Это свойство наследуется [**от \_ системы CIM**](cim-system.md).</span><span class="sxs-lookup"><span data-stu-id="c488b-148">This property is inherited from [**CIM\_System**](cim-system.md).</span></span>

</dd> <dt>

<span data-ttu-id="c488b-149">**намеформат**</span><span class="sxs-lookup"><span data-stu-id="c488b-149">**NameFormat**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c488b-150">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="c488b-150">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c488b-151">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c488b-151">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c488b-152">Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("намеформат")</span><span class="sxs-lookup"><span data-stu-id="c488b-152">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("NameFormat")</span></span>
</dt> </dl>

<span data-ttu-id="c488b-153">Определяет, как создается имя системы компьютера с помощью эвристического алгоритма.</span><span class="sxs-lookup"><span data-stu-id="c488b-153">Identifies how the computer system name is generated, using a heuristic.</span></span> <span data-ttu-id="c488b-154">Эвристический подход подробно описан в спецификации общей модели CIM V2.</span><span class="sxs-lookup"><span data-stu-id="c488b-154">The heuristic is outlined, in detail, in the CIM V2 Common Model specification.</span></span> <span data-ttu-id="c488b-155">Предполагается, что документированные правила обходятся по порядку, чтобы определить и назначить имя.</span><span class="sxs-lookup"><span data-stu-id="c488b-155">It assumes that the documented rules are traversed in order, to determine and assign a name.</span></span> <span data-ttu-id="c488b-156">Список значений **намеформат** определяет порядок приоритета при назначении имени системы компьютера.</span><span class="sxs-lookup"><span data-stu-id="c488b-156">The **NameFormat** values list defines the precedence order for assigning the computer system name.</span></span> <span data-ttu-id="c488b-157">Несколько правил сопоставляются с одним и тем же значением.</span><span class="sxs-lookup"><span data-stu-id="c488b-157">Several rules do map to the same Value.</span></span>

<span data-ttu-id="c488b-158">Обратите внимание, что **имя** объекта вычисляется с использованием эвристического алгоритма — значение ключа системы.</span><span class="sxs-lookup"><span data-stu-id="c488b-158">Note that the object's **Name** is calculated using the heuristic is the system's key value.</span></span> <span data-ttu-id="c488b-159">Другие имена можно назначать и использовать для объекта, который лучше подходит для бизнеса, используя псевдонимы.</span><span class="sxs-lookup"><span data-stu-id="c488b-159">Other names can be assigned and used for the object that better suit the business, using Aliases.</span></span>

<dt>

<span id="IP"></span><span id="ip"></span>

<span data-ttu-id="c488b-160">**IP-адрес** ("IP")</span><span class="sxs-lookup"><span data-stu-id="c488b-160">**IP** ("IP")</span></span>


</dt> <dd></dd> <dt>

<span id="Dial"></span><span id="dial"></span><span id="DIAL"></span>

<span data-ttu-id="c488b-161">**Набрать номер** ("набрать")</span><span class="sxs-lookup"><span data-stu-id="c488b-161">**Dial** ("Dial")</span></span>


</dt> <dd></dd> <dt>

<span id="HID"></span><span id="hid"></span>

<span data-ttu-id="c488b-162">**HID** (HID)</span><span class="sxs-lookup"><span data-stu-id="c488b-162">**HID** ("HID")</span></span>


</dt> <dd></dd> <dt>

<span id="NWA"></span><span id="nwa"></span>

<span data-ttu-id="c488b-163">**НВА** ("НВА")</span><span class="sxs-lookup"><span data-stu-id="c488b-163">**NWA** ("NWA")</span></span>


</dt> <dd></dd> <dt>

<span id="HWA"></span><span id="hwa"></span>

<span data-ttu-id="c488b-164">**Хва** ("Хва")</span><span class="sxs-lookup"><span data-stu-id="c488b-164">**HWA** ("HWA")</span></span>


</dt> <dd></dd> <dt>

<span id="X25"></span><span id="x25"></span>

<span data-ttu-id="c488b-165">**X25** ("x25")</span><span class="sxs-lookup"><span data-stu-id="c488b-165">**X25** ("X25")</span></span>


</dt> <dd></dd> <dt>

<span id="ISDN"></span><span id="isdn"></span>

<span data-ttu-id="c488b-166">**ISDN** (ISDN)</span><span class="sxs-lookup"><span data-stu-id="c488b-166">**ISDN** ("ISDN")</span></span>


</dt> <dd></dd> <dt>

<span id="IPX"></span><span id="ipx"></span>

<span data-ttu-id="c488b-167">**IPX** ("IPX")</span><span class="sxs-lookup"><span data-stu-id="c488b-167">**IPX** ("IPX")</span></span>


</dt> <dd></dd> <dt>

<span id="DCC"></span><span id="dcc"></span>

<span data-ttu-id="c488b-168">**ДКК** ("ДКК")</span><span class="sxs-lookup"><span data-stu-id="c488b-168">**DCC** ("DCC")</span></span>


</dt> <dd></dd> <dt>

<span id="ICD"></span><span id="icd"></span>

<span data-ttu-id="c488b-169">**ICD** ("ICD")</span><span class="sxs-lookup"><span data-stu-id="c488b-169">**ICD** ("ICD")</span></span>


</dt> <dd></dd> <dt>

<span id="E.164"></span><span id="e.164"></span>

<span data-ttu-id="c488b-170">**E. 164** ("E. 164")</span><span class="sxs-lookup"><span data-stu-id="c488b-170">**E.164** ("E.164")</span></span>


</dt> <dd></dd> <dt>

<span id="SNA"></span><span id="sna"></span>

<span data-ttu-id="c488b-171">**SNA** ("SNA")</span><span class="sxs-lookup"><span data-stu-id="c488b-171">**SNA** ("SNA")</span></span>


</dt> <dd></dd> <dt>

<span id="OID_OSI"></span><span id="oid_osi"></span>

<span data-ttu-id="c488b-172">**OID/OSI** ("OID/OSI")</span><span class="sxs-lookup"><span data-stu-id="c488b-172">**OID/OSI** ("OID/OSI")</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="c488b-173">**Другое** ("другое")</span><span class="sxs-lookup"><span data-stu-id="c488b-173">**Other** ("Other")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="c488b-174">**примарйовнерконтакт**</span><span class="sxs-lookup"><span data-stu-id="c488b-174">**PrimaryOwnerContact**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c488b-175">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="c488b-175">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c488b-176">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c488b-176">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c488b-177">Способ достижения основного владельца системы (например, номер телефона или адрес электронной почты).</span><span class="sxs-lookup"><span data-stu-id="c488b-177">How the primary system owner can be reached (for example, phone number or email address).</span></span>

<span data-ttu-id="c488b-178">Это свойство наследуется [**от \_ системы CIM**](cim-system.md).</span><span class="sxs-lookup"><span data-stu-id="c488b-178">This property is inherited from [**CIM\_System**](cim-system.md).</span></span>

</dd> <dt>

<span data-ttu-id="c488b-179">**примарйовнернаме**</span><span class="sxs-lookup"><span data-stu-id="c488b-179">**PrimaryOwnerName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c488b-180">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="c488b-180">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c488b-181">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c488b-181">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c488b-182">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="c488b-182">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="c488b-183">Имя основного владельца системы.</span><span class="sxs-lookup"><span data-stu-id="c488b-183">Name of the primary system owner.</span></span>

<span data-ttu-id="c488b-184">Это свойство наследуется [**от \_ системы CIM**](cim-system.md).</span><span class="sxs-lookup"><span data-stu-id="c488b-184">This property is inherited from [**CIM\_System**](cim-system.md).</span></span>

</dd> <dt>

<span data-ttu-id="c488b-185">**Роли**</span><span class="sxs-lookup"><span data-stu-id="c488b-185">**Roles**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c488b-186">Тип данных: массив **строк**</span><span class="sxs-lookup"><span data-stu-id="c488b-186">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="c488b-187">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="c488b-187">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="c488b-188">Роли, которые система играет в среде информационных технологий.</span><span class="sxs-lookup"><span data-stu-id="c488b-188">Roles the system plays in the information technology environment.</span></span> <span data-ttu-id="c488b-189">Подклассы системы могут переопределять это свойство для определения явных значений ролей.</span><span class="sxs-lookup"><span data-stu-id="c488b-189">Subclasses of the system can override this property to define explicit role values.</span></span> <span data-ttu-id="c488b-190">Кроме того, Рабочая группа может описывать эвристику, соглашения и правила для указания ролей.</span><span class="sxs-lookup"><span data-stu-id="c488b-190">Alternately, a working group can describe the heuristics, conventions, and guidelines for specifying roles.</span></span> <span data-ttu-id="c488b-191">Например, для экземпляра сетевой системы это свойство может содержать строку "Switch" или "Bridge".</span><span class="sxs-lookup"><span data-stu-id="c488b-191">For example, for an instance of a networking system, this property might contain the string "Switch" or "Bridge".</span></span>

<span data-ttu-id="c488b-192">Это свойство наследуется [**от \_ системы CIM**](cim-system.md).</span><span class="sxs-lookup"><span data-stu-id="c488b-192">This property is inherited from [**CIM\_System**](cim-system.md).</span></span>

</dd> <dt>

<span data-ttu-id="c488b-193">**Состояние**</span><span class="sxs-lookup"><span data-stu-id="c488b-193">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c488b-194">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="c488b-194">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c488b-195">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c488b-195">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c488b-196">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("состояние")</span><span class="sxs-lookup"><span data-stu-id="c488b-196">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="c488b-197">Строка, указывающая текущее состояние объекта.</span><span class="sxs-lookup"><span data-stu-id="c488b-197">String that indicates the current status of the object.</span></span> <span data-ttu-id="c488b-198">Можно определить операционное и нерабочее состояние.</span><span class="sxs-lookup"><span data-stu-id="c488b-198">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="c488b-199">Оперативное состояние может включать "ОК", "деградация" и "пред Fail".</span><span class="sxs-lookup"><span data-stu-id="c488b-199">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="c488b-200">"Пред-Fail" указывает, что элемент работает правильно, но прогнозирует сбой (например, жесткий диск с поддержкой SMART).</span><span class="sxs-lookup"><span data-stu-id="c488b-200">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="c488b-201">Нерабочее состояние может включать "Error", "starting", "остановка" и "обслуживание".</span><span class="sxs-lookup"><span data-stu-id="c488b-201">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="c488b-202">"Служба" может применяться при зеркальном отображении дисков, перезагрузке списка разрешений пользователя или выполнении других административных задач.</span><span class="sxs-lookup"><span data-stu-id="c488b-202">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="c488b-203">Не вся такая работа находится в оперативном режиме, но управляемый элемент не является ни "ОК", ни в одном из других состояний.</span><span class="sxs-lookup"><span data-stu-id="c488b-203">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="c488b-204">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="c488b-204">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="c488b-205">В эти значения входят:</span><span class="sxs-lookup"><span data-stu-id="c488b-205">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="c488b-206">**ОК** ("ОК")</span><span class="sxs-lookup"><span data-stu-id="c488b-206">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="c488b-207">**Ошибка** ("ошибка")</span><span class="sxs-lookup"><span data-stu-id="c488b-207">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="c488b-208">**Пониженная работоспособность** (пониженная работоспособность)</span><span class="sxs-lookup"><span data-stu-id="c488b-208">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="c488b-209">**Неизвестно** ("неизвестно")</span><span class="sxs-lookup"><span data-stu-id="c488b-209">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="c488b-210">**Пред-ошибка** ("пред Fail")</span><span class="sxs-lookup"><span data-stu-id="c488b-210">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="c488b-211">**Запуск** ("Запуск")</span><span class="sxs-lookup"><span data-stu-id="c488b-211">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="c488b-212">**Остановка** ("остановка")</span><span class="sxs-lookup"><span data-stu-id="c488b-212">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="c488b-213">**Служба** ("служба")</span><span class="sxs-lookup"><span data-stu-id="c488b-213">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="c488b-214">**Пренапряжению** ("напряжению")</span><span class="sxs-lookup"><span data-stu-id="c488b-214">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="c488b-215">**Невосстановление** ("невосстановление")</span><span class="sxs-lookup"><span data-stu-id="c488b-215">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="c488b-216">**Нет контакта** ("нет контакта")</span><span class="sxs-lookup"><span data-stu-id="c488b-216">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="c488b-217">**Потеря** связи ("потеря связи")</span><span class="sxs-lookup"><span data-stu-id="c488b-217">**Lost Comm** ("Lost Comm")</span></span>


<span data-ttu-id="c488b-218"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="c488b-218"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="remarks"></a><span data-ttu-id="c488b-219">Комментарии</span><span class="sxs-lookup"><span data-stu-id="c488b-219">Remarks</span></span>

<span data-ttu-id="c488b-220">Класс **\_ ComputerSystem CIM** является производным от [**\_ системы CIM**](cim-system.md).</span><span class="sxs-lookup"><span data-stu-id="c488b-220">The **CIM\_ComputerSystem** class is derived from [**CIM\_System**](cim-system.md).</span></span>

<span data-ttu-id="c488b-221">Инструментарий WMI не реализует этот класс.</span><span class="sxs-lookup"><span data-stu-id="c488b-221">WMI does not implement this class.</span></span> <span data-ttu-id="c488b-222">Дополнительные сведения о классах, производных от **CIM \_ ComputerSystem**, см. в разделе [Классы Win32](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="c488b-222">For more information about classes derived from **CIM\_ComputerSystem**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="c488b-223">Эта документация является производной от описаний класса CIM, опубликованных в формате DMTF.</span><span class="sxs-lookup"><span data-stu-id="c488b-223">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="c488b-224">Корпорация Майкрософт могла внести изменения в Исправление незначительных ошибок, соответствовать стандартам документации пакета Microsoft SDK или предоставить дополнительные сведения.</span><span class="sxs-lookup"><span data-stu-id="c488b-224">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="c488b-225">Требования</span><span class="sxs-lookup"><span data-stu-id="c488b-225">Requirements</span></span>



| <span data-ttu-id="c488b-226">Требование</span><span class="sxs-lookup"><span data-stu-id="c488b-226">Requirement</span></span> | <span data-ttu-id="c488b-227">Значение</span><span class="sxs-lookup"><span data-stu-id="c488b-227">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c488b-228">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="c488b-228">Minimum supported client</span></span><br/> | <span data-ttu-id="c488b-229">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="c488b-229">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="c488b-230">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="c488b-230">Minimum supported server</span></span><br/> | <span data-ttu-id="c488b-231">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c488b-231">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="c488b-232">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="c488b-232">Namespace</span></span><br/>                | <span data-ttu-id="c488b-233">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="c488b-233">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="c488b-234">MOF</span><span class="sxs-lookup"><span data-stu-id="c488b-234">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c488b-235"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="c488b-235"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="c488b-236">DLL</span><span class="sxs-lookup"><span data-stu-id="c488b-236">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c488b-237"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c488b-237"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c488b-238">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c488b-238">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c488b-239">**\_Система CIM**</span><span class="sxs-lookup"><span data-stu-id="c488b-239">**CIM\_System**</span></span>](cim-system.md)
</dt> </dl>

 

