---
description: '\_Класс WMI классиккомкласс для Win32 представляет свойства COM-компонента.'
ms.assetid: 49b10991-cc2e-40a1-bbb3-a816a52d1a91
ms.tgt_platform: multiple
title: Класс Win32_ClassicCOMClass
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_ClassicCOMClass
- Win32_ClassicCOMClass.Caption
- Win32_ClassicCOMClass.Description
- Win32_ClassicCOMClass.InstallDate
- Win32_ClassicCOMClass.Status
- Win32_ClassicCOMClass.ComponentId
- Win32_ClassicCOMClass.Name
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 92299b46c3942b2a8a3304da3b1c41b8ec985e6c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105655994"
---
# <a name="win32_classiccomclass-class"></a><span data-ttu-id="8f5b0-103">\_Класс Win32 классиккомкласс</span><span class="sxs-lookup"><span data-stu-id="8f5b0-103">Win32\_ClassicCOMClass class</span></span>

<span data-ttu-id="8f5b0-104">[Класс WMI](/windows/desktop/WmiSdk/retrieving-a-class) **\_ классиккомкласс для Win32** представляет свойства COM-компонента.</span><span class="sxs-lookup"><span data-stu-id="8f5b0-104">The **Win32\_ClassicCOMClass** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) represents the properties of a COM component.</span></span>

