---
description: '\_Класс WMI компоненткатегори инструментария Win32 представляет категорию компонента.'
ms.assetid: 9c6fc856-8300-4fa5-ae1c-a7d6476f5c51
ms.tgt_platform: multiple
title: Класс Win32_ComponentCategory
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_ComponentCategory
- Win32_ComponentCategory.Caption
- Win32_ComponentCategory.Description
- Win32_ComponentCategory.InstallDate
- Win32_ComponentCategory.Status
- Win32_ComponentCategory.CategoryId
- Win32_ComponentCategory.Name
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 1730abf9058f5068def4a01f0d7e7601b9c69e53
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103990701"
---
# <a name="win32_componentcategory-class"></a><span data-ttu-id="5def2-103">\_Класс Win32 компоненткатегори</span><span class="sxs-lookup"><span data-stu-id="5def2-103">Win32\_ComponentCategory class</span></span>

<span data-ttu-id="5def2-104">Класс **WMI \_ компоненткатегори** [инструментария](/windows/desktop/WmiSdk/retrieving-a-class) Win32 представляет категорию компонента.</span><span class="sxs-lookup"><span data-stu-id="5def2-104">The **Win32\_ComponentCategory** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) represents a component category.</span></span> <span data-ttu-id="5def2-105">Категории компонентов — это группы классов модели COM с определенным набором функций, которыми они являются общими.</span><span class="sxs-lookup"><span data-stu-id="5def2-105">Component categories are groups of Component Object Model (COM) classes with a defined functionality set shared between them.</span></span> <span data-ttu-id="5def2-106">Клиент, использующий эти интерфейсы, запрашивает в реестре заголовок категории и уникальный идентификатор **CategoryID**, который создается из глобального уникального идентификатора (GUID).</span><span class="sxs-lookup"><span data-stu-id="5def2-106">A client using these interfaces queries the registry for the category title and unique identifier called **CategoryID**, which is created from a globally unique identifier (GUID).</span></span>

