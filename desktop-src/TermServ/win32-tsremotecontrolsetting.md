---
title: Класс Win32_TSRemoteControlSetting
description: Определяет параметры конфигурации удаленного управления для \_ класса терминала Win32.
ms.assetid: 2e23915e-ee1c-4e53-8d0d-4d3fc2fefce6
ms.tgt_platform: multiple
keywords:
- Класс Win32_TSRemoteControlSetting службы удаленных рабочих столов
- Службы удаленных рабочих столов класса Win32_TSRemoteControlSetting, описание
topic_type:
- apiref
api_name:
- Win32_TSRemoteControlSetting
- Win32_TSRemoteControlSetting.Caption
- Win32_TSRemoteControlSetting.Description
- Win32_TSRemoteControlSetting.InstallDate
- Win32_TSRemoteControlSetting.Name
- Win32_TSRemoteControlSetting.Status
- Win32_TSRemoteControlSetting.TerminalName
- Win32_TSRemoteControlSetting.LevelOfControl
- Win32_TSRemoteControlSetting.PolicySourceLevelOfControl
- Win32_TSRemoteControlSetting.RemoteControlPolicy
api_location:
- TSCfgWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 96e327744ad864e14e1f2580b3b71116e448f36e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104490965"
---
# <a name="win32_tsremotecontrolsetting-class"></a><span data-ttu-id="64bd0-105">\_Класс Win32 тсремотеконтролсеттинг</span><span class="sxs-lookup"><span data-stu-id="64bd0-105">Win32\_TSRemoteControlSetting class</span></span>

<span data-ttu-id="64bd0-106">Класс **WMI \_ тсремотеконтролсеттинг** инструментария Win32 определяет параметры конфигурации удаленного управления для класса [**\_ терминала Win32**](win32-terminal.md) .</span><span class="sxs-lookup"><span data-stu-id="64bd0-106">The **Win32\_TSRemoteControlSetting** WMI class defines the remote control configuration settings for the [**Win32\_Terminal**](win32-terminal.md) class.</span></span>

<span data-ttu-id="64bd0-107">Следующий синтаксис упрощен из MOF-кода и включает все определенные и унаследованные свойства в алфавитном порядке.</span><span class="sxs-lookup"><span data-stu-id="64bd0-107">The following syntax is simplified from MOF code and includes all defined and inherited properties, in alphabetical order.</span></span> <span data-ttu-id="64bd0-108">Справочные сведения о методах см. в таблице методов далее в этом разделе.</span><span class="sxs-lookup"><span data-stu-id="64bd0-108">For reference information on methods, see the table of methods later in this topic.</span></span>

## <a name="syntax"></a><span data-ttu-id="64bd0-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="64bd0-109">Syntax</span></span>

``` syntax
[dynamic, provider("Win32_WIN32_TSREMOTECONTROLSETTING_Prov"), ClassContext("local|hkey_local_machine\\SYSTEM\\CurrentControlSet\\Control\\TerminalServer\\WinStations"), AMENDMENT]
class Win32_TSRemoteControlSetting : Win32_TerminalSetting
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
  string   TerminalName;
  uint32   LevelOfControl;
  uint32   PolicySourceLevelOfControl;
  uint32   RemoteControlPolicy;
};
```

## <a name="members"></a><span data-ttu-id="64bd0-110">Члены</span><span class="sxs-lookup"><span data-stu-id="64bd0-110">Members</span></span>

<span data-ttu-id="64bd0-111">Класс **Win32 \_ тсремотеконтролсеттинг** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="64bd0-111">The **Win32\_TSRemoteControlSetting** class has these types of members:</span></span>

