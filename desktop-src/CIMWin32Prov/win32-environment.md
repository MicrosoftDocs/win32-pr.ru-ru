---
description: Представляет среду или системный параметр среды в системе Windows.
ms.assetid: da7ee891-c759-4046-a9d8-d3caf66ab5a9
ms.tgt_platform: multiple
title: Класс Win32_Environment
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Environment
- Win32_Environment.Caption
- Win32_Environment.Description
- Win32_Environment.InstallDate
- Win32_Environment.Status
- Win32_Environment.Name
- Win32_Environment.SystemVariable
- Win32_Environment.UserName
- Win32_Environment.VariableValue
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 3b7267e3ac03c14cfc6ad6ca73ede42cc8478b41
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103896482"
---
# <a name="win32_environment-class"></a><span data-ttu-id="80506-103">\_Класс среды Win32</span><span class="sxs-lookup"><span data-stu-id="80506-103">Win32\_Environment class</span></span>

<span data-ttu-id="80506-104">[Класс WMI](/windows/desktop/WmiSdk/retrieving-a-class) **\_ среды Win32** представляет среду или системный параметр среды в системе Windows.</span><span class="sxs-lookup"><span data-stu-id="80506-104">The **Win32\_Environment** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) represents an environment or system environment setting on a Windows computer system.</span></span> <span data-ttu-id="80506-105">Запрос к этому классу Возвращает переменные среды, найденные в:</span><span class="sxs-lookup"><span data-stu-id="80506-105">Querying this class returns environment variables found in:</span></span>

<span data-ttu-id="80506-106">**HKey \_ \_** \\  \\  \\ **Управление** \\  \\ **средой** сессионманажер в системе локального компьютера CurrentControlSet</span><span class="sxs-lookup"><span data-stu-id="80506-106">**HKEY\_LOCAL\_MACHINE**\\**System**\\**CurrentControlSet**\\**Control**\\**Sessionmanager**\\**Environment**</span></span>

<span data-ttu-id="80506-107">и</span><span class="sxs-lookup"><span data-stu-id="80506-107">and</span></span>

<span data-ttu-id="80506-108">**HKey \_** \\ **< Пользовательская >** \\ **Среда**</span><span class="sxs-lookup"><span data-stu-id="80506-108">**HKEY\_USERS**\\**<*user*>**\\**Environment**</span></span>

