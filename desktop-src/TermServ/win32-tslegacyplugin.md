---
title: Класс Win32_TSLegacyPlugin
description: Представляет удаленный рабочий стол сервер, который встроенные подключаемые модули службы управление подключениями к удаленным рабочим столам и приложениям RemoteApp будут запрашивать программы RemoteApp.
ms.assetid: 99bec477-ae9d-4bc9-bf9d-11a4e439306b
ms.tgt_platform: multiple
keywords:
- Класс Win32_TSLegacyPlugin службы удаленных рабочих столов
- Службы удаленных рабочих столов класса Win32_TSLegacyPlugin, описание
topic_type:
- apiref
api_name:
- Win32_TSLegacyPlugin
- Win32_TSLegacyPlugin.Caption
- Win32_TSLegacyPlugin.Description
- Win32_TSLegacyPlugin.InstallDate
- Win32_TSLegacyPlugin.Name
- Win32_TSLegacyPlugin.Status
- Win32_TSLegacyPlugin.Type
api_location:
- TscPubWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 548eadac272f6f87daf1c43020cb65485e434aec
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105681770"
---
# <a name="win32_tslegacyplugin-class"></a><span data-ttu-id="6545a-105">\_Класс Win32 тслегациплугин</span><span class="sxs-lookup"><span data-stu-id="6545a-105">Win32\_TSLegacyPlugin class</span></span>

<span data-ttu-id="6545a-106">Представляет удаленный рабочий стол сервер, который встроенные подключаемые модули службы управление подключениями к удаленным рабочим столам и приложениям RemoteApp будут запрашивать программы RemoteApp.</span><span class="sxs-lookup"><span data-stu-id="6545a-106">Represents a Remote Desktop server that the built-in RemoteApp and Desktop Connection Management Service plug-ins will query for RemoteApp programs.</span></span>

<span data-ttu-id="6545a-107">Следующий пример синтаксиса — упрощенный MOF-код, который включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="6545a-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

<span data-ttu-id="6545a-108">Этот класс является устаревшим, начиная с Windows Server 2012.</span><span class="sxs-lookup"><span data-stu-id="6545a-108">This class is deprecated beginning with Windows Server 2012.</span></span>

## <a name="syntax"></a><span data-ttu-id="6545a-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="6545a-109">Syntax</span></span>

``` syntax
[DEPRECATED, dynamic, provider("Win32_TSCentralPublisher_Prov")]
class Win32_TSLegacyPlugin : CIM_LogicalElement
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
  sint32   Type;
};
```

## <a name="members"></a><span data-ttu-id="6545a-110">Члены</span><span class="sxs-lookup"><span data-stu-id="6545a-110">Members</span></span>

<span data-ttu-id="6545a-111">Класс **Win32 \_ тслегациплугин** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="6545a-111">The **Win32\_TSLegacyPlugin** class has these types of members:</span></span>

