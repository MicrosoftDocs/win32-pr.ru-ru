---
description: '\_Абстрактный класс WMI COMClass Win32 представляет свойства компонента модели COM.'
ms.assetid: 0e1d3930-1499-423a-96b0-89b2f05a1191
ms.tgt_platform: multiple
title: Класс Win32_COMClass
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_COMClass
- Win32_COMClass.Caption
- Win32_COMClass.Description
- Win32_COMClass.InstallDate
- Win32_COMClass.Name
- Win32_COMClass.Status
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 685b0b1f869d159df12dfcf12f3a61fed8d76ad8
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103990702"
---
# <a name="win32_comclass-class"></a><span data-ttu-id="8e712-103">\_Класс Win32 COMClass</span><span class="sxs-lookup"><span data-stu-id="8e712-103">Win32\_COMClass class</span></span>

<span data-ttu-id="8e712-104">Абстрактный [класс WMI](/windows/desktop/WmiSdk/retrieving-a-class) **\_ COMClass Win32** представляет свойства компонента модели COM.</span><span class="sxs-lookup"><span data-stu-id="8e712-104">The **Win32\_COMClass** abstract [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) represents the properties of a Component Object Model (COM) component.</span></span>

<span data-ttu-id="8e712-105">Следующий пример синтаксиса — упрощенный MOF-код, который включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="8e712-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="8e712-106">Свойства перечислены в алфавитном порядке, а не в MOF.</span><span class="sxs-lookup"><span data-stu-id="8e712-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="8e712-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="8e712-107">Syntax</span></span>

``` syntax
[abstract, UUID("{0F73ED50-8ED9-11d2-B340-00105A1F8569}"), AMENDMENT]
class Win32_COMClass : CIM_LogicalElement
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
};
```

## <a name="members"></a><span data-ttu-id="8e712-108">Члены</span><span class="sxs-lookup"><span data-stu-id="8e712-108">Members</span></span>

<span data-ttu-id="8e712-109">Класс **Win32 \_ COMClass** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="8e712-109">The **Win32\_COMClass** class has these types of members:</span></span>

-   [<span data-ttu-id="8e712-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="8e712-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="8e712-111">Свойства</span><span class="sxs-lookup"><span data-stu-id="8e712-111">Properties</span></span>

<span data-ttu-id="8e712-112">Класс **Win32 \_ COMClass** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="8e712-112">The **Win32\_COMClass** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="8e712-113">**Заголовок**</span><span class="sxs-lookup"><span data-stu-id="8e712-113">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8e712-114">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="8e712-114">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8e712-115">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="8e712-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8e712-116">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="8e712-116">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="8e712-117">Краткое текстовое описание объекта.</span><span class="sxs-lookup"><span data-stu-id="8e712-117">A short textual description of the object.</span></span>

<span data-ttu-id="8e712-118">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="8e712-118">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="8e712-119">**Описание**</span><span class="sxs-lookup"><span data-stu-id="8e712-119">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8e712-120">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="8e712-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8e712-121">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="8e712-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8e712-122">Квалификаторы: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Описание")</span><span class="sxs-lookup"><span data-stu-id="8e712-122">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="8e712-123">Текстовое описание объекта.</span><span class="sxs-lookup"><span data-stu-id="8e712-123">A textual description of the object.</span></span>