<span data-ttu-id="80506-109">Следующий пример синтаксиса — упрощенный MOF-код, который включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="80506-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="80506-110">Свойства перечислены в алфавитном порядке, а не в MOF.</span><span class="sxs-lookup"><span data-stu-id="80506-110">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="80506-111">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="80506-111">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), Privileges("SeRestorePrivilege"), UUID("{8502C4D2-5FBB-11D2-AAC1-006008C78BC7}"), SupportsCreate, CreateBy("PutInstance"), SupportsDelete, DeleteBy("DeleteInstance"), SupportsUpdate, AMENDMENT]
class Win32_Environment : CIM_SystemResource
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Status;
  string   Name;
  boolean  SystemVariable;
  string   UserName;
  string   VariableValue;
};
```

## <a name="members"></a><span data-ttu-id="80506-112">Члены</span><span class="sxs-lookup"><span data-stu-id="80506-112">Members</span></span>

<span data-ttu-id="80506-113">Класс **\_ среды Win32** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="80506-113">The **Win32\_Environment** class has these types of members:</span></span>

-   [<span data-ttu-id="80506-114">Свойства</span><span class="sxs-lookup"><span data-stu-id="80506-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="80506-115">Свойства</span><span class="sxs-lookup"><span data-stu-id="80506-115">Properties</span></span>

<span data-ttu-id="80506-116">Класс **\_ среды Win32** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="80506-116">The **Win32\_Environment** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="80506-117">**Заголовок**</span><span class="sxs-lookup"><span data-stu-id="80506-117">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="80506-118">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="80506-118">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="80506-119">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="80506-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="80506-120">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="80506-120">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="80506-121">Краткое текстовое описание объекта.</span><span class="sxs-lookup"><span data-stu-id="80506-121">A short textual description of the object.</span></span>

<span data-ttu-id="80506-122">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="80506-122">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="80506-123">**Описание**</span><span class="sxs-lookup"><span data-stu-id="80506-123">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="80506-124">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="80506-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="80506-125">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="80506-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="80506-126">Квалификаторы: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Описание")</span><span class="sxs-lookup"><span data-stu-id="80506-126">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="80506-127">Текстовое описание объекта.</span><span class="sxs-lookup"><span data-stu-id="80506-127">A textual description of the object.</span></span>

<span data-ttu-id="80506-128">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="80506-128">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="80506-129">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="80506-129">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="80506-130">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="80506-130">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="80506-131">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="80506-131">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="80506-132">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" Дата установки ")</span><span class="sxs-lookup"><span data-stu-id="80506-132">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="80506-133">Указывает, когда был установлен объект.</span><span class="sxs-lookup"><span data-stu-id="80506-133">Indicates when the object was installed.</span></span> <span data-ttu-id="80506-134">Отсутствие значения не означает, что объект не установлен.</span><span class="sxs-lookup"><span data-stu-id="80506-134">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="80506-135">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="80506-135">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="80506-136">**Name**</span><span class="sxs-lookup"><span data-stu-id="80506-136">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="80506-137">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="80506-137">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="80506-138">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="80506-138">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="80506-139">Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("имя"), [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Control \\ \\ Session Manager \\ \\ Environment")</span><span class="sxs-lookup"><span data-stu-id="80506-139">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name"), [**key**](/windows/desktop/WmiSdk/key-qualifier), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry\|System\\\\CurrentControlSet\\\\Control\\\\Session Manager\\\\Environment")</span></span>
</dt> </dl>

<span data-ttu-id="80506-140">Символьная строка, указывающая имя переменной среды на основе Windows.</span><span class="sxs-lookup"><span data-stu-id="80506-140">Character string that specifies the name of a Windows-based environment variable.</span></span> <span data-ttu-id="80506-141">Указав имя переменной, которая еще не существует, приложение создает новую переменную среды.</span><span class="sxs-lookup"><span data-stu-id="80506-141">By specifying the name of a variable that does not yet exist, an application creates a new environment variable.</span></span>

<span data-ttu-id="80506-142">Пример: "Path"</span><span class="sxs-lookup"><span data-stu-id="80506-142">Example: "Path"</span></span>

</dd> <dt>

<span data-ttu-id="80506-143">**Состояние**</span><span class="sxs-lookup"><span data-stu-id="80506-143">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="80506-144">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="80506-144">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="80506-145">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="80506-145">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="80506-146">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("состояние")</span><span class="sxs-lookup"><span data-stu-id="80506-146">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="80506-147">Строка, указывающая текущее состояние объекта.</span><span class="sxs-lookup"><span data-stu-id="80506-147">String that indicates the current status of the object.</span></span> <span data-ttu-id="80506-148">Можно определить операционное и нерабочее состояние.</span><span class="sxs-lookup"><span data-stu-id="80506-148">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="80506-149">Оперативное состояние может включать "ОК", "деградация" и "пред Fail".</span><span class="sxs-lookup"><span data-stu-id="80506-149">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="80506-150">"Пред-Fail" указывает, что элемент работает правильно, но прогнозирует сбой (например, жесткий диск с поддержкой SMART).</span><span class="sxs-lookup"><span data-stu-id="80506-150">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="80506-151">Нерабочее состояние может включать "Error", "starting", "остановка" и "обслуживание".</span><span class="sxs-lookup"><span data-stu-id="80506-151">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="80506-152">"Служба" может применяться при зеркальном отображении дисков, перезагрузке списка разрешений пользователя или выполнении других административных задач.</span><span class="sxs-lookup"><span data-stu-id="80506-152">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="80506-153">Не вся такая работа находится в оперативном режиме, но управляемый элемент не является ни "ОК", ни в одном из других состояний.</span><span class="sxs-lookup"><span data-stu-id="80506-153">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="80506-154">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="80506-154">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="80506-155">В эти значения входят:</span><span class="sxs-lookup"><span data-stu-id="80506-155">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="80506-156">**ОК** ("ОК")</span><span class="sxs-lookup"><span data-stu-id="80506-156">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="80506-157">**Ошибка** ("ошибка")</span><span class="sxs-lookup"><span data-stu-id="80506-157">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="80506-158">**Пониженная работоспособность** (пониженная работоспособность)</span><span class="sxs-lookup"><span data-stu-id="80506-158">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="80506-159">**Неизвестно** ("неизвестно")</span><span class="sxs-lookup"><span data-stu-id="80506-159">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="80506-160">**Пред-ошибка** ("пред Fail")</span><span class="sxs-lookup"><span data-stu-id="80506-160">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="80506-161">**Запуск** ("Запуск")</span><span class="sxs-lookup"><span data-stu-id="80506-161">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="80506-162">**Остановка** ("остановка")</span><span class="sxs-lookup"><span data-stu-id="80506-162">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="80506-163">**Служба** ("служба")</span><span class="sxs-lookup"><span data-stu-id="80506-163">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="80506-164">**Пренапряжению** ("напряжению")</span><span class="sxs-lookup"><span data-stu-id="80506-164">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="80506-165">**Невосстановление** ("невосстановление")</span><span class="sxs-lookup"><span data-stu-id="80506-165">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="80506-166">**Нет контакта** ("нет контакта")</span><span class="sxs-lookup"><span data-stu-id="80506-166">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="80506-167">**Потеря** связи ("потеря связи")</span><span class="sxs-lookup"><span data-stu-id="80506-167">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="80506-168">**системвариабле**</span><span class="sxs-lookup"><span data-stu-id="80506-168">**SystemVariable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="80506-169">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="80506-169">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="80506-170">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="80506-170">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="80506-171">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Control \\ \\ Configuration Manager \\ \\ Environment")</span><span class="sxs-lookup"><span data-stu-id="80506-171">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry\|System\\\\CurrentControlSet\\\\Control\\\\Session Manager\\\\Environment")</span></span>
</dt> </dl>

<span data-ttu-id="80506-172">Указывает, является ли переменная системной переменной.</span><span class="sxs-lookup"><span data-stu-id="80506-172">Indicates whether the variable is a system variable.</span></span> <span data-ttu-id="80506-173">Системная переменная задается операционной системой и не зависит от параметров среды пользователя.</span><span class="sxs-lookup"><span data-stu-id="80506-173">A system variable is set by the operating system, and is independent from user environment settings.</span></span>

</dd> <dt>

<span data-ttu-id="80506-174">**UserName**</span><span class="sxs-lookup"><span data-stu-id="80506-174">**UserName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="80506-175">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="80506-175">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="80506-176">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="80506-176">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="80506-177">Квалификаторы: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (260), [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| система \\ \\ CurrentControlSet \\ \\ управляющего \\ \\ сеанса диспетчером сеансов \\ \\ ")</span><span class="sxs-lookup"><span data-stu-id="80506-177">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (260), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry\|System\\\\CurrentControlSet\\\\Control\\\\Session Manager\\\\Environment")</span></span>
</dt> </dl>

<span data-ttu-id="80506-178">Имя владельца параметра среды.</span><span class="sxs-lookup"><span data-stu-id="80506-178">Name of the owner of the environment setting.</span></span> <span data-ttu-id="80506-179">Он имеет значение <SYSTEM> для параметров, характерных для системы Windows (в отличие от конкретного пользователя) и <DEFAULT> параметров пользователя по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="80506-179">It is set to <SYSTEM> for settings that are specific to the Windows-based system (as opposed to a specific user) and <DEFAULT> for default user settings.</span></span>

<span data-ttu-id="80506-180">Пример: "JSmith"</span><span class="sxs-lookup"><span data-stu-id="80506-180">Example: "JSmith"</span></span>

</dd> <dt>

<span data-ttu-id="80506-181">**вариаблевалуе**</span><span class="sxs-lookup"><span data-stu-id="80506-181">**VariableValue**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="80506-182">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="80506-182">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="80506-183">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="80506-183">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="80506-184">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Control \\ \\ Configuration Manager \\ \\ Environment")</span><span class="sxs-lookup"><span data-stu-id="80506-184">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry\|System\\\\CurrentControlSet\\\\Control\\\\Session Manager\\\\Environment")</span></span>
</dt> </dl>

<span data-ttu-id="80506-185">Заполнитель переменной среды на основе Windows.</span><span class="sxs-lookup"><span data-stu-id="80506-185">Placeholder variable of a Windows-based environment variable.</span></span> <span data-ttu-id="80506-186">Такие сведения, как каталог файловой системы, могут изменяться с компьютера на компьютер.</span><span class="sxs-lookup"><span data-stu-id="80506-186">Information like the file system directory can change from computer to computer.</span></span> <span data-ttu-id="80506-187">Операционная система заменяет заполнители для них.</span><span class="sxs-lookup"><span data-stu-id="80506-187">The operating system substitutes placeholders for these.</span></span>

<span data-ttu-id="80506-188">Пример: "% SystemRoot%"</span><span class="sxs-lookup"><span data-stu-id="80506-188">Example: "%SystemRoot%"</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="80506-189">Комментарии</span><span class="sxs-lookup"><span data-stu-id="80506-189">Remarks</span></span>

<span data-ttu-id="80506-190">Класс **\_ среды Win32** является производным от [**CIM \_ системресаурце**](cim-systemresource.md).</span><span class="sxs-lookup"><span data-stu-id="80506-190">The **Win32\_Environment** class is derived from [**CIM\_SystemResource**](cim-systemresource.md).</span></span> <span data-ttu-id="80506-191">Этот класс можно использовать для поиска путей к специальным папкам, таким как системная папка или программные файлы на удаленном компьютере.</span><span class="sxs-lookup"><span data-stu-id="80506-191">You can use this class to find the paths of special folders such as the System folder or Program files on a remote machine.</span></span> <span data-ttu-id="80506-192">Вот некоторые примеры: WINDIR, системный_корневой_каталог, ProgramFiles и UserProfile.</span><span class="sxs-lookup"><span data-stu-id="80506-192">Some examples are: windir, systemroot, programfiles, and userprofile.</span></span> <span data-ttu-id="80506-193">**Win32 \_ Среда** по сути возвращает сведения о том, что можно найти в:</span><span class="sxs-lookup"><span data-stu-id="80506-193">**Win32\_Environment** basically returns what can be found in:</span></span>

<span data-ttu-id="80506-194">**HKey \_ \_** \\  \\  \\ **Управление** \\  \\ **средой** сессионманажер в системе локального компьютера CurrentControlSet</span><span class="sxs-lookup"><span data-stu-id="80506-194">**HKEY\_LOCAL\_MACHINE**\\**System**\\**CurrentControlSet**\\**Control**\\**Sessionmanager**\\**Environment**</span></span>

<span data-ttu-id="80506-195">и</span><span class="sxs-lookup"><span data-stu-id="80506-195">and</span></span>

<span data-ttu-id="80506-196">**HKey \_** \\ **< Пользовательская >** \\ **Среда**</span><span class="sxs-lookup"><span data-stu-id="80506-196">**HKEY\_USERS**\\**<*user*>**\\**Environment**</span></span>

<span data-ttu-id="80506-197">Вызывающий процесс, использующий этот класс, должен иметь привилегию **SE \_ reside \_ Name** на компьютере, где размещается реестр.</span><span class="sxs-lookup"><span data-stu-id="80506-197">The calling process that uses this class must have the **SE\_RESTORE\_NAME** privilege on the computer in which the registry resides.</span></span> <span data-ttu-id="80506-198">Например, если перечислить этот класс на локальном компьютере, учетная запись, под которой выполняется приложение, должна иметь эту привилегию.</span><span class="sxs-lookup"><span data-stu-id="80506-198">For example, if you enumerate this class on the local computer, the account under which your application runs must have this privilege.</span></span> <span data-ttu-id="80506-199">Дополнительные сведения см. в разделе [выполнение привилегированных операций](/windows/desktop/WmiSdk/executing-privileged-operations).</span><span class="sxs-lookup"><span data-stu-id="80506-199">For more information, see [Executing Privileged Operations](/windows/desktop/WmiSdk/executing-privileged-operations).</span></span>

## <a name="examples"></a><span data-ttu-id="80506-200">Примеры</span><span class="sxs-lookup"><span data-stu-id="80506-200">Examples</span></span>

<span data-ttu-id="80506-201">В примере [переменных среды на компьютере на основе](https://Gallery.TechNet.Microsoft.Com/79ae998e-2e29-4a6d-b0a6-34ed5b709d49) Perl для получения сведений обо всех переменных среды на компьютере используется инструментарий WMI.</span><span class="sxs-lookup"><span data-stu-id="80506-201">The [List Environment Variables on a Computer](https://Gallery.TechNet.Microsoft.Com/79ae998e-2e29-4a6d-b0a6-34ed5b709d49) Perl sample uses WMI to return information about all the environment variables on a computer.</span></span>

<span data-ttu-id="80506-202">В следующем примере кода VBScript перечисляются переменные среды на локальном компьютере.</span><span class="sxs-lookup"><span data-stu-id="80506-202">The following VBScript code example enumerates the environment variables on the local computer.</span></span>


```VB
strComputer = "."
Set objWMIService = GetObject("winmgmts:\\" & strComputer & "\root\cimv2")
Set colVar = objWMIService.ExecQuery("Select * from Win32_Environment")
For Each objVar in colVar
    Wscript.Echo "Description: " & objVar.Description & VBNewLine _
               & "Name: " & objVar.Name & VBNewLine _
               & "System Variable: " & objVar.SystemVariable & VBNewLine _
               & "User Name: " & objVar.UserName & VBNewLine _
               & "Variable Value: " & objVar.VariableValue 
