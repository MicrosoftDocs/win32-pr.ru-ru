---
description: '\_Класс WMI нетворкклиент для Win32 представляет сетевой клиент в системе Windows. Любая компьютерная система в сети с клиентской связью с системой является потомком (или членом) этого класса.'
ms.assetid: f0cc2cef-be23-42f4-a592-2c292aa5085f
ms.tgt_platform: multiple
title: Класс Win32_NetworkClient
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_NetworkClient
- Win32_NetworkClient.Caption
- Win32_NetworkClient.Description
- Win32_NetworkClient.InstallDate
- Win32_NetworkClient.Status
- Win32_NetworkClient.Manufacturer
- Win32_NetworkClient.Name
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 54579073b3974a6c4954ef95b1da3fe2e9fd8348
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103990731"
---
# <a name="win32_networkclient-class"></a><span data-ttu-id="65ecb-104">\_Класс Win32 нетворкклиент</span><span class="sxs-lookup"><span data-stu-id="65ecb-104">Win32\_NetworkClient class</span></span>

<span data-ttu-id="65ecb-105">[Класс WMI](../wmisdk/retrieving-a-class.md) **\_ нетворкклиент для Win32** представляет сетевой клиент в системе Windows.</span><span class="sxs-lookup"><span data-stu-id="65ecb-105">The **Win32\_NetworkClient** [WMI class](../wmisdk/retrieving-a-class.md) represents a network client on a Windows system.</span></span> <span data-ttu-id="65ecb-106">Любая компьютерная система в сети с клиентской связью с системой является потомком (или членом) этого класса.</span><span class="sxs-lookup"><span data-stu-id="65ecb-106">Any computer system on the network with a client relationship to the system is a descendant (or member) of this class.</span></span>