-   [<span data-ttu-id="6545a-112">Свойства</span><span class="sxs-lookup"><span data-stu-id="6545a-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="6545a-113">Свойства</span><span class="sxs-lookup"><span data-stu-id="6545a-113">Properties</span></span>

<span data-ttu-id="6545a-114">Класс **Win32 \_ тслегациплугин** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="6545a-114">The **Win32\_TSLegacyPlugin** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="6545a-115">**Заголовок**</span><span class="sxs-lookup"><span data-stu-id="6545a-115">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6545a-116">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="6545a-116">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6545a-117">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="6545a-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6545a-118">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="6545a-118">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="6545a-119">Краткое описание (однострочная строка) объекта.</span><span class="sxs-lookup"><span data-stu-id="6545a-119">Short description (one-line string) of the object.</span></span>

<span data-ttu-id="6545a-120">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="6545a-120">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="6545a-121">**Описание**</span><span class="sxs-lookup"><span data-stu-id="6545a-121">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6545a-122">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="6545a-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6545a-123">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="6545a-123">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6545a-124">Описание объекта.</span><span class="sxs-lookup"><span data-stu-id="6545a-124">Description of the object.</span></span>

<span data-ttu-id="6545a-125">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="6545a-125">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="6545a-126">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="6545a-126">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6545a-127">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="6545a-127">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="6545a-128">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="6545a-128">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6545a-129">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. \|Значение ComponentID \| 001,5 в DMTF</span><span class="sxs-lookup"><span data-stu-id="6545a-129">Qualifiers: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5")</span></span>
</dt> </dl>

<span data-ttu-id="6545a-130">Дата установки объекта.</span><span class="sxs-lookup"><span data-stu-id="6545a-130">The date the object was installed.</span></span> <span data-ttu-id="6545a-131">Отсутствие значения не означает, что объект не установлен.</span><span class="sxs-lookup"><span data-stu-id="6545a-131">A lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="6545a-132">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="6545a-132">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="6545a-133">**Name**</span><span class="sxs-lookup"><span data-stu-id="6545a-133">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6545a-134">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="6545a-134">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6545a-135">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="6545a-135">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6545a-136">Имя объекта.</span><span class="sxs-lookup"><span data-stu-id="6545a-136">The name of the object.</span></span>

<span data-ttu-id="6545a-137">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="6545a-137">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="6545a-138">**Состояние**</span><span class="sxs-lookup"><span data-stu-id="6545a-138">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6545a-139">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="6545a-139">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6545a-140">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="6545a-140">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6545a-141">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span><span class="sxs-lookup"><span data-stu-id="6545a-141">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span></span>
</dt> </dl>

<span data-ttu-id="6545a-142">Текущее состояние объекта.</span><span class="sxs-lookup"><span data-stu-id="6545a-142">Current status of the object.</span></span> <span data-ttu-id="6545a-143">Можно определить различные операционные и неоперационные состояния.</span><span class="sxs-lookup"><span data-stu-id="6545a-143">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="6545a-144">Рабочие состояния включают: "ОК", "деградация" и "пред-ошибка" (элемент, например жесткий диск с поддержкой SMART, может работать правильно, но прогнозировать сбой в ближайшем будущем).</span><span class="sxs-lookup"><span data-stu-id="6545a-144">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="6545a-145">Неработающие состояния включают: "ошибка", "Запуск", "остановка" и "служба".</span><span class="sxs-lookup"><span data-stu-id="6545a-145">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="6545a-146">Последняя, «служба», может применяться во время зеркального копирования диска, перезагрузки списка разрешений пользователя или другой административной работы.</span><span class="sxs-lookup"><span data-stu-id="6545a-146">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="6545a-147">Не вся такая работа выполняется в интерактивном состоянии, но управляемый элемент не является ни "ОК", ни одним из других состояний.</span><span class="sxs-lookup"><span data-stu-id="6545a-147">Not all such work is on-line, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="6545a-148">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="6545a-148">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<dt>



 <span data-ttu-id="6545a-149">("ОК")</span><span class="sxs-lookup"><span data-stu-id="6545a-149">("OK")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="6545a-150">("Ошибка")</span><span class="sxs-lookup"><span data-stu-id="6545a-150">("Error")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="6545a-151">("Пониженное состояние")</span><span class="sxs-lookup"><span data-stu-id="6545a-151">("Degraded")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="6545a-152">("Неизвестно")</span><span class="sxs-lookup"><span data-stu-id="6545a-152">("Unknown")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="6545a-153">("Пред Fail")</span><span class="sxs-lookup"><span data-stu-id="6545a-153">("Pred Fail")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="6545a-154">("Запуск")</span><span class="sxs-lookup"><span data-stu-id="6545a-154">("Starting")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="6545a-155">("Остановка")</span><span class="sxs-lookup"><span data-stu-id="6545a-155">("Stopping")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="6545a-156">("Служба")</span><span class="sxs-lookup"><span data-stu-id="6545a-156">("Service")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="6545a-157">**Тип**</span><span class="sxs-lookup"><span data-stu-id="6545a-157">**Type**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6545a-158">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="6545a-158">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="6545a-159">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="6545a-159">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="6545a-160">Тип сервера службы удаленных рабочих столов.</span><span class="sxs-lookup"><span data-stu-id="6545a-160">The type of the Remote Desktop Services server.</span></span>

<dt>

<span id="Terminal_Server_0_"></span><span id="terminal_server_0_"></span><span id="TERMINAL_SERVER_0_"></span>

<span data-ttu-id="6545a-161"><span id="Terminal_Server_0_"></span><span id="terminal_server_0_"></span><span id="TERMINAL_SERVER_0_"></span>**Сервер терминалов (0** ) (0)</span><span class="sxs-lookup"><span data-stu-id="6545a-161"><span id="Terminal_Server_0_"></span><span id="terminal_server_0_"></span><span id="TERMINAL_SERVER_0_"></span>**Terminal Server(0)** (0)</span></span>


</dt> <dd>

<span data-ttu-id="6545a-162">Удаленный рабочий стол Server.</span><span class="sxs-lookup"><span data-stu-id="6545a-162">Remote Desktop server.</span></span>

</dd> <dt>

<span id="Dummy_Terminal_Server_for_VM_Farm_1_"></span><span id="dummy_terminal_server_for_vm_farm_1_"></span><span id="DUMMY_TERMINAL_SERVER_FOR_VM_FARM_1_"></span>

<span data-ttu-id="6545a-163"><span id="Dummy_Terminal_Server_for_VM_Farm_1_"></span><span id="dummy_terminal_server_for_vm_farm_1_"></span><span id="DUMMY_TERMINAL_SERVER_FOR_VM_FARM_1_"></span>**Фиктивный сервер терминалов для фермы виртуальных машин (** 1) (1)</span><span class="sxs-lookup"><span data-stu-id="6545a-163"><span id="Dummy_Terminal_Server_for_VM_Farm_1_"></span><span id="dummy_terminal_server_for_vm_farm_1_"></span><span id="DUMMY_TERMINAL_SERVER_FOR_VM_FARM_1_"></span>**Dummy Terminal Server for VM Farm(1)** (1)</span></span>


</dt> <dd>

<span data-ttu-id="6545a-164">Искусственный удаленный рабочий стол Server для фермы виртуальных машин.</span><span class="sxs-lookup"><span data-stu-id="6545a-164">Artificial Remote Desktop server for a VM farm.</span></span>

</dd> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="6545a-165">Требования</span><span class="sxs-lookup"><span data-stu-id="6545a-165">Requirements</span></span>



| <span data-ttu-id="6545a-166">Требование</span><span class="sxs-lookup"><span data-stu-id="6545a-166">Requirement</span></span> | <span data-ttu-id="6545a-167">Значение</span><span class="sxs-lookup"><span data-stu-id="6545a-167">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="6545a-168">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="6545a-168">Minimum supported client</span></span><br/> | <span data-ttu-id="6545a-169">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="6545a-169">None supported</span></span><br/>                                                                |
| <span data-ttu-id="6545a-170">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="6545a-170">Minimum supported server</span></span><br/> | <span data-ttu-id="6545a-171">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="6545a-171">Windows Server 2008 R2</span></span><br/>                                                        |
| <span data-ttu-id="6545a-172">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="6545a-172">Namespace</span></span><br/>                | <span data-ttu-id="6545a-173">Корневой \\ CIMv2 \\ терминалсервицес</span><span class="sxs-lookup"><span data-stu-id="6545a-173">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="6545a-174">MOF</span><span class="sxs-lookup"><span data-stu-id="6545a-174">MOF</span></span><br/>                      | <dl> <span data-ttu-id="6545a-175"><dt>Тскпуб. mof</dt></span><span class="sxs-lookup"><span data-stu-id="6545a-175"><dt>TscPub.mof</dt></span></span> </dl>    |
| <span data-ttu-id="6545a-176">DLL</span><span class="sxs-lookup"><span data-stu-id="6545a-176">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6545a-177"><dt>TscPubWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6545a-177"><dt>TscPubWmi.dll</dt></span></span> </dl> |



 

