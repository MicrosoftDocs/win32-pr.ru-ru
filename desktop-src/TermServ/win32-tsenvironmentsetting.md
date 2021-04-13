---
title: Класс Win32_TSEnvironmentSetting
description: Определяет параметры конфигурации для \_ класса терминала Win32, включая политику начальной программы.
ms.assetid: 2d310a1e-a1bd-4ccb-965e-8389aaa2e4c1
ms.tgt_platform: multiple
keywords:
- Класс Win32_TSEnvironmentSetting службы удаленных рабочих столов
- Службы удаленных рабочих столов класса Win32_TSEnvironmentSetting, описание
topic_type:
- apiref
api_name:
- Win32_TSEnvironmentSetting
- Win32_TSEnvironmentSetting.Caption
- Win32_TSEnvironmentSetting.Description
- Win32_TSEnvironmentSetting.InstallDate
- Win32_TSEnvironmentSetting.Name
- Win32_TSEnvironmentSetting.Status
- Win32_TSEnvironmentSetting.TerminalName
- Win32_TSEnvironmentSetting.ClientWallPaper
- Win32_TSEnvironmentSetting.InitialProgramPath
- Win32_TSEnvironmentSetting.InitialProgramPolicy
- Win32_TSEnvironmentSetting.PolicySourceClientWallPaper
- Win32_TSEnvironmentSetting.PolicySourceInitialProgramPath
- Win32_TSEnvironmentSetting.PolicySourceStartIn
- Win32_TSEnvironmentSetting.Startin
api_location:
- TSCfgWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0689536385644ae3ef95d106e50ab198e5a57f93
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104535201"
---
# <a name="win32_tsenvironmentsetting-class"></a><span data-ttu-id="0e239-105">\_Класс Win32 тсенвиронментсеттинг</span><span class="sxs-lookup"><span data-stu-id="0e239-105">Win32\_TSEnvironmentSetting class</span></span>

<span data-ttu-id="0e239-106">Класс **WMI \_ Тсенвиронментсеттинг для Win32** определяет параметры конфигурации для класса [**\_ терминала Win32**](win32-terminal.md) , включая политику начальной программы.</span><span class="sxs-lookup"><span data-stu-id="0e239-106">The **Win32\_TSEnvironmentSetting** WMI class defines the configuration settings for the [**Win32\_Terminal**](win32-terminal.md) class including initial program policy.</span></span>

<span data-ttu-id="0e239-107">Следующий синтаксис упрощен из MOF-кода и включает все определенные и унаследованные свойства в алфавитном порядке.</span><span class="sxs-lookup"><span data-stu-id="0e239-107">The following syntax is simplified from MOF code and includes all defined and inherited properties, in alphabetical order.</span></span> <span data-ttu-id="0e239-108">Справочные сведения о методах см. в таблице методов далее в этом разделе.</span><span class="sxs-lookup"><span data-stu-id="0e239-108">For reference information on methods, see the table of methods later in this topic.</span></span>

## <a name="syntax"></a><span data-ttu-id="0e239-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="0e239-109">Syntax</span></span>

``` syntax
[dynamic, provider("Win32_WIN32_TSENVIRONMENTSETTING_Prov"), ClassContext("local|hkey_local_machine\\SYSTEM\\CurrentControlSet\\Control\\TerminalServer\\WinStations"), AMENDMENT]
class Win32_TSEnvironmentSetting : Win32_TerminalSetting
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
  string   TerminalName;
  uint32   ClientWallPaper;
  string   InitialProgramPath;
  uint32   InitialProgramPolicy;
  uint32   PolicySourceClientWallPaper;
  uint32   PolicySourceInitialProgramPath;
  uint32   PolicySourceStartIn;
  string   Startin;
};
```

## <a name="members"></a><span data-ttu-id="0e239-110">Члены</span><span class="sxs-lookup"><span data-stu-id="0e239-110">Members</span></span>

