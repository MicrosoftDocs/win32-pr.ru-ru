---
description: Описание виртуальных аспектов виртуальной системы с помощью набора свойств, связанных с виртуализацией. CIM \_ виртуалсистемсеттингдата также используется в качестве класса верхнего уровня конфигураций виртуальных систем.
ms.assetid: 501e659d-f190-41f9-aafa-447048a60e7c
title: Класс CIM_VirtualSystemSettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_VirtualSystemSettingData
- CIM_VirtualSystemSettingData.VirtualSystemIdentifier
- CIM_VirtualSystemSettingData.VirtualSystemType
- CIM_VirtualSystemSettingData.Notes
- CIM_VirtualSystemSettingData.CreationTime
- CIM_VirtualSystemSettingData.ConfigurationID
- CIM_VirtualSystemSettingData.ConfigurationDataRoot
- CIM_VirtualSystemSettingData.ConfigurationFile
- CIM_VirtualSystemSettingData.SnapshotDataRoot
- CIM_VirtualSystemSettingData.SuspendDataRoot
- CIM_VirtualSystemSettingData.SwapFileDataRoot
- CIM_VirtualSystemSettingData.LogDataRoot
- CIM_VirtualSystemSettingData.AutomaticStartupAction
- CIM_VirtualSystemSettingData.AutomaticStartupActionDelay
- CIM_VirtualSystemSettingData.AutomaticStartupActionSequenceNumber
- CIM_VirtualSystemSettingData.AutomaticShutdownAction
- CIM_VirtualSystemSettingData.AutomaticRecoveryAction
- CIM_VirtualSystemSettingData.RecoveryFile
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: ff2c9725c8469b3e2c29d2e98a708d27e80378f1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105663997"
---
# <a name="cim_virtualsystemsettingdata-class"></a><span data-ttu-id="3d796-104">\_Класс CIM виртуалсистемсеттингдата</span><span class="sxs-lookup"><span data-stu-id="3d796-104">CIM\_VirtualSystemSettingData class</span></span>

<span data-ttu-id="3d796-105">Описание виртуальных аспектов виртуальной системы с помощью набора свойств, связанных с виртуализацией.</span><span class="sxs-lookup"><span data-stu-id="3d796-105">Describes the virtual aspects of a virtual system through a set of virtualization specific properties.</span></span> <span data-ttu-id="3d796-106">**Модель CIM \_ Виртуалсистемсеттингдата** также используется в качестве класса верхнего уровня конфигураций виртуальных систем.</span><span class="sxs-lookup"><span data-stu-id="3d796-106">**CIM\_VirtualSystemSettingData** is also used as the top level class of virtual system configurations.</span></span>

## <a name="syntax"></a><span data-ttu-id="3d796-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="3d796-107">Syntax</span></span>

``` syntax
[Abstract, Version("2.25.0"), UMLPackagePath("CIM::System::SystemElements"), AMENDMENT]
class CIM_VirtualSystemSettingData : CIM_SettingData
{
  string   VirtualSystemIdentifier;
  string   VirtualSystemType;
  string   Notes[];
  datetime CreationTime;
  string   ConfigurationID;
  string   ConfigurationDataRoot;
  string   ConfigurationFile;
  string   SnapshotDataRoot;
  string   SuspendDataRoot;
  string   SwapFileDataRoot;
  string   LogDataRoot;
  uint16   AutomaticStartupAction;
  datetime AutomaticStartupActionDelay;
  uint16   AutomaticStartupActionSequenceNumber;
  uint16   AutomaticShutdownAction;
  uint16   AutomaticRecoveryAction;
  string   RecoveryFile;
};
```

## <a name="members"></a><span data-ttu-id="3d796-108">Члены</span><span class="sxs-lookup"><span data-stu-id="3d796-108">Members</span></span>

<span data-ttu-id="3d796-109">Класс **CIM \_ виртуалсистемсеттингдата** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="3d796-109">The **CIM\_VirtualSystemSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="3d796-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="3d796-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="3d796-111">Свойства</span><span class="sxs-lookup"><span data-stu-id="3d796-111">Properties</span></span>

