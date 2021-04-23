---
description: '\_Абстрактный WMI-класс Win32 комаппликатион представляет приложение модели COM. В этом контексте COM-приложение является логической группировкой классов COM.'
ms.assetid: a70939e2-5812-4ade-aa75-819c8d4b9173
ms.tgt_platform: multiple
title: Класс Win32_COMApplication
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_COMApplication
- Win32_COMApplication.Caption
- Win32_COMApplication.Description
- Win32_COMApplication.InstallDate
- Win32_COMApplication.Name
- Win32_COMApplication.Status
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 705f0f7b3c17ffca809de9a124748a74b5537f26
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104072506"
---
# <a name="win32_comapplication-class"></a><span data-ttu-id="84804-104">\_Класс Win32 комаппликатион</span><span class="sxs-lookup"><span data-stu-id="84804-104">Win32\_COMApplication class</span></span>

<span data-ttu-id="84804-105">Абстрактный WMI- [класс](/windows/desktop/WmiSdk/retrieving-a-class) **Win32 \_ КОМАППЛИКАТИОН** представляет приложение модели COM.</span><span class="sxs-lookup"><span data-stu-id="84804-105">The **Win32\_COMApplication** abstract [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) represents a Component Object Model (COM) application.</span></span> <span data-ttu-id="84804-106">В этом контексте COM-приложение является логической группировкой классов COM.</span><span class="sxs-lookup"><span data-stu-id="84804-106">In this context, a COM application is a logical grouping of COM classes.</span></span>

<span data-ttu-id="84804-107">Следующий пример синтаксиса — упрощенный MOF-код, который включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="84804-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="84804-108">Свойства перечислены в алфавитном порядке, а не в MOF.</span><span class="sxs-lookup"><span data-stu-id="84804-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="84804-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="84804-109">Syntax</span></span>

``` syntax
[abstract, UUID("{0F73ED4F-8ED9-11d2-B340-00105A1F8569}"), AMENDMENT]
class Win32_COMApplication : CIM_LogicalElement
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
};
```

## <a name="members"></a><span data-ttu-id="84804-110">Члены</span><span class="sxs-lookup"><span data-stu-id="84804-110">Members</span></span>

<span data-ttu-id="84804-111">Класс **Win32 \_ комаппликатион** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="84804-111">The **Win32\_COMApplication** class has these types of members:</span></span>