-   [<span data-ttu-id="64bd0-112">Методы</span><span class="sxs-lookup"><span data-stu-id="64bd0-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="64bd0-113">Свойства</span><span class="sxs-lookup"><span data-stu-id="64bd0-113">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="64bd0-114">Методы</span><span class="sxs-lookup"><span data-stu-id="64bd0-114">Methods</span></span>

<span data-ttu-id="64bd0-115">Класс **Win32 \_ тсремотеконтролсеттинг** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="64bd0-115">The **Win32\_TSRemoteControlSetting** class has these methods.</span></span>



| <span data-ttu-id="64bd0-116">Метод</span><span class="sxs-lookup"><span data-stu-id="64bd0-116">Method</span></span>                                                              | <span data-ttu-id="64bd0-117">Описание</span><span class="sxs-lookup"><span data-stu-id="64bd0-117">Description</span></span>                                                    |
|:--------------------------------------------------------------------|:---------------------------------------------------------------|
| [<span data-ttu-id="64bd0-118">**ремотеконтрол**</span><span class="sxs-lookup"><span data-stu-id="64bd0-118">**RemoteControl**</span></span>](win32-tsremotecontrolsetting-remotecontrol.md) | <span data-ttu-id="64bd0-119">Задает свойство **левелофконтрол** этого класса.</span><span class="sxs-lookup"><span data-stu-id="64bd0-119">Sets the **LevelOfControl** property of this class.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="64bd0-120">Свойства</span><span class="sxs-lookup"><span data-stu-id="64bd0-120">Properties</span></span>

<span data-ttu-id="64bd0-121">Класс **Win32 \_ тсремотеконтролсеттинг** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="64bd0-121">The **Win32\_TSRemoteControlSetting** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="64bd0-122">**Заголовок**</span><span class="sxs-lookup"><span data-stu-id="64bd0-122">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="64bd0-123">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="64bd0-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="64bd0-124">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="64bd0-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="64bd0-125">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="64bd0-125">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="64bd0-126">Краткое описание (однострочная строка) объекта.</span><span class="sxs-lookup"><span data-stu-id="64bd0-126">Short description (one-line string) of the object.</span></span>

<span data-ttu-id="64bd0-127">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="64bd0-127">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="64bd0-128">**Описание**</span><span class="sxs-lookup"><span data-stu-id="64bd0-128">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="64bd0-129">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="64bd0-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="64bd0-130">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="64bd0-130">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="64bd0-131">Описание объекта.</span><span class="sxs-lookup"><span data-stu-id="64bd0-131">Description of the object.</span></span>

<span data-ttu-id="64bd0-132">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="64bd0-132">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="64bd0-133">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="64bd0-133">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="64bd0-134">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="64bd0-134">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="64bd0-135">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="64bd0-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="64bd0-136">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. \|Значение ComponentID \| 001,5 в DMTF</span><span class="sxs-lookup"><span data-stu-id="64bd0-136">Qualifiers: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5")</span></span>
</dt> </dl>

<span data-ttu-id="64bd0-137">Дата установки объекта.</span><span class="sxs-lookup"><span data-stu-id="64bd0-137">The date the object was installed.</span></span> <span data-ttu-id="64bd0-138">Отсутствие значения не означает, что объект не установлен.</span><span class="sxs-lookup"><span data-stu-id="64bd0-138">A lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="64bd0-139">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="64bd0-139">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="64bd0-140">**левелофконтрол**</span><span class="sxs-lookup"><span data-stu-id="64bd0-140">**LevelOfControl**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="64bd0-141">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="64bd0-141">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="64bd0-142">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="64bd0-142">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="64bd0-143">Уровень контроля для сеанса, который указывает, будет ли сеанс просматриваться только удаленным пользователем или просматриваться и контролироваться с помощью клавиатуры и мыши.</span><span class="sxs-lookup"><span data-stu-id="64bd0-143">Level of control for the session, which specifies whether the session will only be viewed by the remote user, or viewed and controlled through a keyboard and mouse.</span></span> <span data-ttu-id="64bd0-144">Дополнительные сведения см. в подразделе "Примечания" метода [**ремотеконтрол**](win32-tsremotecontrolsetting-remotecontrol.md) .</span><span class="sxs-lookup"><span data-stu-id="64bd0-144">For more information, see the Remarks section of the [**RemoteControl**](win32-tsremotecontrolsetting-remotecontrol.md) method.</span></span> <span data-ttu-id="64bd0-145">Поддерживаются следующие значения.</span><span class="sxs-lookup"><span data-stu-id="64bd0-145">The following values are supported.</span></span>

<dt>

<span id="Disable"></span><span id="disable"></span><span id="DISABLE"></span>