<span data-ttu-id="3d796-112">Класс **CIM \_ виртуалсистемсеттингдата** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="3d796-112">The **CIM\_VirtualSystemSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="3d796-113">**аутоматикрековеряктион**</span><span class="sxs-lookup"><span data-stu-id="3d796-113">**AutomaticRecoveryAction**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3d796-114">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="3d796-114">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="3d796-115">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="3d796-115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3d796-116">Действие, выполняемое для виртуальной системы при сбое программного обеспечения, выполняемого виртуальной системой.</span><span class="sxs-lookup"><span data-stu-id="3d796-116">The action to take for the virtual system when the software executed by the virtual system fails.</span></span> <span data-ttu-id="3d796-117">Ошибки, устраняемые этим свойством, включают только те, которые обнаруживаются платформой узла, например условие состояния ожидания без перенаправления.</span><span class="sxs-lookup"><span data-stu-id="3d796-117">The failures addressed by this property only include those that are detectable by the host platform, such as a non-interruptible wait state condition.</span></span>

<dt>

<span id="None"></span><span id="none"></span><span id="NONE"></span>

<span data-ttu-id="3d796-118">**Нет** (2)</span><span class="sxs-lookup"><span data-stu-id="3d796-118">**None** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Restart"></span><span id="restart"></span><span id="RESTART"></span>

<span data-ttu-id="3d796-119">**Перезапустить** (3)</span><span class="sxs-lookup"><span data-stu-id="3d796-119">**Restart** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Revert_to_snapshot"></span><span id="revert_to_snapshot"></span><span id="REVERT_TO_SNAPSHOT"></span>

<span data-ttu-id="3d796-120">**Вернуться к моментальному снимку** (4)</span><span class="sxs-lookup"><span data-stu-id="3d796-120">**Revert to snapshot** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="3d796-121">**Зарезервировано DMTF** (..)</span><span class="sxs-lookup"><span data-stu-id="3d796-121">**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="3d796-122">**аутоматикшутдовнактион**</span><span class="sxs-lookup"><span data-stu-id="3d796-122">**AutomaticShutdownAction**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3d796-123">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="3d796-123">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="3d796-124">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="3d796-124">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3d796-125">Действие, выполняемое для виртуальной системы при завершении работы узла.</span><span class="sxs-lookup"><span data-stu-id="3d796-125">The action to take for the virtual system when the host is shut down.</span></span>

<dt>

<span id="Turn_Off"></span><span id="turn_off"></span><span id="TURN_OFF"></span>

<span data-ttu-id="3d796-126">**Выключить (2** )</span><span class="sxs-lookup"><span data-stu-id="3d796-126">**Turn Off** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Save_state"></span><span id="save_state"></span><span id="SAVE_STATE"></span>

<span data-ttu-id="3d796-127">**Сохранить состояние** (3)</span><span class="sxs-lookup"><span data-stu-id="3d796-127">**Save state** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Shutdown"></span><span id="shutdown"></span><span id="SHUTDOWN"></span>

<span data-ttu-id="3d796-128">**Завершение работы** (4)</span><span class="sxs-lookup"><span data-stu-id="3d796-128">**Shutdown** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="3d796-129">**Зарезервировано DMTF** (..)</span><span class="sxs-lookup"><span data-stu-id="3d796-129">**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="3d796-130">**аутоматикстартупактион**</span><span class="sxs-lookup"><span data-stu-id="3d796-130">**AutomaticStartupAction**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3d796-131">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="3d796-131">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="3d796-132">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="3d796-132">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3d796-133">Действие, выполняемое в виртуальной системе при запуске узла.</span><span class="sxs-lookup"><span data-stu-id="3d796-133">The action to take on the virtual system when the host is started.</span></span>

<dt>

<span id="None"></span><span id="none"></span><span id="NONE"></span>