Next
```



<span data-ttu-id="80506-203">Следующий пример кода на языке VBScript изменяет переменную среды с именем BUILD \_ на значение, введенное пользователем.</span><span class="sxs-lookup"><span data-stu-id="80506-203">The following VBScript code example changes an environment variable named BUILD\_TYPE to a value input by the user.</span></span> <span data-ttu-id="80506-204">В скрипте предполагается, что \_ переменная типа сборки уже существует.</span><span class="sxs-lookup"><span data-stu-id="80506-204">The script assumes that the BUILD\_TYPE variable already exists.</span></span> <span data-ttu-id="80506-205">Если он не существует, сценарий завершается.</span><span class="sxs-lookup"><span data-stu-id="80506-205">If it does not exist then the script ends.</span></span> <span data-ttu-id="80506-206">Входное значение проверяется: оно должно быть "Build1", "Build2" или "Build3", а другое значение не принимается.</span><span class="sxs-lookup"><span data-stu-id="80506-206">The input value is checked: it must be either "Build1", "Build2", or "Build3", and no other value is accepted.</span></span> <span data-ttu-id="80506-207">Функция VBScript [Укасе](https://msdn.microsoft.com/library/aa902519.aspx) делает нечувствительным к входу регистр.</span><span class="sxs-lookup"><span data-stu-id="80506-207">The VBScript [UCase](https://msdn.microsoft.com/library/aa902519.aspx) function makes the input case-insensitive.</span></span> <span data-ttu-id="80506-208">Если значение, введенное в, не является одним из трех допустимых значений, сценарий завершается.</span><span class="sxs-lookup"><span data-stu-id="80506-208">If what is typed in is not one of the three acceptable values, the script ends.</span></span>


```VB
On Error Resume Next
strComputer = "."
Set objWMIService = GetObject("winmgmts:\\" & strComputer & "\root\cimv2")
Set colItems = objWMIService.ExecQuery("Select * from Win32_Environment")
Found = False
For Each objItem in colItems
    If objItem.Name = "BUILD_TYPE" Then
    Found = True
    Change = UCase(InputBox("BUILD_TYPE currently = " & objItem.VariableValue & VBNewLine _
                          & "Change options are Build1, Build2, Build3 "))
        If UCase(Change) = "BUILD1" OR Change = "BUILD2" OR Change = "BUILD3" Then
            objItem.VariableValue = Change
            objItem.Put_
        WScript.Echo "BUILD_TYPE changed to " & objItem.VariableValue
        Else 
        WScript.Echo "No input or unacceptable input." & " No change to BUILD_TYPE"
        End If
    End If