<span data-ttu-id="64bd0-146"><span id="Disable"></span><span id="disable"></span><span id="DISABLE"></span>**Отключить** (0)</span><span class="sxs-lookup"><span data-stu-id="64bd0-146"><span id="Disable"></span><span id="disable"></span><span id="DISABLE"></span>**Disable** (0)</span></span>


</dt> <dd>

<span data-ttu-id="64bd0-147">Удаленное управление отключено.</span><span class="sxs-lookup"><span data-stu-id="64bd0-147">Remote control is disabled.</span></span>

</dd> <dt>

<span id="EnableInputNotify"></span><span id="enableinputnotify"></span><span id="ENABLEINPUTNOTIFY"></span>

<span data-ttu-id="64bd0-148"><span id="EnableInputNotify"></span><span id="enableinputnotify"></span><span id="ENABLEINPUTNOTIFY"></span>**Енаблеинпутнотифи** (1)</span><span class="sxs-lookup"><span data-stu-id="64bd0-148"><span id="EnableInputNotify"></span><span id="enableinputnotify"></span><span id="ENABLEINPUTNOTIFY"></span>**EnableInputNotify** (1)</span></span>


</dt> <dd>

<span data-ttu-id="64bd0-149">Пользователь удаленного управления имеет полный контроль над сеансом пользователя с разрешением пользователя.</span><span class="sxs-lookup"><span data-stu-id="64bd0-149">The user of remote control has full control of the user's session, with the user's permission.</span></span>

</dd> <dt>

<span id="EnableInputNoNotify"></span><span id="enableinputnonotify"></span><span id="ENABLEINPUTNONOTIFY"></span>

<span data-ttu-id="64bd0-150"><span id="EnableInputNoNotify"></span><span id="enableinputnonotify"></span><span id="ENABLEINPUTNONOTIFY"></span>**Енаблеинпутнонотифи** (2)</span><span class="sxs-lookup"><span data-stu-id="64bd0-150"><span id="EnableInputNoNotify"></span><span id="enableinputnonotify"></span><span id="ENABLEINPUTNONOTIFY"></span>**EnableInputNoNotify** (2)</span></span>


</dt> <dd>

<span data-ttu-id="64bd0-151">Пользователь удаленного управления имеет полный контроль над сеансом пользователя; разрешение пользователя не требуется.</span><span class="sxs-lookup"><span data-stu-id="64bd0-151">The user of remote control has full control of the user's session; the user's permission is not required.</span></span>

</dd> <dt>

<span id="EnableNoInputNotify"></span><span id="enablenoinputnotify"></span><span id="ENABLENOINPUTNOTIFY"></span>

<span data-ttu-id="64bd0-152"><span id="EnableNoInputNotify"></span><span id="enablenoinputnotify"></span><span id="ENABLENOINPUTNOTIFY"></span>**Енабленоинпутнотифи** (3)</span><span class="sxs-lookup"><span data-stu-id="64bd0-152"><span id="EnableNoInputNotify"></span><span id="enablenoinputnotify"></span><span id="ENABLENOINPUTNOTIFY"></span>**EnableNoInputNotify** (3)</span></span>


</dt> <dd>

<span data-ttu-id="64bd0-153">Пользователь удаленного управления может просматривать сеанс удаленно с разрешением пользователя; удаленный пользователь не может активно управлять сеансом.</span><span class="sxs-lookup"><span data-stu-id="64bd0-153">The user of remote control can view the session remotely, with the user's permission; the remote user cannot actively control the session.</span></span>

</dd> <dt>

<span id="EnableNoInputNoNotify"></span><span id="enablenoinputnonotify"></span><span id="ENABLENOINPUTNONOTIFY"></span>

<span data-ttu-id="64bd0-154"><span id="EnableNoInputNoNotify"></span><span id="enablenoinputnonotify"></span><span id="ENABLENOINPUTNONOTIFY"></span>**Енабленоинпутнонотифи** (4)</span><span class="sxs-lookup"><span data-stu-id="64bd0-154"><span id="EnableNoInputNoNotify"></span><span id="enablenoinputnonotify"></span><span id="ENABLENOINPUTNONOTIFY"></span>**EnableNoInputNoNotify** (4)</span></span>