<span data-ttu-id="3d796-134">**Нет** (2)</span><span class="sxs-lookup"><span data-stu-id="3d796-134">**None** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Restart_if_previously_active"></span><span id="restart_if_previously_active"></span><span id="RESTART_IF_PREVIOUSLY_ACTIVE"></span>

<span data-ttu-id="3d796-135">**Перезапустить, если ранее активна** (3)</span><span class="sxs-lookup"><span data-stu-id="3d796-135">**Restart if previously active** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Always_startup"></span><span id="always_startup"></span><span id="ALWAYS_STARTUP"></span>

<span data-ttu-id="3d796-136">**Всегда запуска** (4)</span><span class="sxs-lookup"><span data-stu-id="3d796-136">**Always startup** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="3d796-137">**Зарезервировано DMTF** (..)</span><span class="sxs-lookup"><span data-stu-id="3d796-137">**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="3d796-138">**аутоматикстартупактионделай**</span><span class="sxs-lookup"><span data-stu-id="3d796-138">**AutomaticStartupActionDelay**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3d796-139">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="3d796-139">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="3d796-140">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="3d796-140">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3d796-141">Задержка для действия запуска.</span><span class="sxs-lookup"><span data-stu-id="3d796-141">The delay for the startup action.</span></span> <span data-ttu-id="3d796-142">Это значение является вариантом интервала для типа данных **DateTime** .</span><span class="sxs-lookup"><span data-stu-id="3d796-142">This value is an interval variant of the **datetime** data type.</span></span>

</dd> <dt>

<span data-ttu-id="3d796-143">**аутоматикстартупактионсекуенценумбер**</span><span class="sxs-lookup"><span data-stu-id="3d796-143">**AutomaticStartupActionSequenceNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3d796-144">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="3d796-144">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="3d796-145">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="3d796-145">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3d796-146">Порядковый номер активации виртуальной системы при запуске главной системы.</span><span class="sxs-lookup"><span data-stu-id="3d796-146">The sequence number for virtual system activation when the host system is started.</span></span> <span data-ttu-id="3d796-147">Меньшее значение указывает на более раннюю активацию.</span><span class="sxs-lookup"><span data-stu-id="3d796-147">A lower number indicates earlier activation.</span></span> <span data-ttu-id="3d796-148">Если одна или несколько конфигураций отображают одно и то же значение, последовательность зависит от реализации.</span><span class="sxs-lookup"><span data-stu-id="3d796-148">If one or more configurations show the same value, the sequence is implementation dependent.</span></span> <span data-ttu-id="3d796-149">Значение "0" указывает, что последовательность зависит от реализации.</span><span class="sxs-lookup"><span data-stu-id="3d796-149">A value of "0" indicates that the sequence is implementation dependent.</span></span>

</dd> <dt>

<span data-ttu-id="3d796-150">**конфигуратиондатарут**</span><span class="sxs-lookup"><span data-stu-id="3d796-150">**ConfigurationDataRoot**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3d796-151">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="3d796-151">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3d796-152">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="3d796-152">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3d796-153">Путь к каталогу, в который хранится информация о конфигурации виртуальной системы.</span><span class="sxs-lookup"><span data-stu-id="3d796-153">The file path of the directory where information about the virtual system configuration is stored.</span></span> <span data-ttu-id="3d796-154">Формат этого свойства — URI, основанный на RFC 2079.</span><span class="sxs-lookup"><span data-stu-id="3d796-154">The format of this property is a URI based on RFC 2079.</span></span>

</dd> <dt>

<span data-ttu-id="3d796-155">**Файл ConfigurationFile**</span><span class="sxs-lookup"><span data-stu-id="3d796-155">**ConfigurationFile**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3d796-156">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="3d796-156">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3d796-157">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="3d796-157">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3d796-158">Относительный путь к файлу, где хранятся сведения о конфигурации виртуальной системы.</span><span class="sxs-lookup"><span data-stu-id="3d796-158">The relative path of the file where information about the virtual system configuration is stored.</span></span> <span data-ttu-id="3d796-159">Относительный путь добавляет к значению свойства **конфигуратиондатарут** .</span><span class="sxs-lookup"><span data-stu-id="3d796-159">The relative path appends to the value of the **ConfigurationDataRoot** property.</span></span> <span data-ttu-id="3d796-160">Формат этого свойства — URI, основанный на RFC 2079.</span><span class="sxs-lookup"><span data-stu-id="3d796-160">The format of this property is a URI based on RFC 2079.</span></span>

