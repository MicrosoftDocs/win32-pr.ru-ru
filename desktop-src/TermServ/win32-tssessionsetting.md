---
title: Класс Win32_TSSessionSetting
description: Определяет параметры конфигурации для \_ класса терминала Win32, такие как ограничения времени, а также действия по отсоединению и повторному подключению.
ms.assetid: e115f370-270c-404f-b6c6-7781c1ff376f
ms.tgt_platform: multiple
keywords:
- Класс Win32_TSSessionSetting службы удаленных рабочих столов
- Службы удаленных рабочих столов класса Win32_TSSessionSetting, описание
topic_type:
- apiref
api_name:
- Win32_TSSessionSetting
- Win32_TSSessionSetting.Caption
- Win32_TSSessionSetting.Description
- Win32_TSSessionSetting.InstallDate
- Win32_TSSessionSetting.Name
- Win32_TSSessionSetting.Status
- Win32_TSSessionSetting.TerminalName
- Win32_TSSessionSetting.ActiveSessionLimit
- Win32_TSSessionSetting.BrokenConnectionAction
- Win32_TSSessionSetting.BrokenConnectionPolicy
- Win32_TSSessionSetting.DisconnectedSessionLimit
- Win32_TSSessionSetting.IdleSessionLimit
- Win32_TSSessionSetting.PolicySourceActiveSessionLimit
- Win32_TSSessionSetting.PolicySourceBrokenConnectionAction
- Win32_TSSessionSetting.PolicySourceDisconnectedSessionLimit
- Win32_TSSessionSetting.PolicySourceIdleSessionLimit
- Win32_TSSessionSetting.PolicySourceReconnectionPolicy
- Win32_TSSessionSetting.ReconnectionPolicy
- Win32_TSSessionSetting.TimeLimitPolicy
- Win32_TSSessionSetting.EnableTimeoutWarning
api_location:
- TSCfgWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6e780cdedee0fe447499bed5013dadc2ba9b448b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104535363"
---
# <a name="win32_tssessionsetting-class"></a><span data-ttu-id="babc1-105">\_Класс Win32 тссессионсеттинг</span><span class="sxs-lookup"><span data-stu-id="babc1-105">Win32\_TSSessionSetting class</span></span>

<span data-ttu-id="babc1-106">Класс **WMI \_ тссессионсеттинг** инструментария Win32 определяет параметры конфигурации для [**класса \_ терминала Win32**](win32-terminal.md) , например ограничения по времени, а также действия по отсоединению и повторному подключению.</span><span class="sxs-lookup"><span data-stu-id="babc1-106">The **Win32\_TSSessionSetting** WMI class defines configuration settings for the [**Win32\_Terminal**](win32-terminal.md) class such as time-limits, and disconnection and reconnection actions.</span></span>

<span data-ttu-id="babc1-107">Следующий синтаксис упрощен из MOF-кода и включает все определенные и унаследованные свойства в алфавитном порядке.</span><span class="sxs-lookup"><span data-stu-id="babc1-107">The following syntax is simplified from MOF code and includes all defined and inherited properties, in alphabetical order.</span></span> <span data-ttu-id="babc1-108">Справочные сведения о методах см. в таблице методов далее в этом разделе.</span><span class="sxs-lookup"><span data-stu-id="babc1-108">For reference information on methods, see the table of methods later in this topic.</span></span>

## <a name="syntax"></a><span data-ttu-id="babc1-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="babc1-109">Syntax</span></span>

``` syntax
[dynamic, provider("Win32_WIN32_TSSESSIONSETTING_Prov"), ClassContext("local|hkey_local_machine\\SYSTEM\\CurrentControlSet\\Control\\TerminalServer\\WinStations"), AMENDMENT]
class Win32_TSSessionSetting : Win32_TerminalSetting
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
  string   TerminalName;
  uint32   ActiveSessionLimit;
  uint32   BrokenConnectionAction;
  uint32   BrokenConnectionPolicy;
  uint32   DisconnectedSessionLimit;
  uint32   IdleSessionLimit;
  uint32   PolicySourceActiveSessionLimit;
  uint32   PolicySourceBrokenConnectionAction;
  uint32   PolicySourceDisconnectedSessionLimit;
  uint32   PolicySourceIdleSessionLimit;
  uint32   PolicySourceReconnectionPolicy;
  uint32   ReconnectionPolicy;
  uint32   TimeLimitPolicy;
  uint32   EnableTimeoutWarning;
};
```

## <a name="members"></a><span data-ttu-id="babc1-110">Члены</span><span class="sxs-lookup"><span data-stu-id="babc1-110">Members</span></span>