</dt> <dd>

<span data-ttu-id="64bd0-155">Пользователь удаленного управления может просматривать сеанс удаленно, но не управляет им активно. разрешение пользователя не требуется.</span><span class="sxs-lookup"><span data-stu-id="64bd0-155">The user of remote control can view the session remotely, but not actively control the session; the user's permission is not required.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="64bd0-156">**Name**</span><span class="sxs-lookup"><span data-stu-id="64bd0-156">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="64bd0-157">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="64bd0-157">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="64bd0-158">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="64bd0-158">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="64bd0-159">Имя объекта.</span><span class="sxs-lookup"><span data-stu-id="64bd0-159">The name of the object.</span></span>

<span data-ttu-id="64bd0-160">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="64bd0-160">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="64bd0-161">**полицисаурцелевелофконтрол**</span><span class="sxs-lookup"><span data-stu-id="64bd0-161">**PolicySourceLevelOfControl**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="64bd0-162">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="64bd0-162">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="64bd0-163">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="64bd0-163">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="64bd0-164">Указывает, настроено ли свойство **левелофконтрол** сервером, групповой политикой или по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="64bd0-164">Indicates whether the **LevelOfControl** property is configured by the server, group policy, or by default.</span></span>

<dt>

<span data-ttu-id="64bd0-165">0 (0x0)</span><span class="sxs-lookup"><span data-stu-id="64bd0-165">0 (0x0)</span></span>
</dt> <dd>

<span data-ttu-id="64bd0-166">Сервер</span><span class="sxs-lookup"><span data-stu-id="64bd0-166">Server</span></span>

</dd> <dt>

<span data-ttu-id="64bd0-167">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="64bd0-167">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="64bd0-168">Групповая политика</span><span class="sxs-lookup"><span data-stu-id="64bd0-168">Group policy</span></span>

</dd> <dt>

<span data-ttu-id="64bd0-169">2 (0x2)</span><span class="sxs-lookup"><span data-stu-id="64bd0-169">2 (0x2)</span></span>
</dt> <dd>

<span data-ttu-id="64bd0-170">Значение по умолчанию</span><span class="sxs-lookup"><span data-stu-id="64bd0-170">Default</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="64bd0-171">**ремотеконтролполици**</span><span class="sxs-lookup"><span data-stu-id="64bd0-171">**RemoteControlPolicy**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="64bd0-172">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="64bd0-172">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="64bd0-173">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="64bd0-173">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="64bd0-174">Политика, используемая сервером для получения параметров удаленного управления.</span><span class="sxs-lookup"><span data-stu-id="64bd0-174">The policy the server uses to retrieve the remote control settings.</span></span>

<dt>

<span id="Per_User"></span><span id="per_user"></span><span id="PER_USER"></span>

<span data-ttu-id="64bd0-175"><span id="Per_User"></span><span id="per_user"></span><span id="PER_USER"></span>**На пользователя** (0)</span><span class="sxs-lookup"><span data-stu-id="64bd0-175"><span id="Per_User"></span><span id="per_user"></span><span id="PER_USER"></span>**Per User** (0)</span></span>


</dt> <dd>

<span data-ttu-id="64bd0-176">Параметры удаленного управления пользователя вступают в действие.</span><span class="sxs-lookup"><span data-stu-id="64bd0-176">The user's remote control settings are in effect.</span></span>

</dd> <dt>

<span id="Server-Override"></span><span id="server-override"></span><span id="SERVER-OVERRIDE"></span>

<span data-ttu-id="64bd0-177"><span id="Server-Override"></span><span id="server-override"></span><span id="SERVER-OVERRIDE"></span>**Переопределение сервера** (1)</span><span class="sxs-lookup"><span data-stu-id="64bd0-177"><span id="Server-Override"></span><span id="server-override"></span><span id="SERVER-OVERRIDE"></span>**Server-Override** (1)</span></span>


</dt> <dd>

