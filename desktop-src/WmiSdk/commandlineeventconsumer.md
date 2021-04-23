---
description: Класс Коммандлинивентконсумер запускает произвольный процесс в локальной системе при доставке события в него.
ms.assetid: 0dcae783-1722-45a4-b5d4-3fcf455dacf8
ms.tgt_platform: multiple
title: Класс Коммандлинивентконсумер
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CommandLineEventConsumer
- CommandLineEventConsumer.CreatorSID
- CommandLineEventConsumer.MachineName
- CommandLineEventConsumer.MaximumQueueSize
- CommandLineEventConsumer.CommandLineTemplate
- CommandLineEventConsumer.CreateNewConsole
- CommandLineEventConsumer.CreateNewProcessGroup
- CommandLineEventConsumer.CreateSeparateWowVdm
- CommandLineEventConsumer.CreateSharedWowVdm
- CommandLineEventConsumer.DesktopName
- CommandLineEventConsumer.ExecutablePath
- CommandLineEventConsumer.FillAttributes
- CommandLineEventConsumer.ForceOffFeedback
- CommandLineEventConsumer.ForceOnFeedback
- CommandLineEventConsumer.KillTimeout
- CommandLineEventConsumer.Name
- CommandLineEventConsumer.Priority
- CommandLineEventConsumer.RunInteractively
- CommandLineEventConsumer.ShowWindowCommand
- CommandLineEventConsumer.UseDefaultErrorMode
- CommandLineEventConsumer.WindowTitle
- CommandLineEventConsumer.WorkingDirectory
- CommandLineEventConsumer.XCoordinate
- CommandLineEventConsumer.XNumCharacters
- CommandLineEventConsumer.XSize
- CommandLineEventConsumer.YCoordinate
- CommandLineEventConsumer.YNumCharacters
- CommandLineEventConsumer.YSize
- CommandLineEventConsumer.FillAttribute
api_type:
- DllExport
api_location:
- Wbemcons.dll
ms.openlocfilehash: 1784ba116417f6ed94aed2249a797cf8de4b3527
ms.sourcegitcommit: 0e611cdff84ff9f897c59e4e1d2b2d134bc4e133
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/02/2021
ms.locfileid: "106187937"
---
# <a name="commandlineeventconsumer-class"></a><span data-ttu-id="078a2-103">Класс Коммандлинивентконсумер</span><span class="sxs-lookup"><span data-stu-id="078a2-103">CommandLineEventConsumer class</span></span>

<span data-ttu-id="078a2-104">Класс **коммандлинивентконсумер** запускает произвольный процесс в локальной системе при доставке события в него.</span><span class="sxs-lookup"><span data-stu-id="078a2-104">The **CommandLineEventConsumer** class starts an arbitrary process in the local system when an event is delivered to it.</span></span> <span data-ttu-id="078a2-105">Этот класс является одним из стандартных потребителей событий, предоставляемых инструментарием WMI.</span><span class="sxs-lookup"><span data-stu-id="078a2-105">This class is one of the standard event consumers that WMI provides.</span></span> <span data-ttu-id="078a2-106">Дополнительные сведения см. [в разделе Мониторинг и реагирование на события с помощью стандартных потребителей](monitoring-and-responding-to-events-with-standard-consumers.md).</span><span class="sxs-lookup"><span data-stu-id="078a2-106">For more information, see [Monitoring and Responding to Events with Standard Consumers](monitoring-and-responding-to-events-with-standard-consumers.md).</span></span>

> [!Note]  
> <span data-ttu-id="078a2-107">При использовании класса **коммандлинивентконсумер** Обеспечьте безопасность исполняемого файла, который требуется запустить.</span><span class="sxs-lookup"><span data-stu-id="078a2-107">When using the **CommandLineEventConsumer** class, secure the executable that you want to start.</span></span> <span data-ttu-id="078a2-108">Если исполняемый файл не находится в безопасном месте или защищен с помощью строгого списка управления доступом (ACL), неавторизованный пользователь может заменить исполняемый файл вредоносным.</span><span class="sxs-lookup"><span data-stu-id="078a2-108">If the executable is not in a secure location, or secured with a strong access control list (ACL), an unauthorized user can replace your executable with a malicious executable.</span></span> <span data-ttu-id="078a2-109">Дополнительные сведения об ACL см. в разделе "безопасность" пакета средств разработки программного обеспечения Microsoft Windows (SDK) и разделе [Создание дескриптора безопасности для нового объекта](/windows/desktop/SecAuthZ/creating-a-security-descriptor-for-a-new-object-in-c--).</span><span class="sxs-lookup"><span data-stu-id="078a2-109">For more information about ACLs, visit the Security section of the Microsoft Windows Software Development Kit (SDK), and see [Creating a Security Descriptor for a New Object](/windows/desktop/SecAuthZ/creating-a-security-descriptor-for-a-new-object-in-c--).</span></span>

 

## <a name="syntax"></a><span data-ttu-id="078a2-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="078a2-110">Syntax</span></span>

``` syntax
[AMENDMENT]
class CommandLineEventConsumer : __EventConsumer
{
  uint8   CreatorSID[];
  string  MachineName;
  uint32  MaximumQueueSize;
  string  CommandLineTemplate;
  boolean CreateNewConsole = False;
  boolean CreateNewProcessGroup = True;
  boolean CreateSeparateWowVdm = False;
  boolean CreateSharedWowVdm = False;
  string  DesktopName;
  string  ExecutablePath;
  uint32  FillAttributes;
  boolean ForceOffFeedback = False;
  boolean ForceOnFeedback = False;
  uint32  KillTimeout = 0;
  string  Name;
  sint32  Priority = 0x20;
  boolean RunInteractively = False;
  uint32  ShowWindowCommand;
  boolean UseDefaultErrorMode = False;
  string  WindowTitle;
  string  WorkingDirectory;
  uint32  XCoordinate;
  uint32  XNumCharacters;
  uint32  XSize;
  uint32  YCoordinate;
  uint32  YNumCharacters;
  uint32  YSize;
  uint32  FillAttribute;
};
```

## <a name="members"></a><span data-ttu-id="078a2-111">Члены</span><span class="sxs-lookup"><span data-stu-id="078a2-111">Members</span></span>

<span data-ttu-id="078a2-112">Класс **коммандлинивентконсумер** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="078a2-112">The **CommandLineEventConsumer** class has these types of members:</span></span>

