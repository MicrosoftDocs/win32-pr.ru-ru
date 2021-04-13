---
description: '&Win32 \_ логикалпрограмграупитем \# 8194; Класс WMI представляет элемент, содержащийся в \_ Логикалпрограмграуп Win32, который также не является другим \_ экземпляром логикалпрограмграуп Win32.'
ms.assetid: 70b127bf-4e94-4c1a-98ff-909bdfe0f009
ms.tgt_platform: multiple
title: Класс Win32_LogicalProgramGroupItem
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_LogicalProgramGroupItem
- Win32_LogicalProgramGroupItem.Caption
- Win32_LogicalProgramGroupItem.Description
- Win32_LogicalProgramGroupItem.InstallDate
- Win32_LogicalProgramGroupItem.Status
- Win32_LogicalProgramGroupItem.Name
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 1afd78ba17e444520d8dec81eac05fffa103aede
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104539359"
---
# <a name="win32_logicalprogramgroupitem-class"></a><span data-ttu-id="c50e1-103">\_Класс Win32 логикалпрограмграупитем</span><span class="sxs-lookup"><span data-stu-id="c50e1-103">Win32\_LogicalProgramGroupItem class</span></span>

<span data-ttu-id="c50e1-104">Класс **WMI \_ логикалпрограмграупитем** [инструментария](/windows/desktop/WmiSdk/retrieving-a-class) Win32 представляет элемент, содержащийся [**в \_ логикалпрограмграуп Win32**](win32-logicalprogramgroup.md) , который не является также другим экземпляром **Win32 \_ логикалпрограмграуп** .</span><span class="sxs-lookup"><span data-stu-id="c50e1-104">The **Win32\_LogicalProgramGroupItem** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) represents an element contained by a [**Win32\_LogicalProgramGroup**](win32-logicalprogramgroup.md) that is not also another **Win32\_LogicalProgramGroup** instance.</span></span>

