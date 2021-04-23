---
description: '\_Класс WMI дкомаппликатион для Win32 представляет свойства DCOM-приложения.'
ms.assetid: 11856834-6774-4262-bac4-e0265d4ba7e3
ms.tgt_platform: multiple
title: Класс Win32_DCOMApplication
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_DCOMApplication
- Win32_DCOMApplication.Caption
- Win32_DCOMApplication.Description
- Win32_DCOMApplication.InstallDate
- Win32_DCOMApplication.Name
- Win32_DCOMApplication.Status
- Win32_DCOMApplication.AppID
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: a90ddaab9565557b5bbc83f52d0dce82447ab15d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105656062"
---
# <a name="win32_dcomapplication-class"></a><span data-ttu-id="b6118-103">\_Класс Win32 дкомаппликатион</span><span class="sxs-lookup"><span data-stu-id="b6118-103">Win32\_DCOMApplication class</span></span>

<span data-ttu-id="b6118-104">[Класс WMI](/windows/desktop/WmiSdk/retrieving-a-class) **\_ дкомаппликатион для Win32** представляет свойства DCOM-приложения.</span><span class="sxs-lookup"><span data-stu-id="b6118-104">The **Win32\_DCOMApplication** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) represents the properties of a DCOM application.</span></span>

<span data-ttu-id="b6118-105">Следующий пример синтаксиса — упрощенный MOF-код, который включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="b6118-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="b6118-106">Свойства перечислены в алфавитном порядке, а не в MOF.</span><span class="sxs-lookup"><span data-stu-id="b6118-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="b6118-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b6118-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{0F73ED52-8ED9-11d2-B340-00105A1F8569}"), AMENDMENT]
class Win32_DCOMApplication : Win32_COMApplication
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
  string   AppID;
};
```

## <a name="members"></a><span data-ttu-id="b6118-108">Члены</span><span class="sxs-lookup"><span data-stu-id="b6118-108">Members</span></span>

<span data-ttu-id="b6118-109">Класс **Win32 \_ дкомаппликатион** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="b6118-109">The **Win32\_DCOMApplication** class has these types of members:</span></span>

-   [<span data-ttu-id="b6118-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="b6118-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="b6118-111">Свойства</span><span class="sxs-lookup"><span data-stu-id="b6118-111">Properties</span></span>

<span data-ttu-id="b6118-112">Класс **Win32 \_ дкомаппликатион** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="b6118-112">The **Win32\_DCOMApplication** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="b6118-113">**AppID**</span><span class="sxs-lookup"><span data-stu-id="b6118-113">**AppID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b6118-114">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="b6118-114">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b6118-115">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="b6118-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b6118-116">Квалификаторы: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| hKey \_ . \_ \\ \\ классы программного обеспечения локального компьютера \\ \\ \\ \\ AppID \\ \\ {GUID} \[ Default \] ")</span><span class="sxs-lookup"><span data-stu-id="b6118-116">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry\|HKEY\_LOCAL\_MACHINE\\\\SOFTWARE\\\\Classes\\\\AppID\\\\{GUID}\[Default\]")</span></span>
</dt> </dl>

<span data-ttu-id="b6118-117">Глобальный уникальный идентификатор (GUID) для DCOM-приложения.</span><span class="sxs-lookup"><span data-stu-id="b6118-117">Globally unique identifier (GUID) for the DCOM application.</span></span>

</dd> <dt>

<span data-ttu-id="b6118-118">**Заголовок**</span><span class="sxs-lookup"><span data-stu-id="b6118-118">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b6118-119">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="b6118-119">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b6118-120">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="b6118-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b6118-121">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="b6118-121">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="b6118-122">Краткое текстовое описание объекта.</span><span class="sxs-lookup"><span data-stu-id="b6118-122">A short textual description of the object.</span></span>

<span data-ttu-id="b6118-123">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="b6118-123">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="b6118-124">**Описание**</span><span class="sxs-lookup"><span data-stu-id="b6118-124">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b6118-125">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="b6118-125">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b6118-126">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="b6118-126">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b6118-127">Квалификаторы: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Описание")</span><span class="sxs-lookup"><span data-stu-id="b6118-127">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="b6118-128">Текстовое описание объекта.</span><span class="sxs-lookup"><span data-stu-id="b6118-128">A textual description of the object.</span></span>

<span data-ttu-id="b6118-129">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="b6118-129">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="b6118-130">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="b6118-130">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b6118-131">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="b6118-131">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="b6118-132">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="b6118-132">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b6118-133">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" Дата установки ")</span><span class="sxs-lookup"><span data-stu-id="b6118-133">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="b6118-134">Указывает, когда был установлен объект.</span><span class="sxs-lookup"><span data-stu-id="b6118-134">Indicates when the object was installed.</span></span> <span data-ttu-id="b6118-135">Отсутствие значения не означает, что объект не установлен.</span><span class="sxs-lookup"><span data-stu-id="b6118-135">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="b6118-136">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="b6118-136">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="b6118-137">**Name**</span><span class="sxs-lookup"><span data-stu-id="b6118-137">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b6118-138">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="b6118-138">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b6118-139">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="b6118-139">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b6118-140">Квалификаторы: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("имя")</span><span class="sxs-lookup"><span data-stu-id="b6118-140">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="b6118-141">Метка, по которой известен объект.</span><span class="sxs-lookup"><span data-stu-id="b6118-141">Label by which the object is known.</span></span> <span data-ttu-id="b6118-142">При создании подклассов это свойство может быть переопределено как свойство ключа.</span><span class="sxs-lookup"><span data-stu-id="b6118-142">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="b6118-143">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="b6118-143">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="b6118-144">**Состояние**</span><span class="sxs-lookup"><span data-stu-id="b6118-144">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b6118-145">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="b6118-145">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b6118-146">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="b6118-146">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b6118-147">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("состояние")</span><span class="sxs-lookup"><span data-stu-id="b6118-147">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="b6118-148">Строка, указывающая текущее состояние объекта.</span><span class="sxs-lookup"><span data-stu-id="b6118-148">String that indicates the current status of the object.</span></span> <span data-ttu-id="b6118-149">Можно определить операционное и нерабочее состояние.</span><span class="sxs-lookup"><span data-stu-id="b6118-149">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="b6118-150">Оперативное состояние может включать "ОК", "деградация" и "пред Fail".</span><span class="sxs-lookup"><span data-stu-id="b6118-150">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="b6118-151">"Пред-Fail" указывает, что элемент работает правильно, но прогнозирует сбой (например, жесткий диск с поддержкой SMART).</span><span class="sxs-lookup"><span data-stu-id="b6118-151">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="b6118-152">Нерабочее состояние может включать "Error", "starting", "остановка" и "обслуживание".</span><span class="sxs-lookup"><span data-stu-id="b6118-152">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="b6118-153">"Служба" может применяться при зеркальном отображении дисков, перезагрузке списка разрешений пользователя или выполнении других административных задач.</span><span class="sxs-lookup"><span data-stu-id="b6118-153">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="b6118-154">Не вся такая работа находится в оперативном режиме, но управляемый элемент не является ни "ОК", ни в одном из других состояний.</span><span class="sxs-lookup"><span data-stu-id="b6118-154">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="b6118-155">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="b6118-155">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="b6118-156">В эти значения входят:</span><span class="sxs-lookup"><span data-stu-id="b6118-156">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="b6118-157">**ОК** ("ОК")</span><span class="sxs-lookup"><span data-stu-id="b6118-157">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="b6118-158">**Ошибка** ("ошибка")</span><span class="sxs-lookup"><span data-stu-id="b6118-158">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="b6118-159">**Пониженная работоспособность** (пониженная работоспособность)</span><span class="sxs-lookup"><span data-stu-id="b6118-159">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="b6118-160">**Неизвестно** ("неизвестно")</span><span class="sxs-lookup"><span data-stu-id="b6118-160">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="b6118-161">**Пред-ошибка** ("пред Fail")</span><span class="sxs-lookup"><span data-stu-id="b6118-161">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="b6118-162">**Запуск** ("Запуск")</span><span class="sxs-lookup"><span data-stu-id="b6118-162">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="b6118-163">**Остановка** ("остановка")</span><span class="sxs-lookup"><span data-stu-id="b6118-163">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="b6118-164">**Служба** ("служба")</span><span class="sxs-lookup"><span data-stu-id="b6118-164">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="b6118-165">**Пренапряжению** ("напряжению")</span><span class="sxs-lookup"><span data-stu-id="b6118-165">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="b6118-166">**Невосстановление** ("невосстановление")</span><span class="sxs-lookup"><span data-stu-id="b6118-166">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="b6118-167">**Нет контакта** ("нет контакта")</span><span class="sxs-lookup"><span data-stu-id="b6118-167">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="b6118-168">**Потеря** связи ("потеря связи")</span><span class="sxs-lookup"><span data-stu-id="b6118-168">**Lost Comm** ("Lost Comm")</span></span>


<span data-ttu-id="b6118-169"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="b6118-169"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="remarks"></a><span data-ttu-id="b6118-170">Комментарии</span><span class="sxs-lookup"><span data-stu-id="b6118-170">Remarks</span></span>

<span data-ttu-id="b6118-171">Класс **Win32 \_ дкомаппликатион** является производным от [**Win32 \_ комаппликатион**](win32-comapplication.md).</span><span class="sxs-lookup"><span data-stu-id="b6118-171">The **Win32\_DCOMApplication** class is derived from [**Win32\_COMApplication**](win32-comapplication.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="b6118-172">Требования</span><span class="sxs-lookup"><span data-stu-id="b6118-172">Requirements</span></span>



| <span data-ttu-id="b6118-173">Требование</span><span class="sxs-lookup"><span data-stu-id="b6118-173">Requirement</span></span> | <span data-ttu-id="b6118-174">Значение</span><span class="sxs-lookup"><span data-stu-id="b6118-174">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b6118-175">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="b6118-175">Minimum supported client</span></span><br/> | <span data-ttu-id="b6118-176">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="b6118-176">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="b6118-177">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="b6118-177">Minimum supported server</span></span><br/> | <span data-ttu-id="b6118-178">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b6118-178">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="b6118-179">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="b6118-179">Namespace</span></span><br/>                | <span data-ttu-id="b6118-180">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="b6118-180">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="b6118-181">MOF</span><span class="sxs-lookup"><span data-stu-id="b6118-181">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b6118-182"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="b6118-182"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="b6118-183">DLL</span><span class="sxs-lookup"><span data-stu-id="b6118-183">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b6118-184"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b6118-184"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b6118-185">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b6118-185">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b6118-186">**\_Комаппликатион Win32**</span><span class="sxs-lookup"><span data-stu-id="b6118-186">**Win32\_COMApplication**</span></span>](win32-comapplication.md)
</dt> <dt>

<span data-ttu-id="b6118-187">[Классы операционной системы](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="b6118-187">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> </dl>

 