<span data-ttu-id="64bd0-178">Параметры удаленного управления пользователя переопределяются сервером.</span><span class="sxs-lookup"><span data-stu-id="64bd0-178">The user's remote control settings are overridden by the server.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="64bd0-179">**Состояние**</span><span class="sxs-lookup"><span data-stu-id="64bd0-179">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="64bd0-180">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="64bd0-180">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="64bd0-181">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="64bd0-181">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="64bd0-182">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span><span class="sxs-lookup"><span data-stu-id="64bd0-182">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span></span>
</dt> </dl>

<span data-ttu-id="64bd0-183">Текущее состояние объекта.</span><span class="sxs-lookup"><span data-stu-id="64bd0-183">Current status of the object.</span></span> <span data-ttu-id="64bd0-184">Можно определить различные операционные и неоперационные состояния.</span><span class="sxs-lookup"><span data-stu-id="64bd0-184">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="64bd0-185">Рабочие состояния включают: "ОК", "деградация" и "пред-ошибка" (элемент, например жесткий диск с поддержкой SMART, может работать правильно, но прогнозировать сбой в ближайшем будущем).</span><span class="sxs-lookup"><span data-stu-id="64bd0-185">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="64bd0-186">Неработающие состояния включают: "ошибка", "Запуск", "остановка" и "служба".</span><span class="sxs-lookup"><span data-stu-id="64bd0-186">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="64bd0-187">Последняя, «служба», может применяться во время зеркального копирования диска, перезагрузки списка разрешений пользователя или другой административной работы.</span><span class="sxs-lookup"><span data-stu-id="64bd0-187">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="64bd0-188">Не вся такая работа выполняется в интерактивном состоянии, но управляемый элемент не является ни "ОК", ни одним из других состояний.</span><span class="sxs-lookup"><span data-stu-id="64bd0-188">Not all such work is on-line, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="64bd0-189">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="64bd0-189">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<dt>



 <span data-ttu-id="64bd0-190">("ОК")</span><span class="sxs-lookup"><span data-stu-id="64bd0-190">("OK")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="64bd0-191">("Ошибка")</span><span class="sxs-lookup"><span data-stu-id="64bd0-191">("Error")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="64bd0-192">("Пониженное состояние")</span><span class="sxs-lookup"><span data-stu-id="64bd0-192">("Degraded")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="64bd0-193">("Неизвестно")</span><span class="sxs-lookup"><span data-stu-id="64bd0-193">("Unknown")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="64bd0-194">("Пред Fail")</span><span class="sxs-lookup"><span data-stu-id="64bd0-194">("Pred Fail")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="64bd0-195">("Запуск")</span><span class="sxs-lookup"><span data-stu-id="64bd0-195">("Starting")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="64bd0-196">("Остановка")</span><span class="sxs-lookup"><span data-stu-id="64bd0-196">("Stopping")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="64bd0-197">("Служба")</span><span class="sxs-lookup"><span data-stu-id="64bd0-197">("Service")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="64bd0-198">**терминалнаме**</span><span class="sxs-lookup"><span data-stu-id="64bd0-198">**TerminalName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="64bd0-199">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="64bd0-199">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="64bd0-200">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="64bd0-200">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="64bd0-201">Имя терминала.</span><span class="sxs-lookup"><span data-stu-id="64bd0-201">The name of the terminal.</span></span>