<span data-ttu-id="babc1-111">Класс **Win32 \_ тссессионсеттинг** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="babc1-111">The **Win32\_TSSessionSetting** class has these types of members:</span></span>

-   [<span data-ttu-id="babc1-112">Методы</span><span class="sxs-lookup"><span data-stu-id="babc1-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="babc1-113">Свойства</span><span class="sxs-lookup"><span data-stu-id="babc1-113">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="babc1-114">Методы</span><span class="sxs-lookup"><span data-stu-id="babc1-114">Methods</span></span>

<span data-ttu-id="babc1-115">Класс **Win32 \_ тссессионсеттинг** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="babc1-115">The **Win32\_TSSessionSetting** class has these methods.</span></span>



| <span data-ttu-id="babc1-116">Метод</span><span class="sxs-lookup"><span data-stu-id="babc1-116">Method</span></span>                                                              | <span data-ttu-id="babc1-117">Описание</span><span class="sxs-lookup"><span data-stu-id="babc1-117">Description</span></span>                                                              |
|:--------------------------------------------------------------------|:-------------------------------------------------------------------------|
| [<span data-ttu-id="babc1-118">**брокенконнектион**</span><span class="sxs-lookup"><span data-stu-id="babc1-118">**BrokenConnection**</span></span>](win32-tssessionsetting-brokenconnection.md) | <span data-ttu-id="babc1-119">Задает свойства разорванного соединения, входящие в этот класс.</span><span class="sxs-lookup"><span data-stu-id="babc1-119">Sets the broken connection properties included in this class.</span></span><br/> |
| [<span data-ttu-id="babc1-120">**тимелимит**</span><span class="sxs-lookup"><span data-stu-id="babc1-120">**TimeLimit**</span></span>](win32-tssessionsetting-timelimit.md)               | <span data-ttu-id="babc1-121">Задает свойства предела времени, включаемые в этот класс.</span><span class="sxs-lookup"><span data-stu-id="babc1-121">Sets the time-limit properties included in this class.</span></span><br/>        |



 

### <a name="properties"></a><span data-ttu-id="babc1-122">Свойства</span><span class="sxs-lookup"><span data-stu-id="babc1-122">Properties</span></span>

<span data-ttu-id="babc1-123">Класс **Win32 \_ тссессионсеттинг** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="babc1-123">The **Win32\_TSSessionSetting** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="babc1-124">**активесессионлимит**</span><span class="sxs-lookup"><span data-stu-id="babc1-124">**ActiveSessionLimit**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="babc1-125">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="babc1-125">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="babc1-126">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="babc1-126">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="babc1-127">Максимальное количество времени в миллисекундах, выделенное для активного сеанса.</span><span class="sxs-lookup"><span data-stu-id="babc1-127">The maximum amount of time, in milliseconds, allocated to an active session.</span></span> <span data-ttu-id="babc1-128">Значение 0 указывает на бесконечное количество времени.</span><span class="sxs-lookup"><span data-stu-id="babc1-128">A value of 0 specifies an infinite amount of time.</span></span>

</dd> <dt>

<span data-ttu-id="babc1-129">**брокенконнектионактион**</span><span class="sxs-lookup"><span data-stu-id="babc1-129">**BrokenConnectionAction**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="babc1-130">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="babc1-130">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="babc1-131">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="babc1-131">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="babc1-132">Действие, которое сервер принимает в сеансе, когда подключение разорвано из-за потери сети или превышения предельного времени.</span><span class="sxs-lookup"><span data-stu-id="babc1-132">The action the server takes on the session when a connection has been broken due to network loss or exceeded time-limits.</span></span>

<dt>

<span id="Disconnect"></span><span id="disconnect"></span><span id="DISCONNECT"></span>

<span data-ttu-id="babc1-133"><span id="Disconnect"></span><span id="disconnect"></span><span id="DISCONNECT"></span>**Отключить** (0)</span><span class="sxs-lookup"><span data-stu-id="babc1-133"><span id="Disconnect"></span><span id="disconnect"></span><span id="DISCONNECT"></span>**Disconnect** (0)</span></span>


</dt> <dd>

<span data-ttu-id="babc1-134">Пользователь отключен от сеанса.</span><span class="sxs-lookup"><span data-stu-id="babc1-134">The user is disconnected from the session.</span></span>

</dd> <dt>

<span id="Terminate"></span><span id="terminate"></span><span id="TERMINATE"></span>

<span data-ttu-id="babc1-135"><span id="Terminate"></span><span id="terminate"></span><span id="TERMINATE"></span>**Завершить** (1)</span><span class="sxs-lookup"><span data-stu-id="babc1-135"><span id="Terminate"></span><span id="terminate"></span><span id="TERMINATE"></span>**Terminate** (1)</span></span>


</dt> <dd>

<span data-ttu-id="babc1-136">Сеанс окончательно удаляется с сервера.</span><span class="sxs-lookup"><span data-stu-id="babc1-136">The session is permanently deleted from the server.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="babc1-137">**брокенконнектионполици**</span><span class="sxs-lookup"><span data-stu-id="babc1-137">**BrokenConnectionPolicy**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="babc1-138">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="babc1-138">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="babc1-139">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="babc1-139">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="babc1-140">Политика, используемая сервером для определения времени разрыва подключения из-за потери сети или превышения предельного времени.</span><span class="sxs-lookup"><span data-stu-id="babc1-140">The policy the server uses to determine when to break a connection because of network loss or exceeded time-limits.</span></span>

<dt>

<span id="Server-Override"></span><span id="server-override"></span><span id="SERVER-OVERRIDE"></span>

<span data-ttu-id="babc1-141"><span id="Server-Override"></span><span id="server-override"></span><span id="SERVER-OVERRIDE"></span>**Переопределение сервера** (1)</span><span class="sxs-lookup"><span data-stu-id="babc1-141"><span id="Server-Override"></span><span id="server-override"></span><span id="SERVER-OVERRIDE"></span>**Server-Override** (1)</span></span>


</dt> <dd>

<span data-ttu-id="babc1-142">Параметры политики отключения пользователя переопределяются сервером.</span><span class="sxs-lookup"><span data-stu-id="babc1-142">The user's disconnection policy settings are overridden by the server.</span></span>

</dd> <dt>

<span id="Per_User"></span><span id="per_user"></span><span id="PER_USER"></span>

<span data-ttu-id="babc1-143"><span id="Per_User"></span><span id="per_user"></span><span id="PER_USER"></span>**На пользователя** (0)</span><span class="sxs-lookup"><span data-stu-id="babc1-143"><span id="Per_User"></span><span id="per_user"></span><span id="PER_USER"></span>**Per User** (0)</span></span>


</dt> <dd>

<span data-ttu-id="babc1-144">Параметры политики отключения пользователя вступают в действие.</span><span class="sxs-lookup"><span data-stu-id="babc1-144">The user's disconnection policy settings are in effect.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="babc1-145">**Заголовок**</span><span class="sxs-lookup"><span data-stu-id="babc1-145">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="babc1-146">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="babc1-146">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="babc1-147">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="babc1-147">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="babc1-148">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="babc1-148">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="babc1-149">Краткое описание (однострочная строка) объекта.</span><span class="sxs-lookup"><span data-stu-id="babc1-149">Short description (one-line string) of the object.</span></span>

<span data-ttu-id="babc1-150">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="babc1-150">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="babc1-151">**Описание**</span><span class="sxs-lookup"><span data-stu-id="babc1-151">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="babc1-152">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="babc1-152">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="babc1-153">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="babc1-153">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="babc1-154">Описание объекта.</span><span class="sxs-lookup"><span data-stu-id="babc1-154">Description of the object.</span></span>

<span data-ttu-id="babc1-155">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="babc1-155">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="babc1-156">**дисконнектедсессионлимит**</span><span class="sxs-lookup"><span data-stu-id="babc1-156">**DisconnectedSessionLimit**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="babc1-157">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="babc1-157">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="babc1-158">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="babc1-158">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="babc1-159">Интервал времени (в миллисекундах), по истечении которого отключенный сеанс завершается.</span><span class="sxs-lookup"><span data-stu-id="babc1-159">The time interval, in milliseconds, after which a disconnected session is terminated.</span></span> <span data-ttu-id="babc1-160">Значение 0 указывает на бесконечное количество времени.</span><span class="sxs-lookup"><span data-stu-id="babc1-160">A value of 0 specifies an infinite amount of time.</span></span>

</dd> <dt>

<span data-ttu-id="babc1-161">**енаблетимеаутварнинг**</span><span class="sxs-lookup"><span data-stu-id="babc1-161">**EnableTimeoutWarning**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="babc1-162">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="babc1-162">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="babc1-163">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="babc1-163">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="babc1-164">Включает предупреждение о превышении времени ожидания.</span><span class="sxs-lookup"><span data-stu-id="babc1-164">Enables the timeout warning.</span></span>

<span data-ttu-id="babc1-165">**Windows 7, Windows server 2008 R2, Windows Vista и Windows server 2008:** Это свойство недоступно.</span><span class="sxs-lookup"><span data-stu-id="babc1-165">**Windows 7, Windows Server 2008 R2, Windows Vista and Windows Server 2008:** This property is not available.</span></span>

</dd> <dt>

<span data-ttu-id="babc1-166">**идлесессионлимит**</span><span class="sxs-lookup"><span data-stu-id="babc1-166">**IdleSessionLimit**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="babc1-167">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="babc1-167">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="babc1-168">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="babc1-168">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="babc1-169">Интервал времени в миллисекундах, по истечении которого бездействующий сеанс завершается.</span><span class="sxs-lookup"><span data-stu-id="babc1-169">The time interval, in milliseconds, after which an idle session is terminated.</span></span> <span data-ttu-id="babc1-170">Значение 0 указывает на бесконечное количество времени.</span><span class="sxs-lookup"><span data-stu-id="babc1-170">A value of 0 specifies an infinite amount of time.</span></span>

</dd> <dt>

<span data-ttu-id="babc1-171">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="babc1-171">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="babc1-172">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="babc1-172">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="babc1-173">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="babc1-173">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="babc1-174">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. \|Значение ComponentID \| 001,5 в DMTF</span><span class="sxs-lookup"><span data-stu-id="babc1-174">Qualifiers: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5")</span></span>
</dt> </dl>

<span data-ttu-id="babc1-175">Дата установки объекта.</span><span class="sxs-lookup"><span data-stu-id="babc1-175">The date the object was installed.</span></span> <span data-ttu-id="babc1-176">Отсутствие значения не означает, что объект не установлен.</span><span class="sxs-lookup"><span data-stu-id="babc1-176">A lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="babc1-177">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="babc1-177">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="babc1-178">**Name**</span><span class="sxs-lookup"><span data-stu-id="babc1-178">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="babc1-179">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="babc1-179">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="babc1-180">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="babc1-180">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="babc1-181">Имя объекта.</span><span class="sxs-lookup"><span data-stu-id="babc1-181">The name of the object.</span></span>

<span data-ttu-id="babc1-182">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="babc1-182">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="babc1-183">**полицисаурцеактивесессионлимит**</span><span class="sxs-lookup"><span data-stu-id="babc1-183">**PolicySourceActiveSessionLimit**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="babc1-184">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="babc1-184">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="babc1-185">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="babc1-185">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="babc1-186">Указывает, настроено ли свойство **активесессионлимит** сервером, групповой политикой или по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="babc1-186">Indicates whether the **ActiveSessionLimit** property is configured by the server, group policy, or by default.</span></span>

<dt>

<span data-ttu-id="babc1-187">0</span><span class="sxs-lookup"><span data-stu-id="babc1-187">0</span></span>
</dt> <dd>

<span data-ttu-id="babc1-188">Сервер</span><span class="sxs-lookup"><span data-stu-id="babc1-188">Server</span></span>

</dd> <dt>

<span data-ttu-id="babc1-189">1</span><span class="sxs-lookup"><span data-stu-id="babc1-189">1</span></span>
</dt> <dd>

<span data-ttu-id="babc1-190">Групповая политика</span><span class="sxs-lookup"><span data-stu-id="babc1-190">Group policy</span></span>

</dd> <dt>

<span data-ttu-id="babc1-191">2</span><span class="sxs-lookup"><span data-stu-id="babc1-191">2</span></span>
</dt> <dd>

<span data-ttu-id="babc1-192">Значение по умолчанию</span><span class="sxs-lookup"><span data-stu-id="babc1-192">Default</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="babc1-193">**полицисаурцеброкенконнектионактион**</span><span class="sxs-lookup"><span data-stu-id="babc1-193">**PolicySourceBrokenConnectionAction**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="babc1-194">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="babc1-194">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="babc1-195">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="babc1-195">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="babc1-196">Указывает, настроено ли свойство **брокенконнектионактион** сервером, групповой политикой или по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="babc1-196">Indicates whether the **BrokenConnectionAction** property is configured by the server, group policy, or by default.</span></span>

<dt>

<span data-ttu-id="babc1-197">0</span><span class="sxs-lookup"><span data-stu-id="babc1-197">0</span></span>
</dt> <dd>

<span data-ttu-id="babc1-198">Сервер</span><span class="sxs-lookup"><span data-stu-id="babc1-198">Server</span></span>

</dd> <dt>

<span data-ttu-id="babc1-199">1</span><span class="sxs-lookup"><span data-stu-id="babc1-199">1</span></span>
</dt> <dd>

<span data-ttu-id="babc1-200">Групповая политика</span><span class="sxs-lookup"><span data-stu-id="babc1-200">Group policy</span></span>

</dd> <dt>

<span data-ttu-id="babc1-201">2</span><span class="sxs-lookup"><span data-stu-id="babc1-201">2</span></span>
</dt> <dd>

<span data-ttu-id="babc1-202">Значение по умолчанию</span><span class="sxs-lookup"><span data-stu-id="babc1-202">Default</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="babc1-203">**полицисаурцедисконнектедсессионлимит**</span><span class="sxs-lookup"><span data-stu-id="babc1-203">**PolicySourceDisconnectedSessionLimit**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="babc1-204">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="babc1-204">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="babc1-205">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="babc1-205">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="babc1-206">Указывает, настроено ли свойство **дисконнектедсессионлимит** сервером, групповой политикой или по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="babc1-206">Indicates whether the **DisconnectedSessionLimit** property is configured by the server, group policy, or by default.</span></span>

<dt>

<span data-ttu-id="babc1-207">0</span><span class="sxs-lookup"><span data-stu-id="babc1-207">0</span></span>
</dt> <dd>

<span data-ttu-id="babc1-208">Сервер</span><span class="sxs-lookup"><span data-stu-id="babc1-208">Server</span></span>

</dd> <dt>

<span data-ttu-id="babc1-209">1</span><span class="sxs-lookup"><span data-stu-id="babc1-209">1</span></span>
</dt> <dd>

<span data-ttu-id="babc1-210">Групповая политика</span><span class="sxs-lookup"><span data-stu-id="babc1-210">Group policy</span></span>

</dd> <dt>

<span data-ttu-id="babc1-211">2</span><span class="sxs-lookup"><span data-stu-id="babc1-211">2</span></span>
</dt> <dd>

<span data-ttu-id="babc1-212">Значение по умолчанию</span><span class="sxs-lookup"><span data-stu-id="babc1-212">Default</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="babc1-213">**полицисаурцеидлесессионлимит**</span><span class="sxs-lookup"><span data-stu-id="babc1-213">**PolicySourceIdleSessionLimit**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="babc1-214">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="babc1-214">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="babc1-215">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="babc1-215">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="babc1-216">Указывает, настроено ли свойство **идлесессионлимит** сервером, групповой политикой или по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="babc1-216">Indicates whether the **IdleSessionLimit** property is configured by the server, group policy, or by default.</span></span>

<dt>

<span data-ttu-id="babc1-217">0</span><span class="sxs-lookup"><span data-stu-id="babc1-217">0</span></span>
</dt> <dd>

<span data-ttu-id="babc1-218">Сервер</span><span class="sxs-lookup"><span data-stu-id="babc1-218">Server</span></span>

</dd> <dt>

<span data-ttu-id="babc1-219">1</span><span class="sxs-lookup"><span data-stu-id="babc1-219">1</span></span>
</dt> <dd>

<span data-ttu-id="babc1-220">Групповая политика</span><span class="sxs-lookup"><span data-stu-id="babc1-220">Group policy</span></span>

</dd> <dt>

<span data-ttu-id="babc1-221">2</span><span class="sxs-lookup"><span data-stu-id="babc1-221">2</span></span>
</dt> <dd>

<span data-ttu-id="babc1-222">Значение по умолчанию</span><span class="sxs-lookup"><span data-stu-id="babc1-222">Default</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="babc1-223">**полицисаурцереконнектионполици**</span><span class="sxs-lookup"><span data-stu-id="babc1-223">**PolicySourceReconnectionPolicy**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="babc1-224">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="babc1-224">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="babc1-225">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="babc1-225">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="babc1-226">Указывает, настроено ли свойство **реконнектполици** сервером, групповой политикой или по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="babc1-226">Indicates whether the **ReconnectPolicy** property is configured by the server, group policy, or by default.</span></span>

<dt>

<span data-ttu-id="babc1-227">0</span><span class="sxs-lookup"><span data-stu-id="babc1-227">0</span></span>
</dt> <dd>

<span data-ttu-id="babc1-228">Сервер</span><span class="sxs-lookup"><span data-stu-id="babc1-228">Server</span></span>

</dd> <dt>

<span data-ttu-id="babc1-229">1</span><span class="sxs-lookup"><span data-stu-id="babc1-229">1</span></span>
</dt> <dd>

<span data-ttu-id="babc1-230">Групповая политика</span><span class="sxs-lookup"><span data-stu-id="babc1-230">Group policy</span></span>

</dd> <dt>

<span data-ttu-id="babc1-231">2</span><span class="sxs-lookup"><span data-stu-id="babc1-231">2</span></span>
</dt> <dd>

<span data-ttu-id="babc1-232">Значение по умолчанию</span><span class="sxs-lookup"><span data-stu-id="babc1-232">Default</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="babc1-233">**реконнектионполици**</span><span class="sxs-lookup"><span data-stu-id="babc1-233">**ReconnectionPolicy**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="babc1-234">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="babc1-234">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="babc1-235">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="babc1-235">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="babc1-236">Указывает, должен ли пользователь использовать предыдущий клиент для повторного подключения к отключенному сеансу.</span><span class="sxs-lookup"><span data-stu-id="babc1-236">Specifies whether a user must use the previous client to reconnect to a disconnected session.</span></span>

<dt>

<span id="Any_Client"></span><span id="any_client"></span><span id="ANY_CLIENT"></span>

<span data-ttu-id="babc1-237"><span id="Any_Client"></span><span id="any_client"></span><span id="ANY_CLIENT"></span>**Любой клиент** (0)</span><span class="sxs-lookup"><span data-stu-id="babc1-237"><span id="Any_Client"></span><span id="any_client"></span><span id="ANY_CLIENT"></span>**Any Client** (0)</span></span>


</dt> <dd>

<span data-ttu-id="babc1-238">Любой клиент будет использоваться для повторного подключения.</span><span class="sxs-lookup"><span data-stu-id="babc1-238">Any client will be used to reconnect.</span></span>

</dd> <dt>

<span id="Previous_Client"></span><span id="previous_client"></span><span id="PREVIOUS_CLIENT"></span>

<span data-ttu-id="babc1-239"><span id="Previous_Client"></span><span id="previous_client"></span><span id="PREVIOUS_CLIENT"></span>**Предыдущий клиент** (1)</span><span class="sxs-lookup"><span data-stu-id="babc1-239"><span id="Previous_Client"></span><span id="previous_client"></span><span id="PREVIOUS_CLIENT"></span>**Previous Client** (1)</span></span>


</dt> <dd>

<span data-ttu-id="babc1-240">Предыдущий клиент, используемый в соединении, будет использоваться для повторного подключения.</span><span class="sxs-lookup"><span data-stu-id="babc1-240">The previous client used in a connection will be used to reconnect.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="babc1-241">**Состояние**</span><span class="sxs-lookup"><span data-stu-id="babc1-241">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="babc1-242">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="babc1-242">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="babc1-243">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="babc1-243">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="babc1-244">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span><span class="sxs-lookup"><span data-stu-id="babc1-244">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span></span>
</dt> </dl>

<span data-ttu-id="babc1-245">Текущее состояние объекта.</span><span class="sxs-lookup"><span data-stu-id="babc1-245">Current status of the object.</span></span> <span data-ttu-id="babc1-246">Можно определить различные операционные и неоперационные состояния.</span><span class="sxs-lookup"><span data-stu-id="babc1-246">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="babc1-247">Рабочие состояния включают: "ОК", "деградация" и "пред-ошибка" (элемент, например жесткий диск с поддержкой SMART, может работать правильно, но прогнозировать сбой в ближайшем будущем).</span><span class="sxs-lookup"><span data-stu-id="babc1-247">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="babc1-248">Неработающие состояния включают: "ошибка", "Запуск", "остановка" и "служба".</span><span class="sxs-lookup"><span data-stu-id="babc1-248">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="babc1-249">Последняя, «служба», может применяться во время зеркального копирования диска, перезагрузки списка разрешений пользователя или другой административной работы.</span><span class="sxs-lookup"><span data-stu-id="babc1-249">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="babc1-250">Не вся такая работа выполняется в интерактивном состоянии, но управляемый элемент не является ни "ОК", ни одним из других состояний.</span><span class="sxs-lookup"><span data-stu-id="babc1-250">Not all such work is on-line, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="babc1-251">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="babc1-251">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<dt>



 <span data-ttu-id="babc1-252">("ОК")</span><span class="sxs-lookup"><span data-stu-id="babc1-252">("OK")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="babc1-253">("Ошибка")</span><span class="sxs-lookup"><span data-stu-id="babc1-253">("Error")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="babc1-254">("Пониженное состояние")</span><span class="sxs-lookup"><span data-stu-id="babc1-254">("Degraded")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="babc1-255">("Неизвестно")</span><span class="sxs-lookup"><span data-stu-id="babc1-255">("Unknown")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="babc1-256">("Пред Fail")</span><span class="sxs-lookup"><span data-stu-id="babc1-256">("Pred Fail")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="babc1-257">("Запуск")</span><span class="sxs-lookup"><span data-stu-id="babc1-257">("Starting")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="babc1-258">("Остановка")</span><span class="sxs-lookup"><span data-stu-id="babc1-258">("Stopping")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="babc1-259">("Служба")</span><span class="sxs-lookup"><span data-stu-id="babc1-259">("Service")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="babc1-260">**терминалнаме**</span><span class="sxs-lookup"><span data-stu-id="babc1-260">**TerminalName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="babc1-261">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="babc1-261">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="babc1-262">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="babc1-262">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="babc1-263">Имя терминала.</span><span class="sxs-lookup"><span data-stu-id="babc1-263">The name of the terminal.</span></span>

<span data-ttu-id="babc1-264">Это свойство наследуется из [**Win32 \_ терминалсеттинг**](win32-terminalsetting.md).</span><span class="sxs-lookup"><span data-stu-id="babc1-264">This property is inherited from [**Win32\_TerminalSetting**](win32-terminalsetting.md).</span></span>

</dd> <dt>

<span data-ttu-id="babc1-265">**тимелимитполици**</span><span class="sxs-lookup"><span data-stu-id="babc1-265">**TimeLimitPolicy**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="babc1-266">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="babc1-266">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="babc1-267">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="babc1-267">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="babc1-268">Политика, используемая сервером для определения ограничений по времени для пользовательских сеансов.</span><span class="sxs-lookup"><span data-stu-id="babc1-268">The policy the server uses to determine time-limits for user sessions.</span></span>

<dt>

<span id="Per_User"></span><span id="per_user"></span><span id="PER_USER"></span>

<span data-ttu-id="babc1-269"><span id="Per_User"></span><span id="per_user"></span><span id="PER_USER"></span>**На пользователя** (0)</span><span class="sxs-lookup"><span data-stu-id="babc1-269"><span id="Per_User"></span><span id="per_user"></span><span id="PER_USER"></span>**Per User** (0)</span></span>


</dt> <dd>

<span data-ttu-id="babc1-270">Действуют параметры политики ограничения времени пользователя.</span><span class="sxs-lookup"><span data-stu-id="babc1-270">The user's time-limits policy settings are in effect.</span></span>

</dd> <dt>

<span id="Server_Override"></span><span id="server_override"></span><span id="SERVER_OVERRIDE"></span>

<span data-ttu-id="babc1-271"><span id="Server_Override"></span><span id="server_override"></span><span id="SERVER_OVERRIDE"></span>**Переопределение сервера** (1)</span><span class="sxs-lookup"><span data-stu-id="babc1-271"><span id="Server_Override"></span><span id="server_override"></span><span id="SERVER_OVERRIDE"></span>**Server Override** (1)</span></span>


</dt> <dd>

<span data-ttu-id="babc1-272">Параметры политики ограничения времени пользователя переопределяются сервером.</span><span class="sxs-lookup"><span data-stu-id="babc1-272">The user's time-limits policy settings are overridden by the server.</span></span>

</dd> </dl>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="babc1-273">Комментарии</span><span class="sxs-lookup"><span data-stu-id="babc1-273">Remarks</span></span>

<span data-ttu-id="babc1-274">Имейте в виду, что Винстатионс, связанный с сеансом консоли, не может получить доступ к методам и свойствам этого класса.</span><span class="sxs-lookup"><span data-stu-id="babc1-274">Be aware that Winstations associated with the console session cannot access the methods and properties of this class.</span></span> <span data-ttu-id="babc1-275">Если предпринимается попытка сделать это, указав "Console" в качестве значения свойства Терминалнаме, методы этого объекта будут возвращать **WBEM \_ E \_ не \_ поддерживаются**.</span><span class="sxs-lookup"><span data-stu-id="babc1-275">If an attempt is made to do so by specifying "Console" as the value of the TerminalName property, methods of this object will return **WBEM\_E\_NOT\_SUPPORTED**.</span></span> <span data-ttu-id="babc1-276">Этот код ошибки также будет возвращен, если станция Windows пытается вызвать методы этого объекта для добавления или изменения свойств безопасности учетных записей LocalSystem, LocalService или NetworkService.</span><span class="sxs-lookup"><span data-stu-id="babc1-276">This error code will also be returned if a window station attempts to call methods of this object for the purpose of adding or modifying the security properties of the LocalSystem, LocalService, or NetworkService accounts.</span></span>

<span data-ttu-id="babc1-277">Чтобы подключиться к \\ \\ пространству имен root cimv2 терминалсервицес, уровень проверки подлинности должен включать в себя конфиденциальность пакетов.</span><span class="sxs-lookup"><span data-stu-id="babc1-277">To connect to the "root\\CIMV2\\TerminalServices" namespace, the authentication level must include packet privacy.</span></span> <span data-ttu-id="babc1-278">Для вызовов C/C++ это будет уровень проверки подлинности **AUTHN на \_ \_ \_ уровне \_ \_ безопасности RPC C уровня "PKT**".</span><span class="sxs-lookup"><span data-stu-id="babc1-278">For C/C++ calls, this would be an authentication level of **RPC\_C\_AUTHN\_LEVEL\_PKT\_PRIVACY**.</span></span> <span data-ttu-id="babc1-279">Для вызовов Visual Basic и сценариев это будет уровень проверки подлинности **вбемаусентикатионлевелпктприваци** или "пктприваци" со значением 6.</span><span class="sxs-lookup"><span data-stu-id="babc1-279">For Visual Basic and scripting calls, this would be an authentication level of **WbemAuthenticationLevelPktPrivacy** or "pktPrivacy", with a value of 6.</span></span> <span data-ttu-id="babc1-280">В следующем примере Visual Basic Scripting Edition (VBScript) показано, как подключиться к удаленному компьютеру с использованием конфиденциальности пакетов.</span><span class="sxs-lookup"><span data-stu-id="babc1-280">The following Visual Basic Scripting Edition (VBScript) example shows how to connect to a remote computer with packet privacy.</span></span>


```VB
strComputer = "RemoteServer1" 
Set objServices = GetObject( _
    "winmgmts:{authenticationLevel=pktPrivacy}!Root/CIMv2/TerminalServices")
```



<span data-ttu-id="babc1-281">Файлы MOF-файл (MOF) содержат определения для классов инструментарий управления Windows (WMI) (WMI).</span><span class="sxs-lookup"><span data-stu-id="babc1-281">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="babc1-282">MOF-файлы не устанавливаются в составе пакета средств разработки программного обеспечения Microsoft Windows (SDK).</span><span class="sxs-lookup"><span data-stu-id="babc1-282">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="babc1-283">Они устанавливаются на сервере при добавлении связанной роли с помощью диспетчер сервера.</span><span class="sxs-lookup"><span data-stu-id="babc1-283">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="babc1-284">Дополнительные сведения о файлах MOF см. в разделе [MOF-файл (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="babc1-284">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="babc1-285">Требования</span><span class="sxs-lookup"><span data-stu-id="babc1-285">Requirements</span></span>



| <span data-ttu-id="babc1-286">Требование</span><span class="sxs-lookup"><span data-stu-id="babc1-286">Requirement</span></span> | <span data-ttu-id="babc1-287">Значение</span><span class="sxs-lookup"><span data-stu-id="babc1-287">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="babc1-288">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="babc1-288">Minimum supported client</span></span><br/> | <span data-ttu-id="babc1-289">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="babc1-289">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="babc1-290">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="babc1-290">Minimum supported server</span></span><br/> | <span data-ttu-id="babc1-291">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="babc1-291">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="babc1-292">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="babc1-292">Namespace</span></span><br/>                | <span data-ttu-id="babc1-293">Корневой \\ CIMv2 \\ терминалсервицес</span><span class="sxs-lookup"><span data-stu-id="babc1-293">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="babc1-294">MOF</span><span class="sxs-lookup"><span data-stu-id="babc1-294">MOF</span></span><br/>                      | <dl> <span data-ttu-id="babc1-295"><dt>Тскфгвми. mof</dt></span><span class="sxs-lookup"><span data-stu-id="babc1-295"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="babc1-296">DLL</span><span class="sxs-lookup"><span data-stu-id="babc1-296">DLL</span></span><br/>                      | <dl> <span data-ttu-id="babc1-297"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="babc1-297"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="babc1-298">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="babc1-298">See also</span></span>

<dl> <dt>

[<span data-ttu-id="babc1-299">**\_Терминалсеттинг Win32**</span><span class="sxs-lookup"><span data-stu-id="babc1-299">**Win32\_TerminalSetting**</span></span>](win32-terminalsetting.md)
</dt> <dt>

[<span data-ttu-id="babc1-300">**\_Параметр CIM**</span><span class="sxs-lookup"><span data-stu-id="babc1-300">**CIM\_Setting**</span></span>](/windows/desktop/CIMWin32Prov/cim-setting)
</dt> </dl>

 