</dd> <dt>

<span data-ttu-id="3d796-161">**ConfigurationID**</span><span class="sxs-lookup"><span data-stu-id="3d796-161">**ConfigurationID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3d796-162">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="3d796-162">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3d796-163">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="3d796-163">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3d796-164">Уникальный идентификатор конфигурации виртуальной системы.</span><span class="sxs-lookup"><span data-stu-id="3d796-164">The unique id of the virtual system configuration.</span></span>

> [!Note]  
> <span data-ttu-id="3d796-165">**ConfigurationID** отличается от **InstanceId** и назначается реализацией для виртуальной системы или конфигурации виртуальной системы.</span><span class="sxs-lookup"><span data-stu-id="3d796-165">**ConfigurationID** is different from the **InstanceID**, and is assigned by the implementation to a virtual system or a virtual system configuration.</span></span> <span data-ttu-id="3d796-166">**ConfigurationID** не является ключом, и одно и то же значение может возникать для нескольких экземпляров.</span><span class="sxs-lookup"><span data-stu-id="3d796-166">**ConfigurationID** is not a key, and the same value may occur for more than one instance.</span></span>

 

</dd> <dt>

<span data-ttu-id="3d796-167">**CreationTime**</span><span class="sxs-lookup"><span data-stu-id="3d796-167">**CreationTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3d796-168">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="3d796-168">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="3d796-169">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="3d796-169">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3d796-170">Дата и время создания конфигурации виртуальной системы.</span><span class="sxs-lookup"><span data-stu-id="3d796-170">The date and time when the virtual system configuration was created.</span></span>

</dd> <dt>

<span data-ttu-id="3d796-171">**логдатарут**</span><span class="sxs-lookup"><span data-stu-id="3d796-171">**LogDataRoot**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3d796-172">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="3d796-172">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3d796-173">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="3d796-173">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3d796-174">Относительный путь к каталогу, в котором хранятся сведения о журнале для виртуальной системы.</span><span class="sxs-lookup"><span data-stu-id="3d796-174">The relative file path of the directory where log information for the virtual system is stored.</span></span> <span data-ttu-id="3d796-175">Относительный путь добавляет к значению свойства **конфигуратиондатарут** .</span><span class="sxs-lookup"><span data-stu-id="3d796-175">The relative path appends to the value of the **ConfigurationDataRoot** property.</span></span> <span data-ttu-id="3d796-176">Формат этого свойства — URI, основанный на RFC 2079.</span><span class="sxs-lookup"><span data-stu-id="3d796-176">The format of this property is a URI based on RFC 2079.</span></span>

</dd> <dt>

<span data-ttu-id="3d796-177">**Примечания**</span><span class="sxs-lookup"><span data-stu-id="3d796-177">**Notes**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3d796-178">Тип данных: массив **строк**</span><span class="sxs-lookup"><span data-stu-id="3d796-178">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="3d796-179">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="3d796-179">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3d796-180">Массив, содержащий заметки пользователя, связанные с виртуальной системой.</span><span class="sxs-lookup"><span data-stu-id="3d796-180">An array that contains user supplied notes that are related to the virtual system.</span></span>

</dd> <dt>