<span data-ttu-id="8e712-124">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="8e712-124">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="8e712-125">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="8e712-125">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8e712-126">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="8e712-126">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="8e712-127">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="8e712-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8e712-128">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" Дата установки ")</span><span class="sxs-lookup"><span data-stu-id="8e712-128">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="8e712-129">Указывает, когда был установлен объект.</span><span class="sxs-lookup"><span data-stu-id="8e712-129">Indicates when the object was installed.</span></span> <span data-ttu-id="8e712-130">Отсутствие значения не означает, что объект не установлен.</span><span class="sxs-lookup"><span data-stu-id="8e712-130">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="8e712-131">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="8e712-131">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="8e712-132">**Name**</span><span class="sxs-lookup"><span data-stu-id="8e712-132">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8e712-133">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="8e712-133">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8e712-134">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="8e712-134">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8e712-135">Квалификаторы: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("имя")</span><span class="sxs-lookup"><span data-stu-id="8e712-135">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="8e712-136">Метка, по которой известен объект.</span><span class="sxs-lookup"><span data-stu-id="8e712-136">Label by which the object is known.</span></span> <span data-ttu-id="8e712-137">При создании подклассов это свойство может быть переопределено как свойство ключа.</span><span class="sxs-lookup"><span data-stu-id="8e712-137">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="8e712-138">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="8e712-138">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="8e712-139">**Состояние**</span><span class="sxs-lookup"><span data-stu-id="8e712-139">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8e712-140">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="8e712-140">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8e712-141">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="8e712-141">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8e712-142">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("состояние")</span><span class="sxs-lookup"><span data-stu-id="8e712-142">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="8e712-143">Строка, указывающая текущее состояние объекта.</span><span class="sxs-lookup"><span data-stu-id="8e712-143">String that indicates the current status of the object.</span></span> <span data-ttu-id="8e712-144">Можно определить операционное и нерабочее состояние.</span><span class="sxs-lookup"><span data-stu-id="8e712-144">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="8e712-145">Оперативное состояние может включать "ОК", "деградация" и "пред Fail".</span><span class="sxs-lookup"><span data-stu-id="8e712-145">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="8e712-146">"Пред-Fail" указывает, что элемент работает правильно, но прогнозирует сбой (например, жесткий диск с поддержкой SMART).</span><span class="sxs-lookup"><span data-stu-id="8e712-146">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="8e712-147">Нерабочее состояние может включать "Error", "starting", "остановка" и "обслуживание".</span><span class="sxs-lookup"><span data-stu-id="8e712-147">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="8e712-148">"Служба" может применяться при зеркальном отображении дисков, перезагрузке списка разрешений пользователя или выполнении других административных задач.</span><span class="sxs-lookup"><span data-stu-id="8e712-148">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="8e712-149">Не вся такая работа находится в оперативном режиме, но управляемый элемент не является ни "ОК", ни в одном из других состояний.</span><span class="sxs-lookup"><span data-stu-id="8e712-149">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="8e712-150">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="8e712-150">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="8e712-151">В эти значения входят:</span><span class="sxs-lookup"><span data-stu-id="8e712-151">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="8e712-152">**ОК** ("ОК")</span><span class="sxs-lookup"><span data-stu-id="8e712-152">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="8e712-153">**Ошибка** ("ошибка")</span><span class="sxs-lookup"><span data-stu-id="8e712-153">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="8e712-154">**Пониженная работоспособность** (пониженная работоспособность)</span><span class="sxs-lookup"><span data-stu-id="8e712-154">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="8e712-155">**Неизвестно** ("неизвестно")</span><span class="sxs-lookup"><span data-stu-id="8e712-155">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="8e712-156">**Пред-ошибка** ("пред Fail")</span><span class="sxs-lookup"><span data-stu-id="8e712-156">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="8e712-157">**Запуск** ("Запуск")</span><span class="sxs-lookup"><span data-stu-id="8e712-157">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="8e712-158">**Остановка** ("остановка")</span><span class="sxs-lookup"><span data-stu-id="8e712-158">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="8e712-159">**Служба** ("служба")</span><span class="sxs-lookup"><span data-stu-id="8e712-159">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="8e712-160">**Пренапряжению** ("напряжению")</span><span class="sxs-lookup"><span data-stu-id="8e712-160">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="8e712-161">**Невосстановление** ("невосстановление")</span><span class="sxs-lookup"><span data-stu-id="8e712-161">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="8e712-162">**Нет контакта** ("нет контакта")</span><span class="sxs-lookup"><span data-stu-id="8e712-162">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="8e712-163">**Потеря** связи ("потеря связи")</span><span class="sxs-lookup"><span data-stu-id="8e712-163">**Lost Comm** ("Lost Comm")</span></span>


<span data-ttu-id="8e712-164"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="8e712-164"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="remarks"></a><span data-ttu-id="8e712-165">Комментарии</span><span class="sxs-lookup"><span data-stu-id="8e712-165">Remarks</span></span>

<span data-ttu-id="8e712-166">Класс **Win32 \_ COMClass** является производным от [**CIM \_ логикалелемент**](cim-logicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="8e712-166">The **Win32\_COMClass** class is derived from [**CIM\_LogicalElement**](cim-logicalelement.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="8e712-167">Требования</span><span class="sxs-lookup"><span data-stu-id="8e712-167">Requirements</span></span>



| <span data-ttu-id="8e712-168">Требование</span><span class="sxs-lookup"><span data-stu-id="8e712-168">Requirement</span></span> | <span data-ttu-id="8e712-169">Значение</span><span class="sxs-lookup"><span data-stu-id="8e712-169">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="8e712-170">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="8e712-170">Minimum supported client</span></span><br/> | <span data-ttu-id="8e712-171">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="8e712-171">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="8e712-172">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="8e712-172">Minimum supported server</span></span><br/> | <span data-ttu-id="8e712-173">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="8e712-173">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="8e712-174">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="8e712-174">Namespace</span></span><br/>                | <span data-ttu-id="8e712-175">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="8e712-175">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="8e712-176">MOF</span><span class="sxs-lookup"><span data-stu-id="8e712-176">MOF</span></span><br/>                      | <dl> <span data-ttu-id="8e712-177"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="8e712-177"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="8e712-178">DLL</span><span class="sxs-lookup"><span data-stu-id="8e712-178">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8e712-179"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8e712-179"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8e712-180">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="8e712-180">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8e712-181">**\_ЛОГИКАЛЕЛЕМЕНТ CIM**</span><span class="sxs-lookup"><span data-stu-id="8e712-181">**CIM\_LogicalElement**</span></span>](cim-logicalelement.md)
</dt> <dt>

<span data-ttu-id="8e712-182">[Классы операционной системы](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="8e712-182">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> </dl>

 