<span data-ttu-id="8f5b0-105">Следующий пример синтаксиса — упрощенный MOF-код, который включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="8f5b0-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="8f5b0-106">Свойства перечислены в алфавитном порядке, а не в MOF.</span><span class="sxs-lookup"><span data-stu-id="8f5b0-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="8f5b0-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="8f5b0-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{0F73ED53-8ED9-11d2-B340-00105A1F8569}"), AMENDMENT]
class Win32_ClassicCOMClass : Win32_COMClass
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Status;
  string   ComponentId;
  string   Name;
};
```

## <a name="members"></a><span data-ttu-id="8f5b0-108">Члены</span><span class="sxs-lookup"><span data-stu-id="8f5b0-108">Members</span></span>

<span data-ttu-id="8f5b0-109">Класс **Win32 \_ классиккомкласс** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="8f5b0-109">The **Win32\_ClassicCOMClass** class has these types of members:</span></span>

-   [<span data-ttu-id="8f5b0-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="8f5b0-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="8f5b0-111">Свойства</span><span class="sxs-lookup"><span data-stu-id="8f5b0-111">Properties</span></span>

<span data-ttu-id="8f5b0-112">Класс **Win32 \_ классиккомкласс** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="8f5b0-112">The **Win32\_ClassicCOMClass** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="8f5b0-113">**Заголовок**</span><span class="sxs-lookup"><span data-stu-id="8f5b0-113">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f5b0-114">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="8f5b0-114">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8f5b0-115">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="8f5b0-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8f5b0-116">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="8f5b0-116">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="8f5b0-117">Краткое текстовое описание объекта.</span><span class="sxs-lookup"><span data-stu-id="8f5b0-117">A short textual description of the object.</span></span>

<span data-ttu-id="8f5b0-118">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="8f5b0-118">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="8f5b0-119">**ComponentId**</span><span class="sxs-lookup"><span data-stu-id="8f5b0-119">**ComponentId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f5b0-120">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="8f5b0-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8f5b0-121">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="8f5b0-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8f5b0-122">Квалификаторы: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| hKey \_ , \_ \\ \\ классы программного обеспечения локального компьютера, \\ \\ \\ \\ CLSID \\ \\ {GUID} \[ по умолчанию \] ")</span><span class="sxs-lookup"><span data-stu-id="8f5b0-122">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry\|HKEY\_LOCAL\_MACHINE\\\\SOFTWARE\\\\Classes\\\\CLSID\\\\{GUID}\[Default\]")</span></span>
</dt> </dl>

<span data-ttu-id="8f5b0-123">Глобальный уникальный идентификатор (GUID) этого класса COM.</span><span class="sxs-lookup"><span data-stu-id="8f5b0-123">Globally unique identifier (GUID) of this COM class.</span></span>

</dd> <dt>

<span data-ttu-id="8f5b0-124">**Описание**</span><span class="sxs-lookup"><span data-stu-id="8f5b0-124">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f5b0-125">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="8f5b0-125">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8f5b0-126">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="8f5b0-126">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8f5b0-127">Квалификаторы: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Описание")</span><span class="sxs-lookup"><span data-stu-id="8f5b0-127">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="8f5b0-128">Текстовое описание объекта.</span><span class="sxs-lookup"><span data-stu-id="8f5b0-128">A textual description of the object.</span></span>

<span data-ttu-id="8f5b0-129">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="8f5b0-129">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="8f5b0-130">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="8f5b0-130">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f5b0-131">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="8f5b0-131">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="8f5b0-132">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="8f5b0-132">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8f5b0-133">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" Дата установки ")</span><span class="sxs-lookup"><span data-stu-id="8f5b0-133">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="8f5b0-134">Указывает, когда был установлен объект.</span><span class="sxs-lookup"><span data-stu-id="8f5b0-134">Indicates when the object was installed.</span></span> <span data-ttu-id="8f5b0-135">Отсутствие значения не означает, что объект не установлен.</span><span class="sxs-lookup"><span data-stu-id="8f5b0-135">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="8f5b0-136">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="8f5b0-136">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="8f5b0-137">**Name**</span><span class="sxs-lookup"><span data-stu-id="8f5b0-137">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f5b0-138">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="8f5b0-138">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8f5b0-139">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="8f5b0-139">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8f5b0-140">Квалификаторы: [**fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**reoverride**](/windows/desktop/WmiSdk/standard-qualifiers) ("имя"), [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| hKey \_ Local \_ Machine \\ \\ Software \\ \\ Classes \\ \\ CLSID \\ \\ {GUID} \[ Default \] ")</span><span class="sxs-lookup"><span data-stu-id="8f5b0-140">Qualifiers: [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry\|HKEY\_LOCAL\_MACHINE\\\\SOFTWARE\\\\Classes\\\\CLSID\\\\{GUID}\[Default\]")</span></span>
</dt> </dl>

<span data-ttu-id="8f5b0-141">Свойство Name содержит удобное для восприятия имя класса COM.</span><span class="sxs-lookup"><span data-stu-id="8f5b0-141">The Name property contains the human-readable name for the COM class.</span></span>

</dd> <dt>

<span data-ttu-id="8f5b0-142">**Состояние**</span><span class="sxs-lookup"><span data-stu-id="8f5b0-142">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f5b0-143">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="8f5b0-143">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8f5b0-144">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="8f5b0-144">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8f5b0-145">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("состояние")</span><span class="sxs-lookup"><span data-stu-id="8f5b0-145">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="8f5b0-146">Строка, указывающая текущее состояние объекта.</span><span class="sxs-lookup"><span data-stu-id="8f5b0-146">String that indicates the current status of the object.</span></span> <span data-ttu-id="8f5b0-147">Можно определить операционное и нерабочее состояние.</span><span class="sxs-lookup"><span data-stu-id="8f5b0-147">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="8f5b0-148">Оперативное состояние может включать "ОК", "деградация" и "пред Fail".</span><span class="sxs-lookup"><span data-stu-id="8f5b0-148">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="8f5b0-149">"Пред-Fail" указывает, что элемент работает правильно, но прогнозирует сбой (например, жесткий диск с поддержкой SMART).</span><span class="sxs-lookup"><span data-stu-id="8f5b0-149">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="8f5b0-150">Нерабочее состояние может включать "Error", "starting", "остановка" и "обслуживание".</span><span class="sxs-lookup"><span data-stu-id="8f5b0-150">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="8f5b0-151">"Служба" может применяться при зеркальном отображении дисков, перезагрузке списка разрешений пользователя или выполнении других административных задач.</span><span class="sxs-lookup"><span data-stu-id="8f5b0-151">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="8f5b0-152">Не вся такая работа находится в оперативном режиме, но управляемый элемент не является ни "ОК", ни в одном из других состояний.</span><span class="sxs-lookup"><span data-stu-id="8f5b0-152">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="8f5b0-153">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="8f5b0-153">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="8f5b0-154">В эти значения входят:</span><span class="sxs-lookup"><span data-stu-id="8f5b0-154">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="8f5b0-155">**ОК** ("ОК")</span><span class="sxs-lookup"><span data-stu-id="8f5b0-155">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="8f5b0-156">**Ошибка** ("ошибка")</span><span class="sxs-lookup"><span data-stu-id="8f5b0-156">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="8f5b0-157">**Пониженная работоспособность** (пониженная работоспособность)</span><span class="sxs-lookup"><span data-stu-id="8f5b0-157">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="8f5b0-158">**Неизвестно** ("неизвестно")</span><span class="sxs-lookup"><span data-stu-id="8f5b0-158">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="8f5b0-159">**Пред-ошибка** ("пред Fail")</span><span class="sxs-lookup"><span data-stu-id="8f5b0-159">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="8f5b0-160">**Запуск** ("Запуск")</span><span class="sxs-lookup"><span data-stu-id="8f5b0-160">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="8f5b0-161">**Остановка** ("остановка")</span><span class="sxs-lookup"><span data-stu-id="8f5b0-161">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="8f5b0-162">**Служба** ("служба")</span><span class="sxs-lookup"><span data-stu-id="8f5b0-162">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="8f5b0-163">**Пренапряжению** ("напряжению")</span><span class="sxs-lookup"><span data-stu-id="8f5b0-163">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="8f5b0-164">**Невосстановление** ("невосстановление")</span><span class="sxs-lookup"><span data-stu-id="8f5b0-164">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="8f5b0-165">**Нет контакта** ("нет контакта")</span><span class="sxs-lookup"><span data-stu-id="8f5b0-165">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="8f5b0-166">**Потеря** связи ("потеря связи")</span><span class="sxs-lookup"><span data-stu-id="8f5b0-166">**Lost Comm** ("Lost Comm")</span></span>


<span data-ttu-id="8f5b0-167"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="8f5b0-167"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="remarks"></a><span data-ttu-id="8f5b0-168">Комментарии</span><span class="sxs-lookup"><span data-stu-id="8f5b0-168">Remarks</span></span>

<span data-ttu-id="8f5b0-169">Класс **Win32 \_ классиккомкласс** является производным от [**Win32 \_ COMClass**](win32-comclass.md).</span><span class="sxs-lookup"><span data-stu-id="8f5b0-169">The **Win32\_ClassicCOMClass** class is derived from [**Win32\_COMClass**](win32-comclass.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="8f5b0-170">Требования</span><span class="sxs-lookup"><span data-stu-id="8f5b0-170">Requirements</span></span>



| <span data-ttu-id="8f5b0-171">Требование</span><span class="sxs-lookup"><span data-stu-id="8f5b0-171">Requirement</span></span> | <span data-ttu-id="8f5b0-172">Значение</span><span class="sxs-lookup"><span data-stu-id="8f5b0-172">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="8f5b0-173">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="8f5b0-173">Minimum supported client</span></span><br/> | <span data-ttu-id="8f5b0-174">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="8f5b0-174">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="8f5b0-175">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="8f5b0-175">Minimum supported server</span></span><br/> | <span data-ttu-id="8f5b0-176">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="8f5b0-176">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="8f5b0-177">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="8f5b0-177">Namespace</span></span><br/>                | <span data-ttu-id="8f5b0-178">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="8f5b0-178">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="8f5b0-179">MOF</span><span class="sxs-lookup"><span data-stu-id="8f5b0-179">MOF</span></span><br/>                      | <dl> <span data-ttu-id="8f5b0-180"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="8f5b0-180"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="8f5b0-181">DLL</span><span class="sxs-lookup"><span data-stu-id="8f5b0-181">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8f5b0-182"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8f5b0-182"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8f5b0-183">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="8f5b0-183">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8f5b0-184">**\_COMClass Win32**</span><span class="sxs-lookup"><span data-stu-id="8f5b0-184">**Win32\_COMClass**</span></span>](win32-comclass.md)
</dt> <dt>

<span data-ttu-id="8f5b0-185">[Классы операционной системы](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="8f5b0-185">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> </dl>

 