<span data-ttu-id="5def2-107">Следующий пример синтаксиса — упрощенный MOF-код, который включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="5def2-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="5def2-108">Свойства перечислены в алфавитном порядке, а не в MOF.</span><span class="sxs-lookup"><span data-stu-id="5def2-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="5def2-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="5def2-109">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{0F73ED5A-8ED9-11d2-B340-00105A1F8569}"), AMENDMENT]
class Win32_ComponentCategory : CIM_LogicalElement
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Status;
  string   CategoryId;
  string   Name;
};
```

## <a name="members"></a><span data-ttu-id="5def2-110">Члены</span><span class="sxs-lookup"><span data-stu-id="5def2-110">Members</span></span>

<span data-ttu-id="5def2-111">Класс **Win32 \_ компоненткатегори** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="5def2-111">The **Win32\_ComponentCategory** class has these types of members:</span></span>

-   [<span data-ttu-id="5def2-112">Свойства</span><span class="sxs-lookup"><span data-stu-id="5def2-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="5def2-113">Свойства</span><span class="sxs-lookup"><span data-stu-id="5def2-113">Properties</span></span>

<span data-ttu-id="5def2-114">Класс **Win32 \_ компоненткатегори** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="5def2-114">The **Win32\_ComponentCategory** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="5def2-115">**Заголовок**</span><span class="sxs-lookup"><span data-stu-id="5def2-115">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5def2-116">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="5def2-116">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5def2-117">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="5def2-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5def2-118">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="5def2-118">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="5def2-119">Краткое текстовое описание объекта.</span><span class="sxs-lookup"><span data-stu-id="5def2-119">A short textual description of the object.</span></span>

<span data-ttu-id="5def2-120">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="5def2-120">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="5def2-121">**CategoryId**</span><span class="sxs-lookup"><span data-stu-id="5def2-121">**CategoryId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5def2-122">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="5def2-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5def2-123">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="5def2-123">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5def2-124">Квалификаторы: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (16), [**Маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (" \| категории компонентов Win32API \| [**CATEGORYINFO**](/windows/win32/api/comcat/ns-comcat-categoryinfo) \| CATID")</span><span class="sxs-lookup"><span data-stu-id="5def2-124">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (16), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Component Categories\|[**CATEGORYINFO**](/windows/win32/api/comcat/ns-comcat-categoryinfo)\|catid")</span></span>
</dt> </dl>

<span data-ttu-id="5def2-125">Идентификатор GUID для этой категории компонентов.</span><span class="sxs-lookup"><span data-stu-id="5def2-125">GUID for this component category.</span></span>

</dd> <dt>

<span data-ttu-id="5def2-126">**Описание**</span><span class="sxs-lookup"><span data-stu-id="5def2-126">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5def2-127">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="5def2-127">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5def2-128">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="5def2-128">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5def2-129">Квалификаторы: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Описание")</span><span class="sxs-lookup"><span data-stu-id="5def2-129">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="5def2-130">Текстовое описание объекта.</span><span class="sxs-lookup"><span data-stu-id="5def2-130">A textual description of the object.</span></span>

<span data-ttu-id="5def2-131">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="5def2-131">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="5def2-132">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="5def2-132">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5def2-133">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="5def2-133">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="5def2-134">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="5def2-134">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5def2-135">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" Дата установки ")</span><span class="sxs-lookup"><span data-stu-id="5def2-135">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="5def2-136">Указывает, когда был установлен объект.</span><span class="sxs-lookup"><span data-stu-id="5def2-136">Indicates when the object was installed.</span></span> <span data-ttu-id="5def2-137">Отсутствие значения не означает, что объект не установлен.</span><span class="sxs-lookup"><span data-stu-id="5def2-137">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="5def2-138">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="5def2-138">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="5def2-139">**Name**</span><span class="sxs-lookup"><span data-stu-id="5def2-139">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5def2-140">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="5def2-140">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5def2-141">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="5def2-141">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5def2-142">Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("имя"), [**Маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (" \| категории компонентов Win32API \| [**CATEGORYINFO**](/windows/win32/api/comcat/ns-comcat-categoryinfo) \| сздескриптион")</span><span class="sxs-lookup"><span data-stu-id="5def2-142">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Component Categories\|[**CATEGORYINFO**](/windows/win32/api/comcat/ns-comcat-categoryinfo)\|szDescription")</span></span>
</dt> </dl>

<span data-ttu-id="5def2-143">Свойство Name указывает описательное имя этой категории компонента.</span><span class="sxs-lookup"><span data-stu-id="5def2-143">The Name property indicates a descriptive name of this component category.</span></span>

</dd> <dt>

<span data-ttu-id="5def2-144">**Состояние**</span><span class="sxs-lookup"><span data-stu-id="5def2-144">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5def2-145">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="5def2-145">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5def2-146">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="5def2-146">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5def2-147">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("состояние")</span><span class="sxs-lookup"><span data-stu-id="5def2-147">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="5def2-148">Строка, указывающая текущее состояние объекта.</span><span class="sxs-lookup"><span data-stu-id="5def2-148">String that indicates the current status of the object.</span></span> <span data-ttu-id="5def2-149">Можно определить операционное и нерабочее состояние.</span><span class="sxs-lookup"><span data-stu-id="5def2-149">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="5def2-150">Оперативное состояние может включать "ОК", "деградация" и "пред Fail".</span><span class="sxs-lookup"><span data-stu-id="5def2-150">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="5def2-151">"Пред-Fail" указывает, что элемент работает правильно, но прогнозирует сбой (например, жесткий диск с поддержкой SMART).</span><span class="sxs-lookup"><span data-stu-id="5def2-151">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="5def2-152">Нерабочее состояние может включать "Error", "starting", "остановка" и "обслуживание".</span><span class="sxs-lookup"><span data-stu-id="5def2-152">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="5def2-153">"Служба" может применяться при зеркальном отображении дисков, перезагрузке списка разрешений пользователя или выполнении других административных задач.</span><span class="sxs-lookup"><span data-stu-id="5def2-153">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="5def2-154">Не вся такая работа находится в оперативном режиме, но управляемый элемент не является ни "ОК", ни в одном из других состояний.</span><span class="sxs-lookup"><span data-stu-id="5def2-154">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="5def2-155">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="5def2-155">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="5def2-156">В эти значения входят:</span><span class="sxs-lookup"><span data-stu-id="5def2-156">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="5def2-157">**ОК** ("ОК")</span><span class="sxs-lookup"><span data-stu-id="5def2-157">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="5def2-158">**Ошибка** ("ошибка")</span><span class="sxs-lookup"><span data-stu-id="5def2-158">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="5def2-159">**Пониженная работоспособность** (пониженная работоспособность)</span><span class="sxs-lookup"><span data-stu-id="5def2-159">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="5def2-160">**Неизвестно** ("неизвестно")</span><span class="sxs-lookup"><span data-stu-id="5def2-160">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="5def2-161">**Пред-ошибка** ("пред Fail")</span><span class="sxs-lookup"><span data-stu-id="5def2-161">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="5def2-162">**Запуск** ("Запуск")</span><span class="sxs-lookup"><span data-stu-id="5def2-162">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="5def2-163">**Остановка** ("остановка")</span><span class="sxs-lookup"><span data-stu-id="5def2-163">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="5def2-164">**Служба** ("служба")</span><span class="sxs-lookup"><span data-stu-id="5def2-164">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="5def2-165">**Пренапряжению** ("напряжению")</span><span class="sxs-lookup"><span data-stu-id="5def2-165">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="5def2-166">**Невосстановление** ("невосстановление")</span><span class="sxs-lookup"><span data-stu-id="5def2-166">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="5def2-167">**Нет контакта** ("нет контакта")</span><span class="sxs-lookup"><span data-stu-id="5def2-167">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="5def2-168">**Потеря** связи ("потеря связи")</span><span class="sxs-lookup"><span data-stu-id="5def2-168">**Lost Comm** ("Lost Comm")</span></span>


<span data-ttu-id="5def2-169"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="5def2-169"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="remarks"></a><span data-ttu-id="5def2-170">Комментарии</span><span class="sxs-lookup"><span data-stu-id="5def2-170">Remarks</span></span>

<span data-ttu-id="5def2-171">Класс **Win32 \_ компоненткатегори** является производным от [**CIM \_ логикалелемент**](cim-logicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="5def2-171">The **Win32\_ComponentCategory** class is derived from [**CIM\_LogicalElement**](cim-logicalelement.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="5def2-172">Требования</span><span class="sxs-lookup"><span data-stu-id="5def2-172">Requirements</span></span>



| <span data-ttu-id="5def2-173">Требование</span><span class="sxs-lookup"><span data-stu-id="5def2-173">Requirement</span></span> | <span data-ttu-id="5def2-174">Значение</span><span class="sxs-lookup"><span data-stu-id="5def2-174">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5def2-175">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="5def2-175">Minimum supported client</span></span><br/> | <span data-ttu-id="5def2-176">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="5def2-176">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="5def2-177">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="5def2-177">Minimum supported server</span></span><br/> | <span data-ttu-id="5def2-178">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="5def2-178">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="5def2-179">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="5def2-179">Namespace</span></span><br/>                | <span data-ttu-id="5def2-180">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="5def2-180">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="5def2-181">MOF</span><span class="sxs-lookup"><span data-stu-id="5def2-181">MOF</span></span><br/>                      | <dl> <span data-ttu-id="5def2-182"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="5def2-182"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="5def2-183">DLL</span><span class="sxs-lookup"><span data-stu-id="5def2-183">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5def2-184"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5def2-184"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5def2-185">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="5def2-185">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5def2-186">**\_ЛОГИКАЛЕЛЕМЕНТ CIM**</span><span class="sxs-lookup"><span data-stu-id="5def2-186">**CIM\_LogicalElement**</span></span>](cim-logicalelement.md)
</dt> <dt>

<span data-ttu-id="5def2-187">[Классы операционной системы](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="5def2-187">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> </dl>

 