<span data-ttu-id="3d796-181">**рековерифиле**</span><span class="sxs-lookup"><span data-stu-id="3d796-181">**RecoveryFile**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3d796-182">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="3d796-182">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3d796-183">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="3d796-183">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3d796-184">Путь к файлу, где хранятся сведения о восстановлении виртуальной системы.</span><span class="sxs-lookup"><span data-stu-id="3d796-184">The path of the file where recovery related information of the virtual system is stored.</span></span> <span data-ttu-id="3d796-185">Формат этого свойства — URI, основанный на RFC 2079.</span><span class="sxs-lookup"><span data-stu-id="3d796-185">The format of this property is a URI based on RFC 2079.</span></span>

</dd> <dt>

<span data-ttu-id="3d796-186">**снапшотдатарут**</span><span class="sxs-lookup"><span data-stu-id="3d796-186">**SnapshotDataRoot**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3d796-187">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="3d796-187">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3d796-188">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="3d796-188">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3d796-189">Относительный путь к каталогу, в котором хранятся сведения о моментальных снимках виртуальной системы.</span><span class="sxs-lookup"><span data-stu-id="3d796-189">The relative path of the directory where information about virtual system snapshots is stored.</span></span> <span data-ttu-id="3d796-190">Относительный путь добавляет к значению свойства **конфигуратиондатарут** .</span><span class="sxs-lookup"><span data-stu-id="3d796-190">The relative path appends to the value of the **ConfigurationDataRoot** property.</span></span> <span data-ttu-id="3d796-191">Формат этого свойства — URI, основанный на RFC 2079.</span><span class="sxs-lookup"><span data-stu-id="3d796-191">The format of this property is a URI based on RFC 2079.</span></span>

</dd> <dt>

<span data-ttu-id="3d796-192">**суспенддатарут**</span><span class="sxs-lookup"><span data-stu-id="3d796-192">**SuspendDataRoot**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3d796-193">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="3d796-193">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3d796-194">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="3d796-194">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3d796-195">Относительный путь к каталогу, в котором хранятся сведения о приостановке, связанные с виртуальной системой.</span><span class="sxs-lookup"><span data-stu-id="3d796-195">The relative path of the directory where suspend related information about the virtual system is stored.</span></span> <span data-ttu-id="3d796-196">Относительный путь добавляет к значению свойства **конфигуратиондатарут** .</span><span class="sxs-lookup"><span data-stu-id="3d796-196">The relative path appends to the value of the **ConfigurationDataRoot** property.</span></span> <span data-ttu-id="3d796-197">Формат этого свойства — URI, основанный на RFC 2079.</span><span class="sxs-lookup"><span data-stu-id="3d796-197">The format of this property is a URI based on RFC 2079.</span></span>

</dd> <dt>

<span data-ttu-id="3d796-198">**свапфиледатарут**</span><span class="sxs-lookup"><span data-stu-id="3d796-198">**SwapFileDataRoot**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3d796-199">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="3d796-199">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3d796-200">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="3d796-200">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3d796-201">Относительный путь к каталогу, в котором хранятся файлы подкачки виртуальной системы.</span><span class="sxs-lookup"><span data-stu-id="3d796-201">The relative file path of the directory where swap files of the virtual system are stored.</span></span> <span data-ttu-id="3d796-202">Относительный путь добавляет к значению свойства **конфигуратиондатарут** .</span><span class="sxs-lookup"><span data-stu-id="3d796-202">The relative path appends to the value of the **ConfigurationDataRoot** property.</span></span> <span data-ttu-id="3d796-203">Формат этого свойства — URI, основанный на RFC 2079.</span><span class="sxs-lookup"><span data-stu-id="3d796-203">The format of this property is a URI based on RFC 2079.</span></span>

</dd> <dt>

<span data-ttu-id="3d796-204">**виртуалсистемидентифиер**</span><span class="sxs-lookup"><span data-stu-id="3d796-204">**VirtualSystemIdentifier**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3d796-205">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="3d796-205">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3d796-206">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="3d796-206">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3d796-207">Уникальное имя системы на платформе виртуализации.</span><span class="sxs-lookup"><span data-stu-id="3d796-207">The unique name for the system within the virtualization platform.</span></span> <span data-ttu-id="3d796-208">**Виртуалсистемидентифиер** не является именем узла, назначенным экземпляру операционной системы, работающему в виртуальной системе, и не является IP-адресом или MAC адресом, назначенным ни одному из сетевых портов.</span><span class="sxs-lookup"><span data-stu-id="3d796-208">**VirtualSystemIdentifier** is not the hostname assigned to the operating system instance running within the virtual system, nor is it an IP address or MAC address assigned to any of its network ports.</span></span>