<span data-ttu-id="0e239-111">Класс **Win32 \_ тсенвиронментсеттинг** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="0e239-111">The **Win32\_TSEnvironmentSetting** class has these types of members:</span></span>

-   [<span data-ttu-id="0e239-112">Методы</span><span class="sxs-lookup"><span data-stu-id="0e239-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="0e239-113">Свойства</span><span class="sxs-lookup"><span data-stu-id="0e239-113">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="0e239-114">Методы</span><span class="sxs-lookup"><span data-stu-id="0e239-114">Methods</span></span>

<span data-ttu-id="0e239-115">Класс **Win32 \_ тсенвиронментсеттинг** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="0e239-115">The **Win32\_TSEnvironmentSetting** class has these methods.</span></span>



| <span data-ttu-id="0e239-116">Метод</span><span class="sxs-lookup"><span data-stu-id="0e239-116">Method</span></span>                                                                      | <span data-ttu-id="0e239-117">Описание</span><span class="sxs-lookup"><span data-stu-id="0e239-117">Description</span></span>                                                            |
|:----------------------------------------------------------------------------|:-----------------------------------------------------------------------|
| [<span data-ttu-id="0e239-118">**инитиалпрограм**</span><span class="sxs-lookup"><span data-stu-id="0e239-118">**InitialProgram**</span></span>](win32-tsenvironmentsetting-initialprogram.md)         | <span data-ttu-id="0e239-119">Задает свойства программы запуска, включенные в этот класс.</span><span class="sxs-lookup"><span data-stu-id="0e239-119">Sets the startup program properties included in this class.</span></span><br/> |
| [<span data-ttu-id="0e239-120">**сетклиентваллпапер**</span><span class="sxs-lookup"><span data-stu-id="0e239-120">**SetClientWallPaper**</span></span>](win32-tsenvironmentsetting-setclientwallpaper.md) | <span data-ttu-id="0e239-121">Задает свойство **клиентваллпапер** .</span><span class="sxs-lookup"><span data-stu-id="0e239-121">Sets the **ClientWallPaper** property.</span></span><br/>                      |



 

### <a name="properties"></a><span data-ttu-id="0e239-122">Свойства</span><span class="sxs-lookup"><span data-stu-id="0e239-122">Properties</span></span>

<span data-ttu-id="0e239-123">Класс **Win32 \_ тсенвиронментсеттинг** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="0e239-123">The **Win32\_TSEnvironmentSetting** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="0e239-124">**Заголовок**</span><span class="sxs-lookup"><span data-stu-id="0e239-124">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0e239-125">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="0e239-125">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0e239-126">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="0e239-126">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0e239-127">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="0e239-127">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="0e239-128">Краткое описание (однострочная строка) объекта.</span><span class="sxs-lookup"><span data-stu-id="0e239-128">Short description (one-line string) of the object.</span></span>

<span data-ttu-id="0e239-129">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="0e239-129">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="0e239-130">**клиентваллпапер**</span><span class="sxs-lookup"><span data-stu-id="0e239-130">**ClientWallPaper**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0e239-131">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="0e239-131">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="0e239-132">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="0e239-132">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0e239-133">Указывает, отображается ли изображение обоев на клиенте.</span><span class="sxs-lookup"><span data-stu-id="0e239-133">Specifies whether the wallpaper image is displayed on the client.</span></span> <span data-ttu-id="0e239-134">Отсутствие отображения изображения обоев может сэкономить системные ресурсы, уменьшая время, необходимое для перерисовки экрана.</span><span class="sxs-lookup"><span data-stu-id="0e239-134">Not displaying the wallpaper image can save system resources by decreasing the time required to repaint the screen.</span></span>

<dt>

<span id="False"></span><span id="false"></span><span id="FALSE"></span>

<span data-ttu-id="0e239-135"><span id="False"></span><span id="false"></span><span id="FALSE"></span>**False** (0)</span><span class="sxs-lookup"><span data-stu-id="0e239-135"><span id="False"></span><span id="false"></span><span id="FALSE"></span>**False** (0)</span></span>


</dt> <dd>

<span data-ttu-id="0e239-136">Изображение фонового рисунка не отображается на клиенте.</span><span class="sxs-lookup"><span data-stu-id="0e239-136">The wallpaper image is not displayed on the client.</span></span>

</dd> <dt>

<span id="True"></span><span id="true"></span><span id="TRUE"></span>

<span data-ttu-id="0e239-137"><span id="True"></span><span id="true"></span><span id="TRUE"></span>**True** (1)</span><span class="sxs-lookup"><span data-stu-id="0e239-137"><span id="True"></span><span id="true"></span><span id="TRUE"></span>**True** (1)</span></span>


</dt> <dd>

<span data-ttu-id="0e239-138">Изображение фонового рисунка отображается на клиенте.</span><span class="sxs-lookup"><span data-stu-id="0e239-138">The wallpaper image is displayed on the client.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="0e239-139">**Описание**</span><span class="sxs-lookup"><span data-stu-id="0e239-139">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0e239-140">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="0e239-140">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0e239-141">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="0e239-141">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0e239-142">Описание объекта.</span><span class="sxs-lookup"><span data-stu-id="0e239-142">Description of the object.</span></span>

<span data-ttu-id="0e239-143">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="0e239-143">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="0e239-144">**инитиалпрогрампас**</span><span class="sxs-lookup"><span data-stu-id="0e239-144">**InitialProgramPath**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0e239-145">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="0e239-145">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0e239-146">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="0e239-146">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0e239-147">Имя и путь к программе, которые пользователь будет запускать сразу после входа на сервер узла сеансов удаленных рабочих столов.</span><span class="sxs-lookup"><span data-stu-id="0e239-147">The name and the path of the program the user will run immediately after logging on to the RD Session Host server.</span></span>

</dd> <dt>

<span data-ttu-id="0e239-148">**инитиалпрограмполици**</span><span class="sxs-lookup"><span data-stu-id="0e239-148">**InitialProgramPolicy**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0e239-149">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="0e239-149">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="0e239-150">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="0e239-150">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="0e239-151">Политика, используемая сервером для определения пути и имени файла запуска программы, а также имени папки, в которой он находится.</span><span class="sxs-lookup"><span data-stu-id="0e239-151">The policy the server uses to determine the startup program path and file name, and the name of the folder it is located in.</span></span>

<dt>

<span id="Per_User"></span><span id="per_user"></span><span id="PER_USER"></span>

<span data-ttu-id="0e239-152"><span id="Per_User"></span><span id="per_user"></span><span id="PER_USER"></span>**На пользователя** (0)</span><span class="sxs-lookup"><span data-stu-id="0e239-152"><span id="Per_User"></span><span id="per_user"></span><span id="PER_USER"></span>**Per User** (0)</span></span>


</dt> <dd>

<span data-ttu-id="0e239-153">Параметры программы запуска пользователя вступают в действие.</span><span class="sxs-lookup"><span data-stu-id="0e239-153">The user's startup program settings are in effect.</span></span>

</dd> <dt>

<span id="Server-Override"></span><span id="server-override"></span><span id="SERVER-OVERRIDE"></span>

<span data-ttu-id="0e239-154"><span id="Server-Override"></span><span id="server-override"></span><span id="SERVER-OVERRIDE"></span>**Переопределение сервера** (1)</span><span class="sxs-lookup"><span data-stu-id="0e239-154"><span id="Server-Override"></span><span id="server-override"></span><span id="SERVER-OVERRIDE"></span>**Server-Override** (1)</span></span>


</dt> <dd>

<span data-ttu-id="0e239-155">Параметры программы запуска пользователя переопределяются сервером.</span><span class="sxs-lookup"><span data-stu-id="0e239-155">The user's startup program settings are overridden by the server.</span></span>

</dd> <dt>

<span id="Single-App_Mode"></span><span id="single-app_mode"></span><span id="SINGLE-APP_MODE"></span>

<span data-ttu-id="0e239-156"><span id="Single-App_Mode"></span><span id="single-app_mode"></span><span id="SINGLE-APP_MODE"></span>**Режим одного приложения** (2)</span><span class="sxs-lookup"><span data-stu-id="0e239-156"><span id="Single-App_Mode"></span><span id="single-app_mode"></span><span id="SINGLE-APP_MODE"></span>**Single-App Mode** (2)</span></span>


</dt> <dd>

<span data-ttu-id="0e239-157">В этом сеансе будет запущено только одно приложение.</span><span class="sxs-lookup"><span data-stu-id="0e239-157">Only a single application will be run in this session.</span></span> <span data-ttu-id="0e239-158">Сведения о программе запуска игнорируются.</span><span class="sxs-lookup"><span data-stu-id="0e239-158">The startup program information is ignored.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="0e239-159">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="0e239-159">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0e239-160">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="0e239-160">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="0e239-161">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="0e239-161">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0e239-162">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. \|Значение ComponentID \| 001,5 в DMTF</span><span class="sxs-lookup"><span data-stu-id="0e239-162">Qualifiers: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5")</span></span>
</dt> </dl>

<span data-ttu-id="0e239-163">Дата установки объекта.</span><span class="sxs-lookup"><span data-stu-id="0e239-163">The date the object was installed.</span></span> <span data-ttu-id="0e239-164">Отсутствие значения не означает, что объект не установлен.</span><span class="sxs-lookup"><span data-stu-id="0e239-164">A lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="0e239-165">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="0e239-165">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="0e239-166">**Name**</span><span class="sxs-lookup"><span data-stu-id="0e239-166">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0e239-167">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="0e239-167">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0e239-168">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="0e239-168">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0e239-169">Имя объекта.</span><span class="sxs-lookup"><span data-stu-id="0e239-169">The name of the object.</span></span>

<span data-ttu-id="0e239-170">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="0e239-170">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="0e239-171">**полицисаурцеклиентваллпапер**</span><span class="sxs-lookup"><span data-stu-id="0e239-171">**PolicySourceClientWallPaper**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0e239-172">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="0e239-172">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="0e239-173">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="0e239-173">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0e239-174">Указывает, настроено ли свойство **клиентваллпапер** сервером, групповой политикой или по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="0e239-174">Indicates whether the **ClientWallPaper** property is configured by the server, group policy, or by default.</span></span>

<dt>

<span data-ttu-id="0e239-175">0</span><span class="sxs-lookup"><span data-stu-id="0e239-175">0</span></span>
</dt> <dd>

<span data-ttu-id="0e239-176">Сервер</span><span class="sxs-lookup"><span data-stu-id="0e239-176">Server</span></span>

</dd> <dt>

<span data-ttu-id="0e239-177">1</span><span class="sxs-lookup"><span data-stu-id="0e239-177">1</span></span>
</dt> <dd>

<span data-ttu-id="0e239-178">Групповая политика</span><span class="sxs-lookup"><span data-stu-id="0e239-178">Group policy</span></span>

</dd> <dt>

<span data-ttu-id="0e239-179">2</span><span class="sxs-lookup"><span data-stu-id="0e239-179">2</span></span>
</dt> <dd>

<span data-ttu-id="0e239-180">Значение по умолчанию</span><span class="sxs-lookup"><span data-stu-id="0e239-180">Default</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="0e239-181">**полицисаурцеинитиалпрогрампас**</span><span class="sxs-lookup"><span data-stu-id="0e239-181">**PolicySourceInitialProgramPath**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0e239-182">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="0e239-182">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="0e239-183">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="0e239-183">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0e239-184">Указывает, настроено ли свойство **инитиалпрогрампас** сервером, групповой политикой или по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="0e239-184">Indicates whether the **InitialProgramPath** property is configured by the server, group policy, or by default.</span></span>

<dt>

<span data-ttu-id="0e239-185">0</span><span class="sxs-lookup"><span data-stu-id="0e239-185">0</span></span>
</dt> <dd>

<span data-ttu-id="0e239-186">Сервер</span><span class="sxs-lookup"><span data-stu-id="0e239-186">Server</span></span>

</dd> <dt>

<span data-ttu-id="0e239-187">1</span><span class="sxs-lookup"><span data-stu-id="0e239-187">1</span></span>
</dt> <dd>

<span data-ttu-id="0e239-188">Групповая политика</span><span class="sxs-lookup"><span data-stu-id="0e239-188">Group policy</span></span>

</dd> <dt>

<span data-ttu-id="0e239-189">2</span><span class="sxs-lookup"><span data-stu-id="0e239-189">2</span></span>
</dt> <dd>

<span data-ttu-id="0e239-190">Значение по умолчанию</span><span class="sxs-lookup"><span data-stu-id="0e239-190">Default</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="0e239-191">**полицисаурцестартин**</span><span class="sxs-lookup"><span data-stu-id="0e239-191">**PolicySourceStartIn**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0e239-192">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="0e239-192">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="0e239-193">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="0e239-193">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0e239-194">Указывает, настроено ли свойство **starting** сервером, групповой политикой или по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="0e239-194">Indicates whether the **StartIn** property is configured by the server, group policy, or by default.</span></span>

<dt>

<span data-ttu-id="0e239-195">0</span><span class="sxs-lookup"><span data-stu-id="0e239-195">0</span></span>
</dt> <dd>

<span data-ttu-id="0e239-196">Сервер</span><span class="sxs-lookup"><span data-stu-id="0e239-196">Server</span></span>

</dd> <dt>

<span data-ttu-id="0e239-197">1</span><span class="sxs-lookup"><span data-stu-id="0e239-197">1</span></span>
</dt> <dd>

<span data-ttu-id="0e239-198">Групповая политика</span><span class="sxs-lookup"><span data-stu-id="0e239-198">Group policy</span></span>

</dd> <dt>

<span data-ttu-id="0e239-199">2</span><span class="sxs-lookup"><span data-stu-id="0e239-199">2</span></span>
</dt> <dd>

<span data-ttu-id="0e239-200">Значение по умолчанию</span><span class="sxs-lookup"><span data-stu-id="0e239-200">Default</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="0e239-201">**Startin**</span><span class="sxs-lookup"><span data-stu-id="0e239-201">**Startin**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0e239-202">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="0e239-202">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0e239-203">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="0e239-203">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0e239-204">Путь к рабочему каталогу программы, который пользователь будет запускать сразу после входа на сервер узла сеансов удаленных рабочих столов.</span><span class="sxs-lookup"><span data-stu-id="0e239-204">The path of the working directory of the program the user will run immediately after logging on to the RD Session Host server.</span></span>

</dd> <dt>

<span data-ttu-id="0e239-205">**Состояние**</span><span class="sxs-lookup"><span data-stu-id="0e239-205">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0e239-206">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="0e239-206">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0e239-207">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="0e239-207">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0e239-208">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span><span class="sxs-lookup"><span data-stu-id="0e239-208">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span></span>
</dt> </dl>

<span data-ttu-id="0e239-209">Текущее состояние объекта.</span><span class="sxs-lookup"><span data-stu-id="0e239-209">Current status of the object.</span></span> <span data-ttu-id="0e239-210">Можно определить различные операционные и неоперационные состояния.</span><span class="sxs-lookup"><span data-stu-id="0e239-210">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="0e239-211">Рабочие состояния включают: "ОК", "деградация" и "пред-ошибка" (элемент, например жесткий диск с поддержкой SMART, может работать правильно, но прогнозировать сбой в ближайшем будущем).</span><span class="sxs-lookup"><span data-stu-id="0e239-211">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="0e239-212">Неработающие состояния включают: "ошибка", "Запуск", "остановка" и "служба".</span><span class="sxs-lookup"><span data-stu-id="0e239-212">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="0e239-213">Последняя, «служба», может применяться во время зеркального копирования диска, перезагрузки списка разрешений пользователя или другой административной работы.</span><span class="sxs-lookup"><span data-stu-id="0e239-213">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="0e239-214">Не вся такая работа выполняется в интерактивном состоянии, но управляемый элемент не является ни "ОК", ни одним из других состояний.</span><span class="sxs-lookup"><span data-stu-id="0e239-214">Not all such work is on-line, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="0e239-215">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="0e239-215">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<dt>



 <span data-ttu-id="0e239-216">("ОК")</span><span class="sxs-lookup"><span data-stu-id="0e239-216">("OK")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="0e239-217">("Ошибка")</span><span class="sxs-lookup"><span data-stu-id="0e239-217">("Error")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="0e239-218">("Пониженное состояние")</span><span class="sxs-lookup"><span data-stu-id="0e239-218">("Degraded")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="0e239-219">("Неизвестно")</span><span class="sxs-lookup"><span data-stu-id="0e239-219">("Unknown")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="0e239-220">("Пред Fail")</span><span class="sxs-lookup"><span data-stu-id="0e239-220">("Pred Fail")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="0e239-221">("Запуск")</span><span class="sxs-lookup"><span data-stu-id="0e239-221">("Starting")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="0e239-222">("Остановка")</span><span class="sxs-lookup"><span data-stu-id="0e239-222">("Stopping")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="0e239-223">("Служба")</span><span class="sxs-lookup"><span data-stu-id="0e239-223">("Service")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="0e239-224">**терминалнаме**</span><span class="sxs-lookup"><span data-stu-id="0e239-224">**TerminalName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0e239-225">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="0e239-225">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0e239-226">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="0e239-226">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0e239-227">Имя терминала.</span><span class="sxs-lookup"><span data-stu-id="0e239-227">The name of the terminal.</span></span>

<span data-ttu-id="0e239-228">Это свойство наследуется из [**Win32 \_ терминалсеттинг**](win32-terminalsetting.md).</span><span class="sxs-lookup"><span data-stu-id="0e239-228">This property is inherited from [**Win32\_TerminalSetting**](win32-terminalsetting.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="0e239-229">Комментарии</span><span class="sxs-lookup"><span data-stu-id="0e239-229">Remarks</span></span>

<span data-ttu-id="0e239-230">Имейте в виду, что Винстатионс, связанные с сеансом консоли, не могут получить доступ к методам и свойствам этого класса.</span><span class="sxs-lookup"><span data-stu-id="0e239-230">Be aware that Winstations that are associated with the console session cannot access the methods and properties of this class.</span></span> <span data-ttu-id="0e239-231">Если предпринимается попытка сделать это, указав "Console" в качестве значения свойства **терминалнаме** , методы этого объекта возвращают **WBEM \_ E \_ не \_ поддерживаются**.</span><span class="sxs-lookup"><span data-stu-id="0e239-231">If an attempt is made to do so by specifying "Console" as the value of the **TerminalName** property, methods of this object return **WBEM\_E\_NOT\_SUPPORTED**.</span></span> <span data-ttu-id="0e239-232">Этот код ошибки также возвращается, если станция окна пытается вызвать методы этого объекта для добавления или изменения свойств безопасности учетных записей LocalSystem, LocalService или NetworkService.</span><span class="sxs-lookup"><span data-stu-id="0e239-232">This error code is also returned if a window station attempts to call methods of this object to add or modify the security properties of the LocalSystem, LocalService, or NetworkService accounts.</span></span>

<span data-ttu-id="0e239-233">Чтобы подключиться к \\ корневому \\ \\ пространству имен CIMV2 терминалсервицес, уровень проверки подлинности должен включать в себя конфиденциальность пакетов.</span><span class="sxs-lookup"><span data-stu-id="0e239-233">To connect to the \\root\\CIMV2\\TerminalServices namespace, the authentication level must include packet privacy.</span></span> <span data-ttu-id="0e239-234">Для вызовов C/C++ это уровень проверки подлинности **AUTHN на \_ \_ \_ уровне \_ \_ безопасности RPC C уровня "PKT**".</span><span class="sxs-lookup"><span data-stu-id="0e239-234">For C/C++ calls, this is an authentication level of **RPC\_C\_AUTHN\_LEVEL\_PKT\_PRIVACY**.</span></span> <span data-ttu-id="0e239-235">Для Visual Basic и написания сценариев это уровень проверки подлинности **вбемаусентикатионлевелпктприваци** или "пктприваци" со значением 6.</span><span class="sxs-lookup"><span data-stu-id="0e239-235">For Visual Basic and scripting calls, this is an authentication level of **WbemAuthenticationLevelPktPrivacy** or "pktPrivacy", with a value of 6.</span></span> <span data-ttu-id="0e239-236">В следующем примере Visual Basic Scripting Edition (VBScript) показано, как подключиться к удаленному компьютеру с использованием конфиденциальности пакетов.</span><span class="sxs-lookup"><span data-stu-id="0e239-236">The following Visual Basic Scripting Edition (VBScript) example shows how to connect to a remote computer with packet privacy.</span></span>


```VB
strComputer = "RemoteServer1" 
Set objServices = GetObject( _
    "winmgmts:{authenticationLevel=pktPrivacy}!Root/CIMv2/TerminalServices")
```



<span data-ttu-id="0e239-237">Файлы MOF-файл (MOF) содержат определения для классов инструментарий управления Windows (WMI) (WMI).</span><span class="sxs-lookup"><span data-stu-id="0e239-237">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="0e239-238">MOF-файлы не устанавливаются в составе пакета средств разработки программного обеспечения Microsoft Windows (SDK).</span><span class="sxs-lookup"><span data-stu-id="0e239-238">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="0e239-239">Они устанавливаются на сервере при добавлении связанной роли с помощью диспетчер сервера.</span><span class="sxs-lookup"><span data-stu-id="0e239-239">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="0e239-240">Дополнительные сведения о файлах MOF см. в разделе [MOF-файл (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="0e239-240">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="0e239-241">Требования</span><span class="sxs-lookup"><span data-stu-id="0e239-241">Requirements</span></span>



| <span data-ttu-id="0e239-242">Требование</span><span class="sxs-lookup"><span data-stu-id="0e239-242">Requirement</span></span> | <span data-ttu-id="0e239-243">Значение</span><span class="sxs-lookup"><span data-stu-id="0e239-243">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="0e239-244">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="0e239-244">Minimum supported client</span></span><br/> | <span data-ttu-id="0e239-245">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="0e239-245">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="0e239-246">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="0e239-246">Minimum supported server</span></span><br/> | <span data-ttu-id="0e239-247">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="0e239-247">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="0e239-248">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="0e239-248">Namespace</span></span><br/>                | <span data-ttu-id="0e239-249">Корневой \\ CIMv2 \\ терминалсервицес</span><span class="sxs-lookup"><span data-stu-id="0e239-249">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="0e239-250">MOF</span><span class="sxs-lookup"><span data-stu-id="0e239-250">MOF</span></span><br/>                      | <dl> <span data-ttu-id="0e239-251"><dt>Тскфгвми. mof</dt></span><span class="sxs-lookup"><span data-stu-id="0e239-251"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="0e239-252">DLL</span><span class="sxs-lookup"><span data-stu-id="0e239-252">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0e239-253"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0e239-253"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0e239-254">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="0e239-254">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0e239-255">**\_Терминалсеттинг Win32**</span><span class="sxs-lookup"><span data-stu-id="0e239-255">**Win32\_TerminalSetting**</span></span>](win32-terminalsetting.md)
</dt> </dl>

 

