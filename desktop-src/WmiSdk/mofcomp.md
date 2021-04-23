---
description: Компилятор MOF-файл (MOF) анализирует файл, содержащий инструкции MOF, и добавляет классы и экземпляры классов, определенные в файле, в репозиторий WMI.
ms.assetid: 9858da09-fb91-43a4-9817-83b10e2ee08f
ms.tgt_platform: multiple
title: mofcomp
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: da63525e4bb8a32f3628b68295e5cc8ade0b08de
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103898093"
---
# <a name="mofcomp"></a><span data-ttu-id="55a3a-103">mofcomp</span><span class="sxs-lookup"><span data-stu-id="55a3a-103">mofcomp</span></span>

<span data-ttu-id="55a3a-104">Компилятор [*MOF-файл (MOF)*](gloss-m.md) анализирует файл, СОДЕРЖАЩИЙ инструкции MOF, и добавляет классы и экземпляры классов, определенные в файле, в репозиторий WMI.</span><span class="sxs-lookup"><span data-stu-id="55a3a-104">The [*Managed Object Format (MOF)*](gloss-m.md) compiler parses a file containing MOF statements and adds the classes and class instances defined in the file to the WMI repository.</span></span> <span data-ttu-id="55a3a-105">MOF-файлы обычно автоматически компилируются во время установки систем, с которыми они предоставляются, но можно также компилировать MOF-файлы с помощью этого средства.</span><span class="sxs-lookup"><span data-stu-id="55a3a-105">MOF files are usually automatically compiled during the installation of the systems with which they are provided, but you can also compile MOF files by using this tool.</span></span>

<span data-ttu-id="55a3a-106">Дополнительные сведения о поиске и использовании mofcomp.exe см. [в разделе Использование средств управления WMI](/previous-versions/system-center/configuration-manager-2003/cc180468(v=technet.10)).</span><span class="sxs-lookup"><span data-stu-id="55a3a-106">For more information about locating and using mofcomp.exe, see [Using WMI Management Tools](/previous-versions/system-center/configuration-manager-2003/cc180468(v=technet.10)).</span></span> <span data-ttu-id="55a3a-107">Сведения об удалении классов и экземпляров из репозитория WMI см. в описании команды препроцессора [**pragma делетекласс**](pragma-deleteclass.md) .</span><span class="sxs-lookup"><span data-stu-id="55a3a-107">For information about removing classes and instances from the WMI repository, see the [**pragma deleteclass**](pragma-deleteclass.md) preprocessor command.</span></span>

<span data-ttu-id="55a3a-108">В следующем примере кода показано, как запустить компилятор MOF для файла.</span><span class="sxs-lookup"><span data-stu-id="55a3a-108">The following code example shows how to run the MOF compiler on a file.</span></span>

``` syntax
mofcomp
  [-autorecover]
  [-check]
  [-N:<namespacepath>]
  [-class:createonly | -class:forceupdate | 
   -class:safeupdate | -class:updateonly ] 
  [-instance:updateonly | -instance:createonly]
  [-B:<filename>]
  [-WMI]
  [-P:<Password>]
  [-U:<UserName>]
  [-A:<Authority>]
  [-MOF:<path>] 
  [-MFL:<path>] 
  [-AMENDMENT:<Locale>]
  [-ER:<ResourceName>]
  [-L:<ResourceLocale>] 
  <MOFfile>
```

## <a name="switches"></a><span data-ttu-id="55a3a-109">коммутаторы;</span><span class="sxs-lookup"><span data-stu-id="55a3a-109">Switches</span></span>

<dl> <dt>

<span data-ttu-id="55a3a-110"><span id="-autorecover"></span><span id="-AUTORECOVER"></span>**— автовосстановление**</span><span class="sxs-lookup"><span data-stu-id="55a3a-110"><span id="-autorecover"></span><span id="-AUTORECOVER"></span>**-autorecover**</span></span>
</dt> <dd>

<span data-ttu-id="55a3a-111">Добавляет именованный MOF-файл в список файлов, скомпилированных во время восстановления репозитория.</span><span class="sxs-lookup"><span data-stu-id="55a3a-111">Adds the named MOF file to the list of files compiled during repository recovery.</span></span> <span data-ttu-id="55a3a-112">Список MOF-файлов для автовосстановления хранится в разделе реестра:</span><span class="sxs-lookup"><span data-stu-id="55a3a-112">The list of autorecover MOF files is stored in the registry key:</span></span>

<span data-ttu-id="55a3a-113">**HKey \_ \_** \\ **Программное обеспечение** \\ **Microsoft** \\ **WBEM** \\ **CIMOM \\** для локального компьютера</span><span class="sxs-lookup"><span data-stu-id="55a3a-113">**HKEY\_LOCAL\_MACHINE**\\**SOFTWARE**\\**Microsoft**\\**WBEM**\\**CIMOM\\**</span></span>