<span data-ttu-id="65ecb-107">Следующий пример синтаксиса — упрощенный MOF-код, который включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="65ecb-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="65ecb-108">Свойства и методы имеют алфавитный порядок, а не порядок MOF.</span><span class="sxs-lookup"><span data-stu-id="65ecb-108">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="65ecb-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="65ecb-109">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C4D5-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_NetworkClient : CIM_LogicalElement
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Status;
  string   Manufacturer;
  string   Name;
};
```

## <a name="members"></a><span data-ttu-id="65ecb-110">Члены</span><span class="sxs-lookup"><span data-stu-id="65ecb-110">Members</span></span>

<span data-ttu-id="65ecb-111">Класс **Win32 \_ нетворкклиент** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="65ecb-111">The **Win32\_NetworkClient** class has these types of members:</span></span>

-   [<span data-ttu-id="65ecb-112">Свойства</span><span class="sxs-lookup"><span data-stu-id="65ecb-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="65ecb-113">Свойства</span><span class="sxs-lookup"><span data-stu-id="65ecb-113">Properties</span></span>

<span data-ttu-id="65ecb-114">Класс **Win32 \_ нетворкклиент** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="65ecb-114">The **Win32\_NetworkClient** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="65ecb-115">**Заголовок**</span><span class="sxs-lookup"><span data-stu-id="65ecb-115">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="65ecb-116">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="65ecb-116">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="65ecb-117">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="65ecb-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="65ecb-118">Квалификаторы: [**maxlen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="65ecb-118">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="65ecb-119">Краткое текстовое описание объекта.</span><span class="sxs-lookup"><span data-stu-id="65ecb-119">A short textual description of the object.</span></span>

<span data-ttu-id="65ecb-120">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="65ecb-120">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="65ecb-121">**Описание**</span><span class="sxs-lookup"><span data-stu-id="65ecb-121">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="65ecb-122">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="65ecb-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="65ecb-123">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="65ecb-123">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="65ecb-124">Квалификаторы: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Описание")</span><span class="sxs-lookup"><span data-stu-id="65ecb-124">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="65ecb-125">Текстовое описание объекта.</span><span class="sxs-lookup"><span data-stu-id="65ecb-125">A textual description of the object.</span></span>

<span data-ttu-id="65ecb-126">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="65ecb-126">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="65ecb-127">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="65ecb-127">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="65ecb-128">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="65ecb-128">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="65ecb-129">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="65ecb-129">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="65ecb-130">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) (MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](../wmisdk/standard-qualifiers.md) (" Дата установки ")</span><span class="sxs-lookup"><span data-stu-id="65ecb-130">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="65ecb-131">Указывает, когда был установлен объект.</span><span class="sxs-lookup"><span data-stu-id="65ecb-131">Indicates when the object was installed.</span></span> <span data-ttu-id="65ecb-132">Отсутствие значения не означает, что объект не установлен.</span><span class="sxs-lookup"><span data-stu-id="65ecb-132">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="65ecb-133">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="65ecb-133">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="65ecb-134">**Производителя**</span><span class="sxs-lookup"><span data-stu-id="65ecb-134">**Manufacturer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="65ecb-135">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="65ecb-135">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="65ecb-136">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="65ecb-136">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="65ecb-137">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services \\ \\ LanmanWorkstation \\ \\ нетворкпровидер \| производственная")</span><span class="sxs-lookup"><span data-stu-id="65ecb-137">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Services\\\\LanmanWorkstation\\\\NetworkProvider\|Mfg")</span></span>
</dt> </dl>

<span data-ttu-id="65ecb-138">Имя производителя сетевого клиента, работающего в компьютерной системе под управлением Windows.</span><span class="sxs-lookup"><span data-stu-id="65ecb-138">Name of the manufacturer of the network client running on the computer system running Windows.</span></span>

<span data-ttu-id="65ecb-139">Пример: "Корпорация Майкрософт"</span><span class="sxs-lookup"><span data-stu-id="65ecb-139">Example: "Microsoft Corporation"</span></span>

</dd> <dt>

<span data-ttu-id="65ecb-140">**Name**</span><span class="sxs-lookup"><span data-stu-id="65ecb-140">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="65ecb-141">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="65ecb-141">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="65ecb-142">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="65ecb-142">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="65ecb-143">Квалификаторы: [**ключ**](../wmisdk/key-qualifier.md), [**Переопределение**](../wmisdk/standard-qualifiers.md) ("имя"), [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services \\ \\ LanmanWorkstation \\ \\ нетворкпровидер \| Name")</span><span class="sxs-lookup"><span data-stu-id="65ecb-143">Qualifiers: [**key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("Name"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Services\\\\LanmanWorkstation\\\\NetworkProvider\|Name")</span></span>
</dt> </dl>

<span data-ttu-id="65ecb-144">Сетевое имя сетевого клиента, работающего в компьютерной системе под управлением Windows.</span><span class="sxs-lookup"><span data-stu-id="65ecb-144">Network name of the network client running on the computer system running Windows.</span></span>

<span data-ttu-id="65ecb-145">Пример: "сеть Microsoft Windows"</span><span class="sxs-lookup"><span data-stu-id="65ecb-145">Example: "Microsoft Windows Network"</span></span>

</dd> <dt>

<span data-ttu-id="65ecb-146">**Состояние**</span><span class="sxs-lookup"><span data-stu-id="65ecb-146">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="65ecb-147">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="65ecb-147">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="65ecb-148">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="65ecb-148">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="65ecb-149">Квалификаторы: [**maxlen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("состояние")</span><span class="sxs-lookup"><span data-stu-id="65ecb-149">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="65ecb-150">Строка, указывающая текущее состояние объекта.</span><span class="sxs-lookup"><span data-stu-id="65ecb-150">String that indicates the current status of the object.</span></span> <span data-ttu-id="65ecb-151">Можно определить операционное и нерабочее состояние.</span><span class="sxs-lookup"><span data-stu-id="65ecb-151">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="65ecb-152">Оперативное состояние может включать "ОК", "деградация" и "пред Fail".</span><span class="sxs-lookup"><span data-stu-id="65ecb-152">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="65ecb-153">"Пред-Fail" указывает, что элемент работает правильно, но прогнозирует сбой (например, жесткий диск с поддержкой SMART).</span><span class="sxs-lookup"><span data-stu-id="65ecb-153">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="65ecb-154">Нерабочее состояние может включать "Error", "starting", "остановка" и "обслуживание".</span><span class="sxs-lookup"><span data-stu-id="65ecb-154">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="65ecb-155">"Служба" может применяться при зеркальном отображении дисков, перезагрузке списка разрешений пользователя или выполнении других административных задач.</span><span class="sxs-lookup"><span data-stu-id="65ecb-155">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="65ecb-156">Не вся такая работа находится в оперативном режиме, но управляемый элемент не является ни "ОК", ни в одном из других состояний.</span><span class="sxs-lookup"><span data-stu-id="65ecb-156">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="65ecb-157">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="65ecb-157">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="65ecb-158">В эти значения входят:</span><span class="sxs-lookup"><span data-stu-id="65ecb-158">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="65ecb-159">**ОК** ("ОК")</span><span class="sxs-lookup"><span data-stu-id="65ecb-159">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="65ecb-160">**Ошибка** ("ошибка")</span><span class="sxs-lookup"><span data-stu-id="65ecb-160">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="65ecb-161">**Пониженная работоспособность** (пониженная работоспособность)</span><span class="sxs-lookup"><span data-stu-id="65ecb-161">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="65ecb-162">**Неизвестно** ("неизвестно")</span><span class="sxs-lookup"><span data-stu-id="65ecb-162">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="65ecb-163">**Пред-ошибка** ("пред Fail")</span><span class="sxs-lookup"><span data-stu-id="65ecb-163">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="65ecb-164">**Запуск** ("Запуск")</span><span class="sxs-lookup"><span data-stu-id="65ecb-164">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="65ecb-165">**Остановка** ("остановка")</span><span class="sxs-lookup"><span data-stu-id="65ecb-165">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="65ecb-166">**Служба** ("служба")</span><span class="sxs-lookup"><span data-stu-id="65ecb-166">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="65ecb-167">**Пренапряжению** ("напряжению")</span><span class="sxs-lookup"><span data-stu-id="65ecb-167">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="65ecb-168">**Невосстановление** ("невосстановление")</span><span class="sxs-lookup"><span data-stu-id="65ecb-168">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="65ecb-169">**Нет контакта** ("нет контакта")</span><span class="sxs-lookup"><span data-stu-id="65ecb-169">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="65ecb-170">**Потеря** связи ("потеря связи")</span><span class="sxs-lookup"><span data-stu-id="65ecb-170">**Lost Comm** ("Lost Comm")</span></span>


<span data-ttu-id="65ecb-171"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="65ecb-171"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="remarks"></a><span data-ttu-id="65ecb-172">Комментарии</span><span class="sxs-lookup"><span data-stu-id="65ecb-172">Remarks</span></span>

<span data-ttu-id="65ecb-173">Класс **Win32 \_ нетворкклиент** является производным от [**CIM \_ логикалелемент**](cim-logicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="65ecb-173">The **Win32\_NetworkClient** class is derived from [**CIM\_LogicalElement**](cim-logicalelement.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="65ecb-174">Требования</span><span class="sxs-lookup"><span data-stu-id="65ecb-174">Requirements</span></span>



| <span data-ttu-id="65ecb-175">Требование</span><span class="sxs-lookup"><span data-stu-id="65ecb-175">Requirement</span></span> | <span data-ttu-id="65ecb-176">Значение</span><span class="sxs-lookup"><span data-stu-id="65ecb-176">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="65ecb-177">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="65ecb-177">Minimum supported client</span></span><br/> | <span data-ttu-id="65ecb-178">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="65ecb-178">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="65ecb-179">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="65ecb-179">Minimum supported server</span></span><br/> | <span data-ttu-id="65ecb-180">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="65ecb-180">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="65ecb-181">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="65ecb-181">Namespace</span></span><br/>                | <span data-ttu-id="65ecb-182">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="65ecb-182">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="65ecb-183">MOF</span><span class="sxs-lookup"><span data-stu-id="65ecb-183">MOF</span></span><br/>                      | <dl> <span data-ttu-id="65ecb-184"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="65ecb-184"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="65ecb-185">DLL</span><span class="sxs-lookup"><span data-stu-id="65ecb-185">DLL</span></span><br/>                      | <dl> <span data-ttu-id="65ecb-186"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="65ecb-186"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="65ecb-187">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="65ecb-187">See also</span></span>

<dl> <dt>

[<span data-ttu-id="65ecb-188">**\_ЛОГИКАЛЕЛЕМЕНТ CIM**</span><span class="sxs-lookup"><span data-stu-id="65ecb-188">**CIM\_LogicalElement**</span></span>](cim-logicalelement.md)
</dt> <dt>

[<span data-ttu-id="65ecb-189">Классы операционной системы</span><span class="sxs-lookup"><span data-stu-id="65ecb-189">Operating System Classes</span></span>](./operating-system-classes.md)
</dt> </dl>

 

 
