---
description: '&Win32 \_ стартупкомманд \# 8194; Класс WMI представляет команду, которая запускается автоматически при входе пользователя в систему компьютера.'
ms.assetid: 7184ade8-fcc9-47b3-af04-8054b2fca937
ms.tgt_platform: multiple
title: Класс Win32_StartupCommand
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_StartupCommand
- Win32_StartupCommand.Caption
- Win32_StartupCommand.Description
- Win32_StartupCommand.SettingID
- Win32_StartupCommand.Command
- Win32_StartupCommand.Location
- Win32_StartupCommand.Name
- Win32_StartupCommand.User
- Win32_StartupCommand.UserSID
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 1c38ec84b9df38687a32211f3294258fd58efb96
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103896349"
---
# <a name="win32_startupcommand-class"></a><span data-ttu-id="7ca86-103">\_Класс Win32 стартупкомманд</span><span class="sxs-lookup"><span data-stu-id="7ca86-103">Win32\_StartupCommand class</span></span>

<span data-ttu-id="7ca86-104"> [Класс WMI](../wmisdk/retrieving-a-class.md) *\*\_ стартупкомманд для Win32** представляет команду, которая выполняется автоматически при входе пользователя в систему компьютера.</span><span class="sxs-lookup"><span data-stu-id="7ca86-104">The **Win32\_StartupCommand** [WMI class](../wmisdk/retrieving-a-class.md) represents a command that runs automatically when a user logs onto the computer system.</span></span>