<span data-ttu-id="3d796-209">**Виртуалсистемидентифиер** может содержать правила реализации, такие как простые шаблоны или регулярное выражение, которые могут интерпретироваться реализацией при задании **виртуалсистемидентифиер**.</span><span class="sxs-lookup"><span data-stu-id="3d796-209">The **VirtualSystemIdentifier** may contain implementation specific rules, like simple patterns or a regular expression that may be interpreted by the implementation when setting **VirtualSystemIdentifier**.</span></span>

</dd> <dt>

<span data-ttu-id="3d796-210">**виртуалсистемтипе**</span><span class="sxs-lookup"><span data-stu-id="3d796-210">**VirtualSystemType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3d796-211">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="3d796-211">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3d796-212">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="3d796-212">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3d796-213">Тип виртуальной системы.</span><span class="sxs-lookup"><span data-stu-id="3d796-213">The type of the virtual system.</span></span>

> [!Note]  
> <span data-ttu-id="3d796-214">Если тип виртуальной системы неизвестен, это значение должно быть равно "DMTF: Unknown".</span><span class="sxs-lookup"><span data-stu-id="3d796-214">If the virtual system type is unknown, this value must be set to "DMTF:unknown".</span></span>

 

<span data-ttu-id="3d796-215">Это свойство форматируется с использованием следующего формата Backus Наура Form (ABNF):</span><span class="sxs-lookup"><span data-stu-id="3d796-215">This property is formatted using the following Augmented Backus Naur Form (ABNF) format:</span></span>

<span data-ttu-id="3d796-216">VS-Type = DMTF-value/другое-org-value/устаревшее значение; DMTF-value = "DMTF:", "определение-org": "org-VS-Type; другое-org-value = определение-org ":" org-VS-Type;</span><span class="sxs-lookup"><span data-stu-id="3d796-216">vs-type = dmtf-value / other-org-value / legacy-value; dmtf-value = "DMTF:" defining-org ":" org-vs-type; other-org-value = defining-org ":" org-vs-type;</span></span>

<span data-ttu-id="3d796-217">Значение приведенного выше формата ABNF:</span><span class="sxs-lookup"><span data-stu-id="3d796-217">The value of the above ABNF format are:</span></span>