-   [<span data-ttu-id="84804-112">Свойства</span><span class="sxs-lookup"><span data-stu-id="84804-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="84804-113">Свойства</span><span class="sxs-lookup"><span data-stu-id="84804-113">Properties</span></span>

<span data-ttu-id="84804-114">Класс **Win32 \_ комаппликатион** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="84804-114">The **Win32\_COMApplication** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="84804-115">**Заголовок**</span><span class="sxs-lookup"><span data-stu-id="84804-115">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84804-116">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="84804-116">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="84804-117">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="84804-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="84804-118">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="84804-118">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="84804-119">Краткое текстовое описание объекта.</span><span class="sxs-lookup"><span data-stu-id="84804-119">A short textual description of the object.</span></span>

<span data-ttu-id="84804-120">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="84804-120">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="84804-121">**Описание**</span><span class="sxs-lookup"><span data-stu-id="84804-121">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84804-122">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="84804-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="84804-123">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="84804-123">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="84804-124">Квалификаторы: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Описание")</span><span class="sxs-lookup"><span data-stu-id="84804-124">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="84804-125">Текстовое описание объекта.</span><span class="sxs-lookup"><span data-stu-id="84804-125">A textual description of the object.</span></span>

<span data-ttu-id="84804-126">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="84804-126">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="84804-127">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="84804-127">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84804-128">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="84804-128">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="84804-129">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="84804-129">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="84804-130">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" Дата установки ")</span><span class="sxs-lookup"><span data-stu-id="84804-130">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="84804-131">Указывает, когда был установлен объект.</span><span class="sxs-lookup"><span data-stu-id="84804-131">Indicates when the object was installed.</span></span> <span data-ttu-id="84804-132">Отсутствие значения не означает, что объект не установлен.</span><span class="sxs-lookup"><span data-stu-id="84804-132">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="84804-133">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="84804-133">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="84804-134">**Name**</span><span class="sxs-lookup"><span data-stu-id="84804-134">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84804-135">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="84804-135">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="84804-136">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="84804-136">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="84804-137">Квалификаторы: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("имя")</span><span class="sxs-lookup"><span data-stu-id="84804-137">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="84804-138">Метка, по которой известен объект.</span><span class="sxs-lookup"><span data-stu-id="84804-138">Label by which the object is known.</span></span> <span data-ttu-id="84804-139">При создании подклассов это свойство может быть переопределено как свойство ключа.</span><span class="sxs-lookup"><span data-stu-id="84804-139">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="84804-140">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="84804-140">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="84804-141">**Состояние**</span><span class="sxs-lookup"><span data-stu-id="84804-141">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84804-142">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="84804-142">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="84804-143">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="84804-143">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="84804-144">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("состояние")</span><span class="sxs-lookup"><span data-stu-id="84804-144">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="84804-145">Строка, указывающая текущее состояние объекта.</span><span class="sxs-lookup"><span data-stu-id="84804-145">String that indicates the current status of the object.</span></span> <span data-ttu-id="84804-146">Можно определить операционное и нерабочее состояние.</span><span class="sxs-lookup"><span data-stu-id="84804-146">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="84804-147">Оперативное состояние может включать "ОК", "деградация" и "пред Fail".</span><span class="sxs-lookup"><span data-stu-id="84804-147">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="84804-148">"Пред-Fail" указывает, что элемент работает правильно, но прогнозирует сбой (например, жесткий диск с поддержкой SMART).</span><span class="sxs-lookup"><span data-stu-id="84804-148">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="84804-149">Нерабочее состояние может включать "Error", "starting", "остановка" и "обслуживание".</span><span class="sxs-lookup"><span data-stu-id="84804-149">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="84804-150">"Служба" может применяться при зеркальном отображении дисков, перезагрузке списка разрешений пользователя или выполнении других административных задач.</span><span class="sxs-lookup"><span data-stu-id="84804-150">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="84804-151">Не вся такая работа находится в оперативном режиме, но управляемый элемент не является ни "ОК", ни в одном из других состояний.</span><span class="sxs-lookup"><span data-stu-id="84804-151">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="84804-152">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="84804-152">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="84804-153">В эти значения входят:</span><span class="sxs-lookup"><span data-stu-id="84804-153">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="84804-154">**ОК** ("ОК")</span><span class="sxs-lookup"><span data-stu-id="84804-154">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="84804-155">**Ошибка** ("ошибка")</span><span class="sxs-lookup"><span data-stu-id="84804-155">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="84804-156">**Пониженная работоспособность** (пониженная работоспособность)</span><span class="sxs-lookup"><span data-stu-id="84804-156">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="84804-157">**Неизвестно** ("неизвестно")</span><span class="sxs-lookup"><span data-stu-id="84804-157">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="84804-158">**Пред-ошибка** ("пред Fail")</span><span class="sxs-lookup"><span data-stu-id="84804-158">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="84804-159">**Запуск** ("Запуск")</span><span class="sxs-lookup"><span data-stu-id="84804-159">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="84804-160">**Остановка** ("остановка")</span><span class="sxs-lookup"><span data-stu-id="84804-160">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="84804-161">**Служба** ("служба")</span><span class="sxs-lookup"><span data-stu-id="84804-161">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="84804-162">**Пренапряжению** ("напряжению")</span><span class="sxs-lookup"><span data-stu-id="84804-162">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="84804-163">**Невосстановление** ("невосстановление")</span><span class="sxs-lookup"><span data-stu-id="84804-163">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="84804-164">**Нет контакта** ("нет контакта")</span><span class="sxs-lookup"><span data-stu-id="84804-164">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="84804-165">**Потеря** связи ("потеря связи")</span><span class="sxs-lookup"><span data-stu-id="84804-165">**Lost Comm** ("Lost Comm")</span></span>


<span data-ttu-id="84804-166"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="84804-166"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="remarks"></a><span data-ttu-id="84804-167">Комментарии</span><span class="sxs-lookup"><span data-stu-id="84804-167">Remarks</span></span>

<span data-ttu-id="84804-168">Класс **Win32 \_ комаппликатион** является производным от [**CIM \_ логикалелемент**](cim-logicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="84804-168">The **Win32\_COMApplication** class is derived from [**CIM\_LogicalElement**](cim-logicalelement.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="84804-169">Требования</span><span class="sxs-lookup"><span data-stu-id="84804-169">Requirements</span></span>



| <span data-ttu-id="84804-170">Требование</span><span class="sxs-lookup"><span data-stu-id="84804-170">Requirement</span></span> | <span data-ttu-id="84804-171">Значение</span><span class="sxs-lookup"><span data-stu-id="84804-171">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="84804-172">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="84804-172">Minimum supported client</span></span><br/> | <span data-ttu-id="84804-173">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="84804-173">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="84804-174">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="84804-174">Minimum supported server</span></span><br/> | <span data-ttu-id="84804-175">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="84804-175">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="84804-176">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="84804-176">Namespace</span></span><br/>                | <span data-ttu-id="84804-177">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="84804-177">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="84804-178">MOF</span><span class="sxs-lookup"><span data-stu-id="84804-178">MOF</span></span><br/>                      | <dl> <span data-ttu-id="84804-179"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="84804-179"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="84804-180">DLL</span><span class="sxs-lookup"><span data-stu-id="84804-180">DLL</span></span><br/>                      | <dl> <span data-ttu-id="84804-181"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="84804-181"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="84804-182">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="84804-182">See also</span></span>

<dl> <dt>

[<span data-ttu-id="84804-183">**\_ЛОГИКАЛЕЛЕМЕНТ CIM**</span><span class="sxs-lookup"><span data-stu-id="84804-183">**CIM\_LogicalElement**</span></span>](cim-logicalelement.md)
</dt> <dt>

<span data-ttu-id="84804-184">[Классы операционной системы](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="84804-184">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> </dl>

 