<span data-ttu-id="64bd0-202">Это свойство наследуется из [**Win32 \_ терминалсеттинг**](win32-terminalsetting.md).</span><span class="sxs-lookup"><span data-stu-id="64bd0-202">This property is inherited from [**Win32\_TerminalSetting**](win32-terminalsetting.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="64bd0-203">Комментарии</span><span class="sxs-lookup"><span data-stu-id="64bd0-203">Remarks</span></span>

<span data-ttu-id="64bd0-204">Чтобы подключиться к \\ корневому \\ \\ пространству имен CIMV2 терминалсервицес, уровень проверки подлинности должен включать в себя конфиденциальность пакетов.</span><span class="sxs-lookup"><span data-stu-id="64bd0-204">To connect to the \\root\\CIMV2\\TerminalServices namespace, the authentication level must include packet privacy.</span></span> <span data-ttu-id="64bd0-205">Для вызовов C/C++ это будет уровень проверки подлинности **AUTHN на \_ \_ \_ уровне \_ \_ безопасности RPC C уровня "PKT**".</span><span class="sxs-lookup"><span data-stu-id="64bd0-205">For C/C++ calls, this would be an authentication level of **RPC\_C\_AUTHN\_LEVEL\_PKT\_PRIVACY**.</span></span> <span data-ttu-id="64bd0-206">Для вызовов Visual Basic и сценариев это будет уровень проверки подлинности **вбемаусентикатионлевелпктприваци** или "пктприваци" со значением 6.</span><span class="sxs-lookup"><span data-stu-id="64bd0-206">For Visual Basic and scripting calls, this would be an authentication level of **WbemAuthenticationLevelPktPrivacy** or "pktPrivacy", with a value of 6.</span></span> <span data-ttu-id="64bd0-207">В следующем примере Visual Basic Scripting Edition (VBScript) показано, как подключиться к удаленному компьютеру с использованием конфиденциальности пакетов.</span><span class="sxs-lookup"><span data-stu-id="64bd0-207">The following Visual Basic Scripting Edition (VBScript) example shows how to connect to a remote computer with packet privacy.</span></span>


```VB
strComputer = "RemoteServer1" 
Set objServices = GetObject( _
    "winmgmts:{authenticationLevel=pktPrivacy}!Root/CIMv2/TerminalServices")
```



<span data-ttu-id="64bd0-208">Файлы MOF-файл (MOF) содержат определения для классов инструментарий управления Windows (WMI) (WMI).</span><span class="sxs-lookup"><span data-stu-id="64bd0-208">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="64bd0-209">MOF-файлы не устанавливаются в составе пакета средств разработки программного обеспечения Microsoft Windows (SDK).</span><span class="sxs-lookup"><span data-stu-id="64bd0-209">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="64bd0-210">Они устанавливаются на сервере при добавлении связанной роли с помощью диспетчер сервера.</span><span class="sxs-lookup"><span data-stu-id="64bd0-210">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="64bd0-211">Дополнительные сведения о файлах MOF см. в разделе [MOF-файл (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="64bd0-211">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="64bd0-212">Требования</span><span class="sxs-lookup"><span data-stu-id="64bd0-212">Requirements</span></span>



| <span data-ttu-id="64bd0-213">Требование</span><span class="sxs-lookup"><span data-stu-id="64bd0-213">Requirement</span></span> | <span data-ttu-id="64bd0-214">Значение</span><span class="sxs-lookup"><span data-stu-id="64bd0-214">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="64bd0-215">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="64bd0-215">Minimum supported client</span></span><br/> | <span data-ttu-id="64bd0-216">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="64bd0-216">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="64bd0-217">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="64bd0-217">Minimum supported server</span></span><br/> | <span data-ttu-id="64bd0-218">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="64bd0-218">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="64bd0-219">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="64bd0-219">Namespace</span></span><br/>                | <span data-ttu-id="64bd0-220">Корневой \\ CIMv2 \\ терминалсервицес</span><span class="sxs-lookup"><span data-stu-id="64bd0-220">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="64bd0-221">MOF</span><span class="sxs-lookup"><span data-stu-id="64bd0-221">MOF</span></span><br/>                      | <dl> <span data-ttu-id="64bd0-222"><dt>Тскфгвми. mof</dt></span><span class="sxs-lookup"><span data-stu-id="64bd0-222"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="64bd0-223">DLL</span><span class="sxs-lookup"><span data-stu-id="64bd0-223">DLL</span></span><br/>                      | <dl> <span data-ttu-id="64bd0-224"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="64bd0-224"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="64bd0-225">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="64bd0-225">See also</span></span>

<dl> <dt>

[<span data-ttu-id="64bd0-226">**\_Терминал Win32**</span><span class="sxs-lookup"><span data-stu-id="64bd0-226">**Win32\_Terminal**</span></span>](win32-terminal.md)
</dt> <dt>

[<span data-ttu-id="64bd0-227">**\_Терминалсеттинг Win32**</span><span class="sxs-lookup"><span data-stu-id="64bd0-227">**Win32\_TerminalSetting**</span></span>](win32-terminalsetting.md)
</dt> </dl>

 