<span data-ttu-id="c50e1-105">Следующий пример синтаксиса — упрощенный MOF-код, который включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="c50e1-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="c50e1-106">Свойства и методы имеют алфавитный порядок, а не порядок MOF.</span><span class="sxs-lookup"><span data-stu-id="c50e1-106">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="c50e1-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c50e1-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), Privileges("SeRestorePrivilege"), UUID("{86E30E82-7DB2-11d2-90CB-0060081A46FD}"), AMENDMENT]
class Win32_LogicalProgramGroupItem : Win32_ProgramGroupOrItem
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Status;
  string   Name;
};
```

## <a name="members"></a><span data-ttu-id="c50e1-108">Члены</span><span class="sxs-lookup"><span data-stu-id="c50e1-108">Members</span></span>

<span data-ttu-id="c50e1-109">Класс **Win32 \_ логикалпрограмграупитем** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="c50e1-109">The **Win32\_LogicalProgramGroupItem** class has these types of members:</span></span>

-   [<span data-ttu-id="c50e1-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="c50e1-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="c50e1-111">Свойства</span><span class="sxs-lookup"><span data-stu-id="c50e1-111">Properties</span></span>

<span data-ttu-id="c50e1-112">Класс **Win32 \_ логикалпрограмграупитем** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="c50e1-112">The **Win32\_LogicalProgramGroupItem** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="c50e1-113">**Заголовок**</span><span class="sxs-lookup"><span data-stu-id="c50e1-113">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c50e1-114">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="c50e1-114">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c50e1-115">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c50e1-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c50e1-116">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="c50e1-116">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="c50e1-117">Краткое текстовое описание объекта.</span><span class="sxs-lookup"><span data-stu-id="c50e1-117">A short textual description of the object.</span></span>

<span data-ttu-id="c50e1-118">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="c50e1-118">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="c50e1-119">**Описание**</span><span class="sxs-lookup"><span data-stu-id="c50e1-119">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c50e1-120">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="c50e1-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c50e1-121">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c50e1-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c50e1-122">Квалификаторы: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Описание")</span><span class="sxs-lookup"><span data-stu-id="c50e1-122">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="c50e1-123">Текстовое описание объекта.</span><span class="sxs-lookup"><span data-stu-id="c50e1-123">A textual description of the object.</span></span>

<span data-ttu-id="c50e1-124">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="c50e1-124">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="c50e1-125">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="c50e1-125">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c50e1-126">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="c50e1-126">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="c50e1-127">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c50e1-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c50e1-128">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" Дата установки ")</span><span class="sxs-lookup"><span data-stu-id="c50e1-128">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="c50e1-129">Указывает, когда был установлен объект.</span><span class="sxs-lookup"><span data-stu-id="c50e1-129">Indicates when the object was installed.</span></span> <span data-ttu-id="c50e1-130">Отсутствие значения не означает, что объект не установлен.</span><span class="sxs-lookup"><span data-stu-id="c50e1-130">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="c50e1-131">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="c50e1-131">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="c50e1-132">**Name**</span><span class="sxs-lookup"><span data-stu-id="c50e1-132">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c50e1-133">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="c50e1-133">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c50e1-134">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c50e1-134">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c50e1-135">Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("имя"), [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (" \| методы класса Win32API квбемпровидерглуе \| [**жеталлинстанцес**](/windows/desktop/api/wbemglue/nf-wbemglue-cwbemproviderglue-getallinstances)")</span><span class="sxs-lookup"><span data-stu-id="c50e1-135">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name"), [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|CWbemProviderGlue Class Methods\|[**GetAllInstances**](/windows/desktop/api/wbemglue/nf-wbemglue-cwbemproviderglue-getallinstances)")</span></span>
</dt> </dl>

<span data-ttu-id="c50e1-136">В системе компьютера.</span><span class="sxs-lookup"><span data-stu-id="c50e1-136">Instance within a computer system.</span></span> <span data-ttu-id="c50e1-137">Группы программ реализуются в виде файловых папок в Win32.</span><span class="sxs-lookup"><span data-stu-id="c50e1-137">Program groups are implemented as file folders in Win32.</span></span> <span data-ttu-id="c50e1-138">Необходимо указать полные имена путей.</span><span class="sxs-lookup"><span data-stu-id="c50e1-138">Full path names should be provided.</span></span>

<span data-ttu-id="c50e1-139">Пример: "C: \\ Пользователи, \\ *кто пользователь* \\ AppData, \\ роуминг в \\ \\ \\ меню" Пуск "Microsoft Windows \\ Programs (Блокнот) \\ \\ . lnk"</span><span class="sxs-lookup"><span data-stu-id="c50e1-139">Example: "C:\\Users\\*someone*\\AppData\\Roaming\\Microsoft\\Windows\\Start Menu\\Programs\\Accessories\\NotePad.Lnk"</span></span>

</dd> <dt>

<span data-ttu-id="c50e1-140">**Состояние**</span><span class="sxs-lookup"><span data-stu-id="c50e1-140">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c50e1-141">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="c50e1-141">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c50e1-142">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c50e1-142">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c50e1-143">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("состояние")</span><span class="sxs-lookup"><span data-stu-id="c50e1-143">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="c50e1-144">Строка, указывающая текущее состояние объекта.</span><span class="sxs-lookup"><span data-stu-id="c50e1-144">String that indicates the current status of the object.</span></span> <span data-ttu-id="c50e1-145">Можно определить операционное и нерабочее состояние.</span><span class="sxs-lookup"><span data-stu-id="c50e1-145">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="c50e1-146">Оперативное состояние может включать "ОК", "деградация" и "пред Fail".</span><span class="sxs-lookup"><span data-stu-id="c50e1-146">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="c50e1-147">"Пред-Fail" указывает, что элемент работает правильно, но прогнозирует сбой (например, жесткий диск с поддержкой SMART).</span><span class="sxs-lookup"><span data-stu-id="c50e1-147">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="c50e1-148">Нерабочее состояние может включать "Error", "starting", "остановка" и "обслуживание".</span><span class="sxs-lookup"><span data-stu-id="c50e1-148">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="c50e1-149">"Служба" может применяться при зеркальном отображении дисков, перезагрузке списка разрешений пользователя или выполнении других административных задач.</span><span class="sxs-lookup"><span data-stu-id="c50e1-149">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="c50e1-150">Не вся такая работа находится в оперативном режиме, но управляемый элемент не является ни "ОК", ни в одном из других состояний.</span><span class="sxs-lookup"><span data-stu-id="c50e1-150">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="c50e1-151">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="c50e1-151">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="c50e1-152">В эти значения входят:</span><span class="sxs-lookup"><span data-stu-id="c50e1-152">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="c50e1-153">**ОК** ("ОК")</span><span class="sxs-lookup"><span data-stu-id="c50e1-153">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="c50e1-154">**Ошибка** ("ошибка")</span><span class="sxs-lookup"><span data-stu-id="c50e1-154">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="c50e1-155">**Пониженная работоспособность** (пониженная работоспособность)</span><span class="sxs-lookup"><span data-stu-id="c50e1-155">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="c50e1-156">**Неизвестно** ("неизвестно")</span><span class="sxs-lookup"><span data-stu-id="c50e1-156">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="c50e1-157">**Пред-ошибка** ("пред Fail")</span><span class="sxs-lookup"><span data-stu-id="c50e1-157">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="c50e1-158">**Запуск** ("Запуск")</span><span class="sxs-lookup"><span data-stu-id="c50e1-158">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="c50e1-159">**Остановка** ("остановка")</span><span class="sxs-lookup"><span data-stu-id="c50e1-159">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="c50e1-160">**Служба** ("служба")</span><span class="sxs-lookup"><span data-stu-id="c50e1-160">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="c50e1-161">**Пренапряжению** ("напряжению")</span><span class="sxs-lookup"><span data-stu-id="c50e1-161">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="c50e1-162">**Невосстановление** ("невосстановление")</span><span class="sxs-lookup"><span data-stu-id="c50e1-162">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="c50e1-163">**Нет контакта** ("нет контакта")</span><span class="sxs-lookup"><span data-stu-id="c50e1-163">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="c50e1-164">**Потеря** связи ("потеря связи")</span><span class="sxs-lookup"><span data-stu-id="c50e1-164">**Lost Comm** ("Lost Comm")</span></span>


<span data-ttu-id="c50e1-165"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="c50e1-165"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="remarks"></a><span data-ttu-id="c50e1-166">Комментарии</span><span class="sxs-lookup"><span data-stu-id="c50e1-166">Remarks</span></span>

<span data-ttu-id="c50e1-167">Класс **Win32 \_ логикалпрограмграупитем** является производным от [**Win32 \_ програмграупоритем**](win32-programgrouporitem.md).</span><span class="sxs-lookup"><span data-stu-id="c50e1-167">The **Win32\_LogicalProgramGroupItem** class is derived from [**Win32\_ProgramGroupOrItem**](win32-programgrouporitem.md).</span></span>

<span data-ttu-id="c50e1-168">Вызывающий процесс, использующий этот класс, должен иметь привилегию **SE \_ reside \_ Name** на компьютере, где размещается реестр.</span><span class="sxs-lookup"><span data-stu-id="c50e1-168">The calling process that uses this class must have the **SE\_RESTORE\_NAME** privilege on the computer in which the registry resides.</span></span> <span data-ttu-id="c50e1-169">Например, если перечислить этот класс на локальном компьютере, учетная запись, под которой выполняется приложение, должна иметь эту привилегию.</span><span class="sxs-lookup"><span data-stu-id="c50e1-169">For example, if you enumerate this class on the local computer, the account under which your application runs must have this privilege.</span></span> <span data-ttu-id="c50e1-170">Дополнительные сведения см. в разделе [выполнение привилегированных операций](/windows/desktop/WmiSdk/executing-privileged-operations).</span><span class="sxs-lookup"><span data-stu-id="c50e1-170">For more information, see [Executing Privileged Operations](/windows/desktop/WmiSdk/executing-privileged-operations).</span></span>

## <a name="requirements"></a><span data-ttu-id="c50e1-171">Требования</span><span class="sxs-lookup"><span data-stu-id="c50e1-171">Requirements</span></span>



| <span data-ttu-id="c50e1-172">Требование</span><span class="sxs-lookup"><span data-stu-id="c50e1-172">Requirement</span></span> | <span data-ttu-id="c50e1-173">Значение</span><span class="sxs-lookup"><span data-stu-id="c50e1-173">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c50e1-174">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="c50e1-174">Minimum supported client</span></span><br/> | <span data-ttu-id="c50e1-175">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="c50e1-175">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="c50e1-176">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="c50e1-176">Minimum supported server</span></span><br/> | <span data-ttu-id="c50e1-177">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c50e1-177">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="c50e1-178">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="c50e1-178">Namespace</span></span><br/>                | <span data-ttu-id="c50e1-179">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="c50e1-179">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="c50e1-180">MOF</span><span class="sxs-lookup"><span data-stu-id="c50e1-180">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c50e1-181"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="c50e1-181"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="c50e1-182">DLL</span><span class="sxs-lookup"><span data-stu-id="c50e1-182">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c50e1-183"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c50e1-183"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c50e1-184">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c50e1-184">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c50e1-185">**\_Програмграупоритем Win32**</span><span class="sxs-lookup"><span data-stu-id="c50e1-185">**Win32\_ProgramGroupOrItem**</span></span>](win32-programgrouporitem.md)
</dt> <dt>

<span data-ttu-id="c50e1-186">[Классы операционной системы](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="c50e1-186">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> </dl>

 