<span data-ttu-id="55a3a-114">MOF-файлы, перечисленные в этой записи реестра, должны находиться на локальном компьютере, так как файлы MOF, использующие команду **автовосстановления** , не могут восстанавливать MOF-файлы, расположенные на удаленном компьютере.</span><span class="sxs-lookup"><span data-stu-id="55a3a-114">The MOF files listed in this registry entry must reside on the local computer because MOF files that use the **autorecover** command cannot recover MOF files located on a remote computer.</span></span>

> [!Note]  
> <span data-ttu-id="55a3a-115">Чтобы гарантировать, что все определения классов WMI для управляемых объектов будут восстановлены в [*репозитории WMI*](gloss-w.md) в случае сбоя и перезапуска WMI, используйте инструкцию препроцессора [**\# pragma автовосстановления**](pragma-autorecover.md) в файле [*MOF-файл*](gloss-m.md) (MOF).</span><span class="sxs-lookup"><span data-stu-id="55a3a-115">To ensure that all your WMI class definitions for managed objects are restored to the [*WMI repository*](gloss-w.md) if WMI has a failure and restarts, use the [**\#pragma autorecover**](pragma-autorecover.md) preprocessor instruction in your [*Managed Object Format*](gloss-m.md) (MOF) file.</span></span>

 

</dd> <dt>

<span data-ttu-id="55a3a-116"><span id="-check"></span><span id="-CHECK"></span>**— Проверка**</span><span class="sxs-lookup"><span data-stu-id="55a3a-116"><span id="-check"></span><span id="-CHECK"></span>**-check**</span></span>
</dt> <dd>

<span data-ttu-id="55a3a-117">Запрашивает выполнение компилятором только проверки синтаксиса и вывод соответствующих сообщений об ошибках.</span><span class="sxs-lookup"><span data-stu-id="55a3a-117">Requests that the compiler perform a syntax check only and print appropriate error messages.</span></span> <span data-ttu-id="55a3a-118">С этим параметром нельзя использовать другие коммутаторы.</span><span class="sxs-lookup"><span data-stu-id="55a3a-118">No other switch can be used with this switch.</span></span> <span data-ttu-id="55a3a-119">При использовании этого параметра подключение к инструментарий управления Windows (WMI) (WMI) не устанавливается и изменения в репозитории WMI не вносятся.</span><span class="sxs-lookup"><span data-stu-id="55a3a-119">When this switch is used, no connection to Windows Management Instrumentation (WMI) is established and no modifications to the WMI repository are made.</span></span>

</dd> <dt>

<span data-ttu-id="55a3a-120"><span id="-N__namespacepath_"></span><span id="-n__namespacepath_"></span><span id="-N__NAMESPACEPATH_"></span>**-N: <** _намеспацепас_*_>_*</span><span class="sxs-lookup"><span data-stu-id="55a3a-120"><span id="-N__namespacepath_"></span><span id="-n__namespacepath_"></span><span id="-N__NAMESPACEPATH_"></span>**-N:<**_namespacepath_*_>_*</span></span>
</dt> <dd><span data-ttu-id="55a3a-121">Запрашивает загрузку MOF-файла компилятором в пространство имен, указанное как *намеспацепас*.</span><span class="sxs-lookup"><span data-stu-id="55a3a-121">Requests that the compiler load the MOF file into the namespace specified as *namespacepath*.</span></span> <span data-ttu-id="55a3a-122">Скомпилированный MOF-файл загружается в пространство имен mofcomp по умолчанию, корневое \\ по умолчанию, если этот параметр не используется.</span><span class="sxs-lookup"><span data-stu-id="55a3a-122">The compiled MOF is loaded into the default Mofcomp namespace, root\\default, unless this switch is used.</span></span> <span data-ttu-id="55a3a-123">Можно также вставить **\# пространство имен директивы pragma** для команды препроцессора ("_путь к пространству имен_*_")_* в MOF-файл, чтобы добиться того же результата.</span><span class="sxs-lookup"><span data-stu-id="55a3a-123">You can also insert the preprocessor command **\#pragma namespace ("**_namespace path_*_")_* in the MOF file to achieve the same effect.</span></span> <span data-ttu-id="55a3a-124">Если используются как параметр **-N:** Switch, так и \# команда <a href="pragma-namespace.md">pragma Namespace</a> , то \# **директива pragma Namespace**  имеет приоритет.</span><span class="sxs-lookup"><span data-stu-id="55a3a-124">If both the **-N:** switch and the \#<a href="pragma-namespace.md">pragma namespace</a> command are used, \#**pragma namespace** **autorecover** takes priority.</span></span> <span data-ttu-id="55a3a-125">В этом случае единственным способом компиляции MOF в другое пространство имен является редактирование MOF-файла и изменение \# команды **pragma Namespace** .</span><span class="sxs-lookup"><span data-stu-id="55a3a-125">In this case, the only way to compile the MOF into another namespace is to edit the MOF file and change the \#**pragma namespace** command.</span></span> <span data-ttu-id="55a3a-126">Удаленный компьютер можно указать с помощью \\ \\ \\ корневого корня \\ по умолчанию MachineName.</span><span class="sxs-lookup"><span data-stu-id="55a3a-126">A remote computer can be specified using \\\\machinename\\root\\default.</span></span></dd> <dt>

<span data-ttu-id="55a3a-127"><span id="-class_createonly"></span><span id="-CLASS_CREATEONLY"></span>**-Class: креатеонли**</span><span class="sxs-lookup"><span data-stu-id="55a3a-127"><span id="-class_createonly"></span><span id="-CLASS_CREATEONLY"></span>**-class:createonly**</span></span>
</dt> <dd>

<span data-ttu-id="55a3a-128">Запрашивает, что компилятор не вносит изменения в существующие классы.</span><span class="sxs-lookup"><span data-stu-id="55a3a-128">Requests that the compiler not make any changes to existing classes.</span></span> <span data-ttu-id="55a3a-129">Если используется этот параметр, операция компиляции завершается, если класс, указанный в MOF-файле, уже существует.</span><span class="sxs-lookup"><span data-stu-id="55a3a-129">When this switch is used, the compile operation terminates if a class specified in the MOF file already exists.</span></span>

</dd> <dt>

<span data-ttu-id="55a3a-130"><span id="-class_forceupdate"></span><span id="-CLASS_FORCEUPDATE"></span>**-Class: форцеупдате**</span><span class="sxs-lookup"><span data-stu-id="55a3a-130"><span id="-class_forceupdate"></span><span id="-CLASS_FORCEUPDATE"></span>**-class:forceupdate**</span></span>
</dt> <dd>

<span data-ttu-id="55a3a-131">Принудительно обновляет классы при наличии конфликтующих дочерних классов.</span><span class="sxs-lookup"><span data-stu-id="55a3a-131">Forces updates of classes when conflicting child classes exist.</span></span> <span data-ttu-id="55a3a-132">Например, предположим, что квалификатор класса определен в дочернем классе, а базовый класс пытается добавить тот же квалификатор.</span><span class="sxs-lookup"><span data-stu-id="55a3a-132">For example, suppose a class qualifier is defined in a child class and the base class tries to add the same qualifier.</span></span> <span data-ttu-id="55a3a-133">В режиме **форцеупдате:** компилятор MOF разрешает этот конфликт, удаляя конфликтующий квалификатор в дочернем классе.</span><span class="sxs-lookup"><span data-stu-id="55a3a-133">In **-class:forceupdate** mode, the MOF compiler resolves this conflict by deleting the conflicting qualifier in the child class.</span></span> <span data-ttu-id="55a3a-134">Если дочерний класс имеет экземпляры, принудительное обновление завершается сбоем.</span><span class="sxs-lookup"><span data-stu-id="55a3a-134">If the child class has instances, the forced update fails.</span></span>

</dd> <dt>

<span data-ttu-id="55a3a-135"><span id="-class_safeupdate"></span><span id="-CLASS_SAFEUPDATE"></span>**-Class: сафеупдате**</span><span class="sxs-lookup"><span data-stu-id="55a3a-135"><span id="-class_safeupdate"></span><span id="-CLASS_SAFEUPDATE"></span>**-class:safeupdate**</span></span>
</dt> <dd>

<span data-ttu-id="55a3a-136">Позволяет обновлять классы даже при наличии дочерних классов, если изменение не вызывает конфликты с дочерними классами.</span><span class="sxs-lookup"><span data-stu-id="55a3a-136">Allows updates of classes even if there are child classes, as long as the change does not cause conflicts with child classes.</span></span> <span data-ttu-id="55a3a-137">Например, этот флаг позволяет добавить новое свойство в базовый класс, который ранее не упоминался в дочерних классах.</span><span class="sxs-lookup"><span data-stu-id="55a3a-137">For example, this flag allows adding a new property to the base class that was not previously mentioned in child classes.</span></span> <span data-ttu-id="55a3a-138">Если дочерние классы имеют экземпляры, обновление завершается ошибкой.</span><span class="sxs-lookup"><span data-stu-id="55a3a-138">If the child classes have instances, the update fails.</span></span>

</dd> <dt>

<span data-ttu-id="55a3a-139"><span id="-class_updateonly"></span><span id="-CLASS_UPDATEONLY"></span>**-Class: упдатеонли**</span><span class="sxs-lookup"><span data-stu-id="55a3a-139"><span id="-class_updateonly"></span><span id="-CLASS_UPDATEONLY"></span>**-class:updateonly**</span></span>
</dt> <dd>

<span data-ttu-id="55a3a-140">Запрашивает, что компилятор не создает никаких новых классов.</span><span class="sxs-lookup"><span data-stu-id="55a3a-140">Requests that the compiler not create any new classes.</span></span> <span data-ttu-id="55a3a-141">Если используется этот параметр, операция компиляции завершается, если класс, указанный в MOF-файле, не существует.</span><span class="sxs-lookup"><span data-stu-id="55a3a-141">When this switch is used, the compile operation terminates if a class specified in the MOF file does not exist.</span></span>

</dd> <dt>

<span data-ttu-id="55a3a-142"><span id="-instance_updateonly"></span><span id="-INSTANCE_UPDATEONLY"></span>**-instance: упдатеонли**</span><span class="sxs-lookup"><span data-stu-id="55a3a-142"><span id="-instance_updateonly"></span><span id="-INSTANCE_UPDATEONLY"></span>**-instance:updateonly**</span></span>
</dt> <dd>

<span data-ttu-id="55a3a-143">Запрашивает, что компилятор не создает никаких новых экземпляров.</span><span class="sxs-lookup"><span data-stu-id="55a3a-143">Requests that the compiler not create any new instances.</span></span> <span data-ttu-id="55a3a-144">При использовании этого параметра операция компиляции завершается, если экземпляр, указанный в MOF-файле, не существует.</span><span class="sxs-lookup"><span data-stu-id="55a3a-144">When this switch is used, the compile operation terminates if an instance specified in the MOF file does not exist.</span></span>

</dd> <dt>

<span data-ttu-id="55a3a-145"><span id="-instance_createonly"></span><span id="-INSTANCE_CREATEONLY"></span>**-instance: креатеонли**</span><span class="sxs-lookup"><span data-stu-id="55a3a-145"><span id="-instance_createonly"></span><span id="-INSTANCE_CREATEONLY"></span>**-instance:createonly**</span></span>
</dt> <dd>

<span data-ttu-id="55a3a-146">Запрашивает, что компилятор не вносит изменения в существующие экземпляры.</span><span class="sxs-lookup"><span data-stu-id="55a3a-146">Requests that the compiler not make any changes to existing instances.</span></span> <span data-ttu-id="55a3a-147">При использовании этого параметра операция компиляции завершается, если экземпляр, указанный в MOF-файле, уже существует.</span><span class="sxs-lookup"><span data-stu-id="55a3a-147">When this switch is used, the compile operation terminates if an instance specified in the MOF file already exists.</span></span>

</dd> <dt>

<span data-ttu-id="55a3a-148"><span id="-B__filename_"></span><span id="-b__filename_"></span><span id="-B__FILENAME_"></span>**-B: <** _имя файла_*_>_*</span><span class="sxs-lookup"><span data-stu-id="55a3a-148"><span id="-B__filename_"></span><span id="-b__filename_"></span><span id="-B__FILENAME_"></span>**-B:<**_filename_*_>_*</span></span>
</dt> <dd>

<span data-ttu-id="55a3a-149">Запрашивает создание компилятором двоичной версии MOF-файла с именем *filename* без внесения изменений в репозиторий WMI.</span><span class="sxs-lookup"><span data-stu-id="55a3a-149">Requests that the compiler create a binary version of the MOF file with the name *filename* without making any modifications to the WMI repository.</span></span>

<span data-ttu-id="55a3a-150">Если для создания двоичного файла MOF используется параметр **-B: <** _filename_ *_>_* , в репозитории WMI будут храниться только флаги квалификаторов по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="55a3a-150">If you use the **-B:<**_filename_*_>_* option to create a binary MOF file, only default qualifier flavors are stored in the WMI repository.</span></span>

<span data-ttu-id="55a3a-151">Двоичный формат MOF — это промежуточный формат для объединения драйвера WDM с MOF в качестве ресурса.</span><span class="sxs-lookup"><span data-stu-id="55a3a-151">Binary MOF format is the intermediate format for combining a WDM-driver with the MOF as a resource.</span></span> <span data-ttu-id="55a3a-152">Двоичный MOF представляет классы и экземпляры так же, как и текстовый MOF-файл, и сжимается перед сохранением на диске.</span><span class="sxs-lookup"><span data-stu-id="55a3a-152">The binary MOF represents classes and instances just as a text MOF file does and is compressed before it is stored on disk.</span></span>

</dd> <dt>

<span data-ttu-id="55a3a-153"><span id="-WMI"></span><span id="-wmi"></span>**— Инструментарий WMI**</span><span class="sxs-lookup"><span data-stu-id="55a3a-153"><span id="-WMI"></span><span id="-wmi"></span>**-WMI**</span></span>
</dt> <dd>

<span data-ttu-id="55a3a-154">Запрашивает выполнение компилятором проверки синтаксиса WMI.</span><span class="sxs-lookup"><span data-stu-id="55a3a-154">Requests that the compiler perform a WMI syntax check.</span></span> <span data-ttu-id="55a3a-155">Параметр **-B:** должен использоваться с этим параметром.</span><span class="sxs-lookup"><span data-stu-id="55a3a-155">The **-B:** switch must be used with this switch.</span></span> <span data-ttu-id="55a3a-156">Параметр **-WMI** используется только для создания двоичных файлов MOF для использования драйверами устройств WDM.</span><span class="sxs-lookup"><span data-stu-id="55a3a-156">The **-WMI** switch is only used for building binary MOF files for use by WDM device drivers.</span></span> <span data-ttu-id="55a3a-157">Этот параметр вызывает отдельное средство проверки двоичных файлов MOF, которое запускается после создания двоичного MOF-файла.</span><span class="sxs-lookup"><span data-stu-id="55a3a-157">This switch invokes a separate binary MOF file checker, which runs after the binary MOF file is created.</span></span>

</dd> <dt>

<span data-ttu-id="55a3a-158"><span id="-P__Password_"></span><span id="-p__password_"></span><span id="-P__PASSWORD_"></span>**-P: <** _пароль_*_>_*</span><span class="sxs-lookup"><span data-stu-id="55a3a-158"><span id="-P__Password_"></span><span id="-p__password_"></span><span id="-P__PASSWORD_"></span>**-P:<**_Password_*_>_*</span></span>
</dt> <dd>

<span data-ttu-id="55a3a-159">Указывает *пароль* для входа пользователя компьютера при входе в систему.</span><span class="sxs-lookup"><span data-stu-id="55a3a-159">Specifies *Password* as the password for the computer user to enter when logging on.</span></span>

</dd> <dt>

<span data-ttu-id="55a3a-160"><span id="-U__UserName_"></span><span id="-u__username_"></span><span id="-U__USERNAME_"></span>**-U: <** _имя пользователя_*_>_*</span><span class="sxs-lookup"><span data-stu-id="55a3a-160"><span id="-U__UserName_"></span><span id="-u__username_"></span><span id="-U__USERNAME_"></span>**-U:<**_UserName_*_>_*</span></span>
</dt> <dd>

<span data-ttu-id="55a3a-161">Указывает имя *пользователя* в качестве имени входа пользователя.</span><span class="sxs-lookup"><span data-stu-id="55a3a-161">Specifies *UserName* as the name of the user logging on.</span></span>

</dd> <dt>

<span data-ttu-id="55a3a-162"><span id="-A__Authority_"></span><span id="-a__authority_"></span><span id="-A__AUTHORITY_"></span>**-A:** _центр_ <*_>_*</span><span class="sxs-lookup"><span data-stu-id="55a3a-162"><span id="-A__Authority_"></span><span id="-a__authority_"></span><span id="-A__AUTHORITY_"></span>**-A:<**_Authority_*_>_*</span></span>
</dt> <dd>

<span data-ttu-id="55a3a-163">Указывает *центр* в качестве центра (доменного имени), используемого для входа в WMI.</span><span class="sxs-lookup"><span data-stu-id="55a3a-163">Specifies *Authority* as the authority (domain name) to use when logging on to WMI.</span></span>

</dd> <dt>

<span data-ttu-id="55a3a-164"><span id="-MOF__path_"></span><span id="-mof__path_"></span><span id="-MOF__PATH_"></span>**-MOF: <** _путь_*_>_*</span><span class="sxs-lookup"><span data-stu-id="55a3a-164"><span id="-MOF__path_"></span><span id="-mof__path_"></span><span id="-MOF__PATH_"></span>**-MOF:<**_path_*_>_*</span></span>
</dt> <dd>

<span data-ttu-id="55a3a-165">Имя выхода, не зависящего от языка.</span><span class="sxs-lookup"><span data-stu-id="55a3a-165">Name of the language neutral output.</span></span> <span data-ttu-id="55a3a-166">Используется с параметром **-** Renames, чтобы указать имя файла MOF, не зависящего от языка, который будет создан.</span><span class="sxs-lookup"><span data-stu-id="55a3a-166">Used with the **-AMENDMENT** switch to specify the name of the language-neutral MOF file that will be generated.</span></span>

</dd> <dt>

<span data-ttu-id="55a3a-167"><span id="-MFL__path_"></span><span id="-mfl__path_"></span><span id="-MFL__PATH_"></span>**-МФЛ: <** _путь_*_>_*</span><span class="sxs-lookup"><span data-stu-id="55a3a-167"><span id="-MFL__path_"></span><span id="-mfl__path_"></span><span id="-MFL__PATH_"></span>**-MFL:<**_path_*_>_*</span></span>
</dt> <dd>

<span data-ttu-id="55a3a-168">Имя вывода, зависящего от языка.</span><span class="sxs-lookup"><span data-stu-id="55a3a-168">Name of the language specific output.</span></span> <span data-ttu-id="55a3a-169">Используется с параметром **-** Renames, чтобы указать имя MOF-файла, который будет создан.</span><span class="sxs-lookup"><span data-stu-id="55a3a-169">Used with the **-AMENDMENT** switch to specify the name of the language-specific MOF file that will be generated.</span></span>

</dd> <dt>

<span data-ttu-id="55a3a-170"><span id="-AMENDMENT__Locale_"></span><span id="-amendment__locale_"></span><span id="-AMENDMENT__LOCALE_"></span>-Поправка **: <** _языковой стандарт_*_>_*</span><span class="sxs-lookup"><span data-stu-id="55a3a-170"><span id="-AMENDMENT__Locale_"></span><span id="-amendment__locale_"></span><span id="-AMENDMENT__LOCALE_"></span>**-AMENDMENT:<**_Locale_*_>_*</span></span>
</dt> <dd>

<span data-ttu-id="55a3a-171">Разделяет MOF-файл на зависящие от языка и независимые версии.</span><span class="sxs-lookup"><span data-stu-id="55a3a-171">Splits the MOF file into language-neutral and -specific versions.</span></span> <span data-ttu-id="55a3a-172">Компилятор MOF создает не зависящий от языка форму MOF-файла, в котором удалены все измененные квалификаторы.</span><span class="sxs-lookup"><span data-stu-id="55a3a-172">The MOF compiler creates a language-neutral form of the MOF file that has all amended qualifiers removed.</span></span> <span data-ttu-id="55a3a-173">Локализованная версия MOF-файла также создается с расширением имени файла МФЛ.</span><span class="sxs-lookup"><span data-stu-id="55a3a-173">A localized version of the MOF file is also created with an MFL file name extension.</span></span> <span data-ttu-id="55a3a-174">Параметр *locale* задает имя дочернего пространства имен, содержащего определения локализованных классов.</span><span class="sxs-lookup"><span data-stu-id="55a3a-174">The *Locale* parameter specifies the name of the child namespace that contains the localized class definitions.</span></span> <span data-ttu-id="55a3a-175">Формат параметра *locale* — MS \_ xxx, где XXX — шестнадцатеричное значение LCID Windows.</span><span class="sxs-lookup"><span data-stu-id="55a3a-175">The format of the *Locale* parameter is MS\_xxx where xxx is the hexadecimal value of the Windows LCID.</span></span> <span data-ttu-id="55a3a-176">Например, языковой стандарт американский английский — MS \_ 409.</span><span class="sxs-lookup"><span data-stu-id="55a3a-176">For example, the locale for American English is MS\_409.</span></span>

</dd> <dt>

<span data-ttu-id="55a3a-177"><span id="-ER__ResourceName_"></span><span id="-er__resourcename_"></span><span id="-ER__RESOURCENAME_"></span>**-ER <** _resourceName_*_>_*</span><span class="sxs-lookup"><span data-stu-id="55a3a-177"><span id="-ER__ResourceName_"></span><span id="-er__resourcename_"></span><span id="-ER__RESOURCENAME_"></span>**-ER <**_ResourceName_*_>_*</span></span>
</dt> <dd>

<span data-ttu-id="55a3a-178">Извлекает двоичный MOF из именованного ресурса.</span><span class="sxs-lookup"><span data-stu-id="55a3a-178">Extracts binary MOF from a named resource.</span></span> <span data-ttu-id="55a3a-179">Этот параметр получает двоичный MOF-файл из класса в репозитории WMI, а параметр-B создает двоичный формат MOF из MOF-файла.</span><span class="sxs-lookup"><span data-stu-id="55a3a-179">This switch gets the binary MOF from the class in the WMI repository while the -B switch creates the binary MOF format from a MOF file.</span></span>

</dd> <dt>

<span data-ttu-id="55a3a-180"><span id="-L__ResourceLocale_"></span><span id="-l__resourcelocale_"></span><span id="-L__RESOURCELOCALE_"></span>**-L: <** _ресаурцелокале_*_>_*</span><span class="sxs-lookup"><span data-stu-id="55a3a-180"><span id="-L__ResourceLocale_"></span><span id="-l__resourcelocale_"></span><span id="-L__RESOURCELOCALE_"></span>**-L:<**_ResourceLocale_*_>_*</span></span>
</dt> <dd>

<span data-ttu-id="55a3a-181">Необязательный элемент.</span><span class="sxs-lookup"><span data-stu-id="55a3a-181">Optional.</span></span> <span data-ttu-id="55a3a-182">Извлекает локализованные описания MOF из двоичного MOF при использовании с параметром-ER.</span><span class="sxs-lookup"><span data-stu-id="55a3a-182">Extracts the localized MOF descriptions from the binary MOF when used with -ER switch.</span></span>

</dd> <dt>

<span data-ttu-id="55a3a-183"><span id="_MOFfile_"></span><span id="_moffile_"></span><span id="_MOFFILE_"></span>**<**_моффиле_*_>_*</span><span class="sxs-lookup"><span data-stu-id="55a3a-183"><span id="_MOFfile_"></span><span id="_moffile_"></span><span id="_MOFFILE_"></span>**<**_MOFfile_*_>_*</span></span>
</dt> <dd>

<span data-ttu-id="55a3a-184">Имя анализируемого файла.</span><span class="sxs-lookup"><span data-stu-id="55a3a-184">Name of the file to parse.</span></span>

</dd> </dl>

## <a name="return-values"></a><span data-ttu-id="55a3a-185">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="55a3a-185">Return Values</span></span>

<span data-ttu-id="55a3a-186">В качестве первой операции компилятор MOF выполняет проверку синтаксиса MOF-файла.</span><span class="sxs-lookup"><span data-stu-id="55a3a-186">As its first operation, the MOF compiler performs a syntax check on the MOF file.</span></span> <span data-ttu-id="55a3a-187">Если компилятор обнаружит ошибки, он выводит сообщение об ошибке и процесс завершается.</span><span class="sxs-lookup"><span data-stu-id="55a3a-187">If the compiler finds any errors, it prints an error message and the process terminates.</span></span>

<span data-ttu-id="55a3a-188">Компилятор MOF может возвращать следующие значения:</span><span class="sxs-lookup"><span data-stu-id="55a3a-188">The MOF compiler can return the following values:</span></span>

<dl> <dt>

<span data-ttu-id="55a3a-189"><span id="0"></span>0</span><span class="sxs-lookup"><span data-stu-id="55a3a-189"><span id="0"></span>0</span></span>
</dt> <dd>

<span data-ttu-id="55a3a-190">Операция компиляции MOF выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="55a3a-190">MOF compile operation was successful.</span></span>

</dd> <dt>

<span data-ttu-id="55a3a-191"><span id="1"></span>1</span><span class="sxs-lookup"><span data-stu-id="55a3a-191"><span id="1"></span>1</span></span>
</dt> <dd>

<span data-ttu-id="55a3a-192">Компилятору MOF не удалось соединиться с сервером WMI.</span><span class="sxs-lookup"><span data-stu-id="55a3a-192">The MOF compiler could not connect with the WMI server.</span></span> <span data-ttu-id="55a3a-193">Это происходит из-за семантической ошибки, такой как несовместимость с существующим репозиторием WMI, или фактической ошибки, такой как сбой сервера WMI для запуска.</span><span class="sxs-lookup"><span data-stu-id="55a3a-193">This is either because of a semantic error such as an incompatibility with the existing WMI repository or an actual error such as the failure of the WMI server to start.</span></span>

</dd> <dt>

<span data-ttu-id="55a3a-194"><span id="2"></span>2</span><span class="sxs-lookup"><span data-stu-id="55a3a-194"><span id="2"></span>2</span></span>
</dt> <dd>

<span data-ttu-id="55a3a-195">Один или несколько параметров командной строки недопустимы.</span><span class="sxs-lookup"><span data-stu-id="55a3a-195">One or more command-line switches were not valid.</span></span>

</dd> <dt>

<span data-ttu-id="55a3a-196"><span id="3"></span>3-5</span><span class="sxs-lookup"><span data-stu-id="55a3a-196"><span id="3"></span>3</span></span>
</dt> <dd>

<span data-ttu-id="55a3a-197">Произошла синтаксическая ошибка MOF.</span><span class="sxs-lookup"><span data-stu-id="55a3a-197">A MOF syntax error occurred.</span></span>

</dd> </dl>

<span data-ttu-id="55a3a-198">Если MOF-файл проанализирован правильно, но предпринята попытка выполнить операцию, запрещенную параметром командной строки, компилятор возвращает код ошибки, сформированный WMI, а не любой из кодов возврата, перечисленных в списке выше.</span><span class="sxs-lookup"><span data-stu-id="55a3a-198">If the MOF file is parsed correctly, but an attempt is made to perform an operation that is forbidden by a command-line switch, the compiler returns an error code generated by WMI instead of any of the return codes listed in the list preceding.</span></span> <span data-ttu-id="55a3a-199">Например, если указан параметр **-instance: упдатеонли** , то возвращается код ошибки WMI, а файл MOF пытается создать экземпляр.</span><span class="sxs-lookup"><span data-stu-id="55a3a-199">For example, a WMI error code is returned when the **-instance:updateonly** switch is specified and the MOF file attempts to create an instance.</span></span>

<span data-ttu-id="55a3a-200">Если инструкция препроцессора [**\# pragma автовосстановления**](pragma-autorecover.md) отсутствует в файле, возвращается следующее предупреждение:</span><span class="sxs-lookup"><span data-stu-id="55a3a-200">If the [**\#pragma autorecover**](pragma-autorecover.md) preprocessor statement is not in the file, then the following warning is returned:</span></span>

``` syntax
WARNING: FileYourMof.Mof does not contain #PRAGMA AUTORECOVER.
If the WMI repository is rebuilt in the future, the contents of this 
MOF file   will not be included in the new WMI repository.
To include this MOF file when the WMI Repository is automatically 
reconstructed, place the #PRAGMA AUTORECOVER statement on the first 
line of the MOF file.
```

## <a name="remarks"></a><span data-ttu-id="55a3a-201">Комментарии</span><span class="sxs-lookup"><span data-stu-id="55a3a-201">Remarks</span></span>

<span data-ttu-id="55a3a-202">Компилятор MOF доступен в каталоге% WINDIR% \\ system32 \\ WBEM.</span><span class="sxs-lookup"><span data-stu-id="55a3a-202">The MOF Compiler is available in the %Windir%\\System32\\wbem directory.</span></span> <span data-ttu-id="55a3a-203">Необходимо указать MOF-файл в качестве параметра компилятора MOF.</span><span class="sxs-lookup"><span data-stu-id="55a3a-203">You must specify the MOF file as the parameter of the MOF Compiler.</span></span> <span data-ttu-id="55a3a-204">Можно также указать параметр автоматического восстановления, если необходимо автоматически перекомпилировать MOF-файл, если репозиторий CIM когда-либо будет автоматически восстановлен.</span><span class="sxs-lookup"><span data-stu-id="55a3a-204">You can also specify an Autorecover switch if you want the MOF file to be automatically recompiled if the CIM Repository ever has to be automatically recovered.</span></span> <span data-ttu-id="55a3a-205">Для получения дополнительных сведений введите **mofcomp/?**</span><span class="sxs-lookup"><span data-stu-id="55a3a-205">For more information, type **Mofcomp /?**</span></span> <span data-ttu-id="55a3a-206">в командной строке.</span><span class="sxs-lookup"><span data-stu-id="55a3a-206">at the command prompt.</span></span>

<span data-ttu-id="55a3a-207">MOF-файл, использующий набор символов Юникода, содержит подпись в виде первых двух байтов файла.</span><span class="sxs-lookup"><span data-stu-id="55a3a-207">A MOF file that uses the Unicode character set contains a signature as the first two bytes of the file.</span></span> <span data-ttu-id="55a3a-208">Эта подпись имеет значение U + ФФФЕ или U + FEFF в зависимости от порядка байтов в файле.</span><span class="sxs-lookup"><span data-stu-id="55a3a-208">This signature is either U+FFFE or U+FEFF, depending on the byte ordering of the file.</span></span>

<span data-ttu-id="55a3a-209">Если в процессе синтаксического анализа ошибки не возникают, компилятор MOF подключается к серверу WMI, выполняющемуся на локальном компьютере, если не указан параметр **-Check** .</span><span class="sxs-lookup"><span data-stu-id="55a3a-209">When no errors occur in the parsing process, the MOF compiler connects to the WMI server running on the local computer unless the **-check** switch is specified.</span></span> <span data-ttu-id="55a3a-210">Классы и экземпляры, определенные в MOF-файле, добавляются в репозиторий WMI.</span><span class="sxs-lookup"><span data-stu-id="55a3a-210">Classes and instances defined in the MOF file are added to the WMI repository.</span></span>

<span data-ttu-id="55a3a-211">При возникновении ошибки при обновлении репозитория WMI компилятор не предпринимает попытки вернуть репозиторий в состояние до начала обработки.</span><span class="sxs-lookup"><span data-stu-id="55a3a-211">When an error occurs in updating the WMI repository, the compiler makes no attempt to return the repository to its state before the compiler began processing.</span></span>

<span data-ttu-id="55a3a-212">**Windows 8:** При установке поставщика mofcomp рассматривает \[ ключ \] и \[ статические \] Квалификаторы как true, если они есть, независимо от их реальных значений.</span><span class="sxs-lookup"><span data-stu-id="55a3a-212">**Windows 8:** When installing a provider, mofcomp treats the \[Key\] and \[Static\] qualifiers as true if they are present, regardless of their actual values.</span></span> <span data-ttu-id="55a3a-213">Другие квалификаторы обрабатываются как false, если они есть, но не имеют явного значения true.</span><span class="sxs-lookup"><span data-stu-id="55a3a-213">Other qualifiers are treated as false if they are present but not explicitly set to true.</span></span>

## <a name="requirements"></a><span data-ttu-id="55a3a-214">Требования</span><span class="sxs-lookup"><span data-stu-id="55a3a-214">Requirements</span></span>



| <span data-ttu-id="55a3a-215">Требование</span><span class="sxs-lookup"><span data-stu-id="55a3a-215">Requirement</span></span> | <span data-ttu-id="55a3a-216">Значение</span><span class="sxs-lookup"><span data-stu-id="55a3a-216">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="55a3a-217">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="55a3a-217">Minimum supported client</span></span><br/> | <span data-ttu-id="55a3a-218">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="55a3a-218">Windows Vista</span></span><br/>       |
| <span data-ttu-id="55a3a-219">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="55a3a-219">Minimum supported server</span></span><br/> | <span data-ttu-id="55a3a-220">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="55a3a-220">Windows Server 2008</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="55a3a-221">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="55a3a-221">See also</span></span>

<dl> <dt>

[<span data-ttu-id="55a3a-222">**пространство имен pragma**</span><span class="sxs-lookup"><span data-stu-id="55a3a-222">**pragma namespace**</span></span>](pragma-namespace.md)
</dt> <dt>

[<span data-ttu-id="55a3a-223">Компиляция MOF-файлов</span><span class="sxs-lookup"><span data-stu-id="55a3a-223">Compiling MOF Files</span></span>](compiling-mof-files.md)
</dt> <dt>

[<span data-ttu-id="55a3a-224">Компиляция локализованных MOF-файлов</span><span class="sxs-lookup"><span data-stu-id="55a3a-224">Compiling Localized MOF Files</span></span>](compiling-localized-mof-files.md)
</dt> <dt>

[<span data-ttu-id="55a3a-225">Регистрация поставщика</span><span class="sxs-lookup"><span data-stu-id="55a3a-225">Registering a Provider</span></span>](registering-a-provider.md)
</dt> <dt>

[<span data-ttu-id="55a3a-226">**Имофкомпилер:: Компилефиле**</span><span class="sxs-lookup"><span data-stu-id="55a3a-226">**IMOFCompiler::CompileFile**</span></span>](/windows/desktop/api/Wbemcli/nf-wbemcli-imofcompiler-compilefile)
</dt> </dl>

 