Next
If Found = False Then
    WScript.Echo "User-defined environment variable BUILD_TYPE not found."
End If
```



## <a name="requirements"></a><span data-ttu-id="80506-209">Требования</span><span class="sxs-lookup"><span data-stu-id="80506-209">Requirements</span></span>



| <span data-ttu-id="80506-210">Требование</span><span class="sxs-lookup"><span data-stu-id="80506-210">Requirement</span></span> | <span data-ttu-id="80506-211">Значение</span><span class="sxs-lookup"><span data-stu-id="80506-211">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="80506-212">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="80506-212">Minimum supported client</span></span><br/> | <span data-ttu-id="80506-213">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="80506-213">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="80506-214">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="80506-214">Minimum supported server</span></span><br/> | <span data-ttu-id="80506-215">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="80506-215">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="80506-216">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="80506-216">Namespace</span></span><br/>                | <span data-ttu-id="80506-217">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="80506-217">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="80506-218">MOF</span><span class="sxs-lookup"><span data-stu-id="80506-218">MOF</span></span><br/>                      | <dl> <span data-ttu-id="80506-219"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="80506-219"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="80506-220">DLL</span><span class="sxs-lookup"><span data-stu-id="80506-220">DLL</span></span><br/>                      | <dl> <span data-ttu-id="80506-221"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="80506-221"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="80506-222">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="80506-222">See also</span></span>

<dl> <dt>

[<span data-ttu-id="80506-223">**\_СИСТЕМРЕСАУРЦЕ CIM**</span><span class="sxs-lookup"><span data-stu-id="80506-223">**CIM\_SystemResource**</span></span>](cim-systemresource.md)
</dt> <dt>

<span data-ttu-id="80506-224">[Классы операционной системы](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="80506-224">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> </dl>

 