-   <span data-ttu-id="3d796-218">*DMTF-value*   значение свойства, определенное DMTF и определяемое в описании этого свойства.</span><span class="sxs-lookup"><span data-stu-id="3d796-218">*dmtf-value*   a property value defined by DMTF and is defined in the description of this property.</span></span>
-   <span data-ttu-id="3d796-219">*другое-org-value*   — это значение свойства, определяемое бизнес-сущностью, отличной от DMTF, и не определена в описании этого свойства.</span><span class="sxs-lookup"><span data-stu-id="3d796-219">*other-org-value*   is a property value defined by a business entity other than DMTF and is not defined in the description of this property.</span></span>
-   <span data-ttu-id="3d796-220">*устаревшее значение*   . значение свойства, определенное бизнес-сущностью, отличной от DMTF, и не определено в описании этого свойства.</span><span class="sxs-lookup"><span data-stu-id="3d796-220">*legacy-value*   a property value defined by a business entity other than DMTF and is not defined in the description of this property.</span></span> <span data-ttu-id="3d796-221">Эти значения разрешены, но рекомендуется использовать с течением времени.</span><span class="sxs-lookup"><span data-stu-id="3d796-221">These values are permitted but recommended to be deprecated over time.</span></span>
-   <span data-ttu-id="3d796-222">*Определение-org*   идентификатор для бизнес-сущности, определяющей тип виртуальной системы.</span><span class="sxs-lookup"><span data-stu-id="3d796-222">*defining-org*   an identifier for the business entity that defines the virtual system type.</span></span> <span data-ttu-id="3d796-223">Он должен включать в себя авторские права, охраняемые товарные знаки или уникальные имена, принадлежащие бизнес-сущности.</span><span class="sxs-lookup"><span data-stu-id="3d796-223">It should include a copyrighted, trademarked, or a unique name that is owned by the business entity.</span></span> <span data-ttu-id="3d796-224">Значение должно быть не "DMTF" и не содержать двоеточия.</span><span class="sxs-lookup"><span data-stu-id="3d796-224">It should not be "DMTF" and shall not contain a colon.</span></span>
-   <span data-ttu-id="3d796-225">*org-VS — введите*   идентификатор для типа виртуальной системы в определяющей бизнес-сущности.</span><span class="sxs-lookup"><span data-stu-id="3d796-225">*org-vs-type*   an identifier for the virtual system type within the defining business entity.</span></span> <span data-ttu-id="3d796-226">Оно должно быть уникальным в рамках определения-org. org-VS-Type может использовать любой символ, разрешенный для строк CIM, за исключением следующих: u0000-U001F (элементы управления Юникода C0), U0020 (пробел), U007F (элементы управления Юникода C0) или U0080-U009F (элементы управления Юникода C1).</span><span class="sxs-lookup"><span data-stu-id="3d796-226">It should be unique within defining-org. org-vs-type may use any character allowed for CIM strings, except the following: U0000-U001F (Unicode C0 controls), U0020 (space), U007F (Unicode C0 controls), or U0080-U009F (Unicode C1 controls).</span></span>
-   <span data-ttu-id="3d796-227">Если необходимо структурировать значение по сегментам, сегменты должны быть разделены одним двоеточием.</span><span class="sxs-lookup"><span data-stu-id="3d796-227">If there is a need to structure the value into segments, the segments should be separated with a single colon.</span></span>
-   <span data-ttu-id="3d796-228">Значения этого свойства должны обрабатываться с учетом регистра.</span><span class="sxs-lookup"><span data-stu-id="3d796-228">The values of this property should be processed case sensitively.</span></span> <span data-ttu-id="3d796-229">Они предназначены для обработки программным способом, а не для отображаемого имени и должны быть короткими.</span><span class="sxs-lookup"><span data-stu-id="3d796-229">They are intended to be processed programmatically, instead of being a display name, and should be short.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="3d796-230">Требования</span><span class="sxs-lookup"><span data-stu-id="3d796-230">Requirements</span></span>



| <span data-ttu-id="3d796-231">Требование</span><span class="sxs-lookup"><span data-stu-id="3d796-231">Requirement</span></span> | <span data-ttu-id="3d796-232">Значение</span><span class="sxs-lookup"><span data-stu-id="3d796-232">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3d796-233">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="3d796-233">Minimum supported client</span></span><br/> | <span data-ttu-id="3d796-234">Windows 8</span><span class="sxs-lookup"><span data-stu-id="3d796-234">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="3d796-235">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="3d796-235">Minimum supported server</span></span><br/> | <span data-ttu-id="3d796-236">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="3d796-236">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="3d796-237">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="3d796-237">Namespace</span></span><br/>                | <span data-ttu-id="3d796-238">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="3d796-238">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="3d796-239">MOF</span><span class="sxs-lookup"><span data-stu-id="3d796-239">MOF</span></span><br/>                      | <dl> <span data-ttu-id="3d796-240"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="3d796-240"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="3d796-241">DLL</span><span class="sxs-lookup"><span data-stu-id="3d796-241">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3d796-242"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="3d796-242"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="3d796-243">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="3d796-243">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3d796-244">**\_SETTINGDATA CIM**</span><span class="sxs-lookup"><span data-stu-id="3d796-244">**CIM\_SettingData**</span></span>](cim-settingdata.md)
</dt> </dl>

 

 