-   [<span data-ttu-id="078a2-113">Свойства</span><span class="sxs-lookup"><span data-stu-id="078a2-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="078a2-114">Свойства</span><span class="sxs-lookup"><span data-stu-id="078a2-114">Properties</span></span>

<span data-ttu-id="078a2-115">Класс **коммандлинивентконсумер** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="078a2-115">The **CommandLineEventConsumer** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="078a2-116">**коммандлинетемплате**</span><span class="sxs-lookup"><span data-stu-id="078a2-116">**CommandLineTemplate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="078a2-117">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="078a2-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="078a2-118">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="078a2-118">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="078a2-119">Стандартный строковый шаблон, указывающий запускаемый процесс.</span><span class="sxs-lookup"><span data-stu-id="078a2-119">Standard string template that specifies the process to be started.</span></span> <span data-ttu-id="078a2-120">Это свойство может иметь **значение NULL**, а свойство **ExecutablePath** используется в качестве командной строки.</span><span class="sxs-lookup"><span data-stu-id="078a2-120">This property can be **NULL**, and the **ExecutablePath** property is used as the command line.</span></span>

</dd> <dt>

<span data-ttu-id="078a2-121">**креатеневконсоле**</span><span class="sxs-lookup"><span data-stu-id="078a2-121">**CreateNewConsole**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="078a2-122">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="078a2-122">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="078a2-123">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="078a2-123">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="078a2-124">Не используется.</span><span class="sxs-lookup"><span data-stu-id="078a2-124">Not used.</span></span> <span data-ttu-id="078a2-125">Если этому свойству присвоено значение, создается сообщение трассировки.</span><span class="sxs-lookup"><span data-stu-id="078a2-125">If a value is assigned to this property, a tracing message is generated.</span></span> <span data-ttu-id="078a2-126">Дополнительные сведения см. в разделе [Трассировка действия WMI](tracing-wmi-activity.md).</span><span class="sxs-lookup"><span data-stu-id="078a2-126">For more information, see [Tracing WMI Activity](tracing-wmi-activity.md).</span></span>

</dd> <dt>

<span data-ttu-id="078a2-127">**креатеневпроцессграуп**</span><span class="sxs-lookup"><span data-stu-id="078a2-127">**CreateNewProcessGroup**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="078a2-128">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="078a2-128">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="078a2-129">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="078a2-129">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="078a2-130">Если **значение — true**, новый процесс является корневым процессом новой группы процессов.</span><span class="sxs-lookup"><span data-stu-id="078a2-130">If **True**, the new process is the root process of a new process group.</span></span> <span data-ttu-id="078a2-131">Группа процессов включает все процессы, являющиеся потомками этого корневого процесса.</span><span class="sxs-lookup"><span data-stu-id="078a2-131">The process group includes all processes that are descendants of this root process.</span></span> <span data-ttu-id="078a2-132">Идентификатор процесса новой группы процессов аналогичен идентификатору этого процесса.</span><span class="sxs-lookup"><span data-stu-id="078a2-132">The process identifier of the new process group is the same as this process identifier.</span></span> <span data-ttu-id="078a2-133">Группы процессов используются методом [**женератеконсолектрлевент**](/windows/console/generateconsolectrlevent) , чтобы разрешить отправку сигналов CTRL + C или Ctrl + Break группе процессов консоли.</span><span class="sxs-lookup"><span data-stu-id="078a2-133">Process groups are used by the [**GenerateConsoleCtrlEvent**](/windows/console/generateconsolectrlevent) method to enable sending a CTRL+C or CTRL+BREAK signal to a group of console processes.</span></span>

</dd> <dt>

<span data-ttu-id="078a2-134">**креатесепаратевоввдм**</span><span class="sxs-lookup"><span data-stu-id="078a2-134">**CreateSeparateWowVdm**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="078a2-135">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="078a2-135">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="078a2-136">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="078a2-136">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="078a2-137">Если задано **значение true**, новый процесс выполняется в частной ВИРТУАЛЬНОЙ машине DOS (VDM).</span><span class="sxs-lookup"><span data-stu-id="078a2-137">If **True**, the new process runs in a private Virtual DOS Machine (VDM).</span></span> <span data-ttu-id="078a2-138">Это допустимо только при запуске приложения, работающего в 16-разрядной операционной системе Windows.</span><span class="sxs-lookup"><span data-stu-id="078a2-138">This is only valid when starting an application running on a 16-bit Windows operating system.</span></span> <span data-ttu-id="078a2-139">Если задано значение **false**, все приложения, работающие в 16-разрядной операционной системе Windows, выполняются как потоки в одном общем виртуальном VDM.</span><span class="sxs-lookup"><span data-stu-id="078a2-139">If set to **False**, all applications running on a 16-bit Windows operating system run as threads in a single, shared VDM.</span></span> <span data-ttu-id="078a2-140">Дополнительные сведения см. в подразделе «Примечания» этого раздела.</span><span class="sxs-lookup"><span data-stu-id="078a2-140">For more information, see the Remarks section of this topic.</span></span>

</dd> <dt>

<span data-ttu-id="078a2-141">**креатешаредвоввдм**</span><span class="sxs-lookup"><span data-stu-id="078a2-141">**CreateSharedWowVdm**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="078a2-142">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="078a2-142">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="078a2-143">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="078a2-143">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="078a2-144">Если **значение — true**, метод [**CreateProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa) запускает новый процесс на общей ВИРТУАЛЬНОЙ машине DOS (VDM).</span><span class="sxs-lookup"><span data-stu-id="078a2-144">If **True**, the [**CreateProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa) method runs the new process in the shared Virtual DOS Machine (VDM).</span></span> <span data-ttu-id="078a2-145">Это свойство может переопределить параметр Дефаултсепаратевдм в разделе Windows Win.ini Если задано значение **true**.</span><span class="sxs-lookup"><span data-stu-id="078a2-145">This property can override the DefaultSeparateVDM switch in the Windows section of Win.ini if set to **True**.</span></span> <span data-ttu-id="078a2-146">Дополнительные сведения см. в подразделе «Примечания» этого раздела.</span><span class="sxs-lookup"><span data-stu-id="078a2-146">For more information, see the Remarks section of this topic.</span></span>

</dd> <dt>

<span data-ttu-id="078a2-147">**креаторсид**</span><span class="sxs-lookup"><span data-stu-id="078a2-147">**CreatorSID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="078a2-148">Тип данных: массив **Uint8**</span><span class="sxs-lookup"><span data-stu-id="078a2-148">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="078a2-149">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="078a2-149">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="078a2-150">Идентификатор безопасности (SID), однозначно определяющий пользователя, который создает фильтр.</span><span class="sxs-lookup"><span data-stu-id="078a2-150">Security identifier (SID) that uniquely identifies the user who creates a filter.</span></span> <span data-ttu-id="078a2-151">WMI хранит идентификатор безопасности пользователя, создающего экземпляр [**\_ \_ евентконсумер**](--eventconsumer.md) , или идентификатор безопасности администратора в зависимости от операционной системы.</span><span class="sxs-lookup"><span data-stu-id="078a2-151">WMI stores the SID of the user who creates an instance of [**\_\_EventConsumer**](--eventconsumer.md) or the Administrator SID, depending on the operating system.</span></span> <span data-ttu-id="078a2-152">Дополнительные сведения см. в статьях [Привязка фильтра событий к логическому потребителю](binding-an-event-filter-with-a-logical-consumer.md) и [мониторинг и реагирование на события с помощью стандартных потребителей](monitoring-and-responding-to-events-with-standard-consumers.md).</span><span class="sxs-lookup"><span data-stu-id="078a2-152">For more information, see [Binding an Event Filter with a Logical Consumer](binding-an-event-filter-with-a-logical-consumer.md) and [Monitoring and Responding to Events with Standard Consumers](monitoring-and-responding-to-events-with-standard-consumers.md).</span></span>

<span data-ttu-id="078a2-153">Это свойство наследуется от [**\_ \_ евентконсумер**](--eventconsumer.md).</span><span class="sxs-lookup"><span data-stu-id="078a2-153">This property is inherited from [**\_\_EventConsumer**](--eventconsumer.md).</span></span>

</dd> <dt>

<span data-ttu-id="078a2-154">**десктопнаме**</span><span class="sxs-lookup"><span data-stu-id="078a2-154">**DesktopName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="078a2-155">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="078a2-155">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="078a2-156">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="078a2-156">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="078a2-157">Не используется.</span><span class="sxs-lookup"><span data-stu-id="078a2-157">Not used.</span></span> <span data-ttu-id="078a2-158">Если этому свойству присвоено значение, создается сообщение трассировки.</span><span class="sxs-lookup"><span data-stu-id="078a2-158">If a value is assigned to this property a tracing message is generated.</span></span> <span data-ttu-id="078a2-159">Дополнительные сведения см. в разделе [Трассировка действия WMI](tracing-wmi-activity.md).</span><span class="sxs-lookup"><span data-stu-id="078a2-159">For more information, see [Tracing WMI Activity](tracing-wmi-activity.md).</span></span>

</dd> <dt>

<span data-ttu-id="078a2-160">**ExecutablePath**</span><span class="sxs-lookup"><span data-stu-id="078a2-160">**ExecutablePath**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="078a2-161">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="078a2-161">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="078a2-162">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="078a2-162">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="078a2-163">Выполняемый модуль.</span><span class="sxs-lookup"><span data-stu-id="078a2-163">Module to execute.</span></span> <span data-ttu-id="078a2-164">В строке можно указать полный путь и имя файла модуля для выполнения, а также указать часть имени.</span><span class="sxs-lookup"><span data-stu-id="078a2-164">The string can specify the full path and file name of the module to execute, or it can specify a partial name.</span></span> <span data-ttu-id="078a2-165">Если указано частичное имя, предполагается текущий диск и текущий каталог.</span><span class="sxs-lookup"><span data-stu-id="078a2-165">If a partial name is specified, the current drive and current directory are assumed.</span></span>

<span data-ttu-id="078a2-166">Свойство **ExecutablePath** может иметь **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="078a2-166">The **ExecutablePath** property can be **NULL**.</span></span> <span data-ttu-id="078a2-167">В этом случае имя модуля должно быть первым пустым маркером, разделенным пробелом, в значении свойства **коммандлинетемплате** .</span><span class="sxs-lookup"><span data-stu-id="078a2-167">In that case, the module name must be the first white space-delimited token in the **CommandLineTemplate** property value.</span></span> <span data-ttu-id="078a2-168">При использовании длинного имени файла, содержащего пробел, используйте заключенные в кавычки строки, чтобы указать, где заканчивается имя файла, а аргументы начинаются для уточнения имени файла.</span><span class="sxs-lookup"><span data-stu-id="078a2-168">If using a long file name that contains a space, use quoted strings to indicate where the file name ends and the arguments begin to clarify the file name.</span></span>

> [!Note]  
> <span data-ttu-id="078a2-169">Так как свойство **коммандлинетемплате** может быть шаблоном, в котором выполняемый модуль предоставляется переменной, свойство **ExecutablePath** **null** разрешает модуль, указанный в параметре, для выполнения, после чего он выходит за пределы вашего элемента управления.</span><span class="sxs-lookup"><span data-stu-id="078a2-169">Because the **CommandLineTemplate** property can be a template where the module to execute is supplied by a variable, a **NULL** **ExecutablePath** property permits the module that is specified in the parameter to execute, and then it is out of your control.</span></span> <span data-ttu-id="078a2-170">Всегда задавайте свойство **ExecutablePath** в регистрации **коммандлинивентконсумер** , чтобы включить необходимый исполняемый файл, что позволяет избежать перезаписи параметров событий.</span><span class="sxs-lookup"><span data-stu-id="078a2-170">Always set the **ExecutablePath** property in the **CommandLineEventConsumer** registration to include the required executable, which avoids overwriting by events parameters.</span></span> <span data-ttu-id="078a2-171">Если необходимо использовать шаблон и переменную для указания модуля для выполнения, будьте внимательны в том, кому предоставлены права на полную запись в пространстве имен.</span><span class="sxs-lookup"><span data-stu-id="078a2-171">If you must use a template and variable to specify the module to execute, be careful about who is granted full write privilege in the namespace.</span></span>

 

</dd> <dt>

<span data-ttu-id="078a2-172">**филлаттрибуте**</span><span class="sxs-lookup"><span data-stu-id="078a2-172">**FillAttribute**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="078a2-173">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="078a2-173">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="078a2-174">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="078a2-174">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="078a2-175">Задает первоначальный текст и цвет фона при создании нового окна консоли в консольном приложении</span><span class="sxs-lookup"><span data-stu-id="078a2-175">Specifies the initial text and background colors if a new console window is created in a console application</span></span>

</dd> <dt>

<span data-ttu-id="078a2-176">**филлаттрибутес**</span><span class="sxs-lookup"><span data-stu-id="078a2-176">**FillAttributes**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="078a2-177">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="078a2-177">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="078a2-178">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="078a2-178">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="078a2-179">Исходные цвета текста и фона, если в консольном приложении создается новое окно консоли.</span><span class="sxs-lookup"><span data-stu-id="078a2-179">Initial text and background colors, if a new console window is created in a console application.</span></span> <span data-ttu-id="078a2-180">Это свойство не учитывается в приложении графического пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="078a2-180">This property is ignored in a GUI application.</span></span> <span data-ttu-id="078a2-181">Значением может быть любое сочетание следующих значений.</span><span class="sxs-lookup"><span data-stu-id="078a2-181">The value can be any combination of the following values.</span></span>

<dt>

<span data-ttu-id="078a2-182">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="078a2-182">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="078a2-183">синий передний план</span><span class="sxs-lookup"><span data-stu-id="078a2-183">blue foreground</span></span>

</dd> <dt>

<span data-ttu-id="078a2-184">2 (0x2)</span><span class="sxs-lookup"><span data-stu-id="078a2-184">2 (0x2)</span></span>
</dt> <dd>

<span data-ttu-id="078a2-185">Зеленый передний план</span><span class="sxs-lookup"><span data-stu-id="078a2-185">green foreground</span></span>

</dd> <dt>

<span data-ttu-id="078a2-186">4 (0x4)</span><span class="sxs-lookup"><span data-stu-id="078a2-186">4 (0x4)</span></span>
</dt> <dd>

<span data-ttu-id="078a2-187">красный передний план</span><span class="sxs-lookup"><span data-stu-id="078a2-187">red foreground</span></span>

</dd> <dt>

<span data-ttu-id="078a2-188">8 (0x8)</span><span class="sxs-lookup"><span data-stu-id="078a2-188">8 (0x8)</span></span>
</dt> <dd>

<span data-ttu-id="078a2-189">интенсивность переднего плана</span><span class="sxs-lookup"><span data-stu-id="078a2-189">foreground intensity</span></span>

</dd> <dt>

<span data-ttu-id="078a2-190">16 (0x10)</span><span class="sxs-lookup"><span data-stu-id="078a2-190">16 (0x10)</span></span>
</dt> <dd>

<span data-ttu-id="078a2-191">синий фон</span><span class="sxs-lookup"><span data-stu-id="078a2-191">blue background</span></span>

</dd> <dt>

<span data-ttu-id="078a2-192">32 (0x20)</span><span class="sxs-lookup"><span data-stu-id="078a2-192">32 (0x20)</span></span>
</dt> <dd>

<span data-ttu-id="078a2-193">зеленый фон</span><span class="sxs-lookup"><span data-stu-id="078a2-193">green background</span></span>

</dd> <dt>

<span data-ttu-id="078a2-194">64 (0x40)</span><span class="sxs-lookup"><span data-stu-id="078a2-194">64 (0x40)</span></span>
</dt> <dd>

<span data-ttu-id="078a2-195">красный фон</span><span class="sxs-lookup"><span data-stu-id="078a2-195">red background</span></span>

</dd> <dt>

<span data-ttu-id="078a2-196">128 (0x80)</span><span class="sxs-lookup"><span data-stu-id="078a2-196">128 (0x80)</span></span>
</dt> <dd>

<span data-ttu-id="078a2-197">интенсивность фона</span><span class="sxs-lookup"><span data-stu-id="078a2-197">background intensity</span></span>

</dd> </dl>

<span data-ttu-id="078a2-198">Например, следующие сочетания выдают красный текст на белом фоне:</span><span class="sxs-lookup"><span data-stu-id="078a2-198">For example, the following combinations produce red text on a white background:</span></span>


```mof
0x4 | 0x40 | 0x20 | 0x10
```



  <span data-ttu-id="078a2-199">или</span><span class="sxs-lookup"><span data-stu-id="078a2-199">or</span></span>  


```mof
0x74
```



</dd> <dt>

<span data-ttu-id="078a2-200">**форцеофффидбакк**</span><span class="sxs-lookup"><span data-stu-id="078a2-200">**ForceOffFeedback**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="078a2-201">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="078a2-201">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="078a2-202">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="078a2-202">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="078a2-203">Если **значение — true**, курсор обратной связи принудительно отключается во время запуска процесса.</span><span class="sxs-lookup"><span data-stu-id="078a2-203">If **True**, the feedback cursor is forced off while the process is starting.</span></span> <span data-ttu-id="078a2-204">Отображается стандартный курсор.</span><span class="sxs-lookup"><span data-stu-id="078a2-204">The normal cursor is displayed.</span></span>

</dd> <dt>

<span data-ttu-id="078a2-205">**форцеонфидбакк**</span><span class="sxs-lookup"><span data-stu-id="078a2-205">**ForceOnFeedback**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="078a2-206">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="078a2-206">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="078a2-207">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="078a2-207">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="078a2-208">Если **значение — true**, курсор находится в режиме обратной связи в течение двух секунд после вызова [**CreateProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa) .</span><span class="sxs-lookup"><span data-stu-id="078a2-208">If **True**, the cursor is in feedback mode for two seconds after [**CreateProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa) is called.</span></span> <span data-ttu-id="078a2-209">В течение этих двух секунд, если процесс выполняет первый вызов графического пользовательского интерфейса, система выдает пять секунд на процесс.</span><span class="sxs-lookup"><span data-stu-id="078a2-209">During those two seconds, if the process makes the first GUI call, the system gives five more seconds to the process.</span></span> <span data-ttu-id="078a2-210">В течение этих пяти секунд, если в процессе отображается окно, система покажет процессу еще пять секунд на завершение рисования окна.</span><span class="sxs-lookup"><span data-stu-id="078a2-210">During those five seconds, if the process shows a window, the system gives another five seconds to the process to finish drawing the window.</span></span>

</dd> <dt>

<span data-ttu-id="078a2-211">**киллтимеаут**</span><span class="sxs-lookup"><span data-stu-id="078a2-211">**KillTimeout**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="078a2-212">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="078a2-212">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="078a2-213">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="078a2-213">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="078a2-214">Число (в секундах), в течение которого служба WMI ожидает перед завершением процесса 0 (нуль), что означает, что процесс не должен быть завершен.</span><span class="sxs-lookup"><span data-stu-id="078a2-214">Number, in seconds, that the WMI service waits before killing a process 0 (zero) indicates a process is not to be killed.</span></span> <span data-ttu-id="078a2-215">Прерывание процесса предотвращает неограниченное время выполнения процесса.</span><span class="sxs-lookup"><span data-stu-id="078a2-215">Killing a process prevents a process from running indefinitely.</span></span>

</dd> <dt>

<span data-ttu-id="078a2-216">**MachineName**</span><span class="sxs-lookup"><span data-stu-id="078a2-216">**MachineName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="078a2-217">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="078a2-217">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="078a2-218">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="078a2-218">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="078a2-219">Имя компьютера, на который инструментарий управления Windows (WMI) (WMI) отправляет события.</span><span class="sxs-lookup"><span data-stu-id="078a2-219">Name of the computer to which Windows Management Instrumentation (WMI) sends events.</span></span>

<span data-ttu-id="078a2-220">Это свойство наследуется от [**\_ \_ евентконсумер**](--eventconsumer.md).</span><span class="sxs-lookup"><span data-stu-id="078a2-220">This property is inherited from [**\_\_EventConsumer**](--eventconsumer.md).</span></span>

</dd> <dt>

<span data-ttu-id="078a2-221">**максимумкуеуесизе**</span><span class="sxs-lookup"><span data-stu-id="078a2-221">**MaximumQueueSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="078a2-222">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="078a2-222">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="078a2-223">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="078a2-223">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="078a2-224">Максимальная очередь для конкретного потребителя в байтах.</span><span class="sxs-lookup"><span data-stu-id="078a2-224">Maximum queue for a specific consumer, in bytes.</span></span>

<span data-ttu-id="078a2-225">Это свойство наследуется от [**\_ \_ евентконсумер**](--eventconsumer.md).</span><span class="sxs-lookup"><span data-stu-id="078a2-225">This property is inherited from [**\_\_EventConsumer**](--eventconsumer.md).</span></span>

</dd> <dt>

<span data-ttu-id="078a2-226">**имя**;</span><span class="sxs-lookup"><span data-stu-id="078a2-226">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="078a2-227">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="078a2-227">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="078a2-228">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="078a2-228">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="078a2-229">Квалификаторы: [ **ключ**](key-qualifier.md)</span><span class="sxs-lookup"><span data-stu-id="078a2-229">Qualifiers: [**key**](key-qualifier.md)</span></span>
</dt> </dl>

<span data-ttu-id="078a2-230">Уникальное имя потребителя.</span><span class="sxs-lookup"><span data-stu-id="078a2-230">Unique name of a consumer.</span></span>

</dd> <dt>

<span data-ttu-id="078a2-231">**Приоритет**</span><span class="sxs-lookup"><span data-stu-id="078a2-231">**Priority**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="078a2-232">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="078a2-232">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="078a2-233">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="078a2-233">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="078a2-234">Планирование уровня приоритета потоков процесса.</span><span class="sxs-lookup"><span data-stu-id="078a2-234">Scheduling priority level of the process threads.</span></span> <span data-ttu-id="078a2-235">В следующем списке перечислены доступные уровни приоритета.</span><span class="sxs-lookup"><span data-stu-id="078a2-235">The following list lists the priority levels available.</span></span>

<dt>

<span data-ttu-id="078a2-236">32 (0x20)</span><span class="sxs-lookup"><span data-stu-id="078a2-236">32 (0x20)</span></span>
</dt> <dd>

<span data-ttu-id="078a2-237">Обозначает нормальную процедуру без необходимости планирования.</span><span class="sxs-lookup"><span data-stu-id="078a2-237">Indicates a normal process without scheduling needs.</span></span>

</dd> <dt>

<span data-ttu-id="078a2-238">64 (0x40)</span><span class="sxs-lookup"><span data-stu-id="078a2-238">64 (0x40)</span></span>
</dt> <dd>

<span data-ttu-id="078a2-239">Обозначает процесс, потоки которого выполняются только в момент бездействия системы, и прерываются потоками любого процесса, запущенного в классе с более высоким приоритетом.</span><span class="sxs-lookup"><span data-stu-id="078a2-239">Indicates a process whose threads run only when the system is idle, and are preempted by the threads of any process running in a higher priority class.</span></span> <span data-ttu-id="078a2-240">Примером является экранная заставка.</span><span class="sxs-lookup"><span data-stu-id="078a2-240">An example is a screen saver.</span></span> <span data-ttu-id="078a2-241">Класс приоритета простоя наследуется дочерними процессами.</span><span class="sxs-lookup"><span data-stu-id="078a2-241">The idle priority class is inherited by child processes.</span></span>

</dd> <dt>

<span data-ttu-id="078a2-242">128 (0x80)</span><span class="sxs-lookup"><span data-stu-id="078a2-242">128 (0x80)</span></span>
</dt> <dd>

<span data-ttu-id="078a2-243">Обозначает процесс, который выполняет критически важные задачи с высоким приоритетом.</span><span class="sxs-lookup"><span data-stu-id="078a2-243">Indicates a process that performs high-priority, time critical tasks.</span></span> <span data-ttu-id="078a2-244">Потоки процесса класса с высоким приоритетом загружают потоки процессов класса с обычным приоритетом или с приоритетом простоя.</span><span class="sxs-lookup"><span data-stu-id="078a2-244">The threads of a high-priority class process preempts the threads of normal-priority or idle-priority class processes.</span></span> <span data-ttu-id="078a2-245">Примером может быть список задач, который должен быстро реагировать при вызове пользователем, независимо от нагрузки на систему.</span><span class="sxs-lookup"><span data-stu-id="078a2-245">An example is the Task List, which must respond quickly when called by the user regardless of the load on the system.</span></span> <span data-ttu-id="078a2-246">При использовании класса с высоким приоритетом следует использовать крайне осторожно, поскольку зависящее от ЦП приложение с высокоприоритетным классом может использовать почти все доступные циклы.</span><span class="sxs-lookup"><span data-stu-id="078a2-246">Use extreme care when using the high-priority class, because a CPU-bound application with a high-priority class can use nearly all available cycles.</span></span>

</dd> <dt>

<span data-ttu-id="078a2-247">256 (0x100)</span><span class="sxs-lookup"><span data-stu-id="078a2-247">256 (0x100)</span></span>
</dt> <dd>

<span data-ttu-id="078a2-248">Указывает процесс с наибольшим возможным приоритетом.</span><span class="sxs-lookup"><span data-stu-id="078a2-248">Indicates a process that has the highest possible priority.</span></span> <span data-ttu-id="078a2-249">Потоки процесса класса приоритета в режиме реального времени выгружают потоки всех других процессов, включая процессы операционной системы, выполняющие важные задачи.</span><span class="sxs-lookup"><span data-stu-id="078a2-249">The threads of a real-time priority class process preempt the threads of all other processes, including operating system processes that perform important tasks.</span></span> <span data-ttu-id="078a2-250">Например, процесс в режиме реального времени, который выполняется в течение более короткого интервала, может привести к тому, что кэши дисков не будут сбрасываться или заставить мышь не отвечать.</span><span class="sxs-lookup"><span data-stu-id="078a2-250">For example, a real-time process that executes for more than a brief interval can cause disk caches not to flush, or cause the mouse to be unresponsive.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="078a2-251">**рунинтерактивели**</span><span class="sxs-lookup"><span data-stu-id="078a2-251">**RunInteractively**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="078a2-252">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="078a2-252">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="078a2-253">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="078a2-253">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="078a2-254">Если **значение — true**, процесс запускается в интерактивном винстатион.</span><span class="sxs-lookup"><span data-stu-id="078a2-254">If **True**, the process is launched in the interactive WinStation.</span></span> <span data-ttu-id="078a2-255">Если **значение равно false**, процесс запускается в службе по умолчанию винстатион.</span><span class="sxs-lookup"><span data-stu-id="078a2-255">If **False**, the process is launched in the default service WinStation.</span></span> <span data-ttu-id="078a2-256">Это свойство переопределяет свойство **десктопнаме** .</span><span class="sxs-lookup"><span data-stu-id="078a2-256">This property overrides the **DesktopName** property.</span></span> <span data-ttu-id="078a2-257">Это свойство используется только локально и только в том случае, если текущий пользователь является тем же пользователем, который настроил потребителя.</span><span class="sxs-lookup"><span data-stu-id="078a2-257">This property is only used locally, and only if the interactive user is the same user who set up the consumer.</span></span>

<span data-ttu-id="078a2-258">Начиная с Windows Vista, процесс, выполняющий экземпляр **коммандлинивентконсумер** , запускается под учетной записью **LocalSystem** и находится в сеансе 0.</span><span class="sxs-lookup"><span data-stu-id="078a2-258">Starting with Windows Vista, the process running the **CommandLineEventConsumer** instance is started under the **LocalSystem** account and is in session 0.</span></span> <span data-ttu-id="078a2-259">Службы, которые работают в сеансе 0, не могут взаимодействовать с пользовательскими сеансами.</span><span class="sxs-lookup"><span data-stu-id="078a2-259">Services which run in session 0 cannot interact with user sessions.</span></span>

</dd> <dt>

<span data-ttu-id="078a2-260">**шоввиндовкомманд**</span><span class="sxs-lookup"><span data-stu-id="078a2-260">**ShowWindowCommand**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="078a2-261">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="078a2-261">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="078a2-262">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="078a2-262">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="078a2-263">Отображение состояния окна.</span><span class="sxs-lookup"><span data-stu-id="078a2-263">Window show state.</span></span> <span data-ttu-id="078a2-264">Это может быть любое из значений, которое можно указать в параметре *нкмдшов* для функции [ShowWindow](/windows/desktop/api/winuser/nf-winuser-showwindow) .</span><span class="sxs-lookup"><span data-stu-id="078a2-264">It can be any of the values that can be specified in the *nCmdShow* parameter for the [ShowWindow](/windows/desktop/api/winuser/nf-winuser-showwindow) function.</span></span>

</dd> <dt>

<span data-ttu-id="078a2-265">**уседефаултеррормоде**</span><span class="sxs-lookup"><span data-stu-id="078a2-265">**UseDefaultErrorMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="078a2-266">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="078a2-266">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="078a2-267">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="078a2-267">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="078a2-268">Если задано **значение true**, используется режим ошибок по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="078a2-268">If **True**, the default error mode is used.</span></span>

</dd> <dt>

<span data-ttu-id="078a2-269">**WindowTitle**</span><span class="sxs-lookup"><span data-stu-id="078a2-269">**WindowTitle**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="078a2-270">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="078a2-270">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="078a2-271">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="078a2-271">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="078a2-272">Заголовок, отображаемый в заголовке процесса.</span><span class="sxs-lookup"><span data-stu-id="078a2-272">Title that appears on the title bar of the process.</span></span> <span data-ttu-id="078a2-273">Это свойство не учитывается для приложений графического пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="078a2-273">This property is ignored for GUI applications.</span></span>

</dd> <dt>

<span data-ttu-id="078a2-274">**WorkingDirectory**</span><span class="sxs-lookup"><span data-stu-id="078a2-274">**WorkingDirectory**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="078a2-275">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="078a2-275">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="078a2-276">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="078a2-276">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="078a2-277">Рабочий каталог для этого процесса.</span><span class="sxs-lookup"><span data-stu-id="078a2-277">Working directory for this process.</span></span>

</dd> <dt>

<span data-ttu-id="078a2-278">**кскурдинате**</span><span class="sxs-lookup"><span data-stu-id="078a2-278">**XCoordinate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="078a2-279">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="078a2-279">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="078a2-280">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="078a2-280">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="078a2-281">Смещение по оси X (в пикселях) от левого края экрана до левого края окна, если создается новое окно.</span><span class="sxs-lookup"><span data-stu-id="078a2-281">X-offset, in pixels, from the left edge of the screen to the left edge of the window, if a new window is created.</span></span>

</dd> <dt>

<span data-ttu-id="078a2-282">**кснумчарактерс**</span><span class="sxs-lookup"><span data-stu-id="078a2-282">**XNumCharacters**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="078a2-283">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="078a2-283">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="078a2-284">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="078a2-284">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="078a2-285">Ширина буфера экрана в символьных столбцах, если создано новое окно консоли.</span><span class="sxs-lookup"><span data-stu-id="078a2-285">Screen buffer width, in character columns, if a new console window is created.</span></span> <span data-ttu-id="078a2-286">Это свойство не учитывается в процессе графического пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="078a2-286">This property is ignored in a GUI process.</span></span>

</dd> <dt>

<span data-ttu-id="078a2-287">**кссизе**</span><span class="sxs-lookup"><span data-stu-id="078a2-287">**XSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="078a2-288">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="078a2-288">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="078a2-289">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="078a2-289">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="078a2-290">Ширина (в пикселях) нового окна, если создается новое окно.</span><span class="sxs-lookup"><span data-stu-id="078a2-290">Width, in pixels, of a new window, if a new window is created.</span></span>

</dd> <dt>

<span data-ttu-id="078a2-291">**икурдинате**</span><span class="sxs-lookup"><span data-stu-id="078a2-291">**YCoordinate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="078a2-292">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="078a2-292">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="078a2-293">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="078a2-293">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="078a2-294">Смещение по оси Y (в пикселях) от верхнего края экрана до верхнего края окна, если создается новое окно.</span><span class="sxs-lookup"><span data-stu-id="078a2-294">Y-offset, in pixels, from the top edge of the screen to the top edge of the window, if a new window is created.</span></span>

</dd> <dt>

<span data-ttu-id="078a2-295">**инумчарактерс**</span><span class="sxs-lookup"><span data-stu-id="078a2-295">**YNumCharacters**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="078a2-296">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="078a2-296">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="078a2-297">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="078a2-297">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="078a2-298">Высота буфера экрана (в строках символов) при создании нового окна консоли.</span><span class="sxs-lookup"><span data-stu-id="078a2-298">Screen buffer height, in character rows, if a new console window is created.</span></span> <span data-ttu-id="078a2-299">Это свойство не учитывается в процессе графического пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="078a2-299">This property is ignored in a GUI process.</span></span>

</dd> <dt>

<span data-ttu-id="078a2-300">**исизе**</span><span class="sxs-lookup"><span data-stu-id="078a2-300">**YSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="078a2-301">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="078a2-301">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="078a2-302">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="078a2-302">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="078a2-303">Высота (в пикселях) нового окна, если создается новое окно.</span><span class="sxs-lookup"><span data-stu-id="078a2-303">Height, in pixels, of the new window, if a new window is created.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="078a2-304">Remarks</span><span class="sxs-lookup"><span data-stu-id="078a2-304">Remarks</span></span>

<span data-ttu-id="078a2-305">Класс **коммандлинивентконсумер** является производным от абстрактного класса [**\_ \_ евентконсумер**](--eventconsumer.md) .</span><span class="sxs-lookup"><span data-stu-id="078a2-305">The **CommandLineEventConsumer** class is derived from the [**\_\_EventConsumer**](--eventconsumer.md) abstract class.</span></span>

<span data-ttu-id="078a2-306">Свойство **креатесепаратевоввдм** указывает, выполняется ли новый процесс в частной ВИРТУАЛЬНОЙ машине DOS (VDM).</span><span class="sxs-lookup"><span data-stu-id="078a2-306">The **CreateSeparateWowVdm** property indicates whether or not the new process runs in a private Virtual DOS Machine (VDM).</span></span> <span data-ttu-id="078a2-307">Преимущество выполнения по отдельности заключается в том, что сбой завершается только для одного VDM.</span><span class="sxs-lookup"><span data-stu-id="078a2-307">The advantage of running separately is that a crash only terminates the single VDM.</span></span> <span data-ttu-id="078a2-308">Программы, работающие в разных ВДМС, продолжают работать в обычном режиме, а 16-разрядные приложения Windows, работающие в разных ВДМС, имеют отдельные входные очереди.</span><span class="sxs-lookup"><span data-stu-id="078a2-308">Programs running in distinct VDMs continue to function normally, and the 16-bit Windows-based applications running in separate VDMs have separate input queues.</span></span> <span data-ttu-id="078a2-309">Это означает, что если одно приложение мгновенно перестает отвечать на запросы, приложения в разных ВДМС продолжают принимать входные данные.</span><span class="sxs-lookup"><span data-stu-id="078a2-309">This means that if one application stops responding momentarily, the applications in separate VDMs continue to receive input.</span></span> <span data-ttu-id="078a2-310">Недостатком выполнения по отдельности является то, что для этого требуется значительно больше памяти.</span><span class="sxs-lookup"><span data-stu-id="078a2-310">The disadvantage of running separately is that it takes significantly more memory to do so.</span></span> <span data-ttu-id="078a2-311">Этому свойству следует присвоить **значение true** , только если пользователь запрашивает выполнение 16-разрядных приложений Windows в своем собственном VDM.</span><span class="sxs-lookup"><span data-stu-id="078a2-311">You should set this property to **True** only if the user requests that 16-bit Windows-based applications run in their own VDM.</span></span>

> [!Note]  
> <span data-ttu-id="078a2-312">**Коммандлинивентконсумер** использует метод [**CreateProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa) для внутренних целей и передает свойства **ExecutablePath** и **коммандлинетемплате** в качестве параметров *лпаппликатионнаме* и *лпкоммандлине* .</span><span class="sxs-lookup"><span data-stu-id="078a2-312">The **CommandLineEventConsumer** uses the [**CreateProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa) method internally, and passes the **ExecutablePath** and **CommandLineTemplate** properties as the *lpApplicationName* and *lpCommandLine* parameters.</span></span> <span data-ttu-id="078a2-313">Следующий пример кода MOF-файл (MOF) не использует **коммандлинивентконсумер** правильно.</span><span class="sxs-lookup"><span data-stu-id="078a2-313">The following Managed Object Format (MOF) code example does not use **CommandLineEventConsumer** correctly.</span></span>

 


```mof
instance of CommandLineEventConsumer
{
  ExecutablePath = "C:\\windows\\system32\\cscript.exe";
  CommandLineTemplate = "C:\\scripts\\MyScript.js param1 param2";
};
```



<span data-ttu-id="078a2-314">Метод [**CreateProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa) передает *лпкоммандлине* как `argv[0]` , `argv[1]` и т. д.</span><span class="sxs-lookup"><span data-stu-id="078a2-314">The [**CreateProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa) method passes *lpCommandLine* as `argv[0]`, `argv[1]`, and so on.</span></span> <span data-ttu-id="078a2-315">Так как `argv[0]` для 16-разрядных приложений используется резервное имя исполняемого файла, предыдущий код MOF создает процесс, как будто в командной строке введена следующая команда: **c: \\ Windows \\ system32 \\cscript.exe Param1 Param2**.</span><span class="sxs-lookup"><span data-stu-id="078a2-315">Because `argv[0]` for 16-bit applications used to be reserved for the executable file name, the previous MOF code results in the process being created as though the following command is entered at the command prompt: **c:\\windows\\system32\\cscript.exe param1 param2**.</span></span>

<span data-ttu-id="078a2-316">Предыдущая команда не выполнена, так как Cscript.exe не просматривает `argv[0]` , и поэтому не распознает, что он не содержит собственное имя, но что-то другое ("c: \\ \\ Scripts \\ \\MyScript.js").</span><span class="sxs-lookup"><span data-stu-id="078a2-316">The previous command does not succeed because Cscript.exe does not look at `argv[0]`, and so it does not recognize that it does not contain its own name, but something else ("c:\\\\scripts\\\\MyScript.js").</span></span> <span data-ttu-id="078a2-317">В следующем примере определяется рекомендуемое использование **коммандлинивентконсумер**.</span><span class="sxs-lookup"><span data-stu-id="078a2-317">The following example identifies the recommended use of **CommandLineEventConsumer**.</span></span>


```mof
instance of CommandLineEventConsumer
{
  ExecutablePath = "C:\\windows\\system32\\cscript.exe";
  CommandLineTemplate = "C:\\windows\\system32\\cscript.exe"
    "C:\\scripts\\MyScript.js param1 param2";
};
```



<span data-ttu-id="078a2-318">Предыдущее использование **коммандлинивентконсумер** приводит к созданию процесса, как будто в командной строке введена следующая команда: **c: \\ Windows \\ system32 \\cscript.exe c: \\ Scripts \\MyScript.js Param1 Param2**</span><span class="sxs-lookup"><span data-stu-id="078a2-318">The previous use of **CommandLineEventConsumer** results in the process created as though the following command was entered at the command prompt: **c:\\windows\\system32\\cscript.exe c:\\scripts\\MyScript.js param1 param2**</span></span>

<span data-ttu-id="078a2-319">Так как "c: \\ \\ scripts \\ \\MyScript.js" сейчас `argv[1]` , он отображается Cscript.exe и команда выполнена.</span><span class="sxs-lookup"><span data-stu-id="078a2-319">Because "c:\\\\scripts\\\\MyScript.js" is now `argv[1]`, it is seen by Cscript.exe and the command succeeds.</span></span>

<span data-ttu-id="078a2-320">Дополнительные сведения см. в описании функции [**CreateProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa) .</span><span class="sxs-lookup"><span data-stu-id="078a2-320">For more information, see the [**CreateProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa) function.</span></span>

## <a name="examples"></a><span data-ttu-id="078a2-321">Примеры</span><span class="sxs-lookup"><span data-stu-id="078a2-321">Examples</span></span>

<span data-ttu-id="078a2-322">Пример использования **коммандлинивентконсумер** для создания потребителя см. в разделе [Запуск программы из командной строки на основе события](running-a-program-from-the-command-line-based-on-an-event.md).</span><span class="sxs-lookup"><span data-stu-id="078a2-322">For an example of using **CommandLineEventConsumer** to create a consumer, see [Running a Program from the Command Line Based on an Event](running-a-program-from-the-command-line-based-on-an-event.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="078a2-323">Требования</span><span class="sxs-lookup"><span data-stu-id="078a2-323">Requirements</span></span>



| <span data-ttu-id="078a2-324">Требование</span><span class="sxs-lookup"><span data-stu-id="078a2-324">Requirement</span></span> | <span data-ttu-id="078a2-325">Значение</span><span class="sxs-lookup"><span data-stu-id="078a2-325">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="078a2-326">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="078a2-326">Minimum supported client</span></span><br/> | <span data-ttu-id="078a2-327">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="078a2-327">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="078a2-328">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="078a2-328">Minimum supported server</span></span><br/> | <span data-ttu-id="078a2-329">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="078a2-329">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="078a2-330">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="078a2-330">Namespace</span></span><br/>                | <span data-ttu-id="078a2-331">Корневая \\ Подписка</span><span class="sxs-lookup"><span data-stu-id="078a2-331">Root\\subscription</span></span><br/>                                                           |
| <span data-ttu-id="078a2-332">MOF</span><span class="sxs-lookup"><span data-stu-id="078a2-332">MOF</span></span><br/>                      | <dl> <span data-ttu-id="078a2-333"><dt>Вбемконс. mof</dt></span><span class="sxs-lookup"><span data-stu-id="078a2-333"><dt>Wbemcons.mof</dt></span></span> </dl> |
| <span data-ttu-id="078a2-334">DLL</span><span class="sxs-lookup"><span data-stu-id="078a2-334">DLL</span></span><br/>                      | <dl> <span data-ttu-id="078a2-335"><dt>Wbemcons.dll</dt></span><span class="sxs-lookup"><span data-stu-id="078a2-335"><dt>Wbemcons.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="078a2-336">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="078a2-336">See also</span></span>

<dl> <dt>

[<span data-ttu-id="078a2-337">Классы стандартных потребителей</span><span class="sxs-lookup"><span data-stu-id="078a2-337">Standard Consumer Classes</span></span>](standard-consumer-classes.md)
</dt> <dt>

[<span data-ttu-id="078a2-338">Мониторинг событий и реагирование на них с помощью стандартных потребителей</span><span class="sxs-lookup"><span data-stu-id="078a2-338">Monitoring and Responding to Events with Standard Consumers</span></span>](monitoring-and-responding-to-events-with-standard-consumers.md)
</dt> <dt>

[<span data-ttu-id="078a2-339">Создание логического потребителя</span><span class="sxs-lookup"><span data-stu-id="078a2-339">Creating a Logical Consumer</span></span>](creating-a-logical-consumer.md)
</dt> <dt>

[<span data-ttu-id="078a2-340">Получение событий в любое время</span><span class="sxs-lookup"><span data-stu-id="078a2-340">Receiving Events At All Times</span></span>](receiving-events-at-all-times.md)
</dt> <dt>

[<span data-ttu-id="078a2-341">**\_\_евентконсумер**</span><span class="sxs-lookup"><span data-stu-id="078a2-341">**\_\_EventConsumer**</span></span>](--eventconsumer.md)
</dt> </dl>

 