<span data-ttu-id="7ca86-105">Следующий пример синтаксиса — упрощенный MOF-код, который включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="7ca86-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="7ca86-106">Свойства и методы имеют алфавитный порядок, а не порядок MOF.</span><span class="sxs-lookup"><span data-stu-id="7ca86-106">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="7ca86-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="7ca86-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), Privileges("SeRestorePrivilege"), UUID("{8502C50A-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_StartupCommand : CIM_Setting
{
  string Caption;
  string Description;
  string SettingID;
  string Command;
  string Location;
  string Name;
  string User;
  string UserSID;
};
```

## <a name="members"></a><span data-ttu-id="7ca86-108">Члены</span><span class="sxs-lookup"><span data-stu-id="7ca86-108">Members</span></span>

<span data-ttu-id="7ca86-109">Класс **Win32 \_ стартупкомманд** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="7ca86-109">The **Win32\_StartupCommand** class has these types of members:</span></span>

-   [<span data-ttu-id="7ca86-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="7ca86-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="7ca86-111">Свойства</span><span class="sxs-lookup"><span data-stu-id="7ca86-111">Properties</span></span>

<span data-ttu-id="7ca86-112">Класс **Win32 \_ стартупкомманд** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="7ca86-112">The **Win32\_StartupCommand** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="7ca86-113">**Заголовок**</span><span class="sxs-lookup"><span data-stu-id="7ca86-113">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ca86-114">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="7ca86-114">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7ca86-115">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="7ca86-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7ca86-116">Квалификаторы: [**maxlen**](../wmisdk/standard-qualifiers.md) (64)</span><span class="sxs-lookup"><span data-stu-id="7ca86-116">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64)</span></span>
</dt> </dl>

<span data-ttu-id="7ca86-117">Краткое текстовое описание текущего объекта.</span><span class="sxs-lookup"><span data-stu-id="7ca86-117">Short textual description of the current object.</span></span>

<span data-ttu-id="7ca86-118">Это свойство наследуется [**от \_ параметра CIM**](cim-setting.md).</span><span class="sxs-lookup"><span data-stu-id="7ca86-118">This property is inherited from [**CIM\_Setting**](cim-setting.md).</span></span>

</dd> <dt>

<span data-ttu-id="7ca86-119">**Команда**</span><span class="sxs-lookup"><span data-stu-id="7ca86-119">**Command**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ca86-120">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="7ca86-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7ca86-121">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="7ca86-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7ca86-122">Квалификаторы: [**Key**](../wmisdk/key-qualifier.md), [**Маппингстрингс**](../wmisdk/standard-qualifiers.md) («Win32Registry \| Software \\ \\ Microsoft \\ \\ Windows \\ \\ CurrentVersion \\ \\ Run»)</span><span class="sxs-lookup"><span data-stu-id="7ca86-122">Qualifiers: [**key**](../wmisdk/key-qualifier.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SOFTWARE\\\\Microsoft\\\\Windows\\\\CurrentVersion\\\\Run")</span></span>
</dt> </dl>

<span data-ttu-id="7ca86-123">Команда, выполняемая командой Startup.</span><span class="sxs-lookup"><span data-stu-id="7ca86-123">Command run by the startup command.</span></span>

<span data-ttu-id="7ca86-124">Инструментарий WMI получает эти данные из раздела реестра</span><span class="sxs-lookup"><span data-stu-id="7ca86-124">WMI obtains this data from the registry key</span></span>

<span data-ttu-id="7ca86-125">**HKey \_ По на локальном \_ компьютере** \\  \\  \\ Запуск Microsoft **Windows** \\ **CurrentVersion** \\ </span><span class="sxs-lookup"><span data-stu-id="7ca86-125">**HKEY\_LOCAL\_MACHINE**\\**SOFTWARE**\\**Microsoft**\\**Windows**\\**CurrentVersion**\\**Run**</span></span>

<span data-ttu-id="7ca86-126">Пример: "C: \\ Windows \\notepad.exe myfile.txt"</span><span class="sxs-lookup"><span data-stu-id="7ca86-126">Example: "C:\\Windows\\notepad.exe myfile.txt"</span></span>

</dd> <dt>

<span data-ttu-id="7ca86-127">**Описание**</span><span class="sxs-lookup"><span data-stu-id="7ca86-127">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ca86-128">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="7ca86-128">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7ca86-129">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="7ca86-129">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7ca86-130">Текстовое описание текущего объекта.</span><span class="sxs-lookup"><span data-stu-id="7ca86-130">Textual description of the current object.</span></span>

<span data-ttu-id="7ca86-131">Это свойство наследуется [**от \_ параметра CIM**](cim-setting.md).</span><span class="sxs-lookup"><span data-stu-id="7ca86-131">This property is inherited from [**CIM\_Setting**](cim-setting.md).</span></span>

</dd> <dt>

<span data-ttu-id="7ca86-132">**Расположение**</span><span class="sxs-lookup"><span data-stu-id="7ca86-132">**Location**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ca86-133">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="7ca86-133">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7ca86-134">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="7ca86-134">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7ca86-135">Квалификаторы: [**Key**](../wmisdk/key-qualifier.md), [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| \\ \\ Software \\ \\ Microsoft \\ \\ Windows \\ \\ CURRENTVERSION \\ \\ Windows")</span><span class="sxs-lookup"><span data-stu-id="7ca86-135">Qualifiers: [**key**](../wmisdk/key-qualifier.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|\\\\SOFTWARE\\\\MICROSOFT\\\\WINDOWS\\\\CURRENTVERSION\\\\Windows")</span></span>
</dt> </dl>

<span data-ttu-id="7ca86-136">Путь, по которому команда запуска находится на дисковой файловой системе.</span><span class="sxs-lookup"><span data-stu-id="7ca86-136">Path where the startup command resides on the disk file system.</span></span>

<span data-ttu-id="7ca86-137">Например: HKLM \\ Software \\ Microsoft \\ Windows \\ CurrentVersion \\ Run</span><span class="sxs-lookup"><span data-stu-id="7ca86-137">For example: HKLM\\SOFTWARE\\Microsoft\\Windows\\CurrentVersion\\Run</span></span>

<dt>

<span id="Startup"></span><span id="startup"></span><span id="STARTUP"></span>

<span data-ttu-id="7ca86-138">**Запуск** ("Запуск")</span><span class="sxs-lookup"><span data-stu-id="7ca86-138">**Startup** ("Startup")</span></span>


</dt> <dd></dd> <dt>

<span id="Common_Startup"></span><span id="common_startup"></span><span id="COMMON_STARTUP"></span>

<span data-ttu-id="7ca86-139">**Общий запуск** (обычный запуск)</span><span class="sxs-lookup"><span data-stu-id="7ca86-139">**Common Startup** ("Common Startup")</span></span>


</dt> <dd></dd> <dt>

<span id="HKLM__SOFTWARE__Microsoft__Windows__CurrentVersion__Run"></span><span id="hklm__software__microsoft__windows__currentversion__run"></span><span id="HKLM__SOFTWARE__MICROSOFT__WINDOWS__CURRENTVERSION__RUN"></span>

<span data-ttu-id="7ca86-140">**\\ HKLM \\ Программное обеспечение \\ \\ Microsoft \\ \\ Windows \\ \\ CurrentVersion \\ \\ Run** («HKLM \\ \\ Software \\ \\ Microsoft \\ \\ Windows \\ \\ CurrentVersion \\ \\ Run»)</span><span class="sxs-lookup"><span data-stu-id="7ca86-140">**HKLM\\\\SOFTWARE\\\\Microsoft\\\\Windows\\\\CurrentVersion\\\\Run** ("HKLM\\\\SOFTWARE\\\\Microsoft\\\\Windows\\\\CurrentVersion\\\\Run")</span></span>


</dt> <dd></dd> <dt>

<span id="HKLM__SOFTWARE__Microsoft__Windows__CurrentVersion__RunServices"></span><span id="hklm__software__microsoft__windows__currentversion__runservices"></span><span id="HKLM__SOFTWARE__MICROSOFT__WINDOWS__CURRENTVERSION__RUNSERVICES"></span>

<span data-ttu-id="7ca86-141">**\\ HKLM \\ Программное обеспечение \\ \\ Microsoft \\ \\ Windows \\ \\ CurrentVersion \\ \\ рунсервицес** ("HKLM \\ \\ Software \\ \\ Microsoft \\ \\ Windows \\ \\ CurrentVersion \\ \\ рунсервицес")</span><span class="sxs-lookup"><span data-stu-id="7ca86-141">**HKLM\\\\SOFTWARE\\\\Microsoft\\\\Windows\\\\CurrentVersion\\\\RunServices** ("HKLM\\\\SOFTWARE\\\\Microsoft\\\\Windows\\\\CurrentVersion\\\\RunServices")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="7ca86-142">**Name**</span><span class="sxs-lookup"><span data-stu-id="7ca86-142">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ca86-143">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="7ca86-143">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7ca86-144">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="7ca86-144">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7ca86-145">Квалификаторы: [**Key**](../wmisdk/key-qualifier.md), [**Маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32API \| File Structures \| [**Win32 \_ Find \_ Data**](/windows/win32/api/minwinbase/ns-minwinbase-win32_find_dataa) \| кфиленаме")</span><span class="sxs-lookup"><span data-stu-id="7ca86-145">Qualifiers: [**key**](../wmisdk/key-qualifier.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|File Structures\|[**WIN32\_FIND\_DATA**](/windows/win32/api/minwinbase/ns-minwinbase-win32_find_dataa)\|cFileName")</span></span>
</dt> </dl>

<span data-ttu-id="7ca86-146">Имя файла команды запуска.</span><span class="sxs-lookup"><span data-stu-id="7ca86-146">File name of the startup command.</span></span>

<span data-ttu-id="7ca86-147">Пример: "Финдфаст"</span><span class="sxs-lookup"><span data-stu-id="7ca86-147">Example: "FindFast"</span></span>

</dd> <dt>

<span data-ttu-id="7ca86-148">**SettingID**</span><span class="sxs-lookup"><span data-stu-id="7ca86-148">**SettingID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ca86-149">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="7ca86-149">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7ca86-150">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="7ca86-150">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7ca86-151">Квалификаторы: [**maxlen**](../wmisdk/standard-qualifiers.md) (256)</span><span class="sxs-lookup"><span data-stu-id="7ca86-151">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)</span></span>
</dt> </dl>

<span data-ttu-id="7ca86-152">Идентификатор, по которому известен текущий объект.</span><span class="sxs-lookup"><span data-stu-id="7ca86-152">Identifier by which the current object is known.</span></span>

<span data-ttu-id="7ca86-153">Это свойство наследуется [**от \_ параметра CIM**](cim-setting.md).</span><span class="sxs-lookup"><span data-stu-id="7ca86-153">This property is inherited from [**CIM\_Setting**](cim-setting.md).</span></span>

</dd> <dt>

<span data-ttu-id="7ca86-154">**Пользователь**</span><span class="sxs-lookup"><span data-stu-id="7ca86-154">**User**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ca86-155">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="7ca86-155">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7ca86-156">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="7ca86-156">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7ca86-157">Квалификаторы: [**Key**](../wmisdk/key-qualifier.md), [**Маппингстрингс**](../wmisdk/standard-qualifiers.md) ("WMI")</span><span class="sxs-lookup"><span data-stu-id="7ca86-157">Qualifiers: [**key**](../wmisdk/key-qualifier.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="7ca86-158">Имя пользователя, для которого будет запускаться эта команда запуска.</span><span class="sxs-lookup"><span data-stu-id="7ca86-158">User name for whom this startup command will run.</span></span>

<span data-ttu-id="7ca86-159">Пример: "mydomain \\ myname"</span><span class="sxs-lookup"><span data-stu-id="7ca86-159">Example: "mydomain\\myname"</span></span>

</dd> <dt>

<span data-ttu-id="7ca86-160">**UserSID**</span><span class="sxs-lookup"><span data-stu-id="7ca86-160">**UserSID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ca86-161">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="7ca86-161">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7ca86-162">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="7ca86-162">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7ca86-163">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("WMI")</span><span class="sxs-lookup"><span data-stu-id="7ca86-163">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="7ca86-164">Свойство «код свойства» указывает идентификатор безопасности пользователя, для которого будет запускаться эта команда запуска.</span><span class="sxs-lookup"><span data-stu-id="7ca86-164">The UserSID property indicates the SID of the user for whom this startup command will run.</span></span> <span data-ttu-id="7ca86-165">Это свойство пользователя может быть пустым, но если имя пользователя не удается разрешить (например, в случае удаленного пользователя), оно по-прежнему имеет значение.</span><span class="sxs-lookup"><span data-stu-id="7ca86-165">That User property may be empty but UserSID still has a value if the user name can't be resolved (like in the case of a deleted user).</span></span> <span data-ttu-id="7ca86-166">Свойство полезно для различения команд, связанных с двумя разными пользователями с неразрешенными именами.</span><span class="sxs-lookup"><span data-stu-id="7ca86-166">The property is helpful to distinguish between commands associated w/ two different users with unresolved names.</span></span> <span data-ttu-id="7ca86-167">Может иметь значение NULL, если команда связана с элементами, которые не идентифицируют пользователя, как, например, для всех пользователей.</span><span class="sxs-lookup"><span data-stu-id="7ca86-167">It may be NULL when the command is associated with items not actually identifying a user like All Users.</span></span>

<span data-ttu-id="7ca86-168">Пример: S-1-5-21-1579938362-1064596589-3161144252-1006</span><span class="sxs-lookup"><span data-stu-id="7ca86-168">Example:S-1-5-21-1579938362-1064596589-3161144252-1006</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="7ca86-169">Комментарии</span><span class="sxs-lookup"><span data-stu-id="7ca86-169">Remarks</span></span>

<span data-ttu-id="7ca86-170">Класс **Win32 \_ стартупкомманд** является производным от [**\_ параметра CIM**](cim-setting.md).</span><span class="sxs-lookup"><span data-stu-id="7ca86-170">The **Win32\_StartupCommand** class is derived from [**CIM\_Setting**](cim-setting.md).</span></span>

<span data-ttu-id="7ca86-171">Запуск компьютера не заканчивается после загрузки операционной системы.</span><span class="sxs-lookup"><span data-stu-id="7ca86-171">Computer startup does not end after the operating system has been loaded.</span></span> <span data-ttu-id="7ca86-172">Вместо этого можно настроить операционную систему Windows таким образом, чтобы команды запуска запускались при каждом запуске Windows.</span><span class="sxs-lookup"><span data-stu-id="7ca86-172">Instead, the Windows operating system can be configured so that startup commands are run each time Windows starts.</span></span> <span data-ttu-id="7ca86-173">Команды запуска хранятся в реестре или в составе профиля пользователя и используются для автоматического запуска определенных сценариев или приложений при каждой загрузке Windows.</span><span class="sxs-lookup"><span data-stu-id="7ca86-173">Startup commands are stored in the registry or as part of the user profile and are used to automatically start specified scripts or applications each time Windows is loaded.</span></span>

<span data-ttu-id="7ca86-174">В большинстве случаев программы автозапуска полезны. они гарантируют, что определенные приложения, такие как антивирусные программы, автоматически запускаются и запускаются при каждой загрузке Windows.</span><span class="sxs-lookup"><span data-stu-id="7ca86-174">In most cases, autostart programs are useful; they ensure that certain applications, such as antivirus tools, are automatically started and run each time Windows is loaded.</span></span> <span data-ttu-id="7ca86-175">Однако программы автозапуска также могут отвечать за такие проблемы, как:</span><span class="sxs-lookup"><span data-stu-id="7ca86-175">However, autostart programs also can be responsible for problems such as:</span></span>

-   <span data-ttu-id="7ca86-176">Компьютеры, которые занимают много времени на запуск.</span><span class="sxs-lookup"><span data-stu-id="7ca86-176">Computers that take an exceptionally long time to start.</span></span> <span data-ttu-id="7ca86-177">Это может быть результатом большого количества приложений, которые должны запускаться при каждом запуске Windows.</span><span class="sxs-lookup"><span data-stu-id="7ca86-177">This might be the result of a large number of applications that must be started each time Windows starts.</span></span>
-   <span data-ttu-id="7ca86-178">Приложения, представленные на панели задач или в диспетчере задач, даже если пользователь не запустил их.</span><span class="sxs-lookup"><span data-stu-id="7ca86-178">Applications that are represented in the Taskbar or in Task Manager, even though the user did not start them.</span></span> <span data-ttu-id="7ca86-179">Хотя эти приложения не обязательно вызывают проблемы, они могут привести к вызовам службы поддержки от пользователей, которые путают с тем, откуда поступают эти программы и почему они работают.</span><span class="sxs-lookup"><span data-stu-id="7ca86-179">Although these applications do not necessarily cause problems, they can result in help desk calls from users who are confused as to where these programs came from and why they are running.</span></span>
-   <span data-ttu-id="7ca86-180">Компьютеры, на которых возникают проблемы, даже если они находятся в состоянии простоя.</span><span class="sxs-lookup"><span data-stu-id="7ca86-180">Computers experiencing problems even when they seem idle.</span></span> <span data-ttu-id="7ca86-181">Эти проблемы часто отслеживаются с командами запуска, которые выполняются, когда никто не знает, что они работают.</span><span class="sxs-lookup"><span data-stu-id="7ca86-181">These problems are often traced to startup commands that are running when no one is aware that they are running.</span></span>

<span data-ttu-id="7ca86-182">Определение приложений и сценариев, автоматически запускаемых при запуске, является важной, но сложной задачей администрирования, так как команды запуска могут храниться во многих разных местах:</span><span class="sxs-lookup"><span data-stu-id="7ca86-182">Identifying the applications and scripts that automatically run at startup is an important but difficult administrative task, because startup commands can be stored in many different locations:</span></span>

-   <span data-ttu-id="7ca86-183">HKLM \\ Software \\ Microsoft \\ Windows \\ CurrentVersion \\ Run</span><span class="sxs-lookup"><span data-stu-id="7ca86-183">HKLM\\Software\\Microsoft\\Windows\\CurrentVersion\\Run</span></span>
-   <span data-ttu-id="7ca86-184">HKLM \\ Software \\ Microsoft \\ Windows \\ CurrentVersion \\ RunOnce</span><span class="sxs-lookup"><span data-stu-id="7ca86-184">HKLM\\Software\\Microsoft\\Windows\\CurrentVersion\\RunOnce</span></span>
-   <span data-ttu-id="7ca86-185">Раздел HKCU \\ Software \\ Microsoft \\ Windows \\ CurrentVersion \\ Run</span><span class="sxs-lookup"><span data-stu-id="7ca86-185">HKCU\\Software\\Microsoft\\Windows\\CurrentVersion\\Run</span></span>
-   <span data-ttu-id="7ca86-186">HKCU \\ программное обеспечение \\ Microsoft \\ Windows \\ CurrentVersion \\ RunOnce</span><span class="sxs-lookup"><span data-stu-id="7ca86-186">HKCU\\Software\\Microsoft\\Windows\\CurrentVersion\\RunOnce</span></span>
-   <span data-ttu-id="7ca86-187">HKU \\ ProgID \\ программное обеспечение \\ Microsoft \\ Windows \\ CurrentVersion \\ Run</span><span class="sxs-lookup"><span data-stu-id="7ca86-187">HKU\\ProgID\\Software\\Microsoft\\Windows\\CurrentVersion\\Run</span></span>
-   <span data-ttu-id="7ca86-188">systemdrive \\ Documents and Settings \\ All Users \\ Start Program Menus \\ \\ Startup</span><span class="sxs-lookup"><span data-stu-id="7ca86-188">systemdrive\\Documents and Settings\\All Users\\Start Menu\\Programs\\Startup</span></span>
-   <span data-ttu-id="7ca86-189">\\загрузить документы и параметры \\ имя пользователя в \\ меню "Пуск" запуск \\ программ \\</span><span class="sxs-lookup"><span data-stu-id="7ca86-189">systemdrive\\Documents and Settings\\username\\Start Menu\\Programs\\Startup</span></span>

<span data-ttu-id="7ca86-190">Класс WMI Win32 стартупкомманд можно использовать \_ для перечисления программ автозапуска независимо от того, где хранится информация.</span><span class="sxs-lookup"><span data-stu-id="7ca86-190">You can use the WMI Win32\_StartupCommand class to enumerate autostart programs regardless of where the information is stored.</span></span>

<span data-ttu-id="7ca86-191">Вызывающий процесс, использующий этот класс, должен иметь привилегию **SE \_ reside \_ Name** на компьютере, где размещается реестр.</span><span class="sxs-lookup"><span data-stu-id="7ca86-191">The calling process that uses this class must have the **SE\_RESTORE\_NAME** privilege on the computer in which the registry resides.</span></span> <span data-ttu-id="7ca86-192">Например, если перечислить этот класс на локальном компьютере, учетная запись, под которой выполняется приложение, должна иметь эту привилегию.</span><span class="sxs-lookup"><span data-stu-id="7ca86-192">For example, if you enumerate this class on the local computer, the account under which your application runs must have this privilege.</span></span> <span data-ttu-id="7ca86-193">Дополнительные сведения см. в разделе [выполнение привилегированных операций](../wmisdk/executing-privileged-operations.md).</span><span class="sxs-lookup"><span data-stu-id="7ca86-193">For more information, see [Executing Privileged Operations](../wmisdk/executing-privileged-operations.md).</span></span>

<span data-ttu-id="7ca86-194">Вы можете изменить значения реестра, в которых **Win32 \_ стартупкомманд** получает данные, вызывая методы [поставщика системного реестра](/previous-versions/windows/desktop/regprov/system-registry-provider) WMI в скрипте или в C++.</span><span class="sxs-lookup"><span data-stu-id="7ca86-194">You can change the registry values where **Win32\_StartupCommand** obtains data by calling the WMI [System Registry Provider](/previous-versions/windows/desktop/regprov/system-registry-provider) methods in script or in C++.</span></span> <span data-ttu-id="7ca86-195">Дополнительные сведения см. [в разделе изменение системного реестра](../wmisdk/modifying-the-system-registry.md).</span><span class="sxs-lookup"><span data-stu-id="7ca86-195">For more information, see [Modifying the System Registry](../wmisdk/modifying-the-system-registry.md).</span></span>

## <a name="examples"></a><span data-ttu-id="7ca86-196">Примеры</span><span class="sxs-lookup"><span data-stu-id="7ca86-196">Examples</span></span>

<span data-ttu-id="7ca86-197">Следующая команда VBScript перечисляет команды запуска на компьютере.</span><span class="sxs-lookup"><span data-stu-id="7ca86-197">The following VBScript enumerates the startup commands on a computer.</span></span>


```VB
strComputer = "."
Set objWMIService = GetObject("winmgmts:" _
 & "{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")
Set colStartupCommands = objWMIService.ExecQuery _
 ("SELECT * FROM Win32_StartupCommand")
For Each objStartupCommand in colStartupCommands
 Wscript.Echo "Command: " & objStartupCommand.Command
 Wscript.Echo "Description: " & objStartupCommand.Description
 Wscript.Echo "Location: " & objStartupCommand.Location
 Wscript.Echo "Name: " & objStartupCommand.Name
 Wscript.Echo "SettingID: " & objStartupCommand.SettingID
 Wscript.Echo "User: " & objStartupCommand.User
Next
```



## <a name="requirements"></a><span data-ttu-id="7ca86-198">Требования</span><span class="sxs-lookup"><span data-stu-id="7ca86-198">Requirements</span></span>



| <span data-ttu-id="7ca86-199">Требование</span><span class="sxs-lookup"><span data-stu-id="7ca86-199">Requirement</span></span> | <span data-ttu-id="7ca86-200">Значение</span><span class="sxs-lookup"><span data-stu-id="7ca86-200">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="7ca86-201">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="7ca86-201">Minimum supported client</span></span><br/> | <span data-ttu-id="7ca86-202">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="7ca86-202">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="7ca86-203">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="7ca86-203">Minimum supported server</span></span><br/> | <span data-ttu-id="7ca86-204">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="7ca86-204">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="7ca86-205">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="7ca86-205">Namespace</span></span><br/>                | <span data-ttu-id="7ca86-206">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="7ca86-206">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="7ca86-207">MOF</span><span class="sxs-lookup"><span data-stu-id="7ca86-207">MOF</span></span><br/>                      | <dl> <span data-ttu-id="7ca86-208"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="7ca86-208"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="7ca86-209">DLL</span><span class="sxs-lookup"><span data-stu-id="7ca86-209">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7ca86-210"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7ca86-210"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7ca86-211">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="7ca86-211">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7ca86-212">**\_Параметр CIM**</span><span class="sxs-lookup"><span data-stu-id="7ca86-212">**CIM\_Setting**</span></span>](cim-setting.md)
</dt> <dt>

[<span data-ttu-id="7ca86-213">Классы операционной системы</span><span class="sxs-lookup"><span data-stu-id="7ca86-213">Operating System Classes</span></span>](./operating-system-classes.md)
</dt> </dl>

 

 
